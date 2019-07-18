---
title: 푸시 알림 정보
seo-title: 푸시 알림 정보
description: 푸시 알림 정보
seo-description: Adobe Campaign에서 푸시 알림 채널의 주요 특징을 살펴볼 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 961 AAEB 5-6948-4 FD 2-B 8 D 7-DE 4510 C 10566
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 채널
content-type: 참조
topic-tags: 푸시 알림
discoiquuid: 23 b 4212 e-e 878-4922-be 20-50 fb 7 fa 88 ae 8
context-tags: mobileapp, 개요
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 80e65c3fedc5452105c296144a683948daa69150

---


# About push notifications{#about-push-notifications}

>[!CAUTION]
>
>푸시 알림 구현은 전문가 사용자가 수행해야 합니다. 도움이 필요한 경우 Adobe 계정 담당자 또는 전문 서비스 파트너에 문의하십시오. 푸시 알림은 선택 기능입니다. 사용권 계약을 확인하고 계정 관리자에게 문의하여 정품 인증을 받으십시오.

Adobe Campaign를 사용하면 개인화된 푸시 알림을 iOS 및 Android 모바일 디바이스로 보낼 수 있습니다.

이러한 메시지는 Experience Cloud Mobile SDK v 4 또는 Experience Platform SDK를 활용하여 Adobe Campaign에서 설정하는 모바일 애플리케이션에서 받습니다. For more information on this, refer to [Configuring a mobile application using SDK V4](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html) and [Configuring a mobile application using Adobe Experience Platform SDKs](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html).

In Adobe Campaign, mobile profile attributes data sent from mobile device are stored in **[!UICONTROL Subscriptions to an application (appSubscriptionRcp)]** resource which allows you to define the data that you want to collect from your applications' subscribers.

모바일 장치에서 Adobe Campaign로 전송할 데이터를 수집하려면 이 리소스를 확장해야 합니다. To do so, refer to this [page](../../developing/using/extending-the-subscriptions-to-an-application-resource.md) for the detailed steps.

Adobe Campaign 에서는 두 가지 유형의 푸시 알림을 사용할 수 있습니다.

* **[!UICONTROL Alert/Message/Badge]** 유형 알림을 통해 추가 컨텐츠 (사운드, 배지, 딥 링크 등) 로 표준 텍스트 기반 메시지를 전송할 수 있습니다. that you can define in the **[!UICONTROL Advanced options]** section.

   이 알림 유형을 통해 개인화 필드를 사용할 수 있는 제목과 메시지를 추가할 수 있습니다. To be able to personalize your message, make sure you select the **[!UICONTROL Send push on profiles]** template.

* **[!UICONTROL Silent push]** 문자 알림은 최종 사용자의 메시지나 컨텐츠 없이 응용 프로그램을 자동으로 알리는 데 사용됩니다. 이러한 유형의 메시지에 대한 일반적인 사용 사례는 다운로드할 서버에서 사용할 수 있는 컨텐츠가 있음을 응용 프로그램을 인식하게 하는 것입니다.

일부 특정 구성을 설정하여 알림 동작을 정의할 수 있습니다. For more on this, refer to [this section](../../channels/using/customizing-a-push-notification.md).

As an expert user, to define these specific configurations, refer to the mobile app [technotes](https://helpx.adobe.com/campaign/kb/acs-article-list.html).

>[!NOTE]
>
>개인정보 보호에 관한 법은 국가마다 다릅니다. 일부 국가에서는 모바일 애플리케이션에서 수집한 데이터 유형을 사용자에게 알려주어야 합니다. 해당 국가의 모바일 애플리케이션과 관련된 법률을 확인하십시오. 모바일 애플리케이션에 전송된 푸시 알림이 Apple (Apple Push Notification 서비스) 및 Google (Google 클라우드 메시지 또는 Firebase 클라우드 메시지) 에 의해 지정된 전제 조건 및 조건을 준수하는지 확인합니다.

**관련 컨텐츠:**

* [푸시 알림 준비 및 전송](../../channels/using/preparing-and-sending-a-push-notification.md)
* [다국어 푸시 알림 만들기](../../channels/using/creating-a-multilingual-push-notification.md)
* [워크플로우 내에서 푸시 알림 전송](../../automating/using/push-notification-delivery.md)
* [푸시 및 인앱 FAQ](https://helpx.adobe.com/campaign/kb/push_inapp_faq.html)

## Prerequisites {#prerequisites}

>[!NOTE]
>Campaign의 푸시 알림 기능을 활용하려면 유효한 푸시 인증서를 암호 없이. pem 형식으로 제공해야 합니다.
유효한 P 12 인증서가 있는 경우 온라인 리소스를 사용하여 쉽게. pem 파일로 변환할 수 있습니다.

먼저 푸시 알림 전송을 시작하려면 SDK v 4를 사용하여 모바일 애플리케이션을 구성해야 합니다. Experience Platform SDK를 사용하여 모바일 애플리케이션을 구성할 수도 있습니다. For more on this, refer to this [page](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html).

푸시 알림을 전송하기 전에 다음을 수행해야 합니다.

1. Make sure you can access the **[!UICONTROL Mobile app]** channel in Adobe Campaign.
1. 모바일 애플리케이션 구성:

   * Adobe Campaign
   * Adobe Mobile Services 인터페이스

1. 모바일 응용 프로그램의 특정 설정을 수행합니다.

   * Adobe Mobile Services 인터페이스에서 다운로드한 구성 파일을 모바일 응용 프로그램과 패키지화합니다.
   * 모바일 애플리케이션에 Experience Cloud Mobile SDK 통합

1. 애플리케이션 구독자로부터 수집할 데이터를 정의합니다. Adobe Campaign 데이터베이스에 프로필이 있는 모바일 응용 프로그램 구독자는 정의한 기준을 기반으로 조정됩니다.

모바일 애플리케이션을 구성한 후 이제 인앱 메시지를 준비하고 전송할 수 있습니다. For more on this, refer to [Preparing and sending a push notification](../../channels/using/preparing-and-sending-a-push-notification.md).
