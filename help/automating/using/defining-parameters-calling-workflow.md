---
title: 외부 파라미터로 워크플로우 호출
description: 이 섹션에서는 외부 매개 변수를 사용한 워크플로우를 호출하는 방법에 대해 자세히 설명합니다.
page-status-flag: never-activated
uuid: beccd1b6-8e6d-4504-9152-9ff537459c4a
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: workflow-general-operation
discoiquuid: 1676da91-55e3-414f-bcd3-bb0804b682bd
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 3cb37426410eeb8be04c9c75afa4505894b15140
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 8%

---


# 워크플로우 호출 시 매개 변수 정의 {#defining-the-parameters-when-calling-the-workflow}

이 섹션에서는 워크플로우를 호출할 때 매개 변수를 정의하는 방법에 대해 자세히 설명합니다. API 호출에서 이 작업을 수행하는 방법에 대한 자세한 내용은 [REST API 설명서를 참조하십시오](../../api/using/triggering-a-signal-activity.md).

매개 변수를 정의하기 전에 다음을 확인하십시오.

* 매개 변수가 **[!UICONTROL External Signal]** 활동에서 선언되었습니다. [](../../automating/using/declaring-parameters-external-signal.md)을 참조하십시오.
* 신호 활동을 포함하는 워크플로우가 실행 중입니다.

활동을 **[!UICONTROL End]** 구성하려면 아래 단계를 따르십시오.

1. Open the **[!UICONTROL End]** activity, then select the **[!UICONTROL External signal]** tab.
1. 호출하려는 워크플로우 및 외부 신호 활동을 선택합니다.
1. 매개 변수를 추가하려면 **[!UICONTROL Create element]** 단추를 클릭한 다음 이름과 값을 입력합니다.

   * **[!UICONTROL Name]**:활동에 선언된 이름( **[!UICONTROL External signal]** 참조 [](../../automating/using/declaring-parameters-external-signal.md)).
   * **[!UICONTROL Value]**:매개 변수에 할당할 값. 이 값은 **이 섹션에 설명된**&#x200B;표준 구문 [다음에 와야 합니다](../../automating/using/advanced-expression-editing.md#standard-syntax).

   ![](assets/extsignal_definingparameters_2.png)

   >[!CAUTION]
   >
   >Make sure that all the parameters have been declared in the **[!UICONTROL External signal]** activity. 그렇지 않으면 활동을 실행할 때 오류가 발생합니다.

1. 매개 변수가 정의되면 활동을 확인한 다음 워크플로우를 저장합니다.
