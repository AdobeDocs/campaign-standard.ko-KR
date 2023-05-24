---
title: 개요
description: 이 섹션에서는 외부 매개 변수를 사용하는 워크플로우를 호출하는 방법에 대해 자세히 설명합니다.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: 538056e6-b5c0-4258-a34b-524fe6e3cbbe
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 4%

---

# 개요 {#calling-a-workflow-with-external-parameters}

Campaign Standard을 사용하면 매개 변수(대상 이름, 가져올 파일 이름, 메시지 콘텐츠의 일부 등)를 사용하여 워크플로우를 호출할 수 있습니다. 이렇게 하면 Campaign 자동화를 외부 시스템과 쉽게 통합할 수 있습니다.

CMS에서 직접 이메일을 전송하려는 다음 예를 살펴보겠습니다. 이 경우 대상자를 선택하고 CMS에 콘텐츠를 전자 메일로 보내도록 시스템을 구성할 수 있습니다. 그런 다음 전송을 클릭하면 이러한 매개 변수를 사용하여 Campaign 워크플로우를 호출하여 워크플로우에서 게재에 사용할 대상과 URL 콘텐츠를 정의할 수 있습니다.

매개변수를 사용하여 워크플로우를 호출하는 프로세스는 다음과 같습니다.

1. 에서 매개 변수 선언 **[!UICONTROL External signal]** 활동. 다음을 참조하십시오 [외부 신호 활동에서 매개 변수 선언](../../automating/using/declaring-parameters-external-signal.md).
1. 구성 **[!UICONTROL End]** 매개 변수를 정의하고 워크플로우를 트리거하기 위한 활동 또는 API 호출 **[!UICONTROL External signal]** 활동. [이 페이지](../../automating/using/defining-parameters-calling-workflow.md)를 참조하십시오
1. 워크플로우가 트리거되면 매개 변수가 워크플로우의 이벤트 변수에 수집되고 워크플로우 내에서 사용할 수 있습니다. [이 페이지](../../automating/using/customizing-workflow-external-parameters.md)를 참조하십시오.

![](assets/extsignal_process.png)
