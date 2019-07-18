---
title: 중복 제거
seo-title: 중복 제거
description: 중복 제거
seo-description: 중복 제거 활동을 사용하면 인바운드 활동의 결과에서 중복을 삭제할 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 11 a 22 a 9 c -3 bfe -4953-8 a 52-2 f 4 e 93 c 128 fb
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 타깃팅 활동
discoiquuid: E 7 A 5 E 1 E 7-4680-46 C 7-98 B 8-0 A 47 BB 7 BE 2 B 8
context-tags: Dedup, main
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 0454dac1a7976c1be2838c2a846d33e77e60c3b3

---


# Deduplication{#deduplication}

## Description {#description}

![](assets/deduplication.png)

**[!UICONTROL Deduplication]** 활동을 사용하면 인바운드 활동의 결과에서 중복을 삭제할 수 있습니다.

## Context of use {#context-of-use}

**[!UICONTROL Deduplication]** 활동은 일반적으로 타깃팅 활동 이후 또는 파일을 가져온 후 타깃팅된 데이터의 사용을 허용하는 활동 전에 사용됩니다.

중복 제거 시 인바운드 전환이 별도로 처리됩니다. 예를 들어 프로필'A'가 쿼리 1의 결과에 있는 경우 쿼리 2의 결과도 중복되지 않습니다.

따라서 중복 제거는 하나의 인바운드 전환만 포함하도록 합니다. 이렇게 하려면, 조합 활동, 교차 활동 등과 같은 타깃팅 요구 사항에 해당하는 활동을 사용하여 다른 쿼리를 결합할 수 있습니다. 예를 들면 다음과 같습니다.

![](assets/dedup_bonnepratique.png)

## Configuration {#configuration}

중복 제거 활동을 구성하려면 레이블, 방법 및 중복 제거 기준을 비롯하여 결과와 관련된 옵션을 입력해야 합니다.

1. **[!UICONTROL Deduplication]** 워크플로우를 워크플로우로 드래그하여 놓습니다.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.

   ![](assets/deduplication_1.png)

1. Select the **[!UICONTROL Resource type]** on which the deduplication has to be carried out:

   * **[!UICONTROL Database resource]** 중복 제거가 데이터베이스에 이미 존재하는 데이터에 대해 수행됩니다. Select the **[!UICONTROL Filtering dimension]** and the **[!UICONTROL Targeting dimension]**, depending on the data that you want to deduplicate. By default, deduplication is carried out on the **profiles**.
   * **[!UICONTROL Temporary resource]** 워크플로우의 임시 데이터에 대해 중복 제거가 수행되는 경우: 중복 해제할 **[!UICONTROL Targeted set]** 데이터 포함을 선택합니다. 이 사용 사례는 파일을 가져온 후 또는 데이터베이스에 있는 데이터가 세그먼트 코드를 사용하여 풍부한 경우 발생할 수 있습니다.

1. **[!UICONTROL Number of unique records to keep]**&#x200B;을 선택합니다. 이 필드의 기본값은 1 입니다. 값 0를 사용하면 모든 중복 항목을 유지할 수 있습니다.

   예를 들어 레코드 A와 B가 레코드 Y의 중복으로 간주되고 C 레코드는 레코드 Z의 중복으로 간주됩니다.

   * 필드의 값이 1 인 경우: Y 및 Z 레코드만 유지됩니다.
   * 필드의 값이 0 인 경우: 모든 레코드가 보관됩니다.
   * 필드의 값이 2 인 경우: 기록 C와 Z는 그대로 유지되고, A, B, Y의 두 레코드는 그 이후에 선택한 중복 제거 방법에 따라 유지됩니다.

1. Define the **[!UICONTROL Duplicate identification]** criteria by adding conditions in the list provided. 동일한 값이 중복될 수 있도록 허용하는 필드 및/또는 표현식을 지정합니다. 이메일 주소, 이름, 성 등 조건 순서를 사용하여 먼저 처리할 조건을 지정할 수 있습니다.
1. In the drop-down list, select the **[!UICONTROL Deduplication method]** to use:

   * **[!UICONTROL Choose for me]**: 레코드가 중복되지 않도록 임의로 선택합니다.
   * **[!UICONTROL Following a list of values]**: 하나 이상의 필드에 대한 값 우선 순위를 정의할 수 있습니다. 값을 정의하려면 필드를 선택하거나 표현식을 만든 다음 해당 테이블에 값을 추가합니다. To define a new field, click the **[!UICONTROL Add]** button located above the list of values.

      ![](assets/deduplication_2.png)

   * **[!UICONTROL Non-empty value]**: 이렇게 하면 선택한 표현식의 값이 비어있지 않은 기록을 유지할 수 있습니다.

      ![](assets/deduplication_3.png)

   * **[!UICONTROL Using an expression]**: 이렇게 하면 입력한 표현식의 값이 가장 작거나 가장 큰 레코드를 유지할 수 있습니다.

      ![](assets/deduplication_4.png)

1. If needed, manage the activity's [Transitions](../../automating/using/executing-a-workflow.md#managing-an-activity-s-outbound-transitions) to access the advanced options for the outbound population.
1. 활동의 구성을 확인하고 워크플로우를 저장합니다.

## Example 1: Identifying duplicates before a delivery {#example-1--identifying-duplicates-before-a-delivery}

다음 예는 이메일을 보내기 전에 Target의 중복을 제외할 수 있는 중복 제거를 보여줍니다. 즉, 동일한 프로필로 여러 번 커뮤니케이션을 보내지 마십시오.

워크플로우는 다음으로 구성됩니다.

![](assets/deduplication_example_workflow.png)

* A **[!UICONTROL Query]** which allows you to define the target of the email. 여기서 워크플로우는 1 년 이상 클라이언트 데이터베이스에 있었던 18 ~ 25 세 사이의 모든 프로필을 타깃팅합니다.

   ![](assets/deduplication_example_query.png)

* **[!UICONTROL Deduplication]** 이전 쿼리에서 오는 중복 항목을 식별할 수 있는 활동. 이 예에서는 각 복제에 대해 하나의 레코드만 저장됩니다. 중복은 이메일 주소를 사용하여 식별됩니다. 즉, 타깃팅에 있는 각 이메일 주소에 대해 이메일 게재를 한 번만 보낼 수 있습니다.

   The deduplication method selected is **[!UICONTROL Non-empty value]**. This allows you to ensure that amongst the records kept in case of duplicates, priority is given to those in which the **First name** has been provided. 이렇게 하면 이메일 컨텐츠의 개인화 필드에서 이름이 사용되는 경우 좀 더 일관성이 있게 됩니다.

   또한 중복을 유지하고 목록을 표시할 수 있는 추가 전환이 추가됩니다.

   ![](assets/deduplication_example_dedup.png)

* An **[!UICONTROL Email delivery]** placed after the main outbound transition of the deduplication. The configuration for email deliveries is detailed in the [Email delivery](../../automating/using/email-delivery.md) section.
* A **[!UICONTROL Save audience]** activity placed after the additional transition of the deduplication to save the duplicates in a **Duplicates** audience. 이 대상은 모든 이메일 배달에서 해당 구성원을 제외하도록 다시 사용할 수 있습니다.

## Example 2: Deduplicating the data from an imported file {#example-2--deduplicating-the-data-from-an-imported-file}

이 예에서는 데이터를 데이터베이스로 로드하기 전에 가져온 파일에서 데이터를 중복 제거하는 방법을 보여줍니다. 이 절차는 데이터베이스에 로드된 데이터의 품질을 향상시킵니다.

워크플로우는 다음으로 구성됩니다.

![](assets/deduplication_example2_workflow.png)

* A file that contains a list of profiles is imported using a **[!UICONTROL Load file]** activity. 이 예에서 가져온 파일은. csv 형식이며 10 개의 프로필을 포함합니다.

   ```
   lastname;firstname;dateofbirth;email
   Smith;Hayden;23/05/1989;hayden.smith@example.com
   Mars;Daniel;17/11/1987;dannymars@example.com
   Smith;Clara;08/02/1989;hayden.smith@example.com
   Durance;Allison;15/12/1978;allison.durance@example.com
   Lucassen;Jody;28/03/1988;jody.lucassen@example.com
   Binder;Tom;19/01/1982;tombinder@example.com
   Binder;Tommy;19/01/1915;tombinder@example.com
   Connor;Jade;10/10/1979;connor.jade@example.com
   Mack;Clarke;02/03/1985;clarke.mack@example.com
   Ross;Timothy;04/07/1986;timross@example.com
   ```

   이 파일을 샘플 파일로 사용하여 열 형식을 감지하고 정의할 수도 있습니다. **[!UICONTROL Column definition]** 탭에서 가져온 파일의 각 열이 올바르게 구성되어 있는지 확인합니다.

   ![](assets/deduplication_example2_fileloading.png)

* **[!UICONTROL Deduplication]** 활동. 중복 제거는 파일을 가져온 후 데이터베이스에 데이터를 삽입하기 전에 바로 수행됩니다. It should therefore be based on the **[!UICONTROL Temporary resource]** from the **[!UICONTROL Load file]** activity.

   이 예에서는 파일에 포함된 고유 이메일 주소당 단일 항목을 보관하려고 합니다. Duplicate identification is therefore carried out on the **email** column of the temporary resource. 그러나 두 개의 이메일 주소가 파일에 두 번 나타납니다. 따라서 두 줄이 중복으로 간주됩니다.

   ![](assets/deduplication_example2_dedup.png)

* **[!UICONTROL Update data]** 활동을 사용하면 중복 제거 프로세스에서 데이터베이스에 저장된 데이터를 삽입할 수 있습니다. 가져온 데이터가 프로필 차원에 속한 것으로 식별된 데이터만 업데이트하면 됩니다.

   Here, we would like to **[!UICONTROL Insert only]** the profiles that do not already exist in the database. We are going to do this by using the file's email column and the email field from the **Profile** dimension as the reconciliation key.

   ![](assets/deduplication_example2_writer1.png)

   Specify the mappings between the file's columns from which you want to insert the data and the database fields from the **[!UICONTROL Fields to update]** tab.

   ![](assets/deduplication_example2_writer2.png)

그런 다음 워크플로우를 시작합니다. 중복 제거 프로세스에서 저장된 레코드는 데이터베이스의 프로필에 추가됩니다.
