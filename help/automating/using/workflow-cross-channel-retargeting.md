---
title: '" 워크플로우 사용 사례: 리타겟팅되지 않은 리타겟팅 "'
seo-title: '" 워크플로우 사용 사례: 리타겟팅되지 않은 리타겟팅 "'
description: '" 워크플로우 사용 사례: 리타겟팅되지 않은 리타겟팅 "'
seo-description: '" 워크플로우 사용 사례: 리타겟팅되지 않은 리타겟팅 "'
page-status-flag: 정품 인증 안 함
uuid: 396 a 3 de 1-6 ffa -4385-ac 9 f -15 fdeae 5 a 366
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 실행 활동
discoiquuid: 377821 E 6-69 F 8-41 CC-A 1 AD -8 A 2 F 5 ED 4 D 409
context-tags: '워크플로우, 사용 사례, 쿼리, 대기, 전달 '
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 035726bbd3112058b9a89525a861521bc3b9867e

---


# 워크플로우 사용 사례: 새 배달을 오프닝으로 전송하는 재타깃팅 워크플로우{#retargeting-delivery-to-non-openers}

고객에게 이메일을 보낸 다음 이메일을 열지 않은 사용자에게 SMS를 보낼 수 있습니다.

1. 에서 **[!UICONTROL Marketing Activities]****[!UICONTROL Create]****[!UICONTROL Workflow]**&#x200B;를 클릭하고 선택합니다.
1. 워크플로우 유형으로 선택하고 **[!UICONTROL New Workflow]** 를 **[!UICONTROL Next]**&#x200B;클릭합니다.
1. 워크플로우의 속성을 입력하고 **[!UICONTROL Create]**&#x200B;를 클릭합니다.

## 쿼리 활동 만들기{#creating-a-query-activity}

1. 에서 **[!UICONTROL Activities]** , A를 **[!UICONTROL Targeting]**&#x200B;드래그하여 놓습니다 **[!UICONTROL Query activity]**![](assets/query.png).
1. 활동을 두 번 클릭합니다.
1. 에서 **[!UICONTROL Shortcuts]**&#x200B;연산자로 드래그하여 놓은 **[!UICONTROL Profiles]****[!UICONTROL email]****[!UICONTROL is not empty]**&#x200B;다음 선택합니다.
1. 에서 **[!UICONTROL Shortcuts]**&#x200B;값을 드래그하여 놓고 **[!UICONTROL Profiles]** 선택합니다 **[!UICONTROL no longer contact by email]****[!UICONTROL no ]**.
1. **[!UICONTROL Confirm]**&#x200B;을 클릭합니다.

![](assets/wf-complement-query.png)

## 이메일 배달 만들기{#creating-an-email-delivery}

1. 각 세그먼트 다음에****[!UICONTROL Email delivery]이메일 배달을 드래그하여 놓습니다.
1. 활동을 클릭하고 ![](assets/edit_darkgrey-24px.png) 편집을 선택합니다.
1. **[!UICONTROL Simple email]****[!UICONTROL Next]**&#x200B;을 선택하고 클릭합니다.
1. **[!UICONTROL Add an outbound transition without the population]****[!UICONTROL Next]**&#x200B;을 선택하고 클릭합니다.
1. 이메일 템플릿을 선택하고 **[!UICONTROL Next]**&#x200B;를 클릭합니다.
1. 이메일 속성을 입력하고 **[!UICONTROL Next]**&#x200B;를 클릭합니다.
1. 이메일의 레이아웃을 만들려면 **[!UICONTROL Using the Email Designer]**&#x200B;을 클릭합니다.
1. 요소를 삽입하거나 기존 템플릿을 선택합니다.
1. 각 위치에 맞는 제안을 이메일로 개인화할 수 있습니다. 자세한 내용은 이메일 [디자인을](../../designing/using/about-email-content-design.md#designing-an-email-content-from-scratch)참조하십시오.
1. 레이아웃을 **[!UICONTROL Preview]** 확인하려면을 클릭합니다.
1. **[!UICONTROL Save]**&#x200B;을 클릭합니다.

## 쿼리 활동에서 오프닝되지 않은 타깃팅 타깃팅{#targeting-non-openers-in-a-query-activity}

1. 에서 **[!UICONTROL Activities]** , A를 **[!UICONTROL Execution]**&#x200B;드래그하여 놓습니다 **[!UICONTROL Wait activity]**![](assets/wait.png).
1. 에서 **[!UICONTROL Duration]**&#x200B;를 클릭하고 ![](assets/duration-icon.png) 하루를 선택합니다.
1. 에서 **[!UICONTROL Activities]** , A를 **[!UICONTROL Targeting]**&#x200B;드래그하여 놓습니다 **[!UICONTROL Query activity]**![](assets/query.png).
1. 활동을 두 번 클릭합니다.
1. in **[!UICONTROL Shortcuts]**, drag and drop **[!UICONTROL Tracking Logs]** and with the operator **[!UICONTROL exists]**.
1. &gt; **[!UICONTROL Shortcuts]****[!UICONTROL Delivery]**&#x200B;연산자를 **[!UICONTROL delivery]****[!UICONTROL is equal to]** 사용하여 드래그하여 놓고 배달을 값으로 선택합니다.
1. [시작] **[!UICONTROL Shortcuts]**&gt; **[!UICONTROL Delivery]**[드래그 앤 드롭 **[!UICONTROL type]** ] 를 클릭하고 [값 **[!UICONTROL Open]** ] 로 확인합니다.
1. 규칙 간에 연산자를 선택합니다 **[!UICONTROL except]**.
1. **[!UICONTROL Confirm]**&#x200B;을 클릭합니다.

## SMS 배달 만들기{#creating-a-sms-delivery}

1. 각 세그먼트 이후에 SMS 배달을 드래그하여 놓습니다.
1. 활동을 클릭하고 ![](assets/edit_darkgrey-24px.png) 편집을 선택합니다.
1. **[!UICONTROL Simple sms]****[!UICONTROL Next]**&#x200B;을 선택하고 클릭합니다.
1. SMS 템플릿을 선택하고 **[!UICONTROL Next]**&#x200B;를 클릭합니다.
1. SMS 속성을 입력하고 **[!UICONTROL Next]**&#x200B;를 클릭합니다.
1. SMS 레이아웃을 만들려면 **[!UICONTROL Email Designer]**&#x200B;을 클릭합니다.
1. 요소를 삽입하거나 기존 템플릿을 선택합니다.
1. 각 위치에 특화된 오퍼를 사용하여 SMS를 개인화할 수 있습니다.
자세한 내용은 SMS [디자인을](../../channels/using/creating-an-sms-message.md)참조하십시오.
1. 레이아웃을 **[!UICONTROL Preview]** 확인하려면을 클릭합니다.
1. **[!UICONTROL Save]**&#x200B;을 클릭합니다.

![](assets/wf-retargeting-non-openers.png)

**관련 항목:**

* [쿼리](../../automating/using/query.md)
* [SMS 배달](../../automating/using/sms-delivery.md)
* [이메일 배달](../../automating/using/email-delivery.md)
* [이메일 채널](../../channels/using/creating-an-email.md)
