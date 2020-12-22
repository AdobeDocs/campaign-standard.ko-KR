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
source-git-commit: 5758e5f0f6811a97f51e995fa3c378a7c7117ff5
workflow-type: tm+mt
source-wordcount: '653'
ht-degree: 30%

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

<!--## Using product listings in a transactional message {#using-product-listings-in-a-transactional-message}

When editing the content of a transactional email, you can create product listings referencing one or more data collections. For example, in a cart abandonment email, you can include a list of all products that were in the users' carts when they left your website, with an image, the price, and a link to each product.

>[!IMPORTANT]
>
>Product listings are only available for the email channel, when editing transactional email content through the [Email Designer](../../designing/using/designing-content-in-adobe-campaign.md#email-designer-interface) interface.

To add a list of abandoned products in a transactional message, follow the steps below.

You can also watch [this set of videos](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/designing-content/product-listings-in-transactional-email.html?lang=en#configure-product-listings-in-transactional-emails) explaining the steps that are required to configure product listings in a transactional email.

>[!NOTE]
>
>Adobe Campaign does not support nested product listings, meaning that you cannot include a product listing inside another one.

### Defining a product listing {#defining-a-product-listing}

Before being able to use a product listing in a transactional message, you need to define at the event level the list of products and the fields for each product of the list you want to display. For more on this, see [Defining data collections](../../channels/using/configuring-transactional-event.md#defining-data-collections).

1. In the transactional message, click the **[!UICONTROL Content]** block to modify the email content.
1. Drag and drop a structure component to the workspace. For more on this, see [Defining the email structure](../../designing/using/designing-from-scratch.md#defining-the-email-structure).

   For example, select a one-column structure component and add a text component, an image component and a button component. For more on this, see [Using content components](../../designing/using/designing-from-scratch.md#about-content-components).

1. Select the structure component you just created and click the **[!UICONTROL Enable product listing]** icon from the contextual toolbar.

   ![](assets/message-center_loop_create.png)

   The structure component is highlighted with an orange frame and the **[!UICONTROL Product listing]** settings are displayed in the left palette.

   ![](assets/message-center_loop_palette.png)

1. Select how the elements of the collection will be displayed:

    * **[!UICONTROL Row]**: horizontally, meaning each element on one row under the other.
    * **[!UICONTROL Column]**: vertically, meaning each element next to the other on the same row.

   >[!NOTE]
   >
   >The **[!UICONTROL Column]** option is only available when using a multicolumn structure component ( **[!UICONTROL 2:2 column]**, **[!UICONTROL 3:3 column]** and **[!UICONTROL 4:4 column]** ). When editing the product listing, only fill in the first column: the other columns will not be taken into account. For more on selecting structure components, see [Defining the email structure](../../designing/using/designing-from-scratch.md#defining-the-email-structure).

1. Select the data collection you created when configuring the event related to the transactional message. You can find it under the **[!UICONTROL Context]** > **[!UICONTROL Real-time event]** > **[!UICONTROL Event context]** node.

   ![](assets/message-center_loop_selection.png)

   For more on configuring the event, see [Defining data collections](../../channels/using/configuring-transactional-event.md#defining-data-collections).

1. Use the **[!UICONTROL First item]** drop-down list to select which element will start the list displayed in the email.

   For example, if you select 2, the first item of the collection will not be displayed in the email. The product listing will start on the second item.

1. Select the maximum number of items to display in the list.

   >[!NOTE]
   >
   >If you want the elements of your list to be displayed vertically ( **[!UICONTROL Column]** ), the maximum number of items is limited according to the selected structure component (2, 3 or 4 columns). For more on selecting structure components, see [Editing the email structure](../../designing/using/designing-from-scratch.md#defining-the-email-structure).

### Populating the product listing {#populating-the-product-listing}

To display a list of products coming from the event linked to the transactional email, follow the steps below.

For more on creating a collection and related fields when configuring the event, see [Defining data collections](../../channels/using/configuring-transactional-event.md#defining-data-collections).

1. Select the image component you inserted, select **[!UICONTROL Enable personalization]** and click the pencil in the Settings pane.

   ![](assets/message-center_loop_image.png)

1. Select **[!UICONTROL Add personalization field]** in the **[!UICONTROL Image source URL]** window that opens.

   From the **[!UICONTROL Context]** > **[!UICONTROL Real-time event]** > **[!UICONTROL Event context]** node, open the node corresponding to the collection that you created (here **[!UICONTROL Product list]** ) and select the image field that you defined (here **[!UICONTROL Product image]** ). Click **[!UICONTROL Save]**.

   ![](assets/message-center_loop_product-image.png)

   The personalization field that you selected is now displayed in the Settings pane.

1. At the desired position, select **[!UICONTROL Insert personalization field]** from the contextual toolbar.

   ![](assets/message-center_loop_product.png)

1. From the **[!UICONTROL Context]** > **[!UICONTROL Real-time event]** > **[!UICONTROL Event context]** node, open the node corresponding to the collection that you created (here **[!UICONTROL Product list]** ) and select the field that you created (here **[!UICONTROL Product name]** ). Click **[!UICONTROL Confirm]**.

   ![](assets/message-center_loop_product_node.png)

   The personalization field that you selected is now displayed at the desired position in the email content.

1. Proceed similarly to insert the price.
1. Select some text and select **[!UICONTROL Insert link]** from the contextual toolbar.

   ![](assets/message-center_loop_link_insert.png)

1. Select **[!UICONTROL Add personalization field]** in the **[!UICONTROL Insert link]** window that opens.

   From the **[!UICONTROL Context]** > **[!UICONTROL Real-time event]** > **[!UICONTROL Event context]** node, open the node corresponding to the collection that you created (here **[!UICONTROL Product list]** ) and select the URL field that you created (here **[!UICONTROL Product URL]** ). Click **[!UICONTROL Save]**.

   >[!IMPORTANT]
   >
   >For security reasons, make sure you insert the personalization field inside a link starting with a proper static domain name.

   ![](assets/message-center_loop_link_select.png)

   The personalization field that you selected is now displayed in the Settings pane.

1. Select the structure component on which the product listing is applied and select **[!UICONTROL Show fallback]** to define a default content.

   ![](assets/message-center_loop_fallback_show.png)

1. Drag one or more content components and edit them as needed.

   ![](assets/message-center_loop_fallback.png)

   The fallback content will be displayed if the collection is empty when the event is triggered, for example if a customer has nothing in his cart.

1. From the Settings pane, edit the styles for the product listing. For more on this, see [Managing email styles](../../designing/using/styles.md).
1. Preview the email using a test profile linked to the relevant transactional event and for which you defined collection data. For example, add the following information in the **[!UICONTROL Event data]** section for the test profile you want to use:

   ![](assets/message-center_loop_test-profile_payload.png)

   For more on defining a test profile in a transactional message, see [this section](../../channels/using/testing-transactional-message.md#defining-specific-test-profile).-->

## 프로파일 기반 트랜잭션 메시지 지정 {#profile-transactional-message-specificities}

모든 프로필 정보를 활용하여 메시지 컨텐츠를 개인화하고, 구독 취소 링크를 사용하고, [피로 규칙](../../sending/using/fatigue-rules.md)과 같은 마케팅 유형 분류 규칙을 적용할 수 있는 고객 마케팅 프로필을 기반으로 트랜잭션 메시지를 보낼 수 있습니다.

* 이벤트 기반 트랜잭션 메시지와 프로필 기반 트랜잭션 메시지 간의 차이에 대한 자세한 내용은 [이 섹션](../../channels/using/getting-started-with-transactional-msg.md#transactional-message-types)을 참조하십시오.

* 프로필 기반 트랜잭션 메시지를 만드는 구성 단계는 [이 섹션](../../channels/using/configuring-transactional-event.md#profile-based-transactional-messages)에 자세히 설명되어 있습니다.

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
