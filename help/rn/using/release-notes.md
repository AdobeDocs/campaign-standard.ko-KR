---
title: 릴리스 노트
seo-title: 릴리스 노트
description: 릴리스 노트
seo-description: 이 페이지에는 Adobe Campaign Standard의 모든 최신 버전이 나열됩니다.
page-status-flag: 정품 인증 안 함
uuid: 1 cf 2 e 40 c-beca -43 db -8261-a 1820 ee 86 ad 3
contentOwner: Sauviat
products: sg_ campaign/standard
audience: RN
content-type: 참조
topic-tags: campaign-standard-release
discoiquuid: 5 c 7 bfb 74-4002-4 ffe -87 e 8-bddb 41 d 34 b 41
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 8c1e17942d03250bbe863b2b57a0c810eaec6fa3

---


# Release Notes{#release-notes}

Adobe Campaign Standard의 특정 릴리스를 찾고 있습니까?

각 릴리스에는 새로운 기능과 패치가 포함되어 있습니다. 컨텐츠를 보려면 릴리스를 클릭합니다. Consult the [Release Planning](https://helpx.adobe.com/campaign/kb/acs-release-planning.html) to find out when the next release will happen.

View the latest [documentation updates](../../rn/using/documentation-updates.md) for Adobe Campaign Standard. If you're looking for a previous release, consult these pages: [2018 Release Notes](../../rn/using/release-notes-2018.md), [2017 Release Notes](../../rn/using/release-notes-2017.md), [2015-2016 Release Notes](../../rn/using/release-notes-2015-2016.md). [더 이상 사용되지 않거나 제거된 기능 목록을](https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html)참조하십시오.

## Release 19.3 - July 2019 {#release-19-3---july-2019}

### What's new? {#what-s-new-3}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> External API Activity (Public Beta)<br /> </td> 
   <td> <p>더 심층적인 개인화를 위해 외부 API 활동을 통해 REST API 호출을 통해 외부 시스템의 데이터를 워크플로우로 가져올 수 있습니다. REST 엔드포인트는 고객 관리 시스템, Adobe I/O 런타임 또는 Adobe Experience Cloud REST 엔드포인트 (예: 데이터 플랫폼, Target, Analytics, Campaign) 일 수 있습니다.</p><p>현재 이 기능은 공개 베타 버전입니다.</p><p>For more information, refer to the <a href="../../automating/using/external-api.html">detailed documentation</a> and the <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/managing-processes-and-data/data-management-activities/external-api-activity.html">how-to video</a>.</p></td> 
  </tr> 
  <tr> 
   <td> Report on workflow segment<br /> </td> 
   <td> <p>이 기능을 사용하면 마케터는 세그먼트 코드별로 배달 성과를 분류할 수 있습니다. 워크플로우를 만들고 세그멘테이션 활동을 사용하여 세그먼트를 배달 모집단에 할당할 때, 이러한 세그먼트는 이제 동일한 배달으로 이동할 수 있습니다. 이렇게 하면 단일 배달 내의 여러 세그먼트를 기반으로 한 클릭/클릭 통계를 표시할 수 있습니다.</p><p>For more information, refer to the <a href="../../reporting/using/creating-a-report-workflow-segment.md">detailed documentation</a> and the <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/reporting/report-on-workflow-segments.html">how-to video</a>.</p></td>
  </tr> 
 </tbody> 
</table>

### Security enhancements {#security-enhancements-2}

* 잘못된 요청에 대한 서비스 거부 (DoS) 공격을 방지하기 위한 보안 문제를 해결했습니다. (CAMP -33454)

### Email Designer enhancements {#email-designer-enhancements-3}

* 구성 요소가 추가될 때마다 HTML 템플릿에 HTML 스타일 태그를 추가하여 템플릿 크기를 대폭 늘릴 수 있었던 문제를 수정했습니다. (CAMP -34694)
* 오른쪽 상단 도구 모음 메뉴 옵션을 사용할 수 없는 문제를 해결했습니다. (CAMP -34577)
* 미러 페이지 URL 콘텐츠 블록이 이메일 콘텐츠에 삽입되면 발생하던 문제가 해결되었습니다. (CAMP -34779)
* 이메일에 JSPP 코드를 사용할 때 컨텐츠를 편집하기가 어려운 문제를 해결했습니다. (CAMP -34574)
* 하이퍼링크가 추가되면 이미지가 맨 위에서 잘리는 문제가 수정되었습니다. (CAMP -34382)
* Firefox에서 이메일 디자이너를 사용할 때 표시 문제가 해결되었습니다. (CAMP -34364)
* 이메일에서 동적 컨텐츠를 정의할 때 고급 모드로 발생하는 여러 가지 문제를 수정했습니다. (CAMP -34351, CAMP -34333, CAMP -34331)
* 다이내믹 컨텐츠 규칙 편집기에서 발생하던 몇 가지 문제가 수정되었습니다 (CAMP -34304, CAMP -34303).
* 이메일 디자이너 설정 창에서 링크 필드가 표시되지 않는 문제를 해결했습니다 (CAMP -33749).
* 보낸 이메일에서 큰 YouTube 아이콘 문제를 해결했습니다. (CAMP -33726)
* 미러 페이지 컨텐츠를 편집 가능하게 만드는 보안 문제를 해결했습니다. (CAMP -33691)
* 동적 컨텐츠에서 보다 큼 심볼을 사용할 때 HTML 출력을 끊는 문제를 해결했습니다. (CAMP -33688)
* 이메일 디자이너에서 텍스트를 편집할 때 실행 취소 옵션을 사용하는 문제가 수정되었습니다. (CAMP -32565)
* 스타일을 제거하지 않고 스타일을 취소할 때 추가 태그를 만든 문제를 수정했습니다. (CAMP -32359)
* 이제 이메일에 사용된 각 구성 요소가 데스크톱 장치 또는 모바일 장치에서만 표시되는지를 정의할 수 있습니다.
* 이제 소셜 컨텐츠 구성 요소의 너비와 높이를 설정할 수 있습니다.
* 동적 컨텐츠 이전 소스 코드가 해당 동적 컨텐츠를 삭제한 후 제거되지 않는 문제를 해결했습니다.
* 이메일이 수정된 후 업데이트되지 않는 문제를 해결했습니다.
* N: N 열 구조를 작업 공간으로 드래그하여 놓을 수 없습니다.
* 이메일 대시보드에서 메시지의 썸네일이 흐리게 표시되는 문제가 수정되었습니다.
* Outlook에서 받은 이메일에 대해 배경이 올바르게 표시되지 않는 문제를 해결했습니다.
* 이메일 디자이너 홈 페이지의 일부 정렬 문제를 해결했습니다.
* 동적 컨텐츠를 사용할 때 변형 복제에 발생하던 문제를 수정했습니다.
* 이메일 디자이너 설정 창에서 원치 않는 필드가 제거되었습니다.

### Other improvements {#other-improvements-3}

* Adobe Campaign 플랫폼 위치 서비스와의 통합을 통해 이제 Adobe Campaign는 Experience Platform SDK를 통해 모바일 애플리케이션의 가입자에게 위치 기반 마케팅 메시지를 전송할 수 있습니다. For more information, refer to the [detailed documentation](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md).
* 향상된 경험을 위해 보고 기능이 개선되었습니다. 이 기능을 사용하려면 동적 보고 사용 계약에 동의해야 합니다. For more on this, refer to the [detailed documentation](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement).
* 워크플로우에서는 워크플로우의 다음 10 개 실행을 미리 보기 위한 새로운 옵션이 추가되었습니다. For more on this, refer to the [detailed documentation](../../automating/using/scheduler.md).
* 스케줄러 활동에서 새 옵션을 사용하면 월별 배달에 특정 주의 특정 요일을 선택할 수 있습니다. For more on this, refer to the [detailed documentation](../../automating/using/scheduler.md).
* 수집 기간 없이 반복 배달을 만들 때 배달 대시보드에서는 배달이 전송되기 전에 확인을 요청할 수 있습니다. For more on this, refer to the [detailed documentation](../../sending/using/confirming-the-send.md).
* 이제 워크플로우의 외부 신호 활동에서 선언한 이벤트 변수를 사용하여 배달 레이블을 개인화할 수 있습니다. For more on this, refer to the [detailed documentation](../../automating/using/calling-a-workflow-with-external-parameters.md).
* GDPR 삭제 쿼리는 향상된 성능을 위해 향상되었습니다. (CAMP -33504)
* «FTP» 옵션이 외부 계정 구성 인터페이스에서 제거되었습니다. (CAMP -34472)
* 이제 각 이메일 메시지에 대해 SMTP 테스트 모드 옵션을 활성화하고 비활성화할 수 있습니다. For more on this, refer to the [detailed documentation](../../administration/using/configuring-email-channel.md#smtp-test-mode). (CAMP -34602)

### Other changes {#other-changes-2}

* 배달 속성 인터페이스에 경고가 추가되었습니다. 이 보고서는 배달을 기반으로 배달이 준비되고 워크플로우에 대해 하루에 여러 번 문의하도록 지정하는 것으로 지정합니다. (CAMP -34393)
* 사용자 지정 리소스 구성 화면에 경고가 추가되었습니다. 사용자 정의 리소스 ID 에는 최대 30 자 이상을 사용하는 것이 좋습니다. 이것은 사용자 지정 리소스 필드, 키, 색인 및 링크에도 적용됩니다.
* 이제 랜딩 페이지에서 확인 메시지로 사용되는 트랜잭션 메시지를 삭제하려고 하면 메시지가 표시됩니다.
* 이제 활동이 6 시간 이상 실행 중이면 워크플로우에 경고가 표시됩니다. 이것은 푸시 알림, 전달, 신호, 시작, 종료, 포크어, 참여, 예약 및 대기 활동에 적용되지 않습니다.
* 이제 동시에 실행 중인 최대 워크플로우 수에 도달하면 경고가 워크플로우에 표시됩니다.
* 이제 7 일 이상 일시 중지 또는 실패 상태인 워크플로우가 디스크 공간을 적게 차지하기 위해 중지됩니다. 작업 흐름 로그에 정리 작업이 표시됩니다.
* " 파일 전송 "활동을 사용할 때 파일 크기가 사용 가능한 디스크 공간을 초과하는 경우 오류가 기록됩니다.
* 인앱 메시지의 보조 단추에 대해 대상으로 리디렉션 URL 작업을 더 이상 선택할 수 없습니다.

### Patches {#patches-3}

* GDPR 액세스 요청이 실패할 수 있는 문제를 해결했습니다.
* 고유 프로필에 대해 여러 트리거를 받았을 때 트리거가 버려질 수 있는 문제를 해결했습니다.
* 로그인 후 잘못된 사용자 지정 리소스 게시 오류 메시지가 표시되는 문제를 해결했습니다.
* 사용자 지정 리소스를 만들거나 확장할 때 빈 페이지가 표시되는 문제를 해결했습니다.
* 모바일 게시에 타깃팅 차원에서 Appsubscriptionrcp를 타깃팅 차원으로 사용할 수 없는 문제를 해결했습니다.
* 하드 바운스 이메일 주소가 격리되지 않도록 하는 오류를 해결했습니다. (CAMP -24587)
* 유형 유형을 추가한 다음 유형을 삭제하기 전에 삭제했던 문제를 수정했습니다. (CAMP -32789)
* 동적 컨텐츠를 비활성화할 때 랜딩 페이지 컨텐츠가 표시되지 않는 문제를 해결했습니다. (CAMP -32924)
* 마스터 게재 특성에 개인화를 사용할 때 발생하는 반복되는 배달 문제를 수정했습니다. (CAMP -32983)
* 들어오는 SMS 메시지 데이터가 포함된 전환 결과를 읽을 수 없는 워크플로우에서 문제를 해결했습니다. (CAMP -33134)
* 포크 및 제외 활동을 결합하여 대상을 만들 때 발생했던 워크플로우에서 발생하는 문제를 수정했습니다. (CAMP -33401)
* 미러 페이지 컨텐츠가 표시되지 않게 할 수 있는 문제와 반복 배달용으로 전송되는 메시지가 수정되었습니다. (CAMP -33413)
* 프로파일과 대상 간에 조합 활동을 사용할 때 오류가 발생하던 문제가 수정되었습니다. 이 문제는 입력 전환 시 식별 키가 비호환성으로 인해 발생합니다. (CAMP -33713)
* " reccount "표현식이 두 번 클릭했을 때 올바른 구문을 사용하지 못하게 하던 테스트 활동의 문제를 수정했습니다. (CAMP -33756)
* 과금 기술 워크플로우 로그를 열 때 오류 메시지가 표시되는 문제를 해결했습니다. (CAMP -34313)
* 가입 시 확인란 필드를 구성할 때 발생할 수 있는 랜딩 페이지의 문제를 수정했습니다. (CAMP -34369)
* 목록을 구성하고 "아이콘" 필드를 추가할 때 발생하던 문제를 수정했습니다. (CAMP -34585)
* "|" and " %" 기호를 로드 파일 워크플로우 활동의 날짜 또는 시간 구분 기호로 사용합니다. (CAMP -34706)
* 랜딩 페이지에서 확인란과 함께 가시성 조건을 사용할 때 발생하던 문제를 수정했습니다. (CAMP -34802)
* 필터링 차원이 추적 로그로 설정되고 타겟 차원이 프로필로 설정되어 있는 경우, "추가 데이터" 탭에 필드가 표시되지 않는 강화 활동의 문제를 수정했습니다.
* " Workflowtemplate "리소스를 내보낼 때 오류 메시지가 표시되는 문제를 해결했습니다.
* 새 프로필을 만들 때 대화 상자에서 "국가/지역 코드" 필드를 선택한 경우 저장되지 않는 문제를 해결했습니다.
* DM (Direct Mail Import) 템플릿 (updatequarantinesdeliverylogsdirectmail) 를 사용할 때 발생하는 몇 가지 문제가 해결되었습니다.
* On-Demand 통합 관련 문제를 수정했습니다.
* 타임라인 보기를 확대할 때 발생하던 문제가 수정되었습니다. (CAMP -33628)
* 예약된 날짜와 시간이 포함된 이메일 메시지에 대한 교정본을 즉시 보내지 못하는 문제를 해결했습니다. (CAMP -33723)
* 사용자가 로그아웃했을 때 오류 로그를 생성한 트랜잭션 메시징과 관련된 문제를 해결했습니다. (CAMP -31698)
* 이메일 메시지를 예약할 때 특정 환경에서 발생할 수 있는 오류를 수정했습니다.
* 업데이트 배달 실행 워크플로우가 실패하는 문제를 해결했습니다.
* 제목 제목이 여러 줄로 포함된 경우 이메일 컨텐츠가 깨지는 보안 문제를 해결했습니다.


## Release 19.2.7 - July 2019 {#release-19-2-7---july-2019}

### Improvements {#improvements-2}

* GDPR 삭제 쿼리는 향상된 성능을 위해 향상되었습니다.
* 19.2 업그레이드 후 웹 충돌이 발생할 수 있는 문제를 해결했습니다. (CAMP -34862)
* 관리자가 아닌 사용자가 보고서를 저장하거나 예약하지 못하는 문제를 해결했습니다. (CAMP -31133)
* "|" 를 로드할 수 있습니다. (CAMP -34706)

## Release 19.2.4 - June 2019 {#release-19-2-4---june-2019}

### Email Designer {#email-designer-2}

* HTML에서 빈 스타일 태그가 사용될 때 조각을 편집할 수 없는 문제를 해결했습니다. 19.2.3에서 CAMP -33778에 대한 후속 수정 사항입니다.

## Release 19.2.3 - June 2019 {#release-19-2-3---june-2019}

### Email Designer {#email-designer-1}

19.2 릴리스의 조각을 최적화하기 위한 일련의 향상된 기능과 수정 사항이 추가되었습니다. 새로 만든 조각은 매끄럽게 작동합니다. 이전에 작성된 조각은 회색으로 처리되었으므로 새 형식으로 마이그레이션해야 합니다. 이렇게 하려면 각 조각을 클릭하고 새 형식으로 마이그레이션을 확인합니다. 모두 마이그레이션하기 전에 몇 개의 조각을 테스트하는 것이 좋습니다.

* 사용자가 조각을 잠금 해제한 후 조각을 편집할 수 없는 문제를 수정했습니다. 이는 19.2로 업데이트할 때 기존 조각에 영향을 주고 있었습니다. (CAMP -33778)
* 동적 컨텐츠를 사용할 때 문제가 해결되었습니다. HTML에 추가 공백이 추가되었습니다.

### Other improvements {#other-improvements-2}

* SMS 커넥터가 단절된 후 SMS 전송이 다시 시작되지 못하게 하는 문제가 해결되었습니다.
* TLS가 활성화된 경우 SMPP 연결을 닫을 수 있는 문제를 해결했습니다.
* TLS가 활성화된 경우 SMPP 연결을 닫을 수 있는 문제를 해결했습니다.
* Adobe Experience Platform Mobile SDK로 만든 모바일 애플리케이션의 속성을 관리하기 위해 Campaign에 "launch_ url_ campaign" 옵션이 추가되었습니다.
* 새로 만든 모바일 속성의 인증서를 업로드하고 모바일 응용 프로그램 속성 페이지를 종료한 후 샌드박스 환경 옵션을 선택 해제하는 오류를 해결했습니다.
* 서비스 리소스의 정보가 포함된 트랜잭션 메시지 컨텐츠를 강화할 수 없는 문제를 해결했습니다. (CAMP -33707)
* 서비스에서 프로필 가입을 취소할 때 발생하던 블랙리스트 랜딩 페이지의 문제를 수정했습니다.

## Release 19.2 - May 2019 {#release-19-2---may-2019}

### What's new? {#what-s-new-}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Control Panel<br /> </td> 
   <td> <p>관리 사용자로 작업의 효율성을 높이려면 인스턴스의 용량을 쉽게 모니터링하고 인스턴스의 설정을 관리할 수 있습니다 (SFTP 서버 관리 시작).</p><p>For more information, refer to the <a href="https://helpx.adobe.com/campaign/kb/control-panel.html">detailed documentation</a> and the <a href="https://helpx.adobe.com/campaign/kt/acs/using/acs-control-panel-video-use.html">how-to video</a>.</p></td> 
  </tr> 
  <tr> 
   <td> Local notifications<br /> </td> 
   <td> <p>로컬 알림 메시지를 사용하면 인터넷 또는 전경의 모바일 애플리케이션에 액세스하지 않고도 모바일 애플리케이션에서 새로운 데이터를 사용할 수 있게 되면 사용자에게 알릴 수 있습니다. 로컬 알림은 특정 시간 및 이벤트에 따라 모바일 응용 프로그램에서 트리거됩니다.</p><p>For more information, refer to the <a href="../../channels/using/customizing-an-in-app-message.md#customizing-a-local-notification-message-type">detailed documentation</a>.</p></td> 
  </tr> 
  <tr> 
   <td> Workflow enhancement - Add a payload to external signal activity<br /> </td> 
   <td> <p>다른 워크플로우나 REST API 호출에서 정의된 조건이 성공적으로 충족되면 페이로드를 사용하여 워크플로우를 시작하여 외부 시스템과 통합합니다. This also includes a new <strong>test</strong> activity where you can run tests on this functionality.</p><p>For more information, refer to the <a href="../../automating/using/calling-a-workflow-with-external-parameters.md">detailed documentation</a> and the <a href="https://helpx.adobe.com/campaign/kt/acs/using/acs-external-signal-activity-feature-video-use.html">how-to video</a>.</p></td> 
  </tr> 
  <tr> 
   <td> Landing Pages enhancement - Google reCAPTCHA<br /> </td> 
   <td> <p>Google recaptcha를 활용하면 고객의 행동 없이 랜딩 페이지에서 스팸을 방지할 수 있습니다.</p><p>For more information, refer to the <a href="../../channels/using/designing-a-landing-page.md#setting-google-recaptcha">detailed documentation</a>.</p></td> 
  </tr> 
 </tbody> 
</table>

### Security enhancements {#security-enhancements}

* 보고 작업 공간에서 잠재적인 클릭재킹 보안 문제를 해결했습니다.

### Email Designer enhancements {#email-designer-enhancements}

* 조각을 복제하고 이메일 디자이너에서 사용할 때 발생하던 문제를 수정했습니다. (CAMP -33193)
* 이메일 디자이너 인터페이스에서 인라인 요소를 사용할 때 원하지 않는 공백이 생성되는 문제를 해결했습니다. (CAMP -32163)
* 이메일 디자이너의 이메일 콘텐트를 저장한 후 사용자가 추가한 일부 추가 HTML 태그 속성이 삭제되는 문제를 수정했습니다. (CAMP -32162)
* Microsoft Office 태그를 제거한 후에도 이메일 디자이너 HTML 모드로 표시하는 문제를 해결했습니다. (CAMP -32141)
* 이메일 디자이너의 이전 버전을 사용하여 이메일을 만든 경우 이 이메일 콘텐트를 열면 팝업 창에 최신 버전으로 업데이트하라는 메시지가 표시됩니다. (CAMP -31529)
* 이메일 디자이너가 일부 메시징 클라이언트에 전달될 때 이메일 디자이너로 만든 이메일에서 이미지를 왜곡할 수 있었던 문제를 수정했습니다. (CAMP -31407)
* HTML 모드로 만들 때 목록 또는 버튼과 같은 일부 요소가 일반 텍스트 모드로 올바르게 표시되지 않는 문제를 해결했습니다. (CAMP -32582, CAMP -32542)
* 컨텐츠 템플릿 또는 조각 속성에 50 개 이상의 조직 단위를 표시할 수 없는 문제를 해결했습니다. (CAMP -32932)
* Outlook에서 이메일 디자이너로 작성된 이메일을 수신할 때 뷰포트 배경색 문제가 해결되었습니다. (CAMP -31402)
* Outlook에서 이메일 디자이너로 만든 이메일 컨텐츠가 반응형으로 표시되지 않는 문제를 해결했습니다. (CAMP -31400)
* 이메일 주체의 경우 동적 컨텐츠가 올바르게 작동하지 않는 문제를 해결했습니다. (CAMP -32837)
* 제대로 이스케이프되지 않은 이메일 제목과 관련된 문제를 해결했습니다.
* 이메일 디자이너 왼쪽 팔레트에서 조각이 로드되지 않는 문제를 해결했습니다.
* 이메일 컨텐츠 에디션의 이메일 컨텐츠 에디션이 이메일 디자이너 왼쪽 팔레트에서 조각 목록을 새로 고칠 때 표시되지 않는 문제를 해결했습니다.
* 이메일에서 동적 컨텐츠를 사용하는 동안 발생하는 몇 가지 문제가 수정되었습니다.
* RGB 값을 사용하여 색상을 정의하려고 할 때 색상 피커에서 발생하는 문제를 수정했습니다.
* 모바일에서 이메일을 수신할 때 미러 페이지가 응답하지 않는 문제를 해결했습니다.

### Transactional Messaging enhancements {#transactional-messaging-enhancements}

작업 및 성능을 최적화하기 위해 트랜잭션 메시징 채널에 몇 가지 개선 사항이 추가되었습니다.

* 트랜잭션 메시지 기간이 연장되어, 특히 재시도가 수행될 때 모든 메시지가 만료되기 전에 전송됩니다.
* 다른 전송 스레드에 로드를 배포하여 트랜잭션 메시징 성능이 향상되었습니다.
* 트랜잭션 메시징 프로세스는 동일한 메시지의 여러 분석을 동시에 시작할 수 있도록 최적화되었습니다.
* 트랜잭션 푸시 알림에 일관되지 않은 처리량 및 지연이 발생할 수 있는 문제를 해결했습니다.
* 트랜잭션 메시지 실행 배달에 대해 잘못된 타겟 대상이 표시되던 문제를 수정했습니다.
* 이벤트 구성 및 관련 트랜잭션 메시지로 패키지를 가져올 때 발생하던 문제를 수정했습니다. For more on this, refer to the [detailed documentation](../../channels/using/about-transactional-messaging.md#exporting-and-importing-transactional-messages).
* 제품 목록이 들어 있는 트랜잭션 메시지에 대해 생성된 테스트 프로필에서 수집 데이터를 삭제한 문제를 수정했습니다.

### Other changes {#other-changes}

* SMS 외부 계정에 새 옵션이 추가되었습니다. 병렬 연결의 수를 보다 효과적으로 제어하기 위해 SMS를 보내는 최대 MTA 프로세스 수를 제한할 수 있습니다. For more information, refer to the [SMS connector protocol and settings](https://helpx.adobe.com/campaign/kb/sms-connector-protocol-and-settings.html) technote.
* API 익스텐션이 포함된 리소스를 게시할 때 API가 이미 게시된 경우 이제 다시 게시할 때마다 자동으로 업데이트됩니다. 이전에는 이 작업이 수동이었으며 API를 업데이트하지 못하는 경우 이 API의 프로필 또는 서비스 리소스가 끊어질 수 있습니다. For more on this, refer to the [detailed documentation](../../developing/using/updating-the-database-structure.md#publishing-a-resource-with-api-extension).
* 우편번호 차원이 다이내믹 보고에서 제거되었습니다. 도시, 국가, 상태 차원을 대신 사용하는 것이 좋습니다.
* 인앱 메시지에 대한'첫 번째 실행'라이프사이클 이벤트 트리거가 제거되었습니다.
* 보안 그룹이 있는 패키지를 내보낼 때 이제 각 그룹에 할당된 역할이 포함됩니다. (CAMP -32960)
* 로드 파일 활동에서 새 옵션을 사용하면 업로드하려는 파일의 열이 열 정의와 일치하는지 확인할 수 있습니다. For more information, refer to the [detailed documentation](../../automating/using/load-file.md). (CAMP -32229)
* 이제 워크플로우를 페이로드로 시작할 수 있으므로 워크플로우 내에서 활동 간에 외부 매개 변수를 사용하고 공유할 수 있습니다. For more information, refer to the [detailed documentation](../../automating/using/calling-a-workflow-with-external-parameters.md). (CAMP -29412 &amp; CAMP -29413)
* 이제 Campaign Standard API를 사용하여 페이로드를 사용하여 프로필의 지리적 및 조직 단위를 업데이트할 수 있습니다. For more information, refer to the [detailed documentation](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html).
* 데이터베이스에서 개체가 액세스할 수 없는 경우 오류 메시지가 명확하게 표시됩니다.
* 파일 추출 작업에서는 내보낼 파일의 이름을 정의할 때 Javascript 기능이 업데이트되었습니다. 이제 출력 필드에서 Formatdate 함수만 사용할 수 있습니다. For more information, refer to the [detailed documentation](../../automating/using/extract-file.md).
* 자동 시퀀스 ID 생성이 사용자 지정 리소스에 대해 향상되었습니다. 새로운 맞춤형 리소스에 대한 기본 키는 이제 기본적으로 64 비트로 제공됩니다.
* 사용자 지정 리소스 발행 테스트 모드가 개선되었습니다. 마지막 사용자 정의 리소스 게시에 실패하고 해결되지 않은 경우 이제 경고 메시지가 사용자에게 표시됩니다. 사용자 지정 리소스 게시 오류가 발생하면 마지막 작업 버전으로 롤백할 수 있습니다. For more information, refer to the [detailed documentation](../../developing/using/updating-the-database-structure.md#publishing-a-custom-resource).
* 전송 파일 활동에 새 옵션이 추가되었습니다. SFTP 모드에서 파일 다운로드 동작을 사용할 때 파일을 정렬할 수 있습니다. For more information, refer to the [detailed documentation](../../automating/using/transfer-file.md). (CAMP -33109)

### Patches {#patches}

* SMS 설정이 다시 로드되었을 때 MTA에 메모리 누수가 발생할 수 있었던 문제를 수정했습니다.
* 복구 모드에서 게시 데이터베이스가 업데이트되지 않는 문제를 해결했습니다.
* Adobe Analytics 보고서와 Adobe Campaign Dynamic Reporting 간에 불일치가 발생하는 문제를 해결했습니다. (CAMP -25393)
* 보고서 공유 워크플로우가 실패하던 문제를 수정했습니다.
* 사용자가 미디어 URL 만으로 인앱 메시지를 보내지 못했던 오류를 수정했습니다.
* 모바일 앱이 인스턴스에 업로드되지 않은 경우에도 모바일 앱을 표시하는 문제를 해결했습니다.
* Fixed an error that prevented personalization fields from working when using the **Target all users of a Mobile app** template.
* 새 캠페인 표준 인스턴스가 프로비저닝되었습니다. (CAMP -32635 &amp; CAMP -32344)
* 워크플로우에서 날짜 공식을 사용자 정의하지 못했던 오류를 수정했습니다. (CAMP -30336)
* " 추가 데이터 "및" 세그먼트 코드 "필드를 드롭다운 목록에서 사용할 수 없게 하는 사용자 지정 날짜 공식을 정의할 때 문제를 수정했습니다. (CAMP -32383)
* " 파일 전송 "및" 파일 추출 "활동이 암호화된 경우 거부되지 않는 문제를 해결했습니다. (CAMP -32377)
* Linecount 필터가 정확한 총 카운트를 렌더링하지 못하게 하는 API의 문제를 해결했습니다. (CAMP -31424)
* 랜딩 페이지의 문제를 수정했습니다. (CAMP -31401)
* 예상치 않게 활성화될 수 있는 신호 활동이 발생하던 문제를 수정했습니다.
* 대상이 비어 있을 때 이메일 미리 보기가 표시되지 않는 문제를 해결했습니다.
* " 파일을 생성하지 않음 "옵션이 활성화된 상태에서 파일을 생성할 수 있는" 파일 추출 "활동의 문제를 수정했습니다.
* 배달이 성공적으로 완료되지 않은 경우 배달 가능성 워크플로우가 꺼지는 문제를 해결했습니다.
* 사용자가 보고서를 저장하거나 예약할 수 없는 문제를 해결했습니다. (CAMP -31133)

## Release 19.1.3 - March 2019 {#release-19-1-3---march-2019}

### Email Designer enhancements {#email-designer-enhancements-1}

* 템플릿을 저장한 후 수정할 수 없는 문제를 해결했습니다.
* 이메일에서 이전에 만든 템플릿을 사용할 때 다양한 문제를 해결했습니다.
* 가져온 템플릿에서 구성 요소가 표시되지 않는 문제를 해결했습니다.

### Other improvements {#other-improvements}

* 유형 지정 규칙을 볼 때 오류가 수정되었습니다. (CAMP -32059 &amp; CAMP -31849)
* 유형 지정 규칙이 편집되지 않는 문제를 해결했습니다. (CAMP -31750)
* 예상치 않게 중지할 수 있는 메일 프로세스 문제를 해결했습니다. (CAMP -31238)

## Release 19.1 - February 2019 {#release-19-1---february-2019}

### What's new? {#what-s-new--1}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Push channel Reporting improvements<br /> </td> 
   <td> <p>푸시 채널 보고에는 사용자 참여를 보다 직관적으로 측정할 수 있도록 해주는 몇 가지 개선 사항이 추가되었습니다. 이번 릴리스에서는 푸시 채널 지표 목록을 세 가지 다른 지표로 확장합니다. 노출 횟수, 클릭 수, 열기 (앱 열기) 는 푸시 알림과의 상호 작용을 보다 효과적으로 측정하고 분석하는 데 도움이 됩니다. 또한 이러한 지표의 정의 및 구현을 표준화합니다. 푸시 알림 내장 보고서도 일반적으로 사용되는 시각화 및 지표로 향상되었습니다.</p><p> For more information, refer to the <a href="../../reporting/using/push-notification-report.md">detailed documentation</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> Launch integration for Mobile App<br /> </td> 
   <td> <p>이 릴리스에는 Adobe Campaign Standard 용 Android 및 iOS 확장 버전과 Adobe Experience Platform Launch 및 Mobile SDK의 Adobe Campaign Standard가 통합되어 있습니다. 이러한 익스텐션은 푸시 메시징, 인앱 메시징 및 모바일 앱 프로파일 업데이트를 지원합니다.</p><p> For more information, refer to the <a href="../../administration/using/about-typology-rules.md#typology-rules">detailed documentation</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> Mobile In-App Messaging<br /> </td> 
   <td> <p>이 릴리스에는 Campaign에서 In-App 채널의 GA 버전이 포함되어 있습니다. 기능적인 관점에서 볼 때 베타 릴리스에 대한 가장 주목할 만한 추가 사항은 앱 내 채널에 대한 동적 보고서와 모바일 SDK와 MCIAS (SDK에 인앱 규칙을 제공하는 Marketing Cloud In-App 메시징 서비스) 간의 보안 핸드셰이크입니다. 보안 핸드셰이크는 사용자의 PII 데이터가 악의적인 사람에게 유출되지 않도록 보장하고 사용자가 로그아웃할 때마다 메시지 캐시를 지우도록 함으로써 공유 디바이스에서 사용자의 개인정보를 유지할 수 있도록 합니다.</p><p>For more information, refer to the <a href="../../channels/using/about-in-app-messaging.md">detailed documentation</a> and the dedicated <a href="https://helpx.adobe.com/campaign/kt/acs/using/acs-in-app-message-tutorial.html">In-App tutorial</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> Workflow enhancements<br /> </td> 
   <td> <p>다음 워크플로우 기능이 추가되었습니다.</p> 
    <ul> 
     <li> 이제 워크플로우 내에서 활동을 복사하거나 동일한 캠페인 인스턴스에서 다른 워크플로우를 붙여넣을 수 있습니다. 이렇게 하면 전체 워크플로우 또는 특정 활동을 쉽게 복제하고 처음 정의된 설정을 유지할 수 있습니다. For more information, refer to the <a href="../../automating/using/workflow-interface.md#duplicating-workflow-activities">detailed documentation</a>. (CAMP -20014) </li> 
     <li> <strong>이제 파일 로드</strong> 활동을 사용할 때 거부된 레코드가 포함된 파일 이름에 타임스탬프를 추가할 수 있습니다. For more information, refer to the <a href="../../automating/using/load-file.md#configuration">detailed documentation</a>. </li> 
     <li> <strong>이제 활동이 데이터를 검색하지 않으면 쿼리</strong> 및 <strong>세그멘테이션</strong> 활동을 통해 아웃바운드 전환을 활성화할 수 있습니다. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### Security enhancements {#security-enhancements-1}

* 생성된 랜딩 페이지 HTML 코드가 검색 엔진 색인화를 방지하도록 업데이트되었습니다.

### Email Designer enhancements {#email-designer-enhancements-2}

* Behance 아티스트가 디자인한 최고의 4 개의 반응형 이메일 템플릿 세트를 사용할 수 있습니다.

   For more information, refer to the [detailed documentation](../../start/using/about-templates.md#content-templates).

* 새로운 온보딩 경험을 통해 신속하게 이메일 제작을 시작하고 설명서 및 자습서를 손쉽게 이용할 수 있습니다.

   For more information, refer to the [detailed documentation](../../designing/using/about-email-content-design.md#email-designer-home-page).

* 이제 필요에 따라 열 수와 너비를 유연하게 구성할 수 있습니다.

   For more information, refer to the [detailed documentation](../../designing/using/defining-the-email-structure.md#editing-the-email-structure).

* 모바일 보기에서 편집할 때 공간 사용을 위해 모바일 디스플레이에서만 특정 구성 요소를 숨길 수 있습니다.

   For more information, refer to the [detailed documentation](../../designing/using/about-email-content-design.md#switching-to-mobile-view).

* 이제 사용자 정의 소셜 채널을 이미 사용 가능한 이메일 템플릿에 추가할 수 있습니다.
* 18 개 이상의 구조를 사용할 때 구조 메뉴를 아래로 스크롤할 수 없는 문제를 해결했습니다. (CAMP -31173)
* Adobe Campaign로 보낸 사전 헤더가 들어 있는 이메일을 전달할 때 컨텐츠 위에 Preheader가 표시되는 문제를 해결했습니다. (CAMP -30736)
* Fixed an issue that prevented the subject line from being updated when clicking the **Refresh AEM content** option after modifying the subject in Adobe Experience Manager. (CAMP -29984)
* Adobe Target에서 동적 이미지를 사용할 수 없는 몇 가지 문제가 수정되었습니다.
* 이전에 URL에서 콘텐트를 가져온 경우 준비 시 컨텐츠를 검색할 때 미리 보기가 업데이트되지 않는 문제를 해결했습니다.
* The YouTube icon has been added to the **Social** content component.
* The **List** view has been added for content components and fragments displayed in the Email Designer palette.

### Other improvements {#other-improvements-1}

* 이제 Adobe Campaign는 SDK v 4 및 AEP SDK 앱 모두에 대한 완벽한 FCM를 준수합니다.
* Adobe Campaign는 Android의 OS 및 Apple의 watchos에서 푸시 알림을 지원합니다.
* 인터페이스에서 탐색할 때 표시할 수 있는 경고 및 오류 메시지가 더욱 명확하고 이해하기 쉬워졌습니다.
* 이제 옵트인 및 옵트아웃 ("더 이상 연락 안 함" 필드) 와 관련된 프로필 목록 열에 추가할 수 있습니다.
* 프로필 작성 화면의 시간대 드롭다운 목록이 주소 섹션에서 인터페이스의 상단 섹션으로 이동되었습니다.
* 이제 사용자 정의 리소스 화면을 구성할 때 구분 기호를 추가하여 필드를 카테고리로 구성할 수 있습니다.

   For more information, refer to the [detailed documentation](../../developing/using/configuring-the-screen-definition.md#defining-the-detail-screen-configuration).

### Other changes {#other-changes-1}

* Adobe Campaign 및 Adobe Experience Cloud는 Microsoft Internet Explorer 11 부터 2019 년 봄 및 Campaign Standard 19.2 릴리스에 대한 지원을 제공합니다. Microsoft Edge 또는 다른 지원 브라우저로 전환하십시오. [더 이상 사용되지 않거나 제거된 기능](https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html) 페이지를 참조하십시오.
* The **Country code** field from the Profile resource has been renamed to **Country/Region code**.

### Patches {#patches-1}

* 이메일 트랜잭션 메시지에 테스트 프로필을 추가할 때 메시지가 전송되지 않는 문제를 해결했습니다. (CAMP -29854)
* 모든 채널에서 메시지 전송이 동시에 트리거되었을 때 한 채널에 대해 낮은 전송이 있을 경우 다른 채널에서의 메시지 전송을 느리게 하는 문제를 해결했습니다.
* 외부 계정 연결이 아직 설정되지 않은 경우 MTA가 SMS 메시지 전송을 시작하게 하는 문제를 해결했습니다.
* 스케줄러 활동 실행 빈도 및 시작 시간으로 발생하던 문제를 수정했습니다. (CAMP -30745)
* 확장된 프로필 리소스를 사용할 때 Pkey 생성 시 발생할 수 있었던 문제를 수정했습니다. (CAMP -30285)
* 달력 일 기반 피로 규칙으로 발생할 수 있는 문제를 수정했습니다. (CAMP -30136)
* " base "로 끝나는 이름으로 사용자 지정 리소스에 액세스하려고 할 때 발생할 수 있었던 문제를 수정했습니다. (CAMP -30109)
* 패치 호출을 사용하여 서비스에 프로필을 구독하는 문제를 해결했습니다. (CAMP -29728)
* 로드 파일 활동을 통해 XML 파일을 가져올 때 워크플로우를 손상시킬 수 있는 문제를 해결했습니다. (CAMP -29208 및 CAMP -28205)
* 역방향 카디널리티 링크를 생성할 수 없는 사용자 지정 리소스를 연결할 때 발생하는 문제를 수정했습니다. (CAMP -30476)
* 세그먼트 코드를 사용할 때만 배달 로그를 확장할 수 없는 문제를 해결했습니다.
* 워크플로우에서 파일 전송 활동을 사용할 때 행을 복제할 수 있는 문제를 해결했습니다.
* 선택한 시간에 예약된 보고서가 전송되지 않는 문제를 해결했습니다.
* 워크플로우에서 인앱 전달을 위해 "전송" KPI와 "전송" KPI가 일치하지 않는 문제를 해결했습니다.
* 사용자 정의 HTML로 제작된 인앱 메시지에 대한 추적이 작동하지 않던 문제를 수정했습니다.
* 워크플로우에서 사용할 때 앱 내 배달 컨텐츠가 저장되지 않는 문제를 해결했습니다.
* 모바일 응용 프로그램이 관리자에 대해 표시되지 않는 문제를 해결했습니다.
* 배달 기능 업데이트 기술 워크플로우에 오류가 발생하던 문제를 수정했습니다. (CAMP -26387)
* 인앱 배달을 만드는 동안 타깃팅된 프로필 및 게재 대시보드에 표시된 프로필 간 불일치가 발생하는 문제를 해결했습니다. (CAMP -28722)
* 이메일에서 공유 자산을 선택할 수 없는 캠페인 및 자산 핵심 서비스 통합 문제를 해결했습니다.

## Release 19.0 - January 2019 {#release-19-0---january-2019}

### What's new? {#what-s-new--2}

<table> 
 <colgroup><col style="width: 30%"><col style="width: 70%"></colgroup>
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Email Designer General Availability<br /> </td> 
   <td> <p>새로운 직관적인 이메일 디자이너 (이전 Creative Designer) 가 GA로 이동했습니다. 이제 다음을 포함한 기존 컨텐츠 편집기의 모든 기능을 지원합니다.</p> 
    <ul> 
     <li> The use of <a href="../../integrating/using/adding-target-dynamic-content.md">dynamic images from Adobe Target</a> </li> 
     <li> The ability to <a href="../../designing/using/importing-content-from-a-url.md#retrieving-content-from-a-url-automatically-at-preparation-time">retrieve content from a URL automatically at preparation time</a> </li> 
     <li> Fully compliant <a href="../../start/using/about-templates.md#content-templates">out-of-the box content templates</a>. </li> 
    </ul> 
    <p>For more information, refer to the <a href="../../designing/using/about-email-content-design.md">detailed documentation</a> and the <a href="https://helpx.adobe.com/campaign/kt/acs/using/acs-email-designer-tutorial.html">how-to video</a>. 개선 사항 및 수정 사항이 아래에 나열되어 있습니다.</p><p>따라서 기존 이메일 컨텐츠 편집기는 이제 더 이상 사용되지 않습니다. For more information, refer to this <a href="https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html">page</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> Product Listings in Transactional Emails<br /> </td> 
   <td> <p>이제 트랜잭션 이메일 메시지에서 하나 이상의 제품 컬렉션을 참조할 수 있습니다. 예를 들어 이미지, 가격 및 각 제품에 대한 링크로 사용자의 장바구니에 포함된 모든 제품을 나열하는 장바구니 포기 이메일을 자동으로 보낼 수 있습니다.</p><p>For more information, refer to the <a href="../../channels/using/event-transactional-messages.md#using-product-listings-in-a-transactional-message">detailed documentation</a> and the <a href="https://helpx.adobe.com/campaign/kt/acs/using/acs-product-listings-in-transactional-emails-feature-video-setup.html">how-to video</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> Mobile View in the Email Designer<br /> </td> 
   <td> <p>이제 이메일 컨텐츠를 편집할 때 전용 모바일 보기로 전환할 수 있습니다. 따라서 여백, 작은 글꼴 크기, 다른 배경색 등과 같이 모바일 디스플레이에 대한 모든 스타일 옵션을 별도로 편집하여 이메일의 반응형 디자인을 세밀하게 조정할 수 있습니다.</p><p> For more information, refer to the <a href="../../designing/using/about-email-content-design.md#switching-to-mobile-view">detailed documentation</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> In-App Messaging Beta Improvements<br /> </td> 
   <td> <p>인앱 메시징 베타 기능이 다음과 같은 기능으로 향상되었습니다.</p> 
    <ul> 
     <li> 앱 내 베타 채널이 GDPR 규격임 </li> 
     <li> Analytics API와 통합트리거 드롭다운을 사용한 채우기 </li> 
     <li> 전달 템플릿에 대한 직관적인 모양 및 설명 </li> 
     <li> 유용성 관점에서 저작 인터페이스에 대한 개선 사항 </li> 
    </ul> <p>For more information, refer to the <a href="../../channels/using/about-in-app-messaging.md">detailed documentation</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Improvements {#improvements}

* 이제 데이터 로드 활동의 새로운 옵션을 사용하면 거부된 레코드를 포함한 파일에 후처리 스테이지를 적용할 수 있습니다 (예: ZIP 형식 압축을 참조하십시오. (CAMP -24521)
* 이제 데이터 업데이트 활동의 새로운 옵션을 사용하여 업로드할 데이터의 최대 일괄 처리 크기를 구성할 수 있습니다. (CAMP -28400)
* 프로필의 주소 상태 선택이 개선되었습니다. 국가를 선택할 때 이제 "주" 드롭다운 목록이 관련 상태 값으로 자동 업데이트됩니다. (CAMP -28874)
* 이제 파일 추출 작업의 새로운 옵션에서는 인바운드 전환이 비어 있는 경우 파일 생성을 방지합니다. 이렇게 하면 Sftp 서버에 빈 파일을 만들고 업로드하지 않아도 됩니다.
* 배달 요약 보고서가 개선되었습니다.
* 프로필 주소를 정의할 때 사용할 수 있는 국가 목록은 풍부합니다. (CAMP -26707)
* 기본 제공 워크플로우를 가져올 때 오류 메시지가 표시됩니다.

### Email Designer {#email-designer}

* 이메일 템플릿 또는 이메일 디자이너로 만든 컨텐츠 조각이 Adobe Campaign에서 비활성화되어 다시 액세스하려고 할 때 템플릿 또는 조각을 사용할 수 없는 경우에도 이메일 템플릿 시 지리적 단위 기능을 활성화하는 문제를 해결했습니다. (CAMP -28174)
* 이메일 디자이너로 컨텐츠를 편집할 때 동적 컨텐츠 조건이 저장되지 않는 문제를 해결했습니다. (CAMP -27905)
* 메시지의 일반 텍스트 버전을 편집하고 이메일 디자이너에서 HTML 동기화를 수행한 후 이메일 컨텐츠에서 HTML 버전을 제거한 문제를 수정했습니다. (CAMP -28507)
* Internet Explorer 11를 사용할 때 이메일 디자이너 인터페이스가 열리지 않는 문제를 해결했습니다. (CAMP -28273)
* 이메일 디자이너와 함께 단추에 적용된 스타일 설정의 Microsoft Outlook 렌더링을 왜곡하는 문제를 해결했습니다.
* 이메일에 사용된 컨텐츠 조각에서 URL를 편집할 수 있게 만든 이메일 디자이너의 문제를 수정했습니다. 이 문제는 조각이 기본적으로 잠겨 있을 때 예상되지 않았습니다.
* 이메일 디자이너 분할자 구성 요소가 Microsoft Office에 표시되지 않는 문제를 해결했습니다.
* 기존 이메일 컨텐츠 편집기를 사용하여 AEM에서 동기화된 컨텐츠를 볼 때 특정 인터넷 브라우저에서 페이지가 동결되는 문제를 해결했습니다. (CAMP -29068)
* 기존 이메일 컨텐츠 편집기를 사용할 때 이메일에서 이미지를 클릭할 때 발생하는 오류를 수정했습니다. (CAMP -30424)
* 이메일 디자이너가 이메일을 편집할 때 새로 만든 조각이 표시되지 않는 문제를 해결했습니다. (CAMP -29928)
* 이메일 디자이너로 만든 이메일 및 Outlook 웹 메일 클라이언트를 사용하여 받은 이메일에 단추 텍스트가 제대로 표시되지 않는 문제를 해결했습니다.
* 이제 이메일 디자이너를 사용하여 프로필 트랜잭션 메시지를 만들 수 있습니다. (CAMP -28900)
* 이메일 디자이너가 준비 시간에 URL에서 컨텐츠를 자동으로 검색할 때 컨텐츠를 편집할 수 있게 하는 오류를 해결했습니다.

### Patches {#patches-2}

* 다이내믹 보고에서 잘못된 배달 로그가 표시되는 문제를 해결했습니다. (CAMP -23446)
* 바운스 요약 보고서의 숫자에 영향을 줄 수 있는 문제가 해결되었습니다 (CAMP -28703).
* Fixed an issue with the Campaign and Assets Core Service integration which could prevent assets from being displayed when selecting **[!UICONTROL Image shared from Adobe Experience Cloud]** in an email (CAMP-28732).
* SMPP 외부 계정에서 변환이 승인된 경우에도 ''' 문자가 포함된 SMS 메시지가 전송되지 않는 문제를 해결했습니다. (CAMP -29041)
* 워크플로우에서 세그멘테이션 활동을 사용할 때 중복 레코드를 표시할 수 있는 문제를 수정했습니다. (CAMP -28743)
* 워크플로우 활동의 열에 대한 값 매핑 중 하나를 삭제하지 못했던 문제를 수정했습니다. (CAMP -28708)
* " 파일이 있는지 확인 "옵션이 있는 와일드카드를 사용할 때 파일 전송 활동의 문제를 수정했습니다. (CAMP -28977)
* 외부 계정 설정을 업데이트할 때 발생할 수 있는 파일 전송 활동의 문제를 수정했습니다. (CAMP -28894)
* " 이메일이 비어 있지 않음 "조건을 사용할 때 쿼리 편집기에서 사용자 정의 필터 문제를 해결했습니다. (CAMP -28741)
* 100 K 이상의 레코드가 있는 사용자 지정 리소스 테이블을 내보낼 때 발생할 수 있었던 문제를 수정했습니다. (CAMP -28150)
* 트리거에 연결된 트랜잭션 메시지를 삭제할 수 없는 문제를 해결했습니다. (CAMP -28385)
* 일부 SMS 로그에 안전하지 않게 표시되는 암호를 제거했습니다.
* Adobe Campaign에서 보낸 빈 암호로 SMPP 시뮬레이터 연결이 실패하는 문제를 해결했습니다.
* SMS 연결이 불안정할 때 캠페인을 보내지 못하는 문제를 해결했습니다.
* 다이내믹 보고에서 삭제된 배달이 표시되는 문제를 해결했습니다.
* 워크플로우에서 강화 활동을 사용할 때 배달 로그, 추적 로그 및 제외 로그 테이블에서 추가 데이터를 검색하지 못했던 문제를 수정했습니다.
* " N Cardinality 컬렉션 링크 "링크 유형을 사용할 때 발생할 수 있는 GDPR 삭제 요청의 문제를 수정했으며" 대상 레코드 삭제 "는 링크에 의한 레코드 참조를 삭제하는 것을 의미합니다.
* 보고서 공유 문제를 수정했습니다.
* 푸시 알림을 전송할 때 Throughput 문제가 발생할 수 있는 문제를 해결했습니다.
* 다이렉트 메일 출력 파일의 필드가 누락되는 문제를 해결했습니다.
* 사용자가 내장된 워크플로우를 수정할 수 있었던 문제를 수정했습니다.
* Extract 활동이 구성된 워크플로우가 포함된 캠페인 템플릿을 기반으로 캠페인을 만들 때 문제를 수정했습니다. (CAMP -29198)
* 여러 요소에 대해 동일한 표현식을 사용할 수 없는 파일 추출 활동 문제를 해결했습니다. (CAMP -29182)
* 쿼리 편집기에서 Rtevent의 확장 로그와 추적 로그 간 연결 조건이 있는 문제를 수정했습니다. (CAMP -28780)
* " 특정 작업 "랜딩 페이지 옵션이 저장되지 않는 문제를 해결했습니다. (CAMP -29422)
* 워크플로우에서 이벤트의 페이로드를 내보낼 수 없는 문제를 해결했습니다. (CAMP -29029)
* 블랙리스트에 추가된 SMS 번호가 SMS 메시지에서 제외되지 않는 문제를 해결했습니다. (CAMP -28898)
* 들어오는 메시지를 처리하는 동안 오류가 발생하는 경우 SMPP 공급자에 알림 메시지가 표시되지 않는 문제를 해결했습니다. (CAMP -29804)
* 연결된 게재가 있는 외부 계정이 삭제되던 문제를 수정했습니다. (CAMP -29738)
* 전송 처리량이 SMS 메시지에 대해 개선되고 안정화되었습니다.
* " ~ "문자가 SMS 메시지에 사용되지 않는 문제를 해결했습니다. (CAMP -29172)
* 전송 시간 최적화 옵션이 있는 배달 문제가 해결되었습니다. (CAMP -29231)

