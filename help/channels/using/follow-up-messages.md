---
title: 후속 메시지
description: 후속 메시지를 만들고 관리하고 보내는 방법을 알아봅니다.
audience: channels
content-type: reference
topic-tags: transactional-messaging
feature: Transactional Messaging
role: User
level: Intermediate
exl-id: 0a05cf20-7c8f-406b-acfd-7aece2c5dd26
source-git-commit: ee7539914aba9df9e7d46144e437c477a7e52168
workflow-type: tm+mt
source-wordcount: '773'
ht-degree: 2%

---

# 후속 메시지 {#follow-up-messages}

후속 메시지는 워크플로우에서 특정 트랜잭션 메시지의 수신자에게 다른 커뮤니케이션을 보내는 데 사용할 수 있는 사전 정의된 마케팅 게재 템플릿입니다.

에 설명된 예를 다시 사용하겠습니다. [트랜잭션 메시지 작동 원리](../../channels/using/getting-started-with-transactional-msg.md#transactional-messaging-operating-principle) 섹션: 장바구니에 제품을 추가했지만 구매를 완료하지 않고 사이트를 떠난 웹 사이트 사용자에게 장바구니 중단 이메일이 전송됩니다.

장바구니 포기 알림을 받았지만 3일 후에도 열지 않은 모든 고객에게 친숙한 미리 알림을 보내려고 합니다. 보낸 첫 번째 이메일에서 사용한 것과 동일한 데이터를 기반으로 후속 메시지를 받게 됩니다.

## 후속 작업 메시지를 보내기 위한 이벤트 구성 {#configuring-an-event-to-send-a-follow-up-message}

후속 메시지를 보내려면 먼저 이미 받은 트랜잭션 메시지에 해당하는 이벤트를 그에 따라 구성해야 합니다.

1. 이벤트 트랜잭션 메시지를 보내기 위해 만든 것과 동일한 이벤트 구성을 사용합니다. 다음을 참조하십시오 [트랜잭션 이벤트 구성](../../channels/using/configuring-transactional-event.md).
1. 이벤트를 구성할 때 다음을 확인하십시오. **[!UICONTROL Create follow-up delivery template for this event]** 이벤트를 게시하기 전에 상자를 표시합니다.

   ![](assets/message-center_follow-up-checkbox.png)

1. [이벤트 미리보기 및 게시](../../channels/using/publishing-transactional-event.md#previewing-and-publishing-the-event).

이벤트가 게시되면 새 이벤트에 연결된 트랜잭션 메시지 및 후속 게재 템플릿이 자동으로 만들어집니다. 후속 메시지를 보내는 단계는에 자세히 설명되어 있습니다. [이 섹션](#sending-a-follow-up-message).

## 후속 메시지 액세스 {#accessing-the-follow-up-messages}

워크플로우에서 이벤트를 처리하려면 게재 템플릿이 필요합니다. 하지만 이벤트를 게시할 때는 [트랜잭션 메시지](../../channels/using/editing-transactional-message.md) 만들어진 항목은 템플릿으로 사용할 수 없습니다. 따라서 이 이벤트 유형을 지원하고 워크플로우에서 템플릿으로 사용할 수 있도록 설계된 특정 후속 게재 템플릿을 만들어야 합니다.

이 템플릿에 액세스하려면:

1. 다음을 클릭합니다. **Adobe** 로고, 왼쪽 상단 모서리
1. 선택 **[!UICONTROL Resources]** > **[!UICONTROL Templates]** > **[!UICONTROL Delivery templates]**.
1. 다음 확인: **[!UICONTROL Follow-up messages]** 왼쪽 창의 상자입니다.

   ![](assets/message-center_follow-up-search.png)

후속 메시지만 표시됩니다.

>[!IMPORTANT]
>
>을(를) 가진 사용자만 [관리](../../administration/using/users-management.md#functional-administrators) 역할은 트랜잭션 메시지에 액세스하고 편집할 수 있습니다.

## 후속 메시지 보내기 {#sending-a-follow-up-message}

후속 게재 템플릿을 만들면 워크플로우에서 후속 메시지를 보낼 수 있습니다.

<!--You need to set up a workflow targeting the event corresponding to the transactional message that was already received.-->

1. 마케팅 활동 목록에 액세스하고 새 워크플로우를 만듭니다.

   다음을 참조하십시오 [워크플로우 구축](../../automating/using/building-a-workflow.md#creating-a-workflow).

1. 드래그 앤 드롭 **[!UICONTROL Scheduler]** 활동을 워크플로우에 추가하고 엽니다. 실행 빈도를 하루에 한 번으로 설정하십시오.

   스케줄러 활동은 다음에 표시됩니다. [스케줄러](../../automating/using/scheduler.md) 섹션.

1. 드래그 앤 드롭 **[!UICONTROL Query]** 활동을 워크플로우에 추가하고 엽니다.

   쿼리 활동은 다음에 표시됩니다. [쿼리](../../automating/using/query.md) 섹션.

1. 프로필 리소스 이외의 리소스에 대해 쿼리를 실행하려면 해당 활동의 **[!UICONTROL Properties]** 탭을 클릭하고 **[!UICONTROL Resource]** 드롭다운 목록입니다.

   ![](assets/message-center_follow-up-query-properties.png)

   >[!NOTE]
   >
   >이 활동은 기본적으로 프로필을 검색하도록 사전 구성되어 있습니다.

1. 이 이벤트의 데이터에만 액세스할 수 있도록 타깃팅할 이벤트를 선택합니다.

   ![](assets/message-center_follow-up-query-resource.png)

1. 활동으로 이동 **[!UICONTROL Target]** 탭을 클릭하고 **[!UICONTROL Delivery logs (logs)]** 팔레트의 요소를 작업 영역으로 복사합니다.

   ![](assets/message-center_follow-up-delivery-logs.png)

   선택 **[!UICONTROL Exists]** 이메일을 받은 모든 고객을 타겟팅합니다.

   ![](assets/message-center_follow-up-delivery-logs-exists.png)

1. 이동 **[!UICONTROL Tracking logs (tracking)]** 팔레트에서 작업 영역으로 요소 추가 및 선택 **[!UICONTROL Does not exist]** 이메일을 열지 않은 모든 고객을 타겟팅합니다.

   ![](assets/message-center_follow-up-delivery-and-tracking-logs.png)

1. 타겟팅하는 이벤트를 끌어서 놓습니다(**장바구니 포기** 이 예제에서는) 팔레트에서 작업 공간으로 이동합니다. 그런 다음 3일 전에 전송된 모든 메시지를 타겟팅하는 규칙을 정의합니다.

   ![](assets/message-center_follow-up-created.png)

   즉, 워크플로우를 실행하기 3일 전에 트랜잭션 메시지를 받고 아직 열지 않은 모든 수신자가 타겟팅됩니다.

   클릭 **[!UICONTROL Confirm]** 을 눌러 쿼리를 저장합니다.

1. 드래그 앤 드롭 **이메일 게재** 활동을 워크플로우에 추가합니다.

   이메일 게재 활동은에 표시됩니다. [이메일 게재](../../automating/using/email-delivery.md) 섹션.

   ![](assets/message-center_follow-up-workflow.png)

   다음을 사용할 수도 있습니다 [SMS 게재](../../automating/using/sms-delivery.md) 또는 [푸시 알림 게재](../../automating/using/push-notification-delivery.md) 활동. 이 경우 다음을 선택하십시오. **[!UICONTROL Mobile (SMS)]** 또는 **[!UICONTROL Mobile application]** 채널 : 이벤트 구성을 만들 때 사용합니다. [이벤트 만들기](../../channels/using/configuring-transactional-event.md#creating-an-event)를 참조하십시오.

1. 를 엽니다. **이메일 게재** 활동. 만들기 마법사에서 **[!UICONTROL Follow-up messages]** 상자를 열고 이벤트를 게시한 후 만든 후속 게재 템플릿을 선택합니다.

   ![](assets/message-center_follow-up-template.png)

1. 후속 메시지 콘텐츠에서 개인화 필드를 추가하여 이벤트의 콘텐츠를 활용할 수 있습니다.

   ![](assets/message-center_follow-up-content.png)

1. 을 선택하여 이벤트를 생성할 때 정의한 필드를 찾습니다 **[!UICONTROL Context]** > **[!UICONTROL Real-time event]** > **[!UICONTROL Event context]**. 다음을 참조하십시오 [트랜잭션 메시지 개인화](../../channels/using/editing-transactional-message.md#personalizing-a-transactional-message).

   ![](assets/message-center_follow-up-personalization.png)

   즉, 이벤트를 처음 전송할 때 사용된 보강된 데이터를 포함하여 동일한 콘텐츠를 활용하여 개인화된 친숙한 알림 메시지를 만들 수 있습니다.

1. 활동을 저장하고 워크플로우를 시작합니다.

워크플로우가 시작되면 3일 전에 장바구니 포기 알림을 받았지만 열지 않은 모든 고객은 동일한 데이터를 기반으로 후속 메시지를 받게 됩니다.

>[!NOTE]
>
>다음을 선택한 경우 **[!UICONTROL Profile]** 타겟팅 차원 이벤트 구성을 만들 때 후속 메시지는 Adobe Campaign 마케팅 데이터베이스도 활용합니다. [프로필 트랜잭션 메시지](../../channels/using/editing-transactional-message.md#profile-transactional-message-specificities)를 참조하십시오.
