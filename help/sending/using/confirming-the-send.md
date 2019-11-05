---
title: 보내기 확인
description: 메시지 준비 완료 방법을 알아봅니다.
page-status-flag: 활성화 안 함
uuid: 1eecb32-ffd2-45d0-a8b4-f97bee59a1bd
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 보내기
content-type: reference
topic-tags: 전송 및 추적 메시지
discoiquuid: 8bb160b1-7de9-4c1f-bb89-b2e5fdafed41
context-tags: 전달,배포,뒤로
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 보내기 확인{#confirming-the-send}

메시지 준비를 완료하고 승인 단계가 수행되면 메시지를 보낼 수 있습니다. 메시지 준비에 대한 자세한 내용은 보내기 [준비를 참조하십시오](../../sending/using/preparing-the-send.md).

역할을 가진 사용자만 전송을 확인할 수 **[!UICONTROL Start deliveries]** 있습니다. 자세한 내용은 역할 [목록](../../administration/using/list-of-roles.md) 섹션을 참조하십시오.

이 역할이 없는 사용자에게는 다음 메시지가 표시됩니다.

![](assets/confirm_delivery_2.png)

배달을 보내려면 메시지 작업 표시줄에 있는 **[!UICONTROL Confirm send]** 단추를 클릭합니다.

![](assets/confirm_delivery.png)

이 **[!UICONTROL OK]** 단추를 클릭하여 전송을 확정할지 묻는 메시지가 나타납니다.

![](assets/confirm_delivery1.png)

메시지를 보내는 중입니다.

>[!NOTE]
>
>메시지가 예약된 경우 전송 시간에 도달하면 전송됩니다. For more on scheduling messages, refer to [this section](../../sending/using/about-scheduling-messages.md).

합계 기간이 없는 반복 배달을 사용하는 경우 배달을 보내기 전에 확인을 요청할 수 있습니다. 이렇게 하려면 배달 대시보드의 **[!UICONTROL Schedule]** 블록을 연 다음 전용 옵션을 활성화합니다.

![](assets/confirmation_recurring_deliveries.png)

이 **[!UICONTROL Deployment]** 블록은 전송 진행 상황을 보여줍니다.

메시지가 연락처에 전송되면 **[!UICONTROL Deployment]** 영역에 다음을 포함한 KPI(주요 성과 지표) 데이터가 표시됩니다.

* 전달할 메시지 수
* 보낸 메시지 수
* 배달된 메시지의 비율
* 바운스 및 오류 비율
* 열린 메시지의 비율
* 메시지의 클릭 비율(이메일)

   >[!NOTE]
   >
   >및 **[!UICONTROL Open rate]** **[!UICONTROL Click-through rate]** 업데이트가 매시간 업데이트됩니다.

![](assets/sending_delivery.png)

KPI가 업데이트되는 데 너무 오래 걸리거나 전송 로그의 결과를 고려하지 않는 경우 **[!UICONTROL Compute stats]** 창의 **[!UICONTROL Deployment]** 단추를 클릭합니다.

![](assets/sending_delivery7.png)

대상자의 일부를 구성하는 클라이언트 프로필 중 하나의 기록에서 메시지를 볼 수 있습니다. See [Integrated customer profile](../../audiences/using/integrated-customer-profile.md).

메시지가 전송되면 수신자의 동작을 추적하고 영향력을 측정할 수 있습니다. 자세한 내용은 다음 섹션을 참조하십시오.

* [메시지 추적](../../sending/using/tracking-messages.md)
* [게재 모니터링](../../sending/using/monitoring-a-delivery.md)

