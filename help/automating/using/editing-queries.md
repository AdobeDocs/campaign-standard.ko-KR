---
title: 쿼리 편집
description: 미리 정의된 필터 및 규칙 덕분에 모집단 생성
page-status-flag: 활성화 안 함
uuid: a49c7739-a96c-45cb-9ac5-1ce299161a97
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 자동화
content-type: reference
topic-tags: 필터링
discoiquuid: 84306a1e-0d9f-44cc-88a7-36d7e5b4da1f
context-tags: queryFilter,overview;audience,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 쿼리 편집{#editing-queries}

## 쿼리 편집기 정보 {#about-query-editor}

쿼리 편집기는 Adobe Campaign 데이터베이스에 포함된 데이터를 필터링할 수 있는 마법사로,

이 기능을 사용하면 미리 정의된 필터 및 규칙 덕분에 받는 사람을 더 잘 타게팅할 수 있는 모집단을 만들 수 있습니다.

몇 가지 응용 프로그램 기능에서 다음 작업을 위해 사용합니다.

* 쿼리 **유형** **대상자 만들기**
* 이메일 **타겟** 정의
* 워크플로우 **활동에서 모집단** 정의

## 쿼리 편집기 인터페이스 {#query-editor-interface}

쿼리 편집기는 팔레트 및 **작업** 영역으로 **구성됩니다**.

![](assets/query_editor_overview.png)

### Palette {#palette}

편집기의 왼쪽에 있는 팔레트는 두 개의 탭으로 나누어져 있으며, 이 탭에는 요소가 테마 블록으로 구분되어 있습니다. 이러한 탭은 다음과 같습니다.

* 기본적으로 **사용**&#x200B;가능하거나 인스턴스 관리자가 만든 단축키입니다. 필드, 노드, 그룹, 1-1 링크, 1-N 링크 및 기타 사전 정의된 필터를 찾을 수 있습니다.
* 타겟 **리소스의** 사용 가능한 모든 필드에 액세스할 수 있는 탐색기:노드, 요소 그룹화, 링크(1-1 및 1-N)

탭에 포함된 요소를 작업 영역으로 이동하여 쿼리를 구성하고 고려해야 합니다. 선택한 타깃팅 차원에 따라(차원 및 [리소스](../../automating/using/query.md#targeting-dimensions-and-resources)타깃팅 참조) 다음을 수행할 수 있습니다.

* 대상 또는 프로필을 하나씩 선택
* 미리 정의된 필터 사용
* 원하는 필드에 대한 간단한 규칙 정의
* 특정 필드에 함수를 적용할 수 있는 고급 규칙을 정의합니다.

### 작업 영역 {#workspace}

작업 영역은 팔레트에서 추가된 규칙, 대상 및 사전 정의된 필터를 구성하고 결합할 수 있는 중앙 영역입니다.

팔레트에서 작업 영역으로 요소를 이동하면 새 창이 열리고 쿼리 [만들기를](#creating-queries)시작할 수 있습니다.

## 쿼리 만들기 {#creating-queries}

쿼리 편집기를 사용하여 메시지의 대상자 또는 테스트 프로필, 워크플로의 모집단 및 쿼리 유형 대상을 만들 수 있습니다.

쿼리를 만드는 동안 **[!UICONTROL Audience]** 창에서 쿼리를 정의하거나 워크플로우를 만드는 **동안 쿼리** 활동에서 정의할 수 있습니다.

1. 팔레트에서 작업 영역으로 요소를 이동합니다. 규칙을 편집할 창이 열립니다.

   * 문자열 또는 숫자 **필드에**&#x200B;비교 연산자와 값을 지정합니다.

      ![](assets/query_editor_audience_definition2.png)

   * 날짜 또는 날짜 및 시간 **필드에**&#x200B;대해 특정 날짜, 두 날짜 사이의 범위 또는 쿼리의 실행 날짜에 상대적인 기간을 정의하도록 선택할 수 있습니다.

      ![](assets/query_editor_date_field.png)

   * 부울 **필드의**&#x200B;경우 필드의 가능한 값에 연결된 상자를 선택합니다.
   * 그룹화 **** 필드에 대해 규칙을 만들 그룹화 필드를 선택한 다음 다른 필드와 같은 방식으로 조건을 정의합니다.

      ![](assets/query_editor_audience_definition4.png)

   * 다른 데이터베이스 리소스와 **1-1** 링크의 경우 타깃팅된 테이블에서 직접 값을 선택합니다.

      ![](assets/query_editor_audience_definition5.png)

   * 다른 데이터베이스 리소스와 **1-N** 링크의 경우 이 두 번째 리소스의 필드에 하위 쿼리를 정의할 수 있습니다.

      하위 조건을 지정할 필요가 없습니다.

      예를 들어 프로필 추적 로그에서 **[!UICONTROL Exists]** 연산자만 선택하고 규칙을 승인할 수 있습니다. 이 규칙은 추적 로그가 있는 모든 프로필을 반환합니다.

      ![](assets/query_editor_audience_definition6.png)

   * 사전 **정의된 필터의**&#x200B;경우 제공된 기준에 따라 원하는 요소를 입력하거나 선택합니다.

      관리자는 필터를 만들어 복잡하고 반복적인 쿼리를 용이하게 할 수 있습니다. 이러한 규칙은 미리 구성된 규칙 형식으로 쿼리 편집기에 표시되며 사용자가 수행하는 데 필요한 단계 수를 제한합니다.

      ![](assets/query-editor_filter_email-audience_filter.png)

1. 규칙의 이름을 지정할 수 있습니다. 그러면 작업 영역에서 규칙 이름으로 표시됩니다. 규칙에 이름이 지정되어 있지 않으면 조건에 대한 자동 설명이 표시됩니다.
1. 작업 영역 요소를 결합하려면 여러 그룹 및/또는 그룹 레벨을 만들 수 있도록 서로 잠급니다. 그런 다음 논리 연산자를 선택하여 동일한 수준에 있는 요소를 결합할 수 있습니다.

   * **[!UICONTROL AND]**:두 기준의 교차. 각 기준과 일치하는 요소만 고려됩니다.
   * **[!UICONTROL OR]**:두 기준의 결합. 두 기준 중 하나 이상에 맞는 요소가 고려됩니다.
   * **[!UICONTROL EXCEPT]**:제외 기준. 첫 번째 기준과 일치하는 요소는 두 번째 기준과도 일치하지 않는 한 고려됩니다.

1. 이제 작업 표시줄의 ![](assets/count.png) 및 ![](assets/preview.png) 단추를 사용하여 쿼리에 의해 타깃팅된 요소의 수를 계산하고 미리 볼 수 있습니다.

   ![](assets/query_editor_combining_rules.png)

쿼리의 요소를 수정하려면 편집 아이콘을 클릭합니다. 규칙이 이전에 구성된 대로 열리고 필요한 조정을 수행할 수 있습니다.

이제 쿼리가 만들어지고 정의되므로 인구를 작성하여 게재를 보다 효과적으로 개인화할 수 있습니다.

**관련 항목:**

* [고급 함수](../../automating/using/advanced-expression-editing.md)
* [필터 정의](../../developing/using/configuring-filter-definition.md)
* [사용 사례:일주일에 한 번 이메일 전달 만들기](../../automating/using/workflow-weekly-offer.md)
* [사용 사례:위치에 세그먼트화된 배달 만들기](../../automating/using/workflow-segmentation-location.md)
* [사용 사례:보충으로 배달 만들기](../../automating/using/workflow-created-query-with-complement.md)
* [사용 사례:비열기 사용자에게 새 배달을 보내는 다시 타깃팅 워크플로우](../../automating/using/workflow-cross-channel-retargeting.md)
