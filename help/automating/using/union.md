---
title: 결합
description: 결합 활동을 사용하면 여러 활동의 결과를 단일 타겟으로 다시 그룹화할 수 있습니다.
page-status-flag: 활성화 안 함
uuid: fafc3ce9-2212-4403-8754-cfbb28ba6e26
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 자동화
content-type: reference
topic-tags: 타깃팅 활동
discoiquuid: 99a8c3a5-7d90-4dbb-aa37-1d0a84719cf6
context-tags: union,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 결합{#union}

## 설명 {#description}

![](assets/union.png)

이 **[!UICONTROL Union]** 활동을 사용하면 여러 활동의 결과를 단일 타겟으로 다시 그룹화할 수 있습니다.

>[!NOTE]
>
>집합은 반드시 동질적일 필요는 없다.

## 사용 상황 {#context-of-use}

이 **[!UICONTROL Union]** 활동은 세그먼테이션을 수행하거나 대상을 정의하거나 메시지 대상을 준비하는 경우 인바운드 전환의 모집단을 결합하는 데 사용됩니다.

## 구성 {#configuration}

1. 워크플로우를 워크플로우로 드래그하여 **[!UICONTROL Union]** 놓을 수 있습니다.
1. 쿼리 등 앞에 오는 다른 활동에 연결합니다.
1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 엽니다.
1. 인바운드 모집단 간 대결에서 중복 항목이 처리되는 방식을 정의하려면 를 **[!UICONTROL Reconciliation type]** 선택합니다.

   * **[!UICONTROL Keys only]**:기본 모드입니다. 활동은 서로 다른 인바운드 전환의 요소가 동일한 키를 가질 때 한 요소만 유지합니다. 이 옵션은 인바운드 모집단이 동질인 경우에만 사용할 수 있습니다.
   * **[!UICONTROL All shared columns]**:데이터는 인바운드 전환과 공통으로 모든 열을 기준으로 조정됩니다. 따라서 중복을 위해 보관될 기본 세트를 선택해야 합니다. 인바운드 모집단 타깃팅 차원이 다른 경우 이 옵션을 사용할 수 있습니다.
   * **[!UICONTROL A selection of columns]**:데이터 조정을 적용할 열 목록을 정의하려면 이 옵션을 선택합니다. 먼저 소스 데이터가 포함된 기본 세트를 선택한 다음 조인에 사용할 열을 선택해야 합니다.

1. 모든 인바운드 전환에 있는 추가 데이터만 유지하려면 **[!UICONTROL Use common additional data only]** 상자를 선택합니다.
1. 최종 모집단 크기를 제한하려면 **[!UICONTROL Limit size of generated population]** 상자를 선택합니다. 필드에 크기를 지정할 수 **[!UICONTROL Maximum number of records]** 있습니다.
1. 필요한 경우 활동의 전환을 관리하여 [계산된](../../automating/using/executing-a-workflow.md#managing-an-activity-s-outbound-transitions) 모집단 고급 옵션에 액세스합니다.
1. 활동 구성을 확인하고 워크플로우를 저장합니다.

## 예 {#example}

다음 예에서는 18세에서 27세 사이의 Adobe Campaign 데이터베이스와 34세에서 40세 사이의 프로필을 재그룹화하는 것을 목표로 하는 두 개의 쿼리 활동의 결과를 보여줍니다. 결과에는 구성 중에 지정된 대로 두 쿼리의 모든 프로필 또는 해당되는 경우 최대 레코드 수가 포함됩니다.

![](assets/wkf_union_example.png)