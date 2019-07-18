---
title: enrichment
seo-title: enrichment
description: enrichment
seo-description: 강화 활동은 워크플로우에서 처리할 추가 데이터를 정의할 수 있도록 해주는 고급 활동입니다.
page-status-flag: 정품 인증 안 함
uuid: 8 C 1693 EF -1312-422 C-B 05 D -263553113 F 8 F
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 타깃팅 활동
discoiquuid: F 67 C 1 CAF -3284-4 C 34-A 5 B 0-8654 A 95640 AE
context-tags: 강화, 기본
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 0454dac1a7976c1be2838c2a846d33e77e60c3b3

---


# Enrichment{#enrichment}

## Description {#description}

![](assets/enrichment.png)

**[!UICONTROL Enrichment]** 활동은 워크플로우에서 처리할 추가 데이터를 정의할 수 있도록 해주는 고급 활동입니다.

## Context of use {#context-of-use}

**[!UICONTROL Enrichment]** 활동은 일반적으로 타깃팅 활동 이후 또는 파일을 가져온 후 타깃팅된 데이터의 사용을 허용하는 활동 전에 사용됩니다.

This activity contains more advanced enrichment functions than the **[!UICONTROL Query]** activity. Some simple cases of enrichment can be directly performed in the [Query activity](../../automating/using/query.md#enriching-data).

**[!UICONTROL Enrichment]** 활동을 통해 인바운드 전환을 활용하고 추가 데이터를 사용하여 출력 전환을 완료하는 활동을 구성할 수 있습니다. 여러 세트에서 나오는 데이터를 결합하거나 임시 리소스에 대한 링크를 만들 수 있습니다.

## Configuration {#configuration}

**[!UICONTROL Enrichment]** 활동을 구성하려면 다음을 수행하십시오.

1. **[!UICONTROL Enrichment]** 워크플로우를 워크플로우로 드래그하여 놓습니다.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. If the activity has several inbound transitions, select the **[!UICONTROL Primary set]**. 이 활동에 구성된 추가 데이터는 아웃바운드 전환 시 이 기본 세트에 추가됩니다.

   기본 세트에 이미 추가 데이터가 들어 있는 경우 해당 세트를 유지하거나 제거하도록 선택할 수 있습니다. **[!UICONTROL Keep all additional data from the main set]** 이 옵션을 선택 취소하면에 구성된 추가 데이터만 **[!UICONTROL Enrichment]** 아웃바운드 전환에서 유지됩니다.

1. If there are several inbound transitions, define relations between the primary set and the other inbound data in the **[!UICONTROL Advanced Relations]** tab of the activity. You can add several relations using the **[!UICONTROL Add element]** button.

   새 관계를 정의할 때 기본 세트에 연결할 인바운드 데이터 세트를 선택합니다. 그런 다음 관계 유형을 정의합니다. 인바운드 데이터 및 데이터 모델에 따라 여러 유형의 관계를 사용할 수 있습니다.

   * **[!UICONTROL 1 cardinality simple link]**: 들어오는 데이터의 각 레코드는 기본 세트에서 한 개의 레코드에만 연결되어 있습니다. 기본 세트의 각 레코드에는 연결된 데이터에 연결된 레코드가 하나 있습니다.
   * **[!UICONTROL N cardinality collection link]**: 0, 연결된 데이터의 1 개 이상의 레코드를 기본 세트의 1 개 레코드에 연결할 수 있습니다.
   * **[!UICONTROL 0 or 1 cardinality simple link]**: 기본 세트의 레코드는 연결된 데이터의 0 또는 1 레코딩과 연결할 수 있지만 두 개 이하여야 합니다.
   Once the **[!UICONTROL Cardinality]** is defined, define a **[!UICONTROL Reconciliation criteria]**. The **[!UICONTROL Source expression]** of the reconciliation criteria can be a field from the target resource, an [expression](../../automating/using/advanced-expression-editing.md) or directly a value specified between quotes.

   Define a **[!UICONTROL Label]** and an **[!UICONTROL ID]** that will be easy to identify later in the workflow.

   >[!NOTE]
   >
   >You can only define relations between the primary set and the other inbound transitions connected to the **[!UICONTROL Enrichment]** activity. For simpler cases aiming at defining relations with database resources, use a [Reconciliation](../../automating/using/reconciliation.md) activity.

1. Define the additional data from the **[!UICONTROL Additional data]** tab of the activity. You can define additional data (simple fields, aggregates and collections) related to the targeting dimension of the primary set or based on the links created in the **[!UICONTROL Advanced relations]** tab of the **[!UICONTROL Enrichment]** activity.

   [데이터 강화](../../automating/using/query.md#enriching-data) 섹션을 참조하십시오.

1. 활동의 구성을 확인하고 워크플로우를 저장합니다.

The data is now available to use in the activities connected after the **[!UICONTROL Enrichment]**. For example, you can find it under the **[!UICONTROL Additional data (targetData)]** link of the personalization fields explorer in an email content.

## Example: Enriching profile data with data contained in a file {#example--enriching-profile-data-with-data-contained-in-a-file}

이 예에서는 파일에 포함된 구매 데이터로 프로필 데이터를 보강하는 방법을 보여줍니다. 구매 데이터가 타사 시스템에 저장되어 있다고 간주합니다. 각 프로필에는 파일에 여러 개의 구매를 저장할 수 있습니다. 워크플로우의 마지막 목표는 두 개 이상의 항목을 구입한 타겟 프로필에 이메일을 전송하여 해당 충성도를 평가하는 것입니다.

워크플로우는 다음과 같이 구성됩니다.

![](assets/enrichment_example_workflow.png)

* A **[!UICONTROL Query]** activity that targets the profiles who will receive the message.
* A **[!UICONTROL Load file]** activity that loads the purchase data. 예를 들면 다음과 같습니다.

   ```
   tcode;tdate;customer;product;tamount
   aze123;21/05/2017;dannymars@example.com;TV;799
   aze124;28/05/2017;dannymars@example.com;Headphones;8
   aze125;31/07/2017;john.smith@example.com;Headphones;8
   aze126;14/12/2017;john.smith@example.com;Plastic Cover;4
   aze127;02/01/2018;dannymars@example.com;Case Cover;79
   aze128;04/03/2017;clara.smith@example.com;Phone;149
   ```

   이 예제 파일을 사용하여 이메일 주소를 사용하여 데이터를 데이터베이스 프로파일과 조정합니다. You can also enable unique IDs as described in [this document](../../developing/using/configuring-the-resource-s-data-structure.md#generating-a-unique-id-for-profiles-and-custom-resources).

* An **[!UICONTROL Enrichment]** activity that creates a link between the transaction data loaded from the file and the profiles selected in the **[!UICONTROL Query]**. The link is defined in the **[!UICONTROL Advanced relations]** tab of the activity. The link is based on the transition coming from the **[!UICONTROL Load file]** activity. 프로필 리소스의 "email" 필드와 가져온 파일의 "customer" 열을 조정 기준으로 사용합니다.

   ![](assets/enrichment_example_workflow2.png)

   Once the link is created, two sets of **[!UICONTROL Additional data]** are added:

   * 각 프로필의 마지막 트랜잭션에 해당하는 두 줄의 모음입니다. 이 컬렉션의 경우 제품 이름, 거래 날짜 및 제품 가격이 추가 데이터로 추가됩니다. 데이터에 내림차순 정렬이 적용됩니다. To create the collection, from the **[!UICONTROL Additional data]** tab:

      Select the link previously defined in the **[!UICONTROL Advanced relations]** tab of the activity.

      ![](assets/enrichment_example_workflow3.png)

      Check **[!UICONTROL Collection]** and specify the number of lines to retrieve (2 in this example). In this screen, you can customize the **[!UICONTROL Alias]** and the **[!UICONTROL Label]** of the collection. 이러한 값은 이 컬렉션을 참조할 때 워크플로우의 다음 활동에 표시됩니다.

      ![](assets/enrichment_example_workflow4.png)

      As **[!UICONTROL Data]** to keep for the collection, select the columns that will be used in the final delivery.

      ![](assets/enrichment_example_workflow6.png)

      거래 날짜에 내림차순 정렬을 적용하여 최신 거래를 검색합니다.

      ![](assets/enrichment_example_workflow7.png)

   * 각 프로필에 대한 총 트랜잭션 수를 계산하는 합계입니다. 이 집계에서는 나중에 두 개 이상의 트랜잭션이 기록된 프로필을 필터링하는 데 사용됩니다. To create the aggregate, from the **[!UICONTROL Additional data]** tab:

      Select the link previously defined in the **[!UICONTROL Advanced relations]** tab of the activity.

      ![](assets/enrichment_example_workflow3.png)

      **[!UICONTROL Aggregate]** Select.

      ![](assets/enrichment_example_workflow8.png)

      As **[!UICONTROL Data]** to keep, define a **Count All** aggregate. 필요한 경우 다음 활동에서 사용자 정의 별칭을 지정하여 더 빠르게 찾을 수 있습니다.

      ![](assets/enrichment_example_workflow9.png)

* A **[!UICONTROL Segmentation]** activity with only one segment, that retrieves profiles of the initial target that have at least two transactions recorded. 트랜잭션이 하나만 있는 프로필은 제외됩니다. 이렇게 하려면 이전에 정의된 세그먼트에서 세그멘테이션의 쿼리가 만들어집니다.

   ![](assets/enrichment_example_workflow5.png)

* An **[!UICONTROL Email delivery]** activity that uses the additional data defined in the **[!UICONTROL Enrichment]** to dynamically retrieve the two last purchases made by the profile. The additional data can be found in the **Additional data (TargetData)** node when adding a personalization field.

   ![](assets/enrichment_example_workflow10.png)

