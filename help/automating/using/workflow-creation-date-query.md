---
title: 프로필 생성 날짜에 게재 만들기
description: 이 사용 사례에서는 프로필이 만들어진 날짜에 게재를 만드는 방법을 보여줍니다.
audience: automating
content-type: reference
topic-tags: execution-activities
context-tags: workflow,use-case,query
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: f611e023-f74c-476e-83b9-aff451f68c81
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 38%

---

# 프로필이 만들어진 날짜에 게재 만들기 {#creation-date-query}

고객 프로필 생성 기념일에 이메일을 통해 오퍼를 보낼 수 있습니다.

1. **[!UICONTROL Marketing Activities]**&#x200B;에서 **[!UICONTROL Create]**&#x200B;을(를) 클릭하고 **[!UICONTROL Workflow]**&#x200B;을(를) 선택합니다.
1. 워크플로우 유형으로 **[!UICONTROL New Workflow]**&#x200B;을(를) 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.
1. 워크플로우의 속성을 입력하고 **[!UICONTROL Create]**&#x200B;을(를) 클릭합니다 .

## 예약 활동 만들기 {#creating-a-scheduler-activity}

1. 위치 **[!UICONTROL Activities]** > **[!UICONTROL Execution]**, 드래그 앤 드롭 [스케줄러](../../automating/using/scheduler.md) 활동.
1. 활동을 두 번 클릭합니다.
1. 게재 실행을 구성합니다.
1. **[!UICONTROL Execution frequency]**&#x200B;에서 **[!UICONTROL Daily]**&#x200B;을(를) 선택합니다.
1. 선택 **[!UICONTROL Time]** 및 **[!UICONTROL Repetition frequency]** 워크플로우에 대한 실행 권한입니다.
1. 선택 **[!UICONTROL Start]** 날짜 및 **[!UICONTROL Expiration]** 워크플로우에 사용됩니다.
1. 활동을 확인하고 워크플로우를 저장합니다.

>[!NOTE]
>
>특정 시간대에 워크플로우를 시작하려면 **[!UICONTROL Execution options]** 탭에서 예약의 시간대를 설정합니다. **[!UICONTROL Time zone]** 필드. 기본적으로 선택된 시간대는 워크플로우 속성에 정의된 시간대입니다([워크플로우 구축](../../automating/using/building-a-workflow.md) 참조).

![](assets/time_zone.png)

## 쿼리 활동 만들기 {#creating-a-query-activity}

1. 수신자를 선택하려면 다음을 드래그 앤 드롭하십시오. [쿼리](../../automating/using/query.md) 활동을 클릭한 다음 두 번 클릭합니다.
1. 추가 **[!UICONTROL Profiles]** 및 선택 **[!UICONTROL no longer contact by email]** 값 포함 **[!UICONTROL no]**.

### 실행 당일 생성된 프로필 검색 {#retrieving-profiles-created-on-the-same-day}

1. 위치 **[!UICONTROL Profile]**, 을(를) 끌어다 놓습니다. **[!UICONTROL Created]** 필드. 및 클릭 **[!UICONTROL Advanced Mode]**.
   ![](assets/advanced_mode.png)
1. 다음에서 **[!UICONTROL list of functions]**, 두 번 클릭 **[!UICONTROL Day]** 다음에서 **[!UICONTROL Date]** 노드.
1. 그런 다음 필드를 삽입합니다 **[!UICONTROL Created]** 를 인수로 사용합니다.
1. 선택 **[!UICONTROL equals to (=)]** 를 연산자로 사용하십시오.
1. Value에서 **[!UICONTROL Day]** 다음에서 **[!UICONTROL Date]** 의 노드 **[!UICONTROL List of functions]**.
1. 삽입 **[!UICONTROL GetDate()]** 인수로 작동합니다.

만든 날짜가 현재 날짜와 동일한 프로필을 검색했습니다.

다음으로 끝남:

```Day(@created) = Day(GetDate())```

![](assets/day_creation_query.png)

**[!UICONTROL Confirm]**&#x200B;를 클릭합니다.

### 실행 월과 동일한 달에 생성된 프로필 검색{#retrieving-profiles-created-on-the-same-month}

1. 다음에서 **[!UICONTROL Query]** 편집기에서 첫 번째 쿼리를 선택하고 복제합니다.
1. 복제본을 엽니다.
1. 바꾸기 **[!UICONTROL Day]** 작성자: **[!UICONTROL Month]** 을 클릭합니다.
1. **[!UICONTROL Confirm]**&#x200B;를 클릭합니다.

![](assets/month_rule.png)

이 문제를 해결해야 합니다.

``` Month(@created) = Month(GetDate()) ```

마지막 쿼리가 표시됩니다.

```Day(@created) = Day(GetDate()) AND Month(@created) = Month(GetDate())```

![](assets/expression_editor_1.png)

## 이메일 게재 만들기{#creating-an-email-delivery}

1. 드래그 앤 드롭 [이메일 게재](../../automating/using/email-delivery.md) 활동.
1. 활동을 클릭하고 편집하려면 ![](assets/edit_darkgrey-24px.png)을(를) 선택합니다.
1. **[!UICONTROL Recurring email]**&#x200B;을(를) 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다 .
1. 전자 메일 템플릿을 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.
1. 전자 메일 속성을 입력하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.
1. 전자 메일 레이아웃을 만들려면 **[!UICONTROL Email Designer]**&#x200B;을(를) 클릭합니다.
1. 요소를 삽입하거나 기존 템플릿을 선택합니다.
1. 필드 및 링크를 사용하여 이메일을 개인화합니다.
자세한 내용은 [전자 메일 디자인](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch)을 참조하십시오.
1. 레이아웃을 확인하려면&#x200B;**[!UICONTROL Preview]**&#x200B;을(를) 클릭합니다.
1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

**관련 항목:**

* [이메일 채널](../../channels/using/creating-an-email.md)
