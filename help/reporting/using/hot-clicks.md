---
title: 핫 클릭
description: 즉시 사용 가능한 핫 클릭 보고서를 사용하여 고객이 게재를 클릭한 위치를 파악합니다.
audience: reporting
content-type: reference
topic-tags: list-of-reports
context-tags: deliveryHotClicksReport,main
feature: Reporting
role: Leader
level: Intermediate
exl-id: 5af37156-e93b-4ae9-9856-053364f211ef
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---

# 핫 클릭{#hot-clicks}

이 보고서는 각 게재 또는 트랜잭션 메시지의 **[!UICONTROL Reports]** 버튼을 통해 액세스할 수 있습니다.

![](assets/delivery_reports_hot-clicks_4.png)

메시지 콘텐츠(HTML 및/또는 텍스트)와 각 링크에 대한 클릭 비율이 표시됩니다.

![](assets/delivery_reports_10.png)

게재하기 위해 동적 콘텐츠를 만든 경우 정의한 각 조건에 대한 백분율을 볼 수 있습니다. 게재에 조건부 콘텐츠 삽입에 대한 자세한 내용은 [동적 콘텐츠 정의](../../designing/using/personalization.md#defining-dynamic-content-in-an-email)를 참조하십시오.

예를 들어 다음 조건이 있는 게재를 만든다고 가정합니다.

* 수신자가 남자 또는 여자인 경우 기본 이미지의 링크가 다릅니다.
* 25세 이상의 수신자에게만 표시되는 특별 오퍼에 대한 링크도 추가했습니다.

메시지가 전송되면 게재 대시보드에서 **[!UICONTROL Reports]** **[!UICONTROL Hot clicks]** 을 선택합니다.

기본적으로 선택한 프로필이 없습니다. 성을 알 수 없는 수신자 및 25세 미만이거나 나이를 알 수 없는 수신자의 클릭 수만 표시됩니다.

![](assets/delivery_reports_hot-clicks_1.png)

여성 클릭 수를 표시하려면 **[!UICONTROL Change profile]** 버튼을 클릭하고 여성 테스트 프로필을 선택합니다. 남성용 클릭 수를 표시하려면 유사하게 진행하여 남성 테스트 프로필을 선택합니다.

![](assets/delivery_reports_hot-clicks_2.png)

25일 동안 수신자에 대한 클릭 수를 표시하려면 **[!UICONTROL Change profile]** 버튼을 클릭하고 생년월일이 이 조건과 일치하는 테스트 프로필을 선택합니다.

테스트 프로필에 대한 자세한 내용은 [테스트 프로필 정보](../../audiences/using/managing-test-profiles.md)를 참조하십시오.

>[!NOTE]
>
>특정 링크에 대한 클릭 수는 게재의 모든 조건부 컨텐츠에 대한 총 클릭 수의 백분율입니다. 따라서 다이내믹 컨텐츠를 정의한 경우 특정 테스트 프로필에 대해 표시되는 백분율의 합계가 100과 같지 않을 수 있습니다.

마찬가지로, 반복 게재 및 트랜잭션 메시지의 경우, 표시할 동적 컨텐츠에 해당하는 테스트 프로필을 선택할 수 있지만 선택한 실행 게재에 따라 클릭 백분율을 볼 수도 있습니다.

실행 게재는 다음과 같은 경우에 만들어지는 실행 가능한 비기능 기술 메시지입니다.

* 반복 게재를 실행하거나 업데이트할 때마다.

   예를 들어 이 게재를 관리하는 워크플로우가 한 달에 한 번 실행되는 경우 매월 하나의 실행 게재가 있습니다. 이 외에도 게재 컨텐츠가 업데이트될 때마다 추가 실행 게재가 만들어집니다.

   반복 이메일 게재에 대한 자세한 내용은 [이메일 게재](../../automating/using/email-delivery.md)를 참조하십시오.

* 기본적으로 트랜잭션 메시지에 대해 매월 한 번, 트랜잭션 메시지가 편집되어 다시 게시될 때마다 이러한 메시지가 나타납니다.

   트랜잭션 메시지에 대한 자세한 내용은 [트랜잭션 메시지 시작](../../channels/using/getting-started-with-transactional-msg.md)을 참조하십시오.

>[!NOTE]
>
>추적된 URL의 ID는 각 실행에 대해 다르므로 지정된 메시지의 실행 게재에 대해 핫 클릭 데이터를 집계할 수 없습니다. 한 번에 한 실행 게재에만 표시할 수 있습니다.

메시지가 전송되면 게재 대시보드에서 **[!UICONTROL Reports]** **[!UICONTROL Hot clicks]** 을 선택합니다.

기본적으로 마지막 실행 게재가 선택됩니다. **[!UICONTROL Change execution delivery]** 단추를 클릭하여 다른 단추를 선택합니다.

![](assets/delivery_reports_hot-clicks_3.png)

선택한 게재 실행에 대한 클릭 백분율만 표시됩니다.
