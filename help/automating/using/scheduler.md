---
solution: Campaign Standard
product: campaign
title: 예약
description: 예약 활동을 통해 워크플로우나 활동의 시작 시점을 예약할 수 있습니다.
audience: automating
content-type: reference
topic-tags: execution-activities
context-tags: schedule,main
translation-type: tm+mt
source-git-commit: 9b76f02b03ba1180f852b446f0dbbae26a27d4bd
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 89%

---


# 예약{#scheduler}

## 설명 {#description}

![](assets/scheduler.png)

**[!UICONTROL Scheduler]** 활동을 통해 워크플로우나 활동의 시작 시점을 예약할 수 있습니다.

## 사용의 컨텍스트 {#context-of-use}

**[!UICONTROL Scheduler]** 활동은 시작을 예약하는 것으로 생각해야 합니다. 차트 내에서의 활동 위치 지정 규칙은 **[!UICONTROL Start]** 활동과 동일합니다. 이 활동에는 인바운드 전환이 없어야 합니다.

워크플로우를 구축할 때는 분기당 **[!UICONTROL Scheduler]** 활동을 하나씩만 사용하고 표준 시간대를 설정해야 합니다. 이를 통해 특정 시간대에 맞추어 워크플로우를 시작할 수 있습니다. 그렇지 않으면 워크플로우는 워크플로우 속성에 정의된 시간대에 맞추어 실행됩니다([워크플로우 구축](../../automating/using/building-a-workflow.md) 참조).

>[!CAUTION]
>
>**[!UICONTROL Repetition frequency]** 활동은 10분 이상이어야 합니다. 즉, 워크플로우를 10분에 2번 이상 자동으로 실행할 수 없습니다.

여러 활동이 포함된 예약된 워크플로우를 디자인할 때 작업이 완료될 때까지 워크플로우의 일정을 조정하지 않아야 합니다. 이렇게 하려면 이전에 수행한 하나 이상의 작업이 아직 보류 중일 때 해당 작업을 실행하지 않도록 워크플로우를 구성해야 합니다. 자세한 정보는 이 [페이지](../../automating/using/scheduled-workflows-execution.md)를 참조하십시오.

**관련 항목:**

* [사용 사례:프로필 생성 날짜에 배달 만들기](../../automating/using/workflow-creation-date-query.md)
* [사용 사례:매주 화요일 이메일 배달 만들기](../../automating/using/workflow-weekly-offer.md)

## 구성 {#configuration}

1. **[!UICONTROL Scheduler]** 활동을 워크플로우로 끌어서 놓습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업에서 ![](assets/edit_darkgrey-24px.png) 버튼을 사용하여 활동을 엽니다.
1. **[!UICONTROL Execution frequency]**&#x200B;을(를) 지정합니다. 

   * **[!UICONTROL Once]**: 워크플로우가 한 번 실행됩니다.
   * **[!UICONTROL Several times a day]**: 워크플로우가 하루에 여러 번 규칙적으로 실행됩니다. 특정 시간에 실행되거나 주기적으로 실행되도록 설정할 수 있습니다.
   * **[!UICONTROL Daily]**: 워크플로우가 하루에 한 번, 지정한 시간에 실행됩니다.
   * **[!UICONTROL Weekly]**: 워크플로우가 일주일에 한 번 또는 여러 번, 지정한 시점에 실행됩니다.
   * **[!UICONTROL Monthly]**: 워크플로우가 한 달에 한 번 또는 여러 번, 지정한 시점에 실행됩니다. 워크플로우를 실행할 달을 선택할 수 있습니다. 해당 월의 지정 요일, 예를 들어 해당 월의 두 번째 화요일에 실행되도록 설정할 수도 있습니다.
   * **[!UICONTROL Yearly]**: 워크플로우가 1년에 한 번 또는 여러 번, 지정한 시점에 실행됩니다.

1. 선택한 빈도에 따라 실행의 세부 정보를 정의합니다. 세부 정보 필드는 사용하는 빈도(시간, 반복 빈도, 지정된 날짜 등)에 따라 달라질 수 있습니다.

   >[!NOTE]
   >
   >**[!UICONTROL Repetition frequency]** 필드를 사용하면 워크플로우가 트리거되는 시간 사이에 간격을 지정할 수 있습니다. 예를 들어 실행 주기를 일 단위로 선택하고 반복 빈도를 **2**(일)로 설정하면 워크플로우가 2일마다 트리거됩니다. 이는 10분 이상이어야 합니다. 반복 빈도를 **0**(기본값)으로 설정한 경우 이 옵션은 고려하지 않고, 지정한 실행 빈도에 따라 워크플로우가 실행됩니다.

1. 실행 만료 시기를 지정합니다.

   * **[!UICONTROL Never]**: 워크플로우가 시간 프레임이나 반복 횟수 제한 없이 지정한 빈도대로 실행됩니다.
   * **[!UICONTROL After a certain number of iterations]**: 워크플로우가 최대 **X** 제한에 도달할 때까지 지정한 빈도대로 실행됩니다. 따라서 **[!UICONTROL Number of iterations]**&#x200B;을(를) 지정해야 합니다.
   * **[!UICONTROL On a specific date]**: 워크플로우가 특정 날짜까지 지정한 빈도대로 실행됩니다. 따라서 실행 기한을 지정해야 합니다.

1. **[!UICONTROL Preview next executions]**&#x200B;을(를) 클릭하여 워크플로우의 다음 10개의 실행 일정을 확인합니다 .

1. **[!UICONTROL Execution options]** 탭에서 **[!UICONTROL Time zone]** 필드에 예약의 시간대를 설정합니다.

   수신자의 시간대에 따라 게재를 보내는 방법에 대한 자세한 내용은 이 [섹션](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md) 또는 되풀이하는 워크플로우에 대한 [예제](../../automating/using/recurring-push-notifications.md)를 참조하십시오.

1. 활동 구성을 확인하고 워크플로우를 저장합니다.

## 예제 {#example}

다음 예제에서는 정해지지 않은 기간 동안 매주 월요일 오전 7시에 워크플로우를 시작하도록 활동을 구성했습니다.

![](assets/wkf_scheduler_example.png)

