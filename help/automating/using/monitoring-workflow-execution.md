---
title: 워크플로우 실행 모니터링
description: 워크플로우 실행을 모니터링하는 방법을 알아봅니다.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
context-tags: workflow,overview;workflow,main
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: d2ce702b-92d1-4b94-bd47-34ef46a8bd9f
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 4%

---

# 워크플로우 실행 모니터링 {#monitoring}

## 워크플로우 로그 및 작업 {#workflow-log-and-tasks}

다음 ![](assets/printpreview_darkgrey-24px.png) 아이콘은 워크플로우 로그 및 작업 메뉴를 엽니다.

워크플로 내역은 워크플로 실행 옵션에 지정된 기간 동안 저장됩니다( 참조). [워크플로우 속성](../../automating/using/managing-execution-options.md)). 따라서 이 기간 동안에는 다시 시작한 후에도 모든 메시지가 저장됩니다. 이전 실행에서 메시지를 저장하지 않으려면 ![](assets/delete_darkgrey-24px.png) 단추를 클릭합니다.

다음 **[!UICONTROL Log]** 탭에는 모든 활동 또는 선택한 활동의 실행 기록이 들어 있습니다. 시간 순서대로 수행된 작업과 실행 오류를 색인화합니다.

![](assets/wkf_execution_4.png)

다음 **[!UICONTROL Tasks]** 탭에서는 활동의 실행 시퀀싱에 대해 자세히 설명합니다. 자세한 내용을 보려면 작업을 클릭하십시오.

![](assets/wkf_execution_5.png)

이 두 목록에는

* 적용된 필터에 따른 총 활동 수를 보려면 카운터를 클릭합니다. 목록에 있는 요소의 수가 30개 미만인 경우 카운터가 기본적으로 표시됩니다.
* 다음 **[!UICONTROL Configure list]** 버튼을 사용하여 표시되는 정보를 선택하고, 열 순서를 정의하고, 목록을 정렬할 수 있습니다.
* 필터를 사용하여 필요한 정보를 보다 신속하게 찾을 수 있습니다. 검색 필드를 사용하여 워크플로우 활동 이름(예: &quot;쿼리&quot;) 및 로그에서 특정 텍스트를 찾습니다.

## 오류 관리 {#error-management}

오류가 발생하면 워크플로우가 일시 중지되고 오류가 발생했을 때 실행 중이던 활동이 빨간색으로 깜박입니다.

워크플로우 상태가 빨간색으로 바뀌고 오류가 로그에 기록됩니다.

일시 중지하지 않고 오류 없이 계속 실행되도록 워크플로우를 구성할 수 있습니다. 이렇게 하려면 다음을 통해 워크플로우 속성으로 이동합니다. ![](assets/edit_darkgrey-24px.png) 단추 및, **[!UICONTROL Execution]** 섹션에서 **무시** 의 옵션 **오류가 있는 경우** 필드.

이 경우 잘못된 작업이 중단됩니다. 이 모드는 나중에 작업을 다시 시도하도록 설계된 워크플로(주기적 작업)에 특히 적합합니다.

>[!NOTE]
>
>각 활동에 대해 개별적으로 이 구성을 적용할 수 있습니다. 이렇게 하려면 활동을 선택하고 빠른 작업을 사용하여 활동을 엽니다 ![](assets/edit_darkgrey-24px.png). 그런 다음 **실행 옵션** 탭. 다음을 참조하십시오 [활동 실행 옵션](../../automating/using/activity-properties.md).

다음에서 [워크플로우 속성](../../automating/using/managing-execution-options.md), 오류 관리와 관련된 추가 옵션을 사용할 수 있습니다.

![](assets/wkf_execution_error.png)

가능한 옵션은 다음과 같습니다.

* **[!UICONTROL Supervisors]**: 워크플로우에 오류가 발생하는 경우 알릴 사람 그룹(이메일 및 인앱 알림)을 정의할 수 있습니다. 정의된 그룹이 없으면 아무도 알림을 받지 않습니다. Adobe Campaign 알림에 대한 자세한 내용은 [Adobe Campaign 알림](../../administration/using/sending-internal-notifications.md)을 참조하세요.

* **[!UICONTROL In case of error]**: 활동에 오류가 발생하는 경우 수행할 작업을 지정할 수 있습니다. 다음 두 가지 옵션을 사용할 수 있습니다.

   * **프로세스 일시 중단**: 워크플로우가 자동으로 일시 중단됩니다. 그러면 워크플로우 상태가 됩니다. **잘못됨** 연관된 색상이 빨간색으로 바뀝니다. 문제가 해결되면 워크플로우를 다시 시작합니다.
   * **무시**: 활동이 실행되지 않으며, 그 결과 해당 활동 뒤에 오는 활동도 동일한 분기에서 모두 실행되지 않습니다. 이는 반복 작업에 유용할 수 있습니다. 분기에 업스트림에 스케줄러가 있는 경우 다음 실행 날짜에 트리거되어야 합니다.

* **[!UICONTROL Consecutive errors]** : 워크플로우 실행이 자동으로 일시 중단되기 전에 승인된 여러 연속 오류를 정의할 수 있습니다.

   * 지정한 수가 **[!UICONTROL 0]**, 또는 지정된 수에 도달하지 않는 한 오류가 발생하는 활동은 무시됩니다. 다른 워크플로우 분기는 정상적으로 실행됩니다.

   * 지정한 수에 도달하면 전체 워크플로우가 일시 중단되고 **[!UICONTROL Erroneous]**. 감독자가 정의된 경우 전자 메일로 자동으로 알림이 전송됩니다. [Adobe Campaign 알림](../../administration/using/sending-internal-notifications.md)을 참조하십시오.
