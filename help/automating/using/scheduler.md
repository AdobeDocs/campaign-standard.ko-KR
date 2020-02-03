---
title: 예약
description: 스케줄러 활동을 사용하면 워크플로우 또는 활동이 시작될 때 예약할 수 있습니다.
page-status-flag: never-activated
uuid: f5e50a11-8dc9-4d98-9531-024c0fb3f7da
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities
discoiquuid: 0fb16cea-3941-404f-899c-33f81ced4ed5
context-tags: schedule,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 41ba6fa44807541dd749f4effca44ae2b4d147ae

---


# 예약{#scheduler}

## 설명 {#description}

![](assets/scheduler.png)

이 **[!UICONTROL Scheduler]**활동을 통해 워크플로우 또는 활동이 시작될 시기를 예약할 수 있습니다.

## 사용 상황 {#context-of-use}

활동은 **[!UICONTROL Scheduler]**예약된 시작으로 간주되어야 합니다. 차트 내의 활동 배치 규칙은**[!UICONTROL Start]** 활동과 동일합니다. 이 활동에는 인바운드 전환이 없어야 합니다.

워크플로우를 구축할 때는 분기당 하나의 **[!UICONTROL Scheduler]**활동만 사용하고 표준 시간대를 설정해야 합니다. 이렇게 하면 특정 시간대에서 워크플로우를 시작할 수 있습니다. 그렇지 않으면 워크플로우는 워크플로우 속성에 정의된 시간대에서 실행됩니다(워크플로우[구축](../../automating/using/building-a-workflow.md)참조).

>[!CAUTION]
>
>활동의 **[!UICONTROL Repetition frequency]**길이는 10분 미만이어야 합니다. 즉, 워크플로우는 10분마다 두 번 이상 자동으로 실행할 수 없습니다.

## 구성 {#configuration}

1. 워크플로우를 워크플로우로 드래그하여 **[!UICONTROL Scheduler]**놓을 수 있습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 엽니다.
1. 다음을 **[!UICONTROL Execution frequency]**지정합니다.

   * **[!UICONTROL Once]**:워크플로우가 한 번 실행됩니다.
   * **[!UICONTROL Several times a day]**:워크플로우는 하루에 여러 번 정기적으로 실행됩니다. 특정 시간 또는 정기적으로 실행을 설정할 수 있습니다.
   * **[!UICONTROL Daily]**:워크플로우는 하루에 한 번 특정 시간에 실행됩니다.
   * **[!UICONTROL Weekly]**:워크플로우는 지정된 순간에 일주일에 한 번 또는 여러 번 실행됩니다.
   * **[!UICONTROL Monthly]**:워크플로우는 한 달에 한 번 또는 여러 번 지정된 순간에 실행됩니다. 워크플로우를 실행해야 할 때 월을 선택할 수 있습니다. 월의 두 번째 화요일과 같이 지정된 평일 오전에 사형을 설정할 수도 있습니다.
   * **[!UICONTROL Yearly]**:워크플로우는 1년에 한 번 또는 여러 번 지정된 순간에 실행됩니다.

1. 선택한 빈도에 따라 실행 세부 사항을 정의합니다. 세부 사항 필드는 사용된 빈도(시간, 반복 빈도, 지정된 일 등)에 따라 달라질 수 있습니다.

   >[!NOTE]
   >
   >이 **[!UICONTROL Repetition frequency]**필드를 사용하면 워크플로우가 트리거되는 시간을 단축할 수 있습니다. 예를 들어 일일 실행 기간을 선택하고 반복 빈도를** 2 **(일)로 설정하면 워크플로우가 2일마다 트리거됩니다. 10분 이하여야 합니다. 반복 빈도를** 0 **(기본값)으로 설정하면 이 옵션이 고려되지 않고 지정된 실행 빈도에 따라 워크플로우가 실행됩니다.

1. 실행 만료 시기를 지정합니다.

   * **[!UICONTROL Never]**:지정된 빈도에 따라 시간 프레임 또는 반복 횟수에 제한이 없이 워크플로우가 실행됩니다.
   * **[!UICONTROL After a certain number of iterations]**:워크플로우는 X의 제한에 도달할 때까지 지정된 빈도에 따라**&#x200B;실행됩니다&#x200B;**. 따라서**[!UICONTROL Number of iterations]** 를 지정해야 합니다.
   * **[!UICONTROL On a specific date]**:특정 날짜까지 지정된 빈도에 따라 워크플로우가 실행됩니다. 따라서 실행 기한을 지정해야 합니다.

1. 을 클릭하여 워크플로우의 다음 10개 실행 일정을 **[!UICONTROL Preview next executions]**확인합니다.

1. 탭에서 **[!UICONTROL Execution options]****[!UICONTROL Time zone]** 필드에 스케줄러의 시간대를 설정합니다.

   받는 사람의 시간대에 따라 배달 보내기에 대한 자세한 내용은 이 [섹션](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md) 또는 반복되는 워크플로우의 [예를](../../automating/using/push-notification-delivery.md#sending-a-recurring-push-notification-with-a-workflow) 참조하십시오.

1. 활동 구성을 확인하고 워크플로우를 저장합니다.

## 예 {#example}

다음 예에서는 활동이 미확정 기간 동안 매주 월요일 오전 7시에 시작하도록 구성됩니다.

![](assets/wkf_scheduler_example.png)

