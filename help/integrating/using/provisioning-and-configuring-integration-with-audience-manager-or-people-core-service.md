---
title: Audience Manager 또는 People 핵심 서비스와의 프로비전 및 구성
description: '다른 Adobe Experience Cloud 솔루션으로 대상 또는 세그먼트 공유를 시작하도록 Audience Manager/People 핵심 서비스 통합을 구성하는 방법을 알아봅니다. '
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-audience-manager-or-people-core-service
feature: People Core Service Integration
role: Data Architect
level: Intermediate
exl-id: 04d0fe26-a8cc-49ae-aaa9-b470169068ee
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '717'
ht-degree: 9%

---

# Audience Manager 또는 People 핵심 서비스와의 프로비전 및 구성{#provisioning-and-configuring-integration-with-audience-manager-or-people-core-service}

Adobe Campaign에서 Audience Manager 및 People 코어의 프로비저닝 및 구성은 두 단계를 수행합니다. [Adobe](#submitting-request-to-adobe)에 요청을 제출한 다음 [Adobe Campaign](#configuring-the-integration-in-adobe-campaign)에서 통합 구성

## Adobe에 요청 제출 {#submitting-request-to-adobe}

AAM(Audience Manager) 또는 People 핵심 서비스 통합을 통해 Adobe Campaign에서 대상 또는 세그먼트를 가져오고 내보낼 수 있습니다.

먼저 이 통합을 구성해야 합니다. 이 통합의 프로비저닝을 요청하려면 [Digital-Request@adobe.com](mailto:Digital-Request@adobe.com)에 다음 정보를 이메일로 보내주십시오.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>요청 유형:</strong><br /> </td> 
   <td> AAM/People 핵심 서비스-Campaign 통합 구성 </td> 
  </tr> 
  <tr> 
   <td> <strong>조직 이름:</strong><br /> </td> 
   <td> 조직 이름 </td> 
  </tr> 
  <tr> 
   <td> <strong>IMS 조직 ID</strong><br /> </td> 
   <td> IMS 조직 ID입니다. <br> 관리 메뉴의 Experience Cloud에서 IMS 조직 ID를 찾을 수 있습니다. Adobe Experience Cloud에 처음 연결할 때도 제공됩니다. </td> 
  </tr> 
  <tr> 
   <td> <strong>환경:</strong><br /> </td> 
   <td> 예: 프로덕션 </td> 
  </tr> 
  <tr> 
   <td> <strong>AAM 또는 People Service</strong><br /> </td> 
   <td> 예: Adobe Audience Manager. Audience Manager 라이센스를 보유하고 있는지 여부에 관계없이 프로비저닝 팀에 문의하십시오.</td> 
  </tr> 
  <tr> 
   <td> <strong>선언된 ID 또는 방문자 ID</strong><br /> </td> 
   <td> 예: 선언된 ID </td> 
  </tr> 
  <tr> 
   <td> <strong>추가 정보</strong><br /> </td> 
   <td> 다음과 같은 유용한 정보나 설명을 제공합니다 </td> 
  </tr> 
 </tbody> 
</table>

## Adobe Campaign에서 통합 구성 {#configuring-the-integration-in-adobe-campaign}

이 요청을 제출한 후 Adobe은 사용자를 위한 통합 프로비저닝을 진행하고 구성을 완료해야 하는 세부 정보와 정보를 제공하도록 사용자에게 문의하십시오.

* [1단계: Adobe Campaign에서 외부 계정 구성 또는 확인](#step-1--configure-or-check-the-external-accounts-in-adobe-campaign)
* [2단계: 데이터 소스 구성](#step-2--configure-the-data-sources)
* [3단계: Campaign 추적 서버 구성](#step-3--configure-campaign-tracking-server)
* [4단계: 방문자 ID 서비스 구성](#step-4--configure-the-visitor-id-service)

### 1단계: Adobe Campaign에서 외부 계정 구성 또는 확인 {#step-1--configure-or-check-the-external-accounts-in-adobe-campaign}

먼저 Adobe Campaign에서 외부 계정을 구성하거나 확인해야 합니다. 이러한 계정은 Adobe에 의해 구성되어야 하며 필요한 정보는 사용자에게 전달되어야 합니다.

방법은 다음과 같습니다.

1. 고급 메뉴에서 **관리 > 응용 프로그램 설정 > 외부 계정**&#x200B;을 선택합니다.

   이 통합에 사용할 수 있는 다음 외부 계정 중 하나를 선택합니다.

   ![](assets/integration_aam_1.png)

1. 다음 형식으로 **[!UICONTROL Receiver server]** 입력
1. **[!UICONTROL AWS Access Key ID]**, **[!UICONTROL Secret Access Key]** 및 **[!UICONTROL AWS Region]**&#x200B;를 입력합니다.

이제 외부 계정이 이 통합에 대해 구성되었습니다.

### 2단계: 데이터 소스 구성 {#step-2--configure-the-data-sources}

다음 두 데이터 소스는 Audience Manager 내에 만들어집니다. Adobe Campaign(MID) 및 Adobe Campaign(선언된 Id). 동시에 이 두 데이터 소스는 Adobe Campaign에서 사용할 수 있습니다.

* **[!UICONTROL Recipient - Visitor ID (Defaultdatasources)]**: 방문자 ID에 대해 기본적으로 구성된 기본 데이터 소스입니다. Campaign에서 만든 세그먼트는 이 데이터 소스의 일부가 됩니다.
* **선언된** ID데이터 소스: 이 데이터 소스는 Audience Manager의  **[!UICONTROL DeclaredId]** 데이터 소스 정의와 함께 만들고 매핑해야 합니다.

서로 다른 도메인이 있는 여러 웹 사이트의 경우 Adobe Campaign에서는 ECID를 기반으로 한 조정을 지원하지 않습니다.

**[!UICONTROL Recipient - Visitor ID (Defaultdatasources)]** 데이터 소스를 구성하려면:

1. **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** > **[!UICONTROL Shared Data Sources]**&#x200B;에서 **[!UICONTROL Recipient - Visitor ID (Defaultdatasources)]**&#x200B;를 선택합니다.

   ![](assets/integration_aam_2.png)

1. **[!UICONTROL Data Source/ Alias]** 드롭다운에서 **[!UICONTROL Adobe Campaign]** 을 선택합니다.
1. Adobe이 제공한 **[!UICONTROL AAM Destination ID]**&#x200B;을 입력합니다.

   ![](assets/integration_aam_3.png)

1. **[!UICONTROL Reconciliation process]** 카테고리에서는 조정 기준을 변경하지 말고 항상 **[!UICONTROL Visitor ID]** 을 사용하는 것이 좋습니다.
1. **[!UICONTROL Save]**&#x200B;를 클릭합니다.

**[!UICONTROL Declared ID]** 데이터 소스를 만들려면:

1. **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** > **[!UICONTROL Shared Data Sources]**&#x200B;에서 **[!UICONTROL Create]** 버튼을 클릭합니다.
1. 데이터 소스의 **[!UICONTROL Label]**&#x200B;을 편집합니다.
1. **[!UICONTROL Data Source/ Alias]** 드롭다운에서 Audience Manager의 **[!UICONTROL DeclaredID]** 데이터 소스에 해당하는 데이터 소스를 선택합니다.
1. Adobe에서 제공한 **[!UICONTROL Data Source / Alias]** 및 **[!UICONTROL AAM Destination ID]**&#x200B;을 입력하여 데이터 소스를 구성합니다.
1. 필요에 따라 **[!UICONTROL Reconciliation process]** 을 설정합니다.
1. **[!UICONTROL Save]**&#x200B;를 클릭합니다.

>[!NOTE]
>
>[Campaign-Triggers 통합](../../integrating/using/configuring-triggers-in-experience-cloud.md)에 대한 공유 데이터 소스를 구성하는 경우에는 **[!UICONTROL AAM Destination ID]** 필드가 필요하지 않습니다. **[!UICONTROL Priority]** 트리거 - 캠페인 통합을 구성할 때만 필요합니다. 우선 순위는 먼저 구성할 데이터 소스를 결정합니다. 우선 순위는 1 또는 100과 같은 임의의 숫자일 수 있습니다. 우선순위가 높을수록 조정 중 선호도가 높습니다.

### 3단계: Campaign 추적 서버 구성 {#step-3--configure-campaign-tracking-server}

People 핵심 서비스 또는 Audience Manager와의 통합을 구성하려면 Campaign 추적 서버를 구성해야 합니다.

여기서는 Campaign 추적 서버가 도메인(CNAME)에 등록되어 있는지 확인해야 합니다. 도메인 이름 구성에 대한 자세한 내용은 [이 문서](https://helpx.adobe.com/kr/campaign/kb/domain-name-delegation.html)에서 확인할 수 있습니다.

### 4단계: 방문자 ID 서비스 구성 {#step-4--configure-the-visitor-id-service}

웹 속성 또는 웹 사이트에서 방문자 ID 서비스가 구성되지 않은 경우 서비스 구성 방법을 배우려면 다음 [document](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-aam-analytics.html) 를 참조하십시오.[](https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html#step-two)

구성 및 프로비저닝이 완료되면 통합을 사용하여 대상 또는 세그먼트를 가져오고 내보낼 수 있습니다.
