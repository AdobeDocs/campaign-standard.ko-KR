---
solution: Campaign Standard
product: campaign
title: Points of Interest 데이터로 Campaign 메시지 개인화
description: 관심 영역 데이터 통합을 통해 사용자의 위치를 기반으로 개인화된 메시지를 만드는 방법을 살펴볼 수 있습니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-analytics-for-mobile
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 10%

---


# Points of Interest 데이터로 Campaign 메시지 개인화{#personalizing-campaign-messages-with-point-of-interest-data}

Adobe Campaign에서는 모바일 애플리케이션 가입자로부터 수집한 관심 영역 데이터를 사용하여 이메일 같은 개인화된 마케팅 메시지를 보낼 수 있습니다.

표준 게재와 함께 관심 영역 데이터만 응답할 수 있습니다. [트랜잭션 메시지](../../channels/using/getting-started-with-transactional-msg.md) 는 위치 데이터를 사용할 수 없습니다.

여러분이 반응할 수 있는 가장 빠른 시간은 약 10분입니다.

이 경우, 지난 2주 이내에 보스턴 스토어를 방문한 모든 구독자에게 이메일을 전송하기로 결정할 수 있습니다.

1. 이메일 마케팅 활동을 만듭니다.
1. 배달 대상을 정의할 때 **[!UICONTROL Subscriptions to an application]** 요소를 작업 공간으로 드래그하여 놓습니다.

   ![](assets/poi_subscriptions_app.png)

   대상 관리는 [대상 정의](../../audiences/using/creating-audiences.md) 섹션에서 자세히 설명합니다.

1. **[!UICONTROL Add a rule - Profile/Subscriptions to an application]** 창에서 **[!UICONTROL POI Location Subscription]** 요소를 작업 공간으로 드래그하여 놓습니다.

   ![](assets/poi_add_rule_profile_subscription.png)

1. **[!UICONTROL Add a rule - POI Location Subscription]** 창에서 사용할 관심 영역의 레이블을 입력합니다.

   ![](assets/poi_location_subscription.png)

1. **[!UICONTROL Filter type]** 필드에서 **[!UICONTROL Relative]**&#x200B;을(를) 선택합니다.
1. **[!UICONTROL Preceding days]** 옵션을 선택하고 해당 필드에 **[!UICONTROL 15]**&#x200B;을 입력합니다.
1. 사용자가 관심 영역을 방문해야 하는 횟수를 정의합니다.
1. **[!UICONTROL Confirm]**&#x200B;을 클릭하여 대상을 저장합니다.

   ![](assets/poi_subscriptions_app_audience_defined.png)

1. 이메일에 컨텐츠를 추가합니다.

   ![](assets/poi_email_content.png)

1. 이메일 대시보드를 볼 활동 만들기를 확인합니다.
1. 메시지 전송

10% 할인 혜택을 제공하는 이메일은 다음과 같은 가입자에게 전송됩니다.

* 지난 2주 내에 최소한 한 번은 보스턴 스토어를 방문했어요.
* 방문 중에 모바일 응용 프로그램이 포그라운드에 적어도 한 번 이상 있었습니다.

**관련 항목:**

* [이메일 만들기](../../channels/using/creating-an-email.md)
* [컨텐츠 정의](../../designing/using/personalization.md#example-email-personalization)
* [메시지 보내기](../../sending/using/confirming-the-send.md)

