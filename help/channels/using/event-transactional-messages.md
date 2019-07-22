---
title: 이벤트 트랜잭션 메시지
seo-title: 이벤트 트랜잭션 메시지
description: 이벤트 트랜잭션 메시지
seo-description: 이벤트 트랜잭션 메시지를 만들고 게시하는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: D 747 Feb 5-58 FB -4 E 12-A 176-404 F 0 ECA 5391
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 채널
content-type: 참조
topic-tags: 트랜잭션 메시징
discoiquuid: 4 F 6317 A 1-9 DFE -4714-BC 1 C -393629 D 855 CD
context-tags: Deliverytransactionaltemplate, 개요
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: e08b7e01956a9106937cb72ab790cb2e98999fcd

---


# Event transactional messages{#event-transactional-messages}

이벤트를 타깃팅하는 이벤트 트랜잭션 메시지를 전송할 수 있습니다. 이 유형의 트랜잭션 메시지에는 프로필 정보가 포함되어 있지 않습니다. 게재 대상은 이벤트 자체에 포함된 데이터로 정의됩니다.

Once you have created and published an event (the cart abandonment as explained in [this section](../../channels/using/about-transactional-messaging.md#transactional-messaging-operating-principle)), the corresponding transactional message is created automatically.

The configuration steps are presented in the [Configuring an event to send an transactional message](../../administration/using/configuring-transactional-messaging.md#use-case--configuring-an-event-to-send-a-transactional-message) section.

이벤트가 트랜잭션 메시지를 보내게 하려면 메시지를 개인화하고 테스트하여 게시해야 합니다.

>[!NOTE]
>
>To access the transactional messages, you must have administration rights or appear in the **[!UICONTROL Message Center agents]** (mcExec) security group. 이벤트 트랜잭션 메시지에는 프로필 정보가 포함되어 있지 않으므로, 프로필이 있는 취약점의 경우에도, 피로도 규칙과 호환되지 않습니다. [피로 규칙을 참조하십시오](../../administration/using/fatigue-rules.md#choosing-the-channel).

## Defining a test profile in a transactional message {#defining-a-test-profile-in-a-transactional-message}

적응형 테스트 프로필을 정의하여 메시지를 미리 보고 검증을 통해 메시지를 확인할 수 있습니다.

### Creating a test profile within the transactional message {#creating-a-test-profile-within-the-transactional-----------message}

1. To access the message that you created, click the **[!UICONTROL Adobe Campaign]** logo, in the top left corner, then select **[!UICONTROL Marketing plans]** &gt; **[!UICONTROL Transactional messages]** &gt; **[!UICONTROL Transactional messages]**.

   ![](assets/message-center_4.png)

1. 이벤트에 연결할 테스트 프로필을 만듭니다.

   ![](assets/message-center_test-profile.png)

1. Specify the information to send in JSON format in the **[!UICONTROL Event data used for personalization]** section. 이것은 메시지를 미리 볼 때와 테스트 프로필이 증명을 받을 때 사용할 내용입니다.

   ![](assets/message-center_event-data.png)

   >[!NOTE]
   >
   >프로필 테이블과 관련된 정보를 입력할 수도 있습니다. See [Enriching the transactional message content](../../administration/using/configuring-transactional-messaging.md#enriching-the-transactional-message-content).

1. 만들어진 테스트 프로필은 트랜잭션 메시지에서 미리 지정됩니다. Click the **[!UICONTROL Test profiles]** block of the message to check the target of your proof.

   ![](assets/message-center_5.png)

### Creating a test profile outside the transactional message {#creating-a-test-profile-outside-the-transactional-----------message}

You can also create a new test profile or use one that already exists in the **[!UICONTROL Test profiles]** menu.

1. Click the **[!UICONTROL Adobe Campaign]** logo, in the top left corner, then select **[!UICONTROL Profiles & audiences]** &gt; **[!UICONTROL Test profiles]**.
1. In the **[!UICONTROL Event]** section of the page of the test profile that you have chosen, select the event that you have just created. 이 예에서는 "장바구니 포기 (Evtcartabandonment)" 를 선택합니다.
1. Specify the information to send in JSON format in the **[!UICONTROL Event data]** text box.

   ![](assets/message-center_3.png)

1. 변경 내용을 저장합니다.

이제 만든 메시지에 액세스하고 업데이트된 테스트 프로필을 선택할 수 있습니다.

**관련 항목:**

* [테스트 프로필 관리](../../sending/using/managing-test-profiles-and-sending-proofs.md)
* [대상 정의](../../audiences/using/creating-audiences.md)

## Personalizing a transactional message {#personalizing-a-transactional-message}

트랜잭션 메시지에서 개인화를 설정하려면 아래 단계를 따르십시오.

1. Click the **[!UICONTROL Content]** block to modify your message's subject and content. 이 예에서는 이미지, 스타일 시트 및 HTML 파일을 포함하는 HTML 템플릿을 가져옵니다. Importing HTML templates is presented in the [Loading an existing content](../../designing/using/selecting-an-existing-content.md) section.

   ![](assets/message-center_6.png)

1. 메시지 내용을 입력합니다. 이 예에서는 다음과 같은 세 개의 개인화 필드를 추가했습니다. 성, 마지막 제품 상담, 총 장바구니 금액. 중단된 장바구니에 대한 링크는 사용자를 장바구니에 리디렉션할 외부 URL에 대한 링크입니다. 이 매개 변수는 Adobe Campaign에서 관리되지 않습니다.

   To add fields that you defined when you created your event (see [Configuring an event](../../administration/using/configuring-transactional-messaging.md#use-case--configuring-an-event-to-send-a-transactional-message)), insert a personalization field in the message content. **[!UICONTROL Transactional event]** &gt; **[!UICONTROL Event context]**&#x200B;를 선택하여 필드를 찾을 수 있습니다.

   ![](assets/message-center_7.png)

1. 메시지의 내용을 보강하려면 이벤트를 연결한 표에서 필드를 선택하여 필드를 추가합니다. In our example, select the **[!UICONTROL Title (salutation)]** field in the **[!UICONTROL Profile]** table.

   ![](assets/message-center_7-enrichment.png)

   The steps for inserting a personalization field are detailed in the [Inserting a personalization field](../../designing/using/inserting-a-personalization-field.md) section.

   ![](assets/message-center_8.png)

1. 이 이벤트에 대해 정의한 프로필을 선택하여 메시지를 미리 봅니다.

   The steps for previewing a message are detailed in the [Previewing messages](../../sending/using/preparing-the-send.md) section.

   ![](assets/message-center_9.png)

   개인화 필드가 테스트 프로필에 입력한 정보와 일치하는지 확인할 수 있습니다. For more on this, see [Defining a test profile in a transactional message](../../channels/using/event-transactional-messages.md#defining-a-test-profile-in-a-transactional-message).

## Using product listings in a transactional message {#using-product-listings-in-a-transactional-message}

거래 이메일의 컨텐츠에서 하나 이상의 데이터 컬렉션을 참조하는 제품 목록을 만들 수 있습니다. 예를 들어 장바구니 포기 이메일에서 웹 사이트를 떠날 때 이미지, 가격 및 각 제품에 대한 링크가 포함된 모든 제품의 목록을 포함할 수 있습니다.

>[!CAUTION]
>
>Product listings are only available when editing transactional email messages through the [Email Designer](../../designing/using/about-email-content-design.md#about-the-email-designer) interface.

트랜잭션 메시지에 중단된 제품 목록을 추가하려면 아래 단계를 따르십시오.

거래 이메일에서 제품 목록을 구성하는 데 필요한 단계를 설명하는 비디오 세트를 볼 수도 있습니다. For more on this, see [this page](https://helpx.adobe.com/campaign/kt/acs/using/acs-product-listings-in-transactional-emails-feature-video-setup.html).

>[!NOTE]
>
>Adobe Campaign는 중첩된 제품 목록을 지원하지 않으며, 이것은 다른 제품 목록 내에 제품 목록을 포함할 수 없음을 의미합니다.

### Defining a product listing {#defining-a-product-listing}

트랜잭션 메시지의 제품 목록을 사용하려면 이벤트 수준에서 표시하려는 목록의 각 제품에 대한 제품 목록과 필드 목록을 정의해야 합니다. For more on this, see [Defining data collections](../../administration/using/configuring-transactional-messaging.md#defining-data-collections).

1. In the transactional message, click the **[!UICONTROL Content]** block to modify the email content.
1. 구조 구성 요소를 작업 공간으로 드래그하여 놓습니다. For more on this, see [Editing the email structure](../../designing/using/defining-the-email-structure.md#editing-the-email-structure).

   예를 들어 1 열 구조 구성 요소를 선택하고 텍스트 구성 요소, 이미지 구성 요소 및 단추 구성 요소를 추가합니다. For more on this, see [Adding fragments and components](../../designing/using/defining-the-email-structure.md#adding-fragments-and-content-components).

1. Select the structure component you just created and click the **[!UICONTROL Enable product listing]** icon from the contextual toolbar.

   ![](assets/message-center_loop_create.png)

   The structure component is highlighted with an orange frame and the **[!UICONTROL Product listing]** settings are displayed in the left palette.

   ![](assets/message-center_loop_palette.png)

1. 컬렉션의 요소가 표시되는 방식을 선택합니다.

   * **[!UICONTROL Row]**: 가로로, 즉 한 행의 각 요소를 다른 행으로 나타냅니다.
   * **[!UICONTROL Column]**: 세로 - 동일한 행에서 다른 요소 옆에 있는 각 요소를 의미합니다.
   >[!NOTE]
   >
   >**[!UICONTROL Column]** 이 옵션은 다중 열 구조 구성 요소 ( **[!UICONTROL 2:2 column]**&#x200B;및 **[!UICONTROL 3:3 column]****[!UICONTROL 4:4 column]** ) 를 사용하는 경우에만 사용할 수 있습니다. 제품 목록을 편집할 때 첫 번째 열만 채웁니다. 다른 열은 고려되지 않습니다. For more on selecting structure components, see [Editing the email structure](../../designing/using/defining-the-email-structure.md#editing-the-email-structure).

1. 트랜잭션 메시지와 관련된 이벤트를 구성할 때 만든 데이터 수집을 선택합니다. **[!UICONTROL Context]** &gt; **[!UICONTROL Real-time event]****[!UICONTROL Event context]** &gt; 노드 아래에서 찾을 수 있습니다.

   ![](assets/message-center_loop_selection.png)

   For more on configuring the event, see [Defining data collections](../../administration/using/configuring-transactional-messaging.md#defining-data-collections).

1. Use the **[!UICONTROL First item]** drop-down list to select which element will start the list displayed in the email.

   예를 들어, 2를 선택하면 컬렉션의 첫 번째 항목이 이메일에 표시되지 않습니다. 제품 목록이 두 번째 항목에서 시작됩니다.

1. 목록에 표시할 최대 항목 수를 선택합니다.

   >[!NOTE]
   >
   >If you want the elements of your list to be displayed vertically ( **[!UICONTROL Column]** ), the maximum number of items is limited according to the selected structure component (2, 3 or 4 columns). For more on selecting structure components, see [Editing the email structure](../../designing/using/defining-the-email-structure.md#editing-the-email-structure).

### Populating the product listing {#populating-the-product-listing}

거래 이메일에 연결된 이벤트에서 제품 목록을 표시하려면 아래 단계를 따르십시오.

For more on creating a collection and related fields when configuring the event, see [Defining data collections](../../administration/using/configuring-transactional-messaging.md#defining-data-collections).

1. Select the image component you inserted, select **[!UICONTROL Enable personalization]** and click the pencil in the Settings pane.

   ![](assets/message-center_loop_image.png)

1. Select **[!UICONTROL Add personalization field]** in the **[!UICONTROL Image source URL]** window that opens.

   **[!UICONTROL Context]** &gt; **[!UICONTROL Real-time event]****[!UICONTROL Event context]** &gt; 노드에서 만든 컬렉션에 해당하는 노드를 열고 (여기에서 **[!UICONTROL Product list]** ) 정의한 이미지 필드를 선택합니다 (여기에서 **[!UICONTROL Product image]** ). **[!UICONTROL Save]**&#x200B;을 클릭합니다.

   ![](assets/message-center_loop_product-image.png)

   선택한 개인화 필드가 이제 설정 창에 표시됩니다.

1. At the desired position, select **[!UICONTROL Insert personalization field]** from the contextual toolbar.

   ![](assets/message-center_loop_product.png)

1. **[!UICONTROL Context]** &gt; **[!UICONTROL Real-time event]****[!UICONTROL Event context]** &gt; 노드에서 만든 컬렉션에 해당하는 노드를 열고 (여기에서 **[!UICONTROL Product list]** ) 만든 필드를 선택합니다 (여기에서 **[!UICONTROL Product name]** ). **[!UICONTROL Confirm]**&#x200B;을 클릭합니다.

   ![](assets/message-center_loop_product_node.png)

   이제 선택한 개인화 필드가 이메일 컨텐츠의 원하는 위치에 표시됩니다.

1. 유사하게 진행하여 가격을 삽입합니다.
1. Select some text and select **[!UICONTROL Insert link]** from the contextual toolbar.

   ![](assets/message-center_loop_link_insert.png)

1. Select **[!UICONTROL Add personalization field]** in the **[!UICONTROL Insert link]** window that opens.

   **[!UICONTROL Context]** &gt; **[!UICONTROL Real-time event]****[!UICONTROL Event context]** &gt; 노드에서 만든 컬렉션에 해당하는 노드를 열고 (여기에서 **[!UICONTROL Product list]** ) 만든 URL 필드를 선택합니다 (여기에서 **[!UICONTROL Product URL]** ). **[!UICONTROL Save]**&#x200B;을 클릭합니다.

   >[!CAUTION]
   >
   >보안상의 이유로 적절한 정적 도메인 이름으로 시작되는 링크 내에 개인화 필드를 삽입해야 합니다.

   ![](assets/message-center_loop_link_select.png)

   선택한 개인화 필드가 이제 설정 창에 표시됩니다.

1. Select the structure component on which the product listing is applied and select **[!UICONTROL Show fallback]** to define a default content.

   ![](assets/message-center_loop_fallback_show.png)

1. 하나 이상의 컨텐츠 구성 요소를 드래그하고 필요에 따라 편집합니다.

   ![](assets/message-center_loop_fallback.png)

   이벤트를 실행할 때 컬렉션이 비어 있는 경우, 예를 들어 장바구니에 아무 것도 없는 경우 폴백 컨텐츠가 표시됩니다.

1. 설정 창에서 제품 목록에 대한 스타일을 편집합니다. For more on this, see [Editing email styles](../../designing/using/editing-email-styles.md).
1. 관련 거래 이벤트에 연결되고 수집 데이터를 정의한 테스트 프로필을 사용하여 이메일을 미리 봅니다. For example, add the following information in the **[!UICONTROL Event data]** section for the test profile you want to use:

   ![](assets/message-center_loop_test-profile_payload.png)

   For more on defining a test profile in a transactional message, see [this section](../../channels/using/event-transactional-messages.md#defining-a-test-profile-in-a-transactional-message).

## Testing a transactional message {#testing-a-transactional-message}

트랜잭션 메시지를 저장한 후에는 테스트를 통해 테스트할 수 있습니다.

![](assets/message-center_10.png)

The steps for sending a proof are detailed in the [Sending a proof](../../sending/using/managing-test-profiles-and-sending-proofs.md#sending-proofs) section.

## Publishing a transactional message {#publishing-a-transactional-message}

트랜잭션 메시지를 확인한 후에는 게시할 수 있습니다.

![](assets/message-center_12.png)

이제 "장바구니 포기" 이벤트가 트리거되면, 받는 사람의 제목 및 성, 장바구니 URL, 제품 목록을 정의한 적이 있는 마지막 제품 또는 제품 목록을 정의한 경우 제품 목록과 같은 메시지가 자동으로 표시되고 총 장바구니 금액이 전송됩니다.

To access reports concerning your transactional message, use the **[!UICONTROL Reports]** button. [보고서를 참조하십시오](../../reporting/using/about-dynamic-reports.md).

![](assets/message-center_13.png)

## Suspending a transactional message publication {#suspending-a-transactional-message-publication}

You can suspend publishing your transactional message by using the **[!UICONTROL Pause]** button, for example, to modify the data contained in the message. 따라서 이벤트가 더 이상 처리되지 않지만 대신 Adobe Campaign 데이터베이스의 대기열에 보관됩니다.

The queued events are kept during a period of time that is defined in the REST API (see [REST API documentation](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html)) or in the trigger event if you are using the Triggers core service (see [Working with Campaign and Experience Cloud Triggers](../../integrating/using/about-adobe-experience-cloud-triggers.md)).

![](assets/message-center_pause.png)

When clicking **[!UICONTROL Resume]**, all of the queued events (provided that they are not expired) are processed. 이제 템플릿 게재가 일시 중단된 동안 수행된 모든 수정 사항을 포함합니다.

## Unpublishing a transactional message {#unpublishing-a-transactional-message}

Clicking **[!UICONTROL Unpublish]** allows you to cancel the transactional message publication, but also the publication of the corresponding event, which deletes from the REST API the resource corresponding to the event that you previously created. 이제 이벤트가 웹 사이트를 통해 트리거되더라도 해당 메시지가 더 이상 전송되지 않고 데이터베이스에 저장됩니다.

![](assets/message-center_unpublish-template.png)

>[!NOTE]
>
>메시지를 다시 게시하려면 해당 이벤트 구성으로 돌아가서 게시한 다음 메시지를 게시해야 합니다. For more on this, see [Publishing a transactional message](../../channels/using/event-transactional-messages.md#publishing-a-transactional-message).

일시 중지된 트랜잭션 메시지를 게시 취소하는 경우 최대 24 시간까지 기다렸다가 다시 게시할 수 있습니다. This is to let the **[!UICONTROL Database cleanup]** workflow clean all the events that were sent to the queue. The steps for pausing a message are detailed in the [Suspending a transactional message publication](../../channels/using/event-transactional-messages.md#suspending-a-transactional-message-publication) section.

The **[!UICONTROL Database cleanup]** workflow, which runs every day at 4am, is accessible through **[!UICONTROL Administration]** &gt; **[!UICONTROL Application settings]** &gt; **[!UICONTROL Workflows]**.

## Deleting a transactional message {#deleting-a-transactional-message}

![](assets/message-center_delete-template.png)

By selecting a transactional message, you can delete it with the **[!UICONTROL Delete element]** button even if it has already been published. 그러나 트랜잭션 메시지 삭제는 특정 조건에서만 수행할 수 있습니다.

* **트랜잭션 메시지**: 트랜잭션 메시지를 삭제하려면 메시지가 게시 취소되고 일시 중지되지 않아야 합니다.

   트랜잭션 메시지가 게시 취소된 경우 다른 트랜잭션 메시지가 해당 이벤트에 연결되어 있지 않으면 트랜잭션 구성을 게시 취소하여 트랜잭션 메시지를 성공적으로 삭제해야 합니다. For more information on how to unpublish a transactional message, refer to this [section](../../channels/using/event-transactional-messages.md#unpublishing-a-transactional-message).

   >[!CAUTION]
   >
   >이미 알림을 보낸 트랜잭션 메시지를 삭제하면 해당 전송 및 추적 로그도 삭제됩니다.

* **기본 이벤트 템플릿 (내부 트랜잭션 메시지) 의 트랜잭션 메시지**: 내부 트랜잭션 메시지를 삭제하려면 메시지가 게시 취소되고 일시 중지되지 않아야 합니다.

   이벤트에서 유일한 트랜잭션 메시지일 수 없으며, 다른 메시지는 해당 이벤트에 링크되어야 합니다.

## Transactional message retry process {#transactional-message-retry-process}

일시적으로 배달되지 않은 트랜잭션 메시지는 배달이 만료될 때까지 수행되는 자동 재시도가 적용됩니다. For more on the delivery duration, see [Validity period parameters](../../administration/using/configuring-email-channel.md#validity-period-parameters).

트랜잭션 메시지를 보낼 수 없는 경우 두 개의 재시도 시스템이 있습니다.

* 트랜잭션 메시지 수준에서 이벤트가 실행 제공에 할당되기 전에 이벤트 수신과 배달 준비 간에 트랜잭션 메시지가 실패할 수 있습니다. [이벤트 처리 재시도 프로세스를 참조하십시오](../../channels/using/event-transactional-messages.md#event-processing-retry-process).
* 전송 프로세스 수준에서 이벤트가 실행 전달에 할당되면 임시 오류로 인해 트랜잭션 메시지가 실패할 수 있습니다. [메시지 전송 재시도 프로세스를 참조하십시오](../../channels/using/event-transactional-messages.md#message-sending-retry-process).

### Event processing retry process {#event-processing-retry-process}

이벤트를 실행 게시에 할당할 수 없는 경우 이벤트 처리가 연기됩니다. 그런 다음 재시도가 새 실행 배달에 할당될 때까지 수행됩니다.

>[!NOTE]
>
>연기된 이벤트는 아직 실행 게시에 할당되지 않았으므로 트랜잭션 메시지 전송 로그에 나타나지 않습니다.

예를 들어, 해당 컨텐츠가 올바르지 않아 실행 게시에 할당할 수 없습니다. 액세스 권한 또는 브랜딩에 문제가 있고 유형 규칙 적용 시 오류가 발생했습니다. 이 경우 메시지를 일시 중지하고 편집하여 문제를 해결하고 다시 게시할 수 있습니다. 그러면 재시도 시스템이 새 실행 배달에 해당 정보를 할당합니다.

### Message sending retry process {#message-sending-retry-process}

이벤트가 실행 전달에 할당되면 받는 사람의 사서함이 꽉 찬 경우 임시 오류로 인해 트랜잭션 메시지가 실패할 수 있습니다. For more on this, see [Retries after a delivery temporary failure](../../sending/using/understanding-delivery-failures.md#retries-after-a-delivery-temporary-failure).

>[!NOTE]
>
>이벤트가 실행 전달에 할당되면 이 실행 게재의 [전송 로그] 에 해당 이벤트가 표시됩니다. The failed deliveries are displayed in the **[!UICONTROL Execution list]** tab of the transactional message.

### Limitations {#limitations}

**로그 업데이트 전송**

재시도 프로세스에서는 새 실행 게재의 전송 로그가 즉시 업데이트되지 않습니다 (업데이트가 예약된 워크플로우를 통해 수행됨). It means that the message could be in **[!UICONTROL Pending]** status even if the transactional event has been processed by the new execution delivery.

**실패한 실행 배달**

실행 제공을 중지할 수 없습니다. 하지만 현재 실행 배달이 실패하면 새 이벤트를 수신하는 즉시 새 이벤트가 만들어지고 새 이벤트가 모두 이 실행 배달에 의해 처리됩니다. 실패한 실행 배달에 의해 새 이벤트가 처리되지 않습니다.

이미 실행 게시에 지정된 일부 이벤트가 지연되고 해당 실행 배달이 실패할 경우, 재시도 시스템에서는 지연된 이벤트를 새 실행 게시에 할당하지 않으므로 이러한 이벤트가 손실됩니다.
