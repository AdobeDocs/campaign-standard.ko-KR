---
title: 푸시 알림 채널 변경 예정 사항
description: 푸시 알림 채널 변경 예정 사항
audience: channels
feature: Push
role: Admin
level: Experienced
exl-id: e273b443-7c43-482b-8f86-60ada4b57cbf
source-git-commit: db035a41515e94836bdfbfc3d620586dc1f5ce31
workflow-type: tm+mt
source-wordcount: '1134'
ht-degree: 1%

---

# 푸시 알림 채널 변경 사항 {#push-upgrade}

Campaign을 사용하여 Android 및 iOS 디바이스에서 푸시 알림을 전송할 수 있습니다. 이를 수행하기 위해 Campaign은 특정 구독 서비스를 사용합니다. Android FCM(Firebase Cloud Messaging) 서비스에 대한 몇 가지 중요한 변경 사항은 2024년에 릴리스되며, Adobe Campaign 구현에 영향을 줄 수 있습니다. 이 변경 사항을 지원하려면 Android 푸시 메시지에 대한 구독 서비스 구성을 업데이트해야 할 수 있습니다.

또한 Adobe은 보다 안전하고 확장 가능한 인증 기반 연결보다 토큰 기반 연결을 APNs로 이동하는 것이 좋습니다.

서비스가 중단되지 않도록 하려면 Adobe Campaign에 등록된 모바일 애플리케이션을 업그레이드하여 FCM(Android) 및 APNs(iOS)에 대한 최신 인증 메커니즘을 통합해야 합니다.


[Adobe Campaign Standard에서 모바일 애플리케이션 인증서를 구성하는 방법에 대해 자세히 알아보십시오](configuring-a-mobile-application.md#channel-specific-config)


## Google Android FCM(Firebase Cloud Messaging) 서비스 {#fcm-push-upgrade}

### 변경 사항 {#fcm-changes}

서비스 개선을 위한 Google의 지속적인 노력의 일환으로 레거시 FCM API는에서 중단됩니다. **2024년 6월 20일**. 에서 Firebase Cloud Messaging HTTP 프로토콜에 대해 자세히 알아보기 [Google Firebase 설명서](https://firebase.google.com/docs/cloud-messaging/http-server-ref){target="_blank"}.

시작 [24.1 릴리스](../../rn/using/release-notes.md), Adobe Campaign Standard은 Android 푸시 알림 메시지를 전송하기 위해 HTTP v1 API를 지원합니다.

### 영향을 받습니까? {#fcm-impact}

이미 Adobe Campaign Standard을 사용하여 푸시 알림을 전송하는 경우 구현을 업데이트해야 합니다.

서비스가 중단되지 않도록 하려면 최신 API로 전환해야 합니다.

<!--To check if you are impacted, you can filter your **Services and Subscriptions** as per the filter below

* If any of your active push notification service uses the **HTTP (legacy)** API, your setup will be directly impacted by this change. You must review your current configurations and move to the newer APIs as described below.

* If your setup exclusively uses the **HTTP v1** API for Android push notifications, then you are already in compliance and no further action will be required on your part.-->

### 업데이트 방법 {#fcm-transition-procedure}

#### 필수 구성 요소 {#fcm-transition-prerequisites}

* 의 지원 **HTTP v1 API** 모드가 24.1 릴리스에 추가되었습니다. 환경이 이전 버전에서 실행 중인 경우 이 변경을 위한 전제 조건은 환경을 [최신 Campaign Standard 릴리스](../../rn/using/release-notes.md).

* 모바일 애플리케이션을 HTTP v1로 이동하려면 Android Firebase 관리 SDK 서비스의 계정 JSON 파일이 필요합니다. 에서 이 파일을 가져오는 방법 알아보기 [Google Firebase 설명서](https://firebase.google.com/docs/admin/setup#initialize-sdk){target="_blank"}.

* 이 레거시 버전의 SDK를 계속 사용하는 경우 Adobe Experience Platform SDK를 사용하여 구현을 업데이트해야 합니다. 에서 Experience Platform SDK Adobe으로 마이그레이션하는 방법에 대해 알아봅니다. [이 문서](sdkv4-migration.md).

* 다음 항목이 있는지 확인하십시오. **모바일 앱 구성** 아래 단계를 수행하기 전에 Adobe Experience Platform Data Collection Mobile의 권한. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/collection/permissions.html?lang=en#adobe-experience-platform-data-collection-permissions){target="_blank"}.


#### 전환 절차 {#fcm-transition-steps}

환경을 HTTP v1로 이동하려면 다음 단계를 수행합니다.

1. 다음으로 이동 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile app (AEP SDK)]**.

   ![](assets/push_technote_1.png)

1. 인증서 업데이트가 필요한 특정 모바일 애플리케이션을 선택하십시오.

1. 다음 확인: **[!UICONTROL Update app credentials]** 확인란.

   ![](assets/push_technote_5.png)

1. Android 프로젝트의 앱 ID(Android 패키지 이름)를 제공합니다. `build.gradle` 파일. 예를 들어, `com.android.test.testApp`. 스테이징 및 프로덕션 환경에 서로 다른 ID를 사용해야 합니다.

1. Android 개인 키 JSON 키 파일을 업로드합니다.

   ![](assets/push_technote_3.png)

1. 다음을 클릭합니다. **저장** 단추를 클릭합니다.

>[!NOTE]
>
>이러한 변경 사항이 적용되면 Android 디바이스에 대한 모든 새로운 푸시 알림 게재는 HTTP v1 API를 사용합니다. 재시도 중, 진행 중 및 사용 중인 기존 푸시 게재는 여전히 HTTP(기존) API를 사용합니다.


## Apple iOS APNs(푸시 알림 서비스) {#apns-push-upgrade}

### 변경 사항 {#ios-changes}

Apple에서 권장하는 대로 상태 비저장 인증 토큰을 사용하여 APNs(Apple 푸시 알림 서비스)와의 통신을 보호해야 합니다.

토큰 기반 인증은 APNs와 통신하는 상태 비저장 방법을 제공합니다. 상태 비저장 통신은 APNs가 공급자 서버와 관련된 인증서 또는 기타 정보를 조회할 필요가 없기 때문에 인증서 기반 통신보다 빠릅니다. 토큰 기반 인증을 사용하면 다음과 같은 다른 이점이 있습니다.

* 여러 공급자 서버에서 동일한 토큰을 사용할 수 있습니다.

* 하나의 토큰을 사용하여 회사의 모든 앱에 대한 알림을 배포할 수 있습니다.

에서 APNs에 대한 토큰 기반 연결에 대해 자세히 알아보십시오. [Apple 개발자 설명서](https://developer.apple.com/documentation/usernotifications/establishing-a-token-based-connection-to-apns){target="_blank"}.

Adobe Campaign Standard은 토큰 기반 연결과 인증서 기반 연결을 모두 지원합니다. 구현이 인증서 기반 연결을 사용하는 경우 Adobe은 토큰 기반 연결로 업데이트할 것을 강력히 권장합니다.

### 영향을 받습니까? {#ios-impact}

현재 구현이 APNs에 연결하기 위해 인증서 기반 요청을 사용하는 경우 영향을 받습니다. 토큰 기반 연결로 전환하는 것이 좋습니다.

<!--To check if you are impacted, you can filter your **Services and Subscriptions** as per the filter below:

![](assets/filter-services-ios.png)


* If any of your active push notification service uses the **Certificate-based authentication** mode (.p12), your current implementations should be reviewed and moved to a **Token-based authentication** mode (.p8) as described below.

* If your setup exclusively uses the **Token-based authentication** mode for iOS push notifications, then your implementation is already up-to-date and no further action will be required on your part.-->

### 업데이트 방법 {#ios-transition-procedure}

#### 필수 구성 요소 {#ios-transition-prerequisites}

* 의 지원 **토큰 기반 인증** 다음 위치에 모드가 추가되었습니다. [24.1 릴리스](../../rn/using/release-notes.md). 환경이 이전 버전에서 실행 중인 경우 이 변경을 위한 전제 조건은 환경을 [최신 Campaign Standard 릴리스](../../rn/using/release-notes.md).

* 서버에서 사용하는 토큰을 생성하려면 APNs 인증 토큰 서명 키가 필요합니다. 에 설명된 대로 Apple 개발자 계정에서 이 키를 요청합니다. [Apple 개발자 설명서](https://developer.apple.com/documentation/usernotifications/establishing-a-token-based-connection-to-apns){target="_blank"}.


#### 전환 절차 {#ios-transition-steps}

iOS 모바일 애플리케이션을 토큰 기반 인증 모드로 이동하려면 다음 단계를 따르십시오.

1. 다음으로 이동 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile app (AEP SDK)]**.

   ![](assets/push_technote_1.png)

1. 인증서 업데이트가 필요한 특정 모바일 애플리케이션을 선택하십시오.

1. 다음 확인: **[!UICONTROL Update app credentials]** 확인란.

   ![](assets/push_technote_2.png)

1. 다음을 제공합니다 **앱 ID** (iOS 번들 ID). Xcode의 앱 기본 타겟에서 iOS 번들 ID(앱 ID)를 찾을 수 있습니다.

1. 업로드 **iOS p8 인증서 파일**.

1. APNs 연결 설정을 입력하십시오. **[!UICONTROL Key Id]** 및 **[!UICONTROL iOS Team Id]**.

   ![](assets/push_technote_4.png)

1. **[!UICONTROL Save]**&#x200B;를 클릭합니다.

이제 iOS 애플리케이션이 토큰 기반 인증 모드로 이동되었습니다.

## FAQ(자주 묻는 질문){#push-upgrade-faq}

+++스테이지 및 프로덕션 인스턴스에 동일한 appID를 유지할 수 있습니까?

iOS 모바일 애플리케이션의 경우 스테이징 및 프로덕션 환경 모두에 동일한 앱 ID(iOS 앱 번들 ID)를 사용할 수 있습니다. 그러나 Android에서 앱 ID는 각 환경에 대해 고유해야 합니다. 따라서 스테이징 환경에서 만든 앱 ID에 &#39;stage&#39;를 추가하는 것이 좋습니다

+++


+++Android 앱만 마이그레이션할 수 있습니까?

아니요. 위에 설명된 단계에 따라 Android 및 iOS 앱을 모두 마이그레이션해야 합니다.

+++

+++마이그레이션 후 어떤 유형의 확인을 수행해야 합니까?

모든 푸시 관련 사용 사례에 대한 기능 유효성 검사를 수행하는 것이 좋습니다.

+++

+++모바일 앱을 저장하는 동안 &#39;승인되지 않음&#39; 오류가 발생하면 어떻게 해야 합니까?

이는 Adobe Experience Platform 데이터 수집과 관련된 권한 문제로 보입니다. 이 문제를 해결하려면 이 문서의 사전 요구 사항 섹션에 설명된 대로 Adobe Admin Console에서 &#39;모바일&#39; 및 &#39;모바일 앱 구성&#39; 권한을 추가해야 합니다.

+++

+++모바일 앱 코드에 변경이 필요합니까?

아니요. Firebase 및 앱 개발자 계정에서 구성 관련 변경 사항만 있으면 됩니다. 고객 모바일 앱의 변경은 필요하지 않습니다.

+++

+++매년 iOS 인증서를 업데이트해야 합니까?

아니요. 이 마이그레이션 후에는 매년 iOS 인증서를 업데이트할 필요가 없습니다.

+++

+++이 마이그레이션이 수행되지 않으면 어떻게 됩니까?

Google의 알림에 따라 Android 푸시 메시지는 2024년 6월 20일 이후에 실패가 시작됩니다. [자세히 보기](https://firebase.google.com/docs/cloud-messaging/migrate-v1){target="_blank"}.

+++

+++FCMv1 마이그레이션을 완료한 후 고객이 다시 FCM으로 마이그레이션할 수 있습니까?

예. 고객은 2024년 6월 20일까지 FCM으로 다시 마이그레이션할 수 있습니다. 이 날짜 이후에는 마이그레이션 옵션을 더 이상 사용할 수 없습니다.

+++

+++SDK V4 모바일 앱에서 HTTP v1 API 마이그레이션이 지원됩니까?

아니요. 고객은 먼저 모바일 앱을 V5 SDK로 마이그레이션한 다음 위의 마이그레이션을 진행해야 합니다. Google의 알림에 따라 2024년 6월부터 푸시 서비스가 실패하기 시작하므로 우선순위로 이 작업을 수행해야 합니다.

+++

+++스테이지 인스턴스의 변경이 프로덕션 인스턴스에 영향을 줍니까?

아니요. 스테이지 모바일 앱의 변경 사항은 프로덕션 인스턴스에 영향을 주지 않습니다.

+++