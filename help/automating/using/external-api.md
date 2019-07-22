---
title: 외부 API
seo-title: 외부 API
description: 외부 API
seo-description: null
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 타깃팅 활동
context-tags: Externalapi, Workflow, Main
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 1444a636f401ed9c34295aaca1a2b3271d6700a4

---


# External API {#external-api}

## Description {#description}

![](assets/wf_externalAPI.png)

**[!UICONTROL External API]** 활동은 REST API 호출을 통해 **외부 시스템에서** 워크플로우에 **데이터를** 가져옵니다.

The REST endpoints can be a Customer management system, an [Adobe I/O Runtime](https://www.adobe.io/apis/experienceplatform/runtime.html) or an Experience Cloud REST endpoints (Data Platform, Target, Analytics, Campaign, etc).

이 활동의 주요 특성은 다음과 같습니다.

* 5 MB HTTP 응답 데이터 크기 제한
* 아웃바운드 특정 전환을 사용한 오류 관리
* 요청 시간 초과는 60 초입니다.
* HTTP 리디렉션은 허용되지 않습니다.
* HTTPS가 아닌 URL 이 거부됨
* " 수락: application/json "request header and" content-type: application/json "응답 헤더가 허용됩니다.

## Configuration {#configuration}

**[!UICONTROL External API]** 활동을 워크플로우로 드래그하여 놓고 활동을 열어 구성을 시작합니다.

### 인바운드 매핑

인바운드 매핑은 UI에서 표시되고 JSON로 전송할 이전 인바운드 활동에 의해 생성된 임시 테이블입니다.
사용자는 이 임시 테이블을 기반으로 인바운드 데이터를 수정할 수 있습니다.

![](assets/externalAPI-inbound.png)

**인바운드 리소스** 드롭다운에서는 임시 테이블을 만들 쿼리 활동을 선택할 수 있습니다.

The **Add count parameter** checkbox will a count value for each row coming from the temporary table. 이 확인란은 인바운드 활동이 임시 테이블을 생성하는 경우에만 사용할 수 있습니다.

**인바운드 열** 섹션은 사용자가 인바운드 전환 테이블의 필드를 추가할 수 있도록 합니다. 선택한 열이 데이터 개체의 키가 됩니다. JSON의 데이터 개체는 인바운드 전환 테이블의 각 행에서 선택한 열에 대한 데이터를 포함하는 배열 목록이 됩니다.

The **customize parameter** text box lets you add a valid JSON with additional data needed by the external API. 이 추가 데이터는 생성된 JSON의 params 개체에 추가됩니다.

### 아웃바운드 매핑

This tab lets you define the sample **JSON structure** returned by the API Call.

![](assets/externalAPI-outbound.png)

The JSON structure pattern is: **{“data”:[{“key”:“value”}, {“key”:“value”},...]}**

The sample JSON definition must have the **following characteristics**:

* **데이터는** JSON에서 필수 속성 이름이고, "data" 의 내용은 JSON 배열입니다.
* **배열 요소에는** 첫 번째 수준 속성이 포함되어야 합니다 (수준이 지원되지 않음).
   **속성 이름은** 출력 임시 테이블의 출력 스키마에 대한 열 이름이 됩니다.
* **열 이름** 정의는 "데이터" 배열의 첫 번째 요소를 기반으로 합니다.
Columns definition (add/remove) and the type value of the property can be edited in the **Column definition** tab.

**구문 분석이 유효하면** "열 정의" 탭에서 데이터 매핑을 사용자 정의하기 위해 메시지가 나타납니다. 다른 경우에는 오류 메시지가 표시됩니다.

### 실행

This tab lets you define the **HTTPS Endpoint** that will send data to ACS. If needed, you can enter authentication information in the fields below.
![](assets/externalAPI-execution.png)

### 속성

This tab lets you control **general properties** on the external API activity like the displayed label in the UI. 내부 ID를 사용자 지정할 수 없습니다.

![](assets/externalAPI-properties.png)

### 열 정의

    &gt;[! 참고]
    &gt;
    &gt; 이 탭은** 응답 데이터 형식** 이 (가) 발신 매핑 탭에서 완료되고 유효할 때 나타납니다.

**열 정의** 탭에서는 오류를 포함하지 않는 데이터를 가져와서 향후 작업을 위해 Adobe Campaign 데이터베이스에 이미 있는 유형과 일치시킬 수 있도록 각 열의 데이터 구조를 정확하게 지정할 수 있습니다.

![](assets/externalAPI-column.png)

예를 들어, 열의 레이블을 변경할 수 있습니다 (문자열, 정수, 날짜 등).오류 처리를 지정할 수도 있습니다.

For more information, refer to the [Load File](../../automating/using/load-file.md) section.

### 전환

This tab lets you activate the **outbound transition** and its label. This specific transition is useful in case of **timeout** or if the payload exceed the **data size limit**.

![](assets/externalAPI-transition.png)

### 실행 옵션

이 탭은 대부분의 워크플로우 활동에서 사용할 수 있습니다. For more information, consult the [Activity properties](../../automating/using/executing-a-workflow.md#activity-properties) section.

![](assets/externalAPI-options.png)

<!--
## Example: Managing coupons with External API Activity

This example illustrates how to **add coupon value** retrieving by a REST call to profiles and then sending an email containing these coupon values.

The workflow is presented as follows:

![](assets/externalAPI_activity_example1.png)

1. Drag and drop an **External API** activity
    1. Parse the JSON sample responsa as {"data":[{"code":"value"}]}.
    1. Add the **Rest endpoint URL** and define authentication setting if needed
    ![](assets/externalAPI_activity_example2.png)
    1. In the **column definition** tab, add a new column called **code** that will store the code value.
        ![](assets/externalAPI_activity_example3.png)
    1. Enabled an **outbound transition** to manage request failures.
1. Drag and drop a **Query** activity
    1. Configure the **Target** tab to query all the **@adobe.com** email. For different Query samples, refer to the [Query](../../automating/using/query.md) section.
    1. In the **additional data** tab, add a new column based on **rowId()** function. This additional column allows you to reconciliate coupon code with the profile ID..
        ![](assets/externalAPI_activity_example4.png)

        >[!NOTE]
        >
        >This reconciliation approach means that the profile query number is equal to the number of coupon values returned by the REST call.
1. Once this two activities are configured, drag and drop an **Enrichment** activity to associate coupon values with profiles.
    1. Select the previous Query activity in the **primarySet** field.
        ![](assets/externalAPI_activity_example5.png)
    1. Create a new relation in the **Advanced relations** tab, and add the following reconciliation criteria:
    1. **@expr1** coming grom the Query activity in the source expression field.
    1. **@lineNum** as an expression that returns the line number for each coupon value in the destination field.
        ![](assets/externalAPI_activity_example6.png)
        More information on the enrichment activity are available [here](../../automating/using/enrichment.md)

    1. The transition **Data Structure** will contain:
        ![](assets/externalAPI_activity_example7.png)
1. Finally drag and drop a **Send via Email** activity.
    You can modify your email template by adding the **code** personnalized field.

-->
