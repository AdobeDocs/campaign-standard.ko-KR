---
title: 고객 저장
seo-title: 고객 저장
description: 고객 저장
seo-description: 대상자 저장 활동을 사용하면 기존 대상을 업데이트하거나 워크플로우의 계산된 업스트림 목록에서 새 대상을 만들 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 8 babb 173-fa 59-44 a 7-a 2 a 5-49 f 45 ba 6 bf 99
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 타깃팅 활동
discoiquuid: 1 F 6 BB 048-7 ABD -499 B-A 4 B 0-187 F 9492 DC 47
context-tags: Saveaudience, main
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 0454dac1a7976c1be2838c2a846d33e77e60c3b3

---


# Save audience{#save-audience}

## Description {#description}

![](assets/save_audience.png)

**[!UICONTROL Save audience]** 활동을 사용하면 기존 대상을 업데이트하거나 워크플로우의 계산된 업스트림 목록에서 새 대상을 만들 수 있습니다. The audiences created or updated from this activity are **List** or **File** audiences. They are added to the list of application audiences, and are made available via the **[!UICONTROL Audiences]** menu.

>[!NOTE]
>
>**[!UICONTROL Save audience]** 활동을 통해 만들어진 대상이 추가 데이터로 강화되는 경우 이러한 데이터를 사용하여 독립형 제공을 개인화할 수 없습니다. 워크플로우에서 실행된 배달에서만 사용할 수 있습니다.

이 활동을 통해 프로파일을 Adobe Experience Cloud 대상/세그먼트로 내보낼 수도 있습니다. 이를 통해 다른 Adobe Experience Cloud 솔루션에서 이러한 고객을 활용할 수 있습니다. For more information about shared audiences, refer to [Working with Campaign and People Core Service](../../integrating/using/about-campaign-audience-manager-or-people-core-service-integration.md).

## Context of use {#context-of-use}

**[!UICONTROL Save audience]** 활동은 본질적으로 동일한 워크플로우에서 계산된 대상을 다시 사용할 수 있는 대상자로 변환하여 해당 그룹을 유지하는 데 사용됩니다.

## Configuration {#configuration}

1. **[!UICONTROL Save audience]** 워크플로우에 활동을 놓습니다.
1. 쿼리, 교차, 조합 또는 제외와 같은 다른 타깃팅 활동 뒤에 연결하십시오.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. 수행할 작업을 선택합니다.

   * **[!UICONTROL Update an existing audience]**: 기존 대상을 선택하고 업데이트 유형을 선택합니다.

      * **[!UICONTROL Replace audience content with new data]**: 대상 콘텐츠의 전체가 대체됩니다. 이전 데이터가 손실됩니다. 고객 저장 활동의 인바운드 전환 데이터만 유지됩니다.
      * **[!UICONTROL Complete audience with new data]**: 이전 대상자 데이터가 유지되고 대상 활동의 인바운드 전환 데이터가 IT에 추가됩니다.
   * **[!UICONTROL Create then update an audience]**: 대상 이름을 입력하고 업데이트 유형을 선택합니다. 대상이 아직 존재하지 않을 경우, 생성됩니다. 이미 존재하는 경우 선택한 모드에 따라 업데이트됩니다.

      * **[!UICONTROL Replace audience content with new data]**: 대상 콘텐츠의 전체가 대체됩니다. 이전 데이터가 손실됩니다. 고객 저장 활동의 인바운드 전환 데이터만 유지됩니다.

         경고, 이 옵션은 업데이트된 대상자의 대상 유형과 타깃팅 차원을 지웁니다.

      * **[!UICONTROL Complete audience with new data]**: 이전 대상자 데이터가 유지되고 대상 활동의 인바운드 전환 데이터가 IT에 추가됩니다.

         경고. 이 옵션은 대상 유형 또는 대상 차원이 워크플로우의 현재 구성과 호환하지 않는 경우 오류가 발생합니다. 예를 들어, 쿼리에서 가져온 프로필로 파일 유형 대상을 완료할 수 없습니다.
   * **[!UICONTROL Create a new audience]**: 만들 대상 이름을 입력합니다. 대상이 만들어진 시간 및 시간은 대상 이름에 자동으로 추가됩니다. 이렇게 하면 워크플로우가 실행될 때마다 대상이 고유하게 설정됩니다.
   * **[!UICONTROL Share in Adobe Experience Cloud]**: 타깃팅된 프로필이 있는 경우 대상을 Adobe Experience Cloud로 내보내려면 이 옵션을 선택한 다음 기존 공유 대상을 선택하거나 새 대상을 만듭니다.

      Also select a **[!UICONTROL Shared Data source]** that corresponds to the resource of the data contained in the audience so that the data is correctly reconciled in Adobe Experience Cloud.

      Using this option, the shared audience is not added to the list of Adobe Campaign audiences available via the **[!UICONTROL Audiences]** menu.

      >[!NOTE]
      >
      >이 옵션은 관리자가 Adobe Experience Cloud를 사용하는 공유 대상 기능을 구성한 경우에만 사용할 수 있습니다. For more information, refer to [Working with Campaign and People Core Service](../../integrating/using/about-campaign-audience-manager-or-people-core-service-integration.md).
   업데이트 중에 저장되거나 사용할 수 있는 대상의 유형은 워크플로우에 업스트림 업스트림 활동이 있는지에 따라 달라집니다.

   If the targeting dimension of the audience is unknown when it is saved (for example if it is from an imported file), the audience is created or updated as a **[!UICONTROL File]** type audience.

   If the targeting dimension of the saved audience is already defined when it is saved (for example, if it comes from a targeting, after a query, etc.), then the audience is saved or updated as a **[!UICONTROL List]** type audience.

   The content of the saved audience is then available in the detail view of the audience, which can be accessed from the **[!UICONTROL Audiences]** menu. 이 보기에서 사용할 수 있는 열은 워크플로우의 고객 활동 저장의 인바운드 전환 열에 해당합니다. 예를 들면 다음과 같습니다. 가져온 파일의 열 (쿼리에서 추가 데이터 추가)

1. 활동의 구성을 확인하고 워크플로우를 저장합니다.

## Example {#example}

이 예에서 정의된 워크플로우는 타깃팅에서 일반 대상 업데이트를 보여 줍니다.

* It is automatically executed once a month using a **[!UICONTROL Scheduler]**.
* You can use a **[!UICONTROL Query]** to recover all the profiles subscribed to the different application services available.
* **[!UICONTROL Save audience]** 활동은 마지막 워크플로우 실행 이후 서비스에서 구독이 해지된 프로필을 삭제하고 새로 가입된 프로필을 추가하여 대상을 업데이트합니다.

![](assets/save_audience_example_1.png)

**[!UICONTROL Save audience]** 활동은 다음과 같이 구성됩니다.

![](assets/save_audience_example_2.png)

