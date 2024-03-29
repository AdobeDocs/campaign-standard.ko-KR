---
title: Microsoft Dynamics 365 통합을 위해 Adobe Developer 구성
description: Microsoft Dynamics 365 통합을 위해 Adobe Developer을 구성하는 방법 알아보기
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-ms-dynamics
feature: Microsoft CRM Integration
role: Data Architect
level: Intermediate
exl-id: ab21b694-d05c-4ba4-b828-936803651b82
source-git-commit: c701043cbba22711de1ea7ddc5266e193d771e14
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 0%

---

# Microsoft Dynamics 365 통합을 위한 Adobe Campaign Standard 및 Adobe Developer 구성

이 문서에서는 통합 애플리케이션이 데이터에 액세스할 수 있도록 Adobe Campaign Standard 및 Adobe I/O을 구성하는 방법을 설명합니다.

## Adobe Campaign Standard 구성 {#campaign-standard}

### 프로필 확장

Adobe Campaign Standard에서 &quot;프로필 확장&quot;을 활성화하십시오.   프로필 리소스의 사용자 정의 필드를 Microsoft Dynamics 365에서 동기화하려면 이 작업이 필요합니다.   이러한 기능을 활성화하는 단계는 다음과 같습니다.

1. 설정 -> 관리 -> 개발 -> 게시로 이동합니다.
1. &quot;게시 준비&quot;를 클릭하여 게시를 준비합니다.
1. 준비가 완료되면 &quot;프로필 및 서비스 외부 API 만들기&quot;를 확인하고 &quot;게시&quot;를 클릭합니다.

## 구성 Adobe I/O {#adobe-io}

Adobe I/O을 사용하면 Adobe Campaign Standard 및 기타 Adobe 제품에 대한 API 액세스를 활성화할 수 있습니다.   이 문서에서는 Microsoft Dynamics 365와 Adobe Campaign Standard 통합을 통해 데이터를 동기화할 수 있도록 Adobe I/O을 구성하는 방법에 대해 자세히 설명합니다.

### 개요

이 문서의 사전 통합 설정을 수행하기 전에 이미 프로비저닝되었으며 조직의 Campaign Standard 인스턴스에 대한 관리자 액세스 권한이 있다고 가정합니다.  이 문제가 발생하지 않은 경우 Adobe 고객 지원 센터에 문의하여 캠페인 프로비저닝을 완료해야 합니다.

>[!CAUTION]
>
>아래 설명된 단계는 관리자가 수행해야 합니다.

### 구성

새 Adobe Developer 프로젝트를 만들고 통합하도록 구성해야 합니다.

#### 새 프로젝트 만들기

이렇게 하려면 아래 절차를 따르십시오.

1. 다음으로 이동 [Adobe Developer 콘솔](https://console.adobe.io/home#) 그리고 화면 오른쪽 상단의 드롭다운 메뉴에서 Adobe 조직 ID 를 선택합니다.

1. 그런 다음 **[!UICONTROL Create new project]** 아래에 **[!UICONTROL Quick Start]**.

   ![](assets/adobeIO1.png)

1. 아래 **[!UICONTROL Get started with your new project]**, 클릭 **[!UICONTROL Add API]**.

   ![](assets/adobeIO2.png)

1. Adobe Campaign을 선택하고 **[!UICONTROL Next]**.

   ![](assets/adobeIO3.png)

1. 다음 화면에서는 인증 유형을 선택할 수 있는 옵션이 제공됩니다. OAuth 서버 간 또는 서비스 계정(JWT)을 선택할 수 있습니다. 서비스 계정(JWT) 자격 증명은 더 이상 새 프로젝트에 권장되지 않으며, 최신 OAuth 서버 간 자격 증명을 위해 더 이상 사용되지 않습니다. 이 안내서에 제공된 지침은 OAuth 서버 간 인증에만 적용됩니다.

   ![](assets/adobeIO4.png)

1. 다음 화면에서는 이 프로젝트와 연결할 제품 프로필을 선택합니다. 제목에 포함된 제품 프로필 선택: Campaign 인스턴스의 테넌트 ID - [!UICONTROL Administrators]

   예: Campaign Standard - your-campaign-tenantID - 관리자

1. **[!UICONTROL Save configured API]**&#x200B;를 클릭합니다.

   ![](assets/adobeIO5.png)

1. 다음 화면에서는 새 Adobe Developer 프로젝트에 대한 세부 사항이 표시됩니다. 클릭 **[!UICONTROL Add to Project]** 화면 왼쪽 상단에서 을 선택합니다. **API** 드롭다운에서.

   ![](assets/adobeIO6.png)

1. 다음 화면에서는 I/O 이벤트 API를 선택한 다음 를 클릭합니다. **[!UICONTROL Next]**.

1. 다음 화면에서 다음을 클릭합니다. **[!UICONTROL Save the configured API]**.  프로젝트 세부 정보 화면으로 돌아갑니다.

1. 이제 클릭 **[!UICONTROL Add to Project]** 화면 왼쪽 상단에서 을 선택합니다. **API** 이전에 수행한 대로 드롭다운에서 을 수행합니다.

1. 다음 화면에서 I/O Management API를 선택하고 **[!UICONTROL Next]**.

1. 다음 화면에서 다음을 클릭합니다. **[!UICONTROL Save the configured API]**.

Campaign의 사전 통합 설정이 완료되었습니다.

**관련 항목**

* [Microsoft Dynamics 365 통합을 위해 Adobe Developer 구성](../../integrating/using/d365-acs-configure-adobe-io.md) 통합 설정의 다음 단계입니다.
* [통합 셀프 서비스 애플리케이션 개요](../../integrating/using/d365-acs-self-service-app-quick-start-guide.md) 통합을 시작하고 실행하는 전체 단계 목록이 포함되어 있습니다.
* [Adobe Developer - 서비스 계정 통합](https://developer.adobe.com/developer-console/docs/guides/#!AdobeDocs/adobeio-auth/master/AuthenticationOverview/ServiceAccountIntegration.md)
* [Campaign Standard - API 액세스 설정](../../api/using/setting-up-api-access.md)
* [Campaign Standard - Dynamics 365 통합](../../integrating/using/d365-acs-configure-d365.md)
* [JWT에서 OAuth 서버 간 자격 증명으로 마이그레이션](../../integrating/using/d365-acs-self-service-app-migrate-credentials.md) jwt에서 OAuth 서버 간 자격 증명으로 마이그레이션하는 단계를 포함합니다.
