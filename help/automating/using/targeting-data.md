---
title: 타깃팅 데이터
seo-title: 타깃팅 데이터
description: 타깃팅 데이터
seo-description: 필요한 데이터를 타깃팅하고 선택하는 다양한 방법을 학습합니다.
page-status-flag: 정품 인증 안 함
uuid: 0645 D 6 E 5-6 A 7 E -4917-874 A -7 E 7725 F 06 ABD
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: workflow-general-operation
discoiquuid: 382 EA 74 E -1662-4 C 64-96 D 7-676040586913
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Targeting data{#targeting-data}

## Selecting data {#selecting-data}

다음 활동을 사용하여 데이터를 선택할 수 있습니다.

* **[!UICONTROL Query]** 활동을 통해 Adobe Campaign 데이터베이스에서 요소 모집단을 필터링하고 추출할 수 있습니다. [쿼리](../../automating/using/query.md) 섹션을 참조하십시오.
* **[!UICONTROL Incremental query]** 활동을 통해 Adobe Campaign 데이터베이스에서 요소 모집단을 필터링하고 추출할 수 있습니다. 이 활동이 실행될 때마다 이전 실행의 결과가 제외됩니다. 이렇게 하면 새 요소만 타깃팅할 수 있습니다. [증분 쿼리](../../automating/using/incremental-query.md) 섹션을 참조하십시오.
* **[!UICONTROL Read audience]** 활동을 사용하면 기존 대상을 검색하고 추가 필터링 조건을 적용하여 중재할 수 있습니다. 대상자 [읽기](../../automating/using/read-audience.md) 섹션을 참조하십시오.

## Segmenting data {#segmenting-data}

Adobe Campaign를 사용하면 인바운드 데이터에 대한 세트를 처리할 수 있습니다. 따라서 여러 모집단을 결합하거나, 일부를 제외하거나, 여러 대상에만 공통되는 데이터를 유지할 수 있습니다.

* **[!UICONTROL Union]** 활동을 통해 여러 활동의 결과를 하나의 타겟으로 다시 그룹화할 수 있습니다. [Union](../../automating/using/union.md) 섹션을 참조하십시오.
* **[!UICONTROL Intersection]** 활동을 사용하면 활동에서 다른 인바운드 모집단에 공통되는 요소만 유지할 수 있습니다. [교차](../../automating/using/intersection.md) 섹션을 참조하십시오.
* **[!UICONTROL Exclusion]** 활동을 통해 특정 기준에 따라 한 모집단에서 요소를 제외할 수 있습니다. [제외](../../automating/using/exclusion.md) 섹션을 참조하십시오.
* **[!UICONTROL Segmentation]** 활동을 사용하면 워크플로우 이전에 제출한 활동에 의해 계산된 모집단으로부터 하나 또는 여러 세그먼트를 만들 수 있습니다. 활동이 종료되면 하나의 전환 또는 다른 전환을 통해 처리할 수 있습니다. [세그멘테이션](../../automating/using/segmentation.md) 섹션을 참조하십시오.

## Enriching data {#enriching-data}

식별되고 수집된 데이터는 Target 건설을 최적화하기 위해 농축되고, 집계되고, 조작할 수 있습니다. 데이터 마트에서 모델링되지 않은 데이터를 포함하여 타깃팅 프로세스를 단순화하고 최적화할 수 있습니다.

The **[!UICONTROL Additional data]** tab of the **[!UICONTROL Query]** and **[!UICONTROL Incremental query]** activities allows you to enrich the data targeted by the query and transfer this data to the following workflow activities, where it can be utilized. 특히 다음을 추가할 수 있습니다.

* 간단한 데이터
* 집계
* 컬렉션

