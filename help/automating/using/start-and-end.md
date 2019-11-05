---
title: 시작 및 종료
description: 시작 및 종료 활동을 사용하면 워크플로우의 시작과 끝을 명확하게 표시할 수 있습니다.
page-status-flag: 활성화 안 함
uuid: 146b6337-122c-453d-8ffd-5c157db29217
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 자동화
content-type: reference
topic-tags: 실행 활동
discoiquuid: a0a8a725-8ede-4626-9798-b86924b58beb
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 시작 및 종료{#start-and-end}

## 설명 {#description}

![](assets/start.png)

![](assets/end.png)

이 **[!UICONTROL Start]** 및 **[!UICONTROL End]** 활동을 통해 워크플로우의 시작과 끝을 명확하게 표시할 수 있습니다.

## 사용 상황 {#context-of-use}

워크플로우 실행은 인바운드 전환 없이 활동으로 시작하고 더 이상 진행 중인 작업이 없을 때 중지됩니다. 그러나 워크플로우의 시작 지점과 종료 지점을 명확하게 표시하는 **[!UICONTROL Start]** 및 **[!UICONTROL End]** 활동을 추가할 수 있습니다. 이는 특히 상대적으로 복잡한 워크플로우에 유용합니다.

워크플로우가 제대로 종료되도록 워크플로우의 마지막 전환을 그대로 두는 대신 **[!UICONTROL End]** 활동을 사용하는 것이 좋습니다.

## 구성 {#configuration}

1. 워크플로우로 **[!UICONTROL Start]** 또는 **[!UICONTROL End]** 활동을 드래그하여 놓을 수 있습니다.
1. 활동을 쿼리와 같은 다른 활동 앞에 놓고 일련의 활동 후에 **[!UICONTROL Start]** **[!UICONTROL End]** 활동을 표시합니다.
1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 엽니다.
1. 완료되지 않은 **작업을 포함하여** 워크플로우의 진행 중인 모든 작업을 중단하도록 끝 개체를 구성할 수 있습니다. 이렇게 하려면 해당 옵션을 선택합니다.
1. 활동 구성을 확인하고 워크플로우를 저장합니다.

## 다른 워크플로우 트리거 {#triggering-another-workflow}

활동의 **[!UICONTROL External signal]** **[!UICONTROL End]** 탭을 사용하여 다른 워크플로우를 트리거할 수 있습니다. 외부 신호 [섹션을 참조하십시오](../../automating/using/external-signal.md) .

## 예 {#example}

다음 예에서는 **[!UICONTROL Start]** 활동 및 여러 **[!UICONTROL End]** 활동과 함께 복잡한 워크플로우가 실행되는 방법을 보여줍니다. 첫 번째 **[!UICONTROL Stop all tasks in progress]** 활동에 대해 **[!UICONTROL End]** 상자가 선택되었습니다. 해당 작업이 완료되면 전체 워크플로우가 중지됩니다.단추를 선택한 것과 동일한 효과가 나타납니다(작업 표시줄 ![](assets/stop_darkgrey-24px.png) 섹션 [](../../automating/using/workflow-interface.md#action-bar) 참조).

![](assets/wkf_start_end_example.png)

