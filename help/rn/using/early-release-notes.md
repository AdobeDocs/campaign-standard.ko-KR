---
title: 초기 릴리스 정보
description: 초기 릴리스 정보
feature: Overview
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 4b10eb63-3fea-438e-a1a7-25fbf7b0e5b0
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 100%

---

# 초기 릴리스 정보 {#new-release}

이 페이지에서는 다음 Campaign Standard 릴리스에 포함된 새로운 기능, 개선 사항 및 문제 해결에 대해 설명합니다.

>[!CAUTION]
>
> 이 콘텐츠는 단계 환경 업그레이드일까지 사전 통지 없이 변경될 수 있습니다. 자세한 내용은 [릴리스 계획 페이지](../../rn/using/release-planning.md)를 참조하세요.

## 릴리스 21.3 - 2021년 9월 {#release-21-3---sept-2021}


**새로운 기능**


<table> 
<thead> 
<tr> 
<th> <strong>통합 Experience Cloud 인터페이스</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td>
<p>Adobe Campaign 헤더 막대를 변경하여 모든 Experience Cloud 제품과 서비스의 환경을 통합하고 개선합니다. 이러한 변경 사항은 다음과 같은 작업을 보다 쉽게 할 수 있도록 마련되었습니다.</p>
<ul>
<li>조직 간 또는 다른 애플리케이션으로 손쉽게 전환할 수 있습니다.</li>
<li>향상된 사용자 도움말 - Experience League를 제품에 적용하면 검색 결과에 커뮤니티 포럼, 더 많은 비디오 콘텐츠 등이 포함되어 더 많은 콘텐츠에 손쉽게 액세스하고 애플리케이션을 최대한 활용할 수 있습니다. 또한 도움말 메뉴에 바로 피드백 메커니즘을 추가하여 문제를 보고하거나 아이디어를 손쉽게 공유할 수 있습니다.</li>
<li>향상된 알림 - 이제 알림 드롭다운에는 2개의 탭 즉, 제품 알림과 더 많은 글로벌 제품 공지가 있습니다.</li>
</ul>
<!--<p>For more information refer to the <a href="../../start/using/interface-description.md#top-bar">detailed documentation</a>.
</p>-->
</td> 
</tr> 
</tbody> 
</table>

<table> 
<thead> 
<tr> 
<th> <strong>감사 추적</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td>
<p>새로운 감사 추적 기능은 Adobe Campaign 내에서 발생하는 작업 및 이벤트의 포괄적인 목록을 실시간으로 캡처합니다. 기능에는 다음과 같은 질문에 답변할 수 있도록 데이터 기록에 액세스하는 셀프서비스 방법이 포함되어 있습니다.</p>
<ul>
<li>이 워크플로우에 무슨 일이 발생했으며, 마지막으로 업데이트한 사람은 누구입니까?</li>
<li>마지막으로 변경한 사람은 누구입니까?</li>
<li>이전 상태는 무엇이었습니까?</li>
</ul>
<p>이제 Adobe Campaign은 워크플로우, 옵션, 사용자 정의 리소스에 대해 생성, 편집, 삭제 작업을 감사합니다. 이러한 항목의 수정 사항 역시 추적됩니다.</p>
<!--<p>For more information refer to the <a href="../../administration/using/audit.md">detailed documentation</a>.
</p>-->
</td> 
</tr> 
</tbody> 
</table>


<table> 
<thead> 
<tr> 
<th> <strong>워크플로우 진단 모드</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td>
<p>이제 진단 모드에서 Campaign 워크플로우를 실행할 수 있습니다. 이 모드는 실행 문제를 해결하는 데 도움이 되는 정보를 기록합니다. 워크플로우 쿼리가 기본적으로 1분 이상 걸리는 경우 전체 실행 플랜이 기록됩니다.</p>
<!--<p>For more information refer to the <a href="../../administration/using/audit.md">detailed documentation</a>.
</p>-->
</td> 
</tr> 
</tbody> 
</table>

**개선 사항**

* 워크플로우에서 Adobe Experience Manager 컨텐츠에 연결된 반복 게재를 만들 때 이제 전송 전에 컨텐츠 승인 상태를 확인합니다.
* 이제 데이터베이스 연결 제한이 연결 오류를 방지하기 위해 Campaign 패키지와 일치합니다.
* 사용자 지정 리소스에서 인덱스를 만드는 동안 일관성 검사를 추가하고 오류 메시지를 개선했습니다.

**패치**

* URL에서 이메일 콘텐츠를 가져올 때 시간이 초과되는 오류를 수정했습니다. (CAMP-49054)
* 책갈피가 지정된 URL에 액세스하거나 브라우저에서 페이지를 새로 고칠 때 세션 종료에 의해 발생하는 오류(-69)를 수정했습니다. (CAMP-49003, CAMP-48930, CAMP-48894)
* 기존 게재 가능성 서버에서 새 게재 가능성 서버로 규칙을 동기화할 때 발생하는 문제를 수정했습니다. (CAMP-48923)
* 이메일 Designer에서 HTML 태그가 있는 이메일 템플릿을 로드할 때 발생하는 문제를 수정했습니다. (CAMP-48243)
