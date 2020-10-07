---
title: Adobe Campaign Standard의 모니터링 제공
description: Adobe Campaign Standard에서 제공하는 툴을 사용하여 플랫폼 제공 여부를 모니터링할 수 있습니다.
page-status-flag: never-activated
uuid: 286fceee-65a9-4cb9-b205-9ce5d024675c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sheduling-messages
discoiquuid: 9c7fd670-bba9-4f3c-8cb1-87397a1acd27
context-tags: delivery,schedule,back
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 7%

---


# 게재 기능 모니터링{#monitor-deliverability}

아래에서는 Adobe Campaign에서 제공하는 다양한 모니터링 도구 및 **[!UICONTROL Delivery throughput]** 보고서에 대한 세부 사항을 확인할 수 있습니다. 다음은 제공 능력 모니터링에 대한 몇 가지 추가 지침입니다.
* 전체 플랫폼에 대한 배달 처리량을 정기적으로 확인하여 원래 설정과 일치하는지 확인합니다.
* 배달 템플릿에서 재시도 횟수가 올바르게 설정되어 있는지(재시도 기간은 30분, 재시도 횟수는 20회 이상) 확인합니다.
* 바운스 사서함에 액세스할 수 있으며 계정이 만료되지 않도록 정기적으로 확인합니다.
* 각 배달 처리량을 확인하여 배달 컨텐츠의 유효성(예:&#39;flash sales&#39;는 며칠이 아니라 몇 분 만에 배달됩니다.)
* 파도를 사용할 때 다음 파동이 트리거되기 전에 각 파동이 끝날 시간이 충분한지 확인합니다.
* 오류 수와 새 검역서가 다른 배달물과 일치하는지 확인하십시오.
* 강조 표시된 오류 유형(차단 목록, DNS 문제, 스팸 방지 규칙 등)을 확인하려면 배달 로그에 자세히 문의하십시오.

## 게재 처리량 {#delivery-throughput}

이 보고서에는 지정된 기간 동안 전체 플랫폼의 배달 처리량에 대한 정보가 포함되어 있어 메시지가 전달되는 속도를 측정합니다.

For more on this, see [Delivery throughput](../../reporting/using/delivery-throughput.md).

![](assets/delivery_reports_1.png)

시간 간격을 변경하여 표시되는 값을 구성할 수 있습니다.

기타 보고서(예: **[!UICONTROL Delivery summary]** 또는 **[!UICONTROL Non-deliverables and bounces]**)를 사용할 수 있습니다. 자세한 내용은 [동적 보고서를 참조하십시오](../../reporting/using/about-dynamic-reports.md).

## 게재 모니터링 {#monitoring-deliveries}

메시지 대시보드를 통해 배달 로그에 액세스할 수 있습니다. **[!UICONTROL Sending logs]**, **[!UICONTROL Exclusion logs]**, **[!UICONTROL Exclusion causes]**, **[!UICONTROL Tracking logs]** and **[!UICONTROL Tracked URLs]**&#x200B;를 참조하십시오. 여기에는 전송 세부 사항과 제외된 타겟 및 그 이유와 함께 오픈과 클릭 등의 추적 정보가 표시됩니다.

자세한 내용은 배달 [모니터링을 참조하십시오](../../sending/using/monitoring-a-delivery.md).

![](assets/sending_delivery1.png)

## 알림 받기 {#receiving-alerts}

The **[!UICONTROL Delivery alerting]** feature is an alert management system that enables a group of users to automatically receive notifications containing information on the execution of their deliveries.

자세한 내용은 오류가 발생할 [때 경고 받기를 참조하십시오](../../sending/using/receiving-alerts-when-failures-happen.md).

## 신호 스팸 {#signal-spam}

Signal Spam은 프랑스 ISP(Orange, SFR)에 대해 익명화된 피드백 루프 보고를 제공하는 프랑스 서비스입니다.

이 서비스를 사용하면 프랑스 ISP의 명성을 확인하고 고객의 활동 진화를 추적할 수 있습니다.

Signal Spam은 최종 사용자가 전용 인터페이스를 통해 로그인하는 직접 불만 사항을 제공합니다. 그런 불만은 이메일 주소 데이터베이스로부터 격리된다.

## 250ok {#solution-250ok}

250ok는 IP 및 도메인 차단 목록과 평판 지표를 제공하는 모니터링 솔루션입니다.

제공된 정보는 실시간으로 제공되므로 적극적인 지원을 받을 수 있습니다. 250ok Adobe 제공 내부 툴에 대한 보완 솔루션
