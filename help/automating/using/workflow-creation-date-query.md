---
solution: Campaign Standard
product: campaign
title: 프로필 생성 날짜에 배달 생성
description: 이 사용 사례에서는 프로필 생성 날짜에 배달을 만드는 방법을 보여줍니다.
audience: automating
content-type: reference
topic-tags: execution-activities
context-tags: workflow,use-case,query
translation-type: tm+mt
source-git-commit: 45c80b5e6bf2169c5acf6eea70da9e2f130982c8
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 38%

---


# 프로필이 만들어진 날짜에 게재 만들기 {#creation-date-query}

고객 프로필 작성 기념일에 이메일을 통해 오퍼를 보낼 수 있습니다.

1. **[!UICONTROL Marketing Activities]**&#x200B;에서 **[!UICONTROL Create]**&#x200B;을(를) 클릭하고 **[!UICONTROL Workflow]**&#x200B;을(를) 선택합니다.
1. 워크플로우 유형으로 **[!UICONTROL New Workflow]**&#x200B;을(를) 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.
1. 워크플로우의 속성을 입력하고 **[!UICONTROL Create]**&#x200B;을(를) 클릭합니다 .

## 예약 활동 만들기 {#creating-a-scheduler-activity}

1. **[!UICONTROL Activities]** > **[!UICONTROL Execution]**&#x200B;에서 [스케줄러](../../automating/using/scheduler.md) 활동을 드래그하여 놓습니다.
1. 활동을 두 번 클릭합니다.
1. 게재 실행을 구성합니다.
1. **[!UICONTROL Execution frequency]**&#x200B;에서 **[!UICONTROL Daily]**&#x200B;을(를) 선택합니다.
1. 워크플로우에 대해 **[!UICONTROL Time]** 및 **[!UICONTROL Repetition frequency]** 실행을 선택합니다.
1. 워크플로우에 대해 **[!UICONTROL Start]** 날짜 및 **[!UICONTROL Expiration]**&#x200B;를 선택합니다.
1. 활동을 확인하고 워크플로우를 저장합니다.

>[!NOTE]
>
>특정 시간대에서 워크플로우를 시작하려면 **[!UICONTROL Execution options]** 탭에서 **[!UICONTROL Time zone]** 필드에 스케줄러의 시간대를 설정합니다. 기본적으로 선택된 시간대는 워크플로우 속성에 정의된 시간대입니다([워크플로우 구축](../../automating/using/building-a-workflow.md) 참조).

![](assets/time_zone.png)

## 쿼리 활동 만들기 {#creating-a-query-activity}

1. 수신자를 선택하려면 [쿼리](../../automating/using/query.md) 활동을 끌어다 놓고 두 번 클릭합니다.
1. **[!UICONTROL Profiles]**&#x200B;을(를) 추가하고 **[!UICONTROL no]** 값으로 **[!UICONTROL no longer contact by email]**&#x200B;을 선택합니다.

### 실행 날짜와 동일한 날짜에 생성된 프로필 검색 중 {#retrieving-profiles-created-on-the-same-day}

1. **[!UICONTROL Profile]**&#x200B;에서 **[!UICONTROL Created]** 필드를 드래그하여 놓습니다. **[!UICONTROL Advanced Mode]**을 클릭합니다.
   ![](assets/advanced_mode.png)
1. **[!UICONTROL list of functions]**&#x200B;에서 **[!UICONTROL Date]** 노드에서 **[!UICONTROL Day]**&#x200B;을 두 번 클릭합니다.
1. 그런 다음 **[!UICONTROL Created]** 필드를 인수로 삽입합니다.
1. **[!UICONTROL equals to (=)]**&#x200B;을 연산자로 선택합니다.
1. 값의 경우 **[!UICONTROL List of functions]**&#x200B;의 **[!UICONTROL Date]** 노드에서 **[!UICONTROL Day]**&#x200B;을 선택합니다.
1. **[!UICONTROL GetDate()]** 함수를 인수로 삽입합니다.

생성일이 현재 날과 같은 프로파일을 검색했습니다.

다음과 같이 끝나야 합니다.

```Day(@created) = Day(GetDate())```

![](assets/day_creation_query.png)

**[!UICONTROL Confirm]**&#x200B;을(를) 클릭합니다.

### 실행 월{#retrieving-profiles-created-on-the-same-month}과 같은 달에 생성된 프로필 검색

1. **[!UICONTROL Query]** 편집기에서 첫 번째 쿼리를 선택하고 복제합니다.
1. 복제를 엽니다.
1. 쿼리에서 **[!UICONTROL Day]**&#x200B;을(를) **[!UICONTROL Month]**&#x200B;로 바꿉니다.
1. **[!UICONTROL Confirm]**&#x200B;을(를) 클릭합니다.

![](assets/month_rule.png)

이렇게 해야 합니다.

``` Month(@created) = Month(GetDate()) ```

최종 쿼리는 다음과 같이 표시됩니다.

```Day(@created) = Day(GetDate()) AND Month(@created) = Month(GetDate())```

![](assets/expression_editor_1.png)

## 이메일 게재 만들기{#creating-an-email-delivery}

1. [이메일 배달](../../automating/using/email-delivery.md) 활동을 드래그하여 놓습니다.
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
