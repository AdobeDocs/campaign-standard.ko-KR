---
solution: Campaign Standard
product: campaign
title: Campaign Standard의 사용 중단되거나 제거된 기능
description: 이 페이지에는 Adobe Campaign Standard의 사용이 중단되거나 제거된 기능의 목록입니다.
audience: rn
content-type: reference
topic-tags: campaign-standard-deprecated-features
translation-type: tm+mt
source-git-commit: 32aba66dd8987414cf90df1e7bfb9c419c5f68ff
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 85%

---


# 사용 중단되거나 제거된 기능 {#deprecated-and-removed-features}

Adobe는 항상 이전 버전과의 호환성을 신중하게 고려하여 전반적인 고객 가치를 향상시키기 위해 제품 기능을 지속적으로 평가하여 보다 현대적인 요소로 대체해야 하는 기존 기능을 식별합니다.

Campaign Standard의 기능을 제거/교체하기 위해 다음 규칙이 적용됩니다.

* 사용 중단 발표가 우선입니다. 기존 사용자는 사용 중단되는 기능을 계속 사용할 수 있지만 더 이상 향상 또는 문서화되지 않습니다.
* 사용 중단되는 기능은 빠른 시일 내에 다음 릴리스에서 제거됩니다. 제거에 대한 실제 타겟 날짜가 이 페이지에 표시되어 있습니다.

이 프로세스를 통해 고객은 실제 제거하기 전에 새로운 버전이나 사용 중단되는 기능의 후속 버전에 맞게 구현을 조정할 수 있는 릴리스 주기를 적어도 하나 이상 확보할 수 있습니다.

>[!NOTE]
>Adobe Campaign Standard 릴리스 및 새 기능은 [릴리스 정보](../../rn/using/release-notes.md)에 나열되어 있습니다.


## 더 이상 사용되지 않는 기능 {#deprecated-features}

이 섹션에는 최신 Campaign Standard 릴리스에서 사용 중단되는 것으로 표시된 기능 및 성능이 나열됩니다.

일반적으로 향후 릴리스에서 제거될 예정인 기능은 먼저 대체 기능을 제공하며 사용 중단되는 것으로 설정됩니다. 이러한 기능은 새 Campaign Standard 고객에게 더 이상 제공되거나 새로운 구현에 사용되지 않습니다. 제품 설명서에서도 제거됩니다.

고객은 현재 배포에서 기능/성능을 사용하는지 검토하고 제공된 대체 기능을 사용하기 위해 구현 변경을 계획해야 합니다. 타겟 제거 날짜를 참조하여 환경 및 프로젝트 업데이트를 알맞게 계획하십시오.

<table> 
 <thead> 
 <tr> 
   <th> <strong>예측 제목 줄</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p> 2020년 12월 15일부터 예측 제목 줄 기능은 더 이상 사용되지 않습니다.</p><br/>
   <p>AI 기반의 이메일 기능을 활용하여 기존 참여 지표를 기반으로 열람률, 최적의 전송 시간, 향후 이탈률을 분석 및 예측하는 것이 좋습니다. <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/testing-and-sending/preparing-and-testing-messages/predictive.html">자세히 알아보기</a></p></br>
     <p>
     <em>Target 제거:2021년 4월</em></p>
     </td> 
  </tr> 
  </tbody> 
</table>
<table> 
 <thead> 
  <tr> 
   <th> <strong>SDK v4를 사용한 푸시 알림</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p> 20.1 릴리스부터 SDK v4는 더 이상 사용되지 않습니다. <a href="https://aep-sdks.gitbook.io/docs/version-4-sdk-end-of-support-faq">자세히 알아보기</a></p><br/>
   <p><a href="https://aep-sdks.gitbook.io/docs/">Adobe Experience Platform 모바일 SDK</a> (과거 v5라고 함)는 향후 출시될 Adobe Experience Cloud 기능 및 성능을 독점적으로 지원합니다.</p></br>
     <p>
     <em>Target 제거 날짜:2021년 8월 31일</em></p>
     </td> 
  </tr> 
 </tbody> 
</table>
<table> 
 <thead> 
  <tr> 
   <th> <strong>개인 정보 보호 요청 - Campaign API 및 인터페이스</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Campaign 19.4 릴리스부터 액세스 및 삭제 요청에 대한 Campaign API 및 인터페이스는 더 이상 사용되지 않습니다. 2단계 프로필 삭제를 사용할 수 없습니다. <a href="https://www.adobe.io/apis/experiencecloud/gdpr.html">Adobe 개인 정보 보호 핵심 서비스</a>를 사용하십시오.</p></br>
   <p>또한 <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/getting-started/privacy/privacy-requests.html?lang=en">개인 정보 보호 요청 관리</a>를 참조하십시오.</p>
  <p> 
  <em>타겟 제거 날짜: 2021년 4월</em></p>
   </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>이메일 디자인 - 기존 이메일 편집기</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Campaign 19.0 릴리스부터 기존 이메일 편집기는 더 이상 사용되지 않습니다. <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/designing-content-in-adobe-campaign.html">캠페인 이메일 디자이너</a>를 사용하여 이메일 컨텐츠를 만들고 개인화합니다. </p></br>
   <p>새로운 편집기에 맞게 이메일 템플릿을 적용하는 방법을 살펴보려면 <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/building-email-content/using-existing-content.html">이 섹션</a>을 참조하십시오.</p></br>
  <p> 
  <em>Target 제거 날짜:2021년 말</em></p>
   </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>사용자 및 보안 - 지리적 단위</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>18.7 릴리스부터 지리적 단위는 더 이상 사용되지 않습니다. 조직적 및 지리적 단위는 Campaign에서 동일한 구문입니다. 사용자는 조직적 단위만 사용하여 사용자 권한/데이터 액세스 계층 구조를 만들어야 합니다. <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/users-and-security/organizational-units.html?lang=ko#administrating">자세히 알아보기</a> 지리적 단위가 만들어지지 않은 기존 인스턴스는 물론 새 Campaign Standard 인스턴스는 18.7 릴리스부터 이 기능을 구현할 수 없습니다.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

## 제거된 기능 {#removed-features}

이 섹션에는 Campaign Standard에서 제거된 기능과 성능이 나열됩니다.

<table> 
 <thead> 
  <tr> 
   <th> <strong>Experience Cloud 트리거를 사용한 성향 점수</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p><b>성향 점수</b>가 Adobe Experience Cloud 트리거에서 서비스 해제되었습니다. 따라서 이 옵션은 Adobe Campaign Standard에서 제거되었습니다. 데이터 보강 스키마에서 성향 점수의 오래된 값을 방지하려면 최신 변경 사항을 검색하고 기존 트리거를 다시 게시하기 위해 스키마를 업데이트하는 것이 좋습니다. 자세한 내용은 <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/integrating-with-adobe-cloud/working-with-campaign-and-triggers/using-triggers-in-campaign.html">Campaign에서 트리거 게시</a>를 참조하십시오 .
</p></br>
   </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>Campaign Standard용 Creative SDK</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>[!DNL Adobe Creative SDK]가 서비스 해제되었습니다. 따라서 Campaign Standard 이메일에서 [!DNL Creative SDK] 기반 이미지 에디션은 Campaign 20.2 릴리스부터 더 이상 사용할 수 없습니다.</p></br>
   </td> 
  </tr> 
 </tbody> 
</table>

## 호환성 종료 {#end-of-compatibility}

<table> 
 <thead> 
  <tr> 
   <th> <strong>Microsoft Internet Explorer 11</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Adobe Campaign과 Adobe Experience Cloud은 2019년 봄 및 Campaign 19.2 릴리스부터 Microsoft Internet Explorer 11에 대한 지원을 중단했습니다. Microsoft Edge 또는 기타 지원되는 브라우저로 전환하십시오. <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/about-configuration-guidelines.html">자세히 알아보기</a></p>
   </td> 
  </tr> 
 </tbody> 
</table>
