---
solution: Campaign Standard
product: campaign
title: 외부 파라미터로 워크플로우 호출
description: 이 섹션에서는 외부 매개 변수를 사용한 워크플로우를 호출하는 방법에 대해 자세히 설명합니다.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 5%

---


# 외부 신호 활동 {#declaring-the-parameters-in-the-external-signal-activity}에서 매개 변수 선언

매개 변수가 있는 워크플로우를 호출하는 첫 번째 단계는 **[!UICONTROL External signal]** 활동에서 매개 변수를 선언하는 것입니다.

1. **[!UICONTROL External signal]** 활동을 연 다음 **[!UICONTROL Parameters]** 탭을 선택합니다.
1. **[!UICONTROL Create element]** 단추를 클릭한 다음 각 매개 변수의 이름과 유형을 지정합니다.

   >[!CAUTION]
   >
   >워크플로 호출 시 정의된 매개 변수의 이름 및 개수가 동일한지 확인하십시오([이 페이지](../../automating/using/defining-parameters-calling-workflow.md) 참조). 또한 매개 변수 유형은 예상 값과 일치해야 합니다.

   ![](assets/extsignal_declaringparameters_1.png)

1. 매개 변수가 선언되면 워크플로우 구성을 완료한 다음 실행합니다.
