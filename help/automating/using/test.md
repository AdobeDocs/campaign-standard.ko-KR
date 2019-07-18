---
title: 테스트
seo-title: 테스트
description: 테스트
seo-description: 테스트 활동은 테스트 결과를 기반으로 전환을 활성화합니다.
page-status-flag: 정품 인증 안 함
uuid: 1562 EC 7 A -253 A -4 F 4 F-B 66 A-C 2948 B 57775 A
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 실행 활동
discoiquuid: 2650 BF 1 F -0 BCE -4049-A 226-2369 F 6666 B 95
context-tags: Jstest, main
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 0454dac1a7976c1be2838c2a846d33e77e60c3b3

---


# Test{#test}

## Description {#description}

![](assets/test.png)

**[!UICONTROL Test]** 활동은 테스트 결과를 기반으로 전환을 활성화합니다.

## Context of use {#context-of-use}

**테스트** 활동은 연관된 조건을 만족하는 첫 번째 전환을 활성화합니다.

If no condition is satisfied and if the **Use default transition** option is activated, a default transition will be activated.

![](assets/wkf_test_activity_example.png)

Conditions can be based on **functions**, or on **variables**, for example events variables that have been declared into the workflow's **[!UICONTROL External signal]** activity.

**관련 항목:**

* [함수 목록](../../automating/using/list-of-functions.md)
* [외부 매개 변수를 사용하여 워크플로우 호출](../../automating/using/calling-a-workflow-with-external-parameters.md)

## Configuration {#configuration}

1. **[!UICONTROL Test]** 활동을 워크플로우로 드래그하여 놓습니다.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. 각 조건의 속성을 정의합니다.

   **[!UICONTROL Condition]** 필드를 편집할 때 두 개의 단추가 이벤트 변수를 호출하고 변수 및 함수를 결합하는 표현식을 편집하는 데 도움이 됩니다.

   * ![](assets/extsignal_picker.png): 워크플로우에서 사용할 수 있는 모든 변수 간에 이벤트 변수를 선택합니다 (외부 매개 변수로 워크플로우 [사용자 지정 참조](../../automating/using/calling-a-workflow-with-external-parameters.md#customizing-a-workflow-with-external-parameters)).

      ![](assets/wkf_test_activity_variables.png)

   * ![](assets/extsignal_expression_editor.png): 변수와 함수를 결합하는 표현식을 편집합니다. For more on the Expression editor, refer to [this section](../../automating/using/advanced-expression-editing.md).

      ![](assets/wkf_test_activity_variables_expression.png)

