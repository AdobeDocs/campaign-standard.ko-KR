---
title: 워크플로우 실행
seo-title: 워크플로우 실행
description: 워크플로우 실행
seo-description: 워크플로우를 실행하고 모니터링하는 방법을 살펴볼 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: ff 02 b 74 e -53 e 8-49 c 6-bf 8 e -0 c 729 eaa 7 d 25
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: workflow-general-operation
discoiquuid: 906 C 85 EA -83 B 7-4268-86 DA-CD 353 F 1 DC 591
context-tags: workflow, overview; 워크플로우, 기본
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 0454dac1a7976c1be2838c2a846d33e77e60c3b3

---


# Executing a workflow{#executing-a-workflow}

## About workflow execution {#about-workflow-execution}

워크플로우는 항상 수동으로 시작됩니다. However, once started, it can remain inactive, depending on the information specified in a [Scheduler](../../automating/using/scheduler.md) activity.

>[!CAUTION]
>
>동시에 5 개 이상의 워크플로우를 실행하지 않는 것이 좋습니다. 너무 많은 워크플로우가 동시에 실행되면 시스템에 리소스가 부족해서 불안정해질 수 있습니다. 또한 시간이 지남에 따라 워크플로우를 확장하는 것이 좋습니다.

실행 관련 작업 (시작, 중지, 일시 중지 등) **비동기** 프로세스임: 명령이 저장되므로 서버를 적용할 수 있게 되면 명령이 적용됩니다.

워크플로우에서 각 활동의 결과는 일반적으로 화살표로 표시된 전환을 통해 다음 활동으로 전송됩니다.

전환이 대상 활동과 연결되어 있지 않으면 종결되지 않습니다.

![](assets/wkf_execution_1.png)

>[!NOTE]
>
>종결되지 않은 전환을 포함하는 워크플로우를 계속 실행할 수 있습니다. 경고 메시지가 생성되고 워크플로우가 전환에 도달하면 일시 중지됩니다. 하지만 오류가 발생하지 않습니다. 또한 디자인을 완전히 완성하지 않고도 워크플로우를 시작할 수 있고 작업을 완료하면서 완료할 수 있습니다.

활동이 실행되면 전환 시 전송된 레코드 수가 위에 표시됩니다.

![](assets/wkf_transition_count.png)

전환 과정을 열 때 또는 워크플로우 실행 후에 전송된 데이터가 올바른지 확인할 수 있습니다. 데이터와 데이터 구조를 볼 수 있습니다.

기본적으로 워크플로우의 마지막 전환에 대한 세부 사항만 액세스할 수 있습니다. To be able to access the results of the preceding activities, you need to check the **[!UICONTROL Keep interim results]** option in the **[!UICONTROL Execution]** section of the workflow properties, before starting the workflow.

>[!NOTE]
>
>이 옵션은 많은 메모리를 사용하며 워크플로우를 구성하고 제대로 구성되었는지 확인하는 데 도움이 됩니다. 프로덕션 인스턴스는 선택하지 않은 상태로 두십시오.

When a transition is open, you can edit its **[!UICONTROL Label]** or link a **[!UICONTROL Segment code]** to it. 이렇게 하려면 해당 필드를 편집하고 수정 사항을 확인합니다.

## Controlling a workflow from the REST API {#controlling-a-workflow-from-the-rest-api}

Using the REST API, you can **start**, **pause**, **resume** and **stop** a workflow.

You can find more details and examples of REST calls in the [API documentation.](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#controlling-a-workflow)

## Life cycle {#life-cycle}

워크플로우의 라이프사이클에는 세 가지 주요 단계가 포함되며 각 단계는 상태 및 색상에 연결되어 있습니다.

* **편집 (** 회색)

   This is the initial design phase of a workflow (refer to [Creating a workflow](../../automating/using/building-a-workflow.md#creating-a-workflow)). 워크플로우는 서버에서 아직 처리되지 않으며 위험 없이 수정할 수 있습니다.

* **진행 중** (파란색)

   초기 디자인 단계가 완료되면 워크플로우를 시작하고 서버에서 처리할 수 있습니다.

* **완료됨 (** 녹색)

   진행 중인 작업이 더 이상 없거나 연산자가 명시적으로 인스턴스를 중지한 경우 워크플로우가 끝납니다.

일단 시작되면 워크플로우에는 다른 상태 2 개가 있을 수 있습니다.

* **경고 (** 노란색)

   The workflow could not finish or was paused using the ![](assets/pause_darkgrey-24px.png) or ![](assets/check_pause_darkgrey-24px.png) buttons.

* **오류 (** 빨간색)

   워크플로우가 실행될 때 오류가 발생했습니다. 워크플로우가 중지되었으며 사용자는 작업을 수행해야 합니다. To find out more about this error, use the ![](assets/printpreview_darkgrey-24px.png) button to access the workflow log (refer to [Monitoring](../../automating/using/executing-a-workflow.md#monitoring)).

마케팅 활동 목록을 통해 모든 워크플로우와 상태를 표시할 수 있습니다. For more on this, see [Managing marketing activities](../../start/using/marketing-activities.md#about-marketing-activities).

![](assets/wkf_execution_3.png)

## Execution commands {#execution-commands}

작업 표시줄의 아이콘을 사용하여 워크플로우의 실행을 시작, 추적 및 수정할 수 있습니다. [작업 막대를 참조하십시오](../../automating/using/workflow-interface.md#action-bar).

![](assets/wkf_execution_2.png)

사용 가능한 작업은 다음과 같습니다.

**start**

![](assets/play_darkgrey-24px.png) 단추가 워크플로우 실행을 시작하고 **진행 중인 (** 파란색) 상태가 됩니다. 워크플로우가 일시 중지되면 다시 시작됩니다. 그렇지 않으면 시작되고 초기 활동이 활성화됩니다.

>[!NOTE]
>
>시작은 비동기 프로세스입니다. 요청이 저장되므로 워크플로우 실행 엔진에서 가능한 한 빨리 처리됩니다.

**일시 중지**

![](assets/pause_darkgrey-24px.png) 단추가 실행을 일시 중지합니다. The workflow takes on the **Warning** (yellow) status. 새 활동은 다시 시작할 때까지 활성화되지만 진행 중인 작업은 일시 중단되지 않습니다.

**stop**

![](assets/stop_darkgrey-24px.png) 이 단추는 실행 중인 워크플로우를 중단하고 **완료된** (녹색) 상태를 유지합니다. 진행 중인 작업은 가능한 경우 중단되며 진행 중인 가져오기 또는 SQL 쿼리는 즉시 취소됩니다. 워크플로우가 중단된 위치는 워크플로우에서 다시 시작할 수 없습니다.

**다시 시작**

The ![](assets/pauseplay_darkgrey-24px.png) button involves stopping, then restarting a workflow. 대부분의 경우 빠르게 다시 시작할 수 있습니다. It can also be useful to automate restarting once stopping takes a certain amount of time, because the ![](assets/play_darkgrey-24px.png) button is only available when the stop is effective.

워크플로우에서 하나 또는 여러 활동을 선택하면 다음과 같이 수행할 수 있는 다른 작업이 있습니다.

**즉각적인 실행**

![](assets/pending_darkgrey-24px.png) 이 단추는 가능한 한 빨리 선택한 보류 중인 활동을 시작합니다.

**일반 실행**

![](assets/check_darkgrey-24px.png) 단추가 일시 중지되거나 비활성화된 모든 활동을 다시 활성화합니다.

**일시 중단된 실행**

![](assets/check_pause_darkgrey-24px.png) 단추가 선택한 활동에서 워크플로우를 일시 중지합니다. 이 작업을 수행하는 것은 물론 동일한 분기에 팔로우하는 모든 것이 실행되지 않습니다.

**실행 안 함**

![](assets/checkdisable.png) 단추가 선택한 활동을 비활성화합니다.

>[!NOTE]
>
>빠른 작업을 사용하면 특정 활동과 관련된 다른 작업에 액세스하고 활동이 선택되면 나타납니다.

## Monitoring {#monitoring}

![](assets/printpreview_darkgrey-24px.png) 이 아이콘은 워크플로우 로그 및 작업 메뉴를 엽니다.

The workflow history is saved for the duration specified in the workflow execution options (refer to [Workflow properties](../../automating/using/executing-a-workflow.md#workflow-properties)). 이 기간 동안 다시 시작한 후에도 모든 메시지가 저장됩니다. If you do not want to save the messages from a previous execution, you have to purge the history by clicking the ![](assets/delete_darkgrey-24px.png) button.

**[!UICONTROL Log]** 탭에는 모든 활동 또는 선택한 활동의 실행 내역이 들어 있습니다. 수행된 작업과 실행 오류를 시간순으로 인덱싱합니다.

![](assets/wkf_execution_4.png)

**[!UICONTROL Tasks]** 탭에는 활동의 실행 순서 지정이 자세히 설명되어 있습니다. 자세한 내용을 보려면 작업을 클릭합니다.

![](assets/wkf_execution_5.png)

In these two lists:

* 필터를 클릭하면 적용된 필터에 따른 총 활동 수가 표시됩니다. 목록에 있는 요소 수가 30 개 미만이면 카운터가 기본적으로 표시됩니다.
* **[!UICONTROL Configure list]** 이 단추를 사용하여 표시되는 정보를 선택하고 열 순서를 정의하며 목록을 정렬할 수 있습니다.
* 필터를 사용하여 필요한 정보를 신속하게 찾을 수 있습니다. 검색 필드를 사용하여 워크플로우 활동 이름의 특정 텍스트를 찾습니다 (예: " 쿼리 "와 로그를 참조하십시오.

## Error management {#error-management}

오류가 발생하면 워크플로우가 일시 중지되고 오류가 발생했을 때 실행되는 활동이 빨간색으로 깜박거립니다.

워크플로우 상태가 빨간색으로 바뀌고 오류가 로그에 기록됩니다.

일시 중지되지 않고 오류 없이 계속 실행되도록 워크플로우를 구성할 수 있습니다. To do this, go to the workflow properties via the ![](assets/edit_darkgrey-24px.png) button and, in the **[!UICONTROL Execution]** section, select the **Ignore** option in the **In case of error** field.

이 경우 잘못된 작업이 취소됩니다. 이 모드는 나중에 작업을 다시 시도하도록 디자인된 워크플로우에 특히 적합합니다 (정기적인 작업).

>[!NOTE]
>
>각 활동에 대해 이 구성을 개별적으로 적용할 수 있습니다. To do this, select an activity and open it using the quick action ![](assets/edit_darkgrey-24px.png). Then select the error management mode in the **Execution options** tab. [활동 실행 옵션을 참조하십시오](../../automating/using/executing-a-workflow.md#activity-execution-options).

The **[!UICONTROL Execution]** section of the workflow properties also allows you to define a number of **[!UICONTROL Consecutive errors]** that are authorized before the workflow execution is automatically suspended. 이 수에 도달하지 않으면 잘못된 요소가 무시되고 다른 워크플로우 분기는 정상적으로 실행됩니다. 이 수에 도달하면 워크플로우가 일시 중단되고 워크플로우 관리자에 자동으로 알림 (이메일 및 인앱 알림) 이 전달됩니다. [워크플로우 속성](../../automating/using/executing-a-workflow.md#workflow-properties) 및 [Adobe Campaign 알림을 참조하십시오](../../administration/using/sending-internal-notifications.md).

관리자는 워크플로우의 실행 속성에 관리자를 정의할 수도 있습니다.

## Workflow properties {#workflow-properties}

To modify a workflow's execution options, use the ![](assets/edit_darkgrey-24px.png) button to access the workflow properties and select the **[!UICONTROL Execution]** section.

**[!UICONTROL Default affinity]** 이 필드를 사용하면 워크플로우나 워크플로우 활동이 특정 컴퓨터에서 실행되도록 강제할 수 있습니다.

**[!UICONTROL History in days]** 필드에서 내역을 삭제해야 하는 기간을 지정합니다.

You can choose to check the **[!UICONTROL Save SQL queries in the log]** and **[!UICONTROL Execute in the engine (do not use in production)]** options if necessary.

Check the **[!UICONTROL Keep interim results]** option if you would like to be able to view the detail of transitions. 경고: 이 옵션을 선택하면 워크플로우 실행이 상당히 느려질 수 있습니다.

**[!UICONTROL Severity]** 이 필드를 사용하여 Adobe Campaign 인스턴스에서 워크플로우 실행을 위한 우선 순위 수준을 지정할 수 있습니다. 중요한 워크플로우가 먼저 실행될 것입니다.

The **[!UICONTROL Supervisors]** field is where you can define the group of people to notify (email and in-app notification) if the workflow encounters an error. 정의된 그룹이 없으면 아무도 알림을 받지 않습니다. For more on Adobe Campaign notifications, refer to [Adobe Campaign notifications](../../administration/using/sending-internal-notifications.md).

**[!UICONTROL In case of error]** 이 필드에서 활동에 오류가 발생하면 수행해야 할 작업을 지정할 수 있습니다. 다음 두 가지 옵션을 사용할 수 있습니다.

* **프로세스 일시 중단**: 워크플로우는 자동으로 일시 중단됩니다. The workflow status is then **Erroneous** and the color associated turns red. 문제가 해결되면 워크플로우를 다시 시작합니다.
* **무시**: 활동은 실행되지 않으며, 그 결과 팔로우하는 활동이 모두 동일합니다 (동일한 분기). 반복되는 작업에 유용합니다. 분기에 스케줄러가 업스트림 배치된 경우 다음 실행 날짜에 트리거해야 합니다.

   By selecting this option, you can also define a number of **[!UICONTROL Consecutive errors]** that are authorized:

   * If the number specified is **[!UICONTROL 0]**, or as long as the number specified is not reached, activities that encounter errors are ignored. 다른 워크플로우 분기는 정상적으로 실행됩니다.
   * If the number specified is reached, the whole of the workflow is suspended and becomes **[!UICONTROL Erroneous]**. 관리자가 정의된 경우 이메일로 자동으로 알림을 받습니다.

![](assets/wkf_execution_6.png)

## Activity properties {#activity-properties}

### General properties of an activity {#general-properties-of-an-activity}

Each activity has a **[!UICONTROL Properties]** tab. 이 탭에서는 활동의 일반 매개 변수, 특히 레이블 및 ID를 수정할 수 있습니다. 이 탭은 선택 사항입니다.

### Managing an activity's outbound transitions {#managing-an-activity-s-outbound-transitions}

기본적으로 특정 활동에는 아웃바운드 전환이 없습니다. **[!UICONTROL Transitions]** 탭 또는 활동 **[!UICONTROL Properties]** 탭에서 하나를 추가하여 동일한 워크플로우에서 다른 프로세스를 적용할 수 있습니다.

활동에 따라 다음과 같은 여러 유형의 아웃바운드 전환을 추가할 수 있습니다.

* 표준 전환: 활동에 의해 계산된 인구
* 인구 없는 전환: 이러한 유형의 아웃바운드 전환을 추가하여 워크플로우를 계속할 수 있으며, 모집단을 포함하지 않아 시스템에 불필요한 공간을 사용할 수 없습니다.
* 거부: 모집단이 거부되었습니다. 예를 들어, 활동의 인바운드 데이터가 잘못되었거나 불완전하므로 처리할 수 없는 경우입니다.
* 보완: 활동을 실행한 후 남은 모집단. 예를 들어 세그멘테이션 활동이 인바운드 인구의 비율만 저장하도록 구성된 경우

If applicable, specify a **[!UICONTROL Segment code]** for the activity's outbound transition. 이 세그먼트 코드를 사용하면 타겟 모집단의 하위 집합이 어디에서 오는지 식별하고 나중에 메시지 개인화 목적을 위해 제공할 수 있습니다.

### Activity execution options {#activity-execution-options}

In the activity's properties screen, there is an **[!UICONTROL Advanced options]** tab that lets you define the activity's execution mode and behavior in case of errors.

To access these options, select an activity in a workflow, then open it using the ![](assets/edit_darkgrey-24px.png) button from the action bar.

![](assets/wkf_advanced_parameters.png)

**[!UICONTROL Execution]** 필드를 사용하여 작업이 시작될 때 수행되는 작업을 정의할 수 있습니다. 다음과 같은 세 가지 옵션이 있습니다.

* **일반**: 활동은 정상적으로 실행됩니다.
* **활성화하지만 실행하지**&#x200B;마십시오. 활동이 일시 중지되고 이후에 이어지는 모든 프로세스가 진행됩니다. 이렇게 하면 작업이 시작될 때 표시되기를 원할 경우 유용합니다.
* **활성화하지 마십시오. 활동이 실행되지 않으며 같은 분기 내의 모든 활동도 함께 수행되지는 않습니다.**

**[!UICONTROL In case of error]** 이 필드에서 활동에 오류가 발생하면 수행해야 할 작업을 지정할 수 있습니다. 다음 두 가지 옵션을 사용할 수 있습니다.

* **프로세스 일시 중단**: 워크플로우는 자동으로 일시 중단됩니다. The workflow status is then **Erroneous** and the color associated turns red. 문제가 해결되면 워크플로우를 다시 시작합니다.
* **무시**: 활동은 실행되지 않으며, 그 결과 팔로우하는 활동이 모두 동일합니다 (동일한 분기). 반복되는 작업에 유용합니다. 분기에 스케줄러가 업스트림 배치된 경우 다음 실행 날짜에 트리거해야 합니다.

The **[!UICONTROL Behavior]** field allows you to define the procedure to follow if asynchronous tasks are used. 다음 두 가지 옵션을 사용할 수 있습니다.

* **허가된 여러 작업**: 첫 번째 작업이 완료되지 않았더라도 동시에 여러 작업을 실행할 수 있습니다.
* **현재 작업에는 우선 순위가**&#x200B;있습니다. 작업이 진행 중이면 우선 순위가 높습니다. 한 작업이 계속 진행 중이면 다른 작업이 실행되지 않습니다.

**[!UICONTROL Max. execution duration]** 필드에서 "30 초" 또는 "1 H" 와 같은 지속 기간을 지정할 수 있습니다. 지정된 기간이 경과한 후 활동이 완료되지 않으면 경고가 트리거됩니다. 워크플로우 기능에 영향을 주지 않습니다.

**[!UICONTROL Affinity]** 이 필드를 사용하면 워크플로우나 워크플로우 활동이 특정 컴퓨터에서 실행되도록 강제할 수 있습니다. 이렇게 하려면 문제의 워크플로우 또는 활동에 대해 하나 또는 여러 개의 친화성을 지정해야 합니다.

**[!UICONTROL Time zone]** 이 필드에서 활동의 시간대를 선택할 수 있습니다. Adobe Campaign를 사용하면 동일한 인스턴스에서 여러 국가 간의 시간 차이를 관리할 수 있습니다. 적용된 설정은 인스턴스를 만들 때 구성됩니다.

**댓글** 필드는 메모를 추가할 수 있는 무료 필드입니다.
