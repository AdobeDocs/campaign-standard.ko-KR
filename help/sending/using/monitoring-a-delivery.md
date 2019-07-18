---
title: 배달 모니터링
seo-title: 배달 모니터링
description: 배달 모니터링
seo-description: 전달을 모니터링하는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: 7772 C 607-Debd -40 FD -8322-4 D 49119979 B 4
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 전송
content-type: 참조
topic-tags: monitoring-messages
discoiquuid: EB 9 FA 216-4568-423 A -9396-8 F 7 B 82181 AE 9
context-tags: 전달, 기본
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: cb6396228e42f99f7e184a82e6c894b09a164cd9

---


# Monitoring a delivery{#monitoring-a-delivery}

배달을 모니터링하고 그 영향력을 측정하는 방법에는 몇 가지가 있습니다.

* **메시지 로그**: 이러한 로그는 메시지 대시보드에서 직접 액세스할 수 있습니다. 또한 전송 세부 사항, 대상이 제외된 이유, 열기 및 클릭과 같은 추적 정보를 표시합니다.

   To view the message logs, click the icon at the bottom right of the **[!UICONTROL Deployment]** block.

   Several tabs contain information (if it exists) regarding the **[!UICONTROL Sending logs]**, **[!UICONTROL Exclusion logs]**, **[!UICONTROL Exclusion causes]**, **[!UICONTROL Tracking logs]** and **[!UICONTROL Tracked URLs]**. [배달 로그를 참조하십시오](../../sending/using/monitoring-a-delivery.md#delivery-logs).

   ![](assets/sending_delivery1.png)

   로그에는 배달 및 증명과 관련된 모든 메시지가 포함되어 있습니다. 특정 아이콘을 사용하여 오류나 경고를 식별할 수 있습니다. For more on this, see [Approving messages](../../sending/using/previewing-messages.md).

   You can export the log by clicking the **[!UICONTROL Export list]** button.

   ![](assets/sending_delivery2.png)

* **배달 경고**: 전달 성공 또는 실패를 추적하기 위해 Adobe Campaign는 사용자에게 중요한 시스템 활동을 알리기 위해 알림을 보내는 이메일 알림 시스템을 제공합니다.
* **보고서**: 메시지 대시보드에서 이 특정 메시지에 대한 여러 보고서에 액세스할 수 있습니다. You also have a **[!UICONTROL Reports]** menu that allows you to access a complete list of built-in or custom reports that you can use to outline specific metrics related to your message or campaign.
* 관리자는 로그 또는 BI 도구에서 처리할 수 있는 별도의 파일로 로그를 내보낼 수도 있습니다. For more on this, see [Exporting logs](../../automating/using/exporting-logs.md).

**관련 항목:**

* [장애 발생 시 알림 받기](../../sending/using/receiving-alerts-when-failures-happen.md)
* [보고서](../../reporting/using/about-dynamic-reports.md)

## Delivery logs {#delivery-logs}

### Sending logs {#sending-logs}

**[!UICONTROL Sending logs]** 탭은 이 게재의 모든 발생 내역을 제공합니다. 보낸 메시지 목록과 상태는 여기에 저장됩니다. 이를 통해 각 수신자의 배달 상태를 볼 수 있습니다.

**[!UICONTROL Sent]** 상태가 있는 각 프로필에 대해 **[!UICONTROL Date]** 이 열은 메시지가 전송된 시기를 보여줍니다.

![](assets/sending_delivery3.png)

### Exclusion logs {#exclusion-logs}

**[!UICONTROL Exclusion logs]** 탭에는 전송된 Target에서 제외된 모든 메시지가 표시되며 전송 실패 이유를 지정합니다.

![](assets/sending_delivery4.png)

### Exclusion causes {#exclusion-causes}

**[!UICONTROL Exclusion causes]** 이 탭에는 Target Send에서 제외된 메시지의 볼륨 (메시지 수) 이 표시됩니다.

![](assets/sending_delivery5.png)

