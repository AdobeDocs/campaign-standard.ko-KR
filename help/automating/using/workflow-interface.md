---
title: 워크플로우 인터페이스
seo-title: 워크플로우 인터페이스
description: 워크플로우 인터페이스
seo-description: 워크플로우를 생성, 편집 및 실행하는 인터페이스와 옵션에 대해 알아보십시오.
page-status-flag: 정품 인증 안 함
uuid: AAFE 33 ED-FA 07-4 DD 9-825 E -242099334 F 1 A
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 워크플로우 및 데이터 관리
discoiquuid: 147 fbb 0 d -17 d 2-444 b-a 215-9 ad 14179 c 549
context-tags: workflow, main; 워크플로우, 개요
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: ff0b995533f34dd8eab7a9a82feaab3ceed4ff29

---


# Workflow interface{#workflow-interface}

캠페인 및 프로그램에서 전체 프로세스를 관리할 수 있는 워크플로우를 만들 수 있습니다.

워크플로우 편집 화면은 다음 요소로 구성됩니다.

* The [Palette](../../automating/using/workflow-interface.md#palette), which references the available activities
* The [Workspace](../../automating/using/workflow-interface.md#workspace), in which the activities are configured and organized
* [작업 막대](../../automating/using/workflow-interface.md#action-bar)- 워크플로우 및/또는 해당 구성 요소와 상호 작용할 수 있는 단추로 구성됩니다.
* The [Quick actions](../../automating/using/workflow-interface.md#quick-actions), which appear around a selected activity, allow you to interact with it.

![](assets/wkf_overview.png)

## Palette {#palette}

팔레트는 화면의 왼쪽에 있습니다. 사용 가능한 모든 활동은 다음과 같이 여러 카테고리로 분류됩니다.

* [타깃팅](../../automating/using/about-targeting-activities.md): 타깃팅, 인구 데이터 조작 및 활동 필터링과 관련된 활동
* [실행](../../automating/using/about-execution-activities.md): 워크플로우 구성 및 실행과 관련된 활동
* [채널](../../automating/using/about-channel-activities.md): 사용 가능한 서로 다른 통신 채널을 나타내는 활동
* [데이터 관리 (ETL)](../../automating/using/about-data-management-activities.md): 데이터 조작 관련 활동

워크플로우에서 팔레트의 활동을 사용하려면 작업 공간으로 드래그하여 놓습니다.

워크플로우를 시작하기 전에 팔레트에서 추가된 각 활동을 구성해야 합니다.

![](assets/workflow_palette.png)

## Workspace {#workspace}

작업 영역은 워크플로우 편집기의 가운데 영역입니다. 활동을 삭제하고 전환을 사용하여 연결하고 구성할 수 있는 이 영역에 있습니다.

두 활동을 연결하려면, 연결할 때까지 첫 활동에서 다음 활동까지 화살표 끝을 이동합니다. 활동을 이전 활동에 연결하기 위해 뒤로 화살표 지점을 이동할 수도 있습니다. 활동을 이동하면 계속 연결되어 있습니다.

데이터 처리 활동에 중간 모집단이 포함된 전환 You can access them if you check the **[!UICONTROL Keep interim results]** option in the **[!UICONTROL Execution]** section of the workflow properties.

활동을 선택하면 활동에 빠른 작업이 나타나 활동과 상호 작용할 수 있습니다. For example, to configure an activity, select it then open it using the ![](assets/edit_darkgrey-24px_table.png) button in the quick actions.

특정 함수는 작업 공간에서만 활성화됩니다.

* 여러 활동 및 전환 효과를 선택할 수 있습니다.
* **Ctrl** + 왼쪽 화살표를 눌러 여러 활동 및/또는 전환을 선택합니다.
* **Enter** 키를 눌러 현재 선택한 활동 또는 전환 세부 정보를 확인합니다.
* **현재** 선택된 활동을 삭제하려면 Delete 키를 누릅니다.
* **Ctrl + C** 를 눌러 선택한 활동을 복사하고 **Ctrl + V** 를 눌러 작업 영역에 붙여넣습니다.

![](assets/workflow_workspace.png)

## Action bar {#action-bar}

작업 영역에서 선택한 요소 또는 작업 과정의 실행 상태에 따라 작업 표시줄에서 사용할 수 있는 단추가 달라질 수 있습니다.

<img height="21px" src="assets/edit_darkgrey-24px.png" /> **[!UICONTROL Open activity]**<br/>워크플로우 속성을 편집할 수 있습니다.

<img height="21px" src="assets/play_darkgrey-24px_table.png" /> **[!UICONTROL Start]**<br/>워크플로우를 시작합니다.

<img height="21px" src="assets/pause_darkgrey-24px_table.png" /> **[!UICONTROL Pause]**<br/>워크플로우를 일시 중지합니다.

<img height="21px" src="assets/stop_darkgrey-24px_table.png" /> **[!UICONTROL Stop]**<br/>워크플로우 실행을 방해합니다. 중단된 위치에서 다시 시작할 수 없습니다.

<img height="21px" src="assets/pauseplay_darkgrey-24px_table.png" /> **[!UICONTROL Restart]**<br/>워크플로우를 다시 시작합니다.

<img height="21px" src="assets/printpreview_darkgrey-24px_table.png" /> **[!UICONTROL Log and tasks]**<br/>워크플로우의 실행 로그를 엽니다.

<img height="21px" src="assets/checkcircle_darkgrey-24px_table.png" /> **[!UICONTROL Enable multi-selection]**<br/>다중 선택 모드를 활성화합니다. 워크플로우는 두 개 이상의 활동으로 구성되어야 합니다.

<img height="21px" src="assets/closecircle_darkgrey-24px_table.png" /> **[!UICONTROL Disable multi-selection]**<br/>다중 선택 모드를 비활성화합니다.<br />

<img height="21px" src="assets/targeted.png" /> **[!UICONTROL Open transition]**<br/>선택한 전환을 엽니다.<br />

<img height="21px" src="assets/check_darkgrey-24px_table.png" />  **[!UICONTROL Normal execution]**<br/>이전에 비활성화되었거나 일시 중지된 것으로 표시된 경우 선택을 다시 활성화합니다.<br />

<img height="21px" src="assets/check_pause_darkgrey-24px_table.png" /> **[!UICONTROL Execution suspended]**<br/>선택한 활동에서 워크플로우를 일시 중지합니다.<br />

<img height="21px" src="assets/checkdisable.png" /> **[!UICONTROL No execution]**<br/>활동을 비활성화합니다.<br />

<img height="21px" src="assets/delete_darkgrey-24px_table.png" /> **[!UICONTROL Delete selection]**<br/>선택한 활동을 삭제합니다.<br />

<img height="21px" src="assets/copy_24px.png" /> **[!UICONTROL Copy selection]**<br/>선택한 활동을 복사합니다.

<img height="21px" src="assets/paste_24px.png" /> **[!UICONTROL Paste]**<br/>복사한 활동을 붙여넣습니다.

## Quick actions {#quick-actions}

활동을 선택하면 활동에 빠른 작업 단추가 나타나 상호 작용할 수 있습니다.

<img height="21px" src="assets/edit_darkgrey-24px.png" /> **[!UICONTROL Open activity]**<br/>선택한 활동을 엽니다.

<img height="21px" src="assets/copy_24px.png" /> **[!UICONTROL Copy selection]**<br/>선택한 활동을 복사합니다.

<img height="21px" src="assets/wkf_dlv_act_params_icon.png" /> **[!UICONTROL Open the activity's advanced options]**<br/>선택한 이메일 또는 SMS 배달 활동의 고급 옵션을 엽니다.

<img height="21px" src="assets/check_darkgrey-24px_table.png" /> **[!UICONTROL Normal execution]**<br/>이전에 비활성화되었거나 일시 중지된 것으로 표시된 경우 선택을 다시 활성화합니다.

<img height="21px" src="assets/check_pause_darkgrey-24px_table.png" /> **[!UICONTROL Execution suspended]**<br/>선택한 활동에서 워크플로우를 일시 중지합니다.

<img height="21px" src="assets/checkdisable.png" /> **[!UICONTROL No execution]**<br/>활동을 비활성화합니다.

<img height="21px" src="assets/pending_darkgrey-24px_table.png" /> **[!UICONTROL Immediate execution]**<br/>선택 사항을 즉시 처리합니다. This button is only available for the <span class="uicontrol">Scheduler</span> and <span class="uicontrol">Wait</span> activities.

<img height="21px" src="assets/delete_darkgrey-24px_table.png" /> **[!UICONTROL Delete selection]**<br/>선택한 활동을 삭제합니다.

## Duplicating workflow activities {#duplicating-workflow-activities}

작업 공간에서는 워크플로우 활동을 동일한 워크플로우로 복사하여 복사하거나 동일한 캠페인 인스턴스의 다른 워크플로우로 복사하여 복제할 수 있습니다.

활동이 복제되면 전체 구성이 유지됩니다. 배달 활동 (이메일, SMS, 푸시 알림...) 의 경우 활동에 첨부된 게재 개체가 복제됩니다.

>[!NOTE]
>
>워크플로우 활동은 인스턴스에서 다른 인스턴스로 복제할 수 없습니다. 기술 워크플로우의 활동은 중복될 수 없습니다.

활동을 복제하려면 아래 단계를 따르십시오.

1. Select the activity, then click the **[!UICONTROL Copy selection]** button from the quick actions.

   **Ctrl + C** 키보드 단축키를 사용할 수도 있습니다.

   ![](assets/wkf_copypaste1.png)

1. Right-click in the target workflow workspace, then click the **[!UICONTROL Paste]** button.

   **CTRL + V** 키보드 단축키를 사용할 수도 있습니다.

   ![](assets/wkf_copypaste2.png)

1. 활동이 복제되고, 초기에 구성된 모든 설정이 복제됩니다.

또한 여러 개의 활성화를 복사하여 전체 흐름을 복제할 수 있습니다.

이렇게 하려면 해당 영역 주위에 영역을 그려 활동을 선택합니다. then click the **[!UICONTROL Copy selection]** button from the action bar (or press **Ctrl + C**). 그런 다음 원하는 위치에 붙여넣을 수 있습니다.

![](assets/wkf_copypaste3.png)

