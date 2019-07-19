---
title: 증분 쿼리
seo-title: 증분 쿼리
description: 증분 쿼리
seo-description: 증분 쿼리 활동을 사용하면 Adobe Campaign 데이터베이스에서 요소 모집단을 필터링하고 추출할 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 73 b 42422-e 815-43 ef -84 c 0-97 c 4433 ccc 98
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 타깃팅 활동
discoiquuid: 80961 e 73-42 ec -463 a -8496-cff 69 fab 0475
context-tags: 증분, 기본
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 3e2081fc3377fe4edbdf3fb8c4765a9acda6d79e

---


# Incremental query{#incremental-query}

## Description {#description}

![](assets/incremental.png)

**[!UICONTROL Incremental query]** 활동을 통해 Adobe Campaign 데이터베이스에서 요소 모집단을 필터링하고 추출할 수 있습니다. 이 활동이 실행될 때마다 이전 실행의 결과가 제외됩니다. 이렇게 하면 새 요소만 타깃팅할 수 있습니다.

You can define **[!UICONTROL Additional data]** for the targeted population via a dedicated tab. 이 데이터는 추가 열에 저장되며 진행 중인 워크플로우에만 사용할 수 있습니다.

활동은 쿼리 편집기 도구를 사용합니다. This tool is detailed in a [dedicated section](../../automating/using/editing-queries.md#about-query-editor).

## Context of use {#context-of-use}

An **[!UICONTROL Incremental query]** has to be linked to a **[!UICONTROL Scheduler]** in order to define the execution frequency of the workflow, and therefore the query.

The **[!UICONTROL Processed data]** tab, which is specific to this activity, allows you to view any results of the activity's previous executions, if required.

**[!UICONTROL Incremental query]** 활동은 다양한 유형의 사용에 사용할 수 있습니다.

* 개인을 세그먼트화하여 메시지 대상, 대상자 등을 정의합니다.
* 데이터 내보내기를 참조하십시오.

## Configuration {#configuration}

1. **[!UICONTROL Incremental query]** 워크플로우를 워크플로우로 드래그하여 놓습니다.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. If you would like to run a query on a resource other than the profile resource, go to the activity's **[!UICONTROL Properties]** tab and select a **[!UICONTROL Resource]** and a **[!UICONTROL Targeting dimension]**.

   The **[!UICONTROL Resource]** allows you to refine the filters displayed in the palette whereas the **[!UICONTROL Targeting dimension]**, contextual with regard to the resource selected, corresponds to the type of population that you would like to obtain (identified profiles, deliveries, data linked to the selected resource, etc.).

1. **[!UICONTROL Target]** 탭에서 규칙을 정의하고 결합하여 쿼리를 실행합니다.
1. **[!UICONTROL Processed data]** 탭에서 다음 워크플로우의 실행에 사용할 증분 모드를 선택합니다.

   * **[!UICONTROL Use the exclusion of the results of previous executions]**: 각 새 실행에 대한 이전 실행의 결과는 제외됩니다.
   * **[!UICONTROL Use a date field]**: 다음 실행은 선택한 날짜 필드가 **[!UICONTROL Incremental query]** 활동의 마지막 실행 날짜와 더 크거나 같은 결과를 고려합니다. You can select any date field pertaining to the resource selected in the **[!UICONTROL Properties]** tab. 이 모드는 로그 데이터와 같은 큰 리소스를 쿼리할 때 성능이 더 좋습니다.

      워크플로우의 처음 실행 후 다음 실행에 사용할 마지막 실행 날짜를 이 탭에서 확인할 수 있습니다. 워크플로우가 실행될 때마다 자동으로 업데이트됩니다. 필요에 따라 새 값을 수동으로 입력하여 이 값을 무시할 수 있습니다.
   >[!NOTE]
   >
   >**[!UICONTROL Use a date field]** 이 모드에서는 선택한 날짜 필드에 따라 더 많은 유연성을 사용할 수 있습니다. 예를 들어, 선택된 필드가 수정 날짜에 해당하는 경우, 날짜 필드 모드를 사용하면 최근에 업데이트한 데이터를 검색할 수 있으며, 다른 모드는 워크플로우의 마지막 실행 이후에 수정된 이전 실행에서 이미 타깃팅된 레코딩을 제외시킬 수 있습니다.

   ![](assets/incremental_query_usedatefield.png)

1. You can define **[!UICONTROL Additional data]** for the targeted population via a dedicated tab. 이 데이터는 추가 열에 저장되며 진행 중인 워크플로우에만 사용할 수 있습니다. 특히, 쿼리의 타깃팅 차원에 연결된 Adobe Campaign 데이터베이스 테이블의 데이터를 추가할 수 있습니다. [데이터 강화](../../automating/using/query.md#enriching-data) 섹션을 참조하십시오.
1. 활동의 구성을 확인하고 워크플로우를 저장합니다.

## Enriching data {#enriching-data}

Just as for a query, you can enrich the data from an **[!UICONTROL Incremental query]**. [데이터 강화](../../automating/using/query.md#enriching-data) 섹션을 참조하십시오.

## Example: incremental query on subscribers to a service {#example--incremental-query-on-subscribers-to-a-service}

The following example shows the configuration of an **[!UICONTROL Incremental query]** activity which filters the profiles in the Adobe Campaign database that are subscribed to the **Running Newsletter** service, to send them a welcome email containing a promo code.

워크플로우는 다음과 같은 요소로 구성됩니다.

![](assets/incremental_query_example1.png)

* **[!UICONTROL Scheduler]** A activity, to execute the workflow every monday at 6 am.

   ![](assets/incremental_query_example2.png)

* An **[!UICONTROL Incremental query]** activity, which targets all of the current subscribers during the first execution, then only the new subscribers of that week during the following executions.

   ![](assets/incremental_query_example3.png)

* **[!UICONTROL Email delivery]** 활동. 워크플로우는 일주일에 한 번 실행되지만, 보낸 이메일과 월간 결과를 집계하여 단 한 주 동안 전체 달의 시간에 대한 보고서를 생성할 수 있습니다.

   To do this, choose to create a **[!UICONTROL Recurring email]** here regrouping the emails and the results **[!UICONTROL By month]**.

   이메일의 내용을 정의하고 환영 프로모션 코드를 삽입합니다.

   For more on this, refer to the [Email delivery](../../automating/using/email-delivery.md) and [Defining email content](../../designing/using/about-personalization.md) sections.

그런 다음 워크플로우 실행을 시작합니다. 매주 새 구독자는 프로모션 코드가 포함된 환영 이메일을 받게 됩니다.

## Example: incremental query on delivery logs {#example--incremental-query-on-delivery-logs}

**[!UICONTROL Incremental query]** 활동을 사용하여 파일에서 새 로그를 정기적으로 내보낼 수 있습니다. 이 기능은 외부 보고 또는 BI 도구에서 로그 데이터를 사용하려는 경우 유용합니다.

A complete example is available in the [Exporting logs](../../automating/using/exporting-logs.md) section.
