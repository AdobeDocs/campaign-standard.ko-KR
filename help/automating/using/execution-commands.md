---
title: 실행 명령
description: 워크플로우 실행 명령을 사용하는 방법을 알아봅니다.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
context-tags: workflow,overview;workflow,main
feature: Workflows
role: Data Architect
level: Beginner
exl-id: fddd88b1-603a-465b-b5e7-624632c0d5cd
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 1%

---

# 실행 명령 {#execution-commands}

작업 표시줄의 아이콘을 사용하면 워크플로우 실행을 시작, 추적 및 수정할 수 있습니다. [작업 표시줄](../../automating/using/workflow-interface.md#action-bar)을 참조하세요.

![](assets/wkf_execution_2.png)

사용 가능한 작업은 다음과 같습니다.

**시작**

![](assets/play_darkgrey-24px.png) 단추는 워크플로 실행을 시작하고 **진행 중**(파란색) 상태가 됩니다. 워크플로우가 일시 중지된 경우에는 다시 시작되고, 그렇지 않으면 시작되고 초기 활동이 활성화됩니다.

>[!NOTE]
>
>시작은 비동기 프로세스입니다. 요청이 저장되고 워크플로우 실행 엔진에 의해 가능한 한 빨리 처리됩니다.

**일시 중지**

![](assets/pause_darkgrey-24px.png) 단추는 실행을 일시 중지합니다. 워크플로는 **경고**(노란색) 상태로 전환됩니다. 다시 시작될 때까지 새 활동이 활성화되지 않지만 진행 중인 작업은 중단되지 않습니다.

**중지**

![](assets/stop_darkgrey-24px.png) 단추를 사용하면 실행 중인 워크플로우가 중지되어 **완료됨**(녹색) 상태가 됩니다. 진행 중인 작업은 가능한 경우 중단되며, 진행 중인 가져오기 또는 SQL 쿼리가 즉시 취소됩니다. 워크플로우가 중지된 동일한 위치에서 다시 시작할 수 없습니다.

**다시 시작**

![](assets/pauseplay_darkgrey-24px.png) 단추에는 워크플로우를 중지한 다음 다시 시작합니다. 대부분의 경우 이를 통해 보다 빠르게 다시 시작할 수 있습니다. ![](assets/play_darkgrey-24px.png) 단추는 중지가 유효한 경우에만 사용할 수 있으므로 중지하는 데 일정 시간이 걸리면 다시 시작을 자동화하는 것도 유용할 수 있습니다.

워크플로우에서 하나 이상의 활동을 선택하면 다음과 같이 수행할 수 있는 다른 작업이 있습니다.

**즉시 실행**

![](assets/pending_darkgrey-24px.png) 단추는 선택한 보류 중인 활동을 가능한 한 빨리 시작합니다.

**정상 실행**

![](assets/check_darkgrey-24px.png) 단추를 사용하면 일시 중지되었거나 비활성화된 활동이 다시 활성화됩니다.

**실행 일시 중단**

![](assets/check_pause_darkgrey-24px.png) 단추를 사용하면 선택한 활동에서 워크플로우가 일시 중지됩니다. 이 작업은 물론 이 작업을 따르는 모든 작업(동일한 분기)도 실행되지 않습니다.

**실행 안 함**

![](assets/checkdisable.png) 단추를 사용하면 선택한 모든 활동이 비활성화됩니다.

>[!NOTE]
>
>빠른 작업 을 사용하면 한 가지 특정 활동에 대한 다양한 작업에 액세스할 수 있으며 활동을 선택할 때 표시됩니다.
