---
title: Campaign 통합 시작하기
description: Adobe Campaign을 사용하면 다른 Adobe 솔루션을 사용하여 다양한 기능을 결합할 수 있습니다.
page-status-flag: never-activated
uuid: 59d7cd99-a6f7-47f1-9b5c-c50e27a2bef8
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: get-started-campaign-integrations
discoiquuid: 9633e9ca-3323-499b-8259-45165d59a4d0
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 816d550d8bd0de085a47f97c1f6cc2fbb5e7acb9

---


# Campaign 통합 기본 정보{#get-started-campaign-integrations}

이 섹션에서는 현재 버전의 Adobe Campaign과 다른 솔루션 및 서비스 간에 사용할 수 있는 기능 통합에 대해 자세히 설명합니다.

아래 나와 있는 다양한 통합을 통해 Adobe Campaign의 전달 및 고급 캠페인 관리 기능과 사용자 경험을 개인화할 수 있는 솔루션을 결합할 수 있습니다.

>[!NOTE]
>
> 기본적으로 Adobe Campaign은 이미 Adobe Experience Cloud 계정에 연결되어 있습니다.

환경에 따라 다른 솔루션도 Adobe Experience Cloud에 연결할 수 있습니다. 조직(세입자라고도 함)으로 연결됩니다.

조직은 관리자가 그룹과 사용자를 구성하고 Experience Cloud에서 Single Sign-On을 제어할 수 있도록 해주는 개체입니다. 조직은 모든 Experience Cloud 제품 및 솔루션을 포괄하는 로그인 회사와 같은 기능을 합니다. 대부분의 경우 조직은 회사 이름입니다. 하지만, 회사는 많은 조직을 가질 수 있습니다. 사용자 및 조직 관리는 [Adobe Experience Cloud 도움말 포털에 자세히 설명되어 있습니다](https://marketing.adobe.com/resources/help/ko_KR/mcloud/organizations.html).

다른 시스템의 데이터 흐름을 Adobe Campaign과 통합하려면 [API 설명서를 참조하십시오](../../api/using/get-started-apis.md).

>[!NOTE]
>
>Adobe Campaign Standard는 Microsoft Dynamics 365에도 연결할 수 있습니다. 이 통합을 통해 CRM 시스템에서 사용 가능한 모든 연락처 데이터를 동기화하여 모든 관련 연락처 데이터를 캠페인 활동에 사용할 수 있습니다. 이 통합에 대한 자세한 내용은 캠페인 및 [Dynamics 365를 사용하여 작업을 참조하십시오](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md).


<table> 
 <thead> 
  <tr> 
   <th> 솔루션<br /> </th> 
   <th> Use Case<br /> </th> 
   <th> 자세한 내용은<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Adobe Experience Manager<br /> 6.1, 6.2, 6.3, 6.4, 6.5<br /> </td> 
   <td> Adobe Experience Manager에서 직접 Adobe Campaign 데이터베이스에 매핑된 이메일 콘텐츠 또는 양식을 만들 수 있습니다.<br /> </td> 
   <td> 
     <a href="../../integrating/using/integrating-with-experience-manager.md">Adobe Campaign 및 Experience Manager</a><br/>, Adobe Experience Manager <a href="https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/campaignstandard.html">및 Campaign Standard</a> 와 통합 <br/>, Adobe Experience Manager 및 Campaign을 사용하여 이메일 <a href="https://docs.campaign.adobe.com/doc/standard/getting_started/en/ACS_AEM.html">만들기</a> 
    </td> 
  </tr> 
  <tr> 
   <td> Target<br /> Classic, Standard<br /> </td> 
   <td> Adobe Campaign에서 만들고 보낸 이메일을 열 때 Adobe Target에서 동적으로 계산된 이미지를 삽입할 수 있습니다.<br /> </td> 
   <td> 
    <a href="../../integrating/using/about-campaign-target-integration.md">캠페인 및 타겟</a><br/>을 사용한 작업, 캠페인 및 <a href="https://marketing.adobe.com/resources/help/en_US/target/a4t/c_campaign_and_target.html">타겟</a><br/>통합, <a href="https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html">이메일 이미지</a> 개인화(3단계)
    </td> 
  </tr> 
  <tr> 
   <td> Analytics<br /> Standard, Premium <br /> </td> 
   <td> Adobe Analytics에서 직접 이메일 게재 성공 여부를 추적할 수 있습니다.<br /> </td> 
   <td> 
    <a href="../../integrating/using/about-campaign-analytics-integration.md">Analytics와 캠페인 데이터 공유</a><br/>, 통합 캠페인 보고 <a href="https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html">비디오를 위한 KPI 공유</a> (1단계)
    </td> 
  </tr> 
  <tr> 
   <td> Adobe Audience Manager 및 사용자 핵심 서비스(프로필 및 대상)<br /> </td> 
   <td> 사용하는 다른 Adobe Experience Cloud 애플리케이션과 대상을 교환할 수 있습니다.<br /> </td> 
   <td> <a href="../../integrating/using/about-campaign-audience-manager-or-people-core-service-integration.md">사람 코어 서비스(프로필 및 대상)</a><br /> </td> 
  </tr> 
  <tr> 
   <td> 자산 핵심 서비스 및 Assets On Demand<br /> </td> 
   <td> Adobe Experience Cloud 라이브러리의 에셋을 Adobe Campaign에서 만든 이메일 및 랜딩 페이지에 삽입할 수 있습니다.<br /> </td> 
   <td> <a href="../../integrating/using/working-with-campaign-and-assets-core-service.md">자산 핵심 서비스</a> 또는 Assets On Demand<br /> </td> 
  </tr> 
  <tr> 
   <td> 관심 영역(모바일용 분석)<br /> </td> 
   <td> 모바일 애플리케이션의 가입자로부터 관심 영역 데이터를 수집하여 Adobe Campaign을 통해 개인화된 마케팅 메시지를 전송할 수 있습니다.<br /> </td> 
   <td> <a href="../../integrating/using/about-campaign-points-of-interest-data-integration.md">캠페인 및 관심 영역 데이터를 사용하여 위치 기반 마케팅 메시지</a> 보내기(모바일용 분석)<br /> </td> 
  </tr> 
  <tr> 
   <td> Experience Cloud Triggers<br /> </td> 
   <td> Adobe Analytics를 통해 웹 사이트에서 추적되는 특정 행동에 대한 반응으로 Adobe Campaign에서 개인화된 이메일을 고객에게 보낼 수 있습니다.<br /> </td> 
   <td> 
    <a href="../../integrating/using/about-adobe-experience-cloud-triggers.md">Campaign Standard에서 Experience Cloud 트리거 사용</a><br/>, <a href="../../integrating/using/abandonment-triggers-use-cases.md">포기 트리거-캠페인 사용 사례</a><br/>, 사이트 활동 <a href="https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html">비디오를 기반으로</a> 리마케팅 메시지 트리거(2단계)
    </td> 
  </tr> 
  <tr> 
   <td> Dreamweaver<br /> </td> 
   <td> Dreamweaver에서 이메일 컨텐츠를 편집하고 Adobe Campaign과 동기화할 수 있습니다.<br /> </td> 
   <td> 
    <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/designing-content/email-designer/dreamweaver-integration.html">Dreamweaver</a> 비디오로 개인화된 이메일 제작, Dreamweaver용 <br/><a href="https://helpx.adobe.com/dreamweaver/using/working-with-dreamweaver-and-campaign.html">캠페인 익스텐션 사용</a> 
  </td> 
  </tr> 
  <tr> 
   <td> Experience Platform SDK<br /> </td> 
   <td> Experience Platform SDK를 사용하여 Adobe Campaign에서 모바일 앱 속성 활성화 프로세스를 자동화할 수 있습니다.<br /> </td> 
   <td> <a href="https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html">Experience Platform SDK를 사용한 모바일 애플리케이션 구성</a><br /> </td> 
  </tr> 
 </tbody> 
</table>

