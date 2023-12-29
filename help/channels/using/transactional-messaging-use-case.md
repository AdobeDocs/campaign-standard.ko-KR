---
title: 트랜잭션 메시지 사용 사례
description: Adobe Campaign 트랜잭션 메시지 기능에 대한 전체적인 예제를 살펴봅니다.
audience: channels
content-type: reference
topic-tags: transactional-messaging
context-tags: null
feature: Transactional Messaging
role: User
level: Intermediate
exl-id: ee1a9705-4c21-4d46-a178-fde2e059f443
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 4%

---

# 트랜잭션 메시지 사용 사례 {#transactional-messaging-use-case}

이 예에서는 Adobe Campaign 트랜잭션 메시지 기능을 사용하여 웹 사이트에서 각 구매 후 CRM ID를 통해 고객을 식별하는 확인 이메일을 보내려고 합니다.

전제 조건은 다음과 같습니다.

* 다음을 확인하십시오. **[!UICONTROL Profile]** 리소스가 CRM ID에 해당하는 새 필드로 확장되었습니다.

* 구매에 해당하는 사용자 지정 리소스를 만들고 게시하여 **[!UICONTROL Profile]** 리소스. 이렇게 하면 이 리소스에서 정보를 검색하여 메시지 콘텐츠를 보강할 수 있습니다.

리소스 확장, 만들기 및 게시에 대한 자세한 내용은 [이 섹션](../../developing/using/key-steps-to-add-a-resource.md).

이 사용 사례를 구현하는 주요 단계는 아래에 나와 있습니다.

>[!NOTE]
>
>트랜잭션 메시지 일반 프로세스의 그래픽 표현은 다음을 참조하십시오. [이 스키마](../../channels/using/getting-started-with-transactional-msg.md#key-steps).

## 1단계 - 이벤트 구성 만들기 및 게시 {#create-event-configuration}

1. 를 사용하여 새 이벤트 만들기 **[!UICONTROL Email]** 채널. [이벤트 만들기](../../channels/using/configuring-transactional-event.md#creating-an-event)를 참조하십시오.

1. 다음 항목 선택 **[!UICONTROL Profile]** 생성할 차원 타겟팅 [프로필 기반 트랜잭션 메시지](../../channels/using/configuring-transactional-event.md#profile-based-transactional-messages).

1. 트랜잭션 메시지를 개인화하는 데 사용할 수 있는 특성을 정의합니다. 이 예에서는 &quot;CRM ID&quot; 및 &quot;제품 식별자&quot; 필드를 추가합니다. 다음을 참조하십시오 [이벤트 속성 정의](../../channels/using/configuring-transactional-event.md#defining-the-event-attributes).

   ![](assets/message-center_usecase1.png)

1. 고객의 구매에 대한 정보로 메시지 콘텐츠를 보강하려면 다음을 타깃팅하는 데이터 보강 을 만듭니다. **[!UICONTROL Purchase]** 리소스. 다음을 참조하십시오 [이벤트 강화](../../channels/using/configuring-transactional-event.md#enriching-the-transactional-message-content).

   ![](assets/message-center_usecase2.png)

1. 이벤트에 이전에 추가한 &quot;제품 식별자&quot; 필드와 의 해당 필드 사이에 조인 조건을 만듭니다. **[!UICONTROL Purchase]** 리소스.

   ![](assets/message-center_usecase3.png)

1. 프로필 기반 이벤트에는 필수이므로, 다음을 타겟팅하는 데이터 보강 또한 만들어야 합니다. **[!UICONTROL Profile]** 리소스.

1. 메시지에 이전에 추가한 &quot;CRM ID&quot; 필드와 의 해당 필드 사이에 조인 조건을 만듭니다. **[!UICONTROL Profile]** 확장한 리소스입니다. <!--What's the purpose to have created a CRM ID for this event and to have the CRM ID as a join condition? could it be any other field provided you created it in the event?-->

   ![](assets/message-center_usecase4.png)

1. 다음에서 **[!UICONTROL Targeting enrichment]** 섹션에서 데이터 보강 **[!UICONTROL Profile]** 게재 실행 중 메시지 대상으로 사용되는 리소스.

   ![](assets/message-center_usecase5.png)

1. 이벤트를 미리 보고 게시합니다. [이벤트 미리 보기 및 게시](../../channels/using/publishing-transactional-event.md#previewing-and-publishing-the-event)를 참조하십시오.

## 2단계 - 트랜잭션 메시지 편집 및 게시 {#create-transactional-message}

1. 이벤트를 게시할 때 자동으로 생성된 트랜잭션 메시지로 이동합니다. 다음을 참조하십시오 [트랜잭션 메시지 액세스](../../channels/using/editing-transactional-message.md#accessing-transactional-messages).

1. 메시지를 편집하고 개인화합니다. 다음을 참조하십시오 [프로필 트랜잭션 메시지 편집](../../channels/using/editing-transactional-message.md#editing-profile-transactional-message).

1. 에 추가한 &quot;CRM ID&quot; 필드와의 조정을 통해 **[!UICONTROL Profile]** 리소스, 모든 프로필 정보에 대한 직접 액세스 권한이 있습니다. [개인화](../../designing/using/personalization.md#inserting-a-personalization-field) 메시지.

   ![](assets/message-center_usecase6.png)

1. &quot;제품 식별자&quot; 필드와의 조정을 통해 의 필드를 추가하여 고객의 구매 관련 정보로 메시지 콘텐츠를 보강할 수 있습니다. **[!UICONTROL Purchase]** 리소스.

   ![](assets/message-center_usecase7.png)

   이렇게 하려면 다음을 선택합니다. **[!UICONTROL Insert personalization field]** 상황별 도구 모음에서 작성합니다. 다음에서 **[!UICONTROL Context]** > **[!UICONTROL Transactional event]** > **[!UICONTROL Event context]** 노드, 다음에 해당하는 노드를 엽니다. **[!UICONTROL Purchase]** 사용자 지정 리소스 및 임의의 필드 선택.

1. 특정 테스트 프로필을 사용하여 메시지를 테스트할 수 있습니다. 다음을 참조하십시오 [트랜잭션 메시지 테스트](../../channels/using/testing-transactional-message.md#testing-a-transactional-message).

1. 콘텐츠가 준비되면 변경 사항을 저장하고 메시지를 게시합니다. [트랜잭션 메시지 게시](../../channels/using/publishing-transactional-message.md#publishing-a-transactional-message)를 참조하십시오.

## 3단계 - 이벤트 트리거 통합 {#integrate-event-trigger}

이벤트를 웹 사이트에 통합합니다. 다음을 참조하십시오 [이벤트 트리거 통합](../../channels/using/getting-started-with-transactional-msg.md#integrate-event-trigger).

## 4단계 - 메시지 게재 {#message-delivery}

이 단계를 모두 완료하면 고객이 웹 사이트에서 제품을 구입하는 즉시 구매에 대한 정보를 포함하는 개인화된 확인 이메일을 받게 됩니다.
