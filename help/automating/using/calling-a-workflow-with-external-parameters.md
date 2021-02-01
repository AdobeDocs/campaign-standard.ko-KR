---
solution: Campaign Standard
product: campaign
title: 개요
description: 이 섹션에서는 외부 매개 변수를 사용하여 워크플로우를 호출하는 방법에 대해 자세히 설명합니다.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
translation-type: tm+mt
source-git-commit: 05b6a9caebdd65f20357070af8bd44cb8ba146c7
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 4%

---


# 개요 {#calling-a-workflow-with-external-parameters}

Campaign Standard을 사용하면 매개 변수(타깃팅할 대상 이름, 가져올 파일 이름, 메시지 내용의 일부 등)가 있는 워크플로우를 호출할 수 있습니다. 이렇게 하면 캠페인 자동화를 외부 시스템과 쉽게 통합할 수 있습니다.

다음 예를 들어 CMS에서 바로 이메일을 보낼 수 있습니다. 이러한 경우 대상을 선택하고 CMS에 콘텐츠를 이메일로 전송하도록 시스템을 구성할 수 있습니다. 전송을 클릭하면 이러한 매개 변수가 있는 캠페인 워크플로우가 호출되므로, 전달에 사용할 대상 및 URL 컨텐츠를 정의하는 워크플로우에 사용할 수 있습니다.

매개 변수가 있는 워크플로우를 호출하는 프로세스는 다음과 같습니다.

1. **[!UICONTROL External signal]** 활동에서 매개 변수를 선언합니다. 외부 신호 활동](../../automating/using/declaring-parameters-external-signal.md)에서 매개 변수 선언을 참조하십시오.[
1. 매개 변수를 정의하고 워크플로 **[!UICONTROL External signal]** 활동을 트리거하도록 **[!UICONTROL End]** 활동 또는 API 호출을 구성합니다. [이 페이지](../../automating/using/defining-parameters-calling-workflow.md)를 참조하십시오
1. 워크플로우가 트리거되면 매개 변수가 워크플로우의 이벤트 변수에 수집되고 워크플로우 내에서 사용할 수 있습니다. [이 페이지](../../automating/using/customizing-workflow-external-parameters.md)를 참조하십시오.

![](assets/extsignal_process.png)
