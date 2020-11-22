---
solution: Campaign Standard
product: campaign
title: 중복 제거
description: 중복 제거 활동을 통해 인바운드 활동의 결과에서 중복을 삭제할 수 있습니다.
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: dedup,main
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '567'
ht-degree: 97%

---


# 중복 제거{#deduplication}

## 설명 {#description}

![](assets/deduplication.png)

**[!UICONTROL Deduplication]** 활동을 통해 인바운드 활동의 결과에서 중복을 삭제할 수 있습니다.

## 사용의 컨텍스트 {#context-of-use}

일반적으로 **[!UICONTROL Deduplication]** 활동은 다음의 타겟팅 활동 또는 파일을 가져온 후 타겟팅된 데이터를 사용할 수 있는 활동 전에 사용됩니다.

중복을 제거하는 동안 인바운드 전환이 개별적으로 처리됩니다. 예를 들어, 프로필 &#39;A&#39;가 쿼리 1의 결과에 있고 쿼리 2의 결과에도 있는 경우 중복 제거되지 않습니다.

따라서 중복 제거에는 인바운드 전환이 하나만 있는 것이 좋습니다. 이를 위해 조합 활동, 교차 활동 등과 같은 타겟팅 요구에 해당하는 활동을 사용하여 서로 다른 쿼리를 결합할 수 있습니다. 예제:

![](assets/dedup_bonnepratique.png)

**관련 항목**

* [사용 사례:배달 전 중복 항목 식별](../../automating/using/identifying-duplicated-before-delivery.md)
* [사용 사례:가져온 파일에서 데이터 중복 제거](../../automating/using/deduplicating-data-imported-file.md)

## 구성 {#configuration}

중복 제거 활동을 구성하려면 결과와 관련된 옵션뿐만 아니라 레이블, 방법 및 중복 제거 기준을 입력해야 합니다.

1. **[!UICONTROL Deduplication]** 활동을 워크플로우로 끌어서 놓습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업에서 ![](assets/edit_darkgrey-24px.png) 버튼을 사용하여 활동을 엽니다.

   ![](assets/deduplication_1.png)

1. 중복 제거를 수행할 **[!UICONTROL Resource type]**&#x200B;을(를) 선택합니다.

   * 중복 제거가 데이터베이스에 이미 존재하는 데이터에 대해 수행되는 경우 **[!UICONTROL Database resource]**&#x200B;을(를) 선택합니다. 중복을 제거하려는 데이터에 따라 **[!UICONTROL Filtering dimension]** 및 **[!UICONTROL Targeting dimension]**&#x200B;을(를) 선택합니다. 기본적으로 중복 제거는 **프로필**&#x200B;에서 수행됩니다.
   * 워크플로우의 임시 데이터에서 중복 제거가 수행되는 경우 **[!UICONTROL Temporary resource]**&#x200B;을(를) 선택합니다. 중복을 제거하려는 데이터가 포함된 **[!UICONTROL Targeted set]**&#x200B;을(를) 선택합니다. 이 사용 사례는 파일을 가져온 후 또는 데이터베이스의 데이터가 보강된 경우(예: 세그먼트 코드 포함) 발생할 수 있습니다.

1. **[!UICONTROL Number of unique records to keep]**&#x200B;을(를) 선택합니다. 이 필드의 기본값은 1입니다. 값 0을 사용하면 모든 중복을 유지할 수 있습니다.

   예를 들어 레코드 A와 B가 레코드 Y의 중복으로 간주되고 레코드 C가 레코드 Z의 중복으로 간주되는 경우:

   * 필드의 값이 1인 경우 레코드 Y와 Z만 유지됩니다.
   * 필드의 값이 0인 경우 모든 레코드가 유지됩니다.
   * 필드의 값이 2인 경우 레코드 C와 Z는 유지되고 A, B 및 Y의 두 레코드는 우연히 또는 이후에 선택한 중복 제거 방법에 따라 유지됩니다.

1. 제공된 목록에 조건을 추가하여 **[!UICONTROL Duplicate identification]** 기준을 정의합니다. 이메일 주소, 이름, 성 등 동일한 값에서 중복을 식별할 수 있는 필드 및/또는 표현식을 지정합니다. 조건 순서를 사용하면 먼저 처리할 항목을 지정할 수 있습니다.
1. 드롭다운 목록에서 사용할 **[!UICONTROL Deduplication method]**&#x200B;을(를) 선택합니다.

   * **[!UICONTROL Choose for me]**: 중복 중에서 유지할 레코드를 임의로 선택합니다.
   * **[!UICONTROL Following a list of values]**: 하나 이상의 필드에 대한 값 우선 순위를 정의할 수 있습니다. 값을 정의하려면 필드를 선택하거나 표현식을 만든 다음 해당 테이블에 값을 추가합니다. 새 필드를 정의하려면 값 목록 위에 있는 **[!UICONTROL Add]** 버튼을 클릭합니다.

      ![](assets/deduplication_2.png)

   * **[!UICONTROL Non-empty value]**: 선택한 표현식의 값이 비어 있지 않은 레코드를 우선 순위로 유지할 수 있습니다.

      ![](assets/deduplication_3.png)

   * **[!UICONTROL Using an expression]**: 입력한 표현식의 값이 가장 작거나 가장 큰 레코드를 유지할 수 있습니다.

      ![](assets/deduplication_4.png)

1. 필요한 경우 활동의 [전환](../../automating/using/activity-properties.md)을 관리하여 아웃바운드 모집단에 대한 고급 옵션에 액세스합니다.
1. 활동 구성을 확인하고 워크플로우를 저장합니다.
