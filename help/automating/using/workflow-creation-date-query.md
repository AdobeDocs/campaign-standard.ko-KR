---
title: 프로필 생성 날짜에 배달 생성
description: 이 사용 사례에서는 프로필 생성 날짜에 배달을 만드는 방법을 보여줍니다.
page-status-flag: never-activated
uuid: 396a3de1-6ffa-4385-ac9f-15fdeae5a366
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities
discoiquuid: 377821e6-69f8-41cc-a1ad-8a2f5ed4d409
context-tags: workflow,use-case,query
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c3911232a3cce00c2b9a2e619f090a7520382dde
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 1%

---


# Creating deliveries on profiles&#39; creation date {#creation-date-query}

고객 프로필 작성 기념일에 이메일을 통해 오퍼를 보낼 수 있습니다.

1. 에서 **[!UICONTROL Marketing Activities]**&#x200B;을 클릭하고 **[!UICONTROL Create]** 선택합니다 **[!UICONTROL Workflow]**.
1. 워크플로우 유형 **[!UICONTROL New Workflow]** 으로 선택하고 을 클릭합니다 **[!UICONTROL Next]**.
1. 워크플로우의 속성을 입력하고 를 클릭합니다 **[!UICONTROL Create]**.

## 스케줄러 활동 만들기 {#creating-a-scheduler-activity}

1. > **[!UICONTROL Activities]** 에서 스케줄러 **[!UICONTROL Execution]**&#x200B;활동을 드래그하여 [](../../automating/using/scheduler.md) 놓습니다.
1. 활동을 두 번 클릭합니다.
1. 배달 실행을 구성합니다.
1. 에서 **[!UICONTROL Execution frequency]**&#x200B;를 선택합니다 **[!UICONTROL Daily]**.
1. 워크플로우에 대한 실행 **[!UICONTROL Time]** 을 **[!UICONTROL Repetition frequency]** 선택합니다.
1. 워크플로우에 사용할 **[!UICONTROL Start]** 날짜 **[!UICONTROL Expiration]** 를 선택합니다.
1. 활동을 확인하고 워크플로우를 저장합니다.

>[!NOTE]
>
>특정 시간대에서 워크플로우를 시작하려면&#x200B;**[!UICONTROL Execution options]**&#x200B;탭에서 **[!UICONTROL Time zone]**&#x200B;필드에 스케줄러의 시간대를 설정합니다. 기본적으로 선택한 시간대는 워크플로우 속성에 정의된 시간대입니다(워크플로우 [작성 참조](../../automating/using/building-a-workflow.md)).

![](assets/time_zone.png)

## 쿼리 활동 만들기 {#creating-a-query-activity}

1. 수신자를 선택하려면 [쿼리](../../automating/using/query.md) 활동을 드래그하여 놓고 두 번 클릭합니다.
1. 값을 **[!UICONTROL Profiles]** 추가하고 **[!UICONTROL no longer contact by email]** 선택합니다 **[!UICONTROL no]**.

### 실행 날짜와 동일한 날짜에 생성된 프로필 검색 {#retriving-profiles-created-on-the-same-day}

1. 에서 **[!UICONTROL Profile]**&#x200B;필드를 드래그하여 **[!UICONTROL Created]** 놓습니다. 을 클릭하고 을 클릭합니다 **[!UICONTROL Advanced Mode]**.
   ![](assets/advanced_mode.png)
1. 노드에서 **[!UICONTROL list of functions]**&#x200B;두 번&#x200B;**[!UICONTROL Day]** 을&#x200B;**[!UICONTROL Date]**&#x200B;클릭합니다.
1. 그런 다음 필드를 인수 **[!UICONTROL Created]** 로 삽입합니다.
1. 연산자로 **[!UICONTROL equals to (=)]** 선택합니다.
1. [값]**[!UICONTROL Day]** 의 **[!UICONTROL Date]** 노드에서 을 선택합니다 **[!UICONTROL List of functions]**.
1. 함수를 인수로&#x200B;**[!UICONTROL GetDate()]**&#x200B;삽입합니다.

생성일이 현재 날과 같은 프로파일을 검색했습니다.

다음과 같이 끝나야 합니다.

```Day(@created) = Day(GetDate())```

![](assets/day_creation_query.png)

**[!UICONTROL Confirm]**&#x200B;을 클릭합니다.

### 실행 월과 동일한 달에 생성된 프로필 검색{#retriving-profiles-created-on-the-same-month}

1. 편집기에서 **[!UICONTROL Query]** 첫 번째 쿼리를 선택하고 복제합니다.
1. 복제를 엽니다.
1. 쿼리에서 다음으로 **[!UICONTROL Day]** **[!UICONTROL Month]** 바꿉니다.
1. **[!UICONTROL Confirm]**&#x200B;을 클릭합니다.

![](assets/month_rule.png)

이렇게 해야 합니다.

``` Month(@created) = Month(GetDate()) ```

최종 쿼리는 다음과 같이 표시됩니다.

```Day(@created) = Day(GetDate()) AND Month(@created) = Month(GetDate())```

![](assets/expression_editor_1.png)

## 이메일 배달 만들기{#creating-an-email-delivery}

1. 이메일 배달 [활동을 드래그하여](../../automating/using/email-delivery.md) 놓습니다.
1. 활동을 클릭하고 ![](assets/edit_darkgrey-24px.png) 편집하려면 선택합니다.
1. 을 선택하고 **[!UICONTROL Recurring email]** 클릭합니다 **[!UICONTROL Next]**.
1. 이메일 템플릿을 선택하고 을 클릭합니다 **[!UICONTROL Next]**.
1. 이메일 속성을 입력하고 을 클릭합니다 **[!UICONTROL Next]**.
1. 이메일 레이아웃을 만들려면 을 클릭합니다 **[!UICONTROL Email Designer]**.
1. 요소를 삽입하거나 기존 템플릿을 선택합니다.
1. 필드 및 링크를 사용하여 이메일 개인화
자세한 내용은 이메일 [디자인을 참조하십시오](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch).
1. 레이아웃 **[!UICONTROL Preview]** 을 확인하려면 을(를) 클릭합니다.
1. **[!UICONTROL Save]**&#x200B;을 클릭합니다.

**관련 항목:**

* [이메일 채널](../../channels/using/creating-an-email.md)
