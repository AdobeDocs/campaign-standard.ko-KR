---
title: 트랜잭션 메시지 실행 및 모니터링
description: 트랜잭션 메시지 실행에 대해 알아보고 트랜잭션 메시지를 모니터링하는 방법을 알아봅니다.
audience: channels
content-type: reference
topic-tags: transactional-messaging
context-tags: null
feature: Transactional Messaging
role: User
level: Intermediate
exl-id: 4cea7207-469c-46c5-9921-ae2f8f12d141
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '740'
ht-degree: 61%

---

# 트랜잭션 메시지 실행 및 모니터링 {#transactional-messaging-execution}

## 트랜잭션 메시지 실행 게재 {#transactional-message-execution-delivery}

메시지가 게시되고 사이트 통합이 완료되면 이벤트가 트리거되면 실행 게재에 할당됩니다.

<img src="assets/do-not-localize/icon_concepts.svg" width="60px">

**실행 게재**&#x200B;는 각 트랜잭션 메시지에 대해 한 달에 한 번 만들어지고 트랜잭션 메시지를 편집하고 다시 게시할 때마다 작동하는 기능 없는 기술 메시지입니다.

**관련 항목**:
* [트랜잭션 메시지 게시](../../channels/using/publishing-transactional-message.md#publishing-a-transactional-message)
* [이벤트 트리거 통합](../../channels/using/getting-started-with-transactional-msg.md#integrate-event-trigger)

## 트랜잭션 메시지 다시 시도 프로세스 {#transactional-message-retry-process}

일시적으로 게재되지 않는 트랜잭션 메시지는 게재가 만료될 때까지 수행되는 자동 다시 시도의 적용을 받습니다. 게재 기간에 대한 자세한 내용은 [유효 기간 매개 변수](../../administration/using/configuring-email-channel.md#validity-period-parameters)를 참조하십시오.

트랜잭션 메시지가 전송되지 않을 때, 두 개의 재시도 시스템이 있습니다.

* 트랜잭션 메시지 수준에서, 이벤트를 실행 배달에 할당하기 전에 트랜잭션 메시지가 실패할 수 있는데, 이는 이벤트 수신과 게재 준비 사이를 의미합니다. [이벤트 처리 다시 시도 프로세스](#event-processing-retry-process)를 참조하십시오.
* 전송 프로세스 수준에서 이벤트가 실행 게재로 할당되면 임시 오류로 인해 트랜잭션 메시지가 실패할 수 있습니다. [메시지 전송 다시 시도 프로세스](#message-sending-retry-process)를 참조하십시오.

### 이벤트 처리 다시 시도 프로세스 {#event-processing-retry-process}

이벤트가 트리거되면 실행 게재에 할당됩니다. 이벤트를 실행 게재에 할당할 수 없는 경우 이벤트 처리가 연기됩니다. 그런 다음 새 실행 게재에 할당될 때까지 다시 시도가 수행됩니다.

>[!NOTE]
>
>지연된 이벤트는 아직 실행 게재에 할당되지 않았기 때문에 트랜잭션 메시지 전송 로그에 나타나지 않습니다.

예를 들어, 콘텐츠가 올바르지 않거나, 액세스 권한 또는 브랜딩에 문제가 있거나, 유형 분류 규칙 등을 적용하는 경우, 오류 발견 등으로 이벤트를 실행 게재에 할당할 수 없습니다. 이 경우 메시지를 일시 중지하고 편집하여 문제를 해결하고 다시 게시할 수 있습니다. 그러면 다시 시도 시스템이 새 실행 게재에 할당합니다.

### 메시지 전송 다시 시도 프로세스 {#message-sending-retry-process}

이벤트가 실행 게재에 할당되었다면, 예를 들어 수신자의 사서함이 가득 찬 경우에 임시 오류로 인해 트랜잭션 메시지가 실패할 수 있습니다. 자세한 내용은 [일시적 게재 실패 후 다시 시도를 참조하십시오](../../sending/using/understanding-delivery-failures.md#retries-after-a-delivery-temporary-failure).

>[!NOTE]
>
>이벤트가 실행 게재에 할당되면 오직 해당 실행 게재의 전송 로그에만 나타납니다. 실패한 게재는 트랜잭션 메시지 전송 로그의 **[!UICONTROL Execution list]** 탭에 표시됩니다.

### 재시도 프로세스 제한 {#limitations}

**로그 업데이트 전송**

다시 시도 프로세스에서는 새 실행 게재의 전송 로그가 즉시 업데이트되지 않습니다(업데이트는 예약된 워크플로우를 통해 수행됩니다). 즉, 트랜잭션 이벤트가 새 실행 게재에서 처리된 경우에도 메시지는 **[!UICONTROL Pending]** 상태일 수 있습니다.

**실행 게재 실패**

실행 게재를 중단할 수 없습니다. 하지만 현재 실행 게재가 실패할 경우 새 이벤트가 수신되는 즉시 새 이벤트가 만들어지고 모든 새 이벤트가 이 새 실행 게재로 처리됩니다. 실패한 실행 게재로 새 이벤트가 처리되지 않습니다.

이미 실행 게재에 할당된 일부 이벤트가 다시 시도 프로세스의 일부로 연기된 경우 해당 실행 게재에 실패하면 다시 시도 시스템은 연기된 이벤트를 새 실행 게재에 할당하지 않습니다. 즉, 해당 이벤트가 손실됩니다. 영향을 받았을 수 있는 받는 사람을 보려면 [게재 로그](#monitoring-transactional-message-delivery)를 확인하세요.

## 트랜잭션 메시지 모니터링 {#monitoring-transactional-message-delivery}

트랜잭션 메시지를 모니터링하려면 해당 [실행 게재](#transactional-message-execution-delivery)에 액세스해야 합니다.

1. 메시지 게재 로그를 보려면 **[!UICONTROL Deployment]** 블록의 오른쪽 하단에 있는 아이콘을 클릭합니다.

   ![](assets/message-center_access_logs.png)

1. **[!UICONTROL Execution list]** 탭을 클릭합니다.

   ![](assets/message-center_execution_tab.png)

1. 선택한 실행 게재를 선택합니다.

   ![](assets/message-center_execution_delivery.png)

1. **[!UICONTROL Deployment]** 블록의 오른쪽 하단에 있는 아이콘을 다시 클릭합니다.

   ![](assets/message-center_execution_access_logs.png)

   각 실행 게재에 대해 표준 게재와 마찬가지로 게재 로그를 참조할 수 있습니다. 로그 액세스 및 사용에 대한 자세한 내용은 [게재 모니터링](../../sending/using/monitoring-a-delivery.md)을 참조하세요.

### 프로필 기반 트랜잭션 메시지 특성 {#profile-transactional-message-monitoring}

프로필 기반 트랜잭션 메시지의 경우 다음 프로필 정보를 모니터링할 수 있습니다.

**[!UICONTROL Sending logs]** 탭을 선택합니다. **[!UICONTROL Status]** 열의 **[!UICONTROL Sent]**&#x200B;은(는) 프로필이 옵트인되었음을 나타냅니다.

![](assets/message-center_marketing_sending_logs.png)

**[!UICONTROL Exclusions logs]** 탭을 선택하여 메시지 대상에서 제외된 주소(예: 차단 목록에 추가하다의 주소)를 확인합니다.

![](assets/message-center_marketing_exclusion_logs.png)

**[!UICONTROL Address on denylist]** 유형화 규칙이 옵트아웃한 프로필의 수신자를 모두 제외합니다.

이 규칙은 **[!UICONTROL Profile]** 표를 기반으로 하는 모든 트랜잭션 메시지에 적용되는 특정 유형화 중 일부입니다.

![](assets/message-center_marketing_typology.png)

**관련 항목**:

* [유형화 및 유형화 규칙 기본 정보](../../sending/using/about-typology-rules.md)
* [게재 모니터링](../../sending/using/monitoring-a-delivery.md)
