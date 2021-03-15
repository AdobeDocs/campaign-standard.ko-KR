---
solution: Campaign Standard
product: campaign
title: Adobe Campaign Standard을 통한 평판 향상
description: 중복 이메일 주소 및 검역물을 관리하여 Adobe Campaign Standard을 통해 명성을 높이는 방법을 살펴볼 수 있습니다.
audience: sending
content-type: reference
topic-tags: sheduling-messages
context-tags: delivery,schedule,back
feature: 게재 가능성
role: 비즈니스 전문가
level: 중간
translation-type: tm+mt
source-git-commit: 088b49931ee5047fa6b949813ba17654b1e10d60
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 2%

---


# 평판 개선{#improving-reputation}

받는 사람이 너무 많은 작업을 하지 않도록 타겟에서 중복된 이메일 주소를 삭제합니다. 이 단계는 전송 명성을 보호하고 안전한 격리 관리를 보장합니다. Adobe Campaign은 이러한 권장 사항을 구현하고 ISP에 의해에 추가되는 위험을 차단 목록 방지하는 데 필요한 도구를 제공합니다.

복제 및 격리 관리에 대한 자세한 내용은 아래에서 확인할 수 있습니다.

## {#duplicates} 복제

이메일 주소가 중복되면 다음과 같은 여러 결과가 발생할 수 있습니다.
* 두 번 이상 전송되는 동일한 메시지입니다. Campaign이 보내기 전에 기본적으로 데이터 중복 제거 절차를 수행하더라도, 대상이 분할될 때 동일한 컨텐츠를 갖는 다른 동작으로 인해 전송되는 동일한 메시지를 중단할 필요가 없습니다.
* 구독 취소 요청이 승인되지 않았습니다. 수신자가 메시지를 받은 후 구독을 취소하는 경우 해당 중복 프로필은 계속 향후 메시지에 사용할 수 있습니다.

이러한 사전 동의 절차를 단계별로 밟는 것 외에, 이러한 상황으로 인해 사용자는 메시지를 스팸으로 간주하여 ISP에서 차단 목록 절차를 시작할 수 있습니다.

데이터베이스에서 작업을 수행할 때는 특히 주의해야 합니다. 중복을 피하려면 다음 작업을 수행해야 합니다.
* **가져오기 작업은 꼼꼼하게 구성해야 합니다.** 이것은 조정 키를 선택할 때 특히 중요합니다.
* **이메일 주소를 수정할 때 주의하십시오.** 변경된 이메일 주소는 중복 소스일 수도 있습니다. 특히, 이름이 변경되고 특정 기간 동안 이전 도메인을 유지한 회사의 경우, 도메인이 다른 두 주소가 동일한 사서함으로 라우팅될 수 있습니다.joe.doe@amce-co.com 및 joe.doe@acme-rebranded.com을 참조하십시오.
* **자동 가져오기 작업 중 주의 사항** 목록이든 다른 데이터베이스의 목록이든 프로파일을 관리할 때 고려해야 할 요소입니다. 다른 파티션에서 프로파일을 삭제하거나 이동하면 어떻게 됩니까? 예를 들어, 구매 발주를 배치할 때 자동 가져오기를 통해 초기 파티션에서 다시 만들 수 있습니다.
* **프로필을 다른 폴더로 정렬해야 합니다.**

다른 파티션 간에 중복되는 경우도 모두 동일하며, 예를 들어 제3자 또는 다른 회사 엔티티용으로 보낼 때 서로 다른 이유로 동일한 사람이 수신자가 되는 것이 논리적입니다. 그러나 동일한 파티션 내에서 복제본을 찾는 것은 거의 정상적이지 않습니다.

## 검역소 {#quarantines}

Adobe Campaign은 격리된 주소 목록을 관리합니다. 주소가 격리된 받는 사람은 배달 분석 중에 기본적으로 제외됩니다.타깃팅되지 않습니다.

격리 관리는 [이 섹션](../../sending/using/understanding-quarantine-management.md)에 자세히 설명되어 있습니다.

받은 편지함이 가득 찼거나 주소가 없는 경우 이메일 주소를 격리할 수 있습니다. 모든 경우, 격리는 [이 섹션](../../sending/using/understanding-quarantine-management.md#conditions-for-sending-an-address-to-quarantine)에 제시된 특정 규칙에 해당합니다.
