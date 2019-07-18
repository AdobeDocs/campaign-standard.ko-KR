---
title: 트랜잭션 푸시 알림
seo-title: 트랜잭션 푸시 알림
description: 트랜잭션 푸시 알림
seo-description: 트랜잭션 푸시 알림을 만들고 게시하는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: EF 31 C 1 B 6-9 EF 8-42 E 3-B 49 D -72 F 9 EAC 8 EA 32
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 채널
content-type: 참조
topic-tags: 트랜잭션 메시징
discoiquuid: E 645 D 4 B 9-001 F -47 D 9-8 A 0 F-B 4696 C 75 C 5 D 3
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 855db33971afdf9f02bf1b00be67c9e3f50bee06

---


# Transactional push notifications{#transactional-push-notifications}

Adobe Campaign를 사용하여 iOS 및 Android 모바일 장치에서 트랜잭션 푸시 알림을 전송할 수 있습니다. 이러한 메시지는 Experience Cloud Mobile SDK를 활용하여 Adobe Campaign에서 설정하는 모바일 애플리케이션에서 받습니다.

>[!NOTE]
>
>푸시 채널은 선택 사항입니다. 사용권 계약을 확인하십시오. For more information on standard push notifications, see [Push notifications](../../channels/using/about-push-notifications.md).

다음과 같은 두 가지 유형의 트랜잭션 푸시 알림을 전송할 수 있습니다.

* 이벤트를 타깃팅하는 트랜잭션 푸시 알림.
* Adobe Campaign 데이터베이스의 트랜잭션 푸시 알림 타깃팅 프로필.

Once you have created and published an event (the cart abandonment explained in [this section](../../channels/using/about-transactional-messaging.md#transactional-messaging-operating-principle)), the corresponding transactional push notification is created automatically.

The configuration steps are presented in the [Configuring an event to send a transactional push notification](../../administration/using/configuring-transactional-messaging.md#use-case--configuring-an-event-to-send-a-transactional-message) section.

이벤트가 트랜잭션 메시지를 보내게 하려면 메시지를 개인화하고 테스트하여 게시해야 합니다.

>[!NOTE]
>
>To access the transactional messages, you must have administration rights or appear in the **[!UICONTROL Message Center agents]** (mcExec) security group.

## Transactional push notifications targeting an event {#transactional-push-notifications-targeting-an-event}

모바일 애플리케이션에서 알림을 받도록 선택한 모든 사용자에게 익명의 트랜잭션 푸시 알림을 전송할 수 있습니다.

이 경우 이벤트 자체에 포함된 데이터만 게재 대상을 정의하는 데 사용됩니다. Adobe Campaign 통합 프로필 데이터베이스의 데이터는 활용되지 않습니다.

### Sending a transactional push notification targeting an event {#sending-a-transactional-push-notification-targeting-an-----------event}

예를 들어 항공사 회사는 모바일 애플리케이션 사용자를 초청하여 관련 게이트를 개설해야 합니다.

회사는 하나의 모바일 애플리케이션을 사용하여 한 개의 단일 장치를 통해 사용자 (등록 토큰으로 식별) 당 한 개의 트랜잭션 푸시 알림을 전송합니다.

1. 편집할 수 있도록 만들어진 트랜잭션 메시지를 이동합니다. [이벤트 트랜잭션 메시지를 참조하십시오](../../channels/using/event-transactional-messages.md).

   ![](assets/message-center_push_message.png)

1. **[!UICONTROL Content]** 메시지를 클릭하여 메시지의 제목과 본문을 수정합니다.

   개인화 필드를 삽입하여 이벤트를 만들 때 정의한 요소를 추가할 수 있습니다.

   ![](assets/message-center_push_content.png)

   To find these fields, click the pencil next to an item, click **[!UICONTROL Insert personalization field]** and select **[!UICONTROL Transactional event]** &gt; **[!UICONTROL Event context]**.

   ![](assets/message-center_push_personalization.png)

   For more on editing a push notification content, see [Creating a push notification](../../channels/using/preparing-and-sending-a-push-notification.md).

1. 변경 내용을 저장하고 메시지를 게시합니다. See [Publishing a transactional message](../../channels/using/event-transactional-messages.md#publishing-a-transactional-message).
1. Adobe Campaign Standard REST API를 사용하여, 보딩 데이터가 들어 있는 Android (GCM) 에서 하나의 모바일 응용 프로그램 (weflight) 를 사용하여 등록 토큰 (ABCDEF 123456789) 로 이벤트를 보냅니다.

   ```
   {
     "registrationToken":"ABCDEF123456789",
     "application":"WeFlight",
     "pushPlatform":"gcm",
     "ctx":
     {
       "gateNumber":"Gate B18",
       "lastname":"Green",
       "firstname":"Jane"
     }
   }
   ```

   For more on integrating the triggering of an event into an external system, see [Site integration](../../administration/using/configuring-transactional-messaging.md#integrating-the-triggering-of-the-event-in-a-website).

등록 토큰이 존재하는 경우 해당 사용자는 다음 내용을 포함하는 트랜잭션 푸시 알림을 받습니다.

" 제인 그린, 바로 탑승이 시작되었습니다! Gate B 18로 진행하십시오. "

## Transactional push notifications targeting a profile {#transactional-push-notifications-targeting-a-profile}

모바일 애플리케이션을 구독한 Adobe Campaign 프로필로 트랜잭션 푸시 알림을 전송할 수 있습니다. This delivery can contain [personalization](../../designing/using/inserting-a-personalization-field.md) fields, such as the recipient's first name.

이 경우 이벤트에 Adobe Campaign 데이터베이스의 프로필로 조정을 허용하는 일부 필드가 포함되어야 합니다.

프로필을 타깃팅할 때 하나의 트랜잭션 푸시 알림이 모바일 애플리케이션 및 디바이스별로 전송됩니다. 예를 들어 Adobe Campaign 사용자가 두 개의 애플리케이션을 구독하면 이 사용자는 두 개의 알림을 받게 됩니다. 사용자가 두 개의 다른 장치로 동일한 응용 프로그램을 구독하면 이 사용자는 각 장치에서 알림을 받게 됩니다.

The mobile applications a profile has subscribed to are listed in the **[!UICONTROL Mobile App Subscriptions]** tab of this profile. To access this tab, select a profile and click the **[!UICONTROL Edit profile properties]** button on the right.

![](assets/push_notif_subscriptions.png)

For more information on accessing and editing profiles, see [Profiles](../../audiences/using/creating-profiles.md).

### Sending a transactional push notification targeting a profile {#sending-a-transactional-push-notification-targeting-a-----------profile}

예를 들어, 항공사 회사는 모바일 애플리케이션을 구독한 모든 Adobe Campaign 사용자에게 마지막 탑승 요청을 보내고자 합니다.

1. 편집할 수 있도록 만들어진 트랜잭션 메시지를 이동합니다. [이벤트 트랜잭션 메시지를 참조하십시오](../../channels/using/event-transactional-messages.md).

   ![](assets/message-center_push_message_profile.png)

1. **[!UICONTROL Content]** 메시지를 클릭하여 메시지의 제목과 본문을 수정합니다.

   실시간 이벤트를 기반으로 하는 구성과 달리 모든 프로파일 정보에 직접 액세스하여 메시지를 개인화할 수 있습니다. See [Inserting a personalization field](../../designing/using/inserting-a-personalization-field.md).

   ![](assets/message-center_push_content_profile.png)

   푸시 알림 컨텐츠 편집에 대한 자세한 내용을 살펴보십시오. See [Creating a push notification](../../channels/using/preparing-and-sending-a-push-notification.md).

1. 변경 내용을 저장하고 메시지를 게시합니다. See [Publishing a transactional message](../../channels/using/event-transactional-messages.md#publishing-a-transactional-message).
1. Adobe Campaign Standard REST API를 사용하여 이벤트를 프로필에 보냅니다.

   ```
   {
     "ctx":
     {
       "email":"janegreen@email.com",
       "gateNumber":"D16",
     }
   }
   ```

   For more on integrating the triggering of an event into an external system, see [Site integration](../../administration/using/configuring-transactional-messaging.md#integrating-the-triggering-of-the-event-in-a-website).

   >[!NOTE]
   >
   >등록 토큰, 응용 프로그램 및 푸시 플랫폼 필드가 없습니다. 이 예에서는 이메일 필드에서 조정을 수행합니다.

