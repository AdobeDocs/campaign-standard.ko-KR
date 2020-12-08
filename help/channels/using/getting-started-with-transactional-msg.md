---
solution: Campaign Standard
product: campaign
title: 트랜잭션 메시지를 설정하는 주요 단계
description: 트랜잭션 메시징의 의미를 살펴보고 Adobe Campaign Standard에서 트랜잭션 메시지를 설정하는 주요 단계를 살펴보십시오.
audience: channels
content-type: reference
topic-tags: transactional-messaging
context-tags: null
translation-type: tm+mt
source-git-commit: c276c468627208b584a0342414cdbe382e349f50
workflow-type: tm+mt
source-wordcount: '966'
ht-degree: 7%

---


# 트랜잭션 메시지 시작 {#getting-started-with-transactional-messaging}

## 개요 {#overview}

<img src="assets/do-not-localize/icon_transactional.svg" width="60px">

트랜잭션 메시지는 웹 사이트와 같은 공급자가 실시간으로 전송하는 개별 고유한 통신입니다. 받는 사람이 확인하거나 확인하려는 중요한 정보가 포함되어 있으므로 특히 예상됩니다.

* **언제까지 해야 합니까?** 이 메시지에는 중요한 정보가 포함되어 있으므로 사용자는 이 메시지가 실시간으로 전송될 것으로 예상하고 있습니다. 따라서 이벤트가 트리거되는 것과 도착하는 메시지 사이의 지연은 매우 짧아야 합니다.

* **왜 중요하죠?** 일반적으로 트랜잭션 메시지는 높은 개방률을 가집니다. 따라서 고객 관계를 정의하는 고객의 행동에 강한 영향을 줄 수 있으므로 신중하게 설계되어야 합니다.

* **예제?** 계정 생성 후 환영 메시지, 주문 배송 확인, 송장, 암호 변경을 확인하는 메시지 또는 고객이 웹 사이트를 방문한 후 알림 등이 될 수 있습니다.

Adobe Campaign을 사용하면 이 기능을 사용자 지정 트랜잭션 메시지로 변환할 이벤트를 전송하는 정보 시스템과 통합할 수 있습니다.

트랜잭션 메시지는 옵션에 따라 이메일, SMS 또는 [푸시 알림](../../channels/using/transactional-push-notifications.md)으로 보낼 수 있습니다. 사용권 계약을 확인하십시오.

>[!NOTE]
>
>Adobe Campaign은 다른 배달보다 트랜잭션 메시지 처리에 우선 순위를 매깁니다.

<!--Guidelines to implement transactional messaging capabilities in your website are detailed in [this section](../../api/using/managing-transactional-messages.md).-->

<!--All transactional messages are now sent with the Adobe Campaign Enhanced MTA for improved deliverability, throughput, and bounce handling. All impacts are the same as for standard marketing messages. For more on this, see [this section](../../administration/using/configuring-email-channel.md).-->

트랜잭션 메시징을 시작하기 전에 해당 [우수 사례 및 제한 사항](../../channels/using/transactional-messaging-limitations.md)을 읽어야 합니다.

## 트랜잭션 메시지 작동 원리 {#transactional-messaging-operating-principle}

트랜잭션 메시지 전체 프로세스는 다음과 같이 설명할 수 있습니다.

![](assets/message-center-process.png)

예를 들어 고객이 제품을 구매할 수 있는 웹 사이트를 보유한 회사인 경우를 가정해 봅시다.

Adobe Campaign을 사용하면 장바구니에 제품을 추가한 고객에게 알림 이메일을 보낼 수 있습니다. 이 중 하나가 구매(캠페인 이벤트를 트리거하는 외부 이벤트)를 거치지 않고 웹 사이트를 떠나면 장바구니 포기 이메일이 자동으로 해당 웹 사이트에 전송됩니다(트랜잭션 메시지 배달).

이 기능을 적용하기 위한 주요 단계는 [이 섹션](#key-steps)에 자세히 설명되어 있습니다.

## 트랜잭션 메시지 유형 {#transactional-message-types}

Adobe Campaign에서는 두 가지 유형의 트랜잭션 메시지를 사용할 수 있습니다.

**이벤트 트랜잭션 메시지** 는 이벤트 자체에 포함된 데이터입니다. 다음 메시지:
* 프로필 정보를 포함하지 마십시오. 따라서 구독 취소 링크를 포함할 수 없습니다.
* 피로 규칙과는 호환하지 않습니다(프로필 정보가 농축된 경우에도).
* 이벤트 자체에 포함된 데이터로 배달 대상을 정의하십시오.

예를 들어, 잊어버린 암호를 검색하거나 주문을 확인해야 하는 고객에게 이벤트 트랜잭션 메시지를 보낼 수 있습니다. 실제로, 귀하는 수신자가 이러한 유형의 커뮤니케이션에서 가입을 해지하는 것을 원치 않으며, 이 알림을 피로 규칙의 일부로서 마케팅 메시지 카운터에 추가하면 안 됩니다.

**Campaign** 마케팅 데이터베이스에서 트랜잭션 메시지를 프로파일링합니다. 이 유형의 메시지를 사용하여 다음을 수행할 수 있습니다.
* Adobe Campaign 데이터베이스에 포함된 데이터를 활용할 수 있습니다.
* 이벤트 구성에 [enrichment](../../channels/using/configuring-transactional-event.md#enriching-the-transactional-message-content)를 추가하여 프로필 정보로 메시지를 개인화합니다.
* [마케팅 유형 규칙](../../sending/using/managing-typology-rules.md) 또는 [피로 규칙](../../sending/using/fatigue-rules.md)을 적용합니다.
* 메시지에 구독 취소 링크를 포함합니다.
* 트랜잭션 메시지를 글로벌 게재 보고서에 추가합니다.
* 트랜잭션 메시지를 고객 여정에 활용합니다.

예를 들어 고객이 웹 사이트에서 장바구니를 포기한 후 고객에게 문의할 때 이러한 유형의 메시지를 사용하여 고객이 구매를 진행할 수 있도록 장려할 수 있습니다. 이를 통해 프로필 데이터베이스의 모든 정보에 직접 액세스하여 메시지를 보다 손쉽게 개인화할 수 있고 마케팅 규칙을 적용하며 글로벌 고객 여정 및 리포팅에 이 메시지를 포함시켜 고객 행동을 보다 정확하게 파악할 수 있습니다.

메시지 유형은 트랜잭션 메시지로 변환할 이벤트를 구성할 때 정의합니다. [이벤트 기반 트랜잭션 메시지](../../channels/using/configuring-transactional-event.md#event-based-transactional-messages) 및 [프로필 기반 트랜잭션 메시지](../../channels/using/configuring-transactional-event.md#profile-based-transactional-messages) 구성 섹션을 참조하십시오.

## 키 단계 {#key-steps}

Adobe Campaign에서 개인화된 트랜잭션 메시지를 만들고 관리할 때의 주요 단계는 아래 스키마에 요약되어 있습니다.

![](assets/message-center-overview.png)

이러한 각 단계는 아래에 자세히 설명되어 있습니다.

>[!IMPORTANT]
>
>[관리](../../administration/using/users-management.md#functional-administrators) 역할을 가진 사용자만 트랜잭션 이벤트를 구성하고 트랜잭션 메시지에 액세스할 수 있습니다.

### 1단계 - 이벤트 구성 {#create-event-configuration} 만들기 및 게시

<img src="assets/do-not-localize/icon_config.svg" width="60px">

| 사용자 | 작업 | 결과 |
|--- |--- |--- |
| 이 단계는 [관리 권한](../../administration/using/users-management.md#functional-administrators)을 가진 관리자가 수행해야 합니다. | &quot;장바구니 포기&quot;라는 이름을 지정할 이벤트를 구성하고 이 이벤트 구성을 게시합니다. | 웹 사이트 개발자가 사용할 API가 배포되고 트랜잭션 메시지가 자동으로 생성됩니다. |

이벤트를 만들고 게시하는 것은 [트랜잭션 이벤트](../../channels/using/configuring-transactional-event.md) 및 [트랜잭션 이벤트](../../channels/using/publishing-transactional-event.md) 섹션 게시에서 볼 수 있습니다.

### 2단계 - 트랜잭션 메시지 {#create-transactional-message} 편집 및 게시

<img src="assets/do-not-localize/icon_notification.svg" width="40px">

| 사용자 | 작업 | 결과 |
|--- |--- |--- |
| 이 단계는 [관리 권한](../../administration/using/users-management.md#functional-administrators)을 가진 마케팅 사용자가 수행할 수 있습니다. | 트랜잭션 메시지를 편집하고 개인화하여 테스트한 다음 게시할 수 있습니다. | 트랜잭션 메시지를 보낼 준비가 되었습니다. |

트랜잭션 메시지 편집 및 게시에 대한 자세한 내용은 [트랜잭션 메시지 편집](../../channels/using/editing-transactional-message.md) 및 [트랜잭션 메시지 라이프사이클](../../channels/using/publishing-transactional-message.md)을 참조하십시오.

### 3단계 - 이벤트를 트리거하는 {#integrate-event-trigger} 통합

<img src="assets/do-not-localize/icon_api.svg" width="55px">

<!--**Event triggering integration**-->

| 사용자 | 작업 | 결과 |
|--- |--- |--- |
| 이 단계는 웹 사이트 개발자가 수행합니다. | REST 트랜잭션 메시지 API를 사용하여 이벤트를 웹 사이트에 통합합니다. | 클라이언트가 장바구니를 포기하면 이벤트가 트리거됩니다. |

이벤트를 만든 후에는 이 이벤트의 트리거가 웹 사이트에 통합되어야 합니다.<!--In this example, you want a "Cart abandonment" event to be triggered whenever one of your clients leaves your website before purchasing the products in their cart.--> 이렇게 하려면 웹 사이트 웹 개발자가  **Adobe Campaign Standard REST API를 사용해야 합니다**.

캠페인 REST API를 사용하여 트랜잭션 메시지를 관리하는 방법에 대한 자세한 내용은 [REST API 설명서](../../api/using/managing-transactional-messages.md)를 참조하십시오.

### 4단계 - 메시지 배달 {#message-delivery}

<img src="assets/do-not-localize/icon_channels.svg" width="60px">

이러한 모든 단계를 수행한 후 메시지가 전달될 수 있습니다.

사용자가 장바구니에서 제품을 주문하지 않고 사이트를 떠나면 해당 캠페인 이벤트가 트리거됩니다. 사용자는 알림 이메일을 자동으로 수신합니다.

## 관련 항목

* [메시지 보내기 주요 단계](../../channels/using/key-steps-to-send-a-message.md)
* [소통 채널 시작](../../channels/using/get-started-communication-channels.md)
* [트랜잭션 푸시 알림](../../channels/using/transactional-push-notifications.md)
* [후속 메시지](../../channels/using/follow-up-messages.md)
