---
title: Campaign 통합 시작
description: 다른 Adobe 솔루션을 사용하여 다양한 기능을 Campaign과 결합할 수 있습니다.
audience: integrating
content-type: reference
topic-tags: get-started-campaign-integrations
feature: Triggers
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: ecf88c7d-6729-4b3a-85c4-60427bb57442
source-git-commit: b3f3309a252971dc527d44913b7918abeea704d9
workflow-type: tm+mt
source-wordcount: '657'
ht-degree: 78%

---

# Campaign 통합 정보{#get-started-campaign-integrations}

이 섹션에서는 현재 버전의 Adobe Campaign과 다른 솔루션 및 서비스 간에 사용할 수 있는 기능적인 통합에 대해 자세히 설명합니다.

아래에 보여지는 다양한 통합을 사용하면 Adobe Campaign의 게재 기능 및 고급 캠페인 관리 기능과 사용자 경험을 개인화할 수 있도록 만들어진 솔루션 세트를 결합할 수 있습니다.

>[!NOTE]
>
> 기본적으로 Adobe Campaign은 이미 Adobe Experience Cloud 계정에 연결되어 있습니다.

사용자의 환경에 따라 다른 솔루션도 Adobe Experience Cloud에 연결할 수 있습니다. 조직(테넌트라고도 함)으로 연결됩니다.

조직은 관리자가 그룹 및 사용자를 구성하고 Experience Cloud에서 단일 로그온을 제어할 수 있도록 해주는 엔터티입니다. 조직은 모든 Experience Cloud 제품 및 솔루션을 포괄하는 로그인 회사와 같은 기능을 합니다. 대부분의 경우 조직은 회사의 이름입니다. 하지만 회사는 여러 조직을 가질 수 있습니다. 사용자 및 조직 관리에 대해서는 [Adobe Experience Cloud 도움말 포털](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/organizations.html)에 자세히 설명되어 있습니다.

다른 시스템의 데이터 흐름을 Adobe Campaign과 통합하려면 [API 설명서](../../api/using/get-started-apis.md)를 참조하십시오.

>[!NOTE]
>
>Adobe Campaign Standard은 Microsoft Dynamics 365와도 연결할 수 있습니다. 이 통합을 통해 CRM 시스템에서 사용 가능한 모든 연락처 데이터를 동기화하여 모든 관련 연락처 데이터를 캠페인 활동에 사용할 수 있습니다. 이 통합에 대한 자세한 내용은 캠페인 및 [Dynamics 365를 사용하여 작업](../../integrating/using/d365-acs-get-started.md)을 참조하십시오.


<table> 
 <thead> 
  <tr> 
   <th> 솔루션<br /> </th> 
   <th> 사용 사례<br /> </th> 
   <th> <br />을(를) 참조하십시오. </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Adobe Experience Manager<br /> </td> 
   <td> Adobe Experience Manager에서 직접 Adobe Campaign 데이터베이스에 매핑된 이메일 콘텐츠 또는 양식을 만들 수 있습니다.<br /> </td> 
   <td> 
     <a href="../../integrating/using/integrating-with-experience-manager.md">Campaign과 Experience Manager에서 작업</a>, <a href="https://helpx.adobe.com/kr/experience-manager/6-4/sites/administering/using/campaignstandard.html">Experience Manager과 Campaign Standard 통합</a>, <a href="https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignstandard.html">Experience Manager과 Campaign에서 전자 메일 만들기</a> 
    </td> 
  </tr> 
  <tr> 
   <td> Adobe Target<br /> </td> 
   <td> Adobe Campaign에서 만들고 보낸 이메일이 열려 있을 때 Adobe Target에서 동적으로 계산된 이미지를 삽입할 수 있습니다.<br /> </td> 
   <td> 
    <a href="../../integrating/using/about-campaign-target-integration.md">Campaign 및 Target 작업</a>, <a href="https://experienceleague.adobe.com/docs/target/using/integrate/campaign-and-target.html">Campaign과 Target 통합</a>, <a href="https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html">실시간으로 이메일 이미지 개인화</a> 비디오(3단계)
    </td> 
  </tr> 
  <tr> 
   <td> Adobe Analytics<br /> </td> 
   <td> Adobe Analytics에서 직접 이메일 게재 성공 여부를 추적할 수 있습니다.<br /> </td> 
   <td> 
    <a href="../../integrating/using/about-campaign-analytics-integration.md">Analytics와 Campaign 데이터 공유</a>, <a href="https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html">통합 Campaign 보고를 위한 KPI 공유 비디오</a> (1단계)
    </td> 
  </tr> 
  <tr> 
   <td> Adobe Audience Manager 및 사용자 핵심 서비스(프로필 및 대상자)<br /> </td> 
   <td> 사용하는 다른 Adobe Experience Cloud 애플리케이션과 대상자를 교환할 수 있습니다.<br /> </td> 
   <td> <a href="../../integrating/using/about-campaign-audience-manager-or-people-core-service-integration.md">사용자 핵심 서비스(프로필 및 대상자)</a><br /> </td> 
  </tr> 
   <tr> 
   <td> Adobe 실시간 고객 데이터 플랫폼(RTCDP)<br /> </td> 
   <td> Adobe Campaign과 Adobe Real-time Customer Data Platform(RTCDP) 간의 통합을 통해 세그먼트 데이터를 공유하고 Adobe Campaign에 대상을 가져올 수 있습니다.</td>
   <td><a href="../../integrating/using/get-started-sources-destinations.md">소스 및 대상 시작</a></td>
  </tr> 
  <tr> 
   <td> Adobe Asset 핵심 서비스 및 Assets On Demand<br /> </td> 
   <td> Adobe Experience Cloud 라이브러리의 자산을 Adobe Campaign에서 만든 이메일 및 랜딩 페이지에 삽입할 수 있습니다.<br /> </td> 
   <td> <a href="../../integrating/using/working-with-campaign-and-assets-core-service.md">자산 핵심 서비스</a> 또는 Assets On Demand<br /> </td> 
  </tr> 
  <tr> 
   <td> 관심 영역(모바일용 분석)<br /> </td> 
   <td> 모바일 애플리케이션의 구독자로부터 관심 영역 데이터를 수집하여 Adobe Campaign과 함께 개인화된 마케팅 메시지를 보낼 수 있습니다.<br /> </td> 
   <td> <a href="../../integrating/using/about-campaign-points-of-interest-data-integration.md">Campaign 및 관심 영역 데이터를 사용하여 위치 기반 마케팅 메시지</a> 보내기(모바일용 분석)<br /> </td> 
  </tr> 
  <tr> 
   <td> Adobe Experience Cloud 트리거<br /> </td> 
   <td> Adobe Analytics가 웹 사이트에서 특정 행동을 추적하면, Adobe Campaign에서 이에 대한 응답으로 고객에게 개인화된 이메일을 보낼 수 있습니다.<br /> </td> 
   <td> 
    <a href="../../integrating/using/about-adobe-experience-cloud-triggers.md">Campaign Standard에 Experience Cloud 트리거 사용</a>, <a href="../../integrating/using/abandonment-triggers-use-cases.md">중단 트리거-Campaign 사용 사례</a>, <a href="https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html">사이트 활동을 기반으로 리마케팅 메시지 트리거</a>비디오 (2단계)
    </td> 
  </tr> 
    <tr> 
   <td> Adobe Journey Orchestration<br /> </td> 
   <td> 기본 동작을 통해 Adobe Campaign Standard Journey Orchestration의 컨텍스트에서 Adobe 트랜잭션 메시지 기능을 사용하여 이메일, 푸시 알림 및 SMS를 보낼 수 있습니다.<br /> </td> 
   <td> <a href="https://experienceleague.adobe.com/docs/journeys/using/action-journeys/working-with-adobe-campaign.html">Adobe Journey Orchestration 및 Adobe Campaign Standard 작업</a><br /> </td> 
  </tr> 
  <tr> 
   <td> Adobe Dreamweaver<br /> </td> 
   <td> Dreamweaver의 이메일 콘텐츠를 편집하고 Adobe Campaign과 동기화할 수 있습니다.<br /> </td> 
   <td> 
    <a href="https://experienceleague.adobe.com/docs/campaign-learn/campaign-standard-tutorials/designing-content/email-designer/dreamweaver-integration.html?lang=ko">Dreamweaver으로 개인화된 전자 메일 만들기</a> 비디오, <a href="https://helpx.adobe.com/kr/dreamweaver/using/working-with-dreamweaver-and-campaign.html">Dreamweaver용 Campaign 확장 사용</a> 
  </td> 
  </tr> 
  <tr> 
   <td> Adobe Experience Platform SDK<br /> </td> 
   <td> Experience Platform SDK를 사용하여 Adobe Campaign에서 모바일 앱 속성 활성화 과정을 자동화할 수 있습니다.<br /> </td> 
   <td> <a href="https://helpx.adobe.com/kr/campaign/kb/configuring-app-sdk.html">Experience Platform SDK를 사용한 모바일 애플리케이션 구성</a><br /> </td> 
  </tr> 
 </tbody> 
</table>
