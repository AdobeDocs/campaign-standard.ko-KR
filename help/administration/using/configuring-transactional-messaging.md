---
title: 트랜잭션 메시지 구성
description: 트랜잭션 메시지를 구성하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: 4caeadbe-f4a7-43ce-986d-e99fa9ca0d0d
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: configuring-channels
discoiquuid: 3f968556-e774-43dc-a0b8-7188d7665fbc
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e31e8c63fa94d190211c7a51e7f1091657c9f479

---


# 트랜잭션 메시지 구성{#configuring-transactional-messaging}

Adobe Campaign을 사용하여 트랜잭션 메시지를 전송하려면 먼저 이벤트 데이터의 구조를 설명해야 합니다.

이벤트 구성은 **관리자가** 아래 단계에 따라 수행해야 합니다.

구성은 전송하려는 트랜잭션 메시지 유형에 따라 달라질 수 있습니다. 자세한 내용은 트랜잭션 이벤트 [특정 구성을 참조하십시오.](#transactional-event-specific-configurations)

이벤트가 게시되면 해당 트랜잭션 메시지가 자동으로 만들어집니다. 트랜잭션 메시지에 대한 자세한 내용은 [이 페이지를](../../channels/using/about-transactional-messaging.md)참조하십시오.

## 이벤트 만들기 {#creating-an-event}

먼저 필요에 따라 이벤트를 만듭니다.

1. 왼쪽 상단 모서리에서 **[!UICONTROL Adobe Campaign]**로고를 클릭한 다음**[!UICONTROL Marketing plans]** > **[!UICONTROL Transactional messages]**>**[!UICONTROL Event configuration]**&#x200B;를 선택합니다.
1. 단추를 **[!UICONTROL Create]**클릭합니다.
1. 이벤트에 **[!UICONTROL Label]**유용한 정보를**[!UICONTROL ID]** 제공합니다. 이 **[!UICONTROL ID]**필드는 필수로 사용할 수 있으며 접두사 &quot;EVT&quot;로 시작해야 합니다. 이 접두사를 사용하지 않으면 클릭하면 자동으로 추가됩니다**[!UICONTROL Create]**.

   ![](assets/message-center_1.png)

   >[!IMPORTANT]
   >
   >ID는 EVT 접두사를 포함하여 64자를 초과할 수 없습니다.

1. 트랜잭션 메시지를 보내는 데 사용할 채널을 **[!UICONTROL Email]**선택하거나**[!UICONTROL Mobile (SMS)]** (푸시 알림) **[!UICONTROL Mobile application]**을 선택합니다.

   >[!NOTE]
   >
   >각 이벤트 구성에는 하나의 채널만 사용할 수 있습니다. 이벤트가 만들어지면 채널을 변경할 수 없습니다.

1. 원하는 이벤트 구성에 해당하는 타깃팅 차원을 선택하고 을 **[!UICONTROL Create]**클릭합니다.

   이벤트 기반 트랜잭션 메시지 대상 데이터는 이벤트 자체에 포함된 반면 프로필 기반 트랜잭션 메시지는 Adobe Campaign 데이터베이스에 들어 있는 대상 데이터입니다. 자세한 내용은 트랜잭션 이벤트 [특정 구성을](#transactional-event-specific-configurations)참조하십시오.

## 이벤트 속성 정의 {#defining-the-event-attributes}

섹션에서 이벤트 컨텐츠에 통합될 속성을 정의한 다음 트랜잭션 메시지를 개인화하는 데 사용할 수 있습니다. **[!UICONTROL Fields]**

필드를 추가 및 수정하는 단계는 [사용자 지정 리소스의](../../developing/using/configuring-the-resource-s-data-structure.md#adding-fields-to-a-resource)경우와 동일합니다.

![](assets/message-center_2.png)

>[!NOTE]
>
>다국어 트랜잭션 메시지를 만들려면 ID로 추가 이벤트 속성을 **[!UICONTROL AC_language]**정의합니다. 이것은 이벤트 트랜잭션 메시지에만 적용됩니다. 이벤트가 게시되면 다국어 트랜잭션 메시지의 컨텐츠를 편집하는 단계는 다국어 표준 이메일과 동일합니다. See[Creating a multilingual email](../../channels/using/creating-a-multilingual-email.md).

## 데이터 컬렉션 정의 {#defining-data-collections}

여러 속성을 포함하는 각 요소 자체를 이벤트 컨텐츠에 요소 모음을 추가할 수 있습니다.

이 컬렉션은 트랜잭션 이메일에서 제품 목록을 사용하여 제품 목록(예: 가격, 참조 번호, 수량 등)과 같은 메시지 내용에 추가할 수 있습니다. for each product of the list.

1. 섹션에서 **[!UICONTROL Collections]****[!UICONTROL Create element]** 단추를 클릭합니다.

   ![](assets/message-center_collection_create.png)

1. 컬렉션에 대한 레이블 및 ID를 추가합니다.
1. 목록의 각 제품에 대한 트랜잭션 메시지에 표시할 필드를 모두 추가합니다.

   이 예에서는 다음 필드를 추가했습니다.

   ![](assets/message-center_collection_fields.png)

이벤트와 메시지가 게시되면 이 컬렉션을 거래 메시지에서 사용할 수 있습니다.

다음은 이 예제의 API 미리 보기입니다.

![](assets/message-center_collection_api-preview.png)

**관련 항목:**

* [이벤트 미리 보기 및 게시](#previewing-and-publishing-the-event)
* [트랜잭션 메시지에서 제품 목록 사용](../../channels/using/event-transactional-messages.md#using-product-listings-in-a-transactional-message)

## 트랜잭션 메시지 컨텐츠 강화 {#enriching-the-transactional-message-content}

Adobe Campaign 데이터베이스의 정보로 트랜잭션 메시지 컨텐츠를 강화하면 메시지를 개인화할 수 있습니다. 예를 들어 각 수신자의 성 또는 CRM ID에서 주소 또는 생년월일 또는 프로필 테이블에 추가된 기타 사용자 정의 필드와 같은 데이터를 복구하여 수신자에게 전송되는 정보를 개인화할 수 있습니다.

확장된 **[!UICONTROL Profile]**또는**[!UICONTROL Service]** 리소스의 정보로 트랜잭션 메시지 컨텐츠를 보완할 수 있습니다.

이 정보는 새 리소스에 저장할 수도 있습니다. 이 경우 리소스는 직접 또는 다른 표를 통해 **[!UICONTROL Profile]**또는**[!UICONTROL Service]** 리소스에 연결되어 있어야 합니다. 예를 들어 아래 구성에서 리소스가 **[!UICONTROL Product]**리소스에 연결된 경우 제품 카테고리 또는 ID와 같은**[!UICONTROL Product]** **[!UICONTROL Profile]**리소스의 정보로 트랜잭션 메시지 컨텐츠를 보완할 수 있습니다.

![](assets/message-center_usecaseschema.png)

리소스 만들기 및 게시에 대한 자세한 내용은 [이 페이지를](../../developing/using/key-steps-to-add-a-resource.md)참조하십시오.

1. 섹션에서 **[!UICONTROL Enrichment]****[!UICONTROL Create element]** 단추를 클릭합니다.

   ![](assets/message-center_addenrichment.png)

1. 메시지를 연결할 리소스를 선택합니다. 이 경우 **[!UICONTROL Profile]**리소스를 선택합니다.

   ![](assets/message-center_new-enrichment.png)

1. 이 **[!UICONTROL Create element]**단추를 사용하여 선택한 리소스의 필드를 이전에 이벤트에 추가한 필드 중 하나로 연결합니다(이벤트 속성[정의 참조](#defining-the-event-attributes)).

   ![](assets/message-center_enrichment-join.png)

1. 이 예에서는 **[!UICONTROL Last name]**리소스의 해당 필드와**[!UICONTROL First name]** 및 **[!UICONTROL Profile]**필드를 조정합니다.

   ![](assets/message-center_enrichment-join-fields.png)

   또한 **[!UICONTROL Service]**리소스를 사용하여 트랜잭션 메시지 컨텐츠를 강화할 수 있습니다. 자세한 내용은 을 참조하십시오.

1. 이 **[!UICONTROL Targeting enrichment]**섹션에서 전달 실행 중에 메시지 대상으로 사용할 농축도를 선택합니다. 이 예에서는 을**[!UICONTROL Profile]**&#x200B;선택합니다. 프로필 기반 이벤트에 타깃팅 요소 선택은 필수입니다.

   ![](assets/message-center_marketing_targeting_enrichment.png)

이벤트와 메시지가 게시되면, **[!UICONTROL Profile]**리소스와 연결된 링크를 통해 트랜잭션 메시지의 컨텐츠를 보완할 수 있습니다.

**관련 항목:**

* [이벤트](#previewing-and-publishing-the-event)미리 보기 및 게시.
* [트랜잭션 메시지](../../channels/using/event-transactional-messages.md#personalizing-a-transactional-message)개인화

## 이벤트 미리 보기 및 게시 {#previewing-and-publishing-the-event}

이벤트를 사용하기 전에 미리 보고 게시해야 합니다.

1. 웹 사이트 개발자가 REST API를 게시하기 전에 사용할 시뮬레이션을 보려면 이 **[!UICONTROL API preview]**단추를 클릭합니다. 이벤트가 게시되면 제작 중인 API의 미리 보기도 가능합니다. 웹[사이트에서](#integrating-the-triggering-of-the-event-in-a-website)이벤트 트리거 통합을 참조하십시오.

   ![](assets/message-center_api_preview.png)

   >[!NOTE]
   >
   >REST API는 선택한 채널과 선택한 타깃팅 차원에 따라 다릅니다. 다양한 구성에 대한 자세한 내용은 트랜잭션 이벤트 [특정 구성을](#transactional-event-specific-configurations)참조하십시오.

1. 게시를 **[!UICONTROL Publish]**시작하려면 클릭합니다.

   ![](assets/message-center_pub.png)

1. 해당 탭을 선택하여 게시 로그를 볼 수 있습니다.

   ![](assets/message-center_logs.png)

   탭을 선택하여 이전 발행물을 참조할 수도 있습니다.

>[!NOTE]
>
>이벤트를 수정할 때마다 웹 사이트 개발자가 사용할 업데이트된 REST API를 생성하려면 **[!UICONTROL Publish]**다시 클릭해야 합니다.

이벤트가 게시되면 새 이벤트에 연결된 트랜잭션 메시지가 자동으로 만들어집니다. 이 이벤트가 트랜잭션 메시지 전송을 트리거하려면 방금 만든 메시지를 수정하고 게시해야 합니다. See [Event transactional messages](../../channels/using/event-transactional-messages.md).

왼쪽 영역의 링크에서 직접 만든 트랜잭션 메시지에 액세스할 수 있습니다.

![](assets/message-center_messagegeneration.png)

또한 이 트리거 이벤트를 웹 사이트에 통합해야 합니다. 웹 [사이트에서](#integrating-the-triggering-of-the-event-in-a-website)이벤트 트리거 통합을 참조하십시오.

### 이벤트 게시 취소 {#unpublishing-an-event}

이 **[!UICONTROL Unpublish]**단추를 사용하면 이벤트 게시를 취소할 수 있으며, 이 게시물은 이전에 만든 이벤트에 해당하는 리소스를 REST API에서 삭제합니다. 이제 웹 사이트를 통해 이벤트가 트리거되더라도 해당 메시지는 더 이상 전송되지 않고 데이터베이스에 저장되지 않습니다.

![](assets/message-center_unpublish.png)

>[!NOTE]
>
>해당 트랜잭션 메시지를 이미 게시한 경우 트랜잭션 메시지 게시가 취소됩니다. 트랜잭션 [메시지](../../channels/using/event-transactional-messages.md#unpublishing-a-transactional-message)게시 취소를 참조하십시오.

단추를 클릭하여 새 REST API를 생성합니다. **[!UICONTROL Publish]**

## 웹 사이트에서 이벤트 트리거 통합 {#integrating-the-triggering-of-the-event-in-a-website}

이벤트를 만든 후에는 이 이벤트의 트리거를 웹 사이트에 통합해야 합니다.

트랜잭션 메시징 운영 [원칙](../../channels/using/about-transactional-messaging.md#transactional-messaging-operating-principle) 섹션에 설명된 예에서, 클라이언트 중 하나가 장바구니에서 제품을 구매하기 전에 웹 사이트를 떠날 때마다 &quot;장바구니 포기&quot; 이벤트를 트리거할 수 있습니다. 이렇게 하려면 웹 사이트 웹 개발자가 Adobe Campaign Standard REST API를 사용해야 합니다.

REST [API 설명서를 참조하십시오](../../api/using/managing-transactional-messages.md) .

## 트랜잭션 이벤트 특정 구성 {#transactional-event-specific-configurations}

트랜잭션 이벤트 구성은 전송하려는 트랜잭션 메시지 유형(이벤트 또는 프로필) 및 사용될 채널에 따라 달라질 수 있습니다.

다음 섹션에서는 원하는 트랜잭션 메시지에 따라 어떤 구성을 설정해야 하는지 자세히 설명합니다. 이벤트 구성 일반 단계에 대한 자세한 내용은 이벤트 [만들기를](#creating-an-event)참조하십시오.

### 이벤트 기반의 트랜잭션 메시지 {#event-based-transactional-messages}

이벤트 기반 트랜잭션 메시지를 전송하려면 먼저 이벤트 자체에 포함된 데이터를 대상으로 하는 이벤트를 만들고 구성해야 합니다.
자세한 내용은 트랜잭션 [메시징을](https://helpx.adobe.com/campaign/kb/simplify-campaign-management.html#Managedatatofuelengagingexperiences)사용한 참여를 참조하십시오.

1. 이벤트 구성을 만들 때 **[!UICONTROL Real-time event]**타깃팅 차원을 선택합니다(이벤트[만들기](#creating-an-event)참조).
1. 트랜잭션 메시지를 개인화할 수 있도록 이벤트에 필드를 추가합니다(이벤트 속성 [정의 참조](#defining-the-event-attributes)).
1. Adobe Campaign 데이터베이스의 추가 정보를 사용하려면 트랜잭션 메시지 컨텐츠를 [보완합니다(트랜잭션 메시지 컨텐츠](#enriching-the-transactional-message-content)강화 참조).

   >[!NOTE]
   >
   >이벤트 기반 트랜잭션 메시지는 보낸 이벤트에 있는 데이터만 사용하여 받는 사람과 메시지 컨텐츠 개인화를 정의해야 합니다. 그러나 Adobe Campaign 데이터베이스의 정보를 사용하여 트랜잭션 메시지의 컨텐츠를 강화할 수 있습니다.

1. 이벤트 미리 보기 및 게시(이벤트 [미리 보기 및 게시](#previewing-and-publishing-the-event)참조)

   이벤트를 미리 볼 때 REST API에는 선택한 채널에 따라 이메일 주소 또는 휴대폰을 지정하는 속성이 포함됩니다.

   이벤트가 게시되면 새 이벤트에 연결된 트랜잭션 메시지가 자동으로 만들어집니다. 이벤트가 트랜잭션 메시지 전송을 트리거하려면 방금 만든 메시지를 수정 및 게시해야 합니다. 이벤트 트랜잭션 [메시지를](../../channels/using/event-transactional-messages.md)참조하십시오.

1. 이벤트를 웹 사이트에 통합합니다(웹 사이트에서 [이벤트 트리거](#integrating-the-triggering-of-the-event-in-a-website)통합 참조).

### 프로파일 기반의 트랜잭션 메시지 {#profile-based-transactional-messages}

프로필 기반 트랜잭션 메시지를 전송하려면 먼저 Adobe Campaign 데이터베이스에 포함된 이벤트 타깃팅 데이터를 만들고 구성해야 합니다.

1. 이벤트 구성을 만들 때 **[!UICONTROL Profile event]**타깃팅 차원을 선택합니다(이벤트[만들기](#creating-an-event)참조).
1. 트랜잭션 메시지를 개인화할 수 있도록 이벤트에 필드를 추가합니다(이벤트 속성 [정의 참조](#defining-the-event-attributes)). 농축하려면 최소한 하나의 필드를 추가해야 합니다. Adobe Campaign 데이터베이스의 개인화 필드를 사용할 수 있으므로 **이름** 및 **성과** 같은 다른 필드를 만들 필요가 없습니다.
1. 이벤트를 **[!UICONTROL Profile]**리소스에 연결하려면 추가 정보 만들기를 참조하십시오(트랜잭션 메시지 컨텐츠[](#enriching-the-transactional-message-content)강화 참조). 타깃팅 차원을 사용할 때는**[!UICONTROL Profile]** 데이터 웨어하우스를 만들어야 합니다.
1. 이벤트 미리 보기 및 게시(이벤트 [미리 보기 및 게시](#previewing-and-publishing-the-event)참조)

   이벤트를 미리 볼 때 REST API에는 **[!UICONTROL Profile]**리소스에서 검색할 이메일 주소 또는 휴대 전화를 지정하는 속성이 포함되어 있지 않습니다.

   이벤트가 게시되면 새 이벤트에 연결된 트랜잭션 메시지가 자동으로 만들어집니다. 이벤트가 트랜잭션 메시지 전송을 트리거하려면 방금 만든 메시지를 수정 및 게시해야 합니다. 프로필 트랜잭션 메시지 [전송을](../../channels/using/profile-transactional-messages.md#sending-a-profile-transactional-message)참조하십시오.

1. 이벤트를 웹 사이트에 통합합니다(웹 사이트에서 [이벤트 트리거](#integrating-the-triggering-of-the-event-in-a-website)통합 참조).

### 이벤트 기반의 트랜잭션 푸시 알림 {#event-based-transactional-push-notifications}

트랜잭션 푸시 알림을 전송하려면 그에 따라 Adobe Campaign을 구성해야 합니다. 푸시 [구성을](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html)참조하십시오.

모바일 응용 프로그램에서 알림을 수신하도록 선택한 모든 사용자에게 익명 트랜잭션 푸시 알림을 전송하려면 먼저 이벤트 자체에 포함된 데이터를 대상으로 하는 이벤트를 만들고 구성해야 합니다. 해당 단계는 아래에 나와 있습니다.

이벤트는 다음 세 가지 요소를 포함해야 합니다.

* 하나의 모바일 응용 프로그램 및 하나의 장치에 대한 사용자 ID인 **등록 토큰입니다**. Adobe Campaign 데이터베이스의 프로필에 해당되지 않을 수 있습니다.
* 모바일 응용 프로그램 이름 **** (모든 장치용 하나 - Android 및 iOS). 사용자의 장치에서 푸시 알림을 받는 데 사용되는 Adobe Campaign에 구성된 모바일 애플리케이션의 ID입니다. 자세한 내용은 이 [페이지를 참조하십시오.](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html)
* Android의 경우 &quot;gcm&quot;, iOS의 경우 &quot;apns&quot;) **푸시 플랫폼** .

1. 이벤트 구성을 만들 때 **[!UICONTROL Mobile application]**채널과**[!UICONTROL Real-time event]** 타깃팅 차원을 선택합니다(이벤트 [만들기 참조](#creating-an-event)).
1. 트랜잭션 메시지를 개인화할 수 있도록 이벤트에 필드를 추가합니다(이벤트 속성 [정의 참조](#defining-the-event-attributes)).
1. Adobe Campaign 데이터베이스의 추가 정보를 사용하려면 트랜잭션 메시지 컨텐츠를 [보완합니다(트랜잭션 메시지 컨텐츠](#enriching-the-transactional-message-content)강화 참조).

   >[!NOTE]
   >
   >이벤트 기반 트랜잭션 메시지는 보낸 이벤트에 있는 데이터만 사용하여 받는 사람과 메시지 컨텐츠 개인화를 정의해야 합니다. 그러나 Adobe Campaign 데이터베이스의 정보를 사용하여 트랜잭션 메시지의 컨텐츠를 강화할 수 있습니다.

1. 이벤트 미리 보기 및 게시(이벤트 [미리 보기 및 게시](#previewing-and-publishing-the-event)참조)

   이벤트를 미리 볼 때 REST API에는 배달을 대상으로 하는 데 사용할 &quot;registrationToken&quot;, &quot;application&quot; 및 &quot;pushPlatform&quot; 속성이 포함됩니다.

   ![](assets/message-center_push_api.png)

   이벤트가 게시되면 새 이벤트에 연결된 트랜잭션 푸시 알림이 자동으로 만들어집니다. 방금 만든 메시지를 수정하고 게시하려면 이벤트를 [타깃팅하는 트랜잭션 푸시 알림 전송을 참조하십시오](../../channels/using/transactional-push-notifications.md#transactional-push-notifications-targeting-an-event).

1. 이벤트를 웹 사이트에 통합합니다(웹 사이트에서 [이벤트 트리거](#integrating-the-triggering-of-the-event-in-a-website)통합 참조).

### 프로파일 기반의 트랜잭션 푸시 알림 {#profile-based-transactional-push-notifications}

모바일 애플리케이션을 구독한 Adobe Campaign 프로필로 트랜잭션 푸시 알림을 전송하려면 먼저 Adobe Campaign 데이터베이스를 대상으로 하는 이벤트를 만들고 구성해야 합니다.

1. 이벤트 구성을 만들 때 **[!UICONTROL Mobile application]**채널과**[!UICONTROL Profile]** 타깃팅 차원을 선택합니다(이벤트 [만들기 참조](#creating-an-event)).

   기본적으로 트랜잭션 푸시 알림은 수신자가 가입한 모든 모바일 애플리케이션으로 전송됩니다. 푸시 알림을 특정 모바일 애플리케이션으로 전송하려면 목록에서 선택합니다. 다른 모바일 응용 프로그램은 메시지의 대상이 되지만 전송에서 제외됩니다.

   ![](assets/message-center_push_appfilter.png)

1. 트랜잭션 메시지를 개인화하려면 이벤트에 필드를 추가합니다(이벤트 속성 [정의 참조](#defining-the-event-attributes)).

   >[!NOTE]
   >
   >농축하려면 최소한 하나의 필드를 추가해야 합니다. Adobe Campaign 데이터베이스의 개인화 필드를 사용할 수 있으므로 **이름** 및 **성과** 같은 다른 필드를 만들 필요가 없습니다.

1. 이벤트를 **[!UICONTROL Profile]**리소스에 연결하려면 추가 정보 만들기를 참조하십시오(트랜잭션 메시지 컨텐츠[](#enriching-the-transactional-message-content)강화 참조). 타깃팅 차원을 사용할 때는**[!UICONTROL Profile]** 데이터 웨어하우스를 만들어야 합니다.
1. 이벤트 미리 보기 및 게시(이벤트 [미리 보기 및 게시](#previewing-and-publishing-the-event)참조)

   이벤트를 미리 볼 때 REST API에는 **[!UICONTROL Profile]**리소스에서 검색할 등록 토큰, 응용 프로그램 이름 및 푸시 플랫폼을 지정하는 속성이 포함되어 있지 않습니다.

   이벤트가 게시되면 새 이벤트에 연결된 트랜잭션 푸시 알림이 자동으로 만들어집니다. 방금 만든 메시지를 수정 및 게시하려면 프로필을 [대상으로 하는 트랜잭션 푸시 알림 전송을 참조하십시오](../../channels/using/transactional-push-notifications.md#transactional-push-notifications-targeting-a-profile).

1. 이벤트를 웹 사이트에 통합합니다(웹 사이트에서 [이벤트 트리거](#integrating-the-triggering-of-the-event-in-a-website)통합 참조).

### 후속 메시지를 보내도록 이벤트 구성 {#configuring-an-event-to-send-a-follow-up-message}

후속 메시지는 특정 트랜잭션 메시지의 수신자에게 메시지를 보내는 워크플로우에 사용할 수 있는 사전 정의된 마케팅 전달 템플릿입니다. 자세한 내용은 후속 [메시지를](../../channels/using/follow-up-messages.md)참조하십시오.

1. 이벤트 트랜잭션 메시지를 전송하기 위해 만든 것과 동일한 이벤트 구성을 사용합니다. 이벤트 [기반의 트랜잭션 메시지를](#event-based-transactional-messages)참조하십시오.
1. 이벤트를 구성할 때 이벤트를 게시하기 전에 **[!UICONTROL Create follow-up delivery template for this event]**상자를 선택합니다.

   ![](assets/message-center_follow-up-checkbox.png)

1. 이벤트 미리 보기 및 게시(이벤트 [미리 보기 및 게시](#previewing-and-publishing-the-event)참조)

   이벤트가 게시되면 트랜잭션 메시지와 새 이벤트에 연결된 후속 배달 템플릿이 자동으로 만들어집니다. 후속 메시지 사용에 대한 자세한 내용은 [후속 메시지](../../channels/using/follow-up-messages.md#sending-a-follow-up-message)전송을 참조하십시오.

## 사용 사례:트랜잭션 메시지를 보낼 이벤트 구성 {#use-case--configuring-an-event-to-send-a-transactional-message}

이 예에서는 다음 전제 조건이 있는 웹 사이트의 각 구매 후 확인 메시지를 전송하기 위해 이벤트를 구성하려고 합니다.

CRM ID를 통해 클라이언트를 확인하려면 먼저 이 새 필드를 사용하여 **[!UICONTROL Profile]**리소스가 확장되었는지 확인하십시오.

이와 마찬가지로 구매에 해당하는 사용자 지정 리소스가 만들어지고 게시되어야 하며 **[!UICONTROL Profile]**리소스에 연결되어 있어야 합니다. 이렇게 하면 이 리소스에서 정보를 검색하여 메시지 내용을 보완할 수 있습니다.

리소스 만들기 및 게시에 대한 자세한 내용은 [이 페이지를](../../developing/using/key-steps-to-add-a-resource.md)참조하십시오.

1. 채널과 타깃팅 차원을 사용하여 새 이벤트를 **[!UICONTROL Email]**만듭니다(이벤트**[!UICONTROL Profile]** [](#creating-an-event)만들기 참조).
1. 트랜잭션 메시지를 개인화하는 데 사용할 수 있는 속성을 정의합니다. 이 경우 &quot;CRM ID&quot; 및 &quot;제품 식별자&quot; 필드를 추가합니다(이벤트 속성 [정의 참조](#defining-the-event-attributes)).

   ![](assets/message-center_usecase1.png)

1. 클라이언트의 이전 구매와 관련된 정보로 메시지 컨텐츠를 강화하려면 **[!UICONTROL Purchase]**리소스를 대상으로[더 많은 기능을 만드십시오(트랜잭션 메시지 컨텐츠](#enriching-the-transactional-message-content)강화 참조).

   ![](assets/message-center_usecase2.png)

1. 이전에 메시지에 추가된 &quot;제품 식별자&quot; 필드와 **[!UICONTROL Purchase]**리소스에서 해당 필드 사이에 조인 조건을 만듭니다

   ![](assets/message-center_usecase3.png)

1. 이벤트 미리 보기 및 게시(이벤트 [미리 보기 및 게시](#previewing-and-publishing-the-event)참조)
1. 웹 사이트에서 이벤트를 통합합니다(웹 [사이트에서](#integrating-the-triggering-of-the-event-in-a-website)이벤트 트리거 통합 참조).

