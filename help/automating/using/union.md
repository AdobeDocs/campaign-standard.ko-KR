---
title: 결합
description: 결합 활동을 사용하면 여러 활동의 결과를 하나의 타겟으로 다시 그룹화할 수 있습니다.
page-status-flag: never-activated
uuid: fafc3ce9-2212-4403-8754-cfbb28ba6e26
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: 99a8c3a5-7d90-4dbb-aa37-1d0a84719cf6
context-tags: union,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 87e0611fae0560aca276caa3c4cf793e9c095d72
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 98%

---


# 결합{#union}

## 설명 {#description}

![](assets/union.png)

**[!UICONTROL Union]** 활동을 사용하면 여러 활동의 결과를 하나의 타겟으로 다시 그룹화할 수 있습니다.

>[!NOTE]
>
>세트가 꼭 동질적이어야 할 필요는 없습니다.

## 사용의 컨텍스트 {#context-of-use}

**[!UICONTROL Union]** 활동은 세분화를 수행하거나 대상자를 정의하거나 메시지 타겟을 준비할 때 인바운드 전환에서 모집단을 결합하는 데 사용됩니다.

**관련 항목:**

* [사용 사례:세련된 두 고객을 위한 결합](../../automating/using/union-on-two-refined-audiences.md)

## 구성 {#configuration}

1. **[!UICONTROL Union]** 활동을 워크플로우로 끌어서 놓습니다.
1. 쿼리와 같은 앞에 오는 다른 활동과 연결합니다.
1. 활동을 선택한 다음 나타나는 빠른 작업에서 ![](assets/edit_darkgrey-24px.png) 버튼을 사용하여 활동을 엽니다.
1. **[!UICONTROL Reconciliation type]**&#x200B;을(를) 선택하여 인바운드 모집단 간 대립 시 중복을 다루는 방법을 정의합니다.

   * **[!UICONTROL Keys only]**: 기본 모드입니다. 다른 인바운드 전환의 요소가 동일한 키를 가지면 활동은 한 요소만 유지합니다. 이 옵션은 인바운드 모집단이 동질적일 경우에만 사용할 수 있습니다.
   * **[!UICONTROL All shared columns]**: 인바운드 전환과 공통되는 모든 열을 기반으로 데이터를 조정합니다. 따라서 중복이 있을 경우 어떤 세트를 기본으로 남길지 선택해야 합니다. 인바운드 모집단 타겟팅 차원이 다른 경우 이 옵션을 사용할 수 있습니다.
   * **[!UICONTROL A selection of columns]**: 데이터 조정을 적용할 열 목록을 정의하려면 이 옵션을 선택합니다. 기본 세트(소스 데이터가 있는 세트)를 먼저 선택한 다음 결합에 사용할 열을 선택해야 합니다.

1. 모든 인바운드 전환에 있는 추가 데이터만 유지하려면 **[!UICONTROL Use common additional data only]** 상자를 선택합니다.
1. 최종 모집단 크기를 제한하려면 **[!UICONTROL Limit size of generated population]** 상자를 선택합니다. 크기는 **[!UICONTROL Maximum number of records]** 필드에서 지정할 수 있습니다.
1. 필요한 경우 해당 활동의 [전환](../../automating/using/activity-properties.md)을 관리하여 계산된 모집단의 고급 옵션에 액세스합니다.
1. 활동 구성을 확인하고 워크플로우를 저장합니다.

## 예제 {#example}

다음 예제에서는 Adobe Campaign 데이터베이스에 있는 18~27세와 34~40세인 프로필을 다시 그룹화하기 위한 두 개의 쿼리 활동 결과를 보여줍니다. 이 결과에는 두 쿼리의 모든 프로필 또는 해당하는 경우 구성 중에 지정된 최대 레코드 수가 포함됩니다.

![](assets/wkf_union_example.png)