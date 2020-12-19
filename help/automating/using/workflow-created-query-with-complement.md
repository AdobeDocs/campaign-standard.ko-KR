---
solution: Campaign Standard
product: campaign
title: 보충 자료를 넣어 게재
description: 이 사용 사례는 보완으로 납품을 만드는 방법을 보여줍니다.
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

고객에게 이메일을 보낼 수 있습니다.1년 전에 만들어진 클라이언트용이고 1년 이상 전에 제작한 클라이언트용입니다.

1. **[!UICONTROL Marketing Activities]**&#x200B;에서 **[!UICONTROL Create]**&#x200B;을(를) 클릭하고 **[!UICONTROL Workflow]**&#x200B;을(를) 선택합니다.
1. 워크플로우 유형으로 **[!UICONTROL New Workflow]**&#x200B;을(를) 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.
1. 워크플로우의 속성을 입력하고 **[!UICONTROL Create]**&#x200B;을(를) 클릭합니다.

## 쿼리 활동 {#create-a-query-activity} 만들기

1. **[!UICONTROL Activities]** > **[!UICONTROL Targeting]**&#x200B;에서 [쿼리](../../automating/using/query.md) 활동을 끌어다 놓습니다.
1. 활동을 두 번 클릭합니다.
1. **[!UICONTROL Shortcuts]**&#x200B;에서 **[!UICONTROL Profiles]**&#x200B;을(를) 드래그 앤 드롭하고 **[!UICONTROL is not empty]** 연산자와 함께 **[!UICONTROL email]**&#x200B;를 선택합니다.
1. **[!UICONTROL Shortcuts]**&#x200B;에서 **[!UICONTROL Profiles]**&#x200B;을(를) 드래그 앤 드롭하고 **[!UICONTROL no]** 값으로 **[!UICONTROL no longer contact by email]**&#x200B;를 선택합니다.
1. **[!UICONTROL Confirm]**&#x200B;을(를) 클릭합니다.

![](assets/wf-complement-query.png)

## 세그멘테이션 활동 {#create-a-segmentation-activity} 만들기

1. **[!UICONTROL Activities]** > **[!UICONTROL Targeting]**&#x200B;에서 [세그멘테이션](../../automating/using/segmentation.md) 활동을 드래그하여 놓고 두 번 클릭합니다.
1. 세그먼트 위로 마우스를 가져간 다음 ![](assets/edit_darkgrey-24px.png)을 클릭하여 데이터베이스에 올해 추가된 고객을 타깃팅합니다.
1. **[!UICONTROL Profiles]**&#x200B;을(를) 드래그 앤 드롭하고 필터 유형이 **[!UICONTROL Relative]**&#x200B;인 **[!UICONTROL Created]**&#x200B;을 선택합니다.
1. **[!UICONTROL Level of precision]**&#x200B;을 **[!UICONTROL Year]**&#x200B;으로 변경하고 **[!UICONTROL This year]**&#x200B;를 선택합니다.
1. **[!UICONTROL Confirm]**&#x200B;을(를) 두 번 클릭합니다.
1. **[!UICONTROL Advanced Options]**&#x200B;에서 **[!UICONTROL Generate complement]**&#x200B;을 선택하여 나머지 받는 사람을 대상으로 하는 세그먼트를 만듭니다.
1. **[!UICONTROL Confirm]**&#x200B;을(를) 클릭합니다.
1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

![](assets/wf-complement-segmentation.png)

>[!NOTE]
>
>규칙 구조를 관찰하려면 **[!UICONTROL Advanced Mode]**&#x200B;을 클릭합니다.

## 이메일 게재 만들기 {#create-an-email-delivery}

1. **[!UICONTROL Activities]** > **[!UICONTROL Channels]**&#x200B;에서 각 세그먼트 뒤에 [이메일 배달](../../automating/using/email-delivery.md) 활동을 드래그하여 놓습니다.
1. 활동을 클릭하고 편집하려면 ![](assets/edit_darkgrey-24px.png)을(를) 선택합니다.
1. **[!UICONTROL Single send email]**&#x200B;을(를) 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다 .
1. 전자 메일 템플릿을 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.
1. 전자 메일 속성을 입력하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.
1. 전자 메일 레이아웃을 만들려면 **[!UICONTROL Email Designer]**&#x200B;을(를) 클릭합니다.
1. 요소를 삽입하거나 기존 템플릿을 선택합니다.
1. 각 전달에 적합한 오퍼로 이메일을 개인화합니다.
1. 레이아웃을 확인하려면&#x200B;**[!UICONTROL Preview]**&#x200B;을(를) 클릭합니다.
1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

자세한 내용은 [이메일 디자인](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch)을 참조하십시오.

![](assets/wf-deliveries-with-a-complement.png)
