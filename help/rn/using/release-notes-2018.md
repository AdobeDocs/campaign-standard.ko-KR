---
title: 릴리스 노트 2018
seo-title: 릴리스 노트 2018
description: 릴리스 노트 2018
seo-description: 이 페이지에는 Adobe Campaign Standard의 2018 릴리스가 모두 나열됩니다.
page-status-flag: 정품 인증 안 함
uuid: 99 F 92 A 54-4 B 3 D -48 B 9-B 08 D-E 98 B 24 E 75 F 62
contentOwner: Sauviat
products: sg_ campaign/standard
audience: RN
content-type: 참조
topic-tags: campaign-standard-release
discoiquuid: E 54 F 8305-7 E 32-4193-8 E 5 A-B 5 D 87 B 03038 C
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 6a877d878f01fa1e541dc20b8b0941602113d15b

---


# Release Notes 2018{#release-notes}

Adobe Campaign Standard 2018 릴리스를 찾고 있습니까?

각 릴리스에는 새로운 기능과 패치가 포함되어 있습니다. 컨텐츠를 보려면 릴리스를 클릭합니다.

View the latest [documentation updates](../../rn/using/documentation-updates.md) for Adobe Campaign Standard. If you're looking for a newer release, consult this [page](../../rn/using/release-notes.md).

## Release 18.9 - September 2018 {#release-18-9---september-2018}

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
   <td> In-App messaging (beta)<br /> </td> 
   <td> 인앱 메시지를 사용하면 컨텍스트 상호 작용을 제공하고 푸시 알림을 옵트아웃했을 수 있는 사용자에게 도달할 수 있어 모바일 앱 사용자를 보다 효과적으로 유도할 수 있습니다. 푸시 알림과 함께 인앱 메시지를 사용하여 고도로 개인화되고 연관성 있는 경험을 제작할 수 있습니다. 이로 인해 앱 사용자의 전환율과 유지율이 향상됩니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../channels/using/about-in-app-messaging.md"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Adobe Launch integration for mobile apps (beta)<br /> </td> 
   <td> Adobe Campaign와 통합된 Adobe Launch는 이제 Mobile SDK v 5를 사용하여 캠페인에서 모바일 앱 속성 활성화 과정을 단순화하고 자동화합니다.<br /> 자세한 내용은 자세한 설명서를 <a href="https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html"></a>참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Improvements {#improvements}

* Adobe Campaign Standard는 이제 Amazon S 3 API의 버전 4를 지원합니다.

### Other changes {#other-changes}

* 이제 확장된 로그에서 최대 연결 수와 시간당 최대 메시지 수 간에 차이가 있습니다. 제한에 도달하면 처리가 제한된 이유를 파악할 수 있습니다. 이전에는 두 사례에 동일한 메시지 (' quota met ') 가 적용되었습니다.
* 이제 캠페인에서 모바일 애플리케이션을 구성할 때 사용자는 iOS 인증서 및 Android 서버 키가 성공적으로 업로드되었는지 및 만료 날짜가 되었는지 알 수 있습니다.

   For more on this, refer to the detailed documentation on how to configure a mobile application using [SDK V4](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html) and [SDK V5](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html).

* 캠페인 속성을 정의하는 동안 모바일 앱을 선택하여 특정 모바일 앱의 사용자를 타깃팅합니다. 이 기능은 푸시 및 인앱 메시징 채널을 위한 것입니다.

   For more information, refer to the [detailed documentation](../../channels/using/preparing-and-sending-a-push-notification.md#preparing-the-notification).

* Creative Designer 인터페이스를 사용하여 컨텐츠 블록을 선택하면 목록에서 모든 컨텐츠 블록이 로드되고 표시됩니다. (CAMP -27311)

   For more on this, refer to the [detailed documentation](../../designing/using/adding-a-content-block.md).

### Patches {#patches}

* 이메일 대시보드와 이메일 요약 보고서 간의 로그 카운트에서 트랜잭션 이메일에 대한 불일치를 표시하는 문제를 해결했습니다. (CAMP -28237
* 파일 전송 활동을 통해 파일을 가져올 때 오류 메시지를 표시할 수 있는 워크플로우에서 문제를 해결했습니다. (CAMP -27435)
* 25 개의 서비스가 포함된 랜딩 페이지에 대한 문제가 양식에서 임의로 선택 취소되도록 하는 문제가 해결되었습니다. (CAMP -26572)
* 파일 전송 활동을 사용할 때 Sftp URL로 외부 계정을 구성할 수 없는 워크플로우에서 문제를 수정했습니다. (CAMP -26475)
* 서비스 요약 보고서가 업데이트되지 않는 문제를 해결했습니다. (CAMP -26301)
* 강화 활동을 사용할 때 사용자 지정 필드가 올바른 날짜를 표시하지 않는 워크플로우의 문제를 해결했습니다. (CAMP -26242)
* 파일 가져오기를 통해 가져올 때 서비스 구독 날짜가 업데이트되지 않는 문제를 해결했습니다.
* 워크플로우가 파일을 가져올 수 없게 하는 로드 파일 활동 오류를 해결했습니다 (CAMP -27068).
* 서비스 요약 보고서에서 잘못된 구독 수를 표시하는 문제를 해결했습니다 (CAMP -25587).
* Adobe Analytics와 Adobe Campaign 보고서 간의 데이터 불일치 문제가 해결되었습니다. (CAMP -25393)
* 제한된 액세스 사용자가 로그인하는 것을 방지할 수 있는 문제를 해결했습니다. (CAMP -27381)
* Creative Designer를 사용하여 이메일을 편집할 때 Adobe Experience Manager 컨텐츠 목록이 표시되지 않는 문제를 해결했습니다. (CAMP -27181)
* Creative Designer가 열리지 않아 오류가 발생하는 문제를 해결했습니다. (CAMP -27304)
* Internet Explorer 11를 사용할 때 Creative Designer에서 드래그 앤 드롭이 올바르게 작동하지 않는 문제를 해결했습니다.
* 카메라에서 업로드한 사진과 세로 모드의 사진을 원하지 않는 회전한 위치에 표시하는 문제를 해결했습니다.
* Creative Designer에서 쿼리 편집기 인터페이스를 사용할 때 선택 사항이 명확하지 않은 문제를 해결했습니다.
* Creative Designer에서 쿼리 편집기 인터페이스를 사용할 때 요소를 올바르게 복제할 수 없는 문제를 해결했습니다.
* 자동 답글을 통해 구독 취소된 경우에도 차단된 수신자에게 SMS 메시지를 계속 전달하는 문제를 해결했습니다. (CAMP -27128)
* **데이터베이스 정리** 작업 과정이 실패하는 오류를 표시할 수 없는 문제를 해결했습니다. (CAMP -26876)
* 푸시 알림 정의에 사용자 정의 필드를 삭제할 수 없는 문제를 해결했습니다. (CAMP -25588)

## Release 18.7 - July 2018 {#release-18-7---july-2018}

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
   <td> High priority flag for Android push notifications<br /> </td> 
   <td> Android에 대한 높은 우선 순위 플래그 - Android 앱에 우선 순위가 높은 푸시 알림을 제공할 수 있으므로 절전 장치가 깨어 일부 제한된 처리가 실행됩니다. 기본 우선 순위는 배터리를 저장하도록 메시지 배달을 지연시킬 수 있는 일반적인 우선 순위입니다. <br /> 자세한 내용은 자세한 설명서를 <a href="../../channels/using/customizing-a-push-notification.md#change-the-notification-behavior-for-android"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Typology filter for mobile app subscribers<br /> </td> 
   <td> 유형 분석의 구독 지원 - 유형 규칙에 대한 필터링 기준을 지정할 때 애플리케이션 가입은 필터링 및 타깃팅 차원으로 선택할 수 있으므로 프로필 사용 여부와 상관없이 사용자를 위한 속성을 필터링할 수 있습니다. <br /> 자세한 내용은 자세한 설명서를 <a href="../../administration/using/about-typology-rules.md#typology-rules"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Automated content import from a URL during message preparation<br /> </td> 
   <td> 준비 단계 동안 URL에서 이메일 컨텐츠를 가져올 수 있습니다. 반복되는 이메일 배달의 경우 메시지가 전송될 때 항상 최신 내용이 항상 최신 상태로 유지되도록 메시지가 준비될 때마다 최신 HTML 콘텐츠가 검색됩니다. 또한 이 기능을 사용하면 컨텐츠가 아직 준비되지 않았더라도 URL의 컨텐츠가 포함된 예약된 배달을 만들 수 있습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../designing/using/importing-content-from-a-url.md#retrieving-content-from-a-url-automatically-at-preparation-time"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Campaign release notification message<br /> </td> 
   <td> 이제 인스턴스가 새 버전으로 업그레이드된 후 사용자가 로그인할 때 팝업 메시지가 나타납니다. 메시지는 버전 번호를 나타내며 릴리스 노트에 대한 링크를 포함합니다. You can choose to hide the message until the next release. <br /> </td> 
  </tr> 
  <tr> 
   <td> User management<br /> </td> 
   <td> 이제 지리적 유닛 기능을 새 캠페인 표준 인스턴스에는 사용할 수 없고, 18.7 릴리스부터는 지리적 단위가 없는 기존 인스턴스는 사용할 수 없습니다.<br /> 자세한 내용은 이 <a href="https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html">페이지를</a>참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Improvements {#improvements-1}

* The Adobe Campaign and Adobe Target integration now allows you to leverage Target’s [Permissions](https://marketing.adobe.com/resources/help/en_US/target/target/properties-overview.html) feature. 이메일에 Adobe Target의 동적 이미지를 포함할 때 이제 target 속성 (_ property code) 를 지정할 수 있습니다.
* 이제 GDPR 개인 정보 액세스/삭제 요청에 의해 프로필 리소스에 대한 owncopy 링크가 있는 사용자 지정 리소스가 고려됩니다. 1 개의 카디널리티 단순 링크 및 n 개의 카디널리티 수집 링크의 경우, "타겟 레코드를 삭제/복제하면 사용자 지정 리소스의 링크에 참조된 레코드를 삭제/복제하는 함축" 를 선택해야 합니다. 0 또는 1 카디널리티 단순 링크의 경우 "레코드를 삭제/복제하는 것은 링크에서 참조하는 대상 레코드를 삭제/복제하는 함수입니다" 를 선택합니다.

### Other changes {#other-changes-1}

* 시간 초과 오류가 발생하지 않도록 보고서 공유 시간이 1 분에서 4 분으로 증가했습니다.
* 이메일의 컨텐츠를 편집할 때 새 디자인 디자이너가 기본적으로 열립니다. 원할 경우 변경 내용을 저장한 후에도 언제든지 기본 컨텐츠 편집기로 돌아갈 수 있습니다. For more on this, refer to the [detailed documentation](../../designing/using/about-email-content-design.md).
* 이제 Creative Designer에서 새 컨텐츠 구성 요소를 이메일에 추가할 수 있습니다. 회전판입니다. For more on this, refer to the [detailed documentation](../../designing/using/defining-the-email-structure.md#about-content-components).
* In a transactional message hot click report, when you click the **Change profile** button, now only the test profiles linked to the event that you defined for your transactional message are listed.

### Patches {#patches-1}

* 결과를 반환하지 못한 Byemail 쿼리 필터 문제를 해결했습니다. (CAMP -23420)
* 표준 사용자가 관리자 (/rest/head/* 끝점, 트랜잭션 메시징 화면, 프로필 및 대상 가져오기 화면) 로 제한된 특정 기능 또는 화면에 액세스하도록 허용하는 문제를 해결했습니다.
* 이름이 숫자로 시작되는 경우 GDPR 개인 정보 삭제 요청이 사용자 지정 리소스를 처리하지 못하는 문제를 해결했습니다.
* Adobe Experience Cloud에서 애플리케이션 가입자를 공유하지 못하게 하는 오류를 해결했습니다.
* 파일 이름에 공백이 포함된 경우 발생할 수 있는 파일 전송 활동 문제가 수정되었습니다. (CAMP -25936)
* 세션이 만료된 후 다시 연결 단추를 사용할 때 발생할 수 있었던 문제가 해결되었습니다. (CAMP -25560)
* 피로 규칙과 관련된 시간대 최적화로 배달을 전송할 때 제외가 발생할 수 있는 문제를 수정했습니다. (CAMP -25425)
* API GDPR 기능을 사용할 때 0-1 유형의 링크로 데이터를 삭제하지 못할 수 있는 문제를 해결했습니다.
* 피로 유형 규칙 규칙을 취소할 때 오류 메시지가 표시되는 문제를 해결했습니다.
* 게재 컨텐츠를 편집한 후 미리 볼 때 발생할 수 있었던 문제를 수정했습니다.
* 압축 해제 옵션을 사용하는 동안 CSV zip 파일을 처리할 때 발생할 수 있는 문제를 수정했습니다.
* 내장된 스타일을 사용하여 일부 텍스트를 링크에 변경하거나 해당 링크를 편집할 때 원치 않는 색상 글꼴과 서식이 표시되는 Creative Designer의 문제를 수정했습니다. (CAMP -26001)
* 핫 클릭 보고서가 동적 컨텐츠가 들어 있는 배달의 각 조건에 대한 백분율을 표시하는 문제를 해결했습니다. 이전에는 기본 변형에 대한 클릭만 표시되었습니다.

## Release 18.6 - June 2018 {#release-18-6---june-2018}

### Improvements {#improvements-2}

* **[!UICONTROL History]** API가 adobe. io에 추가되었습니다. 이를 통해 프로필의 마케팅 내역 관련 정보에 액세스할 수 있습니다. 터치포인트 수, 전송 전송, 미러 페이지 URL 등 For more on this, refer to the [dedicated use case](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#how-to-retrieve-the-mirror-page-for-a-delivery-sent-to-a-profile) .
* **[!UICONTROL Database cleanup]** 기술 워크플로우는 데이터베이스 백업 성능을 향상시키기 위해 최적화되었습니다.
* 이제 이메일을 위한 Creative Designer도 프랑스어와 독일어로 제공됩니다.

### Other changes {#other-changes-2}

* A **[!UICONTROL Compute stats]** button has been added in the **[!UICONTROL Deployment]** window of sent deliveries. 예를 들어 보내기의 결과가 너무 오래 걸리거나 고려되지 않는 경우 최신 KPI를 검색할 수 있습니다. For more on this, refer to this [section](../../sending/using/confirming-the-send.md).
* In the **Update for deliverability** out-of-the-box technical workflow, functional administrators can now define the number of consecutive errors to ignore in the **Update rules** javascript activity. 기본적으로 필드 값은 0로 설정되며 모든 오류는 무시됩니다.
* 유닛 액세스 제한 조건을 관리할 때 생성된 SQL 이 최적화되었습니다.
* **[!UICONTROL Update]** 이제 활동을 통해 가입과 관련된 데이터를 추가, 업데이트 또는 삭제할 수 있습니다 (NMS: Appsubscriptionrcp 테이블을 참조하십시오.
* **[!UICONTROL Update delivery execution]** 기술 워크플로우는 성과를 최적화하기 위해 두 개의 워크플로우로 나뉘어져 있습니다. **[!UICONTROL Update delivery execution]**-: 게재 추적을 업데이트합니다. 기본적으로 10 분마다 시작됩니다. **[!UICONTROL Update delivery indicators]**: 배달의 KPI를 업데이트하면 기본적으로 매 시간마다 시작됩니다. For more on technical workflows, refer to this [section](../../administration/using/technical-workflows.md#list-of-technical-workflows).
* When a delivery is sending messages, the status in the **[!UICONTROL Deployment]** section can now have two values: **[!UICONTROL Sending]**: the messages are being sent. **[!UICONTROL Sending (retry)]**: 재시도 과정이 진행 중입니다.
* **[!UICONTROL Delivery preparation]** 역할이 있는 사용자는 이제 증거 자료를 보낼 수 있습니다. (CAMP -24313)
* The **Enable TLS over SMPP** option has been added to the **SMS routing via SMPP** external account. For more on this refer to this [section](../../administration/using/configuring-sms-channel.md#defining-an-sms-routing).

### Patches {#patches-2}

* Adobe Target의 동적 이미지를 포함할 때 이메일이 전송되지 않는 문제를 해결했습니다 (CAMP -24848).
* Fixed an issue with the **[!UICONTROL Privacy Access/Delete Request]** technical workflows, which did not complete if any of the requests failed.
* 개인 정보 핵심 서비스가 캠페인에서 요청 상태 업데이트를 받지 못하는 문제를 해결했습니다.
* **[!UICONTROL Import shared audience]** 기술 작업 과정이 제대로 작동하지 않는 문제를 해결했습니다 (CAMP -25465).
* 캠페인 개인 정보 요청이 핵심 개인 정보 보호 서비스에서 완료된 것으로 표시되지 않는 문제를 해결했습니다.
* Adobe ID가 너무 긴 경우 IMS 인증을 통해 특정 사용자가 Campaign Standard에 로그인하지 못했던 문제를 수정했습니다. (CAMP -24095)
* 컨텐츠 모듈을 제거할 때 발생할 수 있는 Creative Designer의 문제를 수정했습니다. (CAMP -25242)
* 데이터베이스에 프로필이 없는 가입자에 대해 푸시 알림 사용 규칙 사용 시 문제를 해결했습니다. (CAMP -25344)
* 배달 제외 로그에 액세스할 때 오류 메시지를 표시할 수 있는 문제를 해결했습니다. (CAMP -24724)
* 확장된 전송 로그가 있는 인스턴스에서 교정본을 준비할 수 없는 문제를 해결했습니다.
* Fixed two issues that could occur when publishing custom resources with the **[!UICONTROL Sending log]** extension activated.
* 배달 지속 시간이 반복되는 배달에서 고려되지 않던 문제를 수정했습니다.
* Fixed an issue that could occur when sorting data in the **[!UICONTROL Client data]** menu, for custom resources with more than 100K records. (CAMP -24308)
* 다이내믹 보고서에서 검색 기능을 사용할 때 고려되지 않았던 사용자 지정 프로필 차원 문제를 수정했습니다.
* 다이내믹 보고서에서 계정 수준용 국제 데이터 표시 관련 문제를 해결했습니다.
* 이제 구독 또는 구독 취소 확인 메시지 없이 서비스를 만들 수 있습니다.

## Release 18.5 - May 2018 {#release-18-5---may-2018}

### What's new? {#what-s-new--2}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> GDPR: Core Service Integration<br /> </td> 
   <td> 개인 정보 핵심 서비스 통합을 통해 단일 JSON API 호출을 통해 다중 솔루션 컨텍스트에서 GDPR 요청을 자동화할 수 있습니다. <br /> 개인정보 보호 코어 서비스에서 모든 Experience Cloud 솔루션에 대한 GDPR 요청은 이제 캠페인별로 자동으로 처리됩니다. <br /> 자세한 내용은 자세한 설명서를 <a href="https://docs.campaign.adobe.com/doc/standard/getting_started/en/ACS_GDPR.html"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Push improvements - detailed delivery feedback<br /> </td> 
   <td> Adobe Campaign는 이제 MCPNS를 통해 공급자 (APNS/GCM) 의 푸시 메시지에서 세부 피드백 (로그 ET 제외 로그 전송) 를 받을 수 있는 기능을 제공합니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../channels/using/preparing-and-sending-a-push-notification.md#sending-the-notification"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Delivery logs extension<br /> </td> 
   <td> 배달 로그 확장을 사용하면 워크플로우에서 제공되는 프로파일 데이터와 세그먼트 코드로 로그를 확장할 수 있습니다. 그런 다음 이 정보를 동적 보고서에서 사용할 수 있으며 배달 전송 시 일부 정보의 스냅숏을 유지할 수 있습니다.<br /> 두 가지 사례가 더 있습니다.<br /> 
    <ul> 
     <li> 확장된 확장 로그를 "고정" 데이터로 내보내기: 마케터는 세그먼트 코드가 "A" (워크플로우 엔진에서 제공) 인 모든 프로필을 내보내려고 합니다. </li> 
     <li> Segmentation on "frozen" data: As a marketer, I would like to <strong>retarget</strong> all profiles who have won 1000 loyalty points since the last sending or where segment code was equal to "A". </li> 
    </ul> For more information, refer to the <a href="../../developing/using/configuring-the-resource-s-data-structure.md#defining-sending-logs-extension">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Dynamic reporting with Custom profile data<br /> </td> 
   <td> 이 기능을 사용하면 프로필 리소스 확장 기간 동안 생성된 사용자 지정 프로필 데이터를 기반으로 보고서를 만들고 관리할 수 있습니다. 충성도 프로그램, 기본 채널 등과 같은 프로필 속성별로 보고서를 분류할 수 있습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../developing/using/configuring-the-resource-s-data-structure.md#defining-sending-logs-extension"></a>참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Improvements {#improvements-3}

* 애플리케이션의 전체 메모리 및 CPU 사용이 향상되었습니다.

### Other changes {#other-changes-3}

* 이제 고객 워크플로우 읽기 활동에서 Experience Cloud 대상을 읽을 수 있습니다. 이전에는 이 활동은 쿼리 및 목록 대상자만 읽을 수 있었습니다. [](../../automating/using/read-audience.md)자세한 내용은 설명서를 참조하십시오. (CAMP -23623)
* 기본 공유 데이터 소스의 식별자가 이제 읽기 전용 모드이며 더 이상 변경할 수 없습니다. 이 식별자를 변경하면 Experience Cloud와 대상을 공유할 때 몇 가지 문제가 발생할 수 있습니다.
* 이제 Audience Manager에서 대상을 가져올 때 파일 분할이 작동합니다. 이전에는 Importsharedaudience 기술 워크플로우에서 세그먼트의 마지막 파일만 가져왔습니다.
* 이제 AWS S 3 외부 계정이 지역 및 버전 4 인증 메커니즘을 지원합니다. [](../../administration/using/external-accounts.md)자세한 내용은 설명서를 참조하십시오.
* 이제 자산 선택 창이 더 빠르게 로드되고 자산을 선택할 수 있도록 허용하여 문제 없이 창을 종료합니다.
* 이제 관리 권한이 있는 사용자가 기술 워크플로우의 속성 및 구조를 수정할 수 있으며 "모든" 조직 및 지리적 위치에 속하게 됩니다.
* 새 세그먼트를 만들 때 세그멘테이션 활동 인터페이스에서 개선이 이루어졌습니다. 제한 탭을 추가하면 제한 사항을 추가한 다음 바로 나타납니다. 이제 새 세그먼트의 이름이 증가됩니다 ("segment 1", "segment 2" 등).
* " Nextprocessingdate "필드가 Workflow 리소스에 추가됩니다. 이 필드는 REST API 호출을 통해서만 볼 수 있으며, 다음 처리 날짜를 워크플로우에 시각화할 수 있습니다.
* 이제 "Sourceid" 필드가 추적 로그 리소스에 노출됩니다 (NMS: Trackinglog).
* 이제 워크플로우를 통해 "총 클릭 수" 및 "총 클릭 수" 값을 일반 파일로 내보낼 수 있습니다. (CAMP -24186)
* 이제 프로필의 기본 언어 목록에서 "영어 - Danmark" 를 사용할 수 있습니다. (CAMP -23728)
* 추가 데이터 (Targetdata) 링크가 있는 세그멘테이션 활동을 사용할 때 이제 이 데이터가 워크플로우 외부에서 사용할 수 없다는 메시지가 표시됩니다. 이 메시지는 세그멘테이션 활동에서 카운트 또는 미리 보기 단추를 클릭하면 표시됩니다. (CAMP -23651)
* 워크플로우에서 사용되는 디스크 공간을 최적화하기 위해 개선 사항이 적용되었습니다. (CAMP -21979): 이제 "파일 로드" 활동에 의해 처리된 파일이 기본적으로 삭제됩니다. 옵션을 사용하면 특정 요구 사항에 맞게 유지할 수 있습니다. 워크플로우가 삭제되면 전용 폴더가 서버 디렉토리에서 자동으로 억제됩니다.

### Patches {#patches-3}

* Eventdate 필드가 제대로 채워지지 않아 일부 Raw 보고 이벤트에 연관된 추적 이벤트가 없는 문제를 수정했습니다.
* 푸시 알림 배달의 미리 보기 창에 개인화된 필드가 표시되지 않던 문제를 수정했습니다.
* 미리 보기 창에서 푸시 알림의 메시지 본문을 Word-래핑하지 못했던 문제를 수정했습니다.
* 기본 Target 이 비어 있을 때 워크플로우에서 재방문 제공을 전송할 때의 문제를 수정했습니다.
* 기존 스키마에 연결되어 있을 경우 타겟 매핑에 액세스할 수 없는 문제를 해결했습니다.
* 파일 로드 활동을 통해 zip 파일을 가져올 때 발생할 수 있는 문제를 수정했습니다. (CAMP -24309)
* 반복적인 배달을 전송할 때 Postgresql 오류가 발생하던 문제를 수정했습니다. (CAMP -23613)
* 빈 JSON 속성을 사용하여 REST API 요청을 전송할 때 오류 메시지를 표시하는 문제를 해결했습니다. (CAMP -23506)
* " ß "문자 다음에 나오는 문자를 대문자로 설정하는 프로필 문제가 해결되었습니다. (CAMP -23136)
* 프로필 연결된 프로필의 속성을 사용하는 동안 개인화 또는 동적 컨텐츠 블록의 자격 조건과 함께 사용된 배달을 전송할 때 발생하는 문제를 수정했습니다. (CAMP -22751)
* 서비스를 삭제하지 못하는 문제를 해결했습니다. (CAMP -22050)
* 테스트 프로필에서 국가 또는 상태 값을 변경하지 못하는 문제를 해결했습니다. (CAMP -20426)
* Creative Designer가 로드되지 않는 문제를 해결했습니다. (CAMP -24573)
* 이메일 제목의 개인화 필드 이후에 추가된 문자가 제거된 문제를 수정했습니다. (CAMP -24113)

## Release 18.4 - April 2018 {#release-18-4---april-2018}

### Patches {#patches-4}

#### Platform {#platform}

* GDPR 액세스 또는 삭제 요청을 제대로 처리하지 못하는 오류를 해결했습니다. 이 비헤이비어는 추출된 데이터에 다음 문자 중 하나가 들어 있었던 드문 경우에 관찰되었습니다. &amp; &lt; &gt; "'.

#### Emails, SMS messages and direct mail {#emails--sms-messages-and-direct-mail}

* Broadlog 동기화가 1 시간 이상 걸리는 경우 잘못된 값으로 KPI를 덮어쓰는 문제를 해결했습니다.

#### Workflows {#workflows}

* 워크플로우에서 메모리 관리 및 최적화된 성능을 개선했습니다.

#### Reporting {#reporting}

* 이제 KPI 공유 워크플로우는 지난 6 개월 대신 지난 2 개월 동안의 배달 값을 검색합니다. 잘린 날짜를 표시하는 외부 계정 KPI 공유 문제를 해결했습니다.
* **전송**, **배달됨** 및 **바운시etrics에서 특정 메시지가 고려되지 않는 문제를 해결했습니다**.
* **배달 요약 보고서의** 선택한 시간 범위가 너무 긴 경우 발생하는 오류가 수정되었습니다.

#### Custom resources {#custom-resources}

* 사용자 지정 리소스 준비 오류가 발생하는 오류를 해결했습니다.

## Release 18.3 - March 2018 {#release-18-3---march-2018}

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
   <td> EU General Data Protection Regulation (GDPR)<br /> </td> 
   <td> GDPR는 2018 년 5 월 25 일부터 발효되는 데이터 보호 요구 사항을 통합하고 현대화한 유럽 연합의 새로운 개인 정보 보호 법입니다. GDPR는 EU의 데이터 주체에 대한 데이터를 보유한 Adobe Campaign 고객에게 적용됩니다.<br /> Adobe Campaign (동의 관리, 데이터 유지 설정 및 사용자 역할 포함) 에서 이미 사용할 수 있는 개인정보 보호 기능 이외에도, Adobe는 특정 GDPR 요청에 대한 데이터 관리자로서 귀하의 준비를 용이하게 하기 위해 데이터 처리자의 역할에서 이 기회를 포착하고 있습니다.<br /> 
    <ul> 
     <li> 액세스 권한: 데이터 주체가 데이터 관리자가 캡처한 개인 데이터의 사본을 받을 수 있도록 하며, Adobe Campaign에 저장된 데이터를 포함합니다. </li> 
     <li> 삭제할 권리: 데이터 주체의 개인 데이터가 지워져 Adobe Campaign에 저장된 데이터가 포함될 수 있는 데이터 주체의 권한을 부여합니다. </li> 
    </ul> For more information, refer to the <a href="https://docs.campaign.adobe.com/doc/standard/getting_started/en/ACS_GDPR.html">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Creative Designer for Email (Beta)<br /> </td> 
   <td> Adobe Campaign의 새로운 Creative Designer는 캠페인에서 완벽하게 통합된 제작 경험을 제공하므로 한 줄의 코드를 스크립팅하지 않고도 개인화된 매력적인 이메일을 빠르고 손쉽게 작성할 수 있습니다. Creative Designer는 강력한 드래그 앤 드롭 인터페이스를 통해 사용자가 빈 슬레이트에서 시작하거나 기존 콘텐츠 조각 또는 템플릿을 활용하더라도 이메일 작성을 확장할 수 있습니다. <br /> 주요 기능은 다음과 같습니다.<br /> 
    <ul> 
     <li> 기본 Creative Cloud 통합으로 강화된 드래그 앤 드롭 인터페이스를 통해 완전히 개인화된 반응형 이메일을 시각적으로 디자인 및 제작 </li> 
     <li> 이메일 컨텐츠 템플릿을 작성 및 저장하고 저장된 템플릿을 활용하여 이메일 작성 비율 확장 </li> 
     <li> 컨텐츠 조각 (머리글, 바닥글, 기사 등) 를 만들고 저장합니다. 컨텐츠 제작을 간소화하고 브랜드 일관성을 보장하려면 </li> 
     <li> 드래그 앤 드롭 인터페이스에서 제작 과정을 원활하게 전환하고 클릭 시 이메일 HTML를 직접 편집 </li> 
    </ul> 이메일을 위한 Creative Designer는 영어로만 제공됩니다.<br /> 자세한 내용은 <a href="../../designing/using/about-email-content-design.md#about-the-email-designer">자세한 설명서를</a> 참조하고 <a href="https://www.youtube.com/watch?time_continue=1&amp;v=5S_6A4fsfms">이 비디오를</a>시청하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Multilingual Push Deliveries<br /> </td> 
   <td> 이메일 및 SMS 채널에 이미 존재하는 동일한 간단한 다국어 인터페이스가 푸시 채널에 추가되어 고객이 선호하는 언어로 고객의 시선을 사로잡을 수 있습니다.<br /> 이 기능은 여러 지역을 아우르는 푸시 캠페인을 관리하고 사용자를 선호하는 언어로 타깃팅하려는 고객을 위한 확장 가능한 자동 솔루션을 제공합니다. 템플릿 기반의 스프레드시트를 통해 모든 언어 변형을 한 번의 클릭으로 하나의 푸시 전달 방식으로 업로드할 수 있습니다. 그러면 Adobe Campaign는 사용자의 언어 기본 설정을 기반으로 자동 세그먼테이션을 수행하므로 워크플로우 및 보고를 단순화하여 중복을 줄일 수 있습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../channels/using/creating-a-multilingual-push-notification.md"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Use of Custom Resources in Transactional Messaging<br /> </td> 
   <td> 이제 기본 필드 외에도 트랜잭션 메시징을 사용하여 사용자 정의 리소스를 사용하여 메시지 내용을 강화할 수 있습니다.<br /> 예를 들면 다음과 같습니다.<br /> 
    <ul> 
     <li> 사용자 정의 필드를 조정 기준으로 활용하여 트랜잭션 메시지를 프로필에 일치 </li> 
     <li> 전체 프로파일, 서비스 및 링크로 연결된 데이터를 활용하여 거래 메시지 개인화 </li> 
    </ul> For more information, refer to the <a href="../../administration/using/configuring-transactional-messaging.md">detailed documentation</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-5}

#### Platform {#platform-1}

* 목록에서 5000 개 이상의 레코드를 내보낼 수 없는 문제를 해결했습니다.
* 개인화 필드로 이름이 지정된 파일로 데이터를 내보낼 때의 문제를 수정했습니다.

#### Emails, SMS messages and direct mail {#emails--sms-messages-and-direct-mail-1}

* 부분 크기를 바이트 대신 문자로 계산했기 때문에 다중 부분 SMS가 잘리는 문제를 해결했습니다.
* Added an option which allows the **[!UICONTROL Delivered]** or **[!UICONTROL Bounces + Errors]** KPIs to be updated in real time after sending your delivery. 공급자로부터 받은 SR (상태 보고서) 에서 직접 다시 계산됩니다.
* 배달 스케줄러의 달력 위젯에 대한 문제를 수정했습니다.
* 전송 배달에서 두 번째 타깃팅을 열 때의 표시 문제를 수정했습니다.
* 지연된 전송 날짜로 이메일 템플릿을 만들 때 시작 날짜를 요청하는 오류 메시지가 표시되는 문제를 해결했습니다.
* 게재의 컨텐츠를 편집할 때 이미지 렌더링 문제를 일으킬 수 있는 문제를 해결했습니다.
* 캠페인을 복제할 때 증명 문제가 수정되었습니다.
* 워크플로우에 배달을 추가한 후 내비게이션 막대를 통해 캠페인 템플릿에 액세스할 때 오류 메시지가 표시되는 문제를 해결했습니다.
* A/B 테스트 이메일의 우승자가 자동으로 선택되는 것을 방지하고 이메일을 보내지 않는 문제를 해결했습니다. This behavior could occur if the delivery was in **[!UICONTROL retryInProgress]** state.
* A/B 테스트 이메일의 매개 변수를 다시 열 때 오류 메시지가 표시되는 문제를 해결했습니다.

#### Audiences &amp; queries {#audiences-e-queries}

* Adobe Campaign Classic에서 표준으로 복제한 수신자에 대한 데이터 액세스 및 쿼리 설정이 되지 않던 문제를 수정했습니다.
* **카운트** 또는 **미리 보기** 단추를 사용한 후 쿼리 편집기에서 필터 유형 필드를 사용할 때 발생하던 문제를 수정했습니다.

#### Workflows {#workflows-1}

* **청구** 워크플로우는 배달 준비 지연을 개선하기 위해 최적화되었습니다.
* 반복되는 배달 활동을 사용할 때 아웃바운드 전환 시 모집단 데이터가 표시되지 않는 문제를 해결했습니다.
* Fixed an issue that prevented reject records from being displayed in a transition after an **Update data** activity.
* Fixed an issue which could cause the **deliverabilityUpdate** technical workflow to fail.

#### Integrations {#integrations}

* 국제 문자가 Adobe Analytics로 올바르게 전송되지 않는 문제를 해결했습니다.
* 이제 Experience Cloud 자산 라이브러리의 이미지를 메시지에 삽입하려고 하면 에셋이 빠르게 로드됩니다.
* 자산 선택 창이 가끔씩 닫히는 것을 방지할 수 있는 문제를 해결했습니다.
* 이제 Datasource 세부 정보에서 관련 워크플로우에 직접 액세스하여 워크플로우 상태를 확인할 수 있습니다.
* 트리거 이벤트를 정의하거나 편집할 때 바로 트리거 스키마를 업데이트할 수 있습니다. 이 변경 사항으로, 트리거를 취소하고 다른 트리거를 만들 필요가 없습니다.

#### Transactional messages {#transactional-messages}

* 전달 리소스가 연장될 때 트랜잭션 메시지 템플릿이 있는 오류를 수정했습니다.
* 이제 트랜잭션 메시지를 삭제할 수 있습니다.

## Release 18.2 - February 2018 {#release-18-2---february-2018}

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
   <td> Subscription - subscribe or unsubscribe a list of profiles to multiple services<br /> </td> 
   <td> <strong>구독 서비스</strong> 워크플로우 활동을 통해 프로파일 목록을 구독 또는 구독 취소할 수 있습니다. 워크플로우에서 프로파일이 포함된 파일과 각 프로필, 작업 유형 및 서비스를 가져옵니다. <strong>구독 서비스</strong> 활동은 이 정보를 사용할 수 있고 모든 프로필 구독 및 구독 취소 사항을 한 번에 동적으로 처리할 수 있습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../automating/using/subscription-services.md"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Enrichment activity - enrich data based on previous transitions<br /> </td> 
   <td> <span class="uicontrol">새로운 강화</span> 워크플로우 활동을 통해 인바운드 전환을 활용하고 추가 데이터로 출력 전환을 완료할 수 있습니다. 프로파일을 타깃팅하는 경우, 강화 활동을 통해 데이터베이스에 저장되지 않은 추가 데이터 (예: 가져온 파일에서 오는 데이터) 를 사용하여 프로필 정보를 강화할 수 있습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../automating/using/enrichment.md"></a>참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-6}

#### Platform {#platform-2}

* Adobe Campaign 인터페이스의 상단 막대가 새로운 Experience Cloud 메뉴로 업데이트되었습니다.
* Fixed an issue which prevented the link to **[!UICONTROL Offers]** from being displayed in the solution dropdown list.

#### Emails, SMS messages and direct mail {#emails--sms-messages-and-direct-mail-2}

* 성능 향상을 위해 게재 준비 단계가 향상되었습니다.
* 일부 틈새 상황에서 추적 로그가 손상될 수 있는 몇 가지 문제가 수정되었습니다.
* 배달 준비 및 확인 간에 연락처 날짜가 변경되면 발생하던 연락 날짜 업데이트 문제가 해결되었습니다. 이제 준비 완료 후 연락처 날짜를 변경할 때 전송을 확인하려면 먼저 배달을 준비해야 합니다. [](../../sending/using/preparing-the-send.md)자세한 내용은 설명서를 참조하십시오.

#### Push notifications {#push-notifications}

* 일부 개인화 필드가 iOS 푸시 알림에서 작동하지 않던 문제를 수정했습니다.
* 푸시 알림 대시보드에서 클릭 및 개방 비율이 0%로 표시되는 오류를 수정했습니다.

#### Reports {#reports}

* 일부 브라우저에서 보고서 목록이 비어 있는 것으로 표시되는 오류를 수정했습니다.
* Fixed an error that occurred in the **[!UICONTROL Report sharing]** technical workflow just before its expiration limit was reached.

#### Workflows {#workflows-2}

* 활동을 드래그 앤 드롭한 후 액세스할 수 없는 문제를 해결했습니다.
* Fixed an issue that could cause the order of output transitions of a **[!UICONTROL Segmentation]** activity to change in some situations.
* 열거형 유형 필드가 들어 있고 이전에 워크플로우에서 저장된 대상자를 읽을 때 발생하는 오류가 해결되었습니다.
* Fixed an issue causing the **[!UICONTROL Request confirmation before sending messages]** option to remain checked even after unchecking it when defining the scheduling properties of a delivery created in a workflow.
* Automatic removal of duplicate rows (DISTINCT clause) can now be disabled in **[!UICONTROL Query]** activities, via a new option located in the **[!UICONTROL Additional data]** tab. 성능상의 이유로 많은 (100 개 이상의) 요소를 정의할 때에는 이 옵션을 비활성화하는 것이 좋습니다.

#### Integrations {#integrations-1}

* **[!UICONTROL Data sources]** 구성 화면이 일부 개선되었습니다.

### Known issues {#known-issues}

가능한 디스플레이 문제로 인해 Internet Explorer 버전 11를 사용하지 않는 것이 좋습니다.

캠페인 인터페이스에서 컨텍스트 도움말 링크를 사용할 때 몇 가지 문제가 발생할 수 있습니다. 18.3에서 수정됩니다.

## Release 18.1 - January 2018 {#release-18-1---january-2018}

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
   <td> Reporting for Fatigue Management<br /> </td> 
   <td> 피로 관리에 대한 보고는 전송 전에 지정된 날짜 범위 내에서 이메일, 푸시, SMS 및 DM 채널에서 영향을 받는 피드에 영향을 미치는 영향을 표시하는 구성 가능한 전용 보고서입니다. 단일 뷰에서 모든 충돌하는 캠페인을 신속하게 확인할 수 있다는 통찰력을 더해 마케터는 피로 규칙을 보다 효과적으로 설정하고 커뮤니케이션의 우선 순위를 지정함에 따라 마케팅 캠페인을 계획할 수 있습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../administration/using/fatigue-rules.md#viewing-the-fatigue-rule-summary-report"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Report sharing<br /> </td> 
   <td> 보고서 공유를 사용하면 자동 반복 기반 등의 이메일 첨부 파일로 보고서를 Adobe Campaign 사용자와 공유할 수 있습니다. 반복되는 보고서를 수신하는 사용자는 각 이메일의 전용 링크를 통해 이러한 커뮤니케이션에서 가입을 해지할 수 있습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../reporting/using/reporting-interface.md#share-tab"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Push New capabilities<br /> </td> 
   <td> 푸시 메시지 미리 보기 - 푸시 알림 컨텐츠 편집기 내에서 iOS 및 Android 디바이스에서 푸시 알림을 미리 볼 수 있으므로 테스트 또는 전달 전에 수신자가 보게 될 내용을 정확하게 확인할 수 있습니다.<br /> 자세한 내용은 자세한 설명서를 <a href="../../channels/using/preparing-and-sending-a-push-notification.md#preparing-the-notification"></a>참조하십시오.<br /> 컨텐츠 이용 가능 - 장기간 앱을 열지 않으면 데이터가 최신 상태가 될 수 있습니다. 이렇게 하면 사용자가 마지막으로 앱을 열었을 때 데이터가 업데이트되거나 바뀌어야 하며, 이로 인해 앱 사용에 지연이 발생할 수 있습니다. Adobe Campaign 사용자는 제공되는 컨텐츠에 대한 지원을 추가하여 푸시 알림을 전달할 때 백그라운드에서 데이터를 새로 고칠 수 있으므로 사용자의 앱 내 경험을 보다 일관성 있게 유지하고 제어할 수 있습니다.<br /> 변경 가능한 컨텐츠 - 이제 Adobe Campaign 사용자는 mutable 컨텐츠에 대한 지원이 추가되어 모바일 앱 익스텐션을 활용하여 Adobe Campaign에서 전송된 푸시 알림의 컨텐츠나 프레젠테이션을 수정할 수 있습니다. For example, users can leverage Mutable Content to: <br /> 
    <ul> 
     <li> 암호화된 형식으로 전달된 데이터 해독 </li> 
     <li> 이미지 또는 기타 미디어 파일을 다운로드하여 알림에 첨부 파일로 추가 </li> 
     <li> 알림의 본문 또는 제목 텍스트 변경 </li> 
     <li> 알림에 스레드 식별자 추가 </li> 
    </ul> For more information on Content Available and Mutable Content, refer to the <a href="../../channels/using/customizing-a-push-notification.md#change-the-notification-behavior-for-ios">detailed documentation</a>.<br /><strong>경고:</strong> 푸시 알림에 대한 이러한 업데이트는 고객이 모바일 애플리케이션을 업그레이드해야 합니다. Refer to <a href="https://helpx.adobe.com/campaign/kb/understanding-campaign-standard-push-notifications-payload-struc.html">this technote</a> for more information.<br /> </td> 
  </tr> 
  <tr> 
   <td> Time-zone optimized deliveries<br /> </td> 
   <td> 모든 수신자의 시간대에서 특정 일/시간에 전달되는 반복되는 이메일, SMS 및 푸시 알림을 일정 간격으로 예약하여 여러 배달을 설정하지 않고도 적시에 메시지를 전달할 수 있습니다. <br /> 자세한 내용은 자세한 설명서를 <a href="../../automating/using/scheduler.md"></a>참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> API Signal activity triggering<br /> </td> 
   <td> 이제 Adobe Campaign Standard API에서 직접 워크플로우에 대한 신호 활동을 트리거할 수 있습니다.<br /> 자세한 내용은 자세한 <a class="anchorLink" href="https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#triggering-a-signal-activity" target="_blank">설명서를</a> 참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-7}

#### Platform {#platform-3}

* 프로필 검색은 성능을 개선하기 위해 최적화되었습니다.
* 기본 보안 그룹의 내부 식별자는 이제 표준 사용자를 위한 읽기 전용 모드입니다.

#### Emails, SMS messages and direct mail {#emails--sms-messages-and-direct-mail-3}

* 이모지 삽입 시 발생했던 표시 문제를 수정했습니다.
* 배달이 여전히 에디션에 있을 때 사용자가 전송하는 로그에 액세스할 수 있었던 문제를 수정했습니다.
* **[!UICONTROL Scheduler]** 이제 활동을 통해 수신자의 시간대에 따라 배달을 보낼 수 있습니다.
* SMS: The option **[!UICONTROL Store incoming MO]** in the database has been added to external accounts. When checked, all incoming SMS will be stored into the **inSMS** table.
* SMS: 이제 서비스가 트랜잭션 템플릿 대신 이벤트에 첨부됩니다.
* SMS: 기본 SMTP 연결 시간 초과가 30 초로 줄어들었습니다.

#### Push notifications {#push-notifications-1}

* 푸시 알림 배달이 중지되지 않는 오류를 해결했습니다.
* 푸시 알림으로 응용 프로그램을 깨우도록 푸시 알림 고급 옵션에 옵션을 추가했습니다.
* 푸시 알림 미리 보기 비디오에 대한 일시 중지 단추가 추가되었습니다.
* 이제 iPhone, Android, 태블릿 등의 다양한 장치에 푸시 알림 미리 보기를 사용할 수 있습니다.

   모든 채널

#### Reports {#reports-1}

* 100% 이상의 비율을 표시하는 오류를 수정했습니다.
* 사용자가 CSV로 보고서를 다운로드할 수 없는 문제를 해결했습니다.
* Added a new **[!UICONTROL Report]** item in the homepage.

#### Workflows {#workflows-3}

* 쿼리에 추가 데이터를 사용하고 공백이 포함된 별칭을 추가할 때 오류 메시지로 표시되던 문제를 수정했습니다. 이제 숫자가 아닌 문자는 "_" 로 대체됩니다.
* KPI 계산 시 기본적으로 KPI 계산이 중지되는 문제가 해결되었습니다.

#### Profiles and audiences {#profiles-and-audiences}

* 대상의 쿼리에 여러 필터를 추가할 때 발생하는 오류를 수정했습니다.
* 프로필 사진을 변경할 때 발생하는 표시 문제를 수정했습니다.
* 쿼리의 모집단을 계산한 후 정확한 결과 수를 표시하는 도구 설명을 추가했습니다.
* 사용자가 대상자를 선택하거나 대상 선택기 창을 닫지 못하게 하는 문제를 해결했습니다.
* 표현식 편집기에서 사용할 수 있는 함수 목록이 업데이트되었습니다. **Formatcurrency** 및 **convertcurrency** 함수가 제거되었습니다.

