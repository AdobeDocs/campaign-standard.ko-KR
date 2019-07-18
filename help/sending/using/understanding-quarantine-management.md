---
title: 격리 관리 이해
seo-title: 격리 관리 이해
description: 격리 관리 이해
seo-description: 격리 관리를 통해 전달 가능성을 최적화하는 방법을 살펴볼 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 3 C 287865-1 ADA -4351-B 205-51807 FF 9 F 7 ED
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 전송
content-type: 참조
topic-tags: monitoring-messages
discoiquuid: de 3 a 50 b 6-ea 8 f -4521-996 b-c 49 cc 1 f 3 c 946
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 5b3ea982f08e1198e8c88f78a5faf8a80b935db4

---


# Understanding quarantine management{#understanding-quarantine-management}

## About quarantines {#about-quarantines}

예를 들어, 사서함이 꽉 찼거나 주소가 없는 경우 이메일 주소 또는 전화 번호를 격리할 수 있습니다.

In any case, the quarantine procedure complies with specific rules described in this [section](../../sending/using/understanding-quarantine-management.md#conditions-for-sending-an-address-to-quarantine).

### Optimizing your delivery through quarantines {#optimizing-your-delivery-through-quarantines}

The profiles whose email addresses or phone number are in quarantine are automatically excluded during message preparation (see [Identifying quarantined addresses for a delivery](../../sending/using/understanding-quarantine-management.md#identifying-quarantined-addresses-for-a-delivery)). 오류로 인해 전달 속도에 상당한 영향을 주므로 배달 속도를 높일 수 있습니다.

일부 인터넷 액세스 공급자는 잘못된 주소의 비율이 너무 높은 경우 스팸으로 자동 간주합니다. 따라서 이러한 공급자별로 블랙리스트를 사용하지 않아도 됩니다.

게다가 쿼리는 배달에서 잘못된 전화 번호를 제외하여 SMS 전송 비용을 줄이는 데 도움이 됩니다.

For more on best practices to secure and optimize your deliveries, refer to [this page](https://docs.campaign.adobe.com/doc/standard/getting_started/en/ACS_DeliveryBestPractices.html).

### Quarantine vs blacklisting {#quarantine-vs-blacklisting}

**쿼리는** 프로필 자체가 아닌 주소에만 적용됩니다. 즉, 두 프로필에 동일한 이메일 주소가 있으면 주소가 격리된 경우 두 프로필이 모두 영향을 받게 됩니다.

마찬가지로 이메일 주소가 격리된 프로필은 프로필을 업데이트하고 새 주소를 입력할 수 있으며 이후 배달 작업으로 타깃팅할 수 있습니다.

**반면에 블랙리스트는**&#x200B;구독 취소 (옵트아웃) 후 프로필이 더 이상 배달되지 않습니다. For more on the blacklisting process, refer to [Managing blacklisting in Campaign](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md).

>[!NOTE]
>
>사용자가 SMS 배달에서 옵트아웃하기 위해 "중지" 와 같은 키워드로 SMS 메시지에 답글을 달 때, 그의 프로필은 이메일 옵트아웃 프로세스에서처럼 차단되지 않습니다. The profile phone number is sent to quarantine with the **[!UICONTROL Blacklisted]** status. 이 상태는 전화 번호에만 해당되며, 사용자가 이메일 메시지를 계속 수신할 수 있도록 프로필은 차단되지 않습니다. For more on this, refer to [this section](../../channels/using/managing-incoming-sms.md#managing-stop-sms).

## Identifying quarantined addresses {#identifying-quarantined-addresses}

격리된 주소는 특정 게재 또는 전체 플랫폼에 대해 나열될 수 있습니다.

>[!NOTE]
>
>격리에서 주소를 제거해야 하는 경우 기술 관리자에게 문의하십시오.

### Identifying quarantined addresses for a delivery {#identifying-quarantined-addresses-for-a-delivery}

Quarantined addresses for a specific delivery are listed during the delivery preparation phase, in the **[!UICONTROL Exclusion logs]** tab of the delivery dashboard (see [this section](../../sending/using/monitoring-a-delivery.md#exclusion-logs)). For more on delivery preparation, refer to [this section](../../sending/using/preparing-the-send.md).

![](assets/exclusion_logs.png)

### Identifying quarantined addresses for the entire platform {#identifying-quarantined-addresses-for-the-entire-platform}

Administrators can list the addresses in quarantine for the entire platform from the **[!UICONTROL Administration > Channels > Quarantines > Addresses]** menu.

>[!NOTE]
>
>This menu lists quarantined elements for **email**, **SMS** and **Push notification** channels.

![](assets/quarantines1.png)

>[!NOTE]
>
>쿼리의 수가 증가하면 데이터베이스의 "마모와 찢음" 와 관련된 일반적인 효과가 됩니다. 예를 들어 이메일 주소의 라이프타임이 3 년으로 간주되고 수신자 테이블이 매년 50% 증가하는 경우, 쿼리의 증가는 다음과 같이 계산할 수 있습니다. 1 년 말: (1 * 0.33)/(1+0.5) = 22%. 연말 2: (((1.22 * 0.33) +0.33)/(1.5+0.75) = 32.5%).

## Conditions for sending an address to quarantine {#conditions-for-sending-an-address-to-quarantine}

Adobe Campaign manages quarantine according to the delivery failure type and the reason assigned during error messages qualification (see [Delivery failure types and reasons](../../sending/using/understanding-delivery-failures.md#delivery-failure-types-and-reasons) and [Bounce mail qualification](../../sending/using/understanding-delivery-failures.md#bounce-mail-qualification)).

* **무시됨 오류**: 무시됨 오류가 있으면 주소가 격리되지 않습니다.
* **하드 오류**: 해당 이메일 주소가 즉시 쿼리로 전송됩니다.
* **소프트 오류**: 소프트 오류로 인해 즉시 주소가 격리되지는 않지만 오류 카운터가 증가합니다. 오류 카운터가 한도 한계값에 도달하면 주소가 검역됩니다. 기본 구성에서 임계값은 5 개의 오류로 설정되며, 두 오류는 최소 24 시간 동안 발생하는 경우 중요합니다. 주소는 여섯 번째 오류에서 격리됩니다. 오류 카운터 임계값을 수정할 수 있습니다. For more on this, refer to this [page](../../administration/using/configuring-email-channel.md#email-channel-parameters).

   다시 시도한 후 배달이 성공하면 격리된 이전 주소의 오류 카운터가 다시 초기화됩니다. The address status changes to **[!UICONTROL Valid]** and it is deleted from the list of quarantines after two days by the **[!UICONTROL Database cleanup]** workflow.

If a user qualifies an email as a spam (**Feedback loop**), the message is automatically redirected towards a technical mailbox managed by Campaign. The user's email address is then automatically sent to quarantine with the **[!UICONTROL Blacklisted]** status. 이 상태는 주소만 참조하고 프로필은 차단되지 않으므로 사용자가 SMS 메시지와 푸시 알림을 계속 받을 수 있습니다.

>[!NOTE]
Adobe Campaign의 격리는 대/소문자를 구분합니다. 나중에 다시 시작할 수 없도록 소문자로 이메일 주소를 가져와야 합니다.

In the list of quarantined addresses (see [Identifying quarantined addresses for the entire platform](../../sending/using/understanding-quarantine-management.md#identifying-quarantined-addresses-for-the-entire-platform)), the **[!UICONTROL Error reason]** field indicates why the selected address was placed in quarantine.

![](assets/quarantines2.png)

