---
title: 활동 속성 관리
description: 워크플로우 활동 속성을 관리하는 방법을 알아봅니다.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
context-tags: workflow,overview;workflow,main
feature: Workflows
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: 9c47ef72-59af-4b55-8e65-d8f687fb5fbe
source-git-commit: b3f3309a252971dc527d44913b7918abeea704d9
workflow-type: tm+mt
source-wordcount: '675'
ht-degree: 0%

---

# 활동 속성 관리 {#activity-properties}

## 활동의 전역 속성 {#global-properties-of-an-activity}

각 활동에는 **[!UICONTROL General]** 탭이 있으며, 이를 통해 해당 활동과 관련된 일반 매개 변수를 수정할 수 있습니다.

![](assets/activity-properties.png)

**[!UICONTROL Properties]** 탭에서는 활동의 전역 매개 변수(특히 레이블 및 ID)를 수정할 수 있습니다. 이 탭 구성은 선택 사항입니다.

![](assets/activity-properties2.png)

## 활동의 아웃바운드 전환 관리 {#managing-an-activity-s-outbound-transitions}

기본적으로 특정 활동에는 아웃바운드 전환이 없습니다. **[!UICONTROL Transitions]** 탭 또는 활동의 **[!UICONTROL Properties]** 탭에서 하나를 추가하여 동일한 워크플로우에서 모집단에 다른 프로세스를 적용할 수 있습니다.

활동에 따라 여러 유형의 아웃바운드 전환을 추가할 수 있습니다.

* **표준 전환**: 활동에서 계산한 모집단
* **모집단 없이 전환**: 이 아웃바운드 전환 유형은 워크플로우를 계속하기 위해 추가할 수 있으며 시스템에서 불필요한 공간을 사용하지 않는 모집단을 포함하지 않습니다.
* **거부**: 모집단이 거부되었습니다. 예를 들어 활동의 인바운드 데이터가 잘못되었거나 불완전하여 처리할 수 없는 경우.
* **보충**: 활동을 실행한 후 남은 모집단입니다. 예를 들어 세분화 활동이 인바운드 모집단의 백분율만 저장하도록 구성된 경우.

해당하는 경우 활동의 아웃바운드 전환에 대해 **[!UICONTROL Segment code]**&#x200B;을(를) 지정합니다. 이 세그먼트 코드를 사용하면 대상 모집단의 하위 집합이 나오는 위치를 식별할 수 있으며, 나중에 메시지 개인화 목적으로 제공될 수도 있습니다.

## 활동 실행 옵션 {#activity-execution-options}

활동의 속성 화면에는 오류 발생 시 활동의 실행 모드 및 동작을 정의할 수 있는 **[!UICONTROL Advanced options]** 탭이 있습니다.

이러한 옵션에 액세스하려면 워크플로우에서 활동을 선택한 다음 작업 표시줄의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 활동을 엽니다.

![](assets/wkf_advanced_parameters.png)

**[!UICONTROL Execution]** 필드를 사용하면 작업을 시작할 때 수행할 작업을 정의할 수 있습니다. 다음 세 가지 옵션을 사용할 수 있습니다.

* **보통**: 활동이 정상적으로 실행됩니다.
* **활성화하지만 실행하지 않음**: 활동이 일시 중지되므로 이후 프로세스도 일시 중지됩니다. 이 기능은 작업이 시작될 때 참석하려는 경우 유용할 수 있습니다.
* **활성화하지 않음**: 활동이 실행되지 않으므로 동일한 분기에서 뒤따르는 모든 활동도 실행되지 않습니다.

**[!UICONTROL In case of error]** 필드를 사용하면 활동에 오류가 발생할 경우 수행할 작업을 지정할 수 있습니다. 다음 두 가지 옵션을 사용할 수 있습니다.

* **프로세스 일시 중단**: 워크플로가 자동으로 일시 중단됩니다. 그러면 워크플로 상태가 **잘못됨**&#x200B;이고 연결된 색상은 빨간색으로 바뀝니다. 문제가 해결되면 워크플로우를 다시 시작합니다.
* **무시**: 활동이 실행되지 않으며 따라서 해당 활동 뒤에 오는 활동도 동일한 분기에 없습니다. 이는 반복 작업에 유용할 수 있습니다. 분기에 업스트림에 스케줄러가 있는 경우 다음 실행 날짜에 트리거되어야 합니다.

**[!UICONTROL Behavior]** 필드를 사용하면 비동기 작업이 사용되는 경우 따라야 할 프로시저를 정의할 수 있습니다. 다음 두 가지 옵션을 사용할 수 있습니다.

* **여러 작업이 승인됨**: 첫 번째 작업이 완료되지 않았더라도 여러 작업을 동시에 실행할 수 있습니다.
* **현재 작업에 우선 순위가 있습니다**: 작업이 진행 중이면 우선 순위가 지정됩니다. 하나의 작업이 아직 진행 중이면 다른 작업은 실행되지 않습니다.

**[!UICONTROL Max. execution duration]** 필드를 사용하면 &quot;30s&quot; 또는 &quot;1h&quot;와 같은 기간을 지정할 수 있습니다. 지정된 기간이 경과한 후 활동이 완료되지 않으면 경고가 트리거됩니다. 이는 워크플로의 작동 방식에는 영향을 주지 않습니다.

**[!UICONTROL Affinity]** 필드를 사용하면 워크플로 또는 워크플로 활동을 특정 컴퓨터에서 강제로 실행할 수 있습니다. 이렇게 하려면 해당 워크플로우 또는 활동에 대해 하나 또는 여러 선호도를 지정해야 합니다.

**[!UICONTROL Time zone]** 필드를 사용하면 활동의 시간대를 선택할 수 있습니다. Adobe Campaign을 사용하면 동일한 인스턴스에서 여러 국가 간의 시간 차이를 관리할 수 있습니다. 적용된 설정은 인스턴스가 생성될 때 구성됩니다.

>[!NOTE]
>
>기본적으로 시간대를 선택하지 않으면 활동에서 워크플로우 속성에 정의된 시간대를 사용합니다.

**댓글** 필드는 메모를 추가할 수 있는 무료 필드입니다.
