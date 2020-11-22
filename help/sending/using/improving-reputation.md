---
solution: Campaign Standard
product: campaign
title: Adobe Campaign Standard을 통한 평판 향상
description: 중복 이메일 주소와 격리를 관리하여 Adobe Campaign Standard을 통해 명성을 높일 수 있는 방법을 살펴볼 수 있습니다.
audience: sending
content-type: reference
topic-tags: sheduling-messages
context-tags: delivery,schedule,back
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 2%

---


# 평판 개선{#improving-reputation}

받는 사람이 피곤하지 않도록 타겟에서 중복된 이메일 주소를 삭제합니다. 이 단계는 전송 명성을 보호하고 안전한 격리 관리를 보장합니다. Adobe Campaign은 이러한 권장 사항을 구현하고 ISP가에 추가하는 위험을 차단 목록 방지하는 데 필요한 도구를 제공합니다.

아래에서 복제 및 격리 관리에 대한 세부 사항을 확인할 수 있습니다.

## 중복 {#duplicates}

이메일 주소가 중복되면 다음과 같은 여러 결과가 발생할 수 있습니다.
* 동일한 메시지를 두 번 이상 보냅니다. Campaign이 기본적으로 전송 전에 데이터 중복 제거 절차를 수행하더라도, 타겟이 분할될 때 동일한 컨텐츠를 갖는 다른 작업에 의해 전송되는 동일한 메시지를 중지하기 위한 방법은 없습니다.
* 구독 취소 요청이 승인되지 않았습니다. 수신자가 메시지를 받은 후 구독을 취소하는 경우 해당 중복된 프로필은 여전히 향후 메시지를 받을 수 있습니다.

이러한 옵트인 절차의 사이드 단계 외에도, 이러한 상황은 사용자들이 메시지를 스팸으로 간주하고 ISP에서 절차를 차단 목록 트리거하도록 만들 것입니다.

데이터베이스에서 작업을 수행할 때는 특히 주의해야 합니다. 중복을 피하려면 다음 작업을 수행해야 합니다.
* **가져오기를 세심하게 구성해야 합니다.** 이것은 조정 키를 선택할 때 특히 중요합니다.
* **이메일 주소를 수정할 때 주의하십시오.** 변경된 이메일 주소는 중복된 소스도 될 수 있습니다. 특히 도메인이 다른 두 개의 주소는 같은 사서함으로 라우팅될 수 있습니다. 예를 들어 이름이 변경되고 특정 기간 동안 이전 도메인을 유지한 회사의 경우:joe.doe@amce-co.com 및 joe.doe@acme-rebranded.com을 참조하십시오.
* **자동 가져오기 작업 중 주의 사항** 목록이든 다른 데이터베이스이든 프로파일을 관리할 때 고려해야 할 요소입니다. 다른 파티션에서 프로파일을 삭제하거나 이동하면 어떻게 됩니까? 예를 들어, 구매 발주를 배치할 때 자동 가져오기로 초기 분할 영역에서 다시 만들 수 있습니다.
* **프로필은 다른 폴더로 정렬되어야 합니다.**

동일한 경우, 서로 다른 파티션 간에 중복되는 경우가 모두 있습니다. 예를 들어 서드파티 또는 다른 회사 법인체용으로 보낼 때 서로 다른 이유로 동일한 사람이 수신자가 되는 것이 논리적입니다. 그러나 동일한 파티션 내에서 중복 항목을 찾는 것은 거의 정상적이지 않습니다.

## 검역소 {#quarantines}

Adobe Campaign은 격리된 주소 목록을 관리합니다. 주소가 격리된 수신자는 배달 분석 중에 기본적으로 제외됩니다.타깃팅되지 않습니다.

검역 관리는 [이 섹션에 자세히 설명되어 있습니다](../../sending/using/understanding-quarantine-management.md).

받은 편지함이 가득 찼거나 주소가 없는 경우 이메일 주소를 격리할 수 있습니다. 모든 경우에서 검역은 [이 섹션에 제시된 특정 규칙에 해당합니다](../../sending/using/understanding-quarantine-management.md#conditions-for-sending-an-address-to-quarantine).
