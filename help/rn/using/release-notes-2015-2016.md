---
title: 릴리스 노트 2015-2016
seo-title: 릴리스 노트 2015-2016
description: 릴리스 노트 2015-2016
seo-description: 이 페이지에는 Adobe Campaign Standard 2015 및 2016 릴리스의 모든 목록이 표시됩니다.
page-status-flag: 활성화 안 함
uuid: d5a0f6cc-0bed-46cf-8dff-1717fb624f8f
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: rn
content-type: reference
topic-tags: campaign-standard-releases
discoiquuid: a3ce6b80-1858-4 파섹
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 159c33639ab7b53558dac2ce183c3801c15ccb0f

---


# 릴리스 노트 2015-2016{#release-notes}

Adobe Campaign Standard의 특정 2015-2016 릴리스를 찾고 계십니까?

각 릴리스에는 새로운 기능과 패치가 포함되어 있습니다. 해당 컨텐츠를 보려면 릴리스를 클릭합니다.

Adobe Campaign Standard에 대한 최신 [설명서 업데이트를](../../rn/using/documentation-updates.md) 봅니다. 최신 릴리스를 원하는 경우 이 [페이지를](../../rn/using/release-notes.md)참조하십시오.

## 릴리스 16.11 - 2016년 11월 {#release-16-11---november-2016}

### 새로운 기능 {#new-capabilities}

<table> 
 <thead> 
  <tr> 
   <th> 기능<br /> </th> 
   <th> 설명<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 전달 가능성 제외 규칙<br /> </td> 
   <td> 이제 암호화된 전역 억제 목록이 전달 가능 인스턴스에서 관리되므로 악의적인 활동, 특히 Spamtrap 사용으로 인해 블랙리스트에 추가되지 않습니다.<br /> 각 이메일 배달에 대해 두 가지 기본 유형 분류 규칙은 수신자 이메일 주소와 이 목록에 포함된 금지된 주소 또는 도메인 이름을 비교합니다. 일치하는 항목이 있으면 해당 수신자가 대상 모집단에서 제외됩니다.<br /> 자세한 내용은 <a href="../../administration/using/filtering-rules.md#default-deliverability-exclusion-rules">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 일반 최적화<br /> </td> 
   <td> 이 업데이트에는 고객이 발생하는 문제를 해결하는 많은 변경 사항 및 패치가 포함되어 있습니다. 글로벌 플랫폼 공연도 최적화되었습니다. <br /> </td> 
  </tr> 
 </tbody> 
</table>

### 패치 {#patches}

#### 일반 {#general}

* 몇 가지 보안 문제가 해결되었습니다.
* REST API의 빈 필드 또는 중복 필드와 관련된 몇 가지 문제가 해결되었습니다.
* 이제 애플리케이션의 홈 페이지에서 바로 SMS 메시지와 푸시 알림을 만들 수 있습니다.

#### 이메일 및 SMS 메시지 {#emails-and-sms-messages}

* 사용자가 콘텐트 편집기에서 zip 파일을 업로드하지 못했던 문제를 수정했습니다.
* 교정을 보낸 후 교정을 열 수 없는 문제를 수정했습니다.
* A/B 테스트 이메일의 보고서에 액세스할 때 **[!UICONTROL Hot Clicks]** 오류 메시지가 표시되는 문제를 해결했습니다.
* 모드를 사용하여 수정한 내용이 적용되지 않는 문제를 **[!UICONTROL Show source]** 수정했습니다.
* 예측 제목 줄 xml 모델 파일을 가져올 수 없는 문제를 해결했습니다.
* 제목 줄 교육 모델의 데이터를 가져오기 위한 전용 새로운 화면이 **[!UICONTROL Administration > Channels > Emails > Predictive Subject Line]** 에서 제공됩니다.
* 관리자가 아닌 사용자가 이메일 구성 화면에서 인증된 마스크를 편집할 수 있도록 허용하는 문제를 해결했습니다.

#### 푸시 알림 {#push-notifications}

* 템플릿을 사용하여 푸시 알림을 보낸 후 받는 사람에게 로그 및 이벤트 로그를 보내지 못하는 문제를 **[!UICONTROL Send push on profiles]** 수정했습니다.
* 새 모바일 응용 프로그램을 만들 수 없는 문제를 수정했습니다.

#### 워크플로우 {#workflows}

* 활동을 사용할 때 발생하는 성능 문제를 **[!UICONTROL Subscription]** 수정했습니다.
* 내부 이름에 공백이 있을 때 워크플로우가 작동하지 않는 문제를 해결했습니다.

#### 통합 {#integrations}

* 이메일에서 Adobe Marketing Cloud에서 공유된 **이미지를 사용할 때 오류가** 표시되는 문제를 해결했습니다.

#### 사용자 정의 리소스 {#custom-resources}

* 확장 API 필드의 두 발행물 간의 향상된 API 로그 미리 보기
* 사용자 지정 리소스가 게시되기 전에 삭제되지 않는 문제를 해결했습니다.
* 프로파일이 확장되지 않고 식별자 키가 동적 필드로 설정되지 않는 문제를 해결했습니다.
* 사용자 지정 리소스에 링크를 추가할 때 발생할 수 있는 문제를 수정했습니다.

## 릴리스 16.10 - 2016년 10월 {#release-16-10---october-2016}

### 새로운 기능 {#new-capabilities-1}

<table> 
 <thead> 
  <tr> 
   <th> 기능<br /> </th> 
   <th> 설명<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 예측 제목 줄 이메일<br /> </td> 
   <td> 이메일을 편집할 때 새로운 옵션을 사용하면 다른 제목 줄을 시도해 보고 보내기 전에 공개 비율을 예측할 수 있습니다. 이는 이전 전달 데이터를 기반으로 자체 모델을 교육하거나 업계별 사전 정의된 모델을 사용하여 가능합니다. 이 기능은 이메일 메시지와 영어 내용만 포함하는 데이터베이스에 사용할 수 있습니다. <br /> 활성화 및 사용에 대한 자세한 내용은 <a href="../../designing/using/subject-line.md#predictive-subject-line">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> SMS 트랜잭션 메시지<br /> </td> 
   <td> SMS 채널이 Adobe Campaign의 트랜잭션 메시지 기능에 추가되었습니다. 이제 트랜잭션 메시지에 대해 두 개의 채널이 지원됩니다.이메일 및 SMS<br /> 자세한 내용은 <a href="../../administration/using/configuring-transactional-messaging.md#creating-an-event">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 트랜잭션 메시지 후속 메시지<br /> </td> 
   <td> 이제 이벤트를 타깃팅하는 워크플로우를 만들 수 있습니다. 이는 트랜잭션 메시지를 이전에 받은 고객에게 후속 메시지를 보낼 수 있음을 의미합니다. 이벤트 유형, 이벤트 브로드캐스트 및 추적 로그별로 대상을 필터링할 수 있습니다. 후속 메시지에서 이벤트(페이로드)의 컨텐츠를 활용할 수 있습니다. <br /> 자세한 내용은 <a href="../../channels/using/follow-up-messages.md">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 확장 프로필 및 서비스 API<br /> </td> 
   <td> 이제 프로필 및 서비스 API에서 확장 필드를 표시할 수 있습니다. 게시 메커니즘을 통해 API는 프로필 또는 서비스 사용자 지정 리소스의 확장 필드를 매핑할 수 있습니다. 이를 위해 데이터 모델 <strong>역할이</strong> 추가되었습니다. 이 새 역할을 사용하면 데이터 모델에 액세스할 관리자 집합을 구성할 수 있습니다.<br /> 자세한 내용은 <a href="../../developing/using/updating-the-database-structure.md#publishing-a-resource-with-api-extension">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### 패치 {#patches-1}

#### 일반 {#general-1}

* 몇 가지 보안 문제가 해결되었습니다.

#### 이메일 및 SMS 메시지 {#emails-and-sms-messages-1}

* SMS 외부 계정 구성 화면( **[!UICONTROL Administration > Channels > SMS > SMS accounts]** )이 개선되었습니다. "텍스트" 필드의 오류 코드를 지원하기 위해 **[!UICONTROL SMSC specifics]** 섹션에 여러 매개 변수가 추가되었습니다.

#### 푸시 알림 {#push-notifications-1}

* (mobileApp) 템플릿을 기반으로 푸시 알림의 대상을 편집할 때 사전 정의된 필터가 표시되지 않는 문제를 **[!UICONTROL Send via push notification]** 수정했습니다.
* 이제 모바일 애플리케이션 구성 화면( **[!UICONTROL Administration > Channels > Push Notification > Mobile applications]** )에 iOS 또는 Android 플랫폼이 성공적으로 만들어졌음을 나타내는 메시지가 표시됩니다.

#### 랜딩 페이지 {#landing-pages}

* 랜딩 페이지 양식이 제출될 때 확인 이메일이 전송되지 않던 문제를 수정했습니다.

#### 대상 및 쿼리 {#audiences-and-queries}

* 쿼리 편집기에서 프로필을 선택할 때 발생하는 몇 가지 문제를 수정했습니다.

#### 트랜잭션 메시지 {#transactional-messages}

* 트랜잭션 템플릿의 게시를 취소할 수 없는 오류가 수정되었습니다.
* 이벤트 목록에 표시되는 이벤트를 트리거하는 문제를 해결했습니다.

#### 통합 {#integrations-1}

* 해당 대상이 업데이트된 후 공유 대상이 전달에 사용되지 않는 문제를 해결했습니다.
* 공유 자산( **[!UICONTROL Image shared from Adobe Marketing Cloud]** 옵션)이 랜딩 페이지에서 사용되지 않는 문제를 해결했습니다.
* Adobe Audience Manager에서 가져온 공유 대상을 편집할 때 발생하는 문제가 수정되었습니다.

## 릴리스 16.9 - 2016년 9월 {#release-16-9---september-2016}

### 새로운 기능 {#new-capabilities-2}

<table> 
 <thead> 
  <tr> 
   <th> 기능<br /> </th> 
   <th> 설명<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 리마케팅 트리거<br /> </td> 
   <td> 핵심 서비스 트리거 <span class="uicontrol">와 Adobe Campaign</span> 간의 통합을 통해 Adobe Analytics에서 15분 이내에 웹 사이트에서 추적한 특정 행동에 대한 반응으로 고객에게 개인화된 이메일을 보낼 수 있습니다.<br /> Adobe Marketing Cloud에서는 장바구니 또는 양식을 포기한 모든 클라이언트, 장바구니에서 제품을 제거한 클라이언트 또는 세션이 만료된 클라이언트와 같이 모니터링하려는 고객 행동을 나타내는 서로 다른 트리거를 정의합니다. 트리거를 만들 때 트리거의 조건과 이벤트에서 Adobe Campaign으로 전송되는 데이터를 정의합니다. <br /> Adobe Campaign에서 이전에 만든 트리거를 선택하고 데이터 마트 데이터로 이벤트 데이터를 보완하며 해당 트리거에 연결된 트랜잭션 메시지 템플릿을 정의합니다. 예를 들어 클라이언트가 장바구니를 포기하면 이벤트가 Adobe Campaign으로 전송되어 15분 이내에 클라이언트에 전송된 리마케팅 이메일을 통해 이 이벤트를 활용할 수 있습니다.<br /> 자세한 내용은 <a href="../../integrating/using/about-adobe-experience-cloud-triggers.md">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 트랜잭션 메시지:일시 중지/게시 취소<br /> </td> 
   <td> 이제 컨텐츠를 업데이트하는 동안 트랜잭션 템플릿의 게시를 일시 중지할 수 있습니다. 해당 메시지는 더 이상 전송되지 않지만 데이터베이스에 저장됩니다. 다시 시작하면 큐에 있는 메시지가 처리되고 만료되지 않은 경우 전송됩니다.<br /> 자세한 내용은 <a href="../../channels/using/event-transactional-messages.md#suspending-a-transactional-message-publication">자세한 설명서를</a>참조하십시오.<br /> 이제 이벤트와 트랜잭션 템플릿을 게시 취소할 수도 있습니다. 해당 메시지는 더 이상 전송되지 않으며 데이터베이스에 저장되지 않습니다.<br /> 자세한 내용은 <a href="../../channels/using/event-transactional-messages.md#unpublishing-a-transactional-message">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 멀티브랜딩<br /> </td> 
   <td> 이제 여러 브랜드 클라이언트가 동일한 인스턴스에서 관리할 수 있습니다. 브랜딩은 Adobe Campaign 인스턴스의 관리자가 관리하는 기능으로, Adobe Campaign 내에서 브랜드와 관련된 모든 매개 변수를 중앙에서 구성할 수 있습니다. 여기에는 추적 URL, 웹 분석, 서버 URL, 도메인 이름 등과 같은 보다 전문적인 매개 변수에 대한 로고 등이 포함됩니다.<br /> 자세한 내용은 <a href="../../administration/using/branding.md">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 반응형 이메일 디자인 미리 보기<br /> </td> 
   <td> 이 기능을 사용하면 다양한 유형의 장치에서 이메일의 응답성을 테스트할 수 있습니다. 이메일 미리 보기에서는 다양한 화면 크기로 이메일을 테스트하기 위해 격자가 추가되었습니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 푸시 알림<br /> </td> 
   <td> 마케터가 iOS 및 Android 모바일 장치에서 개인화된 푸시 알림을 전송할 수 있도록 새로운 채널이 추가되었습니다. 메시지는 단일 전달을 통해 또는 워크플로우 활동을 통해 보낼 수 있습니다. 트랜잭션 메시징과의 호환성은 향후 버전에서 제공될 예정입니다. 이 채널은 Mobile 코어 서비스의 SDK( <a href="https://marketing.adobe.com/developer/gallery/marketing-cloud-mobile-libraries">여기에서</a>사용 가능)를 활용합니다.<br /> 자세한 내용은 <a href="../../channels/using/about-push-notifications.md">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### 패치 {#patches-2}

#### 일반 {#general-2}

* 이 릴리스에서는 인터페이스 목록에 새로운 필터링 및 검색 기능이 도입되었습니다. 이 새로운 기능은 로그(배달, 추적), 서비스(구독, 구독 내역), 대상 및 워크플로우 전환 등에서 사용할 수 있습니다.
* 고객 프로필의 터치포인트 수와 관련된 몇 가지 표시 문제를 수정했습니다.
* 몇 가지 유형 문제가 수정되었습니다.

#### 이메일 및 SMS 메시지 {#emails-and-sms-messages-2}

* 잘못된 교정본을 편집할 수 있는 오류를 수정했습니다. 이제 읽기 전용입니다.
* SMS가 너무 길거나 인코딩 문제가 있을 때 수신자가 블랙리스트에 포함되는 문제를 해결했습니다.

#### 사용자 정의 리소스 {#custom-resources-1}

* 사용자 지정 리소스의 고급 필터를 사용할 때 모든 결과가 표시되지 않던 오류를 수정했습니다.

#### 트랜잭션 메시지 {#transactional-messages-1}

* 이제 접두사가 새 이벤트 정의의 식별자에 자동으로 추가됩니다.
* 인터페이스에서 트랜잭션 메시지를 나타내는 아이콘이 변경되었습니다.

#### 통합 {#integrations-2}

* Adobe Target의 동적 이미지를 통해 고해상도 이미지를 삽입하면 발생하는 **표시 오류를** 수정했습니다.
* 대상 ID가 AMC 데이터 소스에 설정되지 않은 경우에도 공유 대상을 저장할 수 있게 하는 오류를 수정했습니다.

## 릴리스 16.7 - 2016년 7월 {#release-16-7---july-2016}

### 새로운 기능 {#new-capabilities-3}

<table> 
 <thead> 
  <tr> 
   <th> 기능<br /> </th> 
   <th> 설명<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 트랜잭션 메시지 강화<br /> </td> 
   <td> 이제 트랜잭션 템플릿을 Adobe Campaign 데이터베이스와 연결하여 트랜잭션 메시지의 컨텐츠를 보완할 수 있는 정보를 복구할 수 있습니다.<br /> 자세한 내용은 <a href="../../administration/using/configuring-transactional-messaging.md#enriching-the-transactional-message-content">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 이미지의 동적 URL<br /> </td> 
   <td> 이 새로운 기능을 사용하면 추적 및 개인화를 위해 컨텐츠 블록과 동적 텍스트를 삽입하여 이미지 소스를 개인화할 수 있습니다.<br /> 그런 다음 이미지 URL에 매개 변수를 입력하여 AEM 자산(S7) 다이내믹 미디어의 기능을 통해 수익을 창출할 수 있습니다. 예를 들어 "Hello Alexandre, get the latest news of Paris!"라는 개인화된 이미지가 포함된 이메일을 보낼 수 있습니다. "안녕 프랭크, 뉴욕에서 다가올 사건에 대한 최신 뉴스를 얻으세요!"<br /> 자세한 내용은 <a href="../../designing/using/personalization.md#personalizing-urls">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> People 코어 서비스와 통합<br /> </td> 
   <td> Adobe Marketing Cloud <strong>선언된 ID는</strong> 이제 Adobe Campaign과 People 코어 서비스(프로필 및 대상) 간의 통합으로 다룹니다.<br /><strong> 즉, 세그먼트를 가져오고 방문자 ID 또는 선언된 ID로 구성된 </strong>대상을<strong>내보낼 </strong>수<br />있습니다.자세한 내용은 <a href="../../integrating/using/about-campaign-audience-manager-or-people-core-service-integration.md">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 배달 로그<br /> </td> 
   <td> 이제 MTA 로그(배달 서버)에 각 메시지의 전체 내역(특히 모든 전달 시도 및 관련 오류 상태가 표시되므로 애플리케이션 성능에 영향을 주지 않습니다.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### 패치 {#patches-3}

#### 일반 {#general-3}

* 완료해야 하는 필드 대신 관련 없는 필드가 표시되던 오류를 수정했습니다. 이는 쿼리에서 조건을 편집할 때 비교 연산자가 여러 번 수정된 후에 발생합니다.
* 날짜 필드에 대한 상대 필터링 조건을 정의할 **[!UICONTROL The last X days/months/quarters/years]** 때 옵션 동작을 수정했습니다. 이제 계산된 기간은 달력 기반이 아닌 서버의 날짜 및 시간을 기준으로 하는 슬라이딩 기간입니다.

#### 워크플로우 {#workflows-1}

* 활동의 속성에서 타깃팅 차원을 선택하기 위해 화면에 잘못된 값 목록을 반환하는 오류를 **[!UICONTROL Query]** 수정했습니다.
* 활동의 컬렉션 요소에 **평균 또는 카운트** 합계를 추가할 때 Exists 연산자를 선택하게 하는 오류를 **[!UICONTROL Query]** 수정했습니다.

#### 컨텐츠 편집 {#content-editing}

* HTML 콘텐츠를 가져올 때 표시 문제(반응형 디자인)를 야기할 수 있는 오류를 수정했습니다.컨텐츠를 가져온 후 처음 열 때 스타일 속성이 더 이상 다시 작성되지 않습니다.
* 동적 컨텐츠 변형에 조건을 추가할 때 발생하던 비차단 오류를 수정했습니다.
* 랜딩 페이지의 컨텐츠에 확인란을 추가하여 발생하는 오류를 수정했습니다. 이 확인란은 사용할 수 없었습니다.
* 블록의 텍스트를 삭제할 때 해당 블록의 시작 부분에 커서가 놓인 경우 발생하는 오류를 수정했습니다.

#### 트랜잭션 메시지 {#transactional-messages-2}

* 이제 웹 사이트를 통합할 때 주어진 이벤트에 대한 만료 날짜를 정의할 수 있습니다. 이 날짜가 지나면 이벤트에 해당하는 메시지를 더 이상 보낼 수 없습니다.

## 릴리스 16.6 - 2016년 6월 {#release-16-6---june-2016}

### 새로운 기능 {#new-capabilities-4}

<table> 
 <thead> 
  <tr> 
   <th> 기능<br /> </th> 
   <th> 설명<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 프로필 및 서비스 API<br /> </td> 
   <td> Adobe Campaign <span class="uicontrol">Profiles and Services</span> API는 <a href="https://www.adobe.io/products/campaign">adobe.io</a> 포털에서 사용할 수 있습니다. 이렇게 하면 Adobe Campaign 프로필을 업데이트, 추가 및 삭제할 수 있으며, REST 호출을 통해 서비스에 가입하거나 가입을 취소할 수 있습니다.<br /> 자세한 내용은 API에 대한 <a href="https://docs.campaign.adobe.com/doc/standard/en/adobeio.html">자세한 설명을 참조하십시오</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### 패치 {#patches-4}

#### 일반 {#general-4}

* 이제 모바일 장치에서 도구 설명이 비활성화되어 화면에 표시되는 정보를 쉽게 읽을 수 있습니다.
* 사용자가 iPad 화면에서 특정 영역의 컨텐츠를 스크롤하지 못했던 오류를 수정했습니다.
* Internet Explorer 11에서 컨텐츠를 편집하는 동안 발생하는 몇 가지 호환성 오류가 수정되었습니다.
* 데이터 가져오기가 처음으로 실패할 때 세부 로그에 액세스하지 못하는 오류를 수정했습니다.
* 범위 필터가 저장되지 않는 문제를 해결했습니다.
* 목록이 표시되는 방식을 구성할 때 리소스의 요소가 표시되지 않는 오류를 해결했습니다.
* 쿼리 편집기 탐색기에서 오류가 수정되었습니다. 검색 필드에서 반환되는 결과는 검색 내역에 보관되었으며 모든 새로운 검색 시 계속 표시됩니다.

#### 이메일 및 SMS 메시지 {#emails-and-sms-messages-3}

* 바운스에 연결된 정보가 배달 로그에서 복구되지 않는 오류를 해결했습니다.
* 트랜잭션 메시지의 동적 콘텐츠 블록에 있는 컨텍스트에 액세스할 수 없는 오류가 수정되었습니다.
* 이메일 컨텐츠의 동적 텍스트에 URL 링크가 정의되지 않았던 오류를 수정했습니다.
* 배달 만들기 마법사의 맨 위 막대 표시를 수정했습니다.
* 게재의 기본 키는 더 이상 개인화 필드로 사용할 수 없습니다.

#### 워크플로우 {#workflows-2}

* 이제 워크플로우의 두 활동 간의 전환에는 한 활동에서 다른 활동으로 계산되고 전송된 요소의 수가 표시됩니다.
* 이제 **[!UICONTROL Query]** 활동에 추가 데이터가 추가되면 호환되지 않는 필드가 숨겨집니다.
* 추가 데이터를 추가할 때 표시되는 합계 정의 창은 사용 중인 데이터와 호환되는 오퍼 옵션만 표시하도록 개선되었습니다(예:평균을 계산하는 것은 숫자 데이터에만 가능합니다.)
* 즉시 사용 가능한 기술 워크플로우를 시작하거나 다시 시작할 수 있는 방법은 이제 관리 권한이 있는 사용자만 수행할 수 있습니다.

#### 랜딩 페이지 {#landing-pages-1}

* 랜딩 페이지의 속성에서 32비트 AES 코딩 키가 잘릴 수 있는 오류를 해결했습니다.
* 가시성 조건을 정의하거나 랜딩 페이지에 동적 컨텐츠를 추가할 때 쿼리 편집기가 제대로 표시되지 않는 오류를 해결했습니다.

#### 사용자 정의 리소스 {#custom-resources-2}

* 이제 프로필의 서비스 가입과 관련된 필터를 정의할 때 이 **[!UICONTROL Switch to parameters]** 옵션이 숨겨집니다.
* 사용자 지정 리소스에서 0-1 유형 링크를 구성할 때 발생할 수 있는 오류를 수정했습니다.
* 관련 있는 경우 사용자 지정 리소스에 날짜 및 시간 **유형 필드를 추가할 때 정의된** 상수 기본값이 **편집되지 않도록** 하는 오류를 수정했습니다.

## 릴리스 16.5 - 2016년 5월 {#release-16-5---may-2016}

### 새로운 기능 {#new-capabilities-5}

<table> 
 <thead> 
  <tr> 
   <th> 기능<br /> </th> 
   <th> 설명<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 사전 정의된 필터<br /> </td> 
   <td> 이제 관리자는 미리 구성된 규칙 형태로 쿼리 편집기에 표시되는 고급 필터를 만들 수 있습니다. 이러한 필터를 선택하면 고객을 정의할 때 간소화된 인터페이스에서 보다 쉽게 복잡한 구성을 개발할 수 있습니다.<br /> 자세한 내용은 <a href="../../developing/using/configuring-filter-definition.md">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 워크플로우:구독 서비스<br /> </td> 
   <td> 새로운 <span class="uicontrol">구독 서비스</span> 활동은 한 번의 클릭으로 여러 프로파일을 서비스에 가입 또는 가입 해제할 수 있는 가능성을 제공합니다.<br /> 이 활동은 타깃팅을 수행하거나 식별된 데이터가 있는 파일을 가져온 후에 사용할 수 있습니다.<br /> 자세한 내용은 <a href="../../automating/using/subscription-services.md">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 워크플로우:데이터 수집<br /> </td> 
   <td> 이제 <span class="uicontrol">쿼리</span> 유형 활동에서 추가 데이터 <span class="uicontrol">탭을 사용할 수</span> 있습니다. 이 기능을 사용하면 쿼리를 통해 타깃팅된 데이터를 보완하고 이 데이터를 활용할 수 있는 다음 워크플로우 활동으로 전송할 수 있습니다.<br /> 추가 데이터를 추가한 후 정의된 추가 데이터를 기반으로 조건을 만들어 처음에 타깃팅된 데이터에 추가 필터 수준을 적용할 수 있습니다.<br /> 자세한 내용은 <a href="../../automating/using/query.md#enriching-data">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 컨텍스트 기반의 도움말<br /> </td> 
   <td> 이제 상황에 맞는 도움말 기능을 다양한 Adobe Campaign 화면에서 사용할 수 있습니다. 즉, 한 번의 클릭으로 현재 사용 중인 기능에 대한 문서에 직접 액세스할 수 있습니다. 상황에 맞는 도움말을 표시하려면 '?'를 클릭하십시오. 아이콘을 클릭합니다.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### 패치 {#patches-5}

#### 일반 {#general-5}

* 다양한 인터페이스 Marketing Cloud 표준을 준수하는 새로운 기능
* 다양한 드롭다운 목록 유형의 표준화

#### 이메일 및 SMS 메시지 {#emails-and-sms-messages-4}

* 오류 주소 마스크가 지정된 경우 이메일이 전송되지 않던 오류를 수정했습니다.
* 이제 TLS 프로토콜이 이메일 배달에 대해 지원됩니다. MX 관리의 새 열을 사용하여 각 도메인에 대해 원하는 TLS 동작을 정의할 수 있습니다.
* SMS 인터페이스가 개선되었습니다.

#### 워크플로우 {#workflows-3}

* 다양한 워크플로우 인터페이스 새로운 기능
* 빠른 작업을 표시할 때 발생하는 오류를 수정했습니다.
* 1-N 링크가 포함된 **[!UICONTROL Segmentation]** 유형 활동을 사용할 때 워크플로가 실패하게 하는 오류를 수정했습니다.
* 워크플로우의 전환이 하이브리드 장치에서 열리지 않는 문제를 해결했습니다.
* 워크플로우를 처음 시작할 때 일시 정지 단추가 표시되지 않던 오류를 수정했습니다.

#### 컨텐츠 편집기 {#content-editor}

* 이제 컨텐츠 편집기에서 이메일이나 랜딩 페이지에 포함된 URL을 개인화할 수 있습니다. 자세한 [설명서를](../../designing/using/personalization.md#personalizing-urls)참조하십시오.
* 게재 작성 마법사에 이미지를 추가하고 나중에 해당 컨텐츠를 수정했을 때 이미지가 손실되는 오류를 수정했습니다.

#### 사용자 정의 리소스 {#custom-resources-3}

* 사용자 지정 리소스의 구성 화면에서 개인화된 1-N 유형 링크를 추가할 때 발생하는 오류를 수정했습니다.
* 사용자 지정 리소스를 준비하고 게시할 때 진행률 표시줄의 표시를 개선했습니다.
* 사용자 지정 리소스의 링크 목록을 표시할 때 발생하는 오류를 수정했습니다.

#### 트랜잭션 메시지 {#transactional-messages-3}

* 인터페이스의 사용자 친화성뿐만 아니라 트랜잭션 메시지 엔진의 성능과 견고성이 최적화되었습니다.
* 이제 트랜잭션 메시지 템플릿의 게시를 일시적으로 일시 중지할 수 있습니다. 자세한 내용은 [자세한 설명서를](../../channels/using/event-transactional-messages.md#suspending-a-transactional-message-publication)참조하십시오.
* 호환되지 않는 타깃팅 차원이 있는 컨텐츠 블록이 트랜잭션 메시지 템플릿에 추가될 수 있는 오류를 수정했습니다.
* API 미리 보기가 이벤트 구성 화면에 표시되지 않던 오류를 수정했습니다.

#### 대상 및 쿼리 {#audiences-and-queries-1}

* 쿼리 편집기에서 날짜 사용과 관련된 다양한 패치 자세한 [설명서를](../../automating/using/editing-queries.md#creating-queries)참조하십시오.

#### 관리 {#administration}

* 사용자가 로그인할 수 없는 "표준 사용자" 보안 그룹 이름과 관련된 오류가 수정되었습니다.

## 릴리스 16.3 - 2016년 3월 {#release-16-3---march-2016}

### 새로운 기능 {#new-capabilities-6}

<table> 
 <thead> 
  <tr> 
   <th> 기능<br /> </th> 
   <th> 설명<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 인터페이스 및 탐색<br /> </td> 
   <td> Adobe Campaign 인터페이스가 향상되어 탐색 및 작업이 간단하고 직관적으로 향상되었습니다.<br /> 이제 응용 프로그램의 상단 막대에서 탐색합니다. 고급 메뉴는 Adobe Campaign <strong>로고를 선택하여 액세스할 수</strong> 있습니다.<br /> 자세한 내용은 <a href="../../start/using/interface-description.md">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 워크플로우:고객 저장<br /> </td> 
   <td> 이제 대상자 <span class="uicontrol"></span> 저장 활동에서 대상자 <span class="uicontrol">만들기 및 업데이트 새로운 옵션을 사용할 수</span> 있습니다. 이 옵션을 사용하면 대상자 레이블을 수동으로 입력할 수 있습니다. 입력한 레이블이 기존 대상에 해당되는 경우 업데이트됩니다. 대상이 없으면 만들어집니다.<br /> 또한, 참가자는 워크플로우가 실행될 때마다(다시) 업데이트됩니다.<br /> 항상 대상 업데이트 모드를 선택할 수 있습니다.새로운 데이터로 고객을 완료하거나 모든 실행 시 고객 데이터를 교체합니다.<br /> 자세한 내용은 <a href="../../automating/using/save-audience.md">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 워크플로우:세그멘테이션<br /> </td> 
   <td> 이제 <span class="uicontrol">세그멘테이션</span> 활동을 통해 사용자가 임시 리소스의 데이터를 세그먼트화할 수 있습니다. 예:가져온 파일의 데이터입니다.<br /> 자세한 내용은 <a href="../../automating/using/segmentation.md">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### 패치 {#patches-6}

#### 일반 {#general-6}

* 목록을 정렬할 때 발생하는 표시 오류를 수정했습니다.열의 정렬 순서를 나타내는 화살표는 특정 데이터 유형에 대해서만 반전될 수 있습니다.
* 쿼리에 규칙이 추가될 때 드롭다운 메뉴에 표시되는 요소 수를 제한하던 오류를 수정했습니다.

#### 이메일 및 SMS 메시지 {#emails-and-sms-messages-5}

* 이메일 렌더링 보고서에 액세스할 수 없는 오류를 수정했습니다.
* 이제 메시지의 준비 전송 단계에서 보낸 사람 주소가 제공되지 않으면 오류를 반환합니다.

#### 워크플로우 {#workflows-4}

* 특정 파일 서식 옵션이 표시되었지만 CSV 형식 파일을 추출할 때는 고려되지 않았습니다. 이제 이러한 옵션이 더 이상 표시되지 않습니다.
* 옵션 유형이 파일 전송에 대해 **[!UICONTROL Delete the source files after transfer]** 선택되었을 때 발생하는 **[!UICONTROL SFTP]** 오류를 수정했습니다.
* 페이지를 새로 고친 후 카운터 및 **[!UICONTROL Query]** 데이터 미리 보기가 표시되지 않는 오류를 수정했습니다.
* 특히 타깃팅 및 필터링 차원이 다른 배달 활동 또는 쿼리 이후 워크플로에서 특정 전환을 여는 경우 발생하는 오류를 수정했습니다.
* 활동 추가 후 워크플로우가 저장되지 않은 경우 개인화 필드가 워크플로의 배달 활동에 삽입되지 않는 오류를 해결했습니다.
* 이메일 배달 활동의 아웃바운드 전환 타깃팅 차원이 표시되지 않는 오류를 해결했습니다.

#### 랜딩 페이지 {#landing-pages-2}

* 랜딩 페이지의 지역화 가능 콘텐츠 블록에서 개인화 필드가 제대로 작동하지 않는 오류를 해결했습니다.

#### 사용자 정의 리소스 {#custom-resources-4}

* 리소스 화면 정의의 **[!UICONTROL Add search fields]** 옵션을 선택하고 에서 여러 필드를 선택한 경우 사용자 지정 리소스에 대한 검색이 수행되지 않는 오류를 **[!UICONTROL Filter zone composition]** 수정했습니다.

## 릴리스 16.2 - 2016년 2월 {#release-16-2---february-2016}

### 새로운 기능 {#new-capabilities-7}

<table> 
 <thead> 
  <tr> 
   <th> 기능<br /> </th> 
   <th> 설명<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 이메일 A/B 테스트<br /> </td> 
   <td> 이제 이메일의 컨텐츠, 제목 또는 발신자 이름에 대한 A/B 테스트를 수행할 수 있습니다. 이 새로운 기능은 요소의 변형을 최대 3개까지 테스트할 수 있습니다.<br /> A/B 테스트와 관련된 새 템플릿 중 하나에서 이메일을 만들 때 만들기 마법사의 새 단계를 통해 테스트의 매개 변수를 정의할 수 있습니다.<br /> 자세한 내용은 <a href="../../channels/using/designing-an-a-b-test-email.md">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 브랜드 관리<br /> </td> 
   <td> 이제 하나 또는 여러 개의 브랜드를 정의하여 브랜드의 ID에 영향을 주는 매개 변수를 중앙에서 입력할 수 있습니다. Adobe Campaign을 사용하면 이러한 브랜드를 만들어 전달 또는 랜딩 페이지 템플릿에 연결할 수 있습니다.<br /> 자세한 내용은 <a href="../../administration/using/branding.md#assigning-a-brand-to-an-email">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 워크플로우:증분 쿼리<br /> </td> 
   <td> 새로운 워크플로우 활동인 <span class="uicontrol">증분 쿼리를</span> 사용하면 모든 실행에서 새 결과만 타깃팅하는 쿼리를 수행할 수 있습니다. 이전 실행 결과는 자동으로 제외됩니다. 스케줄러 <span class="uicontrol">활동에</span> 링크되어 증분 쿼리의 실행 빈도를 정의할 <span class="uicontrol">수 있습니다</span> .<br /> 자세한 내용은 <a href="../../automating/using/incremental-query.md">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 트랜잭션 메시지<br /> </td> 
   <td> 트랜잭션 메시지 인터페이스의 사용자 편의성이 개선되었습니다. 트랜잭션 메시지에 연결된 모든 비즈니스 프로세스 관리는 현재 마케팅 계획 <span class="uicontrol">&gt; 트랜잭션</span> 메시지 <span class="uicontrol">메뉴에서</span> 중앙 집중화된 상태입니다. 이벤트 구성도 향상되었습니다. 이제 이벤트는 사용자 지정 리소스와 독립적으로 관리됩니다.<br /> 자세한 내용은 <a href="../../channels/using/about-transactional-messaging.md">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### 패치 {#patches-7}

#### 일반 {#general-7}

* 보고서, 목록 및 쿼리의 몇 가지 표시 오류를 수정했습니다.
* 모바일 장치의 여러 호환성 및 표시 오류를 수정했습니다.

#### 이메일 및 SMS 메시지 {#emails-and-sms-messages-6}

* 메시지(이메일 또는 SMS)를 만들 때 개인화 필드를 삽입하는 데 사용되는 단추가 표시되지 않던 문제를 수정했습니다.
* Mblox를 통해 전송된 SMS 메시지가 올바르게 전송되지 않도록 하는 오류를 수정했습니다.

#### 대상 및 쿼리 {#audiences-and-queries-2}

* 필터링 차원을 수정한 후 쿼리에 추가 조건을 추가할 때 발생하던 계산 오류가 수정되었습니다.
* 쿼리 결과를 미리 볼 때 잘못된 페이지 매김을 초래할 수 있는 오류를 수정했습니다.

#### 컨텐츠 편집 {#content-editing-1}

* 개인화된 열거형을 사용할 때 동적 콘텐츠 구성이 올바르게 고려되지 않는 오류를 해결했습니다.

#### 워크플로우 {#workflows-5}

* 활동의 **[!UICONTROL Fields to update]** **[!UICONTROL Update data]** 탭에 빈 줄이 있는 경우 워크플로우의 어떤 작업도 수행되지 않도록 하는 오류를 수정했습니다.
* 지역/조직 단위 정보가 들어 있는 데이터를 가져올 수 없는 오류가 수정되었습니다.
* 규칙 **[!UICONTROL Change axis]** 유형을 추가하면 발생하는 오류가 **[!UICONTROL Exclusion]** 수정되었습니다.
* 활동의 아웃바운드 전환을 조작할 때 원치 않는 추가 세그먼트가 생성될 수 있는 오류를 **[!UICONTROL Segmentation]** 수정했습니다.
* 워크플로우 템플릿에서 파일을 로드하여 발생하는 오류를 수정했습니다.
* 공백이 **[!UICONTROL Load file]** 활동에서 열 구분 기호로 사용되지 않도록 하는 오류를 수정했습니다.

#### 사용자 정의 리소스 {#custom-resources-5}

* 리소스를 내보낼 때 게시한 경우 패키지를 가져온 후 사용자 지정 리소스의 상태가 다시 작성되지 않는 오류를 해결했습니다.

#### 패키지 {#packages}

* 워크플로가 포함된 패키지를 내보낼 수 없는 오류를 해결했습니다.
* 동일한 리소스의 여러 요소를 선택할 수 없는 오류가 수정되었습니다.

## 릴리스 16.1 - 2016년 1월 {#release-16-1---january-2016}

### 새로운 기능 {#new-capabilities-8}

<table> 
 <thead> 
  <tr> 
   <th> 기능<br /> </th> 
   <th> 설명<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 보고서<br /> </td> 
   <td> 다음과 같은 이메일 관련 보고서가 추가되었습니다. <span class="uicontrol">불만</span> , <span class="uicontrol">열기</span> 및 가입 <span class="uicontrol">취소</span> .<br /> 다음 보고서가 개선되었습니다.Delivery <span class="uicontrol"></span> , <span class="uicontrol">Delivery throughput</span> <span class="uicontrol"></span> , Tracking Summary <span class="uicontrol"></span> 및 Tracking Indicator.<br /> 자세한 내용은 <a href="../../reporting/using/defining-the-report-period.md">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 쿼리 편집<br /> </td> 
   <td> 쿼리 편집기가 개선되었으며 이제 <strong>1-N 유형 링크를 검색할 수</strong> 있습니다.<br /> 자세한 내용은 <a href="../../automating/using/editing-queries.md#creating-queries">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 콘텐츠 개인화<br /> </td> 
   <td> 이메일 또는 랜딩 페이지 편집의 경우 컨텐츠 블록 표시 조건을 위한 입력 인터페이스가 개선되었습니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 워크플로우:가져올 때 열 정의<br /> </td> 
   <td> 이제 <span class="uicontrol">파일</span> 로드 작업을 통해 가져온 파일의 열을 자세히 구성할 수 있습니다.데이터 유형, 날짜 및 시간 형식, 빈 값 또는 오류 발생 시 적용할 처리, 값 다시 매핑 등이 필요합니다.<br /> 자세한 내용은 <a href="../../automating/using/load-file.md#column-format">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> SMS 인코딩 매핑<br /> </td> 
   <td> 이제 표준 인코딩을 사용하지 않는 공급자에 대한 맞춤형 SMS 메시지 인코딩의 매핑을 정의할 수 있습니다. 관리자는 개인화된 매핑의 구성을 수행하고 이들이 고려해야 하는 순서를 정의할 수 있습니다.<br /> 자세한 내용은 <a href="../../administration/using/configuring-sms-channel.md#smsc-specifics">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### 패치 {#patches-8}

#### 일반 {#general-8}

* 하이브리드/터치스크린 장치용 Internet Explorer 및 Chrome과의 호환성이 개선되었습니다.
* 지정된 이메일 주소에 구문 오류가 있는 경우 새 사용자/프로필/테스트 프로필에 대해 입력한 모든 데이터가 손실될 수 있는 오류를 수정했습니다.

#### 이메일 및 SMS 메시지 {#emails-and-sms-messages-7}

* 이메일 미리 보기 화면에서 컨텐츠 축소판이 생성되지 않는 문제를 해결했습니다.
* 메시지 미리 보기 화면에 메시지의 원시 컨텐츠(이메일 또는 SMS)가 표시되지 않던 문제를 수정했습니다.

#### 대상 및 쿼리 {#audiences-and-queries-3}

* 서비스 리소스에서 쿼리 **유형** 대상자가 생성되지 않는 **오류를** 수정했습니다.
* 고급 모드에서 쿼리 조건을 편집할 때 함수 목록이 제대로 표시되지 않는 오류를 해결했습니다.
* 컬렉션을 기반으로 하는 기준이 **포함된 경우** 쿼리 유형 대상이 생성되지 않는 오류를 수정했습니다.
* 배달 KPI에 대한 필터가 포함된 쿼리를 만들지 못하는 오류를 해결했습니다.
* 워크플로에서 만든 대상의 컨텐츠를 미리 볼 수 없는 오류를 수정했습니다.

#### 사용자 정의 리소스 {#custom-resources-6}

* 사용자 지정 리소스에 동적 기본값이 있는 필드가 포함된 경우 서버 충돌을 야기할 수 있는 오류를 수정했습니다.
* 사용자 지정 리소스의 화면을 정의하는 동안 **[!UICONTROL Detail screen configuration]** 섹션에서 요소를 이동한 다음 삭제하여 발생하는 오류를 수정했습니다.
* 가능한 값 범위에 **0** 을 포함하지 않는 정수 **** 목록에 대해 기본값이 정의되었을 때 발생하는 오류를 수정했습니다.
* 재초기화 후 사용자 지정 리소스의 세부 화면 구성에 요소가 추가되지 않도록 하는 오류를 수정했습니다.

#### 워크플로우 {#workflows-6}

* 선택한 활동의 로그만 표시하는 대신 워크플로의 모든 활동 로그가 표시되던 오류를 수정했습니다.
* 활동의 오류를 **[!UICONTROL Scheduler]** 수정했습니다. 이 **[!UICONTROL Day of the month]** 옵션은 올바로 고려되지 않고 으로 대체되었습니다 **[!UICONTROL Week day]** .
* 만료 모드가 으로 설정된 상태에서 **[!UICONTROL Scheduler]** 활동이 제대로 작동하지 않는 오류를 **[!UICONTROL After a certain number of iterations]** 수정했습니다.
* 활동을 사용하여 데이터를 내보낼 때 발생하는 오류를 **[!UICONTROL Extract file]** 수정했습니다. 내보내기 파일에 있는 줄 수는 내보낸 요소 수보다 적습니다.
* 작업의 파일을 선택할 수 없는 오류를 **[!UICONTROL Load file]** 수정했습니다.
* 활동에서 업데이트할 필드를 삭제하지 못했던 **[!UICONTROL Update data]** 오류를 수정했습니다.
* 워크플로우 실행 로그를 연 후 워크플로우의 수정 사항이 저장되지 않는 오류를 해결했습니다.
* 인바운드 전환에서 파일을 사용하도록 구성하고 이 파일이 활동을 사용하여 로드된 경우 **[!UICONTROL Load file]** **[!UICONTROL Transfer file]** 활동이 두 번 실행되던 오류를 수정했습니다.
* 제외 활동에 의해 특정 임시 개체가 올바르게 처리되지 않는 오류를 **수정했습니다** .
* 타깃팅 차원과 활동에 구성된 필터링 차원이 다른 경우 **[!UICONTROL Query]** 활동이 올바르게 실행되지 않는 오류를 수정했습니다.
* 워크플로가 저장되지 않도록 할 수 있는 **[!UICONTROL Fork]** 활동에 추가된 아웃바운드 전환의 자동 이름 지정에 대한 오류를 수정했습니다.

#### 컨텐츠 편집 {#content-editing-2}

* 컨텐츠를 편집할 때 아이콘 또는 검색 막대가 불필요하게 표시되는 오류를 수정했습니다.

#### 랜딩 페이지 {#landing-pages-3}

* 패키지 가져오기를 사용하여 랜딩 페이지를 가져올 수 없는 오류가 수정되었습니다.

#### 트랜잭션 메시지 {#transactional-messages-4}

* 이제 메시지 센터 푸시 에이전트 연산자의 보안 매개 변수에서 신뢰할 수 있는 IP 주소를 지정할 수 있습니다.
* 새 유형의 이벤트가 생성되지 않도록 하는 오류를 수정했습니다.

## 릴리스 15.11 - 2015년 11월 {#release-15-11---november-2015}

### 새로운 기능 {#new-capabilities-9}

<table> 
 <thead> 
  <tr> 
   <th> 기능<br /> </th> 
   <th> 설명<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> SMS 채널<br /> </td> 
   <td> 이제 Adobe Campaign을 사용하여 SMS 메시지를 보낼 수 있습니다.<br /> 이메일과 마찬가지로 캠페인과 마케팅 활동 목록에서 새 SMS 배달을 만들 수 있습니다. 워크플로우에서 단일 전송 및 반복 SMS 메시지를 만들 수도 있습니다.<br /> 이러한 SMS 배달은 배달 템플릿 목록에서 구성할 수 있는 템플릿을 기반으로 합니다. 기본 템플릿을 사용할 수 있습니다.<br /> 이러한 SMS 전달은 대부분의 SMS 라우터가 사용하는 SMPP 3.4 프로토콜을 사용합니다.<br /> 자세한 내용은 <a href="../../channels/using/about-sms-messages.md">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 전환 탐색<br /> </td> 
   <td> 이제 워크플로우의 마지막 전환에서 데이터와 그 구조를 탐색할 수 있습니다. 이를 통해 각 활동에 의해 적용된 프로세스가 요구 사항에 해당하는지 확인할 수 있습니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 워크플로우에서 파일 사전 처리 및 사후 처리<br /> </td> 
   <td> 이제 파일 <span class="uicontrol">로드 및 파일</span> 추출 작업을 통해 데이터 파일을 가져오거나 내보낼 때 추가 처리를 수행할 <span class="uicontrol">수</span> 있습니다.<br /> 기본적으로 이러한 활동에서 GZIP 포맷 파일의 압축을 풀고 zip 파일을 압축 해제할 수 있습니다.<br /> 자세한 내용은 파일 <a href="../../automating/using/load-file.md">로드 및 파일</a><a href="../../automating/using/extract-file.md"></a> 추출 활동에 대한 설명서를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 배달 가능성 보고서<br /> </td> 
   <td> 이제 이메일 렌더링 보고서를 사용할 수 있습니다. 이 보고서에서는 메시지 읽기에 사용된 지원 및 메시지 서비스에 따라 메시지의 다른 렌더링을 볼 수 있습니다.<br /> 또한 보고서 요약에는 수신한 메시지, 스팸 메시지, 수신되지 않은 메시지 및 수신 대기 중인 메시지의 수도 나와 있습니다.<br /> 자세한 내용은 <a href="../../sending/using/email-rendering.md#email-rendering-report-description">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 패키지 관리<br /> </td> 
   <td> 이제 패키지에서 이미지를 가져오고 내보낼 수 있습니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 빠른 작업<br /> </td> 
   <td> 목록 또는 워크플로우에서 요소를 선택하거나 마우스로 가리키면 특정 작업이 나타납니다. 이러한 작업 중 일부는 이제 액세스를 용이하게 하기 위해 관련 요소 주위에 아이콘으로 표시됩니다. 이러한 빠른 작업은 요소를 복제하거나 삭제하고 세부 사항을 표시하는 데 사용할 수 있습니다.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### 패치 {#patches-9}

#### 일반 {#general-9}

* 관리자 계정에서 인스턴스의 일반 매개 변수에 액세스할 수 없는 오류가 수정되었습니다.
* **이제 사용자 지정 리소스에서 부동** 데이터가 올바르게 고려됩니다.
* 해당 템플릿의 상태가 수정되었을 때 발생하던 간소화된 가져오기 목록의 표시 오류를 수정했습니다.

#### 랜딩 페이지 {#landing-pages-4}

* 영어 인스턴스에서 프랑스어로 잘못 표시될 수 있는 랜딩 페이지 템플릿의 특정 요소를 수정했습니다.

#### Audiences {#audiences}

* Adobe Marketing Cloud에서 가져온 대상이 대상 목록에 표시되지 않던 오류를 수정했습니다.
* 쿼리를 정의할 때 대/소문자 구분을 강제 적용할 수 있는 오류를 수정했습니다.
* 쿼리를 정의할 때 대상이 필터링되지 않는 오류를 수정했습니다.
* 대상에서 작업이 취소되지 않도록 하는 오류가 수정되었습니다.

#### 워크플로우 {#workflows-7}

* 활동에서 업데이트될 필드를 수동으로 구성하지 못하게 하는 오류를 **[!UICONTROL Update data]** 수정했습니다.
* 다이어그램에 활동을 배치한 후 워크플로가 저장되지 않은 경우 열려 있는 경우 **[!UICONTROL Query]** 활동이 무한히 로드되는 오류를 수정했습니다.
* 워크플로우에서 선택한 대상을 카운트하거나 미리 보는 동안 서버가 중지되는 오류를 **[!UICONTROL Query]** 수정했습니다.
* 워크플로우의 활동이 열려 있을 때 나타날 수 있는 중요하지 않은 오류가 수정되었습니다.
* 하루에 여러 번 워크플로우를 실행하도록 **[!UICONTROL Scheduler]** 활동이 구성되지 않는 오류를 수정했습니다.
* 쿼리를 수행할 수 없는 필드가 특정 워크플로우 활동에 표시되던 오류를 수정했습니다.
* 사용자가 아웃바운드 전환의 게재에서 추가된 KPI를 찾을 수 없는 오류를 **[!UICONTROL Query]** 수정했습니다.
* 파일을 워크플로우로 가져온 후 파일 대상자가 생성되지 않는 문제를 해결했습니다.
* 리소스의 **위치/주소3** 필드를 사용하는 경우 프로필에서 데이터가 업데이트되지 않는 오류를 수정했습니다.
* 다양한 활동 컬렉션이 워크플로우에서 중복되지 않던 문제를 수정했습니다.
* SQL이 표시되지 않도록 하여 워크플로우에서 반복적으로 배달할 수 있는 오류를 진단하는 문제를 해결했습니다.

#### 컨텐츠 편집기 {#content-editor-1}

* 랜딩 페이지 또는 이메일의 소스 코드에서 검색이 불가능하게 만드는 오류를 수정했습니다.

#### 패키지 {#packages-1}

* 특정 유형의 요소를 패키지에서 내보내지(특히 랜딩 페이지, 워크플로우)하지 못하게 하는 다양한 오류를 수정했습니다.
* 레이블이 수정된 경우 이전 패키지 가져오기 레이블이 표시되던 오류를 수정했습니다.
* 내보내기 가능한 리소스 목록에 호환되지 않는 리소스가 표시되던 오류를 수정했습니다.

## 릴리스 15.10 - 2015년 10월 {#release-15-10---october-2015-}

### 새로운 기능 {#new-capabilities-10}

<table> 
 <thead> 
  <tr> 
   <th> 기능<br /> </th> 
   <th> 설명<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 워크플로우:데이터 중복 제거 작업<br /> </td> 
   <td> 이제 워크플로우에서 데이터 중복 제거에 관련된 새로운 활동을 사용할 수 있습니다. 이 활동을 사용하면 선택한 기준에 따라 타겟의 모든 중복을 필터링할 수 있습니다.<br /> 자세한 내용은 <a href="../../automating/using/deduplication.md">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 워크플로우:향상된 다이어그램<br /> </td> 
   <td> 이제 워크플로우 작업 영역에서 여러 키보드 단축키를 사용하여 활동을 선택, 열기 및 삭제할 수 있습니다.<br /> 또한 작업 정렬이 개선되어 워크플로우를 시각적으로 보다 효율적으로 구성할 수 있습니다.<br /> 자세한 내용은 <a href="../../automating/using/workflow-interface.md#workspace">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 워크플로우:파일 작업 추출<br /> </td> 
   <td> 이제 내보내기 날짜와 시간이 Extract 파일 <span class="uicontrol">활동을 사용하여 내보낸 파일의 레이블에 자동으로</span> 추가됩니다. 이렇게 생성된 파일은 고유합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 간소화된 데이터 가져오기<br /> </td> 
   <td> 간소화된 가져오기가 수행된 템플릿의 이름은 이제 가져오기 목록과 각 가져오기의 세부 사항에서 기본적으로 표시됩니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 사용자 정의 리소스<br /> </td> 
   <td> 사용자 지정 리소스에 대한 링크 관리 및 정의에 대한 개선 및 확장 가능성<br /> </td> 
  </tr> 
 </tbody> 
</table>

### 패치 {#patches-10}

#### 이메일 {#email}

* 미러 페이지에서 서비스 구독 취소 링크가 제대로 작동하지 않는 오류를 해결했습니다.
* 이메일 배달 레이블이 이메일 편집 페이지에서 올바르게 표시되지 않는 오류를 해결했습니다.
* 중복된 배달 템플릿에서 외부 **[!UICONTROL Routing]** 계정을 선택할 수 없는 오류가 수정되었습니다.

#### Audiences {#audiences-1}

* 쿼리에 1-N 링크가 사용된 경우 대상 수 중에 발생하는 오류가 수정되었습니다.
* 이메일 배달의 대상 대상자에서 프로필이 선택되지 않도록 하는 오류를 수정했습니다.

#### 워크플로우 {#workflows-8}

* 워크플로우에서 이메일 배달을 구성할 때 표시 문제를 일으킬 수 있는 오류를 수정했습니다.
* 활동이 제대로 작동하지 않는 오류를 **[!UICONTROL Load file]** 수정했습니다. 그러면 빈 오류 메시지가 나타납니다.
* 활동이 제대로 작동하지 않는 오류를 **[!UICONTROL Transfer file]** 수정했습니다. 액세스 권한이 항상 올바로 고려되는 것은 아니었다.
* 워크플로에 **[!UICONTROL Recurring email]** .
* 워크플로우에서 이메일 배달을 만들지 못하게 하거나 제목과 정의된 컨텐츠를 고려하지 못하게 하는 오류를 수정했습니다.
* 간소화된 가져오기 템플릿의 워크플로우를 구성할 때 **[!UICONTROL Update data]** 활동에서 조정 키가 선택되지 않도록 하는 오류를 수정했습니다.
* 활동이 삭제된 후 워크플로우가 저장되지 않는 문제를 해결했습니다.

#### 플랫폼 {#platform}

* 사용자 지정 리소스에 해당 요소의 리소스 유형에 대한 링크가 포함된 경우 새 요소가 생성되지 않도록 하는 오류를 수정했습니다.
* 특정 로그가 기록되는 데 15분 지연을 초래할 수 있는 오류를 수정했습니다.
* 마케팅 활동 목록이 **[!UICONTROL Date]** 또는 **[!UICONTROL Indicators]** 열별로 정렬될 때 표시되지 않는 오류를 수정했습니다.

#### 랜딩 페이지 {#landing-pages-5}

* 랜딩 페이지를 미리 보기 위해 테스트 프로필을 선택할 때 발생하는 오류를 수정했습니다.

#### 트랜잭션 메시지 {#transactional-messages-5}

* 테스트 프로필에서 이벤트를 삭제한 후 애플리케이션이 충돌할 수 있는 오류를 수정했습니다.

#### 보고서 {#reports}

* 보고서 및 에 대해 잘못된 데이터가 전송될 수 있는 오류를 **[!UICONTROL deliveryThroughputReport]** 수정했습니다 **[!UICONTROL deliveryTrackingReport]** .

#### 컨텐츠 편집기 {#content-editor-2}

* 다이내믹 컨텐츠 블록을 처리할 때 발생하는 HTML 태그 관리 오류를 수정했습니다.

## 릴리스 15.8 - 2015년 8월 {#release-15-8---august-2015}

### 새로운 기능 {#new-capabilities-11}

<table> 
 <thead> 
  <tr> 
   <th> 기능<br /> </th> 
   <th> 설명<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 간소화된 데이터 가져오기<br /> </td> 
   <td> 이제 데이터를 간단하게 가져올 수 있습니다.<br /> 사용자는 관리자가 미리 정의한 템플릿을 선택하고 가져올 데이터가 포함된 파일을 업로드하면 됩니다. 템플릿에 정의된 워크플로우는 사용자가 가져오기 결과의 세부 정보와 오류 로그에 액세스할 수 있도록 투명하게 실행됩니다.<br /> 이러한 파일의 데이터를 데이터베이스에 삽입하거나 대상을 직접 만드는 수단으로 사용할 수 있습니다.<br /> 자세한 내용은 <a href="../../automating/using/about-data-import-and-export.md">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 프로그램 및 캠페인 만들기<br /> </td> 
   <td> 이제 캠페인과 프로그램이 만들어진 날이 자동으로 시작 날짜로 사용되도록 구성됩니다.<br /> 종료 날짜는 다음과 같이 시작 날짜에 따라 구성됩니다.<br /> 
    <ul> 
     <li> 프로그램을 위한 D+186 </li> 
     <li> 캠페인을 위한 D+61 </li> 
    </ul> 자세한 내용은 <a href="../../start/using/programs-and-campaigns.md">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 이메일<br /> </td> 
   <td> 추적된 URL 목록은 이제 읽기 전용입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 트랜잭션 메시지<br /> </td> 
   <td> 이제 만들고 있는 계정의 암호 변경 또는 확인과 같은 이벤트에 대한 개인화된 트랜잭션 메시지를 관리할 수 있습니다.<br /> 자세한 내용은 <a href="../../channels/using/about-transactional-messaging.md">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 사용자 정의 리소스<br /> </td> 
   <td> 다음과 같은 몇 가지 기능이 추가되었습니다.테스트 프로필 확장, 상태 관리 및 리소스 삭제<br /> 자세한 내용은 <a href="../../developing/using/resource-statuses.md">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### 패치 {#patches-11}

#### 표시 {#display}

* Safari의 쿼리 편집기에서 두 필드를 병치하는 오류를 수정했습니다.

#### 컨텐츠 편집기 {#content-editor-3}

* 이메일 제목에 '&lt;', '&amp;' 및 '&gt;' 문자가 사용되지 않는 오류를 해결했습니다.

#### 이메일 {#email-1}

* 동적 텍스트 뒤에 사용자가 텍스트를 추가하지 못했던 오류가 수정되었습니다.

#### 목록 {#lists}

* 워크플로우 실행 로그의 **메시지** 열을 올바르게 내보내지 못하는 오류를 수정했습니다.

#### 프로필 및 대상 {#profiles-and-audiences}

* 요소가 중복 또는 삭제된 시기를 이중 확인하도록 하는 오류를 수정했습니다. **Internet Explorer 11만**&#x200B;사용하는 하이브리드 장치.

#### 워크플로우 {#workflows-9}

* 워크플로우에서 이메일이 전송되지 않도록 하는 오류가 수정되었습니다.
* 거부 파일 이름이 **[!UICONTROL Load file]** 활동에 지정되지 않은 경우 워크플로우가 실행되지 않는 오류를 해결했습니다.
* 활동 **[!UICONTROL Execution frequency]** 수가 로 설정되어 있을 때 워크플로우가 실행되지 않는 오류를 **[!UICONTROL Schedule]** **[!UICONTROL Daily]** 수정했습니다.

#### 플랫폼 {#platform-1}

* 부하 균형 지정 환경에서 축소판이 생성되지 않던 문제를 수정했습니다.

## 릴리스 15.7 - 2015년 7월 {#release-15-7---july-2015}

### 새로운 기능 {#new-capabilities-12}

<table> 
 <thead> 
  <tr> 
   <th> 기능<br /> </th> 
   <th> 설명<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 목록 내보내기<br /> </td> 
   <td> 이제 목록에서 컨텐츠를 CSV 형식으로 파일로 내보낼 수 있습니다. 이 함수는 목록 모드를 가진 모든 화면에서 사용할 <strong>수</strong> 있습니다(예:프로필 목록)을 참조하십시오.<br /> 내보낸 데이터는 내보낼 때 표시되는 열의 데이터입니다. 목록을 편집하여 내보낼 데이터를 선택할 수 있습니다.<br /> 이 기능 사용에 대한 자세한 내용은 <a href="../../automating/using/exporting-lists.md">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Adobe 프로필 및 대상과의 통합<br /> </td> 
   <td> 이제 Adobe Campaign과 다른 Adobe Marketing Cloud 솔루션 간에 대상을 공유할 수 있습니다.<br /> 
    <ul> 
     <li> 내보내기:워크플로에서 프로파일로 구성된 대상을 저장할 때 Adobe Marketing <span class="uicontrol">Cloud에서</span> 새 공유 옵션을 사용하면 기존 대상에 프로파일을 추가하거나 새 대상을 만들 수 있습니다. </li> 
     <li> 가져오기:대상 관리 <strong>화면에서 목록</strong> 유형 대상을 만들면 새 옵션을 사용하여 Adobe Marketing Cloud <span class="uicontrol">대상으로 식별할 수 있습니다</span> . 그런 다음 기존 공유 대상을 선택하여 Adobe Campaign으로 가져올 수 있습니다. </li> 
    </ul> 이 기능 구성 및 사용에 대한 자세한 내용은 <a href="../../integrating/using/about-campaign-audience-manager-or-people-core-service-integration.md">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 디지털 컨텐츠 편집기 - 다이내믹한 컨텐츠<br /> </td> 
   <td> 동적 컨텐츠 인터페이스가 개선되었습니다. 이제 이메일 본문에서 직접 서로 다른 동적 내용 간을 탐색할 수 있는 화살표가 나타납니다.<br /> 이 기능 사용에 대한 자세한 내용은 <a href="../../designing/using/personalization.md#defining-dynamic-content-in-an-email">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 디지털 컨텐츠 편집기 - 동적 텍스트<br /> </td> 
   <td> 이제 이메일의 컨텐츠 편집기에서 동적 텍스트를 정의할 수 있습니다.<br /> 
    <ul> 
     <li> 이메일 주제에서 </li> 
     <li> HTML 모드에서 </li> 
     <li> 또는 텍스트 모드로 전환할 수 있습니다. </li> 
    </ul>  이 기능 사용에 대한 자세한 내용은 <a href="../../channels/using/defining-dynamic-text.md">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 프로그램 및 캠페인 - 보고서<br /> </td> 
   <td> 보고서의 인터페이스와 그래픽이 개선되었습니다.<br /> 이 기능 사용에 대한 자세한 내용은 <a href="../../reporting/using/defining-the-report-period.md">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### 패치 {#patches-12}

#### 설치 {#installation}

* Adobe Campaign 인스턴스 이름은 이제 32자로 제한됩니다.

#### 워크플로우 {#workflows-10}

* 워크플로에서 쿼리를 편집할 때 '배달' 리소스를 타깃팅하지 못하는 오류를 수정했습니다.
* 워크플로에서 쿼리를 편집할 때 연결된 특정 리소스가 처리되지 않는 오류를 해결했습니다.
* 워크플로우가 이미 실행된 **경우 반복 배달** 활동이 수정되지 않는 오류를 수정했습니다.

#### 이메일 {#emails}

* 표현식 편집기를 통해 동적 컨텐츠가 추가되었을 때 이메일을 보내기 전에 JavaScript 구문 오류를 확인하지 못했던 오류가 수정되었습니다.

#### 랜딩 페이지 {#landing-pages-6}

* 태블릿에서 랜딩 페이지를 편집할 수 없는 오류를 수정했습니다.

#### 자산 핵심 서비스 {#assets-core-service}

* 편집 중인 이메일 또는 랜딩 페이지에서 공유 리소스를 선택하면 이제 Adobe Campaign에 대해 사용 가능한 리소스 목록이 필터링됩니다.

## 릴리스 15.6 - 2015년 6월 {#release-15-6---june-2015}

### 새로운 기능 {#new-capabilities-13}

<table> 
 <thead> 
  <tr> 
   <th> 기능<br /> </th> 
   <th> 설명<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 워크플로우:조정 활동<br /> </td> 
   <td> 새 <strong>조정</strong> 활동은 미확인 데이터(예: 파일을 가져온 후)를 워크플로우 내의 기존 리소스와 연결합니다.<br /> 이 활동은 기본적으로 데이터 관리 용도로 사용됩니다. 두 가지 다른 사용 사례에 응답합니다.<br /> 
    <ul> 
     <li> <strong>관계</strong>추가:관계 <strong>탭에서는</strong> 인바운드 데이터와 Adobe Campaign 데이터베이스의 다른 여러 차원 간에 링크를 추가할 수 있습니다. </li> 
     <li> <strong>데이터 식별</strong>:식별 <strong>탭을</strong> 사용하면 인바운드 데이터를 Adobe Campaign 데이터베이스의 기존 차원의 열에 간단히 연결할 수 있습니다. 활동이 종료되면 데이터는 지정된 차원에 속하는 것으로 식별됩니다. </li> 
    </ul> 자세한 <a href="../../automating/using/reconciliation.md">설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 워크플로우:파일 작업 추출<br /> </td> 
   <td> 새로운 <strong>Extract 파일</strong> 작업을 사용하면 워크플로우에서 외부 파일 형식으로 Adobe Campaign 데이터베이스에서 데이터를 내보낼 수 있습니다. <br /> 제한:현재 출력 파일에 동적 이름을 사용할 수 없습니다.<br /> 자세한 <a href="../../automating/using/extract-file.md">설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 워크플로우:스케줄러 활동<br /> </td> 
   <td> 워크플로우에서 스케줄러 <strong>활동의 실행 시간을 선택할 수</strong> 있는 향상된 위젯입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 워크플로우:파일 전송 작업<br /> </td> 
   <td> 이제 SFTP가 지원됩니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 사용자 정의 리소스<br /> </td> 
   <td> 이제 <span class="uicontrol">개발</span> 메뉴를 통해 관리 권한이 있는 사용자는 구매 또는 제품 테이블과 같은 사용자 지정 리소스를 만들어 제공되는 데이터 템플릿을 보완할 수 있습니다. <br /> 기본 리소스를 확장하여 새 필드를 추가할 수도 있습니다.<br /> 또한 새 사용자 지정 리소스 또는 확장된 사용자 지정 리소스에 해당하는 화면의 탐색을 구성할 수 있습니다.<br /> 자세한 <a href="../../developing/using/data-model-concepts.md">설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 테스트 프로필<br /> </td> 
   <td> 이제 <strong>테스트 프로필</strong> 목록을 구성할 때 테스트 프로필의 중간 이름과 <strong></strong> 제목을 선택할 수 있습니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 컨텐츠 편집기:동적 컨텐츠<br /> </td> 
   <td> 표현식 편집기를 통해 정의된 조건에 따라 사용자에게 동적으로 표시되는 다양한 컨텐츠를 정의할 수 있습니다.<br /> 자세한 <a href="../../designing/using/personalization.md#defining-dynamic-content-in-an-email">설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 이메일<br /> </td> 
   <td> 이제 <strong>이메일의 전송 로그에서 테스트 프로필</strong> 열을 사용할 수 있습니다.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### 패치 {#patches-13}

#### 목록 {#lists-1}

* 이제 목록에서 요소를 삭제하면 목록이 자동으로 새로 고쳐집니다.
* 하나의 열만 포함된 목록에서 요소를 선택할 수 없었던 오류를 수정했습니다.
* 페이지를 새로 고친 후 목록 표시에 적용된 변경 사항이 손실되는 문제를 해결했습니다.
* 이제 테스트 프로필 목록에 중간 이름과 테스트 프로필 제목을 모두 표시할 수 있습니다.
* Mozilla Firefox의 목록에서 확인란을 선택할 때 발생하는 오류가 수정되었습니다.

#### Audiences {#audiences-2}

* 대상 인터페이스에서 **[!UICONTROL Add]** 단추를 사용할 수 없는 오류가 수정되었습니다.

#### 이메일 {#emails-1}

* 이메일을 편집할 때 미리 보기 단추가 한 행에 두 번 사용되지 않는 JavaScript 오류를 수정했습니다.
* Internet Explorer 11을 사용하여 Microsoft Surface Pro3 태블릿에서 **[!UICONTROL Edit properties]** 및 **[!UICONTROL Show proofs]** 단추를 사용할 수 없는 오류를 수정했습니다.
* 이메일의 전송 로그가 표시되지 않던 문제를 수정했습니다.

#### 랜딩 페이지 {#landing-pages-7}

* 랜딩 페이지에서 컨텐츠를 편집할 **때 브랜드 로고** 컨텐츠 블록을 사용할 수 없는 오류를 수정했습니다.
* 랜딩 페이지에 대한 유효성 날짜가 지정된 경우 랜딩 페이지가 마케팅 활동 목록에 표시되지 않는 오류를 해결했습니다.

#### 워크플로우 {#workflows-11}

* 세그멘테이션 활동을 구성할 때 그룹 모드에서 세그먼트를 제한하면 제대로 작동하지 않는 **오류를** 해결했습니다.
* 세그멘테이션 활동을 구성한 후 전환을 선택할 수 없는 **오류를** 수정했습니다.
* 세그멘테이션 활동을 구성한 후 전환이 삭제되지 않는 **문제를** 수정했습니다.
* 세그멘테이션 활동 내에서 모집단이 계산되고 미리 볼 수 없는 **오류를** 수정했습니다.
* 되풀이되는 이메일이 효과적으로 삭제되지 않는 오류를 해결했습니다.
* 삭제된 전송 파일 **작업의 데이터가 새 전송 파일** 작업에 **표시되던** 오류를 수정했습니다.
* 제외 규칙이 제외 활동 내에서 올바로 고려되지 않는 **오류를** 수정했습니다.
* 워크플로우에서 이메일 배달 활동을 삭제할 때 발생하는 오류를 수정했습니다. 이제 해당 게재도 마케팅 활동 목록에서 제거됩니다.

#### 탐색 {#navigation}

* 이제 Tab 키를 사용하여 동일한 페이지의 필드 간을 제대로 탐색할 수 있습니다.

## 릴리스 15.4 - 2015년 4월 {#release-15-4---april-2015}

### 새로운 기능 {#new-capabilities-14}

<table> 
 <thead> 
  <tr> 
   <th> 기능<br /> </th> 
   <th> 설명<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 패키지 내보내기/패키지 가져오기<br /> </td> 
   <td> 이제 <strong>배포</strong> 메뉴를 통해 패키지를 내보내거나 가져와서 다른 Adobe Campaign 인스턴스 간에 리소스를 교환할 수 있습니다.<br /> 자세한 <a href="../../automating/using/managing-packages.md">설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 보고서<br /> </td> 
   <td> 이제 프로그램에서 모든 보고서( <strong>핫 클릭</strong> 보고서 제외)에 액세스할 수 있습니다. 이러한 보고서는 다음과 같습니다.<br /> 
    <ul> 
     <li> 프로그램 전달 처리량 </li> 
     <li> 프로그램 추적 표시기 </li> 
     <li> 도메인별 프로그램 분류 </li> 
     <li> 비결과물 및 바운스 프로그램 </li> 
     <li> 프로그램 URL 및 클릭 스트림 </li> 
    </ul> 이러한 보고서는 지정된 기간(예: 3개월, 6개월 등)에 걸쳐 필터링할 수 있습니다. 캠페인 보고서를 필터링할 수도 있습니다.<br /> 자세한 <a href="../../reporting/using/about-dynamic-reports.md">설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 워크플로우:이메일 <strong>배달</strong> 활동<br /> </td> 
   <td> 워크플로우의 <strong>이메일 배달</strong> 활동이 개선되었습니다. 이제 애플리케이션 마케팅 활동 목록에서 이메일, 반복 이메일 및 반복되는 이메일 실행에 대한 세부 정보를 찾을 수 있습니다.<br /> 자세한 <a href="../../automating/using/email-delivery.md">설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 워크플로우:세그멘테이션 <strong>활동</strong><br /> </td> 
   <td> 이제 <strong>워크플로우에서 세그멘테이션</strong> 활동을 사용할 수 있습니다. 이 활동을 사용하면 하나 또는 여러 개의 세그먼트를 만들고 동일한 워크플로우에서 업스트림에 배치된 활동에 의해 계산된 모집단에서 세그먼트 코드를 이러한 세그먼트에 연결할 수 있습니다. 이 활동에서 세그먼트는 하나의 전환 또는 다른 여러 전환으로 처리할 수 있습니다. 이제 인구를 필터링하고 각 세그먼트의 크기를 제한하여 개인화를 최적화할 수 있는 옵션이 있습니다. 예를 들어 특정 기준에 해당하는 프로파일을 임의로 선택할 수 있습니다.<br /> 자세한 <a href="../../automating/using/segmentation.md">설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 통합:자산 <strong>핵심 서비스</strong><br /> </td> 
   <td> 이제 이메일 및 랜딩 페이지 컨텐츠에서 자산 <strong>코어</strong> 서비스를 통해 공유 리소스를 사용할 수 있습니다. Adobe Marketing Cloud에서 바로 공유 리소스를 관리할 수 있습니다.<br /> 자세한 <a href="../../integrating/using/working-with-campaign-and-assets-core-service.md">설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 통합:Adobe <strong>Target</strong><br /> </td> 
   <td> 이제 Adobe Target에서 동적으로 계산된 이미지를 Adobe <strong>Campaign</strong> 이메일에 삽입할 수 있습니다. 이렇게 하면 Adobe Target 세그먼트에 정의된 기준에 따라 컨텐츠를 개인화하여 동일한 이메일의 여러 버전을 제공할 수 있습니다.<br /> 자세한 <a href="../../integrating/using/about-campaign-target-integration.md">설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 디지털 콘텐츠 편집기:블록 <strong>선택기</strong><br /> </td> 
   <td> HTML 컨텐츠 편집기에서 블록을 선택하면 편집 영역의 아래쪽에 탐색 표시가 표시됩니다. 이렇게 하면 다른 요소로 쉽게 이동하고 선택할 수 있습니다.<br /> 자세한 <a href="../../channels/using/designing-a-landing-page.md#managing-landing-page-structure-and-style">설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

## 릴리스 15.3 - 2015년 3월 {#release-15-3---march-2015}

### 새로운 기능 {#new-capabilities-15}

<table> 
 <thead> 
  <tr> 
   <th> 기능<br /> </th> 
   <th> 설명<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 보고서<br /> </td> 
   <td> 이제 프로그램이나 캠페인에서 직접 보고서에 액세스할 수 있습니다. 게재 <strong>요약</strong> 보고서가 프로그램 수준에서 추가되었습니다.<br /> 자세한 <a href="../../reporting/using/delivery-summary.md">설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 데이터 업데이트<br /> </td> 
   <td> 워크플로우에서 사용 가능한 <strong>데이터</strong> 업데이트 활동에는 새로운 옵션이 있으며, 이를 통해 인바운드 데이터 필드를 응용 프로그램 스키마의 필드와 자동으로 연결할 수 있습니다. 이렇게 하면 필드 업데이트를 위한 선택 프로세스를 용이하게 할 수 있습니다.<br /> 자세한 <a href="../../automating/using/update-data.md">설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 이메일 전달<br /> </td> 
   <td> 워크플로우에서 이제 작업 표시줄의 <strong>특정 단추를 통해 이메일 배달</strong> 활동의 고급 옵션에 액세스할 수 있습니다. 이 단추는 이메일 배달 <strong>활동을</strong> 선택한 경우에만 사용할 수 있습니다. 주된 이점은 활동에 아웃바운드 전환을 추가하고 워크플로우에 표시되는 활동 이름을 편집할 수 있다는 것입니다.<br /> 자세한 <a href="../../automating/using/email-delivery.md">설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### 패치 {#patches-14}

#### 일반 {#general-10}

* 배달을 만들 때 수신자가 표시되지 않던 오류를 수정했습니다.
* '열린 받는 사람' 조건을 기반으로 한 대상이 사용되지 않는 오류를 해결했습니다.
* 빈 프로필을 삭제할 수 없었던 오류를 수정했습니다.
* 배달을 미리 볼 때 발생하는 오류를 수정했습니다.
* 마케팅 활동이 중복되지 않는 오류를 수정했습니다.
* 캠페인을 삭제할 때 발생하는 오류를 수정했습니다.

