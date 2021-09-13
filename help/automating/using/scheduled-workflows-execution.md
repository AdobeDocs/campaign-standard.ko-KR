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

Campaign Standard에서 워크플로우 엔진은 워크플로우 인스턴스가 하나의 프로세스로만 실행되도록 보장합니다. 가져오기, 장기 실행 쿼리 또는 데이터베이스에 쓰기 등의 활동을 차단하면 실행 시 다른 작업이 실행되지 않습니다.

반면 비차단 활동은 다른 작업(일반적으로 **[!UICONTROL Scheduler]** 활동과 같은 이벤트를 기다리는 활동)의 실행을 차단하지 않습니다.

이렇게 하면 동일한 워크플로우의 이전 실행이 아직 완료되지 않은 경우에도 일정 기반 워크플로우가 실행을 시작할 수 있는 시나리오가 나타날 수 있으며, 이로 인해 예기치 않은 데이터 문제가 발생할 수 있습니다.

따라서 여러 활동이 포함된 예약된 워크플로우를 디자인할 때는 워크플로우가 완료될 때까지 워크플로우의 일정이 조정되지 않도록 해야 합니다. 이렇게 하려면 이전에 실행한 하나 이상의 작업이 아직 보류 중인 경우 실행을 방지하기 위해 워크플로우를 구성해야 합니다.

## 워크플로우 구성

이전 워크플로우 실행에서 하나 이상의 작업이 아직 보류 중인지 확인하려면 **[!UICONTROL Query]** 및 **[!UICONTROL Test]** 활동을 사용해야 합니다.

1. **[!UICONTROL Scheduler]** 활동 뒤에 **[!UICONTROL Query]** 활동을 추가한 다음 다음과 같이 구성합니다.

1. 활동의 리소스를 **[!UICONTROL WorkflowTaskDetail]**(으)로 변경합니다. 이것은 워크플로우의 현재 작업을 타겟팅함을 의미합니다.

   ![](assets/scheduled-wkf-resource.png)

1. 아래 규칙으로 쿼리를 구성합니다.

   ![](assets/scheduled-wkf-query.png)

   * 첫 번째 규칙은 현재 작업(query2)과 현재 워크플로우에 속하는 다음 예약 작업(schedule2)을 필터링합니다.

      >[!NOTE]
      >
      >**[!UICONTROL Scheduler]** 활동이 시작되면 즉시 다른 예약 작업이 추가되어 다음에 예약된 시간에 실행되고 워크플로우가 시작됩니다. 따라서 이전 실행에서 보류 중인 작업을 찾을 때 쿼리 및 예약 작업을 모두 필터링하는 것이 중요합니다.

   * 두 번째 규칙은 워크플로우의 이전 실행에서 0개의 실행 상태에 해당하는 작업이 여전히 활성(보류 중)인지 여부를 결정합니다.

1. **[!UICONTROL Query]** 활동에서 반환한 보류 중인 작업 수를 확인하려면 **[!UICONTROL Test]** 활동을 추가합니다. 이렇게 하려면 두 개의 아웃바운드 전환을 구성합니다.

   ![](assets/scheduled-wkf-test.png)

   * 보류 중인 작업이 없는 경우 첫 번째 전환은 워크플로우 실행을 계속합니다.
   * 두 번째 전환은 보류 중인 작업이 있으면 워크플로우 실행을 취소합니다.

   ![](assets/scheduled-wkf-workflow.png)

이제 필요에 따라 나머지 워크플로우를 구성할 수 있습니다. 보류 중인 작업으로 인해 워크플로우 실행이 취소되는 경우 워크플로우가 예약에 따라 다시 실행될 때 다음 단계를 진행할 수 있습니다. 이렇게 하면 이전 실행에서 활성(보류 중) 작업이 없는 경우에만 워크플로우 실행이 진행될 수 있습니다.
