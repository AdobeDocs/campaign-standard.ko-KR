---
title: '" 워크플로우 사용 사례: 세그멘테이션의 세그멘테이션 "'
seo-title: '" 워크플로우 사용 사례: 세그멘테이션의 세그멘테이션 "'
description: '" 워크플로우 사용 사례: 세그멘테이션의 세그멘테이션 "'
seo-description: '" 워크플로우 사용 사례: 세그멘테이션의 세그멘테이션 "'
page-status-flag: 정품 인증 안 함
uuid: 396 a 3 de 1-6 ffa -4385-ac 9 f -15 fdeae 5 a 366
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 실행 활동
discoiquuid: 377821 E 6-69 F 8-41 CC-A 1 AD -8 A 2 F 5 ED 4 D 409
context-tags: '워크플로우, 사용 사례, 쿼리, 세분화, 전달 '
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: e77c8a65834009f2f7157d9535ae8e12e59244ff

---


# 워크플로우 사용 사례: 위치 세그먼테이션 {#segmentation-on-location}

해당 지역의 매장에 대한 오퍼를 통해 고객에게 이메일을 타깃팅할 수 있습니다.

1. 에서 **[!UICONTROL Marketing Activities]****[!UICONTROL Create]****[!UICONTROL Workflow]**&#x200B;를 클릭하고 선택합니다.
1. 워크플로우 유형으로 선택하고 **[!UICONTROL New Workflow]** 를 **[!UICONTROL Next]**&#x200B;클릭합니다.
1. 워크플로우의 속성을 입력하고 **[!UICONTROL Create]**&#x200B;를 클릭합니다.

## 수신자가 이메일을 통해 콘테스트 가능{#selecting-recipients-contactable-via-email}

1. 에서 **[!UICONTROL Activities]** , A를 **[!UICONTROL Targeting]**&#x200B;드래그하여 놓습니다 **[!UICONTROL Query activity]**![](assets/query.png).
1. 활동을 두 번 클릭합니다.
1. 에서 **[!UICONTROL Shortcuts]**&#x200B;연산자와 함께 **[!UICONTROL Profiles]** 필드를 **[!UICONTROL email]** 드래그하여 놓습니다 **[!UICONTROL is not empty]**.
1. 에서 **[!UICONTROL Shortcuts]**&#x200B;값이 있는 필드를 **[!UICONTROL Profiles]****[!UICONTROL no longer contact by email]** 드래그하여 놓은 **[!UICONTROL no]**&#x200B;다음 선택합니다.
1. 두 **[!UICONTROL Confirm]** 번 클릭합니다.

## 세그멘테이션 활동 만들기{#creating-a-segmentation-activity}

1. **[!UICONTROL Segmentation]** 활동을 드래그하여 놓고 두 번 클릭합니다.
1. 세그먼트를 클릭한 다음 전환을 클릭하여 첫 번째 도시의 사용자를 타깃팅합니다. Here Boston.
1. 연산자와 **[!UICONTROL Location]****[!UICONTROL City]****[!UICONTROL equals to]** 값으로 드래그하여 놓고 선택합니다 **[!UICONTROL Boston]**.
참고: 대소문자 구분 옵션의 선택 취소 옵션을 선택 취소하면 보스턴에 입장한 모든 사람에게 도달합니다.
1. **[!UICONTROL Confirm]**&#x200B;을 클릭합니다.
1. In **[!UICONTROL List of outbound segments]**, click **[!UICONTROL Add an element]** and click on ![](assets/edit_darkgrey-24px.png) to create a segment targeting people in the second city. Here Chicago.
1. 연산자를 드래그하여 놓고 **[!UICONTROL Location]****[!UICONTROL City]** 연산자로 **[!UICONTROL equals to]** 선택하고 값을 **[!UICONTROL Chicago]** 입력합니다.
1. 시카고에 입력한 모든 사람에게 도달하려면 대/소문자를 구분하지 않는 옵션을 선택 취소합니다.
1. **[!UICONTROL Confirm]**&#x200B;을 클릭합니다.

## 이메일 배달 만들기{#creating-an-email-delivery}

1. &gt; 각 **[!UICONTROL Activities]****[!UICONTROL Channels]**&#x200B;세그먼트 뒤에 마우스를 **[!UICONTROL Email Delivery]** 드래그하여 놓습니다.
1. 활동을 클릭하고 ![](assets/edit_darkgrey-24px.png) 편집을 선택합니다.
1. **[!UICONTROL Simple email]****[!UICONTROL Next]**&#x200B;을 선택하고 클릭합니다.
1. 이메일 템플릿을 선택하고 **[!UICONTROL Next]**&#x200B;를 클릭합니다.
1. 이메일 속성을 입력하고 **[!UICONTROL Next]**&#x200B;를 클릭합니다.
1. 이메일의 레이아웃을 만들려면 **[!UICONTROL Email Designer]**&#x200B;을 클릭합니다.
1. 요소를 삽입하거나 기존 템플릿을 선택합니다.
1. 각 위치에 맞는 제안을 이메일로 개인화할 수 있습니다.

자세한 내용은 이메일 [디자인을](../../designing/using/about-email-content-design.md#designing-an-email-content-from-scratch)참조하십시오.

1. 레이아웃을 **[!UICONTROL Preview]** 확인하려면을 클릭합니다.
1. **[!UICONTROL Save]**&#x200B;을 클릭합니다.

**관련 항목:**

* [쿼리 활동](../../automating/using/query.md)
* [세그멘테이션 활동](../../automating/using/segmentation.md)
* [이메일 배달](../../automating/using/email-delivery.md)
