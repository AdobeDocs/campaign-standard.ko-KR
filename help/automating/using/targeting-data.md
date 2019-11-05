---
title: 데이터 타겟팅
description: 필요한 데이터를 타깃팅하고 선택하는 다양한 방법을 알아봅니다.
page-status-flag: 활성화 안 함
uuid: 0645d6e5-6a7e-4917-874a-7e7725f06abd
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 자동화
content-type: reference
topic-tags: workflow-general-operation
discoiquuid: 382ea74e-1662-4c64-96d7-676040586913
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 데이터 타겟팅{#targeting-data}

## 데이터 선택 {#selecting-data}

다음 활동을 사용하여 데이터를 선택할 수 있습니다.

* 이 **[!UICONTROL Query]** 활동을 통해 Adobe Campaign 데이터베이스에서 요소 모집단을 필터링하고 추출할 수 있습니다. 쿼리 [섹션을](../../automating/using/query.md) 참조하십시오.
* 이 **[!UICONTROL Incremental query]** 활동을 통해 Adobe Campaign 데이터베이스에서 요소 모집단을 필터링하고 추출할 수 있습니다. 이 활동이 실행될 때마다 이전 실행의 결과는 제외됩니다. 이렇게 하면 새 요소만 타깃팅할 수 있습니다. [증분 쿼리](../../automating/using/incremental-query.md) 섹션.
* 이 **[!UICONTROL Read audience]** 활동을 통해 기존 대상을 검색하고 추가 필터링 조건을 적용하여 세분화할 수 있습니다.대상자 [읽기](../../automating/using/read-audience.md) 섹션을 참조하십시오.

## 데이터 세그먼트화 {#segmenting-data}

Adobe Campaign을 사용하면 인바운드 데이터에 대한 세트를 처리할 수 있습니다. 따라서 여러 모집단을 결합하거나 일부 모집단을 제외하거나 여러 타겟에 공통되는 데이터만 유지할 수 있습니다.

* 이 **[!UICONTROL Union]** 활동을 사용하면 여러 활동의 결과를 단일 타겟으로 다시 그룹화할 수 있습니다. 조합 [섹션을](../../automating/using/union.md) 참조하십시오.
* 활동을 **[!UICONTROL Intersection]** 통해 활동에서 서로 다른 인바운드 모집단에 공통되는 요소만 유지할 수 있습니다. 교차 [섹션을](../../automating/using/intersection.md) 참조하십시오.
* 활동을 **[!UICONTROL Exclusion]** 사용하면 특정 기준에 따라 한 모집단에서 요소를 제외할 수 있습니다. 제외 [섹션을](../../automating/using/exclusion.md) 참조하십시오.
* 이 **[!UICONTROL Segmentation]** 활동을 사용하면 워크플로우에서 이전에 배치한 활동에 의해 계산된 모집단 중에서 하나 또는 여러 개의 세그먼트를 만들 수 있습니다. 활동이 끝나면 단일 전환 또는 다른 전환 시 처리할 수 있습니다. 세그멘테이션 [섹션을](../../automating/using/segmentation.md) 참조하십시오.

## 데이터 강화 {#enriching-data}

식별된 데이터와 수집된 데이터를 수집 및 편집하여 타겟 건설을 최적화할 수 있습니다. 데이터 마트에서 모델링되지 않은 데이터를 포함하여 타깃팅 프로세스를 단순화 및 최적화할 수 있습니다.

The **[!UICONTROL Additional data]** tab of **[!UICONTROL Query]** and **[!UICONTROL Incremental query]** activities allowing the data targeted by the query and transfer this data to the following workflow activities, where it can be used. 특히 다음을 추가할 수 있습니다.

* 간단한 데이터
* 집계
* 컬렉션

**관련 항목**

* [사용 사례:일주일에 한 번 이메일 전달 만들기](../../automating/using/workflow-weekly-offer.md)
* [사용 사례:위치에 세그먼트화된 배달 만들기](../../automating/using/workflow-segmentation-location.md)
* [사용 사례:보충으로 배달 만들기](../../automating/using/workflow-created-query-with-complement.md)
* [사용 사례:비열기 사용자에게 새 배달을 보내는 다시 타깃팅 워크플로우](../../automating/using/workflow-cross-channel-retargeting.md)
