---
title: 워크플로우 인터페이스
seo-title: 워크플로우 인터페이스
description: 워크플로우 인터페이스
seo-description: 워크플로우를 생성, 편집 및 실행하는 인터페이스와 옵션에 대해 알아봅니다.
page-status-flag: 활성화 안 함
uuid: aafe33ed-fa07-4dd9-825e-242099334f1a
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 자동화
content-type: reference
topic-tags: 정보 워크플로우 및 데이터 관리
discoiquuid: 147fbb0d-17d2-444b-a215-9ad14179c549
context-tags: 워크플로,기본;워크플로,개요
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 51d80fc9c683e39b9d08ba7d36b76b71a9dd1e8c

---


# 워크플로우 인터페이스{#workflow-interface}

캠페인 및 프로그램의 전체 프로세스를 관리하는 워크플로우를 만들 수 있습니다.

워크플로우 편집 화면은 다음 요소로 구성됩니다.

* 사용 가능한 [활동을](#palette)참조하는 팔레트입니다.
* 활동이 [구성되고](#workspace)구성되는 작업 공간입니다.
* 작업 [막대는](#action-bar)워크플로우 및/또는 해당 구성 요소와 상호 작용할 수 있는 단추로 구성되어 있습니다.
* 선택한 [활동 주위에 표시되는 빠른 작업을](#quick-actions)통해 상호 작용할 수 있습니다.

![](assets/wkf_overview.png)

## Palette {#palette}

팔레트는 화면의 왼쪽에 있습니다. 사용 가능한 모든 활동은 여러 카테고리로 정렬됩니다.

* [타깃팅](../../automating/using/about-targeting-activities.md):인구 데이터 타깃팅, 조작 및 활동 필터링과 관련된 활동
* [실행](../../automating/using/about-execution-activities.md):워크플로우 구성 및 실행과 관련된 활동
* [채널](../../automating/using/about-channel-activities.md):사용 가능한 여러 통신 채널을 나타내는 활동
* [데이터 관리(ETL)](../../automating/using/about-data-management-activities.md):데이터 조작과 관련된 활동

워크플로우의 팔레트에서 활동을 사용하려면 팔레트를 작업 영역으로 드래그하여 놓습니다.

워크플로우를 시작하기 전에 팔레트에서 추가된 각 활동을 구성해야 합니다.

![](assets/workflow_palette.png)

## 작업 영역 {#workspace}

작업 영역은 워크플로우 편집기에서 중앙 영역입니다. 이 영역에서는 활동을 삭제하고 전환을 사용하여 함께 연결하고 구성할 수 있습니다.

두 활동을 연결하려면 첫 번째 활동에서 다음 활동까지 화살표 끝을 이동합니다. 이전 활동에 연결하려면 뒤에 있는 화살표 지점으로 활동을 이동할 수도 있습니다. 활동을 이동하면 해당 활동이 계속 연결됩니다.

데이터를 처리하는 활동에 따른 전환에는 중간 모집단이 포함됩니다. 워크플로우 속성의 **[!UICONTROL Keep interim results]** **[!UICONTROL Execution]** 섹션에서 옵션을 선택하면 액세스할 수 있습니다.

활동이 선택되면 활동 주위에 빠른 작업이 표시되므로 활동이 가능합니다. 예를 들어 활동을 구성하려면 활동을 선택한 다음 빠른 작업의 ![](assets/edit_darkgrey-24px_table.png) 단추를 사용하여 엽니다.

특정 기능은 작업 영역에서만 활성화됩니다.

* 여러 활동 및 전환 효과를 선택할 수 있습니다.
* Ctrl **+** 왼쪽 버튼을 클릭하여 여러 활동 및/또는 전환을 선택합니다.
* 현재 **선택된** 활동 또는 전환의 세부 사항을 보려면 Enter 키를 누릅니다.
* 삭제를 **눌러** 현재 선택된 활동을 삭제합니다.
* 선택한 **활동을 복사하려면 Ctrl + C** 를 누르고 **Ctrl + V** 를 눌러 작업 영역에 붙여넣습니다.

![](assets/workflow_workspace.png)

## 작업 표시줄 {#action-bar}

작업 공간에서 선택한 요소나 워크플로우의 실행 상태에 따라 작업 표시줄에서 사용할 수 있는 단추가 달라질 수 있습니다.

<img height="21px" src="assets/edit_darkgrey-24px.png" /> **[!UICONTROL Open activity]**<br/>워크플로우의 속성을 편집할 수 있습니다.

<img height="21px" src="assets/play_darkgrey-24px_table.png" /> **[!UICONTROL Start]**<br/>워크플로우를 시작합니다.

<img height="21px" src="assets/pause_darkgrey-24px_table.png" /> **[!UICONTROL Pause]**<br/>워크플로우를 일시 중지합니다.

<img height="21px" src="assets/stop_darkgrey-24px_table.png" /> **[!UICONTROL Stop]**<br/>워크플로우 실행을 중단합니다. 중지한 위치에서 다시 시작할 수 없습니다.

<img height="21px" src="assets/pauseplay_darkgrey-24px_table.png" /> **[!UICONTROL Restart]**<br/>워크플로우를 다시 시작합니다.

<img height="21px" src="assets/printpreview_darkgrey-24px_table.png" /> **[!UICONTROL Log and tasks]**<br/>워크플로우의 실행 로그를 엽니다.

<img height="21px" src="assets/checkcircle_darkgrey-24px_table.png" /> **[!UICONTROL Enable multi-selection]**<br/>다중 선택 모드를 활성화합니다. 워크플로우는 두 개 이상의 활동으로 구성되어야 합니다.

<img height="21px" src="assets/closecircle_darkgrey-24px_table.png" /> **[!UICONTROL Disable multi-selection]**<br/>다중 선택 모드를 비활성화합니다.<br />

<img height="21px" src="assets/targeted.png" /> **[!UICONTROL Open transition]**<br/>선택한 전환을 엽니다.<br />

<img height="21px" src="assets/check_darkgrey-24px_table.png" />  **[!UICONTROL Normal execution]**<br/>이전에 비활성화되었거나 일시 중지됨으로 표시된 선택 항목을 다시 활성화합니다.<br />

<img height="21px" src="assets/check_pause_darkgrey-24px_table.png" /> **[!UICONTROL Execution suspended]**<br/>선택한 활동에서 워크플로우를 일시 중지합니다.<br />

<img height="21px" src="assets/checkdisable.png" /> **[!UICONTROL No execution]**<br/>활동을 비활성화합니다.<br />

<img height="21px" src="assets/delete_darkgrey-24px_table.png" /> **[!UICONTROL Delete selection]**<br/>선택한 활동을 삭제합니다.<br />

<img height="21px" src="assets/copy_24px.png" /> **[!UICONTROL Copy selection]**<br/>선택한 활동을 복사합니다.

<img height="21px" src="assets/paste_24px.png" /> **[!UICONTROL Paste]**<br/>복사한 활동을 붙여넣습니다.

## 빠른 작업 {#quick-actions}

활동을 선택하면 활동 주위에 빠른 작업 단추가 표시되므로 활동이 가능합니다.

<img height="21px" src="assets/edit_darkgrey-24px.png" /> **[!UICONTROL Open activity]**<br/>선택한 활동을 엽니다.

<img height="21px" src="assets/copy_24px.png" /> **[!UICONTROL Copy selection]**<br/>선택한 활동을 복사합니다.

<img height="21px" src="assets/wkf_dlv_act_params_icon.png" /> **[!UICONTROL Open the activity's advanced options]**<br/>선택한 이메일 또는 SMS 배달 활동의 고급 옵션을 엽니다.

<img height="21px" src="assets/check_darkgrey-24px_table.png" /> **[!UICONTROL Normal execution]**<br/>이전에 비활성화되었거나 일시 중지됨으로 표시된 선택 항목을 다시 활성화합니다.

<img height="21px" src="assets/check_pause_darkgrey-24px_table.png" /> **[!UICONTROL Execution suspended]**<br/>선택한 활동에서 워크플로우를 일시 중지합니다.

<img height="21px" src="assets/checkdisable.png" /> **[!UICONTROL No execution]**<br/>활동을 비활성화합니다.

<img height="21px" src="assets/pending_darkgrey-24px_table.png" /> **[!UICONTROL Immediate execution]**<br/>선택 항목을 즉시 처리하도록 합니다. 이 단추는 스케줄러 <span class="uicontrol">및</span> 대기 <span class="uicontrol">활동에만 사용할 수</span> 있습니다.

<img height="21px" src="assets/delete_darkgrey-24px_table.png" /> **[!UICONTROL Delete selection]**<br/>선택한 활동을 삭제합니다.

## 워크플로우 활동 복제 {#duplicating-workflow-activities}

작업 영역을 사용하면 동일한 워크플로에 복사하여 붙여넣거나 동일한 Campaign 인스턴스의 다른 워크플로에 붙여넣어 워크플로우 활동을 복제할 수 있습니다.

활동이 복제되면 전체 구성이 유지됩니다. 배달 활동(이메일, SMS, 푸시 알림...)의 경우 활동에 첨부된 배달 개체가 복제됩니다.

>[!NOTE]
>
>워크플로우 활동은 인스턴스에서 다른 인스턴스로 복제할 수 없습니다. 기술 워크플로우의 활동은 중복될 수 없습니다.

활동을 복제하려면 아래 단계를 따르십시오.

1. 활동을 선택한 다음 빠른 작업에서 **[!UICONTROL Copy selection]** 단추를 클릭합니다.

   Ctrl + C **키보드 단축키를 사용할 수도** 있습니다.

   ![](assets/wkf_copypaste1.png)

1. 대상 워크플로우 작업 영역에서 마우스 오른쪽 버튼을 클릭한 다음 **[!UICONTROL Paste]** 단추를 클릭합니다.

   Ctrl + V **키보드 단축키를 사용할 수도** 있습니다.

   ![](assets/wkf_copypaste2.png)

1. 활동이 복제되며 처음에 구성된 모든 설정이 중복됩니다.

여러 활동을 복사하여 붙여넣을 수 있으므로 전체 워크플로우를 복제할 수 있습니다.

이렇게 하려면 활동 주위에 영역을 그려 활동을 선택합니다. 그런 다음 작업 표시줄에서 **[!UICONTROL Copy selection]** 단추를 클릭합니다(또는 Ctrl + **C**). 그런 다음 원하는 위치에 붙여넣을 수 있습니다.

![](assets/wkf_copypaste3.png)

