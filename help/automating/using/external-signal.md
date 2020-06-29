---
title: 외부 신호
description: 외부 신호 활동은 다른 워크플로우에서 일부 조건이 성공적으로 충족되면 워크플로우를 트리거합니다.
page-status-flag: never-activated
uuid: 884b6daf-bfd9-440b-8336-004b80c76def
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities
discoiquuid: 911c71b5-da8b-4916-b645-13bba6d21715
context-tags: signal,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 16afc307df6902584624d6457954a472b11c5129
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 3%

---


# 외부 신호{#external-signal}

## 설명 {#description}

![](assets/signal.png)

다른 워크플로우 또는 REST API 호출에서 일부 조건이 성공적으로 충족되면 **[!UICONTROL External signal]** 활동이 워크플로우를 트리거합니다.

## 사용 상황 {#context-of-use}

이 **[!UICONTROL External signal]** 활동은 동일한 고객 경로의 일부이며 다양한 워크플로우로 이어지는 여러 프로세스를 구성하고 조정하는 데 사용됩니다. 따라서 다른 워크플로우에서 워크플로우를 시작할 수 있으므로 복잡한 고객 여정을 지원할 수 있고 문제가 발생하는 경우 보다 효과적으로 모니터링하고 대응할 수 있습니다.

이 **[!UICONTROL External signal]** 활동은 워크플로우의 첫 번째 활동으로 배치됩니다. 다른 워크플로우의 **[!UICONTROL End]** 활동이나 REST API 호출에서 트리거될 수 있습니다(자세한 내용은 [API 설명서 참조](../../api/using/triggering-a-signal-activity.md)).

트리거되면 외부 매개 변수를 정의할 수 있으며 워크플로우 이벤트 변수에서 사용할 수 있습니다. 외부 매개 변수를 사용하는 워크플로우를 호출하는 프로세스는 [이 섹션에 자세히 설명되어 있습니다](../../automating/using/calling-a-workflow-with-external-parameters.md).

>[!NOTE]
>
>활동이 10분마다 이상 트리거되지 않습니다.

여러 가지 다른 이벤트에서 활동을 **[!UICONTROL External signal]** 트리거할 수 있습니다. 이 경우 소스 워크플로우 또는 API 호출 중 하나 **[!UICONTROL External signal]** 가 실행되면 트리거됩니다. 모든 소스 워크플로우가 끝나지 않아도 됩니다.

**관련 항목**

* [사용 사례: 외부 신호 활동 및 데이터 가져오기](../../automating/using/external-signal-data-import.md).
* [사용 사례: 외부 매개 변수를 사용하여 파일에서 대상을 만들기 위한 워크플로우 호출](../../automating/using/calling-a-workflow-with-external-parameters.md#use-case)

## 구성 {#configuration}

외부 신호를 구성할 때는 먼저 대상 워크플로우에서 **[!UICONTROL External signal]** 활동을 구성해야 합니다. 이 구성이 완료되면 이 워크플로우의 **[!UICONTROL External signal]** 활동을 사용하여 소스 워크플로우의 **[!UICONTROL End]** 활동을 구성할 수 있습니다.

1. 대상 워크플로우에 **[!UICONTROL External signal]** 활동을 드래그하여 놓습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 활동을 엽니다.
1. 활동의 레이블을 편집합니다. 이 레이블은 소스 워크플로우를 구성할 때 필요합니다 **[!UICONTROL External signal]**.

   매개 변수를 사용하여 워크플로우를 호출하려면 영역을 사용하여 **[!UICONTROL Parameters]** 선언합니다. 이 작업에 대한 자세한 정보는 [이 섹션](../../automating/using/calling-a-workflow-with-external-parameters.md#declaring-the-parameters-in-the-external-signal-activity)을 참조하십시오.

   ![](assets/external_signal_configuration.png)

1. 활동의 구성을 확인하고 필요한 다른 활동을 추가하고 워크플로우를 저장합니다.

   >[!NOTE]
   >
   >다른 워크플로우에서 대상 워크플로우를 트리거하려면 다음 단계를 계속 진행합니다. REST API 호출에서 대상 워크플로우를 트리거하려면 [API 설명서를](../../api/using/triggering-a-signal-activity.md) 참조하여 자세한 내용을 확인하십시오.

1. 소스 워크플로우를 열고 **[!UICONTROL End]** 활동을 선택합니다. 사용 가능한 **[!UICONTROL End]** 활동이 없는 경우, 워크플로우 분기의 마지막 활동 뒤에 활동을 추가합니다.

   일부 활동에는 기본적으로 아웃바운드 전환이 없습니다. 이러한 활동의 **[!UICONTROL Properties]** 탭에서 아웃바운드 전환을 추가할 수 있습니다.

   예를 들어 **[!UICONTROL Update data]** 활동에서 **[!UICONTROL Transitions]** 탭으로 이동하여 옵션을 **[!UICONTROL Add an outbound transition without the population]** 선택합니다. 이 옵션을 사용하면 데이터가 포함되지 않고 시스템에서 불필요한 공간을 사용하지 않는 전환을 추가할 수 있습니다. 대상 워크플로우를 트리거하는 추가 **[!UICONTROL End]** 활동을 연결하는 데 사용됩니다.

   ![](assets/external_signal_empty_transition.png)

1. 활동 **[!UICONTROL External signal]** 탭에서 **[!UICONTROL End]** 대상 워크플로우뿐만 아니라 해당 워크플로우 내에서 트리거할 **[!UICONTROL External signal]** 활동을 선택합니다.

   다른 워크플로우를 트리거하는 **[!UICONTROL End]** 활동을 설정하면 해당 아이콘이 추가 신호 심볼로 업데이트됩니다.

   매개 변수를 사용하여 워크플로우를 호출하려면 **[!UICONTROL Parameters and values]** 영역을 사용합니다. 이 작업에 대한 자세한 정보는 [이 섹션](../../automating/using/calling-a-workflow-with-external-parameters.md#defining-the-parameters-when-calling-the-workflow)을 참조하십시오.

   ![](assets/external_signal_end.png)

1. 소스 워크플로우를 저장합니다.

소스 워크플로우 또는 REST API 호출의 **[!UICONTROL End]** 활동이 실행되면 대상 워크플로우는 활동에서 자동으로 **[!UICONTROL External signal]** 트리거됩니다.

>[!NOTE]
>
>대상 워크플로우를 트리거하려면 먼저 수동으로 시작해야 합니다. 시작될 때 **[!UICONTROL External activity]** 는 활성화되고 소스 워크플로우에서 신호를 기다립니다.
