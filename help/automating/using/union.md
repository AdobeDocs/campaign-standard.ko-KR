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
ht-degree: 1%

---


# 결합{#union}

## 설명 {#description}

![](assets/union.png)

이 **[!UICONTROL Union]** 활동을 통해 여러 활동의 결과를 단일 타겟으로 다시 그룹화할 수 있습니다.

>[!NOTE]
>
>반드시 동질적일 필요는 없다.

## 사용 상황 {#context-of-use}

이 **[!UICONTROL Union]** 활동은 세그멘테이션을 수행하거나 대상을 정의하거나 메시지 대상을 준비하는 경우 인바운드 전환에서 모집단을 결합하는 데 사용됩니다.

**관련 항목:**

* [사용 사례: 세련된 두 고객을 위한 결합](../../automating/using/union-on-two-refined-audiences.md)

## 구성 {#configuration}

1. 활동을 워크플로우로 드래그하여 **[!UICONTROL Union]** 놓습니다.
1. 쿼리 등 앞에 오는 다른 활동과 연결합니다.
1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 활동을 엽니다.
1. 중복 **[!UICONTROL Reconciliation type]** 을 정의하는 방법을 인바운드 모집단 간 대결에서 정의합니다.

   * **[!UICONTROL Keys only]**: 기본 모드입니다. 다른 인바운드 전환의 요소가 동일한 키를 가질 때 활동은 한 요소만 유지합니다. 이 옵션은 인바운드 모집단이 동질인 경우에만 사용할 수 있습니다.
   * **[!UICONTROL All shared columns]**: 데이터는 인바운드 전환과 공통적인 모든 열을 기반으로 조정됩니다. 따라서 중복에 대해 보관될 기본 세트를 선택해야 합니다. 인바운드 모집단 타깃팅 차원이 다른 경우 이 옵션을 사용할 수 있습니다.
   * **[!UICONTROL A selection of columns]**: 데이터 조정을 적용할 열 목록을 정의하려면 이 옵션을 선택합니다. 먼저 소스 데이터가 포함된 기본 세트를 선택한 다음 조인에 사용할 열을 선택해야 합니다.

1. 모든 인바운드 전환 **[!UICONTROL Use common additional data only]** 에 있는 추가 데이터만 유지하려면 이 상자를 선택합니다.
1. 최종 모집단 크기를 제한하려면 **[!UICONTROL Limit size of generated population]** 상자를 선택합니다. 이 크기는 **[!UICONTROL Maximum number of records]** 필드에 지정할 수 있습니다.
1. 필요한 경우 활동의 전환 [을](../../automating/using/activity-properties.md) 관리하여 계산된 모집단 고급 옵션에 액세스합니다.
1. 활동 구성을 확인하고 워크플로우를 저장합니다.

## 예 {#example}

다음 예에서는 18세에서 27세 사이의 Adobe Campaign 데이터베이스와 34세에서 40세 사이의 프로파일을 재그룹화하는 두 개의 쿼리 활동 결과를 보여 줍니다. 결과에는 구성 중에 지정된 대로 두 쿼리의 모든 프로필 또는 해당되는 경우 최대 레코드 수가 포함됩니다.

![](assets/wkf_union_example.png)