---
title: 실행 옵션 관리
description: 워크플로우 실행 옵션을 관리하는 방법을 알아봅니다.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
context-tags: workflow,overview;workflow,main
feature: Workflows
role: Data Architect
level: Beginner
exl-id: b0cc38fe-cf71-4350-8b4e-7daf0bf94066
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 8%

---

# 실행 옵션 관리 {#managing-execution-options}

워크플로우의 실행 옵션을 수정하려면 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 워크플로우 속성에 액세스하고 **[!UICONTROL Execution]** 섹션을 선택합니다.

![](assets/wkf_execution_6.png)

가능한 옵션은 다음과 같습니다.

* **[!UICONTROL Default affinity]**: 이 필드를 사용하면 워크플로 또는 워크플로 활동을 특정 컴퓨터에서 강제로 실행할 수 있습니다.

* **[!UICONTROL History in days]**: 기록을 제거해야 하는 일 수를 지정합니다. 기록에는 **[!UICONTROL Transfer file]** 활동에서 다운로드한 파일뿐만 아니라 워크플로와 관련된 로그, 작업, 이벤트(워크플로 작업에 연결된 기술 개체)와 같은 요소가 포함되어 있습니다. 기본 워크플로 템플릿의 경우 기본값은 30일입니다.

  기록 제거는 기본적으로 매일 실행되는 데이터베이스 정리 기술 워크플로우에서 수행됩니다([기술 워크플로우 목록](../../administration/using/technical-workflows.md) 참조).

  >[!IMPORTANT]
  >
  >**[!UICONTROL History in days]** 필드를 비워 두면 해당 값은 &quot;1&quot;로 간주됩니다. 즉, 기록이 1일 후에 삭제됩니다.

* **[!UICONTROL Save SQL queries in the log]**: 워크플로우의 SQL 쿼리를 로그에 저장할 수 있습니다.

* **[!UICONTROL Diagnostic mode (Log execution plan of long running queries and give recommendations)]**: 전체 실행 계획을 기록하려면 이 옵션을 선택하십시오. 기본적으로 비활성화되어 있습니다.

  이 옵션에 대한 자세한 내용은 이 [섹션](#diagnostic-mode)을 참조하세요.

* **[!UICONTROL Keep interim results]**: 전환의 세부 정보를 보려면 이 옵션을 선택하십시오.

  >[!CAUTION]
  >
  >이 옵션은 많은 디스크 공간을 소모하며 워크플로를 빌드하고 적절한 구성과 동작이 되도록 설계되었습니다. 프로덕션 인스턴스에서 선택하지 않은 상태로 둡니다.

* **[!UICONTROL Execute in the engine (do not use in production)]**: 개발 환경 테스트 목적으로 워크플로우를 로컬에서 실행할 수 있도록 허용합니다.

* **[!UICONTROL Severity]**: Adobe Campaign 인스턴스에서 워크플로우를 실행하기 위한 우선 순위 수준을 지정할 수 있습니다. 이 필드는 Adobe 팀에서 모니터링 용도로만 사용됩니다.

**[!UICONTROL Error management]** 섹션에서는 오류 발생 시 워크플로의 동작 방식을 관리할 수 있는 추가 옵션을 제공합니다. 이러한 옵션은 [오류 관리](../../automating/using/monitoring-workflow-execution.md#error-management) 섹션에 자세히 설명되어 있습니다.

## 진단 모드 {#diagnostic-mode}

>[!CAUTION]
>
>이 옵션은 워크플로우 성능에 큰 영향을 줄 수 있으므로 제한적으로 사용해야 합니다.

활성화되면 쿼리에 1분 이상 걸리는 경우 워크플로 속성의 **[!UICONTROL Execution]** 섹션에 있는 **[!UICONTROL Diagnostic mode (Log execution plan of long running queries and give recommendations)]** 옵션이 전체 실행 계획을 기록합니다.

![](assets/wkf_diagnostic.png)

이 옵션을 활성화하고 워크플로우를 시작한 후 쿼리가 1분 이상 걸리면 실행 계획이 기록됩니다. 그런 다음 EXPLAIN ANALYZE를 사용하여 실행 계획을 검색할 수 있습니다.

자세한 내용은 [PostgreSQL 설명서](https://www.postgresql.org/docs/9.4/using-explain.html)를 참조하세요.

이 쿼리에 시퀀스 검사가 있는 경우 **[!UICONTROL Diagnostic mode]**&#x200B;에서 필터 식을 사용하여 인덱스를 만드는 권장 사항도 제공합니다.

>[!NOTE]
>
> 이러한 권장 사항은 참조용으로만 제공되며 사용 사례에 따라 신중하게 사용해야 합니다.

![](assets/wkf_diagnostic_4.png)

권장 사항을 트리거하려면 워크플로우 실행 중에 다음 두 가지 조건을 충족해야 합니다.

* 시퀀스 스캔은 쿼리에서 40% 이상 걸립니다.

* 시퀀스 스캔 후의 결과 행은 테이블에 있는 총 행의 1% 미만입니다.

고급 메뉴에서 **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** > **[!UICONTROL Options]**&#x200B;을(를) 선택하여 옵션을 관리할 수 있습니다.

* **[!UICONTROL Time of query execution (in milliseconds)(DiagnosticModeQueryTime)]**: **[!UICONTROL Value]** 필드에서 쿼리 실행에 새 시간을 설정할 수 있습니다. 쿼리 실행이 이 값을 초과하면 실행 계획이 기록됩니다.

  ![](assets/wkf_diagnostic_2.png)

* **[!UICONTROL Percentage of seq scan time (DiagnosticModeSeqScanPercentage)]**: **[!UICONTROL Value]** 필드에서 추천 생성을 위해 시퀀스 검색에 소요되는 쿼리 시간의 백분율을 변경할 수 있습니다.

  ![](assets/wkf_diagnostic_3.png)
