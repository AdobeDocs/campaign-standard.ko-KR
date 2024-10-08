---
title: 워크플로 수명 주기
description: 워크플로우 라이프 사이클에 대해 자세히 알아보기
audience: automating
content-type: reference
topic-tags: workflow-general-operation
context-tags: workflow,overview;workflow,main
feature: Workflows
role: Data Architect
level: Beginner
exl-id: ba968add-25a3-4962-9e90-f0a06d9b74a8
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 3%

---

# 워크플로 수명 주기 {#life-cycle}

워크플로우의 라이프 사이클에는 세 가지 주요 단계가 포함되며 각 단계는 상태 및 색상에 연결됩니다.

* **편집**(회색)

  워크플로우의 초기 디자인 단계입니다([워크플로우 만들기](../../automating/using/building-a-workflow.md#creating-a-workflow) 참조). 워크플로우는 아직 서버에서 처리되지 않으며 위험 없이 수정할 수 있습니다.

* **진행 중**(파란색)

  초기 디자인 단계가 완료되면 워크플로우를 시작하고 서버에서 처리합니다.

* **완료됨**(녹색)

  더 이상 진행 중인 작업이 없거나 연산자가 인스턴스를 명시적으로 중지한 경우 워크플로우가 완료됩니다.

워크플로우가 시작되면 두 가지 다른 상태도 있을 수 있습니다.

* **경고**(노란색)

  워크플로우를 완료할 수 없거나 ![](assets/pause_darkgrey-24px.png) 또는 ![](assets/check_pause_darkgrey-24px.png) 단추를 사용하여 일시 중지했습니다.

* **오류**(빨간색)

  워크플로우를 실행하는 동안 오류가 발생했습니다. 워크플로우가 중지되었으므로 사용자가 작업을 수행해야 합니다. 이 오류에 대한 자세한 내용을 보려면 ![](assets/printpreview_darkgrey-24px.png) 단추를 사용하여 워크플로우 로그에 액세스하십시오([모니터링](../../automating/using/monitoring-workflow-execution.md) 참조).

마케팅 활동 목록을 사용하면 모든 워크플로우와 해당 상태를 표시할 수 있습니다. 자세한 내용은 [마케팅 활동 관리](../../start/using/marketing-activities.md#about-marketing-activities)를 참조하십시오.

![](assets/wkf_execution_3.png)
