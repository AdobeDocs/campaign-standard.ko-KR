---
solution: Campaign Standard
product: campaign
title: 이벤트 트랜잭션 메시지
description: 이벤트 트랜잭션 메시지를 만들고 게시하는 방법에 대해 배웁니다.
audience: channels
content-type: reference
topic-tags: transactional-messaging
context-tags: null
translation-type: tm+mt
source-git-commit: 4e157a582de836fa325d95593491c756209b205e
workflow-type: tm+mt
source-wordcount: '1352'
ht-degree: 77%

---


# 트랜잭션 메시지 라이프사이클 {#publishing-transactional-message}

[트랜잭션 메시지](../../channels/using/editing-transactional-message.md)를 보낼 준비가 되면 게시할 수 있습니다.

이벤트를 테스트, 게시, 일시 중지, 게시 취소 및 삭제하는 단계는 아래에 자세히 설명되어 있습니다. 이 섹션에서는 트랜잭션 메시징 재시도 프로세스에 대해서도 설명합니다.

## 트랜잭션 메시지 게시 프로세스 {#transactional-messaging-pub-process}

아래 차트는 전체 트랜잭션 메시지 게시 프로세스를 보여줍니다.

![](assets/message-center_pub-process.png)

트랜잭션 메시지 게시에 대한 자세한 내용은 [이 섹션](#publishing-a-transactional-message)을 참조하십시오.
트랜잭션 메시지 일시 중지에 대한 자세한 내용은 [이 섹션](#suspending-a-transactional-message-publication)을 참조하십시오.
트랜잭션 메시지 게시 취소에 대한 자세한 내용은 [이 섹션](#unpublishing-a-transactional-message)을 참조하십시오.

이벤트 게시 및 게시 취소에 대한 자세한 내용은 [이 섹션](../../channels/using/publishing-transactional-event.md)을 참조하십시오.

## 트랜잭션 메시지 테스트 {#testing-a-transactional-message}

먼저 트랜잭션 메시지를 제대로 확인할 수 있는 특정 테스트 프로필을 만들어야 합니다.

### 특정 테스트 프로필 {#defining-specific-test-profile} 정의

메시지를 미리 보고 관련 증거를 전송할 수 있는 이벤트에 연결할 테스트 프로필을 정의합니다.

1. 트랜잭션 메시지 대시보드에서 **[!UICONTROL Create test profile]** 단추를 클릭합니다.

   ![](assets/message-center_test-profile.png)

1. **[!UICONTROL Event data used for personalization]** 섹션에서 JSON 형식으로 전송할 정보를 지정합니다. 메시지를 미리 볼 때와 테스트 프로필에서 증명를 받을 때 사용할 콘텐츠입니다.

   ![](assets/message-center_event-data.png)

   >[!NOTE]
   >
   >프로필 테이블과 관련된 정보를 입력할 수도 있습니다. [이벤트 실행](../../channels/using/configuring-transactional-event.md#enriching-the-transactional-message-content)<!--and [Personalizing a transactional message](../../channels/using/editing-transactional-message.md#personalizing-a-transactional-message)-->을 참조하십시오.

1. 테스트 프로필이 만들어지면 트랜잭션 메시지에 미리 지정됩니다. 메시지의 **[!UICONTROL Test profiles]** 블록을 클릭하여 증명의 대상을 확인합니다.

   ![](assets/message-center_5.png)

새 테스트 프로필을 만들거나 **[!UICONTROL Test profiles]** 메뉴에 이미 있는 테스트 프로필을 사용할 수도 있습니다. 방법은 다음과 같습니다.

1. 왼쪽 상단 모서리에서 **[!UICONTROL Adobe Campaign]** 로고를 클릭한 다음 **[!UICONTROL Profiles & audiences]** > **[!UICONTROL Test profiles]**&#x200B;을 선택합니다.
1. **[!UICONTROL Event]** 섹션에서 방금 만든 이벤트를 선택합니다. 예제에서는 &quot;장바구니 포기(EVTcartAbandonment)&quot;를 선택합니다.
1. **[!UICONTROL Event data]** 텍스트 상자에 JSON 형식으로 전송할 정보를 지정합니다.

   ![](assets/message-center_3.png)

1. 변경 내용을 저장합니다.
1. 만든 메시지에 액세스하고 업데이트된 테스트 프로필을 선택합니다.

**관련 항목:**

* [테스트 프로필 관리](../../audiences/using/managing-test-profiles.md)
* [대상자 만들기](../../audiences/using/creating-audiences.md)

### 증명 {#sending-proof} 전송

하나 이상의 특정 테스트 프로필을 만들고 트랜잭션 메시지를 저장한 후에는 이를 테스트하기 위한 증거를 보낼 수 있습니다.

![](assets/message-center_10.png)

증명 전송 단계는 [증거 전송](../../sending/using/sending-proofs.md) 섹션에 자세히 설명되어 있습니다.

## 트랜잭션 메시지 게시 {#publishing-a-transactional-message}

트랜잭션 메시지를 확인하고 나면 게시할 수 있습니다.

![](assets/message-center_12.png)

이제 &quot;장바구니 포기&quot; 이벤트가 트리거되는 경우, 수신자의 제목과 성, 장바구니 URL, 제품 목록이 정의되어 있다면 마지막으로 상담한 제품 또는 제품 목록, 그리고 보낼 총 장바구니 금액이 포함된 메시지를 자동으로 표시합니다.

트랜잭션 메시지에 대한 보고서에 액세스하려면 **[!UICONTROL Reports]** 버튼을 사용하십시오. [동적 보고서](../../reporting/using/about-dynamic-reports.md)를 참조하십시오.

![](assets/message-center_13.png)

### 트랜잭션 메시지 게시 일시 중단 {#suspending-a-transactional-message-publication}

예를 들어 메시지에 포함된 데이터를 수정하기 위해 **[!UICONTROL Pause]** 버튼을 사용하여 트랜잭션 메시지 게시를 일시 중단할 수 있습니다. 그러면 이벤트는 더 이상 처리되지 않고 대신 Adobe Campaign 데이터베이스의 큐에 보관됩니다.

큐에 있는 이벤트는 REST API에 정의된 기간 동안 보관됩니다([REST API 문서](../../api/using/managing-transactional-messages.md) 참조). 트리거 코어 서비스를 사용 중인 경우 트리거 이벤트에서 보관됩니다([Adobe Experience Cloud 트리거 정보](../../integrating/using/about-adobe-experience-cloud-triggers.md) 참조).

![](assets/message-center_pause.png)

**[!UICONTROL Resume]**&#x200B;을(를) 클릭하면 큐에 있는 모든 이벤트(만료되지 않은 경우)가 처리됩니다. 템플릿 게시가 일시 중단된 동안 수행된 모든 수정 사항이 포함되어 있습니다.

### 트랜잭션 메시지 게시 취소 {#unpublishing-a-transactional-message}

**[!UICONTROL Unpublish]**&#x200B;을(를) 클릭하면 트랜잭션 메시지 게시를 취소할 수 있고 이전에 만든 이벤트에 해당하는 리소스를 REST API에서 삭제하는 해당 이벤트의 게시도 취소할 수 있습니다.

![](assets/message-center_unpublish-template.png)

이제 웹 사이트를 통해 이벤트가 트리거되더라도 해당 메시지는 더 이상 전송되지 않고 데이터베이스에 저장되지 않습니다.

>[!NOTE]
>
>메시지를 다시 게시하려면 해당 이벤트 구성으로 돌아가서 [이벤트](../../channels/using/publishing-transactional-event.md)를 게시한 다음 [메시지](#publishing-a-transactional-message)를 게시해야 합니다.

일시 중지된 트랜잭션 메시지의 게시를 취소하는 경우 다시 게시하기 전에 최대 24시간까지 기다려야 할 수 있습니다. **[!UICONTROL Database cleanup]** 워크플로우가 대기열로 전송된 모든 이벤트를 지우기 위해서 입니다.

메시지 일시 중지 단계는 [트랜잭션 메시지 게시 일시 중단](#suspending-a-transactional-message-publication) 섹션에 자세히 설명되어 있습니다.

매일 오전 4시에 실행되는 **[!UICONTROL Database cleanup]** 워크플로우는 **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** > **[!UICONTROL Workflows]**&#x200B;을(를) 통해 액세스할 수 있습니다.

### 트랜잭션 메시지 삭제 {#deleting-a-transactional-message}

트랜잭션 메시지 게시가 취소되었거나 트랜잭션 메시지가 아직 게시되지 않았으면 트랜잭션 메시지 목록에서 삭제할 수 있습니다. 삭제 방법:

1. 왼쪽 상단 모서리에서 **[!UICONTROL Adobe Campaign]** 로고를 클릭한 다음 **[!UICONTROL Marketing plans]** > **[!UICONTROL Transactional messages]** > **[!UICONTROL Transactional messages]**&#x200B;을(를) 선택합니다.
1. 마우스를 원하는 메시지 위로 가져갑니다.
1. **[!UICONTROL Delete element]** 버튼을 클릭합니다.

![](assets/message-center_delete-template.png)

하지만 트랜잭션 메시지를 삭제하는 것은 특정 조건에서만 수행할 수 있습니다.

* 트랜잭션 메시지에 **[!UICONTROL Draft]** 상태가 있는지 확인해야 합니다. 없다면 메시지를 삭제할 수 없습니다. **[!UICONTROL Draft]** 상태는 아직 게시되지 않았거나 [게시 취소](#unpublishing-a-transactional-message)([일시 중지](#suspending-a-transactional-message-publication)가 아님)된 메시지에적용됩니다.

* **트랜잭션 메시지**: 다른 트랜잭션 메시지가 해당 이벤트에 연결되어 있지 않는 한, 트랜잭션 메시지의 게시를 취소하는 경우, 트랜잭션 메시지를 성공적으로 삭제하려면 이벤트 구성도 게시 취소해야 합니다. 자세한 내용은 [이벤트 게시 취소](../../channels/using/publishing-transactional-event.md#unpublishing-an-event)를 참조하십시오.

   >[!IMPORTANT]
   >
   >이미 알림을 보낸 트랜잭션 메시지를 삭제하면 전송 및 추적 로그도 삭제됩니다.

* **기본 제공 이벤트 템플릿의 트랜잭션 메시지(내부 트랜잭션 메시지)**: 내부 트랜잭션 메시지가 해당 내부 이벤트와 연결된 유일한 메시지인 경우 삭제할 수 없습니다. 먼저 복제하거나 **[!UICONTROL Resources]** > **[!UICONTROL Templates]** > **[!UICONTROL Transactional message templates]** 메뉴를 통해 다른 트랜잭션 메시지를 만들어야 합니다.

## 트랜잭션 메시지 다시 시도 프로세스 {#transactional-message-retry-process}

일시적으로 게재되지 않는 트랜잭션 메시지는 게재가 만료될 때까지 수행되는 자동 다시 시도의 적용을 받습니다. 게재 기간에 대한 자세한 내용은 [유효 기간 매개 변수](../../administration/using/configuring-email-channel.md#validity-period-parameters)를 참조하십시오.

트랜잭션 메시지가 전송되지 않을 때, 두 개의 재시도 시스템이 있습니다.

* 트랜잭션 메시지 수준에서, 이벤트를 실행 배달에 할당하기 전에 트랜잭션 메시지가 실패할 수 있는데, 이는 이벤트 수신과 게재 준비 사이를 의미합니다. [이벤트 처리 다시 시도 프로세스](#event-processing-retry-process)를 참조하십시오.
* 전송 프로세스 수준에서 이벤트가 실행 게재로 할당되면 임시 오류로 인해 트랜잭션 메시지가 실패할 수 있습니다. [메시지 전송 다시 시도 프로세스](#message-sending-retry-process)를 참조하십시오.

### 이벤트 처리 다시 시도 프로세스 {#event-processing-retry-process}

이벤트를 실행 게재에 할당할 수 없는 경우 이벤트 처리가 연기됩니다. 그런 다음 새 실행 게재에 할당될 때까지 다시 시도가 수행됩니다.

>[!NOTE]
>
>지연된 이벤트는 아직 실행 게재에 할당되지 않았기 때문에 트랜잭션 메시지 전송 로그에 나타나지 않습니다.

예를 들어, 콘텐츠가 올바르지 않거나, 액세스 권한 또는 브랜딩에 문제가 있거나, 유형 분류 규칙 등을 적용하는 경우, 오류 발견 등으로 이벤트를 실행 게재에 할당할 수 없습니다. 이 경우 메시지를 일시 중지하고 편집하여 문제를 해결하고 다시 게시할 수 있습니다. 그러면 다시 시도 시스템이 새 실행 게재에 할당합니다.

### 메시지 전송 다시 시도 프로세스 {#message-sending-retry-process}

이벤트가 실행 게재에 할당되었다면, 예를 들어 수신자의 사서함이 가득 찬 경우에 임시 오류로 인해 트랜잭션 메시지가 실패할 수 있습니다. 자세한 내용은 [일시적 게재 실패 후 다시 시도를 참조하십시오](../../sending/using/understanding-delivery-failures.md#retries-after-a-delivery-temporary-failure).

>[!NOTE]
>
>이벤트가 실행 게재에 할당되면 오직 해당 실행 게재의 전송 로그에만 나타납니다. 실패한 배달은 트랜잭션 메시지 전송 로그의 **[!UICONTROL Execution list]** 탭에 표시됩니다.

### 프로세스 제한 다시 시도 {#limitations}

**로그 업데이트 전송**

다시 시도 프로세스에서는 새 실행 게재의 전송 로그가 즉시 업데이트되지 않습니다(업데이트는 예약된 워크플로우를 통해 수행됩니다). 즉, 트랜잭션 이벤트가 새 실행 게재에서 처리된 경우에도 메시지는 **[!UICONTROL Pending]** 상태일 수 있습니다.

**실행 게재 실패**

실행 게재를 중단할 수 없습니다. 하지만 현재 실행 게재가 실패할 경우 새 이벤트가 수신되는 즉시 새 이벤트가 만들어지고 모든 새 이벤트가 이 새 실행 게재로 처리됩니다. 실패한 실행 게재로 새 이벤트가 처리되지 않습니다.

이미 실행 게재에 지정된 일부 이벤트가 연기된 경우, 해당 실행 게재에 실패하면 다시 시도 시스템은 연기된 이벤트를 새 실행 게재에 할당하지 않습니다. 즉, 해당 이벤트가 손실됩니다.
