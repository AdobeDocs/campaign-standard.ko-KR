---
title: 트랜잭션 메시지 기본 정보
description: 전송할 수 있는 다양한 유형의 트랜잭션 메시지와 Adobe Campaign에서 사용되는 방식을 살펴볼 수 있습니다.
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
translation-type: tm+mt
source-git-commit: 155ed7e50e207e4c4dc0569e5e96b24e712e4be8

---


# 트랜잭션 메시지 기본 정보{#about-transactional-messaging}

Adobe Campaign에서 개인화된 트랜잭션 메시지를 만들고 관리할 수 있습니다.

트랜잭션 메시지는 웹 사이트와 같은 공급자가 사용자에게 보내는 개별 고유한 통신입니다.

* 받는 사람이 확인하거나 확인하려는 정보가 포함되어 있으므로 이러한 유형의 메시지가 특히 필요합니다. 예를 들어 계정을 만든 후 환영 메시지가 될 수도 있고, 주문이 배송되었다는 확인, 청구 또는 암호 변경을 확인하는 메시지가 될 수도 있습니다.
* 클라이언트 관계를 정의하는 중요한 메시지입니다.사용자는 실시간으로 전송될 것으로 예상하고 있습니다. 이벤트가 트리거되는 것과 메시지가 도착하는 것 사이의 지연은 매우 짧아야 합니다.
* 트랜잭션 메시지는 일반적으로 개방률이 높습니다.

Adobe Campaign을 사용하면 이 기능을 사용자 지정 트랜잭션 메시지로 변환할 이벤트를 전송하는 정보 시스템과 통합할 수 있습니다.

>[!NOTE]
>
>트랜잭션 메시지는 옵션에 따라 이메일, SMS 또는 푸시 알림을 통해 보낼 수 있습니다. 사용권 계약을 확인하십시오.

Adobe Campaign에서는 두 가지 유형의 트랜잭션 메시지를 사용할 수 있습니다.

* [이벤트를 타깃팅하는 이벤트 트랜잭션 메시지](../../channels/using/event-transactional-messages.md) . 이벤트 자체에 포함된 데이터는 배달 대상을 정의하는 데 사용됩니다.
* [Adobe Campaign 마케팅 데이터베이스에서 트랜잭션 메시지](../../channels/using/profile-transactional-messages.md) 타깃팅 프로필을 프로파일링합니다. Adobe Campaign 데이터베이스의 정보를 사용하여 고객 마케팅 프로필을 기반으로 트랜잭션 메시지를 보낼 수 있습니다.

트랜잭션 메시지로 변환할 이벤트를 구성할 때 메시지 유형이 정의됩니다. 트랜잭션 [메시징 구성을](../../administration/using/configuring-transactional-messaging.md)참조하십시오.

>[!NOTE]
>
>Adobe Campaign은 다른 전달보다 트랜잭션 메시지 처리를 우선합니다.

트랜잭션 메시지는 Adobe Campaign Standard API에서도 사용할 수 있습니다. 자세한 내용은 [전용 설명서를](../../api/using/managing-transactional-messages.md)참조하십시오.

>[!IMPORTANT]
>
>향상된 MTA [로 업그레이드하면](https://helpx.adobe.com/campaign/kb/campaign-enhanced-mta.html)Adobe Campaign 향상된 MTA를 통해 모든 트랜잭션 메시지가 전송되어 전달 능력, 처리량 및 바운스 처리 기능이 향상되었습니다. 모든 영향은 표준 마케팅 메시지와 동일하며 Adobe Campaign 향상된 MTA [문서에 자세히 설명되어](https://helpx.adobe.com/campaign/kb/campaign-enhanced-mta.html) 있습니다.

## 트랜잭션 메시징 운영 원칙 {#transactional-messaging-operating-principle}

웹 사이트를 보유하고 있고 사용자가 제품을 구입할 수 있는 웹 사이트를 보유하고 있는 회사의 예를 들어보겠습니다.

Adobe Campaign을 사용하면 장바구니에 제품을 추가한 사이트 사용자에게 알림 이메일을 보낼 수 있습니다.이들 중 한 명이 구입을 진행하지 않고 사이트를 떠나면 장바구니 포기 이메일이 자동으로 발송됩니다.

이 문제를 해결하는 단계는 다음과 같습니다.

1. &quot;장바구니 포기&quot;라는 이름을 지정할 이벤트를 구성하고 트랜잭션 메시지를 자동으로 생성하는 이 이벤트 구성을 게시합니다. 이벤트 만들기 및 게시는 이벤트 트랜잭션 메시지 [](../../administration/using/configuring-transactional-messaging.md#use-case--configuring-an-event-to-send-a-transactional-message) 전송을 위한 이벤트 구성 섹션에 나와 있습니다.
1. 트랜잭션 메시지는 개인화된 후 테스트한 다음 게시해야 합니다. See [Event transactional messages](../../channels/using/event-transactional-messages.md).
1. 또한 클라이언트가 장바구니를 포기하면 이벤트가 트리거되도록 하려면 Adobe Campaign Standard REST API를 사용하여 회사의 웹 사이트에서 이 이벤트를 전송해야 합니다. 사이트 [통합을](../../administration/using/configuring-transactional-messaging.md#integrating-the-triggering-of-the-event-in-a-website)참조하십시오.

이러한 모든 단계가 수행되면 사용자가 장바구니에 제품을 주문하지 않고 사이트를 떠나면 알림 이메일을 자동으로 받게 됩니다.

## 트랜잭션 메시지 게시 프로세스 {#transactional-messaging-pub-process}

아래 차트는 트랜잭션 메시지 게시 프로세스를 보여줍니다.

![](assets/message-center_pub-process.png)

이벤트 구성 단계에 대한 자세한 내용은 트랜잭션 [메시징 구성을](../../administration/using/configuring-transactional-messaging.md)참조하십시오.

## 트랜잭션 메시징 제한 사항 {#transactional-messaging-limitations}

>[!NOTE]
>
>트랜잭션 메시지에 액세스하려면 관리 권한이 있어야 합니다.

### 디자인 및 출판 {#design-and-publication}

트랜잭션 메시지를 디자인하고 게시할 때 수행해야 하는 일부 단계는 되돌릴 수 없습니다. 다음 제한 사항을 알고 있어야 합니다.

* 각 이벤트 구성에는 하나의 채널만 사용할 수 있습니다. 이벤트 [만들기를](../../administration/using/configuring-transactional-messaging.md#creating-an-event)참조하십시오.
* 이벤트가 만들어지면 채널을 변경할 수 없습니다. 따라서 메시지가 성공적으로 전송되지 않으면 워크플로우를 사용하여 다른 채널에서 메시지를 보낼 수 있는 메커니즘을 설계해야 합니다. See [Workflow data and processes](../../automating/using/workflow-data-and-processes.md).
* 이벤트를 만든 후에는 타깃팅 차원( **[!UICONTROL Real-time event]** 또는 **[!UICONTROL Profile]** )을 변경할 수 없습니다. 이벤트 [만들기를](../../administration/using/configuring-transactional-messaging.md#creating-an-event)참조하십시오.
* 발행물을 롤백할 수는 없지만 이벤트를 게시 취소할 수 있습니다.이 작업을 수행하면 이벤트와 관련 트랜잭션 메시지에 액세스할 수 없게 됩니다. 이벤트 [게시 취소를 참조하십시오](../../administration/using/configuring-transactional-messaging.md#unpublishing-an-event).
* 이벤트와 연결할 수 있는 유일한 트랜잭션 메시지는 해당 이벤트를 게시하면 자동으로 만들어지는 메시지입니다. 이벤트 [미리 보기 및 게시를](../../administration/using/configuring-transactional-messaging.md#previewing-and-publishing-the-event)참조하십시오.

### 개인화 {#personalization}

메시지 컨텐츠를 개인화할 수 있는 방법은 트랜잭션 메시지 유형에 따라 다릅니다. 다음은 특정 목록입니다.

**이벤트 기반의 트랜잭션 메시지**:

* 개인화 정보는 이벤트 자체에 포함된 데이터에서 가져옵니다. See [Event transactional messages](../../channels/using/event-transactional-messages.md).
* 이벤트 트랜잭션 메시지에는 **구독 취소 링크** 내용 블록을 사용할 수 없습니다.
* 이벤트 기반 트랜잭션 메시지는 보낸 이벤트에 있는 데이터만 사용하여 받는 사람과 메시지 컨텐츠 개인화를 정의해야 합니다. 그러나 Adobe Campaign 데이터베이스의 정보를 사용하여 트랜잭션 메시지의 컨텐츠를 강화할 수 있습니다. 트랜잭션 [메시지 컨텐츠](../../administration/using/configuring-transactional-messaging.md#enriching-the-transactional-message-content)강화를 참조하십시오.
* 트랜잭션 메시지에 프로필 정보가 포함되어 있지 않은 경우 프로필 정보가 포함된 경우에도 피로 규칙과 호환되지 않습니다. 피로 [규칙을](../../sending/using/fatigue-rules.md)참조하십시오.

**프로파일 기반의 트랜잭션 메시지**:

* 개인화 정보는 이벤트에 포함된 데이터나 조정된 프로필 레코드에서 가져올 수 있습니다. See [Profile transactional messages](../../channels/using/profile-transactional-messages.md).
* 프로필 트랜잭션 **메시지에서 구독 취소 링크** 콘텐츠 블록을 사용할 수 있습니다. 컨텐츠 [블록](../../designing/using/personalization.md#adding-a-content-block)추가를 참조하십시오.
* 피로 규칙은 프로필 트랜잭션 메시지와 호환됩니다. 피로 [규칙을](../../sending/using/fatigue-rules.md)참조하십시오.

제품 목록은 트랜잭션 이메일 메시지만 사용할 수 있습니다. 트랜잭션 [메시지의](../../channels/using/event-transactional-messages.md#using-product-listings-in-a-transactional-message)제품 목록 사용을 참조하십시오.

### 권한 및 브랜딩 {#permissions-and-branding}

브랜드 [관리 측면에서](../../administration/using/branding.md) 트랜잭션 메시징은 표준 메시징보다 유연성이 떨어집니다. 거래 메시지에 사용된 모든 브랜드를 **[!UICONTROL All]**[&#x200B;조직 구성 요소에](../../administration/using/organizational-units.md)연결하는 것이 좋습니다. 자세한 내용은 아래 설명을 참조하십시오.

거래 메시지를 편집할 때 브랜드 이름이나 브랜드 로고와 같은 일부 매개 변수를 자동으로 적용할 수 있도록 브랜드에 연결할 수 있습니다. 트랜잭션 메시지 속성에서 기본적으로 **[!UICONTROL Default brand]** 이 선택됩니다.

![](assets/message-center_branding.png)

트랜잭션 메시지에 사용된 모든 개체(브랜딩 포함)는 **[!UICONTROL Message Center]** 조직 구성 요소에서 볼 수 있어야 합니다. 즉, 이러한 개체는 **[!UICONTROL Message Center]** 또는 **[!UICONTROL All]** 조직 단위로 표시되어야 합니다.

하지만 메시지 속성에서 선택한 브랜드가 조직 구성 단위와 연결되어 **[!UICONTROL Message Center]** 있거나 다른 **[!UICONTROL All]**&#x200B;경우 오류가 발생하며 트랜잭션 메시지를 보낼 수 없습니다.

따라서 트랜잭션 메시징의 컨텍스트에서 다중 브랜딩을 사용하려면 모든 브랜드를 **[!UICONTROL Message Center]** 조직 구성 단위 또는 **[!UICONTROL All]** 조직 구성 단위에 연결해야 합니다.

### 트랜잭션 메시지 내보내기 및 가져오기 {#exporting-and-importing-transactional-messages}

* 트랜잭션 메시지를 내보내려면 패키지 내보내기를 [만들](../../automating/using/managing-packages.md#creating-a-package)때 해당 이벤트 구성을 포함해야 합니다.
* 트랜잭션 메시지를 패키지를 [통해](../../automating/using/managing-packages.md#importing-a-package)가져오면 트랜잭션 메시지 목록에 표시되지 않습니다. 관련 트랜잭션 메시지를 사용할 수 있도록 하려면 이벤트 구성을 [게시해야](../../administration/using/configuring-transactional-messaging.md#previewing-and-publishing-the-event) 합니다.

