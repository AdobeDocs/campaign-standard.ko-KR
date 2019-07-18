---
title: 릴리스 노트 2017
seo-title: 릴리스 노트 2017
description: 릴리스 노트 2017
seo-description: 이 페이지에는 Adobe Campaign Standard의 2017 릴리스가 모두 나열됩니다.
page-status-flag: 정품 인증 안 함
uuid: d 73 f 8186-e 309-441 b -969 d -71 d 0 a 1 c 33 cf 4
contentOwner: Sauviat
products: sg_ campaign/standard
audience: RN
content-type: 참조
topic-tags: campaign-standard-release
discoiquuid: 1 CFD 9 B 3 B -9 B 3 E -4587-9 C 46-B 6 FB 02131654
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Release Notes 2017{#release-notes}

Adobe Campaign Standard 2017 릴리스를 찾고 있습니까?

각 릴리스에는 새로운 기능과 패치가 포함되어 있습니다. 컨텐츠를 보려면 릴리스를 클릭합니다.

View the latest [documentation updates](../../rn/using/documentation-updates.md) for Adobe Campaign Standard. If you're looking for a newer release, consult this [page](../../rn/using/release-notes.md).

## Release 17.10 - October 2017 {#release-17-10---october-2017}

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
   <td> Fatigue Management<br /> </td> 
   <td> 피로 관리를 사용하면 피로 규칙을 만들어 프로필과의 커뮤니케이션을 관리할 수 있습니다. 피로 규칙은 쉽게 구축되지만 여러 채널 (트랜잭션 메시지 포함) 에서의 메시지 계산, 특정 전달 횟수 계산, 특정 프로파일에 규칙 적용 등의 기능과 같은 기능이 매우 유연합니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../administration/using/fatigue-rules.md"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Content creation: Import from a URL<br /> </td> 
   <td> URL에서 가져오기 기능을 사용하면 웹 사이트에서 크리에이티브 콘텐츠를 신속하게 검색하여 모든 전달을 위한 이메일을 작성할 수 있습니다. 또한 제 3 자가 URL를 통해 직접 컨텐츠를 공유할 수 있도록 함으로써 크리에이티브 프로세스를 간소화할 수 있습니다. 가져온 컨텐츠는 단일 전달 또는 템플릿 수준에서 유연하게 사용할 수 있으며, 워크플로우 기반이나 트랜잭션 메시지 등 모든 관련 캠페인의 브랜드 일관성을 보장할 수 있고 A/B 테스트 또는 다변량 테스트를 포함시킬 수 있습니다. URL에서 가져오기 기능은 동적 보고를 통해 이메일 성능을 모니터링하기 위해 자동으로 모든 링크를 변환하고 추적합니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../designing/using/importing-content-from-a-url.md"></a>참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches}

#### Platform {#platform}

* 큰 zip 파일의 압축을 해제할 수 있는 문제를 해결했습니다.
* 브랜드 관리의 보안이 향상되었습니다. 이제 Adobe 기술 관리자를 위해 브랜드 이름 및 발신자 주소를 수정할 수 있습니다.
* 사용자 생성 컨텐츠 (이미지, 미러 페이지, 랜딩 페이지 등) 를 adobe.com 도메인에서 더 이상 서비스를 제공할 수 없습니다. 이제 브랜드 사용을 통해 자신의 도메인을 사용하여 이러한 리소스를 처리해야 합니다.
* 마케팅 활동을 표시하고 필터링할 때 인터페이스 문제가 해결되었습니다.
* 구독 날짜 필드가 REST REST API 호출로 업데이트되지 않는 문제를 해결했습니다.

#### Emails, SMS messages and direct mail {#emails--sms-messages-and-direct-mail}

* 메시지 유형 대상자 타깃팅이 실패하여 준비가 실패하는 문제를 해결했습니다.
* 다국어 이메일 전달 기능에 추가된 언어가 없습니다.
* 이제 사용자가 컨텐츠 및 저장 내용을 수정하면 게재 대시보드에 표시되는 컨텐츠 썸네일이 자동으로 업데이트됩니다.
* 배달을 열 수 없는 시간대 관련 문제를 해결했습니다.

#### Push notifications {#push-notifications}

* When configuring the push notification channel, the push provider platform for iOS should be **apns** and for Android **gcm**.
* iOS 모바일 앱이 Adobe Campaign 인터페이스에 추가되지 않던 오류가 수정되었습니다.
* 이제 GCM 및 FCM 이 활성화된 Android 모바일 애플리케이션에서 푸시 알림이 지원됩니다.
* 푸시 알림 템플릿을 복제할 때 컨텐츠를 저장할 수 없는 오류를 수정했습니다.
* 이제 Mobile Application 사용자의 데이터를 조정하여 Adobe Campaign 데이터베이스에서 프로필을 만들거나 업데이트할 수 있습니다.
* 이제 Adobe Campaign에서 표준 푸시 알림으로 트랜잭션 푸시 알림을 처리하도록 우선 순위를 매깁니다.

#### Reports {#reports}

* 이메일 컨텐츠에 핫 클릭 비율이 표시되지 않는 문제를 해결했습니다.
* 바운스 대신 하드 바운스로 카운트되었던 블랙리스트 지표의 문제를 수정했습니다.
* 요약 데이터에 음수 카운트가 표시되는 문제를 해결했습니다.
* 잘못된 연령 세그먼트에서 프로필을 카운트했던 문제를 수정했습니다.
* 소프트 및 하드 바운스 계산 공식이 변경되었습니다.

#### Workflows {#workflows}

* Fixed an issue in the **[!UICONTROL Load file]** activity that could lead to errors after manually adding and removing columns in the activity.
* **[!UICONTROL deliverabilityUpdate]** 이제 기술 워크플로우는 오전 2 시 (서버 시간) 에 실행됩니다.
* 내보내기 역할 없이 목록 내보내기를 수행할 수 있는 보안 문제를 해결했습니다.
* **[!UICONTROL Reconciliation]** 활동 문제가 수정되었습니다.
* Fixed an issue with the use of wildcard characters in the **[!UICONTROL File Transfer]** activity.

#### Profiles and audiences {#profiles-and-audiences}

* 일부 특정 경우에 쿼리 조건이 제대로 고려되지 않아 잘못된 결과가 발생하는 문제를 해결했습니다.
* 준비되었지만 전송 및 만료되지 않은 메시지의 타깃팅된 경우 프로필에 액세스할 수 없는 문제를 해결했습니다.

#### Integrations {#integrations}

* 트리거에 대해 만들어진 일부 데이터 소스가 올바르게 표시되고 선택되는 문제를 해결했습니다.

#### Custom resources {#custom-resources}

* 사용자 지정 리소스 행이 데이터 없이 표시될 수 있는 목록 화면에서 발생하던 문제가 수정되었습니다.
* ' false'값이 있는 부울 유형 필드가 사용자 지정 리소스에 표시되지 않는 문제를 해결했습니다.

## Release 17.9 - September 2017 {#release-17-9---september-2017}

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
   <td> Library of Email templates<br /> </td> 
   <td> 멋진 두 가지 테마인 Astro와 Feather로 디자인된 18 개의 새로운 반응형 템플릿을 소개합니다. 이러한 사용자 정의 가능한 템플릿은 업종을 불문하고 바로 사용할 수 있습니다. 템플릿에는 다양한 활용 사례에 대한 컨텐츠가 포함되어 있으므로 보다 빠르고 효율적으로 그리고 보다 아름답게 이메일 마케팅 캠페인을 디자인하고 전달할 수 있습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../start/using/about-templates.md#content-templates"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Dynamic Reporting with Profile Data<br /> </td> 
   <td> 동적 보고는 완전히 사용자 지정 가능한 실시간 비즈니스 보고서를 제공합니다. 이번 릴리스에서는 동적 보고에 대한 강력한 개선 사항이 프로필 데이터에 대한 액세스를 추가하여 열기 및 클릭과 같은 기능적인 이메일 캠페인 데이터뿐만 아니라 성별, 도시, 우편번호 및 연령과 같은 프로필 차원별 인구 통계학적 분석을 가능하게 합니다. 드래그 앤 드롭 방식의 동일한 인터페이스를 통해 가장 중요한 고객 세그먼트에 대한 이메일 캠페인의 성과를 보다 손쉽게 파악할 수 있습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../reporting/using/about-dynamic-reports.md"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Mass Subscription with Origin &amp; Date<br /> </td> 
   <td> 이러한 대량 구독 개선 사항을 통해 이제 워크플로우에서 구독 서비스 활동을 통해 구독 정보 (원본 및 날짜) 를 Adobe Campaign Standard 데이터베이스에 직접 저장할 수 있습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../automating/using/subscription-services.md"></a>참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-1}

#### Platform {#platform-1}

* 일부 고객은 고유한 기록을 식별하기 위한 고유한 키를 관리하지 않으므로 Adobe Campaign Standard에서 오는 ID를 활용할 수 있어야 합니다. This ID (**ACS ID**) can be exported as well as used as a reconciliation key while updating the data. For more information, refer to the [detailed documentation](../../developing/using/configuring-the-resource-s-data-structure.md#generating-a-unique-id-for-profiles-and-custom-resources).
* FTP 프로토콜은 더 이상 사용되지 않습니다. 이제 Sftp를 사용해야 합니다. 기존 구현을 차단하지 않도록 FTP의 기존 구성은 이전과 동일하게 작동하지만 새 활동에 대해서는 옵션이 표시되지 않습니다.

#### Emails, SMS messages and direct mail {#emails--sms-messages-and-direct-mail-1}

* 이제 새 경고 기준을 만들어 배달 경고 알림에서 사용할 수 있습니다. For more information, refer to the [detailed documentation](../../sending/using/receiving-alerts-when-failures-happen.md#creating-a-delivery-alerting-criterion).
* 배달 알림 알림에 새 디자인이 있고 배달 알림 대시보드 사용자 경험이 향상되었습니다.
* Now when a routing external account is disabled, a warning is displayed in the impacted deliveries (email, SMS and push) and the **Preview** button is hidden in these deliveries.
* 제목 줄에 동적 텍스트가 활성화된 경우 이메일 컨텐츠의 A/B 테스트 미리 보기에서 오류가 발생하는 문제를 해결했습니다.

#### Transactional messages {#transactional-messages}

* 이제 트랜잭션 메시지를 전송한 후 3 일 예를 들어 후속 메시지를 보낼 시기를 정의할 수 있습니다. For more information, refer to the [detailed documentation](../../channels/using/follow-up-messages.md#sending-a-follow-up-message).
* 이제 이벤트에 연결된 트랜잭션 메시지를 보낼 때부터 날짜를 정의할 수 있습니다.
* 수신 및 처리된 이벤트에 연결된 프로필을 삭제한 후 후속 메시지가 들어 있는 워크플로우를 실행할 때 SQL 오류가 발생하던 문제를 수정했습니다.
* 이벤트에 연결된 프로필을 삭제할 수 없는 오류를 수정했습니다.
* 추적된 링크의 리디렉션이 작동하지 않는 문제를 해결했습니다.
* 이메일 또는 SMS 메시지의 특정 링크에 대한 추적을 비활성화하지 못했던 문제를 수정했습니다.

#### Reports {#reports-1}

* **핫 클릭** 보고서가 개선되었습니다. 또한, 게재에 정의된 각 조건부 컨텐츠에 따른 핫클릭을 표시하고 반복되는 배달 또는 트랜잭션 메시지의 각 실행에 대한 핫클릭을 표시할 수 있습니다. For more information, refer to the [detailed documentation](../../sending/using/receiving-alerts-when-failures-happen.md#creating-a-delivery-alerting-criterion).
* 격리 지표가 올바른 데이터를 검색하지 못하는 문제를 해결했습니다.
* 새 사전 설정 기간이 달력 위젯에 추가되었습니다.
* [동적 보고서 지표](../../reporting/using/indicator-calculation.md) 및 [캠페인 KPI](../../sending/using/confirming-the-send.md) (전송된 메시지의 대시보드에 표시됨) 가 더 많은 일관성을 위해 정렬되었습니다.
* Debian 7에서 파이프라인이 충돌할 수 있는 문제를 해결했습니다.

#### Workflows {#workflows-1}

* 가져온 파일 보유가 작동하지 않는 문제를 해결했습니다.

#### Integrations {#integrations-1}

* 이제 분석 및 캠페인 통합에 대해 Evar 및 이벤트가 지원됩니다.
* 중단된 장바구니의 컨텐츠가 포함된 이메일을 전송할 때, 장바구니에서 제거된 요소에 대한 페이로드 매개 변수는 이제 선택 사항입니다.

#### Profiles and audiences {#profiles-and-audiences-1}

* 이제 Adobe Campaign에서 활성 프로필 수를 표시하는 보고서를 제공합니다. 이 보고서는 정보용으로만 제공되므로 청구에 직접적인 영향을 주지 않습니다. For more information, refer to the [detailed documentation](../../audiences/using/active-profiles.md).
* 프로필 및 서비스 API를 사용할 때 프로필이 서비스에 구독되지 않는 문제를 해결했습니다.

## Release 17.7 - July 2017 {#release-17-7---july-2017}

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
   <td> Multilingual email and SMS deliveries<br /> </td> 
   <td> 자동 세그먼트화된 고객의 기본 언어를 기반으로 한 단일 배달을 통해 다국어 이메일 및 SMS 전달 방식을 정의하고 실행할 수 있습니다. 언어 및 개별 수준까지 다운로드에 대한 성과를 보고합니다.<br /> 점점 더 많은 기업이 국내외에서 컨텐츠를 다국어로 전달하는 문제에 직면하고 있습니다. 따라서 현지화된 메시지 배달을 간소화하는 것은 다국적 기업을 위한 효과적인 고객 커뮤니케이션 전략의 핵심 부분입니다. 여러 언어로 된 국가의 회사 고객이 거주하는 위치에 상관없이 서면상에서 컨텐츠를 개인화하고자 하는 기업입니다. For more information, refer to the <a href="../../channels/using/creating-a-multilingual-email.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Adobe Campaign Notifications<br /> </td> 
   <td> Adobe Campaign Standard에서 바로 중요한 시스템 활동에 대한 알림을 받을 수 있습니다. 예를 들어 진행 중인 전송 진행 상황이나 워크플로우가 오류일 때 알림을 받게 됩니다.<br /> 실시간 알림은 관련 이해 관계자가 정보를 알리고 애플리케이션 내에서 활동 알림을 즉시 실행할 수 있는 기능을 사용자에게 제공합니다. 이러한 결과를 통해 민첩성, 효율성 및 캠페인을 보다 원활하게 실행할 수 있습니다. For more information, refer to the <a href="../../administration/using/sending-internal-notifications.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Delivery Alerting<br /> </td> 
   <td> Adobe Campaign Standard에서 바로 알림을 볼 수 있을 뿐만 아니라 Adobe Campaign는 사용자 또는 외부 이해 관계자에게 중요한 시스템 활동에 대한 이메일 경고를 트리거하는 이메일 경고 시스템도 제공합니다. 맞춤형 알림 및 대시보드를 제작, 관리 및 수신하여 전달 성공이나 실패를 추적할 수 있습니다.<br /> Adobe Campaign 전달 알림은 이메일 및 대시보드를 통해 회사의 모든 Adobe Campaign 사용자에게 전달 상태에 대한 정보를 자동으로 알려 효율성을 높입니다. For more information, refer to the <a href="../../sending/using/receiving-alerts-when-failures-happen.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Encrypted Declared ID in Datasources<br /> </td> 
   <td> 암호화된 연락처 정보 (이메일 주소 또는 전화 번호) 를 선언된 ID로 사용하여 캠페인의 기존 프로필이 없어도 이메일 및 SMS 트리거를 보낼 수 있습니다. 암호화된 선언된 ID는 Adobe Campaign Standard를 통해 디코딩할 수 있으므로, 이제 이전에 알려지지 않은 연락처를 포함한 다른 Experience Cloud 솔루션에서 고객을 수신할 때 캠페인을 통해 새로운 시장 프로파일을 만들 수 있습니다.<br /> 이메일 및 SMS를 통해 고객 및 알려지지 않은 잠재 고객을 실시간으로 타겟팅하여 기존 고객층의 충성도를 향상시키고 신규 고객을 확보할 수 있습니다. 잠재 고객이 Adobe Campaign에서 이러한 통찰력을 인증하고 활용할 수 있게 되면 Adobe Audience Manager *에서 퍼스트 파티 쿠키 데이터를 최대한 활용할 수 있습니다. <br /> * Adobe Audience Manager는 필수입니다. For more information, refer to the <a href="../../integrating/using/about-campaign-audience-manager-or-people-core-service-integration.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> KPI sharing from Campaign to Analytics<br /> </td> 
   <td> Adobe Analytics와 캠페인 데이터를 공유하여 전환을 통한 다른 마케팅 및 광고 활동과 함께 캠페인에서 이메일 마케팅 지표를 측정하여 사전 및 사후 클릭 행동을 통합할 수 있습니다.<br /> 분석을 통해 전반적인 성과를 직접 추적하고 외부 프로그램을 통해 시너지 효과를 발견할 수 있습니다. 이러한 통합 보기에서 얻은 학습을 캠페인에 다시 적용할 수 있습니다. 결과적으로 개방, 클릭스루 및 전환율을 향상시킴으로써 매출 및 전반적인 캠페인 성과를 향상시킬 수 있습니다. <br /> Adobe Analytics가 필요합니다. For more information, refer to the <a href="../../integrating/using/about-campaign-analytics-integration.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Direct Mail Channel - Return To Sender<br /> </td> 
   <td> 이제 발신자 정보로 돌아가기 기능이 포함된 일반 메일 공급자와의 일반 파일 교환이 지원됩니다. 이러한 DM (Direct Mail) 채널의 향상된 기능을 통해 향후 커뮤니케이션에서 해당 우편 주소를 제외할 수 있습니다.<br /> 이를 통해 마케터는 다른 채널을 통해 고객에게 잘못된 주소를 알리고 고객과의 관계를 강화하거나 우편 주소를 업데이트할 수 있습니다. 또한 마케터가 잘못된 주소로 메일을 전송하지 못하는 경우 마케팅 비용 낭비를 줄일 수 있습니다. <br /> 다이렉트 메일은 Add-on 채널로 사용할 수 있습니다. For more information, refer to the <a href="../../channels/using/return-to-sender.md">detailed documentation</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-2}

#### General {#general}

* 사용자가 목록을 내보낼 수 있는 문제를 해결했습니다. Now only users with the **[!UICONTROL Export]** role are allowed to.

#### Emails, SMS messages and direct mail {#emails--sms-messages-and-direct-mail-2}

* Fixed an issue with the **updateDeliveryExecInfo** workflow that set the **To deliver** indicator to 0 for SMS deliveries.
* In the **Advanced parameters** of the delivery template’s properties, the **Routing** drop-down list now only displays external accounts corresponding to the template message type. 예를 들어 이메일 배달 템플릿은 이메일 외부 계정만 표시합니다.
* Fixed an issue with the **[!UICONTROL Text]** preferred email format defined for test profiles.
* 게재의 [정의 정의] 화면에서 기본 시간대를 선택할 때 Javascript 오류가 발생하던 문제를 수정했습니다.
* 트랩이 전송 로그에 표시되지 않던 문제를 수정했습니다.
* 이제 배달 만들기 마법사의 템플릿 선택 화면에서 추가 및 A/B 테스트 템플릿이 기본적으로 숨겨져 있습니다. For more information, refer to the [detailed documention](../../channels/using/creating-an-email.md).
* 모든 사용자가 배달을 전송할 수 있는 문제를 해결했습니다. Now only users with the **[!UICONTROL Start deliveries]** role are allowed to. For more information, refer to the [detailed documention](../../sending/using/confirming-the-send.md).

#### Push notifications {#push-notifications-1}

* Fixed an issue with the **Campaign Tracking Endpoint** URL that prevented reporting.
* 푸시 알림 제목이 Android 장치에 표시되지 않는 문제를 해결했습니다.
* 푸시 알림이 제목만 포함된 경우 (그리고 메시지 본문에 아무 것도 표시되지 않음) iOS 장치에 푸시 알림이 표시되지 않는 문제를 해결했습니다.
* 게시에 있는 미디어 첨부 URL 이 추적에 있어 비디오 및 사진이 게시에 포함되지 않던 문제를 수정했습니다. 이제 푸시 알림에 대해 Mediaattachmenturl 유형의 URL 추적이 기본적으로 비활성화됩니다.

#### Reports {#reports-2}

* 차트와 표 간에 값이 다르게 표시되는 문제를 수정했습니다.
* 푸시 알림 값을 이메일 값으로 표시하는 문제를 수정했습니다.
* 캠페인 외부에서 배달을 만들 때 값을 알 수 없음으로 표시하는 문제를 해결했습니다.
* SMS 보고서 데이터를 모바일 애플리케이션 데이터로 표시하는 문제를 수정했습니다.

#### Workflows {#workflows-2}

* 이제 워크플로우 로그 (기간 및 텍스트 검색) 를 필터링할 수 있습니다. For more information, refer to the [detailed documention](../../automating/using/executing-a-workflow.md#monitoring).
* 이제 워크플로우 배달에서 옵션을 사용하여 보내기 전에 확인 기능을 비활성화할 수 있습니다.
* 반복 배달의 만들기 마법사에서 아웃바운드 전환을 설정하지 못했던 문제를 수정했습니다.
* 값이 많은 열거형이 있는 사용자 지정 리소스 필드를 기반으로 워크플로우 쿼리 활동을 사용할 때 발생하는 문제가 해결되었습니다.

## Release 17.5 - May 2017 {#release-17-5---may-2017}

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
   <td> Direct mail<br /> </td> 
   <td> Adobe Campaign Standard의 첫 번째 오프라인 채널인 DM를 통해 디지털 장벽을 없애고 물리적인 환경에 연결할 수 있습니다. 크로스채널 캠페인의 일환으로 DM (Direct Mail) 제공업체가 요구하는 파일을 개인화하고 생성할 수 있습니다. DM (Direct Mail) 를 활용하여 고객을 다시 참여시키거나 앱, 웹 사이트 또는 스토어로 고객을 유도하는 매력적인 접점을 통해 고객 경험을 향상시킬 수 있습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../channels/using/about-direct-mail.md"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Email BCC<br /> </td> 
   <td> 이메일 BCC를 사용하면 개별 수신자에게 전송된 고유한 이메일 메시지를 저장하여 해당 메시지를 보관할 수 있습니다. 모든 이메일에 BCC 이메일 주소를 추가하면 Adobe Campaign Standard 고객은 이 기능을 사용하여 각 이메일의 정확한 사본을 유지할 수 있습니다. 이는 금융 서비스 업계의 일반적인 법적 요구 사항으로서, 고객 서비스 센터에서 실시간으로 충돌을 해결하는 데 도움이 됩니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../administration/using/configuring-email-channel.md#archiving-emails"></a>참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-3}

#### Interface updates {#interface-updates}

* In the top bar, the **[!UICONTROL Timeline]** link has been removed and replaced with a link to **[!UICONTROL Programs & Campaigns]** .

#### Emails and SMS messages {#emails-and-sms-messages}

* Fixed an issue which displayed the wrong color for the **[!UICONTROL Retry in progress]** delivery status. 색상이 파란색이 아닌 회색입니다.

#### Workflows {#workflows-3}

* Fixed an issue that occurred when changing the action to perform in a **[!UICONTROL Transfer file]** activity.

#### Reports {#reports-3}

* **[!UICONTROL Spam]** 및 **[!UICONTROL Spam rate]** 표시기 계산이 변경되었습니다.
* **[!UICONTROL Bounce]** 지표가 더 정확한 결과를 위해 개선되었습니다.

#### Push notifications {#push-notifications-2}

* 프로필의 마케팅 내역에서 푸시 이벤트를 클릭할 수 없는 문제를 해결했습니다.
* 워크플로우에서 푸시 알림의 사용이 향상되었습니다.

## Release 17.4 - April 2017 {#release-17-4---april-2017}

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
   <td> Enhanced Image edition capabilities with the Creative SDK<br /> </td> 
   <td> 이제 Creative SDK에서 제공하는 전체 기능을 이용하여 이메일 또는 랜딩 페이지를 편집할 때 컨텐츠 편집기에서 직접 이미지를 향상시킬 수 있습니다.<br /> 이 기능은 추가 Creative Cloud 솔루션을 획득할 필요가 없습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../designing/using/modifying-images-with-the-adobe-creative-sdk.md"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Transactional push notifications<br /> </td> 
   <td> 모바일 애플리케이션 채널이 Adobe Campaign의 트랜잭션 메시징 기능에 추가되었습니다. 이제 트랜잭션 메시지에 대해 세 개의 채널이 지원됩니다. 이메일, SMS 및 푸시 알림.<br /> 자세한 내용은 자세한 설명서를 <a href="../../channels/using/transactional-push-notifications.md"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Recurring push notifications<br /> </td> 
   <td> 이제 워크플로우에서 반복되는 푸시 알림을 구성할 수 있습니다. 고객이 주간 미리 알림과 같은 정기적인 업데이트를 기대하는 경우 반복되는 푸시 알림을 사용하여 새로운 콘텐츠 또는 판촉 행사를 확인할 수 있습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../automating/using/push-notification-delivery.md"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Amazon Simple Storage Service (S3) connector<br /> </td> 
   <td> 이제 Amazon Simple Storage Service (S 3) 커넥터를 사용하여 데이터를 가져오거나 Adobe Campaign로 내보낼 수 있습니다. 워크플로우 활동에서 설정할 수 있습니다. 구성은 외부 계정에서 수행됩니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../administration/using/external-accounts.md"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Dreamweaver integration live<br /> </td> 
   <td> Adobe Campaign와 Dreamweaver 간의 통합이 이제 라이브되었습니다. 이제 Dreamweaver 공식 릴리스 버전 (17.0.2) 에서 작동합니다.<br /> 여기에서 Adobe Campaign Integration Extension를 설치해야 합니다. <a href="http://adobe.ly/acdw_addon">http://adobe.ly/acdw_addon</a><br /> 자세한 내용은 <a href="https://helpx.adobe.com/campaign/kt/acs/using/acs-dreamweaver-integration-feature-video-use.html">이 비디오를 참조하십시오</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-4}

#### Platform {#platform-2}

* 메모리 소비 문제가 해결되었습니다.

#### Emails and SMS messages {#emails-and-sms-messages-1}

* 메시지를 미리 볼 때 콘텐트가 최신 변경 사항과 제대로 동기화되지 않았던 문제를 수정했습니다.
* MX 또는 도메인 이메일 처리 규칙을 만들거나 삭제하지 못하는 문제를 해결했습니다.
* 여러 별칭이 포함된 이메일을 보내지 못하게 하는 문제를 해결했습니다.
* 배달 로그에서 트랩 배달 로그가 표시되지 않던 문제를 수정했습니다.
* 컨텐츠에 URL 이 없는 배달의 추적된 URL를 표시할 때 오류가 발생하던 문제를 수정했습니다.
* 이미지의 크기 속성이 보낸 메시지에서 올바로 적용되지 않는 문제를 해결했습니다.

#### Transactional messages {#transactional-messages-1}

* Rteventhistoid 필드는 더 이상 트랜잭션 메시지 템플릿의 개인화 필드로 노출되지 않습니다.

#### Landing pages {#landing-pages}

* We have optimized the **[!UICONTROL by email]** filter used in landing pages to reconcile new subscribers with database profiles.
* 양식 구성에서 부울 필드를 사용할 때 확인란 대신 무료 텍스트 입력이 표시되는 문제를 해결했습니다.
* 랜딩 페이지 축소판이 생성되지 않는 문제를 해결했습니다.

#### Workflows {#workflows-4}

* **[!UICONTROL End]** OR **[!UICONTROL External Signal]** 활동을 편집할 때 표시 오류를 수정했습니다 (Safari 에만 해당).
* Improved the error message displayed when editing a **[!UICONTROL Read Audience]** activity containing an erroneous audience.
* 구독 활동을 실행할 때 SQL 오류가 발생할 수 있는 문제를 해결했습니다.

#### Integrations {#integrations-2}

* 관심 영역 데이터: 위치 가입자를 카운트할 때 발생하는 오류를 수정했습니다.

#### Audiences and queries {#audiences-and-queries}

* 쿼리 편집기의 컬렉션에서 합계 및 평균 집계가 사용되지 않던 문제를 수정했습니다.
* 필터 리소스를 변경한 후 쿼리 편집기가 다시 로드되지 않는 문제를 해결했습니다.

#### Reports {#reports-4}

* 테이블에서 여러 행을 선택할 때 Open Rate 지표가 올바르게 계산되지 않는 문제를 해결했습니다.
* 지표만 정수 값으로만 표시하던 오류를 수정했습니다. 이제 지표를 소수점으로 표시할 수 있습니다.

#### Push notifications {#push-notifications-3}

* MCPNS에서 만들지 못한 모바일 앱에 연결된 Android 애플리케이션을 만들 때 오류 메시지가 표시되지 않는 문제가 해결되었습니다.
* 사용자가 자동 알림에 사운드를 추가할 수 있었던 문제를 수정했습니다.

## Release 17.2 - March 2017 {#release-17-2---march-2017}

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
   <td> Dynamic reporting<br /> </td> 
   <td> 동적 보고는 완전히 사용자 지정 가능한 실시간 비즈니스 보고서를 제공합니다. 시각적 동적 피벗 테이블 및 그래픽을 기반으로 하는 이 기능을 사용하면 변수 및 차원을 드래그 앤 드롭하여 마케팅 캠페인의 효율성과 효율성을 분석할 수 있습니다. 또한 동적 보고를 통해 고유한 비즈니스 보고서를 처음부터 만들고 저장하여 나중에 사용할 수 있습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../reporting/using/about-dynamic-reports.md"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Dreamweaver integration (Labs)<br /> </td> 
   <td> Adobe Campaign와 Dreamweaver 통합을 통해 이제 Adobe 솔루션을 사용하여 이메일 캠페인을 만드는 통합 프로세스를 사용할 수 있습니다.<br /> Dreamweaver에서 Adobe Campaign 이메일을 편집하고 두 솔루션 간에 원활하게 컨텐츠를 동기화할 수 있습니다.<br /> 초기 릴리스의 경우 통합을 "Labs" 기능으로 사용할 수 있으며 Dreamweaver 시험판 베타 버전에서만 작동합니다. 정품 인증을 받으려면 AC-DW-integration@adobe.com로 문의하십시오.<br /> 자세한 내용은 이 <a href="https://helpx.adobe.com/campaign/kt/acs/using/acs-dreamweaver-integration-feature-video-use.html">비디오를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Manual send time optimization<br /> </td> 
   <td> 이제 배달 수준에서 또는 워크플로우를 사용하여 수신자당 사용자 지정 전송 시간을 수동으로 정의할 수 있습니다. <br /> 두 가지 새 옵션을 사용할 수 있습니다. <br /> 
    <ul> 
     <li> 모든 수신자는 시간대가 고려된 메시지를 받습니다. </li> 
     <li> 각 수신자는 공식에 의해 정의된 계산된 날짜와 시간에 메시지를 받습니다. </li> 
    </ul> For more information, refer to the <a href="../../sending/using/optimizing-the-sending-time.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Push notifications New capabilities<br /> </td> 
   <td> The push notification channel has been enhanced with several new capabilities:<br /> 
    <ul> 
     <li> 새로운 저작 인터페이스 </li> 
     <li> 자동 알림 </li> 
     <li> 인터랙티브한 푸시 </li> 
     <li> 리치 컨텐츠 지원 </li> 
     <li> 페이로드 크기 계산기 </li> 
    </ul> For more information, refer to the <a href="../../channels/using/about-push-notifications.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: new Signal activity<br /> </td> 
   <td> Trigger a workflow from another workflow using the new <span class="uicontrol">Signal</span> activity.<br /> 이제 다른 워크플로우에서 하나의 워크플로우를 시작할 수 있으므로 보다 복잡한 고객 여정을 지원할 수 있습니다. 문제가 발생하면 고객 여정을 모니터링하고 반응할 수 있습니다.<br /> 몇 가지 워크플로우 활동이 업데이트되었습니다.<br /> 
    <ul> 
     <li> <span class="uicontrol">종료</span> 활동: 새 탭을 사용하면 이 활동이 실행된 후에 트리거할 워크플로우를 지정할 수 있습니다. </li> 
     <li> <span class="uicontrol">데이터</span> 활동 업데이트: 새로운 빈 아웃바운드 전환을 사용하여 다른 워크플로우를 트리거하는 <strong>종료</strong> 활동을 추가합니다. 빈 아웃바운드 변환은 데이터를 전달하지 않고 시스템에서 불필요한 공간을 소모하지 않습니다. </li> 
    </ul> For more information, refer to the <a href="../../automating/using/external-signal.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: new Read audience activity<br /> </td> 
   <td> 하나의 활동에서 손쉽게 선택하고 세분화할 수 있는 기존 대상자와 타겟팅 프로세스를 시작할 수 있습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../automating/using/read-audience.md"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Points of Interest data<br /> </td> 
   <td> 관심 영역 데이터는 Adobe Campaign를 모바일용 Adobe Analytics와 통합합니다. A brand can collect data from users' mobile locations - called <strong>Points of Interest</strong> - when users open the brand's app. 이를 통해 브랜드 기업은 사용자의 위치를 기반으로 개인화된 메시지를 전송하기 위해 Adobe Campaign 워크플로우를 활용할 수 있습니다. 이 채널은 Mobile Core Service의 SDK를 활용합니다.<br /> 이 기능을 사용하려면 유료 솔루션인 Mobile for Mobile 이 필요합니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../integrating/using/about-campaign-points-of-interest-data-integration.md"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> REST APIs<br /> </td> 
   <td> 이제 API에서 프로필 또는 서비스 리소스에 연결된 리소스를 사용할 수 있습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../developing/using/updating-the-database-structure.md#publishing-a-resource-with-api-extension"></a>참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-5}

#### General {#general-1}

* 이제 배달 로그를 내보낼 때 프로필 데이터를 추가할 수 있습니다.

#### Emails and SMS messages {#emails-and-sms-messages-2}

* Fixed an issue causing the **[!UICONTROL Request confirmation before sending messages]** option to remain selected even after unchecking it and saving the delivery.
* 트랜잭션 이메일 게시 취소를 방지할 수 있는 문제를 해결했습니다.
* 컨텐츠를 미리 보기 전에 컨텐츠가 최신 변경 사항과 제대로 동기화되지 않는 문제를 해결했습니다.

#### Landing pages {#landing-pages-1}

* 랜딩 페이지의 컨텐츠를 클릭할 때 사용자가 편집할 수 없는 오류를 수정했습니다.

#### Workflows {#workflows-5}

* Fixed an issue that could prevent from reading the content of the reject transition of a **[!UICONTROL Load file]** activity.
* **[!UICONTROL Load file]** 활동을 구성할 때 교환된 열이 제대로 고려되지 않는 문제를 해결했습니다.

## Release 17.1 - January 2017 {#release-17-1---january-2017}

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
   <td> Log export for external reporting<br /> </td> 
   <td> 배달 및 추적 로그와 같은 로그를 내보내 선호하는 보고 또는 BI 도구에서 처리할 수 있습니다. 점진적인 쿼리를 통해 간단한 워크플로우를 사용하여 새로운 로그의 정기적인 내보내기를 자동화할 수 있습니다.<br /> 리소스 피커에서의 로그 리소스 가용성 이외에도 <a href="../../automating/using/incremental-query.md">증분 쿼리</a> 및 <a href="../../automating/using/extract-file.md">파일 추출</a> 활동 기능이 향상되었습니다.<br /> 
    <ul> 
     <li> <span class="uicontrol">이제 증분 쿼리를</span> 통해 날짜 필드를 사용하여 새 데이터나 업데이트된 데이터를 검색할 수 있습니다. 이전에는 이전 실행의 모든 결과가 마지막 실행 이후 업데이트되더라도 자동으로 제외되었습니다. </li> 
     <li> <span class="uicontrol">이제 Extract 파일에서</span> ID가 아닌 열거형 값에 대한 레이블을 내보낼 수 있습니다. </li> 
    </ul> 이러한 활동은 모든 지역 및 조직 단위에 액세스할 수 있는 관리자가 사용할 수 있습니다.<br /> 로그 내보내기에 대한 자세한 내용은 <a href="../../automating/using/exporting-logs.md">자세한 설명서를</a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Marketing capabilities for transactional messages<br /> </td> 
   <td> 마케터는 고객 마케팅 프로필을 기반으로 트랜잭션 메시지를 보낼 수 있습니다. This allows them to:<br /> 
    <ul> 
     <li> Apply marketing typology rules such as <span class="uicontrol">Blacklisted address</span> . </li> 
     <li> 메시지 내에 구독 취소 링크를 포함합니다. </li> 
     <li> 트랜잭션 메시지를 전역 배달 보고에 추가합니다. </li> 
     <li> 고객 여정의 트랜잭션 메시지를 활용합니다. </li> 
    </ul> For more information, refer to the <a href="../../channels/using/profile-transactional-messages.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Transactional Messaging API<br /> </td> 
   <td> The Transactional Messaging API is now available through <a href="https://docs.campaign.adobe.com/doc/standard/en/adobeio.html">adobe.io</a>, making it easier to use and to monitor:<br /> 
    <ul> 
     <li> Adobe. IO 플랫폼 보고 및 모니터링 기능을 활용할 수 있습니다. </li> 
     <li> 이제 IP 화이트리스트 대신 Adobe. IO 토큰 기반 인증을 사용하여 인증이 수행되므로 보안 프로세스가 간단해집니다. </li> 
     <li> 모든 API는 이제 단일 플랫폼에 통합되어 있으므로 이미 프로필 및 서비스 API를 지원하는 경우 트랜잭션 메시징 기능을 통합으로 손쉽게 추가할 수 있습니다. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-6}

#### General {#general-2}

* **[!UICONTROL Access authorization]** 옵션이 랜딩 페이지 속성으로 반환되었습니다.
* 이전 이미지가 올바른 이미지 대신 렌더링되었던 문제를 수정했습니다. 이는 소스 이미지가 배달 또는 랜딩 페이지의 컨텐츠 정의에서 업데이트된 경우에 발생했습니다.
* 사용자가 기존 SFTP 외부 계정의 특정 필드를 편집할 수 없는 문제를 해결했습니다.
* 여러 UI 문제가 해결되었습니다. 예를 들어 사용자는 이제 UI에 문제가 발생하지 않고 프로필 속성을 편집하고 수정 내용을 저장할 수 있습니다.

#### Emails and SMS messages {#emails-and-sms-messages-3}

* 배달 템플릿과 관련된 문제가

#### Push notifications {#push-notifications-4}

* 애플리케이션에서 Adobe Campaign 서버로 포스트백을 금지했을 수 있었던 문제를 해결했습니다.
* Fixed an issue that may have prevented **[!UICONTROL Play a sound]** and **[!UICONTROL Custom fields]** to be taken into account for Android.
* 이모지지에 사용되는 유니코드 문자에 불필요한 이스케이프 문자가 추가되는 문제를 해결했습니다.
* 가입자의 등록 토큰이 블랙리스트에 추가되면 해당 상태는 이제 Adobe Campaign의 응용 프로그램의 구독자 목록에서 즉시 업데이트됩니다.

#### Workflows {#workflows-6}

* 이벤트 리소스 (예: Rtevent) 에 대한 쿼리 미리 보기가 되지 않던 문제를 수정했습니다.
* **[!UICONTROL Load file]** 활동에 의해 생성된 거부 파일은 이제 아웃바운드 전환에서 검색하여 다음 활동에서 처리할 수 있습니다. For example, upload the reject file via an SFTP server using **[!UICONTROL Transfer file]** .
* Fixed an issue that may have prevented a user from limiting the population of a segment if **[!UICONTROL Temporary resource]** was selected in the **[!UICONTROL General]** tab of **[!UICONTROL Segmentation]** .
* **[!UICONTROL Scheduler]** 더 이상 10 분마다 한 번 이상 워크플로우를 트리거하도록 활동을 설정할 수 없습니다.
* Fixed an issue that may have prevented **[!UICONTROL Use common columns]** from working properly in an **[!UICONTROL Union]** activity.

#### Integrations {#integrations-3}

* Adobe Campaign에서 이벤트 트리거를 배포할 때 오류가 발생하던 문제를 수정했습니다. 이 오류는 Adobe Marketing Cloud의 포기 트리거에 "30 일 후에 다시 돌아갈 수 있음" 메타데이터를 추가할 때 발생했습니다.
* 사용자 핵심 서비스에서 대상을 가져올 때 기술 워크플로우가 타겟 차원 필드를 지우는 문제를 해결했습니다. 이후 쿼리에서 가져온 대상을 검색할 수 없었습니다.
* Fixed an issue that may have caused the **[!UICONTROL Save audience]** activity of a workflow to fail when the option **[!UICONTROL Share in Adobe Marketing Cloud]** was checked.

