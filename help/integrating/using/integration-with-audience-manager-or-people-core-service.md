---
title: Audience Manager 또는 People 핵심 서비스와의 프로비전 및 구성
description: 다양한 Adobe Experience Cloud 솔루션과 대상 또는 세그먼트 공유를 시작하기 위해 Audience Manager/People 핵심 서비스 통합을 구성하는 방법에 대해 알아봅니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-audience-manager-or-people-core-service
feature: People Core Service Integration
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: 04d0fe26-a8cc-49ae-aaa9-b470169068ee
source-git-commit: b3f3309a252971dc527d44913b7918abeea704d9
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 4%

---

# Audience Manager 또는 People 핵심 서비스와의 프로비전 및 구성{#integration-with-audience-manager-or-people-core-service}

Adobe Campaign의 Audience Manager 및 People 코어의 프로비전 및 구성은 두 가지 단계를 수행합니다. [Adobe에 요청 제출](#submitting-request-to-adobe) 및 [Adobe Campaign에서 통합 구성](#configuring-the-integration-in-adobe-campaign).

## Adobe에 요청 제출 {#submitting-request-to-adobe}

Audience Manager(AAM) 또는 People 핵심 서비스 통합을 사용하여 Adobe Campaign에서 대상자 또는 세그먼트를 가져오고 내보낼 수 있습니다.

먼저 이 통합을 구성해야 합니다. 이 통합의 프로비저닝을 요청하려면 Adobe 지원에 다음 정보를 문의하십시오.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>요청 유형:</strong><br /> </td> 
   <td> AAM/People 핵심 서비스-캠페인 통합 구성 </td> 
  </tr> 
  <tr> 
   <td> <strong>조직 이름:</strong><br /> </td> 
   <td> 조직 이름 </td> 
  </tr> 
  <tr> 
   <td> <strong>IMS 조직 ID</strong><br /> </td> 
   <td> 조직 ID입니다. <br> 조직 ID를 찾으려면 <a href="https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=ko">이 페이지</a>를 참조하세요.</td> 
  </tr> 
  <tr> 
   <td> <strong>환경:</strong><br /> </td> 
   <td> 예: 프로덕션 </td> 
  </tr> 
  <tr> 
   <td> <strong>AAM 또는 People 서비스</strong><br /> </td> 
   <td> 예: Adobe Audience Manager. Audience Manager 라이선스 소유 여부는 프로비저닝 팀에 문의하십시오.</td> 
  </tr> 
  <tr> 
   <td> <strong>선언된 ID 또는 방문자 ID</strong><br /> </td> 
   <td> 예: 선언된 ID </td> 
  </tr> 
  <tr> 
   <td> <strong>추가 정보</strong><br /> </td> 
   <td> 보유하고 있을 수 있는 유용한 정보 또는 댓글 </td> 
  </tr> 
 </tbody> 
</table>

## Adobe Campaign에서 통합 구성 {#configuring-the-integration-in-adobe-campaign}

이 요청을 제출하면 Adobe에서 자동으로 통합 프로비저닝을 진행하고 연락하여 구성을 완료해야 하는 세부 정보와 정보를 제공합니다.

* [1단계: Adobe Campaign에서 외부 계정 구성 또는 확인](#step-1--configure-or-check-the-external-accounts-in-adobe-campaign)
* [2단계: 데이터 소스 구성](#step-2--configure-the-data-sources)
* [3단계: Campaign 추적 서버 구성](#step-3--configure-campaign-tracking-server)
* [4단계: 방문자 ID 서비스 구성](#step-4--configure-the-visitor-id-service)

### 1단계: Adobe Campaign에서 외부 계정 구성 또는 확인 {#step-1--configure-or-check-the-external-accounts-in-adobe-campaign}

먼저 Adobe Campaign에서 외부 계정을 구성하거나 확인해야 합니다. 이러한 계정은 Adobe에서 구성했어야 하며 필요한 정보를 귀하에게 전달했어야 합니다.

방법은 다음과 같습니다.

1. 고급 메뉴에서 **관리 > 응용 프로그램 설정 > 외부 계정**&#x200B;을 선택합니다.

   이 통합에 사용할 수 있는 다음 외부 계정 중 하나를 선택합니다.

   ![](assets/integration_aam_1.png)

1. 다음 형식으로 **[!UICONTROL Receiver server]** 입력
1. **[!UICONTROL AWS Access Key ID]**, **[!UICONTROL Secret Access Key]** 및 **[!UICONTROL AWS Region]**&#x200B;을(를) 입력하십시오.

이제 외부 계정이 이 통합에 대해 구성되었습니다.

### 2단계: 데이터 소스 구성 {#step-2--configure-the-data-sources}

Audience Manager 내에는 Adobe Campaign(MID)와 Adobe Campaign(DeclortedId)의 두 가지 데이터 소스가 만들어집니다. 동시에 Adobe Campaign에서는 다음 두 가지 데이터 소스를 사용할 수 있습니다.

* **[!UICONTROL Recipient - Visitor ID (Defaultdatasources)]**: 기본적으로 방문자 ID에 대해 구성된 기본 데이터 원본입니다. Campaign에서 만든 세그먼트는 이 데이터 소스의 일부가 됩니다.
* **선언된 ID** 데이터 원본: 이 데이터 원본을 만들고 Audience Manager의 **[!UICONTROL DeclaredId]** 데이터 원본 정의와 매핑해야 합니다.

도메인이 다른 여러 웹 사이트의 경우 Adobe Campaign은 ECID를 기반으로 하는 조정을 지원하지 않습니다.

**[!UICONTROL Recipient - Visitor ID (Defaultdatasources)]** 데이터 원본을 구성하려면:

1. **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** > **[!UICONTROL Shared Data Sources]**&#x200B;에서 **[!UICONTROL Recipient - Visitor ID (Defaultdatasources)]**&#x200B;을(를) 선택합니다.

   ![](assets/integration_aam_2.png)

1. **[!UICONTROL Adobe Campaign]** 드롭다운에서 **[!UICONTROL Data Source/ Alias]**&#x200B;을(를) 선택합니다.
1. Adobe에서 제공한 **[!UICONTROL AAM Destination ID]**&#x200B;을(를) 입력하십시오.

   ![](assets/integration_aam_3.png)

1. **[!UICONTROL Reconciliation process]** 범주에서 조정 기준을 변경하지 말고 항상 **[!UICONTROL Visitor ID]**&#x200B;을(를) 사용하는 것이 좋습니다.
1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

**[!UICONTROL Declared ID]** 데이터 원본을 만들려면:

1. **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** > **[!UICONTROL Shared Data Sources]**&#x200B;에서 **[!UICONTROL Create]** 단추를 클릭합니다.
1. 데이터 원본의 **[!UICONTROL Label]**&#x200B;을(를) 편집합니다.
1. **[!UICONTROL Data Source/ Alias]** 드롭다운에서 Audience Manager의 **[!UICONTROL DeclaredID]** 데이터 소스에 해당하는 Data Source을 선택합니다.
1. Adobe에서 제공한 **[!UICONTROL Data Source / Alias]** 및 **[!UICONTROL AAM Destination ID]**&#x200B;을(를) 입력하여 데이터 소스를 구성합니다.
1. 필요에 따라 **[!UICONTROL Reconciliation process]**&#x200B;을(를) 설정합니다.
1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

>[!NOTE]
>
>**[!UICONTROL AAM Destination ID]** Campaign-Triggers 통합[에 대한 공유 데이터 원본을 구성하는 경우에는 &#x200B;](../../integrating/using/configuring-triggers-in-experience-cloud.md) 필드가 필요하지 않습니다. **[!UICONTROL Priority]**&#x200B;은(는) 트리거 - Campaign 통합을 구성할 때만 필요합니다. 우선 순위는 어떤 데이터 Source이 먼저 구성될지 결정합니다. 우선 순위는 1 또는 100과 같은 임의의 숫자일 수 있습니다. 우선순위가 높을수록 조정 시 선호도가 높아집니다.

### 3단계: Campaign 추적 서버 구성 {#step-3--configure-campaign-tracking-server}

People 핵심 서비스 또는 Audience Manager와의 통합을 구성하려면 Campaign 추적 서버도 구성해야 합니다.

공유 대상이 방문자 ID로 작동하도록 하려면 추적 서버 도메인이 클릭한 URL 또는 기본 웹 사이트의 하위 도메인이어야 합니다.

>[!IMPORTANT]
>
> Campaign 추적 서버가 도메인(CNAME)에 등록되어 있는지 확인해야 합니다. 도메인 이름 구성에 대한 자세한 내용은 [이 문서](https://helpx.adobe.com/kr/campaign/kb/domain-name-delegation.html)를 참조하십시오.

### 4단계: 방문자 ID 서비스 구성 {#step-4--configure-the-visitor-id-service}

웹 속성이나 웹 사이트에서 방문자 ID 서비스가 구성된 적이 없는 경우 다음 [문서](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-aam-analytics.html?lang=ko)를 참조하여 서비스 또는 다음 [비디오](https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html#step-two)를 구성하는 방법을 알아보십시오.

Experience Cloud ID 서비스의 `setCustomerID` 함수를 사용하여 선언된 ID와 고객 식별자를 통합 코드 `AdobeCampaignID`과(와) 동기화합니다. `AdobeCampaignID`은(는) [2단계: 데이터 원본 구성](#step-2--configure-the-data-sources)에서 구성된 받는 사람 데이터 Source에 설정된 조정 키 값과 일치해야 합니다.

구성 및 프로비저닝이 완료되었으므로 이제 통합을 사용하여 대상자 또는 세그먼트를 가져오고 내보낼 수 있습니다.
