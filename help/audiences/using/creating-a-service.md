---
title: 서비스 만들기
seo-title: 서비스 만들기
description: 서비스 만들기
seo-description: 첫 번째 서비스를 만들고 가입자에게 이메일 확인을 보내도록 구성하는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: 0 D 95 D 852-0 F 22-4 B 7 B-B 301-8 FB 4844 C 3 CA 2
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 대상
content-type: 참조
topic-tags: 관리 구독
discoiquuid: 6 b 7788 FE-FA 6 c -472 a -97 DB -765595 CE 1589
context-tags: 서비스, 마법사; service, main
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 6a877d878f01fa1e541dc20b8b0941602113d15b

---


# Creating a service{#creating-a-service}

구독을 관리하려면 먼저 서비스를 만들고 구성해야 합니다. 새 서비스를 구성하면 서비스에서 구독하거나 가입을 해지하면 받게 될 이메일 확인을 지정할 수 있습니다. 또한 서비스에 연결된 가입 및 가입 해지 랜딩 페이지를 정의합니다. 예를 들어 이메일에 삽입된 서비스 구독 링크는 자동으로 프로필에 지정된 구독 랜딩 페이지로 프로필을 보냅니다.

서비스를 구성하려면:

1. From the advanced menu **Profiles &amp; audiences** &gt; **Services** via the Adobe Campaign logo, add a new service or select an existing service. 새 서비스를 만드는 경우 화면에 표시된 단계를 따르십시오.

   기본 서비스 템플릿을 사용할 수 있습니다. 이 템플릿은 기본 랜딩 페이지와 확인 이메일로 미리 구성되어 있습니다. 다른 템플릿을 만들어 특정 구성을 정의할 수 있습니다. For more on this, refer to the [Managing templates](../../start/using/about-templates.md) section.

1. In the **Service properties** section, accessed via the ![](assets/edit_darkgrey-24px.png) button in the service dashboard, configure the confirmation messages for subscriptions and unsubscriptions.

   ![](assets/lp_service_parameters.png)

1. 구독 및 구독 취소에 대한 확인 메시지 템플릿을 선택합니다. 다음 세 가지 모드를 사용할 수 있습니다.

   * **[!UICONTROL No message]**: 이 모드에서는 확인 메시지 없이 서비스를 만들 수 있습니다.
   * **[!UICONTROL Default message]**: 이 모드에서는 기본 구독 또는 구독 취소 확인 트랜잭션 메시지가 사용됩니다. 기본 확인 메시지는 일반적이며 기본 모드를 사용하는 모든 서비스에 대해 동일합니다.
   * **[!UICONTROL Custom message]**: 이 모드에서는 각 서비스에 대한 사용자 정의 확인 메시지를 처리할 수 있습니다. You then select the **[!UICONTROL Custom subscription event configuration]** which is associated with a specific transactional message template. Refer to [Transactional messages](../../channels/using/about-transactional-messaging.md) for more information on transactional event and message configuration.

1. 서비스를 저장합니다. 이제 사용할 준비가 되었습니다.

서비스가 만들어지면 홍보할 수 있습니다.

**관련 항목:**

* [서비스 및 구독](https://helpx.adobe.com/campaign/kt/acs/using/acs-services-and-subscriptions-feature-video-use.html) 비디오 관리
* [서비스 홍보](../../audiences/using/promoting-a-service.md)
* [가입자로 대상 만들기](../../audiences/using/creating-audiences.md#creating-list-audiences)
* [랜딩 페이지에서 서비스에 양식 연결](../../channels/using/designing-a-landing-page.md#linking-a-form-to-a-service)

