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
source-git-commit: 2d994d85f126951215f1227301599c554c1f12c8
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---


# 예약{#scheduler}

## 설명 {#description}

![](assets/scheduler.png)

이 **[!UICONTROL Scheduler]** 활동을 통해 워크플로우 또는 활동이 시작될 때 예약할 수 있습니다.

## 사용 상황 {#context-of-use}

활동은 **[!UICONTROL Scheduler]** 예약된 시작으로 간주되어야 합니다. 차트 내의 활동 배치 규칙은 활동과 동일합니다 **[!UICONTROL Start]** . 이 활동에는 인바운드 전환이 없어야 합니다.

워크플로우를 구축할 때는 분기당 하나의 **[!UICONTROL Scheduler]** 활동만 사용하고 표준 시간대를 설정해야 합니다. 이렇게 하면 특정 시간대에서 워크플로우를 시작할 수 있습니다. 그렇지 않으면 워크플로우는 워크플로우 속성에 정의된 시간대에서 실행됩니다(워크플로우 [작성 참조](../../automating/using/building-a-workflow.md)).

>[!CAUTION]
>
>활동 **[!UICONTROL Repetition frequency]** 의 길이는 10분을 초과할 수 없습니다. 즉, 10분마다 한 번 이상 워크플로우를 자동으로 실행할 수 없습니다.

**관련 항목:**

* [사용 사례: 프로필 생성 날짜에 배달 만들기](../../automating/using/workflow-creation-date-query.md)
* [사용 사례: 매주 화요일 이메일 배달 만들기](../../automating/using/workflow-weekly-offer.md)

## 구성 {#configuration}

1. 활동을 워크플로우로 드래그하여 **[!UICONTROL Scheduler]** 놓습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 활동을 엽니다.
1. 다음 항목을 지정합니다. **[!UICONTROL Execution frequency]**

   * **[!UICONTROL Once]**: 워크플로우가 한 번 실행됩니다.
   * **[!UICONTROL Several times a day]**: 워크플로우는 하루에 여러 번 정기적으로 실행됩니다. 특정 시간 또는 정기적으로 실행을 설정할 수 있습니다.
   * **[!UICONTROL Daily]**: 워크플로우는 특정 시간에 하루에 한 번 실행됩니다.
   * **[!UICONTROL Weekly]**: 워크플로우는 지정된 순간에 일주일에 한 번 또는 여러 번 실행됩니다.
   * **[!UICONTROL Monthly]**: 워크플로우는 한 달에 한 번 또는 여러 번 지정된 시점에 실행됩니다. 워크플로우를 실행해야 할 때 월을 선택할 수 있습니다. 달의 두 번째 화요일과 같이, 해당 월의 지정된 평일에 실행을 설정할 수도 있습니다.
   * **[!UICONTROL Yearly]**: 워크플로우는 1년에 한 번 또는 여러 번 지정된 시점에 실행됩니다.

1. 선택한 빈도에 따라 실행 세부 사항을 정의합니다. 세부 정보 필드는 사용되는 빈도(시간, 반복 빈도, 지정된 일 등)에 따라 달라질 수 있습니다.

   >[!NOTE]
   >
   >이 **[!UICONTROL Repetition frequency]** 필드를 사용하면 워크플로가 트리거되는 시간을 간격을 지정할 수 있습니다. 예를 들어 일일 실행 기간을 선택하고 반복 빈도를 **2** (일)로 설정하면 워크플로우가 2일마다 트리거됩니다. 10분 이하여야 합니다. 반복 빈도를 **0** (기본값이기도 함)으로 설정하면 이 옵션을 고려하지 않고 지정된 실행 빈도에 따라 워크플로우가 실행됩니다.

1. 실행 만료 시기를 지정합니다.

   * **[!UICONTROL Never]**: 지정된 빈도에 따라 시간 프레임 또는 반복 횟수에 제한이 없이 워크플로우가 실행됩니다.
   * **[!UICONTROL After a certain number of iterations]**: 워크플로우는 지정된 빈도에 따라 최대 **X** 제한에 도달할 때까지 실행됩니다. 따라서 **[!UICONTROL Number of iterations]** 을 지정해야 합니다.
   * **[!UICONTROL On a specific date]**: 특정 날짜까지 지정된 빈도에 따라 워크플로우가 실행됩니다. 따라서 실행 기한을 지정해야 합니다.

1. 을 클릭하여 워크플로우의 다음 10개 실행 일정을 확인합니다 **[!UICONTROL Preview next executions]**.

1. 탭에서 **[!UICONTROL Execution options]** 필드에 스케줄러의 시간대를 **[!UICONTROL Time zone]** 설정합니다.

   받는 사람의 시간대에 따라 배달 보내기에 대한 자세한 내용은 이 [섹션](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md) 또는 반복되는 워크플로우의 [예를](../../automating/using/recurring-push-notifications.md) 참조하십시오.

1. 활동 구성을 확인하고 워크플로우를 저장합니다.

## 예 {#example}

다음 예에서 활동은 정해지지 않은 기간 동안 매주 월요일 오전 7시에 워크플로우를 시작하도록 구성되어 있습니다.

![](assets/wkf_scheduler_example.png)

