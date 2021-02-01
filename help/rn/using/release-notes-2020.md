---
solution: Campaign Standard
product: campaign
title: 2020년 릴리스 정보
description: 이 페이지에는 Adobe Campaign Standard의 2020년 릴리스가 모두 나열되어 있습니다.
audience: rn
content-type: reference
topic-tags: campaign-standard-releases
translation-type: tm+mt
source-git-commit: 36e0f6be4dc8c1a6e4b0d8878d190f2abce99fcd
workflow-type: tm+mt
source-wordcount: '5323'
ht-degree: 100%

---


# 2020년 릴리스 정보{#release-notes-2020}

[릴리스 계획](https://helpx.adobe.com/kr/campaign/kb/acs-release-planning.html) | [Campaign 컨트롤 패널 릴리스](https://docs.adobe.com/content/help/ko-KR/control-panel/using/release-notes.html) | [설명서 업데이트](../../rn/using/documentation-updates.md) | [이전 릴리스 정보](../../rn/using/release-notes-2019.md) | [더 이상 사용되지 않는 기능](https://experienceleague.adobe.com/docs/campaign-standard/using/release-notes/deprecated-features.html?lang=ko#release-notes)

![](assets/do-not-localize/cp-icon.png) 활성 프로필 모니터링, 하위 도메인 게재 기능 감사 및 GPG 키 관리가 포함된 **새로운 제어판 6월 릴리스** . [자세히 알아보기](https://docs.adobe.com/content/help/en/control-panel/using/release-notes.html)

![](assets/do-not-localize/cp-icon.png) CNAME과 새로운 데이터베이스 모니터링 기능을 사용하는 도메인 구성이 포함된 **새로운 10월 Campaign 컨트롤 패널 릴리스**. [자세히 알아보기](https://docs.adobe.com/content/help/en/control-panel/using/release-notes.html)

## 릴리스 20.4 - 2020년 10월 {#release-20-4---october-2020}

**새로운 기능**

<table> 
<thead> 
<tr> 
<th> <strong>컨트롤 그룹</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
  <td> <p>이제 <strong>컨트롤 그룹</strong>을 사용하여 대상의 일부를 제외하여 캠페인의 영향을 측정할 수 있습니다. 그러면 메시지를 받은 대상 모집단과 타겟팅되지 않은 연락처의 동작을 비교할 수 있습니다. 전송 로그를 기준으로 향후 캠페인에서 컨트롤 그룹을 타겟팅할 수도 있습니다.
</p>
<p>자세한 내용은 <a href="../../sending/using/control-group.md">세부 설명서</a> 및 <a href="https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/communication-channels/email/control-groups.html?lang=ko#communication-channels">방법 비디오</a>를 참조하십시오.
</p>
</td> 
</tr> 
</tbody> 
</table>

<table> 
<thead> 
<tr> 
<th> <strong>외부 API - OAuth 지원</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
  <td> <p>이제 Adobe Campaign은 <strong>외부 API</strong> 워크플로우 활동에서 인증을 위해 OAuth를 지원합니다. 이 새로운 기능을 통해 OAuth 지원이 필요한 시스템과 통신할 수 있습니다.
</p>
<p>자세한 내용은 <a href="../../automating/using/external-api.md">세부 설명서</a>를 참조하십시오.
</p>
</td> 
</tr> 
</tbody> 
</table>

<table> 
<thead> 
<tr> 
<th> <strong>Journey AI 통합</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
  <td> <p>모든 Adobe Campaign Standard 고객을 위한 Journey AI를 발표하게 되어 매우 기쁘게 생각합니다.</p>
  <p>Journey AI는 고급 ML(기계 학습)을 사용하여 기업이 각 개인의 참여 선호도를 예측하여 고객 경로의 디자인과 게재를 최적화할 수 있도록 합니다.</p>
  <P>Journey AI는 다음 두 가지 ML 기능으로 구성됩니다.</p>
<ul> 
     <li> <strong>예측 참여 점수 책정</strong> - 고객이 선호하는 참여 수준을 지능적으로 식별하여 메시지를 보다 효과적으로 타겟팅하고 개인화하여 전환율과 유지율을 높일 수 있습니다. <a href="https://docs.adobe.com/content/help/ko-KR/campaign-standard-learn/tutorials/communication-channels/email/journey-ai/predictive-engagement-scoring.html">방법 비디오</a>보기</li> 
     <li> <strong>예측 전송 시간 최적화</strong> - 캠페인의 각 개인에게 이메일을 보내는 가장 적합한 시간을 예측하여 참여율을 높이고 이메일 캠페인 ROI를 향상시킬 수 있습니다. <a href="https://docs.adobe.com/content/help/ko-KR/campaign-standard-learn/tutorials/communication-channels/email/journey-ai/predictive-send-time-optimization.html">방법 비디오</a>보기</li>
    </ul>
  <p>Journey AI를 시작하는 방법을 알려면 <a href="../../sending/using/predictive.md">자세한 설명서</a>를 검토하고 계정 담당자에게 문의하십시오. Journey AI는 기존 Campaign 고객에게 무료로 제공되지만 구현 비용은 약 50시간 정도 입니다.</p>
    </td> 
</tr> 
</tbody> 
</table>

**개선 사항**

* **개인 정보 관리**: Campaign 인터페이스 및 API를 통해 사용할 수 있었던 **CPA 옵트아웃** 필드도 이제 개인 정보 핵심 서비스를 통해 지원합니다. 이 필드를 통해 Adobe Campaign 사용자는 소비자가 개인 정보 판매를 선택했는지 여부를 추적할 수 있습니다. [자세히 알아보기](https://helpx.adobe.com/kr/campaign/kb/acs-privacy.html#ccpa)
* **워크플로우 실행 개선 사항**(베타): 워크플로우에 대한 글로벌 이니셔티브의 맥락에서 메모리 관리를 안정화하고, 지연을 줄이고, 실행 중에 워크플로우에서 사용하는 메모리를 최적화하기 위해 일부 주요 사항을 개선했습니다. 이러한 개선 사항은 현재 베타 버전으로 일부 고객에게만 제공됩니다. 2021년 초에 일반 공개할 예정입니다.
* 보안을 개선하기 위해 이제 Campaign은 이메일의 링크를 추적하는 **서명 메커니즘**&#x200B;을 사용합니다.
* iOS 인증서 또는 Android 키를 업로드할 때 **오류 메시지가 더욱 명확해져** 모바일 앱 구성이 향상되었습니다.
* 너무 많은 프로필이 격리 목록에 추가되지 않도록 **SMS 오류 관리** 기능이 향상되었습니다. 이제 기본적으로 SMS 오류가 하드 오류 대신 소프트 오류로 구성됩니다. [이 페이지](https://helpx.adobe.com/kr/campaign/kb/sms-connector-protocol-and-settings.html)를 참조하십시오.

**향상된 이메일 디자이너**

* 사용자 인터페이스와 문서를 완벽하게 연결하는 **새로운 동적 상황별 도움말** 기능을 통해 이메일 디자이너의 사용자 경험을 개선하여 최신 도움말 콘텐츠에 손쉽게 액세스할 수 있습니다.
* 텍스트 버전을 편집할 때 메시지에서 줄바꿈을 제거하는 문제를 수정했습니다. (CAMP-44483)
* HTML 템플릿의 일반 텍스트 버전이 자동으로 생성되어 동기화되지 않는 문제를 수정했습니다. (CAMP-44195)
* 이미지 크기 조정 시 발생할 수 있는 문제를 수정했습니다. 메시지가 전송되면 이미지가 Microsoft Outlook에서 제대로 표시되지 않습니다. (CAMP-44656)
* 단추를 삽입하고 너비를 &quot;자동&quot;으로 설정할 때 발생하는 문제를 수정했습니다. 메시지가 전송되면 단추의 콘텐츠가 완전히 표시되지 않습니다. (CAMP-44560)
* 첨부된 HTML 파일에서 콘텐츠를 업로드할 때 발생하는 문제가 해결되었습니다. 메시지가 Gmail 주소로 전송되면 CSS가 적용되지 않아 렌더링 문제가 발생합니다. (CAMP-44085)
* 콘텐츠 템플릿에서 직접 콘텐츠를 수정했을 때 이전에 메시지에 사용된 콘텐츠 조각이 업데이트되지 않는 문제를 해결했습니다. (CAMP-43973)
* **조각** 검색 창 관련 문제를 수정했습니다. 기존 조각을 검색할 때 검색 창에 결과가 표시되지 않습니다. (CAMP-44223)
* **콘텐츠 블록** 및 **조각** 검색 창과 관련한 문제를 수정했습니다. 검색 창 중 하나를 사용할 때 결과는 **추가 결과 표시...**&#x200B;를 클릭한 경우에만 표시됩니다. (CAMP-44205)
* Microsoft Outlook에서 텍스트와 이미지 간의 패딩이 적용되지 않는 문제를 해결했습니다. (CAMP-45370)
* 조각을 복제할 때 발생하는 문제를 해결했습니다. 조각을 복제한 후 원본 조각에 HTML 라인이 누락됩니다. (CAMP-45207)
* Microsoft Outlook에서 렌더링 문제를 일으킨 오류를 수정했습니다. (CAMP-44749)
* 게재 템플릿에서 **구조 구성 요소** 패딩 수정 시 발생하는 오류를 수정했습니다. CSS 태그가 변경 사항을 전달하지 않아 렌더링 문제를 일으킵니다. (CAMP-45381)
* 이미지를 업로드할 때 발생하는 문제가 해결되었습니다. 이미지 높이가 0으로 자동 설정되어 렌더링 문제가 발생합니다. (CAMP-45366)

**기타 변경 사항**

* **대상 읽기** 활동을 사용하여 Experience Platform 대상을 가져오려고 할 때 오류가 발생하는 경우 재시도 메커니즘이 추가됩니다. (CAMP-43947, CAMP-43366)
* 이제 프로필 또는 엔터티를 만드는 사용자의 조직 단위와 일치하도록 조직 단위가 자동으로 설정됩니다. 조직의 단위를 더 이상 제거하고 비워 둘 수 없습니다.
* 이제 사용자 지정 리소스를 게시할 때 준비 후 확인 팝업이 표시됩니다.
* 사용자 지정 리소스에 실패할 때 표시되는 팝업 메시지가 더 명확해졌습니다.
* 실행 오류를 방지하기 위해 워크플로우의 표현식 편집기가 개선되었습니다. [새 함수](../../automating/using/customizing-workflow-external-parameters.md)를 사용할 수 있습니다. 이 새 함수는 외부 매개 변수를 사용한 워크플로우를 호출한 후 이벤트 변수를 사용할 수 있도록 하는 모든 활동에서 사용할 수 있습니다. 또한 이제 함수 설명과 함께 도구 설명이 표현식 편집기에 표시됩니다.
* [트랜잭션 이벤트 목록에 새 필터가 추가되었습니다. ](../../channels/using/configuring-transactional-event.md#searching-transactional-events) 이 매개 변수를 사용하면 이벤트 수신의 마지막 시간과 해당 상태에 따라 이벤트 구성을 필터링할 수 있습니다.
* 패키지를 내보낼 때 표시되는 로그는 오류가 발생한 경우 발생하는 오류에 대해 보다 구체적이고 자세히 작성되었습니다.
* 이제 메시지를 보낸 후 [추적된 URL](../../sending/using/tracking-messages.md) 목록을 검색, 필터링 및 내보낼 수 있습니다.
* [Adobe Experience Platform Launch와 Campaign 간의 자동 동기화](../../administration/using/configuring-a-mobile-application.md#aepsdk-workflow)는 이제 일반적으로 사용할 수 있으며 기본적으로 활성화됩니다.
* 전송 증명 내보내기를 제거하여 워크플로우 내보내기 패키지의 크기가 최적화되었습니다.
* **파일 전송** 활동에 다운로드한 파일의 크기를 표시하는 새 메시지가 추가되었습니다 .
* 잘못된 세션 토큰에 대한 오류 메시지가 개선되었습니다.
* 이제 새로운 메커니즘으로 추적 이벤트가 프록시에서 추적 로그 및 보고에 추가되지 않습니다.
* 게재 활동에 연결된 데이터 관리 활동을 디버깅하는 데 도움이 되는 새 경고 메시지가 추가되었습니다.
* 보고 작업 공간의 레이블이 개선되었습니다.
* 트랜잭션 메시지에서 기술 개체가 삭제되지 않도록 새 유효성 검사 단계가 추가되었습니다.
* 문제 해결을 개선하기 위해 트랜잭션 메시지의 **실행 목록** 탭에 게재 상태에 대한 새 필터가 추가되었습니다.
* 성능을 향상시키고 실행 시간을 최적화하기 위해 350명 이상의 고객을 위한 사전 분석에서 식별된 표의 사용 상태를 기반으로 사용되지 않는 인덱스가 제거되었습니다. 영향을 받은 표는 다음과 같습니다. nmsaddressStatus, nmscampaign, nmsdelivery, nmslandingpage, nmsprogram, nmsseedmember, nmsseedmember, nmsservice, nmssubhistorcp, nmsaudience, xtworkflow

**패치**

* 추적을 활성화했을 때 푸시 알림 또는 인앱 메시지에 대상 링크를 사용할 수 없는 문제를 수정했습니다.
* 대량 게재에서 트랜잭션 메시지의 높은 우선 순위가 적용되지 않는 문제를 수정했습니다.
* 트랜잭션 이메일에 브랜드를 할당할 수 없는 문제를 수정했습니다. 게시 단계 동안 여러 오류 메시지가 표시될 수 있습니다. (CAMP-44988)
* 숫자 값을 요청하는 필드에 정보가 저장되지 않는 워크플로우 사용자 인터페이스 문제를 해결했습니다. (CAMP-44025)
* 가져오기 템플릿 워크플로우에서 **테스트** 활동을 사용할 때 오류 메시지가 표시되는 문제를 수정했습니다. (CAMP-42910)
* 열거형 필드가 포함된 **대상 읽기** 활동을 사용하고 **조합** 또는 **데이터 보강 활동**&#x200B;에 연결할 때 발생하는 문제를 해결했습니다. (CAMP-42795)
* 기본 제공 세그먼트를 사용하여 보고서에서 데이터를 필터링할 때의 동적 보고서 문제를 해결했습니다. (CAMP-42627)
* **스케줄러 활동**&#x200B;을 오전 12시로 설정할 수 없는 문제를 수정했습니다. (CAMP-42674)
* SMPP 연결이 불안정할 때 SMS 메시지 전송을 방해하는 문제를 해결했습니다. (CAMP-42789)
* 페이지를 새로 고친 후 **준비 중지** 단추가 표시되지 않는 문제를 해결했습니다. (CAMP-42721)
* URL에서 콘텐츠를 가져올 때 핫 클릭 보고서 비율이 표시되지 않는 문제를 해결했습니다. (CAMP-44468)
* 프로필 대체 컨텍스트에서 사용할 프로필을 선택할 때 시간 초과 오류가 표시되는 문제를 해결했습니다. (CAMP-44746)
* 잘못된 링크 정의가 포함된 사용자 지정 리소스를 배포한 후 인스턴스가 작동하지 않는 문제를 해결했습니다. (CAMP-44406)
* 게재를 복사하여 캠페인 템플릿에 붙여넣은 후 빈 연결된 엔터티(유형, 브랜드 등)를 만드는 문제가 해결되었습니다. (CAMP-44765)
* 데이터베이스 충돌 또는 Azure에서 간단한 데이터베이스를 다시 시작하는 경우 게재 준비 테이블을 잘못 처리하여 증명을 보낼 수 없는 문제를 해결했습니다.
* 다국어 콘텐츠로 구성된 게재에서 Experience Manager 콘텐츠가 포함된 링크를 삭제하지 못하는 문제를 해결했습니다. (CAMP-44029)
* 차원을 필터링하려고 할 때 오류 메시지를 표시할 수 있는 동적 보고서의 문제를 수정했습니다.  (CAMP-43097)
* 특정 링크 정의를 포함하는 사용자 지정 리소스로 구성된 인스턴스의 프로필에 액세스하려고 할 때 빈 화면이 표시되는 문제를 수정했습니다. (CAMP-41009)
* **데이터 보강** 활동에서 두 개의 입력 활동이 서로 연결된 두 개의 대상 리소스를 가지고 있는 경우 발생할 수 있는 워크플로우 문제를 수정했습니다. (CAMP-42133)
* **파일 전송** 활동을 사용할 때 가져오기 워크플로우가 반복되는 문제를 수정했습니다. (CAMP-43754)
* 내보낸 로그로 프로필을 만들 때 중복을 고려하지 않는 문제를 수정했습니다. (CAMP-45031)
* Adobe Campaign의 보고서와 PDF 파일로 내보낸 보고서 간에 데이터 불일치가 발생하는 문제를 수정했습니다. (CAMP-43010)
* 함수에서 기존 데이터 필드를 사용할 때 DM 게재 워크플로우가 실패하는 오류를 수정했습니다. (CAMP-42737)
* 트랜잭션 이벤트 및 메시지 템플릿을 포함한 패키지를 가져올 때 발생하는 문제를 해결했습니다. 가져오기 프로세스가 5%에서 중지합니다. (CAMP-42544)
* **데이터 보강** 활동을 수정하고 워크플로우에서 추가 데이터를 추가한 후 오류 (처리할 수 없는 유형 오류)가 발생하는 문제를 수정했습니다. (CAMP-41877)
* 워크플로우 삭제를 방해하는 오류를 수정했습니다. 워크플로우를 삭제해야 로그가 제거됩니다. (CAMP-44144)
* HTML 코드가 있는 랜딩 페이지를 만들 때 발생하는 오류를 수정했습니다. 필수 확인란이 캠페인에서 인식되지 않고 게시된 랜딩 페이지에서 사용할 수 없습니다. (CAMP-44181)
* **대기** 활동을 사용할 때 워크플로우가 반복되는 문제를 수정했습니다. (CAMP-43981)
* 동일한 게재에서 여러 이메일 주소를 여러 번 타겟팅하는 트랜잭션 메시지를 전송할 때 발생하는 문제를 해결했습니다. (CAMP-44202)
* targetData 개인화에 프로필 대체를 사용할 때 발생하는 오류를 수정했습니다. (CAMP-44996)
* 패키지에서 게재 템플릿을 내보낼 때 게재 미리 보기가 실패하는 문제를 해결했습니다. (CAMP-44084)
* 사용자 지정 대상 매핑을 사용할 때 증명을 테스트 프로필로 보낼 수 없는 문제를 수정했습니다. (CAMP-43701)
* **대상 읽기** 활동을 사용하고 **프로필** 이외의 타겟팅 차원으로 구성된 대상을 타겟팅할 때 워크플로우에서 발생하는 오류를 수정했습니다.  (CAMP-41885)
* updateEventsStatus **기술 워크플로우**&#x200B;가 이벤트 내역을 검색하는 데 너무 많은 시간이 소요되었을 때 오류가 발생하는 문제를 해결했습니다(워크플로우가 중지되었을 때). 문제를 해결하기 위해 미사용 &quot;sumQueueTime&quot; 집계 필드를 워크플로우에서 제거했습니다. (CAMP-43920)
* 사용자 지정 리소스를 배포할 때 발생하는 메모리 문제를 해결했습니다. (CAMP-42909)
* 컬렉션에서 속성을 누락하는 트랜잭션 메시지 문제를 해결했습니다. 이제 누락된 모든 속성이 기본값으로 정의되고 페이로드에 포함됩니다. (CAMP-42882)
* 실시간 이벤트 게재 로그를 쿼리할 때 성능에 영향을 주는 문제를 수정했습니다. (CAMP-42759)
* 공유 자산에서 대문자 파일 확장자를 사용할 때 발생하는 오류를 수정했습니다. (CAMP-44159)
* 외부 계정에 대한 연결을 테스트하기 전에 오류 메시지가 표시되는 문제를 해결했습니다. 이제 **연결 테스트** 단추가 외부 계정을 만든 경우에만 표시됩니다.
* 공유로 구성된 인스턴스에서 향상된 MTA를 다시 시작한 후 메시지가 보류 중으로 표시되는 문제를 수정했습니다.
* 활성 프로필 카운트가 유효한 전송된 게재의 수와 일치하지 않는 문제를 해결했습니다.
* 워크플로우 내 쿼리 편집기에서 리소스를 검색할 때 지연될 수 있는 문제를 해결했습니다.
* 사용자 지정 리소스의 **텍스트 검색 옵션에서 고려할 필드 지정**&#x200B;을 선택할 때 발생하는 문제를 해결했습니다. 필드 목록이 비어 있는 경우 사용자 지정 리소스 게시가 실패합니다.
* 대량의 데이터가 있는 사용자 지정 리소스의 개요를 표시할 때 발생하는 성능 문제를 해결했습니다.
* 프로필 대체를 사용하여 게재를 가져올 수 없는 문제를 수정했습니다.
* 프로필 대체를 사용할 때 게재를 예약한 경우 증명을 즉시 보낼 수 없는 문제를 수정했습니다.
* 모바일 애플리케이션용 Android 키를 업로드할 때 발생하는 문제를 해결했습니다. 키를 업로드한 후 나타나는 메시지에 이전 키의 값이 표시됩니다.
* 속성이 없는 컬렉션으로 이벤트 구성을 만든 후 트랜잭션 메시지에서 테스트 프로필을 만들 수 없는 문제를 해결했습니다.
* 집계를 사용하여 새 필터를 만든 후 사용자 지정 리소스에 게시하지 못하는 문제를 수정했습니다.
* Gmail 이미지 프록시로 인해 Gmail 받는 사람에 대한 잘못된 추적 열기 비율이 발생하는 문제를 수정했습니다.
* 패키지를 가져올 때 메모리 부족 오류가 발생하는 문제를 해결했습니다.
* Experience Manager 콘텐츠에 &quot;%20&quot; 문자를 포함한 경로가 있는 경우 Experience Manager 연결 해제 작업이 실패하는 문제를 해결했습니다.
* 워크플로우 활동을 복제할 때 레이블에 발생하는 오류를 수정했습니다.
* **메시지 보내기 시작** 옵션을 선택한 경우 랜딩 페이지에서 트랜잭션 메시지 선택기 문제가 해결되었습니다.
* 게재 상태를 올바른 기본값으로 초기화할 수 없는 트랜잭션 메시지 또는 반복 게재 문제를 수정했습니다. 오류 로그가 향상되었습니다.
* 사용자 지정 필드를 사용하는 프로필 링크가 있는 **애플리케이션에 구독 스키마** (appSubscriptionRcp)를 확장할 때 발생하는 문제를 수정했습니다. 푸시 전송 시간에 영향을 줄 수 있는 인덱스가 자동으로 만들어지지 않습니다. (CAMP-41120)



## 릴리스 20.3 - 2020년 5월 {#release-20-3---may-2020}

**새로운 소식**

<table> 
<thead> 
<tr> 
<th> <strong>태국 개인 정보 보호법(Personal Data Protection Act, PDPA)</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td> <p>태국 개인 정보 보호법(PDPA)은 태국에서 적용되는 데이터 보호 요구 사항을 통합 및 현대화한 새로운 개인 정보 보호법입니다. 이 규정은 해당 국가에 거주하는 데이터 주체의 데이터를 보유하고 있는 Adobe Campaign 고객에게 적용됩니다.</p>
<p>Adobe Campaign에서 이미 사용 가능한 개인 정보 보호 기능(동의 관리, 데이터 보유 설정 및 사용자 역할 등) 이외에도 Adobe는 이 기회를 통해 사용자의 PDPA에 대한 준비를 돕기 위해 추가 기능을 포함하고 있습니다.</p>
<ul>
<li>액세스 권한 및 삭제 권한: Adobe는 GDPR 및 CCPA에 추가된 기능을 활용하고 있습니다. <a href="https://helpx.adobe.com/kr/campaign/kb/acs-privacy.html#righttoaccess">자세히 알아보기</a> </li>
<li><p>개인 정보 보호 요청을 만들 때 개인 정보 보호 핵심 서비스에 PDPA 규정 유형이 추가되었습니다. 이 방법은 모든 액세스 및 삭제 요청에 사용해야 합니다. 액세스 및 삭제 요청에 대한 Campaign API 및 인터페이스는 더 이상 사용되지 않습니다. <a href="../../rn/using/deprecated-features.md">사용이 중단되거나 제거된 기능 문서</a>를 참조하십시오.</p></li>
</ul>
<p><a href="https://docs.adobe.com/content/help/ko-KR/campaign-standard-learn/tutorials/privacy/privacy-overview.html">방법 비디오</a>를 참조하십시오.</p>
</td> 
</tr> 
</tbody> 
</table>

<table> 
<thead> 
<tr> 
<th> <strong>외부 API 활동(GA)</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
  <td> <p><strong>외부 API</strong> 활동이 Beta에서 GA로 전환됩니다. 이 릴리스에서는 JSON 반응형 본문 파서가 더 유연해집니다. 이제 다음을 수행할 수 있습니다.</p>
<ul>
<li>중첩된 JSON을 최대 깊이 10수준으로 구문 분석합니다. </li>
<li>선택한 속성을 JSON의 리프 노드로 구문 분석하고 단일 표의 행으로 병합합니다.</li>
<li>JSON에서 배열 개체를 선택하고 사용할 때 개체 이름을 "data"로 지정하거나 최상위 수준에 둘 필요가 없습니다.</li>
</ul>
<p><strong>주의:</strong> 고객은 워크플로우에서 GA 외부 API 활동으로 <strong>모든 Beta 외부 API 활동을 대체</strong>해야 합니다. 외부 API의 Beta 버전을 사용하는 워크플로우는 20.3에서 작동하지 않습니다.</p>
<p>자세한 내용은 <a href="../../automating/using/external-api.md">세부 설명서</a> 및 <a href="https://docs.adobe.com/content/help/ko-KR/campaign-standard-learn/tutorials/managing-processes-and-data/data-management-activities/external-api-activity.html">방법 비디오</a>를 참조하십시오.</p>
</td> 
</tr> 
</tbody> 
</table>

**추가 기능** (7월 13일부터 시작)

* **AI 기반의 전송 시간 최적화 및 프로필 점수 책정** - 이제 고객 여정의 디자인과 게재를 최적화하여 각 개인의 참여 선호도를 예측할 수 있습니다. Journey AI를 기반으로 하는 Adobe Campaign은 참여 지표 기록을 기반으로 공개 비율, 최적의 전송 시간, 가능한 이탈률을 분석하고 예측합니다. [자세히 알아보기](../../sending/using/predictive.md)
* **브라질의 새로운 개인 정보 보호 규정** - Campaign에서 이미 사용 가능한 개인 정보 보호 기능 외에도 브라질의 LGPD(Lei Geral de Proteçao de Datos)에 쉽게 대처할 수 있도록 도와줍니다. 개인 정보 보호 요청을 만들 때 Adobe 개인 정보 보호 핵심 서비스에 LGPD 규정이 추가되었습니다. [자세히 알아보기](https://helpx.adobe.com/kr/campaign/kb/campaign-privacy-overview.html)

**향상된 기능**

* **접두사** 필드에서 [타겟팅 프로필을 사용하여 메시지 테스트](../../sending/using/testing-messages-using-target.md)에 사용할 수 있는 문자 수가 32자에서 500자로 늘었습니다.
* 한 인스턴스에 게시할 수 있는 최대 실시간 이벤트 수가 350개에서 2000개로 늘었습니다. (CAMP-41608)
* syncWithLaunch 기술 워크플로우를 사용하여 Adobe Launch와 Campaign Standard 간의 동기화가 개선되었습니다. 이 워크플로우를 통해 모든 Adobe Launch 모바일 속성을 자동으로 Adobe Campaign Standard로 가져올 수 있습니다. 자세한 정보는 [이 페이지](../../administration/using/technical-workflows.md)를 참조하십시오.

   Adobe 고객 지원 센터에 티켓을 제출(직접 또는 Adobe 문의를 통해)하여 Campaign 인스턴스에서 syncWithLaunch 기술 워크플로우를 활성화해야 합니다. (CAMP-40082)

**향상된 이메일 디자이너**

* 이제 이메일 디자이너가 엄격한 W3C보다 더 유연한 HTML 서식을 처리할 수 있습니다. (CAMP-42529)
*  콘텐츠 블록의 이미지 옆에 링크가 표시되지 않도록 [클릭 가능한 이미지](../../designing/using/links.md#inserting-a-link) 문제를 수정했습니다. (CAMP-41586)
* 템플릿에서 [추적된 URL](../../designing/using/links.md#about-tracked-urls)에 카테고리를 추가했을 때 랜딩 페이지로 리디렉션되지 않는 문제를 수정했습니다. (CAMP-41537)
* Outlook 내 버튼 패딩 문제를 수정했습니다.
* HTML 태그가 일반 텍스트로 표시되는 문제를 수정했습니다.
* 이제 콘텐츠 블록 검색에 미리 로드된 결과와 서버 검색 결과가 함께 표시됩니다. (CAMP-41870)

**기타 변경 사항**

* 사용자 정의 리소스 게시 인터페이스의 오류 메시지가 명확해졌습니다.
* 사용하지 않는 게재 매핑을 인터페이스에서 제거했습니다.
* 불필요한 관리자 역할을 인터페이스에서 제거했습니다.
* 이제 랜딩 페이지의 체크박스를 필수로 지정할 수 있습니다.
* 다이내믹 보고서의 CSV 파일을 다운로드할 때 200개 행 제한을 제거했습니다. 이제 보고서의 모든 행을 포함할 수 있습니다. (CAMP-40810)
* 다국어 이메일에 대한 기본 언어 목록에 미국 스페인어(ES-US)를 추가했습니다. (CAMP-42279)
* 이제 파일 전송 활동으로 다운로드한 파일은 X일 후 삭제됩니다. 여기서 X는 워크플로우 속성의 **실행** 메뉴 아래에 있는 **일 단위 기록** 필드로 결정됩니다. [자세한 내용](../../automating/using/managing-execution-options.md)

**Experience Platform 통합**

* **대상자 읽기** 활동에서 Adobe [Experience Platform 대상자](../../automating/using/aep-targeting-audiences.md)의 활성화를 개선하여 더 나은 성능과 안정성을 제공합니다. 또한 워크플로우 로그가 활성화 작업에 대해 더욱 명확하고 자세해졌으므로 Adobe Experience Platform 대상자를 읽어올 때 보다 손쉽게 모니터링하고 문제를 해결할 수 있습니다.

**패치**

* 사용자 정의 리소스 게시 작업 중 유령 리소스가 만들어지는 오류를 수정했습니다.
* 프로필 리소스를 사용자 정의 리소스로 확장한 경우 프로필의 마케팅 기록이 표시되지 않는 문제를 수정했습니다. (CAMP-41009)
* 편집기를 열 때 기본 랜딩 페이지 템플릿의 콘텐츠가 프랑스어로 표시되는 문제를 수정했습니다. (CAMP-41639)
* 다이내믹 콘텐츠가 있는 푸시 알림에 이모지가 표시되지 않는 문제를 수정했습니다. (CAMP-40715)
* **중복 제거** 활동 시 아웃바운드 보완 전환 중 하나에 잘못된 세그먼트 코드가 할당될 수 있는 문제를 수정했습니다. (CAMP-41400)
* 예약된 보고서가 삭제되지 않는 오류를 수정했습니다. (CAMP-41302)
* 게재 대시보드와 **게재 요약** 보고서 간에 불일치가 발생하는 문제를 수정했습니다 . (CAMP-41145)
* 다운로드한 보고서에서 문자가 겹쳐 표시되는 문제를 수정했습니다.
* 증명 대체에서 게재 미리 보기가 작동하지 않는 문제를 수정했습니다.
* 인앱 로컬 알림의 사용자 정의 필드를 삭제할 때 발생하는 오류를 수정했습니다.
* 워크플로우의 **종료** 또는 **파일 전송** 활동에서 charIndex 함수가 작동하지 않는 문제를 수정했습니다.
* 워크플로우에서 연결된 타겟 리소스를 포함하는 두 개의 입력 활동과 **데이터 보강** 활동을 함께 사용할 때 발생할 수 있는 문제를 수정했습니다. (CAMP-42133)
* 알 수 없는 함수를 사용할 때 워크플로우가 실행되지 않는 문제를 수정했습니다. (CAMP-41873)
* 워크플로우에서 아웃바운드 전환을 보완하는 여러 **대상자 저장** 활동을 사용하여 대상자를 만들 때 발생할 수 있는 문제를 수정했습니다. (CAMP-39992)
* 트랜잭션 이메일에서 개인화를 사용할 때 데이터 불일치가 발생하는 문제를 수정했습니다. (CAMP-41842)
* 푸시 알림 게재에서 사용자 정의 필드를 삭제할 때 발생하는 문제를 수정했습니다. (CAMP-37586)
* 사용자가 보고서를 변경할 수 없는 오류를 수정했습니다. (CAMP-42505)


CNAME 하위 도메인에 대한 인증서 갱신과 ![](assets/do-not-localize/cp-icon.png) **새 Campaign 컨트롤 패널 5월 릴리스**&#x200B;입니다. [자세히 알아보기](https://docs.adobe.com/content/help/en/control-panel/using/release-notes.html)

## 릴리스 20.2 - 2020년 4월 {#release-20-2---april-2020}

**새로운 소식**

<table> 
 <thead> 
  <tr> 
   <th> <strong>Azure Blob 통합</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>이제 Azure Blob 저장소 커넥터를 사용하여 <strong>파일 전송</strong> 워크플로우 활동을 통해 데이터를 Adobe Campaign으로 가져오거나 내보낼 수 있습니다. </p>
    <p>자세한 내용은 <a href="../../administration/using/external-accounts.md#microsoft-azure-external-account">세부 설명서</a>를 참조하십시오.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>타겟팅된 프로필을 사용한 이메일 테스트</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>이제 테스트 프로필 외에도 실제 타겟팅된 프로필에서 이메일을 테스트할 수 있습니다. 이를 통해 사용자 지정 필드, 워크플로우의 추가 데이터를 포함한 동적 및 개인화된 정보 등 프로필에서 받게 될 메시지를 정확하게 표현할 수 있습니다.  </p>
    <p>자세한 내용은 <a href="../../sending/using/testing-messages-using-target.md">세부 설명서</a> 및 <a href="https://docs.adobe.com/content/help/ko-KR/campaign-standard-learn/tutorials/communication-channels/email/profile-substitution.html">튜토리얼 비디오</a>를 참조하십시오. </p>
   </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Google TXT 레코드 관리, 데이터베이스 공간 모니터링 및 이메일 경고 등 새로운 기능이 4월에 Campaign 컨트롤 패널에서 릴리스됩니다. 이러한 기능에 대한 자세한 내용은 [Campaign 컨트롤 패널 릴리스 정보](https://docs.adobe.com/content/help/en/control-panel/using/release-notes.html)를 참조하십시오.

**향상된 기능**

* 트랜잭션 메시지 사용자 경험이 향상되었으며 인터페이스 일관성이 개선되었습니다. [자세한 내용](../../channels/using/getting-started-with-transactional-msg.md)
* 이제 Campaign Standard에서 워크플로우의 추가 데이터를 사용하여 테스트 프로필에 증명을 전송할 수 있습니다.
* 외부 API 활동에 대한 보호 기능이 업데이트되었습니다. [자세한 내용](../../automating/using/external-api.md)

**향상된 이메일 디자이너**

* 개인화된 이미지를 여러 번 클릭하면 이스케이프에 영향을 주는 문제를 수정했습니다.
* 동적 텍스트 구성 요소를 복제할 때 잘못된 줄이 복제되는 문제를 수정했습니다. (CAMP-41249)
* div 수준 대신 테이블 수준에서 패딩을 정의할 때 발생하는 Outlook 패딩 문제를 수정했습니다.
* HTML 모드로 전환할 때 이미지 너비가 수정되는 문제를 수정했습니다. (CAMP-41116)
* 아이콘에 대체 텍스트를 제공할 때 소셜 미디어 구성 요소에 액세스할 수 없는 문제를 수정했습니다. (CAMP-41345)
* 이메일 디자이너에서 복사 붙여넣기를 사용할 때 보이는 `<br>` 태그가 표시되는 문제를 수정했습니다.
* HTML 콘텐츠에서 일반 텍스트로 전환한 후 이메일에 HTML 태그가 표시되는 문제를 수정했습니다. (CAMP-41138)
* 테두리가 하나만 정의된 버튼이 렌더링되지 않는 문제를 수정했습니다.
* Microsoft Outlook에서 이메일의 바닥글이 왼쪽 화면으로 이동하는 HTML 들여쓰기 문제를 수정했습니다. (CAMP-40987)
* HTML로 정의된 컬렉션 속성을 타겟팅하는 개인화 필드가 일반 텍스트 모드로 전환할 때 일반 텍스트 콘텐츠로 복사되는 문제를 수정했습니다. (CAMP-40365)
* 선택한 텍스트 세그먼트에 링크가 삽입되지 않는 문제를 수정했습니다. (CAMP-41406)
* 쿼리 편집기에서 시간대를 선택할 때 날짜가 변경되는 문제를 수정했습니다. (CAMP-38277)

**기타 변경 사항**

* 이제 **Adobe Analytics를 통한 KPI 조정** 워크플로우는 하루 동안 실행되는 대신 현재 날짜까지 실행됩니다.
* MCPNS에서는 APNS 및 APNS-SANDBOX 모두를 앱의 플랫폼으로 추가할 수 없습니다. 이제 Adobe Campaign Standard에서 인증서를 성공적으로 추가한 후에는 MCPNS 앱에 하나의 APNS 플랫폼(프로덕션 또는 샌드박스)만 추가할 수 있으므로 설정을 다시 변경할 수 없습니다.

**Experience Platform 통합**

>[!NOTE]
>
>현재 Campaign Standard의 Adobe Experience Platform 기능은 Beta 버전으로, 사전 통지 없이 수시로 업데이트될 수 있습니다. 세부 설명서 [Experience Platform 데이터 커넥터](../../developing/using/aep-about-data-connector.md), [대상자 대상](../../audiences/using/aep-about-audience-destinations-service.md)을 참조하십시오. 

* 이제 Campaign은 워크플로우 로그에서 10분마다 현재 실행 중인 작업에 의해 이미 처리된 레코드 수를 표시합니다.
* 데이터베이스에서 삭제된 Adobe Experience Platform 프로필을 가져올 때 발생할 수 있는 문제를 수정했습니다.
* 가져온 전체 레코드 수에 대해 잘못된 결과를 표시하는 워크플로우 로그 문제를 수정했습니다.

**패치**

* **별칭** 필드에 공백을 추가한 다음 새 행 항목을 만들 때 발생할 수 있는 **데이터 보강** 워크플로우 활동 문제를 수정했습니다. (CAMP-39229)
* 증명 메시지를 보낼 때 모든 테스트 프로필을 타겟팅하는 문제를 수정했습니다.
* 이벤트 구성을 게시 취소하고 삭제한 후 발생하는 문제를 수정했습니다. [자세한 내용](../../channels/using/publishing-transactional-event.md#deleting-an-event)
* 워크플로우를 변경할 때 **저장** 버튼이 사라지는 문제를 수정했습니다.
* 개인 정보 보호 요청을 처리한 후 Campaign에서 수동으로 삭제할 때 발생하고 정리 후에도 요청과 관련된 데이터가 삭제되지 않도록 방지되는 문제를 수정했습니다.
* Adobe Experience Manager에서 특수 문자가 포함된 메시지를 미리 보거나 전송할 때 발생할 수 있는 문제를 수정했습니다.
* 여러 인바운드 전환이 있는 활동을 실행할 때 워크플로우에서 발생할 수 있는 문제를 수정했습니다.
* 표준 사용자가 워크플로우 쿼리 또는 게재에서 타겟 차원으로 &#39;애플리케이션 구독&#39;을 사용하지 못하는 문제를 수정했습니다. (CAMP-37618)

## 릴리스 20.1.4 - 2020년 2월 {#release-20-1-4---february-2020}

* 기존 워크플로우에서 **대상자 읽기** 활동을 열 때 발생하는 문제를 수정했습니다. (CAMP-41002)

## 릴리스 20.1.3 - 2020년 2월 {#release-20-1-3---february-2020}

* 루프홀을 사용하는 고객을 위해 CAMP-39273의 20.1에 소개한 회귀 문제를 수정했습니다. CAMP-39273이 복귀되었습니다.

## 릴리스 20.1.2 - 2020년 2월 {#release-20-1-2---february-2020}

**향상된 이메일 디자이너**

* HTML 태그 요소를 패치한 다음 콘텐츠를 저장할 때 오래된 조각에 추가되는 문제를 수정했습니다. (CAMP-40685)
* 다이내믹 콘텐츠를 사용할 때 공백이 추가되는 문제를 수정했습니다. (CAMP-40605)
* 트랜잭션 이메일 템플릿을 구성할 때 발생하는 문제를 수정했습니다. (CAMP-40604)

## 릴리스 20.1 - 2020년 2월 {#release-20-1---february-2020}

**새로운 소식**


<table> 
 <thead> 
  <tr> 
   <th> <strong>Adobe Experience Platform 데이터 커넥터(Beta)</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>이제 Adobe Experience Platform 데이터 커넥터가 Adobe Campaign Standard와 통합되었습니다. XTK 데이터(Campaign에서 수집한 데이터)를 Adobe Experience Platform 데이터 모델(XDM)에 매핑하여 Adobe Experience Platform에서 캠페인 데이터를 사용할 수 있도록 만들 수 있습니다. </p>
    <p>이 기능은 Azure에서 호스팅되는 고객에게만 제공됩니다. 이 기능 및 활성화 조건에 대한 자세한 내용은 <a href="../../developing/using/aep-about-data-connector.md">상세 설명서</a> 및 <a href="https://docs.adobe.com/content/help/ko-KR/campaign-standard-learn/tutorials/administrating/adobe-experience-platform-data-connector/understanding-the-adobe-experience-platform-data-connector.html">방법 비디오</a>를 참조하십시오.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>대상자 대상(Beta) </strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>대상자 대상을 사용하면 Adobe Experience Platform에서 Adobe Campaign으로 세그먼트를 공유할 수 있습니다.</p>
    <p>이 기능은 Azure에서 호스팅되는 고객에게만 제공됩니다. 이 기능 및 활성화 조건에 대한 자세한 내용은 <a href="../../audiences/using/aep-about-audience-destinations-service.md">상세 설명서</a> 및 <a href="https://docs.adobe.com/content/help/ko-KR/campaign-standard-learn/tutorials/profiles-and-audiences/audience-destinations/audience-destinations-overview.html">방법 비디오</a>를 참조하십시오. </p>
   </td> 
  </tr> 
 </tbody> 
</table>

**향상된 기능**

* 향상된 MTA의 글로벌 가용성: 이제 메시지(트랜잭션 메시지 포함)는 개선된 전송 인프라를 제공하는 Adobe Campaign Enhanced MTA에 의해 전송되며, 이를 통해 게재 능력, 처리량 및 반송 처리를 향상시킬 수 있습니다. [자세한 내용](https://helpx.adobe.com/kr/campaign/kb/campaign-enhanced-mta.html)

* 시간대 관리가 향상되었습니다. 이제 전체 워크플로우에 대한 [특정 시간대](../../automating/using/building-a-workflow.md)를 정의할 수 있습니다. 선택한 시간대가 모든 워크플로우의 활동에 적용됩니다. 이제 운영자나 서버에 대해 구성된 시간대에 대한 정보가 인터페이스에 표시됩니다(로그에, 시간대를 선택한 후 표시). (CAMP-37672)

* 이제 Campaign Standard API를 사용하여 호출 URL에 `_forcePagination=true` 매개 변수를 추가하여 큰 테이블을 사용할 때 페이지 매김을 수행할 수 있습니다. [자세한 내용](../../api/using/pagination.md)

* 이제 모든 타겟팅 차원에 대한 게재 로그 및 추적 로그 리소스에서 각 로그의 고유 식별자인 게재 로그 ID를 사용할 수 있습니다. 예를 들어 내보내기 시 전송 또는 추적 로그를 식별할 수 있습니다. [자세한 내용](../../automating/using/exporting-logs.md)

**향상된 이메일 디자이너**

* 대상자를 만들 때 누락된 필수 텍스트 지침이 추가되었습니다.
* 기존 이메일 편집기 마법사에서 **콘텐츠 변경** 버튼을 클릭할 때 발생하는 문제를 수정했습니다.
* 서비스 요약 보고서의 콘텐츠와 헤더가 정렬되지 않는 문제를 수정했습니다. (CAMP-38103)
* 제목 줄의 나머지 부분에 영향을 주지 않고 다이내믹 콘텐츠 변형을 삭제되지 않도록 하는 문제를 수정했습니다. (CAMP-40096)
* 제목 줄에서 B 변형을 사용할 때 발생하는 A/B 테스트 문제를 수정했습니다. (CAMP-40327)
* HTML 가져오기 업로드 기능을 사용할 때 파일을 끌어서 놓지 못하는 문제를 수정했습니다. (CAMP-39326)
* 텍스트 편집기에서 텍스트를 복사하고 붙여넣을 수 없는 문제를 수정했습니다. (CAMP-39028)
* 단어 제안 기능이 표시되지 않는 문제를 수정했습니다. (CAMP-38970)
* 사용자가 조각을 저장하지 못하는 문제를 수정했습니다. (ATU-2447)
* 동적 구조가 복제되지 않는 문제를 수정했습니다. (CAMP-38367)
* 다이내믹 콘텐츠를 복제할 때 조건을 유지할 수 없는 문제를 수정했습니다. (CAMP-39051)

**기타 변경 사항**

* 이제 &quot;준비에 실패한 게재&quot; 필터는 마지막 수정 날짜가 아닌 게재의 생성 날짜를 고려합니다.
* 관리자 보안 그룹의 조직 단위는 더 이상 변경할 수 없습니다.
* 이제 프로필을 만들 때 조직 단위 필드를 채워야 합니다.
* 이제 Experience Cloud 트리거는 연결된 이벤트 및 트랜잭션 템플릿이 모두 삭제된 경우에만 삭제할 수 있습니다.
* [!DNL Adobe Creative SDK]이(가) 서비스 해제되었습니다. 이제 Campaign Standard에서 더 이상 사용되지 않습니다. [더 이상 사용되지 않는 기능 및 제거된 기능](../../rn/using/deprecated-features.md) 페이지를 참조하십시오.


**패치**

* 개인 정보 보호 요청 삭제를 수행할 때 사용자 데이터가 제외 로그에서 삭제되지 않는 문제를 수정했습니다. (CAMP-39003)
* 컨테이너 요소에서 텍스트 크기를 조정할 때 발생하는 접근성 문제를 수정했습니다.
* 마케팅 활동에 마우스를 가져가면 나타나는 캘린더 팝업을 사용자가 닫을 수 없는 문제를 수정했습니다.
* 데이터가 수정되지 않은 경우에도 **[!UICONTROL Confirm]** 버튼을 표시했던 **[!UICONTROL External API]** 활동의 문제를 수정했습니다.
* 다른 타겟 차원이 있는 쿼리에 **[!UICONTROL Union]** 활동을 사용할 때 발생하는 문제를 수정했습니다. 전환 데이터는 기본 집합의 타겟팅 차원의 레코드만 표시합니다. (CAMP-36831)
* 두 개의 인바운드 활동이 있고 그 중 하나가 제외 활동인 경우 등 특정 컨텍스트에서 **[!UICONTROL Reconciliation]** 활동을 사용할 때 오류가 발생하던 문제를 수정했습니다. (CAMP-37490)
* 테스트 프로필을 선택하고 업데이트할 때 발생하는 성능 문제를 수정했습니다. (CAMP-37976)
* 랜딩 페이지를 통해 구독 또는 구독 취소 시 오류 페이지를 표시하는 문제를 수정했습니다. (CAMP-37771)
* zip 포맷의 콘텐츠를 업로드할 때 HTML에서 참조되는 PNG 파일과 확장자가 대문자로 표시되는 문제를 수정했습니다. (CAMP-37913)
* 게재에 테스트 프로필을 추가할 때 인앱 메시지가 전송되지 않는 문제를 수정했습니다.
* 데이터 보강 활동에 연결할 때 실패하는 외부 API 워크플로우 활동 오류를 수정했습니다.
* SMS 메시지 상태가 잘못 표시되는 문제를 수정했습니다.
* 다른 API 엔드포인트에 중복 항목이 표시되는 사용자 지정 리소스 문제를 수정했습니다.
* 게시 후 랜딩 페이지를 사용할 수 없는 문제를 수정했습니다. (CAMP-38695)
* 서로 다른 두 리소스에서 온 교차 전환에서 데이터를 표시할 때 발생하는 버그를 수정했습니다. (CAMP-38974)
* 게재 템플릿의 열거형 값이 잘못 설정되는 문제를 수정했습니다. (CAMP-38388)
* 게재 상태를 보류 중으로 표시하고 전송 상태를 완료로 표시하는 이메일 대량 게재 오류를 수정했습니다. (CAMP-35355)
* 동적 보고에서 발신자 도메인을 잘못 표시하는 오류를 수정했습니다. (CAMP-33123)
* 동적 보고에서 구독 취소 카운트가 일치하지 않는 문제를 수정했습니다. (CAMP-39949)
* 인앱 메시지를 보낼 때 전송 로그 화면에 주소가 표시되지 않는 문제를 수정했습니다.
* SMS 전송 로그가 정확한 반송 수로 업데이트되지 않는 문제를 수정했습니다. (CAMP-38395)
* 애플리케이션 구독 게시물 호출에서 푸시 알림 토큰을 업데이트하도록 허용하는 루프홀을 수정했습니다. (CAMP-39273)
