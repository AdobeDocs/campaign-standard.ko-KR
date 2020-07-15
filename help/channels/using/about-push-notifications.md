---
title: 푸시 알림 기본 정보
description: Adobe Campaign에서 푸시 알림 채널의 주요 특성을 알아봅니다.
page-status-flag: never-activated
uuid: 961aaeb5-6948-4fd2-b8d7-de4510c10566
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: push-notifications
discoiquuid: 23b4212e-e878-4922-be20-50fb7fa88ae8
context-tags: mobileApp,overview
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: f9632e88b49c2280c76e709376cfb7a7a27abc1f
workflow-type: tm+mt
source-wordcount: '1280'
ht-degree: 2%

---


# 푸시 알림 기본 정보{#about-push-notifications}

>[!CAUTION]
>
>푸시 알림 구현은 전문가 사용자가 수행해야 합니다. 도움이 필요한 경우 Adobe 계정 담당자 또는 Professional 서비스 파트너에게 문의하십시오. 푸시 알림은 선택 기능입니다. 라이선스 계약을 확인하고 계정 관리자에게 문의하여 정품 인증을 받으십시오.

Adobe Campaign을 사용하면 개인화된 푸시 알림을 iOS 및 Android 모바일 디바이스로 전송할 수 있습니다.

이러한 메시지는 Experience Platform SDK를 활용하여 Adobe Campaign에서 설정한 모바일 애플리케이션에서 수신됩니다. 자세한 내용은 Adobe Experience Platform SDK를 [사용하여 모바일 애플리케이션 구성을 참조하십시오](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html).

In Adobe Campaign, mobile profile attributes data sent from mobile device are stored in **[!UICONTROL Subscriptions to an application (appSubscriptionRcp)]** resource which allows you to define the data that you want to collect from your applications&#39; subscribers.

모바일 장치에서 Adobe Campaign으로 전송할 데이터를 수집하려면 이 리소스를 확장해야 합니다. 이렇게 하려면 이 [페이지를](../../developing/using/extending-the-subscriptions-to-an-application-resource.md) 참조하십시오.

두 가지 유형의 푸시 알림을 Adobe Campaign에서 사용할 수 있습니다.

* **[!UICONTROL Alert/Message/Badge]** 문자 알림을 사용하면 추가 컨텐츠(사운드, 배지, 디플링크 등)를 사용하여 표준 텍스트 기반 메시지를 보낼 수 있습니다. 섹션에서 정의할 수 **[!UICONTROL Advanced options]** 있습니다.

   이 알림 유형을 사용하면 개인화 필드를 사용할 수 있는 제목과 메시지를 추가할 수 있습니다. 메시지를 개인화할 수 있으려면 **[!UICONTROL Send push on profiles]** 템플릿을 선택해야 합니다.

* **[!UICONTROL Silent push]** 문자 알림은 최종 사용자에 대한 메시지나 내용 없이 응용 프로그램을 자동으로 알리는 데 사용됩니다. 이러한 유형의 메시지의 일반적인 사용 사례는 응용 프로그램에서 다운로드할 서버에서 사용 가능한 컨텐츠가 있음을 인식하도록 하는 것입니다.

일부 특정 구성은 알림 동작을 정의하도록 설정할 수 있습니다. 이 작업에 대한 자세한 정보는 [이 섹션](../../channels/using/customizing-a-push-notification.md)을 참조하십시오.

전문가 사용자는 이러한 특정 구성을 정의하려면 모바일 앱 [기술 정보를 참조하십시오](https://helpx.adobe.com/kr/campaign/kb/acs-article-list.html).

>[!NOTE]
>
>개인정보 보호에 관한 법은 국가마다 다르다. 일부 국가에서는 모바일 애플리케이션에서 수집한 데이터 유형을 사용자에게 알려주어야 합니다. 해당 국가의 모바일 애플리케이션과 관련된 법을 확인하십시오. 모바일 응용 프로그램에 전송된 푸시 알림은 Apple(Apple Push Notification 서비스) 및 Google(Google Cloud Messaging 또는 Firebase Cloud Messaging)에서 지정한 사전 요구 사항 및 조건을 준수합니다.

**관련 컨텐츠:**

* [푸시 알림 준비 및 보내기](../../channels/using/preparing-and-sending-a-push-notification.md)
* [다국어 푸시 알림 만들기](../../channels/using/creating-a-multilingual-push-notification.md)
* [푸시 알림 보고서](../../reporting/using/push-notification-report.md)
* [Campaign Standard 모바일 안내서](https://helpx.adobe.com/kr/campaign/kb/acs-mobile.html)

## 사전 요구 사항 {#prerequisites}

>[!NOTE]
>Campaign의 푸시 알림 기능을 활용하려면 암호가 없는 .pem 형식의 유효한 푸시 인증서를 제공해야 합니다.
유효한 p12 인증서가 있는 경우 온라인 리소스를 사용하여 .pem 파일로 손쉽게 변환할 수 있습니다.

푸시 알림을 전송하기 전에 다음을 수행해야 합니다.

1. Adobe Campaign에서 채널에 액세스할 수 있는지 **[!UICONTROL Push notification]** 확인합니다. 이러한 채널에 액세스할 수 없는 경우 계정 팀에 문의하십시오.

1. Adobe Campaign Standard 및 Experience Platform Launch에서 필요한 권한이 있는지 확인합니다.

1. Experience Platform Launch에서 모바일 속성을 만듭니다. 자세한 내용은 [모바일 속성 설정을 참조하십시오](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property).

1. Experience Platform Launch에서 익스텐션을 **[!UICONTROL Adobe Campaign Standard]** 설치합니다.

1. Adobe Campaign Standard에서 Experience Platform Launch에서 만든 모바일 속성을 구성합니다. 자세한 내용은 Adobe Campaign [에서 Experience Platform Launch 응용 프로그램 설정을 참조하십시오](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html#SettingupyourAdobeExperiencePlatformLaunchapplicationinAdobeCampaign).

1. 모바일 애플리케이션 설정에 채널별 구성을 추가합니다. 자세한 내용은 Adobe Campaign의 [채널별 애플리케이션 구성을 참조하십시오](../../administration/using/configuring-a-mobile-application.md#channel-specific-config).

1. 모바일 사용 사례 구현을 지원하려면 Adobe Campaign Standard SDK를 사용하여 Adobe Experience Platform에서 지원되는 [Mobile 사용 사례에서의 확장, Experience Platform Launch 규칙 및 SDK 구현에 대한 자세한 지침을 참조하십시오](https://helpx.adobe.com/campaign/kb/configure-launch-rules-acs-use-cases.html).

## 푸시 알림 FAQ {#push-faq}

### 푸시 채널에 대해 자세히 알아보려면 유용한 리소스 권장 사항은 무엇입니까? {#resource-push}

아래 리소스를 확인하십시오.

* [비디오 자습서](https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/communication-channels/mobile/push/creating-a-push-notification.html)
* [제품 설명서](../../channels/using/about-push-notifications.md)
* AEP SDK [설명서를 사용하여 구성](../../administration/using/configuring-a-mobile-application.md)
* [커뮤니티 페이지](https://experienceleaguecommunities.adobe.com/t5/adobe-campaign-standard/ct-p/adobe-campaign-standard-community)

### Campaign에서 푸시 토큰을 획득하려면 어떻게 해야 합니까? {#push-token-acquisition}

프로비저닝 팀이 Adobe Campaign Standard에서 푸시 채널 프로비전을 완료했는지 확인하십시오. SDK에서 setPushIdentifier API를 구현합니다. For more on this, refer to this [page](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard#set-up-push-messaging).

### Campaign에 푸시 토큰 및 ECID가 있는 경우 푸시 알림을 전송해야 하는 또 다른 방법은 무엇입니까? {#sending-push}

고객은 푸시 알림을 전송하려면 유효한 푸시 인증서를 .pem 형식으로 제공해야 합니다. 이 인증서에 대한 암호가 필요하지 않습니다.

### .pem 인증서 대신 .p12 인증서가 있으면 어떻게 됩니까? {#certificates}

터미널에서 아래 명령을 실행하여 .p12 인증서를 .pem 인증서로 변환할 수 있습니다. 전환 지침에는 몇 가지 온라인 리소스도 있습니다.

```
openssl pkcs12 -in pushcert.p12 -out pushcert.pem -nodes -clcerts
```

### 인증서 업로드가 성공했는지 어떻게 알 수 있습니까? {#certificate-upload}

다음 메시지가 표시됩니다.

![](assets/faq_2.png)

### iOS 앱(Android용 N/A)에 대해 프로덕션 및 샌드박스 인증서를 동시에 업로드할 수 있습니까? {#prod-sandbox-certificate}

아니요. 앱은 샌드박스 또는 프로덕션 모드에서 작동하며 설정되면 다른(즉, 샌드박스와 프로덕션 앱)으로 변경할 수 없습니다. 먼저 샌드박스 모드에서 앱을 테스트한 다음 프로덕션 모드로 전환하는 것이 좋습니다.

프로덕션 모드로 변경하려면 다른 앱을 만들어야 합니다. 또한 샌드박스 확인란을 선택하지 않고 프로덕션 인증서를 업로드하지 마십시오.

### iOS와 Android 자격 증명을 동시에 업로드할 수 있습니까? {#ios-android-credentials}

예. Campaign은 두 플랫폼을 동시에 지원하므로 두 플랫폼 모두에 대한 자격 증명을 업로드할 수 있습니다.

### 푸시 인증서를 업로드했지만 푸시 메시지가 전송되지 않았습니다. {#push-certificates-upload}

푸시 인증서가 [여기에서](https://pushtry.com/)테스트되어 유효한지 확인하십시오.

### 푸시 알림을 pushtry.com에서 성공적으로 보낼 수는 있지만 Campaign을 통해 보낼 수는 없습니다. {#push-not-sending}

여기에 제공된 푸시 페이로드 지침을 따르고 있는지 [확인하십시오](../../administration/using/push-payload.md).

Android의 경우 Campaign은 알림 페이로드가 아닌 데이터 페이로드만 지원합니다

### Adobe Campaign Standard의 관리 섹션에 앱을 구성했지만 배포 속성에서 모바일 앱을 사용할 수 없습니다. {#mobile-app-unavailable}

앱이 배달 속성에서 사용할 수 있으려면 먼저 유효한 푸시 인증서가 업로드되어야 합니다.

### 이 페이지의 모든 지침을 시도했지만 Campaign에서 푸시를 보낼 수 없습니다. {#push-troubleshoot}

고객 관리 티켓을 열어주세요

### 푸시 알림이 Campaign에서 배달되지만 미디어 파일이 표시되지 않습니다.{#media-file-unavailable}

모바일 앱 개발자는 앱에서 미디어 파일에 대한 지원을 처리해야 합니다. 경우에 따라 네트워크 대역폭이 미디어 파일이 렌더링되지 않을 수 있습니다. 추가 포인터는 이 [페이지를](../../administration/using/image-push-notification.md) 참조하십시오.

### 캠페인에서 푸시 보고를 활성화하려면 어떻게 해야 합니까? {#push-reporting-enable}

아래 단계를 따르십시오.

* 푸시 추적 포스트백을 구성합니다. 지침은 [여기에서 확인할 수 있습니다](../../administration/using/configuring-a-mobile-application.md).
* Mobile Core에서 trackAction API를 구현합니다. 자세한 내용은 이 [페이지를](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/mobile-core-api-reference) 참조하십시오.

자세한 지침은 이 [페이지에서 확인할 수 있습니다](../../administration/using/push-tracking.md).

### 푸시 채널에 사용할 수 있는 보고서는 무엇입니까? {#push-report-available}

기본 보고서는 푸시 채널에 대해 Adobe Campaign에서 사용할 수 있습니다. 이 [설명서를 참조하십시오](../../reporting/using/push-notification-report.md).

각 푸시 지표가 계산되는 방법을 이해하려면 이 [페이지를](../../reporting/using/indicator-calculation.md#push-notification-delivery) 참조하십시오.

### 푸시 및 인앱 메시지에서는 링크가 지원됩니까? {#deeplink-push}

예. 푸시 메시지는 기본 링크를 지원합니다. 링크는 다음을 포함해야 합니다.

* 배달 추적이 제대로 작동하도록 하기 위해 배달 추적을 비활성화해야 한다고 말하는 언어입니다.
* 링크 추적을 수행할 수 있는 파트너로 분기를 추가합니다. 분기 및 Adobe Campaign Standard 통합에 대한 자세한 내용은 이 [페이지를 참조하십시오](https://help.branch.io/using-branch/docs/adobe-campaign-standard-1).