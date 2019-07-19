---
title: 스케줄러
seo-title: 스케줄러
description: 스케줄러
seo-description: 스케줄러 활동을 사용하면 워크플로우나 활동이 시작될 때 일정을 예약할 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: F 5 E 50 A 11-8 DC 9-4 D 98-9531-024 C 0 FB 3 F 7 DA
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 실행 활동
discoiquuid: 0 FB 16 CEA -3941-404 F -899 C -33 F 81 CED 4 ED 5
context-tags: 일정, 기본
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 3e2081fc3377fe4edbdf3fb8c4765a9acda6d79e

---


# Scheduler{#scheduler}

## Description {#description}

![](assets/scheduler.png)

**[!UICONTROL Scheduler]** 활동을 사용하면 워크플로우나 활동이 시작될 때 일정을 예약할 수 있습니다.

## Context of use {#context-of-use}

**[!UICONTROL Scheduler]** 활동은 예약된 시작으로 간주해야 합니다. The activity positioning rules within the chart are the same as for the **[!UICONTROL Start]** activity. 이 활동에는 인바운드 전환이 없어야 합니다.

When building your workflow, only use one **[!UICONTROL Scheduler]** activity per branch and remember to set a time zone. 서버 시간대에서 실행되도록 설정되지 않습니다.

>[!CAUTION]
>
>The **[!UICONTROL Repetition frequency]** of the activity cannot be less than 10 minutes. 즉, 10 분마다 한 번 이상 워크플로우를 자동으로 실행할 수 없습니다.

## Configuration {#configuration}

1. **[!UICONTROL Scheduler]** 워크플로우를 워크플로우로 드래그하여 놓습니다.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. Specify the **[!UICONTROL Execution frequency]**:

   * **[!UICONTROL Once]**: 워크플로우는 한 번만 실행됩니다.
   * **[!UICONTROL Several times a day]**: 워크플로우는 하루에 여러 번 실행됩니다.
   * **[!UICONTROL Daily]**: 워크플로우는 하루에 한 번 특정 시간에 실행됩니다.
   * **[!UICONTROL Weekly]**: 워크플로우는 지정된 순간에 한 번 또는 여러 번 실행됩니다.
   * **[!UICONTROL Monthly]**: 워크플로우는 한 달에 한 번 또는 여러 번 지정된 시간에 실행됩니다.
   * **[!UICONTROL Yearly]**: 워크플로우는 지정된 시간, 한 번 또는 몇 번씩 실행됩니다.

1. 선택한 빈도에 따라 실행 세부 사항을 정의합니다. 세부 사항 필드는 사용된 빈도 (시간, 반복 빈도, 지정된 일 수 등) 에 따라 달라질 수 있습니다.

   >[!NOTE]
   >
   >**[!UICONTROL Repetition frequency]** 이 필드를 사용하여 워크플로우가 트리거되는 시간을 지울 수 있습니다. For example, if you select a daily execution period and the repetition frequency is set at **2** (days), the workflow will be triggered every two days. 10 분 이내여야 합니다. If the repetition frequency is set at **0** (also the default value), this option is not taken into account and the workflow will run according to the execution frequency specified.

1. 실행이 만료되는 시점을 지정합니다.

   * **[!UICONTROL Never]**: 워크플로우는 지정된 빈도에 따라 시간 프레임 또는 반복 수에 대한 제한 없이 실행됩니다.
   * **[!UICONTROL After a certain number of iterations]**: 워크플로우는 지정된 빈도에 따라 실행되며 **, 한도에** 도달할 때까지 증가합니다. The **[!UICONTROL Number of iterations]** will therefore need to be specified.
   * **[!UICONTROL On a specific date]**: 워크플로우는 지정된 빈도에 따라 특정 날짜까지 실행됩니다. 따라서 실행 마감 기간을 지정해야 합니다.

1. **[!UICONTROL Execution options]** 탭에서 **[!UICONTROL Time zone]** 필드에 스케줄러에 대한 시간대를 설정합니다. 이렇게 하면 특정 시간대에서 워크플로우를 시작할 수 있으며, 그렇지 않으면 기본적으로 서버 시간대에서 워크플로우가 실행됩니다.

   For more information on sending delivery depending on the recipient's time zone, refer to this [section](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md) or this [example](../../automating/using/push-notification-delivery.md#sending-a-recurring-push-notification-with-a-workflow) of a recurring workflow.

1. 활동의 구성을 확인하고 워크플로우를 저장합니다.

## Example {#example}

다음 예에서 활동은 정품이 확인되지 않은 기간 동안 매주 월요일 오전 7 시에 워크플로우를 시작하도록 구성됩니다.

![](assets/wkf_scheduler_example.png)

