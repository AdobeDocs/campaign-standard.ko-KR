---
title: 트랜잭션 메시지를 설정하는 주요 단계
description: 트랜잭션 메시징의 의미를 살펴보고 Adobe Campaign Standard에서 트랜잭션 메시지를 설정하는 주요 단계를 살펴보십시오.
page-status-flag: never-activated
uuid: b316bf47-7d98-46fa-ab4f-67ff50de8095
contentOwner: lemaitre
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: landing-pages
discoiquuid: ca8d1698-6e8a-4f5a-b017-74a152e14286
context-tags: landingPage,wizard;landingPage,overview;landingPage,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 429142610b969f3bd1460a8ba401c7e83acb7dea
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 28%

---


# 트랜잭션 메시지 시작하기 {#getting-started-with-transactional-messaging}

## 개요


<img src="assets/do-not-localize/icon_transactional.svg" width="60px">

트랜잭션 메시지를 통해 고객에게 실시간으로 개별 메시지 <b>및 고유한 메시지를</b> 보낼 수 있습니다. 환영 메시지, 주문 확인, 암호 변경 등이 가능합니다.

Adobe Campaign을 사용하면 이 기능을 사용자 지정 트랜잭션 메시지로 변환할 이벤트를 전송하는 정보 시스템과 통합할 수 있습니다.

>[!NOTE]
>
>트랜잭션 메시지는 옵션에 따라 이메일, SMS 또는 푸시 알림으로 보낼 수 있습니다. 사용권 계약을 확인하십시오.

Adobe Campaign은 다른 배달보다 트랜잭션 메시지 처리에 우선 순위를 매깁니다.

트랜잭션 메시지는 Adobe Campaign Standard API에서도 사용할 수 있습니다. 자세한 내용은 [전용 설명서](../../api/using/managing-transactional-messages.md)를 참조하십시오.

>[!NOTE]
>
>이제 Adobe Campaign Enhanced MTA를 통해 모든 트랜잭션 메시지를 보냄으로써 게재 능력, 처리량 및 반송 처리를 개선할 수 있습니다. 모든 영향은 표준 마케팅 메시지와 동일합니다. 자세한 내용은 이 [섹션](../../administration/using/configuring-email-channel.md)을 참조하십시오.

## 트랜잭션 메시지 정의 {#transactional-messaging-definition}

<table>
<tr>
<td align="center"><img src="assets/do-not-localize/icon_concepts.svg" width="60px"><br><p><b>트랜잭션 메시지</b></p></td>
<td><p>웹 사이트와 같은 제공업체에서 전송하는 개인 및 고유한 통신입니다.</p></td>
<td><p>받는 사람이 확인하거나 확인하려는 중요한 정보가 포함되어 있으므로 특히 예상됩니다.</p></td>
</tr>
<tr>
<td align="center"><img src="assets/do-not-localize/icon_channels.svg" width="60px"><br><p><b>언제까지 해야 합니까?</b></p></td>
<td><p> 이 메시지에는 중요한 정보가 포함되어 있으므로 사용자는 이 메시지가 실시간으로 전송될 것으로 예상하고 있습니다.</p></td>
<td><p>따라서 이벤트가 트리거되는 것과 도착하는 메시지 사이의 지연은 매우 짧아야 합니다.</p></td>
</tr>
<tr>
<td align="center"><img src="assets/do-not-localize/icon_important.svg" width="60px"><br><p><b>왜 중요하죠?</b></p></td>
<td><p>일반적으로 트랜잭션 메시지는 높은 개방률을 가집니다. 그러므로 그것은 신중하게 설계되어야 한다.</p></td>
<td><p>실제로 고객 관계를 정의하는 고객의 행동에 강한 영향을 미칠 수 있습니다.</p></td>
</tr>
<tr>
<td align="center"><img src="assets/do-not-localize/icon_example.svg" width="60px"><br><p><b>예제?</b></p></td>
<td><p>계정 생성 후 환영 메시지, 주문 발송 확인, 송장..</p></td>
<td><p>또한 암호 변경을 확인하는 메시지나 고객이 웹 사이트를 탐색한 후 알림을 받을 수 있습니다.</p></td>
</tr>
</table>

## 트랜잭션 메시지 유형

Adobe Campaign에서는 두 가지 유형의 트랜잭션 메시지를 사용할 수 있습니다.

<!--[Event transactional messages](../../channels/using/event-transactional-messages.md) targeting an **event**. The data contained in the event itself is used to define the delivery target.-->

<table>
<tr>
<td align="center"><img src="assets/do-not-localize/icon_event.svg" width="60px"><br><p><a href="../../channels/using/event-transactional-messages.md">이벤트 트랜잭션 메시지</a><br><b>는 이벤트를 타겟팅합니다</b></p></td>
<td><p><ul><li>프로필 정보는 포함하지 않습니다.</li><li>또한 <a href="../../sending/using/fatigue-rules.md">피로 규칙과는</a> 호환하지 않습니다(프로파일을 사용한 경우에도).</li><li>전달 대상은 이벤트 자체에 포함된 데이터로 정의됩니다.</li></ul></p></td>
</tr>
<tr>
<td align="center"><img src="assets/do-not-localize/icon_profile.svg" width="60px"><br><p><a href="../../channels/using/profile-transactional-messages.md">Adobe Campaign 마케팅</a><br>데이터베이스의 트랜잭션 메시지 <b>타깃팅 프로필 프로필 프로필</b></p></td>
<td><p>트랜잭션 메시지를 프로파일링하여 다음을 수행할 수 있습니다.<ul><li>차단 목록 <b>또는</b> 피로 규칙의 <a href="../../sending/using/fatigue-rules.md">주소와 같은 마케팅 유형 규칙을 적용합니다</a>.</li><li>메시지에 구독 취소 링크를 포함합니다.</li><li>트랜잭션 메시지를 글로벌 게재 보고서에 추가합니다.</li><li>트랜잭션 메시지를 고객 여정에 활용합니다.</li></ul></p></td>
</tr>
</table>

<!--[Profile transactional messages](../../channels/using/profile-transactional-messages.md) targeting **profiles from the Adobe Campaign marketing database**. You can use information from the Adobe Campaign database to send a transactional message based on customer marketing profiles.-->

메시지 유형은 트랜잭션 메시지로 변환할 이벤트를 구성할 때 정의합니다. [트랜잭션 메시지 구성](../../administration/using/configuring-transactional-messaging.md)을 참조하십시오.

>[!IMPORTANT]
>
>To access all transactional messages, you must be part of the **[!UICONTROL Administrators (all units)]** security group.

<!--Event transactional messages do not contain profile information, therefore they are not compatible with fatigue rules (even in the case of an enrichment with profiles). However, profile transactional messages are compatible. For more on fatigue rules, see [this section](../../sending/using/fatigue-rules.md#choosing-the-channel).-->

## 트랜잭션 메시지 작동 원리 {#transactional-messaging-operating-principle}

예를 들어 웹 사이트를 보유하고 있고 고객이 제품을 구입할 수 있는 웹 사이트를 보유하고 있는 회사의 예를 들어보겠습니다.

Adobe Campaign을 통해 장바구니에 제품을 추가한 사이트 사용자에게 알림 이메일을 보낼 수 있습니다. 가령 한 사용자가 구매 과정을 완료하지 않고 사이트를 떠나면 장바구니 중단 이메일을 자동으로 보냅니다.

이 작업을 수행하는 단계는 다음과 같습니다.

### 1단계 - 이벤트 구성 만들기 및 게시 {#create-event-configuration}

<!--<img src="assets/do-not-localize/icon_config.svg" width="60px">

Configure an event that will be named "Cart abandonment" and publish this event configuration.

The API that will be used by your website developer is deployed and a transactional message is automatically created.-->

<table>
<tr>
<td align="center"><img src="assets/do-not-localize/icon_config.svg" width="60px"><br><p>"장바구니 포기"라는 이름을 지정할 이벤트를 구성하고 이 이벤트 구성을 게시합니다.</p></td>
<td>웹 사이트 개발자가 사용할 API가 배포되고 트랜잭션 메시지가 자동으로 생성됩니다.</td>
</tr>
</table>

이벤트 만들기와 게시에 대한 설명은 [이벤트 트랜잭션 메시지를 보내기 위한 이벤트 구성](../../administration/using/configuring-transactional-messaging.md#use-case--configuring-an-event-to-send-a-transactional-message) 섹션에 있습니다.

### 2단계 - 트랜잭션 메시지 편집 및 게시 {#create-transactional-message}

<!--<img src="assets/do-not-localize/icon_transactional.svg" width="60px">

Edit and personalize the transactional message, test it, and then publish it.-->

<table>
<tr>
<td align="center"><img src="assets/do-not-localize/icon_notification.svg" width="45px"><br><p>트랜잭션 메시지를 편집하고 개인화하여 테스트한 다음 게시할 수 있습니다.</p></td>
<td>트랜잭션 메시지를 보낼 준비가 됩니다.</td>
</tr>
</table>

For more on editing and publishing a transactional message, see [Event transactional messages](../../channels/using/event-transactional-messages.md).

### 3단계 - 이벤트 트리거 통합 {#integrate-event-trigger}

<!--<img src="assets/do-not-localize/icon_api.svg" width="60px">

Use the REST Transactional Messages API to integrate the event into your website.

The event will be triggered when a client abandons their cart.-->

<table>
<tr>
<td align="center"><img src="assets/do-not-localize/icon_api.svg" width="60px"><br><p>REST 트랜잭션 메시지 API를 사용하여 이벤트를 웹 사이트에 통합합니다.</p></td>
<td>클라이언트가 장바구니를 포기하면 이벤트가 트리거됩니다.</td>
</tr>
</table>

이벤트를 웹 사이트에 통합하는 방법에 대한 자세한 내용은 [사이트 통합을 참조하십시오](../../administration/using/configuring-transactional-messaging.md#integrating-the-triggering-of-the-event-in-a-website).

### 4단계 - 메시지 배달 {#message-delivery}

<!--Once all of these steps have been carried out, the message can be delivered:

<img src="assets/do-not-localize/icon_notification.svg" width="40px">

As soon as a user leaves the site without ordering the products in their cart, they automatically receive a notification email.-->

<table>
<tr>
<td align="center"><img src="assets/do-not-localize/icon_channels.svg" width="60px"><br><p>이러한 모든 단계를 수행한 후 메시지가 전달될 수 있습니다.</p></td>
<td>사용자가 장바구니에 제품을 주문하지 않고 사이트를 떠나면 알림 이메일을 자동으로 받게 됩니다.</td>
</tr>
</table>

## 주요 단계 {#key-steps}

Adobe Campaign에서 개인화된 트랜잭션 메시지를 만들고 관리할 때의 주요 단계는 아래 차트에 요약되어 있습니다.

![](assets/message-center-overview.png)

<!--## Transactional messaging publication process {#transactional-messaging-pub-process}

The chart below illustrates the whole transactional messaging publication process.

![](assets/message-center_pub-process.png)

For more on the event configuration steps, see [Transactional messaging configuration](../../administration/using/configuring-transactional-messaging.md).

Read more:

* [About transactional messaging](../../channels/using/about-transactional-messaging.md)
* [Event transactional messages](../../channels/using/event-transactional-messages.md)
* [Profile transactional messages](../../channels/using/profile-transactional-messages.md)
* [Transactional push notifications](../../channels/using/transactional-push-notifications.md)
* [Follow-up messages](../../channels/using/follow-up-messages.md)-->

**관련 항목:**

* [메시지 보내기 주요 단계](../../channels/using/key-steps-to-send-a-message.md)
* [소통 채널 시작](../../channels/using/get-started-communication-channels.md)