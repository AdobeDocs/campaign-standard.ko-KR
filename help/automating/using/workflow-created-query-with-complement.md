---
solution: Campaign Standard
product: campaign
title: 보충 자료를 넣어 게재
description: 이 사용 사례에서는 보충으로 납품을 만드는 방법을 보여줍니다.
audience: automating
content-type: reference
topic-tags: execution-activities
context-tags: workflow,use-case,segmentation
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 41%

---


# 보충 자료를 넣어 게재 {#deliveries-with-complement}

고객에게 이메일을 보낼 수 있습니다.1년 전에 만든 클라이언트용 솔루션으로 1년 이상 전에 만든 클라이언트용 클라이언트용입니다.

1. **[!UICONTROL Marketing Activities]**&#x200B;에서 **[!UICONTROL Create]**&#x200B;을(를) 클릭하고 **[!UICONTROL Workflow]**&#x200B;을(를) 선택합니다.
1. 워크플로우 유형으로 **[!UICONTROL New Workflow]**&#x200B;을(를) 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.
1. 워크플로우의 속성을 입력하고 **[!UICONTROL Create]**&#x200B;을(를) 클릭합니다.

## Create a Query activity {#create-a-query-activity}

1. **[!UICONTROL Activities]** > **[!UICONTROL Targeting]**&#x200B;에서 [쿼리](../../automating/using/query.md) 활동을 끌어다 놓습니다.
1. 활동을 두 번 클릭합니다.
1. In **[!UICONTROL Shortcuts]**, drag and drop **[!UICONTROL Profiles]** and select **[!UICONTROL email]** with the operator **[!UICONTROL is not empty]**.
1. In **[!UICONTROL Shortcuts]**, drag and drop **[!UICONTROL Profiles]** and select **[!UICONTROL no longer contact by email]** with the value **[!UICONTROL no]**.
1. **[!UICONTROL Confirm]**&#x200B;을(를) 클릭합니다.

![](assets/wf-complement-query.png)

## Create a Segmentation activity {#create-a-segmentation-activity}

1. In **[!UICONTROL Activities]** > **[!UICONTROL Targeting]**, drag and drop a [Segmentation](../../automating/using/segmentation.md) activity and double-click it.
1. 세그먼트 위로 마우스를 가져간 다음 을 클릭하여 데이터베이스에 올해 추가된 고객 ![](assets/edit_darkgrey-24px.png) 을 타깃팅합니다.
1. Drag and drop **[!UICONTROL Profiles]** and select **[!UICONTROL Created]** with the filter type **[!UICONTROL Relative]**.
1. Change the **[!UICONTROL Level of precision]** to **[!UICONTROL Year]** and select **[!UICONTROL This year]**.
1. **[!UICONTROL Confirm]**&#x200B;을(를) 두 번 클릭합니다.
1. 에서 **[!UICONTROL Advanced Options]**&#x200B;나머지 받는 사람 **[!UICONTROL Generate complement]** 을 대상으로 하는 세그먼트를 만들려면 을 선택합니다.
1. **[!UICONTROL Confirm]**&#x200B;을(를) 클릭합니다.
1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

![](assets/wf-complement-segmentation.png)

>[!NOTE]
>
>규칙의 구조를 관찰하려면 을 클릭합니다 **[!UICONTROL Advanced Mode]**.

## 이메일 게재 만들기 {#create-an-email-delivery}

1. > **[!UICONTROL Activities]** 에서 **[!UICONTROL Channels]**&#x200B;각 세그먼트 뒤에 [이메일 배달](../../automating/using/email-delivery.md) 활동을 드래그하여 놓습니다.
1. 활동을 클릭하고 편집하려면 ![](assets/edit_darkgrey-24px.png)을(를) 선택합니다.
1. **[!UICONTROL Single send email]**&#x200B;을(를) 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다 .
1. 전자 메일 템플릿을 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.
1. 전자 메일 속성을 입력하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.
1. 전자 메일 레이아웃을 만들려면 **[!UICONTROL Email Designer]**&#x200B;을(를) 클릭합니다.
1. 요소를 삽입하거나 기존 템플릿을 선택합니다.
1. 각 전달에 맞는 제안을 통해 이메일을 개인화할 수 있습니다.
1. 레이아웃을 확인하려면&#x200B;**[!UICONTROL Preview]**&#x200B;을(를) 클릭합니다.
1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

자세한 내용은 [이메일 디자인](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch)을 참조하십시오.

![](assets/wf-deliveries-with-a-complement.png)
