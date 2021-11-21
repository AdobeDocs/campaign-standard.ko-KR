---
title: Adobe Campaign Standard에서 게재 기능 모니터링
description: Adobe Campaign Standard에서 제공하는 도구를 사용하여 플랫폼의 게재 기능을 모니터링합니다.
audience: sending
content-type: reference
topic-tags: sheduling-messages
context-tags: delivery,schedule,back
feature: Deliverability
role: User
level: Intermediate
exl-id: 683341fb-fef5-4aa1-8606-9526d9ae6290
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 10%

---

# 전달성 모니터링{#monitor-deliverability}

아래에는 **[!UICONTROL Delivery throughput]** 보고서 및 Adobe Campaign에서 제공하는 다양한 모니터링 도구를 제공합니다. 다음은 게재 기능 모니터링에 대한 몇 가지 추가 지침입니다.
* 전체 플랫폼에 대한 게재 처리량을 정기적으로 확인하여 원래 설정과 일치하는지 확인합니다.
* 다시 시도가 게재 템플릿에서 올바르게 설정되었는지(다시 시도 기간의 경우 30분, 20번 이상 다시 시도) 확인합니다.
* 바운스 사서함에 액세스할 수 있고 계정이 만료되지 않았는지 정기적으로 확인합니다.
* 각 게재 처리량을 확인하여 게재 컨텐츠의 유효성(예: &#39;플래시 판매&#39;는 며칠이 아니라 몇 분 안에 배달되어야 합니다.
* 오류 및 새 격리 수가 다른 게재와 일치하는지 확인합니다.
* 강조 표시된 오류 유형(차단 목록, DNS 문제, 스팸 방지 규칙 등)을 확인하려면 게재 로그를 자세히 참조하십시오.

## 게재 처리량 {#delivery-throughput}

이 보고서에는 특정 기간 동안 전체 플랫폼의 게재 처리량에 대한 정보를 포함하여 메시지가 전달되는 속도를 측정합니다.

자세한 내용은 [게재 처리량](../../reporting/using/delivery-throughput.md).

![](assets/delivery_reports_1.png)

시간 표시줄을 변경하여 표시되는 값을 구성할 수 있습니다.

다음과 같은 다른 보고서를 사용할 수 있습니다 **[!UICONTROL Delivery summary]** 또는 **[!UICONTROL Non-deliverables and bounces]**. 자세한 내용은 [동적 보고서](../../reporting/using/about-dynamic-reports.md).

## 게재 모니터링 {#monitoring-deliveries}

메시지 대시보드에서 게재 로그에 액세스할 수 있습니다. **[!UICONTROL Sending logs]**, **[!UICONTROL Exclusion logs]**, **[!UICONTROL Exclusion causes]**, **[!UICONTROL Tracking logs]** 및 **[!UICONTROL Tracked URLs]**. 여기에는 전송 세부 사항과 제외된 타겟 및 그 이유와 함께 오픈과 클릭 등의 추적 정보가 표시됩니다.

자세한 내용은 [게재 모니터링](../../sending/using/monitoring-a-delivery.md).

![](assets/sending_delivery1.png)

## 경고 수신 {#receiving-alerts}

다음 **[!UICONTROL Delivery alerting]** 기능은 사용자 그룹이 게재 실행에 대한 정보가 포함된 알림을 자동으로 수신할 수 있는 경고 관리 시스템입니다.

자세한 내용은 [게재 실패 시 경고 받기](../../sending/using/receiving-alerts-when-failures-happen.md).

<!--## External tools (#external-tools)

### Signal Spam {#signal-spam}

Signal Spam is a French service which offers anonymized feedback loop reporting for French ISPs (Orange, SFR).

This service allows you to follow the reputation of the French ISPs and track customers' activity evolution.

Signal Spam also provides direct complaints that end users log through a dedicated interface. Those complaints are then quarantined from the email address database.

### 250ok {#solution-250ok}

250ok is a monitoring solution which provides IP and domain denylists, as well as reputation indicators.

The information provided is real-time, which allows for a pro-active assistance. 250ok a complementary solution to the Adobe deliverability internal tools.-->
