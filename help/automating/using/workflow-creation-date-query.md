---
title: '" 워크플로우 사용 사례: 프로필 작성 날짜에 배달 만들기 "'
seo-title: '" 워크플로우 사용 사례: 프로필 작성 날짜에 배달 만들기 "'
description: '" 워크플로우 사용 사례: 프로필 작성 날짜에 배달 만들기 "'
seo-description: '" 워크플로우 사용 사례: 프로필 작성 날짜에 배달 만들기 "'
page-status-flag: 정품 인증 안 함
uuid: 396 a 3 de 1-6 ffa -4385-ac 9 f -15 fdeae 5 a 366
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: '실행 활동 '
discoiquuid: 377821 E 6-69 F 8-41 CC-A 1 AD -8 A 2 F 5 ED 4 D 409
context-tags: 워크플로우, 사용 사례, 쿼리
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: f57775ec88925d43046fe4162f2753c189d50c62

---


# 워크플로우 사용 사례: 프로필 작성 날짜에 배달 만들기 {#creation-date-query}

고객의 프로필 작성 시 이메일을 통해 이메일을 보낼 수 있습니다.

1. 에서 **[!UICONTROL Marketing Activities]****[!UICONTROL Create]****[!UICONTROL Workflow]**&#x200B;를 클릭하고 선택합니다.
1. 워크플로우 유형으로 선택하고 **[!UICONTROL New Workflow]** 를 **[!UICONTROL Next]**&#x200B;클릭합니다.
1. 워크플로우의 속성을 입력하고 **[!UICONTROL Create]**&#x200B;를 클릭합니다.

## 스케줄러 활동 만들기 {#creating-a-scheduler-activity}

1. 에서 **[!UICONTROL Activities]** , A를 **[!UICONTROL Execution]**&#x200B;드래그하여 놓습니다 **[!UICONTROL Scheduler activity]**![](assets/scheduler_icon.png).
1. 활동을 두 번 클릭합니다.
1. 전달 실행을 구성합니다.
1. 에서 **[!UICONTROL Execution frequency]****[!UICONTROL Daily]**&#x200B;를 선택합니다.
1. 워크플로우에 대한 실행 **[!UICONTROL Time]****[!UICONTROL Repetition frequency]** 및 실행을 선택합니다.
1. 날짜와 워크플로우의 **[!UICONTROL Start]****[!UICONTROL Expiration]** 날짜를 선택합니다.

>[!NOTE]
>
>특정 시간대에서 워크플로우를 시작하려면&#x200B;**[!UICONTROL Execution options]**&#x200B;탭에서 스케줄러에 대한 표준 시간대를 **[!UICONTROL Time zone]**&#x200B;설정합니다.

![](assets/time_zone.png)

1. 활동을 확인하고 워크플로우를 저장합니다.

## 쿼리 활동 만들기 {#creating-a-query-activity}

1. 수신자를 선택하려면 A를 **[!UICONTROL Query activity]** 드래그하여 놓은 다음 두 번 클릭합니다.
1. 값을 추가하고 **[!UICONTROL Profiles]** 값을 **[!UICONTROL no longer contact by email]** 선택합니다 **[!UICONTROL no]**.

### 실행 날짜와 같은 날에 생성된 검색 프로필 {#retriving-profiles-created-on-the-same-day}

1. 에서 **[!UICONTROL Profile]****[!UICONTROL Created]** 필드를 드래그하여 놓습니다. **[!UICONTROL Advanced Mode]**을 클릭하고 클릭합니다.
   ![](assets/advanced_mode.png)
1. 에서 **[!UICONTROL list of functions]****[!UICONTROL Day]****[!UICONTROL Date]**&#x200B;노드를 두 번 클릭합니다.
1. 그런 다음 필드를 **[!UICONTROL Created]** 인수로 삽입합니다.
1. **[!UICONTROL equals to (=)]** 연산자로 선택합니다.
1. 값의 경우의 노드&#x200B;**[!UICONTROL Day]****[!UICONTROL Date]** 에서를 선택합니다 **[!UICONTROL List of functions]**.
1. **[!UICONTROL GetDate()]**&#x200B;함수를 인수로 삽입합니다.

작성일이 현재 일과 같은 프로필을 검색했습니다.

다음을 수행해야 합니다.

```Day(@created) = Day(GetDate())```

![](assets/day_creation_query.png)

**[!UICONTROL Confirm]**&#x200B;을 클릭합니다.

### 실행 월과 동일한 달에 생성된 검색 프로필{#retriving-profiles-created-on-the-same-month}

1. **[!UICONTROL Query]** 편집기에서 첫 번째 쿼리를 선택하고 복제합니다.
1. 복제를 엽니다.
1. 쿼리에서 **[!UICONTROL Day]****[!UICONTROL Month]** 로 바꿉니다.
이것으로 끝내야 합니다.

``` Month(@created) = Month(GetDate()) ```

1. **[!UICONTROL Confirm]**&#x200B;을 클릭합니다.

![](assets/month_rule.png)

최종 쿼리가 표시됩니다.

```Day(@created) = Day(GetDate()) AND Month(@created) = Month(GetDate())```

![](assets/expression_editor_1.png)

## 이메일 배달 만들기{#creating-an-email-delivery}

1. 이메일 배달을 드래그하여 놓습니다.
1. 활동을 클릭하고 ![](assets/edit_darkgrey-24px.png) 편집을 선택합니다.
1. **[!UICONTROL Recurring email]****[!UICONTROL Next]**&#x200B;을 선택하고 클릭합니다.
1. 이메일 템플릿을 선택하고 **[!UICONTROL Next]**&#x200B;를 클릭합니다.
1. 이메일 속성을 입력하고 **[!UICONTROL Next]**&#x200B;를 클릭합니다.
1. 이메일의 레이아웃을 만들려면 **[!UICONTROL Email Designer]**&#x200B;을 클릭합니다.
1. 요소를 삽입하거나 기존 템플릿을 선택합니다.
1. 필드와 링크를 사용하여 이메일을 개인화합니다.
자세한 내용은 이메일 [디자인을](../../designing/using/about-email-content-design.md#designing-an-email-content-from-scratch)참조하십시오.
1. 레이아웃을 **[!UICONTROL Preview]** 확인하려면을 클릭합니다.
1. **[!UICONTROL Save]**&#x200B;을 클릭합니다.

**관련 항목:**

* [쿼리](../../automating/using/query.md)
* [스케줄러](../../automating/using/scheduler.md)
* [이메일 배달](../../automating/using/email-delivery.md)
* [이메일 채널](../../channels/using/creating-an-email.md)
