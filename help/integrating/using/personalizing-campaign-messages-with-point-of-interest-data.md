---
title: 관심 영역 데이터와 캠페인 메시지 개인화
seo-title: 관심 영역 데이터와 캠페인 메시지 개인화
description: 관심 영역 데이터와 캠페인 메시지 개인화
seo-description: 관심 영역 데이터 통합으로 가입자의 위치를 기반으로 개인화된 메시지를 만드는 방법을 살펴볼 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: d 74 c 3 e 55-f 130-441 b-bc 2 a -06 ddcd 5 d 9784
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 통합
content-type: 참조
topic-tags: working-with-campaign-and-analytics-for-mobile
discoiquuid: A 1736 BA 3-5121-4 D 01-BF 04-EBB 7 E 701 E 2 E 0
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 698466596fdacd005dc4d72b8071208c8c39f77d

---


# Personalizing Campaign messages with Point of Interest data{#personalizing-campaign-messages-with-point-of-interest-data}

Adobe Campaign 에서는 모바일 애플리케이션의 구독자로부터 수집한 관심 영역 데이터를 사용하여 이메일과 같은 개인화된 마케팅 메시지를 보낼 수 있습니다.

표준 배달을 통해 관심 영역 데이터에만 반응할 수 있습니다. [트랜잭션 메시지는](../../channels/using/about-transactional-messaging.md) 위치 데이터를 사용할 수 없습니다.

가장 빨리 반응할 수 있는 시간은 약 10 분입니다.

이 경우 지난 2 주 내에 보스톤 스토어를 방문한 모든 가입자에게 이메일을 전송하기로 결정했습니다.

1. 이메일 마케팅 활동 만들기를 참조하십시오.
1. When defining the delivery's audience, drag and drop the **[!UICONTROL Subscriptions to an application]** element into the workspace.

   ![](assets/poi_subscriptions_app.png)

   Managing audiences is detailed in the [Defining audiences](../../audiences/using/creating-audiences.md) section.

1. **[!UICONTROL Add a rule - Profile/Subscriptions to an application]** 창에서 **[!UICONTROL POI Location Subscription]** 요소를 드래그하여 작업 공간으로 놓습니다.

   ![](assets/poi_add_rule_profile_subscription.png)

1. In the **[!UICONTROL Add a rule - POI Location Subscription]** window, enter the label of the Point of Interest that you want to use.

   ![](assets/poi_location_subscription.png)

1. **[!UICONTROL Filter type]** 필드에서 **[!UICONTROL Relative]**&#x200B;를 선택합니다.
1. **[!UICONTROL Preceding days]** 옵션을 확인하고 해당 **[!UICONTROL 15]** 필드에 입력합니다.
1. 사용자가 관심 영역을 방문한 횟수를 정의합니다.
1. Click **[!UICONTROL Confirm]** to save your audience.

   ![](assets/poi_subscriptions_app_audience_defined.png)

1. 이메일에 콘텐츠를 추가합니다.

   ![](assets/poi_email_content.png)

1. 이메일 대시보드를 보려면 활동 만들기를 확인합니다.
1. 메시지를 전송합니다.

다음과 같은 이유로 10% 할인 혜택이 포함된 이메일이 가입자에게 전송됩니다.

* 지난 2 주 동안 보스톤 스토어를 최소 한 번 방문했습니다.
* 모바일 애플리케이션이 방문 중에 적어도 한 번 전경에 있었습니다.

**관련 항목:**

* [이메일 만들기](../../channels/using/creating-an-email.md)
* [컨텐츠 정의](../../designing/using/example--email-personalization.md)
* [메시지 보내기](../../sending/using/confirming-the-send.md)

