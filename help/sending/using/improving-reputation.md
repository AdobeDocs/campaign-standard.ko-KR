---
title: Adobe Campaign Standard를 사용하여 평판 향상
description: Adobe Campaign Standard를 사용하여 중복 이메일 주소와 격리를 관리하여 명성을 높이는 방법을 살펴볼 수 있습니다.
page-status-flag: never-activated
uuid: 286fceee-65a9-4cb9-b205-9ce5d024675c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sheduling-messages
discoiquuid: 9c7fd670-bba9-4f3c-8cb1-87397a1acd27
context-tags: delivery,schedule,back
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 44049443f8028ed26089ee0d49944ebac6a62111

---


# 평판 향상{#improving-reputation}

수신자가 번거롭게 되지 않도록 타겟에서 중복된 이메일 주소를 삭제합니다. 이 단계에서는 전송 명성을 보호하고 철저한 격리 관리를 보장합니다. Adobe Campaign은 이러한 권장 사항을 구현하고 ISP에 의해 블랙리스트에 오르는 위험을 방지하기 위해 필요한 도구를 제공합니다.

다음은 복제 및 격리 관리에 대한 세부 사항을 확인할 수 있습니다.

## 중복 {#duplicates}

중복된 이메일 주소를 사용하면 다음과 같은 여러 가지 결과가 발생할 수 있습니다.
* 동일한 메시지를 두 번 이상 보냅니다. Campaign이 기본적으로 전송 전에 데이터 중복 제거 절차를 수행하더라도 대상이 분할될 때 동일한 컨텐츠를 갖는 다른 동작으로 인해 전송되는 동일한 메시지를 중지할 수 없습니다.
* 구독 취소 요청이 처리되지 않았습니다. 수신자가 메시지를 받은 후 구독을 취소하는 경우 해당 중복 프로필은 여전히 향후 메시지 이용 가능 상태가 됩니다.

이러한 옵트인 절차의 사이드 단계 외에도, 이러한 상황은 사용자가 메시지를 스팸으로 간주하도록 하고 ISP에서 블랙리스트 절차를 트리거하도록 만들 수 있습니다.

데이터베이스에서 작업을 수행할 때는 특히 주의해야 합니다. 중복을 방지하려면 다음 작업을 수행해야 합니다.
* **가져오기는 꼼꼼하게 구성해야 합니다.** 이것은 조정 키를 선택할 때 특히 중요합니다.
* **이메일 주소를 수정할 때 주의하십시오.** 변경된 이메일 주소는 중복의 소스도 될 수 있습니다. 특히, 이름이 변경되고 특정 기간 동안 이전 도메인을 유지한 회사의 경우, 도메인이 다른 두 주소가 동일한 사서함으로 라우팅될 수 있습니다 joe.doe@amce-co.com 및 joe.doe@acme-rebranded.com.
* **자동 가져오기 작업 시 주의하십시오.** 목록 또는 다른 데이터베이스에서 프로파일을 관리할 때 고려해야 할 요소입니다. 다른 파티션에서 프로필을 삭제하거나 이동하면 어떻게 됩니까? 예를 들어, 구매 발주를 배치할 때 자동 가져오기로 초기 분할 영역에서 다시 만들 수 있습니다.
* **프로필은 다른 폴더로 정렬해야 합니다.**

동일한 경우 서로 다른 파티션 간에 중복되는 경우가 모두 있습니다. 예를 들어 서드 파티 또는 다른 회사 엔티티용으로 전송할 때 서로 다른 이유로 동일한 사람이 수신자가 되는 것이 논리적입니다. 그러나 동일한 파티션 내에서 복제본을 찾는 것은 거의 일반적이지 않습니다.

## 검역소 {#quarantines}

Adobe Campaign에서 격리된 주소 목록을 관리합니다. 주소가 격리된 수신자는 게재 분석 중에 기본적으로 제외됩니다.타깃팅되지 않습니다.

격리 관리는 [이 섹션에](../../sending/using/understanding-quarantine-management.md)자세히 설명되어 있습니다.

이메일 주소는 받은 편지함이 가득 찼거나 주소가 존재하지 않는 경우와 같이 격리될 수 있습니다. 모든 경우에, 격리는 [이 섹션에](../../sending/using/understanding-quarantine-management.md#conditions-for-sending-an-address-to-quarantine)제시된 특정 규칙에 해당합니다.
