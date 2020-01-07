---
title: 함수 목록
description: 쿼리 편집 도구를 사용하면 고급 기능을 사용하여 복잡한 필터링을 수행할 수 있습니다.
page-status-flag: never-activated
uuid: fd50fc99-1e7a-479b-beb7-1f246b419d46
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: filtering-data
discoiquuid: 3cdbe962-1c59-4cd8-b29e-36aa2562fac6
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: fa9d2be71b4bbf5eceadbd1835db324618f9529c

---


# 함수 목록{#list-of-functions}

## 함수 정보 {#about-functions}

쿼리 편집 도구를 사용하면 고급 기능을 사용하여 복잡한 필터링을 수행할 수 있습니다. 이를 위해 도구 팔레트에는 작업 공간에서 사용할 수 있는 **[!UICONTROL Expression]**요소가 포함되어 있습니다. 이 요소에 대한 자세한 내용은[특정 섹션에](../../automating/using/advanced-expression-editing.md)설명되어 있습니다.

이 요소를 사용하면 조건을 수동으로 입력할 수 있습니다. 여기에서 다음 섹션에 정의된 함수를 사용할 수 있습니다.

원하는 결과와 조작된 데이터 유형에 따라 여러 가지 함수 유형을 사용할 수 있습니다.

* 날짜
* Geomarketing
* 숫자 값
* 기타 함수
* 집계
* 문자열 조작
* 정렬

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
   <td> 날짜에 일 수 추가<br /> </td> 
   <td> AddDays(&lt;date&gt;, &lt;number&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>시간 추가</strong><br /> </td> 
   <td> 날짜에 시간 추가<br /> </td> 
   <td> AddHours(&lt;date&gt;, &lt;number&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AddMinutes</strong><br /> </td> 
   <td> 날짜에 시간(분) 추가<br /> </td> 
   <td> AddMinutes(&lt;date&gt;, &lt;number&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>월 추가</strong><br /> </td> 
   <td> 날짜에 월 수 추가<br /> </td> 
   <td> AddMonths(&lt;date&gt;, &lt;number&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AddSeconds</strong><br /> </td> 
   <td> 날짜에 시간(초) 추가<br /> </td> 
   <td> AddSeconds(&lt;date&gt;, &lt;number&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AddYears</strong><br /> </td> 
   <td> 날짜에 연도 추가<br /> </td> 
   <td> AddYears(&lt;date&gt;, &lt;number&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>DateOnly</strong><br /> </td> 
   <td> 날짜만 반환(시간 00:00)<br /> </td> 
   <td> DateOnly(&lt;date&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>일</strong><br /> </td> 
   <td> 날짜의 날짜를 나타내는 숫자를 반환합니다.<br /> </td> 
   <td> 일(&lt;날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>일/년</strong><br /> </td> 
   <td> 날짜의 연도의 일을 나타내는 숫자를 반환합니다.<br /> </td> 
   <td> DayOfYear(&lt;date&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>DaysAgo</strong><br /> </td> 
   <td> 현재 날짜 빼기 n일 값을 반환합니다.<br /> </td> 
   <td> DaysAgo(&lt;number&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>DaysAgoInt</strong><br /> </td> 
   <td> 현재 날짜 빼기 n일(정수 yyymmdd)을 반환합니다.<br /> </td> 
   <td> DaysAgoInt(&lt;number&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>DaysDiff</strong><br /> </td> 
   <td> 두 날짜 사이의 일 수<br /> </td> 
   <td> DaysDiff(&lt;종료 날짜&gt;, &lt;시작 날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>DaysOld</strong><br /> </td> 
   <td> 날짜의 일수를 반환합니다.<br /> </td> 
   <td> DaysOld(&lt;date&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>GetDate</strong><br /> </td> 
   <td> 서버의 현재 시스템 날짜를 반환합니다.<br /> </td> 
   <td> GetDate()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>시간</strong><br /> </td> 
   <td> 날짜의 시간을 반환합니다.<br /> </td> 
   <td> 시간(&lt;날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>HoursDiff</strong><br /> </td> 
   <td> 두 날짜 사이의 시간 수를 반환합니다.<br /> </td> 
   <td> HoursDiff(&lt;종료 날짜&gt;, &lt;시작 날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>LocalToUTC</strong><br /> </td> 
   <td> 로컬 날짜 및 시간을 UTC로 변환합니다.<br /> </td> 
   <td> LocalToUTC(&lt;날짜&gt;, &lt;시간대&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>분</strong><br /> </td> 
   <td> 날짜의 분을 반환합니다.<br /> </td> 
   <td> Minute(&lt;date&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>분 차이</strong><br /> </td> 
   <td> 두 날짜 사이의 분 수를 반환합니다.<br /> </td> 
   <td> MinutesDiff(&lt;종료 날짜&gt;, &lt;시작 날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>월</strong><br /> </td> 
   <td> 날짜의 월을 나타내는 숫자를 반환합니다.<br /> </td> 
   <td> 월(&lt;날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>MonthsAgo</strong><br /> </td> 
   <td> 현재 날짜 빼기 월 수를 뺀 날짜를 반환합니다.<br /> </td> 
   <td> MonthsAgo(&lt;number&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>월 비교</strong><br /> </td> 
   <td> 두 날짜 사이의 월 수를 반환합니다.<br /> </td> 
   <td> MonthsDiff(&lt;종료 날짜&gt;, &lt;시작 날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>MonthsOld</strong><br /> </td> 
   <td> 날짜의 월 수를 반환합니다.<br /> </td> 
   <td> MonthsOld(&lt;date&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>두 번째</strong><br /> </td> 
   <td> 날짜의 초 반환<br /> </td> 
   <td> Second(&lt;date&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>가장 오래된 것</strong><br /> </td> 
   <td> 가장 오래된 날짜를 반환합니다. </td> 
   <td> 가장 오래된 항목(&lt;날짜&gt;, &lt;날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>초 차이</strong><br /> </td> 
   <td> 두 날짜 사이의 시간(초)을 반환합니다.<br /> </td> 
   <td> SecondsDiff(&lt;종료 날짜&gt;, &lt;시작 날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>하위 일 수</strong><br /> </td> 
   <td> 날짜로부터 일 수 빼기<br /> </td> 
   <td> SubDays(&lt;date&gt;, &lt;number&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>하위 시간</strong><br /> </td> 
   <td> 날짜로부터 시간 빼기<br /> </td> 
   <td> SubHours(&lt;date&gt;, &lt;number&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>SubMinutes</strong><br /> </td> 
   <td> 날짜에서 분 빼기<br /> </td> 
   <td> SubMinutes(&lt;date&gt;, &lt;number&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>하위 월</strong><br /> </td> 
   <td> 날짜로부터 월 수 빼기<br /> </td> 
   <td> SubMonths(&lt;date&gt;, &lt;number&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>SubSeconds</strong><br /> </td> 
   <td> 날짜에서 초 빼기<br /> </td> 
   <td> SubSeconds(&lt;date&gt;, &lt;number&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>2년</strong><br /> </td> 
   <td> 날짜로부터 연도 빼기<br /> </td> 
   <td> SubYears(&lt;date&gt;, &lt;number&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>종료 날짜</strong><br /> </td> 
   <td> 날짜 + 시간을 날짜로 변환합니다.<br /> </td> 
   <td> ToDate(&lt;date + time&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ToDateTime</strong><br /> </td> 
   <td> 문자열을 날짜 + 시간으로 변환합니다.<br /> </td> 
   <td> ToDateTime(&lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ToDateTimeWithTimezone</strong><br /> </td> 
   <td> 문자열을 날짜 + 시간대로 변환합니다.<br /> 예:ToDateTimeWithTimezone("2019-02-19 08:09:00", "Asia/Confirme")<br /> </td> 
   <td> ToDateTimeWithTimezone(&lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>TruncDate</strong><br /> </td> 
   <td> 날짜+시간을 가장 근접한 초 단위로 반올림합니다.<br /> </td> 
   <td> TruncDate(@lastModified, &lt;초 수&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>TruncDateTZ</strong><br /> </td> 
   <td> 날짜 + 시간을 주어진 정확한 시간(초)으로 반올림합니다.<br /> </td> 
   <td> TruncDateTZ(&lt;date&gt;, &lt;초 수&gt;, &lt;시간대&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>TruncQuarter</strong><br /> </td> 
   <td> 날짜를 분기까지 반올림합니다.<br /> </td> 
   <td> TruncQuarter(&lt;날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>TruncTime</strong><br /> </td> 
   <td> 시간 부분을 가장 가까운 초까지 반올림합니다.<br /> </td> 
   <td> TruncTime(&lt;date&gt;, &lt;초 수&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>TruncWeek</strong><br /> </td> 
   <td> 날짜를 다음 주로 반올림합니다.<br /> </td> 
   <td> TruncWeek(&lt;date&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>TruncYear</strong><br /> </td> 
   <td> 날짜 + 시간을 1월 1일로 반올림합니다.<br /> </td> 
   <td> TruncYear(&lt;date&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>요일</strong><br /> </td> 
   <td> 날짜의 주 중 일을 나타내는 숫자를 반환합니다.<br /> </td> 
   <td> WeekDay(&lt;date&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>연도</strong><br /> </td> 
   <td> 날짜의 연도를 나타내는 숫자를 반환합니다.<br /> </td> 
   <td> 연도(&lt;날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>연도 및 월</strong><br /> </td> 
   <td> 날짜의 년 및 월을 나타내는 숫자를 반환합니다.<br /> </td> 
   <td> YearAndMonth(&lt;date&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>연도 비교</strong><br /> </td> 
   <td> 두 날짜 사이의 연도 수를 반환합니다.<br /> </td> 
   <td> YearsDiff(&lt;종료 날짜&gt;, &lt;시작 날짜&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>YearsOld</strong><br /> </td> 
   <td> 날짜 연령을 반환합니다.<br /> </td> 
   <td> YearOld(&lt;date&gt;)<br /> </td> 
  </tr> 
 </tbody> 
</table>

## Geomarketing {#geomarketing}

지리 마케팅 함수는 지리적 값을 조작하는 데 사용됩니다.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>이름</strong><br /> </td> 
   <td> <strong>설명</strong><br /> </td> 
   <td> <strong>구문</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>거리</strong><br /> </td> 
   <td> 경도와 위도로 정의된 두 지점 사이의 거리(도 단위)를 반환합니다.<br /> </td> 
   <td> 거리(&lt;경도 A&gt;, &lt;위도 A&gt;, &lt;경도 B&gt;, &lt;위도 B&gt;)<br /> </td> 
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
   <td> 숫자의 절대값을 반환합니다.<br /> </td> 
   <td> Abs(&lt;number&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Ceil</strong><br /> </td> 
   <td> 숫자보다 크거나 같은 가장 낮은 정수를 반환합니다.<br /> </td> 
   <td> Ceil(&lt;number&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>플로어</strong><br /> </td> 
   <td> 숫자보다 작거나 같은 최대 정수를 반환합니다.<br /> </td> 
   <td> Floor(&lt;number&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>최고</strong><br /> </td> 
   <td> 두 숫자 중 큰 숫자를 반환합니다.<br /> </td> 
   <td> Greest(&lt;number 1&gt;, &lt;number 2&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>최소</strong><br /> </td> 
   <td> 두 숫자 중 작은 수를 반환합니다.<br /> </td> 
   <td> Least(&lt;number 1&gt;, &lt;number 2&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Mod</strong><br /> </td> 
   <td> n1에서 n2까지 정수 분리의 나머지를 반환합니다.<br /> </td> 
   <td> Mod(&lt;number 1&gt;, &lt;number 2&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>백분율</strong><br /> </td> 
   <td> 백분율로 표현된 두 수의 비율을 반환합니다.<br /> </td> 
   <td> 퍼센트(&lt;number 1&gt;, &lt;number 2&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>임의</strong><br /> </td> 
   <td> 임의 값을 반환합니다.<br /> </td> 
   <td> Random()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>라운드</strong><br /> </td> 
   <td> 숫자를 소수 n으로 반올림합니다.<br /> </td> 
   <td> Round(&lt;number&gt;, &lt;소수 수&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>서명</strong><br /> </td> 
   <td> 숫자 기호를 반환합니다.<br /> </td> 
   <td> Sign(&lt;number&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ToDouble</strong><br /> </td> 
   <td> 정수를 부동 항목으로 변환<br /> </td> 
   <td> ToDouble(&lt;number&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ToInt64</strong><br /> </td> 
   <td> 부동을 64비트 정수로 변환합니다.<br /> </td> 
   <td> ToInt64(&lt;number&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ToInteger</strong><br /> </td> 
   <td> 부동 요소를 정수로 변환합니다.<br /> </td> 
   <td> ToInteger(&lt;number&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Trunc</strong><br /> </td> 
   <td> n1에서 n2까지의 십진수 자르기<br /> </td> 
   <td> Trunc(&lt;n1&gt;, &lt;n2&gt;)<br /> </td> 
  </tr> 
 </tbody> 
</table>

## 기타 {#others}

이 표에는 사용 가능한 나머지 함수가 들어 있습니다.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>이름</strong><br /> </td> 
   <td> <strong>설명</strong><br /> </td> 
   <td> <strong>구문</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>사례</strong><br /> </td> 
   <td> 조건이 확인되면 값 1을 반환합니다. 그렇지 않으면 값 2를 반환합니다.<br /> </td> 
   <td> Case(When(&lt;condition&gt;, &lt;value 1&gt;), Else(&lt;value 2&gt;)))<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ClearBit</strong><br /> </td> 
   <td> 값에서 플래그를 삭제합니다.<br /> </td> 
   <td> ClearBit(&lt;identifier&gt;, &lt;flag&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Coalesce</strong><br /> </td> 
   <td> 값 1이 0이거나 null이면 값 2를 반환하고, 그렇지 않으면 값 1을 반환합니다.<br /> </td> 
   <td> Coalesce(&lt;value 1&gt;, &lt;value 2&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>디코드</strong><br /> </td> 
   <td> 반환 값 3은 값 1 = 값 2이고, 그렇지 않으면 4가 반환됩니다.<br /> </td> 
   <td> Decode(&lt;value 1&gt;, &lt;value 2&gt;, &lt;value 3&gt;, &lt;value 4&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>기타</strong><br /> </td> 
   <td> 값 1을 반환합니다(case 함수의 매개 변수로만 사용할 수 있음).<br /> </td> 
   <td> Else(&lt;value 1&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>GetEmailDomain</strong><br /> </td> 
   <td> 이메일 주소에서 도메인 추출<br /> </td> 
   <td> GetEmailDomain(&lt;value&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>GetMirrorURL</strong><br /> </td> 
   <td> 미러 페이지 서버의 URL을 검색합니다.<br /> </td> 
   <td> GetMirrorURL(&lt;value&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Iif</strong><br /> </td> 
   <td> 표현식이 true이면 값 1을 반환하고, 그렇지 않으면 값 2를 반환합니다.<br /> </td> 
   <td> Iif(&lt;condition&gt;, &lt;value 1&gt;, &lt;value 2&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>IsBitSet</strong><br /> </td> 
   <td> 플래그가<br /> </td> 
   <td> IsBitSet(&lt;identifier&gt;, &lt;flag&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>IsEmptyString</strong><br /> </td> 
   <td> 문자열이 비어 있으면 값 2를 반환하고, 그렇지 않으면 값 3을 반환합니다.<br /> </td> 
   <td> IsEmptyString(&lt;문자열&gt;, &lt;값 2&gt;, &lt;값 3&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>NoNull</strong><br /> </td> 
   <td> 인수가 NULL이면 빈 문자열을 반환합니다.<br /> </td> 
   <td> NoNull(&lt;value&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>RowId</strong><br /> </td> 
   <td> 라인 번호를 반환합니다.<br /> </td> 
   <td> RowId<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>SetBit</strong><br /> </td> 
   <td> Formats the Flag in the value<br /> </td> 
   <td> SetBit(&lt;identifier&gt;, &lt;flag&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ToBoolean</strong><br /> </td> 
   <td> 숫자를 부울로 변환합니다.<br /> </td> 
   <td> ToBoolean(&lt;number&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>언제</strong><br /> </td> 
   <td> 표현식이 확인되면 값 1을 반환합니다. 그렇지 않으면 값 2를 반환합니다(case 함수의 매개 변수로만 사용할 수 있음).<br /> </td> 
   <td> When(&lt;condition&gt;, &lt;value 1&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>newUUID</strong><br /> </td> 
   <td> 새 UUID를 반환합니다.<br /> </td> 
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
   <td> 모든 매개 변수가 null이 아니며 비어 있지 않은지 여부를 나타냅니다.<br /> </td> 
   <td> AllNonNull2(&lt;문자열&gt;, &lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AllNonNull3</strong><br /> </td> 
   <td> 모든 매개 변수가 null이 아니며 비어 있지 않은지 여부를 나타냅니다.<br /> </td> 
   <td> AllNonNull3(&lt;문자열&gt;, &lt;문자열&gt;, &lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ASCII</strong><br /> </td> 
   <td> 문자열에서 첫 번째 문자의 ASCII 값을 반환합니다.<br /> </td> 
   <td> Ascii(&lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Char</strong><br /> </td> 
   <td> 'n' ASCII 코드에 해당하는 문자를 반환합니다.<br /> </td> 
   <td> Char(&lt;number&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Charindex</strong><br /> </td> 
   <td> 문자열 1에서 문자열 2의 위치를 반환합니다.<br /> </td> 
   <td> Charindex(&lt;문자열&gt;, &lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>DataLength</strong><br /> </td> 
   <td> 문자열의 문자 수를 반환합니다.<br /> </td> 
   <td> DataLength(&lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>GetLine</strong><br /> </td> 
   <td> 문자열의 n번째(1-n) 행을 반환합니다.<br /> </td> 
   <td> GetLine(&lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>IfEquals</strong><br /> </td> 
   <td> 처음 두 매개 변수가 같은 경우 세 번째 매개 변수를 반환합니다. 그렇지 않으면 마지막 매개 변수를 반환합니다.<br /> </td> 
   <td> IfEquals(&lt;문자열&gt;, &lt;문자열&gt;, &lt;문자열&gt;, &lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>IsMemoNull</strong><br /> </td> 
   <td> 매개 변수로 전달된 메모가 null인지 여부를 나타냅니다.<br /> </td> 
   <td> IsMemoNull(&lt;메모&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>JuxtWords</strong><br /> </td> 
   <td> 매개 변수로 전달된 두 문자열을 설명합니다. 반환된 값의 각 문자열 사이에 공백이 추가됩니다.<br /> </td> 
   <td> JuxtWords(&lt;문자열&gt;, &lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>JuxtWords3</strong><br /> </td> 
   <td> 매개 변수로 전달된 세 문자열을 설명합니다. 반환된 값의 각 문자열 사이에 공백이 추가됩니다.<br /> </td> 
   <td> JuxtWords3(&lt;문자열&gt;, &lt;문자열&gt;, &lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>LPad</strong><br /> </td> 
   <td> 왼쪽에서 완료된 문자열을 반환합니다.<br /> </td> 
   <td> LPad(&lt;문자열&gt;, &lt;숫자&gt;, &lt;caractuère&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>왼쪽</strong><br /> </td> 
   <td> 문자열의 첫 번째 n자를 반환합니다.<br /> </td> 
   <td> Left(&lt;string&gt;, &lt;number&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>길이</strong><br /> </td> 
   <td> 문자열 길이를 반환합니다.<br /> </td> 
   <td> 길이(&lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>하한</strong><br /> </td> 
   <td> 문자열을 소문자로 반환합니다.<br /> </td> 
   <td> Lower(&lt;string&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Ltrim</strong><br /> </td> 
   <td> 문자열 왼쪽에 공백을 제거합니다.<br /> </td> 
   <td> Ltrim(&lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Md5Digest</strong><br /> </td> 
   <td> 문자열의 MD5 키의 16진수 표현을 반환합니다.<br /> </td> 
   <td> Md5Digest(&lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>메모포함</strong><br /> </td> 
   <td> 메모에 매개 변수로 전달된 문자열이 포함되어 있는지 여부를 지정합니다.<br /> </td> 
   <td> MemoContains(&lt;메모&gt;, &lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>RPad</strong><br /> </td> 
   <td> 오른쪽의 완료된 문자열을 반환합니다.<br /> </td> 
   <td> RPad(&lt;문자열&gt;, &lt;숫자&gt;, &lt;문자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>바꾸기</strong><br /> </td> 
   <td> 지정된 문자열(두 번째 매개 변수) 값의 모든 발생을 문자열의 다른 문자열 값(세 번째 매개 변수)으로 바꿉니다(첫 번째 매개 변수).<br /> </td> 
   <td> Replace(&lt;String&gt;, &lt;String&gt;, &lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>오른쪽</strong><br /> </td> 
   <td> 문자열의 마지막 n자를 반환합니다.<br /> </td> 
   <td> 오른쪽(&lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Rtrim</strong><br /> </td> 
   <td> 문자열 오른쪽에 공백을 제거합니다.<br /> </td> 
   <td> Rtrim(&lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha256Digest</strong><br /> </td> 
   <td> 지정된 UTF8 <strong>문자열에</strong> 대한 표준 SHA256 해시를 계산합니다.<br /> </td> 
   <td> Sha256Digest(&lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha384Digest</strong><br /> </td> 
   <td> 지정된 UTF8 <strong>문자열에</strong> 대한 표준 SHA384 해시를 계산합니다.<br /> </td> 
   <td> Sha384Digest(&lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha512Digest</strong><br /> </td> 
   <td> 지정된 UTF8 <strong>문자열에</strong> 대한 표준 SHA512 해시를 계산합니다.<br /> </td> 
   <td> Sha512Digest(&lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>스마트</strong><br /> </td> 
   <td> 각 단어의 첫 번째 문자로 된 문자열을 대문자로 반환합니다.<br /> </td> 
   <td> Smart(&lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>하위 문자열</strong><br /> </td> 
   <td> 문자열 n1에서 시작하여 n2의 길이로 하위 문자열을 추출합니다.<br /> </td> 
   <td> 하위 문자열(&lt;문자열&gt;, &lt;오프셋&gt;, &lt;길이&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ToIntlString</strong><br /> </td> 
   <td> 숫자를 문자열로 변환합니다.<br /> </td> 
   <td> ToIntlString(&lt;number&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ToString</strong><br /> </td> 
   <td> 숫자를 문자열로 변환합니다.<br /> </td> 
   <td> ToString(&lt;number&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>상단</strong><br /> </td> 
   <td> 문자열을 대문자로 반환합니다.<br /> </td> 
   <td> Upper(&lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>VirtualLink</strong><br /> </td> 
   <td> 다른 두 매개 변수가 동일한 경우 매개 변수로 전달된 링크의 외래 키를 반환합니다.<br /> </td> 
   <td> VirtualLink(&lt;number&gt;, &lt;number&gt;, &lt;number&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>VirtualLinkStr</strong><br /> </td> 
   <td> 다른 두 매개 변수가 동일한 경우 매개 변수로 전달된 링크의 외래(텍스트) 키를 반환합니다.<br /> </td> 
   <td> VirtualLinkStr(&lt;문자열&gt;, &lt;숫자&gt;, &lt;번호&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>encryption_aescbcDecrypt</strong><br /> </td> 
   <td> HEX 형식(2차 매개 변수) 및 HEX 형식의 초기화 벡터(3rd 매개 변수)를 사용하여 "<strong>x</strong>" 접두어(1st 매개 변수)를 사용하여 암호화된 값을 HEX 형식으로 해독합니다.<br /> </td> 
   <td> encryption_aescbcDecrypt(&lt;String&gt;, &lt;String&gt;, &lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>encryption_aescbcEncrypt</strong><br /> </td> 
   <td> 키(2번째 매개 변수)와 초기화 벡터(3번째 매개 변수)를 사용하여 AES 알고리즘(CBC 블록 모드)을 사용하여 암호화합니다. 키와 초기화 벡터는 <strong>\x부터 시작하는 16진수 표현으로 지정해야 합니다</strong>. 결과는 <strong>\x</strong>없이 16진수로 표시됩니다.<br /> 키 크기는 128비트, 192비트, 256비트(16, 24, 32개의 16진수 문자)일 수 있지만 키와 동일한 길이의 무작위 IV를 사용하는 것이 좋습니다.<br /> </td> 
   <td> encryption_aescbcEncrypt(&lt;String&gt;, &lt;String&gt;, &lt;String&gt;)<br /> 예:encryption_aescbcEncrypt(johndoe@example.com, "<strong>\x0123456789ABCDEF0123456789ABCDEF</strong>", "<strong>\x0123456789ABCDEFFEDCBA0ABCBA 9876543210</strong>")<br /> </td> 
  </tr> 
 </tbody> 
</table>

## 집계 {#aggregates}

집계 함수는 워크플로우의 [활동에서 추가 데이터를](../../automating/using/query.md#enriching-data) **[!UICONTROL Query]**추가할 때만 사용할 수 있습니다.

집계 함수는 값 세트에 대한 계산을 수행하는 데 사용됩니다.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>이름</strong><br /> </td> 
   <td> <strong>설명</strong><br /> </td> 
   <td> <strong>구문</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>평균</strong>, 평균<br /> </td> 
   <td> 숫자 열의 평균을 반환합니다.<br /> </td> 
   <td> Avg(&lt;value&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>카운트</strong>, 카운트(NULL 제외)<br /> </td> 
   <td> 열에서 null이 아닌 값을 계산합니다.<br /> </td> 
   <td> Count(&lt;value&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>모두 계산</strong>, 모두 계산<br /> </td> 
   <td> 모든 값(null 값 및 중복 포함)을 계산합니다.<br /> </td> 
   <td> CountAll()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>고유</strong>수, 고유 수<br /> </td> 
   <td> 열에서 null이 아닌 고유한 값을 계산합니다.<br /> </td> 
   <td> Countdistinct(&lt;value&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Max</strong>, Max<br /> </td> 
   <td> 숫자, 문자열 또는 날짜 열에서 최대값을 반환합니다.<br /> </td> 
   <td> Max(&lt;value&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>최소</strong>, 최소<br /> </td> 
   <td> 숫자, 문자열 또는 날짜 열에서 최소값을 반환합니다.<br /> </td> 
   <td> Min(&lt;value&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>합계</strong>, 합계<br /> </td> 
   <td> 숫자 열에 있는 값의 합계를 반환합니다.<br /> </td> 
   <td> Sum(&lt;value&gt;)<br /> </td> 
  </tr> 
 </tbody> 
</table>

## 표현 {#representation}

표현 함수는 값을 정렬하는 데 사용됩니다.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>이름</strong><br /> </td> 
   <td> <strong>설명</strong><br /> </td> 
   <td> <strong>구문</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>설명</strong><br /> </td> 
   <td> 내림차순 정렬 적용<br /> </td> 
   <td> Desc(&lt;value 1&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>OrderBy</strong><br /> </td> 
   <td> 파티션 내의 결과 정렬<br /> </td> 
   <td> OrderBy(&lt;value 1&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>PartitionBy</strong><br /> </td> 
   <td> 테이블의 쿼리 결과 분할<br /> </td> 
   <td> PartitionBy(&lt;value 1&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>행 번호</strong><br /> </td> 
   <td> 테이블 분할 영역과 정렬 순서에 따라 라인 번호를 생성합니다. 이 함수는 MySQL에서 지원되지 않습니다.<br /> </td> 
   <td> RowNum(PartitionBy(&lt;value 1&gt;), OrderBy(&lt;value 1&gt;))<br /> </td> 
  </tr> 
 </tbody> 
</table>

