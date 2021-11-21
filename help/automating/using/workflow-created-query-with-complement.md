---
title: 보충 자료를 넣어 게재
description: 이 사용 사례에서는 보충 자료로 게재를 만드는 방법을 보여줍니다.
audience: automating
content-type: reference
topic-tags: execution-activities
context-tags: workflow,use-case,segmentation
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: 5cd71e07-f955-4c15-bdfb-14b0daccec1a
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 41%

---

# 보충 자료를 넣어 게재 {#deliveries-with-complement}

고객에게 이메일을 보낼 수 있습니다. 1년 전에 만들어진 클라이언트용 1개, 1년 이상 전에 생성된 클라이언트용 1개.

1. **[!UICONTROL Marketing Activities]**&#x200B;에서 **[!UICONTROL Create]**&#x200B;을(를) 클릭하고 **[!UICONTROL Workflow]**&#x200B;을(를) 선택합니다.
1. 워크플로우 유형으로 **[!UICONTROL New Workflow]**&#x200B;을(를) 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.
1. 워크플로우의 속성을 입력하고 **[!UICONTROL Create]**&#x200B;을(를) 클릭합니다.

## 쿼리 활동 만들기 {#create-a-query-activity}

1. **[!UICONTROL Activities]** > **[!UICONTROL Targeting]**&#x200B;에서 [쿼리](../../automating/using/query.md) 활동을 끌어다 놓습니다.
1. 활동을 두 번 클릭합니다.
1. in **[!UICONTROL Shortcuts]**, 드래그 앤 드롭 **[!UICONTROL Profiles]** 을(를) 선택합니다. **[!UICONTROL email]** 연산자 사용 **[!UICONTROL is not empty]**.
1. in **[!UICONTROL Shortcuts]**, 드래그 앤 드롭 **[!UICONTROL Profiles]** 을(를) 선택합니다. **[!UICONTROL no longer contact by email]** 값 사용 **[!UICONTROL no]**.
1. **[!UICONTROL Confirm]**&#x200B;를 클릭합니다.

![](assets/wf-complement-query.png)

## 세분화 활동 만들기 {#create-a-segmentation-activity}

1. in **[!UICONTROL Activities]** > **[!UICONTROL Targeting]**, 드래그 앤 드롭 [세그먼테이션](../../automating/using/segmentation.md) 활동을 두 번 클릭하고 클릭합니다.
1. 마우스를 세그먼트 위로 가져간 다음 을(를) 클릭합니다. ![](assets/edit_darkgrey-24px.png) 데이터베이스에 올해 추가된 고객을 대상으로 합니다.
1. 드래그 앤 드롭 **[!UICONTROL Profiles]** 을(를) 선택합니다. **[!UICONTROL Created]** 필터 유형 사용 **[!UICONTROL Relative]**.
1. 변경 **[!UICONTROL Level of precision]** to **[!UICONTROL Year]** 을(를) 선택합니다. **[!UICONTROL This year]**.
1. **[!UICONTROL Confirm]**&#x200B;을(를) 두 번 클릭합니다.
1. in **[!UICONTROL Advanced Options]**, check **[!UICONTROL Generate complement]** 나머지 수신자를 타겟팅하는 세그먼트를 만들려면
1. **[!UICONTROL Confirm]**&#x200B;를 클릭합니다.
1. **[!UICONTROL Save]**&#x200B;를 클릭합니다.

![](assets/wf-complement-segmentation.png)

>[!NOTE]
>
>규칙 구조를 관찰하려면 **[!UICONTROL Advanced Mode]**.

## 이메일 게재 만들기 {#create-an-email-delivery}

1. in **[!UICONTROL Activities]** > **[!UICONTROL Channels]**, 드래그 앤 드롭 [이메일 게재](../../automating/using/email-delivery.md) 활동은 각 세그먼트 뒤에 표시됩니다.
1. 활동을 클릭하고 편집하려면 ![](assets/edit_darkgrey-24px.png)을(를) 선택합니다.
1. **[!UICONTROL Single send email]**&#x200B;을(를) 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다 .
1. 전자 메일 템플릿을 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.
1. 전자 메일 속성을 입력하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.
1. 전자 메일 레이아웃을 만들려면 **[!UICONTROL Email Designer]**&#x200B;을(를) 클릭합니다.
1. 요소를 삽입하거나 기존 템플릿을 선택합니다.
1. 각 게재와 관련된 오퍼로 이메일을 개인화합니다.
1. 레이아웃을 확인하려면&#x200B;**[!UICONTROL Preview]**&#x200B;을(를) 클릭합니다.
1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

자세한 내용은 [이메일 디자인](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch)을 참조하십시오.

![](assets/wf-deliveries-with-a-complement.png)
