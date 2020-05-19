---
title: 외부 API
description: null
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: externalAPI,workflow,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 21faea89b3b38f3e667ed6c4de0be6d07f0b7197
workflow-type: tm+mt
source-wordcount: '1703'
ht-degree: 0%

---


# 외부 API {#external-api}

## 설명 {#description}

![](assets/wf_externalAPI.png)

이 **[!UICONTROL External API]** 활동은 **HTTP API** 호출을 통해 **외부 시스템의** 워크플로우로 데이터를가져옵니다.

외부 시스템 끝점은 몇 가지 카테고리를 언급하고 공용 API 끝점, 고객 관리 시스템 또는 서버리스 응용 프로그램 인스턴스(예: [Adobe I/O 런타임](https://www.adobe.io/apis/experienceplatform/runtime.html))일 수 있습니다.

>[!NOTE]
>
>보안상의 이유로 JSSP의 사용은 캠페인 표준에서 지원되지 않습니다. 코드를 실행해야 하는 경우 외부 API 활동을 통해 Adobe I/O 런타임 인스턴스를 호출할 수 있습니다.

이 활동의 주요 특징은 다음과 같습니다.

* JSON 형식의 데이터를 타사 REST API 끝점에 전달하는 기능
* JSON 응답을 다시 받아 출력 테이블에 매핑하고 다운스트림을 다른 워크플로우 활동에 전달하는 기능
* 아웃바운드 특정 전환을 통한 오류 관리

### 베타에서 GA로 전환 {#from-beta-to-ga}

Campaign Standard 20.3 릴리스에서는 외부 API 기능이 제어 베타를 GA(일반 가용성)로 이동했습니다.

>[!CAUTION]
>
>따라서 베타 외부 API 활동을 사용하는 경우 모든 워크플로우에서 GA 외부 API 활동으로 대체해야 합니다.  External API의 베타 버전을 사용하는 워크플로우는 20.3 릴리스부터 작동하지 않습니다.

외부 API 활동을 대체할 때 새 외부 API 활동을 워크플로우에 추가하고 구성 세부 사항을 수동으로 복사한 다음 이전 활동을 삭제합니다.

>[!NOTE]
>
>헤더 값은 활동 내에 마스크되어 있으므로 복사할 수 없습니다.

다음으로, 새로운 외부 API 활동의 데이터를 가리켜거나 사용하기 위해 베타 외부 API 활동의 데이터를 사용하는 워크플로우의 다른 활동을 다시 구성하십시오. 활동의 예: 이메일 전달(개인화 필드), 활동 강화 등

### 제한 및 보장 {#guardrails}

이 활동에는 다음과 같은 보증인이 배치되었다.

* 50MB HTTP 응답 데이터 크기 제한
* 요청 제한 시간은 10분입니다.
* HTTP 리디렉션이 허용되지 않음
* HTTPS가 아닌 URL이 거부됨
* &quot;수락: application/json&quot; 요청 헤더 및 &quot;Content-Type: application/json&quot; 응답 헤더가 허용됩니다.

>[!CAUTION]
>
>활동은 대량의 데이터가 전송될 수 있으므로 각 프로필에 대한 특정 정보를 검색하는 것이 아니라 캠페인 전체 데이터(최신 오퍼 세트, 최신 점수 등)를 가져오기 위한 것입니다. 사용 사례에서 이를 필요로 하는 경우 파일 [전송 활동을](../../automating/using/transfer-file.md) 사용하는 것이 좋습니다.


JSON에는 다음과 같은 특정 보증서가 있습니다.

* **JSON 최대 깊이**: 처리할 수 있는 사용자 지정 중첩 JSON의 최대 깊이를 10개 수준으로 제한합니다.
* **JSON 최대 키 길이**: 생성된 내부 키의 최대 길이를 255로 제한합니다. 이 키는 열 ID와 연결됩니다.
* **허용되는 JSON 최대 복제 키**:  열 ID로 사용되는 복제 JSON 속성 이름의 최대 총 개수를 150개로 제한합니다.


활동은 다음과 같이 JSON 구조가 지원되지 않습니다.

* 배열 개체와 다른 비 배열 요소 결합
* JSON 배열 개체는 하나 이상의 중간 배열 개체 내에 중첩됩니다.


## 구성 {#configuration}

활동을 워크플로우로 드래그하여 놓고 활동을 열어 구성을 시작합니다. **[!UICONTROL External API]**

### 인바운드 매핑

인바운드 매핑은 UI에서 JSON으로 표시되고 전송되는 이전 인바운드 활동으로 생성된 임시 테이블입니다.
사용자는 이 임시 테이블을 기반으로 인바운드 데이터를 수정할 수 있습니다.

![](assets/externalAPI-inbound.png)

인바운드 **리소스** 드롭다운을 사용하여 임시 테이블을 만들 쿼리 활동을 선택할 수 있습니다.

카운트 매개 변수 **추가** 확인란은 임시 테이블에서 나오는 각 행에 대한 카운트 값을 추가합니다. 이 확인란은 인바운드 활동이 임시 테이블을 생성하는 경우에만 사용할 수 있습니다.

인바운드 **열** 섹션에서는 인바운드 전환 테이블에서 필드를 추가할 수 있습니다. 선택한 열이 데이터 개체의 키가 됩니다. JSON의 데이터 개체는 인바운드 전환 테이블의 각 행에서 선택한 열에 대한 데이터가 포함된 배열 목록이 됩니다.

사용자 **지정 매개 변수** 텍스트 상자를 사용하면 외부 API에 필요한 추가 데이터가 포함된 유효한 JSON을 추가할 수 있습니다. 생성된 JSON의 params 개체에 이 추가 데이터가 추가됩니다.

### 아웃바운드 매핑

이 탭에서는 API 호출에서 반환되는 샘플 **JSON 구조를** 정의할 수 있습니다.

![](assets/externalAPI-outbound.png)

JSON 구문 분석기는 몇 가지 예외를 제외하고 표준 JSON 구조 패턴 유형을 수용하도록 설계되었습니다. 표준 패턴의 예는 다음과 같습니다.`{“data”:[{“key”:“value”}, {“key”:“value”},...]}`

샘플 JSON 정의에는 **다음 특성이 있어야 합니다**.

* **배열 요소에는** 첫 번째 수준 속성이 포함되어야 합니다(더 깊은 레벨은 지원되지 않음).
   **속성 이름은** 출력 임시 테이블의 출력 스키마에 대한 열 이름이 됩니다.
* **캡처할 JSON 요소는** JSON 응답 내에 10개 이하의 중첩 수준이어야 합니다.
* **열 이름** 정의는 &quot;data&quot; 배열의 첫 번째 요소를 기반으로 합니다.
열 정의(추가/제거) 및 속성의 유형 값은 열 정의 **탭에서 편집할 수** 있습니다.

**분리 확인란** 동작:

분리 확인란(기본값: 선택 안 함)은 JSON을 키/값 맵으로 병합할지 여부를 나타내기 위해 제공됩니다.

* 이 **확인란을 선택 취소하지** 않으면 샘플 JSON을 구문 분석하여 배열 개체를 찾습니다. 사용자는 Adobe Campaign에서 사용자가 사용하려는 배열을 정확하게 파악할 수 있도록 트리밍된 버전의 API 응답 샘플 JSON 포맷을 제공해야 합니다. 워크플로우 작성 시, 중첩된 배열 개체의 경로가 결정 및 기록되므로 실행 시 API 호출에서 수신되는 JSON 응답 본문에서 해당 배열 개체에 액세스하는 데 사용할 수 있습니다.

* 이 **확인란을 활성화** (선택 사항)하면 샘플 JSON이 분리되고 제공된 샘플 JSON에 지정된 모든 속성이 출력 임시 테이블의 열을 만드는 데 사용되고 열 정의 탭에 표시됩니다. 샘플 JSON에 배열 개체가 있으면 해당 배열 개체의 모든 요소도 분리됩니다.


파싱이 **확인되면**&#x200B;메시지가 나타나고 &quot;열 정의&quot; 탭에서 데이터 매핑을 사용자 정의할 수 있도록 초대합니다. 다른 경우에는 오류 메시지가 표시됩니다.

### 실행

이 탭에서는 ACS로 데이터를 전송할 **HTTPS 종단점을** 정의할 수 있습니다. 필요한 경우 아래 필드에 인증 정보를 입력할 수 있습니다.
![](assets/externalAPI-execution.png)

### 속성

이 탭에서는 UI에 표시된 레이블과 같은 외부 API 활동에 대한 **일반 속성을** 제어할 수 있습니다. 내부 ID를 사용자 지정할 수 없습니다.

![](assets/externalAPI-properties.png)

### 열 정의

>[!NOTE]
>
>이 탭은 [아웃바운드 매핑] 탭에서 **응답 데이터 형식** 을 완료하고 검증한 경우에 나타납니다.

열 정의 **** 탭을 사용하면 오류가 없는 데이터를 가져와서 향후 작업을 위해 Adobe Campaign 데이터베이스에 이미 있는 유형과 일치하도록 하기 위해 각 열의 데이터 구조를 정확하게 지정할 수 있습니다.

![](assets/externalAPI-column.png)

예를 들어 열의 레이블을 변경하고 해당 유형(문자열, 정수, 날짜 등)을 선택할 수 있습니다. 오류 처리를 지정할 수도 있습니다.

자세한 내용은 파일 [로드 섹션을](../../automating/using/load-file.md) 참조하십시오.

### 전환

이 탭에서는 **아웃바운드 전환** 및 해당 레이블을 활성화할 수 있습니다. 이 특정 전환은 **시간** 초과나 페이로드가 **데이터 크기 제한을 초과하는 경우에 유용합니다**.

![](assets/externalAPI-transition.png)

### 실행 옵션

이 탭은 대부분의 워크플로우 활동에서 사용할 수 있습니다. 자세한 내용은 [활동 속성](../../automating/using/activity-properties.md) 섹션을 참조하십시오.

![](assets/externalAPI-options.png)

## 문제 해결

이 새로운 워크플로우 활동에 추가된 로그 메시지 유형은 다음과 같습니다. 정보 및 오류. 잠재적인 문제를 해결하는 데 도움이 될 수 있습니다.

### 정보

이러한 로그 메시지는 워크플로우 활동을 실행하는 동안 유용한 체크포인트에 대한 정보를 기록하는 데 사용됩니다. 특히 다음 로그 메시지는 API에 액세스하기 위한 첫 번째 시도와 재시도(첫 번째 시도가 실패한 이유)를 기록하는 데 사용됩니다.

<table> 
 <thead> 
  <tr> 
   <th> 메시지 형식<br /> </th> 
   <th> 예<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> API URL '%s'을(를) 호출하는 중입니다.</td> 
   <td> <p>API URL 'https://example.com/api/v1/web-coupon?count=2' 호출.</p></td> 
  </tr> 
  <tr> 
   <td> API URL '%s'을(를) 다시 시도하고 있습니다. 이전 시도가 실패했습니다('%s').</td> 
   <td> <p>API URL 'https://example.com/api/v1/web-coupon?count=2'을 다시 시도하는 중, 이전 시도가 실패했습니다('HTTP - 401').</p></td>
  </tr> 
  <tr> 
   <td> '%s'(%s / %s)에서 컨텐츠를 전송하는 중입니다.</td> 
   <td> <p>'https://example.com/api/v1/web-coupon?count=2'(1234 / 1234)에서 내용 전송.</p></td> 
  </tr>
 </tbody> 
</table>

### 오류

이러한 로그 메시지는 예기치 않은 오류 조건에 대한 정보를 기록하는 데 사용되며 이로 인해 워크플로우 활동이 실패할 수 있습니다.

<table> 
 <thead> 
  <tr> 
   <th> 코드 - 메시지 형식<br /> </th> 
   <th> 예<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> WKF-560250 - API 요청 본문 초과 제한(제한: '%d').</td> 
   <td> <p>API 요청 본문이 한도를 초과했습니다(제한: '5242880').</p></td> 
  </tr> 
  <tr> 
   <td> WKF-560239 - API 응답 초과 제한(제한: '%d').</td> 
   <td> <p>API 응답이 한도를 초과했습니다(제한: 5242880').</p></td> 
  </tr> 
  <tr> 
   <td> WKF-560245 - API URL을 구문 분석할 수 없습니다(오류: '%d').</td> 
   <td> <p>API URL을 구문 분석할 수 없습니다(오류: '-2010').</p>
   <p> 참고: 이 오류는 API URL이 유효성 검사 규칙에 실패할 때 기록됩니다.</p></td>
  </tr> 
  <tr>
   <td> WKF-560244 - API URL 호스트는 'localhost' 또는 IP 주소 리터럴(URL 호스트: '%s').</td> 
   <td> <p>API URL 호스트는 'localhost' 또는 IP 주소 리터럴(URL 호스트: 'localhost').</p>
    <p>API URL 호스트는 'localhost' 또는 IP 주소 리터럴(URL 호스트: '192.168.0.5').</p>
    <p>API URL 호스트는 'localhost' 또는 IP 주소 리터럴(URL 호스트: '[2001]').</p></td>
  </tr> 
  <tr> 
   <td> WKF-560238 - API URL은 보안 URL(https)(요청된 URL: '%s').</td> 
   <td> <p>API URL은 보안 URL(https)(요청된 URL: 'https://example.com/api/v1/web-coupon?count=2').</p></td> 
  </tr> 
  <tr> 
   <td> WKF-560249 - 요청 본문 JSON을 만들지 못했습니다. '%s'을(를) 추가하는 동안 오류가 발생했습니다.</td> 
   <td> <p>요청 본문 JSON을 만들지 못했습니다. 'params'를 추가하는 동안 오류가 발생했습니다.</p>
    <p>요청 본문 JSON을 만들지 못했습니다. 'data'를 추가하는 동안 오류가 발생했습니다.</p></td>
  </tr> 
  <tr> 
   <td> WKF-560246 - HTTP 헤더 키가 잘못되었습니다(헤더 키: '%s').</td> 
   <td> <p>HTTP 헤더 키가 잘못되었습니다(헤더 키: '%s').</p>
   <p> 참고: 이 오류는 사용자 지정 헤더 키가 <a href="https://tools.ietf.org/html/rfc7230#section-3.2.html">RFC에 따라 유효성 검사에 실패할 때 기록됩니다</a></p></td> 
  </tr>
 <tr> 
   <td> WKF-560248 - HTTP 헤더 키가 허용되지 않음(헤더 키: '%s').</td> 
   <td> <p>HTTP 헤더 키가 허용되지 않음(헤더 키: 수락).</p></td> 
  </tr> 
  <tr> 
   <td> WKF-560247 - AHTTP 헤더 값이 잘못되었습니다(헤더 값: '%s').</td> 
   <td> <p>HTTP 헤더 값이 잘못되었습니다(헤더 값: '%s'). </p>
    <p>참고: 이 오류는 사용자 지정 헤더 값이 <a href="https://tools.ietf.org/html/rfc7230#section-3.2.html">RFC에 따라 유효성 검사에 실패할 때 기록됩니다</a></p></td> 
  </tr> 
  <tr> 
   <td> WKF-560240 - JSON 페이로드에 잘못된 속성 '%s'이(가) 있습니다.</td> 
   <td> <p>JSON 페이로드에 잘못된 속성 'blah'가 있습니다.</p></td>
  </tr> 
  <tr>
   <td> WKF-560241 - 잘못된 형식의 JSON 또는 허용되지 않는 형식입니다.</td> 
   <td> <p>형식이 잘못된 JSON 또는 허용되지 않는 형식입니다.</p>
   <p>참고: 이 메시지는 외부 API의 응답 본문을 구문 분석하는 경우에만 적용되며, 응답 본문이 이 활동에서 지정한 JSON 형식을 준수하는지 여부를 확인하려고 할 때 기록됩니다.</p></td>
  </tr>
  <tr> 
   <td> WKF-560246 - 활동이 실패했습니다(이유: '%s').</td> 
   <td> <p>HTTP 401 오류 응답으로 인해 활동이 실패하는 경우 - 활동이 실패했습니다(이유: 'HTTP - 401')</p>
        <p>실패한 내부 호출로 인해 활동이 실패하는 경우 - 활동이 실패했습니다(이유: 'Rc - -N').</p>
        <p>잘못된 Content-Type 헤더로 인해 활동이 실패하는 경우 - 활동 실패(이유: 'Content-Type - application/html').</p></td> 
  </tr>
 </tbody> 
</table>

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
