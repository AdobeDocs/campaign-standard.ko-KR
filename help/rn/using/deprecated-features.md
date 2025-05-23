---
title: Campaign Standard의 사용 중단되거나 제거된 기능
description: 이 페이지에는 Adobe Campaign Standard의 사용이 중단되거나 제거된 기능의 목록입니다.
feature: Overview
role: User
level: Beginner
exl-id: 03797137-c01c-48dc-b25b-8e72741abb04
source-git-commit: 6b683ccd93e10f78ff643eed9f374a794c085cb1
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 58%

---

# 사용 중단되거나 제거된 기능 {#deprecated-and-removed-features}

Adobe는 항상 이전 버전과의 호환성을 신중하게 고려하여 전반적인 고객 가치를 향상시키기 위해 제품 기능을 지속적으로 평가하여 보다 현대적인 요소로 대체해야 하는 기존 기능을 식별합니다.

Campaign Standard의 기능을 제거/교체하기 위해 다음 규칙이 적용됩니다.

* 사용 중단 발표가 우선입니다. 기존 사용자는 사용 중단되는 기능을 계속 사용할 수 있지만 더 이상 향상 또는 문서화되지 않습니다.
* 사용 중단되는 기능은 빠른 시일 내에 다음 릴리스에서 제거됩니다. 제거에 대한 실제 타겟 날짜가 이 페이지에 표시되어 있습니다.

이 프로세스를 통해 고객은 실제 제거하기 전에 새로운 버전이나 사용 중단되는 기능의 후속 버전에 맞게 구현을 조정할 수 있는 릴리스 주기를 적어도 하나 이상 확보할 수 있습니다.

>[!NOTE]
>Adobe Campaign Standard 릴리스 및 새 기능은 [릴리스 정보](../../rn/using/release-notes.md)에 나열되어 있습니다.


## 지원 종료 기능 {#deprecated-features}

이 섹션에는 최신 Campaign Standard 릴리스에서 사용 중단되는 것으로 표시된 기능 및 성능이 나열됩니다.

일반적으로 향후 릴리스에서 제거될 예정인 기능은 먼저 대체 기능을 제공하며 사용 중단되는 것으로 설정됩니다. 이러한 기능은 새 Campaign Standard 고객에게 더 이상 제공되거나 새로운 구현에 사용되지 않습니다. 제품 설명서에서도 제거됩니다.

고객은 현재 배포에서 기능/성능을 사용하는지 검토하고 제공된 대체 기능을 사용하기 위해 구현 변경을 계획해야 합니다. 타겟 제거 날짜를 참조하여 환경 및 프로젝트 업데이트를 알맞게 계획하십시오.



<table> 
 <thead> 
  <tr> 
   <th> 모바일 애플리케이션용 <strong>SDK V4</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Adobe Experience Platform Mobile 버전 4 SDK에 대한 지원이 2021년 8월 31일부로 종료되었습니다. Adobe Campaign Standard에서 이 레거시 버전의 SDK를 사용 중인 경우 2024년 6월 말까지 <strong>Adobe Experience Platform SDK로 구현을 업데이트해야 합니다</strong>. </p></br>
   <p>구현을 조정하고 최신 Experience Platform SDK로 전환하는 방법에 대해 알아보려면 <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/configuring-mobile/sdkv4-migration.html?lang=ko">이 문서</a>를 읽어 보십시오.</p></br>
   <p><strong>주의</strong>: SDK V4는 2024년 6월 말부터 더 이상 Campaign Standard에서 지원되지 않습니다.</p>
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
   <td> <p>Campaign 19.0 릴리스부터 기존 이메일 편집기는 더 이상 사용되지 않습니다. <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/designing-content-in-adobe-campaign.html?lang=ko">Campaign 이메일 Designer</a>을(를) 사용하여 이메일 콘텐츠를 만들고 개인화합니다. </p></br>
   <p>새로운 편집기에 맞게 이메일 템플릿을 적용하는 방법을 살펴보려면 <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/building-email-content/using-existing-content.html?lang=ko">이 섹션</a>을 참조하십시오.</p></br>
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
   <td> <p>Campaign 18.7 릴리스부터 지리적 단위는 더 이상 사용되지 않습니다. 조직적 및 지리적 단위는 Campaign에서 동일한 구문입니다. 사용자는 조직적 단위만 사용하여 사용자 권한/데이터 액세스 계층 구조를 만들어야 합니다. <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/users-and-security/organizational-units.html?lang=ko#administrating">자세히 알아보기</a> 지리적 단위가 만들어지지 않은 기존 인스턴스는 물론 새 Campaign Standard 인스턴스는 18.7 릴리스부터 이 기능을 구현할 수 없습니다.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

## 제거된 기능 {#removed-features}

이 섹션에는 Campaign Standard에서 제거된 기능과 성능이 나열됩니다.

<table> 
 <thead> 
  <tr> 
   <th> <strong>Audience Destinations 서비스와 통합</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p> Campaign Standard 21.3 릴리스부터 Audience Destinations 서비스와의 통합이 더 이상 사용되지 않습니다.  이제 제거되었습니다.</p>
   <p>새 구현의 경우 Audience Destinations 서비스를 Adobe Campaign Standard과 더 이상 통합할 수 없습니다. 그러나 소스 및 대상을 통해 Campaign과 Adobe Experience Platform을 통합할 수 있습니다. <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/integrating-with-adobe-cloud/adobe-experience-platform/aep-sources-destinations/get-started-sources-destinations.html?lang=ko">자세히 알아보기</a>.</p>
     </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>Adobe Experience Platform 데이터 커넥터와 통합</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p> Campaign Standard 21.3 릴리스부터 Adobe Experience Platform Data Connector와의 통합은 더 이상 사용되지 않습니다.  이제 제거되었습니다.</p>
   <p>새 구현의 경우 Adobe Experience Platform 데이터 커넥터를 Adobe Campaign Standard과 더 이상 통합할 수 없습니다. 그러나 소스 및 대상을 통해 Campaign과 Adobe Experience Platform을 통합할 수 있습니다. <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/integrating-with-adobe-cloud/adobe-experience-platform/aep-sources-destinations/get-started-sources-destinations.html?lang=ko">자세히 알아보기</a>.</p>
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
   <td> <p> Campaign 20.1 릴리스부터 SDK v4는 더 이상 사용되지 않습니다. 이제 제거되었습니다. <a href="https://experienceleague.adobe.com/docs/discontinued/using/mobile-services.htmlhtml?lang=ko">자세히 알아보기</a>.</p><br/>
   <p><a href="https://developer.adobe.com/client-sdks/documentation/">Adobe Experience Platform Mobile SDK</a>(이전 이름 v5)는 이제 예정된 Adobe Experience Cloud 기능 및 기능을 독점적으로 지원합니다.</p>
   <p>2021년 8월 31일 이후에도 고객은 버전 4 SDK를 계속 다운로드하여 사용할 수 있지만 고객 지원 센터 또는 포럼에 액세스할 수는 없습니다.</p>
   <p>SDK v4에서 Adobe Experience Platform Mobile SDK로 마이그레이션하는 방법은 <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/configuring-mobile/sdkv4-migration.html?lang=ko">이 페이지에서</a>알아볼 수 있습니다.</p></br>
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
   <td> <p>Campaign 21.2 릴리스부터 액세스 및 삭제 요청에 대한 Campaign API 및 인터페이스는 더 이상 사용되지 않습니다. 2단계 프로필 삭제를 더 이상 사용할 수 없습니다. <a href="https://developer.adobe.com/experience-platform-apis/references/privacy-service">Adobe 개인 정보 보호 핵심 서비스</a>를 사용합니다.</p></br>
   <p>또한 <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/getting-started/privacy/privacy-requests.html?lang=ko">개인 정보 보호 요청 관리</a>를 참조하십시오.</p>
  </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
 <tr> 
   <th> <strong>예측 제목 줄</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p> 2021년 4월부터 예측 제목 줄 기능이 중단됩니다.</p><br/>
   <p>AI 기반 이메일 기능을 활용하여 참여 지표 기록을 기반으로 공개 비율, 최적의 전송 시간, 가능한 이탈률을 분석하고 예측하는 것이 좋습니다. <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/testing-and-sending/preparing-and-testing-messages/predictive.html?lang=ko">자세히 알아보기</a></p></br>
     </td> 
  </tr> 
  </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>Experience Cloud 트리거를 사용한 성향 점수</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p><b>성향 점수</b>가 Adobe Experience Cloud 트리거에서 서비스 해제되었습니다. 따라서 이 옵션은 Adobe Campaign Standard에서 제거되었습니다. 데이터 보강 스키마에서 성향 점수의 오래된 값을 방지하려면 최신 변경 사항을 검색하고 기존 트리거를 다시 게시하기 위해 스키마를 업데이트하는 것이 좋습니다. 자세한 내용은 <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/integrating-with-adobe-cloud/working-with-campaign-and-triggers/using-triggers-in-campaign.html?lang=ko">Campaign에서 트리거 게시</a>를 참조하십시오 .
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
   <td> <p>[!DNL Adobe Creative SDK] 이(가) 서비스 해제되었습니다. 따라서 Campaign 20.2 릴리스부터 Campaign Standard 이메일에서 [!DNL Creative SDK] 기반의 이미지 에디션을 더 이상 사용할 수 없습니다.</p></br>
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
   <td> <p>Adobe Campaign과 Adobe Experience Cloud은 2019년 봄 및 Campaign 19.2 릴리스부터 Microsoft Internet Explorer 11에 대한 지원을 중단했습니다. Microsoft Edge 또는 기타 지원되는 브라우저로 전환하십시오. <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/about-configuration-guidelines.html?lang=ko">자세히 알아보기</a></p>
   </td> 
  </tr> 
 </tbody> 
</table>
