---
title: Adobe Campaign Standard에서 게재 모니터링
description: Adobe Campaign Standard에서 배달을 모니터링하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: 7772c607-debd-40fd-8322-4d49119979b4
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: monitoring-messages
discoiquuid: eb9fa216-4568-423a-9396-8f7b82181ae9
context-tags: delivery,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 54612511de07edc3e6f3eea34ef095c26b35f4af

---


# 게재 모니터링{#monitoring-a-delivery}

전달을 모니터링하고 영향력을 측정하는 방법에는 몇 가지가 있습니다.

* **메시지 로그**:이러한 로그는 메시지 대시보드에서 직접 액세스할 수 있습니다. 여기에는 제외된 대상 및 이유와 열기 및 클릭과 같은 추적 정보가 표시됩니다.

   메시지 로그를 보려면 **[!UICONTROL Deployment]** 블록의 오른쪽 하단에 있는 아이콘을 클릭합니다.

   몇 개의 탭에는 **[!UICONTROL Sending logs]**, **[!UICONTROL Exclusion logs]**, **[!UICONTROL Exclusion causes]****[!UICONTROL Tracking logs]** 및 **[!UICONTROL Tracked URLs]**&#x200B;에 대한 정보(있는 경우)가 포함되어 있습니다. 배달 [로그를](#delivery-logs)참조하십시오.

   ![](assets/sending_delivery1.png)

   로그에는 게재 및 교정본 내용과 관련된 모든 메시지가 포함됩니다. 특정 아이콘을 사용하여 오류 또는 경고를 식별할 수 있습니다. 자세한 내용은 메시지 [승인을](../../sending/using/previewing-messages.md)참조하십시오.

   단추를 클릭하여 로그를 내보낼 수 **[!UICONTROL Export list]** 있습니다.

   ![](assets/sending_delivery2.png)

* **전달 경고**:Adobe Campaign은 전달 성공 또는 실패를 추적하기 위해 사용자에게 중요한 시스템 활동을 알리는 알림을 전송하는 이메일 알림 시스템을 제공합니다.
* **보고서**:메시지 대시보드에서 이 특정 메시지에 대한 여러 보고서에 액세스할 수 있습니다. 메시지 또는 캠페인과 관련된 특정 지표의 개요를 설명하는 데 사용할 수 있는 기본 제공 또는 사용자 지정 보고서의 전체 목록에 액세스할 수 있는 **[!UICONTROL Reports]** 메뉴가 있습니다.
* 관리자는 별도의 파일로 로그를 내보내 보고 또는 BI 도구에서 처리할 수도 있습니다. 자세한 내용은 로그 [내보내기를 참조하십시오](../../automating/using/exporting-logs.md).

**관련 항목:**

* [게재 실패 시 경고 받기](../../sending/using/receiving-alerts-when-failures-happen.md)
* [보고서](../../reporting/using/about-dynamic-reports.md)

## 배달 로그 {#delivery-logs}

### 로그 보내기 {#sending-logs}

이 **[!UICONTROL Sending logs]** 탭에는 이 배달의 모든 발생 내역이 표시됩니다. 보낸 메시지 및 상태 목록은 여기에 저장됩니다. 각 수신자의 배달 상태를 볼 수 있습니다.

상태가 **[!UICONTROL Sent]** 있는 각 프로필에 대해 메시지가 전송된 **[!UICONTROL Date]** 시간이 열에 표시됩니다.

![](assets/sending_delivery3.png)

특정 전송 로그의 세부 정보에 액세스하려면 해당 행 오른쪽에 있는 연필 아이콘을 클릭합니다.

![](assets/sending_access-sending-log.png)

모든 전송 로그 세부 사항은 읽기 전용입니다. 미러 페이지의 미리 보기도 볼 수 있습니다.

![](assets/sending_sending-log.png)

>[!NOTE]
>
>Campaign 사용자 인터페이스에 미러 페이지 렌더링을 표시하려면 미러 페이지 서버 URL이 안전해야 합니다. 이러한 경우, 브랜드를 [구성할 때 이 URL을 설정하려면 http://이 아닌 https://을 사용하십시오](../../administration/using/branding.md#configuring-and-using-brands).

### 제외 로그 {#exclusion-logs}

이 **[!UICONTROL Exclusion logs]** 탭에는 전송된 대상에서 제외된 모든 메시지가 나열되며 전송 실패 이유를 지정합니다.

![](assets/sending_delivery4.png)

### 제외 원인 {#exclusion-causes}

이 **[!UICONTROL Exclusion causes]** 탭에는 대상 전송에서 제외된 메시지의 볼륨(메시지 수)이 표시됩니다.

![](assets/sending_delivery5.png)
