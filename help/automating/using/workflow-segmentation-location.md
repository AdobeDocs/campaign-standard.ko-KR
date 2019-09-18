---
title: '"워크플로우 사용 사례:위치 세그먼테이션"'
seo-title: '"워크플로우 사용 사례:위치 세그먼테이션"'
description: '"워크플로우 사용 사례:위치 세그먼테이션"'
seo-description: '"워크플로우 사용 사례:위치 세그먼테이션"'
page-status-flag: 활성화 안 함
uuid: 396a3de1-6ffa-4385-ac9f-15fdeae5a366
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 자동화
content-type: reference
topic-tags: 실행 활동
discoiquuid: 377821e6-69f8-41cc-a1ad-8a2f5ed4d409
context-tags: '워크플로,사용 사례,쿼리,세그멘테이션,전달 '
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: f7e56dcb4c2bbdc802c9d271d4a44d9a72b239ed

---


# 워크플로우 사용 사례:위치 세분화 {#segmentation-on-location}

해당 지역의 상점에서 오퍼를 제공하는 고객에게 타깃팅 이메일을 보낼 수 있습니다.

1. 에서 **[!UICONTROL Marketing Activities]**&#x200B;을 클릭하고 **[!UICONTROL Create]** 선택합니다 **[!UICONTROL Workflow]**.
1. 워크플로우 **[!UICONTROL New Workflow]** 유형으로 선택하고 을 클릭합니다 **[!UICONTROL Next]**.
1. 워크플로우의 속성을 입력하고 을 클릭합니다 **[!UICONTROL Create]**.

## 이메일을 통해 연락처 선택{#selecting-recipients-contactable-via-email}

1. &gt; **[!UICONTROL Activities]** 에서 **[!UICONTROL Targeting]**&#x200B;드래그하여 **[!UICONTROL Query activity]** ![](assets/query.png)놓습니다.
1. 활동을 두 번 클릭합니다.
1. 에서 **[!UICONTROL Shortcuts]**&#x200B;연산자를 사용하여 필드를 드래그하여 **[!UICONTROL Profiles]** **[!UICONTROL email]** **[!UICONTROL is not empty]**&#x200B;선택하고,
1. 에서 **[!UICONTROL Shortcuts]**&#x200B;드래그하여 **[!UICONTROL Profiles]** 놓고 값이 **[!UICONTROL no longer contact by email]** 있는 필드를 선택합니다 **[!UICONTROL no]**.
1. 두 **[!UICONTROL Confirm]** 번 클릭합니다.

![](assets/wf-complement-query.png)

## 세그멘테이션 활동 만들기{#creating-a-segmentation-activity}

1. 활동을 드래그하여 놓고 두 번 클릭합니다. **[!UICONTROL Segmentation]**
1. 세그먼트를 클릭한 다음 첫 번째 도시에서 사용자를 타깃팅하기 위한 전환을 엽니다. 여기 보스턴.
1. 연산자와 값을 사용하여 **[!UICONTROL Location]** 드래그하여 놓고 **[!UICONTROL City]** **[!UICONTROL equals to]** **[!UICONTROL Boston]**선택합니다.
참고:보스턴에 들어온 모든 사람에게 연락하려면 대/소문자를 구분하지 않고 대/소문자를 구분하십시오.
1. Click **[!UICONTROL Confirm]**.
1. 에서 **[!UICONTROL List of outbound segments]**&#x200B;을 **[!UICONTROL Add an element]** ![](assets/edit_darkgrey-24px.png) 클릭하고 클릭하여 두 번째 도시의 사람을 대상으로 하는 세그먼트를 만듭니다. 여기 시카고
1. 연산자를 사용하여 드래그 앤 드롭 **[!UICONTROL Location]** 및 **[!UICONTROL City]** 선택하고 **[!UICONTROL equals to]** 값을 **[!UICONTROL Chicago]** 입력합니다.
1. 시카고에 입장한 모든 사람에게 연락하려면 대/소문자를 구분하지 않고 대/소문자 구분 옵션의 선택을 취소합니다.
1. Click **[!UICONTROL Confirm]**.

## 이메일 배달 만들기{#creating-an-email-delivery}

1. &gt; **[!UICONTROL Activities]** 에서 각 세그먼트 **[!UICONTROL Channels]****[!UICONTROL Email Delivery]** 다음에 끌어 놓습니다.
1. 활동을 클릭하고 ![](assets/edit_darkgrey-24px.png) 편집하려면 선택합니다.
1. 을 선택하고 **[!UICONTROL Simple email]** 클릭합니다 **[!UICONTROL Next]**.
1. 이메일 템플릿을 선택하고 을 **[!UICONTROL Next]**&#x200B;클릭합니다.
1. 이메일 속성을 입력하고 을 **[!UICONTROL Next]**&#x200B;클릭합니다.
1. 이메일 레이아웃을 만들려면 을 클릭합니다 **[!UICONTROL Email Designer]**.
1. 요소를 삽입하거나 기존 템플릿을 선택합니다.
1. 각 위치에 맞는 제안을 통해 이메일을 개인화할 수 있습니다.

자세한 내용은 이메일 [디자인을 참조하십시오](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch).

1. 레이아웃을 **[!UICONTROL Preview]** 확인하려면 클릭합니다.
1. Click **[!UICONTROL Save]**.

![](assets/wf-segmentation-location.png)

**관련 항목:**

* [쿼리 활동](../../automating/using/query.md)
* [세그멘테이션 활동](../../automating/using/segmentation.md)
* [이메일 전달](../../automating/using/email-delivery.md)
