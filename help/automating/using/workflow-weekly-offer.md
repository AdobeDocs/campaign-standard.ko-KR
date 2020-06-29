---
title: 주간 게재
description: 이 사용 사례에서는 주별 배달을 만드는 방법을 보여줍니다.
page-status-flag: never-activated
uuid: 396a3de1-6ffa-4385-ac9f-15fdeae5a366
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities
discoiquuid: 377821e6-69f8-41cc-a1ad-8a2f5ed4d409
context-tags: workflow,use-case,query,delivery,scheduler
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c3911232a3cce00c2b9a2e619f090a7520382dde
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 3%

---


# 매주 화요일 이메일 배달 만들기{#creating-email-every-tuesday}

매주 화요일 특별 할인 행사를 위해 모든 고객에게 이메일을 보낼 수 있습니다.

1. 에서 **[!UICONTROL Marketing Activities]**&#x200B;을 클릭하고 **[!UICONTROL Create]** 선택합니다 **[!UICONTROL Workflow]**.
1. 워크플로우 유형 **[!UICONTROL New Workflow]** 으로 선택하고 을 클릭합니다 **[!UICONTROL Next]**.
1. 워크플로우의 속성을 입력하고 를 클릭합니다 **[!UICONTROL Create]**.

## 스케줄러 활동 만들기{#creating-a-scheduler-activity}

1. > **[!UICONTROL Activities]** 에서 스케줄러 **[!UICONTROL Execution]**&#x200B;활동을 드래그하여 [](../../automating/using/scheduler.md) 놓습니다.
1. 활동을 두 번 클릭합니다.
1. 배달 실행을 구성합니다.
1. 에서 **[!UICONTROL Execution frequency]**&#x200B;를 선택합니다 **[!UICONTROL Weekly]**.
1. 게재에 대해 **[!UICONTROL Time]** 및 **[!UICONTROL Repetition frequency]** a를 선택합니다.
1. 에서 **[!UICONTROL Days of the week]**&#x200B;를 선택합니다 **[!UICONTROL Tuesday]**.
1. 워크플로우에 대한 **[!UICONTROL Start]** 및 **[!UICONTROL Expiration]** 매개 변수를 지정합니다.
1. 활동을 확인하고 워크플로우를 저장합니다.

![](assets/scheduler_properties.png)

>[!NOTE]
>
>특정 탭에서 워크플로우를 시작하려면 시간대 필드 **[!UICONTROL Time Zone]**&#x200B;에서 스케줄러의 시간대를&#x200B;**[!UICONTROL Execution options]**&#x200B;설정합니다. 기본적으로 선택한 시간대는 워크플로우 속성에 정의된 시간대입니다(워크플로우 [작성 참조](../../automating/using/building-a-workflow.md)).

## 쿼리 활동 만들기{#creating-a-query-activity}

1. > **[!UICONTROL Activities]** 에서 수신자를 선택하려면 **[!UICONTROL Targeting]**&#x200B;쿼리 [](../../automating/using/query.md) 활동을 끌어다 놓고 두 번 클릭합니다.
1. > **[!UICONTROL Shortcuts]** 에서 **[!UICONTROL Profile]**&#x200B;드래그하여 놓습니다 **[!UICONTROL Email]**.
1. 연산자 **[!UICONTROL is not empty]** 로 선택합니다.
1. > **[!UICONTROL Shortcuts]** 에서 프로필 **[!UICONTROL General]**&#x200B;을 추가하고 값 **[!UICONTROL no longer contact by email]** 으로 선택합니다 **[!UICONTROL No]**.
1. **[!UICONTROL Confirm]**&#x200B;을 클릭합니다.

![](assets/wf-complement-query.png)

## 이메일 배달 만들기{#creating-an-email-delivery}

1. > **[!UICONTROL Activities]** 에서 **[!UICONTROL Channels]**&#x200B;이메일 배달 [](../../automating/using/email-delivery.md) 활동을 드래그하여 놓습니다.
1. 활동을 클릭하고 ![](assets/edit_darkgrey-24px.png) 편집하려면 선택합니다.
1. 을 선택하고 **[!UICONTROL Recurring email]** 클릭합니다 **[!UICONTROL Next]**.
1. 이메일 템플릿을 선택하고 을 클릭합니다 **[!UICONTROL Next]**.
1. 이메일 속성을 입력하고 을 클릭합니다 **[!UICONTROL Next]**.
1. 이메일 레이아웃을 만들려면 을 클릭합니다 **[!UICONTROL Use Email Designer]**.
1. 요소를 삽입하거나 기존 템플릿을 선택합니다.
1. 필드 및 링크를 사용하여 이메일 개인화
1. **[!UICONTROL Save]**&#x200B;을 클릭합니다.

자세한 내용은 이메일 [디자인을 참조하십시오](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch).

**관련 항목:**

* [이메일 채널](../../channels/using/creating-an-email.md)
