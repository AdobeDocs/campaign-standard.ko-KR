---
solution: Campaign Standard
product: campaign
title: 위치 세분화"
description: 이 사용 사례에서는 위치에서 세그먼테이션을 수행하는 방법을 보여줍니다.
audience: automating
content-type: reference
topic-tags: execution-activities
context-tags: workflow,use-case,query,segmentation,delivery
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 83%

---


# 위치 세분화 {#segmentation-on-location}

해당 지역 상점의 오퍼를 제공하는 타겟팅 이메일을 고객에게 보낼 수 있습니다.

1. **[!UICONTROL Marketing Activities]**&#x200B;에서 **[!UICONTROL Create]**&#x200B;을(를) 클릭하고 **[!UICONTROL Workflow]**&#x200B;을(를) 선택합니다.
1. 워크플로우 유형으로 **[!UICONTROL New Workflow]**&#x200B;을(를) 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.
1. 워크플로우의 속성을 입력하고 **[!UICONTROL Create]**&#x200B;을(를) 클릭합니다 .

## 전자 메일을 통해 연결 가능한 수신자 선택{#selecting-recipients-contactable-via-email}

1. In **[!UICONTROL Activities]** > **[!UICONTROL Targeting]**, drag and drop a [Query](../../automating/using/query.md) activity ![](assets/query.png).
1. 활동을 두 번 클릭합니다.
1. **[!UICONTROL Shortcuts]**&#x200B;에서 **[!UICONTROL Profiles]**&#x200B;을(를) 끌어다 놓고 **[!UICONTROL is not empty]** 연산자가 있는 **[!UICONTROL email]** 필드를 선택합니다 .
1. **[!UICONTROL Shortcuts]**&#x200B;에서 **[!UICONTROL Profiles]**&#x200B;을(를) 끌어다 놓고 **[!UICONTROL no]**&#x200B;값이 있는 **[!UICONTROL no longer contact by email]** 필드를 선택합니다 .
1. **[!UICONTROL Confirm]**&#x200B;을(를) 두 번 클릭합니다.

![](assets/wf-complement-query.png)

## 세분화 활동 만들기{#creating-a-segmentation-activity}

1. Drag and drop a [Segmentation](../../automating/using/segmentation.md) activity and double-click it.
1. 세그먼트를 클릭한 다음 첫 번째 도시의 사용자를 타겟팅하기 위해 전환을 엽니다. 보스턴입니다.
1. **[!UICONTROL Location]**&#x200B;을(를) 끌어다 놓고 연산자 **[!UICONTROL equals to]**&#x200B;와(과) 값 **[!UICONTROL Boston]**(으)로 **[!UICONTROL City]**을(를) 선택합니다. 
참고: 보스턴에 들어온 모든 사람과 연결하려면 대/소문자 구분 옵션의 선택을 취소하십시오.
1. **[!UICONTROL Confirm]**&#x200B;을(를) 클릭합니다.
1. **[!UICONTROL List of outbound segments]**&#x200B;에서 **[!UICONTROL Add an element]**&#x200B;을(를) 클릭하고 ![](assets/edit_darkgrey-24px.png)을(를) 클릭하여 두 번째 도시의 사용자를 타겟팅하는 세그먼트를 만듭니다. 시카고입니다.
1. **[!UICONTROL Location]**&#x200B;을(를) 끌어다 놓고 **[!UICONTROL equals to]** 연산자로 **[!UICONTROL City]**&#x200B;을(를) 선택하고 값 **[!UICONTROL Chicago]**&#x200B;을(를) 입력합니다.
1. 시카고에 들어온 모든 사람과 연결하려면 대/소문자 구분 옵션의 선택을 취소하십시오.
1. **[!UICONTROL Confirm]**&#x200B;을(를) 클릭합니다.

## 이메일 게재 만들기{#creating-an-email-delivery}

1. > **[!UICONTROL Activities]** 에서 **[!UICONTROL Channels]**&#x200B;각 세그먼트 뒤에 [이메일 배달](../../automating/using/email-delivery.md) 활동을 드래그하여 놓습니다.
1. 활동을 클릭하고 편집하려면 ![](assets/edit_darkgrey-24px.png)을(를) 선택합니다.
1. **[!UICONTROL Simple email]**&#x200B;을(를) 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다 .
1. 전자 메일 템플릿을 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.
1. 전자 메일 속성을 입력하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.
1. 전자 메일 레이아웃을 만들려면 **[!UICONTROL Email Designer]**&#x200B;을(를) 클릭합니다.
1. 요소를 삽입하거나 기존 템플릿을 선택합니다.
1. 각 위치에 맞는 제안을 통해 전자 메일을 개인화할 수 있습니다.

   자세한 내용은 [전자 메일 디자인](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch)을 참조하십시오.

1. 레이아웃을 확인하려면&#x200B;**[!UICONTROL Preview]**&#x200B;을(를) 클릭합니다.
1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

![](assets/wf-segmentation-location.png)

