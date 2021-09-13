---
title: 워크플로우로 되풀이하는 푸시 알림 보내기
description: 이 예에서는 개인화된 푸시 알림이 시간대에 따라 모바일 애플리케이션 구독자에게 매월 첫 날 오후 8시에 전송됩니다.
audience: automating
content-type: reference
topic-tags: channel-activities
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: d5e6034c-3673-4069-ac0b-49c7ad07259d
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 4%

---

# 워크플로우로 되풀이하는 푸시 알림 보내기 {#sending-a-recurring-push-notification-with-a-workflow}

![](assets/wkf_push_example_1.png)

이 예에서는 개인화된 푸시 알림이 시간대에 따라 모바일 애플리케이션 구독자에게 매월 첫 날 오후 8시에 전송됩니다.

워크플로우를 빌드하려면 다음 단계를 수행합니다.

1. [스케줄러](../../automating/using/scheduler.md) 활동을 사용하면 게재 시작 전 워크플로우 일수를 시작하여 지정된 시간대의 오후 8시에 모든 구독자에게 알림을 보낼 수 있습니다.

   * **[!UICONTROL Execution frequency]** 필드에서 월별 을 선택합니다.
   * **[!UICONTROL Time]** 필드에서 오후 8시를 선택합니다.
   * 매월 게재를 보낼 날짜를 선택합니다.
   * 게재 시작 1일 전까지 워크플로우의 시작 날짜를 선택합니다. 그렇지 않으면 일부 수신자는 선택한 시간이 이미 시간대에서 경과한 경우 메시지를 하루 늦게 수신할 수 있습니다.
   * **[!UICONTROL Execution options]** 탭에서 워크플로우가 **[!UICONTROL Time zone]** 필드에서 시작할 시간대를 선택합니다. 예를 들어 워크플로우는 적용 가능한 모든 시간대에서 게재를 만들 수 있도록 해당 월의 첫 날 1주일 전에 태평양 표준시 오후 8시에 시작됩니다.

   >[!NOTE]
   >
   >기본적으로 선택된 시간대는 워크플로우 속성에 정의된 시간대입니다([워크플로우 구축](../../automating/using/building-a-workflow.md) 참조).

   ![](assets/wkf_push_example_5.png)

1. [Query](../../automating/using/query.md) 활동을 사용하면 20~30세 사이의 VIP 고객을 타깃팅할 수 있습니다. 20~30세 사이이며, 모바일 애플리케이션을 구독했으며 보낸 이메일을 열지 않았습니다.

   * 대상(VIP 고객)을 선택하고 해당 나이에 따라 필터링합니다.
   * **애플리케이션** 요소에 대한 구독을 작업 영역으로 끌어다 놓습니다. **존재함**&#x200B;을 선택하고 사용할 모바일 애플리케이션을 선택합니다.
   * 고객에게 보낸 이메일을 선택합니다.
   * **게재 로그(로그)** 요소를 작업 영역으로 끌어다 놓고 **존재함**&#x200B;을 선택하여 이메일을 받은 모든 고객을 타겟팅합니다.
   * **추적 로그(추적)** 요소를 작업 영역으로 끌어다 놓고 **존재하지 않음**&#x200B;을 선택하여 이메일을 열지 않은 모든 고객을 타겟팅합니다.

      ![](assets/wkf_push_example_2.png)

1. [푸시 알림 전달](../../automating/using/push-notification-delivery.md) 활동을 사용하면 메시지의 콘텐츠를 입력하고 사용할 개인화 필드를 선택할 수 있습니다.

   * **[!UICONTROL Recurring notification]** 옵션을 선택합니다.
   * 푸시 알림 콘텐츠를 정의합니다. 푸시 알림 콘텐츠에 대한 자세한 내용은 이 [섹션](../../channels/using/preparing-and-sending-a-push-notification.md)을 참조하십시오.
   * **[!UICONTROL Schedule]** 블록에서 **[!UICONTROL Messages to be sent automatically on the time zone specified below]** 을 선택합니다. 여기에서는 워크플로우 **[!UICONTROL Scheduler]**&#x200B;에서와 같이 **[!UICONTROL Time zone of the contact date]** 태평양을 선택했습니다.
   * **[!UICONTROL Optimize the sending time per recipient]** 필드에서 **[!UICONTROL Send at the recipient's time zone]**&#x200B;을(를) 선택합니다.

      ![](assets/wkf_push_example_4.png)

1. 반복 워크플로우를 시작하려면 **[!UICONTROL Start]** 단추를 클릭하십시오.

   ![](assets/wkf_push_example_3.png)

이제 워크플로우가 실행 중입니다. 선택한 **[!UICONTROL Scheduler]** 시작일(태평양 표준시)부터 시작되며 반복 푸시는 고객 시간대에 따라 매월 첫 날 오후 8시에 전송됩니다.
