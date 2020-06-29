---
title: 세분화
description: 세그멘테이션 활동을 사용하면 워크플로우에서 이전에 배치한 활동에 의해 계산된 모집단 중에서 하나 또는 여러 개의 세그먼트를 만들 수 있습니다.
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
ht-degree: 0%

---


# 세분화{#segmentation}

## 설명 {#description}

![](assets/segmentation.png)

이 **[!UICONTROL Segmentation]** 활동을 사용하면 워크플로우에서 이전에 배치된 활동에 의해 계산된 모집단 중에서 하나 또는 여러 개의 세그먼트를 만들 수 있습니다. 활동이 끝나면 단일 전환 또는 다른 전환 효과에서 처리할 수 있습니다.

>[!NOTE]
>
>기본적으로 인바운드 인구의 구성원은 하나의 세그먼트에만 속할 수 있습니다. 필터는 활동에서 세그먼트의 순서에 따라 적용됩니다.

**관련 항목:**
* [사용 사례: 위치 세분화](../../automating/using/workflow-segmentation-location.md)
* [사용 사례: 컨트롤 그룹 만들기](../../automating/using/workflow-control-group.md)
* [사용 사례: 연령 그룹에 따른 세분화](../../automating/using/segmentation-age-groups.md)

## 사용 상황 {#context-of-use}

일반적으로 **[!UICONTROL Segmentation]** 활동은 타깃팅 활동(쿼리, 교차, 결합, 제외 등) 후에 배치됩니다. 세그먼트를 구성하는 기준으로 표준 모집단 정의

**관련 항목**

* [사용 사례: 연령 그룹에 따라 프로필 세그먼트화](../../automating/using/segmentation-age-groups.md).

## 구성 {#configuration}

1. 활동을 워크플로우로 드래그하여 **[!UICONTROL Segmentation]** 놓습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 활동을 엽니다.
1. 탭에서 **[!UICONTROL General]** 세그멘테이션을 **[!UICONTROL Resource type]** 수행해야 하는 대상을 선택합니다.

   * **[!UICONTROL Database resource]** 세그먼테이션이 데이터베이스에 이미 있는 데이터에 대해 수행되는 경우 세그먼트화할 데이터에 **[!UICONTROL Filtering dimension]** 따라 을 선택합니다. 기본적으로 세그먼테이션은 **프로파일에서 수행됩니다**.
   * **[!UICONTROL Temporary resource]** 워크플로우의 임시 데이터에서 세그먼테이션이 수행되는 경우: 세그먼트화할 데이터 **[!UICONTROL Targeted set]** 포함 항목을 선택합니다. 이 사용 사례는 파일을 가져온 후 또는 데이터베이스의 데이터가 농축된 경우에 발생할 수 있습니다.

1. 사용할 아웃바운드 전환 유형을 선택합니다.

   * **[!UICONTROL Generate one transition per segment]**: 활동의 끝에 구성된 각 세그먼트에 대해 하나의 아웃바운드 전환이 추가됩니다.
   * **[!UICONTROL Generate all segments in one transition]**: 구성된 모든 세그먼트는 하나의 아웃바운드 전환으로 다시 그룹화됩니다. 전환 레이블을 지정합니다. 각 세그먼트의 구성원은 세그먼트에 할당된 세그먼트 코드를 유지합니다.

1. 또는 단추를 사용하여 세그먼트 ![](assets/add_darkgrey-24px.png) 를 추가하고 표준 **[!UICONTROL Add an element]** 속성을 지정합니다.

   * **[!UICONTROL Do not activate the transition if the population is empty]**: 세그먼트는 데이터가 검색되는 경우에만 활성화됩니다.
   * **[!UICONTROL Filter initial population (query)]**: 이 세그먼트의 인구를 필터링할 수 있습니다.
   * **[!UICONTROL Limit segment population]**: 세그먼트 크기를 제한할 수 있습니다.
   * **[!UICONTROL Filter and limit segment population]**: 세그먼트 모집단을 필터링하고 크기를 제한할 수 있습니다.
   * **[!UICONTROL Label]**: 세그먼트 레이블.
   * **[!UICONTROL Segment code]**: 코드를 세그먼트 모집단에 지정합니다.세그먼트 코드는 표준 표현식 및 이벤트 변수를 사용하여 개인화할 수 있습니다(이벤트 변수를 사용하여 [활동 사용자 지정 참조](../../automating/using/calling-a-workflow-with-external-parameters.md#customizing-activities-with-events-variables)).
   * **[!UICONTROL Exclude segment from population]**: 지정된 세그먼트를 활동의 아웃바운드 모집단에서 제외할 수 있습니다. 이 옵션은 옵션을 선택한 경우에만 사용할 수 **[!UICONTROL Generate all segments in the same transition]** 있습니다.
   ![](assets/wkf_segment_new_segment.png)

1. 세그먼트의 세부 사항 보기를 열어 후자의 구성 옵션에 액세스합니다. 이렇게 하려면 활동의 세그먼트 목록에서 관련 상자를 선택한 다음 선택합니다 ![](assets/wkf_segment_parameters_24px.png).
1. 초기 모집단을 필터링하는 옵션이 선택되어 있으면 탭을 열고 **[!UICONTROL Filter]** 세그먼트의 모집단을 지정합니다. 필터는 4단계에서 선택한 필터링 차원을 기반으로 합니다. 모집단 필터링에 대한 자세한 내용은 [쿼리 편집](../../automating/using/editing-queries.md) 섹션을 참조하십시오.

   세그먼테이션이 임시 리소스에서 수행되는 경우 이 탭에서 모집단 수와 미리 보기를 사용할 수 없습니다.

1. 세그먼트 크기를 제한하는 옵션이 선택되어 있으면 **[!UICONTROL Limitation]** 탭을 엽니다.

   먼저 사용할 항목 **[!UICONTROL Type of limit]** 을 선택합니다.

   * **[!UICONTROL Random sampling]**: 필요한 경우 탭 구성을 고려하여 세그먼트 모집단 **[!UICONTROL Filter]** 이 임의로 선택됩니다.
   * **[!UICONTROL Ordered sampling]**: 세그먼트 모집단 선택 따라서 적용할 열과 정렬 유형을 지정해야 합니다. 예를 들어, **연령** 필드를 정렬 열로 선택하고 제한을 100으로 설정하면 상위 100명의 **[!UICONTROL Descending sort]** 가장 나이가 많은 사람들의 프로필만 유지됩니다.
   이제 세그먼트 크기 **[!UICONTROL Limit]** 를 지정합니다.

   * **[!UICONTROL Size (as a % of the initial population)]**: 활동의 초기 모집단에서 백분율을 사용하여 세그먼트 크기를 지정합니다.
   * **[!UICONTROL Maximum size]**: 세그먼트 모집단 최대 구성원 수를 지정합니다.
   * **[!UICONTROL By data grouping]**: 인바운드 모집단의 특정 필드 값에 따라 세그먼트 모집단 수를 제한할 수 있습니다. 그룹화할 필드를 선택한 다음 사용할 값을 지정합니다.
   * **[!UICONTROL By data grouping (as a %)]**: 백분율을 사용하여 특정 인바운드 모집단 필드의 값에 따라 세그먼트 모집단 수를 제한할 수 있습니다. 그룹을 적용할 필드를 선택한 다음 사용할 값을 지정합니다.

      >[!NOTE]
      >
      >각 값에 대해 다른 제한 사항을 사용할 수 있습니다. 예를 들어 필드에 대한 그룹을 지정하고 **[!UICONTROL Gender]** 구성원을 10으로, 구성원을 포함한 인구를 30명으로 제한할 수 **[!UICONTROL Male]** **[!UICONTROL Female]** 있습니다. 여러 데이터 그룹 필드를 사용하는 경우 모든 그룹의 크기가 같아야 합니다.
   ![](assets/wkf_segment_limit_by_grouping.png)

1. 세그먼트의 구성을 확인합니다.
1. 이 절차의 6단계부터 10단계까지 반복하여 필요한 만큼 세그먼트를 추가합니다.
1. 필요한 경우 탭에서 매개 변수를 **[!UICONTROL Advanced options]** 편집합니다.

   * 인바운드 인구의 구성원이 동시에 여러 세그먼트에 포함되도록 하려면 **[!UICONTROL Enable overlapping of outbound populations]** 옵션을 선택합니다. 활동의 아웃바운드 인구가 인바운드 인구를 초과할 수 있습니다.
   * 인바운드 모집단 **[!UICONTROL Concatenate the code of each segment]** 에 보관하려는 세그먼트 코드가 이미 할당된 경우 옵션을 선택합니다. 활동에 지정된 세그먼트 코드가 초기 세그먼트 코드에 추가됩니다.
   * 나머지 인구를 이용하려면 **[!UICONTROL Generate complement]** 옵션을 선택합니다. 사용 [사례 참조: 보충으로 배달](../../automating/using/workflow-created-query-with-complement.md)생성

1. 활동 구성을 확인하고 워크플로우를 저장합니다.
