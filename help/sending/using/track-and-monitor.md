---
solution: Campaign Standard
product: campaign
title: 메시지 추적 및 모니터링
audience: delivery
content-type: reference
topic-tags: deliveries-best-practices
index: y
description: Adobe Campaign을 통해 전송된 메시지를 추적하고 수신자가 게재에 어떻게 반응하는지를 확인하는 방법을 알아봅니다
feature: 전달성
role: User
level: Intermediate
exl-id: dd3bd672-fb9d-4e82-bdf3-d319f372baaa
source-git-commit: aeeb6b4984b3bdd974960e8c6403876fdfedd886
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 4%

---

# 추적 및 모니터링 {#track-and-monitor}

전송 단추를 클릭했습니까? 어떻게 되는지 봅시다. 게재를 전송하면 Adobe Campaign을 통해 전송된 메시지를 추적하고 수신자가 게재에 어떻게 반응하는지를 알 수 있습니다. 이를 통해 향후 전송을 개선하고 다음 캠페인을 최적화할 수 있습니다.

## 게재 모니터링 {#monitoring-deliveries}

캠페인을 제어하려면 메시지가 수신자에게 실제로 전달되었는지 확인해야 합니다.

**팁**

* 게재 로그에서 메시지 상태를 제어할 수 있습니다.

* Adobe Campaign은 게재 성공 또는 실패를 추적하기 위해 사용자에게 중요한 시스템 활동에 대한 알림을 전송하는 이메일 경고 시스템을 제공합니다.

* 메시지 대시보드에서 특정 메시지에 대한 여러 보고서에 액세스할 수 있습니다.

자세한 내용은 [게재 모니터링](../../sending/using/monitoring-a-delivery.md)을 참조하십시오.

## 추적 {#tracking-deliveries}

타겟팅된 프로필의 행동을 더 잘 알기 위해 게재에 어떻게 반응하는지를 추적할 수 있습니다. 수신, 열기, 링크 클릭 수, 구독 취소 등 게재의 **추적 로그** 탭을 참조하십시오.

**팁**: 메시지 추적은 기본적으로 활성화되어 있습니다. URL을 구성하려면 게재 마법사의 아래 섹션에서 URL 표시 옵션을 선택합니다. 메시지의 각 URL에 대해 추적을 활성화할지 여부를 선택할 수 있습니다.

자세한 내용은 [메시지 추적](../../sending/using/tracking-messages.md) 섹션 및 [추적 표시기](../../reporting/using/tracking-indicators.md) 설명을 참조하십시오.

## 동적 보고서 {#dyn-reports}

동적 보고서를 사용하면 캠페인을 모니터링하기 위해 완전히 사용자 지정 가능하고 실시간 보고서를 만들 수 있습니다. Dimension, 지표 및 시각화를 사용하여 수신자에게 캠페인의 영향과 성공을 측정할 수 있습니다.

**팁**  - 기본 제공 보고서는 캠페인을 모니터링할 수 있지만 지표나 차원을 보고서에 끌어다 놓아 사용자 지정할 수도 있습니다.

자세한 내용은 [보고 안내서](../../reporting/using/about-dynamic-reports.md)를 참조하십시오.

## 핫 클릭

핫 클릭 보고서는 각 링크에 대한 클릭 비율(%)과 함께 메시지 콘텐츠(HTML 및/또는 텍스트)를 표시합니다. 각 다이내믹 컨텐츠에 대한 클릭 비율을 표시하여 수신자에게 가장 많이 어필하는 콘텐츠를 측정할 수 있습니다.

자세한 내용은 [핫 클릭 보고서](../../reporting/using/hot-clicks.md)를 참조하십시오.

## 게재 성능 팁 {#performance-tips}

* 임시 테이블을 유지 관리하고 성능에 영향을 주므로 인스턴스에서 게재를 실패 상태로 유지하지 마십시오.

* 주소 품질을 유지하기 위해 더 이상 필요하지 않은 게재 및 비활성 수신자를 데이터베이스에서 제거합니다.

* 대규모 게재를 함께 예약하지 마십시오. 부하를 시스템에 균일하게 분산하는 데 5~10분이 걸릴 수 있습니다.

**관련 항목:**

* [게재 실패 시 경고 받기](../../sending/using/receiving-alerts-when-failures-happen.md)
* [보고서](../../reporting/using/about-dynamic-reports.md)
