---
title: 전송 시간 최적화
seo-title: 전송 시간 최적화
description: 전송 시간 최적화
seo-description: 보내는 시간을 설정하고 메시지의 개방형 비율을 개선하는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: C 2 C 13934-9819-4 E 18-B 5 C 7-60915 C 907 F 37
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 전송
content-type: 참조
topic-tags: sheduling-messages
discoiquuid: 609355 f 6-9003-41 b 9-9981-ea 787419 fbf 5
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 6a877d878f01fa1e541dc20b8b0941602113d15b

---


# Optimizing the sending time{#optimizing-the-sending-time}

메시지의 열린 비율을 개선하기 위해 수신자당 보내는 시간을 수동으로 정의할 수 있습니다. 각 프로필은 가능하면 지정된 날짜와 시간에 메시지를 받게 됩니다.

전송 시간 정의는 배달 수준에서 또는 워크플로우를 사용하여 수행할 수 있습니다.

이메일의 경우 서버 로드와 재시도 양에 따라 각 받는 사람에 대해 예약된 날짜와 시간에 메시지를 전송하기 위해 최선의 노력을 기울일 것입니다.

* 재시도는 인터넷 공급자와 사용자의 명성을 좌우합니다. 메시지는 첫 번째 시도에서 허용되지 않을 수 있으며 여러 번 시도할 수 있습니다. See [List of email channel parameters](../../administration/using/configuring-email-channel.md).
* 대역폭이 불충분하여 이메일 수신이 지연될 수 있습니다.

You can view when the message was sent to each recipient in the [sending logs](../../sending/using/monitoring-a-delivery.md#sending-logs).

다음과 같은 여러 옵션을 사용할 수 있습니다.

* **[!UICONTROL No optimization]**: 메시지는 사용자의 시간에 전송됩니다.

   For example, if your time zone is GMT+1 and if you enter 9:00 AM in the **[!UICONTROL Start sending from]** field, a recipient located in the GMT+3 time zone will receive the message at 11:00 AM local time for that recipient.

* **[!UICONTROL Send at the recipient's time zone]**: 모든 수신자는 시간대가 고려된 메시지를 받게 됩니다.

   For example, if you enter 9:00 AM in the **[!UICONTROL Start sending from]** field, a recipient located in the GMT+3 time zone will receive the message at 9:00 AM local time for that recipient.

   See [Sending messages at the recipient's time zone](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md).

* **[!UICONTROL Send at a custom date defined by a formula]**: 각 수신자는 지정된 공식으로 구성된 날짜와 시간에 메시지를 받게 됩니다.

   See [Computing the sending date](../../sending/using/computing-the-sending-date.md).

