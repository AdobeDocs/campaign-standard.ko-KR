---
title: 트랜잭션 메시지 프로파일링
seo-title: 트랜잭션 메시지 프로파일링
description: 트랜잭션 메시지 프로파일링
seo-description: 프로필 트랜잭션 메시지를 만들고 게시하는 방법에 대해 알아봅니다.
page-status-flag: 활성화 안 함
uuid: a8efe979-74ae-46ff-a305-b86a90679581
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 채널
content-type: reference
topic-tags: 트랜잭션 메시지
discoiquuid: dcb90afc-42c3-419e-8345-79cddf969e41
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: d9357481a567cb0d11eea43211abf08a6dcb07d6

---


# 트랜잭션 메시지 프로파일링{#profile-transactional-messages}

고객 마케팅 프로필을 기반으로 트랜잭션 메시지를 전송할 수 있으므로 다음과 같은 작업을 수행할 수 있습니다.

* 마케팅 유형 규칙(예: **[!UICONTROL Blacklisted address]** 또는 [피로 규칙](../../administration/using/fatigue-rules.md))을 적용합니다.
* 메시지 내에 구독 취소 링크를 포함합니다.
* 트랜잭션 메시지를 전역 배달 보고에 추가합니다.
* 고객 여정의 트랜잭션 메시지 활용

이벤트를 만들고 게시하면(위의 [예제에](../../channels/using/about-transactional-messaging.md#transactional-messaging-operating-principle) 따라 장바구니 포기) 해당 트랜잭션 메시지가 자동으로 생성됩니다.

구성 단계는 프로필 트랜잭션 메시지를 [보낼 이벤트 구성](../../administration/using/configuring-transactional-messaging.md#use-case--configuring-an-event-to-send-a-transactional-message) 섹션에 나와 있습니다.

이벤트가 트랜잭션 메시지 전송을 트리거하려면 메시지를 개인화한 다음 테스트하여 게시해야 합니다.

>[!NOTE]
>
>트랜잭션 메시지에 액세스하려면 관리 권한이 있거나 **[!UICONTROL Message Center agents]** (mcExec) 보안 그룹에 표시되어야 합니다. 피로 규칙은 프로필 트랜잭션 메시지와 호환됩니다. 피로 [규칙을](../../administration/using/fatigue-rules.md)참조하십시오.

## 프로필 트랜잭션 메시지 보내기 {#sending-a-profile-transactional-message}

프로필 트랜잭션 메시지를 만들고, 개인화하고, 게시하기 위한 단계는 이벤트 트랜잭션 메시지의 경우와 동일합니다. 이벤트 [트랜잭션 메시지를](../../channels/using/event-transactional-messages.md)참조하십시오.

차이점이 아래에 나와 있습니다.

1. 편집하기 위해 만든 트랜잭션 메시지로 이동합니다.
1. 트랜잭션 메시지에서 **[!UICONTROL Content]** 섹션을 클릭합니다. 트랜잭션 템플릿 외에 이메일 템플릿 타깃팅을 선택할 수도 **[!UICONTROL Profile]**&#x200B;있습니다.

   ![](assets/message-center_marketing_templates.png)

1. 기본 이메일 템플릿을 선택합니다.

   모든 마케팅 이메일과 유사하게 구독 취소 링크가 포함되어 있습니다.

   ![](assets/message-center_marketing_perso_unsubscription.png)

   또한 실시간 이벤트를 기반으로 하는 구성과 달리 모든 프로필 정보에 직접 액세스하여 메시지를 개인화할 수 있습니다. 개인화 [필드](../../designing/using/personalization.md#inserting-a-personalization-field)삽입을 참조하십시오.

1. 변경 내용을 저장하고 메시지를 게시합니다. 트랜잭션 [메시지](../../channels/using/event-transactional-messages.md#publishing-a-transactional-message)게시를 참조하십시오.

## 프로필 트랜잭션 메시지 전달 모니터링 {#monitoring-a-profile-transactional-message-delivery}

메시지가 게시되고 사이트 통합이 완료되면 배달을 모니터링할 수 있습니다.

1. 메시지 배달 로그를 보려면 **[!UICONTROL Deployment]** 블록의 오른쪽 하단에 있는 아이콘을 클릭합니다.

   로그 액세스에 대한 자세한 내용은 배달 [모니터링을](../../sending/using/monitoring-a-delivery.md)참조하십시오.

1. 탭을 **[!UICONTROL Sending logs]** 선택합니다. 이 **[!UICONTROL Status]** 열에서, **[!UICONTROL Sent]** 프로필이 선택되었음을 나타냅니다.

   ![](assets/message-center_marketing_sending_logs.png)

1. 블랙리스트에 추가된 주소와 같이 메시지 대상에서 제외된 수신자를 보려면 이 **[!UICONTROL Exclusions logs]** 탭을 선택합니다.

   ![](assets/message-center_marketing_exclusion_logs.png)

옵트아웃한 모든 프로필의 경우 Typical **[!UICONTROL Blacklisted address]** 규칙은 해당 수신자를 제외했습니다.

이 규칙은 **[!UICONTROL Profile]** 테이블을 기반으로 하는 모든 트랜잭션 메시지에 적용되는 특정 유형 중 하나입니다.

![](assets/message-center_marketing_typology.png)

**관련 항목**:

* [사이트 통합](../../administration/using/configuring-transactional-messaging.md#integrating-the-triggering-of-the-event-in-a-website)
* [유형 지정](../../administration/using/about-typology-rules.md)

