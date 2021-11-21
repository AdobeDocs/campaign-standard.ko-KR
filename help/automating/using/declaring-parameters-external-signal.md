---
title: 외부 매개 변수로 워크플로우 호출
description: 이 섹션에서는 외부 매개 변수로 워크플로우를 호출하는 방법에 대해 자세히 설명합니다.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: e6148b40-f608-4aab-81f6-756608c6828e
source-git-commit: 13d419c5fc51845ee14f8a3b288f4c467e0a60d9
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 5%

---

# 외부 신호 활동에서 매개 변수 선언 {#declaring-the-parameters-in-the-external-signal-activity}

매개 변수를 사용하는 워크플로우를 호출하는 첫 번째 단계는 **[!UICONTROL External signal]** 활동.

1. 를 엽니다. **[!UICONTROL External signal]** 활동을 선택한 다음 **[!UICONTROL Parameters]** 탭.
1. 을(를) 클릭합니다. **[!UICONTROL Create element]** 단추를 누른 다음 각 매개 변수의 이름과 유형을 지정합니다.

   >[!CAUTION]
   >
   >워크플로우 호출 시 정의된 매개 변수의 이름 및 개수가 동일한지 확인합니다( 참조). [이 페이지](../../automating/using/defining-parameters-calling-workflow.md)). 또한 매개 변수의 유형은 예상 값과 일치해야 합니다.

   ![](assets/extsignal_declaringparameters_1.png)

1. 매개 변수가 선언되면 워크플로우 구성을 완료한 다음 실행합니다.
