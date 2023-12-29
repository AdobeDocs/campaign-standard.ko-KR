---
title: 게재 실패 이해
description: Campaign을 사용하여 게재 실패를 관리하는 방법을 알아봅니다.
audience: sending
content-type: reference
topic-tags: monitoring-messages
feature: Deliverability
role: User
level: Intermediate
exl-id: 92a83400-447a-4d23-b05c-0ea013042ffa
source-git-commit: ee7539914aba9df9e7d46144e437c477a7e52168
workflow-type: tm+mt
source-wordcount: '1281'
ht-degree: 63%

---

# 게재 실패 이해{#understanding-delivery-failures}

## 게재 실패 기본 정보 {#about-delivery-failures}

프로필에 게재를 보낼 수 없는 경우 원격 서버는 오류 메시지를 자동으로 전송합니다. 오류 메시지는 Adobe Campaign 플랫폼에서 선택하며 이메일 주소 또는 전화 번호 격리 여부를 결정할 수 있습니다. [반송 메일 조건](#bounce-mail-qualification)을 참조하십시오.

>[!NOTE]
>
>**이메일** 오류 메시지(또는 &quot;반송&quot;)는 Enhanced MTA(동기 반송) 또는 inMail 프로세스(비동기 반송)에 의해 검증됩니다.
>
>**SMS** 오류 메시지(또는 &quot;상태 보고서&quot;의 경우 &quot;SR&quot;)는 MTA 프로세스에 의해 검증됩니다.

프로필이 격리되어 있거나 프로필이 차단 목록에 추가하다에 있는 경우 게재 준비 중에 메시지가 제외될 수도 있습니다. 제외된 메시지는 게재 대시보드의 **[!UICONTROL Exclusion logs]** 탭에 나열됩니다([이 섹션](../../sending/using/monitoring-a-delivery.md#exclusion-logs) 참조).

![](assets/exclusion_logs.png)

**관련 항목:**

* [격리 관리 이해](../../sending/using/understanding-quarantine-management.md)
* [Campaign의 옵트인 및 옵트아웃 기본 정보](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md)
* [바운스](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/bounces.html#metrics-for-deliverability)

## 메시지에 대한 게재 실패 식별 {#identifying-delivery-failures-for-a-message}

게재를 전송하면 **[!UICONTROL Sending logs]** 탭([이 섹션](../../sending/using/monitoring-a-delivery.md#sending-logs) 참조)을 통해 각 프로필에 대한 게재 상태, 관련 실패 유형 및 이유를 확인할 수 있습니다( [게재 실패 유형 및 이유](#delivery-failure-types-and-reasons) 참조).

![](assets/sending_logs.png)

전용 기본 제공 보고서 또한 사용할 수 있습니다. 이 보고서에는 반송 자동 처리뿐만 아니라 게재 중에 발생한 전체 하드 및 소프트 오류에 대해 자세히 설명되어 있습니다. 자세한 정보는 [이 섹션](../../reporting/using/bounce-summary.md)을 참조하십시오.

## 게재 실패 유형 및 이유 {#delivery-failure-types-and-reasons}

게재가 실패할 경우 세 가지 유형의 오류가 있습니다.

* **하드**: &quot;하드&quot; 오류는 잘못된 주소를 나타냅니다. 여기에는 &quot;알 수 없는 사용자&quot;와 같이 주소가 유효하지 않다는 오류 메시지가 명시적으로 표시됩니다.
* **소프트**: 일시적인 오류이거나 &quot;잘못된 도메인&quot; 또는 &quot;사서함 가득 참&quot;과 같이 분류할 수 없는 오류일 수 있습니다.
* **무시됨**: &quot;부재 중&quot;과 같이 일시적인 것으로 알려진 오류이거나 예를 들어 발신자 유형이 &quot;postmaster&quot;인 경우와 같이 기술적인 오류입니다.

게재 실패 이유는 다음과 같습니다.

| 오류 레이블 | 오류 유형 | 설명 |
| ---------|----------|---------|
| **[!UICONTROL User unknown]** | 하드 | 주소가 존재하지 않습니다. 이 프로필에 대해 더 이상 게재를 시도하지 않습니다. |
| **[!UICONTROL Quarantined address]** | 하드 | 주소가 격리되었습니다. |
| **[!UICONTROL Unreachable]** | 소프트/하드 | 메시지 게재 체인에서 오류가 발생했습니다(예: 일시적으로 연결할 수 없는 도메인). 제공자가 반환하는 오류에 따라 Campaign이 격리 상태를 정당화하는 오류를 수신할 때까지 또는 오류 수가 5개에 도달할 때까지 주소가 직접 격리로 전송되거나 게재를 다시 시도합니다. |
| **[!UICONTROL Address empty]** | 하드 | 주소가 정의되지 않았습니다. |
| **[!UICONTROL Mailbox full]** | 소프트 | 이 사용자의 사서함이 가득 차서 더 이상의 메시지를 받을 수 없습니다. 이 주소를 격리 목록에서 제거하여 다시 시도할 수 있습니다. 30일 후 자동으로 제거됩니다. 격리된 주소 목록에서 주소를 자동으로 제거하려면, **[!UICONTROL Database cleanup]** 기술 워크플로우를 시작해야 합니다. |
| **[!UICONTROL Refused]** | 소프트/하드 | 스팸 보고서로 보안 피드백이 발생하여 주소가 격리되었습니다. 제공자가 반환하는 오류에 따라 Campaign이 격리 상태를 정당화하는 오류를 수신할 때까지 또는 오류 수가 5개에 도달할 때까지 주소가 직접 격리로 전송되거나 게재를 다시 시도합니다. |
| **[!UICONTROL Duplicate]** | 무시됨 | 주소가 세분화에서 이미 감지되었습니다. |
| **[!UICONTROL Not defined]** | 소프트 | 오류가 증가하지 않았기 때문에 주소가 유효합니다. | 아직. 이 유형의 오류는 서버에서 새 오류 메시지를 보낼 때 발생합니다. 이는 격리된 오류일 수 있지만 다시 발생하면 오류 카운터가 증가하여 기술 팀에게 알립니다. |
| **[!UICONTROL Error ignored]** | 무시됨 | 주소는 허용 목록에 추가하다에 있으며 어떤 경우에든 이메일이 전송됩니다. |
| **[!UICONTROL Address on denylist]** | 하드 | 발송 시 주소가 차단 목록에 추가하다에 추가되었습니다. |
| **[!UICONTROL Account disabled]** | 소프트/하드 | IAP(인터넷 접속 제공자)가 장기간 동안 비활성화 상태를 감지하면 사용자의 계정을 닫을 수 있습니다. 그러면 사용자 주소로 게재할 수 없습니다. 소프트 또는 하드 유형은 받은 오류 유형에 따라 달라집니다. 6개월 동안 활동이 없어 계정이 일시적으로 비활성화되고 아직 활성화될 수 있는 경우 **[!UICONTROL Erroneous]** 상태가 할당되고 게재를 다시 시도합니다. 수신된 오류가 계정이 영구적으로 비활성화되었음을 나타내는 경우 해당 계정은 즉시 격리로 전송됩니다. |
| **[!UICONTROL Not connected]** | 무시됨 | 메시지가 전송될 때 프로필의 휴대폰은 꺼져 있거나 네트워크에 연결되어 있지 않습니다. |
| **[!UICONTROL Invalid domain]** | 소프트 | 이메일 주소의 도메인이 잘못되었거나 더 이상 존재하지 않습니다. 이 프로필은 오류 수가 5개에 도달할 때까지 다시 타겟팅됩니다. 이후 레코드가 격리 상태로 설정되며 다시 시도되지 않습니다. |
| **[!UICONTROL Text too long]** | 무시됨 | SMS 메시지의 문자 수가 한도를 초과합니다. 자세한 내용은 [SMS 인코딩, 길이 및 음역](../../administration/using/configuring-sms-channel.md#sms-encoding--length-and-transliteration)을 참조하십시오. |
| **[!UICONTROL Character not supported by encoding]** | 무시됨 | SMS 메시지에 인코딩에서 지원하지 않는 문자가 하나 이상 포함되어 있습니다. 자세한 내용은 [문자 테이블 - GSM 표준](../../administration/using/configuring-sms-channel.md#table-of-characters---gsm-standard)을 참조하십시오. |


**관련 항목:**
* [하드 바운스](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/bounces.html#hard-bounces)
* [소프트 바운스](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/bounces.html#soft-bounces)

## 일시적 게재 실패 후 다시 시도 {#retries-after-a-delivery-temporary-failure}

일시적인 오류로 인해 메시지가 실패하면 게재 기간 동안 다시 시도됩니다. 오류 유형에 대한 자세한 내용은 [게재 실패 유형 및 이유](#delivery-failure-types-and-reasons)를 참조하십시오.

다시 시도 횟수(전송을 시작한 다음 날에 수행되어야 하는 다시 시도 횟수) 및 다시 시도 사이의 최소 지연 시간은 이제<!--managed by the Adobe Campaign Enhanced MTA,--> ip가 과거 및 현재 주어진 도메인에서 얼마나 잘 수행되고 있는지 기준으로 합니다. Campaign의 **다시 시도** 설정은 무시됩니다.

<!--Please note that Adobe Campaign Enhanced MTA is not available for the Push channel.-->

게재 기간을 수정하려면 개제 또는 게재 템플릿의 고급 매개 변수로 이동하여 [유효 기간](../../administration/using/configuring-email-channel.md#validity-period-parameters) 섹션의 **[!UICONTROL Delivery duration]** 필드를 편집합니다.

>[!IMPORTANT]
>
>**이제 Campaign 게재의&#x200B;**[!UICONTROL Delivery duration]**매개 변수는 3.5일 이내로 설정된 경우에만 사용됩니다.** 3.5일 이상의 값을 정의하면 고려되지 않습니다.

예를 들어 게재를 위한 다시 시도가 1일 후 중단되도록 하려면 게재 기간을 다음으로 설정할 수 있습니다. **1d**&#x200B;및 다시 시도 큐의 메시지는 1일 후 제거됩니다.

>[!NOTE]
>
>메시지가 최대 3.5일 동안 다시 시도 큐에 있고 게재에 실패하면 시간이 초과되고 상태가 업데이트됩니다<!--from **[!UICONTROL Sent]**--> 끝 **[!UICONTROL Failed]** 다음에서 [게재 로그](../../sending/using/monitoring-a-delivery.md#delivery-logs).

<!--MOVED TO configuring-email-channel.md > LEGACY SETTINGS
The default configuration allows five retries at one-hour intervals, followed by one retry per day for four days. The number of retries can be changed globally (contact your Adobe technical administrator) or for each delivery or delivery template (see [this section](../../administration/using/configuring-email-channel.md#sending-parameters)).-->

## 동기 및 비동기 오류 {#synchronous-and-asynchronous-errors}

게재가 전송되면 즉시(동기 오류) 또는 나중에(비동기 오류) 실패할 수 있습니다.

* **동기 오류**: Adobe Campaign 게재 서버가 접속한 원격 서버에서 즉시 오류 메시지를 반환하여 게재를 프로필 서버로 보낼 수 없습니다.
* **비동기 오류**: 반송 메일 또는 SR이 나중에 수신 서버에 의해 다시 전송되었습니다. 게재를 보낸 후 1주일까지 비동기 오류가 발생할 수 있습니다.

## 반송 메일 조건 {#bounce-mail-qualification}

동기 게재 실패 오류 메시지의 경우 Adobe Campaign Enhanced MTA(메시지 전송 에이전트)가 반송 유형 및 조건을 결정하고 해당 정보를 Campaign에 다시 전송합니다.

>[!NOTE]
>
>Campaign **[!UICONTROL Message qualification]** 테이블의 반송 조건은 더 이상 사용되지 않습니다.

비동기 반송은 **[!UICONTROL Inbound email]** 규칙을 통해 inMail 프로세스에 의해 계속 검증됩니다. 이러한 규칙에 액세스하려면 다음을 클릭하십시오. **Adobe** 로고, 왼쪽 상단에서 **[!UICONTROL Administration > Channels > Email > Email processing rules]** 및 선택 **[!UICONTROL Bounce mails]**. 이 규칙에 대한 자세한 내용은 [이 섹션](../../administration/using/configuring-email-channel.md#email-processing-rules).

바운스 및 다양한 유형의 바운스에 대한 자세한 내용은 [이 섹션](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/bounces.html#metrics-for-deliverability).

<!--MOVED TO configuring-email-channel.md > LEGACY SETTINGS

Bounces can have the following qualification statuses:

* **[!UICONTROL To qualify]**: the bounce mail needs to be qualified. Qualification must be done by the Deliverability team to ensure that the platform deliverability functions correctly. As long as it is not qualified, the bounce mail is not used to enrich the list of email processing rules.
* **[!UICONTROL Keep]**: the bounce mail was qualified and will be used by the **Update for deliverability** workflow to be compared to existing email processing rules and enrich the list.
* **[!UICONTROL Ignore]**: the bounce mail was qualified but will not be used by the **Update for deliverability** workflow. So it will not be sent to the client instances.

To list the various bounces and their associated error types et reasons, click the **Adobe** logo, in the top-left, then select **[!UICONTROL Administration > Channels > Quarantines > Message qualification]**.

![](assets/qualification.png)-->

## 이중 옵트인 메커니즘을 통해 이메일 전달성 최적화 {#optimizing-mail-deliverability-with-double-opt-in-mechanism}

이중 옵트인 메커니즘은 이메일을 보낼 때 가장 좋은 방법입니다. 틀리거나 잘못된 이메일 주소, 스팸 메일로부터 플랫폼을 보호하고 스팸 불만 가능성을 방지합니다.

원칙은 Campaign 데이터베이스에 &#39;프로필&#39;로 저장하기 전에 이메일 전송을 통해 방문자의 동의를 확인하는 것입니다. 방문자는 온라인 랜딩 페이지를 작성한 후 이메일을 수신하고 확인 링크를 클릭하여 구독을 마무리해야 합니다.

자세한 내용은 [이 섹션](../../channels/using/setting-up-a-double-opt-in-process.md)을 참조하십시오.
