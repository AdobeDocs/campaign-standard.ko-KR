---
title: 후속 메시지
seo-title: 후속 메시지
description: 후속 메시지
seo-description: 후속 메시지를 만들고 게시하는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: D 2 A 17 DA 2-E 935-420 A -8531-78 ED 6 A 1 FE 68 B
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 채널
content-type: 참조
topic-tags: 트랜잭션 메시징
discoiquuid: 9615 E 369-754 F -4 F 6 A-A 1 B 1-14462 F 946666
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 855db33971afdf9f02bf1b00be67c9e3f50bee06

---


# Follow-up messages{#follow-up-messages}

특정 트랜잭션 메시지를 받은 고객에게 후속 메시지를 보낼 수 있습니다. 이렇게 하려면 해당 이벤트를 타깃팅하는 워크플로우를 설정해야 합니다.

[트랜잭션 메시지 작업 원칙](../../channels/using/about-transactional-messaging.md#transactional-messaging-operating-principle) 섹션에 설명된 예제를 재사용하겠습니다. 장바구니에 제품을 추가하는 장바구니 포기 이메일이 장바구니에 제품을 추가했지만 구매하지 않고 사이트를 떠납니다.

장바구니 포기 알림을 받았지만 3 일 후에 열지 않은 모든 고객에게 친숙한 미리 알림을 보내려는 경우

각 관심 고객은 전송된 첫 번째 이메일에 사용된 동일한 데이터를 기반으로 후속 메시지를 받게 됩니다.

## Accessing the follow-up messages {#accessing-the-follow-up-messages}

Once you have created and published an event (the cart abandonment as per the [example](../../channels/using/about-transactional-messaging.md#transactional-messaging-operating-principle) above), the corresponding transactional message and follow-up message are created automatically.

The configuration steps are presented in the [Configuring an event to send a follow-up message](../../administration/using/configuring-transactional-messaging.md#use-case--configuring-an-event-to-send-a-transactional-message) section.

워크플로우에서 이벤트를 처리하려면 배달 템플릿이 필요합니다. However, when publishing the event, the [transactional message](../../channels/using/event-transactional-messages.md) that is created cannot be used as a template. 따라서 이 이벤트 유형을 지원하고 워크플로우에서 템플릿으로 사용할 수 있도록 디자인된 특정 후속 배달 템플릿을 만들어야 합니다.

이 템플릿에 액세스하려면:

1. Click the **[!UICONTROL Adobe Campaign]** logo, in the top left corner.
1. **[!UICONTROL Resources]** &gt; **[!UICONTROL Templates]****[!UICONTROL Delivery templates]**&#x200B;를 선택합니다.
1. Check the **[!UICONTROL Follow-up messages]** box in the left pane.

   ![](assets/message-center_follow-up-search.png)

후속 메시지만 표시됩니다.

>[!NOTE]
>
>To access the transactional messages, you must have administration rights or appear in the **[!UICONTROL Message Center agents]** (mcExec) security group.

## Sending a follow-up message {#sending-a-follow-up-message}

후속 배달 템플릿을 만든 후에는 워크플로우에서 이를 사용하여 후속 메시지를 보낼 수 있습니다.

1. 마케팅 활동 목록에 액세스하고 새 워크플로우를 만듭니다.

   See [Creating a workflow](../../automating/using/building-a-workflow.md#creating-a-workflow).

1. **[!UICONTROL Scheduler]** 워크플로우를 워크플로우로 드래그하여 놓고 엽니다. 실행 빈도를 하루에 한 번 설정합니다.

   The Scheduler activity is presented in the [Scheduler](../../automating/using/scheduler.md) section.

1. **[!UICONTROL Query]** 워크플로우를 워크플로우로 드래그하여 놓고 엽니다.

   The Query activity is presented in the [Query](../../automating/using/query.md) section.

1. To run the query on a resource other than the profile resource, go to the activity's **[!UICONTROL Properties]** tab and click the **[!UICONTROL Resource]** drop-down list.

   ![](assets/message-center_follow-up-query-properties.png)

   >[!NOTE]
   >
   >기본적으로 활동은 프로필을 검색할 수 있도록 미리 구성되어 있습니다.

1. 이 이벤트의 데이터에만 액세스할 수 있도록 타게팅할 이벤트를 선택합니다.

   ![](assets/message-center_follow-up-query-resource.png)

1. Go to the activity's **[!UICONTROL Target]** tab and drag and drop the **[!UICONTROL Delivery logs (logs)]** element from the **[!UICONTROL Email]** section into the workspace.

   ![](assets/message-center_follow-up-delivery-logs.png)

   Select **[!UICONTROL Exists]** to target all of the customers who received the email.

   ![](assets/message-center_follow-up-delivery-logs-exists.png)

1. Move the **[!UICONTROL Tracking logs (tracking)]** element from the palette to the workspace and select **[!UICONTROL Does not exist]** to target all of the customers who did not open the email.

   ![](assets/message-center_follow-up-delivery-and-tracking-logs.png)

1. Drag and drop the event that you are targeting (**Cart abandonment** in this example) from the **[!UICONTROL Email]** section into the workspace. 그런 다음 3 일 전에 보낸 모든 메시지를 타깃팅하는 규칙을 정의합니다.

   ![](assets/message-center_follow-up-created.png)

   즉, 워크플로우가 실행되기 3 일 전에 트랜잭션 메시지를 받은 모든 받는 사람이 여전히 타깃팅됩니다.

   Click **[!UICONTROL Confirm]** to save the query.

1. **이메일 전달** 활동을 워크플로우로 드래그하여 놓습니다.

   The Email delivery activity is presented in the [Email delivery](../../automating/using/email-delivery.md) section.

   ![](assets/message-center_follow-up-workflow.png)

   [SMS 배달](../../automating/using/sms-delivery.md) 또는 [모바일 앱 배달](../../automating/using/push-notification-delivery.md) 활동을 사용할 수도 있습니다. In this case, make sure you select the **[!UICONTROL Mobile (SMS)]** or **[!UICONTROL Mobile application]** channel when creating your event configuration. See [Creating an event](../../administration/using/configuring-transactional-messaging.md#creating-an-event).

1. **이메일 배달** 활동을 엽니다. In the creation wizard, check the **[!UICONTROL Follow-up messages]** box and select the follow-up delivery template that was created after publishing the event.

   ![](assets/message-center_follow-up-template.png)

1. 추가 메시지 콘텐트에서 개인화 필드를 추가하여 이벤트의 컨텐츠를 활용할 수 있습니다.

   ![](assets/message-center_follow-up-content.png)

1. Find the fields that you defined when creating your event by selecting **[!UICONTROL Transactional event]** &gt; **[!UICONTROL Event context]**. See [Personalizing a transactional message](../../channels/using/event-transactional-messages.md#personalizing-a-transactional-message).

   ![](assets/message-center_follow-up-personalization.png)

   즉, 이벤트를 처음 보낼 때 사용한 풍부한 데이터를 포함하여 동일한 컨텐츠를 활용하여 개인화된 친근한 미리 알림을 만들 수 있습니다.

1. 활동을 저장하고 워크플로우를 시작합니다.

워크플로우가 시작되면, 장바구니 포기 알림을 3 일 전 수신했지만, 열지 않은 모든 고객은 동일한 데이터를 기반으로 하는 후속 메시지를 받게 됩니다.

>[!NOTE]
>
>If you selected the **[!UICONTROL Profile]** targeting dimension when creating the event configuration, the follow-up message will also leverage the Adobe Campaign marketing database. [프로필 트랜잭션 메시지를 참조하십시오](../../channels/using/profile-transactional-messages.md).

