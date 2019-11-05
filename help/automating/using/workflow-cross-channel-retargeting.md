---
title: '"워크플로우 사용 사례:비열기 다시 타깃팅"'
description: '"워크플로우 사용 사례:비열기 다시 타깃팅"'
page-status-flag: 활성화 안 함
uuid: 396a3de1-6ffa-4385-ac9f-15fdeae5a366
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 자동화
content-type: reference
topic-tags: 실행 활동
discoiquuid: 377821e6-69f8-41cc-a1ad-8a2f5ed4d409
context-tags: '워크플로,사용 사례,쿼리,대기,전달 '
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 워크플로우 사용 사례:비열기 사용자에게 새 배달을 보내는 다시 타깃팅 워크플로우{#retargeting-delivery-to-non-openers}

고객에게 이메일을 보낸 다음 해당 메일을 열지 않은 고객에게 이메일을 보낼 수 있습니다.

1. 에서 **[!UICONTROL Marketing Activities]**&#x200B;을 클릭하고 **[!UICONTROL Create]** 선택합니다 **[!UICONTROL Workflow]**.
1. 워크플로우 **[!UICONTROL New Workflow]** 유형으로 선택하고 을 클릭합니다 **[!UICONTROL Next]**.
1. 워크플로우의 속성을 입력하고 을 클릭합니다 **[!UICONTROL Create]**.

## 쿼리 활동 만들기{#creating-a-query-activity}

1. &gt; **[!UICONTROL Activities]** 에서 **[!UICONTROL Targeting]**&#x200B;드래그하여 **[!UICONTROL Query activity]** ![](assets/query.png)놓습니다.
1. 활동을 두 번 클릭합니다.
1. 에서 **[!UICONTROL Shortcuts]**&#x200B;드래그하여 **[!UICONTROL Profiles]** 놓고 연산자로 **[!UICONTROL email]** 선택합니다 **[!UICONTROL is not empty]**.
1. 에서 **[!UICONTROL Shortcuts]**&#x200B;드래그하여 **[!UICONTROL Profiles]** 놓고 값을 **[!UICONTROL no longer contact by email]** 사용하여 선택합니다 **[!UICONTROL no ]**.
1. Click **[!UICONTROL Confirm]**.

![](assets/wf-complement-query.png)

## 이메일 배달 만들기{#creating-an-email-delivery}

1. 각 세그먼트 **[!UICONTROL Email delivery]** 뒤에 드래그하여 놓습니다.
1. 활동을 클릭하고 ![](assets/edit_darkgrey-24px.png) 편집하려면 선택합니다.
1. 을 선택하고 **[!UICONTROL Simple email]** 클릭합니다 **[!UICONTROL Next]**.
1. 을 선택하고 **[!UICONTROL Add an outbound transition without the population]** 클릭합니다 **[!UICONTROL Next]**.
1. 이메일 템플릿을 선택하고 을 **[!UICONTROL Next]**&#x200B;클릭합니다.
1. 이메일 속성을 입력하고 을 **[!UICONTROL Next]**&#x200B;클릭합니다.
1. 이메일 레이아웃을 만들려면 을 클릭합니다 **[!UICONTROL Using the Email Designer]**.
1. 요소를 삽입하거나 기존 템플릿을 선택합니다.
1. 각 위치에 맞는 오퍼로 이메일을 개인화합니다.자세한 내용은 이메일 [디자인을 참조하십시오](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch).
1. 레이아웃을 **[!UICONTROL Preview]** 확인하려면 클릭합니다.
1. Click **[!UICONTROL Save]**.

## 쿼리 활동에서 비열기 타깃팅{#targeting-non-openers-in-a-query-activity}

1. &gt; **[!UICONTROL Activities]** 에서 **[!UICONTROL Execution]**&#x200B;드래그하여 **[!UICONTROL Wait activity]** ![](assets/wait.png)놓습니다.
1. 에서 **[!UICONTROL Duration]**&#x200B;을 클릭하고 ![](assets/duration-icon.png) 하루를 선택합니다.
1. &gt; **[!UICONTROL Activities]** 에서 **[!UICONTROL Targeting]**&#x200B;드래그하여 **[!UICONTROL Query activity]** ![](assets/query.png)놓습니다.
1. 활동을 두 번 클릭합니다.
1. 에서 **[!UICONTROL Shortcuts]**&#x200B;드래그하여 **[!UICONTROL Tracking Logs]** 놓고 연산자를 사용합니다 **[!UICONTROL exists]**.
1. &gt; **[!UICONTROL Shortcuts]**&#x200B;에서 연산자와 **[!UICONTROL Delivery]**&#x200B;함께 드래그하여 놓고 배달을 값으로 **[!UICONTROL delivery]** **[!UICONTROL is equal to]** 선택합니다.
1. &gt; **[!UICONTROL Shortcuts]****[!UICONTROL Delivery]**&#x200B;에서 드래그 앤 드롭 **[!UICONTROL type]** 및 값으로 **[!UICONTROL Open]** 확인합니다.
1. 규칙 사이의 연산자를 로 **[!UICONTROL except]**&#x200B;선택합니다.
1. Click **[!UICONTROL Confirm]**.

## SMS 배달 만들기{#creating-a-sms-delivery}

1. 각 세그먼트 뒤에 SMS를 드래그하여 놓을 수 있습니다.
1. 활동을 클릭하고 ![](assets/edit_darkgrey-24px.png) 편집하려면 선택합니다.
1. 을 선택하고 **[!UICONTROL Simple sms]** 클릭합니다 **[!UICONTROL Next]**.
1. sms 템플릿을 선택하고 을 클릭합니다 **[!UICONTROL Next]**.
1. sms 속성을 입력하고 을 클릭합니다 **[!UICONTROL Next]**.
1. sms의 레이아웃을 만들려면 을 클릭합니다 **[!UICONTROL Email Designer]**.
1. 요소를 삽입하거나 기존 템플릿을 선택합니다.
1. 각 위치별 오퍼를 통해 SMS를 개인화할 수 있습니다.
자세한 내용은 sms [디자인을 참조하십시오](../../channels/using/creating-an-sms-message.md).
1. 레이아웃을 **[!UICONTROL Preview]** 확인하려면 클릭합니다.
1. Click **[!UICONTROL Save]**.

![](assets/wf-retargeting-non-openers.png)

**관련 항목:**

* [쿼리](../../automating/using/query.md)
* [SMS 게재](../../automating/using/sms-delivery.md)
* [이메일 게재](../../automating/using/email-delivery.md)
* [이메일 채널](../../channels/using/creating-an-email.md)
