---
title: Points of Interest 데이터로 Campaign 메시지 개인화
description: 관심 영역 데이터 통합을 통해 고객의 위치를 기반으로 개인화된 메시지를 만드는 방법을 살펴볼 수 있습니다.
page-status-flag: never-activated
uuid: d74c3e55-f130-441b-bc2a-06ddcd5d9784
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-analytics-for-mobile
discoiquuid: a1736ba3-5121-4d01-bf04-ebb7e701e2e0
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 10%

---


# Points of Interest 데이터로 Campaign 메시지 개인화{#personalizing-campaign-messages-with-point-of-interest-data}

Adobe Campaign에서는 모바일 애플리케이션 가입자로부터 수집한 관심 영역 데이터를 사용하여 이메일 같은 개인화된 마케팅 메시지를 보낼 수 있습니다.

표준 게재와 함께 관심 영역 데이터만 응답할 수 있습니다. [트랜잭션 메시지는](../../channels/using/getting-started-with-transactional-msg.md) 위치 데이터를 사용할 수 없습니다.

여러분이 반응할 수 있는 가장 빠른 시간은 약 10분입니다.

이 경우, 귀하는 지난 2주 이내에 보스턴 스토어를 방문한 모든 가입자에게 이메일을 보내기로 결정할 것입니다.

1. 이메일 마케팅 활동을 만듭니다.
1. 전달 대상을 정의할 때 요소를 작업 공간으로 드래그하여 **[!UICONTROL Subscriptions to an application]** 놓습니다.

   ![](assets/poi_subscriptions_app.png)

   대상자 관리는 대상 [정의](../../audiences/using/creating-audiences.md) 섹션에서 자세히 설명합니다.

1. In the **[!UICONTROL Add a rule - Profile/Subscriptions to an application]** window, drag and drop the **[!UICONTROL POI Location Subscription]** element into the workspace.

   ![](assets/poi_add_rule_profile_subscription.png)

1. 창에 사용할 관심 영역의 레이블을 **[!UICONTROL Add a rule - POI Location Subscription]** 입력합니다.

   ![](assets/poi_location_subscription.png)

1. **[!UICONTROL Filter type]** 필드에서 **[!UICONTROL Relative]**&#x200B;을(를) 선택합니다.
1. 옵션을 **[!UICONTROL Preceding days]** 선택하고 해당 필드 **[!UICONTROL 15]** 에 입력합니다.
1. 사용자가 관심 영역을 방문한 횟수를 정의합니다.
1. Click **[!UICONTROL Confirm]** to save your audience.

   ![](assets/poi_subscriptions_app_audience_defined.png)

1. 이메일에 컨텐츠 추가

   ![](assets/poi_email_content.png)

1. 이메일 대시보드를 볼 활동 만들기를 확인합니다.
1. 메시지 전송

10% 할인 혜택이 포함된 이메일은 다음과 같은 가입자에게 발송됩니다.

* 지난 2주 내에 최소한 한 번은 보스턴 스토어를 방문했어요.
* 방문 중에 모바일 응용 프로그램이 포그라운드에 적어도 한 번 이상 있었던 경우.

**관련 항목:**

* [이메일 만들기](../../channels/using/creating-an-email.md)
* [컨텐츠 정의](../../designing/using/personalization.md#example-email-personalization)
* [메시지 보내기](../../sending/using/confirming-the-send.md)

