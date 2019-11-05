---
title: 증가식 쿼리
description: 증분 쿼리 활동을 사용하면 Adobe Campaign 데이터베이스에서 요소 모집단을 필터링하고 추출할 수 있습니다.
page-status-flag: 활성화 안 함
uuid: 73b42422-e815-43ef-84c0-97c4433ccc98
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 자동화
content-type: reference
topic-tags: 타깃팅 활동
discoiquuid: 80961e73-42ec-46 파섹
context-tags: 증분,기본
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 증가식 쿼리{#incremental-query}

## 설명 {#description}

![](assets/incremental.png)

이 **[!UICONTROL Incremental query]** 활동을 통해 Adobe Campaign 데이터베이스에서 요소 모집단을 필터링하고 추출할 수 있습니다. 이 활동이 실행될 때마다 이전 실행의 결과는 제외됩니다. 이렇게 하면 새 요소만 타깃팅할 수 있습니다.

전용 탭을 통해 타깃팅된 **[!UICONTROL Additional data]** 모집단에 대해 정의할 수 있습니다. 이 데이터는 추가 열에 저장되며 진행 중인 워크플로우에만 사용할 수 있습니다.

활동은 쿼리 편집기 도구를 사용합니다. 이 도구는 [전용 섹션에](../../automating/using/editing-queries.md#about-query-editor)자세히 설명되어 있습니다.

## 사용 상황 {#context-of-use}

워크플로우의 실행 빈도와 쿼리를 정의하려면 에 **[!UICONTROL Incremental query]** 연결해야 **[!UICONTROL Scheduler]** 합니다.

이 활동과 관련된 **[!UICONTROL Processed data]** 탭에서는 필요한 경우 활동의 이전 실행 결과를 볼 수 있습니다.

이 **[!UICONTROL Incremental query]** 활동은 다양한 유형의 용도로 사용할 수 있습니다.

* 메시지, 대상 등을 정의하기 위한 개인 세그먼트화
* 데이터 내보내기를 참조하십시오.

## 구성 {#configuration}

1. 워크플로우를 워크플로우로 드래그하여 **[!UICONTROL Incremental query]** 놓을 수 있습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 엽니다.
1. 프로필 리소스 이외의 리소스에서 쿼리를 실행하려면 활동의 **[!UICONTROL Properties]** 탭으로 이동하여 **[!UICONTROL Resource]** 및 **[!UICONTROL Targeting dimension]** a를 선택합니다.

   The **[!UICONTROL Resource]** allows you to refine the filters displayed in the palette while the contextual **[!UICONTROL Targeting dimension]**, contextual to the resource selected, delivery, data linked to the selected resource, etc.

1. 탭에서 규칙을 정의하고 결합하여 쿼리를 **[!UICONTROL Target]** 실행합니다.
1. 탭에서 워크플로우의 다음 실행에 사용할 증분 모드를 선택합니다. **[!UICONTROL Processed data]**

   * **[!UICONTROL Use the exclusion of the results of previous executions]**:새 실행에 대한 이전 실행 결과는 제외됩니다.
   * **[!UICONTROL Use a date field]**:다음 실행은 선택된 날짜 필드가 **[!UICONTROL Incremental query]** 활동의 마지막 실행 날짜 이상인 결과만 고려합니다. 탭에서 선택한 리소스와 관련된 날짜 필드를 선택할 수 **[!UICONTROL Properties]** 있습니다. 로그 데이터와 같은 큰 리소스를 쿼리할 때 이 모드의 성능이 향상됩니다.

      워크플로우가 처음 실행된 후 다음 실행에 사용될 마지막 실행 날짜를 이 탭에서 볼 수 있습니다. 워크플로우가 실행될 때마다 자동으로 업데이트됩니다. 필요에 맞게 새 값을 수동으로 입력하여 이 값을 재정의할 수도 있습니다.
   >[!NOTE]
   >
   >이 **[!UICONTROL Use a date field]** 모드에서는 선택한 날짜 필드에 따라 보다 유연하게 사용할 수 있습니다. 예를 들어 선택한 필드가 수정 날짜에 해당하는 경우 날짜 필드 모드에서는 최근에 업데이트된 데이터를 검색할 수 있고 다른 모드는 워크플로우의 마지막 실행 이후 수정된 레코딩이라도 이전 실행에서 이미 타깃팅된 레코딩을 제외합니다.

   ![](assets/incremental_query_usedatefield.png)

1. 전용 탭을 통해 타깃팅된 **[!UICONTROL Additional data]** 모집단에 대해 정의할 수 있습니다. 이 데이터는 추가 열에 저장되며 진행 중인 워크플로우에만 사용할 수 있습니다. 특히 쿼리의 타깃팅 차원에 연결된 Adobe Campaign 데이터베이스 테이블에서 데이터를 추가할 수 있습니다. 데이터 [수집](../../automating/using/query.md#enriching-data) 섹션을 참조하십시오.
1. 활동 구성을 확인하고 워크플로우를 저장합니다.

## 데이터 강화 {#enriching-data}

쿼리의 경우와 마찬가지로, **[!UICONTROL Incremental query]** 데이터 [수집](../../automating/using/query.md#enriching-data) 섹션을 참조하십시오.

## 예:서비스의 가입자에 대한 증분 쿼리 {#example--incremental-query-on-subscribers-to-a-service}

다음 예는 Newsletter 실행 서비스에 가입한 Adobe Campaign 데이터베이스의 프로필을 필터링하여 **[!UICONTROL Incremental query]** 프로모션 코드가 포함된 환영 이메일을 **** 발송하는 활동 구성을 보여줍니다.

워크플로우는 다음 요소로 구성됩니다.

![](assets/incremental_query_example1.png)

* 매주 월요일 오전 6시에 워크플로우를 실행하는 **[!UICONTROL Scheduler]** 활동.

   ![](assets/incremental_query_example2.png)

* 첫 번째 실행 동안 현재 모든 가입자를 대상으로 한 **[!UICONTROL Incremental query]** 활동이며 다음 실행 중 해당 주의 새 구독자만 타깃팅합니다.

   ![](assets/incremental_query_example3.png)

* 활동 **[!UICONTROL Email delivery]** . 워크플로우는 일주일에 한 번 실행되지만, 한 주가 아닌 한 달 동안의 기간 동안 보고서를 생성하는 등 전송된 이메일과 월별 결과를 집계할 수 있습니다.

   이렇게 하려면 이메일과 결과를 다시 그룹화하는 **[!UICONTROL Recurring email]** 여기에서 이메일을 만듭니다 **[!UICONTROL By month]**.

   이메일의 내용을 정의하고 환영 프로모션 코드를 삽입합니다.

   자세한 내용은 이메일 배달 [및](../../automating/using/email-delivery.md) 이메일 컨텐츠 [정의](../../designing/using/personalization.md) 섹션을 참조하십시오.

그런 다음 워크플로우 실행을 시작합니다. 새 구독자는 매주 프로모션 코드와 함께 환영 이메일을 받게 됩니다.

## 예:배달 로그의 증분 쿼리 {#example--incremental-query-on-delivery-logs}

활동을 사용하여 새 로그를 정기적으로 파일로 내보낼 수 있습니다. **[!UICONTROL Incremental query]** 외부 보고 또는 BI 도구에서 로그 데이터를 사용하려는 경우 유용합니다.

전체 예는 [로그 내보내기] [섹션에서 사용할 수](../../automating/using/exporting-logs.md) 있습니다.
