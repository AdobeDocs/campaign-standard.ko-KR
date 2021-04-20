---
solution: Campaign Standard
product: campaign
title: 열지 않은 사용자 재타겟팅
description: 이 사용 사례는 오프너가 아닌 사용자를 다시 타깃팅하는 방법을 보여줍니다.
audience: automating
content-type: reference
topic-tags: execution-activities
context-tags: workflow,use-case,query,wait,delivery
feature: Workflows
role: Data Architect
level: Intermediate
translation-type: tm+mt
source-git-commit: 088b49931ee5047fa6b949813ba17654b1e10d60
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 38%

---


# 따개가 아닌 사람에게 새 배달을 보내는 작업 흐름 다시 타깃팅{#retargeting-delivery-to-non-openers}

고객에게 이메일을 보낸 다음 해당 메일을 열지 않은 고객에게 이메일을 보낼 수 있습니다.

1. **[!UICONTROL Marketing Activities]**&#x200B;에서 **[!UICONTROL Create]**&#x200B;을(를) 클릭하고 **[!UICONTROL Workflow]**&#x200B;을(를) 선택합니다.
1. 워크플로우 유형으로 **[!UICONTROL New Workflow]**&#x200B;을(를) 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.
1. 워크플로우의 속성을 입력하고 **[!UICONTROL Create]**&#x200B;을(를) 클릭합니다 .

## 쿼리 활동 만들기{#creating-a-query-activity}

1. **[!UICONTROL Activities]** > **[!UICONTROL Targeting]**&#x200B;에서 [쿼리](../../automating/using/query.md) 활동을 끌어다 놓습니다.
1. 활동을 두 번 클릭합니다.
1. **[!UICONTROL Shortcuts]**&#x200B;에서 **[!UICONTROL Profiles]**&#x200B;을(를) 드래그 앤 드롭하고 **[!UICONTROL is not empty]** 연산자와 함께 **[!UICONTROL email]**&#x200B;를 선택합니다.
1. **[!UICONTROL Shortcuts]**&#x200B;에서 **[!UICONTROL Profiles]**&#x200B;을(를) 드래그 앤 드롭하고 **[!UICONTROL no ]** 값으로 **[!UICONTROL no longer contact by email]**&#x200B;를 선택합니다.
1. **[!UICONTROL Confirm]**&#x200B;을(를) 클릭합니다.

![](assets/wf-complement-query.png)

## 이메일 게재 만들기{#creating-an-email-delivery}

1. 각 세그먼트 뒤에 [이메일 배달](../../automating/using/email-delivery.md)을 드래그하여 놓습니다.
1. 활동을 클릭하고 편집하려면 ![](assets/edit_darkgrey-24px.png)을(를) 선택합니다.
1. **[!UICONTROL Simple email]**&#x200B;을(를) 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다 .
1. **[!UICONTROL Add an outbound transition without the population]**&#x200B;을(를) 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다 .
1. 전자 메일 템플릿을 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.
1. 전자 메일 속성을 입력하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.
1. 전자 메일 레이아웃을 만들려면 **[!UICONTROL Using the Email Designer]**&#x200B;을(를) 클릭합니다.
1. 요소를 삽입하거나 기존 템플릿을 선택합니다.
1. 각 위치에 맞는 오퍼로 이메일을 개인화합니다. 자세한 내용은 [이메일](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch) 디자인을 참조하십시오.
1. 레이아웃을 확인하려면&#x200B;**[!UICONTROL Preview]**&#x200B;을(를) 클릭합니다.
1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

## 쿼리 활동에서 열개가 아닌 사용자를 타깃팅합니다{#targeting-non-openers-in-a-query-activity}

1. **[!UICONTROL Activities]** > **[!UICONTROL Execution]**&#x200B;에서 [Wait](../../automating/using/wait.md) 활동을 드래그하여 놓습니다.
1. **[!UICONTROL Duration]**&#x200B;에서 ![](assets/duration-icon.png)을 클릭하고 하루 중 하나를 선택합니다.
1. **[!UICONTROL Activities]** > **[!UICONTROL Targeting]**&#x200B;에서 **[!UICONTROL Query activity]**&#x200B;을(를) 끌어다 놓습니다.
1. 활동을 두 번 클릭합니다.
1. **[!UICONTROL Shortcuts]**&#x200B;에서 **[!UICONTROL Tracking Logs]** 연산자와 **[!UICONTROL exists]** 함께 드래그하여 놓습니다.
1. **[!UICONTROL Shortcuts]** **[!UICONTROL Delivery]**&#x200B;에서 **[!UICONTROL delivery]** 연산자를 사용하여 **[!UICONTROL is equal to]**&#x200B;을(를) 드래그하여 놓고 배달을 값으로 선택합니다.
1. **[!UICONTROL Shortcuts]** **[!UICONTROL Delivery]**&#x200B;에서 **[!UICONTROL type]**&#x200B;를 드래그하여 놓고 **[!UICONTROL Open]**&#x200B;을 값으로 선택합니다.
1. 규칙 사이의 연산자를 **[!UICONTROL except]**&#x200B;으로 선택합니다.
1. **[!UICONTROL Confirm]**&#x200B;을(를) 클릭합니다.

## sms 배달 만들기{#creating-a-sms-delivery}

1. 각 세그먼트 뒤에 sms 배달을 드래그하여 놓습니다.
1. 활동을 클릭하고 편집하려면 ![](assets/edit_darkgrey-24px.png)을(를) 선택합니다.
1. **[!UICONTROL Simple sms]**&#x200B;을(를) 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다 .
1. sms 템플릿을 선택하고 **[!UICONTROL Next]**&#x200B;을 클릭합니다.
1. sms 속성을 입력하고 **[!UICONTROL Next]**&#x200B;을 클릭합니다.
1. sms 레이아웃을 만들려면 **[!UICONTROL Email Designer]**&#x200B;을 클릭합니다.
1. 요소를 삽입하거나 기존 템플릿을 선택합니다.
1. 각 위치에 맞는 제안을 통해 SMS를 개인화할 수 있습니다.
자세한 내용은 [sms](../../channels/using/creating-an-sms-message.md) 디자인 섹션을 참조하십시오.
1. 레이아웃을 확인하려면&#x200B;**[!UICONTROL Preview]**&#x200B;을(를) 클릭합니다.
1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

![](assets/wf-retargeting-non-openers.png)

**관련 항목:**

* [이메일 채널](../../channels/using/creating-an-email.md)
