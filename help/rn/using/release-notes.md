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
source-git-commit: c4500832b87e986cdbbbf72b9b8c0591f64f7da8

---


# 최신 릴리스{#latest-release}

[릴리스 계획](https://helpx.adobe.com/campaign/kb/acs-release-planning.html) | [제어판 릴리스](https://docs.adobe.com/content/help/en/control-panel/using/release-notes.html) | [설명서 업데이트](../../rn/using/documentation-updates.md) | [이전 릴리스 노트](../../rn/using/release-notes-2019.md) | [더 이상 사용되지 않는 기능](https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html)

## 릴리스 20.2 - 2020년 3월 {#release-20-2---march-2020}

**새로운 기능?**

<table> 
 <thead> 
  <tr> 
   <th> <strong>Azure Blob 통합</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>이제 Azure Blob 저장소 커넥터를 사용하여 파일 <strong>전송 워크플로 활동을 사용하여 데이터를 Adobe Campaign으로 가져오거나 내보낼</strong> 수 있습니다. </p>
    <p>자세한 내용은 <a href="../../administration/using/external-accounts.md#microsoft-azure-external-account">자세한 설명서를</a>참조하십시오.</p>
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
   <td> <p>이제 테스트 프로필 외에도 실제 타깃팅된 프로필에서 이메일을 테스트할 수 있습니다. 이렇게 하면 프로필에서 받을 메시지를 정확하게 표현할 수 있습니다.사용자 정의 필드, 동적 및 개인화된 정보, 워크플로우 등의 추가 데이터 포함 </p>
    <p>자세한 내용은 <a href="../../sending/using/testing-messages-using-target.md">자세한 설명서</a> 및 <a href="https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/communication-channels/email/profile-substitution.html">자습서 비디오를</a>참조하십시오. </p>
   </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Google TXT 레코드 관리, 데이터베이스 공간 모니터링 및 이메일 경고 등 새로운 기능이 4월에 캠페인 제어판에서 릴리스됩니다. 이러한 기능에 대한 자세한 내용은 제어판 릴리스 [노트를 참조하십시오](https://docs.adobe.com/content/help/en/control-panel/using/release-notes.html).

**향상된 기능**

* 트랜잭션 메시징 사용자 환경이 개선되었으며 인터페이스 일관성이 개선되었습니다. [자세한 내용](../../channels/using/about-transactional-messaging.md)
* 이제 Campaign Standard에서 워크플로우의 추가 데이터를 사용하여 테스트 프로파일에 교정본을 전송할 수 있습니다.
* 외부 API 활동에 대한 가드레일이 업데이트되었습니다. [자세한 내용](../../automating/using/external-api.md)

**향상된 이메일 디자이너**

* 개인화된 이미지에서 여러 번 클릭하면 escape에 영향을 주는 문제를 수정했습니다.
* 동적 텍스트 구성 요소를 복제할 때 잘못된 줄이 중복될 수 있는 문제를 수정했습니다. (CAMP-41249)
* div 수준 대신 표 수준에서 패딩을 정의할 때 Outlook 패딩 문제가 해결되었습니다.
* HTML 모드로 전환할 때 이미지의 너비가 수정되는 문제를 해결했습니다. (CAMP-41116)
* 아이콘에 대체 텍스트를 제공할 때 소셜 미디어 구성 요소에 액세스할 수 없는 문제를 해결했습니다. (CAMP-41345)
* 이메일 디자이너에서 복사 붙여넣기를 사용할 때 보이는 `<br>` 태그가 표시되는 문제를 수정했습니다.
* HTML 콘텐츠에서 일반 텍스트로 전환한 후 이메일에 HTML 태그가 표시되는 문제를 해결했습니다. (CAMP-41138)
* 테두리가 하나만 정의된 단추가 렌더링되지 않는 문제를 해결했습니다.
* Microsoft Outlook에서 전자 메일 바닥글이 왼쪽 화면으로 이동하던 HTML 들여쓰기 문제를 수정했습니다. (CAMP-40987)
* HTML에 정의된 컬렉션 속성을 타깃팅하는 개인화 필드가 일반 텍스트 모드로 전환할 때 일반 텍스트 컨텐츠에 복사되는 문제를 해결했습니다. (CAMP-40365)
* 선택한 텍스트 세그먼트에 링크가 삽입되지 않는 문제를 해결했습니다. (CAMP-41406)
* 쿼리 편집기에서 시간대를 선택할 때 날짜가 변경되는 문제를 해결했습니다. (CAMP-38277)

**기타 변경 사항**

* Adobe **Analytics와의** 기본 조정 워크플로우는 이제 하루 동안 실행되는 대신 현재 날짜까지 실행됩니다.
* MCPNS는 APNS 및 APNS-SANDBOX 모두를 앱에서 플랫폼으로 추가할 수 없도록 지원합니다. Adobe Campaign Standard에서 인증서를 성공적으로 추가한 후 이제 하나의 APNS 플랫폼(프로덕션 또는 샌드박스)만 MCPNS 앱에 추가할 수 있으므로 설정을 다시 변경할 수 없습니다.

**경험 플랫폼 통합**

>[!NOTE]
>
>Campaign Standard의 Adobe Experience Platform 기능은 현재 베타 버전으로, 예고 없이 자주 업데이트될 수 있습니다. 자세한 설명서를 참조하십시오.Experience [Platform 데이터 커넥터](../../administration/using/aep-about-data-connector.md), [대상](../../audiences/using/aep-about-audience-destinations-service.md)

* 이제 워크플로우 로그에서 10분마다 Campaign은 현재 실행 중인 작업에 의해 이미 처리된 레코드 수를 표시합니다.
* 데이터베이스에서 삭제된 Adobe Experience Platform 프로필을 가져올 때 발생할 수 있는 문제를 수정했습니다.
* 가져온 전체 레코드 수에 대해 잘못된 결과를 표시할 수 있는 워크플로우 로그 문제를 해결했습니다.

**패치**

* 별칭 **필드에 공백을 추가한 다음** 새 행 항목을 만들 때 발생할 수 **있는** 데이터강화 워크플로우 활동 문제를 수정했습니다. (CAMP-39229)
* 증명 메시지를 보낼 때 모든 테스트 프로필을 타깃팅할 수 있는 문제를 해결했습니다.
* 이벤트 구성을 게시 취소 및 삭제한 후 발생하는 문제를 수정했습니다. [자세한 내용](../../administration/using/configuring-transactional-messaging.md#deleting-an-event)
* 워크플로우를 변경할 때 **저장** 단추가 사라지는 문제를 수정했습니다.
* Campaign이 처리된 후 Campaign에서 개인 정보 요청을 수동으로 삭제할 때 정리 후에도 요청에 연결된 데이터가 삭제되지 않는 문제를 해결했습니다.
* Adobe Experience Manager의 특수 문자가 포함된 메시지를 미리 보거나 전송할 때 발생할 수 있는 문제를 수정했습니다.
* 여러 인바운드 전환이 있는 활동을 실행할 때 워크플로우에서 발생할 수 있는 문제를 수정했습니다.