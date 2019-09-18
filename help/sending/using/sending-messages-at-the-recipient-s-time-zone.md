---
title: 받는 사람의 시간대에서 메시지 보내기
seo-title: 받는 사람의 시간대에서 메시지 보내기
description: 받는 사람의 시간대에서 메시지 보내기
seo-description: 수신자의 시간대에서 메시지를 보내는 방법을 알아봅니다.
page-status-flag: 활성화 안 함
uuid: 70228c07-451f-4ddb-8d26-92a5a4814e3a
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 보내기
content-type: reference
topic-tags: 예약 메시지
discoiquuid: daa980ba-8c7c-4673-a68f-379d63e4b8bd
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 781904d58f520987e978ad5d1cdc9e34871ca876

---


# 받는 사람의 시간대에서 메시지 보내기{#sending-messages-at-the-recipient-s-time-zone}

날짜와 시간이 중요한 캠페인을 관리할 때 각 수신자의 현지 시간을 고려하여 배달을 예약할 수 있습니다.이메일, SMS 또는 푸시 알림을 사용자가 예약된 시간에 수신하게 됩니다.

>[!NOTE]
>
>이 기능을 사용하려면 게재에 의해 타깃팅된 모든 프로필에 속성 **[!UICONTROL Address]** 섹션에 지정된 시간대가 있는지 확인합니다. 프로필 속성에 액세스하는 방법에 대한 자세한 내용은 이 [섹션을](../../audiences/using/editing-profiles.md)참조하십시오.

받는 사람의 시간대에서 배달을 보내려면 워크플로우에서 **[!UICONTROL Scheduler]** 활동을 사용할 수도 있습니다. 자세한 내용은 이 [페이지를](../../automating/using/scheduler.md)참조하십시오.

다음 예에서는 발렌타인데이에만 유효한 프로모션 코드를 전 세계 모든 고객에게 전송하려고 합니다. 하루 동안 사용할 수 있는 충분한 시간을 제공하기 위해 모든 고객은 시간대에 따라 2월 14일 오전 8시에 메시지를 수신해야 합니다.

1. 탭에서 이메일 배달 만들기를 **[!UICONTROL Marketing activities]** 시작합니다. 배달 생성에 대한 자세한 내용은 이 [섹션을](../../channels/using/creating-an-email.md)참조하십시오.
1. 발렌타인 데이 이메일을 디자인한 후 을 클릭하여 배달 대시보드에 **[!UICONTROL Create]** 액세스합니다. 이메일 디자인에 대한 자세한 내용은 이 [페이지를](../../designing/using/personalization.md#example-email-personalization)참조하십시오.

   ![](assets/send-time_opt_valentine_1.png)

1. 배달 대시보드에서 **[!UICONTROL Schedule]** 블록을 선택합니다.

   ![](assets/send-time_opt_valentine_2.png)

1. 아래에 지정된 **[!UICONTROL Messages to be sent automatically on the date]** 옵션을 선택합니다. 그런 다음, **[!UICONTROL Start sending from]** 필드에서 2월 14일 오전 8시에 연락처 날짜를 설정하여 모든 수신자가 발렌타인 데이에 이 날짜를 받도록 하십시오.

   ![](assets/send-time_opt_valentine.png)

1. 필드에서 기본적으로 배달을 보낼 시간대를 선택합니다. **[!UICONTROL Time zone of the contact date]**

   프로파일이 **[!UICONTROL Time zone]** 로 남아 **[!UICONTROL Default]**&#x200B;있는 경우 수신자는 여기에서 선택한 시간대에 따라 배달을 받습니다.

1. 드롭다운 **[!UICONTROL Optimize the sending time per recipient]** 메뉴에서 선택합니다 **[!UICONTROL Send at the recipient's time zone]**. 이는 수신자가 표준 시간대에 따라 2월 14일에 발렌타인 데이 이메일을 받을 수 있도록 해줍니다.

   ![](assets/send-time_opt_valentine_3.png)

1. 배달 일정을 확인한 후 **[!UICONTROL Prepare]** 단추를 클릭한 다음 배달을 **[!UICONTROL Confirm]** 클릭합니다.

   적어도 24시간 전에 발송 여부를 확인하십시오. 그렇지 않은 경우, 위치에 따라, 일부 수신자는 실제 발렌타인 데이에 앞서 배달을 받을 수 있습니다.

   ![](assets/send-time_opt_valentine_4.png)

모든 수신자는 어디에 있든 2월 14일 오전 8시에 메시지를 수신하게 됩니다.
