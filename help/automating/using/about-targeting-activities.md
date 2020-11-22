---
solution: Campaign Standard
product: campaign
title: 타겟팅 활동 기본 정보
description: 화면의 왼쪽에서 타깃팅 활동에 액세스할 수 있습니다.
audience: automating
content-type: reference
topic-tags: targeting-activities
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 48%

---


# 타겟팅 활동 기본 정보{#about-targeting-activities}

화면 왼쪽에 있는 팔레트에서 **[!UICONTROL Targeting]** 섹션을 펼칩니다.

이러한 활동은 모집단 데이터 타깃팅, 조작 및 필터링 활동에 따라 다릅니다. 이러한 구성 요소를 사용하면 세트를 정의하고 교차, 결합 또는 제외 작업을 사용하여 이러한 세트를 분할하거나 결합함으로써 하나 이상의 대상을 만들 수 있습니다.

![](assets/wkf_targeting_activities.png)

이 **[!UICONTROL Targeting]** 섹션에는 다음 활동이 표시됩니다.

* [쿼리](../../automating/using/query.md)
* [증분 쿼리](../../automating/using/incremental-query.md)
* [결합](../../automating/using/union.md)
* [교차](../../automating/using/intersection.md)
* [예외](../../automating/using/exclusion.md)
* [세분화](../../automating/using/segmentation.md)
* [대상자 읽기](../../automating/using/read-audience.md)
* [대상자 저장](../../automating/using/save-audience.md)
* [중복 제거](../../automating/using/deduplication.md)
* [데이터 보강](../../automating/using/enrichment.md)

**[!UICONTROL Targeting]** 활동을 통해 아웃바운드 전환의 **세그먼트 코드를** 정의할 수 있습니다. 그런 다음 마케팅 캠페인의 효율성을 측정하기 위해 이러한 세그먼트 코드를 기반으로 보고서를 만들 수 있습니다. 자세한 정보는 [이 섹션](../../reporting/using/creating-a-report-workflow-segment.md)을 참조하십시오.

## 데이터 선택 {#selecting-data}

다음 활동을 사용하여 데이터를 선택할 수 있습니다.

* **[!UICONTROL Query]** 활동을 통해 Adobe Campaign 데이터베이스에서 요소 모집단을 필터링하고 추출할 수 있습니다. 쿼리 [섹션을](../../automating/using/query.md) 참조하십시오.
* **[!UICONTROL Incremental query]** 활동을 통해 Adobe Campaign 데이터베이스에서 요소 모집단을 필터링하고 추출할 수 있습니다. 이 활동이 실행될 때마다 이전 실행의 결과가 제외됩니다. 이를 통해 새 요소만 타깃팅할 수 있습니다. [증분 쿼리](../../automating/using/incremental-query.md) 섹션.
* The **[!UICONTROL Read audience]** activity allows you to retrieve an existing audience and to refine it by applying additional filtering conditions.See the [Read audience](../../automating/using/read-audience.md) section.

## 데이터 세그먼트화 {#segmenting-data}

Adobe Campaign을 사용하면 인바운드 데이터에 대한 설정을 처리할 수 있습니다. 따라서 여러 모집단을 결합하거나 일부 모집단을 제외하거나 여러 개의 타겟에 공통되는 데이터만 유지할 수 있습니다.

* **[!UICONTROL Union]** 활동을 사용하면 여러 활동의 결과를 하나의 타겟으로 다시 그룹화할 수 있습니다. 조합 [섹션을](../../automating/using/union.md) 참조하십시오.
* **[!UICONTROL Intersection]** 활동을 사용하면 활동에서 다른 인바운드 모집단에 공통되는 요소만 유지할 수 있습니다. 교차 [섹션을](../../automating/using/intersection.md) 참조하십시오.
* **[!UICONTROL Exclusion]** 활동을 통해 특정 기준에 따라 한 모집단에서 요소를 제외할 수 있습니다. 제외 [섹션을](../../automating/using/exclusion.md) 참조하십시오.
* **[!UICONTROL Segmentation]** 활동을 사용하면 워크플로우 앞에 배치된 활동으로 계산된 모집단에서 하나 또는 여러 개의 세그먼트를 만들 수 있습니다. 활동 종료 시점에 단일 전환 또는 여러 전환으로 처리할 수 있습니다. 세그멘테이션 [섹션을](../../automating/using/segmentation.md) 참조하십시오.

## 데이터 강화 {#enriching-data}

식별되고 수집된 데이터는 목표 건설을 최적화하기 위해 농축되고 집계되고 조작할 수 있습니다. 데이터 마트에서 모델링되지 않은 데이터를 포함하여 타깃팅 프로세스를 단순화하고 최적화할 수 있습니다.

The **[!UICONTROL Additional data]** tab of the **[!UICONTROL Query]** and **[!UICONTROL Incremental query]** activities allows you to enrich the data targeted by the query and transfer this data to the following workflow activities, where it can be utilized. 특히 다음을 추가할 수 있습니다.

* 단순 데이터
* 집계
* 컬렉션

**관련 항목:**

* [사용 사례:추가 데이터를 사용하여 이메일 개인화](../../automating/using/personalizing-email-with-additional-data.md)
