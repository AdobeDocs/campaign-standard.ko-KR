---
title: 트랜잭션 메시지 제한 사항
description: Adobe Campaign Standard의 트랜잭션 메시지에 대한 주요 제한 사항 및 권장 사항에 대해 알아봅니다.
page-status-flag: never-activated
uuid: b316bf47-7d98-46fa-ab4f-67ff50de8095
contentOwner: lemaitre
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: landing-pages
discoiquuid: ca8d1698-6e8a-4f5a-b017-74a152e14286
context-tags: landingPage,wizard;landingPage,overview;landingPage,main
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '640'
ht-degree: 88%

---


# 트랜잭션 메시지 제한 사항 {#transactional-messaging-limitations}

<img src="assets/do-not-localize/icon_concepts.svg" width="60px">

아래의 섹션에는 트랜잭션 메시지 작성을 시작하기 전에 알아야 할 제한 사항이 나와 있습니다.

구성 및 작성 방법을 포함한 트랜잭션 메시지에 대한 자세한 내용은 트랜잭션 메시지 [시작하기를 참조하십시오](../../channels/using/getting-started-with-transactional-msg.md).

>[!IMPORTANT]
>
>트랜잭션 메시지에 액세스하려면 관리 권한이 있어야 합니다.

## 디자인 및 게시 {#design-and-publication}

트랜잭션 메시지를 디자인 및 게시할 때 수행해야 하는 일부 단계는 되돌릴 수 없습니다. 다음 제한 사항을 알아 두어야 합니다.

* 각 이벤트 구성에 대해 채널은 하나씩만 사용할 수 있습니다. [이벤트 만들기](../../administration/using/configuring-transactional-messaging.md#creating-an-event)를 참조하십시오.
* 이벤트를 만든 후에는 채널을 변경할 수 없습니다. 따라서 메시지가 성공적으로 보내지지 않는 경우 워크플로우를 사용하여 다른 채널에서 메시지를 보낼 수 있는 메커니즘을 설계해야 합니다. [워크플로우 데이터 및 프로세스](../../automating/using/get-started-workflows.md)를 참조하십시오.
* 이벤트를 만든 후에는 타겟팅 차원(**[!UICONTROL Real-time event]** 또는 **[!UICONTROL Profile]**)을 변경할 수 없습니다. [이벤트 만들기](../../administration/using/configuring-transactional-messaging.md#creating-an-event)를 참조하십시오.
* 게시를 롤백할 수는 없지만, 이벤트를 게시 취소할 수는 있습니다. 이 작업을 수행하면 해당 이벤트와 관련 트랜잭션 메시지가 액세스할 수 없는 상태가 됩니다. [이벤트 게시 취소](../../administration/using/configuring-transactional-messaging.md#unpublishing-an-event)를 참조하십시오.
* 이벤트를 게시할 때 자동으로 만들어지는 트랜잭션 메시지만 해당 이벤트와 연결할 수 있습니다. [이벤트 미리 보기 및 게시](../../administration/using/configuring-transactional-messaging.md#previewing-and-publishing-the-event)를 참조하십시오.

## 개인화 {#personalization}

메시지 콘텐츠를 개인화할 수 있는 방법은 트랜잭션 메시지의 유형에 따라 다릅니다. 다음은 특정 목록입니다.

### 이벤트 기반 트랜잭션 메시지

* 이벤트 자체에 포함된 데이터에서 개인화 정보를 가져옵니다. [이벤트 트랜잭션 메시지](../../channels/using/event-transactional-messages.md)를 참조하십시오.
* You **cannot** use **[!UICONTROL Unsubscription link]** content blocks in an event transactional message.
* 이벤트 기반 트랜잭션 메시지는 보낸 이벤트에 있는 데이터만 사용하여 수신자와 메시지 콘텐츠 개인화를 정의합니다. 그러나 Adobe Campaign 데이터베이스의 정보를 사용하여 트랜잭션 메시지의 콘텐츠를 보강할 수 있습니다. [트랜잭션 메시지 콘텐츠 보강](../../administration/using/configuring-transactional-messaging.md#enriching-the-transactional-message-content)을 참조하십시오.
* 이벤트 트랜잭션 메시지에는 프로필 정보가 포함되어 있지 않기 때문에 피로도 규칙이 적용되지 않습니다. 프로필로 보강했을 경우에도 마찬가지입니다. [피로도 규칙](../../sending/using/fatigue-rules.md)을 참조하십시오.

### 프로필 기반 트랜잭션 메시지

* 이벤트에 포함된 데이터나 조정된 프로필 레코드에서 개인화 정보를 가져올 수 있습니다. [프로필 트랜잭션 메시지](../../channels/using/profile-transactional-messages.md)를 참조하십시오.
* You **can** use **[!UICONTROL Unsubscription link]** content blocks in a profile transactional message. [콘텐츠 블록 추가](../../designing/using/personalization.md#adding-a-content-block)를 참조하십시오.
* 프로필 트랜잭션 메시지의 경우 피로도 규칙이 적용됩니다. [피로도 규칙](../../sending/using/fatigue-rules.md)을 참조하십시오.

제품 목록은 트랜잭션 이메일 메시지에만 사용할 수 있습니다. [트랜잭션 메시지에서 제품 목록 사용](../../channels/using/event-transactional-messages.md#using-product-listings-in-a-transactional-message)을 참조하십시오.

## 권한 및 브랜딩 {#permissions-and-branding}

[브랜딩](../../administration/using/branding.md) 관리 측면에서 볼 때, 트랜잭션 메시지는 표준 메시지보다 유연성이 낮습니다. Adobe는 트랜잭션 메시지에 사용하는 모든 브랜드를 **[!UICONTROL All]** [ 조직 단위](../../administration/using/organizational-units.md)로 연결하는 것을 권장합니다. 자세한 내용은 아래 설명을 참조하십시오.

트랜잭션 메시지를 편집할 때 브랜드에 연결하여 브랜드 이름이나 브랜드 로고와 같은 일부 매개 변수를 자동으로 적용할 수 있습니다. 트랜잭션 메시지 속성에서 기본적으로 **[!UICONTROL Default brand]**&#x200B;이(가) 선택됩니다.

![](assets/message-center_branding.png)

트랜잭션 메시지에 사용하는 모든 개체(브랜딩 포함)는 **[!UICONTROL Message Center]** 조직 단위에서 볼 수 있어야 합니다. 즉, 이 개체는 **[!UICONTROL Message Center]** 또는 **[!UICONTROL All]** 조직 단위로 표시되어야 합니다.

하지만 메시지 속성에서 선택한 브랜드가 **[!UICONTROL Message Center]**&#x200B;나 **[!UICONTROL All]**&#x200B;와(과) 다른 조직 단위에 연결되어 있는 경우 오류가 발생하여 트랜잭션 메시지를 보낼 수 없습니다.

따라서 트랜잭션 메시지의 컨텍스트에서 다중 브랜딩을 사용하려면 모든 브랜드를 **[!UICONTROL Message Center]** 조직 단위나 **[!UICONTROL All]** 조직 단위에 연결해야 합니다.

## 트랜잭션 메시지 내보내기 및 가져오기 {#exporting-and-importing-transactional-messages}

* 트랜잭션 메시지를 내보내려면 [패키지 내보내기 만들기](../../automating/using/managing-packages.md#creating-a-package) 시 해당 이벤트 구성을 포함해야 합니다.
* 트랜잭션 메시지를 [패키지로 가져오기](../../automating/using/managing-packages.md#importing-a-package)하면 트랜잭션 메시지 목록에 표시되지 않습니다. 연결된 트랜잭션 메시지를 사용할 수 있게 하려면 해당 이벤트 구성을 [게시](../../administration/using/configuring-transactional-messaging.md#previewing-and-publishing-the-event)해야 합니다.
