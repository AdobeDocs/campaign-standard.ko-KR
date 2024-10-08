---
title: 열지 않은 사용자 다시 타기팅하기
description: 이 사용 사례에서는 열지 않은 사용자를 다시 타겟팅하는 방법을 보여 줍니다.
audience: automating
content-type: reference
topic-tags: execution-activities
context-tags: workflow,use-case,query,wait,delivery
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: cba4e5c6-8acd-47a1-824e-14415e90d451
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 37%

---

# 열지 않은 사용자에게 새 게재를 보내는 워크플로우 재타겟팅{#retargeting-delivery-to-non-openers}

고객에게 이메일을 보낸 다음 메일을 열지 않은 고객에게 SMS를 보낼 수 있습니다.

1. **[!UICONTROL Marketing Activities]**&#x200B;에서 **[!UICONTROL Create]**&#x200B;을(를) 클릭하고 **[!UICONTROL Workflow]**&#x200B;을(를) 선택합니다.
1. 워크플로 유형으로 **[!UICONTROL New Workflow]**&#x200B;을(를) 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.
1. 워크플로의 속성을 입력하고 **[!UICONTROL Create]**&#x200B;을(를) 클릭합니다 .

## 쿼리 활동 만들기{#creating-a-query-activity}

1. **[!UICONTROL Activities]** > **[!UICONTROL Targeting]**&#x200B;에서 [쿼리](../../automating/using/query.md) 활동을 끌어다 놓습니다.
1. 활동을 두 번 클릭합니다.
1. **[!UICONTROL Shortcuts]**&#x200B;에서 **[!UICONTROL Profiles]**&#x200B;을(를) 끌어다 놓고 **[!UICONTROL is not empty]** 연산자로 **[!UICONTROL email]**&#x200B;을(를) 선택합니다.
1. **[!UICONTROL Shortcuts]**&#x200B;에서 **[!UICONTROL Profiles]**&#x200B;을(를) 끌어서 놓고 값이 **[!UICONTROL no]**&#x200B;인 **[!UICONTROL no longer contact by email]**&#x200B;을(를) 선택합니다.
1. **[!UICONTROL Confirm]**&#x200B;를 클릭합니다.

![](assets/wf-complement-query.png)

## 이메일 게재 만들기{#creating-an-email-delivery}

1. 각 세그먼트 뒤에 [전자 메일 게재](../../automating/using/email-delivery.md)을(를) 끌어다 놓습니다.
1. 활동을 클릭하고 편집하려면 ![](assets/edit_darkgrey-24px.png)을(를) 선택합니다.
1. **[!UICONTROL Simple email]**&#x200B;을(를) 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다 .
1. **[!UICONTROL Add an outbound transition without the population]**&#x200B;을(를) 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다 .
1. 전자 메일 템플릿을 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.
1. 전자 메일 속성을 입력하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.
1. 전자 메일 레이아웃을 만들려면 **[!UICONTROL Using the Email Designer]**&#x200B;을(를) 클릭합니다.
1. 요소를 삽입하거나 기존 템플릿을 선택합니다.
1. 각 위치에 맞는 오퍼를 사용하여 전자 메일을 개인화할 수 있습니다. 자세한 내용은 [전자 메일 디자인](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch)을 참조하세요.
1. 레이아웃을 확인하려면&#x200B;**[!UICONTROL Preview]**&#x200B;을(를) 클릭합니다.
1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

## 쿼리 활동에서 열지 않은 사용자 타겟팅{#targeting-non-openers-in-a-query-activity}

1. **[!UICONTROL Activities]** > **[!UICONTROL Execution]**&#x200B;에서 [대기](../../automating/using/wait.md) 활동을 끌어다 놓습니다.
1. **[!UICONTROL Duration]**&#x200B;에서 ![](assets/duration-icon.png)을(를) 클릭하고 하루를 선택하십시오.
1. **[!UICONTROL Activities]** > **[!UICONTROL Targeting]**&#x200B;에서 **[!UICONTROL Query activity]**&#x200B;을(를) 끌어다 놓습니다.
1. 활동을 두 번 클릭합니다.
1. **[!UICONTROL Shortcuts]**&#x200B;에서 연산자 **[!UICONTROL exists]**&#x200B;을(를) 사용하여 **[!UICONTROL Tracking Logs]**&#x200B;을(를) 끌어서 놓습니다.
1. **[!UICONTROL Shortcuts]**> **[!UICONTROL Delivery]**&#x200B;에서 연산자 **[!UICONTROL is equal to]**&#x200B;을(를) 사용하여 **[!UICONTROL delivery]**&#x200B;을(를) 끌어다 놓고 게재를 값으로 선택합니다.
1. **[!UICONTROL Shortcuts]**> **[!UICONTROL Delivery]**&#x200B;에서 **[!UICONTROL type]**&#x200B;을(를) 끌어서 놓고 **[!UICONTROL Open]**&#x200B;을(를) 값으로 선택합니다.
1. **[!UICONTROL except]**(으)로 규칙 사이의 연산자를 선택하십시오.
1. **[!UICONTROL Confirm]**&#x200B;를 클릭합니다.

## SMS 게재 만들기{#creating-a-sms-delivery}

1. 각 세그먼트 뒤에 SMS 게재를 끌어다 놓습니다.
1. 활동을 클릭하고 편집하려면 ![](assets/edit_darkgrey-24px.png)을(를) 선택합니다.
1. **[!UICONTROL Simple sms]**&#x200B;을(를) 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다 .
1. SMS 템플릿을 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.
1. SMS 속성을 입력하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.
1. SMS의 레이아웃을 만들려면 **[!UICONTROL Email Designer]**&#x200B;을(를) 클릭합니다.
1. 요소를 삽입하거나 기존 템플릿을 선택합니다.
1. 각 위치에 맞는 오퍼를 사용하여 SMS를 개인화할 수 있습니다.
자세한 내용은 [SMS 디자인](../../channels/using/creating-an-sms-message.md) 섹션을 참조하십시오.
1. 레이아웃을 확인하려면&#x200B;**[!UICONTROL Preview]**&#x200B;을(를) 클릭합니다.
1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

![](assets/wf-retargeting-non-openers.png)

**관련 항목:**

* [이메일 채널](../../channels/using/creating-an-email.md)
