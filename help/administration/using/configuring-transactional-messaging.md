---
title: 트랜잭션 메시징 구성
seo-title: 트랜잭션 메시징 구성
description: 트랜잭션 메시징 구성
seo-description: 트랜잭션 메시징을 구성하는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: 4 caeadbe-f 4 a 7-43 ce -986 d-e 99 fa 9 ca 0 d 0 d
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 관리
content-type: 참조
topic-tags: 채널 구성
discoiquuid: 3 F 968556-E 774-43 DC-A 0 B 8-7188 D 7665 FBC
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 8e2f947cce39ce08f233292d34cb4440aa48a2b5

---


# Configuring transactional messaging{#configuring-transactional-messaging}

Adobe Campaign로 트랜잭션 메시지를 전송하려면 먼저 이벤트 데이터의 구조를 설명해야 합니다.

Event configuration must be performed by an **administrator** by following the steps below:

구성은 보내려는 트랜잭션 메시지의 유형에 따라 달라질 수 있습니다. For more on this, refer to [Transactional event specific configurations](../../administration/using/configuring-transactional-messaging.md#transactional-event-specific-configurations)

이벤트가 게시되면 해당 트랜잭션 메시지가 자동으로 생성됩니다. For more on transactional messaging, refer to [this page](../../channels/using/about-transactional-messaging.md).

## Creating an event {#creating-an-event}

먼저 필요에 따라 이벤트를 만듭니다.

1. Click the **[!UICONTROL Adobe Campaign]** logo, in the top left corner, then select **[!UICONTROL Marketing plans]** &gt; **[!UICONTROL Transactional messages]** &gt; **[!UICONTROL Event configuration]**.
1. **[!UICONTROL Create]** 단추를 클릭합니다.
1. Give a **[!UICONTROL Label]** and an **[!UICONTROL ID]** to the event. **[!UICONTROL ID]** 필드는 필수이며 접두어 "evt" 로 시작해야 합니다. If you do not use this prefix, it is automatically added once you click **[!UICONTROL Create]**.

   ![](assets/message-center_1.png)

   >[!CAUTION]
   >
   >ID는 Evt 접두사를 포함하여 64 자를 초과할 수 없습니다.

1. Select the channel that will be used to send your transactional messages **[!UICONTROL Email]**, **[!UICONTROL Mobile (SMS)]** or **[!UICONTROL Mobile application]** (push notification).

   >[!NOTE]
   >
   >각 이벤트 구성에 대해 하나의 채널만 사용할 수 있습니다. 이벤트가 만들어지면 채널은 변경할 수 없습니다.

1. Select the targeting dimension corresponding to the desired event configuration and click **[!UICONTROL Create]**.

   이벤트 기반 트랜잭션 메시지는 이벤트 자체에 포함된 데이터를 기준으로 하지만, 프로필 기반의 트랜잭션 메시지는 Adobe Campaign 데이터베이스에 포함된 데이터를 타깃팅합니다. For more on this, refer to [Transactional event specific configurations](../../administration/using/configuring-transactional-messaging.md#transactional-event-specific-configurations).

## Defining the event attributes {#defining-the-event-attributes}

**[!UICONTROL Fields]** 섹션에서 이벤트 컨텐츠에 통합할 속성을 정의하면 트랜잭션 메시지를 개인화하는 데 사용할 수 있습니다.

The steps for adding and modifying fields are the same as for [custom resources](../../developing/using/configuring-the-resource-s-data-structure.md#adding-fields-to-a-resource).

![](assets/message-center_2.png)

>[!NOTE]
>
>If you want to create a multilingual transactional message, define an additional event attribute with the **[!UICONTROL AC_language]** ID. 이것은 이벤트 트랜잭션 메시지에만 적용됩니다. 이벤트가 게시되면 다국어 트랜잭션 메시지의 컨텐츠를 편집하는 단계는 다국어 표준 이메일과 동일합니다. See [Creating a multilingual email](../../channels/using/creating-a-multilingual-email.md).

## Defining data collections {#defining-data-collections}

이벤트 컨텐츠에 여러 속성을 포함한 각 요소 자체만 추가할 수 있습니다.

이 컬렉션은 거래 이메일에서 가격, 참조 번호, 수량 등과 함께 제품 목록과 같이 제품 목록에 제품 목록을 추가할 수 있습니다. 목록의 각 제품에 대해

1. **[!UICONTROL Collections]** 섹션에서 **[!UICONTROL Create element]** 단추를 클릭합니다.

   ![](assets/message-center_collection_create.png)

1. 컬렉션의 레이블과 ID를 추가합니다.
1. 목록의 각 제품에 대해 트랜잭션 메시지에 표시할 모든 필드를 추가합니다.

   이 예에서는 다음 필드를 추가했습니다.

   ![](assets/message-center_collection_fields.png)

이벤트와 메시지가 게시되면 트랜잭션 메시지에서 이 컬렉션을 사용할 수 있습니다.

다음은 이 예제에 대한 API 미리 보기입니다.

![](assets/message-center_collection_api-preview.png)

**관련 항목:**

* [이벤트 미리 보기 및 게시](../../administration/using/configuring-transactional-messaging.md#previewing-and-publishing-the-event)
* [트랜잭션 메시지의 제품 목록 사용](../../channels/using/event-transactional-messages.md#using-product-listings-in-a-transactional-message)

## Enriching the transactional message content {#enriching-the-transactional-message-content}

Adobe Campaign 데이터베이스의 정보가 포함된 트랜잭션 메시지 컨텐츠를 강화하면 메시지를 개인화할 수 있습니다. 예를 들어 각 수신자의 성 또는 CRM ID에서 전송된 정보를 개인화하기 위해 해당 주소 또는 생일 또는 프로필 테이블에 추가된 기타 사용자 정의 필드와 같은 데이터를 복구할 수 있습니다.

It is possible to enrich the transactional message content with information from extended **[!UICONTROL Profile]** or **[!UICONTROL Service]** resources.

이 정보는 새 리소스에도 저장할 수 있습니다. In that case, the resource must be linked to the **[!UICONTROL Profile]** or **[!UICONTROL Service]** resources either directly, or via another table. For example, in the configuration below, it is possible to enrich the transactional message content with information from the **[!UICONTROL Product]** resource like the product category or ID, if the **[!UICONTROL Product]** resource is linked to the **[!UICONTROL Profile]** resource.

![](assets/message-center_usecaseschema.png)

For more on resource creation and publishing, refer to [this page](../../developing/using/key-steps-to-add-a-resource.md).

1. **[!UICONTROL Enrichment]** 섹션에서 **[!UICONTROL Create element]** 단추를 클릭합니다.

   ![](assets/message-center_addenrichment.png)

1. 메시지를 연결할 리소스를 선택합니다. In this case, choose the **[!UICONTROL Profile]** resource.

   ![](assets/message-center_new-enrichment.png)

1. **[!UICONTROL Create element]** 단추를 사용하여 선택한 리소스의 필드를 이벤트에 이전에 추가한 필드 중 하나에 연결합니다 (이벤트 속성 [](../../administration/using/configuring-transactional-messaging.md#defining-the-event-attributes)정의 참조).

   ![](assets/message-center_enrichment-join.png)

1. In this example, we reconcile the **[!UICONTROL Last name]** and the **[!UICONTROL First name]** fields with the corresponding fields in the **[!UICONTROL Profile]** resource.

   ![](assets/message-center_enrichment-join-fields.png)

1. **[!UICONTROL Targeting enrichment]** 섹션에서 게재 실행 동안 메시지 타겟으로 사용될 강화를 선택합니다. In this example, select **[!UICONTROL Profile]**. 프로필 기반 이벤트에 대한 타깃팅 취약성 선택은 필수입니다.

   ![](assets/message-center_marketing_targeting_enrichment.png)

Once the event and the message are published, the link with the **[!UICONTROL Profile]** resource will allow you to enrich the content of the transactional message.

**관련 항목:**

* [이벤트 미리 보기 및 게시](../../administration/using/configuring-transactional-messaging.md#previewing-and-publishing-the-event).
* [트랜잭션 메시지](../../channels/using/event-transactional-messages.md#personalizing-a-transactional-message)개인화

## Previewing and publishing the event {#previewing-and-publishing-the-event}

이벤트를 사용하려면 먼저 미리 보고 게시해야 합니다.

1. **[!UICONTROL API preview]** 이 단추를 클릭하면 웹 사이트 개발자가 게시하기 전에 사용할 REST API의 시뮬레이션을 볼 수 있습니다. 이벤트가 게시되면 이 단추를 사용하여 프로덕션 중인 API의 미리 보기를 볼 수도 있습니다. See [Integrating the triggering of the event in a website](../../administration/using/configuring-transactional-messaging.md#integrating-the-triggering-of-the-event-in-a-website).

   ![](assets/message-center_api_preview.png)

   >[!NOTE]
   >
   >REST API는 선택한 채널 및 선택한 타깃팅 차원에 따라 다릅니다. For more details on the various configurations, refer to [Transactional event specific configurations](../../administration/using/configuring-transactional-messaging.md#transactional-event-specific-configurations).

1. Click **[!UICONTROL Publish]** to start publication.

   ![](assets/message-center_pub.png)

1. 해당 탭을 선택하여 발행물 로그를 볼 수 있습니다.

   ![](assets/message-center_logs.png)

   탭을 선택하여 이전 발행물을 참조할 수도 있습니다.

>[!NOTE]
>
>Each time you modify the event, you must click **[!UICONTROL Publish]** again to generate the updated REST API that will be used by your website developer.

이벤트가 게시되면 새 이벤트에 연결된 트랜잭션 메시지가 자동으로 생성됩니다. 이 이벤트가 트랜잭션 메시지를 보내게 하려면 방금 만들어진 메시지를 수정하고 게시해야 합니다. [이벤트 트랜잭션 메시지를 참조하십시오](../../channels/using/event-transactional-messages.md).

왼쪽 영역의 링크에서 직접 생성된 트랜잭션 메시지에 액세스할 수 있습니다.

![](assets/message-center_messagegeneration.png)

이 트리거 이벤트를 웹 사이트에 통합해야 합니다. See [Integrating the triggering of the event in a website](../../administration/using/configuring-transactional-messaging.md#integrating-the-triggering-of-the-event-in-a-website).

### Unpublishing an event {#unpublishing-an-event}

**[!UICONTROL Unpublish]** 이 단추를 사용하면 이벤트 게시를 취소할 수 있으므로 이전에 만든 이벤트에 해당하는 리소스를 REST API에서 삭제할 수 있습니다. 이제 이벤트가 웹 사이트를 통해 트리거되더라도 해당 메시지가 더 이상 전송되지 않고 데이터베이스에 저장됩니다.

![](assets/message-center_unpublish.png)

>[!NOTE]
>
>해당 트랜잭션 메시지를 이미 게시한 경우에는 트랜잭션 메시지 게시도 취소됩니다. See [Unpublishing a transactional message](../../channels/using/event-transactional-messages.md#unpublishing-a-transactional-message).

**[!UICONTROL Publish]** 단추를 클릭하여 새 REST API를 생성합니다.

## Integrating the triggering of the event in a website {#integrating-the-triggering-of-the-event-in-a-website}

이벤트를 만든 후에는 이 이벤트의 트리거와 웹 사이트를 통합해야 합니다.

[트랜잭션 메시지 작업 원칙](../../channels/using/about-transactional-messaging.md#transactional-messaging-operating-principle) 섹션에 설명된 예에서는 고객이 장바구니에 제품을 구매하기 전에 웹 사이트를 떠날 때마다 "장바구니 포기" 이벤트가 트리거되도록 해야 합니다. 이렇게 하려면 웹 사이트 웹 개발자가 Adobe Campaign Standard REST API를 사용해야 합니다.

[REST API 설명서를](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#transactional-messages-api) 참조하십시오.

## Transactional event specific configurations {#transactional-event-specific-configurations}

트랜잭션 이벤트 구성은 보내려는 트랜잭션 메시지 유형 (이벤트 또는 프로필) 와 사용할 채널에 따라 달라질 수 있습니다.

다음 섹션에서는 원하는 트랜잭션 메시지에 따라 설정해야 하는 특정 구성을 자세히 설명합니다. For more on the general steps to configure an event, refer to [Creating an event](../../administration/using/configuring-transactional-messaging.md#creating-an-event).

### Event-based transactional messages {#event-based-transactional-messages}

이벤트 기반 트랜잭션 메시지를 전송하려면 먼저 이벤트 자체에 포함된 데이터를 타깃팅한 이벤트를 만들고 구성해야 합니다.

1. When creating the event configuration, select the **[!UICONTROL Real-time event]** targeting dimension (see [Creating an event](../../administration/using/configuring-transactional-messaging.md#creating-an-event)).
1. Add fields to the event, in order to be able to personalize the transactional message (see [Defining the event attributes](../../administration/using/configuring-transactional-messaging.md#defining-the-event-attributes)).
1. Enrich the transactional message content if you want to use additional information from the Adobe Campaign database (see [Enriching the transactional message content](../../administration/using/configuring-transactional-messaging.md#enriching-the-transactional-message-content)).

   >[!NOTE]
   >
   >이벤트 기반 트랜잭션 메시지는 전송된 이벤트에 있는 데이터만 사용하여 받는 사람 및 메시지 컨텐츠 개인화를 정의해야 합니다. 하지만 Adobe Campaign 데이터베이스의 정보를 사용하여 트랜잭션 메시지의 컨텐츠를 강화할 수 있습니다.

1. Preview and publish the event (see [Previewing and publishing the event](../../administration/using/configuring-transactional-messaging.md#previewing-and-publishing-the-event)).

   이벤트를 미리 볼 때 REST API 에는 선택한 채널에 따라 이메일 주소 또는 휴대폰을 지정하는 특성이 포함됩니다.

   이벤트가 게시되면 새 이벤트에 연결된 트랜잭션 메시지가 자동으로 생성됩니다. In order for the event to trigger sending a transactional message, you must modify and publish the message that was just created, see [Event transactional messages](../../channels/using/event-transactional-messages.md).

1. Integrate the event into your website (see [Integrating the triggering of the event in a website](../../administration/using/configuring-transactional-messaging.md#integrating-the-triggering-of-the-event-in-a-website)).

### Profile-based transactional messages {#profile-based-transactional-messages}

프로필 기반 트랜잭션 메시지를 전송하려면 먼저 Adobe Campaign 데이터베이스에 포함된 이벤트 타깃팅 데이터를 만들고 구성해야 합니다.

1. When creating the event configuration, select the **[!UICONTROL Profile event]** targeting dimension (see [Creating an event](../../administration/using/configuring-transactional-messaging.md#creating-an-event)).
1. Add fields to the event, in order to be able to personalize the transactional message (see [Defining the event attributes](../../administration/using/configuring-transactional-messaging.md#defining-the-event-attributes)). 강화를 만들려면 하나 이상의 필드를 추가해야 합니다. You do not need to create other fields such as **First name** and **Last name** as you will be able to use personalization fields from the Adobe Campaign database.
1. Create an enrichment in order to link the event to the **[!UICONTROL Profile]** resource (see [Enriching the transactional message content](../../administration/using/configuring-transactional-messaging.md#enriching-the-transactional-message-content)). Creating an enrichment is mandatory when using a **[!UICONTROL Profile]** targeting dimension.
1. Preview and publish the event (see [Previewing and publishing the event](../../administration/using/configuring-transactional-messaging.md#previewing-and-publishing-the-event)).

   When previewing the event, the REST API does not contain an attribute specifying the email address or the mobile phone as it will be retrieved from the **[!UICONTROL Profile]** resource.

   이벤트가 게시되면 새 이벤트에 연결된 트랜잭션 메시지가 자동으로 생성됩니다. In order for the event to trigger sending a transactional message, you must modify and publish the message that was just created, see [Sending a profile transactional message](../../channels/using/profile-transactional-messages.md#sending-a-profile-transactional-message).

1. Integrate the event into your website (see [Integrating the triggering of the event in a website](../../administration/using/configuring-transactional-messaging.md#integrating-the-triggering-of-the-event-in-a-website)).

### Event-based transactional push notifications {#event-based-transactional-push-notifications}

트랜잭션 푸시 알림을 전송하려면 그에 따라 Adobe Campaign를 구성해야 합니다. [푸시 구성을 참조하십시오](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html).

모바일 애플리케이션에서 알림을 받도록 선택한 모든 사용자에게 익명 트랜잭션 푸시 알림을 전송하려면 먼저 이벤트 자체에 포함된 데이터를 타깃팅한 이벤트를 만들고 구성해야 합니다. 해당 단계는 아래에 나와 있습니다.

이벤트는 다음 세 가지 요소를 포함해야 합니다.

* A **registration token**, which is the user ID for one mobile application and one device. Adobe Campaign 데이터베이스의 프로필과는 일치하지 않을 수 있습니다.
* **모바일 응용 프로그램 이름** (모든 장치 - Android 및 iOS) 사용자의 장치에서 푸시 알림을 수신하는 데 사용될 Adobe Campaign에 구성된 모바일 애플리케이션의 ID 입니다. For more on this, refer to this [page](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html)
* **푸시 플랫폼** (Android의 경우 "GCM", iOS의 경우 "apns").

1. When creating the event configuration, select the **[!UICONTROL Mobile application]** channel and the **[!UICONTROL Real-time event]** targeting dimension (see [Creating an event](../../administration/using/configuring-transactional-messaging.md#creating-an-event)).
1. Add fields to the event, in order to be able to personalize the transactional message (see [Defining the event attributes](../../administration/using/configuring-transactional-messaging.md#defining-the-event-attributes)).
1. Enrich the transactional message content if you want to use additional information from Adobe Campaign database (see [Enriching the transactional message content](../../administration/using/configuring-transactional-messaging.md#enriching-the-transactional-message-content)).

   >[!NOTE]
   >
   >이벤트 기반 트랜잭션 메시지는 전송된 이벤트에 있는 데이터만 사용하여 받는 사람 및 메시지 컨텐츠 개인화를 정의해야 합니다. 하지만 Adobe Campaign 데이터베이스의 정보를 사용하여 트랜잭션 메시지의 컨텐츠를 강화할 수 있습니다.

1. Preview and publish the event (see [Previewing and publishing the event](../../administration/using/configuring-transactional-messaging.md#previewing-and-publishing-the-event)).

   이벤트를 미리 볼 때 REST API 에는 전달을 타깃팅하는 데 사용될 "registrationtoken", "application" 및 "pushplatform" 속성이 포함됩니다.

   ![](assets/message-center_push_api.png)

   이벤트가 게시되면, 새 이벤트에 연결된 트랜잭션 푸시 알림이 자동으로 생성됩니다. To modify and publish the message that was just created, see [Sending a transactional push notification targeting an event](/channels/using/transactional-push-notifications.html#sending-a-transactional-push-notification-targeting-an
----------event#sending-a-transactional-push-notification-targeting-an
----------event#sending-a-transactional-push-notification-targeting-an
----------event#sending-a-transactional-push-notification-targeting-an
----------event).

1. Integrate the event into your website (see [Integrating the triggering of the event in a website](../../administration/using/configuring-transactional-messaging.md#integrating-the-triggering-of-the-event-in-a-website)).

### Profile-based transactional push notifications {#profile-based-transactional-push-notifications}

모바일 응용 프로그램에 가입한 Adobe Campaign 프로필로 트랜잭션 푸시 알림을 전송하려면 먼저 Adobe Campaign 데이터베이스를 대상으로 하는 이벤트를 만들고 구성해야 합니다.

1. When creating the event configuration, select the **[!UICONTROL Mobile application]** channel and the **[!UICONTROL Profile]** targeting dimension (see [Creating an event](../../administration/using/configuring-transactional-messaging.md#creating-an-event)).

   기본적으로 트랜잭션 푸시 알림은 수신자가 구독한 모든 모바일 애플리케이션에 전송됩니다. 푸시 알림을 특정 모바일 애플리케이션에 전송하려면 목록에서 해당 알림을 선택합니다. 다른 모바일 애플리케이션은 메시지가 타깃팅되지만 전송에서 제외됩니다.

   ![](assets/message-center_push_appfilter.png)

1. Add fields to the event, if you want to personalize the transactional message (see [Defining the event attributes](../../administration/using/configuring-transactional-messaging.md#defining-the-event-attributes)).

   >[!NOTE]
   >
   >강화를 만들려면 하나 이상의 필드를 추가해야 합니다. You do not need to create other fields such as **First name** and **Last name** as you will be able to use personalization fields from the Adobe Campaign database.

1. Create an enrichment in order to link the event to the **[!UICONTROL Profile]** resource (see [Enriching the transactional message content](../../administration/using/configuring-transactional-messaging.md#enriching-the-transactional-message-content)). Creating an enrichment is mandatory when using a **[!UICONTROL Profile]** targeting dimension.
1. Preview and publish the event (see [Previewing and publishing the event](../../administration/using/configuring-transactional-messaging.md#previewing-and-publishing-the-event)).

   When previewing the event, the REST API does not contain an attribute specifying the registration token, the application name and the push platform as they will be retrieved from the **[!UICONTROL Profile]** resource.

   이벤트가 게시되면, 새 이벤트에 연결된 트랜잭션 푸시 알림이 자동으로 생성됩니다. To modify and publish the message that was just created, see [Sending a transactional push notification targeting a profile](/channels/using/transactional-push-notifications.html#sending-a-transactional-push-notification-targeting-a
----------profile#sending-a-transactional-push-notification-targeting-a
----------profile#sending-a-transactional-push-notification-targeting-a
----------profile#sending-a-transactional-push-notification-targeting-a
----------profile).

1. Integrate the event into your website (see [Integrating the triggering of the event in a website](../../administration/using/configuring-transactional-messaging.md#integrating-the-triggering-of-the-event-in-a-website)).

### Configuring an event to send a follow-up message {#configuring-an-event-to-send-a-follow-up-message}

후속 메시지는 특정 트랜잭션 메시지의 수신자에게 메시지를 보내는 워크플로우에서 사용할 수 있는 사전 정의된 마케팅 배달 템플릿입니다. For more on this, see [Follow-up messages](../../channels/using/follow-up-messages.md).

1. 생성된 동일한 이벤트 구성을 사용하여 이벤트 트랜잭션 메시지를 보냅니다. [이벤트 기반 트랜잭션 메시지를 참조하십시오](../../administration/using/configuring-transactional-messaging.md#event-based-transactional-messages).
1. When configuring your event, check the **[!UICONTROL Create follow-up delivery template for this event]** box before publishing the event.

   ![](assets/message-center_follow-up-checkbox.png)

1. Preview and publish the event (see [Previewing and publishing the event](../../administration/using/configuring-transactional-messaging.md#previewing-and-publishing-the-event)).

   이벤트가 게시되면, 트랜잭션 메시지와 새 이벤트에 연결된 후속 배달 템플릿이 자동으로 만들어집니다. For more on using follow-up messages, see [Sending a follow-up message](../../channels/using/follow-up-messages.md#sending-a-follow-up-message).

## Use case: configuring an event to send a transactional message {#use-case--configuring-an-event-to-send-a-transactional-message}

이 예에서는 다음 전제 조건으로 웹 사이트에서 각 구매 후 확인 메시지를 보내도록 이벤트를 구성합니다.

As we want to identify our client via his CRM ID, first make sure that the **[!UICONTROL Profile]** resource has been extended with this new field.

In the same way, a custom resource corresponding to purchases must have been created and published, and must be linked to the **[!UICONTROL Profile]** resource. 이렇게 하면 이 리소스에서 정보를 검색하여 메시지 내용을 강화할 수 있습니다.

For more on resource creation and publishing, refer to [this page](../../developing/using/key-steps-to-add-a-resource.md).

1. **[!UICONTROL Email]** 채널과 **[!UICONTROL Profile]** 타깃팅 차원을 사용하여 새 이벤트를 만듭니다 (이벤트 [](../../administration/using/configuring-transactional-messaging.md#creating-an-event)만들기 참조).
1. 트랜잭션 메시지를 개인화하는 데 사용할 속성을 정의합니다. In our case, add the "CRM ID" and the "Product identifier" fields (see [Defining the event attributes](../../administration/using/configuring-transactional-messaging.md#defining-the-event-attributes)).

   ![](assets/message-center_usecase1.png)

1. To enrich the message content with information regarding the client's previous purchases, create an enrichment targeting the **[!UICONTROL Purchase]** resource (see [Enriching the transactional message content](../../administration/using/configuring-transactional-messaging.md#enriching-the-transactional-message-content)).

   ![](assets/message-center_usecase2.png)

1. Create a join condition between the "Product identifier" field that was previously added to the message, and the corresponding field from the **[!UICONTROL Purchase]** resource

   ![](assets/message-center_usecase3.png)

1. Preview and publish the event (see [Previewing and publishing the event](../../administration/using/configuring-transactional-messaging.md#previewing-and-publishing-the-event)).
1. Integrate the event in your website (see [Integrating the triggering of the event in a website](../../administration/using/configuring-transactional-messaging.md#integrating-the-triggering-of-the-event-in-a-website)).

