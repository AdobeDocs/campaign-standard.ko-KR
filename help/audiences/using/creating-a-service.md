---
title: 서비스 만들기
seo-title: 서비스 만들기
description: 서비스 만들기
seo-description: 첫 번째 서비스를 만들고 구독자에게 이메일 확인을 보내도록 구성하는 방법을 알아봅니다.
page-status-flag: 활성화 안 함
uuid: 0d95d852-0f22-4b7b-b301-8fb4844c3ca2
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: 구독 관리
discoiquuid: 6b7788fe-fa6c-472a-97db-765595ce1589
context-tags: 서비스,마법사;서비스,주
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: da59fad19bcf35b63afdfc6389be527c27f21fc3

---


# 서비스 만들기{#creating-a-service}

구독을 관리하려면 먼저 서비스를 만들고 구성해야 합니다. 새 서비스를 구성하면 사용자가 서비스에 가입하거나 가입을 해지할 때 프로필에서 받을 이메일 확인을 지정할 수 있습니다. 또한 서비스에 연결된 구독 및 구독 취소 랜딩 페이지를 정의합니다. 예를 들어, 이메일에 삽입된 서비스 구독 링크는 자동으로 해당 서비스에 지정된 구독 랜딩 페이지로 프로필을 보냅니다.

서비스를 구성하려면:

1. 고급 메뉴 **[!UICONTROL Profiles & audiences]** &gt; **[!UICONTROL Services]** Adobe Campaign 로고를 통해 새 서비스를 추가하거나 기존 서비스를 선택합니다. 새 서비스를 만드는 경우 화면에 표시된 단계를 따르기만 하면 됩니다.

   기본 서비스 템플릿을 사용할 수 있습니다. 이 템플릿은 기본 랜딩 페이지와 확인 이메일로 미리 구성됩니다. 다른 템플릿을 만들어 특정 구성을 정의할 수 있습니다. 자세한 내용은 템플릿 [관리](../../start/using/about-templates.md) 섹션을 참조하십시오.

1. 서비스 **[!UICONTROL Service properties]** ![](assets/edit_darkgrey-24px.png) 대시보드의 단추를 통해 액세스하는 섹션에서 구독 및 가입 취소에 대한 확인 메시지를 구성합니다.

   ![](assets/lp_service_parameters.png)

1. 필드를 **[!UICONTROL Service label]** 채웁니다. 사용자 지정 확인 메시지를 사용하는 경우 서비스 레이블은 필수입니다.

1. 구독 및 가입 취소에 대한 확인 메시지 템플릿을 선택합니다. Three modes are available:

   * **[!UICONTROL No message]**: this mode allows you to create a service without a confirmation message.
   * **[!UICONTROL Default message]**: this mode will use the default subscription or unsubscription confirmation transactional message. The default confirmation messages are generic and will be the same for all services that use the default mode.

      >[NOTE]
      >
      >You can modify a default message by clicking its label in the  section or by selecting it from the Adobe Campaign transactional message list, after checking the  box.**[!UICONTROL Service properties]****[!UICONTROL Show internal transactional messages]**

   * **[!UICONTROL Custom message]**: this mode allows you to handle custom confirmation messages, specific for each service. You then select the **[!UICONTROL Custom subscription event configuration]** which is associated with a specific [transactional message](../../channels/using/about-transactional-messaging.md) template. For more on this, see Confirming subscription to a service.[](../../audiences/using/confirming-subscription-to-a-service.md)

1. Save the service. It is now ready to be used.

Once a service has been created, you can start promoting it.

**Related topics:**

* [Managing a service and subscriptions video](https://helpx.adobe.com/campaign/kt/acs/using/acs-services-and-subscriptions-feature-video-use.html)
* [Promoting a service](../../audiences/using/promoting-a-service.md)
* [가입자로 구성된 대상 만들기](../../audiences/using/creating-audiences.md#creating-list-audiences)
* [랜딩 페이지에서 서비스에 양식 연결](../../channels/using/designing-a-landing-page.md#linking-a-form-to-a-service)

