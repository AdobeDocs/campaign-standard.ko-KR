---
title: 격리 관리 이해
description: 격리 관리를 통해 게재 능력을 최적화하는 방법을 알아봅니다.
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
ht-degree: 81%

---


# 격리 관리 이해{#understanding-quarantine-management}

## 격리 기본 정보 {#about-quarantines}

이메일 주소나 전화번호를 격리하기도 합니다. 예를 들어 사서함이 가득 찼거나 주소가 존재하지 않는 경우가 있습니다.

어떤 경우든, 격리 절차는 이 [섹션](#conditions-for-sending-an-address-to-quarantine)에서 설명하는 특정한 규칙을 준수합니다.

### 격리를 통한 게재 최적화 {#optimizing-your-delivery-through-quarantines}

이메일 주소나 전화번호가 격리된 프로필은 메시지를 준비하는 동안 자동으로 제외됩니다([게재에 대해 격리된 주소 확인](#identifying-quarantined-addresses-for-a-delivery) 참조). 이를 통해 게재 속도를 높일 수 있습니다. 오류율은 게재 속도에 상당한 영향을 미치기 때문입니다.

일부 인터넷 액세스 제공 업체는 잘못된 주소의 비율이 너무 높은 경우 이메일을 자동으로 스팸으로 간주합니다. 따라서 격리 기능을 사용하면 이러한 공급자가 차단 목록에 추가하지 않을 수 있습니다.

또한 격리를 통해 잘못된 전화번호를 게재에서 제외하면 SMS를 보내는 비용을 줄이는 데 도움이 됩니다.

게재 보안 향상 및 최적화 모범 사례를 더 알아보려면 [이 페이지](https://helpx.adobe.com/kr/campaign/kb/delivery-best-practices.html)를 참조하십시오.

### 검역 대 차단 목록 {#quarantine-vs-block-list}

**격리**&#x200B;는 프로필 자체가 아니라 주소에만 적용됩니다. 즉, 두 프로필에 동일한 이메일 주소가 있는 경우 해당 주소가 격리되면 두 프로필 모두에 영향을 줍니다.

마찬가지로, 프로필의 이메일 주소가 격리 상태이더라도 프로필을 업데이트하여 새 주소를 입력하면 게재 작업 시 다시 타겟팅될 수 있습니다.

Being on the **block list**, on the other hand, will result in the profile no longer being targeted by any delivery, for example after an unsubscription (opt-out). 차단 목록 프로세스에 대한 자세한 내용은 캠페인 [에서 옵트인 및 옵트아웃 정보를 참조하십시오](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md).

>[!NOTE]
>
>사용자가 SMS 전달에서 옵트아웃하기 위해 &quot;STOP&quot;과 같은 키워드로 SMS 메시지에 댓글을 달면 이메일 옵트아웃 절차처럼 차단 목록에 프로필이 추가되지 않습니다. 해당 프로필의 전화번호는 **[!UICONTROL On block list]** 상태로 격리에 전송됩니다. 이 상태는 전화 번호만 가리키며, 프로필은 차단 목록에 없으므로 사용자가 이메일 메시지를 계속 수신하게 됩니다. 자세한 정보는 [이 섹션](../../channels/using/managing-incoming-sms.md#managing-stop-sms)을 참조하십시오.

## 격리된 주소 확인 {#identifying-quarantined-addresses}

특정 게재 또는 플랫폼 전체에 대해 격리된 주소를 나열할 수 있습니다.

>[!NOTE]
>
>주소를 격리 목록에서 제거해야 하는 경우 기술 관리자에게 문의하십시오.

### 게재에 대해 격리된 주소 확인 {#identifying-quarantined-addresses-for-a-delivery}

특정 게재에 대해 격리된 주소 목록은 게재 준비 단계 중 게재 대시보드의 **[!UICONTROL Exclusion logs]** 탭에서 확인할 수 있습니다([이 섹션](../../sending/using/monitoring-a-delivery.md#exclusion-logs) 참조). 게재 준비에 대한 자세한 정보는 [이 섹션](../../sending/using/preparing-the-send.md)을 참조하십시오.

![](assets/exclusion_logs.png)

### 플랫폼 전체에 대해 격리된 주소 확인 {#identifying-quarantined-addresses-for-the-entire-platform}

관리자는 **[!UICONTROL Administration > Channels > Quarantines > Addresses]** 메뉴에서 플랫폼 전체에 대해 격리된 주소 목록을 확인할 수 있습니다.

>[!NOTE]
>
>이 메뉴에는 **이메일**, **SMS** 및 **푸시 알림** 채널에 대해 격리된 요소의 목록이 표시됩니다.

![](assets/quarantines1.png)

>[!NOTE]
>
>격리 수의 증가는 데이터베이스의 &quot;소모&quot;에 따른 정상적인 현상입니다. 예를 들어 이메일 주소의 수명을 3년으로 보고 수신자 표가 매년 50%씩 증가할 경우, 격리 증가는 다음과 같이 계산할 수 있습니다. 첫 해가 끝나는 시점: (1*0.33)/(1+0.5)=22% 두 번째 해가 끝나는 시점: ((1.22*0.33)+0.33)/(1.5+0.75)=32.5% 

## 주소를 격리하는 조건 {#conditions-for-sending-an-address-to-quarantine}

Adobe Campaign은 게재 실패 유형 및 오류 메시지 자격 중에 할당된 이유에 따라 격리를 관리합니다([게재 실패 유형 및 이유](../../sending/using/understanding-delivery-failures.md#delivery-failure-types-and-reasons)와 [반송 메일 자격](../../sending/using/understanding-delivery-failures.md#bounce-mail-qualification) 참조).

* **무시된 오류**: 오류가 무시된 경우 주소가 격리되지 않습니다.
* **하드 오류**: 해당 이메일 주소가 즉시 격리됩니다.
* **소프트 오류**: 소프트 오류의 경우 주소가 즉시 격리되지는 않지만, 오류 카운터가 증가합니다. 오류 카운터가 제한 임계값에 도달하면 주소가 격리됩니다. 기본 구성에서 오류 임계값은 5로 설정되며, 두 오류가 최소 24시간 간격으로 발생하면 유효한 오류 두 개로 취급됩니다. 다섯 번째 오류 발생 시 주소가 격리됩니다. 오류 카운터 임계값은 수정할 수 있습니다. 자세한 정보는 이 [페이지](../../administration/using/configuring-email-channel.md#email-channel-parameters)를 참조하십시오.

   다시 시도하여 게재가 성공하면 격리되기 전의 해당 주소의 오류 카운터는 다시 초기화됩니다. 주소 상태가 **[!UICONTROL Valid]**(으)로 변경되며, 이틀 후에 **[!UICONTROL Database cleanup]** 워크플로우를 통해 격리 목록에서 삭제됩니다.

사용자가 이메일을 스팸 처리하면(**피드백 루프**) 해당 메시지는 Campaign에서 관리하는 기술 사서함으로 자동 리디렉션됩니다. 그러면 사용자의 이메일 주소가 자동으로 **[!UICONTROL On block list]** 상태로 격리됩니다. 이 상태는 주소만 참조하고, 프로필은 차단 목록에 있지 않으므로 사용자가 계속해서 SMS 메시지와 푸시 알림을 수신하게 됩니다.

>[!NOTE]
Adobe Campaign의 격리는 대소문자를 구분합니다. 이메일 주소를 소문자로 가져와야 이후에 다시 타겟팅되지 않습니다.

격리된 주소 목록([플랫폼 전체에 대해 격리된 주소 확인](#identifying-quarantined-addresses-for-the-entire-platform) 참조)의 **[!UICONTROL Error reason]** 필드에 선택한 주소가 격리된 이유가 표시됩니다.

![](assets/quarantines2.png)

