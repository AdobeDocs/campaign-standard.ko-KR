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
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 92%

---


# Campaign 통합 기본 정보{#get-started-campaign-integrations}

이 섹션에서는 현재 버전의 Adobe Campaign과 다른 솔루션 및 서비스 간에 사용할 수 있는 기능적인 통합에 대해 자세히 설명합니다.

아래에 보여지는 다양한 통합을 사용하면 Adobe Campaign의 게재 기능 및 고급 캠페인 관리 기능과 사용자 경험을 개인화할 수 있도록 만들어진 솔루션 세트를 결합할 수 있습니다.

>[!NOTE]
>
> 기본적으로 Adobe Campaign은 이미 Adobe Experience Cloud 계정에 연결되어 있습니다.

사용자의 환경에 따라 다른 솔루션도 Adobe Experience Cloud에 연결할 수 있습니다. 조직(테넌트라고도 함)으로 연결됩니다.

조직은 관리자가 그룹 및 사용자를 구성하고 Experience Cloud에서 단일 로그온을 제어할 수 있도록 해주는 엔터티입니다. 조직은 모든 Experience Cloud 제품 및 솔루션을 포괄하는 로그인 회사와 같은 기능을 합니다. 대부분의 경우 조직은 회사의 이름입니다. 하지만 회사는 여러 조직을 가질 수 있습니다. 사용자 및 조직 관리에 대해서는 [Adobe Experience Cloud 도움말 포털](https://docs.adobe.com/content/help/ko-KR/core-services/interface/manage-users-and-products/organizations.html)에 자세히 설명되어 있습니다.

다른 시스템의 데이터 흐름을 Adobe Campaign과 통합하려면 [API 설명서](../../api/using/get-started-apis.md)를 참조하십시오.

>[!NOTE]
>
>Adobe Campaign Standard은 Microsoft Dynamics 365와도 연결할 수 있습니다. 이 통합을 통해 CRM 시스템에서 사용 가능한 모든 연락처 데이터를 동기화하여 모든 관련 연락처 데이터를 캠페인 활동에 사용할 수 있습니다. 이 통합에 대한 자세한 내용은 캠페인 및 [Dynamics 365를 사용하여 작업](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md)을 참조하십시오.


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
   <td> Experience Manager<br /> 6.1, 6.2, 6.3, 6.4, 6.5<br /> </td> 
   <td> Adobe Experience Manager에서 직접 Adobe Campaign 데이터베이스에 매핑된 이메일 콘텐츠 또는 양식을 만들 수 있습니다.<br /> </td> 
   <td> 
     <a href="../../integrating/using/integrating-with-experience-manager.md">캠페인 및 Experience Manager을 사용한 작업</a>, Experience Manager 및 Campaign Standard <a href="https://helpx.adobe.com/kr/experience-manager/6-4/sites/administering/using/campaignstandard.html">통합</a>, Experience Manager 및 <a href="https://docs.adobe.com/content/help/ko-KR/campaign-standard/using/integrating-with-adobe-cloud/working-with-campaign-and-experience-manager/creating-email-experience-manager.html">캠페인이 포함된 이메일 만들기</a> 
    </td> 
  </tr> 
  <tr> 
   <td> Target<br /> Classic, Standard<br /> </td> 
   <td> Adobe Campaign에서 만들고 보낸 이메일이 열려 있을 때 Adobe Target에서 동적으로 계산된 이미지를 삽입할 수 있습니다.<br /> </td> 
   <td> 
    <a href="../../integrating/using/about-campaign-target-integration.md">캠페인 및 Target을 사용한</a>작업, 캠페인 <a href="https://docs.adobe.com/content/help/ko-KR/target/using/integrate/campaign-and-target.html">및 Target</a>통합, <a href="https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html">이메일 이미지</a> 개인화(3단계)
    </td> 
  </tr> 
  <tr> 
   <td> Analytics<br /> Standard, Premium <br /> </td> 
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
   <td> 자산 핵심 서비스 및 Assets On Demand<br /> </td> 
   <td> Adobe Experience Cloud 라이브러리의 자산을 Adobe Campaign에서 만든 이메일 및 랜딩 페이지에 삽입할 수 있습니다.<br /> </td> 
   <td> <a href="../../integrating/using/working-with-campaign-and-assets-core-service.md">자산 핵심 서비스</a> 또는 Assets On Demand<br /> </td> 
  </tr> 
  <tr> 
   <td> 관심 영역(모바일용 분석)<br /> </td> 
   <td> 모바일 애플리케이션의 구독자로부터 관심 영역 데이터를 수집하여 Adobe Campaign과 함께 개인화된 마케팅 메시지를 보낼 수 있습니다.<br /> </td> 
   <td> <a href="../../integrating/using/about-campaign-points-of-interest-data-integration.md">Campaign 및 관심 영역 데이터를 사용하여 위치 기반 마케팅 메시지</a> 보내기(모바일용 분석)<br /> </td> 
  </tr> 
  <tr> 
   <td> Experience Cloud 트리거<br /> </td> 
   <td> Adobe Analytics가 웹 사이트에서 특정 행동을 추적하면, Adobe Campaign에서 이에 대한 응답으로 고객에게 개인화된 이메일을 보낼 수 있습니다.<br /> </td> 
   <td> 
    <a href="../../integrating/using/about-adobe-experience-cloud-triggers.md">Campaign Standard에 Experience Cloud 트리거 사용</a>, <a href="../../integrating/using/abandonment-triggers-use-cases.md">중단 트리거-Campaign 사용 사례</a>, <a href="https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html">사이트 활동을 기반으로 리마케팅 메시지 트리거</a>비디오 (2단계)
    </td> 
  </tr> 
  <tr> 
   <td> Dreamweaver<br /> </td> 
   <td> Dreamweaver의 이메일 콘텐츠를 편집하고 Adobe Campaign과 동기화할 수 있습니다.<br /> </td> 
   <td> 
    <a href="https://docs.adobe.com/content/help/ko-KR/campaign-standard-learn/tutorials/designing-content/email-designer/dreamweaver-integration.html">Dreamweaver</a> 비디오로 개인화된 이메일 제작, Dreamweaver용 캠페인 <a href="https://helpx.adobe.com/kr/dreamweaver/using/working-with-dreamweaver-and-campaign.html">익스텐션 사용</a> 
  </td> 
  </tr> 
  <tr> 
   <td> Experience Platform SDK<br /> </td> 
   <td> Experience Platform SDK를 사용하여 Adobe Campaign에서 모바일 앱 속성 활성화 과정을 자동화할 수 있습니다.<br /> </td> 
   <td> <a href="https://helpx.adobe.com/kr/campaign/kb/configuring-app-sdk.html">Experience Platform SDK를 사용한 모바일 애플리케이션 구성</a><br /> </td> 
  </tr> 
 </tbody> 
</table>

