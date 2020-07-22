---
title: 사용되지 않는 Campaign Standard 및 제거된 기능
description: 이 페이지에는 Adobe Campaign Standard의 사용 중단되거나 제거된 기능이 나열됩니다.
page-status-flag: never-activated
uuid: null
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: rn
content-type: reference
topic-tags: campaign-standard-deprecated-features
discoiquuid: null
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 2d4b1ba38a7aa33d1fff3415d71080e370cb80f4
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 1%

---


# 사용 중단되거나 제거된 기능 {#deprecated-and-removed-features}

Adobe는 항상 이전 버전과의 호환성을 신중하게 고려하여 전반적인 고객 가치를 향상시키기 위해 보다 현대적인 대체 요소로 대체해야 하는 기존 기능을 식별하기 위해 제품 기능을 지속적으로 평가합니다.

Campaign Standard 기능을 제거/교체하기 위해 다음 규칙이 적용됩니다.

* 사용 중단 발표가 우선입니다. 더 이상 사용되지 않는 기능을 기존 사용자도 사용할 수 있지만 더 이상 향상된 기능 또는 문서화된 기능은 사용할 수 없습니다.
* 더 이상 사용되지 않는 기능은 빠른 시일 내에 다음 릴리스에서 제거됩니다. 제거에 대한 실제 타겟 날짜가 이 페이지에 표시되어 있습니다.

이 프로세스를 통해 고객은 실제 제거하기 전에 새로운 버전이나 더 이상 사용되지 않는 기능의 후속 버전에 맞게 구현을 조정할 수 있는 릴리스 주기를 적어도 하나 이상 확보할 수 있습니다.

>[!NOTE]
>Adobe Campaign Standard 릴리스 및 새 기능은 릴리스 [노트에 나와 있습니다](../../rn/using/release-notes.md).


## 더 이상 사용되지 않는 기능 {#deprecated-features}

이 섹션에는 최신 Campaign Standard 릴리스에서 더 이상 사용되지 않는 것으로 표시된 기능 및 기능이 나열됩니다.

일반적으로 향후 릴리스에서 제거될 예정인 기능은 먼저 가치가 하락하도록 설정되며, 여기에 대체 요소가 제공됩니다. 이러한 기능과 기능은 새 Campaign Standard 고객에게 더 이상 제공되지 않거나 새로운 구현에 사용되어서는 안됩니다. 또한 제품 설명서에서 제거됩니다.

고객은 현재 배포에서 기능/기능을 사용하는지 검토하고 제공된 대체 요소를 사용하도록 구현을 변경할 계획을 수립하는 것이 좋습니다. 환경 및 프로젝트 업데이트를 계획하려면 대상 제거 버전을 참조하십시오.

<table> 
 <thead> 
  <tr> 
   <th> <strong>SDK v4를 사용한 푸시 알림</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p> 20.1 릴리스부터 SDK v4는 더 이상 사용되지 않습니다. <a href="https://aep-sdks.gitbook.io/docs/version-4-sdk-end-of-support-faq">자세한</a>내용</p><br/>
   <p>Adobe Experience Platform <a href="https://aep-sdks.gitbook.io/docs/">Mobile SDK</a> (이전 v5라고도 함)는 향후 출시될 Adobe Experience Cloud 기능 및 기능을 독점적으로 지원합니다.</p></br>
     <p>
     <em>Target 제거 날짜: 2020년 9월 30일</em></p>
     </td> 
  </tr> 
 </tbody> 
</table>
<table> 
 <thead> 
  <tr> 
   <th> <strong>개인 정보 요청 - 캠페인 API 및 인터페이스</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Campaign 19.4 릴리스를 시작하면 액세스 및 삭제 요청에 대해 캠페인 API와 인터페이스를 사용하는 것이 더 이상 사용되지 않습니다. 2단계 프로필 삭제는 사용할 수 없습니다. Adobe <a href="https://www.adobe.io/apis/experiencecloud/gdpr.html">Privacy Core Service를 사용하십시오</a>.</p></br>
   <p>Campaign Standard <a href="https://helpx.adobe.com/campaign/kb/acs-privacy.html">의 개인 정보 관리를 참조하십시오</a>.</p>
  <p> 
  <em>Target 제거 날짜: 2021년</em></p>
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
   <td> <p>Campaign 19.0 릴리스를 시작하면 기존 이메일 편집기는 더 이상 사용되지 않습니다. 새로운 이메일 디자이너 <a href="https://docs.adobe.com/content/help/en/campaign-standard/using/designing-content/designing-content-in-adobe-campaign.html">를</a> 사용하여 이메일 컨텐츠를 만들고 개인화합니다. </p></br>
   <p>새로운 편집기에 맞게 이메일 템플릿을 적용하는 방법을 살펴보려면 <a href="https://docs.adobe.com/content/help/en/campaign-standard/using/designing-content/building-email-content/using-existing-content.html">이 섹션을</a> 참조하십시오.</p></br>
  <p> 
  <em>Target 제거 날짜: 2021년</em></p>
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
   <td> <p>18.7 릴리스를 시작으로 지리적 단위는 더 이상 사용되지 않습니다. 조직 및 지리적 단위는 Campaign의 동일한 구문입니다. 사용자는 조직의 단위만 사용하여 사용자 권한/데이터 액세스 계층 구조를 만들어야 합니다. <a href="https://helpx.adobe.com/campaign/standard/administration/using/organizational-units.html">자세한</a>내용 지리학적 단위가 만들어지지 않은 기존 인스턴스는 물론 새 Campaign Standard 인스턴스는 18.7 릴리스부터 이 기능을 구현할 수 없습니다.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

## 제거된 기능 {#removed-features}

이 섹션에는 Campaign Standard에서 제거된 기능과 기능이 나열됩니다.

<table> 
 <thead> 
  <tr> 
   <th> <strong>Campaign Standard을 위한 Creative SDK</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Adobe Creative SDK가 중단되었습니다. 따라서 Campaign Standard 이메일에 포함된 Creative SDK에서 제공하는 이미지 에디션은 Campaign 20.2 릴리스부터 더 이상 사용할 수 없습니다.</p></br>
   </td> 
  </tr> 
 </tbody> 
</table>

## 호환성 끝 {#end-of-compatibility}

<table> 
 <thead> 
  <tr> 
   <th> <strong>Microsoft Internet Explorer 11</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Adobe Campaign 및 Adobe Experience Cloud는 2019년 봄 및 Campaign 19.2 릴리스에서 Microsoft Internet Explorer 11에 대한 지원을 중단했습니다. Microsoft Edge 또는 다른 지원 브라우저로 전환하십시오. <a href="https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/about-configuration-guidelines.html#compatible-browsers">자세한</a>내용</p>
   </td> 
  </tr> 
 </tbody> 
</table>
