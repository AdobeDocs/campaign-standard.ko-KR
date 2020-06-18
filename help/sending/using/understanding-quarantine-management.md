---
title: 스팸 차단 관리 이해
description: 검역 관리를 통해 전달 능력을 최적화하는 방법을 살펴볼 수 있습니다.
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
source-git-commit: 121ec37cef6193d3a7085b6d0296b6a2e7cafa06
workflow-type: tm+mt
source-wordcount: '801'
ht-degree: 1%

---


# 스팸 차단 관리 이해{#understanding-quarantine-management}

## 검열에 대해 {#about-quarantines}

예를 들어, 사서함이 가득 찼거나 주소가 없는 경우 이메일 주소 또는 전화 번호를 격리할 수 있습니다.

어떤 경우든, 격리 절차는 이 [섹션에 설명된 특정 규칙을 준수합니다](#conditions-for-sending-an-address-to-quarantine).

### 검역을 통해 전달의 최적화 {#optimizing-your-delivery-through-quarantines}

이메일 주소 또는 전화 번호가 격리된 프로필은 메시지 준비 시 자동으로 제외됩니다(배달할 [주소 격리됨 참조](#identifying-quarantined-addresses-for-a-delivery)). 이 경우 오류 비율이 배달 속도에 중요한 영향을 주기 때문에 배달 시간을 단축할 수 있습니다.

일부 인터넷 액세스 제공업체는 잘못된 주소의 비율이 너무 높은 경우 이메일을 스팸으로 자동 간주합니다. 따라서 격리 기능을 사용하면 이러한 공급자가 블록 목록에 추가하지 않을 수 있습니다.

게다가, 검역원은 잘못된 전화 번호를 배달에서 제외함으로써 SMS를 보내는 비용을 줄이는 데 도움을 주었다.

배달 보안 및 최적화를 위한 우수 사례에 대한 자세한 내용은 [이 페이지를 참조하십시오](https://docs.campaign.adobe.com/doc/standard/getting_started/en/ACS_DeliveryBestPractices.html).

### 격리 및 블록 목록 {#quarantine-vs-block-list}

**검역은** 프로필 자체가 아닌 주소에만 적용됩니다. 즉, 두 프로필에 동일한 이메일 주소가 있는 경우 주소가 격리되면 두 프로필 모두에 영향을 줍니다.

마찬가지로, 격리된 이메일 주소를 가진 프로필은 자신의 프로필을 업데이트하고 새 주소를 입력한 다음 배달 작업으로 다시 타깃팅될 수 있습니다.

반면에 **블록 목록에**&#x200B;있으면 더 이상 프로필이 전달의 대상이 되지 않습니다(예: 가입 해지). 차단 목록 프로세스에 대한 자세한 내용은 캠페인 [에서 옵트인 및 옵트아웃 정보를 참조하십시오](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md).

>[!NOTE]
>
>사용자가 SMS 전달에서 옵트아웃하기 위해 &quot;STOP&quot;과 같은 키워드로 SMS 메시지에 댓글을 달면 이메일 옵트아웃 과정과 같이 차단 목록에 프로필이 추가되지 않습니다. 프로필 전화 번호는 **[!UICONTROL On block list]** 상태 확인 대상으로 전송됩니다. 이 상태는 전화 번호만 참조하며, 프로필은 차단 목록에 없으므로 사용자가 이메일 메시지를 계속 수신하게 됩니다. 이 작업에 대한 자세한 정보는 [이 섹션](../../channels/using/managing-incoming-sms.md#managing-stop-sms)을 참조하십시오.

## 격리된 주소 식별 {#identifying-quarantined-addresses}

격리된 주소는 특정 배달 또는 전체 플랫폼에 대해 나열될 수 있습니다.

>[!NOTE]
>
>격리 시 주소를 제거해야 하는 경우 기술 관리자에게 문의하십시오.

### 배달할 격리된 주소 식별 {#identifying-quarantined-addresses-for-a-delivery}

특정 게재에 대해 격리된 주소는 배달 준비 단계 중 배달 대시보드의 **[!UICONTROL Exclusion logs]** 탭( [이 섹션 참조)에 나열됩니다](../../sending/using/monitoring-a-delivery.md#exclusion-logs). For more on delivery preparation, refer to [this section](../../sending/using/preparing-the-send.md).

![](assets/exclusion_logs.png)

### 전체 플랫폼의 격리된 주소 식별 {#identifying-quarantined-addresses-for-the-entire-platform}

관리자는 **[!UICONTROL Administration > Channels > Quarantines > Addresses]** 메뉴에서 전체 플랫폼의 격리 주소를 나열할 수 있습니다.

>[!NOTE]
>
>이 메뉴에는 **이메일**, **SMS** 및 **푸시 알림** 채널에 대해 격리된 요소가나열됩니다.

![](assets/quarantines1.png)

>[!NOTE]
>
>검역소의 수가 증가한 것은 데이터베이스의 &quot;마모&quot;와 관련된 정상적인 효과이다. 예를 들어 이메일 주소의 수명이 3년으로 간주되고 수신자의 테이블이 매년 50%씩 증가하면 다음과 같이 격리조치를 계산할 수 있습니다. 1년말: (1*0.33)/(1+0.5)=22%. 2년말: (1.22*0.33)+0.33)/(1.5+0.75)=32.5%

## 격리에 주소 보내기 조건 {#conditions-for-sending-an-address-to-quarantine}

Adobe Campaign은 배달 실패 유형 및 오류 메시지 자격 조건 중에 할당된 이유에 따라 검역을 관리합니다( [배달 실패 유형 및 원인](../../sending/using/understanding-delivery-failures.md#delivery-failure-types-and-reasons) 및 [바운스 메일 자격 조건](../../sending/using/understanding-delivery-failures.md#bounce-mail-qualification)참조).

* **무시된 오류**: 무시된 오류는 격리된 주소를 보내지 않습니다.
* **오류**: 해당 이메일 주소는 즉시 격리하도록 전송됩니다.
* **소프트 오류**: 소프트 오류는 즉시 격리된 주소를 보내지 않지만 오류 카운터를 증가시킵니다. 오류 카운터가 제한 임계값에 도달하면 주소가 격리됩니다. 기본 구성에서 임계값은 5개의 오류로 설정되며, 최소 24시간 간격으로 발생하는 경우 두 개의 오류가 중요합니다. 다섯 번째 오류 발생 시 주소가 격리되어 있다. 오류 카운터 임계값을 수정할 수 있습니다. For more on this, refer to this [page](../../administration/using/configuring-email-channel.md#email-channel-parameters).

   재시도 후 배달이 성공하면 격리된 주소 이전의 오류 카운터가 다시 초기화됩니다. 주소 상태가 로 바뀌며 **[!UICONTROL Valid]** , 이틀 후에 검역국 목록에서 **[!UICONTROL Database cleanup]** 삭제된다.

사용자가 이메일을 스팸(**피드백 루프**)으로 자격이 되는 경우 메시지가 Campaign에서 관리하는 기술 사서함으로 자동 리디렉션됩니다. 그러면 사용자의 이메일 주소가 **[!UICONTROL On block list]** 상태로 격리되도록 자동으로 전송됩니다. 이 상태는 주소만 참조하고, 프로필은 차단 목록에 없으므로 사용자가 계속해서 SMS 메시지와 푸시 알림을 수신합니다.

>[!NOTE]
Adobe Campaign에서의 검역은 대/소문자를 구분합니다. 이메일 주소가 나중에 다시 타깃팅되지 않도록 이메일 주소를 낮은 대소문자 로 가져와야 합니다.

격리된 주소 목록(전체 플랫폼 [에 대해 격리된 주소](#identifying-quarantined-addresses-for-the-entire-platform)확인 참조)에서 선택한 주소가 격리된 이유를 **[!UICONTROL Error reason]** 나타내는 필드입니다.

![](assets/quarantines2.png)

