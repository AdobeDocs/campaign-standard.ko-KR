---
title: Campaign 통합을 위해 Microsoft Dynamics 365 구성
description: Campaign 통합을 위해 Microsoft Dynamics 365를 구성하는 방법을 알아봅니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-ms-dynamics
feature: Microsoft CRM Integration
old-role: Data Architect
role: Developer
level: Experienced
exl-id: 57e85f8e-65b4-44ea-98e6-0c555acf6dee
source-git-commit: b3f3309a252971dc527d44913b7918abeea704d9
workflow-type: tm+mt
source-wordcount: '880'
ht-degree: 0%

---

# Adobe Campaign Standard과의 통합을 위해 Microsoft Dynamics 365 구성

Adobe Campaign Standard과의 크로스 채널 통신에서 Microsoft Dynamics 365 통합을 구성하고 CRM 데이터를 활성화하는 방법에 대해 알아봅니다.

## 개요

Microsoft Dynamics 365와 Adobe Campaign Standard 통합에 대한 일반적인 설명은 [이 페이지](../../integrating/using/d365-acs-get-started.md)에 설명되어 있습니다.

통합을 활성화하려면 여러 애플리케이션을 구성해야 하지만, 이 문서에서는 Dynamics 365 내에서 필요한 단계에 중점을 둡니다.

## 필수 구성 요소

이 문서에서 사전 통합 설정을 수행하기 전에 사용자가 이미 프로비저닝하고 조직의 Microsoft Dynamics 365 인스턴스에 대한 관리자 액세스 권한을 가지고 있다고 가정합니다.  이 문제가 발생하지 않은 경우 Microsoft 고객 지원 센터에 문의하여 Dynamics 365 프로비저닝을 완료해야 합니다.

스테이징 및 프로덕션 환경 모두에 대한 통합을 구성하는 경우 스테이징 및 프로덕션 Dynamics 365 인스턴스 모두에 대해 아래 단계를 수행해야 합니다. 아래 지침은 단계 또는 프로덕션 Dynamics 365 인스턴스를 구성하는 경우에 따라 약간 달라집니다(예: 프로덕션 인스턴스의 경우 `<stage or prod>`에 대해 &quot;prod&quot;를 선택)

## 애플리케이션 및 권한 설정

OAuth 액세스 토큰을 사용하면 통합 도구가 웹 API를 통해 Microsoft Dynamics 365 인스턴스로 인증하여 Campaign Standard 경험 이벤트를 Microsoft Dynamics 365 인터페이스의 타임라인 보기에 게시할 수 있습니다.

주요 단계는 다음 비디오에 요약되어 있습니다.

>[!VIDEO](https://video.tv.adobe.com/v/27637)

OAuth 액세스 토큰을 생성하려면 아래에 설명된 단계를 수행합니다.

### 새 애플리케이션 등록 {#register-a-new-app}

1. 관리자 로그인에서 [portal.azure.com](https://portal.azure.com){target="_blank"}에 로그인합니다.

1. 왼쪽 메뉴에서 **[!UICONTROL Azure Active Directory]**&#x200B;을(를) 클릭한 다음 표시되는 하위 메뉴에서 **[!UICONTROL App registrations]**&#x200B;을(를) 클릭합니다.

1. 화면 상단의 **[!UICONTROL New registration]**&#x200B;을(를) 클릭합니다.

1. 앱 등록 화면을 채웁니다.

   * 이름: adobe campaign `<stage or prod>`
   * 지원되는 계정 유형: **[!UICONTROL Accounts in this organizational directory only]**(기본값)

새 응용 프로그램을 만드는 방법에 대한 자세한 내용은 [이 섹션](https://docs.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app){target="_blank"}을 참조하세요.

>[!NOTE]
>
>Microsoft Azure Directory는 앱에 고유한 애플리케이션(클라이언트) ID를 할당합니다. 나중에 Dynamics 365를 구성할 때와 통합 도구 설정을 수행할 때 이 ID가 필요합니다.

### 클라이언트 암호 생성 {#generate-a-client-secret}

1. 앱 개요 화면에서 왼쪽의 하위 메뉴에서 **[!UICONTROL Certificates and Secrets > New client secret]**&#x200B;을(를) 클릭합니다.

1. 설명을 입력하고 기간을 설정하고 **[!UICONTROL OK]**&#x200B;을(를) 클릭합니다.

이제 클라이언트 암호가 생성되었습니다. 통합 도구의 통합 전 설정을 완료하기 위해 값을 일시적으로 유지합니다.

>[!CAUTION]
>
>통합 도구 사전 통합 설정을 완료하는 데 필요한 경우 이 값을 유지하십시오. 나중에 검색할 수 없습니다.


### 설정 권한

1. 이 화면 또는 앱 개요 화면에서 왼쪽의 하위 메뉴에 있는 **[!UICONTROL API permissions]**&#x200B;을(를) 클릭합니다.  **[!UICONTROL Add a permission]**&#x200B;을(를) 클릭한 후 메뉴에서 **[!UICONTROL Dynamics CRM]**&#x200B;을(를) 선택해야 합니다.

1. **[!UICONTROL user_impersonation]**&#x200B;에 대한 확인란을 선택하고 **[!UICONTROL Add permissions]** 단추를 클릭합니다.

권한 설정에 대한 자세한 내용은 [이 섹션](https://docs.microsoft.com/en-us/azure/active-directory/develop/quickstart-configure-app-access-web-apis#add-permissions-to-access-web-apis){target="_blank"}을 참조하세요.

### 앱 사용자 만들기

이 새 사용자는 일반 사용자입니다. 애플리케이션에서 사용됩니다. API를 사용하는 Microsoft Dynamics 365에 대한 모든 변경 작업은 이 사용자가 수행합니다. 만들려면 아래 단계를 수행합니다.

1. Dynamics 365 인스턴스로 이동하여 관리자로 로그인합니다.

1. 오른쪽 상단의 톱니바퀴 아이콘을 클릭하고 **[!UICONTROL Advanced Settings]**&#x200B;을(를) 클릭합니다. 상단 배너에서 **[!UICONTROL Settings]** 옆에 있는 드롭다운을 클릭하고 **[!UICONTROL Security > Users]**&#x200B;을(를) 클릭합니다.

1. 드롭다운 메뉴를 클릭하여 **[!UICONTROL Application Users]**(으)로 이동합니다. **[!UICONTROL New]**&#x200B;을(를) 클릭합니다.

1. 사용자 아이콘 옆에 **[!UICONTROL USER:APPLICATION사용자]**&#x200B;이(가) 표시되어 있는지 확인하십시오.

   새 사용자의 화면을 채웁니다.  매개 변수 제안:

   * **[!UICONTROL User Name]**(이메일): adobe_api_`<stage-or-prod>`@`<your-d365-hostname>`&quot;(예: adobe_api_stage@some-company.crm.dynamics.com)
   * **[!UICONTROL Application ID]**: Azure AD에 등록한 응용 프로그램의 ID(필수)
   * 빈 **[!UICONTROL Application ID URI]** 및 **[!UICONTROL Azure AD Object ID]**&#x200B;을(를) 남길 수 있습니다.
   * **[!UICONTROL Full Name]**: Adobe API `<stage or prod>`
   * **[!UICONTROL Email]**: **[!UICONTROL User Name]**&#x200B;과(또는 원하는 경우 관리자의 이메일과) 동일

   앱 사용자 만들기에 대한 자세한 내용은 [이 섹션](https://docs.microsoft.com/en-gb/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user){target="_blank"}을 참조하세요.

1. 사용자 아이콘을 클릭하고 Adobe Campaign 아이콘을 업로드합니다. 이 아이콘은 새 Adobe 이벤트가 Dynamics 365에 나타날 때 타임라인 보기에 표시됩니다.

1. 상단 리본에서 **[!UICONTROL MANAGE ROLES]**&#x200B;을(를) 클릭하여 사용자 역할 목록을 엽니다.

1. 아래로 스크롤하여 이 사용자에 대한 **[!UICONTROL System administrator]** 액세스를 선택하십시오.

1. **[!UICONTROL OK]**&#x200B;을(를) 클릭합니다.

### 테넌트 ID 가져오기 {#get-the-tenant-id}

이 페이지의 [지침](https://docs.microsoft.com/en-us/onedrive/find-your-office-365-tenant-id)에 따라 테넌트 ID를 찾으십시오.  통합 도구에서 통합 전 설정 중에 이 ID가 필요합니다.

## Microsoft Dynamics 365용 Campaign Standard 설치 {#install-appsource-app}

Dynamics 365 앱을 Campaign Standard 환경에 통합하려면 아래 단계를 따르십시오.

1. [Microsoft 비즈니스 앱](https://appsource.microsoft.com/en-us/marketplace/apps)&#x200B;(으)로 이동한 다음 검색 창에서_Adobe Campaign Standard_을(를) 검색합니다.
또는 이 [링크](https://appsource.microsoft.com/en-us/product/dynamics-365/adobe.adobe_campaign_d365?tab=Overview){target="_blank"}(으)로 이동할 수 있습니다.
1. 지침에 따라 Dynamics 365 인스턴스용 앱을 설치하십시오.
1. 설치가 완료되면 Dynamics 365 인스턴스로 이동하여 관리자로 로그인합니다.
1. 오른쪽 상단의 톱니바퀴 아이콘을 클릭하고 **[!UICONTROL Advanced Settings]**&#x200B;을(를) 클릭합니다. 상단 배너에서 **[!UICONTROL Settings]** 옆에 있는 드롭다운을 클릭하고 **[!UICONTROL Processes]**&#x200B;에서 **[!UICONTROL Process Center]**&#x200B;을(를) 클릭합니다.
1. **[!UICONTROL Adobe Campaign Email Bounce]** 작업을 검색하고 클릭합니다.
1. **[!UICONTROL Administration]** 탭에서 맨 위 리본에서 **[!UICONTROL Actions]**&#x200B;을(를) 클릭하여 이전에 만든 Adobe API 응용 프로그램 사용자로 소유자를 변경한 다음 **[!UICONTROL Assign to another User]** 옵션을 선택하고 드롭다운에서 **[!UICONTROL Adobe API application user]**&#x200B;을(를) 선택하여 할당합니다.
1. 프로세스를 다시 활성화합니다.
1. **[!UICONTROL Adobe Campaign Email Click]** 작업에 대해서도 동일한 작업을 수행합니다.

>[!NOTE]
>
>언제든지 이러한 프로세스를 비활성화하려는 경우 이 **[!UICONTROL Processes]** 화면에서 비활성화할 수 있습니다.

**관련 항목**

* [Microsoft Dynamics 365 통합을 위해 Adobe Developer 구성](../../integrating/using/d365-acs-configure-adobe-io.md)은(는) 통합 설정의 다음 단계입니다.
* [셀프 서비스 통합 앱 시작](../../integrating/using/d365-acs-self-service-app-quick-start-guide.md)에는 통합을 시작하고 실행하는 전체 단계 목록이 포함되어 있습니다.
