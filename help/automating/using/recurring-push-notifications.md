---
solution: Campaign Standard
product: campaign
title: 워크플로우로 반복 푸시 알림 보내기
description: 이 예에서, 개인화된 푸시 알림은 시간대에 따라 매달 첫 번째 날 오후 8시에 모바일 애플리케이션 구독자에게 전송됩니다.
audience: automating
content-type: reference
topic-tags: channel-activities
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 4%

---


# 워크플로 {#sending-a-recurring-push-notification-with-a-workflow}(으)로 반복 푸시 알림 보내기

![](assets/wkf_push_example_1.png)

이 예에서, 개인화된 푸시 알림은 시간대에 따라 매달 첫 번째 날 오후 8시에 모바일 애플리케이션 구독자에게 전송됩니다.

워크플로우를 빌드하려면 다음 단계를 따르십시오.

1. [스케줄러](../../automating/using/scheduler.md) 활동을 사용하면 배달을 시작하기 전의 워크플로우 일을 시작하여 지정된 시간대의 오후 8시에 모든 가입자에게 알림을 보낼 수 있습니다.

   * **[!UICONTROL Execution frequency]** 필드에서 [월별]을 선택합니다.
   * **[!UICONTROL Time]** 필드에서 오후 8시를 선택합니다.
   * 매달 배달되는 날짜를 선택합니다.
   * 배달을 시작하기 최소 1일 전에 워크플로우의 시작 날짜를 선택합니다. 그렇지 않은 경우 선택한 시간이 이미 시간대에서 경과된 경우 일부 받는 사람이 하루 후에 메시지를 받을 수 있습니다.
   * **[!UICONTROL Execution options]** 탭에서 워크플로우가 시작될 시간대를 **[!UICONTROL Time zone]** 필드에서 선택합니다. 예를 들어, 워크플로우는 해당하는 모든 시간대에 대해 게재를 만들 수 있는 시간을 허용하기 위해 해당 월의 첫째 날 1주 전인 오후 8시(태평양 표준시)부터 시작됩니다.

   >[!NOTE]
   >
   >기본적으로 선택된 시간대는 워크플로우 속성에 정의된 시간대입니다([워크플로우 구축](../../automating/using/building-a-workflow.md) 참조).

   ![](assets/wkf_push_example_5.png)

1. [쿼리](../../automating/using/query.md) 활동을 통해 20-30세 사이의 VIP 고객을 대상으로 모바일 애플리케이션을 구독했고 보낸 이메일을 열지 않은 고객을 타깃팅할 수 있습니다.

   * 대상자(VIP 고객)를 선택하고 해당 나이를 필터링합니다.
   * **Subscriptions를 응용 프로그램** 요소에 드래그하여 작업 공간으로 놓습니다. **존재함**&#x200B;을 선택하고 사용할 모바일 응용 프로그램을 선택합니다.
   * 고객에게 보낸 이메일을 선택합니다.
   * **배달 로그(로그)** 요소를 작업 영역으로 드래그 앤 드롭하고 **존재**&#x200B;를 선택하여 이메일을 받은 모든 고객을 대상으로 합니다.
   * **추적 로그(추적)** 요소를 작업 영역으로 드래그 앤 드롭하고 **존재하지 않음**&#x200B;을 선택하여 이메일을 열지 않은 모든 고객을 대상으로 합니다.

      ![](assets/wkf_push_example_2.png)

1. [푸시 알림 배달](../../automating/using/push-notification-delivery.md) 활동을 통해 메시지의 내용을 입력하고 사용할 개인화 필드를 선택할 수 있습니다.

   * **[!UICONTROL Recurring notification]** 옵션을 선택합니다.
   * 푸시 알림 컨텐츠를 정의합니다. 푸시 알림 콘텐츠에 대한 자세한 내용은 이 [섹션](../../channels/using/preparing-and-sending-a-push-notification.md)을 참조하십시오.
   * **[!UICONTROL Schedule]** 블록에서 **[!UICONTROL Messages to be sent automatically on the time zone specified below]**&#x200B;을 선택합니다. 여기서 **[!UICONTROL Time zone of the contact date]** Pacific을 **[!UICONTROL Scheduler]** 워크플로우에서와 같이 선택했습니다.
   * **[!UICONTROL Optimize the sending time per recipient]** 필드에서 **[!UICONTROL Send at the recipient's time zone]**&#x200B;을(를) 선택합니다.

      ![](assets/wkf_push_example_4.png)

1. **[!UICONTROL Start]** 단추를 클릭하여 반복 워크플로우를 시작합니다.

   ![](assets/wkf_push_example_3.png)

워크플로우가 실행 중입니다. 선택한 시작 날짜(태평양 표준시 오후 8시)부터 시작되며 반복되는 푸시는 고객 시간대에 따라 해당 월의 첫 날 저녁 8시에 전송됩니다.**[!UICONTROL Scheduler]**
