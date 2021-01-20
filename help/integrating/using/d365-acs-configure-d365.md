---
solution: Campaign Standard
product: campaign
title: Campaign 통합을 위해 Microsoft Dynamics 365 구성
description: Adobe Campaign 통합을 위해 Microsoft Dynamics 365를 구성하는 방법을 알아봅니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-ms-dynamics
translation-type: tm+mt
source-git-commit: 3ba3e0db816832ea57c124a9bea1fa82cf068859
workflow-type: tm+mt
source-wordcount: '911'
ht-degree: 1%

---


# Adobe Campaign Standard와의 통합을 위해 Microsoft Dynamics 365 구성

Adobe Campaign Standard와의 크로스 채널 커뮤니케이션에서 Microsoft Dynamics 365 통합을 구성하고 CRM 데이터를 활성화하는 방법을 알아봅니다.

## 개요

Microsoft Dynamics 365와의 Adobe Campaign Standard 통합에 대한 일반 설명은 [이 페이지](../../integrating/using/d365-acs-get-started.md)에 설명되어 있습니다.

통합을 사용하려면 여러 애플리케이션을 구성해야 하지만 이 문서는 Dynamics 365 내에서 필요한 단계에 중점을 둡니다.

## 사전 요구 사항

이 문서에서 사전 통합 설정을 수행하기 전에 이미 프로비저닝되어 조직의 Microsoft Dynamics 365 인스턴스에 대한 관리자 액세스 권한이 있는 것으로 가정합니다.  이러한 문제가 발생하지 않으면 Microsoft 고객 지원 센터에 문의하여 Dynamics 365 프로비저닝을 완료해야 합니다.

스테이징 환경과 프로덕션 환경에 대해 통합을 구성하는 경우 스테이징 및 프로덕션 Dynamics 365 인스턴스 모두에 대해 아래 단계를 수행해야 합니다. 아래 몇 가지 지침은 스테이지 또는 프로덕션 Dynamics 365 인스턴스를 구성할 경우에 따라 약간 달라집니다(예: 프로덕션 인스턴스의 경우 `<stage or prod>`에 대해 &quot;prod&quot;를 선택합니다.)

## 애플리케이션 및 권한 설정

OAuth 액세스 토큰을 사용하면 Microsoft Dynamics 365 인터페이스의 타임라인 보기에 Campaign Standard 경험 이벤트를 게시하기 위해 통합 도구가 웹 API를 통해 Microsoft Dynamics 365 인스턴스와 인증할 수 있습니다.

주요 단계는 다음 비디오에 요약되어 있습니다.

>[!VIDEO](https://video.tv.adobe.com/v/27637)

OAuth 액세스 토큰을 생성하려면 아래 설명된 단계를 따르십시오.

### 새 응용 프로그램 {#register-a-new-app} 등록

1. 관리자 로그인 아래에서 portal.azure.com에 로그인합니다.

1. 왼쪽 메뉴에서 **[!UICONTROL Azure Active Directory]**&#x200B;을 클릭합니다.그런 다음 나타나는 하위 메뉴에서 **[!UICONTROL App registrations]**&#x200B;을 클릭합니다.

1. 화면 상단에 있는 **[!UICONTROL New registration]**&#x200B;을 클릭합니다.

   ![](assets/do-not-localize/MSdynACSIntegration-7.png)

1. 앱 등록 화면을 채웁니다.

   * 이름:adobe campaign `<stage or prod>`
   * 지원되는 계정 유형:**[!UICONTROL Accounts in this organizational directory only]**(기본값)

새 응용 프로그램을 만드는 방법에 대한 자세한 내용은 [이 섹션](https://docs.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app)을 참조하십시오.

>[!NOTE]
>
>Microsoft Azure Directory가 앱에 고유한 응용 프로그램(클라이언트) ID를 할당합니다. 이 ID는 나중에 통합 도구 설정을 수행할 때뿐만 아니라 Dynamics 365 구성에 대해서도 필요합니다.

### 클라이언트 암호 {#generate-a-client-secret} 생성

1. 앱 개요 화면의 왼쪽에 있는 하위 메뉴에서 **[!UICONTROL Certificates and Secrets > New client secret]**

   ![](assets/do-not-localize/MSdynACSIntegration-8.png)

1. 설명을 입력하고 기간을 설정하고 **[!UICONTROL OK]**&#x200B;을 클릭합니다.

이제 클라이언트 암호가 만들어집니다. 통합 도구의 사전 통합 설정이 완료되도록 일시적으로 값을 유지합니다.

>[!CAUTION]
>
>통합 도구 사전 통합 설정을 완료하는 데 필요한 만큼 이 값을 유지합니다. 나중에 검색할 수 없습니다.


### 설정 권한

1. 이 화면 또는 앱 개요 화면에서 왼쪽의 하위 메뉴에서 **[!UICONTROL API permissions]**&#x200B;을 클릭합니다.  **[!UICONTROL Add a permission]**&#x200B;을 클릭한 후 메뉴에서 **[!UICONTROL Dynamics CRM]**&#x200B;을 선택해야 합니다.

   ![](assets/do-not-localize/MSdynACSIntegration-9.png)

1. 그런 다음 **[!UICONTROL user_impersonation]** 상자를 선택하고 **[!UICONTROL Add permissions]** 단추를 클릭합니다.

   ![](assets/do-not-localize/MSdynACSIntegration-10.png)

설정된 권한에 대한 자세한 내용은 [이 섹션](https://docs.microsoft.com/en-us/azure/active-directory/develop/quickstart-configure-app-access-web-apis#add-permissions-to-access-web-apis)을 참조하십시오.

### 앱 사용자 만들기

이 새 사용자는 일반 사용자입니다. 응용 프로그램에서 사용됩니다.API를 사용하는 Microsoft Dynamics 365에 대한 모든 변경 사항은 이 사용자가 수행합니다. 이를 만들려면 아래 단계를 수행하십시오.

1. Dynamics 365 인스턴스로 이동하여 관리자로 로그인합니다.

1. 오른쪽 위 모서리의 톱니바퀴 아이콘을 클릭하고 **[!UICONTROL Advanced Settings]**&#x200B;을 클릭합니다. 위쪽 배너에서 **[!UICONTROL Settings]** 옆의 드롭다운을 클릭하고 **[!UICONTROL Security > Users]**&#x200B;을 클릭합니다.

1. 드롭다운 메뉴를 클릭하여 **[!UICONTROL Application Users]**&#x200B;으로 이동합니다. **[!UICONTROL New]**&#x200B;을(를) 클릭합니다.

1. 사용자 아이콘 옆에 **[!UICONTROL USER:APPLICATION USER]**&#x200B;이(가) 표시되어 있는지 확인합니다.

   새 사용자의 화면을 채웁니다.  매개 변수 제안:

   * **[!UICONTROL User Name]** (이메일):adobe_api_`<stage-or-prod>`@`<your-d365-hostname>`&quot;(예: adobe_api_stage@some-company.crm.dynamics.com)
   * **[!UICONTROL Application ID]**:Azure AD에 등록한 응용 프로그램 ID(필수)
   * **[!UICONTROL Application ID URI]** 및 **[!UICONTROL Azure AD Object ID]**&#x200B;을(를) 비워둘 수 있습니다.
   * **[!UICONTROL Full Name]**:Adobe API  `<stage or prod>`
   * **[!UICONTROL Email]**:( **[!UICONTROL User Name]** 또는 원할 경우 관리자의 이메일과 동일)

   앱 사용자 만들기에 대한 자세한 내용은 [이 섹션](https://docs.microsoft.com/en-gb/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user)을 참조하십시오.

1. 사용자 아이콘을 클릭하고 Adobe Campaign 아이콘을 업로드합니다.새로운 Adobe 이벤트가 Dynamics 365에 표시될 때 [타임라인] 보기에 표시되는 아이콘입니다.

1. 상단 리본에서 **[!UICONTROL MANAGE ROLES]**&#x200B;을 클릭하여 사용자 역할 목록을 엽니다.

1. 아래로 스크롤하고 이 사용자에 대한 **[!UICONTROL System administrator]** 액세스를 선택합니다.

1. **[!UICONTROL OK]**&#x200B;을(를) 클릭합니다.

### 테넌트 ID {#get-the-tenant-id} 가져오기

이 페이지](https://docs.microsoft.com/en-us/onedrive/find-your-office-365-tenant-id)의 지침 [에 따라 테넌트 ID를 찾습니다.  통합 도구에서 사전 통합 설정 중에 이 ID가 필요합니다.

## Microsoft Dynamics 365용 Campaign Standard 설치 {#install-appsource-app}

Dynamics 365 앱을 Campaign Standard 환경에 통합하려면 아래 단계를 따르십시오.

1. 다음 링크로 이동합니다.[https://appsource.microsoft.com/en-us/marketplace/apps](https://appsource.microsoft.com/en-us/marketplace/apps) 검색 막대에서 _Adobe Campaign for Dynamics 365_를 검색하고 검색합니다.
또는 이 [link](https://appsource.microsoft.com/en-us/product/dynamics-365/adobecampaign.re4snj-a4n7-5t6y-a14br-d5d1b?flightCodes=adobesignhide&amp;tab=Overview)로 이동할 수 있습니다.
1. 지침에 따라 Dynamics 365 인스턴스용 앱을 설치합니다.
1. 설치가 완료되면 Dynamics 365 인스턴스로 이동하여 관리자로 로그인합니다.
1. 오른쪽 위 모서리의 톱니바퀴 아이콘을 클릭하고 **[!UICONTROL Advanced Settings]**&#x200B;을 클릭합니다. 위쪽 배너에서 **[!UICONTROL Settings]** 옆의 드롭다운을 클릭하고 **[!UICONTROL Process Center]** 아래의 **[!UICONTROL Processes]**&#x200B;을 클릭합니다.
1. **[!UICONTROL Adobe Campaign Email Bounce]** 작업을 검색하고 클릭합니다.
1. **[!UICONTROL Administration]** 탭에서 상단 리본에서 **[!UICONTROL Actions]**&#x200B;을 클릭하여 이전에 만든 Adobe API 응용 프로그램 사용자로 소유자를 변경한 다음 **[!UICONTROL Assign to another User]** 옵션을 선택하고 드롭다운에서 **[!UICONTROL Adobe API application user]**&#x200B;을 선택하여 할당합니다.
1. 프로세스를 다시 활성화합니다.
1. **[!UICONTROL Adobe Campaign Email Click]** 작업에도 동일하게 수행합니다.

>[!NOTE]
>
>언제든지 이러한 프로세스를 비활성화하려면 이 **[!UICONTROL Processes]** 화면에서 비활성화할 수 있습니다.

**관련 항목**

* [Microsoft Dynamics 365 통합을 위한 Adobe IO 구성](../../integrating/using/d365-acs-configure-adobe-io.md) 은 통합을 설정하는 다음 단계입니다
* [셀프 서비스 통합 앱 시작하기](../../integrating/using/d365-acs-self-service-app-quick-start-guide.md) 에는 통합을 원활하게 시작하는 데 필요한 전체 단계 목록이 포함되어 있습니다.
