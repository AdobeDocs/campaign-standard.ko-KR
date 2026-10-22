---
title: 개요
description: 이 섹션에서는 외부 매개 변수를 사용하는 워크플로우를 호출하는 방법에 대해 자세히 설명합니다.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
feature: Workflows
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: 538056e6-b5c0-4258-a34b-524fe6e3cbbe
TQID: 'https://experienceleague.adobe.com/Pin9vFRMMylFFKw6VSvQowwXvzAn1Ihg76e2cSoaeyw'
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
  - id: f5407121-8933-4ac3-8e06-a9b692a4e88a
    internal-label: Campaign Standard
feature_v2:
  - id: a658c786-869b-4194-a780-2594d663adda
    internal-label: Data management
subfeature_v2:
  - id: fcb46c0f-76e1-48bc-9dd0-fcf9d97526cf
    internal-label: Workflows
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
source-git-commit: bb37e2bfbc52de1b0cc03f0f8e03985caff5e5b0
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 2%
---
# 개요 {#calling-a-workflow-with-external-parameters}

Campaign Standard을 사용하면 매개 변수(대상 이름, 가져올 파일 이름, 메시지 콘텐츠의 일부 등)를 사용하여 워크플로우를 호출할 수 있습니다. 이렇게 하면 Campaign 자동화를 외부 시스템과 쉽게 통합할 수 있습니다.

CMS에서 직접 이메일을 전송하려는 다음 예를 살펴보겠습니다. 이 경우 대상을 선택하고 CMS에 콘텐츠를 전자 메일로 보내도록 시스템을 구성할 수 있습니다. 그런 다음 전송을 클릭하면 이러한 매개 변수를 사용하여 Campaign 워크플로우를 호출하여 워크플로우에서 게재에 사용할 대상과 URL 콘텐츠를 정의할 수 있습니다.

매개변수를 사용하여 워크플로우를 호출하는 프로세스는 다음과 같습니다.

1. **[!UICONTROL External signal]** 활동에서 매개 변수를 선언합니다. [외부 신호 활동에서 매개 변수 선언](../../automating/using/declaring-parameters-external-signal.md)을 참조하십시오.
1. 매개 변수를 정의하고 워크플로우 **[!UICONTROL External signal]** 활동을 트리거하도록 **[!UICONTROL End]** 활동 또는 API 호출을 구성합니다. [이 페이지](../../automating/using/defining-parameters-calling-workflow.md) 보기
1. 워크플로우가 트리거되면 매개 변수가 워크플로우의 이벤트 변수에 수집되고 워크플로우 내에서 사용할 수 있습니다. [이 페이지](../../automating/using/customizing-workflow-external-parameters.md)를 참조하십시오.

![](assets/extsignal_process.png)
