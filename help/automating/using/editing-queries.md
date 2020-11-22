---
solution: Campaign Standard
product: campaign
title: 쿼리 편집
description: 사전 정의된 필터 및 규칙으로 모집단 만들기
audience: automating
content-type: reference
topic-tags: filtering-data
context-tags: queryFilter,overview;audience,main
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '782'
ht-degree: 100%

---


# 쿼리 편집{#editing-queries}

## 쿼리 편집기 기본 정보 {#about-query-editor}

쿼리 편집기는 Adobe Campaign 데이터베이스에 포함된 데이터를 필터링할 수 있는 마법사입니다.

이 기능을 사용하면 사전 정의된 필터 및 규칙을 사용하여 수신자를 더 잘 타겟팅하기 위한 모집단을 만들 수 있습니다.

몇 가지 애플리케이션 기능에서는 다음을 위해 쿼리 편집기를 사용합니다.

* **쿼리** 유형 **대상자** 만들기
* **이메일** 타겟 정의
* **워크플로우** 활동에서 모집단 정의

## 쿼리 편집기 인터페이스 {#query-editor-interface}

쿼리 편집기는 **팔레트** 및 **작업 영역**&#x200B;으로 구성됩니다.

![](assets/query_editor_overview.png)

### 팔레트 {#palette}

편집기 왼쪽에 있는 팔레트는 두 개의 탭으로 나뉘며, 여기에는 주제별 블록으로 구분된 요소를 포함합니다. 이 탭은 다음과 같습니다.

* **바로 가기**&#x200B;는 기본적으로 사용되거나 인스턴스 관리자가 만들 수 있습니다. 여기에는 필드, 노드, 그룹화, 1-1 링크, 1-N 링크 및 기타 사전 정의된 필터가 있습니다.
* **탐색기**&#x200B;를 통해 노드, 그룹화 요소, 링크(1-1 및 1-N) 등 대상 리소스의 사용 가능한 모든 필드에 액세스할 수 있습니다.

탭 안에 있는 요소를 구성하여 쿼리에 사용하려면 작업 영역으로 옮겨야 합니다. 선택한 타겟팅 차원([타겟팅 차원 및 리소스](../../automating/using/query.md#targeting-dimensions-and-resources) 참조)에 따라 다음을 수행할 수 있습니다.

* 대상자 또는 프로필을 하나씩 선택
* 사전 정의된 필터 사용
* 선택한 필드에 대해 간단한 규칙 정의
* 특정 필드에 함수를 적용할 수 있는 고급 규칙 정의

### 작업 영역 {#workspace}

작업 영역은 팔레트에서 추가한 규칙, 대상자 및 사전 정의된 필터를 구성하고 결합할 수 있는 중앙 영역입니다.

팔레트에서 작업 영역으로 요소를 옮기면 새 창이 열리고 [쿼리 만들기](#creating-queries)를 시작할 수 있습니다.

## 쿼리 만들기 {#creating-queries}

쿼리 편집기를 사용하여 메시지의 대상자나 테스트 프로필, 워크플로우의 모집단을 정의하고 쿼리 유형 대상자를 만들 수 있습니다.

쿼리는 게재를 만드는 동안 **[!UICONTROL Audience]** 창에서 정의하거나 워크플로우를 만드는 동안 **쿼리** 활동에서 정의할 수 있습니다.

1. 팔레트에서 작업 영역으로 요소를 옮깁니다. 규칙 편집 창이 열립니다.

   * 문자열 또는 숫자 **필드**&#x200B;의 경우 비교 연산자와 값을 지정합니다.

      ![](assets/query_editor_audience_definition2.png)

   * 날짜 또는 날짜 및 시간 **필드**&#x200B;의 경우 특정 날짜, 두 날짜 사이의 범위 또는 쿼리의 실행 날짜를 기준으로 했을 때의 기간을 정의하도록 선택할 수 있습니다.

      ![](assets/query_editor_date_field.png)

   * 부울 **필드**&#x200B;의 경우 필드에 입력할 수 있는 값에 연결된 상자를 선택합니다.
   * 그룹화 **필드**&#x200B;의 경우 규칙을 만들 그룹화 필드를 선택한 다음 다른 필드와 같은 방식으로 조건을 정의합니다.

      ![](assets/query_editor_audience_definition4.png)

   * 다른 데이터베이스 리소스와 연결된 **1-1** 링크의 경우 타겟팅된 테이블에서 직접 값을 선택합니다.

      ![](assets/query_editor_audience_definition5.png)

   * 다른 데이터베이스 리소스와 연결된 **1-N** 링크의 경우 이 두 번째 리소스의 필드에 하위 쿼리를 정의할 수 있습니다.

      꼭 하위 조건을 지정할 필요는 없습니다.

      예를 들어 프로필 추적 로그에 대해 **[!UICONTROL Exists]** 연산자만 선택하고 규칙을 승인할 수 있습니다. 이 규칙은 추적 로그가 있는 모든 프로필을 반환합니다.

      ![](assets/query_editor_audience_definition6.png)

   * **사전 정의된 필터**&#x200B;의 경우 제공된 기준에 따라 원하는 요소를 입력하거나 선택합니다.

      관리자는 필터를 만들어 복잡하고 반복적인 쿼리 작업을 용이하게 할 수 있습니다. 이는 사전 구성된 규칙 형태로 쿼리 편집기에 표시되며 사용자의 작업 수행에 필요한 단계 수를 제한합니다.

      ![](assets/query-editor_filter_email-audience_filter.png)

1. 규칙의 이름을 지정할 수 있습니다. 그러면 작업 영역에 규칙 이름으로 표시됩니다. 규칙에 이름이 지정되어 있지 않으면 조건에 대한 자동 설명이 표시됩니다.
1. 작업 영역 요소를 결합하려면 서로 인터로크하여 다른 그룹 및/또는 그룹 수준을 만듭니다. 그런 다음 논리 연산자를 선택하여 동일한 수준에서 요소를 결합할 수 있습니다.

   * **[!UICONTROL AND]**: 두 가지 기준의 교집합. 각 기준에 일치하는 요소만 고려합니다.
   * **[!UICONTROL OR]**: 두 가지 기준의 결합. 두 기준 중 하나 이상에 일치하는 요소를 고려합니다.
   * **[!UICONTROL EXCEPT]**: 제외 기준. 첫 번째 기준과 일치하면서 두 번째 기준에는 일치하지 않는 요소를 고려합니다.

1. 이제 작업 표시줄의 ![](assets/count.png) 및 ![](assets/preview.png) 버튼을 사용하여 쿼리가 타겟팅한 요소의 수를 계산하고 미리 볼 수 있습니다.

   ![](assets/query_editor_combining_rules.png)

쿼리의 요소를 수정하려면 편집 아이콘을 클릭합니다. 규칙이 이전에 구성한 대로 열리고 필요한 조정을 수행할 수 있습니다.

이제 쿼리를 만들고 정의하여 게재를 보다 잘 개인화하기 위한 모집단을 만들 수 있습니다.

**관련 항목:**

* [고급 함수](../../automating/using/advanced-expression-editing.md)
* [필터 정의](../../developing/using/configuring-filter-definition.md)
* [사용 사례: 일주일에 한 번 보내는 이메일 게재 만들기](../../automating/using/workflow-weekly-offer.md)
* [사용 사례: 위치별로 분류된 게재 만들기](../../automating/using/workflow-segmentation-location.md)
* [사용 사례: 보충 자료로 게재 만들기](../../automating/using/workflow-created-query-with-complement.md)
* [사용 사례: 열지 않은 사용자에게 새 게재를 보내는 워크플로우 재타겟팅](../../automating/using/workflow-cross-channel-retargeting.md)
