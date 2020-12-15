---
solution: Campaign Standard
product: campaign
title: 트랜잭션 메시지 편집
description: 트랜잭션 메시지에 액세스하고 편집하고 개인화하는 방법을 살펴볼 수 있습니다.
audience: channels
content-type: reference
topic-tags: transactional-messaging
context-tags: null
translation-type: tm+mt
source-git-commit: f19d4b5c1837f3f03789958abb1539d4edea0744
workflow-type: tm+mt
source-wordcount: '1489'
ht-degree: 59%

---


# 트랜잭션 메시지 편집 {#editing-transactional-message}

이벤트<!--(the cart abandonment example as explained in [this section](../../channels/using/getting-started-with-transactional-msg.md#transactional-messaging-operating-principle))-->를 만들고 게시하면 해당 트랜잭션 메시지가 자동으로 만들어집니다.

이벤트를 구성하고 게시하는 단계는 [트랜잭션 이벤트](../../channels/using/configuring-transactional-event.md) 및 [트랜잭션 이벤트](../../channels/using/publishing-transactional-event.md) 게시 섹션에 제공됩니다.

이 메시지에 액세스하고 편집하고 개인화하는 단계는 아래에 설명되어 있습니다.

>[!IMPORTANT]
>
>[관리](../../administration/using/users-management.md#functional-administrators) 역할을 가진 사용자만 트랜잭션 메시지에 액세스하고 편집할 수 있습니다.

메시지가 준비되면 테스트하고 게시할 수 있습니다. [트랜잭션 메시지 테스트](../../channels/using/testing-transactional-message.md) 및 [트랜잭션 메시지 수명](../../channels/using/publishing-transactional-message.md)을 참조하십시오.

## 트랜잭션 메시지 액세스 {#accessing-transactional-messages}

만든 트랜잭션 메시지에 액세스하려면:

1. 왼쪽 위 모서리에서 **[!UICONTROL Adobe Campaign]** 로고를 클릭합니다.
1. **[!UICONTROL Marketing plans]** > **[!UICONTROL Transactional messages]** > **[!UICONTROL Transactional messages]**&#x200B;를 선택합니다.

   ![](assets/message-center_4.png)

1. 편집할 메시지를 클릭합니다.

   ![](assets/message-center_message-board.png)

해당 이벤트 구성 화면의 왼쪽 영역에 있는 링크를 통해 트랜잭션 메시지에 직접 액세스할 수도 있습니다. [이벤트 미리 보기 및 게시 참조](../../channels/using/publishing-transactional-event.md#previewing-and-publishing-the-event)

## 트랜잭션 메시지 개인화 {#personalizing-a-transactional-message}

트랜잭션 메시지를 편집하고 개인화하려면 아래 단계를 따르십시오.

>[!NOTE]
>
>이 섹션에서는 **이벤트 기반** 트랜잭션 메시지를 편집하는 방법에 대해 설명합니다. **프로필 기반** 트랜잭션 메시지 지정은 [아래에 자세히 표시됩니다](#profile-transactional-message-specificities).
>
>이벤트 기반 트랜잭션 메시지를 만드는 구성 단계는 [이 섹션](../../channels/using/configuring-transactional-event.md#event-based-transactional-messages)에 있습니다.

예를 들어 장바구니에 제품을 추가한 다음 구매를 진행하지 않고 사이트를 나가는 웹 사이트 사용자에게 알림을 전송해야 합니다. 이 예는 [트랜잭션 메시징 운영 원칙](../../channels/using/getting-started-with-transactional-msg.md#transactional-messaging-operating-principle) 섹션에 있습니다.

1. 메시지 제목과 콘텐츠를 수정하려면 **[!UICONTROL Content]** 블록을 클릭합니다. 예제에서는 이미지와 텍스트가 포함된 템플릿을 선택합니다. 이메일 콘텐츠 템플릿에 대한 자세한 내용은 [템플릿을 사용하여 이메일 디자인](../../designing/using/using-reusable-content.md#designing-templates)을 참조하십시오.

   ![](assets/message-center_6.png)

1. 제목을 추가하고 필요에 따라 메시지 콘텐츠를 편집합니다.

   >[!NOTE]
   >
   >포기한 장바구니에 대한 링크는 사용자를 장바구니에 리디렉션하는 외부 URL에 대한 링크입니다. 이 매개 변수는 Adobe Campaign에서 관리되지 않습니다.

1. 예제에서는 [이벤트를 만들 때](../../channels/using/configuring-transactional-event.md) 정의한 이름, 마지막 제품 상담, 총 장바구니 금액의 세 가지 필드를 추가하려고 합니다. 이렇게 하려면 메시지 콘텐츠에 [개인화 필드 삽입](../../designing/using/personalization.md#inserting-a-personalization-field)을 하십시오.

1. **[!UICONTROL Context]** > **[!UICONTROL Real-time event]** > **[!UICONTROL Event context]**&#x200B;을(를) 통해 해당 필드를 찾아봅니다.

   ![](assets/message-center_7.png)

1. 메시지의 내용을 강화할 수도 있습니다. 이렇게 하려면 이벤트 구성에 연결된 테이블에서 필드를 추가합니다([이벤트 돋보기](../../channels/using/configuring-transactional-event.md#enriching-the-transactional-message-content) 참조). 이 예에서 **[!UICONTROL Profile]** 테이블에서 **[!UICONTROL Context]** > **[!UICONTROL Real-time event]** > **[!UICONTROL Event context]**&#x200B;까지 **[!UICONTROL Title (salutation)]** 필드를 선택합니다.

   ![](assets/message-center_7-enrichment.png)

1. 필요한 모든 필드를 삽입합니다.

   ![](assets/message-center_8.png)

1. 이 이벤트에 대해 정의한 프로필을 선택하여 메시지를 미리 봅니다.

   메시지 미리 보기 단계는 [메시지 미리 보기](../../sending/using/previewing-messages.md) 섹션에 자세히 설명되어 있습니다.

   ![](assets/message-center_9.png)

   개인화 필드가 테스트 프로필에 입력한 정보와 일치하는지 확인할 수 있습니다. 자세한 내용은 [특정 테스트 프로필 정의](../../channels/using/testing-transactional-message.md#defining-specific-test-profile)를 참조하십시오.

## 트랜잭션 메시지에서 제품 목록 사용 {#using-product-listings-in-a-transactional-message}

트랜잭션 이메일의 내용을 편집할 때 하나 이상의 데이터 컬렉션을 참조하는 제품 목록을 만들 수 있습니다. 예를 들어 장바구니 포기 이메일에는 사용자가 웹 사이트를 떠날 때 장바구니에 있던 모든 제품 목록과 이미지, 가격 및 각 제품에 대한 링크를 포함할 수 있습니다.

>[!IMPORTANT]
>
>제품 목록은 [이메일 디자이너](../../designing/using/designing-content-in-adobe-campaign.md#email-designer-interface) 인터페이스를 통해 트랜잭션 이메일 컨텐츠를 편집할 때 이메일 채널에만 사용할 수 있습니다.

트랜잭션 메시지에 포기된 제품 목록을 추가하려면 아래 단계를 따르십시오.

트랜잭션 이메일에서 제품 목록을 구성하는 데 필요한 단계를 설명하는 [이 비디오 집합](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/designing-content/product-listings-in-transactional-email.html?lang=en#configure-product-listings-in-transactional-emails)을 볼 수도 있습니다.

>[!NOTE]
>
>Adobe Campaign은 중첩된 제품 목록을 지원하지 않습니다. 즉, 다른 제품 목록 내에 제품 목록을 포함할 수 없습니다.

### 제품 목록 정의 {#defining-a-product-listing}

트랜잭션 메시지에서 제품 목록을 사용하려면 이벤트 수준에서 표시하려는 목록의 각 제품에 대한 제품 목록과 필드를 정의해야 합니다. 자세한 내용은 [데이터 컬렉션 정의](../../channels/using/configuring-transactional-event.md#defining-data-collections)를 참조하십시오.

1. 트랜잭션 메시지에서 **[!UICONTROL Content]** 블록을 클릭하여 전자 메일 콘텐츠를 수정합니다.
1. 구조 구성 요소를 작업 영역으로 끌어다 놓습니다. 자세한 내용은 [이메일 구조 정의](../../designing/using/designing-from-scratch.md#defining-the-email-structure)를 참조하십시오.

   예를 들어 하나의 열 구조 구성 요소를 선택하고 텍스트 구성 요소, 이미지 구성 요소 및 단추 구성 요소를 추가합니다. 자세한 내용은 [콘텐츠 구성 요소 사용](../../designing/using/designing-from-scratch.md#about-content-components)을 참조하십시오.

1. 방금 만든 구조 구성 요소를 선택하고 상황별 도구 모음에서 **[!UICONTROL Enable product listing]** 아이콘을 클릭합니다.

   ![](assets/message-center_loop_create.png)

   구조 구성 요소는 주황색 프레임으로 강조 표시되고 **[!UICONTROL Product listing]** 설정이 왼쪽 팔레트에 표시됩니다.

   ![](assets/message-center_loop_palette.png)

1. 다음과 같은 컬렉션의 요소가 표시되는 방식을 선택합니다.

   * **[!UICONTROL Row]**: 가로 즉, 다른 행 아래에 있는 각 요소를 의미합니다.
   * **[!UICONTROL Column]**: 세로 즉, 같은 행의 다른 요소 옆에 있는 각 요소를 의미합니다.

   >[!NOTE]
   >
   >**[!UICONTROL Column]** 옵션은 다중 열 구조 구성 요소( **[!UICONTROL 2:2 column]**, **[!UICONTROL 3:3 column]** 및 **[!UICONTROL 4:4 column]** )를 사용하는 경우에만 사용할 수 있습니다. 제품 목록을 편집할 때는 다른 열은 고려하지 않고 첫 번째 열만 채웁니다. 구조 구성 요소 선택에 대한 자세한 내용은 [이메일 구조 정의](../../designing/using/designing-from-scratch.md#defining-the-email-structure)를 참조하십시오.

1. 트랜잭션 메시지와 관련된 이벤트를 구성할 때 만든 데이터 컬렉션을 선택합니다. **[!UICONTROL Context]** > **[!UICONTROL Real-time event]** > **[!UICONTROL Event context]** 노드 아래에서 찾을 수 있습니다.

   ![](assets/message-center_loop_selection.png)

   이벤트 구성에 대한 자세한 내용은 [데이터 컬렉션 정의](../../channels/using/configuring-transactional-event.md#defining-data-collections)를 참조하십시오.

1. 전자 메일에 표시된 목록을 시작할 요소를 선택하려면 **[!UICONTROL First item]** 드롭다운 목록을 사용합니다.

   예를 들어 2를 선택하면 컬렉션의 첫 번째 항목이 전자 메일에 표시되지 않습니다. 제품 목록은 두 번째 항목에서 시작됩니다.

1. 목록에 표시할 최대 항목 수를 선택합니다.

   >[!NOTE]
   >
   >목록의 요소를 세로( **[!UICONTROL Column]** )로 표시하려면 선택한 구조 구성 요소(2, 3 또는 4열)에 따라 최대 항목 수가 제한됩니다. 구조 구성 요소 선택에 대한 자세한 내용은 [전자 메일 구조 편집](../../designing/using/designing-from-scratch.md#defining-the-email-structure)을 참조하십시오.

### 제품 목록 채우기 {#populating-the-product-listing}

트랜잭션 전자 메일에 연결된 이벤트에서 오는 제품 목록을 표시하려면 아래 단계를 따르십시오.

이벤트 구성 시 컬렉션 및 관련 필드 만들기에 대한 자세한 내용은 [데이터 컬렉션 정의](../../channels/using/configuring-transactional-event.md#defining-data-collections)를 참조하십시오.

1. 삽입한 이미지 구성 요소를 선택하고 설정 창에서 **[!UICONTROL Enable personalization]**&#x200B;을(를) 선택한 다음 연필을 클릭합니다.

   ![](assets/message-center_loop_image.png)

1. 열려 있는 **[!UICONTROL Image source URL]** 창에서 **[!UICONTROL Add personalization field]**&#x200B;을 선택합니다.

   **[!UICONTROL Context]** > **[!UICONTROL Real-time event]** > **[!UICONTROL Event context]** 노드에서 만든 컬렉션에 해당하는 노드(여기서는 **[!UICONTROL Product list]**)를 열고 정의한 이미지 필드(여기서는 **[!UICONTROL Product image]** )를 선택합니다. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

   ![](assets/message-center_loop_product-image.png)

   선택한 개인화 필드가 이제 설정 창에 표시됩니다.

1. 원하는 위치에서 상황별 도구 모음의 **[!UICONTROL Insert personalization field]**&#x200B;을(를) 선택합니다.

   ![](assets/message-center_loop_product.png)

1. **[!UICONTROL Context]** > **[!UICONTROL Real-time event]** > **[!UICONTROL Event context]** 노드에서 만든 컬렉션에 해당하는 노드(여기서는 **[!UICONTROL Product list]**)를 열고 만든 필드(여기서는 **[!UICONTROL Product name]**)를 선택합니다. **[!UICONTROL Confirm]**&#x200B;을(를) 클릭합니다.

   ![](assets/message-center_loop_product_node.png)

   선택한 개인화 필드가 이제 전자 메일 콘텐츠의 원하는 위치에 표시됩니다.

1. 가격을 삽입하려면 유사하게 진행합니다..
1. 텍스트를 선택하고 상황별 도구 모음에서 **[!UICONTROL Insert link]**&#x200B;를 선택합니다.

   ![](assets/message-center_loop_link_insert.png)

1. 열려 있는 **[!UICONTROL Insert link]** 창에서 **[!UICONTROL Add personalization field]**&#x200B;을(를) 선택합니다.

   **[!UICONTROL Context]** > **[!UICONTROL Real-time event]** > **[!UICONTROL Event context]** 노드에서 만든 컬렉션에 해당하는 노드(여기서는 **[!UICONTROL Product list]**)를 열고 만든 URL 필드(여기서는 **[!UICONTROL Product URL]**)를 선택합니다. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

   >[!IMPORTANT]
   >
   >보안상의 이유로 적합한 정적 도메인 이름으로 시작하는 링크 내에 개인화 필드를 삽입해야 합니다.

   ![](assets/message-center_loop_link_select.png)

   선택한 개인화 필드가 이제 설정 창에 표시됩니다.

1. 제품 목록이 적용되는 구조 구성 요소를 선택하고 기본 콘텐츠를 정의하려면 **[!UICONTROL Show fallback]**&#x200B;을(를) 선택합니다.

   ![](assets/message-center_loop_fallback_show.png)

1. 하나 이상의 콘텐츠 구성 요소를 끌어서 필요에 따라 편집합니다.

   ![](assets/message-center_loop_fallback.png)

   예를 들어 고객이 장바구니에 아무것도 없는 경우, 이벤트가 트리거될 때 컬렉션이 비어 있으면 대체 콘텐츠가 표시됩니다.

1. 설정 창에서 제품 목록의 스타일을 편집합니다. 자세한 내용은 [이메일 스타일 관리](../../designing/using/styles.md)를 참조하십시오.
1. 관련 트랜잭션 이벤트에 연결된 컬렉션 데이터를 정의한 테스트 프로필을 사용하여 전자 메일을 미리 봅니다. 예를 들어, 사용할 테스트 프로필의 **[!UICONTROL Event data]** 섹션에 다음 정보를 추가합니다.

   ![](assets/message-center_loop_test-profile_payload.png)

   트랜잭션 메시지에서 테스트 프로필을 정의하는 방법에 대한 자세한 내용은 [이 섹션](../../channels/using/testing-transactional-message.md#defining-specific-test-profile)을 참조하십시오.

## 프로파일 기반 트랜잭션 메시지 지정 {#profile-transactional-message-specificities}

모든 프로필 정보를 활용하여 메시지 컨텐츠를 개인화하고, 구독 취소 링크를 사용하고, [피로 규칙](../../sending/using/fatigue-rules.md)과 같은 마케팅 유형 분류 규칙을 적용할 수 있는 고객 마케팅 프로필을 기반으로 트랜잭션 메시지를 보낼 수 있습니다.

* 이벤트 기반 트랜잭션 메시지와 프로필 기반 트랜잭션 메시지 간의 차이에 대한 자세한 내용은 [이 섹션](../../channels/using/getting-started-with-transactional-msg.md#transactional-message-types)을 참조하십시오.

* 프로필 기반 트랜잭션 메시지를 만드는 구성 단계는 [이 섹션](../../channels/using/configuring-transactional-event.md#profile-based-transactional-messages)에 자세히 설명되어 있습니다.

<!--### Editing a profile transactional message {#editing-profile-transactional-message}-->

프로필 트랜잭션 메시지를 만들고, 편집하고, 개인화하는 단계는 이벤트 트랜잭션 메시지의 경우와 대부분 동일합니다.

차이점은 아래에 나와 있습니다.

1. [만든 트랜잭션 메시지로 이동하여 편집합니다.](#accessing-transactional-messages)
1. 트랜잭션 메시지에서 **[!UICONTROL Content]** 섹션을 클릭합니다. 트랜잭션 이메일 템플릿 외에도 **[!UICONTROL Profile]** 리소스를 대상으로 하는 이메일 템플릿을 선택할 수도 있습니다.

   ![](assets/message-center_marketing_templates.png)

1. 기본 이메일 템플릿을 선택합니다. 모든 마케팅 이메일과 유사하게 **구독 취소 링크**&#x200B;가 포함되어 있습니다.

   ![](assets/message-center_marketing_perso_unsubscription.png)

   템플릿에 대한 자세한 내용은 [이 섹션](../../designing/using/using-reusable-content.md#content-templates)을 참조하십시오.

1. 또한 실시간 이벤트 기반의 구성과 달리 메시지를 개인화하기 위해 **모든 프로필 정보에 직접 액세스할 수 있습니다**. 다른 표준 마케팅 이메일과 마찬가지로 [개인화 필드](../../designing/using/personalization.md#inserting-a-personalization-field)를 추가할 수 있습니다.

1. 메시지를 게시하기 전에 변경 내용을 저장합니다. 자세한 내용은 [트랜잭션 메시지 게시](../../channels/using/publishing-transactional-message.md#publishing-a-transactional-message)를 참조하십시오.

<!--### Monitoring a profile transactional message delivery {#monitoring-a-profile-transactional-message-delivery}

Once the message is published and your site integration is done, you can monitor the delivery.

1. To view the message delivery log, click the icon at the bottom right of the **[!UICONTROL Deployment]** block.

1. Click the **[!UICONTROL Execution list]** tab.

   ![](assets/message-center_execution_tab.png)

1. Select the latest execution delivery.

   An **execution delivery** is a non-actionable and non-functional technical message created once a month for each transactional message, and each time a transactional message is edited and published again

1. Select the **[!UICONTROL Sending logs]** tab. In the **[!UICONTROL Status]** column, **[!UICONTROL Sent]** indicates that a profile has opted in.

   ![](assets/message-center_marketing_sending_logs.png)

1. Select the **[!UICONTROL Exclusions logs]** tab to view recipients who have been excluded from the message target, such as addresses on denylist.

   ![](assets/message-center_marketing_exclusion_logs.png)

>[!NOTE]
>
>For more information on accessing and using the logs, see [Monitoring a delivery](../../sending/using/monitoring-a-delivery.md).

For any profile that has opted out, the **[!UICONTROL Address on denylist]** typology rule excluded the corresponding recipient.

This rule is part of a specific typology that applies to all transactional messages based on the **[!UICONTROL Profile]** table.

![](assets/message-center_marketing_typology.png)

**Related topics**:

* [Integrate the event triggering](../../channels/using/getting-started-with-transactional-msg.md#integrate-event-trigger)
* [About typologies and typology rules](../../sending/using/about-typology-rules.md)-->
