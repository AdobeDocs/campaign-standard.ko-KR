---
title: 배달 실패 이해
seo-title: 배달 실패 이해
description: 배달 실패 이해
seo-description: 캠페인으로 배달 실패를 관리하는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: 2735 AA 05-7 B 6 F -47 C 9-98 C 4-A 15 CC 33 BE 39 D
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 전송
content-type: 참조
topic-tags: monitoring-messages
discoiquuid: 38452841-4 CD 4-4 F 92-A 5 C 3-1 DFDD 54 FF 6 F 4
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: a12df43de55dedf388a397fbf4670d99e3ea7f3d

---


# Understanding delivery failures{#understanding-delivery-failures}

## About delivery failures {#about-delivery-failures}

게재를 프로필로 보낼 수 없는 경우, 원격 서버는 Adobe Campaign 플랫폼에서 선택한 오류 메시지를 자동으로 보내고, 이메일 주소 또는 전화 번호가 격리되어야 하는지 여부를 결정합니다. See [Bounce mail qualification](../../sending/using/understanding-delivery-failures.md#bounce-mail-qualification).

>[!NOTE]
>
>**이메일** 오류 메시지 (또는 "바운스") 는 이메일 프로세스에 의해 자격이 됩니다. **SMS** 오류 메시지 (또는 "상태 보고서" 의 "SR") 는 MTA 프로세스에 의해 자격이 됩니다.

주소가 격리되거나 프로필이 차단된 경우 배달 준비 중에 메시지를 제외할 수도 있습니다. Excluded messages are listed in the **[!UICONTROL Exclusion logs]** tab of the delivery dashboard (see [this section](../../sending/using/monitoring-a-delivery.md#exclusion-logs)).

![](assets/exclusion_logs.png)

**관련 항목:**

* [격리 관리 이해](../../sending/using/understanding-quarantine-management.md)
* [캠페인의 블랙 리스트 관리](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md)

## Identifying delivery failures for a message {#identifying-delivery-failures-for-a-message}

Once a delivery is sent, the **[!UICONTROL Sending logs]** tab (see [this section](../../sending/using/monitoring-a-delivery.md#sending-logs)) allows you to view the delivery status for each profile and the associated failure type and reason (see [Delivery failure types and reasons](../../sending/using/understanding-delivery-failures.md#delivery-failure-types-and-reasons)).

![](assets/sending_logs.png)

전용 보고서도 사용할 수 있습니다. 이 보고서는 배달하는 동안 발생한 전반적인 하드 및 소프트 오류와 바운스 자동 처리를 자세히 설명합니다. For more on this, refer to [this section](../../reporting/using/bounce-summary.md).

## Delivery failure types and reasons {#delivery-failure-types-and-reasons}

게시에 실패하면 다음 세 가지 오류가 있습니다.

* ****&#x200B;하드: " 하드 "오류는 잘못된 주소를 나타냅니다. 여기에는 다음과 같이 주소가 유효하지 않음을 명시적으로 알려주는 오류 메시지가 포함됩니다. " 알 수 없는 사용자 ".
* **Soft**: 일시적인 오류이거나 다음과 같이 분류할 수 없는 일시적인 오류일 수 있습니다. " 잘못된 도메인 "또는" 사서함 꽉 참 ".
* **무시됨: 이것은 "사무실 밖" 와 같이 일시적인 것으로 알려진 오류이거나, 발신자 유형이 "Postmaster" 인 경우 기술적인 오류입니다.**

배달 실패 원인은 다음과 같습니다.

* **[!UICONTROL User unknown]** (하드 유형): 주소가 존재하지 않습니다. 이 프로필에는 추가 배달이 시도되지 않습니다.
* **[!UICONTROL Quarantined address]** (하드 유형): 주소가 격리되었습니다.
* **[!UICONTROL Unreachable]** (soft/hard type): 메시지 배달 체인 (SMTP 릴레이, 일시적으로 접근할 수 없는 도메인 등) 에서 오류가 발생했습니다. 공급자가 반환한 오류에 따라, 주소가 쿼리에 직접 보내지거나, 캠페인이 격리 상태를 정당화하거나 오류 수가 5까지 도달할 때까지 캠페인이 다시 시도될 때까지 배달이 다시 시도됩니다.
* **[!UICONTROL Address empty]** (하드 유형): 주소가 정의되지 않았습니다.
* **[!UICONTROL Mailbox full]** (소프트 유형): 이 사용자의 사서함이 꽉 차서 더 많은 메시지를 수락할 수 없습니다. 이 주소는 격리 목록에서 제거할 수 있습니다. 30 일 후 자동으로 제거됩니다.

   In order for the address to be automatically removed from the list of quarantined addresses, the **[!UICONTROL Database cleanup]** technical workflow must be started.

* **[!UICONTROL Refused]** (soft/hard type): 보안 피드백으로 인해 주소가 스팸 보고서로 격리되었습니다. 공급자가 반환한 오류에 따라, 주소가 쿼리에 직접 보내지거나, 캠페인이 격리 상태를 정당화하거나 오류 수가 5까지 도달할 때까지 캠페인이 다시 시도될 때까지 배달이 다시 시도됩니다.
* **[!UICONTROL Duplicate]**: 세그멘테이션에서 주소가 이미 발견되었습니다.
* **[!UICONTROL Not defined]** (소프트 유형): 오류가 아직 증분되지 않았기 때문에 주소가 유효합니다.

   이 오류는 서버에서 새 오류 메시지를 보낼 때 발생합니다. 분리된 오류일 수 있지만 오류가 다시 발생하면 오류 카운터가 증가하여 기술 팀에게 알립니다.

* **[!UICONTROL Error ignored]**: 주소는 허용 목록에 있으며 어떤 경우에서든 이메일이 전송됩니다.
* **[!UICONTROL Blacklisted address]**: 주소가 전송 시 차단되었습니다.
* **[!UICONTROL Account disabled]** (soft/hard type): 인터넷 액세스 공급자 (IAP) 에서 장기간 사용되지 않은 기간을 감지하면 사용자의 계정을 닫을 수 있습니다. 그러면 사용자 주소로 배달할 수 없게 됩니다. The Soft or Hard type depends upon the type of error received: if the account is temporarily disabled due to six months of inactivity and can still be activated, the status **[!UICONTROL Erroneous]** will be assigned and the delivery will be tried again. 수신된 오류가 있으면 계정이 영구적으로 비활성화되고, 코드가 쿼리로 보내집니다.
* **[!UICONTROL Not connected]**: 메시지가 전송될 때 프로필의 휴대 전화기가 꺼져 있거나 네트워크에 연결되지 않습니다.
* **[!UICONTROL Invalid domain]** (소프트 유형): 이메일 주소의 도메인이 잘못되었거나 더 이상 존재하지 않습니다. 이 프로필은 오류 수가 5까지 도달할 때까지 다시 타깃팅됩니다. 이후에는 레코드가 격리 상태로 설정되며 다시 시도되지 않습니다.
* **[!UICONTROL Text too long]**: SMS 메시지의 문자 수가 제한을 초과합니다. For more on this, see [SMS encoding, length and transliteration](../../administration/using/configuring-sms-channel.md#sms-encoding--length-and-transliteration).
* **[!UICONTROL Character not supported by encoding]**: SMS 메시지에 인코딩이 지원하지 않는 문자가 하나 이상 포함되어 있습니다. &amp;For more on this, see [Table of characters - GSM Standard](../../administration/using/configuring-sms-channel.md#table-of-characters---gsm-standard).

## Retries after a delivery temporary failure {#retries-after-a-delivery-temporary-failure}

**무시된 유형의** 임시 오류로 인해 메시지가 실패할 경우 배달 기간 동안 재시도가 수행됩니다. For more on the types of errors, see [Delivery failure types and reasons](../../sending/using/understanding-delivery-failures.md#delivery-failure-types-and-reasons).

배달 기간을 수정하려면 배달 또는 배달 템플릿의 고급 매개 변수로 이동하여 해당 필드에 원하는 기간을 지정합니다. The advanced delivery properties are presented in [this section](../../administration/using/configuring-email-channel.md#validity-period-parameters).

기본 구성을 사용하면 한 시간 간격으로 5 회 재시도 후 4 일 동안 하루에 한 번 다시 시도할 수 있습니다. The number of retries can be changed globally (contact your Adobe technical administrator) or for each delivery or delivery template (see [this section](../../administration/using/configuring-email-channel.md#sending-parameters)).

## Synchronous and asynchronous errors {#synchronous-and-asynchronous-errors}

배달이 전송된 후 (비동기 오류) 즉시 (동기 오류) 또는 나중에 실패할 수 있습니다.

* **동기 오류**: Adobe Campaign 배달 서버에서 연락한 원격 서버에서 즉시 오류 메시지를 반환하면 프로필 서버로 배달이 허용되지 않습니다.
* **비동기 오류**: 바운스 메일 또는 SR 이 나중에 수신 서버에서 다시 전송되었습니다. 비동기 오류는 배달이 전송된 후 1 주일 후에 발생할 수 있습니다.

## Bounce mail qualification {#bounce-mail-qualification}

배달 실패 오류 메시지 (또는 "바운스") 는 Adobe Campaign 플랫폼에서 채택되며 이메일 관리 규칙 목록을 보강하기 위해 inmail 프로세스에 의해 자격이 됩니다.

이 목록은 관리자에게만 제공되며 Adobe Campaign에서 사용되는 모든 규칙이 포함되어 배달 오류를 정규화할 수 있습니다.

To access it, click the **[!UICONTROL Adobe Campaign]** logo, at the top left, then select **[!UICONTROL Administration > Channels > Email > Email processing rules]**.

For more on this, refer to this [section](../../administration/using/configuring-email-channel.md#email-processing-rules).

바운스는 다음 자격 조건을 가질 수 있습니다.

* **[!UICONTROL To qualify]**: 바운스 메일을 정규화해야 합니다. 플랫폼 게재 기능이 올바르게 작동하도록 하려면 배달 능력 팀이 자격을 갖추어야 합니다. 자격이 없으면 바운스 메일이 이메일 처리 규칙 목록을 보강하는 데 사용되지 않습니다.
* **[!UICONTROL Keep]**: 바운스 메일은 자격이 되었으며, 기존 이메일 **처리 규칙과 비교할 수 있는 배달 가능성** 워크플로우에 사용되며 목록을 보강합니다.
* **[!UICONTROL Ignore]**: 바운스 메일은 유효했지만 **배달 가능성** 워크플로우에 대한 업데이트에는 사용되지 않습니다. 따라서 클라이언트 인스턴스로 전송되지 않습니다.

To list the various bounces and their associated error types et reasons, click the **[!UICONTROL Adobe Campaign]** logo, in the top left, then select **[!UICONTROL Administration > Channels > Quarantines > Message qualification]**.

![](assets/qualification.png)

## Optimizing mail deliverability with double opt-in mechanism {#optimizing-mail-deliverability-with-double-opt-in-mechanism}

이메일을 보낼 때 이중 옵트인 메커니즘은 우수 사례입니다. 플랫폼이 잘못되었거나 잘못된 이메일 주소, 스팸, 스팸 차단 등을 방지합니다.

이 원칙은 방문자의 계약서를 캠페인 데이터베이스에'프로필'으로 저장하기 전에 방문자의 계약서를 확인하기 위해 보내는 것입니다. 방문자가 온라인 랜딩 페이지를 채우고 이메일을 받고 확인 링크를 클릭해야 구독을 마무리할 수 있습니다.

For more on this, refer to [this section](../../channels/using/setting-up-a-double-opt-in-process.md).
