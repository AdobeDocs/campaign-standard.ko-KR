---
title: 메시지 예약 기본 정보
description: 메시지를 예약하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: 286fceee-65a9-4cb9-b205-9ce5d024675c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sheduling-messages
discoiquuid: 9c7fd670-bba9-4f3c-8cb1-87397a1acd27
context-tags: delivery,schedule,back
internal: n
snippet: y
translation-type: ht
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e
workflow-type: ht
source-wordcount: '268'
ht-degree: 100%

---


# 메시지 예약 기본 정보{#about-scheduling-messages}

>[!CAUTION]
>
>게재 일정을 변경할 때마다 **확인**&#x200B;을 클릭하기 전에 **준비** 버튼을 클릭하여 게재를 다시 준비해야 합니다 .

메시지 대시보드에서 **[!UICONTROL Schedule]** 블록을 사용하면 메시지(이메일, SMS 또는 푸시 알림)를 보낼 시점을 정의할 수 있습니다.

![](assets/delivery_dashboard.png)

**[!UICONTROL Schedule]** 속성을 사용하여 이메일, SMS 또는 푸시 알림에 대한 전송 옵션을 설정할 수 있습니다.

* **[!UICONTROL Messages to be sent once confirmed]**: 전송 작업을 확인하는 즉시 메시지가 전송됩니다. [전송 확인](../../sending/using/confirming-the-send.md)을 참조하십시오.

   ![](assets/delivery_planning_1.png)

* **[!UICONTROL Messages to be sent automatically on the date specified below]**: 이후 날짜 및 시간을 설정하여 메시지를 전송합니다. **다음 시점부터 전송 시작** 필드에서 **연락 날짜**&#x200B;를 지정합니다.

   전송을 준비하고 확인할 수 있지만, 메시지는 선택한 날짜 및 시간에만 전송됩니다. 전송을 준비하고 확인하는 방법은 [전송 준비](../../sending/using/preparing-the-send.md) 및 [전송 확인](../../sending/using/confirming-the-send.md) 섹션에 나와 있습니다.

   **[!UICONTROL Time zone of the contact date]** 드롭다운 목록에서 전송 시간 설정 시 고려할 시간대를 수정할 수 있습니다. 예를 들어, **[!UICONTROL Start sending from]** 필드에 오전 9시를 입력하고 **[!UICONTROL Time zone of the contact date]** 드롭다운 목록에서 브뤼셀, 코펜하겐, 마드리드, 파리(GMT+1)를 선택하면 모든 수신자는 파리 시간으로 오전 9시에 메시지를 수신하게 됩니다. 따라서 모스크바(GMT+3)에 있는 수신자는 모스크바 시간으로 오전 11시에 메시지를 수신하게 됩니다.

   전송을 수동으로 확인하려면 **[!UICONTROL Request confirmation before sending messages]** 옵션을 선택합니다. 이 옵션은 기본적으로 활성화되어 있습니다.

   ![](assets/delivery_planning.png)

>[!CAUTION]
>
>게재를 복제하면 모든 예약 설정이 삭제됩니다. 새 연락 날짜를 예약하지 않으면 전송을 확인하는 즉시 복제한 게재가 전송됩니다.

**관련 항목**:

* [보내는 시각 최적화](../../sending/using/optimizing-the-sending-time.md)
* [수신자의 시간대에 맞추어 메시지 보내기](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md)
* [보내는 날짜 계산](../../sending/using/computing-the-sending-date.md)

