---
title: 조정
seo-title: 조정
description: 조정
seo-description: 조정 활동을 사용하면 식별할 수 없는 데이터를 기존 리소스에 연결할 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 7884 DB 8 C -1717-4724-BE 15-3 B 0 B 32 CCC 071
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 데이터 관리 활동
discoiquuid: CB 8 C 43 F 4-9 CDD -4 E 85-99 A 4-004 B 36 B 336 AA
context-tags: 조정, 기본
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 0454dac1a7976c1be2838c2a846d33e77e60c3b3

---


# Reconciliation{#reconciliation}

## Description {#description}

![](assets/reconciliation.png)

**[!UICONTROL Reconciliation]** 활동을 통해 식별할 수 없는 데이터를 기존 리소스에 연결할 수 있습니다.

## Context of use {#context-of-use}

**[!UICONTROL Reconciliation]** 활동은 본질적으로 데이터 관리 목적으로 사용되며 두 가지 다른 사용 사례를 암시합니다.

* Adding relations: a **[!UICONTROL Links]** tab allows you to add links between the inbound data and several other Adobe Campaign database dimensions.

   예를 들어 구매 데이터가 들어 있는 파일에는 구매자와 구매한 제품을 식별하기 위한 정보도 들어 있을 수 있습니다. Two additional dimensions (besides that of **Purchases**) are therefore concerned by the file data: the **Products** and **Profiles** dimensions. Relations then need to be created between these and the **Purchases** dimension (refer to the following example).

   관계를 정의할 때 연결된 차원의 외래 키를 참조하기 위해 인바운드 데이터에 열이 추가됩니다.

   >[!NOTE]
   >
   >이 작업은 연결된 차원의 데이터가 데이터베이스에 이미 있음을 의미합니다. 예를 들어 구매한 제품을 보여주는 구매 파일, 어떤 시기에 어떤 클라이언트 등에 의해 구매되었는지에 관계없이 해당 제품은 데이터베이스에 이미 존재해야 합니다.

* Data identification: an **[!UICONTROL Identification]** tab allows you to simply link inbound data to columns of an existing dimension in the Adobe Campaign database. 활동 후에는 데이터가 정의된 차원에 속하는 것으로 식별됩니다.

   예를 들어, 대상자 저장, 데이터베이스 업데이트 등을 수행할 수 있습니다.

For example, the **[!UICONTROL Reconciliation]** activity can be placed after a load data activity with the aim of importing non-standard data into the database.

## Configuration {#configuration}

1. Drag and drop a **[!UICONTROL Reconciliation]** activity into your workflow, following a transition containing a population whose targeting dimension does not directly come from Adobe Campaign. For more on this, referr to [Targeting dimensions and resources](../../automating/using/query.md#targeting-dimensions-and-resources).
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. If you would like to define links between the inbound data and other database dimensions, go to the **[!UICONTROL Links]** tab.

   필요한 만큼 관계를 추가합니다. 각 관계에 대해 먼저 연결된 차원을 선택한 다음 링크 세부 정보에서 해당 필드를 지정합니다.

1. If you would like to simply identify the inbound data, go to the **[!UICONTROL Identification]** tab and check the **[!UICONTROL Identify the document from the working data]** box.

   인바운드 데이터를 조정할 타깃팅 차원을 선택합니다.

   인바운드 전환 레코드를 선택된 타깃팅 차원 레코드에 연결하는 조정 기준을 추가합니다. 여러 기준을 지정하는 경우 모든 데이터 간의 링크가 작동하도록 모든 기준을 확인해야 합니다.

   **[!UICONTROL Processing unidentified source lines]** 모드를 선택합니다.

   * **[!UICONTROL Ignore them]**: 식별 가능한 데이터만 활동의 아웃바운드 전환에서 유지됩니다.
   * **[!UICONTROL Keep in the outbound population]**: 인바운드 전환의 모든 데이터는 활동의 아웃바운드 전환에서 유지됩니다.

1. 활동의 구성을 확인하고 워크플로우를 저장합니다.

## Example 1: Relation definition {#example-1--relation-definition}

다음 예제에서는 파일의 구매 데이터를 사용하여 데이터베이스를 업데이트하는 워크플로우를 보여 줍니다. 구매 데이터에는 클라이언트 이메일과 제품 코드와 같은 다른 차원의 요소를 참조하는 데이터가 포함됩니다.

>[!NOTE]
>
>The **Transactions** and **Products** resources used in this example do not exist in the Adobe Campaign database by default. They were therefore created beforehand using the [Custom resources](../../developing/using/data-model-concepts.md) function. 가져온 파일과 제품 내의 이메일 주소에 해당하는 프로필은 데이터베이스에 미리 로드되었습니다.

워크플로우는 다음 활동으로 구성됩니다.

![](assets/reconciliation_example1.png)

* **[!UICONTROL Load file]** 가져올 파일의 데이터를 로드하고 감지하는 활동. 가져온 파일에는 다음 데이터가 포함됩니다.

   * 거래 날짜
   * 클라이언트 이메일 주소
   * 구입한 제품 코드
   ```
   date;client;product
   2015-05-19 09:00:00;mail1@email.com;ZZ1
   2015-05-19 09:01:00;mail2@email.com;ZZ2
   2015-05-19 09:01:01;mail3@email.com;ZZ2
   2015-05-19 09:01:02;mail4@email.com;ZZ2
   2015-05-19 09:02:00;mail5@email.com;ZZ3
   2015-05-19 09:03:00;mail6@email.com;ZZ4
   2015-05-19 09:04:00;mail7@email.com;ZZ5
   2015-05-19 09:05:00;mail8@email.com;ZZ7
   2015-05-19 09:06:00;mail9@email.com;ZZ6
   ```

* A **[!UICONTROL Reconciliation]** activity to bind purchasing data to database profiles as well as products. 따라서 제품 표는 물론 파일 데이터와 프로필 테이블 사이의 관계를 정의해야 합니다. This configuration is carried out in the activity's **[!UICONTROL Relations]** tab:

   * **프로필과의 관계**: 파일의 **클라이언트** 열은 프로필 차원의 **이메일** 필드에 **연결되어** 있습니다.
   * **제품과**&#x200B;관련성: 파일의 **제품** 열이 프로필 차원의 **Productcode** 필드에 **연결되어** 있습니다.
   연결된 차원의 외래 키를 참조하기 위해 열이 인바운드 데이터에 추가됩니다.

   ![](assets/reconciliation_example3.png)

* **[!UICONTROL Update data]** 활동에서는 가져온 데이터를 사용하여 업데이트할 데이터베이스 필드를 정의할 수 있습니다. As the data was already identified as belonging to the **Transactions** dimension in the previous activity, here you can use the **[!UICONTROL Directly using the targeting dimension]** identification option.

   By using the option that automatically detects fields to update, the links configured in the previous activity (to profiles and products) are added to the list of **[!UICONTROL Fields to update]**. 거래 날짜에 해당하는 필드가 이 목록에 올바르게 추가되었는지 확인해야 합니다.

   ![](assets/reconciliation_example5.png)

   ![](assets/reconciliation_example4.png)

## Example 2: Identification {#example-2--identification}

다음 예제에서는 새 클라이언트를 포함하는 가져온 파일에서 직접 프로필 대상을 만드는 워크플로우를 보여 줍니다. 다음 활동으로 구성됩니다.

![](assets/identification_example2.png)

* **[!UICONTROL Load file]** 가져올 파일의 데이터를 로드하고 감지하는 활동. 가져온 파일에는 다음 데이터가 포함됩니다.

   ```
   lastname;firstname;email;dateofbirth
   jackman;megan;megan.jackman@testmail.com;07/08/1975
   phillips;edward;phillips@testmail.com;09/03/1986
   weaver;justin;justin_w@testmail.com;11/15/1990
   martin;babeth;babeth_martin@testmail.net;11/25/1964
   reese;richard;rreese@testmail.com;02/08/1987
   cage;nathalie;cage.nathalie227@testmail.com;07/03/1989
   xiuxiu;andrea;andrea.xiuxiu@testmail.com;09/12/1992
   grimes;daryl;daryl_890@testmail.com;12/06/1979
   tycoon;tyreese;tyreese_t@testmail.net;10/08/1971
   ```

* **[!UICONTROL Reconciliation]** 불러온 파일의 각 열을 프로필 차원 열에 연결하는 활동. 식별할 수 없는 파일 레코드 (데이터 누락, 호환되지 않는 데이터 유형 등) final 대상 데이터의 무결성을 유지하기 위해 무시됩니다.

   ![](assets/identification_example1.png)

* **[!UICONTROL Save audience]** 활동 - 프로필 대상자를 저장합니다.

   ![](assets/identification_example3.png)

