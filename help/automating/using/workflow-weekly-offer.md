---
solution: Campaign Standard
product: campaign
title: 주간 게재
description: 이 사용 사례에서는 주별 배달을 만드는 방법을 보여줍니다.
audience: automating
content-type: reference
topic-tags: execution-activities
context-tags: workflow,use-case,query,delivery,scheduler
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 81%

---


# 매주 화요일 이메일 배달 만들기{#creating-email-every-tuesday}

매주 화요일에 모든 고객에게 이메일을 보내어 특별 할인을 알릴 수 있습니다.

1. **[!UICONTROL Marketing Activities]**&#x200B;에서 **[!UICONTROL Create]**&#x200B;을(를) 클릭하고 **[!UICONTROL Workflow]**&#x200B;을(를) 선택합니다.
1. 워크플로우 유형으로 **[!UICONTROL New Workflow]**&#x200B;을(를) 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.
1. 워크플로우의 속성을 입력하고 **[!UICONTROL Create]**&#x200B;을(를) 클릭합니다.

## 예약 활동 만들기{#creating-a-scheduler-activity}

1. In **[!UICONTROL Activities]** > **[!UICONTROL Execution]**, drag and drop a [Scheduler](../../automating/using/scheduler.md) activity.
1. 활동을 두 번 클릭합니다.
1. 게재 실행을 구성합니다.
1. **[!UICONTROL Execution frequency]**&#x200B;에서 **[!UICONTROL Weekly]**&#x200B;을(를) 선택합니다.
1. 게재의 **[!UICONTROL Time]** 및 **[!UICONTROL Repetition frequency]**&#x200B;을(를) 선택합니다.
1. **[!UICONTROL Days of the week]**&#x200B;에서 **[!UICONTROL Tuesday]**&#x200B;을(를) 선택합니다.
1. 워크플로우의 **[!UICONTROL Start]** 및 **[!UICONTROL Expiration]** 매개 변수를 지정합니다.
1. 활동을 확인하고 워크플로우를 저장합니다.

![](assets/scheduler_properties.png)

>[!NOTE]
>
>특정 **[!UICONTROL Time Zone]**&#x200B;에 워크플로우를 시작하려면 **[!UICONTROL Execution options]** 탭의 시간대 필드에서 예약의 시간대를 설정합니다. 기본적으로 선택된 시간대는 워크플로우 속성에 정의된 시간대입니다([워크플로우 구축](../../automating/using/building-a-workflow.md) 참조).

## 쿼리 활동 만들기{#creating-a-query-activity}

1. In **[!UICONTROL Activities]** > **[!UICONTROL Targeting]**, to select recipients, drag and drop a [Query](../../automating/using/query.md) activity and double-click it.
1. **[!UICONTROL Shortcuts]** > **[!UICONTROL Profile]**&#x200B;에서 **[!UICONTROL Email]**&#x200B;을(를) 끌어다 놓습니다.
1. **[!UICONTROL is not empty]**&#x200B;을(를) 연산자로 선택합니다.
1. **[!UICONTROL Shortcuts]** > **[!UICONTROL General]**&#x200B;에서 프로필을 추가하고 **[!UICONTROL no longer contact by email]**&#x200B;을(를) **[!UICONTROL No]** 값으로 선택합니다.
1. **[!UICONTROL Confirm]**&#x200B;을(를) 클릭합니다.

![](assets/wf-complement-query.png)

## 이메일 게재 만들기{#creating-an-email-delivery}

1. > **[!UICONTROL Activities]** 에서 **[!UICONTROL Channels]**&#x200B;이메일 배달 [](../../automating/using/email-delivery.md) 활동을 드래그하여 놓습니다.
1. 활동을 클릭하고 편집하려면 ![](assets/edit_darkgrey-24px.png)을(를) 선택합니다.
1. **[!UICONTROL Recurring email]**&#x200B;을(를) 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다 .
1. 전자 메일 템플릿을 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.
1. 전자 메일 속성을 입력하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.
1. 전자 메일 레이아웃을 만들려면 **[!UICONTROL Use Email Designer]**&#x200B;을(를) 클릭합니다.
1. 요소를 삽입하거나 기존 템플릿을 선택합니다.
1. 필드 및 링크를 사용하여 이메일을 개인화합니다.
1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

자세한 내용은 [이메일 디자인](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch)을 참조하십시오.

**관련 항목:**

* [이메일 채널](../../channels/using/creating-an-email.md)
