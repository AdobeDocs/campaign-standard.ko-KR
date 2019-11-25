---
title: 외부 신호
description: 외부 신호 활동은 다른 워크플로우에서 일부 조건이 성공적으로 충족되면 워크플로우를 트리거합니다.
page-status-flag: never-activated
uuid: 884b6daf-bfd9-440b-8336-004b80c76def
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities
discoiquuid: 911c71b5-da8b-4916-b645-13bba6d21715
context-tags: signal,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: b06edadfa963881403328c4ab37d25d701bc8237

---


# 외부 신호{#external-signal}

## 설명 {#description}

![](assets/signal.png)

다른 워크플로 또는 REST API 호출에서 일부 조건이 성공적으로 충족되면 **[!UICONTROL External signal]** 활동이 워크플로우를 트리거합니다.

## 사용 상황 {#context-of-use}

이 **[!UICONTROL External signal]** 활동은 동일한 고객 여정의 일부인 다양한 프로세스를 다양한 워크플로우로 구성하고 조정하는 데 사용됩니다. 또한 다른 워크플로우에서 워크플로우를 시작하여 보다 복잡한 고객 여정을 지원할 수 있을 뿐만 아니라 문제 발생 시 보다 효과적으로 모니터링하고 대응할 수 있습니다.

활동은 **[!UICONTROL External signal]** 워크플로우의 첫 번째 활동으로 배치되도록 디자인되었습니다. 다른 워크플로우의 **[!UICONTROL End]** 활동 또는 REST API 호출에서 트리거할 수 있습니다(자세한 내용은 API 설명서를 [참조하십시오](../../api/using/managing-workflows.md)).

트리거되면 외부 매개 변수를 정의하고 워크플로 이벤트 변수에서 사용할 수 있습니다. 외부 매개 변수를 사용하여 워크플로우를 호출하는 프로세스는 [이 섹션에](../../automating/using/calling-a-workflow-with-external-parameters.md)자세히 설명되어 있습니다.

>[!NOTE]
>
>활동이 10분마다 더 자주 트리거될 수 없습니다.

활동은 여러 가지 다른 이벤트에서 트리거될 수 있습니다. **[!UICONTROL External signal]** 이 경우 소스 워크플로우 또는 API 호출 중 하나가 실행되면 **[!UICONTROL External signal]** 트리거됩니다. 모든 소스 워크플로우가 완료되지 않아도 됩니다.

## 구성 {#configuration}

외부 신호를 구성할 때는 먼저 대상 워크플로우에서 **[!UICONTROL External signal]** 활동을 구성해야 합니다. 이 구성이 완료되면 이 워크플로우의 **[!UICONTROL External signal]** 활동을 사용하여 소스 워크플로우의 **[!UICONTROL End]** 활동을 구성할 수 있습니다.

1. 대상 워크플로우로 **[!UICONTROL External signal]** 활동을 드래그하여 놓습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 엽니다.
1. 활동의 레이블을 편집합니다. 이 레이블은 를 트리거하는 소스 워크플로우를 구성할 때 필요합니다 **[!UICONTROL External signal]**.

   매개 변수를 사용하여 워크플로우를 호출하려면 해당 **[!UICONTROL Parameters]** 영역을 사용하여 선언합니다. For more on this, refer to [this section](../../automating/using/calling-a-workflow-with-external-parameters.md#declaring-the-parameters-in-the-external-signal-activity).

   ![](assets/external_signal_configuration.png)

1. 활동 구성을 확인하고 필요한 다른 활동을 추가하고 워크플로우를 저장합니다.

   >[!NOTE]
   >
   >다른 워크플로우에서 대상 워크플로우를 트리거하려면 다음 단계를 진행합니다. REST API 호출에서 대상 워크플로우를 트리거하려면 API [설명서를](../../api/using/managing-workflows.md) 참조하십시오.

1. 소스 워크플로우를 열고 **[!UICONTROL End]** 활동을 선택합니다. 사용할 수 있는 **[!UICONTROL End]** 활동이 없는 경우, 워크플로우의 분기의 마지막 활동 뒤에 활동을 추가합니다.

   일부 활동에는 기본적으로 아웃바운드 전환이 없습니다. 이러한 활동의 **[!UICONTROL Properties]** 탭에서 아웃바운드 전환을 추가할 수 있습니다.

   예를 들어 **[!UICONTROL Update data]** 활동에서 **[!UICONTROL Transitions]** 탭으로 이동하여 **[!UICONTROL Add an outbound transition without the population]** 옵션을 선택합니다. 이 옵션을 사용하면 데이터를 포함하지 않고 시스템에서 불필요한 공간을 사용하지 않는 전환을 추가할 수 있습니다. 대상 워크플로우를 트리거하는 추가 **[!UICONTROL End]** 활동을 연결하는 데 사용됩니다.

   ![](assets/external_signal_empty_transition.png)

1. 활동의 **[!UICONTROL External signal]** 탭에서 대상 워크플로우와 해당 워크플로우 내에서 트리거할 **[!UICONTROL End]** **[!UICONTROL External signal]** 활동을 선택합니다.

   다른 워크플로우를 트리거하는 **[!UICONTROL End]** 활동을 설정하면 추가 신호 심볼로 해당 아이콘이 업데이트됩니다.

   매개 변수를 사용하여 워크플로우를 호출하려면 **[!UICONTROL Parameters and values]** 영역을 사용합니다. For more on this, refer to [this section](../../automating/using/calling-a-workflow-with-external-parameters.md#defining-the-parameters-when-calling-the-workflow).

   ![](assets/external_signal_end.png)

1. 소스 워크플로우를 저장합니다.

소스 워크플로우 또는 REST API 호출의 **[!UICONTROL End]** 활동이 실행되면 대상 워크플로우는 **[!UICONTROL External signal]** 활동에서 자동으로 트리거됩니다.

>[!NOTE]
>
>대상 워크플로우를 트리거하려면 먼저 수동으로 시작해야 합니다. 시작되면 **[!UICONTROL External activity]** 소스 워크플로우가 활성화되고 신호를 기다립니다.

## 예 {#example}

다음 예는 일반적인 사용 사례의 **[!UICONTROL External signal]** 활동을 보여줍니다. 데이터 가져오기는 소스 워크플로우에서 수행됩니다. 가져오기가 완료되고 데이터베이스가 업데이트되면 두 번째 워크플로우가 트리거됩니다. 이 두 번째 워크플로우는 가져온 데이터의 집계를 업데이트하는 데 사용됩니다.

소스 워크플로우는 다음과 같이 표시됩니다.

* 파일 [로드](../../automating/using/load-file.md) 활동은 새 구매 데이터가 포함된 파일을 업로드합니다. 구매 데이터가 기본적으로 [datamart에 없으므로 데이터베이스가 적절하게 확장되었습니다](../../developing/using/data-model-concepts.md) .

   예:

   ```
   tcode;tdate;customer;product;tamount
   aze123;21/05/2015;dannymars@example.com;A2;799
   aze124;28/05/2015;dannymars@example.com;A7;8
   aze125;31/07/2015;john.smith@example.com;A7;8
   aze126;14/12/2015;john.smith@example.com;A10;4
   aze127;02/01/2016;dannymars@example.com;A3;79
   aze128;04/03/2016;clara.smith@example.com;A8;149
   ```

* 조정 [활동은](../../automating/using/reconciliation.md) 가져온 데이터와 데이터베이스 사이에 링크를 만들어 트랜잭션 데이터가 프로파일과 제품에 제대로 연결되도록 합니다.
* 업데이트 [데이터](../../automating/using/update-data.md) 활동은 들어오는 데이터로 데이터베이스의 트랜잭션 리소스를 삽입하고 업데이트합니다.
* 활동은 집계를 업데이트하는 데 사용되는 대상 워크플로우를 트리거합니다. **[!UICONTROL End]**

![](assets/signal_example_source1.png)

대상 워크플로우는 다음과 같이 표시됩니다.

* 활동이 소스 워크플로우가 성공적으로 완료될 때까지 **[!UICONTROL External signal]** 기다립니다.
* 쿼리 [활동은](../../automating/using/query.md#enriching-data) 프로파일을 타깃팅하고 마지막 구매 날짜를 검색할 수 있는 컬렉션 세트로 프로파일을 보완합니다.
* 업데이트 [데이터](../../automating/using/update-data.md) 활동은 전용 사용자 지정 필드에 추가 데이터를 저장합니다. 프로파일 리소스가 확장되어 마지막 구매 **날짜** 필드를 추가했음을 참고하십시오.

![](assets/signal_example_source2.png)

