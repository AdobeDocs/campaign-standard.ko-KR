---
title: 테스트
description: 테스트 활동은 테스트 결과를 기반으로 전환을 활성화합니다.
page-status-flag: 활성화 안 함
uuid: 1562ec7a-253a-4f4f-b66a-c2948b5775a
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 자동화
content-type: reference
topic-tags: 실행 활동
discoiquuid: 2650bf1f-0bce-4049-a226-2369f666b95
context-tags: jstest,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 테스트{#test}

## 설명 {#description}

![](assets/test.png)

이 **[!UICONTROL Test]** 활동은 테스트 결과를 기반으로 전환을 활성화합니다.

## 사용 상황 {#context-of-use}

테스트 **활동은** 연결된 조건을 충족하는 첫 번째 전환을 활성화합니다.

조건이 충족되지 않고 **기본 전환** 사용 옵션이 활성화되면 기본 전환이 활성화됩니다.

![](assets/wkf_test_activity_example.png)

조건은 **함수**&#x200B;또는 **변수**(예: 워크플로우의 **[!UICONTROL External signal]** 활동으로 선언된 이벤트 변수)를 기반으로할 수 있습니다.

**관련 항목:**

* [함수 목록](../../automating/using/list-of-functions.md)
* [외부 파라미터로 워크플로우 호출](../../automating/using/calling-a-workflow-with-external-parameters.md)

## 구성 {#configuration}

1. 작업을 워크플로우로 드래그하여 **[!UICONTROL Test]** 놓습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 엽니다.
1. 각 조건의 속성을 정의합니다.

   필드를 편집할 때 두 개의 **[!UICONTROL Condition]** 단추가 이벤트 변수를 호출하고 변수와 함수를 결합한 표현식을 편집하는 데 도움이 됩니다.

   * ![](assets/extsignal_picker.png):워크플로우에서 사용할 수 있는 모든 변수 중에서 events 변수를 선택합니다(외부 매개 변수를 [사용하여 워크플로우 사용자 지정](../../automating/using/calling-a-workflow-with-external-parameters.md#customizing-a-workflow-with-external-parameters)참조).

      ![](assets/wkf_test_activity_variables.png)

   * ![](assets/extsignal_expression_editor.png):변수와 함수를 결합하는 표현식을 편집합니다. 표현식 편집기에 대한 자세한 내용은 [이 섹션을](../../automating/using/advanced-expression-editing.md)참조하십시오.

      ![](assets/wkf_test_activity_variables_expression.png)

