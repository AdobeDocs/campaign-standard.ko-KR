---
title: 릴리스 노트 2015-2016
seo-title: 릴리스 노트 2015-2016
description: 릴리스 노트 2015-2016
seo-description: 이 페이지에는 Adobe Campaign Standard의 2015 및 2016 릴리스가 모두 나열됩니다.
page-status-flag: 정품 인증 안 함
uuid: D 5 A 0 F 6 CC -0 BED -46 CF -8 DFF -1717 FB 624 F 8 F
contentOwner: Sauviat
products: sg_ campaign/standard
audience: RN
content-type: 참조
topic-tags: campaign-standard-release
discoiquuid: A 3 CE 6 B 80-1858-49 D 1-8880-3543181127 F 4
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Release Notes 2015-2016{#release-notes}

Adobe Campaign Standard 2015-2016 릴리스를 찾고 있습니까?

각 릴리스에는 새로운 기능과 패치가 포함되어 있습니다. 컨텐츠를 보려면 릴리스를 클릭합니다.

View the latest [documentation updates](../../rn/using/documentation-updates.md) for Adobe Campaign Standard. If you're looking for a newer release, consult this [page](../../rn/using/release-notes.md).

## Release 16.11 - November 2016 {#release-16-11---november-2016}

### New capabilities {#new-capabilities}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Deliverability exclusion rules<br /> </td> 
   <td> 암호화된 전역 억제 목록은 이제 배달 가능성 인스턴스에서 관리되므로 악의적인 활동, 특히 스팸 공격으로 인해 차단되지 않습니다.<br /> 각 이메일 배달에 대해 두 가지 기본 유형 규칙 규칙은 수신자 이메일 주소를 이 목록에 포함된 금지된 주소 또는 도메인 이름과 비교합니다. 일치하는 항목이 있으면 해당 수신자는 타겟 모집단에서 제외됩니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../administration/using/filtering-rules.md#default-deliverability-exclusion-rules"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> General optimization<br /> </td> 
   <td> 이 업데이트에는 고객이 발생하는 문제를 수정하는 다양한 변경 사항 및 패치가 포함되어 있습니다. The global platform performances have also been optimized. <br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches}

#### General {#general}

* 몇 가지 보안 문제가 해결되었습니다.
* REST API의 빈 필드 또는 중복 필드와 관련된 몇 가지 문제가 해결되었습니다.
* 이제 응용 프로그램의 홈 페이지에서 직접 SMS 메시지와 푸시 알림을 만들 수 있습니다.

#### Emails and SMS messages {#emails-and-sms-messages}

* 사용자가 컨텐츠 편집기에서 zip 파일을 업로드할 수 없는 문제를 수정했습니다.
* 문서를 전송한 후 열지 못하는 문제를 해결했습니다.
* Fixed an issue that led to an error message displaying when accessing the **[!UICONTROL Hot Clicks]** report on an A/B test email.
* Fixed an issue that prevented modifications made using the **[!UICONTROL Show source]** mode from being applied.
* 예측 주제 라인 XML 모델 파일을 가져올 수 없는 문제를 해결했습니다.
* A new screen dedicated to importing data for the subject line trained model is now available in **[!UICONTROL Administration > Channels > Emails > Predictive Subject Line]** .
* 관리자가 아닌 사용자가 이메일 구성 화면에서 허가된 마스크를 편집할 수 있었던 문제를 수정했습니다.

#### Push notifications {#push-notifications}

* Fixed an issue that prevented sending logs and event logs from being displayed for the recipients after sending a push notification using the **[!UICONTROL Send push on profiles]** template.
* 새 모바일 애플리케이션을 만들지 못하게 하는 문제를 해결했습니다.

#### Workflows {#workflows}

* Fixed a performance issue that occured when using the **[!UICONTROL Subscription]** activity.
* 내부 이름에 공백이 포함될 때 워크플로우가 작동하지 않는 문제를 해결했습니다.

#### Integrations {#integrations}

* Fixed an issue that could lead to an error being displayed when using the **Image shared from Adobe Marketing Cloud** option in an email.

#### Custom resources {#custom-resources}

* 확장된 API 필드의 두 발행물 간 향상된 API 로그 미리 보기.
* 사용자 지정 리소스가 게시되기 전에 삭제되지 않는 문제를 해결했습니다.
* 프로필 확장 및 식별자 키가 동적 필드로 설정되지 않는 문제를 해결했습니다.
* 사용자 지정 리소스에 링크를 추가할 때 발생할 수 있는 문제를 수정했습니다.

## Release 16.10 - October 2016 {#release-16-10---october-2016}

### New capabilities {#new-capabilities-1}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Email predictive subject line<br /> </td> 
   <td> 이메일을 편집할 때 새 옵션을 사용하면 다른 제목 선을 시도해보고 보내기 전에 열린 비율을 평가할 수 있습니다. 이전 배송 데이터를 기반으로 자체 모델을 트레이닝하거나 업종에 맞는 사전 정의된 모델을 사용함으로써 가능합니다. 이 기능은 이메일 메시지와 영어 컨텐츠만 포함된 데이터베이스에 사용할 수 있습니다. <br /> 활성화 및 사용에 대한 자세한 내용은 <a href="../../designing/using/personalizing-the-subject-line-of-an-email.md#predictive-subject-line">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> SMS transactional messaging<br /> </td> 
   <td> SMS 채널이 Adobe Campaign의 트랜잭션 메시징 기능에 추가되었습니다. 이제 트랜잭션 메시지에 대해 두 개의 채널이 지원됩니다. 이메일 및 SMS.<br /> 자세한 내용은 자세한 설명서를 <a href="../../administration/using/configuring-transactional-messaging.md#creating-an-event"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Follow-up message for transactional messaging<br /> </td> 
   <td> 이제 이벤트를 타깃팅하는 워크플로우를 만들 수 있습니다. 이것은 이전에 트랜잭션 메시지를 받은 고객에게 후속 메시지를 보낼 수 있음을 의미합니다. 이벤트 유형으로 대상을 필터링할 수 있으며, 이벤트는 확장된 로그 및 추적 로그를 제공합니다. 후속 메시지에서 이벤트 (페이로드) 의 컨텐츠를 활용할 수 있습니다. <br /> 자세한 내용은 자세한 설명서를 <a href="../../channels/using/follow-up-messages.md"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Extended Profile &amp; Services API<br /> </td> 
   <td> 이제 프로필 및 서비스 API에 확장 필드를 표시할 수 있습니다. API를 사용하면 API가 프로필 또는 서비스 사용자 지정 리소스의 확장된 필드를 매핑할 수 있습니다. For this to work, the <strong>Datamodel</strong> role has been added. 이 새 역할을 사용하면 사용자가 데이터 모델에 액세스할 수 있는 관리자 세트를 구성할 수 있습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../developing/using/updating-the-database-structure.md#publishing-a-resource-with-api-extension"></a>참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-1}

#### General {#general-1}

* 몇 가지 보안 문제가 해결되었습니다.

#### Emails and SMS messages {#emails-and-sms-messages-1}

* The SMS external account configuration screen ( **[!UICONTROL Administration > Channels > SMS > SMS accounts]** ) has been improved. Several parameters have been added in the **[!UICONTROL SMSC specifics]** section to support error codes in the "Text" field.

#### Push notifications {#push-notifications-1}

* Fixed an issue that prevented the predefined filters from being displayed when editing the audience of a push notification based on the **[!UICONTROL Send via push notification]** (mobileApp) template.
* The mobile application configuration screen ( **[!UICONTROL Administration > Channels > Push Notification > Mobile applications]** ) now displays a message to indicate that the iOS or Android platform has been successfully created.

#### Landing pages {#landing-pages}

* 랜딩 페이지 양식을 제출할 때 확인 이메일이 전송되지 않는 문제를 해결했습니다.

#### Audiences and queries {#audiences-and-queries}

* 쿼리 편집기에서 프로필을 선택할 때 발생하던 몇 가지 문제가 수정되었습니다.

#### Transactional messages {#transactional-messages}

* 트랜잭션 템플릿이 게시 취소되지 않던 오류를 수정했습니다.
* 이벤트 목록에 표시되는 이벤트를 트리거하는 문제를 해결했습니다.

#### Integrations {#integrations-1}

* 해당 대상이 업데이트된 후 공유 대상이 게시에 사용되지 않는 문제를 해결했습니다.
* Fixed an issue that prevented a shared asset ( **[!UICONTROL Image shared from Adobe Marketing Cloud]** option) from being used in a landing page.
* Adobe Audience Manager에서 가져온 공유 대상을 편집할 때 발생하는 문제가 수정되었습니다.

## Release 16.9 - September 2016 {#release-16-9---september-2016}

### New capabilities {#new-capabilities-2}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Remarketing Triggers<br /> </td> 
   <td> Integration between the core service <span class="uicontrol">Triggers</span> and Adobe Campaign allows you to send personalized emails to your customers as a reaction to specific behaviors that are tracked on your website by Adobe Analytics (within 15 minutes).<br /> Adobe Marketing Cloud 에서는 장바구니 또는 양식을 포기한 모든 클라이언트, 장바구니에서 제품을 제거했거나 세션이 만료된 클라이언트 등 모니터링하려는 고객 행동을 정의합니다. 트리거를 만들 때 트리거의 조건과 이벤트 (pload) 에 전송될 데이터를 Adobe Campaign에 정의합니다. <br /> Adobe Campaign에서 이전에 만든 트리거를 선택하면 datamart 데이터를 사용하여 이벤트 데이터를 강화하고 해당 트리거에 연결된 트랜잭션 메시지 템플릿을 정의합니다. 예를 들어 클라이언트가 장바구니를 포기하는 경우 Adobe Campaign로 이벤트가 전송되어 15 분 내에 클라이언트에 전송되는 재마케팅 이메일을 통해 이 이벤트를 활용할 수 있습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../integrating/using/about-adobe-experience-cloud-triggers.md"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Transactional messages: Pause / Unpublish<br /> </td> 
   <td> 이제 컨텐츠를 업데이트하는 동안 트랜잭션 템플릿의 게시를 일시 중단할 수 있습니다. 해당 메시지는 더 이상 전송되지 않지만 데이터베이스에 저장됩니다. 다시 시작할 때 대기열에 있는 메시지가 처리되고 만료되지 않은 경우 전송됩니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../channels/using/event-transactional-messages.md#suspending-a-transactional-message-publication"></a>참조하십시오.<br /> 이제 이벤트 및 트랜잭션 템플릿도 게시 취소할 수 있습니다. 해당 메시지는 더 이상 전송되지 않으며 데이터베이스에 저장되지 않습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../channels/using/event-transactional-messages.md#unpublishing-a-transactional-message"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Multibranding<br /> </td> 
   <td> 이제 여러 브랜드의 클라이언트가 동일한 인스턴스에서 관리할 수 있습니다. 브랜딩은 Adobe Campaign 인스턴스 관리자가 관리하는 기능으로, Adobe Campaign 내에서 브랜드와 관련된 모든 매개 변수를 중앙에서 구성할 수 있습니다. 여기에는 추적 URL, 웹 분석, 서버 URL, 도메인 이름 등과 같은 더 많은 기술 매개 변수에 로고와 같은 사항이 포함됩니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../administration/using/branding.md"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Responsive email design preview<br /> </td> 
   <td> 이 기능을 사용하면 다양한 유형의 디바이스에서 이메일의 응답성을 테스트할 수 있습니다. In the email preview, a grid has been added to test your email on various screen sizes.<br /> </td> 
  </tr> 
  <tr> 
   <td> Push notifications<br /> </td> 
   <td> 마케터가 iOS 및 Android 모바일 디바이스에서 개인화되고 세그먼트화된 푸시 알림을 전송할 수 있도록 새로운 채널이 추가되었습니다. 메시지는 단일 배달을 통해 보내거나 워크플로우 활동을 사용하여 전송할 수 있습니다. 트랜잭션 메시징과의 호환성은 향후 버전에서 사용할 수 있습니다. This channel leverages the Mobile core service’s SDK (available <a href="https://marketing.adobe.com/developer/gallery/marketing-cloud-mobile-libraries">here</a>).<br /> 자세한 내용은 자세한 설명서를 <a href="../../channels/using/about-push-notifications.md"></a>참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-2}

#### General {#general-2}

* 이 릴리스에서는 인터페이스 목록에 새로운 필터링 및 검색 기능을 도입했습니다. 이 새로운 기능은 로그 (예: 로그 (전달, 추적), 서비스 (구독, 구독 내역), 대상 및 워크플로우 전환) 에서 사용할 수 있습니다.
* 고객 프로필의 터치포인트 수와 관련된 몇 가지 표시 문제를 수정했습니다.
* 여러 유형 문제를 수정했습니다.

#### Emails and SMS messages {#emails-and-sms-messages-2}

* 잘못된 교정본을 편집할 수 있었던 오류를 수정했습니다. 이제 읽기 전용입니다.
* SMS가 너무 길거나 인코딩 문제가 발생했을 때 받는 사람이 블랙리스트에 추가되던 문제를 수정했습니다.

#### Custom resources {#custom-resources-1}

* 사용자 지정 리소스의 고급 필터를 사용할 때 모든 결과가 표시되지 않던 오류를 수정했습니다.

#### Transactional messages {#transactional-messages-1}

* 이제 접두사가 새 이벤트 정의의 식별자에 자동으로 추가됩니다.
* 인터페이스에서 트랜잭션 메시지를 나타내는 아이콘이 변경되었습니다.

#### Integrations {#integrations-2}

* Fixed a display error that would occur when a high resolution image was inserted via the **Dynamic image from Adobe Target** option.
* 대상 ID가 AMC 데이터 소스에서 설정되지 않았더라도 공유 대상이 저장될 수 있었던 오류를 수정했습니다.

## Release 16.7 - July 2016 {#release-16-7---july-2016}

### New capabilities {#new-capabilities-3}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Enriched transactional messages<br /> </td> 
   <td> 이제 트랜잭션 템플릿을 Adobe Campaign 데이터베이스와 연결하여 트랜잭션 메시지의 컨텐츠를 강화할 수 있는 정보를 복구할 수 있습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../administration/using/configuring-transactional-messaging.md#enriching-the-transactional-message-content"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Dynamic URLs for images<br /> </td> 
   <td> 이 새로운 기능을 사용하면 추적 및 개인화 목적으로 컨텐츠 블록과 동적 텍스트를 삽입하여 이미지 소스를 개인화할 수 있습니다.<br /> 그런 다음, 이미지 URL에 매개 변수를 입력하여 AEM 자산 (S 7) 다이내믹 미디어의 기능을 통해 이익을 얻는 것이 가능해집니다. 예를 들어 "Hello Alexandre, Paris에서 예정된 이벤트에 대한 최신 뉴스를 받아보십시오!" 라는 개인화된 이미지가 포함된 이메일을 보낼 수 있습니다. 또는 "Frank Frank, 뉴욕에서 예정된 이벤트에 대한 최신 뉴스를 받아보십시오!"<br /> 자세한 내용은 자세한 설명서를 <a href="../../designing/using/personalizing-urls.md"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Integration with People Core Service<br /> </td> 
   <td> The Adobe Marketing Cloud <strong>Declared IDs</strong> are now covered by the integration between Adobe Campaign and People Core Service (Profiles &amp; Audiences).<br /> 즉, 세그먼트를 가져오고 <strong>방문자 ID</strong>또는 <strong>선언된 ID로 구성된 대상을 내보낼</strong>수 있습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../integrating/using/about-campaign-audience-manager-or-people-core-service-integration.md"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Delivery logs<br /> </td> 
   <td> The MTA logs (delivery server) now display the complete history of each message, particularly all of the delivery attempts as well as the associated error statuses, and this has no impact on the application's performance.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-3}

#### General {#general-3}

* 완료해야 하는 필드가 아닌 관련 없는 필드를 표시할 수 있는 오류를 수정했습니다. 이것은 비교 연산자가 쿼리에서 조건을 편집할 때 여러 번 수정되면 발생합니다.
* Fixed the behavior of the option **[!UICONTROL The last X days/months/quarters/years]** when defining a relative filtering condition for a date field. 계산된 기간은 이제 달력 기반이 아닌 서버의 날짜 및 시간과 관련된 슬라이딩 기간입니다.

#### Workflows {#workflows-1}

* Fixed an error that would return an incorrect list of values in the screen for selecting the targeting dimension in the properties of a **[!UICONTROL Query]** activity.
* Fixed an error that would force the **Exists** operator to be selected when adding an average or count aggregate on a collection element in a **[!UICONTROL Query]** activity.

#### Content editing {#content-editing}

* HTML 컨텐츠를 가져올 때 표시 문제 (응답형 디자인) 를 발생시킬 수 있는 오류를 수정했습니다. 가져온 후 처음 콘텐트를 열 때 스타일 속성이 다시 작성되지 않습니다.
* 동적 컨텐츠 변형에 조건이 추가될 때 발생하는 비블로킹 오류를 수정했습니다.
* 랜딩 페이지의 컨텐츠에 확인란을 추가하여 발생하는 오류를 수정했습니다. 확인란을 사용할 수 없습니다.
* 커서가 문제의 블록의 시작 부분에 배치된 경우 블록의 텍스트를 삭제할 때 발생할 수 있는 오류를 수정했습니다.

#### Transactional messages {#transactional-messages-2}

* 이제 웹 사이트를 통합할 때 해당 이벤트에 대한 만료 날짜를 정의할 수 있습니다. 이 날짜가 지나면 이벤트에 해당하는 메시지가 더 이상 전송되지 않을 수 있습니다.

## Release 16.6 - June 2016 {#release-16-6---june-2016}

### New capabilities {#new-capabilities-4}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Profiles and Services API<br /> </td> 
   <td> The Adobe Campaign <span class="uicontrol">Profiles and Services</span> API is available in the <a href="https://www.adobe.io/products/campaign">adobe.io</a> portal. 이렇게 하면 Adobe Campaign 프로필을 업데이트, 추가 및 삭제할 수 있으며 REST 호출을 통해 서비스에 가입하거나 가입을 해지할 수 있습니다.<br /> 자세한 내용은 API에 대한 <a href="https://docs.campaign.adobe.com/doc/standard/en/adobeio.html">자세한 설명을</a>참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-4}

#### General {#general-4}

* 이제 모바일 장치에서 도구 설명이 비활성화되어 화면에 표시되는 정보를 쉽게 읽을 수 있습니다.
* 사용자가 iPad 화면에서 특정 영역의 컨텐츠를 스크롤하지 못했던 오류를 수정했습니다.
* Internet Explorer 11에서 컨텐츠를 편집하는 동안 발생하는 몇 가지 호환성 오류가 수정되었습니다.
* 데이터 가져오기가 처음 실패할 때 세부 로그에 액세스할 수 없는 오류를 해결했습니다.
* 범위 필터가 저장되지 못하게 하는 오류를 해결했습니다.
* 목록이 표시되는 방식을 구성할 때 리소스 요소가 표시되지 않던 오류를 수정했습니다.
* 쿼리 편집기 탐색기에서 오류가 수정되었습니다. 검색 필드에서 반환된 결과가 검색 내역에 유지되었으며 모든 새 검색에서 계속 표시됩니다.

#### Emails and SMS messages {#emails-and-sms-messages-3}

* 바운스 수에 연결된 정보가 배달 로그에서 복구되지 않던 오류를 수정했습니다.
* 트랜잭션 메시지의 동적 컨텐츠 블록에 있는 컨텍스트가 액세스되지 않는 오류를 해결했습니다.
* 이메일 컨텐츠의 동적 텍스트에 URL 링크가 정의되지 않던 오류를 수정했습니다.
* 배달 작성 마법사의 상단 막대 표시를 수정했습니다.
* 게재의 기본 키는 더 이상 개인화 필드로 사용할 수 없습니다.

#### Workflows {#workflows-2}

* 워크플로우의 두 활동 간 전환에는 한 활동에서 다른 활동으로 계산되고 전송된 요소의 수가 표시됩니다.
* Incompatible fields are now hidden when additional data is added in a **[!UICONTROL Query]** activity.
* 추가 데이터를 추가할 때 표시되는 집계 정의 창이 사용 중인 데이터와 호환되는 옵션 (예: 평균 계산은 숫자 데이터에만 가능합니다.
* 이제 곧바로 사용 가능한 기술 워크플로우를 시작하거나 다시 시작할 때 관리 권한이 있는 사용자만 수행할 수 있습니다.

#### Landing pages {#landing-pages-1}

* 랜딩 페이지의 속성에서 32 비트 AES 코딩 키를 잘릴 수 있는 오류를 수정했습니다.
* 가시성 조건을 정의할 때 또는 랜딩 페이지에 동적 컨텐츠를 추가할 때 쿼리 편집기가 올바르게 표시되지 않는 오류를 해결했습니다.

#### Custom resources {#custom-resources-2}

* The **[!UICONTROL Switch to parameters]** option is now hidden when defining a filter related to a profile's subscriptions to a service.
* 0-1 유형 링크가 사용자 지정 리소스에서 구성되었을 때 발생할 수 있었던 오류를 수정했습니다.
* Fixed an error that, where relevant, could prevent the defined **Constant default value** from being edited when adding a **Date and time** type field in a custom resource.

## Release 16.5 - May 2016 {#release-16-5---may-2016}

### New capabilities {#new-capabilities-5}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Predefined filters<br /> </td> 
   <td> 관리자는 이제 사전 구성된 규칙 형태의 쿼리 편집기에 표시되는 고급 필터를 만들 수 있습니다. 이러한 필터를 선택하면 사용자가 대상자를 정의할 때 단순화된 인터페이스를 통해 복잡한 구성을 보다 쉽게 개발할 수 있습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../developing/using/configuring-filter-definition.md"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: Subscription Services<br /> </td> 
   <td> A new <span class="uicontrol">Subscription Services</span> activity offers the possibility of subscribing several profiles to a service or unsubscribing them from a service with in a single action.<br /> 이 활동은 타깃팅을 수행한 후 또는 식별된 데이터로 파일을 가져온 후 사용할 수 있습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../automating/using/subscription-services.md"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: data enrichment<br /> </td> 
   <td> The <span class="uicontrol">Additional data</span> tab is now available in <span class="uicontrol">Query</span> type activities. 이 기능을 사용하면 쿼리에 의해 타깃팅된 데이터를 강화하고 이 데이터를 악용될 수 있는 다음 워크플로우 활동에 전송할 수 있습니다.<br /> 추가 데이터를 추가한 후 정의된 추가 데이터를 기반으로 조건을 만들어 처음에 타깃팅된 데이터에 추가 필터 수준을 적용할 수 있습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../automating/using/query.md#enriching-data"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Contextual help<br /> </td> 
   <td> 이제 다양한 Adobe Campaign 화면에서 컨텍스트 도움말 기능을 사용할 수 있습니다. 즉, 한 번의 클릭으로 현재 사용 중인 기능에 대한 설명서에 직접 액세스할 수 있습니다. 컨텍스트 도움말을 표시하려면 '?' icon in the upper-right corner of the screen, as shown in the example below.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-5}

#### General {#general-5}

* 다양한 인터페이스 Marketing Cloud 표준을 준수하는 새로운 기능입니다.
* 다른 드롭다운 목록 유형 표준화.

#### Emails and SMS messages {#emails-and-sms-messages-4}

* 오류 주소 마스크가 지정된 경우 이메일이 전송되지 않는 오류를 해결했습니다.
* 이제 TLS 프로토콜이 이메일 배달을 위해 지원됩니다. MX 관리의 새로운 열을 사용하면 각 도메인에 대해 원하는 TLS 동작을 정의할 수 있습니다.
* SMS 인터페이스가 개선되었습니다.

#### Workflows {#workflows-3}

* 다양한 워크플로우 인터페이스 새로운 기능.
* 빠른 작업을 표시할 때 발생하는 오류를 수정했습니다.
* Fixed an error that could cause a workflow to fail when using a **[!UICONTROL Segmentation]** type activity containing a 1-N link.
* 워크플로우 전환이 하이브리드 장치에서 열리지 않는 오류를 해결했습니다.
* 워크플로우 시작 시 일시 중지 단추가 표시되지 않는 오류를 해결했습니다.

#### Content editor {#content-editor}

* 이제 컨텐츠 편집기를 사용하여 이메일 또는 랜딩 페이지에 포함된 URL를 개인화할 수 있습니다. [](../../designing/using/personalizing-urls.md)자세한 내용은 설명서를 참조하십시오.
* 이미지가 전달의 만들기 마법사에 추가되었고 이후에 해당 컨텐츠가 수정된 경우 이미지가 손실될 수 있었던 오류를 수정했습니다.

#### Custom resources {#custom-resources-3}

* 사용자 지정 리소스의 구성 화면에 개인화된 1-n 유형 링크를 추가할 때 발생하는 오류를 수정했습니다.
* 사용자 지정 리소스를 준비하고 게시할 때 진행률 표시줄이 표시되었습니다.
* 사용자 지정 리소스의 링크 목록을 표시할 때 발생하는 오류가 수정되었습니다.

#### Transactional messages {#transactional-messages-3}

* 인터페이스의 사용자 친화성과 트랜잭션 메시지 엔진의 성능 및 견고성이 최적화되었습니다.
* 이제 트랜잭션 메시지 템플릿의 게시를 일시적으로 중단할 수 있습니다. For more on this, refer to the [detailed documentation](../../channels/using/event-transactional-messages.md#suspending-a-transactional-message-publication).
* 호환되지 않는 타깃팅 차원이 있는 컨텐츠 블록이 트랜잭션 메시지 템플릿에 추가될 수 있는 오류를 수정했습니다.
* API 미리 보기가 이벤트 구성 화면에 표시되지 않는 오류를 해결했습니다.

#### Audiences and queries {#audiences-and-queries-1}

* 쿼리 편집기에서 날짜 사용에 대한 다양한 패치. [](../../automating/using/editing-queries.md#creating-queries)자세한 내용은 설명서를 참조하십시오.

#### Administration {#administration}

* 사용자가 로그인할 수 없는 "표준 사용자" 보안 그룹의 이름에 대한 오류가 수정되었습니다.

## Release 16.3 - March 2016 {#release-16-3---march-2016}

### New capabilities {#new-capabilities-6}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Interface and navigation<br /> </td> 
   <td> Adobe Campaign 인터페이스가 개선되어 탐색과 작업을 간단하고 직관적으로 수행할 수 있었습니다.<br /> 이제 애플리케이션의 상단 막대에서 탐색합니다. The advanced menus are accessible by selecting the <strong>Adobe Campaign</strong> logo.<br /> 자세한 내용은 자세한 설명서를 <a href="../../start/using/interface-description.md"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: Save audience<br /> </td> 
   <td> A new option, <span class="uicontrol">Create then update an audience</span> , is now available in the <span class="uicontrol">Save audience</span> activity. 이 옵션을 사용하면 대상 레이블을 수동으로 입력할 수 있습니다. 입력한 레이블이 기존 대상에 해당하면 업데이트됩니다. 대상이 존재하지 않는 경우 만들어집니다.<br /> 또한 대상이 실행될 때마다 대상이 업데이트됩니다 (다시).<br /> 항상 대상 업데이트 모드를 선택할 수 있습니다. 새로운 데이터로 대상을 완료하거나 모든 실행 시 대상 데이터의 전체를 바꿉니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../automating/using/save-audience.md"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: Segmentation<br /> </td> 
   <td> <span class="uicontrol">이제 세그멘테이션</span> 활동을 통해 임시 리소스의 데이터를 세그먼트화할 수 있습니다. 예를 들면 다음과 같습니다. 가져온 파일의 데이터입니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../automating/using/segmentation.md"></a>참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-6}

#### General {#general-6}

* 목록을 정렬할 때 발생하는 표시 오류를 수정했습니다. 열의 정렬 순서를 나타내는 화살표는 특정 유형의 데이터에 대해서만 반전할 수 있습니다.
* 쿼리에 규칙이 추가되었을 때 드롭다운 메뉴에 표시되는 요소 수를 제한하는 오류를 수정했습니다.

#### Emails and SMS messages {#emails-and-sms-messages-5}

* 이메일 렌더링 보고서에 대한 액세스를 차단할 수 있는 오류를 수정했습니다.
* 이제 보낸 사람 주소가 제공되지 않으면 메시지의 전송 준비 단계에서 오류가 반환됩니다.

#### Workflows {#workflows-4}

* CSV 포맷 파일을 추출할 때 특정 파일 서식 옵션이 표시되었지만 고려되지는 않았습니다. 이제 이러한 옵션이 더 이상 표시되지 않습니다.
* Fixed an error caused when the **[!UICONTROL Delete the source files after transfer]** option was checked for a **[!UICONTROL SFTP]** type file transfer.
* Fixed an error that could prevent the counter and preview of **[!UICONTROL Query]** data from being displayed after refreshing the page.
* 특히 배달 활동 또는 필터링 및 필터링 차원이 다른 쿼리 후에 워크플로우에서 특정 전환을 열 때 발생하는 오류를 수정했습니다.
* 활동을 추가한 후에 워크플로우가 저장되지 않은 경우 개인화 필드가 워크플로우의 전달 활동에 삽입되지 않는 오류를 해결했습니다.
* 이메일 배달 활동의 아웃바운드 전환 타깃팅 차원이 표시되지 않는 오류를 해결했습니다.

#### Landing pages {#landing-pages-2}

* 랜딩 페이지의 현지화할 수 있는 컨텐츠 블록에서 개인화 필드가 제대로 작동하지 않는 오류를 해결했습니다.

#### Custom resources {#custom-resources-4}

* Fixed an error that prevented a search on a custom resource from being carried out if the **[!UICONTROL Add search fields]** option of the resource screen definition was checked and if several fields were selected in the **[!UICONTROL Filter zone composition]** .

## Release 16.2 - February 2016 {#release-16-2---february-2016}

### New capabilities {#new-capabilities-7}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> A/B test for emails<br /> </td> 
   <td> 이제 이메일의 컨텐츠, 제목 또는 보낸 사람 이름에 대한 A/B 테스트를 수행할 수 있습니다. 이 새로운 기능은 요소의 변형을 최대 3 개까지 테스트할 수 있습니다.<br /> A/B 테스트와 관련된 새 템플릿 중 하나에서 이메일을 만들 때 만들기 마법사의 새로운 단계를 통해 테스트 매개 변수를 정의할 수 있습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../channels/using/designing-an-a-b-test-email.md"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Brand management<br /> </td> 
   <td> 이제 한 개 또는 여러 브랜드를 정의하여 브랜드 ID에 영향을 주는 매개 변수를 중앙에서 입력할 수 있습니다. Adobe Campaign를 사용하면 이러한 브랜드를 만들고 배달 또는 랜딩 페이지 템플릿에 연결할 수 있습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../administration/using/branding.md#assigning-a-brand-to-an-email"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: Incremental query<br /> </td> 
   <td> A new workflow activity, <span class="uicontrol">Incremental query</span> , allows you to carry out a query which, on every execution, targets only the new results. 이전 실행의 결과는 자동으로 제외됩니다. <span class="uicontrol">스케줄러</span> 활동과 연결된 <span class="uicontrol">경우 증분 쿼리의 실행 빈도를 정의할</span> 수 있습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../automating/using/incremental-query.md"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Transactional messages<br /> </td> 
   <td> 트랜잭션 메시지 인터페이스의 사용자 친화성이 개선되었습니다. All business process management linked to transactional messages is currently centralized in the <span class="uicontrol">Marketing plans</span> &gt; <span class="uicontrol">Transactional messages</span> menu. 이벤트 구성이 향상되었습니다. 이벤트는 이제 사용자 지정 리소스와 독립적으로 관리됩니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../channels/using/about-transactional-messaging.md"></a>참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-7}

#### General {#general-7}

* 보고서, 목록 및 쿼리의 여러 표시 오류를 수정했습니다.
* 모바일 장치에서 여러 호환성 및 표시 오류를 수정했습니다.

#### Emails and SMS messages {#emails-and-sms-messages-6}

* 메시지 (이메일 또는 SMS) 를 만들 때 개인화 필드를 삽입하는 데 단추가 표시되지 않는 오류를 해결했습니다.
* mblox를 통해 전송된 SMS 메시지가 제대로 전송되지 못하게 하는 오류를 해결했습니다.

#### Audiences and queries {#audiences-and-queries-2}

* 필터링 차원을 수정한 후 쿼리에 추가 조건을 추가할 때 발생할 수 있는 계산 오류를 수정했습니다.
* 쿼리 결과를 미리 볼 때 잘못된 페이지로 연결될 수 있는 오류를 수정했습니다.

#### Content editing {#content-editing-1}

* 개인화된 열거 사용 시 다이내믹 컨텐츠 구성이 제대로 고려되지 않는 오류를 해결했습니다.

#### Workflows {#workflows-5}

* Fixed an error that could prevent any action in a workflow from being carried out if there was an empty line in the **[!UICONTROL Fields to update]** tab of an **[!UICONTROL Update data]** activity.
* 지리적/조직 단위 정보가 들어 있는 데이터를 가져올 수 없는 오류를 수정했습니다.
* Fixed an error caused by adding a **[!UICONTROL Change axis]** type of **[!UICONTROL Exclusion]** rule.
* Fixed an error that could lead to an unwanted additional segment being created when manipulating an outbound transition of a **[!UICONTROL Segmentation]** activity.
* 워크플로우 템플릿에서 파일을 로드하여 발생하는 오류를 수정했습니다.
* Fixed an error that could prevent spaces from being used as column separators in a **[!UICONTROL Load file]** activity.

#### Custom resources {#custom-resources-5}

* 내보내기 시간에 리소스가 게시된 경우 패키지를 가져온 후 사용자 지정 리소스의 상태가 다시 작성되지 않는 오류를 해결했습니다.

#### Packages {#packages}

* 워크플로우가 들어 있는 패키지를 내보낼 수 없는 오류를 수정했습니다.
* 동일한 리소스의 여러 요소를 선택할 수 없는 오류를 수정했습니다.

## Release 16.1 - January 2016 {#release-16-1---january-2016}

### New capabilities {#new-capabilities-8}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Reports<br /> </td> 
   <td> The following email specific reports have been added: <span class="uicontrol">Complaints</span> , <span class="uicontrol">Opens</span> , and <span class="uicontrol">Unsubscriptions</span> .<br /> 다음 보고서가 개선되었습니다. <span class="uicontrol">배달 요약</span> , <span class="uicontrol">바운스 요약</span> , <span class="uicontrol">배달 처리량</span> 및 <span class="uicontrol">추적 표시기</span> .<br /> 자세한 내용은 자세한 설명서를 <a href="../../reporting/using/defining-the-report-period.md"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Query editing<br /> </td> 
   <td> The query editor has been improved and now allows you to scan the <strong>1-N</strong> type links.<br /> 자세한 내용은 자세한 설명서를 <a href="../../automating/using/editing-queries.md#creating-queries"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Content personalization<br /> </td> 
   <td> As for email or landing page editing, the input interface for content block display conditions has been improved.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: column definition when importing<br /> </td> 
   <td> <span class="uicontrol">이제 파일 로드</span> 활동을 통해 가져온 파일의 열을 자세히 구성할 수 있습니다. 예상 데이터 유형, 날짜 및 시간 형식, 빈 값 또는 오류 시 처리가 적용되는 처리, 값 재매핑이 필요합니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../automating/using/load-file.md#column-format"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Mapping of SMS encodings<br /> </td> 
   <td> 이제 표준 인코딩을 사용하지 않는 공급자에 대해 개인화된 SMS 메시지의 인코딩에 대한 매핑을 정의할 수 있습니다. 관리자는 개인화된 매핑의 구성을 수행하고 해당 매핑을 고려해야 하는 순서를 정의할 수 있습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../administration/using/configuring-sms-channel.md#smsc-specifics"></a>참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-8}

#### General {#general-8}

* 하이브리드/터치스크린 장치를 위한 Internet Explorer 및 크롬과의 호환성이 개선되었습니다.
* 지정된 이메일 주소에 구문 오류가 포함된 경우 새 사용자/프로필/테스트 프로필에 대해 입력한 모든 데이터가 손실될 수 있는 오류를 수정했습니다.

#### Emails and SMS messages {#emails-and-sms-messages-7}

* 이메일 미리 보기 화면에서 컨텐츠 썸네일이 생성되지 않도록 하는 오류를 해결했습니다.
* 메시지 미리 보기 화면에서 메시지 (이메일 또는 SMS) 의 원시 컨텐츠가 표시되지 않는 오류를 해결했습니다.

#### Audiences and queries {#audiences-and-queries-3}

* Fixed an error that could prevent a **Query** type audience from being created in the **Service** resource.
* 고급 모드에서 쿼리의 조건을 편집할 때 함수 목록이 올바르게 표시되지 않는 오류를 해결했습니다.
* Fixed an error that could prevent a **Query** type audience from being created if it contained criteria based on collections.
* 배달 KPI에서 필터가 포함된 쿼리를 만들 수 없는 오류를 수정했습니다.
* 워크플로우에서 만든 대상의 컨텐츠를 미리 보지 못하게 하는 오류를 해결했습니다.

#### Custom resources {#custom-resources-6}

* 사용자 지정 리소스에 동적 기본값이 있는 필드가 포함된 경우 서버 충돌이 발생할 수 있는 오류를 수정했습니다.
* Fixed an error caused by moving, then deleting an element in the **[!UICONTROL Detail screen configuration]** section while defining screens of a custom resource.
* Fixed an error that occurred when a default value had been defined for an **integer** list that did not include **0** in its range of possible values.
* 재초기화 후 사용자 지정 리소스의 세부 사항 화면 구성에 요소가 추가되지 못하게 하는 오류를 해결했습니다.

#### Workflows {#workflows-6}

* 워크플로우에서 선택한 활동의 일부만 표시하는 대신 워크플로우에서 모든 활동의 로그가 표시되는 오류를 해결했습니다.
* Fixed an error in the **[!UICONTROL Scheduler]** activity. **[!UICONTROL Day of the month]** 옵션이 제대로 **[!UICONTROL Week day]** 고려되지 않고 대체되었습니다.
* Fixed an error that could prevent a **[!UICONTROL Scheduler]** activity from working correctly with the expiration mode set to **[!UICONTROL After a certain number of iterations]** .
* Fixed an error that occurred when exporting data using an **[!UICONTROL Extract file]** activity. 내보내기 파일에 있는 라인 수가 내보낸 요소 수보다 적습니다.
* Fixed an error that could prevent a file in a **[!UICONTROL Load file]** activity from being selected.
* Fixed an error that prevented fields that were to be updated in an **[!UICONTROL Update data]** activity from being deleted.
* 워크플로우 실행 로그를 연 후 워크플로우에 대한 수정 사항이 저장되지 않던 오류를 수정했습니다.
* Fixed an error that caused a **[!UICONTROL Load file]** activity to be executed twice if it was configured to use the file from its inbound transition and this file had been loaded using a **[!UICONTROL Transfer file]** activity.
* **제외** 활동에 의해 특정 임시 개체가 올바로 처리되지 못하게 하는 오류를 해결했습니다.
* Fixed an error that could prevent a **[!UICONTROL Query]** activity from being executed correctly if the targeting dimension and the filtering dimension configured in the activity were different.
* Fixed an error concerning the automatic naming of outbound transitions added to a **[!UICONTROL Fork]** activity that could prevent the workflow from being saved.

#### Content editing {#content-editing-2}

* 컨텐츠를 편집할 때 아이콘이나 검색 막대가 크게 표시되는 오류를 수정했습니다.

#### Landing pages {#landing-pages-3}

* 패키지 가져오기를 사용하여 랜딩 페이지를 가져올 수 없는 오류를 수정했습니다.

#### Transactional messages {#transactional-messages-4}

* 이제 메시지 센터 푸시 에이전트 연산자의 보안 매개 변수에서 신뢰할 수 있는 IP 주소를 지정할 수 있습니다.
* 새 이벤트 유형을 만들지 못하게 하는 오류를 수정했습니다.

## Release 15.11 - November 2015 {#release-15-11---november-2015}

### New capabilities {#new-capabilities-9}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> SMS Channel<br /> </td> 
   <td> 이제 Adobe Campaign로 SMS 메시지를 보낼 수 있습니다.<br /> 이메일과 마찬가지로 캠페인 및 마케팅 활동 목록에서 새 SMS 배달을 만들 수 있습니다. 워크플로우에서 단일 전송 및 반복되는 SMS 메시지도 만들 수 있습니다.<br /> 이러한 SMS 배달은 배달 템플릿 목록에서 구성할 수 있는 템플릿을 기반으로 합니다. 기본 템플릿을 사용할 수 있습니다.<br /> 이러한 SMS 전달은 대부분의 SMS 라우터에서 사용되는 SMPP 3.4 프로토콜을 사용합니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../channels/using/about-sms-messages.md"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Exploring transitions<br /> </td> 
   <td> 이제 워크플로우의 마지막 전환 시 데이터와 해당 구조를 탐색할 수 있습니다. This allows you to check that the processes applied by each activity correspond to your needs.<br /> </td> 
  </tr> 
  <tr> 
   <td> File pre- and post-processing in workflows<br /> </td> 
   <td> You can now carry out additional processing on a data file when importing or exporting it via the <span class="uicontrol">Load file</span> and <span class="uicontrol">Extract file</span> activities.<br /> 기본적으로 이러한 활동에서 GZIP 포맷 파일의 압축을 풀고 압축을 해제할 수 있습니다.<br /> 자세한 내용은 <a href="../../automating/using/load-file.md">파일 로드</a> 및 파일 <a href="../../automating/using/extract-file.md">추출</a> 활동에 대한 설명서를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Deliverability reports<br /> </td> 
   <td> 이제 이메일 렌더링 보고서를 사용할 수 있습니다. 이 보고서를 통해 지원 및 메시지 서비스를 읽는 데 사용된 메시지 서비스에 따라 여러 가지 메시지를 볼 수 있습니다.<br /> 보고서 요약에는 수신된 메시지, 스팸 메시지, 받지 못한 메시지 및 수신을 기다리는 메시지가 표시됩니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../sending/using/email-rendering.md#email-rendering-report-description"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Package Management<br /> </td> 
   <td> It is now possible to import and export images in packages.<br /> </td> 
  </tr> 
  <tr> 
   <td> Quick actions<br /> </td> 
   <td> 목록 또는 워크플로우에서 요소를 마우스로 가리키거나 선택한 후에 특정 작업이 나타납니다. 이러한 작업 중 일부는 이제 액세스를 용이하게 하기 위해 관련 요소 주변에서 아이콘으로 표시됩니다. These quick actions can be used to duplicate an element, delete it, show the detail, etc.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-9}

#### General {#general-9}

* 관리자 계정에서 인스턴스의 일반 매개 변수에 액세스할 수 없는 오류를 수정했습니다.
* **이제 부동** 데이터가 사용자 지정 리소스에서 제대로 고려됩니다.
* 해당 템플릿의 상태가 수정되었을 때 발생한 간소화된 가져오기 목록에서 표시 오류를 수정했습니다.

#### Landing pages {#landing-pages-4}

* 영어 인스턴스에서 프랑스어로 잘못 표시할 수 있는 랜딩 페이지 템플릿의 특정 요소를 수정했습니다.

#### Audiences {#audiences}

* Adobe Marketing Cloud에서 가져온 대상이 대상 목록에 표시되지 않도록 하는 오류를 해결했습니다.
* 쿼리를 정의할 때 대소문자 구분을 적용할 수 있는 오류를 수정했습니다.
* 쿼리를 정의할 때 대상이 필터링되지 않는 오류를 해결했습니다.
* 대상자에서 작업이 취소되지 않을 수 있는 오류를 수정했습니다.

#### Workflows {#workflows-7}

* Fixed an error that could prevent the fields that were to be updated in an **[!UICONTROL Update data]** activity from manually being configured.
* Fixed an error that could cause the **[!UICONTROL Query]** activity to load infinitely when opened if the workflow had not been saved after having placed the activity in the diagram.
* Fixed an error that could cause the server to stop while counting or previewing an audience selected from a **[!UICONTROL Query]** in a workflow.
* 워크플로우에서 활동이 열려 있을 때 나타날 수 있는 치명적이지 않은 오류가 수정되었습니다.
* Fixed an error that prevented a **[!UICONTROL Scheduler]** activity from being configured to execute a workflow several times a day.
* 쿼리를 수행할 수 없는 필드가 특정 워크플로우 활동에 나타나던 오류를 수정했습니다.
* Fixed an error that could prevent the user from locating the KPIs added from a **[!UICONTROL Query]** on deliveries in the outbound transition.
* 파일을 워크플로우로 가져온 후 파일 대상이 생성되지 않는 오류를 해결했습니다.
* Fixed an error that could prevent data from being updated on profiles if the **location/address3** field of the resource was used.
* 워크플로우에 이기종 활동 컬렉션이 중복되지 않던 오류를 수정했습니다.
* SQL 이 표시되지 않아 워크플로우에서 반복되는 배달을 위해 오류를 진단하는 오류를 해결했습니다.

#### Content editor {#content-editor-1}

* 랜딩 페이지 또는 이메일의 소스 코드에서 검색이 불가능한 오류를 수정했습니다.

#### Packages {#packages-1}

* 특정 유형의 요소를 패키지 (특히 랜딩 페이지, 워크플로우) 로 내보낼 수 없는 다양한 오류를 해결했습니다.
* 레이블이 수정된 경우 이전 패키지 가져오기 레이블이 표시되는 오류를 해결했습니다.
* 내보내기 가능한 리소스 목록에 호환되지 않는 리소스가 표시될 수 있는 오류를 해결했습니다.

## Release 15.10 - October 2015 {#release-15-10---october-2015-}

### New capabilities {#new-capabilities-10}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Workflows: Deduplication activity<br /> </td> 
   <td> 이제 데이터 중복 제거에 전용 활동을 워크플로우에서 사용할 수 있습니다. 이 활동을 사용하면 선택한 기준에 따라 타겟에서 중복을 필터링할 수 있습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../automating/using/deduplication.md"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: Improved diagram<br /> </td> 
   <td> 이제 워크플로우 작업 영역에서 여러 개의 키보드 단축키를 사용하여 활동을 선택하거나 열고 삭제할 수 있습니다.<br /> 또한 활동 정렬이 개선되었으며 워크플로우를 시각적으로 체계적으로 구성할 수 있습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../automating/using/workflow-interface.md#workspace"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: Extract file activity<br /> </td> 
   <td> The date and time of the export is now automatically added to the labels of the files exported using an <span class="uicontrol">Extract file</span> activity. This way the files generated are unique.<br /> </td> 
  </tr> 
  <tr> 
   <td> Simplified data import<br /> </td> 
   <td> The name of the template from which a simplified import was carried out is now visible by default in the import list and in the detail of each import.<br /> </td> 
  </tr> 
  <tr> 
   <td> Custom resources<br /> </td> 
   <td> Improvement and extended possibilities for managing and defining links for custom resources.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-10}

#### Email {#email}

* 미러 페이지에서 서비스 가입 해지 링크가 제대로 작동하지 않는 오류를 해결했습니다.
* 이메일 편집 페이지에 이메일 배달 레이블이 올바로 표시되지 않는 오류를 해결했습니다.
* Fixed an error that could prevent an external **[!UICONTROL Routing]** account from being selected in a duplicated delivery template.

#### Audiences {#audiences-1}

* 쿼리에 1-n 링크가 사용된 경우 대상 카운트 중에 발생하는 오류를 수정했습니다.
* 이메일 게재 대상 대상에서 프로필을 선택할 수 없는 오류를 해결했습니다.

#### Workflows {#workflows-8}

* 워크플로우에서 이메일 배달을 구성할 때 표시 문제를 일으킬 수 있는 오류를 수정했습니다.
* **[!UICONTROL Load file]** 활동이 올바르게 작동하지 않는 오류를 해결했습니다. 그러면 빈 오류 메시지가 표시됩니다.
* **[!UICONTROL Transfer file]** 활동이 올바르게 작동하지 않는 오류를 해결했습니다. 액세스 권한이 항상 제대로 고려되지는 않았습니다.
* Fixed an error that could prevent a file from being exported if the workflow contained a **[!UICONTROL Recurring email]** .
* 이메일 배달이 워크플로우에서 생성되지 않거나 주제 및 정의된 컨텐츠가 고려되지 않도록 하는 오류를 해결했습니다.
* Fixed an error that could prevent a reconciliation key from being selected in an **[!UICONTROL Update data]** activity when configuring the workflow of a simplified import template.
* 활동이 삭제된 후 워크플로우가 저장되지 않는 오류를 해결했습니다.

#### Platform {#platform}

* 사용자 지정 리소스에 해당 요소의 리소스 유형에 대한 링크가 포함되어 있는 경우 새 요소를 만들 수 없는 오류를 수정했습니다.
* 특정 로그가 작성되도록 15 분 지연을 발생시킬 수 있는 오류를 해결했습니다.
* **[!UICONTROL Date]** 또는 **[!UICONTROL Indicators]** 열을 기준으로 정렬할 때 마케팅 활동 목록이 표시되지 않는 오류를 해결했습니다.

#### Landing pages {#landing-pages-5}

* 랜딩 페이지를 미리 보기 위해 테스트 프로필을 선택할 때 발생하는 오류를 수정했습니다.

#### Transactional messages {#transactional-messages-5}

* 테스트 프로필에서 이벤트를 삭제한 후 애플리케이션이 충돌할 수 있는 오류를 수정했습니다.

#### Reports {#reports}

* Fixed an error that could cause incorrect data to be sent for the reports **[!UICONTROL deliveryThroughputReport]** and **[!UICONTROL deliveryTrackingReport]** .

#### Content editor {#content-editor-2}

* 동적 컨텐츠 블록을 처리할 때 발생하는 HTML 태그 관리 오류를 수정했습니다.

## Release 15.8 - August 2015 {#release-15-8---august-2015}

### New capabilities {#new-capabilities-11}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Simplified data import<br /> </td> 
   <td> 이제 간소화된 방식으로 데이터를 가져올 수 있습니다.<br /> 관리자는 관리자가 미리 정의한 템플릿을 선택하고 가져올 데이터가 포함된 파일을 업로드하기만 하면 됩니다. 템플릿에 정의된 워크플로우는 사용자에 대해 투명하게 실행되며, 사용자는 가져오기에 대한 세부 정보와 오류 로그에서 액세스할 수 있습니다.<br /> 이러한 파일의 데이터는 데이터베이스에 삽입하거나 대상을 직접 만드는 방법으로 사용할 수 있습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../automating/using/about-data-import-and-export.md"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Creating programs and campaigns<br /> </td> 
   <td> 이제 캠페인과 프로그램이 구성되므로 작성된 날짜가 시작 날짜로 자동으로 사용됩니다.<br /> 종료 날짜는 다음과 같이 시작 날짜에 따라 구성됩니다.<br /> 
    <ul> 
     <li> 프로그램의 경우 D +186 </li> 
     <li> 캠페인 D +61 </li> 
    </ul> For more information, refer to the <a href="../../start/using/programs-and-campaigns.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Email<br /> </td> 
   <td> The list of tracked URLs is now read only.<br /> </td> 
  </tr> 
  <tr> 
   <td> Transactional messages<br /> </td> 
   <td> 이제 만들어진 계정 다음에 암호 변경 또는 확인 메시지와 같은 이벤트에 대한 맞춤형 트랜잭션 메시지를 관리할 수 있습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../channels/using/about-transactional-messaging.md"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Custom resources<br /> </td> 
   <td> 다음과 같이 추가된 여러 가지 기능: 테스트 프로필 확장, 상태 관리 및 삭제 리소스.<br /> 자세한 내용은 자세한 설명서를 <a href="../../developing/using/resource-statuses.md"></a>참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-11}

#### Display {#display}

* Safari의 쿼리 편집기에서 두 개의 필드가 juxtapdoublosed 되는 오류를 해결했습니다.

#### Content editor {#content-editor-3}

* 이메일 제목에서 ' &lt;',' &amp;' 및 ' &gt;' 문자가 사용되지 않는 오류를 해결했습니다.

#### Email {#email-1}

* 사용자가 동적 텍스트 뒤에 텍스트를 추가하지 못했던 오류를 수정했습니다.

#### Lists {#lists}

* Fixed an error that prevented the **Message** column in workflow execution logs from being exported correctly.

#### Profiles and audiences {#profiles-and-audiences}

* 요소가 복제 또는 삭제된 시기를 이중 확인하는 오류를 해결했습니다. **Internet Explorer 11를 사용하는 하이브리드 장치**.

#### Workflows {#workflows-9}

* 워크플로우에서 이메일을 보내지 못하게 하는 오류를 해결했습니다.
* Fixed an error that could prevent a workflow from executing when the name of the rejection file was not specified in a **[!UICONTROL Load file]** activity.
* Fixed an error that could prevent a workflow from executing when the **[!UICONTROL Execution frequency]** of a **[!UICONTROL Schedule]** activity was set to **[!UICONTROL Daily]** .

#### Platform {#platform-1}

* 로드 균형 환경에서 축소판이 생성되지 않는 오류를 해결했습니다.

## Release 15.7 - July 2015 {#release-15-7---july-2015}

### New capabilities {#new-capabilities-12}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Exporting lists<br /> </td> 
   <td> 이제 목록의 컨텐츠를 CSV 형식의 파일로 내보낼 수 있습니다. This function is available in all screens with a <strong>List</strong> mode (for example: profile list).<br /> 내보낸 데이터는 내보낼 때 표시되는 열의 데이터입니다. 따라서 목록을 편집하여 내보낼 데이터를 선택할 수 있습니다.<br /> 이 기능 사용에 대한 자세한 내용은 <a href="../../automating/using/exporting-lists.md">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Integration with Adobe Profiles &amp; Audiences<br /> </td> 
   <td> You can now share audiences between Adobe Campaign and your other Adobe Marketing Cloud solutions:<br /> 
    <ul> 
     <li> Export: when you save an audience composed of profiles in a workflow, a new <span class="uicontrol">Share in Adobe Marketing Cloud</span> option allows you to add profiles to an existing audience or to create a new audience. </li> 
     <li> Import: by creating a <strong>List</strong> type audience from the audience management screen, a new option allows you to identify it as an <span class="uicontrol">Adobe Marketing Cloud Audience</span> . 그런 다음 기존 공유 대상을 선택하여 Adobe Campaign로 가져올 수 있습니다. </li> 
    </ul> For more information on configuring and using this functionality, refer to the <a href="../../integrating/using/about-campaign-audience-manager-or-people-core-service-integration.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Digital Content Editor - Dynamic content<br /> </td> 
   <td> 동적 컨텐츠 인터페이스가 향상되었습니다. 이제 이메일 본문에 직접 다른 동적 컨텐츠 간을 이동할 수 있는 화살표가 표시됩니다.<br /> 이 기능 사용에 대한 자세한 내용은 <a href="../../designing/using/defining-dynamic-content-in-a-landing-page.md">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Digital Content Editor - Dynamic text<br /> </td> 
   <td> From the content editor of an email, you can now define dynamic text:<br /> 
    <ul> 
     <li> 이메일 제목에서 </li> 
     <li> HTML 모드에서 </li> 
     <li> 텍스트 모드에서 </li> 
    </ul> For more information on using this functionality, refer to the <a href="../../designing/using/defining-dynamic-text.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Programs and campaigns - Reports<br /> </td> 
   <td> 보고서의 인터페이스 및 그래픽이 개선되었습니다.<br /> 이 기능 사용에 대한 자세한 내용은 <a href="../../reporting/using/defining-the-report-period.md">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-12}

#### Installation {#installation}

* 이제 Adobe Campaign 인스턴스 이름은 32 자로 제한됩니다.

#### Workflows {#workflows-10}

* 워크플로우에서 쿼리를 편집할 때'배달'리소스의 타깃팅을 방지할 수 있는 오류를 수정했습니다.
* 워크플로우에서 쿼리를 편집할 때 연결된 특정 리소스가 처리되지 못하게 하는 오류를 해결했습니다.
* Fixed an error that could prevent a **Recurring delivery** activity from being modified if the workflow had already been executed.

#### Emails {#emails}

* 표현식 편집기를 통해 동적 컨텐츠가 추가되면 이메일을 전송하기 전에 JavaScript 구문 오류를 확인하지 못하는 오류를 수정했습니다.

#### Landing pages {#landing-pages-6}

* 태블릿에서 랜딩 페이지를 편집할 수 없는 오류를 수정했습니다.

#### Assets Core Service {#assets-core-service}

* 편집할 이메일 또는 랜딩 페이지에서 공유 리소스를 선택할 때 사용 가능한 리소스 목록이 이제 Adobe Campaign에 대해 필터링됩니다.

## Release 15.6 - June 2015 {#release-15-6---june-2015}

### New capabilities {#new-capabilities-13}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Workflows: Reconciliation activity<br /> </td> 
   <td> A new <strong>Reconciliation</strong> activity links unidentified data (for example, after importing a file) with existing resources within a workflow.<br /> 이 활동은 본질적으로 데이터 관리 목적으로 사용됩니다. It responds to two different use cases:<br /> 
    <ul> 
     <li> <strong>관계 추가</strong>: <strong>관계</strong> 탭에서는 인바운드 데이터와 Adobe Campaign 데이터베이스의 다른 차원 사이에 링크를 추가할 수 있습니다. </li> 
     <li> <strong>데이터 식별</strong>: <strong>ID</strong> 탭을 사용하면 Adobe Campaign 데이터베이스에 있는 기존 차원의 열에 인바운드 데이터를 간단히 연결할 수 있습니다. 활동을 나가면 데이터가 지정된 차원에 속하는 것으로 식별됩니다. </li> 
    </ul> <a href="../../automating/using/reconciliation.md"></a>자세한 내용은 설명서를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: Extract file activity<br /> </td> 
   <td> A new <strong>Extract file</strong> activity allows you to export data from the Adobe Campaign database in the form of an external file from a workflow. <br /> 제한 사항: 현재 출력 파일에 동적 이름을 사용할 수 없습니다.<br /><a href="../../automating/using/extract-file.md"></a>자세한 내용은 설명서를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: Scheduler activity<br /> </td> 
   <td> Improved widget that allows you to select the execution time of the <strong>Scheduler</strong> activity in a workflow.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: Transfer file activity<br /> </td> 
   <td> SFTP is now supported.<br /> </td> 
  </tr> 
  <tr> 
   <td> Custom resources<br /> </td> 
   <td> <span class="uicontrol">이제 개발</span> 메뉴를 통해 관리자 권한이 있는 사용자가 구매 또는 제품 테이블과 같은 자체 사용자 지정 리소스를 만들어 제공된 데이터 템플릿을 강화할 수 있습니다. <br /> 또한 즉시 사용 가능한 리소스를 확장하여 새 필드를 추가할 수 있습니다.<br /> 또한, 새 사용자 정의 리소스 또는 확장된 사용자 지정 리소스에 해당하는 화면의 네비게이션을 구성할 수 있습니다.<br /><a href="../../developing/using/data-model-concepts.md"></a>자세한 내용은 설명서를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Test profiles<br /> </td> 
   <td> The <strong>Middle name</strong> and <strong>Title</strong> of the test profiles can now be selected when configuring the list of test profiles.<br /> </td> 
  </tr> 
  <tr> 
   <td> Content editor: Dynamic content<br /> </td> 
   <td> 표현식 편집기를 통해 정의된 조건에 따라 사용자에게 동적으로 표시되는 다양한 컨텐츠를 정의할 수 있습니다.<br /><a href="../../designing/using/defining-dynamic-content-in-a-landing-page.md"></a>자세한 내용은 설명서를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Email<br /> </td> 
   <td> A <strong>Test profiles</strong> column is now available in an email's sending logs.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-13}

#### Lists {#lists-1}

* 목록에서 요소를 삭제하면 목록이 자동으로 새로 고쳐집니다.
* 하나의 열만 포함하는 목록에서 요소를 선택할 수 없는 오류를 수정했습니다.
* 페이지를 새로 고침 후 목록 표시에 적용된 변경 사항이 손실되는 오류를 해결했습니다.
* 이제 테스트 프로필 목록에 테스트 프로필의 중간 이름과 제목을 표시할 수 있습니다.
* Mozilla Firefox와 함께 목록에서 확인란을 선택할 때 발생하는 오류를 수정했습니다.

#### Audiences {#audiences-2}

* Fixed an error that prevented the **[!UICONTROL Add]** button from being used in the audience interface.

#### Emails {#emails-1}

* 이메일을 편집할 때 미리 보기 단추가 한 행에서 두 번 사용될 수 없는 JavaScript 오류를 수정했습니다.
* Fixed an error that prevented the **[!UICONTROL Edit properties]** and **[!UICONTROL Show proofs]** buttons from being used on Microsoft Surface Pro3 tablets using Internet Explorer 11.
* 이메일의 전송 로그가 표시되지 않는 오류를 해결했습니다.

#### Landing pages {#landing-pages-7}

* Fixed an error that prevented the **Brand logo** content block from being used when editing content in a landing page.
* 랜딩 페이지에 대해 유효성 날짜가 지정된 경우 마케팅 활동 목록에 랜딩 페이지가 표시되지 않는 오류를 수정했습니다.

#### Workflows {#workflows-11}

* **세그멘테이션** 활동을 구성할 때 그룹 모드에서 세그먼트 제한을 제대로 수행하지 못하는 오류를 해결했습니다.
* **세그멘테이션** 활동을 구성한 후 전환이 선택되지 않는 오류를 해결했습니다.
* **세그멘테이션** 활동을 구성한 후 전환이 삭제되지 않던 오류를 수정했습니다.
* Fixed an error that prevented populations from being counted and previewed within a **Segmentation** activity.
* 반복되는 이메일이 실제로 삭제되지 않는 오류를 해결했습니다.
* Fixed an error that caused data from a deleted **Transfer file** activity to appear in a new **Transfer file** activity.
* Fixed an error that prevented an exclusion rule from being correctly taken into account within an **Exclusion** activity.
* 워크플로우에서 이메일 배달 활동을 삭제할 때 발생하는 오류를 수정했습니다. 해당 게재 내역이 이제 마케팅 활동 목록에서도 제거됩니다.

#### Navigation {#navigation}

* 이제 Tab 키를 사용하여 동일한 페이지의 필드 간을 올바르게 이동할 수 있습니다.

## Release 15.4 - April 2015 {#release-15-4---april-2015}

### New capabilities {#new-capabilities-14}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Package exports / Package imports<br /> </td> 
   <td> <strong>이제 배포</strong> 메뉴를 통해 관리 권한이 있는 사용자가 패키지를 내보내고 가져올 수 있어 다른 Adobe Campaign 인스턴스 간에 리소스를 교환할 수 있습니다.<br /><a href="../../automating/using/managing-packages.md"></a>자세한 내용은 설명서를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Reports<br /> </td> 
   <td> All reports (except the <strong>Hot clicks</strong> report) can now be accessed from a program. These reports are:<br /> 
    <ul> 
     <li> 프로그램 전달 처리량 </li> 
     <li> 프로그램 추적 표시기 </li> 
     <li> 도메인별 프로그램 분류 </li> 
     <li> 프로그램 비결과물 및 바운스 수 </li> 
     <li> 프로그램 URL 및 스트림 클릭 </li> 
    </ul> 이러한 보고서는 지정된 기간 (예: 3 개월, 6 개월 등) 동안 필터링할 수 있습니다. 캠페인 보고서를 필터링할 수도 있습니다.<br /><a href="../../reporting/using/about-dynamic-reports.md"></a>자세한 내용은 설명서를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: <strong>Email delivery</strong> activity<br /> </td> 
   <td> The <strong>Email delivery</strong> activity in the workflows has been improved. 이제 응용 프로그램 마케팅 활동 목록에서 반복되는 이메일 실행에 대한 이메일, 반복 이메일 및 자세한 정보를 찾을 수 있습니다.<br /><a href="../../automating/using/email-delivery.md"></a>자세한 내용은 설명서를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: <strong>Segmentation</strong> activity<br /> </td> 
   <td> <strong>이제 세그멘테이션</strong> 활동을 워크플로우에서 사용할 수 있습니다. 이 활동을 사용하면 하나 또는 여러 세그먼트를 만들고 동일한 워크플로우에서 업스트림 위에 위치한 활동에 의해 계산된 모집단 모집단 코드를 세그먼트화할 수 있습니다. 이 활동에서 세그먼트는 단일 전환 또는 여러 전환을 통해 처리할 수 있습니다. 이제 모집단을 필터링하고 각 세그먼트 크기를 제한하여 개인화를 최적화할 수 있는 옵션이 있습니다. 예를 들어 특정 기준에 해당하는 프로필을 임의로 선택할 수 있습니다.<br /><a href="../../automating/using/segmentation.md"></a>자세한 내용은 설명서를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Integrations: <strong>Assets Core Service</strong><br /> </td> 
   <td> You can now use shared resources via <strong>Assets Core Service</strong> in your email and landing page contents. Adobe Marketing Cloud에서 직접 공유 리소스를 관리할 수 있습니다.<br /><a href="../../integrating/using/working-with-campaign-and-assets-core-service.md"></a>자세한 내용은 설명서를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Integrations: <strong>Adobe Target</strong><br /> </td> 
   <td> You can now insert images that are dynamically computed by <strong>Adobe Target</strong> into your Adobe Campaign emails. 이를 통해 Adobe Target 세그먼트에 정의된 기준에 따라 컨텐츠를 개인화하여 동일한 이메일의 여러 버전을 제공할 수 있습니다.<br /><a href="../../integrating/using/about-campaign-target-integration.md"></a>자세한 내용은 설명서를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Digital Content Editor: <strong>Block selector</strong><br /> </td> 
   <td> HTML 컨텐츠 편집기에서 블록을 선택하면 편집 영역의 하단에 브레드크럼이 표시됩니다. 이렇게 하면 다른 요소로 쉽게 이동하여 선택할 수 있습니다.<br /><a href="../../designing/using/managing-landing-page-structure-and-style.md"></a>자세한 내용은 설명서를 참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

## Release 15.3 - March 2015 {#release-15-3---march-2015}

### New capabilities {#new-capabilities-15}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Reports<br /> </td> 
   <td> 이제 프로그램 또는 캠페인에서 바로 보고서에 액세스할 수 있습니다. <strong>배달 요약</strong> 보고서가 프로그램 수준에서 추가되었습니다.<br /><a href="../../reporting/using/delivery-summary.md"></a>자세한 내용은 설명서를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Update data<br /> </td> 
   <td> In the workflows, the available <strong>Update data</strong> activity has a new option, which allows you to automatically link inbound data fields with the fields of an application schema. 이렇게 하면 필드를 업데이트하는 선택 프로세스를 용이하게 할 수 있습니다.<br /><a href="../../automating/using/update-data.md"></a>자세한 내용은 설명서를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Email delivery<br /> </td> 
   <td> In workflows, the advanced options of the <strong>Email delivery</strong> activity can now be accessed via a specific button in the action bar. This button is only available if an <strong>Email delivery</strong> activity is selected. 주요 이점은 활동에 아웃바운드 전환을 추가하고 워크플로우에서 표시된 활동의 이름을 편집할 수 있다는 것입니다.<br /><a href="../../automating/using/email-delivery.md"></a>자세한 내용은 설명서를 참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-14}

#### General {#general-10}

* 배달을 만들 때 받는 사람이 표시되지 않는 오류를 수정했습니다.
* ' 연 사람'조건을 사용하는 대상을 사용하지 못하게 하는 오류가 수정되었습니다.
* 빈 프로필을 삭제할 수 없는 오류를 수정했습니다.
* 배달을 미리 볼 때 발생하는 오류를 수정했습니다.
* 마케팅 활동이 중복되지 않는 오류를 수정했습니다.
* 캠페인을 삭제할 때 발생하는 오류를 수정했습니다.

