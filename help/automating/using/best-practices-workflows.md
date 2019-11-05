---
title: 워크플로우 모범 사례
description: 워크플로우에 적용되는 모범 사례를 살펴볼 수 있습니다.
page-status-flag: 활성화 안 함
uuid: ff02b74e-53e8-49c6-bf8e-0c729eaa7d25
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 자동화
content-type: reference
topic-tags: workflow-general-operation
context-tags: 워크플로,개요;워크플로,기본
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 워크플로우 모범 사례{#workflow-best-practices}

Adobe Campaign을 사용하면 모든 유형의 워크플로우를 설정하여 다양한 작업을 수행할 수 있습니다. 그러나 워크플로우를 설계하고 실행할 때 잘못된 구현으로 인해 성능, 오류 및 플랫폼 문제가 발생할 수 있으므로 매우 신중해야 합니다. 다음은 우수 사례 및 문제 해결 팁의 목록을 참조하십시오.

>[!NOTE]
>
>워크플로우 디자인 및 실행은 Adobe Campaign 고급 사용자가 수행해야 합니다.

## 이름 지정{#naming}

워크플로우 문제 해결을 간소화하려면 워크플로우의 이름을 명시적으로 지정하고 레이블을 지정하는 것이 좋습니다. 워크플로우의 설명 필드를 채워 연산자가 쉽게 이해할 수 있도록 수행할 프로세스를 요약합니다.
워크플로우가 여러 워크플로우가 포함된 프로세스의 일부인 경우 레이블을 입력할 때 숫자를 사용하여 명확하게 순서를 지정할 수 있습니다.

예:

* 001 - 가져오기 - 수신자 가져오기
* 002 - 가져오기 - 판매 가져오기
* 003 - 가져오기 - 세일즈 세부 정보 가져오기
* 010 - 내보내기 - 배달 로그 내보내기
* 011 - 내보내기 - 추적 로그 내보내기

## 워크플로우 복제{#duplicating-workflows}

워크플로우를 복제할 수 있습니다. 워크플로우에서 **[!UICONTROL Marketing Activities]**&#x200B;마우스를 가져간 다음 을 클릭합니다 **[!UICONTROL Duplicate element]**. 워크플로우가 복제되면 워크플로우의 수정 사항이 워크플로우의 복사본으로 전달되지 않습니다. 워크플로우의 복사본을 편집할 수 있습니다.

![](assets/duplicating_workflow.png)

## 실행{#execution}

### 워크플로우 수

기본적으로 20개 이상의 활성 워크플로우 실행을 동시에 실행하지 않는 것이 좋습니다. 이 제한을 초과하면 워크플로우는 성능에 영향을 주지 않도록 큐에 오르게 됩니다. 마찬가지로, Adobe는 시간에 따라 워크플로우 탐색을 확산시킬 것을 권장합니다.
특정 컨텍스트에서는 20개 이상의 워크플로우를 실행해야 할 수 있습니다. 예약된 실행을 기다리는 워크플로우에는 적용되지 않습니다.  그런 경우 캠페인 전문가에게 활용 사례를 확인하고 Adobe 고객 지원 센터에 문의하여 한도를 늘려야 합니다.

### 빈도

워크플로우는 10분마다 두 번 이상 자동으로 실행할 수 없습니다.
활동의 반복 빈도는 10분 미만이어야 합니다. 반복 빈도가 0(기본값)으로 설정된 경우 이 옵션을 고려하지 않으며 워크플로우는 실행 빈도에 따라 실행됩니다.

### 일시 중지된 워크플로우

7일 이상 일시 중지 또는 실패 상태인 워크플로우는 디스크 공간을 적게 사용하기 위해 중지됩니다. 청소 작업이 워크플로 로그에 표시됩니다.

### 전환

종료되지 않은 전환이 포함된 워크플로우는 여전히 실행할 수 있습니다.경고 메시지가 생성되며 워크플로우가 전환에 도달하면 일시 중지되지만 오류가 생성되지 않습니다. 또한 완성된 디자인 없이 워크플로우를 시작하여 작업을 완료할 수 있습니다.

자세한 내용은 워크플로우 [실행을 참조하십시오](../../automating/using//executing-a-workflow.md).

## 활동{#activity}

### 워크플로우 디자인

워크플로우가 제대로 종료되도록 하려면 **[!UICONTROL End activity]** 워크플로우의 마지막 전환을 그대로 두지 마십시오.

전환의 세부 사항 보기에 액세스하려면 워크플로우 속성의 실행 섹션에서 **[!UICONTROL Keep interim results]** 옵션을 선택합니다.

>[!CAUTION]
>
>이 옵션은 많은 디스크 공간을 사용하며, 작업 흐름을 구축하고 적절한 구성 및 동작을 유지하도록 설계되었습니다. 프로덕션 인스턴스에서 선택 취소하지 않습니다.

![](assets/keep_interim_best_practices.png)


### 레이블 지정 활동{#activity-labeling}

워크플로우를 개발하는 동안 모든 Adobe Campaign 개체에 대해 이름이 생성됩니다. 도구에 의해 활동 이름이 생성되어 편집할 수 없지만 구성할 때 명시적인 이름으로 레이블을 지정하는 것이 좋습니다.

### 활동 복제{#activity-duplicating}

기존 활동을 복제하려면 복사-붙여넣기를 사용할 수 있습니다. 이렇게 하면 원래 정의된 설정을 유지합니다. 자세한 내용은 워크플로우 활동 [복제를 참조하십시오](../../automating/using/workflow-interface.md).

### 스케줄러 활동{#acheduler-activity}

워크플로우를 구축할 때는 분기당 하나만 **[!UICONTROL Scheduler activity]** 사용합니다. 워크플로우의 동일한 분기에 여러 개의 스케줄러(서로 연결)가 있는 경우 실행될 작업 수를 기하급수적으로 곱하므로 데이터베이스가 상당히 오버로드됩니다.

을 클릭하여 워크플로우의 다음 10개 실행을 미리 볼 수 **[!UICONTROL Preview next executions]**&#x200B;있습니다.

![](assets/preview_scheduler.png)

자세한 내용은 스케줄러 [활동을](../../automating/using/scheduler.md)참조하십시오.

## 매개 변수를 사용하여 워크플로 호출{#workflow-with-parameters}

워크플로우 호출 시 정의된 매개 변수의 이름 및 수와 동일한지 확인합니다(워크플로우 [호출 시 매개 변수 정의 참조](../../automating/using/calling-a-workflow-with-external-parameters.md#defining-the-parameters-when-calling-the-workflow)). 매개 변수의 유형은 예상 값과 일치해야 합니다.

모든 매개 변수가 에서 선언되었는지 확인합니다 **[!UICONTROL External signal activity]**. 그렇지 않으면 활동을 실행할 때 오류가 발생합니다.

자세한 내용은 외부 매개 변수를 [사용하여 워크플로우](../../automating/using/calling-a-workflow-with-external-parameters.md)호출을 참조하십시오.

## 패키지 내보내기{#exporting-packages}

패키지를 내보내려면 내보낸 리소스에 기본 ID가 없어야 합니다. 따라서 Adobe Campaign Standard에서 표준으로 제공된 템플릿과는 다른 이름을 사용하여 내보내기 가능한 리소스의 ID를 변경해야 합니다.
자세한 내용은 패키지 [관리를](../../automating/using/managing-packages.md)참조하십시오.

## 목록 내보내기{#exporting-lists}

내보내기 목록 옵션을 사용하면 기본적으로 최대 100,000개의 줄을 내보내고 Nms_ExportListLimit **옵션으로**&#x200B;정의할 수 있습니다. 이 옵션은 기능 관리자가 &gt; **[!UICONTROL Administration]** &gt; **[!UICONTROL Application settings]** &gt; **[!UICONTROL Options]**에서 관리할 수 있습니다.
자세한 내용은 목록 [내보내기를](../../automating/using/exporting-lists.md)참조하십시오.

## 문제 해결{#workflow-troubleshooting}

Adobe Campaign은 워크플로우 문제를 더 잘 이해할 수 있도록 다양한 로그를 제공합니다.

### 워크플로우 로그 사용{#using-workflow-logs}

워크플로우 로그에 액세스하여 활동 실행을 모니터링할 수 있습니다. 시간 순서대로 수행 및 실행 오류를 인덱싱합니다. 로그 탭은 선택한 모든 활동 또는 일부 활동의 실행 내역에 있습니다.
작업 탭은 활동의 실행 순서에 대해 자세히 설명합니다. 활동에 대한 자세한 내용을 보려면 작업을 클릭합니다.
자세한 내용은 워크플로우 [실행](../../automating/using/executing-a-workflow.md#monitoring)모니터링을 참조하십시오.

#### Troubleshooting data management activities{#troubleshooting-data-management-activities}

[로그] 탭에서 SQL 쿼리를 분석할 수 있습니다.

1. 워크플로우 작업 영역에서 을 클릭합니다 **[!UICONTROL Edit properties]**.
1. &gt; **[!UICONTROL General]** 에서 **[!UICONTROL Execution]**&#x200B;및 **[!UICONTROL Save SQL queries in the log]** 옵션을 선택하고 **[!UICONTROL Execute in the engine]** **[!UICONTROL Confirm]**&#x200B;을 클릭합니다.

**로그에서 SQL 쿼리를 보려면:**
1. Click **[!UICONTROL Log and Tasks]**.
1. 탭에서 **[!UICONTROL Logs]** **[!UICONTROL Search]** 패널을 엽니다.
1. 확인해 **[!UICONTROL Display SQL logs only]**&#x200B;보십시오.

쿼리가 로그의 **[!UICONTROL Message]** 열에 표시됩니다.

### 배달 로그 사용{#using-delivery-logs}

배달 로그를 사용하면 배달 성공을 모니터링할 수 있습니다. 제외 로그는 전송을 준비하는 동안 제외된 메시지를 반환합니다. 전송 로그는 각 프로필에 대한 배달 상태를 제공합니다.
자세한 내용은 배달 실패 [이해를 참조하십시오](../../sending/using/understanding-delivery-failures.md).

### 전달 경고 사용{#delivery-alerting}

전달 경고 기능은 사용자 그룹이 배달 실행에 대한 정보가 포함된 알림을 자동으로 수신할 수 있는 경고 관리 시스템입니다.
자세한 내용은 전달 경고를 [참조하십시오](../../sending/using/receiving-alerts-when-failures-happen.md).

**관련 항목:**

* [오류 관리](../../automating/using/executing-a-workflow.md#error-management)
