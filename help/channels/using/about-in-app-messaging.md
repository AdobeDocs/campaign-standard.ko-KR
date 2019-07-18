---
title: 인앱 메시지 정보
seo-title: 인앱 메시지 정보
description: 인앱 메시지 정보
seo-description: 인앱 메시지로 모바일 애플리케이션 내에서 메시지 또는 경고를 표시합니다.
page-status-flag: 정품 인증 안 함
uuid: 6784 cdfc -6 db 9-41 dd -9 fbb -2 e 756 a 5 bcb 5 f
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 채널
content-type: 참조
topic-tags: in-app-messaging
discoiquuid: a 4168 cfb -22 bf -4 ab 3-b 9 d 8-6 e 76 e 1 bdc 055
context-tags: 전달, 트리거, 뒤로
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 90b478d1d58b67e763b8b6685c12530a5b5ee9c3

---


# About In-App messaging{#about-in-app-messaging}

인앱 메시지는 사용자가 모바일 애플리케이션 내에서 활성 상태일 때 메시지를 표시할 수 있도록 해주는 메시징 채널입니다. 이 메시지 유형은 푸시 알림에 무료이며 사용자의 전화 알림 센터로 전달됩니다. For more information on the push notification channel, refer to this [section](../../channels/using/about-push-notifications.md).

이 채널을 사용하려면 모바일 애플리케이션이 Adobe Experience Platform SDK와 통합되어야 합니다. 이러한 앱은 Adobe Experience Platform Launch에서 활성화해야 인앱 전달을 위한 Adobe Campaign에서 사용할 수 있습니다.

![](assets/launch_campaign.png)

Experience Platform SDK를 활용하는 모바일 애플리케이션에서 인앱 메시지를 전송하려면 다음 전제 조건을 충족해야 합니다.

1. In Adobe Campaign, make sure you can access the **[!UICONTROL In-App]** channel. 이러한 채널에 액세스할 수 없는 경우 계정 팀에 문의하십시오.
1. Experience Platform Launch에서 모바일 속성을 만들어 모바일 애플리케이션을 제작하고 Experience Platform SDK를 사용하여 모바일 앱을 제작할 수 있습니다.

   For more information, refer to the [Set up a mobile property](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property) section in Adobe Launch documentation.

1. In Experience Platform Launch, install the **[!UICONTROL Adobe Campaign Standard]** extension for your mobile application in Experience Platform Launch:

   For more on extensions, refer to the [Configure Campaign Standard Extension in Experience Platform Launch](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard) in Experience Platform Launch documentation.

1. In Experience Platform Launch, configure rules and data elements for your application, see [Configuring your application in Experience Platform Launch](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html#ConfiguringyourapplicationinLaunch)
1. Configure your Experience Platform Launch application in Adobe Campaign Standard, see [Setting up your Experience Platform Launch application in Adobe Campaign](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html#SettingupyourAdobeLaunchapplicationinAdobeCampaign) .

To learn how to configure Experience Platform SDKs, refer to this [page](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html).

**관련 컨텐츠:**

* [인앱 메시지 준비 및 보내기](../../channels/using/preparing-and-sending-an-in-app-message.md)
* [인앱 메시지 사용자 정의](../../channels/using/customizing-an-in-app-message.md)
* [로컬 알림 메시지 유형 사용자 지정](../../channels/using/customizing-an-in-app-message.md#customizing-a-local-notification-message-type)
* [워크플로우 내에서 인앱 메시지 전송](../../automating/using/in-app-delivery.md)
* [푸시 및 인앱 FAQ](https://helpx.adobe.com/campaign/kb/push_inapp_faq.html)