---
solution: Campaign Standard
product: campaign
title: 트랜잭션 메시지 수명 주기
description: 트랜잭션 메시지를 게시, 일시 중지, 게시 취소 및 삭제하는 방법을 알아봅니다.
audience: channels
content-type: reference
topic-tags: transactional-messaging
context-tags: null
translation-type: tm+mt
source-git-commit: f19d4b5c1837f3f03789958abb1539d4edea0744
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 76%

---


# 트랜잭션 메시지 수명 주기 {#publishing-transactional-message}

[트랜잭션 메시지](../../channels/using/editing-transactional-message.md)를 보낼 준비가 되면 게시할 수 있습니다.

트랜잭션 메시지를 게시, 일시 중지, 게시 취소 및 삭제하는 단계는 아래에 자세히 설명되어 있습니다.

>[!IMPORTANT]
>
>[관리](../../administration/using/users-management.md#functional-administrators) 역할을 가진 사용자만 트랜잭션 메시지에 액세스하고 게시할 수 있습니다.

## 트랜잭션 메시지 게시 프로세스 {#transactional-messaging-pub-process}

아래 차트에는 전체 트랜잭션 메시징 게시 프로세스가 나와 있습니다.

![](assets/message-center_pub-process.png)

**관련 항목:**
* [트랜잭션 메시지 게시](#publishing-a-transactional-message)
* [트랜잭션 메시지 일시 중지](#suspending-a-transactional-message-publication)
* [트랜잭션 메시지 게시 취소](#unpublishing-a-transactional-message)
* [이벤트 게시](../../channels/using/publishing-transactional-event.md)

<!--## Testing a transactional message {#testing-a-transactional-message}

You first need to create a specific test profile that will allow you to properly check the transactional message.

### Defining a specific test profile {#defining-specific-test-profile}

Define a test profile that will be linked to your event, which will allow you to preview your message and send a relevant proof.

1. From the transactional message dashboard, click the **[!UICONTROL Create test profile]** button.

   ![](assets/message-center_test-profile.png)

1. Specify the information to send in JSON format in the **[!UICONTROL Event data used for personalization]** section. This is the content that will be used when previewing the message and when the test profile receives the proof.

   ![](assets/message-center_event-data.png)

   >[!NOTE]
   >
   >You can also enter the information relating to the profile table. See [Enriching the event](../../channels/using/configuring-transactional-event.md#enriching-the-transactional-message-content) and [Personalizing a transactional message](../../channels/using/editing-transactional-message.md#personalizing-a-transactional-message).

1. Once created, the test profile will be pre-specified in the transactional message. Click the **[!UICONTROL Test profiles]** block of the message to check the target of your proof.

   ![](assets/message-center_5.png)

You can also create a new test profile or use one that already exists in the **[!UICONTROL Test profiles]** menu. To do this:

1. Click the **[!UICONTROL Adobe Campaign]** logo, in the top left corner, then select **[!UICONTROL Profiles & audiences]** > **[!UICONTROL Test profiles]**.
1. In the **[!UICONTROL Event]** section, select the event that you have just created. In this example, select "Cart abandonment (EVTcartAbandonment)".
1. Specify the information to send in JSON format in the **[!UICONTROL Event data]** text box.

   ![](assets/message-center_3.png)

1. Save your changes.
1. Access the message that you created and select the updated test profile.

**Related topics:**

* [Managing test profiles](../../audiences/using/managing-test-profiles.md)
* [Creating audiences](../../audiences/using/creating-audiences.md)

### Sending the proof {#sending-proof}

Once you have created one or more specific test profiles and saved your transactional message, you can send a proof to test it.

![](assets/message-center_10.png)

The steps for sending a proof are detailed in the [Sending proofs](../../sending/using/sending-proofs.md) section.-->

## 트랜잭션 메시지 게시 {#publishing-a-transactional-message}

트랜잭션 메시지를 편집하고 테스트한 후 게시할 수 있습니다. **[!UICONTROL Publish]** 버튼을 클릭하면 됩니다.

![](assets/message-center_12.png)

이제 &quot;장바구니 포기&quot; 이벤트가 트리거되는 경우, 수신자의 제목과 성, 장바구니 URL, 제품 목록이 정의되어 있다면 마지막으로 상담한 제품 또는 제품 목록, 그리고 보낼 총 장바구니 금액이 포함된 메시지를 자동으로 표시합니다.

트랜잭션 메시지에 대한 보고서에 액세스하려면 **[!UICONTROL Reports]** 버튼을 사용하십시오. [동적 보고서](../../reporting/using/about-dynamic-reports.md)를 참조하십시오.

![](assets/message-center_13.png)

**관련 항목**:
* [트랜잭션 메시지 편집](../../channels/using/editing-transactional-message.md)
* [트랜잭션 메시지 테스트](../../channels/using/testing-transactional-message.md)
* [이벤트 트리거 통합](../../channels/using/getting-started-with-transactional-msg.md#integrate-event-trigger)

## 트랜잭션 메시지 게시 일시 중단 {#suspending-a-transactional-message-publication}

예를 들어 메시지에 포함된 데이터를 수정하기 위해 **[!UICONTROL Pause]** 버튼을 사용하여 트랜잭션 메시지 게시를 일시 중단할 수 있습니다. 그러면 이벤트는 더 이상 처리되지 않고 대신 Adobe Campaign 데이터베이스의 큐에 보관됩니다.

큐에 있는 이벤트는 REST API에 정의된 기간 동안 보관됩니다([REST API 문서](../../api/using/managing-transactional-messages.md) 참조). 또는 트리거 핵심 서비스를 사용 중인 경우 트리거 이벤트에서 보관됩니다([Adobe Experience Cloud Triggers](../../integrating/using/about-adobe-experience-cloud-triggers.md) 참조).

![](assets/message-center_pause.png)

**[!UICONTROL Resume]**&#x200B;을(를) 클릭하면 큐에 있는 모든 이벤트(만료되지 않은 경우)가 처리됩니다. 템플릿 게시가 일시 중단된 동안 수행된 모든 수정 사항이 포함되어 있습니다.

## 트랜잭션 메시지 게시 취소 {#unpublishing-a-transactional-message}

**[!UICONTROL Unpublish]**&#x200B;을(를) 클릭하면 트랜잭션 메시지 게시를 취소할 수 있고 이전에 만든 이벤트에 해당하는 리소스를 REST API에서 삭제하는 해당 이벤트의 게시도 취소할 수 있습니다.

![](assets/message-center_unpublish-template.png)

이제 웹 사이트를 통해 이벤트가 트리거되더라도 해당 메시지는 더 이상 전송되지 않고 데이터베이스에 저장되지 않습니다.

>[!NOTE]
>
>메시지를 다시 게시하려면 해당 이벤트 구성으로 돌아가서 [이벤트](../../channels/using/publishing-transactional-event.md)를 게시한 다음 [메시지](#publishing-a-transactional-message)를 게시해야 합니다.

일시 중지된 트랜잭션 메시지의 게시를 취소하는 경우 다시 게시하기 전에 최대 24시간까지 기다려야 할 수 있습니다. **[!UICONTROL Database cleanup]** 워크플로우가 대기열로 전송된 모든 이벤트를 지우기 위해서 입니다.

메시지 일시 중지 단계는 [트랜잭션 메시지 게시 일시 중단](#suspending-a-transactional-message-publication) 섹션에 자세히 설명되어 있습니다.

매일 오전 4시에 실행되는 **[!UICONTROL Database cleanup]** 워크플로우는 **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** > **[!UICONTROL Workflows]**&#x200B;을(를) 통해 액세스할 수 있습니다.

## 트랜잭션 메시지 삭제 {#deleting-a-transactional-message}

트랜잭션 메시지 게시가 취소되었거나 트랜잭션 메시지가 아직 게시되지 않았으면 트랜잭션 메시지 목록에서 삭제할 수 있습니다. 삭제 방법:

1. 왼쪽 상단 모서리에서 **[!UICONTROL Adobe Campaign]** 로고를 클릭한 다음 **[!UICONTROL Marketing plans]** > **[!UICONTROL Transactional messages]** > **[!UICONTROL Transactional messages]**&#x200B;을(를) 선택합니다.
1. 마우스를 원하는 메시지 위로 가져갑니다.
1. **[!UICONTROL Delete element]** 버튼을 클릭합니다.

![](assets/message-center_delete-template.png)

하지만 트랜잭션 메시지를 삭제하는 것은 특정 조건에서만 수행할 수 있습니다.

* 트랜잭션 메시지에 **[!UICONTROL Draft]** 상태가 있는지 확인해야 합니다. 없다면 메시지를 삭제할 수 없습니다. **[!UICONTROL Draft]** 상태는 아직 게시되지 않았거나 [게시 취소](#unpublishing-a-transactional-message)([일시 중지](#suspending-a-transactional-message-publication)가 아님)된 메시지에적용됩니다.

* **트랜잭션 메시지**: 다른 트랜잭션 메시지가 해당 이벤트에 연결되어 있지 않는 한, 트랜잭션 메시지의 게시를 취소하는 경우, 트랜잭션 메시지를 성공적으로 삭제하려면 이벤트 구성도 게시 취소해야 합니다. 자세한 내용은 [이벤트 게시 취소](../../channels/using/publishing-transactional-event.md#unpublishing-an-event)를 참조하십시오.

   >[!IMPORTANT]
   >
   >이미 알림을 보낸 트랜잭션 메시지를 삭제하면 전송 및 추적 로그도 삭제됩니다.

* **기본 제공 이벤트 템플릿의 트랜잭션 메시지(내부 트랜잭션 메시지)**: 내부 트랜잭션 메시지가 해당 내부 이벤트와 연결된 유일한 메시지인 경우 삭제할 수 없습니다. 먼저 복제하거나 **[!UICONTROL Resources]** > **[!UICONTROL Templates]** > **[!UICONTROL Transactional message templates]** 메뉴를 통해 다른 트랜잭션 메시지를 만들어야 합니다.

<!--## Monitoring transactional message delivery {#monitoring-transactional-message-delivery}

Once the message is published and your site integration is done, you can monitor the delivery.

To monitor transactional messaging, you need to access **execution deliveries**. An execution delivery is a non-actionable and non-functional technical message created once a month for each transactional message, and each time a transactional message is edited and published again.

1. To view the message delivery log, click the icon at the bottom right of the **[!UICONTROL Deployment]** block.

   ![](assets/message-center_access_logs.png)

1. Click the **[!UICONTROL Execution list]** tab.

   ![](assets/message-center_execution_tab.png)

1. Select the execution delivery of your choice.

   ![](assets/message-center_execution_delivery.png)

1. Click again the icon at the bottom right of the **[!UICONTROL Deployment]** block.

   ![](assets/message-center_execution_access_logs.png)

   For each execution delivery, you can consult the delivery logs as you would do for a standard delivery. For more on accessing and using the logs, see [Monitoring a delivery](../../sending/using/monitoring-a-delivery.md).

**Related topics**:
* [Publishing a transactional message](#publishing-a-transactional-message)
* [Integrate the event triggering](../../channels/using/getting-started-with-transactional-msg.md#integrate-event-trigger)

### Profile-based transactional message specificities {#profile-transactional-message-monitoring}

For profile-based transactional messages, you can monitor the following profile information.

Select the **[!UICONTROL Sending logs]** tab. In the **[!UICONTROL Status]** column, **[!UICONTROL Sent]** indicates that a profile has opted in.

![](assets/message-center_marketing_sending_logs.png)

Select the **[!UICONTROL Exclusions logs]** tab to view recipients who have been excluded from the message target, such as addresses on denylist.

![](assets/message-center_marketing_exclusion_logs.png)

For any profile that has opted out, the **[!UICONTROL Address on denylist]** typology rule excluded the corresponding recipient.

This rule is part of a specific typology that applies to all transactional messages based on the **[!UICONTROL Profile]** table.

![](assets/message-center_marketing_typology.png)

**Related topics**:

* [About typologies and typology rules](../../sending/using/about-typology-rules.md)
* [Monitoring a delivery](../../sending/using/monitoring-a-delivery.md)

## Transactional message retry process {#transactional-message-retry-process}

A temporarily undelivered transactional message is subject to automatic retries that are performed until the delivery expires. For more on the delivery duration, see [Validity period parameters](../../administration/using/configuring-email-channel.md#validity-period-parameters).

When a transactional message fails to be sent, there are two retry systems:

* At the transactional messaging level, a transactional message can fail before the event is assigned to an execution delivery, meaning between the event reception and the delivery preparation. See [Event processing retry process](#event-processing-retry-process).
* At the sending process level, once the event has been assigned to an execution delivery, the transactional message can fail due to a temporary error. See [Message sending retry process](#message-sending-retry-process).

The definition of **execution delivery** can be found in the [Monitoring transactional message delivery](#monitoring-transactional-message-delivery) section.

### Event processing retry process {#event-processing-retry-process}

When an event is triggered, it is assigned to an execution delivery.

If the event cannot be assigned to an execution delivery, the event processing is postponed. Retries are then performed until it is assigned to a new execution delivery.

>[!NOTE]
>
>A postponed event does not appear in the transactional message sending logs, because it is not assigned to an execution delivery yet.

For example, the event could not be assigned to an execution delivery because its content was not correct, there was an issue with access rights or branding, an error was detected on applying typology rules, etc. In this case, you can pause the message, edit it to fix the problem and publish it again. The retry system will then assign it to a new execution delivery.

### Message sending retry process {#message-sending-retry-process}

Once the event has been assigned to an execution delivery, the transactional message can fail due to a temporary error, if the recipient's mailbox is full for example. For more on this, see [Retries after a delivery temporary failure](../../sending/using/understanding-delivery-failures.md#retries-after-a-delivery-temporary-failure).

>[!NOTE]
>
>When an event is assigned to an execution delivery, it appears in the sending logs of this execution delivery, and only at this time. The failed deliveries are displayed in the **[!UICONTROL Execution list]** tab of the transactional message sending logs.

### Retry process limitations {#limitations}

**Sending logs update**

In the retry process, the sending logs of the new execution delivery are not immediately updated (the update is performed through a scheduled workflow). It means that the message could be in **[!UICONTROL Pending]** status even if the transactional event has been processed by the new execution delivery.

**Failed execution delivery**

You cannot stop an execution delivery. However, if the current execution delivery fails, a new one is created as soon as a new event is received, and all new events are processed by this new execution delivery. No new events are processed by the failed execution delivery.

If some events already assigned to an execution delivery have been postponed as part of the retry process and if that execution delivery fails, the retry system does not assign the postponed events to the new execution delivery, which means that these events are lost. Check the [delivery logs](#monitoring-transactional-message-delivery) to see the recipients that may have been impacted.-->
