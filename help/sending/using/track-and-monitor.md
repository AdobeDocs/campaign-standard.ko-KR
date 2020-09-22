---
title: 메시지 추적 및 모니터링
seo-title: 메시지 추적 및 모니터링
page-status-flag: never-activated
uuid: a540efc7-105d-4c7f-a2ee-ade4d22b3445
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: delivery
content-type: reference
topic-tags: deliveries-best-practices
discoiquuid: 0cbc4e92-482f-4dac-a1fb-b738e7127938
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 469d2a8b3f8026087929583affd2c294e2a954bb
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 3%

---


# 추적 및 모니터 {#track-and-monitor}

전송 버튼을 클릭했습니까? 어떻게 되는지 봅시다. 배달이 전송되면 Adobe Campaign을 통해 보낸 메시지를 추적하고 수신자가 전달에 어떻게 반응하는지 알 수 있습니다. 이를 통해 향후 전송을 개선하고 다음 캠페인을 최적화할 수 있습니다.

## 게재 모니터링 {#monitoring-deliveries}

캠페인을 제어하려면 메시지를 받는 사람에게 실제로 전달했는지 확인해야 합니다.

**팁**

* 배달 로그에 있는 메시지의 상태를 제어할 수 있습니다.

* 배달 성공이나 실패를 추적하기 위해, Adobe Campaign은 사용자에게 중요한 시스템 활동을 알리는 알림을 보내는 이메일 경고 시스템을 제공합니다.

* 메시지 대시보드에서 이 특정 메시지에 대한 여러 보고서에 액세스할 수 있습니다.

자세한 내용은 배달 [모니터링을 참조하십시오](../../sending/using/monitoring-a-delivery.md).

## 추적 {#tracking-deliveries}

타깃팅된 프로필의 동작을 더 잘 이해하려면 해당 프로필의 전달 방식을 추적할 수 있습니다.수신, 열기, 링크 클릭, 구독 취소 등 게재의 **추적 로그** 탭을 참조하십시오.

**팁**:메시지 추적은 기본적으로 활성화되어 있습니다. URL을 구성하려면 배달 마법사의 아래 섹션에서 URL 표시 옵션을 선택합니다. 메시지의 각 URL에 대해 추적을 활성화할지 여부를 선택할 수 있습니다.

이에 대한 자세한 내용은 [추적 메시지](../../sending/using/tracking-messages.md) 섹션 및 [추적 지표](../../reporting/using/tracking-indicators.md) 설명을 참조하십시오.

## 동적 보고서 {#dyn-reports}

동적 보고서를 사용하면 완전히 사용자 지정 가능하고 실시간 보고서를 만들어 캠페인을 모니터링할 수 있습니다. Dimension, 지표 및 시각화를 사용하면 캠페인이 수신자에게 미치는 영향과 성공을 측정할 수 있습니다.

**팁** - 내장된 보고서를 사용하여 캠페인을 모니터링할 수 있지만, 지표나 차원을 보고서에 드래그하여 놓아 이러한 보고서를 사용자 지정할 수도 있습니다.

For more on this, refer to the [Reporting guide](../../reporting/using/about-dynamic-reports.md).

## 핫 클릭

핫 클릭 수 보고서는 각 링크에 대한 클릭 수의 백분율과 함께 메시지 내용(HTML 및/또는 텍스트)을 표시합니다. 각 동적 컨텐츠에 대한 클릭 수를 백분율로 표시함으로써 받는 사람에게 가장 인기 있는 컨텐츠를 측정할 수 있습니다.

자세한 내용은 [핫 클릭 보고서를 참조하십시오](../../reporting/using/hot-clicks.md).

## 전달 성능 팁 {#performance-tips}

* 임시 테이블을 유지하고 성능에 영향을 주므로 인스턴스에 배달을 실패한 상태로 유지하지 마십시오.

* 더 이상 필요하지 않은 게재와 비활성 수신자를 데이터베이스에서 제거하여 주소 품질을 유지합니다.

* 큰 배달은 함께 예약하지 마십시오. 시스템에 로드를 균일하게 분산하는 데 5~10분이 걸릴 수 있습니다.

**관련 항목:**

* [게재 실패 시 경고 받기](../../sending/using/receiving-alerts-when-failures-happen.md)
* [보고서](../../reporting/using/about-dynamic-reports.md)