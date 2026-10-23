---
title: 워크플로 호출 시 매개 변수 정의
description: 이 섹션에서는 외부 매개 변수를 사용하는 워크플로우를 호출하는 방법에 대해 자세히 설명합니다.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
feature: Workflows
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: f7de0186-4136-4603-8f80-9f58c641cd9d
TQID: 'https://experienceleague.adobe.com/-YjlK1Op8P08sxb--BOHl8AWyciX4BqPnCPQ3lpD3Co'
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
  - id: f5407121-8933-4ac3-8e06-a9b692a4e88a
    internal-label: Campaign Standard
feature_v2:
  - id: b12f6872-9271-4369-85e5-86969a0b99a2
    internal-label: APIs
  - id: a658c786-869b-4194-a780-2594d663adda
    internal-label: Data management
subfeature_v2:
  - id: bf97c196-a4d1-4fa3-a151-e68a114c8ac0
    internal-label: REST API
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
