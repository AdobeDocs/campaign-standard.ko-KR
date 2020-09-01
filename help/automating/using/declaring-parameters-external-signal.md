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
source-git-commit: 51e98bb6212ad96d9c11b848df9dcad25b3f1b61
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 5%

---


# 외부 신호 활동에서 매개 변수 선언 {#declaring-the-parameters-in-the-external-signal-activity}

매개 변수가 있는 워크플로우를 호출하는 첫 번째 단계는 **[!UICONTROL External signal]** 활동에서 해당 매개 변수를 선언하는 것입니다.

1. Open the **[!UICONTROL External signal]** activity, then select the **[!UICONTROL Parameters]** tab.
1. 단추를 **[!UICONTROL Create element]** 클릭한 다음 각 매개 변수의 이름과 유형을 지정합니다.

   >[!CAUTION]
   >
   >워크플로우 호출 시 정의된 매개 변수의 이름 및 개수가 동일한지 확인합니다(참조 [](../../automating/using/defining-parameters-calling-workflow.md)). 또한 매개 변수의 유형은 예상 값과 일치해야 합니다.

   ![](assets/extsignal_declaringparameters_1.png)

1. 매개 변수가 선언되면 워크플로우 구성을 완료한 다음 실행합니다.
