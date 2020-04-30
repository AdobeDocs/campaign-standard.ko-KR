---
title: Microsoft Dynamics 365 for Campaign 통합 구성
description: Adobe Campaign 통합을 위해 Microsoft Dynamics 365를 구성하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: effa1028-66b2-4bef-b5e4-7319dbb23d5d
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-analytics
discoiquuid: eb3639f5-7246-46c4-8ddb-da9413b40c32
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 4e05dafb087c43a13c60d6bb2f54d0e44455ea8d

---


# Microsoft Dynamics 365 for Campaign 통합 구성

Adobe Campaign Standard를 사용하여 크로스 채널 커뮤니케이션에서 Microsoft Dynamics 365 통합을 구성하고 CRM 데이터를 활성화하는 방법을 알아봅니다.

## 개요

Adobe Campaign Standard - Microsoft Dynamics 365 통합에 대해서는 [이 페이지에서](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md)설명합니다.

이 통합을 위해 프로비저닝해야 하는 세 가지 시스템:

1. Adobe Campaign Standard - [자세한 내용](../../integrating/using/configure-adobe-io-for-ms-dynamic.md)
1. 영업을 위한 Microsoft Dynamics 365 - 아래 설명
1. Unifi - [자세한 내용](../../integrating/using/configure-unifi-for-microsoft-dynamics-365-integration.md)

프로비저닝된 후에는 관리자가 이러한 시스템을 구성해야 합니다.

이 문서에서는 고객이 Adobe Campaign Standard - Microsoft Dynamics 365 통합을 사용할 수 있도록 사후 프로비저닝 과정에서 필요한 Microsoft Dynamics 365측의 단계를 설명합니다.

## 사전 요구 사항

이 문서에서 프로비전 후 단계를 수행하기 전에 이미 프로비전되었으며 조직의 Microsoft Dynamics 365 인스턴스에 대한 관리자 액세스 권한이 있는 것으로 가정합니다.  이러한 문제가 발생하지 않은 경우 Microsoft 고객 지원에 문의하여 Dynamics 365 프로비저닝을 완료해야 합니다.

## 애플리케이션 및 권한 설정

Microsoft Dynamics 365 인터페이스의 타임라인 보기에 Campaign Standard 경험 이벤트를 게시하기 위해 OAuth 액세스 토큰을 사용하면 Unifi에서 웹 API를 통해 Microsoft Dynamics 365 인스턴스에 인증할 수 있습니다.

주요 단계는 다음 비디오에 요약되어 있습니다.

>[!VIDEO](https://video.tv.adobe.com/v/27637)

OAuth 액세스 토큰을 생성하려면 아래 설명된 단계를 따르십시오.

### 새 응용 프로그램 등록

1. 관리자 로그인 아래에서 portal.azure.com에 로그인합니다.

1. 왼쪽 **[!UICONTROL Azure Active Directory]** 메뉴에서 을 클릭합니다.그런 다음 표시되는 하위 **[!UICONTROL App registrations]** 메뉴를 클릭합니다.

1. 화면 **[!UICONTROL New registration]** 상단에서 을 클릭합니다.

   ![](assets/do-not-localize/MSdynACSIntegration-7.png)

1. 앱 등록 화면 채우기:

   * 이름:adobe campaign
   * 지원되는 계정 유형: **[!UICONTROL Accounts in this organizational directory only]** (기본값)

새 응용 프로그램 만들기에 대한 자세한 내용은 [이 섹션을](https://docs.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app)참조하십시오.

>[!NOTE]
>
>Azure AD 파섹 나중에 Dynamics 365를 구성할 때와 Universal Post 프로비저닝 단계를 수행할 때 이 ID가 필요합니다.

### 클라이언트 암호 생성

1. 앱 개요 화면에서 왼쪽의 하위 메뉴에서 **[!UICONTROL Certificates and Secrets > New client secret]**

   ![](assets/do-not-localize/MSdynACSIntegration-8.png)

1. 설명을 입력하고 기간을 설정한 다음 을 클릭합니다 **[!UICONTROL OK]**.

이제 클라이언트 암호가 만들어집니다.  Unifi 사후 프로비저닝 단계 완료를 위한 값을 유지합니다.

>[!CAUTION]
>
>Unifi 사후 프로비저닝 단계를 완료하는 데 필요한 만큼 이 값을 유지합니다. 나중에 검색할 수 없습니다.

클라이언트 암호 생성에 대한 자세한 내용은 이 섹션을 참조하십시오.

### 설정 권한

1. 이 화면 또는 앱 개요 화면에서 왼쪽의 하위 **[!UICONTROL API permissions]** 메뉴에서 을 클릭합니다.  클릭 **[!UICONTROL Add a permission]**&#x200B;후 메뉴에서 **[!UICONTROL Dynamics CRM]** 선택해야 합니다.

   ![](assets/do-not-localize/MSdynACSIntegration-9.png)

1. 그런 다음 확인란을 선택하고 **[!UICONTROL user_impersonation]**&#x200B;단추를 클릭합니다 **[!UICONTROL Add permissions]** .

   ![](assets/do-not-localize/MSdynACSIntegration-10.png)

권한 설정에 대한 자세한 내용은 [이 섹션을](https://docs.microsoft.com/en-us/azure/active-directory/develop/quickstart-configure-app-access-web-apis#add-permissions-to-access-web-apis)참조하십시오.

### 앱 사용자 만들기

이 새 사용자는 일반 사용자입니다. 애플리케이션에서 사용됩니다.이 사용자는 API를 사용하여 Microsoft Dynamics 365를 변경합니다. 이를 만들려면 아래 단계를 수행하십시오.

1. Dynamics 365 인스턴스로 이동하여 관리자로 로그인합니다.

1. 오른쪽 위 모서리에 있는 톱니바퀴 아이콘을 클릭하고 **[!UICONTROL Advanced Settings]**&#x200B;클릭합니다. 상단 배너에서 옆에 있는 드롭다운을 클릭하고 **[!UICONTROL Settings]**&#x200B;을 클릭합니다 **[!UICONTROL Security > Users]**.

1. 드롭다운 메뉴를 클릭하여 이동합니다. **[!UICONTROL Application Users]** 클릭 **[!UICONTROL New]**.

1. 사용자 아이콘 옆에 있는 드롭다운을 확인합니다. **[!UICONTROL USER:APPLICATION USER]**

   새 사용자의 화면을 채웁니다.  매개 변수 제안:

   * **[!UICONTROL User Name]** (이메일):adobeapi@`<hostname>`, where `<hostname>` is the hostname of your Dynamics 365 instance
   * **[!UICONTROL Application ID]**:Azure AD에 등록한 응용 프로그램의 ID(필수)
   * 빈칸으로 **[!UICONTROL Application ID URI]** 남겨주시면 **[!UICONTROL Azure AD Object ID]**
   * **[!UICONTROL Full Name]**:Adobe API
   * **[!UICONTROL Email]**:( **[!UICONTROL User Name]** 또는 원하는 경우 관리자 이메일과 동일)
   앱 사용자 생성에 대한 자세한 내용은 [이 섹션을](https://docs.microsoft.com/en-gb/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user)참조하십시오.

1. 사용자 아이콘을 클릭하고 Adobe Campaign 아이콘을 업로드합니다.이 아이콘은 Dynamics 365에 새 Adobe 이벤트가 표시될 때 [타임라인] 보기에 표시됩니다.

<!-- ***getfile*** adobe campaign logo-->

1. 상단 리본에서 을 클릭하여 사용자 역할 목록을 **[!UICONTROL MANAGE ROLES]** 엽니다.

1. 아래로 스크롤하여 이 사용자에 대한 **[!UICONTROL System administrator]** 액세스를 선택합니다.

1. 클릭 **[!UICONTROL OK]**.

### 테넌트 ID 가져오기

다음 링크의 지침에 따라 테넌트 ID를 찾습니다.  Unifi에서 프로비저닝 후 작업 시 이 ID가 필요합니다.https://docs.microsoft.com/en-us/onedrive/find-your-office-365-tenant-id [](https://docs.microsoft.com/en-us/onedrive/find-your-office-365-tenant-id).

## Microsoft Dynamics 365용 Campaign Standard 설치

Dynamics 365 앱을 Campaign Standard 환경에 통합하려면 아래 단계를 따르십시오.

1. 다음 링크로 이동합니다.https://appsource.microsoft.com/en-us/marketplace/apps [](https://appsource.microsoft.com/en-us/marketplace/apps) 검색 _막대에서 Adobe Campaign_ for Dynamics 365를검색하고 있습니다.
또는 이 [링크로](https://appsource.microsoft.com/en-us/product/dynamics-365/adobecampaign.re4snj-a4n7-5t6y-a14br-d5d1b?flightCodes=adobesignhide&amp;tab=Overview)이동할 수 있습니다.
1. 지침에 따라 Dynamics 365 인스턴스용 앱을 설치합니다.
1. 설치되면 Dynamics 365 인스턴스로 이동하여 관리자로 로그인합니다.
1. 오른쪽 위 모서리에 있는 톱니바퀴 아이콘을 클릭하고 **[!UICONTROL Advanced Settings]**&#x200B;클릭합니다. 상단 배너에서 옆에 있는 드롭다운을 클릭하고 **[!UICONTROL Settings]**&#x200B;아래에서 을 **[!UICONTROL Processes]** 클릭합니다 **[!UICONTROL Process Center]**.
1. 작업을 **[!UICONTROL Adobe Campaign Email Bounce]** 검색하고 클릭합니다.
1. 탭의 맨 위 리본에서 을 클릭하여 이전에 만든 Adobe API 애플리케이션 사용자로 소유자를 **[!UICONTROL Administration]** 변경한 다음 **[!UICONTROL Actions]** 옵션을 선택하고 드롭다운에서 **[!UICONTROL Assign to another User]** **[!UICONTROL Adobe API application user]** 할당하십시오.
1. 프로세스를 다시 활성화합니다.
1. 동일한 작업을 **[!UICONTROL Adobe Campaign Email Click]** 수행합니다.

>[!NOTE]
>
>이러한 프로세스를 비활성화하려면 언제든지 이 **[!UICONTROL Processes]** 화면에서 비활성화할 수 있습니다.

이 구성이 완료되면 Unifi 구성을 설정할 수 있습니다. 자세한 내용은 이 [페이지를](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md)참조하십시오.

**관련 항목**

* [Campaign Standard - Microsoft Dynamics 365 통합](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md)
* [Microsoft Dynamics 365용 Adobe IO 통합 구성](../../integrating/using/configure-adobe-io-for-ms-dynamic.md)
* [캠페인에 대한 Unifi 구성 - Microsoft Dynamics 365 통합](../../integrating/using/configure-unifi-for-microsoft-dynamics-365-integration.md)
