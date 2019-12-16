---
title: Audience Manager 또는 People 핵심 서비스와의 통합 제공 및 구성
description: '다른 Adobe Experience Cloud 솔루션을 사용하여 대상이나 세그먼트를 공유하도록 Audience Manager/People 핵심 서비스 통합을 구성하는 방법을 알아봅니다. '
page-status-flag: never-activated
uuid: e7329644-0033-4729-b4a7-61bef137f4b5
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-audience-manager-or-people-core-service
discoiquuid: eb24f4ea-325f-433a-91a0-c45906320bcb
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 7e887fff76660dcb0369d4222e1ab3ac391c3a2d

---


# Audience Manager 또는 People 핵심 서비스와의 통합 제공 및 구성{#provisioning-and-configuring-integration-with-audience-manager-or-people-core-service}

Adobe Campaign에서 Audience Manager 및 사람 코어의 제공 및 구성은 다음 두 단계를 수행합니다.Adobe [에 요청을 제출한](#submitting-request-to-adobe) 다음 [Adobe Campaign에서 통합 구성을 참조하십시오](#configuring-the-integration-in-adobe-campaign).

## Adobe에 요청 제출 {#submitting-request-to-adobe}

Audience Manager(AAM) 또는 People 핵심 서비스 통합을 통해 Adobe Campaign에서 대상자 또는 세그먼트를 가져오고 내보낼 수 있습니다.

먼저 이 통합을 구성해야 합니다. 이 통합의 프로비저닝을 요청하려면 [Digital-Request@adobe.com](mailto:Digital-Request@adobe.com)에 다음 정보를 이메일로 보내주십시오.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>요청 유형:</strong><br /> </td> 
   <td> AAM/사람 핵심 서비스-캠페인 통합 구성 </td> 
  </tr> 
  <tr> 
   <td> <strong>조직명:</strong><br /> </td> 
   <td> 조직 이름 </td> 
  </tr> 
  <tr> 
   <td> <strong>IMS 조직 ID</strong><br /> </td> 
   <td> IMS 조직 ID. <br> 관리 메뉴의 Experience Cloud에서 IMS 조직 ID를 찾을 수 있습니다. Adobe Experience Cloud에 처음 연결할 때도 제공됩니다. </td> 
  </tr> 
  <tr> 
   <td> <strong>환경:</strong><br /> </td> 
   <td> 예:프로덕션 </td> 
  </tr> 
  <tr> 
   <td> <strong>AAM 또는 사용자 서비스</strong><br /> </td> 
   <td> 예:Adobe Audience Manager. Audience Manager 라이선스를 보유하고 있는지 여부와 상관없이 프로비저닝 팀에 문의하십시오.</td> 
  </tr> 
  <tr> 
   <td> <strong>선언된 ID 또는 방문자 ID</strong><br /> </td> 
   <td> 예:선언된 ID </td> 
  </tr> 
  <tr> 
   <td> <strong>추가 정보</strong><br /> </td> 
   <td> 유용한 정보 또는 의견 </td> 
  </tr> 
 </tbody> 
</table>

## Adobe Campaign에서 통합 구성 {#configuring-the-integration-in-adobe-campaign}

이 요청을 제출한 후 Adobe는 사용자를 위해 통합 프로비저닝을 계속 진행할 것이며 구성을 완료하기 위해 필요한 세부 정보와 정보를 제공할 것입니다.

* [1단계:Adobe Campaign에서 외부 계정 구성 또는 확인](#step-1--configure-or-check-the-external-accounts-in-adobe-campaign)
* [2단계:데이터 소스 구성](#step-2--configure-the-data-sources)
* [3단계:캠페인 추적 서버 구성](#step-3--configure-campaign-tracking-server)
* [4단계:방문자 ID 서비스 구성](#step-4--configure-the-visitor-id-service)

### 1단계:Adobe Campaign에서 외부 계정 구성 또는 확인 {#step-1--configure-or-check-the-external-accounts-in-adobe-campaign}

먼저 Adobe Campaign에서 외부 계정을 구성하거나 확인해야 합니다. 이러한 계정은 Adobe에 의해 구성되어야 하며 필요한 정보는 귀하에게 전달되어야 합니다.

이렇게 하려면 다음을 수행하십시오.

1. 고급 메뉴에서 관리 &gt; 응용 프로그램 **설정 &gt; 외부 계정을**&#x200B;선택합니다.

   이 통합에 사용할 수 있는 다음 외부 계정 중 하나를 선택합니다.

   ![](assets/integration_aam_1.png)

1. 다음 **[!UICONTROL Receiver server]** 형식으로 입력하십시오.
1. 를 **[!UICONTROL AWS Access Key ID]**&#x200B;입력하고 **[!UICONTROL Secret Access Key]** 를 **[!UICONTROL AWS Region]**&#x200B;입력합니다.

이제 외부 계정이 이 통합에 대해 구성됩니다.

### 2단계:데이터 소스 구성 {#step-2--configure-the-data-sources}

다음 두 개의 데이터 소스는 Audience Manager 내에서 만들어집니다.Adobe Campaign(MID) 및 Adobe Campaign(선언된 ID). 이와 동시에 다음 두 개의 데이터 소스를 Adobe Campaign에서 사용할 수 있습니다.

* **[!UICONTROL Recipient - Visitor ID (Defaultdatasources)]**:방문자 ID에 대해 기본적으로 구성된 기본 데이터 소스입니다. Campaign에서 생성된 세그먼트는 이 데이터 소스의 일부가 됩니다.
* **선언된 ID** 데이터 소스:이 데이터 소스를 만들고 Audience Manager의 **[!UICONTROL DeclaredId]** 데이터 소스 정의와 매핑해야 합니다.

도메인이 다른 여러 웹 사이트의 경우 Adobe Campaign은 ECID를 기반으로 하는 조정을 지원하지 않습니다.

데이터 소스를 구성하려면 **[!UICONTROL Recipient - Visitor ID (Defaultdatasources)]** 다음을 수행하십시오.

1. &gt; **[!UICONTROL Administration]** &gt; **[!UICONTROL Application settings]** &gt; **[!UICONTROL Shared Data Sources]**&#x200B;에서 **[!UICONTROL Recipient - Visitor ID (Defaultdatasources)]**&#x200B;선택합니다.

   ![](assets/integration_aam_2.png)

1. 드롭다운에서 **[!UICONTROL Adobe Campaign]** **[!UICONTROL Data Source/ Alias]** 선택합니다.
1. Adobe에서 **[!UICONTROL AAM Destination ID]** 제공한 항목을 입력합니다.

   ![](assets/integration_aam_3.png)

1. 이 **[!UICONTROL Reconciliation process]** 카테고리에서, 조정 기준을 변경하지 말고 항상 을 사용하는 것이 좋습니다. **[!UICONTROL Visitor ID]**
1. Click **[!UICONTROL Save]**.

데이터 소스를 만들려면 **[!UICONTROL Declared ID]** 다음을 수행하십시오.

1. &gt; **[!UICONTROL Administration]** &gt; **[!UICONTROL Application settings]** &gt; **[!UICONTROL Shared Data Sources]**&#x200B;에서 **[!UICONTROL Create]** 단추를 클릭합니다.
1. 데이터 **[!UICONTROL Label]** 소스의 편집
1. 드롭다운에서 Audience Manager의 데이터 소스에 해당하는 데이터 소스를 **[!UICONTROL Data Source/ Alias]** **[!UICONTROL DeclaredID]** 선택합니다.
1. Adobe에서 **[!UICONTROL Data Source / Alias]** 제공하고 제공하는 데이터 소스를 **[!UICONTROL AAM Destination ID]** 입력합니다.
1. 필요에 따라 **[!UICONTROL Reconciliation process]** 설정합니다.
1. Click **[!UICONTROL Save]**.

>[!NOTE]
>
>캠페인 트리거 통합을 **[!UICONTROL AAM Destination ID]** 위해 공유 데이터 소스를 구성하는 경우에는 [](../../integrating/using/configuring-triggers-in-experience-cloud.md)필드가 필요하지 않습니다. **[!UICONTROL Priority]** 은 트리거 - 캠페인 통합을 구성할 때만 필요합니다. 우선 순위는 먼저 구성할 데이터 소스를 결정합니다. 우선 순위는 1 또는 100과 같은 숫자일 수 있습니다. 우선 순위가 높을수록 조정 중 선호도가 높습니다.

### 3단계:캠페인 추적 서버 구성 {#step-3--configure-campaign-tracking-server}

People 코어 서비스 또는 Audience Manager와의 통합을 구성하려면 캠페인 추적 서버를 구성해야 합니다.

여기서는 캠페인 추적 서버가 도메인(CNAME)에 등록되어 있는지 확인해야 합니다. 도메인 이름 위임에 대한 자세한 내용은 [이 문서에서](https://docs.campaign.adobe.com/doc/AC/en/technicalResources/Technotes/AdobeCampaign_Deliverability_Sub_Domain_Delegation.pdf)참조할 수 있습니다.

### 4단계:방문자 ID 서비스 구성 {#step-4--configure-the-visitor-id-service}

방문자 ID 서비스가 웹 속성 또는 웹 사이트에 구성되지 않은 경우 다음 [문서를](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-setup-aam-analytics.html) 참조하여 서비스 또는 다음 [비디오를](https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html#step-two)구성하는 방법을 알아보십시오.

구성 및 프로비저닝이 완료되어 이제 통합으로 대상 또는 세그먼트를 가져오고 내보낼 수 있습니다.
