---
title: 강화
description: Enrichment 활동은 워크플로우에서 처리할 추가 데이터를 정의할 수 있는 고급 활동입니다.
page-status-flag: 활성화 안 함
uuid: 8c1693ef-1312-422c-b05d-26353113f8f
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 자동화
content-type: reference
topic-tags: 타깃팅 활동
discoiquuid: f67c1caf-3284-4c34-a5b0-8654a95640ae
context-tags: increation,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 강화{#enrichment}

## 설명 {#description}

![](assets/enrichment.png)

활동은 **[!UICONTROL Enrichment]** 워크플로우에서 처리할 추가 데이터를 정의할 수 있는 고급 활동입니다.

## 사용 상황 {#context-of-use}

이 **[!UICONTROL Enrichment]** 활동은 일반적으로 타깃팅 활동 다음에 또는 파일을 가져온 후 타깃팅된 데이터를 사용할 수 있는 활동 전에 사용됩니다.

이 활동은 **[!UICONTROL Query]** 활동보다 더 많은 고급 농축 기능을 포함합니다. 일부 간단한 데이터 중복 사례는 쿼리 활동에서 직접 수행할 수 [있습니다](../../automating/using/query.md#enriching-data).

활동을 **[!UICONTROL Enrichment]** 사용하면 인바운드 전환을 활용하고 추가 데이터로 출력 전환을 완료하도록 활동을 구성할 수 있습니다. 여러 세트에서 가져온 데이터를 결합하거나 임시 리소스에 대한 링크를 만들 수 있습니다.

## 구성 {#configuration}

활동을 구성하려면 **[!UICONTROL Enrichment]** 다음을 수행하십시오.

1. 워크플로우를 워크플로우로 드래그하여 **[!UICONTROL Enrichment]** 놓을 수 있습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 엽니다.
1. 활동에 여러 인바운드 전환이 있는 경우 을 **[!UICONTROL Primary set]**&#x200B;선택합니다. 이 활동에 구성된 추가 데이터는 아웃바운드 전환의 이 기본 세트에 추가됩니다.

   기본 세트에 이미 추가 데이터가 포함되어 있는 경우 이를 유지하거나 제거할 수 있습니다. 이 **[!UICONTROL Keep all additional data from the main set]** 옵션을 선택 해제하면 아웃바운드 전환에는 에 구성된 추가 데이터만 **[!UICONTROL Enrichment]** 유지됩니다.

1. 여러 인바운드 전환이 있을 경우 활동의 **[!UICONTROL Advanced Relations]** 탭에서 기본 세트와 다른 인바운드 데이터 간의 관계를 정의합니다. 이 **[!UICONTROL Add element]** 단추를 사용하여 여러 관계를 추가할 수 있습니다.

   새 관계를 정의할 때 기본 세트에 연결할 인바운드 데이터 세트를 선택합니다. 그런 다음 관계식의 유형을 정의합니다. 인바운드 데이터와 데이터 모델에 따라 몇 가지 유형의 관계를 사용할 수 있습니다.

   * **[!UICONTROL 1 cardinality simple link]**:들어오는 데이터의 각 레코드는 기본 집합에서 한 개의 레코드에만 연결됩니다. 기본 세트의 각 레코드에는 연결된 데이터에 연결된 레코드가 하나씩 있습니다.
   * **[!UICONTROL N cardinality collection link]**:연결된 데이터의 0, 1 이상(N) 레코드는 기본 세트의 1개 레코드에 연결할 수 있습니다.
   * **[!UICONTROL 0 or 1 cardinality simple link]**:기본 세트의 레코드는 연결된 데이터의 0 또는 1 레코드와 연결할 수 있지만 하나 이하여야 합니다.
   가 **[!UICONTROL Cardinality]** 정의되면 을 정의합니다 **[!UICONTROL Reconciliation criteria]**. 조정 **[!UICONTROL Source expression]** 기준의 필드는 대상 리소스의 필드, [표현식](../../automating/using/advanced-expression-editing.md) 또는 따옴표 사이에 직접 지정된 값일 수 있습니다.

   워크플로우에서 나중에 쉽게 식별할 수 있는 **[!UICONTROL Label]** 및 **[!UICONTROL ID]** 를 정의합니다.

   >[!NOTE]
   >
   >기본 세트와 **[!UICONTROL Enrichment]** 활동에 연결된 다른 인바운드 전환 사이의 관계만 정의할 수 있습니다. 데이터베이스 리소스와의 관계를 정의하는 것이 더 간단한 경우를 위해 조정 [활동을](../../automating/using/reconciliation.md) 사용합니다.

1. 활동의 **[!UICONTROL Additional data]** 탭에서 추가 데이터를 정의합니다. 기본 세트의 타깃팅 차원과 관련된 추가 데이터(단순 필드, 합계 및 컬렉션)를 정의하거나 활동의 **[!UICONTROL Advanced relations]** 탭에서 만든 링크를 기반으로 할 수 **[!UICONTROL Enrichment]** 있습니다.

   데이터 [수집](../../automating/using/query.md#enriching-data) 섹션을 참조하십시오.

1. 활동 구성을 확인하고 워크플로우를 저장합니다.

이제 데이터 이후에 연결된 활동에 데이터를 사용할 수 **[!UICONTROL Enrichment]**&#x200B;있습니다. 예를 들어, 이메일 컨텐츠의 개인화 필드 탐색기 **[!UICONTROL Additional data (targetData)]** 링크 아래에서 찾을 수 있습니다.

## 예:파일에 포함된 데이터로 프로필 데이터 강화 {#example--enriching-profile-data-with-data-contained-in-a-file}

이 예에서는 파일에 포함된 구매 데이터를 사용하여 프로필 데이터를 향상시키는 방법을 보여줍니다. 구매 데이터는 서드 파티 시스템에 저장되어 있습니다. 각 프로필에는 여러 개의 구매가 파일에 저장되어 있을 수 있습니다. 워크플로우의 최종 목표는 두 개 이상의 항목을 구매한 대상 프로필에 이메일을 보내 충성도에 대한 감사를 표시하는 것입니다.

워크플로우는 다음과 같이 구성됩니다.

![](assets/enrichment_example_workflow.png)

* 메시지를 받을 프로필을 타깃팅하는 **[!UICONTROL Query]** 활동.
* 구매 데이터를 로드하는 **[!UICONTROL Load file]** 활동. 예:

   ```
   tcode;tdate;customer;product;tamount
   aze123;21/05/2017;dannymars@example.com;TV;799
   aze124;28/05/2017;dannymars@example.com;Headphones;8
   aze125;31/07/2017;john.smith@example.com;Headphones;8
   aze126;14/12/2017;john.smith@example.com;Plastic Cover;4
   aze127;02/01/2018;dannymars@example.com;Case Cover;79
   aze128;04/03/2017;clara.smith@example.com;Phone;149
   ```

   이 예제 파일을 사용하면 이메일 주소를 사용하여 데이터를 데이터베이스 프로파일과 조정합니다. 또한 [이 문서에](../../developing/using/configuring-the-resource-s-data-structure.md#generating-a-unique-id-for-profiles-and-custom-resources)설명된 대로 고유 ID를 활성화할 수도 있습니다.

* 파일에서 로드된 거래 데이터와 에서 선택한 프로필 간의 링크를 만드는 **[!UICONTROL Enrichment]** 활동 **[!UICONTROL Query]**. 링크는 활동의 **[!UICONTROL Advanced relations]** 탭에 정의됩니다. 링크는 **[!UICONTROL Load file]** 활동에서 들어오는 전환을 기반으로 합니다. 프로필 리소스의 "이메일" 필드와 가져온 파일의 "고객" 열을 조정 기준으로 사용합니다.

   ![](assets/enrichment_example_workflow2.png)

   링크가 만들어지면 두 가지 세트가 **[!UICONTROL Additional data]** 추가됩니다.

   * 각 프로파일의 마지막 두 트랜잭션에 해당하는 두 라인의 모음. 이 수집의 경우 제품 이름, 거래 날짜 및 제품 가격이 추가 데이터로 추가됩니다. 데이터에 내림차순 정렬이 적용됩니다. 컬렉션을 만들려면 **[!UICONTROL Additional data]** 탭에서 다음을 수행합니다.

      활동의 **[!UICONTROL Advanced relations]** 탭에서 이전에 정의한 링크를 선택합니다.

      ![](assets/enrichment_example_workflow3.png)

      검색할 줄 수(이 예에서는 2개)를 **[!UICONTROL Collection]** 선택하고 지정합니다. 이 화면에서 컬렉션의 **[!UICONTROL Alias]** 및 컬렉션을 사용자 지정할 **[!UICONTROL Label]** 수 있습니다. 이러한 값은 이 컬렉션을 참조할 때 워크플로우의 다음 활동에서 표시됩니다.

      ![](assets/enrichment_example_workflow4.png)

      컬렉션을 **[!UICONTROL Data]** 유지하려면 최종 전달에 사용할 열을 선택합니다.

      ![](assets/enrichment_example_workflow6.png)

      거래 날짜에 내림차순 정렬을 적용하여 최신 트랜잭션을 검색합니다.

      ![](assets/enrichment_example_workflow7.png)

   * 각 프로필에 대한 총 트랜잭션 수를 카운트합니다. 이 집계는 나중에 두 개 이상의 트랜잭션이 기록된 프로파일을 필터링하는 데 사용됩니다. 합계를 만들려면 **[!UICONTROL Additional data]** 탭에서 다음을 수행합니다.

      활동의 **[!UICONTROL Advanced relations]** 탭에서 이전에 정의한 링크를 선택합니다.

      ![](assets/enrichment_example_workflow3.png)

      을 **[!UICONTROL Aggregate]**&#x200B;선택합니다.

      ![](assets/enrichment_example_workflow8.png)

      보관하려면 모두 계산 **[!UICONTROL Data]** 합계를 **** 정의합니다. 필요한 경우 사용자 지정 별칭을 지정하여 다음 활동에서 더 빨리 찾습니다.

      ![](assets/enrichment_example_workflow9.png)

* 두 개 이상의 트랜잭션을 기록한 초기 대상의 프로파일을 검색하는 단일 세그먼트만 있는 **[!UICONTROL Segmentation]** 활동. 트랜잭션이 하나만 있는 프로필은 제외됩니다. 이를 위해 이전에 정의한 합계에 대해 세그멘테이션의 쿼리가 수행됩니다.

   ![](assets/enrichment_example_workflow5.png)

* 에 정의된 추가 데이터를 사용하여 프로필에서 수행한 두 개의 마지막 구매를 동적으로 **[!UICONTROL Email delivery]** **[!UICONTROL Enrichment]** 검색하는 활동입니다. 추가 데이터는 개인화 필드를 추가할 때 **추가 데이터(TargetData)** 노드에서 찾을 수 있습니다.

   ![](assets/enrichment_example_workflow10.png)

**관련 항목:**

* [외부 데이터로 고객 프로파일 향상](https://helpx.adobe.com/campaign/kb/simplify-campaign-management.html#Managedatatofuelengagingexperiences)

