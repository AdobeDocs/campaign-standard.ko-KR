---
title: 보내는 시각 최적화
description: 전송 시간을 설정하고 메시지 공개 비율을 개선하는 방법을 알아봅니다.
page-status-flag: 활성화 안 함
uuid: c2c13934-9819-4e18-b5c7-60915c907f37
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 보내기
content-type: reference
topic-tags: 예약 메시지
discoiquuid: 609355f6-9003-41b9-9981-ea787419fbf5
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 보내는 시각 최적화{#optimizing-the-sending-time}

메시지의 공개 비율을 개선하기 위해 수신자당 전송 시간을 수동으로 정의할 수 있습니다. 각 프로필은 가능한 한 지정된 날짜와 시간에 메시지를 수신합니다.

전송 시간 정의는 배달 수준에서 또는 워크플로우를 사용하여 수행할 수 있습니다.

이메일의 경우 서버 로드 및 재시도 횟수에 따라 각 수신자에 대해 예약된 날짜와 시간에 메시지를 전송하는 것이 가장 좋습니다.

* 재시도는 인터넷 공급자와 사용자의 평판에 따라 다릅니다. 첫 번째 시도에서 메시지가 수락되지 않을 수 있으며 여러 번 시도할 수 있습니다. 이메일 [채널 매개 변수](../../administration/using/configuring-email-channel.md)목록을 참조하십시오.
* 대역폭이 부족하여 이메일 수신이 지연될 수 있습니다.

메시지를 [전송 로그의](../../sending/using/monitoring-a-delivery.md#sending-logs)각 수신자에게 보낸 시간을 볼 수 있습니다.

다음과 같은 몇 가지 옵션을 사용할 수 있습니다.

* **[!UICONTROL No optimization]**:메시지가 사용자의 시간에 전송됩니다.

   예를 들어 시간대가 GMT+1이고 **[!UICONTROL Start sending from]** 필드에 오전 9시를 입력하면 GMT+3 시간대의 수신자는 해당 수신자의 현지 시간으로 오전 11시에 메시지를 수신하게 됩니다.

* **[!UICONTROL Send at the recipient's time zone]**:모든 수신자는 시간대를 고려하여 메시지를 수신하게 됩니다.

   예를 들어, 필드에 오전 9:00을 입력하면 GMT+3 시간대의 수신자는 해당 수신자의 현지 시간으로 오전 9:00에 메시지를 수신하게 됩니다. **[!UICONTROL Start sending from]**

   See [Sending messages at the recipient's time zone](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md).

* **[!UICONTROL Send at a custom date defined by a formula]**:각 수신자는 지정된 수식으로 구성된 날짜 및 시간에 메시지를 수신하게 됩니다.

   See [Computing the sending date](../../sending/using/computing-the-sending-date.md).

