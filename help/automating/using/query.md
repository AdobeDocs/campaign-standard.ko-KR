---
title: 쿼리
description: 쿼리 활동을 사용하면 Adobe Campaign 데이터베이스에서 요소 모집단을 필터링하고 추출할 수 있습니다.
page-status-flag: never-activated
uuid: b3c629fa-370e-481c-b347-fcf9f5a5e847
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: 8d46ce28-0101-4f13-865a-2208ed6d6139
context-tags: query,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 87e0611fae0560aca276caa3c4cf793e9c095d72
workflow-type: tm+mt
source-wordcount: '1725'
ht-degree: 0%

---


# 쿼리{#query}

## 설명 {#description}

![](assets/query.png)

이 **[!UICONTROL Query]** 활동을 통해 Adobe Campaign 데이터베이스에서 요소 모집단을 필터링하고 추출할 수 있습니다. 전용 탭 **[!UICONTROL Additional data]** 을 통해 타깃팅된 모집단에 대해 정의할 수 있습니다. 이 데이터는 추가 열에 저장되며 진행 중인 워크플로우에만 사용할 수 있습니다.

활동은 쿼리 편집기 도구를 사용합니다. 이 도구는 [전용 섹션에 자세히 설명되어 있습니다](../../automating/using/editing-queries.md#about-query-editor).

**관련 항목:**

* [쿼리 샘플](../../automating/using/query-samples.md)
* [사용 사례: 따개가 아닌 사람에게 새 배달을 보내는 다시 타깃팅 워크플로우](../../automating/using/workflow-cross-channel-retargeting.md)

## 사용 상황 {#context-of-use}

이 **[!UICONTROL Query]** 활동은 다양한 유형의 용도로 사용할 수 있습니다.

* 메시지, 대상 등의 대상을 정의하기 위한 개인 세그먼트화
* 전체 Adobe Campaign 데이터베이스 테이블의 데이터를 증가시킵니다.
* 데이터 내보내기를 참조하십시오.

## 구성 {#configuration}

1. 활동을 워크플로우로 드래그하여 **[!UICONTROL Query]** 놓습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 활동을 엽니다. 기본적으로 활동이 프로파일을 검색하도록 미리 구성되어 있습니다.
1. 프로필 리소스 이외의 리소스에 대해 쿼리를 실행하려면 활동의 **[!UICONTROL Properties]** 탭으로 이동하여 **[!UICONTROL Resource]** 및 **[!UICONTROL Targeting dimension]** a를 선택합니다.

   The **[!UICONTROL Resource]** **[!UICONTROL Targeting dimension]** allows you to refine the filters discreases in the palette, whereas the context of the resource selected, contextual to obtain the type of populse that you want to obtain (identified profiles, delivery, linked to the selected resource 등에 연결된 데이터 등).

   자세한 내용은 [차원 및 리소스 타깃팅을 참조하십시오](#targeting-dimensions-and-resources).

1. 탭에서 규칙을 **[!UICONTROL Target]** 정의하고 결합하여 쿼리를 실행합니다.
1. 전용 탭 **[!UICONTROL Additional data]** 을 통해 타깃팅된 모집단에 대해 정의할 수 있습니다. 이 데이터는 추가 열에 저장되며 진행 중인 워크플로우에만 사용할 수 있습니다. 특히 쿼리의 타깃팅 차원에 연결된 Adobe Campaign 데이터베이스 테이블의 데이터를 추가할 수 있습니다. 데이터 [를](#enriching-data) 농축합니다.

   >[!NOTE]
   >
   >기본적으로 쿼리 **[!UICONTROL Remove duplicate rows (DISTINCT)]** 탭 **[!UICONTROL Advanced options]** 에서 **[!UICONTROL Additional data]** 옵션이 선택되어 있습니다. 활동에 많은(100부터) 추가 데이터가 정의된 경우, 성능상의 이유로 이 옵션의 선택을 취소하는 것이 좋습니다. **[!UICONTROL Query]** 이 옵션을 선택 해제하면 쿼리된 데이터에 따라 중복 항목이 생성될 수 있습니다.

1. 이 **[!UICONTROL Transition]** 탭에서 쿼리 활동 뒤에 아웃바운드 전환 **[!UICONTROL Enable an outbound transition]** 을 추가할 수 있습니다(데이터가 검색되지 않더라도).

   아웃바운드 전환 세그먼트 코드는 표준 표현식 및 이벤트 변수를 사용하여 개인화할 수 있습니다(이벤트 변수를 사용하여 [활동 사용자 지정 참조](../../automating/using/calling-a-workflow-with-external-parameters.md#customizing-activities-with-events-variables)).

1. 활동 구성을 확인하고 워크플로우를 저장합니다.

## 차원 및 리소스 타깃팅 {#targeting-dimensions-and-resources}

차원 및 리소스 타깃팅을 사용하면 쿼리의 기반이 되는 요소를 정의하여 배달을 결정할 수 있습니다.

타깃팅 차원은 대상 매핑에서 정의됩니다. 이 작업에 대한 자세한 정보는 [이 섹션](../../administration/using/target-mappings-in-campaign.md)을 참조하십시오.

타깃팅 차원 및 리소스는 워크플로우를 만들 때 쿼리 활동의 **[!UICONTROL Properties]** 탭에서 정의됩니다.

>[!NOTE]
>
>대상을 만들 때도 타깃팅 차원을 정의할 수 있습니다( [이 섹션 참조](../../audiences/using/creating-audiences.md)).

![](assets/targeting_dimension1.png)

타깃팅 차원 및 리소스가 연결됩니다. 따라서 사용 가능한 타깃팅 차원은 선택한 리소스에 따라 다릅니다.

예를 들어 리소스의 경우 다음 타깃팅 차원 **[!UICONTROL Profiles (profile)]**&#x200B;을 사용할 수 있습니다.

![](assets/targeting_dimension2.png)

for **[!UICONTROL Deliveries (delivery)]**&#x200B;의 경우, 목록에는 다음 타깃팅 차원이 포함됩니다.

![](assets/targeting_dimension3.png)

타깃팅 차원과 리소스가 지정되면 쿼리에 다른 필터를 사용할 수 있습니다.

리소스에 사용할 수 있는 필터 **[!UICONTROL Profiles (profile)]** 예:

![](assets/targeting_dimension4.png)

리소스에 사용할 수 있는 필터 **[!UICONTROL Deliveries (delivery)]** 예:

![](assets/targeting_dimension5.png)

기본적으로 타깃팅 차원 및 리소스는 프로파일을 타깃팅하기 위해 설정됩니다. 하지만 멀리 떨어진 테이블에서 특정 레코드를 검색하려는 경우 타깃팅 차원과 다른 리소스를 사용하는 것이 유용할 수 있습니다.

자세한 내용은 다음 사용 사례를 참조하십시오. [타깃팅 차원과 다른 리소스 사용](../../automating/using/using-resources-different-from-targeting-dimensions.md)

## 데이터 농축 {#enriching-data}

탭 **[!UICONTROL Additional data]** **[!UICONTROL Query]**&#x200B;과 **[!UICONTROL Incremental query]** **[!UICONTROL Enrichment]** 활동을 통해 타깃팅된 데이터를 보강하고 이 데이터를 활용할 수 있는 다음 워크플로우 활동으로 전송할 수 있습니다. 특히 다음을 추가할 수 있습니다.

* 간단한 데이터
* 집계
* 컬렉션

집계 및 컬렉션의 경우 **[!UICONTROL Alias]** 는 복잡한 표현식에 기술 ID를 제공하도록 자동으로 정의됩니다. 이 별칭은 고유해야 하므로 이후 수집 및 컬렉션을 쉽게 찾을 수 있습니다. 쉽게 인식할 수 있도록 수정할 수 있습니다.

>[!NOTE]
>
>별칭은 다음 구문 규칙을 준수해야 합니다. 영숫자 및 &quot;_&quot; 문자만 허용됩니다. 별칭은 대소문자를 구분합니다. 별칭은 &quot;@&quot; 문자로 시작해야 합니다. &quot;@&quot; 바로 다음에 오는 문자는 숫자일 수 없습니다. 예: @myAlias_1 및 @_1별칭이 올바릅니다. 반면에 @myAlias#1 및 @1별칭은 잘못되었습니다.

추가 데이터를 추가한 후 정의된 추가 데이터를 기반으로 조건을 만들어 처음에 타깃팅된 데이터에 추가 필터 수준을 적용할 수 있습니다.

>[!NOTE]
>
>기본적으로 쿼리 **[!UICONTROL Remove duplicate rows (DISTINCT)]** 탭 **[!UICONTROL Advanced options]** 에서 **[!UICONTROL Additional data]** 옵션이 선택되어 있습니다. 활동에 많은(100부터) 추가 데이터가 정의된 경우, 성능상의 이유로 이 옵션의 선택을 취소하는 것이 좋습니다. **[!UICONTROL Query]** 이 옵션을 선택 해제하면 쿼리된 데이터에 따라 중복 항목이 생성될 수 있습니다.

추가 데이터가 포함된 이메일을 개인화하는 방법에 대한 사용 사례가 [이 섹션에 나와 있습니다](../../automating/using/personalizing-email-with-additional-data.md).

### 간단한 필드 추가 {#adding-a-simple-field}

단순 필드를 추가 데이터로 추가하면 해당 필드가 활동의 아웃바운드 전환에서 직접 표시됩니다. 이를 통해 사용자는 쿼리의 데이터가 원하는 데이터인지 확인할 수 있습니다.

1. 탭에서 **[!UICONTROL Additional data]** 새 요소를 추가합니다.
1. 표시되는 창의 **[!UICONTROL Expression]** 필드에서 타깃팅 차원이나 연결된 차원 중 하나에서 직접 사용할 수 있는 필드 중 하나를 선택합니다. 표현식을 편집하고 차원 필드의 함수 또는 간단한 계산(합계 제외)을 사용할 수 있습니다.

   단순 XPATH 경로 **[!UICONTROL Alias]** 가 아닌 표현식을 편집하면 가 자동으로 만들어집니다(예: &quot;Year(&lt;@birthDate>)&quot;). 원하는 경우 수정할 수 있습니다. 필드를 하나만 선택하면 됩니다(예: &quot;@age&quot;), **[!UICONTROL Alias]**

1. 추가 데이터 **[!UICONTROL Add]** 에 필드를 추가하려면 선택합니다. 쿼리가 실행될 때 추가된 필드에 해당하는 추가 열이 활동의 아웃바운드 전환에 나타납니다.

![](assets/enrichment_add_simple_field.png)

### 집계 추가 {#adding-an-aggregate}

집계를 사용하면 타깃팅 차원의 필드 또는 타깃팅 차원에 연결된 차원의 필드에서 값을 계산할 수 있습니다. 예: 프로필에서 구매한 평균 금액.
집계 함수를 쿼리와 함께 사용할 경우 해당 함수는 0으로 반환되고 이 함수는 NULL로 간주됩니다. 쿼리의 **[!UICONTROL Output filtering]** 탭을 사용하여 집계된 값을 필터링합니다.

* 0 값을 원하는 경우 필터링해야 합니다 **[!UICONTROL is null]**.
* 0으로 필터링하지 않으려는 경우 **[!UICONTROL is not null]**.

집계에 정렬을 적용해야 하는 경우 0값을 필터링해야 합니다. 그렇지 않으면 NULL 값이 가장 큰 숫자로 나타납니다.

1. 탭에서 **[!UICONTROL Additional data]** 새 요소를 추가합니다.
1. 표시되는 창에서 필드에 집계를 만드는 데 사용할 컬렉션을 **[!UICONTROL Expression]** 선택합니다.

   자동으로 **[!UICONTROL Alias]** 만들어집니다. 원하는 경우 쿼리의 **[!UICONTROL Additional data]** 탭으로 돌아가 수정할 수 있습니다.

   합계 정의 창이 열립니다.

1. 탭에서 합계를 **[!UICONTROL Data]** 정의합니다. 선택한 집계 유형에 따라 데이터가 호환되는 요소만 **[!UICONTROL Expression]** 필드에서 사용할 수 있습니다. 예를 들어 숫자 데이터만 사용하여 합계를 계산할 수 있습니다.

   ![](assets/enrichment_add_aggregate.png)

   선택한 컬렉션의 필드에 여러 개의 집계를 추가할 수 있습니다. 활동의 아웃바운드 데이터에 대한 세부 사항에서 서로 다른 열을 구분하기 위해 명시적 레이블을 정의해야 합니다.

   각 합계에 대해 자동으로 정의된 별칭을 변경할 수도 있습니다.

   ![](assets/enrichment_add_aggregate2.png)

1. 필요한 경우 필터를 추가하여 고려되는 데이터를 제한할 수 있습니다.

   추가된 데이터 [필터링 섹션을](#filtering-added-data) 참조하십시오.

1. 집계 **[!UICONTROL Confirm]** 를 추가하려면 선택합니다.

>[!NOTE]
>
>창의 필드에서 직접 집계를 포함하는 표현식을 만들 수 **[!UICONTROL Expression]** **[!UICONTROL New additional data]** 없습니다.

### 컬렉션 추가 {#adding-a-collection}

1. 탭에서 **[!UICONTROL Additional data]** 새 요소를 추가합니다.
1. 표시되는 창에서 **[!UICONTROL Expression]** 필드에 추가할 컬렉션을 선택합니다. 자동으로 **[!UICONTROL Alias]** 만들어집니다. 원하는 경우 쿼리의 **[!UICONTROL Additional data]** 탭으로 돌아가 수정할 수 있습니다.
1. 선택합니다 **[!UICONTROL Add]**. 표시할 컬렉션 데이터를 조정할 수 있는 새 창이 열립니다.
1. 탭에서 **[!UICONTROL Parameters]** 추가하려는 컬렉션의 줄 수 **[!UICONTROL Collection]** 를 선택하고 정의합니다. 예를 들어 각 프로필에서 수행한 최근 3개 구매를 받으려면 **[!UICONTROL Number of lines to return]** 필드에 &quot;3&quot;을 입력합니다.

   >[!NOTE]
   >
   >1보다 크거나 같은 숫자를 입력해야 합니다.

1. 탭에서 **[!UICONTROL Data]** 각 행에 대해 표시할 컬렉션의 필드를 정의합니다.

   ![](assets/enrichment_add_collection.png)

1. 원하는 경우 필터를 추가하여 고려되는 수집 라인을 제한할 수 있습니다.

   추가된 데이터 [필터링 섹션을](#filtering-added-data) 참조하십시오.

1. 원하는 경우 데이터 정렬을 정의할 수 있습니다.

   예를 들어, **[!UICONTROL Parameters]** 탭에서 반환할 3개의 라인을 선택하고 가장 최근 3개의 구매를 결정하려는 경우 트랜잭션에 해당하는 컬렉션의 &quot;날짜&quot; 필드에 내림차순 정렬을 정의할 수 있습니다.

1. 추가 데이터 [정렬 섹션을](#sorting-additional-data) 참조하십시오.
1. 컬렉션 **[!UICONTROL Confirm]** 을 추가하려면 선택합니다.

### 추가된 데이터 필터링 {#filtering-added-data}

집계 또는 컬렉션을 추가할 때 표시할 데이터를 제한하는 추가 필터를 지정할 수 있습니다.

예를 들어 50달러 이상의 금액을 가진 트랜잭션 수집 라인만 처리하려는 경우 **[!UICONTROL Filter]** 탭에서 트랜잭션 금액에 해당하는 필드에 조건을 추가할 수 있습니다.

![](assets/enrichment_filter_data.png)

### 추가 데이터 정렬 {#sorting-additional-data}

쿼리 데이터에 집계 또는 컬렉션을 추가할 때 필드 또는 정의된 식에 따라 오름차순인지 내림차순인지를 정렬할지 여부를 지정할 수 있습니다.

예를 들어, 프로필에서 가장 최근에 실행한 거래만 저장하려면 **[!UICONTROL Number of lines to return]** 탭의 **[!UICONTROL Parameters]** 필드에 &quot;1&quot;을 입력하고 **[!UICONTROL Sort]** 탭을 통해 거래 날짜에 해당하는 필드에 내림차순 정렬을 적용합니다.

![](assets/enrichment_sort_data.png)

### 추가 데이터에 따라 타깃팅된 데이터 필터링 {#filtering-the-targeted-data-according-to-additional-data}

추가 데이터를 추가했으면 에 새 **[!UICONTROL Output filtering]** 탭이 나타납니다 **[!UICONTROL Query]**. 이 탭에서는 추가된 데이터를 고려하여 처음에 **[!UICONTROL Target]** 탭에 타깃팅된 데이터에 추가 필터를 적용할 수 있습니다.

예를 들어, 하나 이상의 트랜잭션을 수행한 모든 프로파일을 타깃팅하고 각 프로파일에 대해 수행된 평균 트랜잭션 금액을 집계한 합계가 에 추가된 경우, 이 평균을 사용하여 처음에 계산된 인구를 조정할 수 **[!UICONTROL Additional data]**&#x200B;있습니다.

이렇게 하려면 **[!UICONTROL Output filtering]** 탭에서 이 추가 데이터에 조건을 추가하면 됩니다.

![](assets/enrichment_output_filtering2.png)

![](assets/enrichment_output_filtering.png)
