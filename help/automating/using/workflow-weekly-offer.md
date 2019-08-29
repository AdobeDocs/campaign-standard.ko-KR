---
title: '" 워크플로우 사용 사례: 주별 배달 만들기 "'
seo-title: '" 워크플로우 사용 사례: 주별 배달 만들기 "'
description: '" 워크플로우 사용 사례: 주별 배달 만들기 "'
seo-description: '" 워크플로우 사용 사례: 주별 배달 만들기 "'
page-status-flag: 정품 인증 안 함
uuid: 396 a 3 de 1-6 ffa -4385-ac 9 f -15 fdeae 5 a 366
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: '실행 활동 '
discoiquuid: 377821 E 6-69 F 8-41 CC-A 1 AD -8 A 2 F 5 ED 4 D 409
context-tags: 워크플로우, 사용 사례, 쿼리, 전달, 스케줄러
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: f57775ec88925d43046fe4162f2753c189d50c62

---


# Worflow 사용 사례: 매주 화요일 이메일 배달{#creating-email-every-tuesday}

모든 특별 할인을 위해 매주 화요일마다 이메일을 보낼 수 있습니다.

1. 에서 **[!UICONTROL Marketing Activities]****[!UICONTROL Create]****[!UICONTROL Workflow]**&#x200B;를 클릭하고 선택합니다.
1. 워크플로우 유형으로 선택하고 **[!UICONTROL New Workflow]** 를 **[!UICONTROL Next]**&#x200B;클릭합니다.
1. 워크플로우의 속성을 입력하고 **[!UICONTROL Create]**&#x200B;를 클릭합니다.

## 스케줄러 활동 만들기{#creating-a-scheduler-activity}

1. 에서 **[!UICONTROL Activities]** , A를 **[!UICONTROL Execution]**&#x200B;드래그하여 놓습니다 **[!UICONTROL Scheduler activity]**![](assets/scheduler_icon.png).
1. 활동을 두 번 클릭합니다.
1. 전달 실행을 구성합니다.
1. 에서 **[!UICONTROL Execution frequency]****[!UICONTROL Weekly]**&#x200B;를 선택합니다.
1. 게재의 A **[!UICONTROL Time]** 와 A **[!UICONTROL Repetition frequency]** 를 선택합니다.
1. 에서 **[!UICONTROL Days of the week]****[!UICONTROL Tuesday]**&#x200B;를 선택합니다.
1. 워크플로우에 대한 **[!UICONTROL Start]** AND 매개 **[!UICONTROL Expiration]** 변수를 지정합니다.

![](assets/scheduler_properties.png)

>[!NOTE]
>
>특정 위치에서 워크플로우를 **[!UICONTROL Time Zone]**&#x200B;시작하려면&#x200B;**[!UICONTROL Execution options]**, 탭에서 시간대 필드에 스케줄러에 대한 시간대를 설정합니다.

1. 활동을 확인하고 워크플로우를 저장합니다.

## 쿼리 활동 만들기{#creating-a-query-activity}

1. &gt; **[!UICONTROL Activities]****[!UICONTROL Targeting]**&#x200B;수신자를 선택하려면 **[!UICONTROL query]** 활동을 드래그하여 놓고 두 번 클릭합니다.
1. 시작 **[!UICONTROL Shortcuts]** &gt; **[!UICONTROL Profile]**&#x200B;드래그하여 **[!UICONTROL Email]**&#x200B;놓습니다.
1. **[!UICONTROL is not empty]** 연산자로 선택합니다.
1. &gt; **[!UICONTROL Shortcuts]****[!UICONTROL General]**&#x200B;프로필을 추가하고 값을 **[!UICONTROL no longer contact by email]****[!UICONTROL No]**&#x200B;선택합니다.
1. **[!UICONTROL Confirm]**&#x200B;을 클릭합니다.

## 이메일 배달 만들기{#creating-an-email-delivery}

1. 에서 **[!UICONTROL Activities]****[!UICONTROL Channels]**&#x200B;를 드래그하여 놓습니다 **[!UICONTROL Email delivery]**.
1. 활동을 클릭하고 ![](assets/edit_darkgrey-24px.png) 편집을 선택합니다.
1. **[!UICONTROL Recurring email]****[!UICONTROL Next]**&#x200B;을 선택하고 클릭합니다.
1. 이메일 템플릿을 선택하고 **[!UICONTROL Next]**&#x200B;를 클릭합니다.
1. 이메일 속성을 입력하고 **[!UICONTROL Next]**&#x200B;를 클릭합니다.
1. 이메일의 레이아웃을 만들려면 **[!UICONTROL Use Email Designer]**&#x200B;을 클릭합니다.
1. 요소를 삽입하거나 기존 템플릿을 선택합니다.
1. 필드와 링크를 사용하여 이메일을 개인화합니다.
1. Click **[!UICONTROL Save]**.

자세한 내용은 이메일 [디자인을](../../designing/using/about-email-content-design.md#designing-an-email-content-from-scratch)참조하십시오.

**관련 항목:**

* [쿼리 활동](../..//automating/using/query.md)
* [스케줄러 활동](../..//automating/using/scheduler.md)
* [이메일 배달](../..//automating/using/email-delivery.md)
* [이메일 채널](../..//channels/using/creating-an-email.md)
