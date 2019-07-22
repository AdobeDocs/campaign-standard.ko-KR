---
title: 전송 확인
seo-title: 전송 확인
description: 전송 확인
seo-description: 메시지 준비 완료 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: 1 eaecb 32-ffd 2-45 d 0-a 8 b 4-f 97 bee 59 a 1 bd
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 전송
content-type: 참조
topic-tags: 전송 및 추적 메시지
discoiquuid: 8 bb 160 b 1-7 de 9-4 c 1 f-bb 89-b 2 e 5 fdafed 41
context-tags: 전달, 배포, 뒤로
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: e9dd7c374903d0c57ac4881ed125c3215bd7fe11

---


# Confirming the send{#confirming-the-send}

메시지 준비를 완료하고 승인 단계를 완료하면 보낼 수 있습니다. For more on messages preparation, refer to [Preparing the send](../../sending/using/preparing-the-send.md).

**[!UICONTROL Start deliveries]** 역할이 있는 사용자만 전송을 확인할 수 있습니다. For more on this, refer to the [List of roles](../../administration/using/list-of-roles.md) section.

이 역할이 없는 사용자에게는 다음 메시지가 표시됩니다.

![](assets/confirm_delivery_2.png)

To send your delivery, click the **[!UICONTROL Confirm send]** button found in the message's action bar.

![](assets/confirm_delivery.png)

You will be asked to finalize the send definitively by clicking the **[!UICONTROL OK]** button.

![](assets/confirm_delivery1.png)

메시지가 전송되고 있습니다.

>[!NOTE]
>
>메시지가 예약되면 전송 시간이 경과하면 전송됩니다. For more on scheduling messages, refer to [this section](../../sending/using/about-scheduling-messages.md).

집계 기간 없이 반복 배달을 사용하는 경우 배달이 전송되기 전에 확인을 요청할 수 있습니다. To do this, open the **[!UICONTROL Schedule]** block of the delivery dashboard, then activate the dedicated option.

![](assets/confirmation_recurring_deliveries.png)

**[!UICONTROL Deployment]** 블록은 전송 진행률을 보여줍니다.

Once the message is sent to the contacts, the **[!UICONTROL Deployment]** zone shows your KPIs (Key Performance Indicator) data , including:

* 배달할 메시지 수
* 전송된 메시지 수
* 배달된 메시지 비율
* 바운스 및 오류 비율
* 열린 메시지의 비율
* 메시지의 클릭 수 (이메일의 경우)

   >[!NOTE]
   >
   >**[!UICONTROL Open rate]****[!UICONTROL Click-through rate]** 는 항상 업데이트됩니다.

![](assets/sending_delivery.png)

If the KPIs take too long to update or don't take into account the results from the sending logs, click the **[!UICONTROL Compute stats]** button in the **[!UICONTROL Deployment]** window.

![](assets/sending_delivery7.png)

메시지는 대상의 일부를 구성하는 클라이언트 프로필 중 한 곳의 내역에서 볼 수 있습니다. [통합된 고객 프로필을 참조하십시오](../../audiences/using/integrated-customer-profile.md).

메시지가 전송되면 받는 사람의 동작을 추적하고 그 효과를 측정하기 위해 모니터링할 수 있습니다. 이에 대한 자세한 내용은 다음 섹션을 참조하십시오.

* [추적 메시지](../../sending/using/tracking-messages.md)
* [배달 모니터링](../../sending/using/monitoring-a-delivery.md)

