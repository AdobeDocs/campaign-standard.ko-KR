---
title: 트랜잭션 메시지 테스트
description: Adobe Campaign에서 트랜잭션 메시지를 테스트하는 방법을 알아봅니다.
audience: channels
content-type: reference
topic-tags: transactional-messaging
context-tags: null
feature: Transactional Messaging
role: User
level: Intermediate
exl-id: 5138826d-ae08-403b-91ef-91027ef6e78e
source-git-commit: ee7539914aba9df9e7d46144e437c477a7e52168
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 30%

---

# 트랜잭션 메시지 테스트 {#testing-a-transactional-message}

트랜잭션 메시지를 게시하기 전에 메시지를 제대로 확인할 수 있는 특정 테스트 프로필을 만들 수 있습니다.

## 특정 테스트 프로필 정의 {#defining-specific-test-profile}

이벤트에 연결할 테스트 프로필을 정의하여 메시지를 미리 보고 관련 증명을 보낼 수 있습니다.

1. 다음에서 [트랜잭션 메시지 대시보드](../../channels/using/editing-transactional-message.md#accessing-transactional-messages)를 클릭하고 **[!UICONTROL Create test profile]** 단추를 클릭합니다.

   ![](assets/message-center_test-profile.png)

1. **[!UICONTROL Event data used for personalization]** 섹션에서 JSON 형식으로 전송할 정보를 지정합니다. 메시지를 미리 볼 때와 테스트 프로필에서 증명를 받을 때 사용할 콘텐츠입니다.

   ![](assets/message-center_event-data.png)

   >[!NOTE]
   >
   >메시지를 보강하는 경우 다음과 같은 다른 테이블과 관련된 정보를 입력할 수도 있습니다. **[!UICONTROL Profile]**. 다음을 참조하십시오 [이벤트 강화](../../channels/using/configuring-transactional-event.md#enriching-the-transactional-message-content) 및 [트랜잭션 메시지 개인화](../../channels/using/editing-transactional-message.md#personalizing-a-transactional-message).

1. 테스트 프로필이 만들어지면 트랜잭션 메시지에 미리 지정됩니다. 메시지의 **[!UICONTROL Test profiles]** 블록을 클릭하여 증명의 대상을 확인합니다.

   ![](assets/message-center_5.png)

새 테스트 프로필을 만들거나 **[!UICONTROL Test profiles]** 메뉴 아래의 제품에서 사용할 수 있습니다. 방법은 다음과 같습니다.

1. 다음을 클릭합니다. **Adobe** 로고, 왼쪽 상단 모서리에서 **[!UICONTROL Profiles & audiences]** > **[!UICONTROL Test profiles]**.
1. 다음에서 **[!UICONTROL Event]** 섹션에서 방금 만든 이벤트를 선택합니다. 예제에서는 &quot;장바구니 포기(EVTcartAbandonment)&quot;를 선택합니다.
1. **[!UICONTROL Event data]** 텍스트 상자에 JSON 형식으로 전송할 정보를 지정합니다.

   ![](assets/message-center_3.png)

1. 변경 내용을 저장합니다.
1. [메시지 액세스](../../channels/using/editing-transactional-message.md#accessing-transactional-messages) 을(를) 만들고 업데이트된 테스트 프로필을 선택합니다.

**관련 항목:**

* [테스트 프로필 관리](../../audiences/using/managing-test-profiles.md)
* [대상자 만들기](../../audiences/using/creating-audiences.md)

## 증명 보내기 {#sending-proof}

하나 이상의 특정 테스트 프로필을 만들고 트랜잭션 메시지를 저장하면 증명을 전송하여 테스트할 수 있습니다.

![](assets/message-center_10.png)

증명 전송 단계는 [증명 보내기](../../sending/using/sending-proofs.md) 섹션.
