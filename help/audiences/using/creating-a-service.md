---
title: 서비스 만들기
description: 첫 번째 서비스를 만들고 구독자에게 이메일 확인을 보내도록 구성하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: 0d95d852-0f22-4b7b-b301-8fb4844c3ca2
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: managing-subscriptions
discoiquuid: 6b7788fe-fa6c-472a-97db-765595ce1589
context-tags: service,wizard;service,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: a8ee3b864b6916871711c6bd2e2d3b794bc706f8

---


# 서비스 만들기{#creating-a-service}

구독을 관리하려면 먼저 서비스를 만들고 구성해야 합니다. 새 서비스를 구성하면 사용자가 서비스에 가입하거나 가입을 해지할 때 프로필에서 받을 이메일 확인을 지정할 수 있습니다. 또한 서비스에 연결된 구독 및 구독 취소 랜딩 페이지를 정의합니다. 예를 들어, 이메일에 삽입된 서비스 구독 링크는 자동으로 해당 서비스에 지정된 구독 랜딩 페이지로 프로필을 보냅니다.

서비스를 구성하려면:

1. 고급 메뉴 **[!UICONTROL Profiles & audiences]**>**[!UICONTROL Services]** Adobe Campaign 로고를 통해 새 서비스를 추가하거나 기존 서비스를 선택합니다. 새 서비스를 만드는 경우 화면에 표시된 단계를 따르기만 하면 됩니다.

   기본 서비스 템플릿을 사용할 수 있습니다. 이 템플릿은 기본 랜딩 페이지와 확인 이메일로 미리 구성됩니다. 다른 템플릿을 만들어 특정 구성을 정의할 수 있습니다. 자세한 내용은 템플릿 [관리](../../start/using/marketing-activity-templates.md) 섹션을 참조하십시오.

1. 서비스 **[!UICONTROL Service properties]**![](assets/edit_darkgrey-24px.png)대시보드의 단추를 통해 액세스하는 섹션에서 구독 및 가입 취소에 대한 확인 메시지를 구성합니다.

   ![](assets/lp_service_parameters.png)

1. 사용료 지불 옵션의 유효 기간을 설정하려면 이 **[!UICONTROL Subscriptions with an expiration date]**옵션을 선택합니다.

   ![](assets/lp_service_expiration.png)

   세그먼테이션 활동의 만료 날짜를 사용하여 만료되지 않은 서비스에 가입한 프로파일을 타깃팅할 수 있습니다.

1. 필드를 **[!UICONTROL Service label]**채웁니다. 사용자 지정 확인 메시지를 사용하는 경우 서비스 레이블은 필수입니다.

1. 구독 및 가입 취소에 대한 확인 메시지 템플릿을 선택합니다. 다음 세 가지 모드를 사용할 수 있습니다.

   * **[!UICONTROL No message]**:이 모드에서는 확인 메시지 없이 서비스를 만들 수 있습니다.
   * **[!UICONTROL Default message]**:이 모드는 기본 구독 또는 구독 취소 확인 트랜잭션 메시지를 사용합니다. 기본 확인 메시지는 일반적이며 기본 모드를 사용하는 모든 서비스에 대해 동일합니다.

      >[!NOTE]
      >
      >확인란을 선택한 후 **[!UICONTROL Service properties]**섹션에서 해당 레이블을 클릭하거나 Adobe Campaign 트랜잭션 메시지 목록에서 선택하여 기본 메시지를 수정할 수**[!UICONTROL Show internal transactional messages]** 있습니다.

   * **[!UICONTROL Custom message]**:이 모드에서는 각 서비스별 사용자 지정 확인 메시지를 처리할 수 있습니다. 그런 다음 특정**[!UICONTROL Custom subscription event configuration]** 거래 메시지 [](../../channels/using/about-transactional-messaging.md) 템플릿과 연결된 항목을 선택합니다. 자세한 내용은 서비스 [가입](../../audiences/using/confirming-subscription-to-a-service.md)확인을 참조하십시오.

1. 서비스를 저장합니다. 이제 사용할 준비가 되었습니다.

서비스가 만들어지면 홍보를 시작할 수 있습니다.

**관련 항목:**

* [서비스 및 구독](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/profiles-and-audiences/services-and-subscriptions.html) 관리 비디오
* [서비스 홍보](../../audiences/using/promoting-a-service.md)
* [가입자로 구성된 대상 만들기](../../audiences/using/creating-audiences.md#creating-list-audiences)
* [랜딩 페이지를 서비스에 연결](../../channels/using/configuring-landing-page.md#linking-a-landing-page-to-a-service)
