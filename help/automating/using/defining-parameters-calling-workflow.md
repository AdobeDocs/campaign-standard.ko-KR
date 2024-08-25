---
title: 워크플로 호출 시 매개 변수 정의
description: 이 섹션에서는 외부 매개 변수를 사용하는 워크플로우를 호출하는 방법에 대해 자세히 설명합니다.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: f7de0186-4136-4603-8f80-9f58c641cd9d
source-git-commit: a6471d2970a55373574301fb5d49ee73103fa870
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 13%

---

# 워크플로 호출 시 매개 변수 정의 {#defining-the-parameters-when-calling-the-workflow}

이 섹션에서는 워크플로우를 호출할 때 매개 변수를 정의하는 방법을 자세히 설명합니다. API 호출에서 이 작업을 수행하는 방법에 대한 자세한 내용은 [REST API 설명서](../../api/using/triggering-a-signal-activity.md)를 참조하십시오.

매개 변수를 정의하기 전에 다음을 확인하십시오.

* **[!UICONTROL External Signal]** 활동에서 매개 변수가 선언되었습니다. [이 페이지](../../automating/using/declaring-parameters-external-signal.md)를 참조하십시오.
* 신호 활동이 포함된 워크플로우가 실행 중입니다.

**[!UICONTROL End]** 활동을 구성하려면 아래 단계를 수행합니다.

1. **[!UICONTROL End]** 활동을 연 다음 **[!UICONTROL External signal]** 탭을 선택합니다.
1. 호출할 워크플로우 및 외부 신호 활동을 선택합니다.
1. **[!UICONTROL Create element]** 단추를 클릭하여 매개 변수를 추가한 다음 이름과 값을 입력합니다.

   * **[!UICONTROL Name]**: **[!UICONTROL External signal]** 활동에서 선언된 이름입니다([이 페이지](../../automating/using/declaring-parameters-external-signal.md) 참조).
   * **[!UICONTROL Value]**: 매개 변수에 할당할 값입니다. 값은 [이 섹션](../../automating/using/advanced-expression-editing.md#standard-syntax)에 설명된 **표준 구문**&#x200B;을 따라야 합니다.

   ![](assets/extsignal_definingparameters_2.png)

   >[!CAUTION]
   >
   >**[!UICONTROL External signal]** 활동에서 모든 매개 변수가 선언되었는지 확인하십시오. 그렇지 않으면 활동을 실행할 때 오류가 발생합니다.

1. 매개 변수가 정의되면 활동을 확인한 다음 워크플로우를 저장합니다.
