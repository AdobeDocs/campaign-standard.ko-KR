---
title: 외부 API
description: null
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: externalAPI,workflow,main
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '2269'
ht-degree: 100%

---


# 외부 API {#external-api}

## 설명 {#description}

![](assets/wf_externalAPI.png)

**[!UICONTROL External API]** 활동은 **HTTP API** 호출을 통해 **외부 시스템**&#x200B;의 워크플로우로 데이터를 가져옵니다.

외부 시스템 엔드포인트는 퍼블릭 API 엔드포인트, 고객 관리 시스템 또는 서버리스 애플리케이션 인스턴스(예: [Adobe I/O Runtime](https://www.adobe.io/apis/experienceplatform/runtime.html))일 수 있습니다.

>[!NOTE]
>
>보안상의 이유로 Campaign Standard에서는 JSSP 사용이 지원되지 않습니다. 코드를 실행해야 하는 경우 외부 API 활동을 통해 Adobe I/O Runtime 인스턴스를 호출할 수 있습니다.

이 활동의 주요 특징은 다음과 같습니다.

* JSON 포맷의 데이터를 타사 REST API 엔드포인트에 전달하는 기능
* JSON 응답을 다시 수신하여 출력 테이블에 매핑하고 다른 워크플로우 활동으로 다운스트림을 전달하는 기능
* 아웃바운드 특정 전환을 통한 장애 관리

### 이전 버전과의 호환성 알림 {#from-beta-to-ga}

Campaign Standard 20.4 릴리스에서는 모범 사례에 맞게 http 응답 데이터 크기 제한 및 응답 시간 제한이 완화되었습니다(&quot;제한 및 보호 기능&quot; 섹션 참조). 이러한 보안 수정 사항은 기존 외부 API 활동에는 적용되지 않습니다. 따라서 모든 워크플로우에서 기존 외부 API 활동을 새 버전으로 대체하는 것이 좋습니다.

Campaign Standard 20.2(또는 이전 버전)에서 업그레이드하는 경우, 외부 API 기능이 Campaign Standard 20.3 릴리스의 Beta에서 일반 출시로 이동했습니다.

따라서 Beta 외부 API 활동을 사용하는 경우 모든 워크플로우에서 GA(일반 출시) 외부 API 활동으로 바꾸어야 합니다.  외부 API의 베타 버전을 사용하는 워크플로우는 Campaign Standard 20.3 릴리스부터 작동하지 않습니다.

외부 API 활동을 바꿀 때 새 외부 API 활동을 워크플로우에 추가하고 구성 세부 사항을 수동으로 복사한 다음 이전 활동을 삭제합니다.

>[!NOTE]
>
>활동 지정 헤더 값은 활동 내에 마스킹되어 있으므로 복사할 수 없습니다.

다음으로, Beta 외부 API 활동의 데이터를 가리키거나 사용하는 워크플로우의 다른 활동을 다시 구성하여 대신 새로운 외부 API 활동의 데이터를 가리키거나 사용합니다. 예를 들어 이메일 게재(개인화 필드), 데이터 보강 활동 등의 활동이 있습니다.

### 제한 및 보호 기능 {#guardrails}

이 활동에는 다음과 같은 보호 기능이 적용됩니다.

* 5MB http 응답 데이터 크기 제한(참고:이전 릴리스의 50MB 제한에서 변경됨)
* 요청 시간 제한은 1분(참고:이전 릴리스의 10분 시간 제한에서 변경한 내용)
* HTTP 리디렉션이 허용되지 않음
* HTTPS가 아닌 URL은 거부됨
* &quot;Accept: application/json&quot; 요청 헤더 및 &quot;Content-Type: application/json&quot; 응답 헤더가 허용됨

다음과 같은 가드 레일이 배치되었습니다.

* **JSON 최대 깊이**: 처리할 수 있는 사용자 지정 중첩 JSON의 최대 깊이를 10개 수준으로 제한합니다.
* **JSON 최대 키 길이**: 생성된 내부 키의 최대 길이를 255로 제한합니다. 이 키는 열 ID와 연결됩니다.
* **허용되는 JSON 최대 중복 키**: 열 ID로 사용되는 중복 JSON 속성 이름의 최대 총 개수를 150개로 제한합니다.

>[!CAUTION]
>
>외부 API 활동은 캠페인 전체 데이터(최신 오퍼 집합, 최신 점수 등)를 가져오기 위한 것이며 대량의 데이터가 전송될 수 있으므로 각 프로필에 대한 특정 정보를 검색하기 위한 것이 아닙니다. 사용 사례에서 이를 필요로 하는 경우 [파일 전송](../../automating/using/transfer-file.md) 활동을 사용하는 것이 좋습니다.

## 구성 {#configuration}

**[!UICONTROL External API]** 활동을 워크플로우로 끌어서 놓고 활동을 열어 구성을 시작합니다.

### 인바운드 매핑

인바운드 매핑은 UI에서 JSON으로 표시되고 전송되는 이전 인바운드 활동에 의해 생성된 임시 테이블입니다. 이 임시 테이블을 기반으로 사용자는 인바운드 데이터를 수정할 수 있습니다.

![](assets/externalAPI-inbound.png)

**인바운드 리소스** 드롭다운을 사용하여 임시 테이블을 생성할 쿼리 활동을 선택할 수 있습니다.

**카운트 매개 변수 추가** 확인란은 임시 테이블에서 얻은 각 행에 대해 카운트 값을 추가합니다. 이 확인란은 인바운드 활동이 임시 테이블을 생성하는 경우에만 사용할 수 있습니다.

사용자는 **인바운드 열** 섹션을 통해 인바운드 전환 테이블에서 모든 필드를 추가할 수 있습니다. 선택한 열이 데이터 개체의 키가 됩니다. JSON의 데이터 개체는 인바운드 전환 테이블의 각 행에서 선택한 열에 대한 데이터가 포함된 배열 목록입니다.

**사용자 지정 매개 변수** 입력란을 통해 외부 API에 필요한 추가 데이터와 함께 유효한 JSON을 추가할 수 있습니다. 이 추가 데이터는 생성된 JSON의 params 개체에 추가됩니다.

### 아웃바운드 매핑

이 탭에서는 API 호출에서 반환되는 샘플 **JSON 구조**&#x200B;를 정의할 수 있습니다.

![](assets/externalAPI-outbound.png)

JSON 파서는 일부 예외를 제외하고 표준 JSON 구조 패턴 유형을 수용하도록 설계되었습니다. 표준 패턴의 예는 `{“data”:[{“key”:“value”}, {“key”:“value”},...]}`와(과) 같습니다.

샘플 JSON 정의에는 **다음 특성**&#x200B;이 있어야 합니다.

* **배열 요소**에는 첫 번째 수준 속성이 포함되어야 합니다(더 깊은 레벨은 지원되지 않음).
   **속성 이름**&#x200B;은 출력 임시 테이블의 출력 스키마에 대한 열 이름이 됩니다.
* 캡처할 **JSON 요소**&#x200B;는 JSON 응답 내에 10 이하의 중첩 수준이어야 합니다.
* **열 이름** 정의는 &quot;data&quot; 배열의 첫 번째 요소를 기반으로 합니다. 열 정의(추가/제거) 및 속성의 유형 값은 **열 정의** 탭에서 편집할 수 있습니다.

**평면화 확인란** 동작:

평면화 확인란(기본값: 선택 안 함)은 JSON을 키/값 맵으로 평면화할지 여부를 표시하기 위해 제공됩니다.

* **확인란을 비활성화**(선택 안 함)하면 샘플 JSON을 구문 분석하여 배열 개체를 찾습니다.  Adobe Campaign에서 사용자가 사용하려는 배열을 정확하게 파악할 수 있도록 트리밍된 버전의 API 응답 샘플 JSON 포맷을 제공해야 합니다. 워크플로우 작성 시, 중첩된 배열 개체의 경로가 결정 및 기록되므로 실행 시 API 호출에서 수신된 JSON 응답 본문에서 해당 배열 개체에 액세스하는 데 사용할 수 있습니다.

* **확인란을 활성화**(선택)하면 샘플 JSON이 평면화되고 제공된 샘플 JSON에 지정된 모든 속성이 출력 임시 테이블의 열을 만드는 데 사용되며 열 정의 탭에 표시됩니다. 샘플 JSON에 배열 개체가 있으면 해당 배열 개체의 모든 요소도 평면화됩니다.


**구문 분석의 유효성을 검사**&#x200B;하면 메시지가 나타나고 &quot;열 정의&quot; 탭에서 데이터 매핑을 사용자 지정할 수 있도록 초대합니다. 다른 경우에는 오류 메시지가 표시됩니다.

### 실행

이 탭에서는 연결 엔드포인트를 정의할 수 있습니다. 이 **[!UICONTROL URL]** 필드에서는 ACS로 데이터를 전송할 **HTTPS 엔드포인트**&#x200B;를 정의할 수 있습니다.

엔드포인트에 필요한 경우 두 가지 유형의 인증 방법을 사용할 수 있습니다.

* 기본 인증: 사용자 이름/암호 정보를 **[!UICONTROL Request Header(s)]** 필드에 입력합니다.

* OAuth 인증: **[!UICONTROL Use connection parameters defined in an external account]**&#x200B;을(를) 클릭하여 OAuth 인증이 정의된 외부 계정을 선택할 수 있습니다. 자세한 내용은 [외부 계정](../../administration/using/external-accounts.md) 섹션을 참조하십시오.

![](assets/externalAPI-execution.png)

### 속성

이 탭에서는 UI에 표시된 레이블과 같은 외부 API 활동에 대한 **일반 속성**&#x200B;을 제어할 수 있습니다. 내부 ID는 사용자 지정할 수 없습니다.

![](assets/externalAPI-properties.png)

### 열 정의

>[!NOTE]
>
>이 탭은 아웃바운드 매핑 탭에서 **응답 데이터 포맷**&#x200B;을 완성하고 검증한 경우에 나타납니다.

**열 정의** 탭에서는 오류가 없는 데이터를 가져오기 위해 각 열의 데이터 구조를 정확하게 지정하고 향후 작업을 위해 Adobe Campaign 데이터베이스에 이미 있는 유형과 일치시킬 수 있습니다.

![](assets/externalAPI-column.png)

예를 들어 열의 레이블을 변경하고 해당 유형(문자열, 정수, 날짜 등)을 선택할 수 있습니다.  오류 처리를 지정할 수도 있습니다.

자세한 내용은 [파일 로드](../../automating/using/load-file.md) 섹션을 참조하십시오.

### 전환

이 탭에서는 **아웃바운드 전환** 및 해당 레이블을 활성화할 수 있습니다. 이 특정 전환은 **시간 제한** 또는 페이로드가 **데이터 크기 제한**&#x200B;을 초과하는 경우에 유용합니다.

![](assets/externalAPI-transition.png)

### 실행 옵션

이 탭은 대부분의 워크플로우 활동에서 사용할 수 있습니다. 자세한 내용은 [활동 속성](../../automating/using/activity-properties.md) 섹션을 참조하십시오.

![](assets/externalAPI-options.png)

## 문제 해결

이 새로운 워크플로우 활동에 추가된 로그 메시지의 두 가지 유형은 정보 및 오류입니다. 이는 잠재적인 문제를 해결하는 데 도움이 될 수 있습니다.

### 정보

이러한 로그 메시지는 워크플로우 활동을 실행하는 동안 유용한 체크포인트에 대한 정보를 기록하는 데 사용됩니다.
<table> 
 <thead> 
  <tr> 
   <th> 메시지 포맷<br /> </th> 
   <th> 예제<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Invoking API URL '%s'.</td> 
   <td> <p>API URL 'https://example.com/api/v1/web-coupon?count=2'을(를) 호출하는 중입니다.</p></td> 
  </tr> 
  <tr> 
   <td> Retrying API URL '%s' due to %s in %d ms, attempt %d.</td> 
   <td> <p>2364 ms에 있는 HTTP - 401 때문에 API URL 'https://example.com/api/v1/web-coupon?count=0'을 재시도합니다. 시도 2.</p></td>
  </tr> 
  <tr> 
   <td> Transferring content from '%s' (%s / %s).</td> 
   <td> <p>'https://example.com/api/v1/web-coupon?count=2'(1234 / 1234)에서 콘텐츠를 전송하는 중입니다.</p></td> 
  </tr>
  <tr> 
   <td> Using cached access token for provider ID '%s'.</td> 
   <td> <p>공급자 ID 'EXT25'에 대해 캐시된 액세스 토큰을 사용하는 중입니다. 참고: EXT25는 외부 계정의 ID(또는 이름)입니다. </p></td> 
  </tr>
  <tr> 
   <td> Fetched access token from server for provider ID '%s'.</td> 
   <td> <p>공급자 ID 'EXT25'에 대한 액세스 토큰을 서버에서 가져왔습니다. 참고:EXT25는 외부 계정의 ID(또는 이름)입니다.</p></td> 
  </tr>
  <tr> 
   <td> Refreshing OAuth access token due to error (HTTP: '%d').</td> 
   <td> <p>오류로 인해 OAuth 액세스 토큰을 새로 고치는 중(HTTP: '401').</p></td> 
  </tr>
  <tr> 
   <td> Error refreshing OAuth access token (error: '%d'). </td> 
   <td> <p>OAuth 액세스 토큰을 새로 고치는 동안 오류가 발생했습니다(오류: '404').</p></td> 
  </tr>
  <tr> 
   <td> Failed to fetch the OAuth access token using the specified external account on attempt %d, retrying in %d ms.</td> 
   <td> <p>시도 1에서 지정된 외부 계정을 사용하여 OAuth 액세스 토큰을 가져오지 못했습니다. 1387 ms에서 다시 시도합니다.</p></td> 
  </tr>
 </tbody> 
</table>

### 오류

이러한 로그 메시지는 예기치 않은 오류 조건에 대한 정보를 기록하는 데 사용되며 이로 인해 워크플로우 활동이 실패할 수 있습니다.

<table> 
 <thead> 
  <tr> 
   <th> 코드 - 메시지 포맷<br /> </th> 
   <th> 예제<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> WKF-560250 - API request body exceeded limit (limit: '%d').</td> 
   <td> <p>API 요청 본문이 한도를 초과했습니다(한도: '5242880').</p></td> 
  </tr> 
  <tr> 
   <td> WKF-560239 -  API response exceeded limit (limit: '%d').</td> 
   <td> <p>API 응답이 한도를 초과했습니다(한도: 5242880').</p></td> 
  </tr> 
  <tr> 
   <td> WKF-560245 - API URL could not be parsed (error: '%d').</td> 
   <td> <p>API URL을 구문 분석할 수 없습니다(오류: '-2010').</p>
   <p> 참고: 이 오류는 API URL이 유효성 검사 규칙에 실패하면 기록됩니다.</p></td>
  </tr> 
  <tr>
   <td> WKF-560244 - API URL host must not be 'localhost', or IP address literal (URL host: '%s').</td> 
   <td> <p>API URL 호스트는 'localhost' 또는 IP 주소 리터럴(URL 호스트: 'localhost')이 아니어야 합니다.</p>
    <p>API URL 호스트는 'localhost' 또는 IP 주소 리터럴(URL 호스트: '192.168.0.5')이 아니어야 합니다.</p>
    <p>API URL 호스트는 'localhost' 또는 IP 주소 리터럴(URL 호스트: '[2001]')이 아니어야 합니다.</p></td>
  </tr> 
  <tr> 
   <td> WKF-560238 - API URL must be a secure URL (https) (requested URL: '%s').</td> 
   <td> <p>API URL은 보안 URL(https)이어야 합니다(요청된 URL: 'https://example.com/api/v1/web-coupon?count=2').</p></td> 
  </tr> 
  <tr> 
   <td> WKF-560249 - 요청 본문 JSON을 만들지 못했습니다. Error when adding '%s'.</td> 
   <td> <p>요청 본문 JSON을 만들지 못했습니다. 'params'를 추가하는 동안 오류가 발생했습니다.</p>
    <p>요청 본문 JSON을 만들지 못했습니다. 'data'를 추가하는 동안 오류가 발생했습니다.</p></td>
  </tr> 
  <tr> 
   <td> WKF-560246 - HTTP header key is bad (header key: '%s').</td> 
   <td> <p>HTTP header key is bad (header key: '%s').</p>
   <p> 참고: 이 오류는 <a href="https://tools.ietf.org/html/rfc7230#section-3.2.html">RFC</a>에 따라 사용자 지정 헤더 키의 유효성 검사에 실패하면 기록됩니다.</p></td> 
  </tr>
 <tr> 
   <td> WKF-560248 - HTTP header key is not allowed (header key: '%s').</td> 
   <td> <p>HTTP 헤더 키가 허용되지 않습니다(헤더 키: 'Accept').</p></td> 
  </tr> 
  <tr> 
   <td> WKF-560247 -  A HTTP header value is bad (header value: '%s').</td> 
   <td> <p>HTTP header value is bad (header value: '%s'). </p>
    <p>참고: 이 오류는 <a href="https://tools.ietf.org/html/rfc7230#section-3.2.html">RFC</a>에 따라 사용자 지정 헤더 값의 유효성 검사에 실패하면 기록됩니다.</p></td> 
  </tr> 
  <tr> 
   <td> WKF-560240 - JSON payload has bad property '%s'.</td> 
   <td> <p>JSON 페이로드에 잘못된 속성 'blah'가 있습니다.</p></td>
  </tr> 
  <tr>
   <td> WKF-560241 - Malformed JSON or unacceptable format.</td> 
   <td> <p>잘못된 포맷의 JSON 또는 허용되지 않는 포맷입니다.</p>
   <p>참고: 이 메시지는 외부 API의 응답 본문을 구문 분석하는 경우에만 적용되며, 응답 본문이 이 활동에서 지정한 JSON 포맷을 준수하는지 여부를 유효성 검사하려고 할 때 기록됩니다.</p></td>
  </tr>
  <tr> 
   <td> WKF-560246 - Activity failed (reason: '%s').</td> 
   <td> <p>HTTP 401 오류 응답으로 인해 활동이 실패하는 경우 - 활동이 실패했습니다(이유: 'HTTP - 401').</p>
        <p>내부 호출 실패로 인해 활동이 실패하는 경우 - 활동이 실패했습니다(이유: 'Rc - -N').</p>
        <p>잘못된 Content-Type 헤더로 인해 활동이 실패하는 경우 - 활동이 실패했습니다(이유: 'Content-Type - application/html').</p></td> 
  </tr>
  <tr> 
   <td> WKF-560278 - "Error initializing OAuth helper (error: '%d')" .</td> 
   <td> <p>이 오류는 외부 계정에 구성된 특성을 사용하여 도우미를 초기화하는 동안 오류가 발생하여 활동이 내부 OAuth2.0 도우미 기능을 초기화할 수 없음을 나타냅니다.</p></td>
  </tr>
  <tr> 
   <td> WKF-560279 - "HTTP header key is not allowed (header key: '%s')."</td> 
   <td> <p>이 경고(오류 아님) 메시지는 OAuth 2.0 외부 계정이 HTTP 헤더로 자격 증명을 추가하도록 구성되었지만, 사용되는 헤더 키는 예약된 헤더 키이므로 허용되지 않음을 나타냅니다.</p></td>
  </tr>
  <tr> 
   <td> WKF-560280 - External account of '%s' ID cannot be found.</td> 
   <td> <p>'EXT25' ID의 외부 계정을 찾을 수 없습니다.  참고: 이 오류는 더 이상 찾을 수 없는 외부 계정을 사용하도록 활동이 구성되어 있음을 나타냅니다. 이는 DB에서 계정이 삭제되었을 때 발생할 수 있으며 정상적인 운영 환경에서는 이러한 일이 발생하지 않을 가능성이 높습니다.</p></td>
  </tr>
  <tr> 
   <td> WKF-560281 - External account of '%s' ID is disabled.</td> 
   <td> <p>'EXT25' ID의 외부 계정을 사용할 수 없습니다. 참고: 이 오류는 활동이 외부 계정을 사용하도록 구성되었지만 해당 계정이 비활성화되어 있거나 비활성 상태로 표시되었음을 나타냅니다.</p></td>
  </tr>
  <tr> 
   <td> WKF-560282 - Protocol not supported.</td> 
   <td> <p>이 오류는 활동과 연결된 외부 계정이 OAuth2.0 외부 계정이 아님을 나타냅니다. 따라서 활동 구성에 일부 손상 또는 수동 변경 사항이 없으면 이 오류가 발생하지 않습니다.</p></td>
  </tr>
  <tr> 
   <td> WKF-560283 - Failed to fetch the OAuth access token.</td> 
   <td> <p>이 오류의 가장 일반적인 원인은 외부 계정의 잘못된 구성입니다(예: 연결 성공 여부를 테스트하지 않고 외부 계정 사용). 외부 계정의 URL/자격 증명이 변경될 수 있습니다.</p></td>
  </tr>
  <tr> 
   <td> CRL-290199 - Cannot reach page at: %s.</td> 
   <td> <p>이 오류 메시지는 OAuth에 대해 설정할 때 외부 계정 UI 화면에 표시됩니다. 즉, 외부 인증 서버의 URL이 부정확하거나, 변경되었거나, 페이지 찾을 수 없음이라는 서버의 응답을 받았다는 뜻입니다.</p></td>
  </tr>
  <tr> 
   <td> CRL-290200 - Incomplete/Incorrect credentials.</td> 
   <td> <p>이 오류 메시지는 OAuth에 대해 설정할 때 외부 계정 UI 화면에 표시됩니다. 즉, 인증 서버에 연결하기 위해 필요한 자격 증명이 잘못되었거나 누락되었다는 의미입니다.
</p></td>
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
