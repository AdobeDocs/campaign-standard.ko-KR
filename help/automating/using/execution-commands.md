---
title: 실행 명령
description: 워크플로우 실행 명령을 사용하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: ff02b74e-53e8-49c6-bf8e-0c729eaa7d25
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: workflow-general-operation
discoiquuid: 906c85ea-83b7-4268-86da-cd353f1dc591
context-tags: workflow,overview;workflow,main
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 2%

---


# 실행 명령 {#execution-commands}

작업 표시줄의 아이콘을 사용하면 워크플로우 실행을 시작, 추적 및 수정할 수 있습니다. 작업 [막대를 참조하십시오](../../automating/using/workflow-interface.md#action-bar).

![](assets/wkf_execution_2.png)

사용 가능한 작업은 다음과 같습니다.

**시작**

이 ![](assets/play_darkgrey-24px.png) 버튼은 워크플로우 실행을 시작으로 **진행** 중(파란색) 상태가 됩니다. 워크플로가 일시 중지된 경우 다시 시작되거나, 시작된 후 초기 활동이 활성화됩니다.

>[!NOTE]
>
>시작은 비동기 프로세스입니다.요청이 저장되고 워크플로 실행 엔진에서 가능한 한 빨리 처리됩니다.

**일시 정지**

이 ![](assets/pause_darkgrey-24px.png) 단추는 실행을 일시 중지합니다. 워크플로우는 **경고** (노란색) 상태를 수행합니다. 다시 시작될 때까지 새 활동이 활성화되지는 않지만 진행 중인 작업이 일시 중단되지 않습니다.

**정지**

이 ![](assets/stop_darkgrey-24px.png) 단추는 실행 중인 워크플로우를 중단하고, 그런 다음 **완료** (녹색) 상태가 됩니다. 진행 중인 작업이 가능한 경우 중단되고 진행 중인 가져오기 또는 SQL 쿼리가 즉시 취소됩니다. 워크플로우가 중지된 동일한 위치에서 다시 시작할 수 없습니다.

**다시 시작**

이 ![](assets/pauseplay_darkgrey-24px.png) 단추에는 워크플로를 중지한 다음 다시 시작하는 작업이 포함됩니다. 대부분의 경우 빠르게 다시 시작할 수 있습니다. 또한 정지 실행 시 버튼을 사용할 때만 사용할 수 있으므로, 다시 시작을 자동화하는 데 일정 시간이 걸립니다. 이때 정지가 유효한 경우에만 ![](assets/play_darkgrey-24px.png) 단추를 사용할 수 있습니다.

워크플로우에서 하나 이상의 활동을 선택하면 수행할 수 있는 다른 작업이 있습니다. 예:

**즉각적인 실행**

이 ![](assets/pending_darkgrey-24px.png) 단추는 가능한 한 빨리 선택된 보류 중인 활동을 시작합니다.

**일반 실행**

이 ![](assets/check_darkgrey-24px.png) 단추는 일시 중지되거나 비활성화된 활동을 다시 활성화합니다.

**실행이 일시 중단됨**

이 ![](assets/check_pause_darkgrey-24px.png) 단추는 선택한 활동에서 워크플로우를 일시 중지합니다.이 작업은 물론 후속 작업(동일한 분기)을 수행하는 모든 작업이 실행되지 않습니다.

**실행 안 함**

이 ![](assets/checkdisable.png) 단추는 선택한 활동을 비활성화합니다.

>[!NOTE]
>
>빠른 작업을 사용하면 특정 활동과 관련된 다양한 작업에 액세스할 수 있으며 활동이 선택되면 나타납니다.
