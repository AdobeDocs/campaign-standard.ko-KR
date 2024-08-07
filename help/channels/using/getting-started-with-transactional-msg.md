---
title: 트랜잭션 메시지 시작
description: 트랜잭션 메시지가 무엇인지 알아보고 Adobe Campaign Standard에서 트랜잭션 메시지를 설정하는 주요 단계를 알아봅니다.
audience: channels
content-type: reference
topic-tags: transactional-messaging
context-tags: null
feature: Transactional Messaging
role: User
level: Beginner
exl-id: 49fba1af-3c99-45b7-bcbb-b9b9678eedcd
source-git-commit: 0e486e87c94e273442de23d6eb65c99f065e5a71
workflow-type: tm+mt
source-wordcount: '992'
ht-degree: 8%

---

# 트랜잭션 메시지 시작 {#getting-started-with-transactional-messaging}

트랜잭션 메시지는 웹 사이트와 같은 공급자가 실시간으로 전송하는 개별적이고 고유한 통신입니다. 수신자가 확인하거나 확정하려는 중요한 정보가 포함되어 있기 때문에 특히 기대됩니다.

* **기한이 언제입니까?** 이 메시지에는 중요한 정보가 포함되어 있으므로 사용자는 이 메시지가 실시간으로 전송될 것으로 예상합니다. 따라서 트리거되는 이벤트와 메시지 도착 사이의 지연 시간이 매우 짧아야 합니다.

* **중요한 이유** 일반적으로 트랜잭션 메시지의 열기 비율이 높습니다. 따라서 고객 관계를 정의하므로 고객의 행동에 강력한 영향을 줄 수 있으므로 신중하게 설계해야 합니다.

* **예?** 계정 만들기, 주문 배송 확인, 청구서, 암호 변경 확인 메시지 또는 고객이 웹 사이트를 열람한 후 알림 등이 환영 메시지가 될 수 있습니다.

Adobe Campaign에서는 이 기능을 사용자 지정 트랜잭션 메시지로 변환할 이벤트를 전송하는 정보 시스템과 통합할 수 있습니다.

트랜잭션 메시지는 옵션에 따라 전자 메일, SMS 또는 [푸시 알림](../../channels/using/transactional-push-notifications.md)으로 보낼 수 있습니다. 사용권 계약을 확인하십시오.

>[!NOTE]
>
>Adobe Campaign은 다른 어떤 게재보다 트랜잭션 메시지 처리에 우선 순위를 둡니다.

<!--Guidelines to implement transactional messaging capabilities in your website are detailed in [this section](../../api/using/managing-transactional-messages.md).-->

트랜잭션 메시지를 시작하기 전에 해당 [모범 사례 및 제한 사항](../../channels/using/transactional-messaging-limitations.md)을 읽어야 합니다.

## 트랜잭션 메시지 작동 원리 {#transactional-messaging-operating-principle}

트랜잭션 메시지 전체 프로세스는 다음과 같이 설명할 수 있습니다.

![](assets/message-center-process.png)

예를 들어 고객이 제품을 구매할 수 있는 웹 사이트를 보유한 회사라고 가정해 보겠습니다.

Adobe Campaign을 사용하면 장바구니에 제품을 추가한 고객에게 알림 이메일을 보낼 수 있습니다. 둘 중 한 명이 구매(캠페인 이벤트를 트리거하는 외부 이벤트)를 수행하지 않고 웹 사이트를 떠나면 장바구니 포기 이메일이 자동으로 전송됩니다(트랜잭션 메시지 게재).

이 작업을 수행하는 주요 단계는 [이 섹션](#key-steps)에 자세히 설명되어 있습니다.

## 트랜잭션 메시지 유형 {#transactional-message-types}

Adobe Campaign에서는 두 가지 유형의 트랜잭션 메시지를 사용할 수 있습니다.

이벤트 자체에 포함된 **이벤트 트랜잭션 메시지** 대상 데이터입니다. 이 메시지는 다음과 같습니다.
* 프로필 정보를 포함하지 않으므로 구독 취소 링크를 포함할 수 없습니다.
* 피로도 규칙(프로필이 보강된 경우에도)과 호환되지 않습니다.
* 이벤트 자체에 포함된 데이터로 게재 대상을 정의하도록 합니다.

예를 들어 잊은 암호를 검색하거나 주문을 확인해야 하는 고객에게 이벤트 트랜잭션 메시지를 보낼 수 있습니다. 실제로, 수신자가 이러한 유형의 커뮤니케이션에서 구독을 취소하는 것을 원치 않으며 이 알림은 피로도 규칙의 일부로 마케팅 메시지 카운터에 추가되어서는 안 됩니다.

Campaign 마케팅 데이터베이스에서 **프로필 트랜잭션 메시지**&#x200B;대상 프로필. 이러한 유형의 메시지를 사용하여 다음과 같은 작업을 수행할 수 있습니다.
* Adobe Campaign 데이터베이스에 포함된 데이터를 활용합니다.
* 이벤트 구성에 [데이터 보강](../../channels/using/configuring-transactional-event.md#enriching-the-transactional-message-content)을(를) 추가하여 프로필 정보로 메시지를 개인화합니다.
* [마케팅 유형화 규칙](../../sending/using/managing-typology-rules.md) 또는 [피로도 규칙](../../sending/using/fatigue-rules.md)을 적용합니다.
* 메시지에 구독 취소 링크를 포함합니다.
* 트랜잭션 메시지를 글로벌 게재 보고서에 추가합니다.
* 트랜잭션 메시지를 고객 여정에 활용합니다.

예를 들어, 고객이 웹 사이트에 장바구니를 포기한 후 연락할 때 이 유형의 메시지를 사용하여 구매를 진행할 수 있도록 유도할 수 있습니다. 이렇게 하면 프로필 데이터베이스의 모든 정보에 직접 액세스하여 메시지를 보다 쉽게 개인화하고, 마케팅 규칙을 적용하고, 글로벌 고객 여정 및 보고에 이 메시지를 포함시켜 고객 행동을 보다 잘 볼 수 있습니다.

메시지 유형은 트랜잭션 메시지로 변환할 이벤트를 구성할 때 정의합니다. [이벤트 기반 트랜잭션 메시지](../../channels/using/configuring-transactional-event.md#event-based-transactional-messages) 및 [프로필 기반 트랜잭션 메시지](../../channels/using/configuring-transactional-event.md#profile-based-transactional-messages) 구성 섹션을 참조하십시오.

## 주요 단계 {#key-steps}

Adobe Campaign에서 개인화된 트랜잭션 메시지를 만들고 관리할 때의 주요 단계는 아래 스키마에 요약되어 있습니다.

![](assets/message-center-overview.png)

이러한 각 단계는 아래에 자세히 설명되어 있습니다.

>[!IMPORTANT]
>
>[관리](../../administration/using/users-management.md#functional-administrators) 역할을 가진 사용자만 트랜잭션 이벤트를 구성하고 트랜잭션 메시지에 액세스할 수 있습니다.

### 1단계 - 이벤트 구성 만들기 및 게시 {#create-event-configuration}

<!--<img src="assets/do-not-localize/icon_config.svg" width="60px">-->

| 이벤트 만들기 | 사용자 | 작업 | 결과 |
| --- |--- |--- |--- |
| <img src="assets/do-not-localize/icon_config.svg" width="60px"> | 이 단계는 [관리 권한](../../administration/using/users-management.md#functional-administrators)을 보유한 관리자가 수행해야 합니다. | 이름을 &quot;장바구니 포기&quot;로 지정할 이벤트를 구성하고 이 이벤트 구성을 게시합니다. | 웹 사이트 개발자가 사용할 API가 배포되고 트랜잭션 메시지가 자동으로 만들어집니다. |

이벤트를 만들고 게시하는 방법은 [트랜잭션 이벤트 구성](../../channels/using/configuring-transactional-event.md) 및 [트랜잭션 이벤트 게시](../../channels/using/publishing-transactional-event.md) 섹션에 나와 있습니다.

### 2단계 - 트랜잭션 메시지 편집 및 게시 {#create-transactional-message}

<!--<img src="assets/do-not-localize/icon_notification.svg" width="40px">-->

| 메시지 편집 | 사용자 | 작업 | 결과 |
| --- |--- |--- |--- |
| <img src="assets/do-not-localize/icon_notification.svg" width="40px"> | 이 단계는 [관리 권한](../../administration/using/users-management.md#functional-administrators)을 보유한 마케팅 사용자가 수행할 수 있습니다. | 트랜잭션 메시지를 편집 및 개인화하고, 테스트한 다음 게시합니다. | 그러면 트랜잭션 메시지를 보낼 준비가 된 것입니다. |

트랜잭션 메시지 편집 및 게시에 대한 자세한 내용은 [트랜잭션 메시지 편집](../../channels/using/editing-transactional-message.md) 및 [트랜잭션 메시지 수명 주기](../../channels/using/publishing-transactional-message.md)를 참조하십시오.

### 3단계 - 이벤트 트리거 통합 {#integrate-event-trigger}

<!--<img src="assets/do-not-localize/icon_api.svg" width="55px">-->

이벤트를 만든 후에는 이 이벤트의 트리거를 웹 사이트에 통합해야 합니다.<!--In this example, you want a "Cart abandonment" event to be triggered whenever one of your clients leaves your website before purchasing the products in their cart.--> 웹 사이트 웹 개발자는 **Adobe Campaign Standard REST API**&#x200B;를 사용해야 합니다.

| 트리거 구현 | 사용자 | 작업 | 결과 |
| --- |--- |--- |--- |
| <img src="assets/do-not-localize/icon_api.svg" width="55px"> | 이 단계는 웹 사이트 개발자가 수행합니다. | REST 트랜잭션 메시지 API를 사용하여 이벤트를 웹 사이트에 통합합니다. | 클라이언트가 장바구니를 중단하면 이벤트가 트리거됩니다. |

캠페인 REST API를 사용하여 트랜잭션 메시지를 관리하는 방법에 대한 자세한 내용은 [REST API 설명서](../../api/using/managing-transactional-messages.md)를 참조하십시오.

### 4단계 - 메시지 게재 {#message-delivery}

<!--<img src="assets/do-not-localize/icon_channels.svg" width="60px">-->

위의 단계가 모두 수행되면 메시지를 전달할 수 있습니다.

| 메시지 게재 | 사용자 | 작업 | 결과 |
| --- |--- |--- |--- |
| <img src="assets/do-not-localize/icon_channels.svg" width="60px"> | 이 단계는 웹 사이트를 방문하는 고객이 수행합니다. | 사용자가 장바구니에 있는 제품을 주문하지 않고 사이트를 떠나자마자 해당 캠페인 이벤트가 트리거됩니다. | 사용자는 자동으로 알림 이메일을 수신합니다. |

## 관련 항목

* [메시지를 보내는 주요 단계](../../channels/using/key-steps-to-send-a-message.md)
* [소통 채널 시작](../../channels/using/get-started-communication-channels.md)
* [트랜잭션 푸시 알림](../../channels/using/transactional-push-notifications.md)
* [후속 메시지](../../channels/using/follow-up-messages.md)
