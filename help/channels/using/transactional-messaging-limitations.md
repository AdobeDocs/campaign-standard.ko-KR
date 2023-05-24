---
title: 트랜잭션 메시지 제한 사항
description: Adobe Campaign Standard의 트랜잭션 메시지와 관련된 주요 권장 사항 및 제한 사항에 대해 알아봅니다.
audience: channels
content-type: reference
topic-tags: transactional-messaging
context-tags: null
feature: Transactional Messaging
role: User
level: Intermediate
exl-id: d6aaec6e-c718-46a2-88e8-7402970def1a
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 67%

---

# 트랜잭션 메시지 모범 사례 및 제한 사항 {#transactional-messaging-limitations}

<img src="assets/do-not-localize/icon_concepts.svg" width="60px">

이 섹션에는 트랜잭션 메시지 작성을 시작하기 전에 알아야 하는 모범 사례 및 제한 사항이 나와 있습니다.

<!--For more on transactional messages, including on how to configure and create them, see [Getting started with transactional messaging](../../channels/using/getting-started-with-transactional-msg.md).-->

## 사용 권한 {#permissions}

을(를) 가진 사용자만 [관리](../../administration/using/users-management.md#functional-administrators) 역할은 트랜잭션 이벤트를 구성하고 트랜잭션 메시지에 액세스할 수 있습니다.

## 이벤트 구성 및 게시 {#design-and-publication}

트랜잭션 이벤트를 구성하고 게시할 때 수행해야 하는 일부 단계는 되돌릴 수 없습니다. 다음 제한 사항을 알아 두어야 합니다.

* 트랜잭션 메시지에 사용할 수 있는 채널은 다음과 같습니다. **[!UICONTROL Email]**, **[!UICONTROL Mobile (SMS)]** 및 **[!UICONTROL Push notification]**.
* 각 이벤트 구성에 대해 채널은 하나씩만 사용할 수 있습니다. [이벤트 만들기](../../channels/using/configuring-transactional-event.md#creating-an-event)를 참조하십시오.
* 이벤트를 만든 후에는 채널을 변경할 수 없습니다. 따라서 메시지가 성공적으로 보내지지 않는 경우 워크플로우를 사용하여 다른 채널에서 메시지를 보낼 수 있는 메커니즘을 설계해야 합니다. [워크플로우 데이터 및 프로세스](../../automating/using/get-started-workflows.md)를 참조하십시오.
* 이벤트를 만든 후에는 타겟팅 차원(**[!UICONTROL Real-time event]** 또는 **[!UICONTROL Profile]**)을 변경할 수 없습니다. [이벤트 만들기](../../channels/using/configuring-transactional-event.md#creating-an-event)를 참조하십시오.
* 게시를 롤백할 수는 없지만, 이벤트를 게시 취소할 수는 있습니다. 이 작업을 수행하면 해당 이벤트와 관련 트랜잭션 메시지가 액세스할 수 없는 상태가 됩니다. [이벤트 게시 취소](../../channels/using/publishing-transactional-event.md#unpublishing-an-event)를 참조하십시오.
* 이벤트를 게시할 때 자동으로 만들어지는 트랜잭션 메시지만 해당 이벤트와 연결할 수 있습니다. [이벤트 미리 보기 및 게시](../../channels/using/publishing-transactional-event.md#previewing-and-publishing-the-event)를 참조하십시오.

## 트랜잭션 메시지 수 {#transactional-message-number}

게시된 트랜잭션 메시지의 수는 플랫폼에 중요한 영향을 줄 수 있습니다. 최적의 성능을 위해 게시된 트랜잭션 메시지 수는 100개 미만으로 유지되어야 합니다. 이를 보장하려면 사용하지 않은 트랜잭션 메시지의 게시를 취소하거나 삭제합니다. 다음을 참조하십시오 [트랜잭션 메시지 게시 취소](../../channels/using/publishing-transactional-message.md#unpublishing-a-transactional-message) 및 [트랜잭션 메시지 삭제](../../channels/using/publishing-transactional-message.md#deleting-a-transactional-message).

최상의 성능을 보장하기 위해 게시를 취소하거나 사용하지 않는 이벤트를 삭제할 수도 있습니다. 실제로, 이벤트 게시를 취소하거나 삭제하면 해당 트랜잭션 메시지와 해당 전송 및 추적 로그(있는 경우)도 게시 취소되거나 삭제됩니다. 다음을 참조하십시오 [이벤트 게시 취소](../../channels/using/publishing-transactional-event.md#unpublishing-an-event) 및 [이벤트 삭제](../../channels/using/publishing-transactional-event.md#deleting-an-event).

## 개인화 {#personalization}

메시지 콘텐츠를 개인화할 수 있는 방법은 트랜잭션 메시지의 유형에 따라 다릅니다. 구체적으로는 다음과 같습니다.

### 이벤트 기반 트랜잭션 메시지

* 이벤트 자체에 포함된 데이터에서 개인화 정보를 가져옵니다. 다음을 참조하십시오 [이벤트 기반 트랜잭션 메시지 구성](../../channels/using/configuring-transactional-event.md#event-based-transactional-messages).
* 본인 **할 수 없음** 사용 **[!UICONTROL Unsubscription link]** 이벤트 트랜잭션 메시지의 콘텐츠 블록입니다.
* 이벤트 기반 트랜잭션 메시지는 보낸 이벤트에 있는 데이터만 사용하여 수신자와 메시지 콘텐츠 개인화를 정의합니다. 그러나 Adobe Campaign 데이터베이스의 정보를 사용하여 트랜잭션 메시지의 콘텐츠를 보강할 수 있습니다. 다음을 참조하십시오 [이벤트 강화](../../channels/using/configuring-transactional-event.md#enriching-the-transactional-message-content) 및 [트랜잭션 메시지 개인화](../../channels/using/editing-transactional-message.md#personalizing-a-transactional-message).
* 이벤트 트랜잭션 메시지에는 프로필 정보가 포함되어 있지 않기 때문에 피로도 규칙이 적용되지 않습니다. 프로필로 보강했을 경우에도 마찬가지입니다.

### 프로필 기반 트랜잭션 메시지

* 이벤트에 포함된 데이터나 조정된 프로필 레코드에서 개인화 정보를 가져올 수 있습니다. 다음을 참조하십시오 [프로필 기반 트랜잭션 메시지 구성](../../channels/using/configuring-transactional-event.md#profile-based-transactional-messages) 및 [프로필 기반 트랜잭션 메시지 특성](../../channels/using/editing-transactional-message.md#profile-transactional-message-specificities).
* 본인 **can** 사용 **[!UICONTROL Unsubscription link]** 프로필 트랜잭션 메시지의 콘텐츠 블록입니다. [콘텐츠 블록 추가](../../designing/using/personalization.md#adding-a-content-block)를 참조하십시오.
* 프로필 트랜잭션 메시지의 경우 피로도 규칙이 적용됩니다. [피로도 규칙](../../sending/using/fatigue-rules.md)을 참조하십시오.

### 제품 목록

제품 목록은 트랜잭션에서 사용할 수 있습니다. **이메일 메시지** 만 해당. [트랜잭션 메시지에서 제품 목록 사용](../../designing/using/using-product-listings.md)을 참조하십시오.

## 브랜딩 {#permissions-and-branding}

[브랜딩](../../administration/using/branding.md) 관리 측면에서 볼 때, 트랜잭션 메시지는 표준 메시지보다 유연성이 낮습니다. Adobe는 트랜잭션 메시지에 사용하는 모든 브랜드를 **[!UICONTROL All]** [ 조직 단위](../../administration/using/organizational-units.md)로 연결하는 것을 권장합니다. 자세한 내용은 아래 설명을 참조하십시오.

트랜잭션 메시지를 편집할 때 브랜드에 연결하여 브랜드 이름이나 브랜드 로고와 같은 일부 매개 변수를 자동으로 적용할 수 있습니다. 트랜잭션 메시지 속성에서 기본적으로 **[!UICONTROL Default brand]**&#x200B;이(가) 선택됩니다.

![](assets/message-center_branding.png)

트랜잭션 메시지에 사용하는 모든 개체(브랜딩 포함)는 **[!UICONTROL Message Center]** 조직 단위에서 볼 수 있어야 합니다. 즉, 이 개체는 **[!UICONTROL Message Center]** 또는 **[!UICONTROL All]** 조직 단위로 표시되어야 합니다.

하지만 메시지 속성에서 선택한 브랜드가 **[!UICONTROL Message Center]**&#x200B;나 **[!UICONTROL All]**&#x200B;와(과) 다른 조직 단위에 연결되어 있는 경우 오류가 발생하여 트랜잭션 메시지를 보낼 수 없습니다.

따라서 트랜잭션 메시지의 컨텍스트에서 다중 브랜딩을 사용하려면 모든 브랜드를 **[!UICONTROL Message Center]** 조직 단위나 **[!UICONTROL All]** 조직 단위에 연결해야 합니다.

## 트랜잭션 메시지 내보내기 및 가져오기 {#exporting-and-importing-transactional-messages}

* 트랜잭션 메시지를 내보내려면 [패키지 내보내기 만들기](../../automating/using/managing-packages.md#creating-a-package) 시 해당 이벤트 구성을 포함해야 합니다.
* 트랜잭션 메시지를 [패키지로 가져오기](../../automating/using/managing-packages.md#importing-a-package)하면 트랜잭션 메시지 목록에 표시되지 않습니다. 연결된 트랜잭션 메시지를 사용할 수 있게 하려면 해당 이벤트 구성을 [게시](../../channels/using/publishing-transactional-event.md)해야 합니다.
