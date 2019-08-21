---
title: 워크플로우 우수 사례
seo-title: 워크플로우 우수 사례
description: 워크플로우 우수 사례
seo-description: 워크플로우에 적용되는 모범 사례를 살펴보십시오.
page-status-flag: 정품 인증 안 함
uuid: ff 02 b 74 e -53 e 8-49 c 6-bf 8 e -0 c 729 eaa 7 d 25
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: workflow-general-operation
context-tags: workflow, overview; 워크플로우, 기본
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: fd44c6e6d0f6a4ca75b01c99fbae6d9072dd7736

---


# 워크플로우 우수 사례{#workflow-best-practices}

Adobe Campaign를 사용하면 대규모 작업 범위를 수행하도록 모든 유형의 워크플로우를 설정할 수 있습니다. 그러나 워크플로우를 디자인 및 실행할 때는 잘못된 구현으로 인해 잘못된 성능, 오류 및 플랫폼 문제가 발생할 수 있으므로 매우 신중해야 합니다. 아래에서 우수 사례 및 문제 해결 팁 목록을 찾을 수 있습니다.

>[!NOTE]
>
>워크플로우 디자인 및 실행을 Adobe Campaign 고급 사용자가 수행해야 합니다.

## 이름 지정{#naming}

워크플로우 문제 해결을 용이하게 하려면 워크플로우의 이름을 지정하고 레이블을 명시적으로 지정하는 것이 좋습니다. 워크플로우의 설명 필드를 채워 연산자가 작업을 쉽게 이해할 수 있도록 프로세스를 요약합니다.
워크플로우가 여러 워크플로우와 관련된 프로세스의 일부인 경우 레이블을 입력할 때 숫자를 사용하여 명확히 주문할 수 있습니다.

예를 들면 다음과 같습니다.

* 001 - 가져오기 - 수신자 가져오기
* 002 - 가져오기 - 영업 가져오기
* 003 - 가져오기 - 영업 세부 정보 가져오기
* 010 - 내보내기 - 배달 로그 내보내기
* 011 - 내보내기 - 추적 로그 내보내기

## 워크플로우 복제{#duplicating-workflows}

워크플로우를 복제할 수 있습니다. 에서 **[!UICONTROL Marketing Activities]**&#x200B;워크플로우 위로 마우스를 **[!UICONTROL Duplicate element]**&#x200B;가져간 다음을 클릭합니다. 복제한 후에는 워크플로우가 워크플로우로 복사되지 않습니다. 워크플로우의 사본을 편집할 수 있습니다.

![](assets/duplicating_workflow.png)

## 실행{#execution}

### 워크플로우 수

기본적으로 활성 워크플로우 실행을 동시에 20 개 이상 실행하지 않는 것이 좋습니다. 이 제한에 도달하면 워크플로우는 성능에 영향을 주지 않도록 큐에 표시됩니다. 마찬가지로 시간이 지남에 따라 워크플로우 활동을 펼치도록 권장합니다.
특정 컨텍스트에서는 20 개 이상의 워크플로우를 실행해야 할 수 있습니다. 예약된 실행을 기다리는 워크플로우에는 적용되지 않습니다. 이러한 경우 캠페인 전문가와 함께 사용 사례를 확인하고 Adobe 고객 지원 팀에 문의하여 한도를 늘리십시오.

### 빈도

워크플로우를 10 분마다 한 번 더 자동으로 실행할 수 없습니다.
활동의 반복 빈도는 10 분 이내여야 합니다. 반복 빈도를 0 (기본값) 로 설정하면 이 옵션이 고려되지 않고 워크플로우는 실행 빈도에 따라 실행됩니다.

### 일시 중지된 워크플로우

7 일 이상 일시 중지 또는 실패 상태인 워크플로우는 디스크 공간을 적게 차지하기 위해 중지됩니다. 작업 흐름 로그에 정리 작업이 표시됩니다.

### 전환 효과

종결되지 않은 전환을 포함하는 워크플로우를 계속 실행할 수 있습니다. 경고 메시지가 생성되고 워크플로우가 전환에 도달하면 일시 중지됩니다. 하지만 오류가 발생하지 않습니다. 또한 완성된 디자인 없이도 워크플로우를 시작하고 작업을 진행할 수 있습니다.

자세한 내용은 워크플로우 [실행을](../../automating/using//executing-a-workflow.md)참조하십시오.

## 활동{#activity}

### 워크플로우 디자인

워크플로우가 제대로 종료되도록 하려면을 **[!UICONTROL End activity]**&#x200B;사용합니다. 워크플로우의 마지막 전환을 직접 종료하지 마십시오.

전환 세부 사항 보기에 액세스하려면 워크플로우 속성의 실행 섹션에서 **[!UICONTROL Keep interim results]** 옵션을 선택합니다.

>[!CAUTION]
>
>이 옵션은 많은 디스크 공간을 사용하며, 워크플로우를 구축하고 적절한 구성 및 비헤이비어를 유지하도록 설계되었습니다. 프로덕션 인스턴스는 선택하지 않은 상태로 두십시오.

![](assets/keep_interim_best_practices.png)


### 레이블 지정 활동{#activity-labeling}

워크플로우를 개발하는 동안 모든 Adobe Campaign 개체에 대해 모든 활동에 대해 이름이 생성됩니다. 활동 이름이 도구에 의해 생성되므로 편집할 수 없는 경우 구성 시 명시적인 이름으로 레이블을 지정하는 것이 좋습니다.

### 활동 복제{#activity-duplicating}

기존 활동을 복제하려면 복사 붙여넣기를 사용할 수 있습니다. 이렇게 하면 원래 정의된 설정을 유지합니다. 자세한 내용은 워크플로우 활동 [복제를](../../automating/using/workflow-interface.md)참조하십시오.

### 스케줄러 활동{#acheduler-activity}

워크플로우를 빌드할 때는 분기당 하나만 **[!UICONTROL Scheduler activity]** 사용합니다. 워크플로우의 동일한 분기에 여러 예약 (서로 연결) 이 있는 경우 실행할 작업 수가 기하급수적으로 곱해져 데이터베이스를 과도하게 오버로드합니다.

을 클릭하여 워크플로우의 다음 10 개 실행을 미리 볼 **[!UICONTROL Preview next executions]**&#x200B;수 있습니다.

![](assets/preview_scheduler.png)

자세한 내용은 [스케줄러 활동을](../../automating/using/scheduler.md)참조하십시오.

## 매개 변수를 사용하여 작업 흐름 호출{#workflow-with-parameters}

매개 변수의 이름과 수는 워크플로우를 호출할 때 정의된 내용과 일치해야 합니다 (워크플로우를 호출할 때 매개 변수 [정의 참조](../../automating/using/calling-a-workflow-with-external-parameters.md#defining-the-parameters-when-calling-the-workflow)). 매개 변수 유형도 필요한 값과 일치해야 합니다.

모든 매개 변수가에서 선언되었는지 **[!UICONTROL External signal activity]**&#x200B;확인합니다. 그렇지 않으면 활동을 실행할 때 오류가 발생합니다.

자세한 내용은 외부 매개 변수를 사용하여 워크플로우 [호출을](../../automating/using/calling-a-workflow-with-external-parameters.md)참조하십시오.

## 패키지 내보내기{#exporting-packages}

패키지를 내보내려면 내보내기한 리소스에 기본 ID가 포함되면 안 됩니다. 따라서 내보내기 가능한 리소스의 ID는 Adobe Campaign Standard에서 표준으로 제공된 템플릿에서 다른 이름을 사용하여 변경해야 합니다.
자세한 내용은 패키지 [관리를](../../automating/using/managing-packages.md)참조하십시오.

## 목록 내보내기{#exporting-lists}

[내보내기 목록] 옵션을 사용하면 기본적으로 최대 100,000 개의 선을 내보낼 수 있으며 **NMS_ exportlistlimit 옵션으로 정의할**&#x200B;수 있습니다. 이 옵션은 &gt; **[!UICONTROL Administration]****[!UICONTROL Application settings]** &gt; **[!UICONTROL Options]**에서 기능 관리자가 관리할 수 있습니다.
자세한 내용은 목록 [내보내기를](../../automating/using/exporting-lists.md)참조하십시오.

## 문제 해결{#workflow-troubleshooting}

Adobe Campaign 에서는 워크플로우 문제를 더 잘 이해할 수 있도록 다양한 로그를 제공합니다.

### 워크플로우 로그 사용{#using-workflow-logs}

워크플로우 로그에 액세스하여 활동 실행을 모니터링할 수 있습니다. 수행된 작업과 실행 오류를 시간순으로 인덱싱합니다. 로그 탭은 선택한 모든 활동 또는 일부 활동의 실행 내역에 포함됩니다.
작업 탭에는 활동의 실행 순서 지정이 자세히 설명되어 있습니다. 활동에 대한 자세한 정보를 보려면 작업을 클릭하십시오.
자세한 내용은 워크플로우 실행 [모니터링을](../../automating/using/executing-a-workflow.md#monitoring)참조하십시오.

#### 데이터 관리 활동 문제 해결{#troubleshooting-data-management-activities}

로그 탭에서 SQL 쿼리를 분석할 수 있습니다.

1. 워크플로우 작업 영역에서 **[!UICONTROL Edit properties]**&#x200B;를 클릭합니다.
1. 에서 **[!UICONTROL General]****[!UICONTROL Execution]****[!UICONTROL Save SQL queries in the log]** 및 **[!UICONTROL Execute in the engine]** 옵션을 선택하고를 클릭합니다 **[!UICONTROL Confirm]**.

**로그에서 SQL 쿼리를 보려면 다음을 수행하십시오.**
1. **[!UICONTROL Log and Tasks]**&#x200B;을 클릭합니다.
1. **[!UICONTROL Logs]** 탭에서 **[!UICONTROL Search]** 패널을 엽니다.
1. **[!UICONTROL Display SQL logs only]**&#x200B;확인합니다.

쿼리는 로그 **[!UICONTROL Message]** 열에 표시됩니다.

### 배달 로그 사용{#using-delivery-logs}

배달 로그를 사용하면 배달의 성공률을 모니터링할 수 있습니다. 제외 로그는 전송을 준비하는 동안 제외된 메시지를 반환합니다. 전송 로그는 각 프로필에 대한 배달 상태를 제공합니다.
자세한 내용은 배달 오류 [이해를](../../sending/using/understanding-delivery-failures.md)참조하십시오.

### 배달 알림 사용{#delivery-alerting}

배달 경고 기능은 사용자 그룹이 게재 실행에 대한 정보를 포함하는 알림을 자동으로 수신할 수 있는 경고 관리 시스템입니다.
자세한 내용은 [배달 경고를](../../sending/using/receiving-alerts-when-failures-happen.md)참조하십시오.

**관련 항목:**

* [오류 관리](../../automating/using/executing-a-workflow.md#error-management)
