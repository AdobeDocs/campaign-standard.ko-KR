---
title: 푸시 알림 기본 정보
description: Adobe Campaign 푸시 알림 채널의 주요 특성을 알아봅니다.
audience: channels
content-type: reference
topic-tags: push-notifications
context-tags: mobileApp,overview
feature: Push
role: User
level: Intermediate
exl-id: e61daed6-a0ec-49d8-b1ad-77590fafb496
source-git-commit: 597ece8d833a216f0540f801461b08fdc9865024
workflow-type: tm+mt
source-wordcount: '1239'
ht-degree: 40%

---

# 푸시 알림 기본 정보{#about-push-notifications}

>[!CAUTION]
>
>푸시 알림 구현은 전문가 사용자가 수행해야 합니다. 도움이 필요한 경우 Adobe 계정 담당자 또는 전문 서비스 파트너에게 문의하십시오. 푸시 알림은 선택 기능입니다. 라이선스 계약을 확인하고 계정 관리자에게 문의하여 기능을 활성화하십시오.

Adobe Campaign을 통해 개인화 및 세그먼트화한 푸시 알림을 iOS 및 Android 모바일 디바이스로 전송할 수 있습니다.

이 메시지는 Adobe Campaign에서 Experience Platform SDK를 활용하여 설정한 모바일 애플리케이션을 통해 수신됩니다. 자세한 내용은 [Adobe Experience Platform SDK를 사용하여 모바일 애플리케이션 구성](../../administration/using/configuring-a-mobile-application.md)을 참조하십시오.

모바일 디바이스에서 전송한 모바일 프로필 속성 데이터는 Adobe Campaign의 **[!UICONTROL Subscriptions to an application (appSubscriptionRcp)]** 리소스에 저장됩니다. 이를 통해 애플리케이션 구독자로부터 수집하려는 데이터를 정의할 수 있습니다.

모바일 디바이스에서 Adobe Campaign으로 전송하려는 데이터를 수집하려면 이 리소스를 확장해야 합니다. 자세한 단계는 이 [페이지](../../developing/using/extending-the-subscriptions-to-an-application-resource.md)를 참조하십시오.

Adobe Campaign에서는 두 가지 유형의 푸시 알림을 사용할 수 있습니다.

* **[!UICONTROL Alert/Message/Badge]** 유형 알림을 사용하면 표준 텍스트 기반 메시지에 콘텐츠(사운드, 배지, 딥링크 등)를 추가하여 보낼 수 있습니다. 추가 콘텐츠는 **[!UICONTROL Advanced options]** 섹션에서 정의할 수 있습니다.

   이 알림 유형을 사용하면 제목과 메시지를 추가하여 개인화 필드를 사용할 수 있습니다. 메시지를 개인화하려면 **[!UICONTROL Send push on profiles]** 템플릿을 선택해야 합니다.

* **[!UICONTROL Silent push]** 유형 알림은 최종 사용자를 위한 메시지나 콘텐츠 없이 애플리케이션에 조용히 알림을 보내는 데 사용됩니다. 이 유형의 메시지는 보통 서버에 다운로드할 콘텐츠가 있음을 애플리케이션에 알리는 데 사용됩니다.

몇 가지 특정한 구성을 설정하여 알림 동작을 정의할 수 있습니다. 자세한 정보는 [이 섹션](../../channels/using/customizing-a-push-notification.md)을 참조하십시오.

>[!NOTE]
>
>개인 정보 보호에 관한 법은 국가마다 다릅니다. 일부 국가에서는 모바일 애플리케이션에서 수집하는 데이터의 유형을 사용자에게 고지하도록 요구합니다. 해당 국가의 모바일 애플리케이션 관련 법규를 확인하십시오. 모바일 애플리케이션에 전송되는 푸시 알림이 Apple(Apple Push Notification Service) 및 Google(Google Cloud Messaging 또는 Firebase Cloud Messaging)에서 지정한 사전 요구 사항 및 조건을 준수하는지 확인합니다.

**관련 콘텐츠:**

* [푸시 알림 준비 및 보내기](../../channels/using/preparing-and-sending-a-push-notification.md)
* [다국어 푸시 알림 만들기](../../channels/using/creating-a-multilingual-push-notification.md)
* [푸시 알림 보고서](../../reporting/using/push-notification-report.md)
* [Campaign Standard Mobile 안내서](../../channels/using/get-started-communication-channels.md)

## 전제 조건 {#prerequisites}

>[!NOTE]
>Campaign의 푸시 알림 기능을 활용하려면 암호가 없는 .pem 포맷의 유효한 푸시 인증서를 제공해야 합니다.
>
>유효한 p12 인증서가 있는 경우 온라인 리소스를 사용하여 .pem 파일로 손쉽게 변환할 수 있습니다.

푸시 알림을 전송하기 전에 다음을 수행해야 합니다.

1. Adobe Campaign에서 **[!UICONTROL Push notification]** 채널에 액세스할 수 있는지 확인합니다. 이 채널에 액세스할 수 없는 경우 계정 팀에 문의하십시오.

1. 사용자에게 Adobe Campaign Standard에서 필요한 권한이 있는지, Adobe Experience Platform의 태그가 있는지 확인합니다.

1. 데이터 수집 UI에서 모바일 속성을 만듭니다. 자세한 내용은 [모바일 속성 설정](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/)을 참조하십시오.

1. 데이터 수집 UI에서 를 설치합니다. **[!UICONTROL Adobe Campaign Standard]** 확장명.

1. Adobe Campaign Standard에서 데이터 수집 UI에서 만든 모바일 속성을 구성합니다. 자세한 내용은 [Adobe Campaign에서 태그 애플리케이션 설정](../../administration/using/configuring-a-mobile-application.md#set-up-campaign).

1. 모바일 애플리케이션 설정에 채널별 구성을 추가합니다. 자세한 내용은 [Adobe Campaign의 채널별 애플리케이션 구성](../../administration/using/configuring-a-mobile-application.md#channel-specific-config)을 참조하십시오.

1. 모바일 사용 사례 구현을 지원하려면 의 확장, 태그 규칙 및 SDK 구현에 대한 자세한 지침을 참조하십시오. [Adobe Experience Platform SDK를 사용하여 Adobe Campaign Standard에서 지원하는 모바일 사용 사례](../../administration/using/configuring-rules-launch.md).

## 푸시 알림 FAQ {#push-faq}

### 푸시 채널에 대해 자세히 알아볼 수 있는 유용한 리소스 권장 사항은 무엇입니까? {#resource-push}

아래 리소스를 확인하십시오.

* [비디오 튜토리얼](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/communication-channels/mobile/push/creating-a-push-notification.html)
* [제품 설명서](../../channels/using/about-push-notifications.md)
* AEP SDK를 사용한 구성 [설명서](../../administration/using/configuring-a-mobile-application.md)
* [커뮤니티 페이지](https://experienceleaguecommunities.adobe.com/t5/adobe-campaign-standard/ct-p/adobe-campaign-standard-community)

### Campaign에서 푸시 토큰을 얻으려면 어떻게 해야 합니까? {#push-token-acquisition}

프로비저닝 팀이 Adobe Campaign Standard에서 푸시 채널 프로비저닝을 완료했는지 확인합니다. SDK에서 setPushIdentifier API를 구현합니다. 자세한 정보는 이 [페이지](https://developer.adobe.com/client-sdks/documentation/adobe-campaign-standard/#set-up-push-messaging)를 참조하십시오.

### Campaign에 푸시 토큰과 ECID가 있으면 푸시 알림을 보내는 데 필요한 그 밖의 사항은 무엇입니까? {#sending-push}

푸시 알림을 전송하려면 고객이 .pem 포맷의 유효한 푸시 인증서를 제공해야 합니다. 이 인증서에는 암호가 필요하지 않습니다.

### .pem 인증서 대신 .p12 인증서가 있는 경우 어떻게 합니까? {#certificates}

터미널에서 아래 명령을 실행하여 .p12 인증서를 .pem 인증서로 변환할 수 있습니다. 전환 지침에 사용할 수 있는 몇 가지 온라인 리소스도 있습니다.

```
openssl pkcs12 -in pushcert.p12 -out pushcert.pem -nodes -clcerts
```

### 인증서 업로드가 성공했는지 어떻게 알 수 있습니까? {#certificate-upload}

다음 메시지가 표시됩니다.

![](assets/faq_2.png)

### iOS 앱(Android의 경우 N/A)에 대해 프로덕션 인증서와 샌드박스 인증서를 동시에 업로드할 수 있습니까? {#prod-sandbox-certificate}

아니요. 앱은 샌드박스 또는 프로덕션 모드에서 작동하며 설정된 경우 다른 모드(즉, 샌드박스에서 프로덕션 앱으로)로 변경할 수 없습니다. 먼저 샌드박스 모드에서 앱을 테스트한 다음 프로덕션 모드로 전환하는 것이 좋습니다.

프로덕션 모드로 변경하려면 다른 앱을 만들어야 합니다. 또한 샌드박스 확인란을 선택하지 않고 프로덕션 인증서를 업로드해야 합니다.

### iOS 및 Android 자격 증명을 동시에 업로드할 수 있습니까? {#ios-android-credentials}

예. Campaign은 두 플랫폼을 동시에 지원하며 두 플랫폼 모두에 대한 자격 증명을 업로드할 수 있습니다.

### 푸시 인증서를 성공적으로 업로드했지만 푸시 메시지가 전송되지 않습니다. {#push-certificates-upload}

푸시 인증서를 테스트하여 인증서가 유효한지 확인하십시오 [여기](https://pushtry.com/).

### pushtry.com에서 푸시 알림을 정상적으로 전송할 수 있지만 Campaign을 통해서는 전송할 수 없습니다. {#push-not-sending}

제공된 푸시 페이로드 지침을 따르고 있는지 확인하십시오. [여기](../../administration/using/push-payload.md).

Android의 경우 Campaign은 알림 페이로드가 아닌 데이터 페이로드만 지원합니다

### Adobe Campaign Standard의 관리 섹션에서 앱을 구성했지만 모바일 앱을 게재 속성에서 사용할 수 없습니다. {#mobile-app-unavailable}

배달 속성에서 사용하려면 앱에 유효한 푸시 인증서가 업로드되어 있어야 합니다.

### 이 페이지의 모든 지침을 시도했지만 Campaign에서 푸시를 보낼 수 없습니다. {#push-troubleshoot}

고객 지원 티켓을 여십시오.

### Campaign에서 푸시 알림을 받고 있지만 미디어 파일이 표시되지 않습니다.{#media-file-unavailable}

모바일 앱 개발자는 앱에서 미디어 파일에 대한 지원을 처리해야 합니다. 경우에 따라 네트워크 대역폭으로 인해 미디어 파일이 렌더링되지 않을 수 있습니다. 다음을 참조하십시오. [페이지](../../administration/using/image-push-notification.md) 추가 포인터에 대해 설명합니다.

### Campaign에서 푸시 보고를 활성화하려면 어떻게 해야 합니까? {#push-reporting-enable}

아래의 단계를 수행하십시오.

* 푸시 추적 포스트백을 구성합니다. 지침을 찾을 수 있음 [여기](../../administration/using/configuring-a-mobile-application.md).
* Mobile Core에서 trackAction API를 구현합니다. 다음을 참조하십시오. [페이지](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/) 추가 정보.

보다 자세한 지침은 여기에서 확인할 수 있습니다. [페이지](../../administration/using/push-tracking.md).

### 푸시 채널에 사용할 수 있는 보고서 {#push-report-available}

푸시 채널용 Adobe Campaign에서 기본 보고서를 사용할 수 있습니다. 다음을 참조하십시오. [설명서](../../reporting/using/push-notification-report.md).

이 항목 보기 [페이지](../../reporting/using/indicator-calculation.md#push-notification-delivery) 각 푸시 지표를 계산하는 방법을 이해할 수 있습니다.

### 푸시 및 인앱 메시지에서 딥링크가 지원됩니까? {#deeplink-push}

예. 딥링크는 푸시 메시지에서 지원됩니다. 딥링크는 다음을 포함해야 합니다.

* 딥링크가 작동하려면 게재 추적을 비활성화해야 한다는 언어입니다.
* 딥링크 추적을 수행할 수 있는 파트너로서 Branch와 함께 Appsflyer를 제공합니다. 분기 및 Adobe Campaign Standard 통합에 대한 자세한 내용은 다음을 참조하십시오. [페이지](https://help.branch.io/using-branch/docs/adobe-campaign-standard-1).
