---
solution: Campaign Standard
product: campaign
title: Adobe Campaign Standard의 모니터링 제공
description: Adobe Campaign Standard에서 제공하는 툴을 사용하여 플랫폼 제공 여부를 모니터링할 수 있습니다.
audience: sending
content-type: reference
topic-tags: sheduling-messages
context-tags: delivery,schedule,back
feature: 게재 가능성
role: 비즈니스 전문가
level: 중간
translation-type: tm+mt
source-git-commit: fb9a6218bb754f803affde1fdf6c6fc01570126f
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 10%

---


# 게재 기능 모니터링{#monitor-deliverability}

아래에서 Adobe Campaign에서 제공하는 다양한 모니터링 도구와 **[!UICONTROL Delivery throughput]** 보고서에 대한 세부 정보를 확인할 수 있습니다. 다음은 제공 가능성 모니터링에 대한 몇 가지 추가 지침입니다.
* 전체 플랫폼에 대한 배달 처리량을 정기적으로 확인하여 원래 설정과 일치하는지 확인합니다.
* 배달 템플릿에서 재시도 횟수가 올바르게 설정되어 있는지 확인합니다(재시도 기간은 30분, 재시도 횟수는 20회 이상).
* 바운스 사서함에 액세스할 수 있으며 계정이 만료되지 않도록 정기적으로 확인합니다.
* 각 전달 처리량을 확인하여 배달 컨텐츠의 유효성(예:&#39;flash sales&#39;는 며칠이 아니라 몇 분 내에 배달됩니다.)
* 오류 수와 새 검역소가 다른 배달물과 일치하는지 확인하십시오.
* 강조 표시된 오류 유형(차단 목록, DNS 문제, 스팸 방지 규칙 등)을 확인하려면 전달 로그에 자세히 문의하십시오.

## 게재 처리량 {#delivery-throughput}

이 보고서에는 지정된 기간 동안 전체 플랫폼의 배달 처리량에 대한 정보가 포함되어 있어 메시지가 전달되는 속도를 측정합니다.

이에 대한 자세한 내용은 [배달 처리량](../../reporting/using/delivery-throughput.md)을 참조하십시오.

![](assets/delivery_reports_1.png)

시간 표시줄을 변경하여 표시되는 값을 구성할 수 있습니다.

**[!UICONTROL Delivery summary]** 또는 **[!UICONTROL Non-deliverables and bounces]** 등의 다른 보고서를 사용할 수 있습니다. 자세한 내용은 [동적 보고서](../../reporting/using/about-dynamic-reports.md)를 참조하십시오.

## 게재 모니터링 {#monitoring-deliveries}

메시지 대시보드에서는 배달 로그에 액세스할 수 있습니다.**[!UICONTROL Sending logs]**, **[!UICONTROL Exclusion logs]**, **[!UICONTROL Exclusion causes]**, **[!UICONTROL Tracking logs]** 및 **[!UICONTROL Tracked URLs]**. 여기에는 전송 세부 사항과 제외된 타겟 및 그 이유와 함께 오픈과 클릭 등의 추적 정보가 표시됩니다.

자세한 내용은 [배달](../../sending/using/monitoring-a-delivery.md) 모니터링을 참조하십시오.

![](assets/sending_delivery1.png)

## 경고 수신 중 {#receiving-alerts}

**[!UICONTROL Delivery alerting]** 기능은 사용자 그룹이 배달 실행에 대한 정보가 포함된 알림을 자동으로 수신할 수 있도록 해주는 경고 관리 시스템입니다.

이에 대한 자세한 내용은 [오류가 발생할 때 경고 받기](../../sending/using/receiving-alerts-when-failures-happen.md)를 참조하십시오.

<!--## External tools (#external-tools)

### Signal Spam {#signal-spam}

Signal Spam is a French service which offers anonymized feedback loop reporting for French ISPs (Orange, SFR).

This service allows you to follow the reputation of the French ISPs and track customers' activity evolution.

Signal Spam also provides direct complaints that end users log through a dedicated interface. Those complaints are then quarantined from the email address database.

### 250ok {#solution-250ok}

250ok is a monitoring solution which provides IP and domain denylists, as well as reputation indicators.

The information provided is real-time, which allows for a pro-active assistance. 250ok a complementary solution to the Adobe deliverability internal tools.-->
