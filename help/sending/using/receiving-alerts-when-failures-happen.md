---
title: 게재 실패 시 경고 받기
description: 경고 관리 시스템을 사용하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: a3ab733a-e3db-4adc-b930-cd4064b6dc1c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: monitoring-messages
discoiquuid: 0766bd57-c5f1-4f56-ac84-e5a04d3819ec
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 155ed7e50e207e4c4dc0569e5e96b24e712e4be8

---


# 게재 실패 시 경고 받기{#receiving-alerts-when-failures-happen}

## 전달 경고 정보 {#about-delivery-alerting}

배달 **경고** 기능은 사용자 그룹이 배달 실행에 대한 정보가 포함된 알림을 자동으로 수신할 수 있는 경고 관리 시스템입니다.

전송된 알림에는 기본적으로 다음 기준에 따른 보고서가 포함됩니다.

* 실패한 배달
* 준비가 실패한 납품
* 소프트 바운스 오류 비율이 나쁜 게재
* 잘못된 하드 바운스 오류 비율이 있는 배달
* 대기 중인 상태가 평소보다 긴 배달
* 처리량이 낮은 배달
* 배달 진행 중

알림 수신자는 Adobe Campaign에서 처리 중인 전달을 모니터링하고 실행 중 문제가 있을 때 적절한 조치를 취할 수 있습니다.

이러한 경고 알림은 Adobe Campaign 인터페이스의 대시보드를 통해 정의된 특정 경고 기준에 따라 사용자 지정할 수 있습니다.

>[!NOTE]
>
>경고 알림은 이메일로만 전달됩니다.

전송된 알림은 다음을 포함합니다.

* 정의한 기준과 각 기준에 대해 선택한 레이블/색상을 충족하는 배달 수를 **[!UICONTROL Summary]** 표시합니다.
* 해당 대시보드에 대해 정의된 모든 배달 기준과 각 기준에 대한 모든 배달을 나열하는 **[!UICONTROL Details]** 섹션.

![](assets/delivery-alerting_notification.png)

## 전달 알림 대시보드 {#delivery-alerting-dashboards}

### 배달 경고 대시보드 정보 {#about-delivery-alerting-dashboards}

알림의 수신자를 관리하려면 경고 기준을 정의하고 경고 내역에 액세스해야 합니다.

>[!NOTE]
>
>대시보드 및 경고 기준을 액세스하고 구성하려면 관리 권한이 있거나 배달 관리자 **보안 그룹에** 표시되어야 합니다. 표준 사용자는 Adobe Campaign 인터페이스에서 대시보드에 액세스할 수 없습니다. 경고 알림만 받을 수 있습니다. Adobe Campaign의 사용자 및 보안에 대한 자세한 내용은 사용자 [유형](../../administration/using/users-management.md) 및 [보안 그룹을](../../administration/using/managing-groups-and-users.md#about-security-groups)참조하십시오.

Adobe Campaign 인터페이스에서 다음을 수행할 수 있습니다.

* 전달 경고 대시보드를 만들고 관리합니다. 배달 [경고 대시보드](#creating-a-delivery-alerting-dashboard)만들기를 참조하십시오.
* 각 대시보드에 대한 배달 경고 기준을 정의하고 관리합니다. 예를 들어 준비 실패 또는 처리량이 낮은 게재와 함께 전달을 기반으로 경고를 작성할 수 있습니다. 경고 [기준](#about-alerting-criteria)정보를 참조하십시오.
* 각 대시보드의 기준 매개 변수를 수정합니다. 기준 [매개 변수를](#criteria-parameters)참조하십시오.
* 각 대시보드에 대한 수신자 그룹을 정의합니다.

   예를 들어, 실패한 게재에 대한 관리 권한이 있는 사용자에게 알리고자 합니다. 그러나 마케팅 사용자가 소프트 바운스 오류 비율이 낮은 게재에 대한 정보를 수신하게 할 수 있습니다. 따라서 두 개의 서로 다른 대시보드를 만들고 각 수신자 그룹에 대해 원하는 기준을 정의해야 합니다.

* 각 대시보드에 대해 전송된 모든 경고 내역에 액세스합니다.

   대시보드를 선택할 때 이 대시보드에 대해 마지막으로 보낸 경고가 기본적으로 표시됩니다. 전송된 모든 경고는 화면 왼쪽에 나열됩니다. 해당 경고에 액세스하려면 **[!UICONTROL History]** 목록에서 항목을 클릭합니다.

![](assets/delivery-alerting_dashboard.png)

### 배달 경고 대시보드 만들기 {#creating-a-delivery-alerting-dashboard}

특정 기준을 기반으로 다른 사용자 그룹에 알림을 전송하려면 여러 개의 대시보드를 사용해야 합니다. 새 대시보드를 만들려면:

1. > **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Delivery alerting]**&#x200B;로 이동합니다.
1. 을 선택하고 **[!UICONTROL Delivery alerting dashboards]** 클릭합니다 **[!UICONTROL Create]**.
1. 현재 대시보드를 활성화하려면 **[!UICONTROL Enabled]** 확인란을 선택합니다.

   이 옵션을 비활성화하면 이 대시보드에 연결된 알림이 더 이상 전송되지 않습니다. 이 옵션은 기본적으로 비활성화됩니다.

   ![](assets/delivery-alerting_dashboard_general.png)

1. 드롭다운 목록에서 알릴 수신자 그룹을 **[!UICONTROL Alert group]** 선택합니다. 그룹을 수정하거나 만들려면 보안 그룹 [만들기 및 사용자](../../administration/using/managing-groups-and-users.md#creating-a-security-group-and-assigning-users)할당을 참조하십시오.
1. 섹션에서 아이콘을 클릭하여 기준을 **[!UICONTROL Delivery alerting criteria]** **[!UICONTROL Create element]** 추가합니다. 경고 [기준](#about-alerting-criteria)정보를 참조하십시오.
1. 단추를 **[!UICONTROL Edit properties]** 선택합니다. 탭에서 기준이 적용되는 방법을 **[!UICONTROL Criteria parameters]** 정의합니다. 기준 [매개 변수를](#criteria-parameters)참조하십시오.
1. 을 **[!UICONTROL Create]** 클릭하여 대시보드를 저장합니다.

이제 배달을 이 대시보드에서 정의한 기준을 충족할 때마다 지정된 사용자 그룹에 알림 메시지가 전송됩니다.

## 전달 알림 기준 {#delivery-alerting-criteria}

### 경고 기준 정보 {#about-alerting-criteria}

전달 경고 기준에 액세스하려면 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Delivery alerting]** 로 이동하여 **[!UICONTROL Delivery alerting criteria]**&#x200B;선택합니다.

![](assets/delivery-alerting_criteria.png)

배달 경고 대시보드에서 다음 기준을 사용할 수 있습니다.

* **[!UICONTROL Deliveries failed]**:정의된 범위 내에서 잘못된 상태로 예약된 모든 배달.
* **[!UICONTROL Deliveries with preparation failed]**:준비 단계(대상 계산 및 컨텐츠 생성)가 실패한 정의된 범위 내에서 수정된 모든 게재입니다. 자세한 내용은 전송 [준비를](../../sending/using/preparing-the-send.md)참조하십시오.
* **[!UICONTROL Delivery with bad error ratio for soft bounces]**:지정된 범위 내에서 예약된 모든 배달, 최소 상태, **[!UICONTROL In progress]**&#x200B;지정된 비율보다 소프트 바운스 오류 비율 이상.
* **[!UICONTROL Delivery with bad error ratio for hard bounces]**:지정된 범위 내에서 예약된 모든 배달, 최소 상태, **[!UICONTROL In progress]**&#x200B;정의된 비율보다 높은 하드 바운스 오류 비율.
* **[!UICONTROL Deliveries with long start pending]**:정의된 범위 내에서 **[!UICONTROL Start pending]** 상태가 정의된 지속 기간을 초과하는 게재는 **[!UICONTROL Start pending]** 메시지가 아직 시스템에 의해 고려되지 않았음을 의미합니다.
* **[!UICONTROL Deliveries with low throughput]**:Any delivery started for a defined duration, with a defined percentage of a defined percent of processed messages, with a defined value.
* **[!UICONTROL Deliveries in progress]**:정의된 범위 내에서 **[!UICONTROL In progress]** 상태가 있는 모든 배달 예약

>[!NOTE]
>
>위의 기준에 적용되는 모든 매개 변수에는 기본값이 있습니다. 이러한 값은 배달 경고 대시보드의 **[!UICONTROL Criteria parameters]** 탭에서 변경할 수 있습니다. 기준 [매개 변수를](#criteria-parameters)참조하십시오.

목록에서 항목을 선택하여 세부 정보에 액세스할 수 **[!UICONTROL Delivery alerting criteria]** 있습니다.

![](assets/delivery-alerting_criteria_definition.png)

각 기준에 대해 다음 설정을 정의할 수 있습니다.

* **[!UICONTROL Indicators to add in alerts]**, 즉, 선택한 기준에 해당하는 배달에 대한 알림의 **[!UICONTROL Details]** 섹션에 표시되는 열입니다.

   ![](assets/delivery-alerting_notification_colums.png)

* **[!UICONTROL Alert type]**&#x200B;에 표시되는 것은 알림의 요약에서 전달 기준 옆에 표시되는 레이블과 색상을 의미합니다.

   ![](assets/delivery-alerting_notification_labels.png)

* **[!UICONTROL Criteria frequency]**:한 전달에 대한 기준이 충족되면 모니터링 기간 내에 전송된 각 알림에서 반복됩니다. 그렇지 않으면 한 번 배달에 대한 경고 기준으로 하루(첫 번째 발생 시) 하나의 경고만 전송됩니다.

   기본적으로 이 옵션은 모든 기준에 대해 하루에 한 번씩 설정됩니다.

**관련 항목:**

* [로그 보내기](../../sending/using/monitoring-a-delivery.md#sending-logs)
* [경고 빈도](#alerting-frequency)
* [마케팅 활동 아이콘 및 상태](../../start/using/marketing-activities.md#marketing-activity-icons-and-statuses)

### 배달 경고 기준 만들기 {#creating-a-delivery-alerting-criterion}

필요에 맞게 새로운 전달 경고 기준을 만들 수 있습니다.

예를 들어, **[!UICONTROL Finished]** 상태가 있는 모든 게재가 나열된 알림을 전송하도록 새 기준을 만들 수 있습니다.

이렇게 하려면 먼저 배달 **리소스를 확장하고** 새 필터를 추가하여 **[!UICONTROL Finished]** 상태가 있는 게재만 선택할 수 있습니다.

1. Adobe Campaign > **관리** > **개발** > **개발** > 사용자 지정 **리소스 및** **[!UICONTROL Create]**&#x200B;사용자 지정 클릭으로 이동합니다.
1. 을 **[!UICONTROL Extend an existing resource]**&#x200B;선택하고 드롭다운 목록에서 **[!UICONTROL Delivery]** 리소스를 선택한 다음 을 클릭하여 **[!UICONTROL Create]** 편집합니다.

   ![](assets/delivery-alerting_extend-delivery-cus.png)

   기존 리소스 확장에 대한 자세한 내용은 리소스 [정의를 참조하십시오](../../developing/using/creating-or-extending-the-resource.md).

1. 리소스에서 **[!UICONTROL Delivery]** 탭으로 이동하여 을 **[!UICONTROL Filter definition]** **[!UICONTROL Add an element]** 클릭하여 필터를 만듭니다.

   ![](assets/delivery-alerting_new-filter.png)

1. 새 필터 정의를 편집합니다.창에서 **[!UICONTROL Filter definition]** 항목을 작업 영역으로 드래그하여 놓고 필터 **[!UICONTROL Status]** **[!UICONTROL Finished]** 조건으로 선택합니다.

   ![](assets/delivery-alerting_filter-status.png)

   사용자 정의 필터 만들기 및 편집에 대한 자세한 내용은 필터 [정의를](../../developing/using/configuring-filter-definition.md)참조하십시오.

1. 변경 내용을 저장하고 리소스를 게시할 수 있습니다. 자세한 내용은 사용자 [지정 리소스](../../developing/using/updating-the-database-structure.md#publishing-a-custom-resource)게시를 참조하십시오.

   필터가 만들어지며 이제 새 배달 경고 기준에서 선택할 수 있습니다.

1. > **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Delivery alerting]**&#x200B;로 이동하여 **[!UICONTROL Delivery alerting criteria]** 선택하고 **[!UICONTROL Create]**&#x200B;클릭합니다.
1. 드롭다운 **[!UICONTROL Delivery filter applied by this criterion]** 목록에서 방금 만든 필터를 선택합니다.

   ![](assets/delivery-alerting_cus-filter.png)

   기본 기준과 같은 방법으로 기준의 설정을 정의할 수 있습니다. 경고 [기준](#about-alerting-criteria)정보를 참조하십시오.

이러한 기준을 만든 후에는 전달 경고 대시보드뿐만 아니라 다른 기준에 추가할 수 있습니다. 전달 [경고 대시보드](#about-delivery-alerting-dashboards)정보를 참조하십시오.

![](assets/delivery-alerting_new-criterion.png)

**관련 항목:**

[리소스 추가 또는 확장](../../developing/using/key-steps-to-add-a-resource.md)

## 전달 경고 매개 변수 {#delivery-alerting-parameters}

### 기준 매개 변수 {#criteria-parameters}

배달 **[!UICONTROL Criteria parameters]** 경고 대시보드의 [](#creating-a-delivery-alerting-dashboard)탭에서 이 대시보드에서 선택한 기준에 적용되는 설정을 정의할 수 있습니다.

![](assets/delivery-alerting_dashboard_criteria-parameters.png)

* **[!UICONTROL Delivery target minimum size]**:예를 들어 이 필드에 100을 입력하면 대상이 수신자와 같거나 100명 이상인 배달에만 알림이 전송됩니다. 이 매개 변수는 모든 기준에 적용됩니다.
* **[!UICONTROL Monitoring period before and after the contact date (in hours)]**:현재 시간 전후의 시간. 이 시간 범위에 연락처 날짜가 있는 배달만 고려됩니다. 이 매개 변수는 모든 기준에 적용됩니다. 기본적으로 이 필드의 값은 24시간으로 설정됩니다.

   연락처 날짜에 대한 자세한 내용은 예약 [정보를 참조하십시오](../../sending/using/about-scheduling-messages.md).

* **[!UICONTROL Maximum ratio of soft bounce errors]**:지정된 값보다 소프트 바운스 오류 비율이 큰 모든 게재에 대해 알림이 전송됩니다. 기본적으로 이 필드의 값은 0.05(5%)로 설정됩니다.

   소프트 바운스 오류에 대한 자세한 내용은 바운스 [메일 자격](../../sending/using/understanding-delivery-failures.md#bounce-mail-qualification) 및 배달 실패 [유형](../../sending/using/understanding-delivery-failures.md#delivery-failure-types-and-reasons)목록을 참조하십시오.

* **[!UICONTROL Maximum ratio of hard bounce errors]**:하드 바운스 오류 비율이 지정된 값보다 큰 모든 게재에 대해 알림이 전송됩니다. 기본적으로 이 필드의 값은 0.05(5%)로 설정됩니다.

   하드 바운스 오류에 대한 자세한 내용은 바운스 [메일 자격](../../sending/using/understanding-delivery-failures.md#bounce-mail-qualification) 및 [배달 실패 유형](../../sending/using/understanding-delivery-failures.md#delivery-failure-types-and-reasons)목록을 참조하십시오.

* **[!UICONTROL Minimum time threshold for delivery in 'Start pending' status (in minutes)]**:이 필드에 지정된 기간 이상 **[!UICONTROL Start pending]** 상태를 가진 모든 게재에 대해 알림이 전송되며, **[!UICONTROL Start pending]** 이는 메시지가 아직 시스템에 의해 고려되지 않았음을 의미합니다.
* **[!UICONTROL Minimum time required for the computation of the throughput (in minutes)]**:지정된 기간 이상( **[!UICONTROL In progress]** 상태 포함) 시작된 배달만 **[!UICONTROL Deliveries with low throughput]** 기준으로 고려됩니다.
* **[!UICONTROL Maximum percentage of processed messages for the computation of the throughput]**:처리된 메시지의 비율이 지정된 비율보다 낮은 배달만 **[!UICONTROL Deliveries with low throughput]** 기준으로 고려됩니다.
* **[!UICONTROL Minimum expected throughput (in sent messages per hour)]**:처리량이 지정된 값보다 낮은 배달만 **[!UICONTROL Deliveries with low throughput]** 기준으로 고려됩니다.
* **[!UICONTROL Minimum processed ratio required for 'Deliveries in progress' criterion]**:처리된 메시지의 비율이 지정된 비율보다 높은 배달만 고려됩니다.

### 경고 빈도 {#alerting-frequency}

이 **[!UICONTROL Frequency of delivery alerting]** 옵션을 사용하면 두 경고 전송 사이의 지연을 정의할 수 있습니다. 기본적으로 10분으로 설정됩니다.

이 설정은 **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** > **[!UICONTROL Options]** 메뉴를 통해 변경할 수 있습니다.

>[!NOTE]
>
>이 옵션은 Adobe Campaign에 정의된 모든 대시보드에 적용됩니다. 각 대시보드에 대해 특정 빈도를 설정할 수 없습니다.

## 전달 알림 이유 {#delivery-alerting-reasons}

게재 **경고** 기능을 사용하면 관련된 모든 Adobe Campaign 사용자가 이메일 및 대시보드를 통해 게재 실행 상태에 대해 자동으로 알려줍니다.

이제 전달 알림 메시지를 수신하면 몇 가지 팁을 확인할 수 있습니다.

우선, 전달 정보 로그 **탭을 확인하여** 전달 및 증거와 관련된 모든 정보를 볼 수 있습니다. 빨간색 및 노란색 아이콘을 사용하여 오류나 경고를 식별할 수 있습니다. 빨간색 아이콘은 게재를 시작할 수 없는 중요한 오류를 나타냅니다.

게재의 모든 발생 내역을 보려면 **[!UICONTROL Sending logs]** 탭을 선택합니다. 여기에는 보낸 메시지 및 상태 목록이 포함됩니다. 여기에서 각 받는 사람( **[!UICONTROL Sent]**, **[!UICONTROL Pending]****[!UICONTROL Failed]**&#x200B;등)의 배달 상태를 확인할 수 있습니다. 자세한 내용은 로그 [전송을 참조하십시오](../../sending/using/monitoring-a-delivery.md#sending-logs).

다음은 게재에 대해 충족된 기준에 따라 경고 알림을 받아야 하는 몇 가지 이유입니다.

* **[!UICONTROL Deliveries failed]**:이 기준은 잘못된 상태의 모든 배달을 알려줍니다. 다음 때문일 수 있습니다.

   * 배달 서버(MTA, 메시지 전송 에이전트) 문제
   * Adobe Campaign 배달 서버와 수신 서버 간의 연결 시간 초과
   * 전달 가능 문제
   * 잘못된 워크플로우
   워크플로우로 게재가 트리거된 경우 해당 워크플로우가 올바르게 시작되었는지 확인합니다. 자세한 내용은 워크플로우 [실행을](../../automating/using/executing-a-workflow.md)참조하십시오. 그렇지 않으면 Adobe Campaign 관리자에게 연락하여 문제를 해결하십시오.

* **[!UICONTROL Deliveries with preparation failed]**:다음 경우 배달 준비 중에 오류가 발생할 수 있습니다.

   * 배달에는 주제가 없습니다.
   * 개인화 필드에 잘못된 구문이 있습니다.
   * 타겟이 없습니다.
   * 배달이 크기 제한을 초과합니다.
   자세한 내용은 전송 [준비를](../../sending/using/preparing-the-send.md)참조하십시오. 하지만 이러한 오류는 일반적으로 메시지 분석 중에 발견되었습니다. 제어 [규칙을](../../sending/using/control-rules.md)참조하십시오.

* 경고의 가능한 원인은 다음과 **[!UICONTROL Delivery with bad error ratio for soft bounces]** 같습니다.

   * 받는 사람의 서버가 다운되었습니다.
   * 받는 사람의 사서함이 가득 찼습니다.
   자세한 내용은 배달 로그의 **[!UICONTROL Exclusion logs]** 및 **[!UICONTROL Exclusion causes]** 탭을 확인하십시오. 제외 [로그를](../../sending/using/monitoring-a-delivery.md#exclusion-logs)참조하십시오.

   경고의 가능한 원인은 다음과 **[!UICONTROL Delivery with bad error ratio for hard bounces]** 같습니다.

   * 수신자가 블랙리스트에 추가되어 있으므로 더 이상 연락하지 않습니다.
   * 받는 사람의 이메일 주소가 없습니다.
   * 받는 사람의 도메인이 없습니다.
   * 받는 사람의 서버가 배달을 차단하고 있습니다.
   소프트 및 하드 바운스 오류를 방지하려면 아래 우수 사례를 따르십시오.

   * 격리된 받는 사람과 같은 배달 분석 중에 메시지 대상의 한 부분을 제외하는 필터링 유형 규칙을 만듭니다. 필터링 [규칙](../../sending/using/filtering-rules.md)만들기를 참조하십시오.
   * 고객 데이터베이스를 정기적으로 업데이트하여 철저한 격리 관리 프로세스를 유지할 수 있습니다. 검역을 [참조하십시오](../../sending/using/understanding-quarantine-management.md#about-quarantines).
   * 일반적으로 말해서, 가능한 한 최상의 결과물을 얻을 수 있습니다. Adobe Campaign 전달 [기능에](../../sending/using/about-deliverability.md) 대한 자세한 설명서를 참조하고 Adobe Campaign 관리자에게 문의하십시오.



* **[!UICONTROL Deliveries with long start pending]**:일반적으로 MTA(메시지 전송 에이전트) 수준에 문제가 있음을 의미합니다. 실행 프로세스가 일부 리소스의 가용성을 기다리고 있습니다. MTA가 시작되지 않았을 수 있습니다.

   **[!UICONTROL Deliveries with low throughput]**:MTA가 너무 느리다는 것을 의미하는 전달 가능성 문제입니다.

   이러한 문제에 대한 자세한 내용은 Adobe Campaign 관리자에게 문의하십시오.

**관련 항목:**

* [게재 실패 이해](../../sending/using/understanding-delivery-failures.md)
* [스팸 차단 관리 이해](../../sending/using/understanding-quarantine-management.md)
* [Campaign에서 블랙 목록 관리](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md)

