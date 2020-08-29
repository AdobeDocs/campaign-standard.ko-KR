---
title: 세분화
description: 세분화 활동을 사용하면 워크플로우 앞에 배치된 활동으로 계산된 모집단에서 하나 또는 여러 개의 세그먼트를 만들 수 있습니다.
page-status-flag: never-activated
uuid: 77796f18-cad5-4e7a-9d7b-4ed0dd8943bf
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: 0ccd9d02-772e-406b-874a-5381dd0c8709
context-tags: segmentation,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 15e5aebdd67e8f5ddee89506c0469a101d94d2e8
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 94%

---


# 세분화{#segmentation}

## 설명 {#description}

![](assets/segmentation.png)

**[!UICONTROL Segmentation]** 활동을 사용하면 워크플로우 앞에 배치된 활동으로 계산된 모집단에서 하나 또는 여러 개의 세그먼트를 만들 수 있습니다. 활동 종료 시점에 단일 전환 또는 여러 전환으로 처리할 수 있습니다.

>[!NOTE]
>
>기본적으로 인바운드 모집단의 멤버는 단일 세그먼트에만 속할 수 있습니다. 활동 내 세그먼트의 순서에 따라 필터가 적용됩니다.

**관련 항목:**
* [사용 사례:위치 세분화](../../automating/using/workflow-segmentation-location.md)
* [사용 사례:컨트롤 그룹 만들기](../../automating/using/workflow-control-group.md)
* [사용 사례:연령 그룹에 따른 세분화](../../automating/using/segmentation-age-groups.md)

## 사용의 컨텍스트 {#context-of-use}

**[!UICONTROL Segmentation]** 활동은 보통 타겟팅 활동(쿼리, 교집합, 결합, 제외 등) 다음에 배치됩니다. 이렇게 함으로써 표준 모집단을 정의하여 이를 기반으로 세그먼트를 형성할 수 있습니다.

**관련 항목**

* [사용 사례:연령 그룹에 따라 프로필 세그먼트화](../../automating/using/segmentation-age-groups.md).

## 구성 {#configuration}

1. **[!UICONTROL Segmentation]** 활동을 워크플로우로 끌어서 놓습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업에서 ![](assets/edit_darkgrey-24px.png) 버튼을 사용하여 활동을 엽니다.
1. In the **[!UICONTROL General]** tab, select the **[!UICONTROL Resource type]** on which the segmentation has to be carried out:

   * 데이터베이스에 이미 있는 데이터에 대해 세분화를 수행하려는 경우 **[!UICONTROL Database resource]**. 세분화할 데이터에 따라 **[!UICONTROL Filtering dimension]**&#x200B;을(를) 선택합니다. 세분화는 기본적으로 **프로필**&#x200B;에 대해 수행됩니다.
   * 워크플로우의 임시 데이터에 대해 세분화를 수행하려는 경우 **[!UICONTROL Temporary resource]**: 세분화할 데이터가 있는 **[!UICONTROL Targeted set]**&#x200B;을(를) 선택합니다. 이 사용 사례는 파일을 가져온 후 또는 데이터베이스의 데이터를 보강한 경우에 발생할 수 있습니다.

1. 사용할 아웃바운드 전환 유형을 선택합니다.

   * **[!UICONTROL Generate one transition per segment]**: 활동 종료 시 구성된 각 세그먼트에 대해 하나의 아웃바운드 전환이 추가됩니다.
   * **[!UICONTROL Generate all segments in one transition]**: 구성된 모든 세그먼트가 하나의 아웃바운드 전환으로 다시 그룹화됩니다. 전환 레이블을 지정합니다. 각 세그먼트의 멤버에게 할당된 세그먼트 코드는 그대로 유지됩니다.

1. ![](assets/add_darkgrey-24px.png) 또는 **[!UICONTROL Add an element]** 버튼을 사용하여 세그먼트를 추가하고 표준 속성을 지정합니다.

   * **[!UICONTROL Do not activate the transition if the population is empty]**: 데이터가 검색되는 경우에만 세그먼트가 활성화됩니다.
   * **[!UICONTROL Filter initial population (query)]**: 세그먼트의 모집단을 필터링할 수 있습니다.
   * **[!UICONTROL Limit segment population]**: 세그먼트 크기를 제한할 수 있습니다.
   * **[!UICONTROL Filter and limit segment population]**: 세그먼트의 모집단을 필터링하고 크기를 제한할 수 있습니다.
   * **[!UICONTROL Label]**: 세그먼트 레이블입니다.
   * **[!UICONTROL Segment code]**: 세그먼트 모집단에 지정된 코드입니다. 세그먼트 코드는 표준 표현식 및 이벤트 변수를 사용하여 개인화할 수 있습니다([이벤트 변수를 사용하여 활동 사용자 지정](../../automating/using/calling-a-workflow-with-external-parameters.md#customizing-activities-with-events-variables) 참조).
   * **[!UICONTROL Exclude segment from population]**: 지정된 세그먼트를 활동의 아웃바운드 모집단에서 제외할 수 있습니다. 이 옵션은 **[!UICONTROL Generate all segments in the same transition]** 옵션을 선택한 경우에만 사용할 수 있습니다.

   ![](assets/wkf_segment_new_segment.png)

1. 후자의 구성 옵션에 액세스하려면 세그먼트의 세부 사항 보기를 엽니다. 이렇게 하려면 활동의 세그먼트 목록에서 관련 상자를 선택한 다음 ![](assets/wkf_segment_parameters_24px.png)을(를) 선택합니다.
1. 초기 모집단을 필터링하는 옵션이 선택되어 있다면 **[!UICONTROL Filter]** 탭을 열고 세그먼트의 모집단을 지정합니다. 필터는 4단계에서 선택한 차원 필터링을 기반으로 합니다. 모집단 필터링에 대한 자세한 내용은 [쿼리 편집](../../automating/using/editing-queries.md) 섹션을 참조하십시오.

   임시 리소스에 대해 세분화를 수행하는 경우 이 탭에서 모집단의 개수 세기와 미리 보기를 사용할 수 없습니다.

1. 세그먼트 크기를 제한하는 옵션이 선택되어 있다면 **[!UICONTROL Limitation]** 탭을 엽니다.

   먼저 사용할 **[!UICONTROL Type of limit]**&#x200B;을(를) 선택합니다.

   * **[!UICONTROL Random sampling]**: 필요한 경우 **[!UICONTROL Filter]** 탭의 구성을 고려하여 세그먼트 모집단을 임의로 선택합니다.
   * **[!UICONTROL Ordered sampling]**: 세그먼트 모집단을 순서대로 선택합니다. 따라서 고려할 열과 적용할 정렬 유형을 지정해야 합니다. 예를 들어, **나이** 필드를 정렬 열로 선택하고 **[!UICONTROL Descending sort]**&#x200B;을(를) 적용한 뒤 제한을 100으로 설정하면 나이가 가장 많은 100명의 프로필만 유지됩니다.

   이제 세그먼트 크기 **[!UICONTROL Limit]**&#x200B;을(를) 지정합니다.

   * **[!UICONTROL Size (as a % of the initial population)]**: 활동의 초기 모집단에 대한 백분율로 세그먼트 크기를 지정합니다.
   * **[!UICONTROL Maximum size]**: 세그먼트 모집단의 최대 멤버 수를 지정합니다.
   * **[!UICONTROL By data grouping]**: 인바운드 모집단의 특정 필드 값에 따라 세그먼트 모집단을 제한할 수 있습니다. 그룹화할 필드를 선택한 다음 사용할 값을 지정합니다.
   * **[!UICONTROL By data grouping (as a %)]**: 백분율을 사용하여 특정 인바운드 모집단 필드의 값에 따라 세그먼트 모집단을 제한할 수 있습니다. 그룹을 적용할 필드를 선택한 다음 사용할 값을 지정합니다.

      >[!NOTE]
      >
      >각 값에 대해 다양한 제한 사항을 사용할 수 있습니다. 예를 들어 **[!UICONTROL Gender]** 필드에 대한 그룹을 지정하고 **[!UICONTROL Male]** 멤버로 이루어진 모집단을 10명으로, **[!UICONTROL Female]** 멤버로 이루어진 모집단을 30명으로 제한할 수 있습니다. 여러 데이터 그룹 필드를 사용하는 경우 모든 그룹의 크기가 같아야 합니다.
   ![](assets/wkf_segment_limit_by_grouping.png)

1. 세그먼트의 구성을 확인합니다.
1. 이 절차의 6단계부터 10단계까지 반복하여 세그먼트를 필요한 만큼 추가합니다.
1. 필요한 경우 **[!UICONTROL Advanced options]** 탭에서 매개 변수를 편집합니다.

   * 인바운드 모집단의 멤버가 동시에 여러 세그먼트에 속하도록 하려면 **[!UICONTROL Enable overlapping of outbound populations]** 옵션을 선택합니다. 활동의 아웃바운드 모집단은 인바운드 모집단을 초과할 수 있습니다.
   * 남겨 두려는 세그먼트 코드가 인바운드 모집단에 이미 할당된 경우 **[!UICONTROL Concatenate the code of each segment]** 옵션을 선택합니다. 활동에 지정된 세그먼트 코드가 초기 세그먼트 코드에 추가됩니다.
   * 나머지 모집단을 활용하려면 **[!UICONTROL Generate complement]** 옵션을 선택합니다. See [Use case: Creating deliveries with a complement](../../automating/using/workflow-created-query-with-complement.md).

1. 활동 구성을 확인하고 워크플로우를 저장합니다.
