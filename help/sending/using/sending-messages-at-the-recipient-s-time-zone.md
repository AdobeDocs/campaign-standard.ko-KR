---
title: 수신자의 시간대에서 메시지 보내기
seo-title: 수신자의 시간대에서 메시지 보내기
description: 수신자의 시간대에서 메시지 보내기
seo-description: 수신자의 시간대에서 메시지를 보내는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: 70228 C 07-451 F -4 DDB -8 D 26-92 A 5 A 4814 E 3 A
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 전송
content-type: 참조
topic-tags: sheduling-messages
discoiquuid: DAA 980 BA -8 C 7 C -4673-A 68 F -379 D 63 E 4 B 8 BD
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 806dc4736ffb395a0eea102090c688102478aaca

---


# Sending messages at the recipient's time zone{#sending-messages-at-the-recipient-s-time-zone}

날짜와 시간이 중요한 캠페인을 관리할 때 각 수신자의 현지 시간이 고려되는 배달을 예약할 수 있습니다. 사용자는 시간대에서 예약한 시간에 이메일, SMS 또는 푸시 알림을 받게 됩니다.

>[!NOTE]
>
>To use this functionality, make sure that all profiles targeted by your delivery have a time zone specified in the **[!UICONTROL Address]** section of their properties. For more information on accessing profile properties, refer to this [section](../../audiences/using/editing-profiles.md).

To send a delivery at the recipient's time zone, you can also use the **[!UICONTROL Scheduler]** activity in a workflow. For more on this, refer to this [page](../../automating/using/scheduler.md).

다음 예에서는 발렌타인 데이에서만 유효한 프로모션 코드를 전 세계 모든 고객에게 발송합니다. 하루 동안 사용할 수 있는 충분한 시간을 제공하기 위해 모든 고객은 2 월 14 일 오전 8 시 (태평양 표준시) 에 해당 시간대에 따라 메시지를 받게 됩니다.

1. **[!UICONTROL Marketing activities]** 탭에서 배송 내용 만들기를 시작합니다. To learn more on delivery creation, refer to this [section](../../channels/using/creating-an-email.md).
1. After designing your Valentine's Day email, click **[!UICONTROL Create]** to access the delivery dashboard. For more on email designing, refer to this [page](../../designing/using/example--email-personalization.md).

   ![](assets/send-time_opt_valentine_1.png)

1. From the delivery dashboard, select the **[!UICONTROL Schedule]** block.

   ![](assets/send-time_opt_valentine_2.png)

1. Select the **[!UICONTROL Messages to be sent automatically on the date]** option specified below. **[!UICONTROL Start sending from]** 이 필드에 연락처 날짜를 설정하여 2 월 14 일 오전 8 시 (오전 8 시) 에 모든 수신자가 발렌타인 데이에 받을 수 있도록 합니다.

   ![](assets/send-time_opt_valentine.png)

1. **[!UICONTROL Time zone of the contact date]** 필드에서 기본적으로 배달이 전송될 시간대를 선택합니다.

   If a profile's **[!UICONTROL Time zone]** is left as **[!UICONTROL Default]**, the recipients will receive the delivery depending on the chosen time zone here.

1. From the **[!UICONTROL Optimize the sending time per recipient]** drop-down menu, choose **[!UICONTROL Send at the recipient's time zone]**. 이를 통해 수신자는 2 월 14 일에 표준 시간대에 따라 발렌타인 데이 이메일을 받을 수 있습니다.

   ![](assets/send-time_opt_valentine_3.png)

1. After confirming your schedule for your delivery, click the **[!UICONTROL Prepare]** button then **[!UICONTROL Confirm]** your delivery.

   적어도 24 시간 전에 전송을 확인합니다. 그렇지 않으면 해당 위치에 따라 일부 수신자는 실제 발렌타인 데이 이벤트 이전에 배달을 받을 수 있습니다.

   ![](assets/send-time_opt_valentine_4.png)

모든 수신자는 2 월 14 일 오전 8 시 (현지 시간) 에 메시지를 받게 됩니다.
