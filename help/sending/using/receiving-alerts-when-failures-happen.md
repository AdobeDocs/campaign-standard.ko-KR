---
title: 장애 발생 시 알림 받기
seo-title: 장애 발생 시 알림 받기
description: 장애 발생 시 알림 받기
seo-description: 경고 관리 시스템을 사용하는 방법에 대해 알아보십시오.
page-status-flag: 정품 인증 안 함
uuid: a 3 ab 733 a-e 3 db -4 adc-b 930-cd 4064 b 6 dc 1 c
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 전송
content-type: 참조
topic-tags: monitoring-messages
discoiquuid: 0766 bd 57-c 5 f 1-4 f 56-ac 84-e 5 a 04 d 3819 ec
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 806dc4736ffb395a0eea102090c688102478aaca

---


# Receiving alerts when failures happen{#receiving-alerts-when-failures-happen}

## About delivery alerting {#about-delivery-alerting}

**배달 경고** 기능은 사용자 그룹이 게재 실행에 대한 정보를 포함하는 알림을 자동으로 수신할 수 있는 경고 관리 시스템입니다.

전송된 알림에는 기본적으로 다음 기준에 기반한 보고서가 포함됩니다.

* 실패한 배달
* 준비가 실패한 배달
* 잘못된 소프트 바운스 오류가 있는 배달
* 잘못된 하드 바운스 오류가 있는 배달
* 보류 중 상태가 평소보다 긴 배달
* 낮은 처리량으로 배달
* 진행 중인 배달

경고 수신자는 Adobe Campaign에서 처리되는 배달을 모니터링하고 실행에 문제가 있을 때 적절한 조치를 취할 수 있습니다.

이러한 알림 알림은 Adobe Campaign 인터페이스에서 대시보드를 통해 정의된 특정 경고 기준에 따라 사용자 정의할 수 있습니다.

>[!NOTE]
>
>알림 알림은 이메일로 배달됩니다.

전송된 알림에는 다음이 포함됩니다.

* A **[!UICONTROL Summary]** displaying the number of deliveries meeting the criteria that you defined and the label/color that you chose for each criterion.
* A **[!UICONTROL Details]** section listing all of the delivery criteria defined for the corresponding dashboard and all of the deliveries for each criterion.

![](assets/delivery-alerting_notification.png)

## Delivery alerting dashboards {#delivery-alerting-dashboards}

### About delivery alerting dashboards {#about-delivery-alerting-dashboards}

알림 수신자의 관리를 관리하려면 알림 기준을 정의하고 경고 기록에 액세스합니다. 대시보드를 사용해야 합니다.

>[!NOTE]
>
>To access and configure the dashboards and the alerting criteria, you must have administration rights or appear in the **Delivery supervisors** security group. 표준 사용자는 Adobe Campaign 인터페이스에서 대시보드에 액세스할 수 없습니다. 알림 알림만 수신할 수 있습니다. For more on users and security in Adobe Campaign, see [Types of users](../../administration/using/types-of-users.md) and [About security groups](../../administration/using/managing-groups-and-users.md#about-security-groups).

Adobe Campaign 인터페이스에서 다음을 수행할 수 있습니다.

* 배달 알림 대시보드를 만들고 관리합니다. See [Creating a delivery alerting dashboard](../../sending/using/receiving-alerts-when-failures-happen.md#creating-a-delivery-alerting-dashboard).
* 각 대시보드에 대한 배달 알림 기준을 정의하고 관리할 수 있습니다. 예를 들어 실패한 준비 또는 낮은 처리량의 배달을 포함한 배달을 기반으로 경고를 작성할 수 있습니다. See [About alerting criteria](../../sending/using/receiving-alerts-when-failures-happen.md#about-alerting-criteria).
* 각 대시보드에 대한 기준 매개 변수를 수정합니다. [기준 매개 변수를 참조하십시오](../../sending/using/receiving-alerts-when-failures-happen.md#criteria-parameters).
* 각 대시보드에 대해 받는 사람 그룹을 정의합니다.

   예를 들어 실패한 배달에 대해서만 관리 권한을 사용자에게 알리려는 경우 하지만 마케팅 사용자가 부드러운 바운스 오류 비율로 배달에 대한 정보를 받을 수 있게 하려면 따라서 두 개의 서로 다른 대시보드를 만들고 각 받는 사람의 그룹에 대해 원하는 기준을 정의해야 합니다.

* 각 대시보드에 대해 전송된 모든 경고 기록에 액세스합니다.

   대시보드를 선택하면 기본적으로 이 대시보드에 대해 마지막으로 전송된 경고가 표시됩니다. 전송된 모든 경고는 화면 왼쪽에 나열됩니다. **[!UICONTROL History]** 목록에서 해당 경고에 액세스하려면 항목을 클릭합니다.

![](assets/delivery-alerting_dashboard.png)

### Creating a delivery alerting dashboard {#creating-a-delivery-alerting-dashboard}

특정 기준에 따른 알림을 다른 사용자 그룹에 전송하려면 여러 대시보드를 사용해야 합니다. 새 대시보드를 만들려면:

1. Go to **[!UICONTROL Administration]** &gt; **[!UICONTROL Channels]** &gt; **[!UICONTROL Delivery alerting]**.
1. **[!UICONTROL Delivery alerting dashboards]****[!UICONTROL Create]**&#x200B;을 선택하고 클릭합니다.
1. Check the **[!UICONTROL Enabled]** box to activate the current dashboard.

   이 옵션을 비활성화하면 이 대시보드에 연결된 알림이 더 이상 전송되지 않습니다. 이 옵션은 기본적으로 비활성화되어 있습니다.

   ![](assets/delivery-alerting_dashboard_general.png)

1. Select the group of recipients that you want to notify from the **[!UICONTROL Alert group]** drop-down list. To modify or create a group, see [Creating a security group and assigning users](../../administration/using/managing-groups-and-users.md#creating-a-security-group-and-assigning-users).
1. **[!UICONTROL Delivery alerting criteria]** 섹션에서를 클릭하여 **[!UICONTROL Create element]** 기준을 추가합니다. See [About alerting criteria](../../sending/using/receiving-alerts-when-failures-happen.md#about-alerting-criteria).
1. **[!UICONTROL Edit properties]** 단추를 선택합니다. **[!UICONTROL Criteria parameters]** 탭에서 기준이 적용되는 방법을 정의합니다. [기준 매개 변수를 참조하십시오](../../sending/using/receiving-alerts-when-failures-happen.md#criteria-parameters).
1. Click **[!UICONTROL Create]** to save the dashboard.

이제 배달이 이 대시보드에서 정의한 기준을 충족할 때마다 알림 알림이 지정된 사용자 그룹에 전송됩니다.

## Delivery alerting criteria {#delivery-alerting-criteria}

### About alerting criteria {#about-alerting-criteria}

To access the delivery alerting criteria, go to **[!UICONTROL Administration]** &gt; **[!UICONTROL Channels]** &gt; **[!UICONTROL Delivery alerting]** and select **[!UICONTROL Delivery alerting criteria]**.

![](assets/delivery-alerting_criteria.png)

배달 경고 대시보드에서 다음 기준을 사용할 수 있습니다.

* **[!UICONTROL Deliveries failed]**: 정의된 범위 내에서 잘못된 상태로 예약된 배달.
* **[!UICONTROL Deliveries with preparation failed]**: 준비 단계 (Target 계산 및 컨텐츠 생성) 가 실패한 정의된 범위 내에서 수정됨. For more on this, see [Preparing the send](../../sending/using/preparing-the-send.md).
* **[!UICONTROL Delivery with bad error ratio for soft bounces]**: 정의된 범위 내에서 최소 바운스 오류 비율이 정의된 비율보다 **[!UICONTROL In progress]**&#x200B;큰 상태로 예약된 범위 내에서 예약된 모든 배달입니다.
* **[!UICONTROL Delivery with bad error ratio for hard bounces]**: 정의된 범위 내에 있는 모든 배달이 정의된 비율보다 더 큰 바운스 **[!UICONTROL In progress]**&#x200B;오류 비율이 있는 상태로 상태가 지정된 범위 내에서 예약됩니다.
* **[!UICONTROL Deliveries with long start pending]**: 정의된 기간 내에 예약된 모든 배달이 **[!UICONTROL Start pending]** 정의된 지속 기간보다 오래 **[!UICONTROL Start pending]** 동안 상태가 시스템에서 고려되지 않았음을 의미합니다.
* **[!UICONTROL Deliveries with low throughput]**: 정의된 백분율이 정의된 비율보다 적은 정의된 기간 동안 시작된 모든 배달이 정의된 값보다 낮은 처리량으로 시작되었습니다.
* **[!UICONTROL Deliveries in progress]**: 정의된 범위 내에서 **[!UICONTROL In progress]** 상태로 예약된 모든 배달.

>[!NOTE]
>
>위의 기준에 적용되는 모든 매개 변수에는 기본값이 있습니다. These values can be changed in the **[!UICONTROL Criteria parameters]** tab of the delivery alerting dashboards. [기준 매개 변수를 참조하십시오](../../sending/using/receiving-alerts-when-failures-happen.md#criteria-parameters).

**[!UICONTROL Delivery alerting criteria]** 목록에서 항목을 선택하여 세부 정보에 액세스할 수 있습니다.

![](assets/delivery-alerting_criteria_definition.png)

각 기준에 대해 다음 설정을 정의할 수 있습니다.

* **[!UICONTROL Indicators to add in alerts]**&#x200B;즉, 선택한 기준에 해당하는 게시에 대한 알림 **[!UICONTROL Details]** 섹션에 표시될 열을 의미합니다.

   ![](assets/delivery-alerting_notification_colums.png)

* **[!UICONTROL Alert type]**&#x200B;즉, 알림 요약의 배달 기준 옆에 표시되는 레이블 및 색상을 의미합니다.

   ![](assets/delivery-alerting_notification_labels.png)

* **[!UICONTROL Criteria frequency]**: 하나의 배달에 대해 기준이 충족되는 경우 모니터링 기간 내에 전송된 각 알림에서 반복됩니다. 그렇지 않으면 한 게시에 대한 경고 기준으로 한 개의 경고만 하루 (첫 번째 발생 시) 에 전송됩니다.

   기본적으로 이 옵션은 모든 기준에 대해 하루에 한 번으로 설정됩니다.

**관련 항목:**

* [로그 보내기](../../sending/using/monitoring-a-delivery.md#sending-logs)
* [경고 빈도](../../sending/using/receiving-alerts-when-failures-happen.md#alerting-frequency)
* [마케팅 활동 아이콘 및 상태](../../start/using/marketing-activities.md#marketing-activity-icons-and-statuses)

### Creating a delivery alerting criterion {#creating-a-delivery-alerting-criterion}

필요에 맞게 새 배달 알림 기준을 만들 수 있습니다.

For example, you can create a new criterion enabling to send a notification listing all deliveries with a **[!UICONTROL Finished]** status.

To do this, you first need to extend the **Delivery** resource and add a new filter allowing you to select only the deliveries with a **[!UICONTROL Finished]** status.

1. **Adobe Campaign** &gt; **관리** &gt; **개발** &gt; **사용자 정의 리소스로** 이동하고를 클릭합니다 **[!UICONTROL Create]**.
1. Select **[!UICONTROL Extend an existing resource]**, select the **[!UICONTROL Delivery]** resource from the drop-down list and click **[!UICONTROL Create]** to edit it.

   ![](assets/delivery-alerting_extend-delivery-cus.png)

   For more on extending an existing resource, see [Define the resource](../../developing/using/creating-or-extending-the-resource.md).

1. **[!UICONTROL Delivery]** 리소스에서 **[!UICONTROL Filter definition]** 탭으로 이동하고 클릭하여 **[!UICONTROL Add an element]** 필터를 만듭니다.

   ![](assets/delivery-alerting_new-filter.png)

1. Edit the new filter definition: in the **[!UICONTROL Filter definition]** window, drag and drop the **[!UICONTROL Status]** item into the workspace and select **[!UICONTROL Finished]** as the filter condition.

   ![](assets/delivery-alerting_filter-status.png)

   For more on creating and editing custom filters, see [Define filters](../../developing/using/configuring-filter-definition.md).

1. 변경 내용을 저장하고 리소스를 게시합니다. For more on this, see [Publishing a custom resource](../../developing/using/updating-the-database-structure.md#publishing-a-custom-resource).

   필터가 만들어지고 새 배달 알림 기준에서 선택할 수 있습니다.

1. **[!UICONTROL Administration]** &gt; **[!UICONTROL Channels]** &gt; **[!UICONTROL Delivery alerting]**&gt;를 **[!UICONTROL Delivery alerting criteria]** 선택하고 클릭합니다 **[!UICONTROL Create]**.
1. **[!UICONTROL Delivery filter applied by this criterion]** 드롭다운 목록에서 방금 만든 필터를 선택합니다.

   ![](assets/delivery-alerting_cus-filter.png)

   기본 기준과 동일한 방법으로 기준 설정을 정의할 수 있습니다. See [About alerting criteria](../../sending/using/receiving-alerts-when-failures-happen.md#about-alerting-criteria).

이러한 기준을 만든 후에는 다른 기준을 비롯하여 배달 경고 대시보드에도 추가할 수 있습니다. See [About delivery alerting dashboards](../../sending/using/receiving-alerts-when-failures-happen.md#about-delivery-alerting-dashboards).

![](assets/delivery-alerting_new-criterion.png)

**관련 항목:**

[리소스 추가 또는 확장](../../developing/using/key-steps-of-adding-a-resource.md)

## Delivery alerting parameters {#delivery-alerting-parameters}

### Criteria parameters {#criteria-parameters}

In the **[!UICONTROL Criteria parameters]** tab of a [delivery alerting dashboard](../../sending/using/receiving-alerts-when-failures-happen.md#creating-a-delivery-alerting-dashboard), you can define the settings that apply to the criteria selected in this dashboard.

![](assets/delivery-alerting_dashboard_criteria-parameters.png)

* **[!UICONTROL Delivery target minimum size]**: 예를 들어 이 필드에 100를 입력하면 100 명 이상의 수신자와 동일한 타겟이 있는 게시에 대해서만 알림이 전송됩니다. 이 매개 변수는 모든 조건에 적용됩니다.
* **[!UICONTROL Monitoring period before and after the contact date (in hours)]**: 현재 시간 전후의 시간. 이 시간 범위에서 연락 날짜가 있는 게시는 고려됩니다. 이 매개 변수는 모든 조건에 적용됩니다. 기본적으로 이 필드의 값은 24 시간으로 설정됩니다.

   For more information on the contact date, see [About the scheduling](../../sending/using/about-scheduling-messages.md).

* **[!UICONTROL Maximum ratio of soft bounce errors]**: 지정된 값보다 부드러운 바운스 오류 비율이 있는 모든 배달에 대해 알림이 전송됩니다. 기본적으로 이 필드의 값은 0.05 (5%) 로 설정됩니다.

   For more on soft bounce errors, see [Bounce mail qualification](../../sending/using/understanding-delivery-failures.md#bounce-mail-qualification) and [List of delivery failure types](../../sending/using/understanding-delivery-failures.md#delivery-failure-types-and-reasons).

* **[!UICONTROL Maximum ratio of hard bounce errors]**: 지정된 값보다 큰 바운스 오류 비율로 모든 배달에 대한 알림이 전송됩니다. 기본적으로 이 필드의 값은 0.05 (5%) 로 설정됩니다.

   For more on hard bounce errors, see [Bounce mail qualification](../../sending/using/understanding-delivery-failures.md#bounce-mail-qualification) and [List of delivery failure types](../../sending/using/understanding-delivery-failures.md#delivery-failure-types-and-reasons).

* **[!UICONTROL Minimum time threshold for delivery in 'Start pending' status (in minutes)]**: 상태가 이 필드에 지정된 기간보다 **[!UICONTROL Start pending]** 긴 모든 배달에 대해 알림이 전송되며 **[!UICONTROL Start pending]** , 상태는 메시지가 아직 시스템에 의해 고려되지 않았음을 의미합니다.
* **[!UICONTROL Minimum time required for the computation of the throughput (in minutes)]**: 지정된 기간 이상의 시작 ( **[!UICONTROL In progress]** 상태 포함) 만 **[!UICONTROL Deliveries with low throughput]** 기준으로 고려됩니다.
* **[!UICONTROL Maximum percentage of processed messages for the computation of the throughput]**: 지정된 비율보다 낮은 처리된 메시지의 백분율이 있는 배달만 **[!UICONTROL Deliveries with low throughput]** 고려됩니다.
* **[!UICONTROL Minimum expected throughput (in sent messages per hour)]**: 지정한 값보다 낮은 처리량을 갖는 배달만 **[!UICONTROL Deliveries with low throughput]** 고려됩니다.
* **[!UICONTROL Minimum processed ratio required for 'Deliveries in progress' criterion]**: 지정된 백분율보다 높은 처리된 메시지의 백분율만 고려됩니다.

### Alerting frequency {#alerting-frequency}

**[!UICONTROL Frequency of delivery alerting]** 이 옵션을 사용하면 두 경고 사이의 지연 시간을 정의할 수 있습니다. 기본적으로 10 분으로 설정됩니다.

**[!UICONTROL Administration]** &gt; **[!UICONTROL Application settings]****[!UICONTROL Options]** &gt; 메뉴를 통해 이 설정을 변경할 수 있습니다.

>[!NOTE]
>
>이 옵션은 Adobe Campaign에 정의된 모든 대시보드에 적용됩니다. 각 대시보드에 대해 특정 빈도를 설정할 수는 없습니다.

## Delivery alerting reasons {#delivery-alerting-reasons}

**배달 알림** 기능은 이메일 및 대시보드를 통해 전달 진행 상태에 대한 정보를 Adobe Campaign 사용자에게 자동으로 알려 줍니다.

전달 알림 알림을 받으면 할 수 있는 작업에 대한 몇 가지 팁이 있습니다.

First of all, check the delivery's **Log** tab to view all information relating to the delivery and proofs. 빨간색 및 노란색 아이콘을 사용하여 오류나 경고를 식별할 수 있습니다. 빨간색 아이콘은 배달이 시작되지 않도록 하는 치명적인 오류를 나타냅니다.

To view the history of every occurrence of a delivery, select the **[!UICONTROL Sending logs]** tab. 보낸 메시지와 상태 목록이 들어 있습니다. There you can check the delivery status for each recipient ( **[!UICONTROL Sent]**, **[!UICONTROL Pending]**, **[!UICONTROL Failed]**, etc.). For more on this, see [Sending logs](../../sending/using/monitoring-a-delivery.md#sending-logs).

다음은 배달용으로 충족되는 기준에 따라 알림 알림을 받는 몇 가지 가능한 이유입니다.

* **[!UICONTROL Deliveries failed]**: 이 기준은 잘못된 상태가 있는 모든 배달을 알려줍니다. 원인은 다음과 같습니다.

   * 배달 서버 (MTA, 메시지 전송 에이전트) 관련 문제
   * Adobe Campaign 배달 서버와 수신 서버 사이의 연결 시간 초과
   * 배달 능력 문제
   * 잘못된 워크플로우
   워크플로우가 워크플로우로 트리거되는 경우 해당 워크플로우가 제대로 시작되었는지 확인하십시오. For more on this, see [Executing a workflow](../../automating/using/executing-a-workflow.md). 그렇지 않으면 Adobe Campaign 관리자에게 문의하여 문제를 해결하십시오.

* **[!UICONTROL Deliveries with preparation failed]**: 다음 경우에 배달 준비 중에 오류가 발생할 수 있습니다.

   * 게시에 제목이 없습니다.
   * 개인화 필드에 잘못된 구문이 있습니다.
   * 타겟이 누락되었습니다.
   * 배달이 크기 제한을 초과합니다.
   For more on this, see [Preparing the send](../../sending/using/preparing-the-send.md). 하지만 이러한 오류는 일반적으로 메시지 분석 중에 발견됩니다. [제어 규칙을 참조하십시오](../../administration/using/control-rules.md).

* The possible causes for a **[!UICONTROL Delivery with bad error ratio for soft bounces]** alert can be:

   * 수신자의 서버가 다운되었습니다.
   * 수신자의 사서함이 꽉 찼습니다.
   For more information, check the **[!UICONTROL Exclusion logs]** and **[!UICONTROL Exclusion causes]** tabs of the delivery logs. [제외 로그를 참조하십시오](../../sending/using/monitoring-a-delivery.md#exclusion-logs).

   The possible causes for a **[!UICONTROL Delivery with bad error ratio for hard bounces]** alert can be:

   * 받는 사람은 블랙리스트에 추가되어 더 이상 연락을 받지 않습니다.
   * 수신자의 이메일 주소가 존재하지 않습니다.
   * 수신자의 도메인이 존재하지 않습니다.
   * 수신자의 서버가 배달을 차단하고 있습니다.
   소프트 바운스 오류를 방지하려면 아래 우수 사례를 따르십시오.

   * 격리된 수신자와 같이 배달 분석 중에 메시지 대상의 한 부분을 제외하기 위한 유형 유형 필터링을 작성합니다. See [Creating a filtering rule](../../administration/using/filtering-rules.md).
   * 적절한 격리 관리 프로세스를 유지하도록 고객 데이터베이스를 정기적으로 업데이트합니다. See [About quarantines](../../sending/using/understanding-quarantine-management.md#about-quarantines).
   * 일반적으로 전달 기능을 최대한 활용할 수 있습니다. See the Adobe Campaign v7 [Managing deliverability](http://docs.campaign.adobe.com/doc/AC/getting_started/EN/deliverability.html) detailed guide and contact your Adobe Campaign administrator for assistance.



* **[!UICONTROL Deliveries with long start pending]**: 일반적으로 MTA (Message Transfer Agent) 수준에서 문제가 발생합니다. 실행 프로세스가 일부 리소스의 가용성을 기다리고 있습니다. MTA가 시작되지 않았을 수 있습니다.

   **[!UICONTROL Deliveries with low throughput]**: 이것은 MTA가 너무 느리다는 것을 의미하는 배달 가능성 문제입니다.

   이러한 문제에 대한 자세한 내용은 Adobe Campaign 관리자에게 문의하십시오.

**관련 항목:**

* [배달 실패 이해](../../sending/using/understanding-delivery-failures.md)
* [격리 관리 이해](../../sending/using/understanding-quarantine-management.md)
* [캠페인의 블랙 리스트 관리](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md)

