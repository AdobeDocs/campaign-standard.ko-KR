---
solution: Campaign Standard
product: campaign
title: 실행 옵션 관리
description: 워크플로우 실행 옵션을 관리하는 방법을 알아봅니다.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
context-tags: workflow,overview;workflow,main
feature: 워크플로우
role: 데이터 아키텍트
level: 초급
translation-type: tm+mt
source-git-commit: 088b49931ee5047fa6b949813ba17654b1e10d60
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 13%

---


# 실행 옵션 관리 {#managing-execution-options}

워크플로우의 실행 옵션을 수정하려면 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 워크플로우 속성에 액세스하고 **[!UICONTROL Execution]** 섹션을 선택합니다.

![](assets/wkf_execution_6.png)

가능한 옵션은 다음과 같습니다.

* **[!UICONTROL Default affinity]**:이 필드를 사용하면 특정 컴퓨터에서 워크플로우 또는 워크플로우 활동을 강제로 실행할 수 있습니다.

* **[!UICONTROL History in days]**:내역을 삭제할 일 수를 지정합니다. 작업 내역에는 작업 과정과 관련된 요소가 포함되어 있습니다.로그, 작업, 이벤트(워크플로우 작업에 연결된 기술 개체) 및 **[!UICONTROL Transfer file]** 활동에 의해 다운로드한 파일 기본 워크플로 템플릿의 기본값은 30일입니다.

   작업 내역 제거는 데이터베이스 정리 기술 워크플로우에 의해 수행되며 기본적으로 매일 실행됩니다([기술 작업 과정 목록](../../administration/using/technical-workflows.md) 참조).

   >[!IMPORTANT]
   >
   >**[!UICONTROL History in days]** 필드를 비워 두면 해당 값이 &quot;1&quot;로 간주됩니다. 즉, 내역은 1일 후에 삭제됩니다.

* **[!UICONTROL Save SQL queries in the log]**:워크플로우의 SQL 쿼리를 로그에 저장할 수 있습니다.

* **[!UICONTROL Keep interim results]**:전환 세부 사항을 보려면 이 옵션을 선택합니다.

   >[!CAUTION]
   >
   >이 옵션은 많은 디스크 공간을 소모하며 워크플로우를 빌드하고 적절한 구성과 동작이 되도록 설계되었습니다. 프로덕션 인스턴스에서 선택하지 않은 상태로 둡니다.

* **[!UICONTROL Execute in the engine (do not use in production)]**:개발 환경 테스트 목적으로 로컬에서 워크플로우를 실행할 수 있도록 해줍니다.

* **[!UICONTROL Severity]**:Adobe Campaign 인스턴스에서 워크플로우를 실행하기 위한 우선 순위 수준을 지정할 수 있습니다. 이 필드는 Adobe 팀이 모니터링 목적으로만 사용합니다.

**[!UICONTROL Error management]** 섹션에서는 오류가 발생하는 경우 워크플로우의 작동 방식을 관리할 수 있는 추가 옵션을 제공합니다. 이러한 옵션은 [오류 관리](../../automating/using/monitoring-workflow-execution.md#error-management) 섹션에 자세히 설명되어 있습니다.
