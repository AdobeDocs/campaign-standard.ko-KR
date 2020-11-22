---
solution: Campaign Standard
product: campaign
title: 트랜잭션 푸시 알림
description: 트랜잭션 푸시 알림을 만들고 게시하는 방법에 대해 알아봅니다.
audience: channels
content-type: reference
topic-tags: transactional-messaging
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '740'
ht-degree: 13%

---


# 트랜잭션 푸시 알림{#transactional-push-notifications}

Adobe Campaign을 사용하여 iOS 및 Android 모바일 장치에서 트랜잭션 푸시 알림을 전송할 수 있습니다. 이러한 메시지는 Experience Cloud Mobile SDK를 활용하여 Adobe Campaign에서 설정한 모바일 애플리케이션에서 수신됩니다.

>[!NOTE]
>
>푸시 채널은 선택 사항입니다. 사용권 계약을 확인하십시오. 표준 푸시 알림에 대한 자세한 내용은 푸시 [알림을 참조하십시오](../../channels/using/about-push-notifications.md).

두 가지 유형의 트랜잭션 푸시 알림을 전송할 수 있습니다.

* 이벤트를 타깃팅하는 트랜잭션 푸시 알림
* Adobe Campaign 데이터베이스의 트랜잭션 푸시 알림을 타깃팅합니다.

Once you have created and published an event (the cart abandonment explained in [this section](../../channels/using/getting-started-with-transactional-msg.md#transactional-messaging-operating-principle)), the corresponding transactional push notification is created automatically.

The configuration steps are presented in the [Configuring an event to send a transactional push notification](../../administration/using/configuring-transactional-messaging.md#use-case--configuring-an-event-to-send-a-transactional-message) section.

이벤트가 트랜잭션 메시지 전송을 트리거하려면 메시지를 개인화한 다음 테스트하여 게시해야 합니다.

>[!NOTE]
>
>트랜잭션 메시지에 액세스하려면 **[!UICONTROL Administrators (all units)]** 보안 그룹의 일부여야 합니다.

## 이벤트를 타깃팅하는 트랜잭션 푸시 알림 {#transactional-push-notifications-targeting-an-event}

모바일 응용 프로그램에서 알림을 받도록 선택한 모든 사용자에게 익명 트랜잭션 푸시 알림을 보낼 수 있습니다.

이 경우 이벤트 자체에 포함된 데이터만 배달 대상을 정의하는 데 사용됩니다. Adobe Campaign 통합 프로필 데이터베이스의 데이터는 활용되지 않습니다.

### 이벤트를 타깃팅하는 트랜잭션 푸시 알림 전송 {#sending-a-transactional-push-notification-targeting-an-----------event}

예를 들어, 한 항공사 회사는 모바일 애플리케이션 사용자를 탑승을 위해 관련 게이트로 이동할 수 있도록 초대하려고 합니다.

이 회사는 하나의 모바일 애플리케이션을 사용하여 단일 디바이스를 통해 사용자당(등록 토큰으로 식별됨) 하나의 트랜잭션 푸시 알림을 전송합니다.

1. 만든 트랜잭션 메시지로 이동하여 편집합니다. [이벤트 트랜잭션 메시지](../../channels/using/event-transactional-messages.md)를 참조하십시오.

   ![](assets/message-center_push_message.png)

1. Click the **[!UICONTROL Content]** block to modify your message&#39;s title and body.

   개인화 필드를 삽입하여 이벤트를 만들 때 정의한 요소를 추가할 수 있습니다.

   ![](assets/message-center_push_content.png)

   이러한 필드를 찾으려면 항목 옆에 있는 연필 **[!UICONTROL Insert personalization field]** 을 클릭하고 **[!UICONTROL Context]** > **[!UICONTROL Real-time event]** > **[!UICONTROL Event context]**&#x200B;를 선택합니다.

   ![](assets/message-center_push_personalization.png)

   푸시 알림 컨텐츠 편집에 대한 자세한 내용은 푸시 알림 [만들기를 참조하십시오](../../channels/using/preparing-and-sending-a-push-notification.md).

1. 변경 내용을 저장하고 메시지를 게시합니다. [트랜잭션 메시지 게시](../../channels/using/event-transactional-messages.md#publishing-a-transactional-message)를 참조하십시오.

1. Adobe Campaign Standard REST API를 사용하여, Android(WeFlight)의 한 모바일 응용 프로그램(WeFlight)을 사용하여 보딩 데이터가 포함된 이벤트를 등록 토큰(ABCDEF123456789)으로 전송합니다.

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

   이벤트 트리거를 외부 시스템에 통합하는 방법에 대한 자세한 내용은 [사이트 통합을 참조하십시오](../../administration/using/configuring-transactional-messaging.md#integrating-the-triggering-of-the-event-in-a-website).

등록 토큰이 존재하는 경우 해당 사용자는 다음 내용이 포함된 트랜잭션 푸시 알림을 받습니다.

&quot;안녕하세요, 제인 그린, 탑승이 막 시작되었습니다! B18 게이트로 가십시오.&quot;

## 프로필을 대상으로 하는 트랜잭션 푸시 알림 {#transactional-push-notifications-targeting-a-profile}

모바일 응용 프로그램을 구독한 Adobe Campaign 프로필에 트랜잭션 푸시 알림을 보낼 수 있습니다. 이 배달에는 받는 사람의 이름과 같은 [개인화](../../designing/using/personalization.md#inserting-a-personalization-field) 필드가 포함될 수 있습니다.

이 경우 이벤트에는 Adobe Campaign 데이터베이스의 프로필과 화해를 허용하는 일부 필드가 포함되어야 합니다.

프로파일을 타깃팅할 때 모바일 애플리케이션 및 디바이스당 하나의 트랜잭션 푸시 알림이 전송됩니다. 예를 들어 Adobe Campaign 사용자가 두 개의 응용 프로그램에 가입한 경우 이 사용자는 두 개의 알림을 받게 됩니다. 사용자가 두 개의 다른 장치를 사용하는 동일한 응용 프로그램에 가입한 경우 이 사용자는 각 장치에 대한 알림을 받게 됩니다.

프로필에서 구독한 모바일 응용 프로그램이 이 프로필의 **[!UICONTROL Mobile App Subscriptions]** 탭에 나열됩니다. 이 탭에 액세스하려면 프로필을 선택하고 오른쪽의 **[!UICONTROL Edit profile properties]** 단추를 클릭합니다.

![](assets/push_notif_subscriptions.png)

프로필 액세스 및 편집에 대한 자세한 내용은 [프로필을 참조하십시오](../../audiences/using/creating-profiles.md).

### 프로필을 대상으로 하는 트랜잭션 푸시 알림 전송 {#sending-a-transactional-push-notification-targeting-a-----------profile}

예를 들어, 한 항공사는 자사의 모바일 애플리케이션에 가입한 모든 Adobe Campaign 사용자에게 탑승을 위한 마지막 전화 통화를 보내려고 합니다.

1. 만든 트랜잭션 메시지로 이동하여 편집합니다. [이벤트 트랜잭션 메시지](../../channels/using/event-transactional-messages.md)를 참조하십시오.

1. Click the **[!UICONTROL Content]** block to modify your message&#39;s title and body.

   실시간 이벤트 기반의 구성과 달리 모든 프로필 정보에 직접 액세스하여 메시지를 개인화할 수 있습니다. [개인화 필드 삽입](../../designing/using/personalization.md#inserting-a-personalization-field)을 참조하십시오.

   푸시 알림 컨텐츠 편집에 대한 자세한 내용을 살펴보십시오. 푸시 [알림 만들기를 참조하십시오](../../channels/using/preparing-and-sending-a-push-notification.md).

1. 변경 내용을 저장하고 메시지를 게시합니다. [트랜잭션 메시지 게시](../../channels/using/event-transactional-messages.md#publishing-a-transactional-message)를 참조하십시오.
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

   이벤트 트리거를 외부 시스템에 통합하는 방법에 대한 자세한 내용은 [사이트 통합을 참조하십시오](../../administration/using/configuring-transactional-messaging.md#integrating-the-triggering-of-the-event-in-a-website).

   >[!NOTE]
   >
   >등록 토큰, 응용 프로그램 및 푸시 플랫폼 필드가 없습니다. 이 예에서는 이메일 필드를 사용하여 조정이 수행됩니다.
