---
title: 스팸 차단 관리 이해
description: 격리 관리를 통해 전달 능력을 최적화하는 방법을 살펴볼 수 있습니다.
page-status-flag: never-activated
uuid: 3c287865-1ada-4351-b205-51807ff9f7ed
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: monitoring-messages
discoiquuid: de3a50b6-ea8f-4521-996b-c49cc1f3c946
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: f7e361d10d039718c421a3684c518347af2be951

---


# 스팸 차단 관리 이해{#understanding-quarantine-management}

## 검열에 대해 {#about-quarantines}

이메일 주소 또는 전화 번호는 사서함이 가득 찼거나 주소가 없는 경우 격리할 수 있습니다.

어떤 경우든 격리 절차는 이 [섹션에](#conditions-for-sending-an-address-to-quarantine)설명된 특정 규칙을 준수합니다.

### 검역을 통한 전달 최적화 {#optimizing-your-delivery-through-quarantines}

이메일 주소 또는 전화 번호가 격리된 프로필은 메시지 준비 동안 자동으로 제외됩니다(배달할 [격리된 주소](#identifying-quarantined-addresses-for-a-delivery)확인 참조). 이 경우 오류 비율이 배달 속도에 중요한 영향을 주므로 배달 시간을 단축할 수 있습니다.

일부 인터넷 액세스 공급자는 잘못된 주소 비율이 너무 높을 경우 이메일을 스팸으로 자동 간주합니다. 따라서 격리 기능을 사용하면 이러한 제공자에 의한 블랙리스트가 발생하지 않습니다.

게다가, 검역원은 잘못된 전화 번호를 배달에서 제외함으로써 SMS를 보내는 비용을 줄이는 데 도움을 주었다.

게재 보안 및 최적화를 위한 우수 사례에 대한 자세한 내용은 [이 페이지를](https://docs.campaign.adobe.com/doc/standard/getting_started/en/ACS_DeliveryBestPractices.html)참조하십시오.

### 격리 대 블랙리스트 {#quarantine-vs-blacklisting}

**검역은** 프로필 자체가 아닌 주소에만 적용됩니다. 즉, 두 프로필의 이메일 주소가 같은 경우 주소가 격리되면 두 프로필 모두에 영향을 줍니다.

마찬가지로, 격리된 이메일 주소를 가진 프로필은 프로필을 업데이트하고 새 주소를 입력한 다음 배달 작업으로 다시 타깃팅될 수 있습니다.

**반면에 블랙리스트는**&#x200B;더 이상 어떤 게재에서도 프로필을 타깃팅하지 않습니다(예: 가입 해지). 블랙 목록 프로세스에 대한 자세한 내용은 Campaign의 [블랙 목록 관리를 참조하십시오](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md).

>[!NOTE]
>
>사용자가 SMS 전달에서 옵트아웃하기 위해 &quot;STOP&quot;과 같은 키워드로 SMS 메시지에 댓글을 달면, 이 프로필은 이메일 옵트아웃 프로세스와 같이 블랙리스트에 추가되지 않습니다. 프로필 전화 번호는 **[!UICONTROL Blacklisted]** 상태 확인 대상으로 전송됩니다. 이 상태는 전화 번호만 참조하며, 프로필이 블랙리스트에 추가되지 않아 사용자가 이메일 메시지를 계속 수신하게 됩니다. For more on this, refer to [this section](../../channels/using/managing-incoming-sms.md#managing-stop-sms).

## 격리된 주소 확인 {#identifying-quarantined-addresses}

격리된 주소는 특정 배달 또는 전체 플랫폼에 대해 나열될 수 있습니다.

>[!NOTE]
>
>격리 시 주소를 제거해야 하는 경우 기술 관리자에게 문의하십시오.

### 배달할 격리된 주소 식별 {#identifying-quarantined-addresses-for-a-delivery}

배달 준비 단계 중에 배달 대시보드의 **[!UICONTROL Exclusion logs]** 탭에 특정 게재에 대해 격리된 주소가 나열됩니다( [이 섹션](../../sending/using/monitoring-a-delivery.md#exclusion-logs)참조). For more on delivery preparation, refer to [this section](../../sending/using/preparing-the-send.md).

![](assets/exclusion_logs.png)

### 전체 플랫폼의 격리된 주소 확인 {#identifying-quarantined-addresses-for-the-entire-platform}

관리자는 **[!UICONTROL Administration > Channels > Quarantines > Addresses]** 메뉴에서 전체 플랫폼의 격리 주소를 나열할 수 있습니다.

>[!NOTE]
>
>이 메뉴는 **이메일**, SMS 및 **푸시 알림** 채널에 대해 격리된 요소를 **나열합니다** .

![](assets/quarantines1.png)

>[!NOTE]
>
>격리의 증가는 데이터베이스의 &quot;마모&quot;와 관련된 일반적인 효과이다. 예를 들어, 이메일 주소의 수명이 3년으로 간주되고 수신자표가 매년 50% 증가하면 다음과 같이 격리의 증가를 계산할 수 있습니다.연말 1년:(1*0.33)/(1+0.5)=22% 연말 2일:((1.22*0.33)+0.33)/(1.5+0.75)=32.5%

## 격리 시 주소를 전송하는 조건 {#conditions-for-sending-an-address-to-quarantine}

Adobe Campaign은 게재 실패 유형 및 오류 메시지 자격 조건(게재 실패 유형 및 원인 [및](../../sending/using/understanding-delivery-failures.md#delivery-failure-types-and-reasons) 바운스 메일 자격 [참조)에 따라](../../sending/using/understanding-delivery-failures.md#bounce-mail-qualification)격리를 관리합니다.

* **무시된 오류**:무시된 오류는 주소를 격리로 보내지 않습니다.
* **오류**:해당 이메일 주소는 즉시 격리되도록 전송됩니다.
* **소프트 오류**:소프트 오류는 즉시 격리된 주소를 전송하지 않지만 오류 카운터를 증가시킵니다. 오류 카운터가 제한 임계값에 도달하면 주소가 격리됩니다. 기본 구성에서 임계값은 5개의 오류로 설정되며, 최소 24시간 간격으로 발생하는 경우 두 개의 오류가 중요합니다. 주소가 다섯 번째 오류 발생 시 격리됩니다. 오류 카운터 임계값을 수정할 수 있습니다. 자세한 내용은 이 [페이지를](../../administration/using/configuring-email-channel.md#email-channel-parameters)참조하십시오.

   다시 시도 후 배달을 성공하면 격리된 주소 이전의 오류 카운터가 다시 초기화됩니다. 주소 상태가 로 변경되고 **[!UICONTROL Valid]** 워크플로우에 의해 이틀 후 검역서 목록에서 삭제됩니다 **[!UICONTROL Database cleanup]** .

사용자가 이메일을 스팸으로 자격이 되는 경우(**피드백 루프**) 메시지는 Campaign에서 관리하는 기술 사서함으로 자동 리디렉션됩니다. 그러면 사용자의 이메일 주소가 **[!UICONTROL Blacklisted]** 상태와 함께 격리 상태로 자동 전송됩니다. 이 상태는 주소만 참조하며, 프로필은 차단되지 않으므로 사용자가 SMS 메시지와 푸시 알림을 계속 수신하게 됩니다.

>[!NOTE]
Adobe Campaign에서 격리 기능은 대소문자를 구분합니다. 이메일 주소를 나중에 다시 타깃팅되지 않도록 소문자로 가져와야 합니다.

격리된 주소 목록( [전체 플랫폼에](#identifying-quarantined-addresses-for-the-entire-platform)대해 격리된 주소 확인 참조)에서 **[!UICONTROL Error reason]** 필드가 선택한 주소가 격리된 이유를 나타냅니다.

![](assets/quarantines2.png)

