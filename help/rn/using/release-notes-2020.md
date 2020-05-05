---
title: 2020년 릴리스 정보
description: 이 페이지에는 Adobe Campaign Standard의 2020개 릴리스가 모두 표시됩니다.
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
source-git-commit: f4c6b74d9b80d80befed65d853cf82b32084c49d

---


# 2020년 릴리스 정보{#release-notes-2020}

[릴리스 계획](https://helpx.adobe.com/kr/campaign/kb/acs-release-planning.html) | [제어판 릴리스](https://docs.adobe.com/content/help/en/control-panel/using/release-notes.html) | [설명서 업데이트](../../rn/using/documentation-updates.md) | [이전 릴리스 노트](../../rn/using/release-notes-2019.md) | [사용되지 않는 기능](https://helpx.adobe.com/kr/campaign/kb/acs-deprecated-and-removed-features.html)

## 릴리스 20.2 - 2020년 4월 {#release-20-2---april-2020}

**새로운 기능?**

<table> 
 <thead> 
  <tr> 
   <th> <strong>Azure Blob 통합</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>이제 Azure Blob 저장소 커넥터를 사용하여 <strong>전송 파일</strong> 워크플로우 활동을 사용하여 데이터를 Adobe Campaign으로 가져오거나 내보낼 수 있습니다. </p>
    <p>자세한 내용은 <a href="../../administration/using/external-accounts.md#microsoft-azure-external-account">자세한 설명서를 참조하십시오</a>.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>타깃팅된 프로파일을 사용한 이메일 테스트</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>이제 테스트 프로필 외에도 실제 타깃팅된 프로필에서 이메일을 테스트할 수 있습니다. 그러면 프로필에서 받게 될 메시지를 정확하게 표현할 수 있습니다. 사용자 정의 필드, 워크플로우 등의 추가 데이터를 비롯한 동적 및 개인화된 정보 </p>
    <p>자세한 내용은 <a href="../../sending/using/testing-messages-using-target.md">자세한 설명서</a> 및 <a href="https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/communication-channels/email/profile-substitution.html">자습서 비디오를 참조하십시오</a>. </p>
   </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Google TXT 레코드 관리, 데이터베이스 공간 모니터링 및 이메일 경고 등 새로운 기능이 4월 캠페인 제어판에서 릴리스됩니다. 이러한 기능에 대한 자세한 내용은 [제어판 릴리스 노트를 참조하십시오](https://docs.adobe.com/content/help/en/control-panel/using/release-notes.html).

**향상된 기능**

* 트랜잭션 메시징 사용자 환경이 개선되었으며 인터페이스 일관성이 개선되었습니다. [자세한 내용](../../channels/using/about-transactional-messaging.md)
* 이제 Campaign Standard에서 워크플로우의 추가 데이터를 사용하여 테스트 프로파일에 교정본을 전송할 수 있습니다.
* 외부 API 활동에 대한 보증서가 업데이트되었습니다. [자세한 내용](../../automating/using/external-api.md)

**향상된 이메일 디자이너**

* 개인화된 이미지에서 여러 번 클릭하면 escape에 영향을 주는 문제를 수정했습니다.
* 동적 텍스트 구성 요소를 복제할 때 잘못된 줄이 중복될 수 있는 문제를 수정했습니다. (CAMP-41249)
* div 수준 대신 표 수준에서 패딩을 정의할 때 Outlook에서 패딩 문제가 해결되었습니다.
* HTML 모드로 전환할 때 이미지의 너비가 수정되는 문제를 해결했습니다. (CAMP-41116)
* 아이콘에 대체 텍스트를 제공할 때 소셜 미디어 구성 요소에 액세스할 수 없는 문제를 해결했습니다. (CAMP-41345)
* 이메일 디자이너에서 복사 붙여넣기를 사용할 때 보이는 `<br>` 태그가 표시되는 문제를 수정했습니다.
* HTML 콘텐츠에서 일반 텍스트로 전환한 후 이메일에 HTML 태그가 표시되는 문제를 해결했습니다. (CAMP-41138)
* 테두리가 하나만 정의된 단추가 렌더링되지 않는 문제를 해결했습니다.
* 이메일의 바닥글이 Microsoft Outlook에서 왼쪽 화면으로 이동하던 HTML 들여쓰기 문제를 수정했습니다. (CAMP-40987)
* HTML에 정의된 컬렉션 속성을 타깃팅하는 개인화 필드가 일반 텍스트 모드로 전환할 때 일반 텍스트 컨텐츠에 복사되는 문제를 해결했습니다. (CAMP-40365)
* 선택한 텍스트 세그먼트에 링크가 삽입되지 않는 문제를 해결했습니다. (CAMP-41406)
* 쿼리 편집기에서 시간대를 선택할 때 날짜가 변경되는 문제를 해결했습니다. (CAMP-38277)

**기타 변경 사항**

* Adobe Analytics **를 사용한** KPI 조정 워크플로우는 이제 하루 동안 실행되는 대신 현재 날짜까지 실행됩니다.
* MCPNS에서는 APNS 및 APNS-SANDBOX 모두를 앱에서 플랫폼으로 추가할 수 없습니다. Adobe Campaign Standard에서 인증서를 추가한 후에는 이제 하나의 APNS 플랫폼(프로덕션 또는 샌드박스)만 MCPNS 앱에 추가할 수 있으므로 설정을 다시 변경할 수 없습니다.

**경험 플랫폼 통합**

>[!NOTE]
>
>Campaign Standard의 Adobe Experience Platform 기능은 현재 베타 버전으로, 예고 없이 수시로 업데이트됩니다. 자세한 설명서를 참조하십시오. [경험 플랫폼 데이터 커넥터](../../developing/using/aep-about-data-connector.md), [대상](../../audiences/using/aep-about-audience-destinations-service.md)

* 이제 워크플로우 로그에서 10분마다 Campaign은 현재 실행 중인 작업에 의해 이미 처리된 레코드 수를 표시합니다.
* 데이터베이스에서 삭제된 Adobe Experience Platform 프로필을 가져올 때 발생할 수 있는 문제를 수정했습니다.
* 가져온 전체 레코드 수에 대해 잘못된 결과를 표시할 수 있는 워크플로우 로그 문제를 해결했습니다.

**패치**

* 별칭 **필드** 에서 공백을 추가한 다음 새 행 항목을 만들 때 발생할 수 있는 데이터 **증가 워크플로우** 활동 문제를 수정했습니다. (CAMP-39229)
* 증명 메시지를 보낼 때 모든 테스트 프로필을 타깃팅할 수 있는 문제를 해결했습니다.
* 이벤트 구성을 게시 취소 및 삭제한 후 발생하는 문제를 수정했습니다. [자세한 내용](../../administration/using/configuring-transactional-messaging.md#deleting-an-event)
* 워크플로우를 변경할 때 **저장** 단추가 사라지는 문제가 해결되었습니다.
* 처리된 후 Campaign에서 개인 정보 요청을 수동으로 삭제할 때 요청 관련 데이터가 정리 후에도 삭제되지 않는 문제를 해결했습니다.
* Adobe Experience Manager의 특수 문자가 포함된 메시지를 미리 보거나 전송할 때 발생할 수 있는 문제를 수정했습니다.
* 여러 인바운드 전환이 있는 활동을 실행할 때 워크플로우에서 발생할 수 있는 문제를 수정했습니다.
* 표준 사용자가 워크플로우 쿼리 또는 전달에서 대상 차원으로 &#39;애플리케이션에 대한 구독&#39;을 사용하지 못하는 문제를 해결했습니다. (CAMP-37618)

## 릴리스 20.1.4 - 2020년 2월 {#release-20-1-4---february-2020}

* 기존 워크플로우에서 대상자 **읽기** 활동을 열 때 발생하는 문제가 해결되었습니다. (CAMP-41002)

## 릴리스 20.1.3 - 2020년 2월 {#release-20-1-3---february-2020}

* CAMP-39273에서 해당 허점을 사용하는 고객을 위해 20.1에 도입된 회귀 문제를 수정했습니다. 캠프-39273은 복귀되었다.

## 릴리스 20.1.2 - 2020년 2월 {#release-20-1-2---february-2020}

**향상된 이메일 디자이너**

* HTML 태그 요소를 패치한 다음 컨텐츠를 저장할 때 오래된 조각에 추가한 문제를 수정했습니다. (CAMP-40685)
* 동적 컨텐츠를 사용할 때 공백이 추가된 문제를 수정했습니다. (CAMP-40605)
* 트랜잭션 이메일 템플릿을 구성할 때 발생하는 문제가 해결되었습니다. (CAMP-40604)

## 릴리스 20.1 - 2020년 2월 {#release-20-1---february-2020}

**새로운 기능?**


<table> 
 <thead> 
  <tr> 
   <th> <strong>Adobe Experience Platform 데이터 커넥터(베타)</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Adobe Experience Platform 데이터 커넥터는 이제 Adobe Campaign Standard와 통합되었습니다. XTK 데이터(Campaign에서 인제스트한 데이터)를 Adobe Experience Platform 데이터 모델(XDM)에 매핑하여 Adobe Experience Platform에서 캠페인 데이터를 사용할 수 있도록 만들 수 있습니다. </p>
    <p>이 기능은 Azure에서 호스팅되는 고객에게만 제공됩니다. 이 기능 및 활성화 조건에 대한 자세한 내용은 <a href="../../developing/using/aep-about-data-connector.md">자세한 설명서</a> 및 <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/adobe-experience-platform-data-connector/understanding-the-adobe-experience-platform-data-connector.html">방법 비디오를 참조하십시오</a>.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>대상 대상(베타) </strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>대상 대상을 사용하면 Adobe Experience Platform에서 Adobe Campaign으로 세그먼트를 공유할 수 있습니다.</p>
    <p>이 기능은 Azure에서 호스팅되는 고객에게만 제공됩니다. 이 기능 및 활성화 조건에 대한 자세한 내용은 <a href="../../audiences/using/aep-about-audience-destinations-service.md">자세한 설명서</a> 및 <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/profiles-and-audiences/audience-destinations/audience-destinations-overview.html">방법 비디오를 참조하십시오</a>. </p>
   </td> 
  </tr> 
 </tbody> 
</table>

**향상된 기능**

* 향상된 MTA의 글로벌 가용성: 메시지(트랜잭션 메시지 포함)는 이제 개선된 전송 인프라를 제공하는 Adobe Campaign Enhanced MTA에 의해 전송되며, 이를 통해 전달 능력, 처리량 및 바운스 처리를 향상시킬 수 있습니다. [자세한 내용](https://helpx.adobe.com/campaign/kb/campaign-enhanced-mta.html)

* 표준 시간대 관리가 향상되었습니다. 이제 전체 워크플로우에 대한 [특정 시간대를](../../automating/using/building-a-workflow.md) 정의할 수 있습니다. 선택한 시간대가 모든 워크플로우의 활동에 적용됩니다. 운영자나 서버에 대해 구성된 시간대에 대한 정보가 이제 인터페이스에 표시됩니다(로그인 및 시간대 선택 후). (CAMP-37672)

* 이제 Campaign Standard API를 사용하여 큰 테이블을 사용할 때 호출 URL에 매개 변수를 추가하여 페이지 매김을 수행할 수 `_forcePagination=true` 있습니다. [자세한 내용](../../api/using/pagination.md)

* 이제 모든 타깃팅 차원에 대한 배달 로그 및 추적 로그 리소스에서 각 로그의 고유 식별자인 배달 로그 ID를 사용할 수 있습니다. 이 기능을 사용하면 내보내기 시 전송 또는 추적 로그를 식별할 수 있습니다. [자세한 내용](../../automating/using/exporting-logs.md)

**향상된 이메일 디자이너**

* 대상을 만들 때 누락된 필수 텍스트 지침이 추가되었습니다.
* 기존 이메일 편집기의 마법사에서 **콘텐츠** 변경 버튼을 클릭할 때 발생하는 문제가 해결되었습니다.
* 서비스 요약 보고서의 컨텐츠와 헤더가 정렬되지 않는 문제를 해결했습니다. (CAMP-38103)
* 제목 라인의 나머지 부분에 영향을 주지 않고 동적 컨텐츠 변형을 삭제할 수 없는 문제를 해결했습니다. (CAMP-40096)
* 제목 라인에서 B 변형을 사용할 때 발생하는 A/B 테스트 문제를 해결했습니다. (CAMP-40327)
* HTML 가져오기 업로드 기능을 사용할 때 파일을 드래그 앤 드롭할 수 없는 문제를 해결했습니다. (CAMP-39326)
* 텍스트 편집기에서 텍스트를 복사하고 붙여넣을 수 없는 문제를 해결했습니다. (CAMP-39028)
* 단어 제안 기능이 표시되지 않던 문제를 수정했습니다. (CAMP-38970)
* 사용자가 조각을 저장할 수 없는 문제를 해결했습니다. (ATU-2447)
* 동적 구조가 중복되지 않는 문제를 해결했습니다. (CAMP-38367)
* 동적 컨텐츠가 중복될 때 조건을 유지할 수 없는 문제를 해결했습니다. (CAMP-39051)

**기타 변경 사항**

* 이제 &quot;준비가 실패한 배달&quot; 필터가 마지막 수정 날짜가 아닌 게재의 생성 날짜를 고려합니다.
* 관리자 보안 그룹의 조직 단위는 더 이상 변경할 수 없습니다.
* 이제 프로필을 만들 때 조직 단위 필드를 채워야 합니다.
* 이제 Experience Cloud 트리거는 연결된 이벤트와 트랜잭션 템플릿이 모두 삭제된 경우에만 삭제할 수 있습니다.
* Adobe Creative SDK가 중단되었습니다. 이제 Campaign Standard에서 더 이상 사용되지 않습니다. 더 이상 사용되지 [않음 및 제거된 기능](https://helpx.adobe.com/kr/campaign/kb/acs-deprecated-and-removed-features.html)페이지를 참조하십시오.


**패치**

* 개인 정보 삭제 요청을 수행할 때 사용자 데이터가 제외 로그에서 삭제되지 않는 문제를 해결했습니다. (CAMP-39003)
* 컨테이너 요소의 텍스트 크기를 조정할 때 접근성 문제가 발생하는 문제를 해결했습니다.
* 사용자가 마케팅 활동에 마우스를 가져가면 나타나는 달력 팝업을 거부할 수 없는 문제를 해결했습니다.
* 데이터가 수정되지 않은 경우에도 단추를 표시했던 **[!UICONTROL External API]** 활동 **[!UICONTROL Confirm]** 문제를 수정했습니다.
* 다른 대상 차원이 있는 쿼리에 **[!UICONTROL Union]** 활동을 사용할 때 발생하는 문제가 해결되었습니다. 전환 데이터에는 기본 세트의 타깃팅 차원에서의 레코드만 표시되었습니다. (CAMP-36831)
* 두 개의 인바운드 활동, 그 중 하나가 제외 활동인 경우 등 특정 컨텍스트에서 **[!UICONTROL Reconciliation]** 활동을 사용할 때 오류가 발생하던 문제를 수정했습니다. (CAMP-37490)
* 테스트 프로필을 선택하고 업데이트할 때 발생할 수 있는 성능 문제를 수정했습니다. (CAMP-37976)
* 랜딩 페이지를 통해 가입 또는 가입 해지 시 오류 페이지를 표시하는 문제를 해결했습니다. (CAMP-37771)
* zip 형식의 콘텐츠를 업로드할 때 HTML에서 참조되는 PNG 파일과 확장자가 대문자로 표시되는 문제가 해결되었습니다. (CAMP-37913)
* 게시에 테스트 프로필을 추가할 때 인앱 메시지가 전송되지 않던 문제를 수정했습니다.
* 외부 API 워크플로우 활동에 연결할 때 실패한 오류가 수정되었습니다.
* SMS 메시지 상태가 잘못 표시되던 문제를 수정했습니다.
* 중복 항목이 다른 API 끝점에 표시되는 사용자 지정 리소스 문제를 해결했습니다.
* 게시 후 랜딩 페이지를 사용할 수 없는 문제를 해결했습니다. (CAMP-38695)
* 서로 다른 두 리소스에서 오는 교차 전환의 데이터를 표시할 때 발생하는 버그를 수정했습니다. (CAMP-38974)
* 배달 템플릿의 열거형 값이 잘못 설정되던 문제를 수정했습니다. (CAMP-38388)
* 게재 상태를 [대기 중]으로 표시하고 [보낸 사람] 상태를 [완료됨]으로 표시하는 이메일 벌크 게재 오류가 수정되었습니다. (CAMP-35355)
* 동적 보고에서 보낸 사람 도메인을 잘못 표시하는 오류를 수정했습니다. (CAMP-33123)
* 동적 보고에서 구독 취소 카운트가 일치하지 않던 문제를 수정했습니다. (CAMP-39949)
* 인앱 메시지를 보낼 때 주소 전송 로그 화면에 표시되지 않는 문제를 해결했습니다.
* SMS 전송 로그가 정확한 바운스 수로 업데이트되지 않는 문제를 해결했습니다. (CAMP-38395)
* 응용 프로그램 구독 게시물 호출에서 푸시 알림 토큰을 업데이트하도록 허용하는 허점을 수정했습니다. (CAMP-39273)
