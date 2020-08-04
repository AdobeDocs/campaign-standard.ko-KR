---
title: 보내는 시간 최적화
description: 보내는 시간을 설정하고 메시지 열람률을 향상시키는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: c2c13934-9819-4e18-b5c7-60915c907f37
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sheduling-messages
discoiquuid: 609355f6-9003-41b9-9981-ea787419fbf5
internal: n
snippet: y
translation-type: ht
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e
workflow-type: ht
source-wordcount: '272'
ht-degree: 100%

---


# 보내는 시간 최적화{#optimizing-the-sending-time}

메시지 열람률을 향상시키기 위해 수신자마다 보내는 시간을 수동으로 정의할 수 있습니다. 각 프로필은 가능한 한 지정된 날짜와 시간에 메시지를 수신합니다.

보내는 시간 정의는 게재 수준에서 수행하거나 워크플로우를 사용하여 수행할 수 있습니다.

이메일의 경우 서버 부하 및 다시 시도 횟수에 따라 각 수신자에 대해 예약된 날짜와 시간에 메시지를 보내기 위해 최선을 다합니다.

* 다시 시도는 인터넷 공급자와 사용자의 평판에 따라 다릅니다. 첫 번째 시도에서는 메시지가 수락되지 않을 수 있으며 여러 번 다시 시도할 수 있습니다. [이메일 채널 매개 변수 목록](../../administration/using/configuring-email-channel.md)을 참조하십시오.
* 대역폭 부족으로 인해 이메일 수신이 지연될 수 있습니다.

[전송 로그](../../sending/using/monitoring-a-delivery.md#sending-logs)에서 각 수신자에게 메시지가 전송된 시기를 볼 수 있습니다.

몇 가지 옵션을 사용할 수 있습니다.

* **[!UICONTROL No optimization]**: 메시지가 사용자의 시간대에 전송됩니다.

   예를 들어 시간대가 GMT+1이고 **[!UICONTROL Start sending from]** 필드에 오전 9시를 입력하면 GMT+3 시간대에 있는 수신자는 해당 수신자의 현지 시간으로 오전 11시에 메시지를 수신하게 됩니다.

* **[!UICONTROL Send at the recipient's time zone]**: 모든 수신자는 시간대를 고려하여 메시지를 수신하게 됩니다.

   예를 들어 **[!UICONTROL Start sending from]** 필드에 오전 9시를 입력하면 GMT+3 시간대에 있는 수신자는 해당 수신자의 현지 시간으로 오전 9시에 메시지를 수신하게 됩니다.

   [수신자의 시간대에 맞추어 메시지 보내기](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md)를 참조하십시오.

* **[!UICONTROL Send at a custom date defined by a formula]**: 각 수신자는 지정된 수식으로 구성된 날짜 및 시간에 메시지를 수신하게 됩니다.

   [보내는 날짜 계산](../../sending/using/computing-the-sending-date.md)을 참조하십시오.

