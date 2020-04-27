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
source-git-commit: 86302762a46a814ecc9b14a5fe1bfe1a4a4e0437

---


# 최신 릴리스{#latest-release}

[릴리스 계획](../../rn/using/release-planning.md) | [제어판 릴리스](https://docs.adobe.com/content/help/en/control-panel/using/release-notes.html) | [설명서 업데이트](../../rn/using/documentation-updates.md) | [이전 릴리스 노트](../../rn/using/release-notes-2020.md) | [더 이상 사용되지 않는 기능](../../rn/using/deprecated-features.md)

## 릴리스 20.3 - 2020년 5월 {#release-20-3---may-2020}

**새로운 기능?**

<table> 
<thead> 
<tr> 
<th> <strong>태국의 개인 데이터 보호법(Personal Data Protection Act, PDPA)</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td> <p>태국의 개인 정보 보호법(PDPA)은 태국에 대한 데이터 보호 요구 사항을 조화시키고 현대화하는 새로운 개인 정보 보호법입니다. 이 규정은 이 국가에 있는 데이터 주체의 데이터를 보유하고 있는 Adobe Campaign 고객에게 적용됩니다.</p>
<p>Adobe Campaign에서 이미 사용 가능한 개인 정보 보호 기능(동의 관리, 데이터 유지 설정 및 사용자 역할 포함) 이외에도 Adobe는 PDPA에 대한 귀하의 준비 상태를 용이하게 하는 추가 기능을 포함시킬 수 있는 기회를 드립니다.</p>
<ul>
<li>액세스 권한 및 삭제 권한:gdpr 및 CPA에 추가된 기능을 활용하고 있습니다. <a href="https://helpx.adobe.com/content/help/en/campaign/kb/acs-privacy.html#righttoaccess">자세한 내용</a> </li>
<li><p>개인 정보 보호 요청을 만들 때 PDPA 규정 유형이 개인 정보 보호 코어 서비스에 추가되었습니다. 이 메서드는 모든 액세스 및 삭제 요청에 사용해야 합니다. 액세스 및 삭제 요청에 대한 캠페인 API 및 인터페이스 사용은 더 이상 사용되지 않습니다.  더 이상 사용되지 <a href="../../rn/using/deprecated-features.md">않음 및 제거된 기능 문서를</a>참조하십시오.</p></li>
</ul>
<p>사용 <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/privacy/privacy-overview.html">방법 비디오를</a>참조하십시오.</p>
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
  <td> <p>외부 <strong>API</strong> 활동이 베타에서 GA로 전환되고 있습니다. 이 릴리스는 JSON 응답 본문 구문 분석기에 추가적인 유연성을 제공합니다. 이제 다음을 수행할 수 있습니다.</p>
<ul>
<li>심도가 최대 10개인 중첩된 JSON을 구문 분석합니다. </li>
<li>선택한 속성을 JSON의 리프 노드로 분석하여 단일 테이블 행으로 병합합니다.</li>
<li>개체 이름을 "data"로 지정하거나 최상위 수준에 두지 않고 JSON에서 배열 개체를 선택하여 사용합니다.</li>
</ul>
<p><strong>주의:</strong> 고객은 워크플로우에서 모든 베타 외부 API 활동을 <strong>GA 외부 API 활동으로</strong> 대체해야 합니다.  External API의 베타 버전을 사용하는 워크플로우는 20.3에서 실행되지 않습니다.</p>
<p>자세한 내용은 <a href="../../automating/using/external-api.md">자세한 설명서</a> 및 <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/managing-processes-and-data/data-management-activities/external-api-activity.html">방법 비디오를</a>참조하십시오.</p>
</td> 
</tr> 
</tbody> 
</table>

**향상된 기능**

* [접두사] 필드에서 대상 프로필을 **** 사용하여 [메시지를](../../sending/using/testing-messages-using-target.md) 테스트하기 위해 사용할 수 있는 문자 수가 32자에서 500자로 늘었습니다.
* 인스턴스에 게시할 수 있는 최대 실시간 이벤트 수가 350개에서 2000개로 증가했습니다. (CAMP-41608)

**향상된 이메일 디자이너**

* 이제 이메일 디자이너는 엄격한 W3C보다 더욱 유연한 HTML 서식을 처리할 수 있습니다. (CAMP-42529)
* 클릭 가능한 [이미지가](../../designing/using/links.md#inserting-a-link) 컨텐츠 블록의 이미지 옆에 링크가 표시되지 않는 문제를 해결했습니다. (CAMP-41586)
* 추적된 URL에 템플릿에 카테고리가 추가되었을 때 랜딩 페이지로 리디렉션되지 [](../../designing/using/links.md#about-tracked-urls) 않는 문제를 해결했습니다. (CAMP-41537)
* Outlook에서 단추 패딩 문제를 해결했습니다.
* HTML 태그가 일반 텍스트로 표시되는 문제를 수정했습니다.
* 이제 콘텐츠 블록 검색에 서버 검색 결과와 미리 로드된 결과가 표시됩니다. (CAMP-41870)

**기타 변경 사항**

* 사용자 지정 리소스 게시 인터페이스가 더욱 명확한 오류 메시지와 함께 개선되었습니다.
* 사용하지 않은 배달 매핑이 인터페이스에서 제거되었습니다.
* 인터페이스에서 불필요한 관리자 역할이 제거되었습니다.
* 이제 랜딩 페이지에서 확인란은 필수일 수 있습니다.
* 동적 보고서의 CSV 파일을 다운로드할 때 200개 행 제한이 제거되었습니다. 이제 보고서의 모든 행을 포함할 수 있습니다. (CAMP-40810)
* 다국어 이메일에 즉시 사용 가능한 언어 목록에 ES-미국 언어가 추가되었습니다. (CAMP-42279)
* 이제 파일 전송 활동으로 다운로드한 파일은 X일 후 삭제됩니다. 여기서 X는 **워크플로우 속성의 실행** 메뉴 아래에 있는 **내역** 필드에의해 결정됩니다. [자세한 내용](../../automating/using/executing-a-workflow.md#workflow-properties)

**경험 플랫폼 통합**

* 읽기 대상 [활동에서](../../automating/using/aep-targeting-audiences.md) Adobe Experience Platform 대상을 **** 활성화하면 향상된 성능과 안정성을 제공할 수 있습니다. 또한 워크플로우 로그가 정품 인증 작업에 대해 더욱 명확하고 자세히 설명되어 Adobe Experience Platform 고객을 읽을 때 보다 손쉽게 모니터링하고 문제를 해결할 수 있습니다.

**패치**

* 사용자 지정 리소스의 게시 작업 중에 유령 리소스가 만들어지는 오류를 수정했습니다.
* 프로필 리소스가 사용자 지정 리소스로 연장된 경우 프로필의 마케팅 내역이 표시되지 않는 문제를 해결했습니다. (CAMP-41009)
* 편집기를 열 때 즉시 사용 가능한 랜딩 페이지 템플릿에서 컨텐츠를 프랑스어로 표시하는 문제를 해결했습니다. (CAMP-41639)
* 동적 컨텐츠가 포함된 푸시 알림의 문제를 해결했습니다. 이 경우 이모지가 표시되지 않습니다. (CAMP-40715)
* 아웃바운드 보완 전환 **중 하나에 잘못된 세그먼트 코드가 할당될** 수 있는 중복 제거 작업의 문제를 수정했습니다. (CAMP-41400)
* 예약된 보고서가 삭제되지 않는 오류를 수정했습니다. (CAMP-41302)
* 배달 대시보드와 배달 요약 보고서 간에 불일치가 발생하는 **문제를** 수정했습니다. (CAMP-41145)
* 다운로드한 보고서에서 문자 오버랩 표시 문제가 발생하는 문제를 수정했습니다.
* 전달 미리 보기가 증명 대체를 위해 작동하지 않는 문제를 해결했습니다.
* 인앱 로컬 알림의 사용자 정의 필드를 삭제할 때 발생하는 오류를 수정했습니다.
* 워크플로우에서 charIndex 함수가 **종료** 또는 파일 **전송** 활동을 사용할 수 없는 문제를 해결했습니다.
* 두 개의 입력 활동과 함께 **데이터 연계** 기능을 사용하는 워크플로우의 문제를 수정했습니다. (CAMP-42133)
* 알 수 없는 함수를 사용할 때 워크플로가 실행되지 않는 문제를 해결했습니다. (CAMP-41873)
* 아웃바운드 전환을 보완하는 여러 대상 저장 **활동을 사용하여 대상을** 만들 때 발생할 수 있는 워크플로우의 문제를 수정했습니다. (CAMP-39992)
* 트랜잭션 이메일에서 개인화를 사용할 때 데이터 불일치가 발생하는 문제를 수정했습니다. (CAMP-41842)
* 푸시 알림 배달에서 사용자 지정 필드를 삭제할 때 발생하는 문제가 수정되었습니다. (CAMP-37586)
* 사용자가 보고서를 변경할 수 없는 오류를 수정했습니다. (CAMP-42505)
