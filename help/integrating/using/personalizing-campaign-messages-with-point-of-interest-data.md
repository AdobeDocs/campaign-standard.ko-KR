---
title: Points of Interest 데이터로 Campaign 메시지 개인화
description: 관심 영역 데이터 통합을 사용하여 구독자의 위치를 기반으로 개인화된 메시지를 만드는 방법을 알아봅니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-analytics-for-mobile
feature: Audiences
role: Data Architect
level: Intermediate
exl-id: fcc79829-902d-4547-87c5-8a213e1257b7
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 10%

---

# Points of Interest 데이터로 Campaign 메시지 개인화{#personalizing-campaign-messages-with-point-of-interest-data}

Adobe Campaign에서는 모바일 애플리케이션의 구독자로부터 수집된 관심 영역 데이터를 사용하여 이메일과 같은 개인화된 마케팅 메시지를 보낼 수 있습니다.

관심 영역 데이터에만 표준 게재와 반응할 수 있습니다. [트랜잭션 메시지](../../channels/using/getting-started-with-transactional-msg.md) 위치 데이터를 사용할 수 없습니다.

가장 빨리 반응할 수 있는 시간은 약 10분입니다.

이 경우, 지난 2주 내에 보스턴 스토어를 방문한 모든 구독자에게 이메일을 보내도록 결정합니다.

1. 이메일 마케팅 활동을 만듭니다.
1. 게재 대상자를 정의할 때 을(를) 끌어다 놓습니다 **[!UICONTROL Subscriptions to an application]** 요소를 작업 공간에 추가합니다.

   ![](assets/poi_subscriptions_app.png)

   대상자 관리는 [대상자 정의](../../audiences/using/creating-audiences.md) 섹션을 참조하십시오.

1. 에서 **[!UICONTROL Add a rule - Profile/Subscriptions to an application]** 창에서 끌어서 놓습니다. **[!UICONTROL POI Location Subscription]** 요소를 작업 공간에 추가합니다.

   ![](assets/poi_add_rule_profile_subscription.png)

1. 에서 **[!UICONTROL Add a rule - POI Location Subscription]** 창에서 사용할 관심 영역 레이블을 입력합니다.

   ![](assets/poi_location_subscription.png)

1. **[!UICONTROL Filter type]** 필드에서 **[!UICONTROL Relative]**&#x200B;을(를) 선택합니다.
1. 을(를) 확인합니다. **[!UICONTROL Preceding days]** 옵션을 선택하고 **[!UICONTROL 15]** 를 입력합니다.
1. 사용자가 관심 영역을 방문해야 하는 횟수를 정의합니다.
1. 클릭 **[!UICONTROL Confirm]** 대상자를 저장합니다.

   ![](assets/poi_subscriptions_app_audience_defined.png)

1. 전자 메일에 컨텐츠를 추가합니다.

   ![](assets/poi_email_content.png)

1. 활동 만들기를 확인하여 이메일의 대시보드를 봅니다.
1. 메시지를 보냅니다.

다음과 같은 가입자에게 10% 할인 오퍼가 포함된 이메일이 전송됩니다.

* 지난 2주 내에 적어도 한 번은 보스턴 상점을 방문했어요.
* 모바일 애플리케이션을 방문 중에 적어도 한 번 이상 포그라운드에 두고 있었습니다.

**관련 항목:**

* [이메일 만들기](../../channels/using/creating-an-email.md)
* [콘텐츠 정의](../../designing/using/personalization.md#example-email-personalization)
* [메시지 보내기](../../sending/using/confirming-the-send.md)
