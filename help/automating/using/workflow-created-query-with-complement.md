---
title: 보충 자료를 넣어 게재
description: 이 사용 사례에서는 보충으로 납품을 만드는 방법을 보여줍니다.
page-status-flag: never-activated
uuid: 396a3de1-6ffa-4385-ac9f-15fdeae5a366
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities
discoiquuid: 377821e6-69f8-41cc-a1ad-8a2f5ed4d409
context-tags: workflow,use-case,segmentation
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 87e0611fae0560aca276caa3c4cf793e9c095d72
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 5%

---


# 보충 자료를 넣어 게재 {#deliveries-with-complement}

고객에게 이메일을 보낼 수 있습니다. 1년 전에 만든 클라이언트용 솔루션으로 1년 이상 전에 만든 클라이언트용 클라이언트용입니다.

1. 에서 **[!UICONTROL Marketing Activities]**&#x200B;을 클릭하고 **[!UICONTROL Create]** 선택합니다 **[!UICONTROL Workflow]**.
1. 워크플로우 유형 **[!UICONTROL New Workflow]** 으로 선택하고 을 클릭합니다 **[!UICONTROL Next]**.
1. 워크플로우의 속성을 입력하고 를 클릭합니다 **[!UICONTROL Create]**.

## 쿼리 활동 만들기 {#create-a-query-activity}

1. > **[!UICONTROL Activities]** 에서 **[!UICONTROL Targeting]**&#x200B;쿼리 활동을 끌어다 [놓습니다](../../automating/using/query.md) .
1. 활동을 두 번 클릭합니다.
1. 에서 **[!UICONTROL Shortcuts]**&#x200B;드래그하여 **[!UICONTROL Profiles]** 놓고 연산자로 **[!UICONTROL email]** 선택합니다 **[!UICONTROL is not empty]**.
1. 에서 **[!UICONTROL Shortcuts]**&#x200B;드래그하여 **[!UICONTROL Profiles]** 놓고 값을 **[!UICONTROL no longer contact by email]** 사용하여 선택합니다 **[!UICONTROL no]**.
1. **[!UICONTROL Confirm]**&#x200B;을 클릭합니다.

![](assets/wf-complement-query.png)

## 세그멘테이션 활동 만들기 {#create-a-segmentation-activity}

1. > **[!UICONTROL Activities]** 에서 **[!UICONTROL Targeting]**&#x200B;세그멘테이션 [](../../automating/using/segmentation.md) 활동을 드래그하여 놓고 두 번 클릭합니다.
1. 세그먼트 위로 마우스를 가져간 다음 을 클릭하여 데이터베이스에 올해 추가된 고객 ![](assets/edit_darkgrey-24px.png) 을 타깃팅합니다.
1. 드래그 앤 드롭 **[!UICONTROL Profiles]** 을 통해 필터 유형 **[!UICONTROL Created]** 을 선택합니다 **[!UICONTROL Relative]**.
1. 을 **[!UICONTROL Level of precision]** 변경하고 **[!UICONTROL Year]** 선택합니다 **[!UICONTROL This year]**.
1. 두 **[!UICONTROL Confirm]** 번 클릭합니다.
1. 에서 **[!UICONTROL Advanced Options]**&#x200B;나머지 받는 사람 **[!UICONTROL Generate complement]** 을 대상으로 하는 세그먼트를 만들려면 을 선택합니다.
1. **[!UICONTROL Confirm]**&#x200B;을 클릭합니다.
1. **[!UICONTROL Save]**&#x200B;을 클릭합니다.

![](assets/wf-complement-segmentation.png)

>[!NOTE]
>
>규칙의 구조를 관찰하려면 을 클릭합니다 **[!UICONTROL Advanced Mode]**.

## 이메일 배달 만들기 {#create-an-email-delivery}

1. > **[!UICONTROL Activities]** 에서 **[!UICONTROL Channels]**&#x200B;각 세그먼트 뒤에 [이메일 배달](../../automating/using/email-delivery.md) 활동을 드래그하여 놓습니다.
1. 활동을 클릭하고 ![](assets/edit_darkgrey-24px.png) 편집하려면 선택합니다.
1. 을 선택하고 **[!UICONTROL Single send email]** 클릭합니다 **[!UICONTROL Next]**.
1. 이메일 템플릿을 선택하고 을 클릭합니다 **[!UICONTROL Next]**.
1. 이메일 속성을 입력하고 을 클릭합니다 **[!UICONTROL Next]**.
1. 이메일 레이아웃을 만들려면 을 클릭합니다 **[!UICONTROL Email Designer]**.
1. 요소를 삽입하거나 기존 템플릿을 선택합니다.
1. 각 전달에 맞는 제안을 통해 이메일을 개인화할 수 있습니다.
1. 레이아웃 **[!UICONTROL Preview]** 을 확인하려면 을(를) 클릭합니다.
1. **[!UICONTROL Save]**&#x200B;을 클릭합니다.

자세한 내용은 이메일 [디자인을 참조하십시오](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch).

![](assets/wf-deliveries-with-a-complement.png)
