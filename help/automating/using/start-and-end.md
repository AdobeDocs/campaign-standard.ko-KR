---
title: 시작 및 종료
seo-title: 시작 및 종료
description: 시작 및 종료
seo-description: 시작 및 종료 활동을 사용하면 워크플로우가 시작되고 끝나는 위치를 명확하게 표시할 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 146 B 6337-122 c -453 D -8 FFD -5 C 157 DB 29217
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 실행 활동
discoiquuid: A 0 A 8 A 725-8 EDE -4626-9798-B 86924 B 58 BEB
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Start and end{#start-and-end}

## Description {#description}

![](assets/start.png)

![](assets/end.png)

**[!UICONTROL Start]** AND **[!UICONTROL End]** 활동을 통해 워크플로우가 시작되고 끝나는 위치를 명확히 표시할 수 있습니다.

## Context of use {#context-of-use}

워크플로우 실행은 인바운드 전환이 없는 활동으로 시작되고 더 이상 진행 중인 작업이 없을 때 중지됩니다. Nevertheless, you can add **[!UICONTROL Start]** and **[!UICONTROL End]** activities to clearly mark the starting and ending points of a workflow. 이 기능은 비교적 복잡한 워크플로우에 특히 유용합니다.

It is a best practice to use an **[!UICONTROL End]** activity instead of leaving the last transition of a workflow on its own to ensure that the workflow properly ends.

## Configuration {#configuration}

1. Drag and drop a **[!UICONTROL Start]** or **[!UICONTROL End]** activity into your workflow.
1. Put the **[!UICONTROL Start]** activity in front of other activities such as queries, and the **[!UICONTROL End]** activity after a series of activities.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. You can configure the **End** object so that it interrupts all of the workflow's ongoing tasks, including those that have not finished. 이렇게 하려면 해당 옵션을 선택합니다.
1. 활동의 구성을 확인하고 워크플로우를 저장합니다.

## Triggering another workflow {#triggering-another-workflow}

Using the **[!UICONTROL External signal]** tab of an **[!UICONTROL End]** activity, you can trigger another workflow. Refer to the [External signal](../../automating/using/external-signal.md) section.

## Example {#example}

The following example shows how a complex workflow is executed with a **[!UICONTROL Start]** activity and several **[!UICONTROL End]** activities. **[!UICONTROL Stop all tasks in progress]** 상자에 **[!UICONTROL End]** 첫 번째 활동이 있는지 확인되었습니다. Once the corresponding task is finished, the entire workflow will be stopped: it will have the same effect as if the ![](assets/stop_darkgrey-24px.png) button had been selected (refer to the [Action bar](../../automating/using/workflow-interface.md#action-bar) section)

![](assets/wkf_start_end_example.png)

