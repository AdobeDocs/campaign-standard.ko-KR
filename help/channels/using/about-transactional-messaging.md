---
title: 트랜잭션 메시지 정보
seo-title: 트랜잭션 메시지 정보
description: 트랜잭션 메시지 정보
seo-description: 전송할 수 있는 다양한 유형의 트랜잭션 메시지와 Adobe Campaign에서 사용하는 방식을 살펴볼 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 8470 E 9 E 2-EE 17-456 F -9 E 4 C -460 E 69 C 78 A 2 C
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 채널
content-type: 참조
topic-tags: 트랜잭션 메시징
discoiquuid: 71 a 4 d 5 d 5-fe 2 a -4 ce 5-b 22 b-a 4736 f 7 add 83
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: d93c2600299a8d2ec3672b3d82222f423878034c

---


# About transactional messaging{#about-transactional-messaging}

Adobe Campaign에서 개인화된 트랜잭션 메시지를 만들고 관리할 수 있습니다.

트랜잭션 메시지는 웹 사이트와 같은 공급자가 사용자에게 전송하는 개별 및 고유한 커뮤니케이션입니다.

* 이 유형의 메시지는 수신자가 확인하거나 확인해야 하는 정보를 포함하므로 특히 필요합니다. 예를 들어 계정을 만든 후 환영 메시지가 될 수 있고 주문이 배송되었음을 확인, 청구 또는 암호 변경을 확인하는 메시지가 될 수 있습니다.
* 클라이언트 관계를 정의하는 중요한 메시지입니다. 사용자는 실시간으로 이 데이터를 전송할 수 있습니다. 트리거되는 이벤트와 도착하는 메시지 사이의 지연 시간이 매우 짧아야 합니다.
* 거래 메시지는 일반적으로 높은 개방 비율을 갖습니다.

Adobe Campaign를 사용하면 이 기능을 사용자 지정 트랜잭션 메시지로 변형할 이벤트를 전송하는 정보 시스템에 통합할 수 있습니다.

>[!NOTE]
>
>이메일, SMS 또는 푸시 알림은 옵션에 따라 이메일 메시지를 보낼 수 있습니다. 사용권 계약을 확인하십시오.

Adobe Campaign 에서는 두 가지 유형의 트랜잭션 메시지를 사용할 수 있습니다.

* [이벤트를](../../channels/using/event-transactional-messages.md) 타깃팅하는 이벤트 트랜잭션 메시지. 이벤트 자체에 포함된 데이터는 게재 대상을 정의하는 데 사용됩니다.
* [Adobe Campaign 마케팅 데이터베이스의 프로필 트랜잭션 메시지](../../channels/using/profile-transactional-messages.md) 타깃팅 프로필을 참조하십시오. Adobe Campaign 데이터베이스의 정보를 사용하여 고객 마케팅 프로필을 기반으로 트랜잭션 메시지를 보낼 수 있습니다.

메시지 유형은 트랜잭션 메시지로 변형될 이벤트를 구성할 때 정의됩니다. [트랜잭션 메시징 구성을 참조하십시오](../../administration/using/configuring-transactional-messaging.md).

>[!NOTE]
>
>Adobe Campaign 우선 순위를 지정하여 다른 배달을 통해 트랜잭션 메시지를 처리합니다.

트랜잭션 메시징은 Adobe Campaign Standard API 에서도 사용할 수 있습니다. For more on this, refer to the [dedicated documentation](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#about-transactional-messaging).

## Transactional messaging operating principle {#transactional-messaging-operating-principle}

웹 사이트를 운영하고 있는 회사의 예를 들어보겠습니다. 이 웹 사이트에서는 사용자가 제품을 구입할 수 있습니다.

Adobe Campaign를 사용하면 장바구니에 제품을 추가한 사이트 사용자에게 알림 이메일을 보낼 수 있습니다. 고객이 구매하지 않고 사이트를 떠나는 경우 장바구니 포기 이메일이 자동으로 발송됩니다.

이를 활용하는 단계는 다음과 같습니다.

1. " 장바구니 포기 "라는 이름의 이벤트를 구성하고 이 이벤트 구성을 게시하여 자동으로 트랜잭션 메시지를 만듭니다. Creating and publishing an event are presented in the [Configuring an event to send an event transactional message](../../administration/using/configuring-transactional-messaging.md#use-case--configuring-an-event-to-send-a-transactional-message) section.
1. 트랜잭션 메시지는 개인화되고 테스트한 다음 게시해야 합니다. [이벤트 트랜잭션 메시지를 참조하십시오](../../channels/using/event-transactional-messages.md).
1. 또한 클라이언트가 장바구니를 포기하면 이벤트가 트리거되도록 하기 위해 Adobe Campaign Standard REST API를 사용하여 회사의 웹 사이트에서 이 이벤트를 전송해야 합니다. [사이트 통합을 참조하십시오](../../administration/using/configuring-transactional-messaging.md#integrating-the-triggering-of-the-event-in-a-website).

이러한 단계를 모두 완료하면 사용자가 장바구니에 포함된 제품을 주문하지 않고 사이트를 떠나자마자 알림 이메일을 자동으로 수신하게 됩니다.

## Transactional messaging limitations {#transactional-messaging-limitations}

### Design and publication {#design-and-publication}

트랜잭션 메시지를 디자인하고 게시할 때 수행해야 하는 단계 중 일부는 되돌릴 수 없습니다. 다음 제한 사항을 알고 있어야 합니다.

* 각 이벤트 구성에 대해 하나의 채널만 사용할 수 있습니다. See [Creating an event](../../administration/using/configuring-transactional-messaging.md#creating-an-event).
* 이벤트가 만들어지면 채널은 변경할 수 없습니다. 따라서 메시지가 성공적으로 전송되지 않으면 워크플로우를 사용하여 다른 채널에서 전송할 수 있는 메커니즘을 디자인해야 합니다. [워크플로우 데이터 및 프로세스를 참조하십시오](../../automating/using/workflow-data-and-processes.md).
* You cannot change the targeting dimension ( **[!UICONTROL Real-time event]** or **[!UICONTROL Profile]** ) after the event is created. See [Creating an event](../../administration/using/configuring-transactional-messaging.md#creating-an-event).
* 발행물을 롤백할 수는 없지만 이벤트 게시를 취소할 수 있습니다. 이 작업을 수행하면 이벤트와 관련 트랜잭션 메시지에 액세스할 수 없습니다. See [Unpublishing an event](../../administration/using/configuring-transactional-messaging.md#unpublishing-an-event).
* 이벤트와 연결할 수 있는 유일한 트랜잭션 메시지는 해당 이벤트를 게시할 때 자동으로 생성되는 메시지입니다. See [Previewing and publishing the event](../../administration/using/configuring-transactional-messaging.md#previewing-and-publishing-the-event).

### Personalization {#personalization}

메시지 내용을 개인화할 수 있는 방법은 트랜잭션 메시지 유형에 따라 다릅니다. specificities are listed below:

**이벤트 기반 트랜잭션 메시지**:

* 개인화 정보는 이벤트 자체에 포함된 데이터에서 나옵니다. [이벤트 트랜잭션 메시지를 참조하십시오](../../channels/using/event-transactional-messages.md).
* You cannot use **Unsubscription link** content blocks in an event transactional message.
* 이벤트 기반 트랜잭션 메시지는 전송된 이벤트에 있는 데이터만 사용하여 받는 사람 및 메시지 컨텐츠 개인화를 정의해야 합니다. 하지만 Adobe Campaign 데이터베이스의 정보를 사용하여 트랜잭션 메시지의 컨텐츠를 강화할 수 있습니다. See [Enriching the transactional message content](../../administration/using/configuring-transactional-messaging.md#enriching-the-transactional-message-content).
* 이벤트 트랜잭션 메시지에는 프로필 정보가 포함되어 있지 않으므로 프로파일을 사용한 보강 경우에도 피로도 규칙과 호환되지 않습니다. [피로 규칙을 참조하십시오](../../administration/using/fatigue-rules.md).

**프로파일 기반의 트랜잭션 메시지**:

* 개인화 정보는 이벤트에 포함된 데이터 또는 중재된 프로필 레코드에서 가져올 수 있습니다. [프로필 트랜잭션 메시지를 참조하십시오](../../channels/using/profile-transactional-messages.md).
* You can use **Unsubscription link** content blocks in a profile transactional message. See [Adding a content block](../../designing/using/adding-a-content-block.md).
* 피로 규칙은 프로필 트랜잭션 메시지와 호환됩니다. [피로 규칙을 참조하십시오](../../administration/using/fatigue-rules.md).

제품 목록은 트랜잭션 이메일 메시지에서만 사용할 수 있습니다. See [Using product listings in a transactional message](../../channels/using/event-transactional-messages.md#using-product-listings-in-a-transactional-message).

### Permissions and branding {#permissions-and-branding}

[브랜드](../../administration/using/branding.md) 관리 측면에서 트랜잭션 메시징은 표준 메시징보다 유연성이 낮습니다. Adobe recommends linking all brands used in transactional messages to the **[!UICONTROL All]** organizational unit. 이에 대한 자세한 내용은 아래 상세 설명을 참조하십시오.

트랜잭션 메시지를 편집할 때 브랜드에 연결하여 브랜드 이름이나 브랜드 로고 등의 일부 매개 변수를 자동으로 적용할 수 있습니다. The **[!UICONTROL Default brand]** is selected by default in the transactional message properties.

![](assets/message-center_branding.png)

To access the transactional messages, you must be part of the **[!UICONTROL Message Center agents]** (mcExec) security group, which is linked to the **[!UICONTROL Message Center]** [organizational unit](../../administration/using/organizational-units.md). Therefore, all objects (including branding) used in a transactional message must be visible from the **[!UICONTROL Message Center]** organizational unit, meaning that these objects must be in the **[!UICONTROL Message Center]** or **[!UICONTROL All]** organizational units.

However, if the brand selected in the message properties is linked to an organizational unit which is different from **[!UICONTROL Message Center]** or **[!UICONTROL All]**, this will cause an error and you will not be able to send the transactional message.

Therefore, if you want to use multi-branding in the context of transactional messaging, you should link all brands either to the **[!UICONTROL Message Center]** organizational unit or to the **[!UICONTROL All]** organizational unit.

### Exporting and importing transactional messages {#exporting-and-importing-transactional-messages}

* To export a transactional message, you need to include the corresponding event configuration when [creating the package export](../../automating/using/managing-packages.md#creating-a-package).
* Once the transactional message is [imported through a package](../../automating/using/managing-packages.md#importing-a-package), it is not displayed in the transactional message list. You need to [publish](../../administration/using/configuring-transactional-messaging.md#previewing-and-publishing-the-event) the event configuration in order to make the associated transactional message available.

