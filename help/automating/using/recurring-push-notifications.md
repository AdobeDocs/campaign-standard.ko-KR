---
title: 워크플로우로 반복 푸시 알림 보내기
description: 이 예에서는 개인화된 푸시 알림이 시간대에 따라 매월 1일 오후 8시에 모바일 애플리케이션 구독자에게 전송됩니다
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: d5e6034c-3673-4069-ac0b-49c7ad07259d
source-git-commit: 0ab950d4124bf459ba889e2f1c2954210dd350e0
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 4%

---

# 워크플로우로 반복 푸시 알림 보내기 {#sending-a-recurring-push-notification-with-a-workflow}

![](assets/wkf_push_example_1.png)

이 예에서는 개인화된 푸시 알림이 시간대에 따라 매월 1일 오후 8시에 모바일 애플리케이션 구독자에게 전송됩니다.

워크플로우를 빌드하려면 다음 단계를 수행합니다.

1. 다음 [스케줄러](../../automating/using/scheduler.md) 활동을 사용하면 게재 시작 며칠 전에 워크플로우를 시작하여 지정된 시간대의 오후 8시에 모든 구독자에게 알림을 전송할 수 있습니다.

   * 다음에서 **[!UICONTROL Execution frequency]** 필드에서 월간을 선택합니다.
   * 다음 목록에서 오후 8시 선택 **[!UICONTROL Time]** 필드.
   * 매월 게재를 보낼 날짜를 선택합니다.
   * 게재 시작 최소 하루 전에 워크플로우 시작 날짜를 선택하십시오. 그렇지 않은 경우, 선택한 시간이 이미 표준 시간대에 지난 경우 일부 수신자는 하루 뒤에 메시지를 받을 수 있습니다.
   * 다음에서 **[!UICONTROL Execution options]** 탭에서 워크플로우가 시작될 시간대를 선택합니다. **[!UICONTROL Time zone]** 필드. 예를 들어 워크플로우는 적용 가능한 모든 시간대에 대해 게재를 만들 수 있는 시간을 허용하기 위해 태평양 표준시 오후 8시에 시작되며, 해당 월의 첫 번째 날 1주일 전에 시작됩니다.

   >[!NOTE]
   >
   >기본적으로 선택된 시간대는 워크플로우 속성에 정의된 시간대입니다([워크플로우 구축](../../automating/using/building-a-workflow.md) 참조).

   ![](assets/wkf_push_example_5.png)

1. 다음 [쿼리](../../automating/using/query.md) 활동을 통해 20~30세 사이의 VIP 고객, 모바일 애플리케이션을 구독했으며 보낸 이메일을 열지 않은 고객을 타겟팅할 수 있습니다.

   * 대상자(VIP 고객)를 선택하고 연령을 기준으로 필터링합니다.
   * 을(를) 끌어다 놓습니다. **애플리케이션에 대한 구독** 요소를 작업 공간에 추가합니다. 선택 **존재함** 을 클릭하고 사용할 모바일 애플리케이션을 선택합니다.
   * 고객에게 보낸 이메일을 선택합니다.
   * 을(를) 끌어다 놓습니다. **게재 로그(로그)** 요소를 작업 공간에 입력하고 다음을 선택합니다. **존재함** 이메일을 받은 모든 고객을 타겟팅합니다.
   * 을(를) 끌어다 놓습니다. **추적 로그(추적)** 요소를 작업 공간에 입력하고 다음을 선택합니다. **존재하지 않음** 이메일을 열지 않은 모든 고객을 타겟팅합니다.

     ![](assets/wkf_push_example_2.png)

1. 다음 [푸시 알림 게재](../../automating/using/push-notification-delivery.md) 활동을 통해 메시지 콘텐츠를 입력하고 사용할 개인화 필드를 선택할 수 있습니다.

   * 다음 항목 선택 **[!UICONTROL Recurring notification]** 옵션을 선택합니다.
   * 푸시 알림 콘텐츠를 정의합니다. 푸시 알림 콘텐츠에 대한 자세한 내용은 다음을 참조하십시오. [섹션](../../channels/using/preparing-and-sending-a-push-notification.md).
   * 다음에서 **[!UICONTROL Schedule]** 블록, 선택 **[!UICONTROL Messages to be sent automatically on the time zone specified below]**. 여기에서 **[!UICONTROL Time zone of the contact date]** 워크플로우의 태평양 **[!UICONTROL Scheduler]**.
   * **[!UICONTROL Optimize the sending time per recipient]** 필드에서 **[!UICONTROL Send at the recipient's time zone]**&#x200B;을(를) 선택합니다.

     ![](assets/wkf_push_example_4.png)

1. 다음을 클릭합니다. **[!UICONTROL Start]** 단추를 클릭하여 반복 워크플로우를 시작합니다.

   ![](assets/wkf_push_example_3.png)

워크플로우가 현재 실행 중입니다. 선택한 의 시작 날짜에 시작됩니다. **[!UICONTROL Scheduler]** 태평양 표준시 오후 8시에 반복 푸시가 고객 시간대에 따라 매월 1일 오후 8시에 전송됩니다.
