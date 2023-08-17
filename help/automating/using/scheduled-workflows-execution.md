---
title: 예약된 워크플로우의 중복 실행
description: 예약된 워크플로우의 중복 실행을 방지하는 방법을 알아봅니다.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
context-tags: workflow,overview;workflow,main
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: 8d9820a4-3c44-45f5-815e-4ed48a96276d
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 1%

---

# 예약된 워크플로우의 중복 실행{#preventing-overlapping-execution-of-scheduled-workflows}

## 예약된 워크플로우 실행 기본 정보

Campaign Standard에서 워크플로 엔진은 워크플로 인스턴스가 한 개의 프로세스에서만 실행되도록 합니다. 가져오기, 장기 실행 쿼리 또는 데이터베이스에 쓰기 등의 활동을 차단하면 실행 시 다른 작업이 실행되지 않습니다.

반면에 비차단 활동은 다른 작업(일반적으로 다음과 같은 이벤트를 기다리는 활동)의 실행을 차단하지 않습니다. **[!UICONTROL Scheduler]** 활동)을 참조하십시오.

이렇게 하면 동일한 워크플로우의 이전 실행이 아직 완료되지 않았더라도 일정 기반 워크플로우가 실행을 시작할 수 있어 예기치 않은 데이터 문제가 발생할 수 있습니다.

따라서 여러 활동이 포함된 예약된 워크플로우를 디자인할 때 완료될 때까지 워크플로우의 일정이 조정되지 않도록 해야 합니다. 이렇게 하려면 이전에 수행한 하나 이상의 작업이 아직 보류 중인 경우 실행을 방지하기 위해 워크플로우를 구성해야 합니다.

## 워크플로우 구성

이전 워크플로우 실행에서 하나 이상의 작업이 아직 보류 중인지 확인하려면 **[!UICONTROL Query]** 및 a **[!UICONTROL Test]** 활동.

1. 추가 **[!UICONTROL Query]** 다음 이후 활동 **[!UICONTROL Scheduler]** 활동을 구성한 다음 다음과 같이 구성합니다.

1. 활동의 리소스를 다음으로 변경 **[!UICONTROL WorkflowTaskDetail]**: 워크플로우의 현재 작업을 타겟팅한다는 의미입니다.

   ![](assets/scheduled-wkf-resource.png)

1. 아래 규칙으로 쿼리를 구성합니다.

   ![](assets/scheduled-wkf-query.png)

   * 첫 번째 규칙은 현재 작업(query2)과 현재 워크플로우에 속하는 다음 일정 작업(schedule2)을 필터링합니다.

     >[!NOTE]
     >
     >다음과 같은 경우 **[!UICONTROL Scheduler]** 활동이 시작되면 예약된 다음 시간에 실행할 다른 예약 작업이 즉시 추가되고 워크플로우가 시작됩니다. 따라서 이전 실행에서 보류 중인 작업을 찾을 때 쿼리뿐만 아니라 일정 작업을 모두 필터링하는 것이 중요합니다.

   * 두 번째 규칙은 워크플로우의 이전 실행에서 생성된 작업이 여전히 활성(보류 중)인지 여부를 결정하며, 이는 실행 상태가 0인 경우에 해당합니다.

1. 추가 **[!UICONTROL Test]** 활동으로 반환되는 보류 중인 작업의 수를 확인합니다. **[!UICONTROL Query]** 활동. 이렇게 하려면 두 개의 아웃바운드 전환을 구성합니다.

   ![](assets/scheduled-wkf-test.png)

   * 첫 번째 전환은 보류 중인 작업이 없는 경우 워크플로우 실행을 계속합니다.
   * 두 번째 전환은 보류 중인 작업이 있는 경우 워크플로우 실행을 취소합니다.

   ![](assets/scheduled-wkf-workflow.png)

이제 필요에 따라 나머지 워크플로우를 구성할 수 있습니다. 보류 중인 작업으로 인해 워크플로우 실행이 취소된 경우 일정에 따라 워크플로우가 다시 실행될 때 다음 단계를 진행할 수 있습니다. 이렇게 하면 이전 실행에서 활성(보류 중인) 작업이 없는 경우에만 워크플로우 실행이 진행될 수 있습니다.
