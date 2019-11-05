---
title: 메시지 예약 기본 정보
description: 메시지를 예약하는 방법을 알아봅니다.
page-status-flag: 활성화 안 함
uuid: 286fceee-65a9-4cb9-b205-9ce5d024675c
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 보내기
content-type: reference
topic-tags: 예약 메시지
discoiquuid: 9c7fd670-bba9-4f3c-8cb1-87397a1acd27
context-tags: 배달,예약,뒤로
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 메시지 예약 기본 정보{#about-scheduling-messages}

>[!CAUTION]
>
>배달 일정을 변경할 때마다 확인(Confirm)을 클릭하기 전에 준비(Prepare) **버튼을 클릭하여** 배달을 다시 준비해야 **합니다**.

메시지 대시보드에서 **[!UICONTROL Schedule]** 블록을 사용하면 메시지(이메일, SMS 또는 푸시 알림)가 전송될 시기를 정의할 수 있습니다.

![](assets/delivery_dashboard.png)

이 **[!UICONTROL Schedule]** 속성을 사용하여 이메일, SMS 또는 푸시 알림에 대한 전송 옵션을 설정할 수 있습니다.

* **[!UICONTROL Messages to be sent once confirmed]**:전송이 확인되는 즉시 메시지가 전송됩니다. See [Confirming the send](../../sending/using/confirming-the-send.md).

   ![](assets/delivery_planning_1.png)

* **[!UICONTROL Messages to be sent automatically on the date specified below]**:메시지는 나중에 보내집니다. 전송 시작 **필드에서 연락처 날짜를** 지정합니다 **** .

   전송을 준비하고 확인할 수 있지만 메시지는 선택한 날짜 및 시간에서만 전송됩니다. 전송 준비 및 확인은 전송 [준비](../../sending/using/preparing-the-send.md) 및 보내기 [섹션](../../sending/using/confirming-the-send.md) 확인에나와 있습니다.

   드롭다운 **[!UICONTROL Time zone of the contact date]** 목록을 사용하면 전송 시간을 고려할 시간대를 수정할 수 있습니다. 예를 들어, 필드에 오전 9시를 입력하고 **[!UICONTROL Start sending from]** **[!UICONTROL Time zone of the contact date]** 드롭다운 목록에서 브뤼셀, 코펜하겐, 마드리드, 파리(GMT+1)를 선택하면 모든 수신자는 오전 9시에 메시지를 수신하게 됩니다. 따라서 모스크바에 있는 수신자(GMT+3)는 오전 11시 모스크바 시간에 메시지를 수신하게 됩니다.

   전송을 수동으로 확인하려면 **[!UICONTROL Request confirmation before sending messages]** 옵션을 선택합니다. 이 옵션은 기본적으로 활성화되어 있습니다.

   ![](assets/delivery_planning.png)

>[!CAUTION]
>
>배달을 복제할 때 모든 예약 설정이 삭제됩니다. 새 연락처 날짜를 예약하지 않는 경우 전송이 확인되는 즉시 중복된 배달이 전송됩니다.

**관련 항목**:

* [보내는 시각 최적화](../../sending/using/optimizing-the-sending-time.md)
* [받는 사람의 시간대에 맞추어 메시지 보내기](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md)
* [보내는 날짜 계산](../../sending/using/computing-the-sending-date.md)

