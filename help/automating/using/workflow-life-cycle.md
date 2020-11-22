---
solution: Campaign Standard
product: campaign
title: 워크플로우 수명 주기
description: 워크플로우 라이프사이클에 대한 자세한 내용
audience: automating
content-type: reference
topic-tags: workflow-general-operation
context-tags: workflow,overview;workflow,main
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 3%

---


# 워크플로우 수명 주기 {#life-cycle}

워크플로우의 라이프 사이클에는 3개의 기본 단계가 포함되며 각 단계는 상태 및 색상으로 연결됩니다.

* **편집** (회색)

   워크플로우의 초기 디자인 단계입니다(워크플로우 [만들기 참조](../../automating/using/building-a-workflow.md#creating-a-workflow)). 워크플로우는 서버에서 아직 처리되지 않으며, 아무런 위험 없이 수정할 수 있습니다.

* **진행** 중(파란색)

   초기 디자인 단계가 완료되면 워크플로우를 시작할 수 있으며 서버에서 처리합니다.

* **완료됨** (녹색)

   진행 중인 작업이 없거나 연산자가 명시적으로 인스턴스를 중지한 경우 워크플로우가 완료됩니다.

워크플로우가 시작되면 워크플로우의 상태가 다음과 같이 두 가지일 수도 있습니다.

* **경고** (노란색)

   워크플로를 완료할 수 없거나 ![](assets/pause_darkgrey-24px.png) 또는 ![](assets/check_pause_darkgrey-24px.png) 단추를 사용하여 일시 중지되었습니다.

* **오류** (빨간색)

   워크플로우를 실행할 때 오류가 발생했습니다. 워크플로가 중지되었으며 사용자가 작업을 수행해야 합니다. 이 오류에 대한 자세한 내용을 보려면 ![](assets/printpreview_darkgrey-24px.png) 단추를 사용하여 워크플로우 로그에 [액세스하십시오(모니터링](../../automating/using/monitoring-workflow-execution.md)참조).

마케팅 활동 목록을 사용하면 모든 워크플로우와 그 상태를 표시할 수 있습니다. For more on this, see [Managing marketing activities](../../start/using/marketing-activities.md#about-marketing-activities).

![](assets/wkf_execution_3.png)
