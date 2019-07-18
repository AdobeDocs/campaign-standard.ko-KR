---
title: 프로필 트랜잭션 메시지
seo-title: 프로필 트랜잭션 메시지
description: 프로필 트랜잭션 메시지
seo-description: 프로필 트랜잭션 메시지를 만들고 게시하는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: a 8 EFE 979-74 AE -46 FF-A 305-B 86 A 90679581
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 채널
content-type: 참조
topic-tags: 트랜잭션 메시징
discoiquuid: DCB 90 AFC -42 C 3-419 E -8345-79 CDDF 969 E 41
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 855db33971afdf9f02bf1b00be67c9e3f50bee06

---


# Profile transactional messages{#profile-transactional-messages}

고객 마케팅 프로필을 기반으로 트랜잭션 메시지를 보낼 수 있으므로 다음을 수행할 수 있습니다.

* Apply marketing typology rules such as **[!UICONTROL Blacklisted address]** or [fatigue rules](../../administration/using/fatigue-rules.md).
* 메시지 내에 구독 취소 링크를 포함합니다.
* 트랜잭션 메시지를 전역 배달 보고에 추가합니다.
* 고객 여정의 트랜잭션 메시지를 활용합니다.

Once you have created and published an event (the cart abandonment as per the [example](../../channels/using/about-transactional-messaging.md#transactional-messaging-operating-principle) above), the corresponding transactional message is created automatically.

The configuration steps are presented in the [Configuring an event to send a profile transactional message](../../administration/using/configuring-transactional-messaging.md#use-case--configuring-an-event-to-send-a-transactional-message) section.

이벤트가 트랜잭션 메시지를 보내게 하려면 메시지를 개인화하고 테스트하여 게시해야 합니다.

>[!NOTE]
>
>To access the transactional messages, you must have administration rights or appear in the **[!UICONTROL Message Center agents]** (mcExec) security group. 피로 규칙은 프로필 트랜잭션 메시지와 호환됩니다. [피로 규칙을 참조하십시오](../../administration/using/fatigue-rules.md).

## Sending a profile transactional message {#sending-a-profile-transactional-message}

프로필 트랜잭션 메시지를 만들고, 개인화하고, 게시하는 단계는 이벤트 트랜잭션 메시지의 경우와 동일합니다. [이벤트 트랜잭션 메시지를 참조하십시오](../../channels/using/event-transactional-messages.md).

차이점은 다음과 같습니다.

1. 편집할 수 있도록 만들어진 트랜잭션 메시지를 이동합니다.
1. In the transactional message, click the **[!UICONTROL Content]** section. In addition to the transactional template, you can also choose the default email template, which targets **[!UICONTROL Profile]**.

   ![](assets/message-center_marketing_templates.png)

1. 기본 이메일 템플릿을 선택합니다.

   모든 마케팅 이메일과 유사하게, 여기에는 구독 취소 링크가 포함됩니다.

   ![](assets/message-center_marketing_perso_unsubscription.png)

   또한 실시간 이벤트를 기반으로 하는 구성과 달리 모든 프로파일 정보를 직접 액세스하여 메시지를 개인화할 수 있습니다. See [Inserting a personalization field](../../designing/using/inserting-a-personalization-field.md).

1. 변경 내용을 저장하고 메시지를 게시합니다. See [Publishing a transactional message](../../channels/using/event-transactional-messages.md#publishing-a-transactional-message).

## Monitoring a profile transactional message delivery {#monitoring-a-profile-transactional-message-delivery}

메시지가 게시되고 사이트 통합이 완료되면 게재를 모니터링할 수 있습니다.

1. To view the message delivery log, click the icon at the bottom right of the **[!UICONTROL Deployment]** block.

   For more information on accessing the logs, see [Monitoring the delivery](../../sending/using/monitoring-a-delivery.md).

1. **[!UICONTROL Sending logs]** 탭을 선택합니다. **[!UICONTROL Status]** 열에서 **[!UICONTROL Sent]** 프로파일이 선택되었음을 나타냅니다.

   ![](assets/message-center_marketing_sending_logs.png)

1. **[!UICONTROL Exclusions logs]** 차단된 주소와 같이 메시지 대상에서 제외된 수신자를 보려면 탭을 선택합니다.

   ![](assets/message-center_marketing_exclusion_logs.png)

For any profile that has opted out, the **[!UICONTROL Blacklisted address]** typology rule excluded the corresponding recipient.

This rule is part of a specific typology that applies to all transactional messages based on the **[!UICONTROL Profile]** table.

![](assets/message-center_marketing_typology.png)

**관련 항목**:

* [사이트 통합](../../administration/using/configuring-transactional-messaging.md#integrating-the-triggering-of-the-event-in-a-website)
* [유형 체계](../../administration/using/about-typology-rules.md)

