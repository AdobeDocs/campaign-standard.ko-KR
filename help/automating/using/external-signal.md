---
title: 외부 신호
seo-title: 외부 신호
description: 외부 신호
seo-description: 다른 워크플로우에서 일부 조건이 성공적으로 충족되면 외부 신호 활동이 워크플로우를 트리거합니다.
page-status-flag: 정품 인증 안 함
uuid: 884 B 6 DAF-BFD 9-440 B -8336-004 B 80 C 76 DEF
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 실행 활동
discoiquuid: 911 c 71 b 5-da 8 b -4916-b 645-13 bba 6 d 21715
context-tags: 신호, 주
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 0454dac1a7976c1be2838c2a846d33e77e60c3b3

---


# External signal{#external-signal}

## Description {#description}

![](assets/signal.png)

The **[!UICONTROL External signal]** activity triggers a workflow when some conditions are successfully met in another workflow or from a REST API call.

## Context of use {#context-of-use}

**[!UICONTROL External signal]** 활동은 다른 워크플로우로 동일한 고객 경로의 일부인 다양한 프로세스를 구성하고 조직화하는 데 사용됩니다. 또한 다른 워크플로우에서 하나의 워크플로우를 시작할 수 있으므로 보다 복잡한 고객 여정을 지원할 수 있을 뿐만 아니라 문제의 경우 보다 효과적으로 모니터링하고 반응할 수 있습니다.

**[!UICONTROL External signal]** 활동은 워크플로우의 첫 번째 활동으로 배치되도록 디자인되었습니다. It can be triggered from the **[!UICONTROL End]** activity of another workflow or from a REST API call (for more on this, refer to the [API documentation](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#triggering-a-signal-activity) ).

트리거되면, 외부 매개 변수를 정의하여 Workflow Events 변수에서 사용할 수 있습니다. The process to call a workflow with external parameters is detailed in [this section](../../automating/using/calling-a-workflow-with-external-parameters.md).

>[!NOTE]
>
>활동이 10 분마다 더 자주 트리거될 수 없습니다.

**[!UICONTROL External signal]** 활동을 여러 다른 이벤트에서 트리거할 수 있습니다. In that case, the **[!UICONTROL External signal]** is triggered as soon as one of the source workflows or API call is executed. 모든 소스 워크플로우가 완료되지 않아도 됩니다.

## Configuration {#configuration}

When configuring an external signal, it is important to first configure the **[!UICONTROL External signal]** activity in the destination workflow. Once this configuration is done, the **[!UICONTROL External signal]** activity of this workflow becomes available to configure the **[!UICONTROL End]** activity of the source workflow.

1. **[!UICONTROL External signal]** 활동을 대상 워크플로우로 드래그하여 놓습니다.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. 활동 레이블을 편집합니다. This label is needed when configuring the source workflow that triggers the **[!UICONTROL External signal]**.

   If you want to call the workflow with parameters, use the **[!UICONTROL Parameters]** area to declare them. For more on this, refer to [this section](../../automating/using/calling-a-workflow-with-external-parameters.md#declaring-the-parameters-in-the-external-signal-activity).

   ![](assets/external_signal_configuration.png)

1. 활동의 구성을 확인하고, 필요한 기타 활동을 추가하고, 워크플로우를 저장합니다.

   >[!NOTE]
   >
   >다른 워크플로우에서 대상 워크플로우를 트리거하려면 다음 단계를 수행하십시오. If you want to trigger the destination workflow from a REST API call, consult the [API documentation](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#triggering-a-signal-activity) to get more details.

1. Open the source workflow and select an **[!UICONTROL End]** activity. If there is no **[!UICONTROL End]** activity available, add one after the last activity of a branch of the workflow.

   일부 활동에는 기본적으로 아웃바운드 전환이 없습니다. From the **[!UICONTROL Properties]** tab of these activities, you can add an outbound transition.

   For example, in an **[!UICONTROL Update data]** activity, go to the **[!UICONTROL Transitions]** tab and check the **[!UICONTROL Add an outbound transition without the population]** option. 이 옵션을 사용하면 데이터를 포함하지 않고 시스템에 불필요한 공간을 사용하지 않는 전환을 추가할 수 있습니다. It is just used to connect the extra **[!UICONTROL End]** activity that triggers the destination workflow.

   ![](assets/external_signal_empty_transition.png)

1. In the **[!UICONTROL External signal]** tab of the **[!UICONTROL End]** activity, select the destination workflow as well as the **[!UICONTROL External signal]** activity to trigger within that workflow.

   When you set an **[!UICONTROL End]** activity to trigger another workflow, its icon is updated with an additional signal symbol.

   If you want to call the workflow with parameters, use the **[!UICONTROL Parameters and values]** area. For more on this, refer to [this section](../../automating/using/calling-a-workflow-with-external-parameters.md#defining-the-parameters-when-calling-the-workflow).

   ![](assets/external_signal_end.png)

1. 소스 워크플로우를 저장합니다.

Once the **[!UICONTROL End]** activity of the source workflow or the REST API call is executed, the destination workflow is automatically triggered from the **[!UICONTROL External signal]** activity.

>[!NOTE]
>
>대상 워크플로우는 트리거되기 전에 수동으로 시작해야 합니다. When started, the **[!UICONTROL External activity]** is activated and waits for the signal from the source workflow.

## Example {#example}

The following example illustrates the **[!UICONTROL External signal]** activity in a typical use case. 데이터 가져오기는 소스 워크플로우에서 수행됩니다. 가져오기가 완료되고 데이터베이스가 업데이트되면 두 번째 워크플로우가 트리거됩니다. 이 두 번째 워크플로우는 가져온 데이터의 합계를 업데이트하는 데 사용됩니다.

소스 워크플로우는 다음과 같이 제공됩니다.

* [로드 파일](../../automating/using/load-file.md) 활동은 새 구매 데이터가 들어 있는 파일을 업로드합니다. Note that the [database has been extended](../../developing/using/data-model-concepts.md) accordingly as purchase data are not present by default in the datamart.

   예를 들면 다음과 같습니다.

   ```
   tcode;tdate;customer;product;tamount
   aze123;21/05/2015;dannymars@example.com;A2;799
   aze124;28/05/2015;dannymars@example.com;A7;8
   aze125;31/07/2015;john.smith@example.com;A7;8
   aze126;14/12/2015;john.smith@example.com;A10;4
   aze127;02/01/2016;dannymars@example.com;A3;79
   aze128;04/03/2016;clara.smith@example.com;A8;149
   ```

* [조정](../../automating/using/reconciliation.md) 활동은 가져온 데이터와 데이터베이스 사이의 링크를 만들어 트랜잭션 데이터가 프로필 및 제품에 제대로 연결되어 있도록 합니다.
* [데이터](../../automating/using/update-data.md) 업데이트 작업은 데이터베이스의 트랜잭션 리소스를 삽입 데이터로 삽입하고 업데이트합니다.
* **[!UICONTROL End]** 활동은 대상을 업데이트하는 데 사용되는 대상 워크플로우를 트리거합니다.

![](assets/signal_example_source1.png)

대상 워크플로우는 다음과 같이 표시됩니다.

* **[!UICONTROL External signal]** 활동은 소스 워크플로우가 성공적으로 완료될 때까지 대기합니다.
* [쿼리](../../automating/using/query.md#enriching-data) 활동은 프로필을 타깃팅하고, 마지막 구매 날짜를 검색할 수 있도록 컬렉션 세트로 보강합니다.
* [데이터 업데이트](../../automating/using/update-data.md) 활동은 추가 데이터를 전용 사용자 지정 필드에 저장합니다. Note that the profile resource has been extended to add the **Last purchase date** field.

![](assets/signal_example_source2.png)

