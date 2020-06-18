---
title: 프로필 트랜잭션 메시지
description: 프로필 트랜잭션 메시지를 만들고 게시하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: a8efe979-74ae-46ff-a305-b86a90679581
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: transactional-messaging
discoiquuid: dcb90afc-42c3-419e-8345-79cddf969e41
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 012546e109b085b7ed968bcefa8f76482656ae0d
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 2%

---


# 프로필 트랜잭션 메시지{#profile-transactional-messages}

고객 마케팅 프로필을 기반으로 트랜잭션 메시지를 전송할 수 있으므로 다음과 같은 작업을 수행할 수 있습니다.

* 마케팅 유형 규칙(예: **[!UICONTROL Address on block list]** 또는 [피로 규칙)을 적용합니다](../../sending/using/fatigue-rules.md).
* 메시지에 구독 취소 링크를 포함합니다.
* 트랜잭션 메시지를 전역 배달 보고에 추가합니다.
* 고객 여정의 트랜잭션 메시지 활용

이벤트를 만들고 게시하면(위의 [예와](../../channels/using/about-transactional-messaging.md#transactional-messaging-operating-principle) 같이 장바구니 포기) 해당 트랜잭션 메시지가 자동으로 생성됩니다.

구성 단계는 프로필 트랜잭션 메시지 [를 전송하기 위한 이벤트 구성 섹션에 나와 있습니다](../../administration/using/configuring-transactional-messaging.md#use-case--configuring-an-event-to-send-a-transactional-message) .

이벤트가 트랜잭션 메시지 전송을 트리거하려면 메시지를 개인화한 다음 테스트하여 게시해야 합니다.

>[!NOTE]
>
>트랜잭션 메시지에 액세스하려면 **[!UICONTROL Administrators (all units)]** 보안 그룹의 일부여야 합니다.
>
>피로 규칙은 프로파일 트랜잭션 메시지와 호환됩니다. 피로 [규칙을 참조하십시오](../../sending/using/fatigue-rules.md).

## 프로필 트랜잭션 메시지 보내기 {#sending-a-profile-transactional-message}

프로필 트랜잭션 메시지를 만들고, 개인화하고, 게시하는 단계는 이벤트 트랜잭션 메시지의 경우와 동일합니다. See [Event transactional messages](../../channels/using/event-transactional-messages.md).

차이점이 아래에 나와 있습니다.

1. 편집하기 위해 만든 트랜잭션 메시지로 이동합니다.
1. 트랜잭션 메시지에서 **[!UICONTROL Content]** 섹션을 클릭합니다. 트랜잭션 템플릿 외에 이메일 템플릿 타깃팅을 선택할 수도 있습니다 **[!UICONTROL Profile]**.

   ![](assets/message-center_marketing_templates.png)

1. 기본 이메일 템플릿을 선택합니다.

   모든 마케팅 이메일과 유사하게 구독 취소 링크가 포함되어 있습니다.

   ![](assets/message-center_marketing_perso_unsubscription.png)

   또한 실시간 이벤트 기반의 구성과 달리 모든 프로필 정보에 직접 액세스하여 메시지를 개인화할 수 있습니다. 개인화 [필드 삽입을 참조하십시오](../../designing/using/personalization.md#inserting-a-personalization-field).

1. 변경 내용을 저장하고 메시지를 게시합니다. 트랜잭션 메시지 [게시를 참조하십시오](../../channels/using/event-transactional-messages.md#publishing-a-transactional-message).

## 프로필 트랜잭션 메시지 전달 모니터링 {#monitoring-a-profile-transactional-message-delivery}

메시지가 게시되고 사이트 통합이 완료되면 배달을 모니터링할 수 있습니다.

1. 메시지 배달 로그를 보려면 **[!UICONTROL Deployment]** 블록의 오른쪽 하단에 있는 아이콘을 클릭합니다.

   로그 액세스에 대한 자세한 내용은 배달 [모니터링을 참조하십시오](../../sending/using/monitoring-a-delivery.md).

1. 탭을 **[!UICONTROL Sending logs]** 선택합니다. 열에서 **[!UICONTROL Status]** 프로필 **[!UICONTROL Sent]** 이 선택되었음을 나타냅니다.

   ![](assets/message-center_marketing_sending_logs.png)

1. 차단 목록의 주소와 같이 메시지 대상에서 제외된 수신자를 보려면 **[!UICONTROL Exclusions logs]** 탭을 선택합니다.

   ![](assets/message-center_marketing_exclusion_logs.png)

옵트아웃한 모든 프로파일의 경우, Typical **[!UICONTROL Address on block list]** 규칙은 해당 수신자를 제외합니다.

이 규칙은 테이블을 기반으로 모든 트랜잭션 메시지에 적용되는 특정 유형 **[!UICONTROL Profile]** 의 일부입니다.

![](assets/message-center_marketing_typology.png)

**관련 항목**:

* [사이트 통합](../../administration/using/configuring-transactional-messaging.md#integrating-the-triggering-of-the-event-in-a-website)
* [유형 지정](../../sending/using/about-typology-rules.md)

