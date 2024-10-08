---
title: 2021년 릴리스 노트
description: 이 페이지에는 Adobe Campaign Standard의 2021년 릴리스가 모두 나열되어 있습니다.
audience: rn
content-type: reference
topic-tags: campaign-standard-releases
feature: Overview
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 225c65cc-2964-4b71-84a9-30fcd22d75bf
source-git-commit: 63cd437c5a19791ffb9d3c0b8690ee1532a4774d
workflow-type: tm+mt
source-wordcount: '4695'
ht-degree: 100%

---

# 2021년 릴리스 정보{#release-notes-2021}

## 릴리스 21.3 - 2021년 9월 {#release-21-3---sept-2021}

최신 Campaign Standard 릴리스에 포함된 새로운 기능, 개선 사항, 수정 사항은 아래 목록에서 확인할 수 있습니다.

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
<p>자세한 내용은 <a href="../../start/using/interface-description.md#top-bar">세부 설명서</a>를 참조하십시오.
</p>
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
<li>이 워크플로에 무슨 일이 발생했으며, 마지막으로 업데이트한 사람은 누구입니까?</li>
<li>마지막으로 변경한 사람은 누구입니까?</li>
<li>이전 상태는 무엇이었습니까?</li>
</ul>
<p>이제 Adobe Campaign은 워크플로, 옵션, 사용자 정의 리소스에 대해 생성, 편집, 삭제 작업을 감사합니다. 이러한 항목의 수정 사항 역시 추적됩니다.</p>
<p>자세한 내용은 <a href="../../administration/using/audit.md">세부 설명서</a>를 참조하세요.</p>
</td> 
</tr> 
</tbody> 
</table>


<table> 
<thead> 
<tr> 
<th> <strong>워크플로 진단 모드</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td>
<p>이제 진단 모드에서 Campaign 워크플로를 실행할 수 있습니다. 이 모드는 실행 문제를 해결하는 데 도움이 되는 정보를 기록합니다. 워크플로 쿼리가 기본적으로 1분 이상 걸리는 경우 전체 실행 플랜이 기록됩니다.</p>
<p>자세한 내용은 <a href="../../automating/using/managing-execution-options.md">세부 설명서</a>를 참조하십시오.</p>
</td> 
</tr> 
</tbody> 
</table>

**보안 개선 사항**

* SSRF 공격으로부터 보호하기 위해 보안이 강화되었습니다. (CAMP-47836)
* 이제 사용자 목록은 관리자만 사용할 수 있습니다. (CAMP-47260)
* 환경 변수는 URL에서 매개 변수 확장의 일부로 더 이상 사용할 수 없습니다. (CAMP-47268)

**개선 사항**

* 워크플로에서 Adobe Experience Manager 컨텐츠에 연결된 반복 게재를 만들 때 이제 전송 전에 컨텐츠 승인 상태를 확인합니다.
* 이제 데이터베이스 연결 제한이 연결 오류를 방지하기 위해 Campaign 패키지와 일치합니다.
* 사용자 지정 리소스 발행에서 새로운 일관성 검사를 수행하면 사용자가 중복 인덱스를 만들지 못하며, 이로 인해 발행에 실패합니다. 필요한 경우 개선된 오류 메시지가 사용자에게 색인의 이름을 바꾸도록 요청합니다. [자세히 알아보기](../../developing/using/updating-the-database-structure.md#publishing-a-custom-resource)

**기타 변경 사항**

* Adobe Experience Platform 데이터 커넥터 및 Audience Destinations 서비스는 이제 Campaign Standard에서 더 이상 사용되지 않습니다. 이러한 기능을 사용하는 경우 Adobe Sources and Destinations로 이동하고 구현을 조정해야 합니다. [자세히 알아보기](../../integrating/using/get-started-sources-destinations.md)
* 사용이 중단되거나 제거된 기능은 [이 페이지](deprecated-features.md)의 목록에서 확인할 수 있습니다.
* 문자열 유형 열의 값을 연결하는 &#39;StringAgg&#39; 합계 함수를 새로 도입했습니다. (CAMP-47077) [자세히 알아보기](../../automating/using/list-of-functions.md#aggregates)
* **게재 지표 업데이트**(updateDeliveryIndicators) 기술 워크플로가 개선되어 성능이 향상되었습니다.
* 이제 Campaign Standard에서 지원되는 모든 언어에 인앱 메시지 템플릿을 사용할 수 있습니다.
* 게재 분석 중에 추적 서버로 전송되는 호출 수를 줄여 게재 준비 시간을 트랜잭션 메시지에 최적화했습니다.
* 새 경고 메시지는 사용자에게 높은 바운스 비율을 알려줍니다.
* 추적 로그를 올바르게 검색하지 못할 때 더 쉽게 디버깅할 수 있도록 로그 오류 메시지 및 경고가 개선되었습니다. (CAMP-48939, CAMP-47360)
* 이제 도메인 이름을 포함하여 URL을 완전히 개인화할 수 있습니다. [자세히 알아보기](../../designing/using/personalization.md#personalizing-urls)
* 이제 [동적 보고서]의 게재 성과 계산에서 증명 및 트랩 프로필을 제외합니다. (CAMP-47338)

**패치**

* URL에서 이메일 콘텐츠를 가져올 때 시간이 초과되는 오류를 수정했습니다. (CAMP-49054)
* 책갈피가 표시된 URL에 액세스하거나 브라우저에서 페이지를 새로 고칠 때 세션 종료에 의해 발생하는 오류(-69)를 수정했습니다. (CAMP-49003, CAMP-48930, CAMP-48894)
* 기존 게재 가능성 서버에서 새 게재 가능성 서버로 규칙을 동기화할 때 발생하는 문제를 수정했습니다. (CAMP-48923)
* 이메일 Designer에서 HTML 태그가 있는 이메일 템플릿을 로드할 때 발생하는 문제를 수정했습니다. (CAMP-48243)
* 이메일 디자이너를 사용하여 트랜잭션 메시지를 만들 때 Adobe Experience Manager 콘텐츠가 로드되지 않는 오류를 수정했습니다. (CAMP-49075)
* 상단 표시줄과 콘텐츠 사이에 패딩이 너무 많이 추가되는 인터페이스의 문제를 수정했습니다.
* Adobe Experience Manager 콘텐츠에서 Campaign 콘텐츠 블록을 사용할 때 발행 오류가 발생할 수 있는 트랜잭션 메시지 관련 문제를 수정했습니다. (CAMP-49233)
* 인증이 실패했을 때 오류 메시지가 표시되는 문제를 해결했습니다. 이제 사용자가 로그인 페이지로 리디렉션됩니다.
* 토큰 표시 문제로 인해 사용자가 보고서를 편집하거나 공유하지 못하는 문제를 수정했습니다.
* 1-n 테이블 관계가 있는 필터 표현식을 사용하여 사용자 지정 리소스를 게시하는 동안 발생하는 문제를 수정했습니다. (CAMP-48740)
* 날짜 형식 문제로 인해 워크플로 전환에서 게재 연락처 날짜가 검색되지 않는 문제를 해결했습니다. (CAMP-48871)
* 사용자 지정 프로필 차원을 만드는 동안 로그 전송 확장이 되지 않는 문제를 수정했습니다.
* 여러 언어 변형이 포함된 게재의 실패를 유발할 수 있는 문제를 해결했습니다. 이제부터 사용자가 기본 언어 변형을 삭제하는 경우 언어 사본을 만들기 전에 다른 언어 변형을 기본 언어 변형으로 설정해야 합니다. (CAMP-48235)
* 메시지를 디자인할 때 사용자가 **모바일 장치에만 표시** 옵션을 선택한 경우 Outlook에서 이메일 메시지에 공백이 추가로 표시되는 문제를 해결했습니다. (CAMP-48902)
* 증분 쿼리 워크플로를 실행한 후 **처리된 데이터** 탭에서 증분 쿼리 활동 필드의 마지막 실행 날짜가 누락되는 문제를 해결했습니다. (CAMP-48879)
* **세분화** 워크플로 활동에서 동적 세그먼트 코드를 제대로 정의하지 못하는 문제를 해결했습니다. (CAMP-48727)
* 워크플로를 편집한 후 저장하려고 할 때 무작위로 발생하는 오류를 수정했습니다. (CAMP-48695)
* 트리거의 삭제 후에도 트리거의 데이터 스키마가 남아 있어 사용자 지정 리소스를 게시하지 못하는 문제를 해결했습니다. (CAMP-48523)
* InMail 프로세스에서 게재 로그를 검색하여 업데이트할 수 없기 때문에 피드백 루프 요청이 허용되지 않는 문제를 해결했습니다. (CAMP-48705)
* **제외** 워크플로 활동에서 제외 옵션을 제대로 정의하지 못하는 문제를 해결했습니다.(CAMP-48355)
* 워크플로의 강화 활동이 서비스 구독 또는 구독 취소와 관련된 경우 발생하는 문제를 수정했습니다. 이 문제로 인해 충돌이 발생했습니다.
* 워크플로가 실행되지 않는 문제를 해결했습니다.
* 사용자가 사용자 인터페이스에서 기본 제공 보안 그룹의 이름을 변경하거나 삭제하지 못하는 문제를 해결했습니다.
* 사용자가 불완전한 이벤트 발행 작업을 삭제하지 못하는 문제를 해결했습니다.
* 오류로 인해 데이터베이스 정리 워크플로가 실패하는 문제를 해결했습니다. (CAMP-49097)


## 릴리스 21.2 - 2021년 6월 {#release-21-2---june-2021}

다음 Campaign Standard 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항은 아래에 나열됩니다. 이번 Campaign Standard 릴리스에 포함된 새로운 기능, 개선 사항 및 버그 해결 내역은 아래에 나와 있습니다.

**개선 사항**

* 이제 랜딩 페이지를 디자인할 때 양식을 제출하기 전에 프로필이 선택해야 하는 필수 확인란을 추가할 수 있습니다. 자세한 내용은 [세부 설명서](../../channels/using/managing-landing-page-form-data.md#agreement-checkbox)를 참조하세요.

* 트리거 통합 시 트리거 페이로드에서 들어오는 조정 데이터가 없을 때 표시되는 오류 메시지를 개선했습니다. 이제 &quot;페이로드에서 별칭 데이터가 누락되었습니다.&quot;라는 메시지가 표시됩니다.

* 대기열에서 푸시 알림을 검색할 때의 성능을 개선했습니다.

**기타 변경 사항**

* 일부 유효하며 서명이 있는 추적 링크를 서드 파티 보안 도구에서 수정한 후 해당 링크가 잘못 차단되는 문제를 방지하기 위해 링크 추적에 대한 URL 서명 메커니즘을 비활성화했습니다.

* 다중 변형 게재에서 기본 변형이 삭제된 경우 사용자는 더 이상 언어 사본을 만들 수 없습니다. 이제 언어 사본 작성 시 메시지가 표시됩니다. (CAMP-48235)

* 2단계 프로필 삭제 프로세스(Campaign 19.4 릴리스부터 지원 종료)가 이제 기본적으로 비활성화됩니다. 이전에는 개인 정보 보호 핵심 서비스를 사용하기 전에 Campaign 인터페이스에서 수동으로 비활성화해야 했으며, 이렇게 하지 않으면 삭제 요청이 완료되지 않고 보류 중인 상태로 유지되었습니다.

* 동적 보고서에서 **증명 제외** 세그먼트가 제거되었습니다. (CAMP-46161)

* Campaign 애플리케이션에서 platformPrincipal 값 없이 iOS 인증서를 업로드할 때 사용자에게 알리는 경고 메시지를 새로 추가했습니다.

* 이제 이메일의 최대 용량이 100MB로 기본 설정됩니다. 이 제한을 통해 이메일 용량을 무한정 늘려 시스템 충돌을 야기할 수 있는 오류를 방지합니다. (CAMP-47445) [자세히 알아보기](../../sending/using/design-and-personalize.md#email-size)

* 이제 Standard 사용자는 에셋 핵심 서비스와 이메일 디자이너 통합을 사용할 수 있습니다.

* v4 푸시 애플리케이션에서 v5 푸시 애플리케이션으로의 성공적인 마이그레이션을 확인하는 메시지를 새로 추가했습니다.

* 이제 Campaign Standard API에 인증하기 위해 JSONWeb 토큰을 만들 때 제품 프로필을 **고려**&#x200B;합니다. 즉, 보안 그룹에 할당된 조직 단위 및 역할(AdobeIO의 제품 프로필과 일치)이 Campaign Standard Rest API 호출에 필요한 IMS 기술 계정에 적용됩니다. (CAMP-47479)

**패치**

* 일괄 처리 프로세스 로그 테이블(**xtkjoblog**)에 대한 만료 옵션이 적용되지 않는 문제를 해결했습니다. 이 버그로 인해 테이블이 올바르게 삭제되지 않는 문제가 있었습니다.

* **세분화** 워크플로 활동에서 필터 순서를 변경할 수 없는 문제를 해결했습니다. (CAMP-48357)

* null 값 오류로 인해 게재가 실패할 수 있는 20.4의 회귀 문제를 해결했습니다. (CAMP-48591)

* **공유** 및 **지금 보고서 보내기** 또는 **보고서 보내기 예약** 메뉴를 통해 보고서를 보낼 수 없는 문제를 해결했습니다. (CAMP-47798)

* Gmail 계정에서 받은 추적 이벤트 필터링으로 인해 Gmail의 확인율을 잘못 표시할 수 있는 회귀 문제를 해결했습니다. (CAMP-46504)

* Adobe Campaign Standard의 보고서와 Adobe Analytics의 보고서 간 데이터 불일치로 이어지는 다양한 문제를 해결했습니다. (CAMP-47671, CAMP-47296)

* 준비에 실패한 후 게재 로그에 액세스할 수 없는 문제를 해결했습니다. (CAMP-48296)

* 사용자 정의 보고서를 편집, 삭제 또는 전송하려고 할 때 오류 메시지가 표시되는 문제를 해결했습니다. (CAMP-47789, CAMP-47798)

* 새 사용자 정의 리소스를 만들고 **동기화 안 함** 옵션을 활성화하면 API 호출이 실패하는 문제를 해결했습니다. (CAMP-48014)

* **동기화 안 함** 옵션이 활성화된 사용자 정의 리소스가 재초안 또는 삭제된 스키마를 참조할 수 있는 문제가 해결되었습니다. 이 문제로 인해 사용자 정의 리소스를 게시할 때 오류가 발생했습니다.

* 동일한 외부 계정에서 여러 짧은 코드를 사용할 때 발생하는 SMS 옵트아웃 문제를 해결했습니다.

* 데이터베이스를 게시한 후 새 게재 경고 기준에 액세스할 수 없는 문제(&quot;액세스하려는 리소스에 연결할 수 없음&quot;)를 해결했습니다. (CAMP-48221)

* 동적 보고가 있는 일부 Campaign 인스턴스에서 추적 로그가 누락되는 문제를 해결했습니다. 이 누락된 추적 로그를 복원하기 위해 새로운 [기술 워크플로](../../administration/using/technical-workflows.md)를 추가했습니다. (CAMP-47885)

* 동적 보고서에 게재 데이터가 표시되지 않던 문제를 해결했습니다. 보고서가 0으로 설정되어 있었습니다. (CAMP-47480)

* 서버 JavaScript HTTP 클라이언트가 외부 URL에 연결할 수 없는 문제를 해결했습니다.

* 워크플로의 내부 이름을 변경한 후 **증분 쿼리** 활동을 재설정하는 문제를 해결했습니다. 이 문제는 날짜 필드가 증분 모드로 사용되었을 때 발생했습니다. (CAMP-47674)

* Adobe Experience Manager 통합으로 다국어 이메일을 만들 때 게재 요약에 미리 보기 썸네일이 표시되지 않는 문제를 해결했습니다. 이 문제는 **언어 사본 작성** 버튼을 사용하여 이메일 변형을 만들 때 발생했습니다. (CAMP-47810)

* 사용자가 이메일 또는 SMS 하위 게재에서 상위 게재에 액세스할 수 없는 문제를 해결했습니다. (CAMP-47986)

* 사용자 정의 이벤트가 누락된 REST API를 통해 트랜잭션 메시지를 전송할 때 CPU 및 메모리 사용량이 초과되는 문제를 해결했습니다. (CAMP-47147)

* 경우에 따라 실시간 메시지가 전송되지 않는 트랜잭션 메시지 API 관련 오류를 해결했습니다.

* **보고서 보내기 예약** 옵션을 사용한 후에 보고서를 받을 수 없는 문제를 해결했습니다. (CAMP-48583, CAMP-47786)

* **지금 보고서 보내기 옵션**&#x200B;을 사용한 후에 받은 보고서가 불완전하고 데이터가 누락되어 있는 문제를 해결했습니다. (CAMP-48583)

* 이메일 디자이너에서 이미지를 업로드할 때 이미지의 치수가 줄어드는 문제를 해결했습니다. (CAMP-47017)

* 게재를 만들 때 사용 가능한 모든 Experience Manager 템플릿이 표시되지 않는 문제를 해결했습니다. (CAMP-48132)

* 보낸 게재의 요약 페이지에 있는 Campaign 링크가 사용자를 관련 캠페인으로 리디렉션하지 못하는 오류를 해결했습니다. (CAMP-48012)

* 이메일 디자이너에서 에셋을 선택하려고 할 때 에셋 핵심 서비스 통합이 계속 실패하는 문제를 해결했습니다. (CAMP-47446)

* Journey Orchestration에서 이벤트를 통해 전송한 정확한 값(즉, 00으로 끝나는 값)의 타임스탬프를 Campaign이 지원하지 않아 일부 Journey Orchestration 게재가 실패하는 문제를 해결했습니다.

## 릴리스 21.1 - 2021년 2월 {#release-21-1---february-2021}

**새로운 기능**

<table> 
<thead> 
<tr> 
<th> <strong>이메일 피드백 서비스</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td>
<p>EFS(이메일 피드백 서비스)는 Enhanced MTA의 피드백을 바로 캡처하여 보고 정확도를 향상하는 확장 가능한 서비스입니다. 이 기능은 개인 베타 버전으로 출시되며 모든 고객은 향후 릴리스에서 점진적으로 사용할 수 있습니다.</p>
<ul>
<li>이제 완벽하고 정밀한 보고를 위해 모든 카테고리의 피드백을 캡처합니다.</li>
<li><b>전달됨</b> 표시기의 계산은 정확도 및 재활동 향상을 위해 Enhanced MTA의 실시간 피드백을 기반으로 합니다.</li>
<li>EFS는 동기식 소프트 바운스 보고로 지연되는 문제를 해결합니다.</li>
</ul>
<p>자세한 내용은 <a href="../../sending/using/confirming-the-send.md">세부 설명서</a>를 참조하십시오.
</p>
</td> 
</tr> 
</tbody> 
</table>

<table> 
<thead> 
<tr> 
<th> <strong>Adobe Experience Manager 통합 개선 사항</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td>
<p>Adobe Experience Manager와 Campaign의 통합을 개선했습니다. 이제 Adobe Experience Manager에서 다국어 콘텐츠를 보다 손쉽게 가져올 수 있습니다. <p>
<p>Adobe Campaign Standard는 이제 Adobe Experience Manager 콘텐츠의 언어 변형을 자동으로 감지하고 일괄 변형 가져오기 및 생성을 허용하므로, 전문가가 Adobe Experience Manager 콘텐츠를 기반으로 다국어 캠페인을 만들기 위해 거쳐야 하는 단계를 대폭 간소화할 수 있습니다.</p>
<p>자세한 내용은 <a href="../../integrating/using/creating-multilingual-email-aem.md">세부 설명서</a>를 참조하십시오.
</p>
</td> 
</tr> 
</tbody> 
</table>

<!--
<table> 
<thead> 
<tr> 
<th> <strong>Unified Experience Cloud interface</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td>
<p>Adobe Campaign header bar has been changed to unify and improve your experience across all Experience Cloud products and services. These changes are designed to make your life easier, including:</p>
<ul>
<li>Easier switching between your organizations or to a different application.</li>
<li>Improved User Help – Bringing the Experience League into the product, search results also include results from community forums and more video content, giving you easier access to more content to help get the most out of the application. We've also added a feedback mechanism right in the Help menu, making it easier to report issues or share your ideas.</li>
<li>Improved Notifications – Notifications drop-down now has two tabs: one for your own product notifications, and one for more global product announcements.</li>
</ul>
<p>For more information refer to the <a href="../../start/using/interface-description.md#top-bar">detailed documentation</a>.
</p>
<p>NOTE: This change will be progressively rolled out to all customer environments between Feb 10 and March 1st.
</p>
</td> 
</tr> 
</tbody> 
</table>
-->

**개선 사항**

* **Microsoft Dynamics 365 통합**&#x200B;을 개선했습니다. 셀프 서비스 전용 통합 앱과 향상된 구현 프로세스를 추가했습니다. [자세히 알아보기](../../integrating/using/d365-acs-get-started.md)

* 트랜잭션 메시지 프로세스에서 문제가 발생할 때 쉽게 해결하도록 개선되었습니다. 이제 Adobe 기술 관리자는 프로세스를 다시 시작하지 않고도 모든 프로세스를 추적할 수 있습니다.

* 이제 **프로필** 목록에서 다음 필드 중 하나를 기반으로 레코드를 검색할 수 있습니다. 이메일, 이름, 성 또는 사용자 정의 필드는 프로필 리소스를 확장할 때 고급 필터링에 추가되었습니다. 이 기능은 filterType 매개 변수를 사용하여 Campaign Standard API에서도 사용할 수 있습니다. [자세히 알아보기](../../audiences/using/integrated-customer-profile.md)

* 매개 변수는 트랜잭션 메시지의 데이터베이스 풀링 프로세스를 실행하는 컨테이너 수로 조정했습니다. 이렇게 하면 사용되는 모든 컨테이너로 로드를 균일하게 분산하고 최적의 성능을 발휘할 수 있습니다.

* 이제 외부 매개 변수로 워크플로를 호출한 후 이벤트 변수를 사용하는 활동에서 새 **GetOption** 함수를 사용할 수 있습니다. 이를 통해 지정된 함수의 값을 반환할 수 있습니다. [자세히 알아보기](../../automating/using/customizing-workflow-external-parameters.md)

* 새 옵션을 사용하면 워크플로를 시작하기 전에 Campaign Standard에서 시스템의 사용 가능한 **실제 메모리를 확인**&#x200B;할 수 있습니다. 메모리의 양이 너무 낮으면 시스템 메모리가 이 임계값에 도달할 때까지 워크플로 실행이 지연됩니다. 이를 통해 성능 저하를 방지하고 작동 중단 위험을 줄일 수 있습니다. 서버에 대한 로드가 줄고 메모리가 증가하면 워크플로가 자동으로 다시 시작됩니다. 이 옵션은 읽기 전용이며 수정할 수 없습니다. [자세히 알아보기](../../automating/using/best-practices-workflows.md#execution)

* 기존 SDK v4 모바일 애플리케이션에서 **Adobe Experience Platform Mobile SDK**&#x200B;로 보다 쉽게 마이그레이션할 수 있는 새로운 프로세스가 Adobe Campaign Standard에서 제공됩니다. [이 페이지](../../administration/using/sdkv4-migration.md)를 참조하십시오.

**기타 변경 사항**

* 롤링 시간당 최대 100개의 콘텐츠 다운로드 제한에 도달할 때 메시지 준비 중 오류가 경고로 변경되었습니다. 이제 제한에 도달하면 경고가 표시되므로 게재를 진행할 수 있습니다.

* 트랜잭션 메시지 콘텐츠를 보강하는 경우 프로필 테이블에서 데이터를 가져올 때 더 이상 링크가 검색되지 않으므로 메시지 준비 중 지연이 줄어들고 프로필 테이블에 정의된 잘못된 관계로 인한 빈 프로필 데이터가 표시되지 않습니다.

* 인스턴스 기술 구성이 안정성이 보장되도록 최적화되었습니다. (CAMP-45681)

* 세션 관리가 메모리를 최적화하기 위해 개선되었습니다. (CAMP-45901, CAMP-46767)

* 이제 **전송 파일** 활동은 업로드되거나 다운로드한 파일의 수를 포함하는 추가 변수(filesCount)를 생성합니다. (CAMP-45842) [자세히 알아보기](../../automating/using/transfer-file.md#output-variables)

* 이제 SMS 커넥터는 각 메시지와 함께 여러 선택적 매개 변수를 보낼 수 있습니다. [자세히 알아보기](../../administration/using/sms-protocol.md)

* 이제 DATAMODEL 역할을 가진 사용자는 게재 로그 확장을 게시할 수 있습니다. (CAMP-46604)

* 더 이상 존재하지 않는 사용자 지정 리소스를 타겟팅하는 리소스를 게시하려고 할 때 표시되는 오류 메시지가 더욱 명확하게 표시됩니다. (CAMP-46893)

* 다음 언어가 **기본 설정 언어** 목록에 추가되었습니다. 인도네시아어 - 인도네시아(id), 영어 - 스웨덴(en-se), 영어 - 아시아 태평양(en-ap), 영어 - 일본(en-jp), 스페인어 - 라틴 아메리카(es-la). (CAMP-46351)

* 이제 랜딩 페이지를 테스트할 때 프로필 선택을 위한 선택기가 시간 초과를 방지하기 위해 프로필 대신 profileBase 리소스를 사용합니다.

* SMPP 로그 포맷이 개선되었습니다.

* Adobe Campaign Standard API와 일치하기 위해 cryptString 및 decryptString JS 함수에 대한 선택적 매개 변수가 추가되었습니다.

* 게재 준비 로그의 경고 또는 오류 메시지가 개선되었습니다.

* Adobe IMS(Identity Management Service)에 연결을 시도할 때 오류 로그가 개선되었습니다.

* 이제 다이내믹 보고에서 검색 창을 사용하여 **게재** 및 **Campaign** 차원을 추가로 필터링할 수 있습니다.

* 이제 트랜잭션 SMS 메시지 유효성 날짜는 트랜잭션 메시지 API의 만료 매개 변수에 대해 설정된 값으로 정의할 수 있습니다. (CAMP-36600)

* 다이내믹 보고에서는 **게재 요약** 기본 제공 보고서에 구독 취소 비율 지표에 대한 잘못된 데이터가 표시되었습니다. 이 문제를 해결하기 위해 **고유 구독 취소**&#x200B;라는 새 지표가 추가되었습니다. (CAMP-46445)

**패치**

* 특정 프로세스로 인해 게재가 매우 느리게 실행되는 문제를 해결했습니다. 몇 개의 매개 변수에 대해 잘못된 단위(예: 초 대신 밀리초)가 정의되었기 때문이었습니다.

* Mobile SDK에서 deliveryID/MessageID가 null이 아니라는 조건을 기준으로 공개 추적 요청을 전송하던 문제를 해결했습니다. 이로 인해 추적이 비활성화된 게재에 대해 404 오류가 발생합니다. 이제 게재의 추적 상태에 대한 정보가 포함된 추가 변수(acsDeliveryTracking)가 페이로드에서 전송됩니다. 이 변수는 설정된 추적 상태에 따라 2개의 값을 설정하거나 해제할 수 있습니다. [자세히 알아보기](../../administration/using/push-tracking.md)

* 한 번 실행되고 임시 리소스를 활용하는 **중복 제거** 활동을 복사하여 붙여넣을 때 발생할 수 있는 워크플로의 문제를 해결했습니다. 중복되면 활동 리소스가 자동으로 비어 있게 설정되므로 워크플로의 다른 활동에서 문제가 발생합니다. 붙여넣으면 이제 활동의 리소스는 워크플로에서 나중에 오류를 트리거하지 않고 가능한 한 빨리 오류를 트리거하기 위해 동일하게 유지됩니다. (CAMP-46903)

* 트랜잭션 푸시 알림 타기팅 프로필을 보낼 때 게재 분석이 실패하는 문제를 해결하기 위해 다음과 같은 새 [타깃 매핑](../../administration/using/target-mappings-in-campaign.md)을 도입했습니다. **프로필 - 푸시할 실시간 이벤트**(*mapRtEventAppSubRcp*). [프로필 기반 트랜잭션 푸시 알림](../../channels/using/transactional-push-notifications.md#transactional-push-notifications-targeting-a-profile)의 게재, 제외 및 추적 로그가 이제 *broadLogAppSubRcp*, *excludeLogAppSubRcp* 및 *trackingLogAppSubRcp* 테이블에 저장됩니다.

  >[!IMPORTANT]
  >
  >이 변경에 따라, 기존 프로필 기반 푸시 트랜잭션 알림(Adobe Campaign 21.1로 업그레이드하기 전에 만든 것)을 사용하는 경우 타깃 매핑을 새 프로필에 업데이트하고 메시지를 다시 게시하는 것이 좋습니다. 자세한 단계는 [여기](../../channels/using/transactional-push-notifications.md#change-target-mapping)를 참조하세요. 이전 타깃 매핑 **프로필 - 실시간 이벤트**(*mapRtEventRcp*)를 사용하면 게재 준비 시간이 길어지고 성능이 저하될 수 있습니다.

* 5,000개의 행이 표시되었을 때 게재 보고서가 실행되지 않던 문제를 해결했습니다.
* 게재 템플릿이 수정된 후 변형 B의 콘텐츠가 업데이트되지 않는 A/B 테스트 문제를 해결했습니다. (CAMP-45235)
* 트랜잭션 메시지 프로세스가 중단되어 메시지가 전송되지 않던 문제를 해결했습니다.
* 내부 링크를 클릭한 후 탐색 문제가 발생하는 문제를 해결했습니다(예: 증명 요약 화면에서 상위 게재에 액세스할 때).
* 게재를 만들 때 사용 가능한 모든 Experience Manager 콘텐츠 템플릿이 표시되지 않던 문제를 해결했습니다. (CAMP-45990)
* **Reason** 열을 추가 데이터 탭에 추가한 후 게재 로그에 오류 메시지가 표시되지 않는 워크플로의 문제를 해결했습니다. (CAMP-45139)
* 두 앱 구독 호출의 Marketing Cloud ID가 동일한 경우 발생하던 문제를 해결했습니다(&#39;복제 키 값이 고유 제한 위반&#39; 오류).
* 대량의 **쿼리** 및 **대상자 읽기** 활동이 포함된 워크플로로 활동을 끌어다 놓을 때 성능 저하를 초래할 수 있는 문제를 수정했습니다. (CAMP-44511)
* 리디렉션 정보가 추적 서버로 업로드되지 않도록 트랜잭션 메시지 준비 끝에 발생할 수 있는 오류를 수정했습니다.
* 워크플로 리소스를 사용자 지정한 후 가져오기 템플릿을 열거나 이전의 가져오기 작업을 열려고 할 때 오류 메시지가 표시될 수 있는 문제를 해결했습니다. (CAMP-46183)
* 동적 대상 이름으로 구성된 경우 **대상자 읽기** 활동이 실행되지 않는 문제를 해결했습니다. (CAMP-46047)
* **목록 내보내기** 단추가 표시되지 않는 문제를 해결했습니다.
* **보고 합계** 워크플로의 실패를 초래할 수 있는 문제를 해결했습니다. (CAMP-45979)
* 사용자 지정 복합 키(텍스트/날짜 다이내믹 콘텐츠)로 사용자 지정 리소스를 만들 때 발생하는 문제를 해결했습니다.
* 쿼리 전환 데이터가 표시되지 않는 문제를 해결했습니다. (CAMP-45669)
* 사용자 지정 리소스 게시와 관련된 메모리 사용량 문제를 해결했습니다.
* 특정 날짜에 전송되도록 게재를 구성할 때 발생하는 문제를 수정했습니다. 게재가 확인되면 즉시 발송되도록 설정된 경우, 게재 준비가 실패하고 처음에 지정된 날짜를 여전히 고려했습니다. (CAMP-44107)
* 트랜잭션 템플릿이 열리지 않는 문제를 해결했습니다. (CAMP-47181)
* 허용되는 문자열 크기를 초과하는 이름의 유형화 및 유형화 규칙이 중복될 수 있는 트랜잭션 메시지 게시 프로세스의 문제를 해결했습니다. (CAMP-47104)
* 입력 매개 변수가 존재하지 않는 레코드를 반환할 때 발생하는 **외부 API** 활동의 문제를 해결했습니다. (CAMP-47023)
* SMPP 커넥터가 다시 연결되지 않는 문제를 해결했습니다.
* 이름에 점이 포함된 파일을 다운로드할 때 **파일 전송** 활동에서 발생하는 문제를 해결했습니다. 점 다음에 오는 문자는 파일의 확장자로 간주되었습니다. (CAMP-46624)
* 데이터베이스 풀링을 수행할 수 없어 트랜잭션 메시지가 라우터 큐에 멈추는 문제를 해결했습니다.
* 취소된 게재 로그가 전송되지 않도록 하지 못했던 오류를 수정했습니다. 
* **AND-join** 활동을 사용할 때 워크플로가 실패하던 문제를 해결했습니다. 처음 유선 전환을 시각적으로 표시하더라도 활동은 기본 설정을 해당 전환으로 연결된 마지막 전환으로 자동으로 변경했습니다. (CAMP-46900)
* 격리된 주소가 상태가 [유효함]으로 잘못 설정되어 격리되지 않는 문제를 해결했습니다.
* 개인화된 필드에 특수 문자가 포함되어 있는 경우 해당 필드가 표시되지 않는 문제를 해결했습니다. (CAMP-46805)
* 프로필에 대한 특정 자세히 보기를 표시하지 못하는 문제를 해결했습니다. 이 문제는 프로필 리소스가 **개인화된 필드 추가 섹션** 옵션이 활성화된 사용자 지정 필드로 확장되는 경우에 발생했습니다.
* 트랜잭션 이벤트를 전송할 때 오류 코드 500을 반환할 수 있는 문제를 해결했습니다. (CAMP-46811)
* 이메일 예약 보고서를 수신하지 못하는 문제를 해결했습니다. (CAMP-46891)
* 1개의 카디널리티 단순 링크를 사용하여 사용자 지정 리소스를 프로필 리소스에 연결할 때 발생하는 문제를 해결했습니다. 사용자 지정 리소스 필드가 비어 있는 프로필에 액세스할 때 이제 빈 목록 대신 오류 메시지가 표시됩니다.
* 대체할 프로필을 선택할 때 페이지가 게재 프로필을 로드하지 못하는 워크플로에서 프로필 대체를 사용할 때 발생하는 문제를 해결했습니다. (CAMP-46522)
* **데이터베이스 정리** 기술 워크플로에서 다음과 같은 오류로 인해 만료된 게재 작업테이블을 삭제하려고 했던 회귀 문제를 해결했습니다. (CAMP-46536)

```
   PGS-220000 PostgreSQL error: ERROR: table ""wkdlv_24439460_data"" does not exist and WDB-200001 SQL statement 'DROP TABLE wkdlv_24448131_data' could not be executed.
```

* 사용자 지정 리소스에 대해 사용자 지정 필터를 사용할 때 몇 가지 사례에서 발생하는 다음과 같은 오류를 수정했습니다. (CAMP-46509)

```
   The 'profile/xxxx' field used in the filter 'xxxxx' does not exist in custom resource 'xxx'
```

* **푸시 알림 준비**&#x200B;가 완료되는 데 시간이 너무 오래 걸리는 문제를 해결했습니다. 이는 일시적인 작업 테이블에 색인이 누락되었기 때문이었습니다.
* 사용자 지정 리소스와 프로필 리소스 간의 관계가 이미 정의된 경우 워크플로의 **조정** 활동에서 **조정 차원** 옵션을 사용 시 발생할 수 있는 오류를 수정했습니다.
* **조정** 또는 **데이터 보강** 활동을 통해 링크를 추가할 때 발생하는 문제를 해결했습니다. 선택한 링크가 출력 변환에 표시되지 않았습니다.
* 워크플로에서 되풀이하는 게재와 함께 **세분화** 활동을 사용할 때 게재를 잘못된 대상자에게 보내는 문제를 해결했습니다. (CAMP-46275, CAMP-46470)
* 다이내믹 보고를 위한 사용자 지정 프로필 차원을 만들기 위해 프로필 리소스를 확장하려고 할 때 사용자 지정 리소스 게시가 실패하는 오류를 수정했습니다. (CAMP-46266)
* 파일 가져오기 테이블에 링크를 추가할 때 발생하는 오류를 수정했습니다. **데이터 보강** 활동을 **파일 가져오기** 활동에 추가한 후 이전에 구성된 링크가 사라졌습니다. (CAMP-46557)
* 저장 시 **세부 사항** 구성 화면의 표시 순서가 변경된 프로필 데이터에 연결된 사용자 지정 리소스를 사용할 때 발생하는 문제를 해결했습니다. (CAMP-46312)
* 사용자 지정 게재 매핑을 기반으로 하는 게재로 인해 다이내믹 보고에서 데이터를 표시하지 않는 문제를 해결했습니다.
* 워크플로 **쿼리** 활동에서 잘못된 리소스 타겟이 있는 컬렉션을 선택할 수 없는 오류를 수정했습니다.
* InMail 프로세스에서 하드 바운스의 유효성을 잘못 확인할 수 있는 문제를 해결했습니다.
* 링크 오류로 인해 프로필 화면을 열 때 발생하는 오류를 수정했습니다.
* 정리 워크플로에서 GDPR 데이터를 삭제하지 못하는 문제를 해결했습니다.
* 이메일 게재 예약 매개 변수에서 키보드로 예약 구성을 수동으로 업데이트할 때 발생하는 오류를 수정했습니다.
* 조직 단위의 잘못된 매개 변수로 인해 프로필을 편집할 수 없는 문제를 수정했습니다.
* 게재 템플릿에 설정되어 있더라도 **서비스** 확장 필드를 비우고 **이메일 속성**&#x200B;에 설정할 수 없는 문제를 수정했습니다.
* 증명을 처리하는 데 더 오래 걸릴 수 있는 문제를 수정했습니다. (CAMP-45048)
* 프로필 개요 화면에서 열을 정렬하지 못하는 문제를 해결했습니다.
* Azure에서 중국어 문자가 포함된 이메일의 변형이 발생할 수 있는 미리 보기 생성 문제를 해결했습니다. (CAMP-47152)
* Gmail 계정에서 받은 추적 이벤트 필터링으로 인해 Gmail에 대해 잘못된 공개 비율을 초래할 수 있는 Campaign 20.4에 도입된 회귀 문제를 해결했습니다. (CAMP-46504)
* HTML 콘텐츠를 트랜잭션 메시지 템플릿으로 가져올 수 없는 문제를 해결했습니다. (CAMP-47318)
* **이메일 렌더링 보고서**&#x200B;에서 렌더링 표시를 느리게 할 수 있는 문제를 해결했습니다. (CAMP-46226)
* 화면 정의에서 목록 유형 요소로 구성된 사용자 지정 리소스를 게시하지 못하는 문제를 해결했습니다. (CAMP-47217)
* 이메일 콘텐츠의 맨 위에 배치할 때 줄 디바이더 **Microsoft Outlook**&#x200B;에서 올바르게 렌더링되지 않는 이메일 디자이너의 문제를 해결했습니다. (CAMP-46294)
* **Adobe Analytics** 기술 워크플로로 KPI 조정이 중단되는 문제를 해결했습니다. (CAMP-46576)
* 콘텐츠 블록을 삽입할 때 조각이 검색 상자에 자동으로 표시되지 않는 **이메일 디자이너**&#x200B;의 문제를 해결했습니다. (CAMP-44205)
* 조각에 이모지를 사용할 때 보낸 이메일에 원하지 않는 문자가 표시되던 **이메일 디자이너**&#x200B;의 문제를 해결했습니다. (CAMP-46621)
* 콘텐츠에서 행 높이 추가 및 이미지 왜곡을 초래하는 디바이더 구성 요소에 영향을 미치는 **이메일 디자이너**&#x200B;에서 20.4에 도입된 회귀 문제를 해결했습니다. (CAMP-46663)
* 메시지를 Outlook 사서함에 보낼 때 **이메일 디자이너**&#x200B;의 오른쪽 또는 왼쪽에 정렬되었더라도 기본 제공 단추를 중앙에 그대로 유지하는 문제를 해결했습니다. (CAMP-46466)
* **이메일 디자이너** 미리 보기에서 프로필을 검색할 때 테스트 프로필 목록이 새로 고침되지 않는 문제를 해결했습니다. (CAMP-45265)
* **이메일 디자이너** 미리 보기에서 프로필을 검색할 때 사용자 지정 테스트 프로필이 목록에 표시되지 않는 문제를 해결했습니다. (CAMP-45589)
* **게재 요약 보고서**&#x200B;에서 트렌드 그래픽을 생성할 때 일치하지 않는 날짜가 표시되는 문제를 해결했습니다. (CAMP-45521)
