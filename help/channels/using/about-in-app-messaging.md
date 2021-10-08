---
title: 인앱 메시지 기본 정보
description: 인앱 메시지를 사용하여 모바일 애플리케이션 내에 메시지 또는 경고를 표시합니다.
audience: channels
content-type: reference
topic-tags: in-app-messaging
context-tags: delivery,triggers,back
feature: In App
role: User
source-git-commit: df7fce6f2fd98688e5a1fb5bc84603e6b3df5cd4
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 100%

---

# 인앱 메시지 기본 정보{#about-in-app-messaging}

인앱 메시지는 사용자가 모바일 애플리케이션 내에서 활성 상태일 때 메시지를 표시할 수 있는 메시지 채널입니다. 이 메시지 유형은 사용자 전화의 알림 센터로 전달되는 푸시 알림과 상호 보완적으로 사용할 수 있습니다. 푸시 알림 채널에 대한 자세한 내용은 이 [섹션](../../channels/using/about-push-notifications.md)을 참조하십시오.

이 채널을 사용하려면 모바일 애플리케이션을 Adobe Experience Platform SDK와 통합해야 합니다. Adobe Campaign에서 인앱 게재를 사용하려면 해당 앱을 Adobe Experience Platform Launch에서 활성화해야 합니다.

![](assets/launch_campaign.png)

Experience Platform SDK를 활용하는 모바일 애플리케이션에서 인앱 메시지를 보내기에 앞서 다음 사전 요구 사항을 충족해야 합니다.

1. Adobe Campaign에서 **[!UICONTROL In-App]** 채널에 액세스할 수 있는지 확인합니다. 이 채널에 액세스할 수 없는 경우 계정 팀에 문의하십시오.

1. Adobe Campaign Standard와 Experience Cloud SDK 애플리케이션을 함께 사용하는 모바일 사용 사례를 활용하려면 Adobe Experience Platform Launch에서 모바일 앱을 제작하고 Adobe Campaign Standard에서 구성해야 합니다. 단계별 안내서는 이 [페이지](../../administration/using/configuring-a-mobile-application.md)를 참조하십시오.

1. 구성하고 나면 이제 인앱 메시지를 준비할 수 있습니다. 자세한 정보는 이 [페이지](../../channels/using/preparing-and-sending-an-in-app-message.md#preparing-your-in-app-message)를 참조하십시오.

1. 그런 다음 [인앱 메시지](../../channels/using/customizing-an-in-app-message.md)를 보낼지 [로컬 알림 메시지 유형 사용자 정의](../../channels/using/customizing-an-in-app-message.md#customizing-a-local-notification-message-type)를 보낼지 결정할 수 있습니다.

1. 이제 게재를 보낼 준비가 되었습니다. 자세한 내용은 이 [페이지](../../channels/using/preparing-and-sending-an-in-app-message.md#sending-your-in-app-message)를 참조하십시오.

**관련 컨텐츠:**

* [인앱 보고서](../../reporting/using/in-app-report.md)
* [Adobe Campaign Standard에서 지원하는 모바일 사용 사례](../../administration/using/configuring-rules-launch.md)
* [Campaign Standard Mobile 안내서](../../channels/using/get-started-communication-channels.md)

## 개인적이고 민감한 데이터를 사용하여 모바일 프로필 필드 처리 {#handling-mobile-profile-fields-with-personal-and-sensitive-data}

모바일 디바이스에서 전송한 모바일 프로필 속성 데이터는 Adobe Campaign의 **[!UICONTROL Subscriptions to an application (appSubscriptionRcp)]** 리소스에 저장됩니다. 이를 통해 애플리케이션 구독자로부터 수집하려는 데이터를 정의할 수 있습니다.

모바일 디바이스에서 Adobe Campaign으로 전송하려는 데이터를 수집하려면 이 리소스를 확장해야 합니다. 자세한 단계는 이 [페이지](../../developing/using/extending-the-subscriptions-to-an-application-resource.md)를 참조하십시오.

인앱 메시지를 보다 안전하게 개인화하려면 이 리소스의 모바일 프로필 필드를 그에 따라 구성해야 합니다. **[!UICONTROL Subscriptions to an application (appSubscriptionRcp)]**&#x200B;에서 새 모바일 프로필 필드를 만들 때 인앱 메시지 개인화 설정 중에 사용할 수 없도록 하려면 **[!UICONTROL Personal and Sensitive]**&#x200B;을(를) 선택합니다.

>[!NOTE]
>
>이 테이블에 사용자 지정 리소스 확장을 사용하는 기존 구현이 있는 경우 인앱 메시지를 개인화하기 위해 필드를 활용하기 전에 해당 필드에 적절하게 레이블을 지정하는 것이 좋습니다.

![](assets/in_app_personal_data_2.png)

**[!UICONTROL Subscriptions to an application]** 사용자 지정 리소스가 구성 및 게시되면 **[!UICONTROL Target users based on their Mobile profile (inApp)]** 템플릿을 사용하여 인앱 게재 준비를 시작할 수 있습니다. 개인화를 위해 **[!UICONTROL Subscriptions to an application (appSubscriptionRcp)]** 리소스에서 개인적이지 않고 민감하지 않은 필드만 사용할 수 있습니다. 

**개인적이고 민감한** 필드를 사용하여 개인화해야 하는 경우, 사용자의 PII 데이터를 안전하게 유지하기 위해 추가적인 보안 메커니즘이 있는 **[!UICONTROL Target users based on their Campaign profile (inAppProfile)]** 템플릿을 사용하는 것이 좋습니다.