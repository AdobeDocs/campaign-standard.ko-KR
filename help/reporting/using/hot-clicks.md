---
title: 클릭 수
seo-title: 클릭 수
description: 클릭 수
seo-description: 즉시 즉시 사용할 수 있는 보고서를 통해 고객이 어디에서 배달을 클릭했는지 알 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 7 ed 49 dd 3-d 7 ee -466 a -9 a 7 b-d 2 aa 16961667
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 보고
content-type: 참조
topic-tags: list-of-reports
discoiquuid: ECBC 1 ADE -63 D 9-4 AC 2-9828-380 A 1 AA 95094
context-tags: Deliveryhotclicksreport, Main
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 77b0933bcd004cedc6a58f80717a4284b284e0cd

---


# Hot clicks{#hot-clicks}

This report can be accessed from the **[!UICONTROL Reports]** button in each delivery or transactional message.

![](assets/delivery_reports_hot-clicks_4.png)

각 링크에 대한 클릭 수의 백분율을 사용하여 메시지 컨텐츠 (HTML 및/또는 텍스트) 를 표시합니다.

![](assets/delivery_reports_10.png)

게재를 위한 동적 컨텐츠를 만든 경우 정의한 각 조건에 대한 백분율을 볼 수 있습니다. For more on inserting conditional content in a delivery, see [Defining dynamic content](../../designing/using/defining-dynamic-content-in-a-landing-page.md).

예를 들어 다음과 같은 조건으로 배달을 만들었다고 가정합니다.

* 받는 사람이 남성 또는 여성인 경우 주 이미지의 링크는 서로 다릅니다.
* 25 세 이상의 수신자만 볼 수 있는 특별 오퍼에 대한 링크가 추가되었습니다.

Once your message is sent, select **[!UICONTROL Reports]** &gt; **[!UICONTROL Hot clicks]** from the delivery dashboard.

기본적으로 [프로필 없음] 이 선택되어 있습니다. 성별은 알 수 없는 수신자와 25 세 미만이거나 나이를 알 수 없는 수신자에 대한 클릭만 표시됩니다.

![](assets/delivery_reports_hot-clicks_1.png)

To display clicks for women, click the **[!UICONTROL Change profile]** button and select a female test profile. 남성용 클릭 수를 표시하려면 유사하게 진행하며 남성 테스트 프로필을 선택합니다.

![](assets/delivery_reports_hot-clicks_2.png)

To display clicks for recipients over 25, click the **[!UICONTROL Change profile]** button and select a test profile whose birth date is matching this condition.

For more on test profiles, see [About test profiles](../../sending/using/managing-test-profiles-and-sending-proofs.md#about-test-profiles).

>[!NOTE]
>
>특정 링크에 대한 클릭 수는 게시에 있는 모든 조건부 컨텐츠에 대한 총 클릭 수의 백분율입니다. 따라서 동적 컨텐츠를 정의한 경우 특정 테스트 프로필에 대해 표시되는 백분율의 합계는 100 이 아닐 수 있습니다.

마찬가지로 반복되는 배달 및 트랜잭션 메시지의 경우 표시할 동적 컨텐츠에 해당하는 테스트 프로필을 선택할 수 있지만 선택한 실행 전달에 따라 클릭 백분율을 볼 수도 있습니다.

실행 배달은 다음과 같은 경우에 만들어지는 실행 불가능하고 기능적인 기술적인 메시지입니다.

* 반복 배달이 실행될 때마다 또는 업데이트됩니다.

   예를 들어, 이 배달을 관리하는 워크플로우가 한 달에 한 번 실행되면 매월 하나의 실행 배달이 발생합니다. 이와 더불어, 게재의 컨텐츠가 업데이트될 때마다 추가 실행 배달이 생성됩니다.

   For more on recurring email deliveries, see [Email delivery](../../automating/using/email-delivery.md).

* 트랜잭션 메시지의 경우 한 달에 한 번, 트랜잭션 메시지는 편집 및 게시할 때마다 기본적으로 한 번씩 표시됩니다.

   For more on transactional messages, see [About transactional messaging](../../channels/using/about-transactional-messaging.md).

>[!NOTE]
>
>추적된 URL의 ID는 실행마다 다르므로, 지정된 메시지의 모든 실행에 대해 핫 클릭 데이터를 집계할 수 없습니다. 한 번에 하나의 실행 전달에만 표시할 수 있습니다.

Once your message is sent, select **[!UICONTROL Reports]** &gt; **[!UICONTROL Hot clicks]** from the delivery dashboard.

기본적으로 마지막 실행 게재가 선택되어 있습니다. **[!UICONTROL Change execution delivery]** 단추를 클릭하여 다른 단추를 선택합니다.

![](assets/delivery_reports_hot-clicks_3.png)

선택한 배달 실행에 대한 클릭 백분율만 표시됩니다.
