---
title: 보내는 시간 최적화
description: 보내는 시간을 설정하고 메시지 열람률을 향상시키는 방법을 알아봅니다.
audience: sending
content-type: reference
topic-tags: sheduling-messages
feature: Send Time Optimization
role: User
level: Intermediate
exl-id: f35b46c6-de88-4efa-b3b7-8bb9024e40a8
TQID: https://experienceleague.adobe.com/FjL5t1ohvrgDdqLiCr03z1Nbq6IukIBysKkmXJ7561c
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 279
ht-degree: 74%

---

# 보내는 시간 최적화{#optimizing-the-sending-time}

메시지 열람률을 향상시키기 위해 수신자마다 보내는 시간을 수동으로 정의할 수 있습니다. 각 프로필은 가능한 한 지정된 날짜와 시간에 메시지를 수신합니다.

보내는 시간 정의는 게재 수준에서 수행하거나 워크플로를 사용하여 수행할 수 있습니다.

이메일의 경우 서버 부하 및 다시 시도 횟수에 따라 각 수신자에 대해 예약된 날짜와 시간에 메시지를 보내기 위해 최선을 다합니다.

* 다시 시도는 인터넷 공급자와 사용자의 평판에 따라 다릅니다. 첫 번째 시도에서는 메시지가 수락되지 않을 수 있으며 여러 번 다시 시도할 수 있습니다. [이메일 채널 매개 변수 목록](../../administration/using/configuring-email-channel.md)을 참조하십시오.
* 대역폭 부족으로 인해 이메일 수신이 지연될 수 있습니다.

[전송 로그](../../sending/using/monitoring-a-delivery.md#sending-logs)에서 각 수신자에게 메시지가 전송된 시기를 볼 수 있습니다.

몇 가지 옵션을 사용할 수 있습니다.

* **[!UICONTROL No optimization]**: 메시지가 사용자의 시간대에 전송됩니다.

  예를 들어 시간대가 GMT+1이고 **[!UICONTROL Start sending from]** 필드에 오전 9시:00을 입력하면 GMT+3 시간대에 있는 수신자는 해당 수신자의 현지 시간으로 오전 11시:00에 메시지를 수신하게 됩니다.

* **[!UICONTROL Send at the recipient's time zone]**: 모든 수신자는 시간대를 고려하여 메시지를 수신하게 됩니다.

  예를 들어 **[!UICONTROL Start sending from]** 필드에 오전 9:00시를 입력하면 GMT+3 시간대에 있는 수신자는 해당 수신자의 현지 시간으로 오전 9:00시에 메시지를 수신하게 됩니다.

  [수신자의 시간대에 맞추어 메시지 보내기](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md)를 참조하십시오.

* **[!UICONTROL Send at a custom date defined by a formula]**: 각 수신자는 지정된 수식으로 구성된 날짜 및 시간에 메시지를 수신하게 됩니다.

  [보내는 날짜 계산](../../sending/using/computing-the-sending-date.md)을 참조하십시오.
