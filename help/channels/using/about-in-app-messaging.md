---
title: 인앱 메시지 기본 정보
description: 인앱 메시징을 사용하여 모바일 애플리케이션 내에서 메시지 또는 경고를 표시합니다.
page-status-flag: never-activated
uuid: 6784cdfc-6db9-41dd-9fbb-2e756a5bcb5f
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: in-app-messaging
discoiquuid: a4168cfb-22bf-4ab3-b9d8-6e76e1bdc055
context-tags: delivery,triggers,back
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 501ba6f97a86076116d4d84f43df674536e12f6a

---


# 인앱 메시지 기본 정보{#about-in-app-messaging}

인앱 메시지는 사용자가 모바일 애플리케이션 내에서 활성 상태일 때 메시지를 표시할 수 있는 메시지 채널입니다. 이 메시지 유형은 사용자의 전화의 알림 센터로 전달되는 푸시 알림에 대해 무료로 사용할 수 있습니다. 푸시 알림 채널에 대한 자세한 내용은 이 [섹션을](../../channels/using/about-push-notifications.md)참조하십시오.

이 채널을 이용하려면 모바일 애플리케이션을 Adobe Experience Platform SDK와 통합해야 합니다. 이러한 앱은 인앱 전달을 위해 Adobe Campaign에서 사용할 수 있으려면 먼저 Adobe Experience Platform Launch에서 활성화해야 합니다.

![](assets/launch_campaign.png)

Experience Platform SDK를 활용하는 모바일 애플리케이션에서 인앱 메시지를 전송하려면 다음 사전 요구 사항을 충족해야 합니다.

1. Adobe Campaign에서 채널에 액세스할 수 있는지 확인합니다. **[!UICONTROL In-App]**이러한 채널에 액세스할 수 없는 경우 계정 팀에 문의하십시오.

1. Adobe Campaign Standard에서 Experience Cloud SDK 애플리케이션을 사용하여 모바일 사용 사례를 활용하려면 Adobe Experience Platform Launch에서 모바일 앱을 제작하고 Adobe Campaign Standard에서 구성해야 합니다. 단계별 안내서는 이 [페이지를](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html)참조하십시오.

1. 구성된 후에는 이제 인앱 메시지를 준비할 수 있습니다. 자세한 내용은 이 [페이지를](../../channels/using/preparing-and-sending-an-in-app-message.md#preparing-your-in-app-message)참조하십시오.

1. 그런 다음 인앱 메시지 [또는](../../channels/using/customizing-an-in-app-message.md) 로컬 알림 메시지 유형 [사용자 지정을](../../channels/using/customizing-an-in-app-message.md#customizing-a-local-notification-message-type)전송하기로 결정할 수 있습니다.

1. 이제 배달을 보낼 준비가 되었습니다. 자세한 내용은 이 [페이지를](../../channels/using/preparing-and-sending-an-in-app-message.md#sending-your-in-app-message)참조하십시오.

**관련 컨텐츠:**

* [인앱 보고서](../../reporting/using/in-app-report.md)
* [푸시 및 인앱 FAQ](https://helpx.adobe.com/campaign/kb/push_inapp_faq.html)
* [Adobe Campaign Standard에서 지원되는 모바일 사용 사례](https://helpx.adobe.com/campaign/kb/configure-launch-rules-acs-use-cases.html)
* [Campaign Standard 모바일 안내서](https://helpx.adobe.com/campaign/kb/acs-mobile.html)
