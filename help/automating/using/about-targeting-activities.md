---
title: 타겟팅 활동 기본 정보
description: 화면의 왼쪽에서 타깃팅 활동에 액세스할 수 있습니다.
page-status-flag: never-activated
uuid: a6cbc431-1ae3-428e-b2c9-893454b32ae2
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: 5f7607a1-5f71-4d66-9688-3e5a1774f1b4
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 44d6126023e9411477ccd7ffc07ecde806e7976d
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 4%

---


# 타겟팅 활동 기본 정보{#about-targeting-activities}

팔레트에서 화면의 왼쪽에 있는 부분을 펼칩니다. **[!UICONTROL Targeting]**

이러한 활동은 모집단 데이터 타깃팅, 조작 및 필터링 활동에 따라 다릅니다. 이러한 구성 요소를 사용하면 세트를 정의하고 교차, 결합 또는 제외 작업을 사용하여 이러한 세트를 분할하거나 결합함으로써 하나 이상의 대상을 만들 수 있습니다.

![](assets/wkf_targeting_activities.png)

이 **[!UICONTROL Targeting]** 섹션에서는 다음 활동을 제공합니다.

* [쿼리](../../automating/using/query.md)
* [증가식 쿼리](../../automating/using/incremental-query.md)
* [결합](../../automating/using/union.md)
* [교차](../../automating/using/intersection.md)
* [예외](../../automating/using/exclusion.md)
* [세분화](../../automating/using/segmentation.md)
* [대상자 읽기](../../automating/using/read-audience.md)
* [대상자 저장](../../automating/using/save-audience.md)
* [중복 제거](../../automating/using/deduplication.md)
* [강화](../../automating/using/enrichment.md)

**[!UICONTROL Targeting]** 활동을 통해 아웃바운드 전환의 **세그먼트 코드를** 정의할 수 있습니다. 그런 다음 마케팅 캠페인의 효율성을 측정하기 위해 이러한 세그먼트 코드를 기반으로 보고서를 만들 수 있습니다. For more on this, refer to [this section](../../reporting/using/creating-a-report-workflow-segment.md).

## 데이터 선택 {#selecting-data}

다음 활동을 사용하여 데이터를 선택할 수 있습니다.

* 이 **[!UICONTROL Query]** 활동을 통해 Adobe Campaign 데이터베이스에서 요소 모집단을 필터링하고 추출할 수 있습니다. 쿼리 [섹션을](../../automating/using/query.md) 참조하십시오.
* 이 **[!UICONTROL Incremental query]** 활동을 통해 Adobe Campaign 데이터베이스에서 요소 모집단을 필터링하고 추출할 수 있습니다. 이 활동이 실행될 때마다 이전 실행의 결과가 제외됩니다. 이를 통해 새 요소만 타깃팅할 수 있습니다. [증분 쿼리](../../automating/using/incremental-query.md) 섹션.
* 이 **[!UICONTROL Read audience]** 활동에서는 추가 필터링 조건을 적용하여 기존 대상을 검색하고 세분화할 수 있습니다.대상자 [읽기](../../automating/using/read-audience.md) 섹션을 참조하십시오.

## 데이터 세그먼트화 {#segmenting-data}

Adobe Campaign을 사용하면 인바운드 데이터에 대한 설정을 처리할 수 있습니다. 따라서 여러 모집단을 결합하거나 일부 모집단을 제외하거나 여러 개의 타겟에 공통되는 데이터만 유지할 수 있습니다.

* 이 **[!UICONTROL Union]** 활동을 통해 여러 활동의 결과를 단일 타겟으로 다시 그룹화할 수 있습니다. 조합 [섹션을](../../automating/using/union.md) 참조하십시오.
* 활동을 통해 활동에서 서로 다른 인바운드 모집단과 공통되는 요소만 유지할 수 있습니다. **[!UICONTROL Intersection]** 교차 [섹션을](../../automating/using/intersection.md) 참조하십시오.
* 활동을 통해 특정 기준에 따라 한 모집단에서 요소를 제외할 수 있습니다. **[!UICONTROL Exclusion]** 제외 [섹션을](../../automating/using/exclusion.md) 참조하십시오.
* 이 **[!UICONTROL Segmentation]** 활동을 사용하면 워크플로우에서 이전에 배치된 활동에 의해 계산된 모집단 중에서 하나 또는 여러 개의 세그먼트를 만들 수 있습니다. 활동이 끝나면 단일 전환 또는 다른 전환 효과에서 처리할 수 있습니다. 세그멘테이션 [섹션을](../../automating/using/segmentation.md) 참조하십시오.

## 데이터 농축 {#enriching-data}

식별되고 수집된 데이터는 목표 건설을 최적화하기 위해 농축되고 집계되고 조작할 수 있습니다. 데이터 마트에서 모델링되지 않은 데이터를 포함하여 타깃팅 프로세스를 단순화하고 최적화할 수 있습니다.

쿼리 **[!UICONTROL Additional data]** 및 **[!UICONTROL Query]** 활동의 **[!UICONTROL Incremental query]** 탭에서는 쿼리를 통해 타깃팅된 데이터를 보완하고 이 데이터를 활용할 수 있는 다음 워크플로우 활동으로 전송할 수 있습니다. 특히 다음을 추가할 수 있습니다.

* 간단한 데이터
* 집계
* 컬렉션

**관련 항목**

* [사용 사례: 일주일에 한 번 이메일 전달 만들기](../../automating/using/workflow-weekly-offer.md)
* [사용 사례: 위치에 세그먼트화된 배달 만들기](../../automating/using/workflow-segmentation-location.md)
* [사용 사례: 보충으로 배달 만들기](../../automating/using/workflow-created-query-with-complement.md)
* [사용 사례: 따개가 아닌 사람에게 새 배달을 보내는 다시 타깃팅 워크플로우](../../automating/using/workflow-cross-channel-retargeting.md)
