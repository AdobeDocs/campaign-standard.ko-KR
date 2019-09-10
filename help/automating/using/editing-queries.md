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
source-git-commit: bb65cbf808a95e8b42b2a682b7c0a9cc6225d920

---


# 쿼리 편집{#editing-queries}

## 쿼리 편집기 정보 {#about-query-editor}

쿼리 편집기는 Adobe Campaign 데이터베이스에 들어 있는 데이터를 필터링할 수 있는 마법사입니다.

이 기능을 사용하면 사전 정의된 필터 및 규칙 덕분에 받는 사람을 더 잘 타게팅할 수 있는 모집단을 만들 수 있습니다.

다음과 같은 목적으로 몇 가지 응용 프로그램 기능이 사용됩니다.

* **쿼리** 유형 **대상 만들기**
* **이메일** 대상 정의
* **워크플로우** 활동의 모집단에서 정의

## 쿼리 편집기 인터페이스 {#query-editor-interface}

쿼리 편집기는 **팔레트와** **작업 영역으로**&#x200B;구성됩니다.

![](assets/query_editor_overview.png)

### palette {#palette}

편집기의 왼쪽에 있는 팔레트는 테마 블록으로 나뉘어진 요소를 포함하는 두 개의 탭으로 나뉩니다. 이러한 탭은 다음과 같습니다.

* **기본적으로**&#x200B;사용할 수 있거나 인스턴스 관리자가 만든 단축키입니다. 여기에서 필드, 노드, 그룹, 1-1 링크, 1-n 링크 및 기타 사전 정의된 필터를 찾을 수 있습니다.
* 대상 **리소스의** 사용 가능한 모든 필드에 액세스할 수 있는 탐색기: 노드, 그룹화 요소, 링크 (1-1 및 1-n).

쿼리에 포함된 요소는 쿼리를 구성하고 고려하기 위해 작업 영역으로 이동해야 합니다. 선택한 타깃팅 차원에 따라 (차원 및 리소스 [타깃팅 참조](../../automating/using/query.md#targeting-dimensions-and-resources)) 다음을 수행할 수 있습니다.

* 대상 또는 프로필을 하나씩 선택
* 사전 정의된 필터 사용
* 원하는 필드에 대한 간단한 규칙 정의
* 특정 필드에 기능을 적용할 수 있는 고급 규칙 정의

### 작업 영역 {#workspace}

작업 영역은 규칙, 대상 및 팔레트에서 추가된 사전 정의된 필터를 구성하고 결합할 수 있는 중앙 영역입니다.

팔레트에서 작업 영역으로 요소를 이동하면 새 창이 열리고 쿼리 작성을 시작할 [](../../automating/using/editing-queries.md#creating-queries)수 있습니다.

## 쿼리 만들기 {#creating-queries}

쿼리 편집기를 사용하여 메시지에서 대상 또는 테스트 프로필을 정의하고, 워크플로우의 모집단에서 쿼리 유형 대상을 만들 수 있습니다.

워크플로우를 만드는 동안 **[!UICONTROL Audience]** 창에서 쿼리를 만들거나 **쿼리** 활동에서 쿼리를 정의할 수 있습니다.

1. 팔레트에서 작업 공간으로 요소를 이동합니다. 규칙을 편집할 창이 열립니다.

   * 문자열 또는 숫자 **필드에**&#x200B;대해 비교 연산자와 값을 지정합니다.

      ![](assets/query_editor_audience_definition2.png)

   * 날짜 또는 날짜 및 시간 **필드에 대해 특정 날짜**, 두 날짜 사이의 범위 또는 쿼리의 실행 날짜에 상대적인 기간을 정의할 수 있습니다.

      ![](assets/query_editor_date_field.png)

   * 부울 **필드에**&#x200B;대해 필드에 가능한 값에 연결된 상자를 선택합니다.
   * **그룹** 필드에서 규칙을 만들 그룹화 필드를 선택한 다음 다른 필드에 대해 동일한 방법으로 조건을 정의합니다.

      ![](assets/query_editor_audience_definition4.png)

   * 다른 데이터베이스 리소스와 **1-1 링크의** 경우 타깃팅된 표에서 직접 값을 선택합니다.

      ![](assets/query_editor_audience_definition5.png)

   * 다른 데이터베이스 리소스가 있는 **1-n** 링크의 경우 이 보조 리소스의 필드에 하위 쿼리를 정의할 수 있습니다.

      하위 조건을 지정할 필요는 없습니다.

      예를 들어 프로필 추적 로그에서 **[!UICONTROL Exists]** 연산자를 선택하고 규칙을 승인할 수만 있습니다. 규칙은 추적 로그가 존재하는 모든 프로필을 반환합니다.

      ![](assets/query_editor_audience_definition6.png)

   * **사전 정의된 필터의**&#x200B;경우 제공된 기준에 따라 원하는 요소를 입력하거나 선택합니다.

      관리자는 필터를 만들어 복잡하고 반복적인 쿼리를 만들 수 있습니다. 이것은 사전 구성된 규칙 형태의 쿼리 편집기에 나타나며 사용자가 수행해야 하는 단계를 제한합니다.

      ![](assets/query-editor_filter_email-audience_filter.png)

1. 규칙 이름을 지정할 수 있습니다. 그런 다음 작업 공간에서 규칙 이름으로 표시됩니다. 규칙에 이름이 지정되어 있지 않으면 조건에 대한 자동 설명이 표시됩니다.
1. 작업 영역 요소를 결합하려면 서로 결합하여 서로 다른 그룹 및/또는 그룹 수준을 만듭니다. 그런 다음 논리 연산자를 선택하여 동일한 수준의 요소를 결합할 수 있습니다.

   * **[!UICONTROL AND]**: 두 가지 기준의 교차점. 각 기준과 일치하는 요소만 고려됩니다.
   * **[!UICONTROL OR]**: 두 가지 기준의 조합입니다. 두 조건 중 적어도 하나와 일치하는 요소가 고려됩니다.
   * **[!UICONTROL EXCEPT]**: 제외 기준. 첫 번째 기준과 일치하는 요소는 두 번째 기준과 일치하지 않는 한 고려됩니다.

1. 이제 작업 표시줄의 ![](assets/count.png) AND ![](assets/preview.png) 단추를 사용하여 쿼리에서 타깃팅한 요소의 수를 계산하고 미리 볼 수 있습니다.

   ![](assets/query_editor_combining_rules.png)

쿼리의 요소를 수정하려면 편집 아이콘을 클릭합니다. 규칙이 이전에 구성된 대로 열리고 필요한 조정을 수행할 수 있습니다.

이제 쿼리가 만들어지고 정의되므로 모집단을 만들어 전달을 보다 효과적으로 개인화할 수 있습니다.

**관련 항목:**

* [고급 함수](../../automating/using/advanced-expression-editing.md)
* [필터 정의](../../developing/using/configuring-filter-definition.md)
* [사용 사례: 일주일에 한 번 이메일 배달 만들기](../../automating/using/workflow-weekly-offer.md)
* [사용 사례: 위치에서 세그먼트화된 배달 만들기](../../automating/using/workflow-segmentation-location.md)
* [사용 사례: 보완을 통한 전달 창출](../../automating/using/workflow-created-query-with-complement.md)
* [사용 사례: 새 배달을 오프닝으로 전송하는 재타깃팅 워크플로우](../../automating/using/workflow-cross-channel-retargeting.md)
