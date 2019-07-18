---
title: 캠페인 통합 정보
seo-title: 캠페인 통합 정보
description: 캠페인 통합 정보
seo-description: Adobe Campaign를 사용하면 다른 Adobe 솔루션을 사용하고 다양한 기능을 결합할 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 59 d 7 cd 99-a 6 f 7-47 f 1-9 b 5 c-c 50 e 27 a 2 bef 8
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 통합
content-type: 참조
topic-tags: 캠페인 통합
discoiquuid: 9633 E 9 CA -3323-499 B -8259-45165 D 59 A 4 D 0
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 337f2270f3f66d5172084a4e2a19d6185bf097ff

---


# About Campaign integrations{#about-campaign-integrations}

이 섹션에서는 현재 버전의 Adobe Campaign와 다른 솔루션 및 서비스 간에 사용할 수 있는 기능 통합에 대해 자세히 설명합니다.

아래 표시된 서로 다른 통합을 통해 Adobe Campaign의 게재 및 고급 캠페인 관리 기능과 사용자 경험을 개인화할 수 있도록 만들어진 솔루션 세트를 결합할 수 있습니다.

>[!NOTE]
>
> 기본적으로 Adobe Campaign는 이미 Adobe Experience Cloud 계정에 연결되어 있습니다.

환경에 따라 다른 솔루션도 Adobe Experience Cloud에 연결할 수 있습니다. 이들은 조직 (테넌트 라고도 함) 로 연결됩니다.

조직은 관리자가 그룹과 사용자를 구성하고 Experience Cloud에서 Single Sign-On를 제어할 수 있는 개체입니다. 조직은 모든 Experience Cloud 제품과 솔루션을 포괄하는 로그인 회사와 같은 기능을 합니다. 대부분의 경우 조직은 회사 이름입니다. 그러나 회사는 여러 조직을 가질 수 있습니다. User and organization management is detailed in the [Adobe Experience Cloud help portal](https://marketing.adobe.com/resources/help/en_US/mcloud/organizations.html).

If you would like to integrate data flows from other systems with Adobe Campaign, have a look at our [API documentation](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html).

>[!NOTE]
>
>Adobe Campaign Standard는 Microsoft Dynamics 365 에도 연결할 수 있습니다. 이러한 통합을 통해 CRM 시스템에서 사용 가능한 모든 연락처 데이터를 동기화하여 캠페인 활동에 사용할 수 있는 모든 관련 연락처 데이터를 만들 수 있습니다. For more on this integration, refer to [Working with Campaign and Dynamics 365](https://helpx.adobe.com/campaign/kb/acs-ms-dynamics.html).


<table> 
 <thead> 
  <tr> 
   <th> Solution<br /> </th> 
   <th> Use Case<br /> </th> 
   <th> Refer to<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Experience Manager<br /> 6.1, 6.2, 6.3, 6.4<br /> </td> 
   <td> Allows you to create email contents or forms mapped to the Adobe Campaign database directly in Adobe Experience Manager.<br /> </td> 
   <td> 
     <a href="../../integrating/using/integrating-with-experience-manager.md">Campaign 및 Experience Manager를 사용하여 작업</a><br/>, <a href="https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/campaignstandard.html">Experience Manager와 Campaign Standard</a> <br/>통합, <a href="https://docs.campaign.adobe.com/doc/standard/getting_started/en/ACS_AEM.html">Experience Manager와 Campaign를 사용한 이메일 제작</a> 
    </td> 
  </tr> 
  <tr> 
   <td> Target<br /> Classic, Standard<br /> </td> 
   <td> Allows you to insert images that are dynamically computed by Adobe Target when an email created and sent by Adobe Campaign is opened.<br /> </td> 
   <td> 
    <a href="../../integrating/using/about-campaign-target-integration.md">캠페인 및 Target</a> <br/>사용, <a href="https://marketing.adobe.com/resources/help/en_US/target/a4t/c_campaign_and_target.html">캠페인 및 Target 통합</a><br/>, <a href="https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html">실시간 비디오에서 이메일 이미지</a> 개인화 (3 단계)
    </td> 
  </tr> 
  <tr> 
   <td> Analytics<br /> Standard, Premium <br /> </td> 
   <td> Allows you to track the success of your email deliveries directly in Adobe Analytics.<br /> </td> 
   <td> 
    <a href="../../integrating/using/about-campaign-analytics-integration.md">Analytics와 캠페인 데이터 공유</a><br/>, <a href="https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html">통합 캠페인 리포팅</a> 비디오에 대한 KPI 공유 (1 단계)
    </td> 
  </tr> 
  <tr> 
   <td> Adobe Audience Manager and People core service (Profiles &amp; Audiences)<br /> </td> 
   <td> Allow you to exchange audiences with the different Adobe Experience Cloud applications that you use.<br /> </td> 
   <td> <a href="../../integrating/using/about-campaign-audience-manager-or-people-core-service-integration.md">People 코어 서비스 (Profiles &amp; Audiences)</a><br /> </td> 
  </tr> 
  <tr> 
   <td> Asset core service and Assets On Demand<br /> </td> 
   <td> Allows you to insert assets from your Adobe Experience Cloud library into emails and landing pages created in Adobe Campaign.<br /> </td> 
   <td> <a href="../../integrating/using/working-with-campaign-and-assets-core-service.md">Assets 핵심 서비스</a> 또는 On-Demand 자산<br /> </td> 
  </tr> 
  <tr> 
   <td> Points of Interest (Analytics for Mobile)<br /> </td> 
   <td> Allows you to collect Points of Interest data from your mobile application's subscribers to send personalized marketing messages with Adobe Campaign.<br /> </td> 
   <td> <a href="../../integrating/using/about-campaign-points-of-interest-data-integration.md">캠페인 및 관심 영역 데이터를 사용하여 위치 기반 마케팅 메시지 전송</a> (모바일 분석)<br /> </td> 
  </tr> 
  <tr> 
   <td> Experience Cloud Triggers<br /> </td> 
   <td> Allows you to send personalized emails to your customers in Adobe Campaign as a reaction to specific behaviors that are tracked on your website by Adobe Analytics.<br /> </td> 
   <td> 
    <a href="../../integrating/using/about-adobe-experience-cloud-triggers.md">Campaign Standard에서 Experience Cloud 트리거 사용</a><br/>, <a href="../../integrating/using/abandonment-triggers-use-cases.md">포기 트리거-캠페인 사용 사례</a><br/>, <a href="https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html">사이트 활동</a> 비디오를 기반으로 재마케팅 메시지 트리거 (2 단계)
    </td> 
  </tr> 
  <tr> 
   <td> Dreamweaver<br /> </td> 
   <td> Allows you to edit an email content from Dreamweaver and synchronize it with Adobe Campaign.<br /> </td> 
   <td> 
    <a href="https://helpx.adobe.com/campaign/kt/acs/using/acs-dreamweaver-integration-feature-video-use.html">Dreamweaver</a> 비디오를 <br/>사용하여 개인화된 이메일 제작, <a href="https://helpx.adobe.com/dreamweaver/using/working-with-dreamweaver-and-campaign.html">Dreamweaver 용 Campaign 익스텐션 사용</a> 
  </td> 
  </tr> 
  <tr> 
   <td> Creative SDK<br /> </td> 
   <td> Allows you to edit images and use a complete set of features powered by the Adobe Creative SDK to enhance your images directly in the content editor.<br /> </td> 
   <td> <a href="../../designing/using/modifying-images-with-the-adobe-creative-sdk.md">Adobe Creative SDK를 사용하여 이미지 수정</a><br /> </td> 
  </tr> 
  <tr> 
   <td> Experience Platform SDKs<br /> </td> 
   <td> Allows automation of the Mobile App Property activation process in Adobe Campaign using the Experience Platform SDKs.<br /> </td> 
   <td> <a href="https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html">Experience Platform SDK를 사용하여 모바일 애플리케이션 구성</a><br /> </td> 
  </tr> 
 </tbody> 
</table>

