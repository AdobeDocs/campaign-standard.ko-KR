---
title: 게재 실패 이해
description: Campaign을 사용하여 배달 실패를 관리하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: 2735aa05-7b6f-47c9-98c4-a15cc33be39d
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: monitoring-messages
discoiquuid: 38452841-4cd4-4f92-a5c3-1dfdd54ff6f4
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: d05d2692607117e056c360e81d85b7d64c4077a3
workflow-type: tm+mt
source-wordcount: '1279'
ht-degree: 0%

---


# 게재 실패 이해{#understanding-delivery-failures}

## 배달 실패 정보 {#about-delivery-failures}

프로필에 배달을 보낼 수 없는 경우 원격 서버는 오류 메시지를 자동으로 전송합니다. 오류 메시지는 Adobe Campaign 플랫폼에서 선택되었으며 이메일 주소 또는 전화 번호를 격리해야 하는지 여부를 결정할 수 있습니다. 바운스 [메일 자격 조건을 참조하십시오](#bounce-mail-qualification).

>[!NOTE]
>
>**이메일** 오류 메시지(또는 &quot;바운스 수&quot;)는 향상된 MTA(동기 바운스) 또는 inMail 프로세스(비동기 바운스)에 의해 자격을 얻게 됩니다.
>
>**SMS** 오류 메시지(또는 &quot;상태 보고서&quot;의 경우 &quot;SR&quot;)는 MTA 프로세스에서 인증합니다.

주소가 격리되거나 프로필이 차단되는 경우에도 배달 준비 중에 메시지를 제외할 수 있습니다. 제외된 메시지는 배달 대시보드의 **[!UICONTROL Exclusion logs]** 탭에 나열됩니다( [이 섹션 참조](../../sending/using/monitoring-a-delivery.md#exclusion-logs)).

![](assets/exclusion_logs.png)

**관련 항목:**

* [스팸 차단 관리 이해](../../sending/using/understanding-quarantine-management.md)
* [캠페인에서 블랙 목록 관리](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md)

## 메시지에 대한 배달 실패 식별 {#identifying-delivery-failures-for-a-message}

배달을 전송하면 **[!UICONTROL Sending logs]** 탭( [이 섹션](../../sending/using/monitoring-a-delivery.md#sending-logs)참조)을 통해 각 프로필에 대한 배달 상태, 연관된 실패 유형 및 이유를 확인할 수 있습니다( [배달 실패 유형 및 이유](#delivery-failure-types-and-reasons)참조).

![](assets/sending_logs.png)

전용 특별 특별 보고서 또한 사용할 수 있습니다. 이 보고서는 바운스 자동 처리뿐만 아니라 배달 중에 발생한 전체 하드 및 소프트 오류에 대해 자세히 설명합니다. For more on this, refer to [this section](../../reporting/using/bounce-summary.md).

## 배달 실패 유형 및 이유 {#delivery-failure-types-and-reasons}

배달이 실패할 경우 세 가지 유형의 오류가 있습니다.

* **하드**: &quot;하드&quot; 오류는 잘못된 주소를 나타냅니다. 여기에는 다음과 같이 주소가 잘못되었음을 명시적으로 표시하는 오류 메시지가 포함됩니다. &quot;알 수 없는 사용자&quot;입니다.
* **소프트**: 이는 일시적인 오류이거나 다음과 같이 분류할 수 없는 오류일 수 있습니다. &quot;잘못된 도메인&quot; 또는 &quot;사서함 꽉 참&quot;입니다.
* **무시됨**: 이는 &quot;부재 중&quot;과 같이 일시적인 것으로 알려진 오류이거나, 예를 들어 발신자 유형이 &quot;postmaster&quot;인 경우 기술 오류입니다.

배달 실패의 가능한 원인은 다음과 같습니다.

| 오류 레이블 | 오류 유형 | 설명 |
---------|----------|---------
| **[!UICONTROL User unknown]** | 하드 | 주소가 없습니다. 이 프로필에 대해 더 이상 배달하지 않습니다. |
| **[!UICONTROL Quarantined address]** | 하드 | 그 주소는 검역에 붙여졌다. |
| **[!UICONTROL Unreachable]** | 부드러운/하드 | 메시지 배달 체인에 오류가 발생했습니다(예: 일시적으로 액세스할 수 없는 도메인). 제공자가 반환하는 오류에 따라 주소가 직접 격리되도록 전송되거나 Campaign이 격리 상태를 정당화하는 오류를 수신하거나 오류 수가 5개가 될 때까지 배달을 다시 시도합니다. |
| **[!UICONTROL Address empty]** | 하드 | 주소가 정의되지 않았습니다. |
| **[!UICONTROL Mailbox full]** | 부드러운 | 이 사용자의 사서함이 가득 차서 더 많은 메시지를 수락할 수 없습니다. 이 주소를 격리 목록에서 제거하여 다시 시도할 수 있습니다. 30일 후 자동으로 제거됩니다. In order for the address to be automatically removed from the list of quarantined addresses, the **[!UICONTROL Database cleanup]** technical workflow must be started. |
| **[!UICONTROL Refused]** | 부드러운/하드 | 스팸 보고서로 보안 피드백이 발생하여 주소가 격리되었습니다. 제공자가 반환하는 오류에 따라 주소가 직접 격리되도록 전송되거나 Campaign이 격리 상태를 정당화하는 오류를 수신하거나 오류 수가 5개가 될 때까지 배달을 다시 시도합니다. |
| **[!UICONTROL Duplicate]** | 무시됨 | 세그먼테이션에서 주소가 이미 검색되었습니다. |
| **[!UICONTROL Not defined]** | 부드러운 | 오류가 아직 증가하지 않았기 때문에 주소가 적격 상태입니다. 이 유형의 오류는 서버에서 새 오류 메시지를 보낼 때 발생합니다. 격리된 오류일 수 있지만 다시 발생하면 오류 카운터가 증가하므로 기술 팀에 경고가 표시됩니다. |
| **[!UICONTROL Error ignored]** | 무시됨 | 주소는 허용 목록에 있으며 어떤 경우에서든 전자 메일이 발송됩니다. |
| **[!UICONTROL Blacklisted address]** | 하드 | 발송 시간에 주소가 차단되었다. |
| **[!UICONTROL Account disabled]** | 부드러운/하드 | IAP(Internet Access Provider)가 장기간 동안 사용되지 않는 경우 사용자의 계정을 닫을 수 있습니다. 그러면 사용자 주소로 배달할 수 없습니다. 소프트 또는 하드 유형은 받은 오류 유형에 따라 달라집니다. 6개월 동안 활동이 없어 계정이 일시적으로 비활성화되어 계속 활성화될 수 있는 경우 상태가 할당되고 배달을 다시 시도합니다. **[!UICONTROL Erroneous]** 오류가 수신되면 계정이 영구적으로 비활성화됨을 나타내는 메시지가 표시되면 즉시 격리로 전송됩니다. |
| **[!UICONTROL Not connected]** | 무시됨 | 메시지가 전송되면 프로필의 휴대폰이 꺼지거나 네트워크에 연결되지 않습니다. |
| **[!UICONTROL Invalid domain]** | 부드러운 | 이메일 주소의 도메인이 잘못되었거나 더 이상 존재하지 않습니다. 이 프로필은 오류 카운트가 5에 도달할 때까지 다시 타깃팅됩니다. 이후 레코드가 격리 상태로 설정되며 다시 시도되지 않습니다. |
| **[!UICONTROL Text too long]** | 무시됨 | SMS 메시지의 문자 수가 한도를 초과합니다. 자세한 내용은 [SMS 인코딩, 길이 및 음역법을 참조하십시오](../../administration/using/configuring-sms-channel.md#sms-encoding--length-and-transliteration). |
| **[!UICONTROL Character not supported by encoding]** | 무시됨 | SMS 메시지에 인코딩에서 지원되지 않는 문자가 하나 이상 포함되어 있습니다. 자세한 내용은 문자 [표 - GSM 표준을 참조하십시오](../../administration/using/configuring-sms-channel.md#table-of-characters---gsm-standard). |

## 배달 임시 실패 후 다시 시도 {#retries-after-a-delivery-temporary-failure}

무시됨 유형의 일시적인 오류로 인해 메시지 **에** 실패하면 배달 기간 동안 재시도가 수행됩니다. 오류 유형에 대한 자세한 내용은 배달 [실패 유형 및 이유를 참조하십시오](#delivery-failure-types-and-reasons).

IP가 이전 및 현재 주어진 도메인에서 얼마나 성과를 거두고 있는지 여부를 기준으로, 재시도 횟수(전송을 시작한 다음 날에 얼마나 많은 재시도를 수행해야 하는지)와 재시도 사이의 최소 지연은 Adobe Campaign 향상된 MTA에 의해 관리됩니다. 캠페인의 **재시도** 설정은 무시됩니다.

배달 기간을 수정하려면 전달 또는 전달 템플릿의 고급 매개 변수로 이동하고 **[!UICONTROL Delivery duration]** 유효성 기간 [섹션](../../administration/using/configuring-email-channel.md#validity-period-parameters) 필드를 편집합니다.

>[!IMPORTANT]
>
>**이제 캠페인 게재의&#x200B;**[!UICONTROL Delivery duration]**매개 변수는 3.5일 이내로 설정된 경우에만 사용됩니다.** 3.5일이 넘는 값을 정의하는 경우 Adobe Campaign 향상된 MTA에서 관리되므로 이 값을 고려하지 않습니다.

예를 들어 배달을 위한 재시도가 1일 후 중지되도록 하려면 배달 기간을 **1d**&#x200B;로 설정하고, 향상된 MTA는 1일 후 재시도 대기열에서 메시지를 제거하여 해당 설정을 확인합니다.

>[!NOTE]
>
>메시지가 3.5일 동안 향상된 MTA 대기열에 있고 전달하지 못하면 시간이 초과되고 해당 상태가 **[!UICONTROL Sent]** 배달 로그인 **[!UICONTROL Failed]** [](../../sending/using/monitoring-a-delivery.md#delivery-logs)에서 업데이트됨

<!--The default configuration allows five retries at one-hour intervals, followed by one retry per day for four days. The number of retries can be changed globally (contact your Adobe technical administrator) or for each delivery or delivery template (see [this section](../../administration/using/configuring-email-channel.md#sending-parameters)).-->

## 동기 및 비동기 오류 {#synchronous-and-asynchronous-errors}

배달이 전송되면 즉시(동기 오류) 또는 나중에 전달되지 않을 수 있습니다(비동기 오류).

* **동기 오류**: Adobe Campaign 게재 서버가 연결한 원격 서버에서 오류 메시지를 바로 반환했습니다. 게재를 프로필의 서버로 보낼 수 없습니다.
* **비동기 오류**: 바운스 메일 또는 SR이 받는 서버에서 나중에 다시 전송되었습니다. 배달을 보낸 후 1주일까지 비동기 오류가 발생할 수 있습니다.

## 바운스 메일 자격 조건 {#bounce-mail-qualification}

동기 배달 실패 오류 메시지의 경우 향상된 MTA가 바운스 유형과 자격 조건을 결정하고 해당 정보를 Campaign으로 다시 전송합니다.

비동기 바운스는 여전히 규칙을 통해 inMail 프로세스에서 자격을 **[!UICONTROL Inbound email]** 갖습니다. 이러한 규칙에 액세스하려면 **[!UICONTROL Adobe Campaign]** 로고를 클릭하고 왼쪽 상단에서 선택한 다음 **[!UICONTROL Administration > Channels > Email > Email processing rules]** 을 선택합니다 **[!UICONTROL Bounce mails]**. 이 규칙에 대한 자세한 내용은 이 [섹션을 참조하십시오](../../administration/using/configuring-email-channel.md#email-processing-rules).

>[!NOTE]
>
>이제 Adobe Campaign 향상된 MTA에서 바운스 메일 자격을 관리합니다. 캠페인 테이블의 바운스 자격 **[!UICONTROL Message qualification]** 은 더 이상 사용되지 않습니다.

<!--Bounces can have the following qualification statuses:

* **[!UICONTROL To qualify]**: the bounce mail needs to be qualified. Qualification must be done by the Deliverability team to ensure that the platform deliverability functions correctly. As long as it is not qualified, the bounce mail is not used to enrich the list of email processing rules.
* **[!UICONTROL Keep]**: the bounce mail was qualified and will be used by the **Update for deliverability** workflow to be compared to existing email processing rules and enrich the list.
* **[!UICONTROL Ignore]**: the bounce mail was qualified but will not be used by the **Update for deliverability** workflow. So it will not be sent to the client instances.

To list the various bounces and their associated error types et reasons, click the **[!UICONTROL Adobe Campaign]** logo, in the top left, then select **[!UICONTROL Administration > Channels > Quarantines > Message qualification]**.

![](assets/qualification.png)-->

## 이중 옵트인 메커니즘을 통해 메일 전달 능력 최적화 {#optimizing-mail-deliverability-with-double-opt-in-mechanism}

이중 옵트인 메커니즘은 이메일을 보낼 때 가장 좋은 방법입니다. 플랫폼을 잘못된 이메일 주소, 스팸 메일, 스팸 메일로부터 보호하고 스팸 불만 사항을 방지합니다.

방문자의 계약을 &#39;프로필&#39;으로 저장하기 전에 이메일 전송을 통해 방문자의 계약을 확인하는 것이 좋습니다. 방문자는 온라인 랜딩 페이지를 채우고, 이메일을 수신하고 확인 링크를 클릭하여 구독을 마무리해야 합니다.

For more on this, refer to [this section](../../channels/using/setting-up-a-double-opt-in-process.md).
