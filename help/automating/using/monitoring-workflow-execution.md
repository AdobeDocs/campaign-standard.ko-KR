---
solution: Campaign Standard
product: campaign
title: 워크플로우 실행 모니터링
description: 워크플로우 실행을 모니터링하는 방법을 알아봅니다.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
context-tags: workflow,overview;workflow,main
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 3%

---


# 워크플로우 실행 모니터링 {#monitoring}

## 워크플로우 로그 및 작업 {#workflow-log-and-tasks}

이 ![](assets/printpreview_darkgrey-24px.png) 아이콘은 워크플로우 로그 및 작업 메뉴를 엽니다.

워크플로우 내역은 워크플로우 실행 옵션에 지정된 기간 동안 저장됩니다(워크플로우 속성 참조 [](../../automating/using/managing-execution-options.md)). 이 기간 동안 다시 시작한 후에도 모든 메시지가 저장됩니다. 이전 실행의 메시지를 저장하지 않으려면 ![](assets/delete_darkgrey-24px.png) 단추를 클릭하여 내역을 삭제해야 합니다.

이 **[!UICONTROL Log]** 탭에는 모든 활동 또는 선택한 활동의 실행 내역이 포함되어 있습니다. 시간 순서대로 수행된 작업과 실행 오류를 색인화합니다.

![](assets/wkf_execution_4.png)

The **[!UICONTROL Tasks]** tab details the execution sequencing of the activities. 작업을 클릭하여 자세한 내용을 확인하십시오.

![](assets/wkf_execution_5.png)

다음 두 가지 목록에서 다음을 수행합니다.

* 적용된 필터에 따라 총 활동 수를 보려면 카운터를 클릭합니다. 목록의 요소 수가 30개 미만인 경우 기본적으로 카운터가 표시됩니다.
* 이 **[!UICONTROL Configure list]** 단추를 사용하면 표시되는 정보를 선택하고 열 순서를 정의하며 목록을 정렬할 수 있습니다.
* 필터를 사용하여 필요한 정보를 빠르게 찾을 수 있습니다. 검색 필드를 사용하여 워크플로우 활동 이름의 특정 텍스트를 찾습니다(예:&quot;query&quot;) 및 로그

## Error management {#error-management}

오류가 발생하면 워크플로우가 일시 중지되고 오류가 발생했을 때 실행 중인 활동이 빨간색으로 표시됩니다.

워크플로우 상태가 빨간색으로 바뀌고 오류가 로그에 기록됩니다.

일시 중지되지 않고 오류 없이 계속 실행되도록 워크플로우를 구성할 수 있습니다. 이 작업을 수행하려면 ![](assets/edit_darkgrey-24px.png) 단추를 통해 워크플로우 속성으로 이동하고 **[!UICONTROL Execution]** 섹션에서 오류 **의 경우 필드** 에서 **무시** 옵션을 선택합니다.

이 경우 잘못된 작업이 중단됩니다. 이 모드는 나중에 작업을 다시 시도하도록 설계된 워크플로우(주기적 작업)에 특히 적합합니다.

>[!NOTE]
>
>각 활동에 대해 이 구성을 개별적으로 적용할 수 있습니다. 이렇게 하려면 활동을 선택하고 빠른 작업을 사용하여 엽니다 ![](assets/edit_darkgrey-24px.png). 그런 다음 실행 옵션 **탭에서 오류 관리 모드를** 선택합니다. 활동 [실행 옵션을 참조하십시오](../../automating/using/activity-properties.md).

워크플로우 [속성에서](../../automating/using/managing-execution-options.md)오류 관리와 관련된 추가 옵션을 사용할 수 있습니다.

![](assets/wkf_execution_error.png)

가능한 옵션은 다음과 같습니다.

* **[!UICONTROL Supervisors]**:워크플로우에 오류가 발생하면 알릴 사람 그룹(이메일 및 인앱 알림)을 정의할 수 있습니다. 정의된 그룹이 없으면 아무도 알림을 받지 않습니다. Adobe Campaign 알림에 대한 자세한 내용은 [Adobe Campaign 알림을 참조하십시오](../../administration/using/sending-internal-notifications.md).

* **[!UICONTROL In case of error]**:활동에 오류가 발생하는 경우 수행할 작업을 지정할 수 있습니다. 다음 두 가지 옵션을 사용할 수 있습니다.

   * **프로세스 일시 중단**:워크플로우가 자동으로 일시 중단됩니다. 그러면 워크플로우 상태가 **잘못됨** 으로 표시되고 연결된 색상이 빨간색으로 표시됩니다. 문제가 해결되면 워크플로우를 다시 시작합니다.
   * **무시**:활동이 실행되지 않으며, 따라서 동일한 분기에 따라 어떤 활동도 실행되지 않습니다. 이는 반복되는 작업에 유용할 수 있습니다. 분기에 업스트림 배치 스케줄러가 있는 경우 다음 실행 날짜에 트리거됩니다.

* **[!UICONTROL Consecutive errors]** :워크플로우 실행이 자동으로 일시 중단되기 전에 인증되는 다수의 연속 오류를 정의할 수 있습니다.

   * 지정된 숫자가 **[!UICONTROL 0]**&#x200B;되거나 지정된 수에 도달하지 않으면 오류가 발생하는 활동이 무시됩니다. 다른 워크플로우 분기는 정상적으로 실행됩니다.

   * 지정된 수에 도달하면 전체 워크플로우가 일시 중단되어 종료됩니다 **[!UICONTROL Erroneous]**. 감독자가 정의된 경우 자동으로 이메일로 통보를 받게 됩니다. [Adobe Campaign 알림](../../administration/using/sending-internal-notifications.md)을 참조하십시오.
