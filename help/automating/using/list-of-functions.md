---
solution: Campaign Standard
product: campaign
title: 함수 목록
description: 쿼리 편집 도구를 사용하면 고급 함수를 사용하여 복잡한 필터링을 수행할 수 있습니다.
audience: automating
content-type: reference
topic-tags: filtering-data
translation-type: tm+mt
source-git-commit: ef170f2282fcc46e36c90dada2083dea25b95f7c
workflow-type: tm+mt
source-wordcount: '1940'
ht-degree: 98%

---


# 함수 목록{#list-of-functions}

## 함수 기본 정보 {#about-functions}

쿼리 편집 도구를 사용하면 고급 함수를 사용하여 복잡한 필터링을 수행할 수 있습니다. 이를 위해 도구 팔레트에는 작업 영역에서 사용할 수 있는 **[!UICONTROL Expression]** 요소가 포함되어 있습니다. 이 요소에 대한 자세한 내용은 [특정 섹션](../../automating/using/advanced-expression-editing.md)에 자세히 설명되어 있습니다.

이 요소를 사용하면 조건을 수동으로 입력할 수 있습니다. 여기에서 다음 섹션에 정의된 함수를 사용할 수 있습니다.

원하는 결과 및 조작된 데이터의 유형에 따라 다양한 함수 유형을 사용할 수 있습니다.

* 날짜
* 지오마케팅
* 숫자 값
* 기타 함수
* 집계
* 문자열 조작
* 정렬

>[!NOTE]
>
>외부 매개 변수를 사용한 워크플로우를 호출한 후 이벤트 변수를 사용할 수 있도록 해주는 모든 활동에서 추가 함수를 사용할 수 있습니다. 이 내용은 [이 섹션](../../automating/using/customizing-workflow-external-parameters.md)에 자세히 설명되어 있습니다.

## 날짜 {#dates}

날짜 함수는 날짜 또는 시간 값을 조작하는 데 사용됩니다.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>이름</strong><br /> </td> 
   <td> <strong>설명</strong><br /> </td> 
   <td> <strong>구문</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AddDays</strong><br /> </td> 
   <td> 날짜에 일자 숫자 추가<br /> </td> 
   <td> AddDays(&lt;날짜&gt;, &lt;숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AddHours</strong><br /> </td> 
   <td> 날짜에 시간(시) 숫자 추가<br /> </td> 
   <td> AddHours(&lt;날짜&gt;, &lt;숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AddMinutes</strong><br /> </td> 
   <td> 날짜에 시간(분) 숫자 추가<br /> </td> 
   <td> AddMinutes(&lt;날짜&gt;, &lt;숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AddMonths</strong><br /> </td> 
   <td> 날짜에 개월 숫자 추가<br /> </td> 
   <td> AddMonths(&lt;날짜&gt;, &lt;숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AddSeconds</strong><br /> </td> 
   <td> 날짜에 시간(초) 숫자 추가<br /> </td> 
   <td> AddSeconds(&lt;날짜&gt;, &lt;숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AddYears</strong><br /> </td> 
   <td> 날짜에 연도 숫자 추가<br /> </td> 
   <td> AddYears(&lt;날짜&gt;, &lt;숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>DateOnly</strong><br /> </td> 
   <td> 날짜만 반환(00:00 시간 포함)<br /> </td> 
   <td> DateOnly(&lt;날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Day</strong><br /> </td> 
   <td> 날짜의 일자를 나타내는 숫자 반환<br /> </td> 
   <td> Day(&lt;날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>DayOfYear</strong><br /> </td> 
   <td> 날짜의 연도를 나타내는 숫자 반환<br /> </td> 
   <td> DayOfYear(&lt;날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>DaysAgo</strong><br /> </td> 
   <td> 현재 날짜에서 n일을 뺀 숫자 반환<br /> </td> 
   <td> DaysAgo(&lt;숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>DaysAgoInt</strong><br /> </td> 
   <td> 현재 날짜에서 n일을 뺀 숫자 반환(정수 yyyymmdd)<br /> </td> 
   <td> DaysAgoInt(&lt;숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>DaysDiff</strong><br /> </td> 
   <td> 두 날짜 사이의 일자 수<br /> </td> 
   <td> DaysDiff(&lt;종료 날짜&gt;, &lt;시작 날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>DaysOld</strong><br /> </td> 
   <td> 날짜를 일 단위로 반환<br /> </td> 
   <td> DaysOld(&lt;날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>GetDate</strong><br /> </td> 
   <td> 서버의 현재 시스템 날짜 반환<br /> </td> 
   <td> GetDate()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Hour</strong><br /> </td> 
   <td> 날짜의 시간 반환<br /> </td> 
   <td> Hour(&lt;날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>HoursDiff</strong><br /> </td> 
   <td> 두 날짜 사이의 시간(시) 숫자 반환<br /> </td> 
   <td> HoursDiff(&lt;종료 날짜&gt;, &lt;시작 날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>LocalToUTC</strong><br /> </td> 
   <td> 로컬 날짜 및 시간을 UTC로 변환<br /> </td> 
   <td> LocalToUTC(&lt;날짜&gt;, &lt;시간대&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Minute</strong><br /> </td> 
   <td> 날짜의 시간(분) 반환<br /> </td> 
   <td> Minute(&lt;날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>MinutesDiff</strong><br /> </td> 
   <td> 두 날짜 사이의 시간(분) 숫자 반환<br /> </td> 
   <td> MinutesDiff(&lt;종료 날짜&gt;, &lt;시작 날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Month</strong><br /> </td> 
   <td> 날짜의 월을 나타내는 숫자 반환<br /> </td> 
   <td> Month(&lt;날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>MonthsAgo</strong><br /> </td> 
   <td> 현재 날짜에서 n개월을 뺀 날짜 반환<br /> </td> 
   <td> MonthsAgo(&lt;숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>MonthsDiff</strong><br /> </td> 
   <td> 두 날짜 사이의 개월 숫자 반환<br /> </td> 
   <td> MonthsDiff(&lt;종료 날짜&gt;, &lt;시작 날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>MonthsOld</strong><br /> </td> 
   <td> 날짜를 월 단위로 반환<br /> </td> 
   <td> MonthsOld(&lt;날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Second</strong><br /> </td> 
   <td> 날짜의 시간(초) 반환<br /> </td> 
   <td> Second(&lt;날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Oldest</strong><br /> </td> 
   <td> 가장 오래된 날짜 반환 </td> 
   <td> Oldest(&lt;날짜&gt;, &lt;날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>SecondsDiff</strong><br /> </td> 
   <td> 두 날짜 사이의 시간(초) 숫자 반환<br /> </td> 
   <td> SecondsDiff(&lt;종료 날짜&gt;, &lt;시작 날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>SubDays</strong><br /> </td> 
   <td> 날짜에서 일자 숫자 빼기<br /> </td> 
   <td> SubDays(&lt;날짜&gt;, &lt;숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>SubHours</strong><br /> </td> 
   <td> 날짜에서 시간(시) 숫자 빼기<br /> </td> 
   <td> SubHours(&lt;날짜&gt;, &lt;숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>SubMinutes</strong><br /> </td> 
   <td> 날짜에서 시간(분) 숫자 빼기<br /> </td> 
   <td> SubMinutes(&lt;날짜&gt;, &lt;숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>SubMonths</strong><br /> </td> 
   <td> 날짜에서 개월 숫자 빼기<br /> </td> 
   <td> SubMonths(&lt;날짜&gt;, &lt;숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>SubSeconds</strong><br /> </td> 
   <td> 날짜에서 시간(초) 숫자 빼기<br /> </td> 
   <td> SubSeconds(&lt;날짜&gt;, &lt;숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>SubYears</strong><br /> </td> 
   <td> 날짜에서 연도 숫자 빼기<br /> </td> 
   <td> SubYears(&lt;날짜&gt;, &lt;숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ToDate</strong><br /> </td> 
   <td> 날짜 + 시간을 날짜로 변환<br /> </td> 
   <td> ToDate(&lt;날짜 + 시간&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ToDateTime</strong><br /> </td> 
   <td> 문자열을 날짜 + 시간으로 변환<br /> </td> 
   <td> ToDateTime(&lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ToDateTimeWithTimezone</strong><br /> </td> 
   <td> 문자열을 날짜 + 시간대로 변환.<br /> 예제: ToDateTimeWithTimezone("2019-02-19 08:09:00", "아시아/테헤란")<br /> </td> 
   <td> ToDateTimeWithTimezone(&lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>TruncDate</strong><br /> </td> 
   <td> 날짜+시간을 가장 가까운 시간(초)으로 반올림<br /> </td> 
   <td> TruncDate(@lastModified, &lt;시간(초) 숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>TruncDateTZ</strong><br /> </td> 
   <td> 날짜 + 시간을 초 단위의 특정 정밀도로 반올림<br /> </td> 
   <td> TruncDateTZ(&lt;날짜&gt;, &lt;시간(초) 숫자&gt;, &lt;시간대&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>TruncQuarter</strong><br /> </td> 
   <td> 날짜를 분기로 반올림<br /> </td> 
   <td> TruncQuarter(&lt;날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>TruncTime</strong><br /> </td> 
   <td> 시간 부분을 가장 가까운 시간(초)으로 반올림<br /> </td> 
   <td> TruncTime(&lt;날짜&gt;, &lt;시간(초) 숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>TruncWeek</strong><br /> </td> 
   <td> 날짜를 요일로 반올림<br /> </td> 
   <td> TruncWeek(&lt;날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>TruncYear</strong><br /> </td> 
   <td> 날짜 + 시간을 연도의 1월 1일로 반올림<br /> </td> 
   <td> TruncYear(&lt;날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>WeekDay</strong><br /> </td> 
   <td> 날짜의 요일을 나타내는 숫자 반환<br /> </td> 
   <td> WeekDay(&lt;날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Year</strong><br /> </td> 
   <td> 날짜의 연도를 나타내는 숫자 반환<br /> </td> 
   <td> Year(&lt;날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>YearAnd Month</strong><br /> </td> 
   <td> 날짜의 연도 및 월을 나타내는 숫자 반환<br /> </td> 
   <td> YearAndMonth(&lt;날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>YearsDiff</strong><br /> </td> 
   <td> 두 날짜 사이의 연도 숫자 반환<br /> </td> 
   <td> YearsDiff(&lt;종료 날짜&gt;, &lt;시작 날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>YearsOld</strong><br /> </td> 
   <td> 날짜를 연 단위로 반환<br /> </td> 
   <td> YearsOld(&lt;날짜&gt;)<br /> </td> 
  </tr> 
 </tbody> 
</table>

## 지오마케팅 {#geomarketing}

지오마케팅 함수는 지리적 값을 조작하는 데 사용됩니다.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>이름</strong><br /> </td> 
   <td> <strong>설명</strong><br /> </td> 
   <td> <strong>구문</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Distance</strong><br /> </td> 
   <td> 경도 및 위도로 정의된 두 지점 사이의 거리(도 단위)를 킬로미터 단위로 반환<br /> </td> 
   <td> Distance(&lt;경도 A&gt;, &lt;위도 A&gt;, &lt;경도 B&gt;, &lt;위도 B&gt;)<br /> </td> 
  </tr> 
 </tbody> 
</table>

## 숫자 {#numerical}

숫자 값 함수는 텍스트를 숫자로 변환하는 데 사용됩니다.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>이름</strong><br /> </td> 
   <td> <strong>설명</strong><br /> </td> 
   <td> <strong>구문</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Abs</strong><br /> </td> 
   <td> 숫자의 절대값 반환<br /> </td> 
   <td> Abs(&lt;숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Ceil</strong><br /> </td> 
   <td> 숫자보다 크거나 같은 최소 정수 반환<br /> </td> 
   <td> Ceil(&lt;숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Floor</strong><br /> </td> 
   <td> 숫자보다 작거나 같은 최대 정수 반환<br /> </td> 
   <td> Floor(&lt;숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Greatest</strong><br /> </td> 
   <td> 두 숫자 중 큰 숫자 반환<br /> </td> 
   <td> Greatest(&lt;숫자 1&gt;, &lt;숫자 2&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Least</strong><br /> </td> 
   <td> 두 숫자 중 작은 숫자 반환<br /> </td> 
   <td> Least(&lt;숫자 1&gt;, &lt;숫자 2&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Mod</strong><br /> </td> 
   <td> n1에서 n2까지 정수 분기의 나머지 반환<br /> </td> 
   <td> Mod(&lt;숫자 1&gt;, &lt;숫자 2&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Percent</strong><br /> </td> 
   <td> 백분율로 표현된 두 수의 비율 반환<br /> </td> 
   <td> Percent(&lt;숫자 1&gt;, &lt;숫자 2&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Random</strong><br /> </td> 
   <td> 임의 값 반환<br /> </td> 
   <td> Random()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Round</strong><br /> </td> 
   <td> 숫자를 n개의 소수로 반올림<br /> </td> 
   <td> Round(&lt;숫자&gt;, &lt;소수 자리수&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sign</strong><br /> </td> 
   <td> 숫자 기호 반환<br /> </td> 
   <td> Sign(&lt;숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ToDouble</strong><br /> </td> 
   <td> 정수를 실수로 변환<br /> </td> 
   <td> ToDouble(&lt;숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ToInt64</strong><br /> </td> 
   <td> 실수를 64비트 정수로 변환<br /> </td> 
   <td> ToInt64(&lt;숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ToInteger</strong><br /> </td> 
   <td> 실수를 정수로 변환<br /> </td> 
   <td> ToInteger(&lt;숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Trunc</strong><br /> </td> 
   <td> n1에서 n2까지의 소수점 자르기<br /> </td> 
   <td> Trunc(&lt;n1&gt;, &lt;n2&gt;)<br /> </td> 
  </tr> 
 </tbody> 
</table>

## 기타 {#others}

이 표에는 사용 가능한 나머지 함수가 포함되어 있습니다.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>이름</strong><br /> </td> 
   <td> <strong>설명</strong><br /> </td> 
   <td> <strong>구문</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Case</strong><br /> </td> 
   <td> 조건이 확인되면 값 1 반환 그렇지 않으면 값 2 반환<br /> </td> 
   <td> Case(When(&lt;조건&gt;, &lt;값 1&gt;), Else(&lt;값 2&gt;))<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ClearBit</strong><br /> </td> 
   <td> 값에서 플래그 삭제<br /> </td> 
   <td> ClearBit(&lt;식별자&gt;, &lt;플래그&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Coalesce</strong><br /> </td> 
   <td> 값 1이 0이거나 null이면 값 2 반환, 그렇지 않으면 값 1 반환<br /> </td> 
   <td> Coalesce(&lt;값 1&gt;, &lt;값 2&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Decode</strong><br /> </td> 
   <td> 반환 값 3은 값 1 = 값 2이고, 그렇지 않으면 4 반환<br /> </td> 
   <td> Decode(&lt;값 1&gt;, &lt;값 2&gt;, &lt;값 3&gt;, &lt;값 4&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Else</strong><br /> </td> 
   <td> 값 1 반환(case 함수의 매개 변수로만 사용할 수 있음)<br /> </td> 
   <td> Else(&lt;값 1&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>GetEmailDomain</strong><br /> </td> 
   <td> 이메일 주소에서 도메인 추출<br /> </td> 
   <td> GetEmailDomain(&lt;값&gt;)<br /> </td> 
  </tr>
  <tr> 
   <td> <strong>GetMirrorURL</strong><br /> </td> 
   <td> 미러 페이지 서버의 URL 검색<br /> </td> 
   <td> GetMirrorURL(&lt;값&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Iif</strong><br /> </td> 
   <td> 표현식이 true면 값 1 반환, 그렇지 않으면 값 2 반환<br /> </td> 
   <td> Iif(&lt;조건&gt;, &lt;값 1&gt;, &lt;값 2&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>IsBitSet</strong><br /> </td> 
   <td> 플래그가 값에 있는지 표시<br /> </td> 
   <td> IsBitSet(&lt;식별자&gt;, &lt;플래그&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>IsEmptyString</strong><br /> </td> 
   <td> 문자열이 비어 있으면 값 2 반환, 그렇지 않으면 값 3 반환<br /> </td> 
   <td> IsEmptyString(&lt;문자열&gt;, &lt;값 2&gt;, &lt;값 3&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>NoNull</strong><br /> </td> 
   <td> 인수가 NULL이면 빈 문자열 반환<br /> </td> 
   <td> NoNull(&lt;값&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>RowId</strong><br /> </td> 
   <td> 행 번호 반환<br /> </td> 
   <td> RowId<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>SetBit</strong><br /> </td> 
   <td> 값에 플래그 강제 적용<br /> </td> 
   <td> SetBit(&lt;식별자&gt;, &lt;플래그&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ToBoolean</strong><br /> </td> 
   <td> 숫자를 부울로 변환<br /> </td> 
   <td> ToBoolean(&lt;숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>When</strong><br /> </td> 
   <td> 표현식이 확인되면 값 1 반환 그렇지 않으면 값 2 반환(case 함수의 매개 변수로만 사용할 수 있음)<br /> </td> 
   <td> When(&lt;조건&gt;, &lt;값 1&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>newUUID</strong><br /> </td> 
   <td> 새 UUID 반환<br /> </td> 
   <td> newUUID<br /> </td> 
  </tr> 
 </tbody> 
</table>

## 문자열 {#string}

문자열 함수는 문자열 집합을 조작하는 데 사용됩니다.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>이름</strong><br /> </td> 
   <td> <strong>설명</strong><br /> </td> 
   <td> <strong>구문</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AllNonNull2</strong><br /> </td> 
   <td> 모든 매개 변수가 null이 아니고 비어 있지 않은지 표시<br /> </td> 
   <td> AllNonNull2(&lt;문자열&gt;, &lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AllNonNull3</strong><br /> </td> 
   <td> 모든 매개 변수가 null이 아니고 비어 있지 않은지 표시<br /> </td> 
   <td> AllNonNull3(&lt;문자열&gt;, &lt;문자열&gt;, &lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ASCII</strong><br /> </td> 
   <td> 문자열에서 첫 번째 문자의 ASCII 값 반환<br /> </td> 
   <td> Ascii(&lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Char</strong><br /> </td> 
   <td> 'n' ASCII 코드에 해당하는 문자 반환<br /> </td> 
   <td> Char(&lt;숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Charindex</strong><br /> </td> 
   <td> 문자열 1에서 문자열 2의 위치 반환<br /> </td> 
   <td> Charindex(&lt;문자열&gt;, &lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>DataLength</strong><br /> </td> 
   <td> 문자열의 문자 수 반환<br /> </td> 
   <td> DataLength(&lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>GetLine</strong><br /> </td> 
   <td> 문자열의 n번째(1에서 n까지) 행 반환<br /> </td> 
   <td> GetLine(&lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>IfEquals</strong><br /> </td> 
   <td> 처음 두 매개 변수가 동일하면 세 번째 매개 변수 반환, 그렇지 않으면 마지막 매개 변수 반환<br /> </td> 
   <td> IfEquals(&lt;문자열&gt;, &lt;문자열&gt;, &lt;문자열&gt;, &lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>IsMemoNull</strong><br /> </td> 
   <td> 매개 변수로 전달된 메모가 null인지 표시<br /> </td> 
   <td> IsMemoNull(&lt;메모&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>JuxtWords</strong><br /> </td> 
   <td> 매개 변수로 전달된 두 개의 문자열 연결. 반환된 값의 각 문자열 사이에 공백이 추가됩니다.<br /> </td> 
   <td> JuxtWords(&lt;문자열&gt;, &lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>JuxtWords3</strong><br /> </td> 
   <td> 매개 변수로 전달된 세 개의 문자열 연결. 반환된 값의 각 문자열 사이에 공백이 추가됩니다.<br /> </td> 
   <td> JuxtWords3(&lt;문자열&gt;, &lt;문자열&gt;, &lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>LPad</strong><br /> </td> 
   <td> 왼쪽에서 완성된 문자열 반환<br /> </td> 
   <td> LPad(&lt;문자열&gt;, &lt;숫자&gt;, &lt;문자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Left</strong><br /> </td> 
   <td> 문자열의 처음 n자 반환<br /> </td> 
   <td> Left(&lt;문자열&gt;, &lt;숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Length</strong><br /> </td> 
   <td> 문자열 길이 반환<br /> </td> 
   <td> Length(&lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Lower</strong><br /> </td> 
   <td> 문자열을 소문자로 반환<br /> </td> 
   <td> Lower(&lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Ltrim</strong><br /> </td> 
   <td> 문자열 왼쪽의 공백 제거<br /> </td> 
   <td> Ltrim(&lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Md5Digest</strong><br /> </td> 
   <td> 문자열의 MD5 키를 16진수로 반환<br /> </td> 
   <td> Md5Digest(&lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>MemoContains</strong><br /> </td> 
   <td> 메모에 매개 변수로 전달된 문자열이 포함되어 있는지 지정<br /> </td> 
   <td> MemoContains(&lt;메모&gt;, &lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>RPad</strong><br /> </td> 
   <td> 오른쪽에 완성된 문자열 반환<br /> </td> 
   <td> RPad(&lt;문자열&gt;, &lt;숫자&gt;, &lt;문자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Replace</strong><br /> </td> 
   <td> 지정된 문자열(2번째 매개 변수) 값의 모든 발생 항목을 문자열(1번째 매개 변수)의 다른 문자열 값(3번째 매개 변수)으로 변환<br /> </td> 
   <td> Replace(&lt;문자열&gt;, &lt;문자열&gt;, &lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Right</strong><br /> </td> 
   <td> 문자열의 마지막 n자 반환<br /> </td> 
   <td> Right(&lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Rtrim</strong><br /> </td> 
   <td> 문자열 오른쪽의 공백 제거<br /> </td> 
   <td> Rtrim(&lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha256Digest</strong><br /> </td> 
   <td> 지정된 UTF8 문자열에 대한 표준 <strong>SHA256</strong> 해시 계산<br /> </td> 
   <td> Sha256Digest(&lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha384Digest</strong><br /> </td> 
   <td> 지정된 UTF8 문자열에 대한 표준 <strong>SHA384</strong> 해시 계산<br /> </td> 
   <td> Sha384Digest(&lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha512Digest</strong><br /> </td> 
   <td> 지정된 UTF8 문자열에 대한 표준 <strong>SHA512</strong> 해시 계산<br /> </td> 
   <td> Sha512Digest(&lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Smart</strong><br /> </td> 
   <td> 각 단어의 첫 번째 문자가 대문자로 표시된 문자열 반환<br /> </td> 
   <td> Smart(&lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Substring</strong><br /> </td> 
   <td> 문자열의 문자 n1에서 시작하여 길이가 n2인 하위 문자열 추출<br /> </td> 
   <td> Substring(&lt;문자열&gt;, &lt;오프셋&gt;, &lt;길이&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ToIntlString</strong><br /> </td> 
   <td> 숫자를 문자열로 변환<br /> </td> 
   <td> ToIntlString(&lt;숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ToString</strong><br /> </td> 
   <td> 숫자를 문자열로 변환<br /> </td> 
   <td> ToString(&lt;숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Upper</strong><br /> </td> 
   <td> 문자열을 대문자로 반환<br /> </td> 
   <td> Upper(&lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>VirtualLink</strong><br /> </td> 
   <td> 다른 두 매개 변수가 동일한 경우 매개 변수로 전달된 링크의 외부 키 반환<br /> </td> 
   <td> VirtualLink(&lt;숫자&gt;, &lt;&lt;숫자&gt;, &lt;숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>VirtualLinkStr</strong><br /> </td> 
   <td> 다른 두 매개 변수가 동일한 경우 매개 변수로 전달된 링크의 외부(텍스트) 키 반환<br /> </td> 
   <td> VirtualLinkStr(&lt;문자열&gt;, &lt;숫자&gt;, &lt;숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>encryption_aescbcDecrypt</strong><br /> </td> 
   <td> HEX 포맷(2번째 매개 변수)의 키 및 HEX 포맷(3번째 매개 변수)의 초기화 벡터를 사용하여 "<strong>x</strong>" 접두사가 있는 HEX 포맷(1번째 매개 변수)의 암호화된 값 해독<br /> </td> 
   <td> encryption_aescbcDecrypt(&lt;문자열&gt;, &lt;문자열&gt;, &lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>encryption_aescbcEncrypt</strong><br /> </td> 
   <td> AES 알고리즘(CBC 블록 모드)을 사용하여 키(2번째 매개 변수)와 초기화 벡터(3번째 매개 변수)가 있는 문자열(1번째 매개 변수) 암호화. 키 및 초기화 벡터는 (<strong>\x</strong>로 시작하는) 16진수로 제공되어야 합니다. 결과는 <strong>\x</strong>없이 16진수로 표시됩니다.<br /> 키 크기는 128비트, 192비트, 256비트(16, 24, 32개의 16진수 문자)가 될 수 있지만 키와 동일한 길이의 임의 IV 및 256비트를 사용하는 것이 좋습니다.<br /> </td> 
   <td> encryption_aescbcEncrypt(&lt;문자열&gt;, &lt;문자열&gt;, &lt;문자열&gt;)<br /> 예: encryption_aescbcEncrypt(johndoe@example.com, "<strong>\x0123456789ABCDEF0123456789ABCDEF</strong>", "<strong>\x0123456789ABCDEFFEDCBA9876543210</strong>")<br /> </td> 
  </tr> 
 </tbody> 
</table>

## 집계 {#aggregates}

집계 함수는 워크플로우 **[!UICONTROL Query]** 활동에서 [추가 데이터를 추가](../../automating/using/query.md#enriching-data)할 때만 사용할 수 있습니다.

집계 함수는 값 집합에 대한 계산을 수행하는 데 사용됩니다.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>이름</strong><br /> </td> 
   <td> <strong>설명</strong><br /> </td> 
   <td> <strong>구문</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Avg</strong>, 평균<br /> </td> 
   <td> 숫자 열의 평균 반환.<br /> </td> 
   <td> Avg(&lt;값&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Count</strong>, 계산(NULL 제외)<br /> </td> 
   <td> 열에서 null이 아닌 값 계산.<br /> </td> 
   <td> Count(&lt;값&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>CountAll</strong>, 모두 계산<br /> </td> 
   <td> 모든 값 계산(null 값 및 중복 포함).<br /> </td> 
   <td> CountAll()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Countdistinct</strong>, 개별 계산t<br /> </td> 
   <td> 열에서 null이 아닌 개별 값 계산<br /> </td> 
   <td> Countdistinct(&lt;값&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Max</strong>, 최대<br /> </td> 
   <td> 숫자, 문자열 또는 날짜 열의 최대값 반환<br /> </td> 
   <td> Max(&lt;값&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Min</strong>, 최소<br /> </td> 
   <td> 숫자, 문자열 또는 날짜 열의 최소값 반환<br /> </td> 
   <td> Min(&lt;값&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sum</strong>, 합계<br /> </td> 
   <td> 숫자 열에 있는 값의 합계 반환<br /> </td> 
   <td> Sum(&lt;값&gt;)<br /> </td> 
  </tr> 
 </tbody> 
</table>

## 표시 {#representation}

표시 함수는 값을 정렬하는 데 사용됩니다.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>이름</strong><br /> </td> 
   <td> <strong>설명</strong><br /> </td> 
   <td> <strong>구문</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Desc</strong><br /> </td> 
   <td> 내림차순 정렬 적용<br /> </td> 
   <td> Desc(&lt;값 1&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>OrderBy</strong><br /> </td> 
   <td> 파티션 내의 결과 정렬<br /> </td> 
   <td> OrderBy(&lt;값 1&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>PartitionBy</strong><br /> </td> 
   <td> 테이블에서 쿼리 결과 분할<br /> </td> 
   <td> PartitionBy(&lt;값 1&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>RowNum</strong><br /> </td> 
   <td> 테이블 파티션 및 정렬 시퀀스에 따라 행 번호 생성. 이 함수는 MySQL에서 지원되지 않습니다.<br /> </td> 
   <td> RowNum(PartitionBy(&lt;값 1&gt;), OrderBy(&lt;값 1&gt;))<br /> </td> 
  </tr> 
 </tbody> 
</table>

