---
title: 게재 실패 시 경고 받기
description: 경고 관리 시스템을 사용하는 방법을 알아봅니다.
audience: sending
content-type: reference
topic-tags: monitoring-messages
feature: Proofs
role: User
level: Beginner
exl-id: dc8bd1d3-e199-4901-9b1f-7b485879897d
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '2038'
ht-degree: 2%

---

# 게재 실패 시 경고 받기{#receiving-alerts-when-failures-happen}

## 게재 경고 기본 정보 {#about-delivery-alerting}

**게재 경고** 기능은 사용자 그룹이 게재 실행에 대한 정보가 포함된 알림을 자동으로 수신할 수 있도록 하는 경고 관리 시스템입니다.

전송된 알림에는 기본적으로 다음 기준에 따라 보고서가 포함됩니다.

* 실패한 게재
* 준비에 실패한 게재
* 소프트 바운스 오류 비율이 잘못된 게재
* 하드 바운스 오류 비율이 잘못된 게재
* 보류 중인 상태가 평소보다 긴 게재
* 낮은 처리량의 게재
* 게재 진행 중

경고 수신자는 Adobe Campaign에서 처리 중인 게재를 모니터링하고 실행에 문제가 있을 때 적절한 작업을 수행할 수 있습니다.

이러한 경고 알림은 Adobe Campaign 인터페이스의 대시보드를 통해 정의된 특정 경고 기준에 따라 사용자 지정할 수 있습니다.

>[!NOTE]
>
>경고 알림은 이메일로만 제공됩니다.

전송된 알림에는 다음이 포함됩니다.

* 정의한 기준을 충족하는 게재 수와 각 기준에 대해 선택한 레이블/색상을 표시하는 **[!UICONTROL Summary]**.
* 해당 대시보드에 대해 정의된 모든 게재 기준과 각 기준에 대한 모든 게재를 나열하는 **[!UICONTROL Details]** 섹션입니다.

![](assets/delivery-alerting_notification.png)

## 게재 경고 대시보드 {#delivery-alerting-dashboards}

### 게재 경고 대시보드 정보 {#about-delivery-alerting-dashboards}

알림 수신자를 관리하고 경고 기준을 정의하고 경고 기록에 액세스하려면 대시보드를 사용해야 합니다.

>[!NOTE]
>
>대시보드 및 경고 기준에 액세스하고 구성하려면 관리 권한이 있거나 **배달 관리자** 보안 그룹에 나타나야 합니다. 표준 사용자는 Adobe Campaign 인터페이스의 대시보드에 액세스할 수 없습니다. 경고 알림만 수신할 수 있습니다. Adobe Campaign의 사용자 및 보안에 대한 자세한 내용은 [사용자 유형](../../administration/using/users-management.md) 및 [보안 그룹 정보](../../administration/using/managing-groups-and-users.md#about-security-groups)를 참조하십시오.

Adobe Campaign 인터페이스에서 다음을 수행할 수 있습니다.

* 게재 경고 대시보드를 만들고 관리합니다. [게재 경고 대시보드 만들기](#creating-a-delivery-alerting-dashboard)를 참조하세요.
* 각 대시보드에 대한 게재 경고 기준을 정의하고 관리합니다. 예를 들어 준비에 실패한 게재 또는 낮은 처리량만 있는 게재를 기반으로 경고를 작성할 수 있습니다. [경고 조건 정보](#about-alerting-criteria)를 참조하세요.
* 각 대시보드에 대한 기준 매개 변수를 수정합니다. [기준 매개 변수](#criteria-parameters)를 참조하십시오.
* 각 대시보드에 대한 수신자 그룹을 정의합니다.

  예를 들어 관리 권한이 있는 사용자에게 실패한 게재에 대해서만 알리려고 합니다. 하지만 마케팅 사용자가 소프트 바운스 불량 오류 비율이 있는 게재 정보를 받도록 할 수 있습니다. 따라서 두 개의 서로 다른 대시보드를 만들고 각 수신자 그룹에 대해 원하는 기준을 정의해야 합니다.

* 각 대시보드에 대해 전송된 모든 경고 내역에 액세스합니다.

  대시보드를 선택하면 기본적으로 이 대시보드에 대해 마지막으로 전송된 경고가 표시됩니다. 전송된 모든 경고는 화면 왼쪽에 나열됩니다. 해당 경고에 액세스하려면 **[!UICONTROL History]** 목록의 항목을 클릭하십시오.

![](assets/delivery-alerting_dashboard.png)

### 게재 경고 대시보드 만들기 {#creating-a-delivery-alerting-dashboard}

특정 기준에 따라 알림을 다른 사용자 그룹에 보내려면 여러 대시보드를 사용해야 합니다. 새 대시보드를 만들려면 다음 작업을 수행하십시오.

1. **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Delivery alerting]**(으)로 이동합니다.
1. **[!UICONTROL Delivery alerting dashboards]**&#x200B;을(를) 선택하고 **[!UICONTROL Create]**&#x200B;을(를) 클릭합니다 .
1. 현재 대시보드를 활성화하려면 **[!UICONTROL Enabled]** 상자를 선택하세요.

   이 옵션이 비활성화되면 이 대시보드에 연결된 알림이 더 이상 전송되지 않습니다. 이 옵션은 기본적으로 비활성화되어 있습니다.

   ![](assets/delivery-alerting_dashboard_general.png)

1. **[!UICONTROL Alert group]** 드롭다운 목록에서 알림을 보낼 수신자 그룹을 선택합니다. 그룹을 수정하거나 만들려면 [보안 그룹 만들기 및 사용자 할당](../../administration/using/managing-groups-and-users.md#creating-a-security-group-and-assigning-users)을 참조하세요.
1. **[!UICONTROL Delivery alerting criteria]** 섹션에서 **[!UICONTROL Create element]**&#x200B;을(를) 클릭하여 기준을 추가합니다. [경고 조건 정보](#about-alerting-criteria)를 참조하세요.
1. **[!UICONTROL Edit properties]** 단추를 선택하십시오. **[!UICONTROL Criteria parameters]** 탭에서 기준을 적용하는 방법을 정의합니다. [기준 매개 변수](#criteria-parameters)를 참조하십시오.
1. **[!UICONTROL Create]**&#x200B;을(를) 클릭하여 대시보드를 저장합니다.

이제 게재가 이 대시보드에서 정의한 기준을 만족할 때마다 지정된 사용자 그룹에 경고 알림이 전송됩니다.

## 게재 경고 기준 {#delivery-alerting-criteria}

### 경고 기준 정보 {#about-alerting-criteria}

게재 경고 기준에 액세스하려면 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Delivery alerting]**(으)로 이동하여 **[!UICONTROL Delivery alerting criteria]**&#x200B;을(를) 선택하십시오.

![](assets/delivery-alerting_criteria.png)

게재 경고 대시보드에서는 다음 기준을 사용할 수 있습니다.

* **[!UICONTROL Deliveries failed]**: 정의된 범위 내에서 예약된 모든 게재가 잘못된 상태입니다.
* **[!UICONTROL Deliveries with preparation failed]**: 준비 단계(대상 계산 및 콘텐츠 생성)가 실패한 정의된 범위 내에서 수정된 게재가 모두 실패했습니다. 자세한 내용은 [전송 준비](../../sending/using/preparing-the-send.md)를 참조하세요.
* **[!UICONTROL Delivery with bad error ratio for soft bounces]**: 정의된 범위 내에서 **[!UICONTROL In progress]** 이상의 상태와 정의된 비율보다 큰 소프트 바운스 오류 비율로 예약된 모든 게재.
* **[!UICONTROL Delivery with bad error ratio for hard bounces]**: 정의된 범위 내에서 **[!UICONTROL In progress]** 이상의 상태로 예약된 모든 게재에서 하드 바운스 오류 비율이 정의된 비율보다 큽니다.
* **[!UICONTROL Deliveries with long start pending]**: 정의된 범위 내에서 **[!UICONTROL Start pending]** 상태가 정의된 기간보다 긴 모든 게재가 예약되었습니다. **[!UICONTROL Start pending]** 상태는 메시지가 아직 시스템에서 고려되지 않았음을 의미합니다.
* **[!UICONTROL Deliveries with low throughput]**: 정의된 기간 이상 동안 시작된 게재(처리된 메시지의 정의된 비율보다 적으며 정의된 값보다 낮은 처리량을 가짐).
* **[!UICONTROL Deliveries in progress]**: 정의된 범위 내에서 **[!UICONTROL In progress]** 상태로 예약된 모든 게재.

>[!NOTE]
>
>위의 기준에 적용되는 모든 매개변수에는 기본값 값이 있습니다. 이러한 값은 게재 경고 대시보드의 **[!UICONTROL Criteria parameters]** 탭에서 변경할 수 있습니다. [기준 매개 변수](#criteria-parameters)를 참조하십시오.

**[!UICONTROL Delivery alerting criteria]** 목록에서 항목을 선택하여 세부 정보에 액세스할 수 있습니다.

![](assets/delivery-alerting_criteria_definition.png)

각 기준에 대해 다음 설정을 정의할 수 있습니다.

* **[!UICONTROL Indicators to add in alerts]**: 선택한 기준에 해당하는 게재에 대해 알림의 **[!UICONTROL Details]** 섹션에 표시되는 열을 의미합니다.

  ![](assets/delivery-alerting_notification_colums.png)

* **[!UICONTROL Alert type]**(알림 요약에서 게재 기준 옆에 표시되는 레이블과 색상)입니다.

  ![](assets/delivery-alerting_notification_labels.png)

* **[!UICONTROL Criteria frequency]**: 한 번의 게재에 대해 기준이 충족되면 모니터링 기간 내에 전송된 각 알림에서 해당 기준이 반복됩니다. 그렇지 않으면 한 번의 게재에 대해 경고 기준으로 하루에 한 개의 경고만 전송됩니다(첫 번째 발생 시).

  기본적으로 이 옵션은 모든 기준에 대해 하루에 한 번으로 설정됩니다.

**관련 항목:**

* [로그 전송](../../sending/using/monitoring-a-delivery.md#sending-logs)
* [경고 빈도](#alerting-frequency)
* [마케팅 활동 아이콘 및 상태](../../start/using/marketing-activities.md#marketing-activity-icons-and-statuses)

### 게재 경고 기준 만들기 {#creating-a-delivery-alerting-criterion}

요구 사항에 더 잘 부합하도록 새 게재 경고 기준을 만들 수 있습니다.

예를 들어 **[!UICONTROL Finished]** 상태의 모든 게재를 나열하는 알림을 보낼 수 있는 새 기준을 만들 수 있습니다.

이렇게 하려면 먼저 **Delivery** 리소스를 확장하고 **[!UICONTROL Finished]** 상태의 게재만 선택할 수 있는 새 필터를 추가해야 합니다.

1. **Adobe Campaign** > **관리** > **개발** > **사용자 지정 리소스**&#x200B;로 이동하고 **[!UICONTROL Create]**&#x200B;을(를) 클릭합니다.
1. **[!UICONTROL Extend an existing resource]**&#x200B;을(를) 선택하고 드롭다운 목록에서 **[!UICONTROL Delivery]** 리소스를 선택한 다음 **[!UICONTROL Create]**&#x200B;을(를) 클릭하여 편집합니다.

   ![](assets/delivery-alerting_extend-delivery-cus.png)

   기존 리소스 확장에 대한 자세한 내용은 [리소스 정의](../../developing/using/creating-or-extending-the-resource.md)를 참조하십시오.

1. **[!UICONTROL Delivery]** 리소스에서 **[!UICONTROL Filter definition]** 탭으로 이동하여 **[!UICONTROL Add an element]**&#x200B;을(를) 클릭하여 필터를 만듭니다.

   ![](assets/delivery-alerting_new-filter.png)

1. 새 필터 정의를 편집합니다. **[!UICONTROL Filter definition]** 창에서 **[!UICONTROL Status]** 항목을 작업 영역으로 끌어다 놓고 **[!UICONTROL Finished]**&#x200B;을(를) 필터 조건으로 선택합니다.

   ![](assets/delivery-alerting_filter-status.png)

   사용자 지정 필터를 만들고 편집하는 방법에 대한 자세한 내용은 [필터 정의](../../developing/using/configuring-filter-definition.md)를 참조하십시오.

1. 변경 사항을 저장하고 리소스를 게시합니다. 자세한 내용은 [사용자 지정 리소스 게시](../../developing/using/updating-the-database-structure.md#publishing-a-custom-resource)를 참조하십시오.

   필터가 생성되었으며 이제 새 게재 경고 기준에서 선택할 수 있습니다.

1. **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Delivery alerting]**(으)로 이동하고 **[!UICONTROL Delivery alerting criteria]**&#x200B;을(를) 선택한 다음 **[!UICONTROL Create]**&#x200B;을(를) 클릭합니다.
1. **[!UICONTROL Delivery filter applied by this criterion]** 드롭다운 목록에서 방금 만든 필터를 선택합니다.

   ![](assets/delivery-alerting_cus-filter.png)

   기본 기준과 동일한 방법으로 기준의 설정을 정의할 수 있습니다. [경고 조건 정보](#about-alerting-criteria)를 참조하세요.

이러한 기준이 생성되면 게재 경고 대시보드와 기타 기준에 추가할 수 있습니다. [게재 경고 대시보드 정보](#about-delivery-alerting-dashboards)를 참조하세요.

![](assets/delivery-alerting_new-criterion.png)

**관련 항목:**

[리소스 추가 또는 확장](../../developing/using/key-steps-to-add-a-resource.md)

## 게재 경고 매개 변수 {#delivery-alerting-parameters}

### 기준 매개변수 {#criteria-parameters}

[게재 경고 대시보드](#creating-a-delivery-alerting-dashboard)의 **[!UICONTROL Criteria parameters]** 탭에서 이 대시보드에서 선택한 기준에 적용되는 설정을 정의할 수 있습니다.

![](assets/delivery-alerting_dashboard_criteria-parameters.png)

* **[!UICONTROL Delivery target minimum size]**: 예를 들어 이 필드에 100을 입력하면 대상이 100명 이상인 게재에 대해서만 알림이 전송됩니다. 이 매개 변수는 모든 기준에 적용됩니다.
* **[!UICONTROL Monitoring period before and after the contact date (in hours)]**: 현재 시간 전후의 시간 수입니다. 이 시간 범위에 연락 날짜가 있는 게재만 고려됩니다. 이 매개 변수는 모든 기준에 적용됩니다. 기본적으로 이 필드의 값은 24시간으로 설정됩니다.

  연락 날짜에 대한 자세한 내용은 [일정 정보](../../sending/using/about-scheduling-messages.md)를 참조하세요.

* **[!UICONTROL Maximum ratio of soft bounce errors]**: 소프트 바운스 오류 비율이 지정된 값보다 큰 모든 게재에 대해 알림이 전송됩니다. 기본적으로 이 필드의 값은 0.05(5%)로 설정됩니다.

  소프트 바운스 오류에 대한 자세한 내용은 [반송 메일 조건](../../sending/using/understanding-delivery-failures.md#bounce-mail-qualification) 및 [게재 실패 유형 목록](../../sending/using/understanding-delivery-failures.md#delivery-failure-types-and-reasons)을 참조하십시오.

* **[!UICONTROL Maximum ratio of hard bounce errors]**: 하드 바운스 오류 비율이 지정된 값보다 큰 모든 게재에 대해 알림이 전송됩니다. 기본적으로 이 필드의 값은 0.05(5%)로 설정됩니다.

  하드 바운스 오류에 대한 자세한 내용은 [반송 메일 조건](../../sending/using/understanding-delivery-failures.md#bounce-mail-qualification) 및 [배달 오류 유형 목록](../../sending/using/understanding-delivery-failures.md#delivery-failure-types-and-reasons)을 참조하세요.

* **[!UICONTROL Minimum time threshold for delivery in 'Start pending' status (in minutes)]**: 이 필드에 지정된 기간보다 긴 **[!UICONTROL Start pending]** 상태의 모든 게재에 대해 알림이 전송됩니다. **[!UICONTROL Start pending]** 상태는 메시지가 아직 시스템에서 고려되지 않았음을 의미합니다.
* **[!UICONTROL Minimum time required for the computation of the throughput (in minutes)]**: 지정한 기간 이상 동안 **[!UICONTROL In progress]** 상태로 시작된 게재만 **[!UICONTROL Deliveries with low throughput]** 기준으로 고려됩니다.
* **[!UICONTROL Maximum percentage of processed messages for the computation of the throughput]**: 처리된 메시지 비율이 지정된 비율보다 낮은 게재만 **[!UICONTROL Deliveries with low throughput]** 기준으로 고려됩니다.
* **[!UICONTROL Minimum expected throughput (in sent messages per hour)]**: 지정된 값보다 낮은 처리량의 게재만 **[!UICONTROL Deliveries with low throughput]** 기준에 고려됩니다.
* **[!UICONTROL Minimum processed ratio required for 'Deliveries in progress' criterion]**: 처리된 메시지 비율이 지정된 비율보다 높은 게재만 고려합니다.

### 경고 빈도 {#alerting-frequency}

**[!UICONTROL Frequency of delivery alerting]** 옵션을 사용하면 두 경고 전송 사이의 지연을 정의할 수 있습니다. 기본적으로 10분으로 설정되어 있습니다.

**[!UICONTROL Administration]** > **[!UICONTROL Application settings]** > **[!UICONTROL Options]** 메뉴를 통해 이 설정을 변경할 수 있습니다.

>[!NOTE]
>
>이 옵션은 Adobe Campaign에 정의된 모든 대시보드에 적용됩니다. 각 대시보드에 대해 특정 빈도를 설정할 수 없습니다.

## 게재 경고 이유 {#delivery-alerting-reasons}

**게재 경고** 기능을 사용하면 관련된 모든 Adobe Campaign 사용자에게 전자 메일 및 대시보드를 통해 게재 실행 상태에 대해 자동으로 알려줍니다.

이제 게재 경고 알림을 받으면 수행할 수 있는 작업에 대한 몇 가지 팁을 알아볼 수 있습니다.

먼저 게재 **로그** 탭에서 게재 및 증명과 관련된 모든 정보를 확인합니다. 빨간색 및 노란색 아이콘을 사용하면 오류나 경고를 식별할 수 있습니다. 빨간색 아이콘은 게재를 시작할 수 없는 심각한 오류를 나타냅니다.

모든 게재 발생 기록을 보려면 **[!UICONTROL Sending logs]** 탭을 선택합니다. 여기에는 보낸 메시지 및 상태 목록이 포함되어 있습니다. 여기에서 각 수신자(**[!UICONTROL Sent]**, **[!UICONTROL Pending]**, **[!UICONTROL Failed]** 등)에 대한 게재 상태를 확인할 수 있습니다. 자세한 내용은 [로그 전송](../../sending/using/monitoring-a-delivery.md#sending-logs)을 참조하세요.

다음은 게재에 대해 충족되는 기준에 따라 경고 알림을 받는 몇 가지 가능한 이유입니다.

* **[!UICONTROL Deliveries failed]**: 이 기준은 잘못된 상태의 모든 게재를 알려줍니다. 다음과 같은 이유 때문일 수 있습니다.

   * 게재 서버(MTA, 메시지 전송 에이전트) 문제
   * Adobe Campaign 게재 서버와 수신 서버 간의 연결 시간 제한
   * 전달성 문제
   * 잘못된 워크플로

  워크플로우로 게재가 트리거되는 경우 해당 워크플로우가 올바르게 시작되었는지 확인합니다. 자세한 내용은 [워크플로우 실행](../../automating/using/about-workflow-execution.md)을 참조하십시오. 그렇지 않으면 Adobe Campaign 관리자에게 연락하여 문제를 해결하십시오.

* **[!UICONTROL Deliveries with preparation failed]**: 다음 경우 게재를 준비하는 동안 오류가 발생할 수 있습니다.

   * 게재에 제목이 없습니다.
   * 개인화 필드에 잘못된 구문이 있습니다.
   * 대상이 누락되었습니다.
   * 게재가 크기 제한을 초과합니다.

  자세한 내용은 [전송 준비](../../sending/using/preparing-the-send.md)를 참조하세요. 그러나 이러한 오류는 일반적으로 메시지 분석 중에 발견됩니다. [제어 규칙](../../sending/using/control-rules.md)을 참조하세요.

* **[!UICONTROL Delivery with bad error ratio for soft bounces]** 경고의 가능한 원인은 다음과 같습니다.

   * 수신자의 서버가 다운되었습니다.
   * 받는 사람의 사서함이 가득 찼습니다.

  자세한 내용은 게재 로그의 **[!UICONTROL Exclusion logs]** 및 **[!UICONTROL Exclusion causes]** 탭을 확인하십시오. [제외 로그](../../sending/using/monitoring-a-delivery.md#exclusion-logs)를 참조하세요.

  **[!UICONTROL Delivery with bad error ratio for hard bounces]** 경고의 가능한 원인은 다음과 같습니다.

   * 수신자가 차단 목록에 추가하다에 추가되어 더 이상 연락하지 않습니다.
   * 수신자의 이메일 주소가 존재하지 않습니다.
   * 받는 사람의 도메인이 존재하지 않습니다.
   * 수신자 서버가 게재를 차단하고 있습니다.

  소프트 및 하드 바운스 오류를 방지하려면 아래 모범 사례를 따르십시오.

   * 격리된 수신자와 같이 게재 분석 중에 메시지 대상의 한 부분을 제외하도록 필터링 유형화 규칙을 작성합니다. [필터링 규칙 만들기](../../sending/using/filtering-rules.md)를 참조하십시오.
   * 적절한 격리 관리 프로세스를 유지하기 위해 고객 데이터베이스를 정기적으로 업데이트합니다. [격리 정보](../../sending/using/understanding-quarantine-management.md#about-quarantines)를 참조하세요.
   * 일반적으로 최대한 전달성을 향상시킵니다. Adobe Campaign [게재 기능](../../sending/using/about-deliverability.md) 세부 설명서를 참조하고 도움이 필요하면 Adobe Campaign 관리자에게 문의하십시오.

* **[!UICONTROL Deliveries with long start pending]**: 일반적으로 MTA(메시지 전송 에이전트) 수준에서 문제가 있음을 의미합니다. 실행 프로세스에서 일부 리소스를 사용할 수 있을 때까지 기다리고 있습니다. MTA가 시작되지 않았을 수 있습니다.

  **[!UICONTROL Deliveries with low throughput]**: MTA가 너무 느리다는 것을 의미하는 전달성 문제입니다.

  이러한 문제에 대한 자세한 내용은 Adobe Campaign 관리자에게 문의하십시오.

**관련 항목:**

* [게재 실패 이해](../../sending/using/understanding-delivery-failures.md)
* [격리 관리 이해](../../sending/using/understanding-quarantine-management.md)
* [Campaign의 옵트인 및 옵트아웃 기본 정보](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md)
