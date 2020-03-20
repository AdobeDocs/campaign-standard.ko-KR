---
title: 푸시 알림 기본 정보
description: Adobe Campaign에서 푸시 알림 채널의 주요 특성을 살펴볼 수 있습니다.
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
source-git-commit: 5ed46987a3778dfa100639de8be9b6d5ac5348b4

---


# 푸시 알림 기본 정보{#about-push-notifications}

>[!CAUTION]
>
>푸시 알림 구현은 전문가 사용자가 수행해야 합니다. 도움이 필요한 경우 Adobe 계정 담당자 또는 Professional 서비스 파트너에게 문의하십시오. 푸시 알림은 선택 기능입니다. 라이선스 계약서를 확인하고 계정 담당자에게 문의하여 활성화하십시오.

Adobe Campaign을 사용하면 개인화된 푸시 알림을 iOS 및 Android 모바일 디바이스에 전송할 수 있습니다.

이러한 메시지는 Experience Platform SDK를 활용하여 Adobe Campaign에서 설정한 모바일 애플리케이션에서 수신됩니다. 자세한 내용은 Adobe Experience [Platform SDK를 사용하여 모바일 애플리케이션 구성을 참조하십시오](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html).

In Adobe Campaign, mobile profile attributes data sent from mobile device are stored in **[!UICONTROL Subscriptions to an application (appSubscriptionRcp)]** resource which allows you to define the data that you want to collect from your applications&#39; subscribers.

모바일 장치에서 Adobe Campaign으로 전송하려는 데이터를 수집하려면 이 리소스를 확장해야 합니다. 이렇게 하려면 이 [페이지를](../../developing/using/extending-the-subscriptions-to-an-application-resource.md) 참조하십시오.

Adobe Campaign에서는 두 가지 유형의 푸시 알림을 사용할 수 있습니다.

* **[!UICONTROL Alert/Message/Badge]** 문자 알림을 사용하면 추가 컨텐츠(사운드, 배지, 디플링크 등)를 사용하여 표준 텍스트 기반 메시지를 전송할 수 있습니다. 섹션에서 정의할 수 **[!UICONTROL Advanced options]** 있습니다.

   이 알림 유형을 사용하면 개인화 필드를 사용할 수 있는 제목과 메시지를 추가할 수 있습니다. 메시지를 개인화할 수 있으려면 **[!UICONTROL Send push on profiles]** 템플릿을 선택해야 합니다.

* **[!UICONTROL Silent push]** 문자 알림은 최종 사용자에 대한 메시지나 내용 없이 응용 프로그램에 자동으로 알리는 데 사용됩니다. 이러한 유형의 메시지의 일반적인 사용 사례는 응용 프로그램에서 다운로드할 서버에 사용 가능한 컨텐츠가 있음을 인식하도록 하는 것입니다.

일부 특정 구성은 알림 동작을 정의하도록 설정할 수 있습니다. For more on this, refer to [this section](../../channels/using/customizing-a-push-notification.md).

전문 사용자는 이러한 특정 구성을 정의하려면 모바일 앱 [기술 정보를 참조하십시오](https://helpx.adobe.com/campaign/kb/acs-article-list.html).

>[!NOTE]
>
>개인정보 보호에 관한 법은 국가마다 다릅니다. 일부 국가에서는 모바일 애플리케이션에서 수집한 데이터 유형을 사용자에게 알려주어야 합니다. 해당 국가의 모바일 애플리케이션과 관련된 법을 확인하십시오. 모바일 응용 프로그램에 전송된 푸시 알림은 Apple(Apple Push Notification 서비스) 및 Google(Google Cloud Messaging 또는 Firebase Cloud Messaging)에서 지정한 사전 요구 사항 및 조건을 준수합니다.

**관련 컨텐츠:**

* [푸시 알림 준비 및 보내기](../../channels/using/preparing-and-sending-a-push-notification.md)
* [다국어 푸시 알림 만들기](../../channels/using/creating-a-multilingual-push-notification.md)
* [푸시 알림 보고서](../../reporting/using/push-notification-report.md)
* [Campaign Standard 모바일 안내서](https://helpx.adobe.com/campaign/kb/acs-mobile.html)

## 사전 요구 사항 {#prerequisites}

>[!NOTE]
>Campaign의 푸시 알림 기능을 활용하려면 암호가 없는 .pem 형식의 유효한 푸시 인증서를 제공해야 합니다.
유효한 p12 인증서가 있는 경우 온라인 리소스를 사용하여 .pem 파일로 손쉽게 변환할 수 있습니다.

먼저 푸시 알림 전송을 시작하려면 Experience Platform SDK를 사용하여 모바일 애플리케이션을 구성해야 합니다. 자세한 내용은 이 [페이지를](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html)참조하십시오.

푸시 알림을 전송하기 전에 다음을 수행해야 합니다.

1. Adobe Campaign에서 **[!UICONTROL Mobile app]** 채널에 액세스할 수 있는지 확인하십시오.
1. 모바일 응용 프로그램을 구성하는 방법:

   * Adobe Campaign
   * Adobe Mobile Services 인터페이스

1. 모바일 응용 프로그램의 특정 설정을 수행합니다.

   * Adobe Mobile Services 인터페이스에서 다운로드한 구성 파일을 모바일 응용 프로그램과 함께 패키징합니다.
   * Experience Cloud Mobile SDK를 모바일 애플리케이션에 통합합니다.

1. 애플리케이션의 가입자로부터 수집할 데이터를 정의합니다. Adobe Campaign 데이터베이스에 프로필이 있는 모바일 응용 프로그램의 구독자는 정의한 기준에 따라 조정됩니다.

모바일 애플리케이션을 구성한 후 이제 인앱 메시지 준비 및 전송을 시작할 수 있습니다. 자세한 내용은 푸시 알림 [준비 및 전송을 참조하십시오](../../channels/using/preparing-and-sending-a-push-notification.md).
