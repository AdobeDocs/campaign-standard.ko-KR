---
title: 쿼리 편집
seo-title: 쿼리 편집
description: 쿼리 편집
seo-description: 사전 정의된 필터 및 규칙 덕분에 모집단을 구축할 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: A 49 C 7739-A 96 C -45 CB -9 AC 5-1 CE 299161 A 97
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 필터링 데이터
discoiquuid: 84306 A 1 E -0 D 9 F -44 CC -88 A 7-36 D 7 E 5 B 4 DA 1 F
context-tags: Queryfilter, overview; 대상, 기본
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 0454dac1a7976c1be2838c2a846d33e77e60c3b3

---


# Editing queries{#editing-queries}

## About query editor {#about-query-editor}

쿼리 편집기는 Adobe Campaign 데이터베이스에 들어 있는 데이터를 필터링할 수 있는 마법사입니다.

이 기능을 사용하면 사전 정의된 필터 및 규칙 덕분에 받는 사람을 더 잘 타게팅할 수 있는 모집단을 만들 수 있습니다.

다음과 같은 목적으로 몇 가지 응용 프로그램 기능이 사용됩니다.

* **쿼리** 유형 **대상 만들기**
* **이메일** 대상 정의
* **워크플로우** 활동의 모집단에서 정의

## Query editor interface {#query-editor-interface}

The query editor is made up of a **Palette** and a **Workspace**.

![](assets/query_editor_overview.png)

### Palette {#palette}

편집기의 왼쪽에 있는 팔레트는 테마 블록으로 나뉘어진 요소를 포함하는 두 개의 탭으로 나뉩니다. 이러한 탭은 다음과 같습니다.

* **기본적으로**&#x200B;사용할 수 있거나 인스턴스 관리자가 만든 단축키입니다. 여기에서 필드, 노드, 그룹, 1-1 링크, 1-n 링크 및 기타 사전 정의된 필터를 찾을 수 있습니다.
* The **Explorer** which allows you to access all available fields in the target resource: nodes, grouping elements, links (1-1 and 1-N).

쿼리에 포함된 요소는 쿼리를 구성하고 고려하기 위해 작업 영역으로 이동해야 합니다. Depending on the targeting dimension selected (see [Targeting dimensions and resources](../../automating/using/query.md#targeting-dimensions-and-resources)), you can:

* 대상 또는 프로필을 하나씩 선택
* 사전 정의된 필터 사용
* 원하는 필드에 대한 간단한 규칙 정의
* 특정 필드에 기능을 적용할 수 있는 고급 규칙 정의

### Workspace {#workspace}

작업 영역은 규칙, 대상 및 팔레트에서 추가된 사전 정의된 필터를 구성하고 결합할 수 있는 중앙 영역입니다.

When you move an element from the palette into the workspace, a new window opens and you can start [Creating queries](../../automating/using/editing-queries.md#creating-queries).

## Creating queries {#creating-queries}

쿼리 편집기를 사용하여 메시지에서 대상 또는 테스트 프로필을 정의하고, 워크플로우의 모집단에서 쿼리 유형 대상을 만들 수 있습니다.

Queries can be defined in the **[!UICONTROL Audience]** window while creating a delivery or in a **Query** activity while creating a workflow.

1. 팔레트에서 작업 공간으로 요소를 이동합니다. 규칙을 편집할 창이 열립니다.

   * For a string or numerical **field**, specify the comparison operator and the value.

      ![](assets/query_editor_audience_definition2.png)

   * For a date or date and time **field**, you can choose to define a specific date, a range between two dates, or a period relative to the query's execution date.

      ![](assets/query_editor_date_field.png)

   * For a Boolean **field**, check the boxes linked to the possible values for the field.
   * **그룹** 필드에서 규칙을 만들 그룹화 필드를 선택한 다음 다른 필드에 대해 동일한 방법으로 조건을 정의합니다.

      ![](assets/query_editor_audience_definition4.png)

   * For a **1-1** link with another database resource, select a value directly from the table targeted.

      ![](assets/query_editor_audience_definition5.png)

   * For a **1-N** link with another database resource, you can define a sub-query on the fields of this second resource.

      하위 조건을 지정할 필요는 없습니다.

      For example, you can only select the **[!UICONTROL Exists]** operator on the profile tracking logs and approve the rule. 규칙은 추적 로그가 존재하는 모든 프로필을 반환합니다.

      ![](assets/query_editor_audience_definition6.png)

   * **사전 정의된 필터의**&#x200B;경우 제공된 기준에 따라 원하는 요소를 입력하거나 선택합니다.

      관리자는 필터를 만들어 복잡하고 반복적인 쿼리를 만들 수 있습니다. 이것은 사전 구성된 규칙 형태의 쿼리 편집기에 나타나며 사용자가 수행해야 하는 단계를 제한합니다.

      ![](assets/query-editor_filter_email-audience_filter.png)

1. 규칙 이름을 지정할 수 있습니다. 그런 다음 작업 공간에서 규칙 이름으로 표시됩니다. 규칙에 이름이 지정되어 있지 않으면 조건에 대한 자동 설명이 표시됩니다.
1. 작업 영역 요소를 결합하려면 서로 결합하여 서로 다른 그룹 및/또는 그룹 수준을 만듭니다. 그런 다음 논리 연산자를 선택하여 동일한 수준의 요소를 결합할 수 있습니다.

   * **[!UICONTROL AND]**: 두 가지 기준의 교차점. 각 기준과 일치하는 요소만 고려됩니다.
   * **[!UICONTROL OR]**: 두 가지 기준의 조합입니다. 두 조건 중 적어도 하나와 일치하는 요소가 고려됩니다.
   * **[!UICONTROL EXCEPT]**: 제외 기준. 첫 번째 기준과 일치하는 요소는 두 번째 기준과 일치하지 않는 한 고려됩니다.

1. You can now calculate and preview the number of elements targeted by your query using the ![](assets/count.png) and ![](assets/preview.png) buttons from the action bar.

   ![](assets/query_editor_combining_rules.png)

쿼리의 요소를 수정하려면 편집 아이콘을 클릭합니다. 규칙이 이전에 구성된 대로 열리고 필요한 조정을 수행할 수 있습니다.

이제 쿼리가 만들어지고 정의되므로 모집단을 만들어 전달을 보다 효과적으로 개인화할 수 있습니다.

**관련 항목:**

* [고급 함수](../../automating/using/advanced-expression-editing.md)
* [필터 정의](../../developing/using/configuring-filter-definition.md)

