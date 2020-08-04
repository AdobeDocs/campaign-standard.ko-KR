---
title: 트랜잭션 메시지 기본 정보
description: 보낼 수 있는 다양한 유형의 트랜잭션 메시지와 Adobe Campaign에서 이를 사용하는 방법에 대해 살펴봅니다.
page-status-flag: never-activated
uuid: 8470e9e2-ee17-456f-9e4c-460e69c78a2c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: transactional-messaging
discoiquuid: 71a4d5d5-fe2a-4ce5-b22b-a4736f7add83
internal: n
snippet: y
translation-type: ht
source-git-commit: 68e825bc3b6b7f94f61875e7da2bc8f63f06d9cb
workflow-type: ht
source-wordcount: '1147'
ht-degree: 100%

---


# 트랜잭션 메시지 기본 정보{#about-transactional-messaging}

Adobe Campaign에서는 개인화된 트랜잭션 메시지를 만들고 관리할 수 있습니다.

트랜잭션 메시지는 웹사이트 등 공급자가 사용자에게 보내는 개별적이고 고유한 통신입니다.

* 수신자는 이런 유형의 메시지를 특히 기대하게 됩니다. 수신자가 확인하거나 확정하려는 정보가 포함되어 있기 때문입니다. 예를 들어 계정을 만든 후의 환영 메시지가 될 수도 있고, 주문 물품이 배송되었다는 확인 메일, 청구서, 또는 암호 변경 확인 메시지가 될 수도 있습니다.
* 이는 고객과의 관계를 정의하는 중요한 메시지입니다. 사용자는 이런 메시지를 실시간으로 받을 것이라고 기대합니다. 따라서 트리거된 이벤트와 메시지 도착 사이의 지연 시간이 매우 짧아야 합니다.
* 트랜잭션 메시지는 보통 오픈율이 높습니다.

Adobe Campaign에서는 이 기능에 이벤트를 보내는 정보 시스템을 통합하여 이벤트를 맞춤형 트랜잭션 메시지로 변환할 수 있습니다.

>[!NOTE]
>
>트랜잭션 메시지는 옵션에 따라 이메일, SMS 또는 푸시 알림으로 보낼 수 있습니다. 사용권 계약을 확인하십시오.

Adobe Campaign에서는 두 가지 유형의 트랜잭션 메시지를 사용할 수 있습니다.

* [이벤트 트랜잭션 메시지](../../channels/using/event-transactional-messages.md)는 이벤트를 타겟팅합니다. 이벤트 자체에 포함된 데이터를 게재 타겟 정의에 사용합니다.
* [프로필 트랜잭션 메시지](../../channels/using/profile-transactional-messages.md)는 Adobe Campaign 마케팅 데이터베이스에 있는 프로필을 타겟팅합니다. Adobe Campaign 데이터베이스의 정보를 사용하여 고객 마케팅 프로필 기반의 트랜잭션 메시지를 보낼 수 있습니다.

메시지 유형은 트랜잭션 메시지로 변환할 이벤트를 구성할 때 정의합니다. [트랜잭션 메시지 구성](../../administration/using/configuring-transactional-messaging.md)을 참조하십시오.

>[!NOTE]
>
>Adobe Campaign은 다른 어떤 게재보다도 트랜잭션 메시지 처리에 우선 순위를 둡니다.

트랜잭션 메시지는 Adobe Campaign Standard API에서도 사용할 수 있습니다. 자세한 내용은 [전용 설명서](../../api/using/managing-transactional-messages.md)를 참조하십시오.

>[!NOTE]
>
>이제 Adobe Campaign Enhanced MTA를 통해 모든 트랜잭션 메시지를 보냄으로써 게재 능력, 처리량 및 반송 처리를 개선할 수 있습니다. 모든 영향은 표준 마케팅 메시지와 동일합니다. 자세한 내용은 이 [섹션](../../administration/using/configuring-email-channel.md)을 참조하십시오.

## 트랜잭션 메시지 작동 원리 {#transactional-messaging-operating-principle}

웹사이트가 있어 이 웹사이트에서 사용자가 제품을 구입할 수 있는 회사의 예를 들어 보겠습니다.

Adobe Campaign을 통해 장바구니에 제품을 추가한 사이트 사용자에게 알림 이메일을 보낼 수 있습니다. 가령 한 사용자가 구매 과정을 완료하지 않고 사이트를 떠나면 장바구니 중단 이메일을 자동으로 보냅니다.

이 작업을 수행하는 단계는 다음과 같습니다.

1. 이벤트를 구성하여 이름을 &quot;장바구니 중단&quot;으로 지정합니다. 이 이벤트 구성을 게시하면 트랜잭션 메시지를 자동으로 만듭니다. 이벤트 만들기와 게시에 대한 설명은 [이벤트 트랜잭션 메시지를 보내기 위한 이벤트 구성](../../administration/using/configuring-transactional-messaging.md#use-case--configuring-an-event-to-send-a-transactional-message) 섹션에 있습니다.
1. 트랜잭션 메시지를 개인화하고 테스트한 후 게시해야 합니다. [이벤트 트랜잭션 메시지](../../channels/using/event-transactional-messages.md)를 참조하십시오.
1. 또한 고객이 장바구니 작업을 중단했을 때 이벤트가 트리거되도록 하려면 Adobe Campaign Standard REST API를 사용하여 회사 웹사이트에서 이 이벤트를 보내야 합니다. [사이트 통합](../../administration/using/configuring-transactional-messaging.md#integrating-the-triggering-of-the-event-in-a-website)을 참조하십시오.

이 단계를 모두 완료하고 나면 사용자가 장바구니의 제품을 주문하지 않고 사이트를 떠나자마자 자동으로 알림 이메일을 받게 됩니다.

## 트랜잭션 메시지 게시 프로세스 {#transactional-messaging-pub-process}

아래 차트는 트랜잭션 메시지 게시 프로세스를 보여줍니다.

![](assets/message-center_pub-process.png)

이벤트 구성 단계에 대한 자세한 내용은 [트랜잭션 메시지 구성](../../administration/using/configuring-transactional-messaging.md)을 참조하십시오.

## 트랜잭션 메시지 제한 사항 {#transactional-messaging-limitations}

>[!NOTE]
>
>트랜잭션 메시지에 액세스하려면 관리 권한이 있어야 합니다.

### 디자인 및 게시 {#design-and-publication}

트랜잭션 메시지를 디자인 및 게시할 때 수행해야 하는 일부 단계는 되돌릴 수 없습니다. 다음 제한 사항을 알아 두어야 합니다.

* 각 이벤트 구성에 대해 채널은 하나씩만 사용할 수 있습니다. [이벤트 만들기](../../administration/using/configuring-transactional-messaging.md#creating-an-event)를 참조하십시오.
* 이벤트를 만든 후에는 채널을 변경할 수 없습니다. 따라서 메시지가 성공적으로 보내지지 않는 경우 워크플로우를 사용하여 다른 채널에서 메시지를 보낼 수 있는 메커니즘을 설계해야 합니다. [워크플로우 데이터 및 프로세스](../../automating/using/get-started-workflows.md)를 참조하십시오.
* 이벤트를 만든 후에는 타겟팅 차원(**[!UICONTROL Real-time event]** 또는 **[!UICONTROL Profile]**)을 변경할 수 없습니다. [이벤트 만들기](../../administration/using/configuring-transactional-messaging.md#creating-an-event)를 참조하십시오.
* 게시를 롤백할 수는 없지만, 이벤트를 게시 취소할 수는 있습니다. 이 작업을 수행하면 해당 이벤트와 관련 트랜잭션 메시지가 액세스할 수 없는 상태가 됩니다. [이벤트 게시 취소](../../administration/using/configuring-transactional-messaging.md#unpublishing-an-event)를 참조하십시오.
* 이벤트를 게시할 때 자동으로 만들어지는 트랜잭션 메시지만 해당 이벤트와 연결할 수 있습니다. [이벤트 미리 보기 및 게시](../../administration/using/configuring-transactional-messaging.md#previewing-and-publishing-the-event)를 참조하십시오.

### 개인화 {#personalization}

메시지 콘텐츠를 개인화할 수 있는 방법은 트랜잭션 메시지의 유형에 따라 다릅니다. 구체적으로는 다음과 같습니다.

**이벤트 기반 트랜잭션 메시지**:

* 이벤트 자체에 포함된 데이터에서 개인화 정보를 가져옵니다. [이벤트 트랜잭션 메시지](../../channels/using/event-transactional-messages.md)를 참조하십시오.
* 이벤트 트랜잭션 메시지에는 **구독 취소 링크** 콘텐츠 블록을 사용할 수 없습니다.
* 이벤트 기반 트랜잭션 메시지는 보낸 이벤트에 있는 데이터만 사용하여 수신자와 메시지 콘텐츠 개인화를 정의합니다. 그러나 Adobe Campaign 데이터베이스의 정보를 사용하여 트랜잭션 메시지의 콘텐츠를 보강할 수 있습니다. [트랜잭션 메시지 콘텐츠 보강](../../administration/using/configuring-transactional-messaging.md#enriching-the-transactional-message-content)을 참조하십시오.
* 이벤트 트랜잭션 메시지에는 프로필 정보가 포함되어 있지 않기 때문에 피로도 규칙이 적용되지 않습니다. 프로필로 보강했을 경우에도 마찬가지입니다. [피로도 규칙](../../sending/using/fatigue-rules.md)을 참조하십시오.

**프로필 기반 트랜잭션 메시지**:

* 이벤트에 포함된 데이터나 조정된 프로필 레코드에서 개인화 정보를 가져올 수 있습니다. [프로필 트랜잭션 메시지](../../channels/using/profile-transactional-messages.md)를 참조하십시오.
* 프로필 트랜잭션 메시지에는 **구독 취소 링크** 콘텐츠 블록을 사용할 수 있습니다. [콘텐츠 블록 추가](../../designing/using/personalization.md#adding-a-content-block)를 참조하십시오.
* 프로필 트랜잭션 메시지의 경우 피로도 규칙이 적용됩니다. [피로도 규칙](../../sending/using/fatigue-rules.md)을 참조하십시오.

제품 목록은 트랜잭션 이메일 메시지에만 사용할 수 있습니다. [트랜잭션 메시지에서 제품 목록 사용](../../channels/using/event-transactional-messages.md#using-product-listings-in-a-transactional-message)을 참조하십시오.

### 권한 및 브랜딩 {#permissions-and-branding}

[브랜딩](../../administration/using/branding.md) 관리 측면에서 볼 때, 트랜잭션 메시지는 표준 메시지보다 유연성이 낮습니다. Adobe는 트랜잭션 메시지에 사용하는 모든 브랜드를 **[!UICONTROL All]** [ 조직 단위](../../administration/using/organizational-units.md)로 연결하는 것을 권장합니다. 자세한 내용은 아래 설명을 참조하십시오.

트랜잭션 메시지를 편집할 때 브랜드에 연결하여 브랜드 이름이나 브랜드 로고와 같은 일부 매개 변수를 자동으로 적용할 수 있습니다. 트랜잭션 메시지 속성에서 기본적으로 **[!UICONTROL Default brand]**&#x200B;이(가) 선택됩니다.

![](assets/message-center_branding.png)

트랜잭션 메시지에 사용하는 모든 개체(브랜딩 포함)는 **[!UICONTROL Message Center]** 조직 단위에서 볼 수 있어야 합니다. 즉, 이 개체는 **[!UICONTROL Message Center]** 또는 **[!UICONTROL All]** 조직 단위로 표시되어야 합니다.

하지만 메시지 속성에서 선택한 브랜드가 **[!UICONTROL Message Center]**&#x200B;나 **[!UICONTROL All]**&#x200B;와(과) 다른 조직 단위에 연결되어 있는 경우 오류가 발생하여 트랜잭션 메시지를 보낼 수 없습니다.

따라서 트랜잭션 메시지의 컨텍스트에서 다중 브랜딩을 사용하려면 모든 브랜드를 **[!UICONTROL Message Center]** 조직 단위나 **[!UICONTROL All]** 조직 단위에 연결해야 합니다.

### 트랜잭션 메시지 내보내기 및 가져오기 {#exporting-and-importing-transactional-messages}

* 트랜잭션 메시지를 내보내려면 [패키지 내보내기 만들기](../../automating/using/managing-packages.md#creating-a-package) 시 해당 이벤트 구성을 포함해야 합니다.
* 트랜잭션 메시지를 [패키지로 가져오기](../../automating/using/managing-packages.md#importing-a-package)하면 트랜잭션 메시지 목록에 표시되지 않습니다. 연결된 트랜잭션 메시지를 사용할 수 있게 하려면 해당 이벤트 구성을 [게시](../../administration/using/configuring-transactional-messaging.md#previewing-and-publishing-the-event)해야 합니다.

