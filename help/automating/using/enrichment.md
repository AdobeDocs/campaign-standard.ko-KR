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
source-git-commit: 782a5f89b0361f1cbe59c9b353ca90dec90c3906

---


# enrichment{#enrichment}

## description {#description}

![](assets/enrichment.png)

**[!UICONTROL Enrichment]** 활동은 워크플로우에서 처리할 추가 데이터를 정의할 수 있도록 해주는 고급 활동입니다.

## 사용 상황 {#context-of-use}

**[!UICONTROL Enrichment]** 활동은 일반적으로 타깃팅 활동 이후 또는 파일을 가져온 후 타깃팅된 데이터의 사용을 허용하는 활동 전에 사용됩니다.

이 활동에는 **[!UICONTROL Query]** 활동보다 더 많은 고급 보강 기능이 포함되어 있습니다. 일부 간단한 취약점은 [쿼리 활동에서 직접 수행할 수 있습니다.](../../automating/using/query.md#enriching-data)

**[!UICONTROL Enrichment]** 활동을 통해 인바운드 전환을 활용하고 추가 데이터를 사용하여 출력 전환을 완료하는 활동을 구성할 수 있습니다. 여러 세트에서 나오는 데이터를 결합하거나 임시 리소스에 대한 링크를 만들 수 있습니다.

## 구성 {#configuration}

**[!UICONTROL Enrichment]** 활동을 구성하려면 다음을 수행하십시오.

1. **[!UICONTROL Enrichment]** 워크플로우를 워크플로우로 드래그하여 놓습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업에서 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 엽니다.
1. 활동에 여러 개의 인바운드 전환이 있는 경우를 선택합니다 **[!UICONTROL Primary set]**. 이 활동에 구성된 추가 데이터는 아웃바운드 전환 시 이 기본 세트에 추가됩니다.

   기본 세트에 이미 추가 데이터가 들어 있는 경우 해당 세트를 유지하거나 제거하도록 선택할 수 있습니다. **[!UICONTROL Keep all additional data from the main set]** 이 옵션을 선택 취소하면에 구성된 추가 데이터만 **[!UICONTROL Enrichment]** 아웃바운드 전환에서 유지됩니다.

1. 여러 개의 인바운드 전환이 있을 경우, 활동 **[!UICONTROL Advanced Relations]** 탭의 기본 세트와 다른 인바운드 데이터 간의 관계를 정의합니다. 단추를 사용하여 여러 관계를 추가할 **[!UICONTROL Add element]** 수 있습니다.

   새 관계를 정의할 때 기본 세트에 연결할 인바운드 데이터 세트를 선택합니다. 그런 다음 관계 유형을 정의합니다. 인바운드 데이터 및 데이터 모델에 따라 여러 유형의 관계를 사용할 수 있습니다.

   * **[!UICONTROL 1 cardinality simple link]**: 들어오는 데이터의 각 레코드는 기본 세트에서 한 개의 레코드에만 연결되어 있습니다. 기본 세트의 각 레코드에는 연결된 데이터에 연결된 레코드가 하나 있습니다.
   * **[!UICONTROL N cardinality collection link]**: 0, 연결된 데이터의 1 개 이상의 레코드를 기본 세트의 1 개 레코드에 연결할 수 있습니다.
   * **[!UICONTROL 0 or 1 cardinality simple link]**: 기본 세트의 레코드는 연결된 데이터의 0 또는 1 레코딩과 연결할 수 있지만 두 개 이하여야 합니다.
   가 정의되고 **[!UICONTROL Cardinality]** 나면 **[!UICONTROL Reconciliation criteria]** a를 정의합니다. 조정 **[!UICONTROL Source expression]** 기준은 타겟 리소스, [표현식의](../../automating/using/advanced-expression-editing.md) 필드 또는 따옴표 사이에 지정된 값이 될 수 있습니다.

   A **[!UICONTROL Label]** and an **[!UICONTROL ID]** that will be easy will be identify in identify in the workflow.

   >[!NOTE]
   >
   >기본 세트와 **[!UICONTROL Enrichment]** 활동에 연결된 다른 인바운드 전환 간의 관계만 정의할 수 있습니다. 데이터베이스 리소스를 사용하여 관계를 정의하는 것을 목표로 하는 보다 간단한 경우를 위해 [조정](../../automating/using/reconciliation.md) 활동을 사용하십시오.

1. 활동 **[!UICONTROL Additional data]** 탭에서 추가 데이터를 정의합니다. 기본 세트의 타깃팅 차원과 관련된 추가 데이터 (단순 필드, 집계 및 컬렉션) 를 정의하거나 활동 **[!UICONTROL Advanced relations]** 탭에서 생성된 링크를 기반으로 할 수 **[!UICONTROL Enrichment]** 있습니다.

   [데이터 강화](../../automating/using/query.md#enriching-data) 섹션을 참조하십시오.

1. 활동의 구성을 확인하고 워크플로우를 저장합니다.

이제 데이터 다음에 연결된 활동에서 데이터를 사용할 수 있습니다 **[!UICONTROL Enrichment]**. 예를 들어 이메일 컨텐츠의 개인화 필드 탐색기의 링크 **[!UICONTROL Additional data (targetData)]** 아래에서 찾을 수 있습니다.

## 예: 파일에 포함된 데이터로 프로필 데이터 강화 {#example--enriching-profile-data-with-data-contained-in-a-file}

이 예에서는 파일에 포함된 구매 데이터로 프로필 데이터를 보강하는 방법을 보여줍니다. 구매 데이터가 타사 시스템에 저장되어 있다고 간주합니다. 각 프로필에는 파일에 여러 개의 구매를 저장할 수 있습니다. 워크플로우의 마지막 목표는 두 개 이상의 항목을 구입한 타겟 프로필에 이메일을 전송하여 해당 충성도를 평가하는 것입니다.

워크플로우는 다음과 같이 구성됩니다.

![](assets/enrichment_example_workflow.png)

* 메시지를 받을 프로필을 타깃팅하는 **[!UICONTROL Query]** 활동입니다.
* 구매 데이터를 로드하는 **[!UICONTROL Load file]** 활동입니다. 예를 들면 다음과 같습니다.

   ```
   tcode;tdate;customer;product;tamount
   aze123;21/05/2017;dannymars@example.com;TV;799
   aze124;28/05/2017;dannymars@example.com;Headphones;8
   aze125;31/07/2017;john.smith@example.com;Headphones;8
   aze126;14/12/2017;john.smith@example.com;Plastic Cover;4
   aze127;02/01/2018;dannymars@example.com;Case Cover;79
   aze128;04/03/2017;clara.smith@example.com;Phone;149
   ```

   이 예제 파일을 사용하여 이메일 주소를 사용하여 데이터를 데이터베이스 프로파일과 조정합니다. 이 문서에 설명된 대로 고유 ID를 활성화할 [](../../developing/using/configuring-the-resource-s-data-structure.md#generating-a-unique-id-for-profiles-and-custom-resources)수도 있습니다.

* 파일에서 로드한 트랜잭션 데이터와에서 선택한 프로필 사이에 링크를 만드는 **[!UICONTROL Enrichment]** 활동입니다 **[!UICONTROL Query]**. 링크는 활동의 **[!UICONTROL Advanced relations]** 탭에 정의됩니다. 링크는 **[!UICONTROL Load file]** 활동에서 나오는 전환을 기반으로 합니다. 프로필 리소스의 "email" 필드와 가져온 파일의 "customer" 열을 조정 기준으로 사용합니다.

   ![](assets/enrichment_example_workflow2.png)

   링크를 만들면 두 개의 세트가 **[!UICONTROL Additional data]** 추가됩니다.

   * 각 프로필의 마지막 트랜잭션에 해당하는 두 줄의 모음입니다. 이 컬렉션의 경우 제품 이름, 거래 날짜 및 제품 가격이 추가 데이터로 추가됩니다. 데이터에 내림차순 정렬이 적용됩니다. To create the collection, from the **[!UICONTROL Additional data]** tab:

      활동 **[!UICONTROL Advanced relations]** 탭에서 이전에 정의한 링크를 선택합니다.

      ![](assets/enrichment_example_workflow3.png)

      검색할 라인 수를 확인하고 **[!UICONTROL Collection]** 지정합니다 (이 예에서는 2). 이 화면에서 컬렉션의 **[!UICONTROL Alias]** AND를 **[!UICONTROL Label]** 사용자 지정할 수 있습니다. 이러한 값은 이 컬렉션을 참조할 때 워크플로우의 다음 활동에 표시됩니다.

      ![](assets/enrichment_example_workflow4.png)

      컬렉션에 **[!UICONTROL Data]** 대해 유지하려면 최종 게시에 사용할 열을 선택합니다.

      ![](assets/enrichment_example_workflow6.png)

      거래 날짜에 내림차순 정렬을 적용하여 최신 거래를 검색합니다.

      ![](assets/enrichment_example_workflow7.png)

   * 각 프로필에 대한 총 트랜잭션 수를 계산하는 합계입니다. 이 집계에서는 나중에 두 개 이상의 트랜잭션이 기록된 프로필을 필터링하는 데 사용됩니다. To create the aggregate, from the **[!UICONTROL Additional data]** tab:

      활동 **[!UICONTROL Advanced relations]** 탭에서 이전에 정의한 링크를 선택합니다.

      ![](assets/enrichment_example_workflow3.png)

      **[!UICONTROL Aggregate]** Select.

      ![](assets/enrichment_example_workflow8.png)

      유지하려면 **[!UICONTROL Data]****모든** 집계 카운트를 정의합니다. 필요한 경우 다음 활동에서 사용자 정의 별칭을 지정하여 더 빠르게 찾을 수 있습니다.

      ![](assets/enrichment_example_workflow9.png)

* 최소 두 개의 트랜잭션이 기록된 초기 타겟의 프로필을 가져오는 한 개의 세그먼트만 있는 **[!UICONTROL Segmentation]** 활동입니다. 트랜잭션이 하나만 있는 프로필은 제외됩니다. 이렇게 하려면 이전에 정의된 세그먼트에서 세그멘테이션의 쿼리가 만들어집니다.

   ![](assets/enrichment_example_workflow5.png)

* 에 **[!UICONTROL Email delivery]** 정의된 추가 데이터를 사용하여 프로필에서 **[!UICONTROL Enrichment]** 마지막으로 수행된 두 개의 구매를 동적으로 검색하는 활동입니다. 개인화 필드를 추가할 때 **추가 데이터 (Targetdata)** 노드에서 추가 데이터를 찾을 수 있습니다.

   ![](assets/enrichment_example_workflow10.png)

**관련 항목:**

* [외부 데이터로 고객 프로파일 강화](https://helpx.adobe.com/campaign/kb/simplify-campaign-management.html#Managedatatofuelengagingexperiences)

