---
solution: Campaign Standard
product: campaign
title: 수신자의 시간대에 맞추어 메시지 보내기
description: 수신자의 시간대에 맞추어 메시지 보내는 방법에 대해 알아봅니다.
audience: sending
content-type: reference
topic-tags: sheduling-messages
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 100%

---


# 수신자의 시간대에 맞추어 메시지 보내기{#sending-messages-at-the-recipient-s-time-zone}

날짜와 시간이 중요한 캠페인을 관리할 때 각 수신자의 현지 시간을 고려하여 게재를 예약할 수 있습니다. 수신자는 사용자가 예약한 시간에 이메일, SMS 또는 푸시 알림을 수신자의 시간대에 받게 됩니다.

>[!NOTE]
>
>이 기능을 사용하려면 게재 대상의 모든 프로필에 속성의 **[!UICONTROL Address]** 섹션에서 지정한 시간대가 있는지 확인해야 합니다. 프로필 속성 액세스에 대한 자세한 내용은 이 [섹션](../../audiences/using/editing-profiles.md)을 참조하십시오.

수신자의 시간대에 게재를 보내려면 워크플로우에서 **[!UICONTROL Scheduler]** 활동을 사용할 수도 있습니다. 자세한 정보는 이 [페이지](../../automating/using/scheduler.md)를 참조하십시오.

다음 예에서는 발렌타인 데이에만 유효한 프로모션 코드를 전 세계 모든 고객에게 전송하려고 합니다. 하루 동안 사용하기에 충분한 시간을 제공하기 위해 모든 고객은 시간대에 따라 2월 14일 오전 8시에 메시지를 수신해야 합니다.

1. **[!UICONTROL Marketing activities]** 탭에서 게재 만들기를 시작합니다(이 예제의 경우 이메일). 게재 만들기에 대한 자세한 내용은 이 [섹션](../../channels/using/creating-an-email.md)을 참조하십시오.
1. 발렌타인 데이 이메일을 디자인한 후 **[!UICONTROL Create]**&#x200B;을(를) 클릭하여 게재 대시보드에 액세스합니다. 이메일 디자인에 대한 자세한 내용은 이 [페이지](../../designing/using/personalization.md#example-email-personalization)를 참조하십시오.

   ![](assets/send-time_opt_valentine_1.png)

1. 게재 대시보드에서 **[!UICONTROL Schedule]** 블록을 선택합니다.

   ![](assets/send-time_opt_valentine_2.png)

1. 아래에 지정된 **[!UICONTROL Messages to be sent automatically on the date]** 옵션을 선택합니다. 그런 다음 **[!UICONTROL Start sending from]** 필드에서 연락 날짜를 설정하여(이 예제의 경우 2월 14일 오전 8시) 모든 수신자가 발렌타인 데이에 받을 수 있도록 합니다.

   ![](assets/send-time_opt_valentine.png)

1. **[!UICONTROL Time zone of the contact date]** 필드에서 기본적으로 게재를 보낼 시간대를 선택합니다.

   프로필의 **[!UICONTROL Time zone]**&#x200B;을(를) **[!UICONTROL Default]**(으)로 남겨두면 수신자는 여기에서 선택한 시간대에 따라 게재를 받습니다.

1. **[!UICONTROL Optimize the sending time per recipient]** 드롭다운 메뉴에서 **[!UICONTROL Send at the recipient's time zone]**&#x200B;을(를) 선택합니다. 이를 통해 수신자는 시간대에 따라 2월 14일에 발렌타인 데이 이메일을 받을 수 있습니다.

   ![](assets/send-time_opt_valentine_3.png)

1. 게재 일정을 확인한 후 **[!UICONTROL Prepare]** 버튼을 클릭한 다음 게재를 **[!UICONTROL Confirm]**&#x200B;합니다.

   적어도 24시간 전에 전송을 확인해야 합니다. 그렇지 않으면, 위치에 따라 일부 수신자는 실제 발렌타인 데이 행사 전에 게재를 받을 수도 있습니다.

   ![](assets/send-time_opt_valentine_4.png)

어디에 있든 모든 수신자는 2월 14일, 현지시간으로 오전 8시에 메시지를 받게 됩니다.
