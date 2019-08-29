---
title: '" 워크플로우 사용 사례: 보완 기능으로 전달 만들기 "'
seo-title: '" 워크플로우 사용 사례: 보완 기능으로 전달 만들기 "'
description: '" 워크플로우 사용 사례: 보완 기능으로 전달 만들기 "'
seo-description: '" 워크플로우 사용 사례: 보완 기능으로 전달 만들기 "'
page-status-flag: 정품 인증 안 함
uuid: 396 a 3 de 1-6 ffa -4385-ac 9 f -15 fdeae 5 a 366
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 실행 활동
discoiquuid: 377821 E 6-69 F 8-41 CC-A 1 AD -8 A 2 F 5 ED 4 D 409
context-tags: 워크플로우, 활용 사례, 세분화
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: e77c8a65834009f2f7157d9535ae8e12e59244ff

---


# 워크플로우 사용 사례: 보완을 통한 전달 창출 {#deliveries-with-complement}

고객에게 이메일을 보낼 수 있습니다. 1 년 전에 생성된 클라이언트의 경우 1 년 전에 생성된 클라이언트용으로 하나

1. 에서 **[!UICONTROL Marketing Activities]****[!UICONTROL Create]****[!UICONTROL Workflow]**&#x200B;를 클릭하고 선택합니다.
1. 워크플로우 유형으로 선택하고 **[!UICONTROL New Workflow]** 를 **[!UICONTROL Next]**&#x200B;클릭합니다.
1. 워크플로우의 속성을 입력하고 **[!UICONTROL Create]**&#x200B;를 클릭합니다.

## 쿼리 활동 만들기 {#create-a-query-activity}

1. 에서 **[!UICONTROL Activities]** , A를 **[!UICONTROL Targeting]**&#x200B;드래그하여 놓습니다 **[!UICONTROL Query activity]**![](assets/query.png).
1. 활동을 두 번 클릭합니다.
1. 에서 **[!UICONTROL Shortcuts]**&#x200B;연산자로 드래그하여 놓은 **[!UICONTROL Profiles]****[!UICONTROL email]****[!UICONTROL is not empty]**&#x200B;다음 선택합니다.
1. 에서 **[!UICONTROL Shortcuts]**&#x200B;값을 드래그하여 놓고 **[!UICONTROL Profiles]** 선택합니다 **[!UICONTROL no longer contact by email]****[!UICONTROL no]**.
1. **[!UICONTROL Confirm]**&#x200B;을 클릭합니다.

## 세그멘테이션 활동 만들기 {#create-a-segmentation-activity}

1. 에서 **[!UICONTROL Activities]****[!UICONTROL Targeting]****[!UICONTROL Segmentation]** 활동을 드래그하여 놓고 두 번 클릭합니다.
1. 세그먼트 위로 마우스를 가져간 다음 ![](assets/edit_darkgrey-24px.png) 올해 데이터베이스에 추가된 타겟 고객을 클릭합니다.
1. 필터 유형을 드래그하여 놓고 **[!UICONTROL Profiles]** 선택합니다 **[!UICONTROL Created]****[!UICONTROL Relative]**.
1. **[!UICONTROL Level of precision]** To **[!UICONTROL Year]** &amp; Select **[!UICONTROL This year]**&#x200B;를 변경합니다.
1. 두 **[!UICONTROL Confirm]** 번 클릭합니다.
1. 에서 **[!UICONTROL Advanced Options]**&#x200B;나머지 **[!UICONTROL Generate complement]** 수신자를 대상으로 하는 세그먼트를 만들려면을 선택합니다.
1. **[!UICONTROL Confirm]**&#x200B;을 클릭합니다.
1. **[!UICONTROL Save]**&#x200B;을 클릭합니다.

>[!NOTE]
>
>규칙의 구조를 관찰하려면 **[!UICONTROL Advanced Mode]**&#x200B;을 클릭합니다.

## 이메일 배달 만들기 {#create-an-email-delivery}

1. &gt; 각 **[!UICONTROL Activities]****[!UICONTROL Channels]**&#x200B;세그먼트 다음에 이메일 배달을 드래그하여 놓습니다.
1. 활동을 클릭하고 ![](assets/edit_darkgrey-24px.png) 편집을 선택합니다.
1. **[!UICONTROL Single send email]****[!UICONTROL Next]**&#x200B;을 선택하고 클릭합니다.
1. 이메일 템플릿을 선택하고 **[!UICONTROL Next]**&#x200B;를 클릭합니다.
1. 이메일 속성을 입력하고 **[!UICONTROL Next]**&#x200B;를 클릭합니다.
1. 이메일의 레이아웃을 만들려면 **[!UICONTROL Email Designer]**&#x200B;을 클릭합니다.
1. 요소를 삽입하거나 기존 템플릿을 선택합니다.
1. 각 전달 상황에 맞는 제안을 이메일로 개인화할 수 있습니다.
1. 레이아웃을 **[!UICONTROL Preview]** 확인하려면을 클릭합니다.
1. **[!UICONTROL Save]**&#x200B;을 클릭합니다.

자세한 내용은 이메일 [디자인을](../../designing/using/about-email-content-design.md#designing-an-email-content-from-scratch)참조하십시오.

**관련 항목:**

* [쿼리](../../automating/using/query.md)
* [세그멘테이션 활동](../../automating/using/segmentation.md)
* [이메일 배달](../../automating/using/email-delivery.md)
