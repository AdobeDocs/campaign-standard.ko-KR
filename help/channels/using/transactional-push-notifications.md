---
title: 트랜잭션 푸시 알림
description: Adobe Campaign Standard을 사용하여 트랜잭션 푸시 알림을 보내는 방법을 알아봅니다.
audience: channels
content-type: reference
topic-tags: transactional-messaging
context-tags: null
feature: Transactional Messaging
role: User
level: Intermediate
exl-id: 61988c1d-d538-47b1-94c1-f3fbdf314b65
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '1451'
ht-degree: 3%

---

# 트랜잭션 푸시 알림{#transactional-push-notifications}

Adobe Campaign을 사용하여 iOS 및 Android 모바일 장치에서 트랜잭션 푸시 알림을 전송할 수 있습니다. 이러한 메시지는 Experience Cloud Mobile SDK를 활용하여 Adobe Campaign에 설정한 모바일 애플리케이션을 통해 수신됩니다.

>[!NOTE]
>
>푸시 채널은 선택 사항입니다. 사용권 계약을 확인하십시오. 표준 푸시 알림에 대한 자세한 내용은 [푸시 알림 기본 정보](../../channels/using/about-push-notifications.md).

트랜잭션 푸시 알림을 전송하려면 그에 따라 Adobe Campaign을 구성해야 합니다. 다음을 참조하십시오 [모바일 애플리케이션 구성](../../administration/using/configuring-a-mobile-application.md).

두 가지 유형의 트랜잭션 푸시 알림을 보낼 수 있습니다.

* [이벤트를 타겟팅하는 트랜잭션 푸시 알림](#transactional-push-notifications-targeting-an-event)
* [트랜잭션 푸시 알림 타겟팅 프로필](#transactional-push-notifications-targeting-a-profile) Adobe Campaign 데이터베이스에서

## 이벤트를 타겟팅하는 트랜잭션 푸시 알림 {#transactional-push-notifications-targeting-an-event}

Adobe Campaign을 사용하여 를 보낼 수 있습니다. **모든 사용자에게 익명 트랜잭션 푸시 알림** 모바일 애플리케이션에서 알림을 받도록 선택한 사용자.

이 경우에는 **이벤트 자체에 포함된 데이터는 게재 대상을 정의하는 데 사용됩니다**. Adobe Campaign 통합 프로필 데이터베이스의 데이터를 활용할 수 없습니다.

### 이벤트 기반 트랜잭션 푸시 알림 구성 {#configuring-event-based-transactional-push-notification}

모바일 애플리케이션에서 알림을 수신하도록 선택한 모든 사용자에게 트랜잭션 푸시 알림을 보내려면 먼저 이벤트 자체에 포함된 데이터를 타겟팅하는 이벤트를 만들고 구성해야 합니다.

>[!NOTE]
>
>을 사용하여 이벤트 기반 트랜잭션 푸시 알림의 콘텐츠를 개인화할 수 있습니다 [이벤트 속성](../../channels/using/configuring-transactional-event.md#defining-the-event-attributes) (이벤트의 데이터) 및 [이벤트 보강](../../channels/using/configuring-transactional-event.md#enriching-the-transactional-message-content) (Campaign 데이터베이스의 데이터). 다음을 참조하십시오 [아래 예](#sending-event-based-transactional-push-notification).

이벤트에는 다음 세 가지 요소가 포함되어야 합니다.

* A **등록 토큰**: 하나의 모바일 애플리케이션 및 하나의 디바이스에 대한 사용자 ID입니다. Adobe Campaign 데이터베이스의 어떤 프로필에도 해당되지 않을 수 있습니다.
* A **모바일 애플리케이션 이름** (모든 장치 - Android 및 iOS용 1개). Adobe Campaign에 구성된 모바일 애플리케이션 ID로, 사용자의 장치에서 푸시 알림을 받는 데 사용됩니다. 자세한 내용은 다음을 참조하십시오. [모바일 애플리케이션 구성](../../administration/using/configuring-a-mobile-application.md).
* A **푸시 플랫폼** ( Android의 경우 &quot;gcm&quot; 또는 iOS의 경우 &quot;apns&quot;).

이벤트를 구성하려면 아래 단계를 수행합니다.

1. 이벤트 구성을 생성할 때 **[!UICONTROL Push notification]** 채널 및 **[!UICONTROL Real-time event]** 타겟팅 차원(참조) [이벤트 만들기](../../channels/using/configuring-transactional-event.md#creating-an-event)).
1. 이벤트에 필드를 추가합니다. 이를 통해 트랜잭션 메시지를 개인화할 수 있습니다( 참조). [이벤트 속성 정의](../../channels/using/configuring-transactional-event.md#defining-the-event-attributes)). 이 예제에서는 &quot;gateNumber&quot;, &quot;lastname&quot; 및 &quot;firstname&quot; 필드를 정의합니다.
1. 메시지의 내용을 보강할 수도 있습니다. 이렇게 하려면 이벤트 구성에 연결한 테이블의 필드를 추가합니다( 참조) [이벤트 강화](../../channels/using/configuring-transactional-event.md#enriching-the-transactional-message-content)).

   <!--Event-based transactional messaging is supposed to use only the data that are in the sent event to define the recipient and the message content personalization. However, you can enrich the content of your transactional message using information from the Adobe Campaign database.-->

1. [이벤트 미리보기 및 게시](../../channels/using/publishing-transactional-event.md#previewing-and-publishing-the-event).

   이벤트를 미리 볼 때 REST API에는 게재를 타깃팅하는 데 사용할 &quot;registrationToken&quot;, &quot;application&quot; 및 &quot;pushPlatform&quot; 특성이 포함되어 있습니다.

   ![](assets/message-center_push_api.png)

   이벤트가 게시되면 새 이벤트에 연결된 트랜잭션 푸시 알림이 자동으로 만들어집니다. 이제 방금 만든 메시지를 수정하고 게시할 수 있습니다(참조) [이 섹션](#sending-event-based-transactional-push-notification)).

1. 이벤트를 웹 사이트에 통합(참조 [이벤트 트리거 통합](../../channels/using/getting-started-with-transactional-msg.md#integrate-event-trigger)).

### 이벤트 기반 트랜잭션 푸시 알림 보내기 {#sending-event-based-transactional-push-notification}

예를 들어 항공사는 모바일 애플리케이션 사용자를 초대하여 탑승을 위한 해당 게이트로 진행하고자 합니다.

이 회사는 하나의 모바일 애플리케이션을 사용하여 사용자당 하나의 트랜잭션 푸시 알림(등록 토큰으로 식별됨)을 하나의 디바이스를 통해 전송합니다.

1. 만든 트랜잭션 메시지로 이동하여 편집합니다. 다음을 참조하십시오 [트랜잭션 메시지 액세스](../../channels/using/editing-transactional-message.md#accessing-transactional-messages).

   ![](assets/message-center_push_message.png)

1. 다음을 클릭합니다. **[!UICONTROL Content]** 메시지 제목과 본문을 수정하려면 차단합니다.

1. 개인화 필드를 삽입하여 이벤트를 만들 때 정의한 요소를 추가할 수 있습니다(참조) [이벤트 속성 정의](../../channels/using/configuring-transactional-event.md#defining-the-event-attributes)).

   ![](assets/message-center_push_content.png)

   이러한 필드를 찾으려면 항목 옆에 있는 연필을 클릭하고 **[!UICONTROL Insert personalization field]** 및 선택 **[!UICONTROL Context]** > **[!UICONTROL Real-time event]** > **[!UICONTROL Event context]**.

   ![](assets/message-center_push_personalization.png)

   푸시 알림 콘텐츠 편집에 대한 자세한 내용은 다음을 참조하십시오. [푸시 알림 준비 및 보내기](../../channels/using/preparing-and-sending-a-push-notification.md).

1. Adobe Campaign 데이터베이스의 추가 정보를 사용하려는 경우 트랜잭션 메시지 콘텐츠를 보강할 수도 있습니다( 참조) [이벤트 강화](../../channels/using/configuring-transactional-event.md#enriching-the-transactional-message-content)).

1. 변경 내용을 저장하고 메시지를 게시합니다. [트랜잭션 메시지 게시](../../channels/using/publishing-transactional-message.md#publishing-a-transactional-message)를 참조하십시오.

1. Adobe Campaign Standard REST API를 사용하여 보딩 데이터가 포함된 Android(gcm)에서 하나의 모바일 애플리케이션(WeFlight)을 사용하여 등록 토큰(ABCDEF123456789)에 이벤트를 보냅니다.

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

   외부 시스템에 이벤트 트리거를 통합하는 방법에 대한 자세한 내용은 [이벤트 트리거 통합](../../channels/using/getting-started-with-transactional-msg.md#integrate-event-trigger).

등록 토큰이 있으면 해당 사용자는 다음 콘텐츠를 포함하는 트랜잭션 푸시 알림을 받습니다.

*&quot;안녕하세요, 제인 그린 씨, 탑승이 막 시작되었습니다! 게이트 B18로 진행하십시오.&quot;*

## 프로필을 타겟팅하는 트랜잭션 푸시 알림 {#transactional-push-notifications-targeting-a-profile}

트랜잭션 푸시 알림을 보낼 수 있습니다. **모바일 애플리케이션을 구독한 Adobe Campaign 프로필**. 이 게재에는 다음이 포함될 수 있습니다. [개인화 필드](../../designing/using/personalization.md#inserting-a-personalization-field)수신자 이름과 같은 로, Adobe Campaign 데이터베이스에서 직접 검색됩니다.

이 경우 이벤트에는 일부 필드가 포함되어야 합니다 **Adobe Campaign 데이터베이스의 프로필로 조정 허용**.

프로필을 타겟팅할 때 모바일 애플리케이션과 디바이스당 하나의 트랜잭션 푸시 알림이 전송됩니다. 예를 들어 Adobe Campaign 사용자가 두 개의 애플리케이션을 구독한 경우 이 사용자는 두 개의 알림을 받게 됩니다. 사용자가 두 개의 다른 장치로 동일한 애플리케이션을 구독한 경우 이 사용자는 각 장치에서 알림을 받게 됩니다.

프로필이 구독한 모바일 애플리케이션이에 나열되어 있습니다. **[!UICONTROL Mobile App Subscriptions]** 이 프로필의 탭 이 탭에 액세스하려면 프로필을 선택하고 **[!UICONTROL Edit profile properties]** 오른쪽 단추

![](assets/push_notif_subscriptions.png)

프로필 액세스 및 편집에 대한 자세한 내용은 [프로필 기본 정보](../../audiences/using/about-profiles.md).

### 프로필 기반 트랜잭션 푸시 알림 구성 {#configuring-profile-based-transactional-push-notification}

모바일 애플리케이션을 구독한 Adobe Campaign 프로필로 트랜잭션 푸시 알림을 보내려면 먼저 Adobe Campaign 데이터베이스를 타겟팅하는 이벤트를 만들고 구성해야 합니다.

1. 이벤트 구성을 생성할 때 **[!UICONTROL Push notification]** 채널 및 **[!UICONTROL Profile]** 타겟팅 차원(참조) [이벤트 만들기](../../channels/using/configuring-transactional-event.md#creating-an-event)).

   기본적으로 트랜잭션 푸시 알림은 수신자가 구독한 모든 모바일 애플리케이션으로 전송됩니다. 푸시 알림을 특정 모바일 애플리케이션으로 전송하려면 목록에서 선택합니다. 다른 모바일 애플리케이션은 메시지의 타겟이 되지만 전송에서는 제외됩니다.

   ![](assets/message-center_push_appfilter.png)

1. 트랜잭션 메시지를 개인화하려는 경우 이벤트에 필드를 추가합니다( 참조). [이벤트 속성 정의](../../channels/using/configuring-transactional-event.md#defining-the-event-attributes)).

   >[!NOTE]
   >
   >데이터 보강 기능을 만들려면 필드를 하나 이상 추가해야 합니다. 다음과 같은 다른 필드는 만들 필요가 없습니다. **이름** 및 **성** Adobe Campaign 데이터베이스의 개인화 필드를 사용할 수 있습니다.

1. 이벤트를 다음에 연결하기 위한 데이터 보강 만들기 **[!UICONTROL Profile]** 리소스(참조) [이벤트 강화](../../channels/using/configuring-transactional-event.md#enriching-the-transactional-message-content)) 이 데이터 보강 기능을 선택하고 **[!UICONTROL Targeting enrichment]**.

   >[!IMPORTANT]
   >
   >프로필 기반 이벤트에는 이 단계가 필수입니다.

1. [이벤트 미리보기 및 게시](../../channels/using/publishing-transactional-event.md#previewing-and-publishing-the-event).

   이벤트를 미리 볼 때 REST API에는 등록 토큰, 애플리케이션 이름 및 푸시 플랫폼이 **[!UICONTROL Profile]** 리소스.

   이벤트가 게시되면 새 이벤트에 연결된 트랜잭션 푸시 알림이 자동으로 만들어집니다. 이제 방금 만든 메시지를 수정하고 게시할 수 있습니다(참조) [이 섹션](#sending-profile-based-transactional-push-notification)).

1. 이벤트를 웹 사이트에 통합(참조 [이벤트 트리거 통합](../../channels/using/getting-started-with-transactional-msg.md#integrate-event-trigger)).

### 프로필 기반 트랜잭션 푸시 알림 보내기 {#sending-profile-based-transactional-push-notification}

예를 들어 항공사에서 모바일 애플리케이션을 구독한 모든 Adobe Campaign 사용자에게 탑승을 위한 마지막 호출을 전송하려고 합니다.

1. 만든 트랜잭션 메시지로 이동하여 편집합니다. 다음을 참조하십시오 [트랜잭션 메시지 액세스](../../channels/using/editing-transactional-message.md#accessing-transactional-messages).

1. 다음을 클릭합니다. **[!UICONTROL Content]** 메시지 제목과 본문을 수정하려면 차단합니다.

   실시간 이벤트 기반 구성과 달리, 모든 프로필 정보에 직접 액세스하여 메시지를 개인화할 수 있습니다. [개인화 필드 삽입](../../designing/using/personalization.md#inserting-a-personalization-field)을 참조하십시오.

   푸시 알림 콘텐츠 편집에 대한 자세한 내용은 다음을 참조하십시오. [푸시 알림 준비 및 보내기](../../channels/using/preparing-and-sending-a-push-notification.md).

1. 변경 내용을 저장하고 메시지를 게시합니다. [트랜잭션 메시지 게시](../../channels/using/publishing-transactional-message.md#publishing-a-transactional-message)를 참조하십시오.
1. Adobe Campaign Standard REST API를 사용하여 프로필에 이벤트를 보냅니다.

   ```
   {
     "ctx":
     {
       "email":"janegreen@email.com",
       "gateNumber":"D16",
     }
   }
   ```

외부 시스템에 이벤트 트리거를 통합하는 방법에 대한 자세한 내용은 [이벤트 트리거 통합](../../channels/using/getting-started-with-transactional-msg.md#integrate-event-trigger).

해당 사용자는 Adobe Campaign 데이터베이스에서 검색된 모든 개인화 요소를 포함하는 트랜잭션 푸시 알림을 받습니다.

>[!NOTE]
>
>등록 토큰, 애플리케이션 및 푸시 플랫폼 필드가 없습니다. 이 예제에서는 전자 메일 필드를 사용하여 조정을 수행합니다.

## 트랜잭션 푸시 알림에서 대상 매핑 변경 {#change-target-mapping}

트랜잭션 푸시 알림은 특정 [대상 매핑](../../administration/using/target-mappings-in-campaign.md) 에는 이 유형의 게재를 보내는 데 필요한 기술 설정이 포함되어 있습니다.

이 대상 매핑을 변경하려면 아래 단계를 따르십시오.

1. 트랜잭션 메시지 목록에서 푸시 알림을 선택합니다.

1. 메시지 대시보드에서 **[!UICONTROL Edit properties]** 단추를 클릭합니다.

   ![](assets/message-center_push_edit.png)

1. 확장 **[!UICONTROL Advanced parameters]** 섹션.

1. **[!UICONTROL Select a 'Target mapping' element]**&#x200B;를 클릭합니다.

   ![](assets/message-center_push_target-mapping.png)

1. 목록에서 대상 매핑을 선택합니다.

   >[!NOTE]
   >
   >전송 시 최적의 게재 준비 시간 및 성능 **프로필 기반** 트랜잭션 푸시 알림, 사용 **[!UICONTROL Profile - Real-time event for Push (mapRtEventAppSubRcp)]** 대상 매핑.

   ![](assets/message-center_push_target-mapping_change.png)

1. 변경 사항을 확인하고 메시지를 게시합니다. [트랜잭션 메시지 게시](../../channels/using/publishing-transactional-message.md#publishing-a-transactional-message)를 참조하십시오.

   >[!IMPORTANT]
   >
   >변경 사항을 적용하려면 메시지를 다시 게시해야 합니다. 그렇지 않으면 이전 대상 매핑이 계속 사용됩니다.


