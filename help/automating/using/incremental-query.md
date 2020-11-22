---
solution: Campaign Standard
product: campaign
title: 증분 쿼리
description: 증분 쿼리 활동을 통해 Adobe Campaign 데이터베이스에서 요소 모집단을 필터링하고 추출할 수 있습니다.
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: incremental,main
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 98%

---


# 증분 쿼리{#incremental-query}

## 설명 {#description}

![](assets/incremental.png)

**[!UICONTROL Incremental query]** 활동을 통해 Adobe Campaign 데이터베이스에서 요소 모집단을 필터링하고 추출할 수 있습니다. 이 활동이 실행될 때마다 이전 실행의 결과가 제외됩니다. 이를 통해 새 요소만 타겟팅할 수 있습니다.

전용 탭을 통해 타겟팅된 모집단에 대한 **[!UICONTROL Additional data]**&#x200B;을(를) 정의할 수 있습니다. 이 데이터는 추가 열에 저장되며 진행 중인 워크플로우에만 사용할 수 있습니다.

이 활동은 쿼리 편집기 도구를 사용합니다. 이 도구는 [전용 섹션](../../automating/using/editing-queries.md#about-query-editor)에 자세히 설명되어 있습니다.

## 사용의 컨텍스트 {#context-of-use}

워크플로우의 실행 빈도를 정의하려면 **[!UICONTROL Scheduler]**&#x200B;에 **[!UICONTROL Incremental query]**&#x200B;을(를) 연결하여 쿼리해야 합니다.

이 활동에 해당하는 **[!UICONTROL Processed data]** 탭에서는 필요한 경우 활동의 이전 실행 결과를 볼 수 있습니다.

**[!UICONTROL Incremental query]** 활동은 다양한 용도로 사용할 수 있습니다.

* 메시지, 대상자 등의 타겟을 정의하기 위한 개인 세그먼트화.

* 데이터 내보내기.

   **[!UICONTROL Incremental query]** 활동을 사용하여 파일에서 새 로그를 정기적으로 내보낼 수 있습니다. 예를 들어 외부 보고 또는 BI 도구에서 로그 데이터를 사용하려는 경우 유용합니다. 전체 예제는 [로그 내보내기](../../automating/using/exporting-logs.md) 섹션에서 확인할 수 있습니다.

**관련 항목**

* [사용 사례:서비스 가입자에 대한 증분 쿼리](../../automating/using/incremental-query-on-subscribers.md)

## 구성 {#configuration}

1. **[!UICONTROL Incremental query]** 활동을 워크플로우로 끌어서 놓습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업에서 ![](assets/edit_darkgrey-24px.png) 버튼을 사용하여 활동을 엽니다.
1. 프로필 리소스 이외의 리소스에 대해 쿼리를 실행하려면 활동의 **[!UICONTROL Properties]** 탭으로 이동하여 **[!UICONTROL Resource]** 및 **[!UICONTROL Targeting dimension]**&#x200B;을(를) 선택합니다.

   **[!UICONTROL Resource]**&#x200B;을(를) 사용하면 팔레트에 표시된 필터를 세분화할 수 있지만, 선택한 리소스와 관련된 상황별 **[!UICONTROL Targeting dimension]**&#x200B;은(는) 가져오려는 모집단 유형(식별된 프로필, 게재, 선택한 리소스에 연결된 데이터 등)에 해당합니다.

1. **[!UICONTROL Target]** 탭에서 규칙을 정의하고 결합하여 쿼리를 실행합니다.
1. **[!UICONTROL Processed data]** 탭에서 워크플로우의 다음 실행에 사용할 증분 모드를 선택합니다.

   * **[!UICONTROL Use the exclusion of the results of previous executions]**: 새로운 각 실행에 대한 이전 실행 결과는 제외됩니다.
   * **[!UICONTROL Use a date field]**: 다음 실행은 선택한 날짜 필드가 **[!UICONTROL Incremental query]** 활동의 마지막 실행 날짜보다 크거나 같은 결과만 고려합니다. **[!UICONTROL Properties]** 탭에서 선택한 리소스와 관련된 날짜 필드를 선택할 수 있습니다. 이 모드는 로그 데이터와 같은 큰 리소스를 쿼리할 때 성능이 향상됩니다.

      워크플로우가 처음 실행된 후 다음 실행에 사용될 마지막 실행 날짜를 이 탭에서 확인할 수 있습니다. 워크플로우가 실행될 때마다 자동으로 업데이트됩니다. 필요에 맞게 새 값을 수동으로 입력하여 이 값을 재정의할 수 있습니다.
   >[!NOTE]
   >
   >**[!UICONTROL Use a date field]** 모드에서는 선택한 날짜 필드에 따라 보다 유연하게 대처할 수 있습니다. 예를 들어 선택한 필드가 수정 날짜에 해당하는 경우 날짜 필드 모드에서는 최근에 업데이트된 데이터를 검색할 수 있고, 다른 모드에서는 워크플로우의 마지막 실행 이후 이미 수정되었더라도 이전 실행에서 이미 타겟팅된 레코딩은 제외합니다.

   ![](assets/incremental_query_usedatefield.png)

1. 전용 탭을 통해 타겟팅된 모집단에 대한 **[!UICONTROL Additional data]**&#x200B;을(를) 정의할 수 있습니다. 이 데이터는 추가 열에 저장되며 진행 중인 워크플로우에만 사용할 수 있습니다. 특히 쿼리의 타겟팅 차원에 연결된 Adobe Campaign 데이터베이스 테이블에서 데이터를 추가할 수 있습니다. [데이터 강화](../../automating/using/query.md#enriching-data) 섹션을 참조하십시오.
1. 활동 구성을 확인하고 워크플로우를 저장합니다.

## 데이터 강화 {#enriching-data}

쿼리의 경우와 마찬가지로 **[!UICONTROL Incremental query]**&#x200B;에서 데이터를 강화할 수 있습니다. [데이터 강화](../../automating/using/query.md#enriching-data) 섹션을 참조하십시오.
