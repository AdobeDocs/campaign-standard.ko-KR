---
title: 최신 릴리스
description: 이 페이지에는 Adobe Campaign Standard의 모든 최신 릴리스가 표시됩니다.
page-status-flag: never-activated
uuid: 1cf2e40c-beca-43db-8261-a1820ee86ad3
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: rn
content-type: reference
topic-tags: campaign-standard-releases
discoiquuid: 5c7bfb74-4002-4ffe-87e8-bddb41d34b41
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 4a3a6930609ab27949d77ccc8a73d9a3a62edb98

---


# 최신 릴리스{#latest-release}

[릴리스 계획](https://helpx.adobe.com/campaign/kb/acs-release-planning.html) | [제어판 릴리스](https://docs.adobe.com/content/help/en/control-panel/using/release-notes.html) | [설명서 업데이트](../../rn/using/documentation-updates.md) | [이전 릴리스 노트](../../rn/using/release-notes-2019.md) | [더 이상 사용되지 않는 기능](https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html)

## 릴리스 20.1.3 - 2020년 2월 {#release-20-1-3---february-2020}

* CAMP-39273에서 해당 허점을 사용하는 고객을 위해 20.1에 도입된 회귀 문제를 수정했습니다. CAMP-39273은 되돌려졌습니다.

## 릴리스 20.1.2 - 2020년 2월 {#release-20-1-2---february-2020}

**향상된 이메일 디자이너**

* 패치를 적용한 다음 컨텐츠를 저장할 때 오래된 조각에 HTML 태그 요소를 추가한 문제를 수정했습니다. (CAMP-40685)
* 동적 컨텐츠를 사용할 때 공백이 추가되는 문제를 수정했습니다. (CAMP-40605)
* 트랜잭션 이메일 템플릿을 구성할 때 발생하는 문제를 수정했습니다. (CAMP-40604)

## 릴리스 20.1 - 2020년 2월 {#release-20-1---february-2020}

**새로운 기능**


<table> 
 <thead> 
  <tr> 
   <th> <strong>Adobe Experience Platform Data Connector(베타)</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Adobe Experience Platform 데이터 커넥터는 이제 Adobe Campaign Standard와 통합되었습니다. XTK 데이터(캠페인에서 인화된 데이터)를 Adobe Experience Platform 데이터 모델(XDM)에 매핑하여 Adobe Experience Platform에서 캠페인 데이터를 사용할 수 있도록 만들 수 있습니다. </p>
    <p>이 기능은 Azure에서 호스팅된 고객만 사용할 수 있습니다. 이 기능 및 활성화 조건에 대한 자세한 내용은 <a href="../../administration/using/aep-about-data-connector.md">자세한 설명서</a> 및 <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/adobe-experience-platform-data-connector/understanding-the-adobe-experience-platform-data-connector.html">방법 비디오를</a>참조하십시오.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>대상(베타) </strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>대상 대상을 사용하면 Adobe Experience Platform에서 Adobe Campaign으로 세그먼트를 공유할 수 있습니다.</p>
    <p>이 기능은 Azure에서 호스팅된 고객만 사용할 수 있습니다. 이 기능 및 활성화 조건에 대한 자세한 내용은 <a href="../../audiences/using/aep-about-audience-destinations-service.md">자세한 설명서</a> 및 <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/profiles-and-audiences/audience-destinations/audience-destinations-overview.html">방법 비디오를</a>참조하십시오. </p>
   </td> 
  </tr> 
 </tbody> 
</table>

**향상된 기능**

* 향상된 MTA의 글로벌 가용성:메시지(트랜잭션 메시지 포함)는 이제 Adobe Campaign Enhanced MTA에서 전송되며, 이 MTA는 향상된 전달 능력, 처리량 및 바운스 처리를 가능하게 해주는 업그레이드된 전송 인프라를 제공합니다. [자세한 내용](https://helpx.adobe.com/campaign/kb/campaign-enhanced-mta.html)

* 시간대 관리가 향상되었습니다. 이제 전체 워크플로우에 대한 [특정 시간대를](../../automating/using/building-a-workflow.md) 정의할 수 있습니다. 선택한 시간대가 모든 워크플로우의 활동에 적용됩니다. 운영자나 서버에 대해 구성된 시간대에 대한 정보가 이제 인터페이스에 표시됩니다(로그인 및 시간대 선택 후). (CAMP-37672)

* 이제 Campaign Standard API를 사용하여 큰 테이블을 사용할 때 호출 URL에 매개 변수를 추가하여 페이지 매김을 수행할 수 `_forcePagination=true` 있습니다. [자세한 내용](../../api/using/pagination.md)

* 이제 배달 로그 ID(각 로그의 고유 식별자)를 모든 타깃팅 차원에 대한 배달 로그 및 추적 로그 리소스에서 사용할 수 있습니다. 이렇게 하면 내보내기 시 전송 또는 추적 로그를 식별할 수 있습니다. [자세한 내용](../../automating/using/exporting-logs.md)

**향상된 이메일 디자이너**

* 대상을 만들 때 누락된 필수 텍스트 지침을 추가했습니다.
* 기존 이메일 편집기의 마법사에서 **컨텐츠** 변경 버튼을 클릭할 때 발생하는 문제가 해결되었습니다.
* 서비스 요약 보고서의 컨텐츠와 헤더가 정렬되지 않는 문제를 해결했습니다. (CAMP-38103)
* 제목 라인의 나머지 부분에 영향을 주지 않고 동적 컨텐츠 변형을 삭제하지 못했던 문제를 수정했습니다. (CAMP-40096)
* 제목 라인에서 B 변형을 사용할 때 A/B 테스트 문제가 해결되었습니다. (CAMP-40327)
* HTML 가져오기 업로드 기능을 사용할 때 파일을 드래그 앤 드롭하지 못했던 문제를 수정했습니다. (CAMP-39326)
* 텍스트 편집기에서 텍스트를 복사하고 붙여넣을 수 없는 문제를 해결했습니다. (CAMP-39028)
* 단어 제안 기능이 표시되지 않는 문제를 해결했습니다. (CAMP-38970)
* 사용자가 조각을 저장하지 못했던 문제를 수정했습니다. (ATU 파섹
* 동적 구조가 중복되지 않는 문제를 해결했습니다. (CAMP-38367)
* 동적 컨텐츠가 중복될 때 조건을 유지할 수 없는 문제를 해결했습니다. (CAMP-39051)

**기타 변경 사항**

* 이제 &quot;준비가 실패한 배달&quot; 필터가 마지막 수정 날짜가 아닌 게재의 생성 날짜를 고려합니다.
* 관리자 보안 그룹의 조직 단위는 더 이상 변경할 수 없습니다.
* 이제 프로필을 만들 때 조직 단위 필드를 채워야 합니다.
* 이제 Experience Cloud 트리거는 연결된 이벤트와 트랜잭션 템플릿이 모두 삭제된 경우에만 삭제할 수 있습니다.

**패치**

* 개인 정보 삭제 요청을 수행할 때 사용자 데이터가 제외 로그에서 삭제되지 않는 문제를 해결했습니다. (CAMP-39003)
* 컨테이너 요소의 텍스트 크기를 조정할 때 액세서빌러티 문제가 발생하는 문제를 해결했습니다.
* 사용자가 마케팅 활동에 마우스로 표시되던 달력 팝업을 닫지 못하게 하는 문제를 수정했습니다.
* 데이터가 수정되지 않았을 때에도 단추를 표시했던 **[!UICONTROL External API]** 활동 **[!UICONTROL Confirm]** 문제를 수정했습니다.
* 다른 대상 차원이 있는 쿼리에 **[!UICONTROL Union]** 활동을 사용할 때 발생하는 문제를 수정했습니다. 전환 데이터는 기본 세트의 타깃팅 차원인 레코드만 표시했습니다. (CAMP-36831)
* 두 개의 인바운드 활동(하나는 제외 활동)과 같이 특정 컨텍스트에서 **[!UICONTROL Reconciliation]** 활동을 사용할 때 오류가 발생하던 문제를 수정했습니다. (CAMP-37490)
* 테스트 프로필을 선택하고 업데이트할 때 발생할 수 있는 성능 문제를 수정했습니다. (CAMP-37976)
* 랜딩 페이지를 통해 가입 또는 가입 해지 시 오류 페이지를 표시하는 문제를 해결했습니다. (CAMP-37771)
* zip 형식의 콘텐트를 업로드할 때 HTML에서 참조되는 PNG 파일과 확장자가 대문자로 표시되는 문제가 해결되었습니다. (CAMP-37913)
* 테스트 프로필을 게시에 추가할 때 인앱 메시지가 전송되지 않던 문제를 수정했습니다.
* 외부 API 워크플로우 활동에 연결할 때 실패했던 오류를 수정했습니다.
* SMS 메시지 상태가 잘못 표시되던 문제를 수정했습니다.
* 사용자 지정 리소스로 인해 중복된 항목이 다른 API 끝점 아래에 표시되는 문제가 해결되었습니다.
* 게시 후 랜딩 페이지를 사용할 수 없는 문제를 수정했습니다. (CAMP-38695)
* 서로 다른 두 리소스에서 오는 교차 전환의 데이터를 표시할 때 발생하는 버그를 수정했습니다. (CAMP-38974)
* 배달 템플릿의 열거형 값이 잘못 설정되는 문제를 해결했습니다. (CAMP-38388)
* 게재 상태를 [보류 중]으로 표시하고 [전송됨] 상태를 [완료됨]으로 표시하는 이메일 벌크 게재 오류가 수정되었습니다. (CAMP-35355)
* 동적 보고에서 보낸 사람 도메인을 잘못 표시하던 오류를 수정했습니다. (CAMP-33123)
* 동적 보고에서 구독 취소 카운트가 일치하지 않던 문제를 수정했습니다. (CAMP-39949)
* 인앱 메시지를 보낼 때 주소 전송 로그 화면에 표시되지 않는 문제를 해결했습니다.
* SMS 전송 로그가 올바른 바운스 수로 업데이트되지 않는 문제를 해결했습니다. (CAMP-38395)
* 응용 프로그램 구독 게시물 호출이 푸시 알림 토큰을 업데이트하도록 하는 허점을 해결했습니다. (CAMP-39273)
