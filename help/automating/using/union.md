---
title: union
seo-title: union
description: union
seo-description: 조합 활동을 사용하면 여러 활동의 결과를 하나의 타겟으로 다시 그룹화할 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: FAFC 3 CE 9-2212-4403-8754-CFBB 28 BA 6 E 26
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 타깃팅 활동
discoiquuid: 99 a 8 c 3 a 5-7 d 90-4 dbb-aa 37-1 d 0 a 84719 cf 6
context-tags: union, main
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 0454dac1a7976c1be2838c2a846d33e77e60c3b3

---


# Union{#union}

## Description {#description}

![](assets/union.png)

**[!UICONTROL Union]** 활동을 통해 여러 활동의 결과를 하나의 타겟으로 다시 그룹화할 수 있습니다.

>[!NOTE]
>
>세트가 반드시 균일하지 않아도 됩니다.

## Context of use {#context-of-use}

**[!UICONTROL Union]** 이 활동은 세그멘테이션을 수행하거나 대상을 정의하거나 예를 들어 메시지 타겟을 준비할 때 인바운드 전환에서 모집단을 결합하는 데 사용됩니다.

## Configuration {#configuration}

1. **[!UICONTROL Union]** 워크플로우를 워크플로우로 드래그하여 놓습니다.
1. 쿼리 등의 다른 활동 (예: 쿼리) 에 연결합니다.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. Select the **[!UICONTROL Reconciliation type]** to define how duplicates are from the confrontation between inbound populations are handled:

   * **[!UICONTROL Keys only]**: 기본 모드입니다. 활동은 다른 인바운드 변환의 요소가 동일한 키를 가질 때 하나의 요소만 유지합니다. 이 옵션은 인바운드 모집단이 동질인 경우에만 사용할 수 있습니다.
   * **[!UICONTROL All shared columns]**: 데이터는 인바운드 전환을 사용하는 모든 열을 기준으로 조정됩니다. 따라서 중복의 경우에 보존할 기본 세트를 선택해야 합니다. 인바운드 모집단 타깃팅 차원이 다른 경우 이 옵션을 사용할 수 있습니다.
   * **[!UICONTROL A selection of columns]**: 이 옵션을 선택하여 데이터 조정이 적용될 열의 목록을 정의합니다. 먼저 기본 세트 (소스 데이터가 들어 있음) 를 선택한 다음 가입에 사용할 열을 선택해야 합니다.

1. Check the **[!UICONTROL Use common additional data only]** box if you would like to keep only the additional data that is in all inbound transitions.
1. If you would like to limit the size of the final population, check the **[!UICONTROL Limit size of generated population]** box. The size can be specified in the **[!UICONTROL Maximum number of records]** field.
1. If needed, manage the activity's [Transitions](../../automating/using/executing-a-workflow.md#managing-an-activity-s-outbound-transitions) to access the advanced options for the calculated population.
1. 활동의 구성을 확인하고 워크플로우를 저장합니다.

## Example {#example}

다음 예에서는 Adobe Campaign 데이터베이스에서 18 세에서 27 세 사이의 사용자와 34 세에서 40 세 사이의 프로필을 다시 그룹화하는 두 개의 쿼리 활동 결과를 보여 줍니다. 결과에는 두 쿼리의 모든 프로필 또는 구성 중에 지정된 최대 레코드 수 (해당되는 경우) 가 포함됩니다.

![](assets/wkf_union_example.png)