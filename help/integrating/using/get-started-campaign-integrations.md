---
title: Campaign Standard 시작
description: 다른 Adobe 솔루션을 사용하여 다양한 기능을 Campaign과 결합할 수 있습니다.
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
source-git-commit: 4ae70ca95cb282a694c41361d859b19385db5673
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 7%

---


# Campaign 통합 기본 정보{#get-started-campaign-integrations}

이 섹션에서는 현재 버전의 Adobe Campaign과 다른 솔루션 및 서비스 간에 사용할 수 있는 기능 통합에 대해 자세히 설명합니다.

아래에 제시된 다양한 통합을 통해 Adobe Campaign의 전달 및 고급 캠페인 관리 기능과 사용자 경험을 개인화할 수 있는 솔루션을 결합할 수 있습니다.

>[!NOTE]
>
> 기본적으로 Adobe Campaign은 이미 Adobe Experience Cloud 계정에 연결되어 있습니다.

환경에 따라 다른 솔루션도 Adobe Experience Cloud에 연결할 수 있습니다. 조직(세입자라고도 함)으로 연결됩니다.

조직은 관리자가 그룹 및 사용자를 구성하고 Experience Cloud에서 Single Sign-On을 제어할 수 있도록 해주는 개체입니다. 조직은 모든 Experience Cloud 제품 및 솔루션을 포괄하는 로그인 회사와 같은 기능을 합니다. 대부분의 경우 조직은 회사 이름입니다. 하지만, 회사는 많은 조직을 가질 수 있습니다. 사용자 및 조직 관리에 대해서는 [Adobe Experience Cloud 도움말 포털에 자세히 설명되어 있습니다](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/organizations.html).

다른 시스템의 데이터 흐름을 Adobe Campaign과 통합하려면 [API 설명서를 참조하십시오](../../api/using/get-started-apis.md).

>[!NOTE]
>
>Adobe Campaign Standard은 Microsoft Dynamics 365와도 연결할 수 있습니다.이 통합을 통해 CRM 시스템에서 사용 가능한 모든 연락처 데이터를 동기화하여 모든 관련 연락처 데이터를 캠페인 활동에 사용할 수 있습니다. 이 통합에 대한 자세한 내용은 캠페인 및 [Dynamics 365를 사용하여 작업을 참조하십시오](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md).


<table> 
 <thead> 
  <tr> 
   <th> 솔루션<br /> </th> 
   <th> Use Case<br /> </th> 
   <th> Refer to<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Experience Manager<br /> 6.1, 6.2, 6.3, 6.4, 6.5<br /> </td> 
   <td> Adobe Experience Manager에서 직접 Adobe Campaign 데이터베이스에 매핑된 이메일 내용 또는 양식을 만들 수 있습니다.<br /> </td> 
   <td> 
     <a href="../../integrating/using/integrating-with-experience-manager.md">캠페인 및 Experience Manager을 사용한 작업</a><br/>, Experience Manager 및 Campaign Standard <a href="https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/campaignstandard.html"></a> 통합, Experience Manager <br/>및 캠페인 <a href="https://docs.campaign.adobe.com/doc/standard/getting_started/en/ACS_AEM.html">을 사용하여 이메일 만들기</a> 
    </td> 
  </tr> 
  <tr> 
   <td> Target<br /> Classic, Standard<br /> </td> 
   <td> Adobe Campaign에서 만들고 보낸 이메일이 열려 있을 때 Adobe Target에서 동적으로 계산된 이미지를 삽입할 수 있습니다.<br /> </td> 
   <td> 
    <a href="../../integrating/using/about-campaign-target-integration.md">캠페인 및 Target</a> 를 사용한 작업 <br/>, 캠페인 및 Target <a href="https://docs.adobe.com/content/help/en/target/using/integrate/campaign-and-target.html">통합,</a><br/>이메일 이미지 <a href="https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html">개인화(3단계</a> )
    </td> 
  </tr> 
  <tr> 
   <td> Analytics<br /> Standard, Premium <br /> </td> 
   <td> Adobe Analytics에서 직접 이메일 배달 성공 여부를 추적할 수 있습니다.<br /> </td> 
   <td> 
    <a href="../../integrating/using/about-campaign-analytics-integration.md">Analytics와 캠페인 데이터 공유</a><br/>, 통합 캠페인 보고 <a href="https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html">비디오를 위한 KPI 공유</a> (1단계)
    </td> 
  </tr> 
  <tr> 
   <td> Adobe Audience Manager 및 사용자 코어 서비스(프로필 및 대상)<br /> </td> 
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
   <td> 모바일 애플리케이션의 가입자로부터 관심 영역 데이터를 수집하여 Adobe Campaign과 함께 개인화된 마케팅 메시지를 보낼 수 있습니다.<br /> </td> 
   <td> <a href="../../integrating/using/about-campaign-points-of-interest-data-integration.md">캠페인 및 관심 영역 데이터를 사용하여 위치 기반 마케팅 메시지</a> 보내기(모바일용 분석)<br /> </td> 
  </tr> 
  <tr> 
   <td> Experience Cloud 트리거<br /> </td> 
   <td> Adobe Analytics이 웹 사이트에서 추적하는 특정 행동에 대한 반응으로 Adobe Campaign의 고객에게 개인화된 이메일을 보낼 수 있습니다.<br /> </td> 
   <td> 
    <a href="../../integrating/using/about-adobe-experience-cloud-triggers.md">Campaign Standard</a><br/>, <a href="../../integrating/using/abandonment-triggers-use-cases.md">포기 트리거-캠페인 사용 사례</a><br/>, <a href="https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html">사이트 활동</a> 비디오를 기반으로 리마케팅 메시지 트리거(2단계)의 Experience Cloud사용
    </td> 
  </tr> 
  <tr> 
   <td> Dreamweaver<br /> </td> 
   <td> Dreamweaver의 이메일 컨텐츠를 편집하고 Adobe Campaign과 동기화할 수 있습니다.<br /> </td> 
   <td> 
    <a href="https://docs.adobe.com/content/help/ko-KR/campaign-standard-learn/tutorials/designing-content/email-designer/dreamweaver-integration.html">Dreamweaver</a> 비디오로 개인화된 이메일 만들기, Dreamweaver용 <br/><a href="https://helpx.adobe.com/kr/dreamweaver/using/working-with-dreamweaver-and-campaign.html">캠페인 확장 사용</a> 
  </td> 
  </tr> 
  <tr> 
   <td> Experience Platform SDK<br /> </td> 
   <td> Experience Platform SDK를 사용하여 Adobe Campaign에서 모바일 앱 속성 활성화 과정을 자동화할 수 있습니다.<br /> </td> 
   <td> <a href="https://helpx.adobe.com/kr/campaign/kb/configuring-app-sdk.html">Experience Platform SDK를 사용한 모바일 애플리케이션 구성</a><br /> </td> 
  </tr> 
 </tbody> 
</table>

