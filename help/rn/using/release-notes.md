---
title: 최신 릴리스
description: 이 페이지에는 Adobe Campaign Standard 최근 릴리스의 전체 목록이 있습니다.
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
source-git-commit: f45985c030c3d5059bfef444287c10b842298f49
workflow-type: tm+mt
source-wordcount: '1160'
ht-degree: 90%

---


# 최신 릴리스{#latest-release}

[릴리스 계획](../../rn/using/release-planning.md) | [Campaign 컨트롤 패널 릴리스](https://docs.adobe.com/content/help/ko-KR/control-panel/using/release-notes.html) | [설명서 업데이트](../../rn/using/documentation-updates.md) | [이전 릴리스 정보](../../rn/using/release-notes-2020.md) | [더 이상 사용되지 않는 기능](../../rn/using/deprecated-features.md)

![](assets/do-not-localize/cp-icon.png) 활성 프로필 모니터링, 하위 도메인 게재 기능 감사 및 GPG 키 관리가 포함된 **새로운 제어판 6월 릴리스** . [자세히 알아보기](https://docs.adobe.com/content/help/ko-KR/control-panel/using/release-notes.html)

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

* **AI 기반의 전송 시간 최적화 및 프로필 점수** - 이제 고객 여정의 디자인과 전달을 최적화하여 각 개인의 참여 선호도를 예측할 수 있습니다. 고객 여정 AI를 기반으로 하는 Adobe Campaign은 과거 참여 지표를 기반으로 공개 비율, 최적의 전송 시간, 예측 이탈을 분석하고 예측할 수 있습니다. [자세히 알아보기](../../sending/using/predictive.md)
* **브라질의 새로운 개인 정보 보호 규정** - Campaign에서 이미 사용 가능한 개인 정보 보호 기능 외에도, Adobe은 브라질의 LGPD(Lei Geral de Proteçao de Datos)에 대한 준비를 용이하게 하는 데 도움이 됩니다. 개인 정보 보호 요청을 만들 때 LGPD 규정이 Adobe 개인 정보 보호 코어 서비스에 추가되었습니다. [자세히 알아보기](https://helpx.adobe.com/kr/campaign/kb/campaign-privacy-overview.html)

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


![](assets/do-not-localize/cp-icon.png) **새 Campaign 컨트롤 패널 CNAME 하위 도메인에 대한 인증서 갱신과 함께 릴리스** 가능합니다. [자세히 알아보기](https://docs.adobe.com/content/help/ko-KR/control-panel/using/release-notes.html)
