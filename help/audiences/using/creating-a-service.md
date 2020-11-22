---
solution: Campaign Standard
product: campaign
title: 서비스 만들기
description: 첫 번째 서비스를 만들고 구독자에게 확인 이메일을 보내도록 구성하는 방법을 알아봅니다.
audience: audiences
content-type: reference
topic-tags: managing-subscriptions
context-tags: service,wizard;service,main
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 100%

---


# 서비스 만들기{#creating-a-service}

구독을 관리하려면 먼저 서비스를 만들고 구성해야 합니다. 새 서비스를 구성하면 프로필이 서비스를 구독하거나 구독을 취소할 때 받을 확인 이메일을 지정할 수 있습니다. 또한 서비스에 연결된 구독 및 구독 취소 랜딩 페이지를 정의할 수 있습니다. 예를 들어, 이메일에 삽입된 서비스 구독 링크는 프로필을 자동으로 해당 서비스에 지정된 구독 랜딩 페이지로 보냅니다.

서비스를 구성하려면 다음을 수행합니다. 

1. Adobe Campaign 로고를 통해 고급 메뉴 **[!UICONTROL Profiles & audiences]** > **[!UICONTROL Services]**&#x200B;에서 새 서비스를 추가하거나 기존 서비스를 선택합니다. 새 서비스를 만드는 경우 화면에 표시된 단계를 따르기만 하면 됩니다.

   기본 제공 서비스 템플릿을 사용할 수 있습니다. 이 템플릿은 기본 랜딩 페이지와 확인 이메일로 사전 구성되어 있습니다. 다른 템플릿을 만들어 구체적인 구성을 정의할 수 있습니다. 자세한 내용은 [템플릿 관리](../../start/using/marketing-activity-templates.md) 섹션을 참조하십시오.

1. 서비스 대시보드의 ![](assets/edit_darkgrey-24px.png) 버튼을 통해 액세스할 수 있는 **[!UICONTROL Service properties]** 섹션에서 구독 및 구독 취소에 대한 확인 메시지를 구성합니다.

   ![](assets/lp_service_parameters.png)

1. 구독 유효 기간을 설정하려면 **[!UICONTROL Subscriptions with an expiration date]** 옵션을 선택합니다.

   ![](assets/lp_service_expiration.png)

   세분화 활동에서 만료 날짜를 사용하여 만료되지 않은 서비스를 구독하는 프로필을 타겟팅할 수 있습니다.

1. **[!UICONTROL Service label]** 필드를 입력합니다. 사용자 정의 확인 메시지를 사용하는 경우 서비스 레이블은 필수입니다.

1. 구독 및 구독 취소에 대한 확인 메시지 템플릿을 선택합니다. 다음 세 가지 모드를 사용할 수 있습니다.

   * **[!UICONTROL No message]**: 이 모드에서는 확인 메시지가 없는 서비스를 만들 수 있습니다.
   * **[!UICONTROL Default message]**: 이 모드에서는 기본 구독 또는 구독 취소 확인 트랜잭션 메시지가 사용됩니다. 기본 확인 메시지는 일반적인 메시지로, 기본 모드를 사용하는 모든 서비스에 대해 동일합니다.

      >[!NOTE]
      >
      >기본 메시지를 수정하려면 **[!UICONTROL Show internal transactional messages]** 상자를 선택한 후 해당 레이블을 **[!UICONTROL Service properties]** 섹션에서 클릭하거나 Adobe Campaign 트랜잭션 메시지 목록에서 선택합니다.

   * **[!UICONTROL Custom message]**: 이 모드에서는 각 서비스의 사용자 정의 확인 메시지를 처리할 수 있습니다. 그 다음 [트랜잭션 메시지](../../channels/using/getting-started-with-transactional-msg.md) 템플릿에 연결된 **[!UICONTROL Custom subscription event configuration]**&#x200B;을(를) 선택합니다. 자세한 내용은 [서비스 구독 확인](../../audiences/using/confirming-subscription-to-a-service.md)을 참조하십시오.

1. 서비스를 저장합니다. 이제 사용할 준비가 되었습니다.

서비스를 만들고 나면 홍보를 시작할 수 있습니다.

**관련 항목:**

* [서비스 및 구독 관리](https://docs.adobe.com/content/help/ko-KR/campaign-standard-learn/tutorials/profiles-and-audiences/services-and-subscriptions.html) 비디오
* [서비스 홍보](../../audiences/using/promoting-a-service.md)
* [구독자로 구성된 대상자 만들기](../../audiences/using/creating-audiences.md#creating-list-audiences)
* [랜딩 페이지를 서비스에 연결](../../channels/using/configuring-landing-page.md#linking-a-landing-page-to-a-service)
