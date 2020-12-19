---
solution: Campaign Standard
product: campaign
title: 실행 명령
description: 워크플로우 실행 명령을 사용하는 방법을 알아봅니다.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
context-tags: workflow,overview;workflow,main
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 2%

---


# 실행 명령 {#execution-commands}

작업 표시줄의 아이콘을 사용하여 워크플로우의 실행을 시작, 추적 및 수정할 수 있습니다. [작업 표시줄](../../automating/using/workflow-interface.md#action-bar)을 참조하십시오.

![](assets/wkf_execution_2.png)

사용 가능한 작업은 다음과 같습니다.

**시작**

![](assets/play_darkgrey-24px.png) 단추는 워크플로우 실행을 시작한 다음 **진행 중**(파란색) 상태를 사용합니다. 워크플로가 일시 중지된 경우 다시 시작되거나, 다시 시작된 후 초기 활동이 활성화됩니다.

>[!NOTE]
>
>시작은 비동기 프로세스입니다.요청이 저장되고 워크플로 실행 엔진에서 가능한 한 빨리 처리됩니다.

**일시 정지**

![](assets/pause_darkgrey-24px.png) 단추는 실행을 일시 중지합니다. 워크플로우는 **경고**(노란색) 상태를 사용합니다. 새 활동을 다시 시작할 때까지 활성화하지 않지만 진행 중인 작업이 일시 중단되지 않습니다.

**정지**

![](assets/stop_darkgrey-24px.png) 단추를 사용하면 실행 중인 워크플로우가 정지되며, 이 단추는 **Finished**(녹색) 상태가 됩니다. 진행 중인 작업이 가능하면 중단되고 진행 중인 가져오기 또는 SQL 쿼리가 즉시 취소됩니다. 워크플로우가 중지된 동일한 위치에서 다시 시작할 수 없습니다.

**다시 시작**

![](assets/pauseplay_darkgrey-24px.png) 버튼은 작업을 중지한 다음 워크플로우를 다시 시작합니다. 대부분의 경우 빠르게 다시 시작할 수 있습니다. 또한 ![](assets/play_darkgrey-24px.png) 단추는 중지가 유효할 때만 사용할 수 있기 때문에 중지는 어느 정도의 시간이 소요되면 재시작을 자동화하는 데에도 유용합니다.

워크플로우에서 하나 이상의 활동을 선택하면 다음과 같이 수행할 수 있는 다른 작업이 있습니다.

**즉각적인 실행**

![](assets/pending_darkgrey-24px.png) 단추는 가능한 한 빨리 선택된 보류 중인 활동을 시작합니다.

**일반 실행**

![](assets/check_darkgrey-24px.png) 단추를 클릭하면 일시 중지되거나 비활성화된 활동이 다시 활성화됩니다.

**실행이 일시 중단됨**

![](assets/check_pause_darkgrey-24px.png) 단추는 선택한 활동에서 워크플로우를 일시 중지합니다.이 작업은 물론 후속 작업(동일한 분기에 있음)을 수행하는 모든 작업이 실행되지 않습니다.

**실행 안 함**

![](assets/checkdisable.png) 단추는 선택한 모든 활동을 비활성화합니다.

>[!NOTE]
>
>빠른 작업을 사용하면 특정 활동과 관련된 여러 작업에 액세스할 수 있으며 활동이 선택되면 나타납니다.
