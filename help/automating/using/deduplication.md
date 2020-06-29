---
title: 중복 제거
description: 데이터 중복 제거 활동을 통해 인바운드 활동의 결과 중복 항목을 삭제할 수 있습니다.
page-status-flag: never-activated
uuid: 11a22a9c-3bfe-4953-8a52-2f4e93c128fb
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: e7a5e1e7-4680-46c7-98b8-0a47bb7be2b8
context-tags: dedup,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c3911232a3cce00c2b9a2e619f090a7520382dde
workflow-type: tm+mt
source-wordcount: '567'
ht-degree: 0%

---


# 중복 제거{#deduplication}

## 설명 {#description}

![](assets/deduplication.png)

활동을 **[!UICONTROL Deduplication]** 통해 인바운드 활동의 결과 중복 항목을 삭제할 수 있습니다.

## 사용 상황 {#context-of-use}

일반적으로 **[!UICONTROL Deduplication]** 활동은 타깃팅된 활동 후에 또는 파일을 가져온 후 타깃팅된 데이터를 사용할 수 있는 활동 전에 사용됩니다.

데이터 중복 제거 시 인바운드 전환이 개별적으로 처리됩니다. 예를 들어, 쿼리 1의 결과에 &#39;A&#39; 프로필이 있고 쿼리 2의 결과에도 있는 경우 중복 제거가 되지 않습니다.

따라서 데이터 중복 제거는 인바운드 전환이 하나만 있는 것이 좋습니다. 이를 위해 조합 활동, 교차 활동 등과 같은 타깃팅 요구 사항에 해당하는 활동을 사용하여 서로 다른 쿼리를 결합할 수 있습니다. 예:

![](assets/dedup_bonnepratique.png)

**관련 항목**

* [사용 사례: 배달 전 중복 항목 식별](../../automating/using/identifying-duplicated-before-delivery.md)
* [사용 사례: 가져온 파일에서 데이터 중복 제거](../../automating/using/deduplicating-data-imported-file.md)

## 구성 {#configuration}

데이터 중복 제거 활동을 구성하려면 결과 관련 옵션뿐만 아니라 레이블, 방법 및 데이터 중복 제거 기준을 입력해야 합니다.

1. 활동을 워크플로우로 드래그하여 **[!UICONTROL Deduplication]** 놓습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 활동을 엽니다.

   ![](assets/deduplication_1.png)

1. 데이터 중복 제거 **[!UICONTROL Resource type]** 를 수행할 대상 선택:

   * **[!UICONTROL Database resource]** 데이터 중복 제거가 데이터베이스에 이미 존재하는 데이터에 대해 수행되는 경우 중복 **[!UICONTROL Filtering dimension]** 을 **[!UICONTROL Targeting dimension]**&#x200B;제거하려는 데이터에 따라 및 를 선택합니다. 데이터 중복 제거는 기본적으로 **프로파일에서 수행됩니다**.
   * **[!UICONTROL Temporary resource]** 워크플로우의 임시 데이터에 대해 중복 제거가 수행되는 경우: 중복 **[!UICONTROL Targeted set]** 제거하려는 데이터가 포함된 항목을 선택합니다. 이 사용 사례는 파일을 가져온 후 또는 데이터베이스의 데이터가 풍부해진 경우(예: 세그먼트 코드 포함) 발생할 수 있습니다.

1. 을 **[!UICONTROL Number of unique records to keep]**&#x200B;선택합니다. 이 필드의 기본값은 1입니다. 값 0을 사용하면 모든 중복을 유지할 수 있습니다.

   예를 들어 레코드 A와 B가 레코드 Y의 중복으로 간주되고 레코드 C가 레코드 Z의 중복으로 간주되는 경우:

   * 필드의 값이 1인 경우: Y와 Z 레코드만 보관됩니다.
   * 필드의 값이 0이면: 모든 기록은 보관된다.
   * 필드의 값이 2인 경우: C 와 Z 는 보존되고 A, B 및 Y의 2개의 레코드는 나중에 선택한 데이터 중복 제거 방법에 따라 보관됩니다.

1. 제공된 목록에 조건을 추가하여 **[!UICONTROL Duplicate identification]** 기준을 정의합니다. 동일한 값에서 중복을 식별할 수 있는 필드 및/또는 표현식을 지정합니다. 이메일 주소, 이름, 성 등 조건의 순서를 사용하면 먼저 처리할 조건을 지정할 수 있습니다.
1. 드롭다운 목록에서 사용할 항목 **[!UICONTROL Deduplication method]** 을 선택합니다.

   * **[!UICONTROL Choose for me]**: 임의로 복제되지 않도록 할 레코드를 선택합니다.
   * **[!UICONTROL Following a list of values]**: 하나 이상의 필드에 대한 값 우선 순위를 정의할 수 있습니다. 값을 정의하려면 필드를 선택하거나 표현식을 만든 다음 해당 표에 값을 추가합니다. 새 필드를 정의하려면 값 목록 위에 있는 **[!UICONTROL Add]** 단추를 클릭합니다.

      ![](assets/deduplication_2.png)

   * **[!UICONTROL Non-empty value]**: 이렇게 하면 선택한 표현식의 값이 우선 순위로 비어 있지 않은 레코드를 유지할 수 있습니다.

      ![](assets/deduplication_3.png)

   * **[!UICONTROL Using an expression]**: 이렇게 하면 입력한 표현식 값이 가장 작거나 가장 큰 레코드를 유지할 수 있습니다.

      ![](assets/deduplication_4.png)

1. 필요한 경우 활동의 전환 [을](../../automating/using/activity-properties.md) 관리하여 아웃바운드 모형에 대한 고급 옵션에 액세스합니다.
1. 활동 구성을 확인하고 워크플로우를 저장합니다.
