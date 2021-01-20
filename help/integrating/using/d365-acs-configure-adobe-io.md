---
title: Microsoft Dynamics 365 통합을 위해 Adobe IO 구성
description: Microsoft Dynamics 365 통합을 위해 Adobe IO를 구성하는 방법을 알아봅니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-ms-dynamics
translation-type: tm+mt
source-git-commit: fe5d40235abc33c0ea7e929cd2e69b7030cea0b1
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 2%

---


# Microsoft Dynamics 365 통합을 위한 Adobe Campaign Standard 및 Adobe I/O 구성

이 문서에서는 통합 응용 프로그램이 데이터에 대한 액세스 권한을 부여하도록 Adobe Campaign Standard 및 Adobe I/O을 구성하는 방법에 대해 설명합니다.

## Adobe Campaign Standard {#campaign-standard} 구성

### 프로필 확장

Adobe Campaign Standard에서 &quot;프로필 확장&quot;을 활성화하십시오.   Microsoft Dynamics 365에서 프로필 리소스의 사용자 지정 필드를 동기화하려면 이 항목이 필요합니다.   이를 활성화하는 단계는 다음과 같습니다.

1. 설정 -> 관리 -> 개발 -> 게시로 이동합니다.
1. &quot;게시 준비&quot;를 클릭하여 게시를 준비합니다.
1. 준비가 완료되면 &quot;프로필 및 서비스 텍스트 API 만들기&quot;를 선택하고 &quot;게시&quot;를 클릭합니다.

## Adobe I/O 구성 {#adobe-io}

Adobe I/O을 사용하면 Adobe Campaign Standard 및 기타 Adobe 제품에 대한 API 액세스를 활성화할 수 있습니다.   이 문서에서는 Adobe Campaign Standard과 Microsoft Dynamics 365의 통합을 통해 데이터를 동기화할 수 있도록 Adobe I/O을 구성하는 방법에 대해 자세히 설명합니다.

### 개요

이 아티클에서 사전 통합 설정을 수행하기 전에 이미 프로비저닝되었으며 조직의 Campaign Standard 인스턴스에 대한 관리자 액세스 권한이 있는 것으로 가정합니다.  이러한 문제가 발생하지 않으면 Adobe 고객 지원 센터에 문의하여 캠페인 제공을 완료해야 합니다.

>[!CAUTION]
>
>아래 설명된 단계는 관리자가 수행해야 합니다.

### 구성

새 Adobe IO 프로젝트를 만들고 통합용으로 구성해야 합니다.

#### 새 프로젝트 만들기

이를 수행하려면 아래 절차를 따르십시오.

1. [Adobe IO 콘솔](https://console.adobe.io/home#)로 이동하고 화면 오른쪽 상단의 드롭다운 메뉴에서 Adobe IMS 조직 ID를 선택합니다.

1. 그런 다음 **[!UICONTROL Quick Start]** 아래의 **[!UICONTROL Create new project]**&#x200B;을 클릭합니다.

   ![](assets/adobeIO1.png)

1. **[!UICONTROL Get started with your new project]** 아래에서 **[!UICONTROL Add API]**&#x200B;을 클릭합니다.

   ![](assets/adobeIO2.png)

1. Adobe Campaign API를 선택하고(아래로 스크롤해야 할 수 있음) **[!UICONTROL Next]**&#x200B;을 클릭합니다.

   ![](assets/adobeIO3.png)

1. 다음 화면에서 자신의 공개 키를 업로드하거나 Adobe IO에서 자동으로 키 쌍을 생성하도록 선택할 수 있습니다. 이러한 지침은 후자의 옵션을 따릅니다. Adobe IO에서 키 쌍을 생성하도록 하려면 옵션 1을 클릭합니다.그런 다음 **[!UICONTROL Generate keypair]** 단추를 클릭합니다.

   ![](assets/adobeIO4.png)

1. 다음 화면에서 키 쌍 zip 파일의 다운로드 위치를 지정하고 선택하라는 메시지가 표시됩니다.

다운로드한 후 파일의 압축을 해제하여 공개 및 개인 키를 표시할 수 있습니다. Adobe IO가 Adobe IO 프로젝트에 공개 키를 이미 적용했습니다. 나중에 개인 키를 유지할 필요가 있습니다.통합 도구의 사전 통합 설정 중에 개인 키가 사용됩니다.

1. 계속하려면 **[!UICONTROL Next]**&#x200B;을 클릭합니다.

   ![](assets/adobeIO5.png)

1. 다음 화면에서 이 프로젝트와 연결할 제품 프로필을 선택합니다. 제목에 포함된 제품 프로필을 선택합니다.캠페인 인스턴스의 테넌트 ID - [!UICONTROL Administrators]

   예:Campaign Standard - 내 캠페인 테넌트 ID - 관리자

1. **[!UICONTROL Save configured API]**&#x200B;을(를) 클릭합니다.

   ![](assets/adobeIO6.png)

1. 다음 화면에는 새 Adobe IO 프로젝트에 대한 세부 사항이 표시됩니다. 화면 왼쪽 상단에 있는 **[!UICONTROL Add to Project]**&#x200B;을 클릭하고 드롭다운에서 **API**&#x200B;를 선택합니다.

   ![](assets/adobeIO7.png)

1. 다음 화면에서 입출력 이벤트 API를 선택한 다음 **[!UICONTROL Next]**&#x200B;을 클릭합니다.

1. 다음 화면에서 **[!UICONTROL Save the configured API]**&#x200B;을 클릭합니다.  프로젝트 세부 사항 화면으로 돌아갑니다.

1. 이제 화면 왼쪽 상단에 있는 **[!UICONTROL Add to Project]**&#x200B;을 클릭하고 드롭다운에서 이전에 보던 대로 **API**&#x200B;를 선택합니다.

1. 다음 화면에서 입출력 관리 API를 선택하고 **[!UICONTROL Next]**&#x200B;을 클릭해야 합니다.

1. 다음 화면에서 **[!UICONTROL Save the configured API]**&#x200B;을 클릭합니다.

이제 Campaign의 사전 통합 설정이 완료되었습니다.

**관련 항목**

* [Microsoft Dynamics 365 통합을 위한 Adobe IO 구성](../../integrating/using/d365-acs-configure-adobe-io.md) 은 통합을 설정하는 다음 단계입니다
* [통합 셀프 서비스 응용 프로그램 ](../../integrating/using/d365-acs-self-service-app-quick-start-guide.md) 개요에는 통합을 실행 및 시작하는 데 필요한 전체 단계 목록이 포함되어 있습니다.


* [Adobe IO - 서비스 계정 통합](https://www.adobe.io/authentication/auth-methods.html#!AdobeDocs/adobeio-auth/master/AuthenticationOverview/ServiceAccountIntegration.md)
* [Campaign Standard - API 액세스 설정](../../api/using/setting-up-api-access.md)
* [Campaign Standard - Dynamics 365 통합](../../integrating/using/d365-acs-configure-d365.md)
