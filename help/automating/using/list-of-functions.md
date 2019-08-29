---
title: 함수 목록
seo-title: 함수 목록
description: 함수 목록
seo-description: 쿼리 편집 도구를 사용하면 고급 기능을 사용하여 복잡한 필터링을 수행할 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: FD 50 FC 99-1 E 7 A -479 B-BEB 7-1 F 246 B 419 D 46
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 필터링 데이터
discoiquuid: 3 CDBE 962-1 c 59-4 CD 8-B 29 E -36 AA 2562 FAC 6
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 83be3f22f3508248f2a4666080a7207998093dc3

---


# 함수 목록{#list-of-functions}

## 함수 정보 {#about-functions}

쿼리 편집 도구를 사용하면 고급 기능을 사용하여 복잡한 필터링을 수행할 수 있습니다. 이렇게 하려면 도구 팔레트에 작업 영역에서 사용할 수 있는 **[!UICONTROL Expression]** 요소가 포함되어 있습니다. 이 요소에 대한 자세한 내용은 특정 섹션에 자세히 [](../../automating/using/advanced-expression-editing.md)설명되어 있습니다.

이 요소를 사용하면 조건을 수동으로 입력할 수 있습니다. 여기에서 다음 섹션에 정의된 기능을 사용할 수 있습니다.

원하는 결과와 조작 데이터의 유형에 따라 몇 가지 함수 유형을 사용할 수 있습니다.

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
   <td> <strong>name</strong><br /> </td> 
   <td> <strong>description</strong><br /> </td> 
   <td> <strong>구문</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Adddays</strong><br /> </td> 
   <td> 날짜에 일 수를 추가합니다.<br /> </td> 
   <td> Adddays (&lt; date &gt;, &lt; number &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Addhours</strong><br /> </td> 
   <td> 날짜에 많은 시간 추가<br /> </td> 
   <td> Addhours (&lt; date &gt;, &lt; number &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Addminutes</strong><br /> </td> 
   <td> 날짜에 분 수 추가<br /> </td> 
   <td> Addminutes (&lt; date &gt;, &lt; number &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Addmonths</strong><br /> </td> 
   <td> 날짜에 월을 추가합니다.<br /> </td> 
   <td> Addmonths (&lt; date &gt;, &lt; number &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Addseconds</strong><br /> </td> 
   <td> 날짜에 초를 추가합니다.<br /> </td> 
   <td> Addseconds (&lt; date &gt;, &lt; number &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Addyears</strong><br /> </td> 
   <td> 날짜를 날짜에 추가합니다.<br /> </td> 
   <td> Addyears (&lt; date &gt;, &lt; number &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Dateonly</strong><br /> </td> 
   <td> 날짜만 반환합니다 (00:00에 시간 포함).<br /> </td> 
   <td> Dateonly (&lt; date &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>day</strong><br /> </td> 
   <td> 날짜 날짜를 나타내는 숫자를 반환합니다.<br /> </td> 
   <td> day (&lt; date &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Dayofyear</strong><br /> </td> 
   <td> 날짜의 연도에서 날짜를 나타내는 숫자를 반환합니다.<br /> </td> 
   <td> Dayofyear (&lt; date &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>daysago</strong><br /> </td> 
   <td> 현재 날짜를 빼기 N 일 반환<br /> </td> 
   <td> Daysago (&lt; number &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>daysagoint</strong><br /> </td> 
   <td> 현재 날짜를 빼기 n 일 (정수 yyyymmdd) 로 반환합니다.<br /> </td> 
   <td> daysagoint (&lt; number &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Daysdiff</strong><br /> </td> 
   <td> 두 날짜 사이의 일 수<br /> </td> 
   <td> Daysdiff (&lt; 종료 날짜 &gt;, &lt; 시작 날짜 &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>판매일</strong><br /> </td> 
   <td> 날짜의 일 수를 반환합니다.<br /> </td> 
   <td> 판매일 (&lt; 날짜 &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Getdate</strong><br /> </td> 
   <td> 서버의 현재 시스템 날짜를 반환합니다.<br /> </td> 
   <td> Getdate ()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>hour</strong><br /> </td> 
   <td> 날짜 시간을 반환합니다.<br /> </td> 
   <td> hour (&lt; date &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Hoursdiff</strong><br /> </td> 
   <td> 두 날짜 사이의 시간 반환<br /> </td> 
   <td> Hoursdiff (&lt; end date &gt;, &lt; start date &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Localtoutc</strong><br /> </td> 
   <td> 로컬 날짜 및 시간을 UTC로 변환합니다.<br /> </td> 
   <td> Localtoutc (&lt; date &gt;, &lt; 시간대 &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>분</strong><br /> </td> 
   <td> 날짜의 분 반환<br /> </td> 
   <td> 분 (&lt; 날짜 &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Minutesdiff</strong><br /> </td> 
   <td> 두 날짜 사이의 분 수를 반환합니다.<br /> </td> 
   <td> Minutesdiff (&lt; end date &gt;, &lt; start date &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>월</strong><br /> </td> 
   <td> 날짜의 월을 나타내는 숫자를 반환합니다.<br /> </td> 
   <td> 월 (&lt; 날짜 &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>monthsago</strong><br /> </td> 
   <td> 현재 날짜에 해당하는 날짜를 빼기 n 개월로 반환합니다.<br /> </td> 
   <td> Monthsago (&lt; number &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Monthsdiff</strong><br /> </td> 
   <td> 두 날짜 사이의 개월 수를 반환합니다.<br /> </td> 
   <td> Monthsdiff (&lt; End Date &gt;, &lt; Start Date &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Monthsold</strong><br /> </td> 
   <td> 날짜의 연령 (개월) 를 반환합니다.<br /> </td> 
   <td> Monthsold (&lt; date &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>second</strong><br /> </td> 
   <td> 날짜의 초를 반환합니다.<br /> </td> 
   <td> second (&lt; date &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>가장 오래된 항목</strong><br /> </td> 
   <td> 가장 오래된 날짜를 반환합니다. </td> 
   <td> 가장 오래된 항목 (&lt; 날짜 &gt;, &lt; 날짜 &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Secondsdiff</strong><br /> </td> 
   <td> 두 날짜 사이의 시간 (초) 를 반환합니다.<br /> </td> 
   <td> Secondsdiff (&lt; 종료 날짜 &gt;, &lt; 시작 날짜 &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Subdays</strong><br /> </td> 
   <td> 날짜에서 일 수를 뺍니다.<br /> </td> 
   <td> Subdays (&lt; date &gt;, &lt; number &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Subhours</strong><br /> </td> 
   <td> 날짜에서 시간 빼기<br /> </td> 
   <td> Subhours (&lt; date &gt;, &lt; number &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>subminutes</strong><br /> </td> 
   <td> 날짜에서 분 수를 뺍니다.<br /> </td> 
   <td> Subminutes (&lt; date &gt;, &lt; number &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Submonths</strong><br /> </td> 
   <td> 날짜에서 개월 수를 뺍니다.<br /> </td> 
   <td> Submonths (&lt; date &gt;, &lt; number &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>subseconds</strong><br /> </td> 
   <td> 날짜에서 시간 (초) 를 뺍니다.<br /> </td> 
   <td> Subseconds (&lt; date &gt;, &lt; number &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Subyears</strong><br /> </td> 
   <td> 날짜에서 년 수를 뺍니다.<br /> </td> 
   <td> Subyears (&lt; date &gt;, &lt; number &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Todate</strong><br /> </td> 
   <td> 날짜를 날짜 + 시간을 날짜로 변환<br /> </td> 
   <td> Todate (&lt; date + time &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Todatetime</strong><br /> </td> 
   <td> 문자열을 날짜 + 시간으로 변환합니다.<br /> </td> 
   <td> Todatetime (&lt; string &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Todatetimewithtimezone</strong><br /> </td> 
   <td> 문자열을 날짜 + 시간대로 변환합니다.<br /> 예: Todatetimewithtimezone ("2019-02-19 08:09:00", "Asia/Tehran")<br /> </td> 
   <td> Todatetimewithtimezone (&lt; string &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Truncdate</strong><br /> </td> 
   <td> 날짜 + 시간을 가장 가까운 두 번째 시간으로 반올림합니다.<br /> </td> 
   <td> Truncdate (@ lastmodified, &lt; number of seconds &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>truncdatetz</strong><br /> </td> 
   <td> 날짜 + 시간을 초 단위의 지정된 정밀도 표시로 반올림합니다.<br /> </td> 
   <td> Truncdatetz (&lt; date &gt;, &lt; number of seconds &gt;, &lt; timezone &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Truncquarter</strong><br /> </td> 
   <td> 분기별로 날짜를 반올림합니다.<br /> </td> 
   <td> Truncquarter (&lt; date &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Trunctime</strong><br /> </td> 
   <td> 시간 부분을 가장 가까운 두 번째 부분으로 반올림합니다.<br /> </td> 
   <td> Trunctime (&lt; date &gt;, &lt; number of seconds &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Truncweek</strong><br /> </td> 
   <td> 일주일로 날짜를 반올림합니다.<br /> </td> 
   <td> Truncweek (&lt; date &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Truncyear</strong><br /> </td> 
   <td> 날짜 + 시간을 연도의 1 월 1 일로 반올림합니다.<br /> </td> 
   <td> Truncyear (&lt; date &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>평일</strong><br /> </td> 
   <td> 날짜의 요일을 나타내는 숫자를 반환합니다.<br /> </td> 
   <td> 평일 (&lt; 날짜 &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>년</strong><br /> </td> 
   <td> 날짜의 연도를 나타내는 숫자를 반환합니다.<br /> </td> 
   <td> 연도 (&lt; 날짜 &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>년 및 월</strong><br /> </td> 
   <td> 날짜의 연도 및 월을 나타내는 숫자를 반환합니다.<br /> </td> 
   <td> Yearandmonth (&lt; date &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Yearsdiff</strong><br /> </td> 
   <td> 두 날짜 사이의 년 수를 반환합니다.<br /> </td> 
   <td> Yearsdiff (&lt; end date &gt;, &lt; start date &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Yearsold</strong><br /> </td> 
   <td> 날짜의 년령을 반환합니다.<br /> </td> 
   <td> Yearsold (&lt; date &gt;)<br /> </td> 
  </tr> 
 </tbody> 
</table>

## Geomarketing {#geomarketing}

지리적 가치를 조작하는 데 Geomarketing 함수가 사용됩니다.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>name</strong><br /> </td> 
   <td> <strong>description</strong><br /> </td> 
   <td> <strong>구문</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>거리</strong><br /> </td> 
   <td> 경도 및 위도로 정의된 두 점 사이의 거리를 킬로미터 단위로 반환합니다 (도로 표시됨).<br /> </td> 
   <td> 거리 (&lt; 경도 A &gt;, &lt; 위도 A &gt;, &lt; 경도 B &gt;, &lt; 위도 B &gt;)<br /> </td> 
  </tr> 
 </tbody> 
</table>

## 숫자 {#numerical}

숫자 값 함수는 텍스트를 숫자로 변환하는 데 사용됩니다.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>name</strong><br /> </td> 
   <td> <strong>description</strong><br /> </td> 
   <td> <strong>구문</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ABS</strong><br /> </td> 
   <td> 숫자의 절대값을 반환합니다.<br /> </td> 
   <td> ABS (&lt; number &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Ceil</strong><br /> </td> 
   <td> 숫자보다 크거나 같은 가장 낮은 정수를 반환합니다.<br /> </td> 
   <td> Ceil (&lt; number &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>floor</strong><br /> </td> 
   <td> 숫자보다 크거나 같은 가장 큰 정수를 반환합니다.<br /> </td> 
   <td> floor (&lt; number &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>greatest</strong><br /> </td> 
   <td> 두 숫자 중 큰 쪽을 반환합니다.<br /> </td> 
   <td> greatest (&lt; number 1 &gt;, &lt; number 2 &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>least</strong><br /> </td> 
   <td> 두 숫자 중 작은 쪽을 반환합니다.<br /> </td> 
   <td> least (&lt; number 1 &gt;, &lt; number 2 &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>MOD</strong><br /> </td> 
   <td> N 1에서 N 2로 정수 나눈 나머지를 반환합니다.<br /> </td> 
   <td> mod (&lt; number 1 &gt;, &lt; number 2 &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>퍼센트</strong><br /> </td> 
   <td> 백분율로 표현된 두 숫자의 비율을 반환합니다.<br /> </td> 
   <td> 퍼센트 (&lt; 숫자 1 &gt;, &lt; 숫자 2 &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>임의</strong><br /> </td> 
   <td> 임의 값을 반환합니다.<br /> </td> 
   <td> random ()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>round</strong><br /> </td> 
   <td> 숫자를 소수점 이하 n 개로 반올림합니다.<br /> </td> 
   <td> round (&lt; number &gt;, &lt; number of decimal &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>sign</strong><br /> </td> 
   <td> 숫자의 기호를 반환합니다.<br /> </td> 
   <td> Sign (&lt; number &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Todouble</strong><br /> </td> 
   <td> 정수를 부동 변수로 변환합니다.<br /> </td> 
   <td> Todouble (&lt; number &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ToInt64</strong><br /> </td> 
   <td> float를 64 비트 정수로 변환합니다.<br /> </td> 
   <td> Toint 64 (&lt; number &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Tointeger</strong><br /> </td> 
   <td> float를 정수로 변환합니다.<br /> </td> 
   <td> Tointeger (&lt; number &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>trunc</strong><br /> </td> 
   <td> N 1를 N 2 십진수로 잘라내기<br /> </td> 
   <td> Trunc (&lt; n 1 &gt;, &lt; n 2 &gt;)<br /> </td> 
  </tr> 
 </tbody> 
</table>

## others {#others}

이 표에는 남아 있는 나머지 함수가 포함되어 있습니다.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>name</strong><br /> </td> 
   <td> <strong>description</strong><br /> </td> 
   <td> <strong>구문</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>case</strong><br /> </td> 
   <td> 조건이 확인되면 값 1를 반환합니다. 그렇지 않으면, 값 2를 반환합니다.<br /> </td> 
   <td> case (when (&lt; condition &gt;, &lt; value 1 &gt;), else (&lt; value 2 &gt;))<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Clearbit</strong><br /> </td> 
   <td> 값에서 플래그를 삭제합니다.<br /> </td> 
   <td> Clearbit (&lt; identifier &gt;, &lt; flag &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Coalesce</strong><br /> </td> 
   <td> 값 1 이 0 이거나 null 이면 value 2를 반환하고, 그렇지 않으면 value 1를 반환합니다.<br /> </td> 
   <td> Coalesce (&lt; value 1 &gt;, &lt; value 2 &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>decode</strong><br /> </td> 
   <td> 반환 값 3는 value 1 = value 2 이고, 그렇지 않으면 4 입니다.<br /> </td> 
   <td> decode (&lt; value 1 &gt;, &lt; value 2 &gt;, &lt; value 3 &gt;, &lt; value 4 &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>else</strong><br /> </td> 
   <td> 반환 값 1 (case 함수의 매개 변수로만 사용할 수 있음)<br /> </td> 
   <td> else (&lt; value 1 &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Getemaildomain</strong><br /> </td> 
   <td> 이메일 주소에서 도메인 추출<br /> </td> 
   <td> Getemaildomain (&lt; value &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Getmirrorurl</strong><br /> </td> 
   <td> 미러 페이지 서버의 URL를 검색합니다.<br /> </td> 
   <td> Getmirrorurl (&lt; value &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>IIF</strong><br /> </td> 
   <td> 표현식이 true 이면 value 1를 반환하고, 그렇지 않으면 value 2를 반환합니다.<br /> </td> 
   <td> IIF (&lt; condition &gt;, &lt; value 1 &gt;, &lt; value 2 &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Isbitset</strong><br /> </td> 
   <td> 플래그가 값에 있는지 여부를 나타냅니다.<br /> </td> 
   <td> Isbitset (&lt; identifier &gt;, &lt; flag &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Isemptystring</strong><br /> </td> 
   <td> 문자열이 비어 있으면 value 2를 반환하고, 그렇지 않으면 value 3를 반환합니다.<br /> </td> 
   <td> Isemptystring (&lt; string &gt;, &lt; value 2 &gt;, &lt; value 3 &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Nonull</strong><br /> </td> 
   <td> 인수가 null 인 경우 빈 문자열을 반환합니다.<br /> </td> 
   <td> Nonull (&lt; value &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ROWID</strong><br /> </td> 
   <td> 줄 번호를 반환합니다.<br /> </td> 
   <td> ROWID<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Setbit</strong><br /> </td> 
   <td> 값에 플래그를 적용합니다.<br /> </td> 
   <td> Setbit (&lt; identifier &gt;, &lt; flag &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Toboolean</strong><br /> </td> 
   <td> 숫자를 부울 값으로 변환합니다.<br /> </td> 
   <td> Toboolean (&lt; number &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>when</strong><br /> </td> 
   <td> 표현식이 확인되면 값 1를 반환합니다. 그렇지 않으면 value 2를 반환합니다 (case 함수의 매개 변수로만 사용할 수 있음).<br /> </td> 
   <td> when (&lt; condition &gt;, &lt; value 1 &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Newuuid</strong><br /> </td> 
   <td> 새 UUID를 반환합니다.<br /> </td> 
   <td> Newuuid<br /> </td> 
  </tr> 
 </tbody> 
</table>

## 문자열 {#string}

문자열 함수는 문자열 집합을 조작하는 데 사용됩니다.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>name</strong><br /> </td> 
   <td> <strong>description</strong><br /> </td> 
   <td> <strong>구문</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AllNonNull2</strong><br /> </td> 
   <td> 모든 매개 변수가 null 이 아니고 비어 있지 않은지 나타냅니다.<br /> </td> 
   <td> Allnonnull 2 (&lt; String &gt;, &lt; String &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AllNonNull3</strong><br /> </td> 
   <td> 모든 매개 변수가 null 이 아니고 비어 있지 않은지 나타냅니다.<br /> </td> 
   <td> Allnonnull 3 (&lt; String &gt;, &lt; String &gt;, &lt; String &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ASCII</strong><br /> </td> 
   <td> 문자열에서 첫 번째 문자의 ASCII 값을 반환합니다.<br /> </td> 
   <td> ASCII (&lt; string &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>char</strong><br /> </td> 
   <td> ' n'ASCII 코드에 해당하는 문자를 반환합니다.<br /> </td> 
   <td> char (&lt; number &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Charindex</strong><br /> </td> 
   <td> String 1에서 String 2의 위치를 반환합니다.<br /> </td> 
   <td> Charindex (&lt; string &gt;, &lt; string &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Datalength</strong><br /> </td> 
   <td> 문자열의 문자 수를 반환합니다.<br /> </td> 
   <td> Datalength (&lt; string &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Getline</strong><br /> </td> 
   <td> 문자열의 nth (1 부터 n) 행을 반환합니다.<br /> </td> 
   <td> Getline (&lt; string &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>IFEQUALS</strong><br /> </td> 
   <td> 처음 두 매개 변수가 동일하면 세 번째 매개 변수를 반환하고 나머지 매개 변수는 반환합니다.<br /> </td> 
   <td> Ifequals (&lt; string &gt;, &lt; string &gt;, &lt; string &gt;, &lt; string &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Ismemonull</strong><br /> </td> 
   <td> 매개 변수로 전달된 메모가 null 인지를 나타냅니다.<br /> </td> 
   <td> Ismemonull (&lt; memo &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>juxtwords</strong><br /> </td> 
   <td> 매개 변수로 전달된 두 문자열을 concates 합니다. 반환된 값의 각 문자열 사이에 공백이 추가됩니다.<br /> </td> 
   <td> Juxtwords (&lt; string &gt;, &lt; string &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>JuxtWords3</strong><br /> </td> 
   <td> 매개 변수로 전달된 세 개의 문자열을 만듭니다. 반환된 값의 각 문자열 사이에 공백이 추가됩니다.<br /> </td> 
   <td> Juxtwords 3 (&lt; string &gt;, &lt; string &gt;, &lt; string &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Lpad</strong><br /> </td> 
   <td> 왼쪽의 완료된 문자열을 반환합니다.<br /> </td> 
   <td> Lpad (&lt; string &gt;, &lt; number &gt;, &lt; caractère &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>left</strong><br /> </td> 
   <td> 문자열의 첫 번째 n 문자를 반환합니다.<br /> </td> 
   <td> left (&lt; string &gt;, &lt; number &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>길이</strong><br /> </td> 
   <td> 문자열 길이를 반환합니다.<br /> </td> 
   <td> length (&lt; string &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>lower</strong><br /> </td> 
   <td> 문자열을 소문자로 반환합니다.<br /> </td> 
   <td> lower (&lt; string &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Ltrim</strong><br /> </td> 
   <td> 문자열 왼쪽에 공백을 제거합니다.<br /> </td> 
   <td> Ltrim (&lt; string &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Md5Digest</strong><br /> </td> 
   <td> 문자열의 MD 5 키를 16 진수 표현으로 반환합니다.<br /> </td> 
   <td> MD 5 Digest (&lt; String &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Memocontains</strong><br /> </td> 
   <td> 메모에 매개 변수로 전달된 문자열이 포함되어 있는지 여부를 지정합니다.<br /> </td> 
   <td> Memocontains (&lt; memo &gt;, &lt; string &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Rpad</strong><br /> </td> 
   <td> 오른쪽의 완료된 문자열을 반환합니다.<br /> </td> 
   <td> Rpad (&lt; string &gt;, &lt; number &gt;, &lt; character &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>replace</strong><br /> </td> 
   <td> 문자열에서 지정된 문자열 (2 nd 매개 변수) 값을 모두 다른 문자열 값 (3 rd 매개 변수) 로 바꿉니다 (첫 번째 매개 변수).<br /> </td> 
   <td> replace (&lt; string &gt;, &lt; string &gt;, &lt; string &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>right</strong><br /> </td> 
   <td> 문자열의 마지막 n 문자를 반환합니다.<br /> </td> 
   <td> right (&lt; string &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Rtrim</strong><br /> </td> 
   <td> 문자열 오른쪽에 공백을 제거합니다.<br /> </td> 
   <td> Rtrim (&lt; string &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha256Digest</strong><br /> </td> 
   <td> 지정된 UTF 8 문자열에 대한 표준 <strong>SHA 256</strong> 해시를 계산합니다.<br /> </td> 
   <td> SHA 256 Digest (&lt; String &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha384Digest</strong><br /> </td> 
   <td> 지정된 UTF 8 문자열에 대한 표준 <strong>SHA 384</strong> 해시를 계산합니다.<br /> </td> 
   <td> SHA 384 Digest (&lt; String &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha512Digest</strong><br /> </td> 
   <td> 지정된 UTF 8 문자열에 대한 표준 <strong>SHA 512</strong> 해시를 계산합니다.<br /> </td> 
   <td> SHA 512 Digest (&lt; String &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>smart</strong><br /> </td> 
   <td> 대문자로 각 단어의 첫 번째 문자가 포함된 문자열을 반환합니다.<br /> </td> 
   <td> Smart (&lt; string &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>하위 문자열</strong><br /> </td> 
   <td> 문자열의 문자 n 1에서 시작하여 길이가 N 2 인 하위 문자열을 추출합니다.<br /> </td> 
   <td> substring (&lt; string &gt;, &lt; offset &gt;, &lt; length &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Tointlstring</strong><br /> </td> 
   <td> 숫자를 문자열로 변환합니다.<br /> </td> 
   <td> Tointlstring (&lt; number &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ToString</strong><br /> </td> 
   <td> 숫자를 문자열로 변환합니다.<br /> </td> 
   <td> ToString (&lt; number &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>upper</strong><br /> </td> 
   <td> 대문자로 문자열을 반환합니다.<br /> </td> 
   <td> UPPER (&lt; string &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Virtuallink</strong><br /> </td> 
   <td> 다른 매개 변수가 같은 경우 매개 변수로 전달된 링크의 외래 키를 반환합니다.<br /> </td> 
   <td> Virtuallink (&lt; number &gt;, &lt; number &gt;, &lt; number &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Virtuallinkstr</strong><br /> </td> 
   <td> 다른 두 매개 변수가 같은 경우 매개 변수로 전달된 링크의 외래 (텍스트) 키를 반환합니다.<br /> </td> 
   <td> Virtuallinkstr (&lt; string &gt;, &lt; number &gt;, &lt; number &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>encryption_ aescbcdecrypt</strong><br /> </td> 
   <td> 16 진수 형식 (2 차 매개 변수) 의 키를 사용하여 "<strong>x</strong>" 접두어 (1 st 매개 변수) 와 16 진수 형식 (3 rd 매개 변수) 의 초기화 벡터를 사용하여 암호화된 값을 16 진수 형식으로 해독합니다.<br /> </td> 
   <td> ENCRYPTION_ AESCBCDECRYPT (&lt; STRING &gt;, &lt; string &gt;, &lt; string &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>encryption_ aescbcencrypt</strong><br /> </td> 
   <td> AES 알고리즘 (CBC 블록 모드) 를 사용하여 키 (2 nd 매개 변수) 와 초기화 벡터 (3 rd 매개 변수) 가 있는 문자열 (첫 번째 매개 변수) 를 암호화합니다. 키와 초기화 벡터는 16 진수 표현으로 주어져야 합니다 (\ x 다음으로 <strong>시작</strong>). 결과는 <strong>\ x</strong>없이 16 진수가 됩니다.<br /> 키 크기는 128 비트, 192 비트, 256 비트 (16, 24, 16, 24, 32 진수 문자) 이지만, 키와 동일한 길이의 임의 IV를 사용하는 것이 좋습니다.<br /> </td> 
   <td> ENCRYPTION_ AESCBCENCRYPT (&lt; STRING &gt;, &lt; STRING &gt;, &lt; STRING &gt;)<br /> : encryption_ aescbcencrypt (johndoe@example.com, "<strong>\ x 0123456789 abcdef 0123456789 abcdef</strong>", "<strong>\ x 0123456789 abcdeffedcba 9876543210</strong>")<br /> </td> 
  </tr> 
 </tbody> 
</table>

## 집계 {#aggregates}

집계 함수는 [워크플로우의](../../automating/using/query.md#enriching-data) **[!UICONTROL Query]** 활동에서 데이터를 추가하는 경우에만 사용할 수 있습니다.

집계 함수는 값 세트에 대한 계산을 수행하는 데 사용됩니다.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>name</strong><br /> </td> 
   <td> <strong>description</strong><br /> </td> 
   <td> <strong>구문</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>평균</strong>, 평균<br /> </td> 
   <td> 숫자 열의 평균을 반환합니다.<br /> </td> 
   <td> avg (&lt; value &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>카운트</strong>, 카운트 (null 제외)<br /> </td> 
   <td> 열에 null 이 아닌 값을 카운트합니다.<br /> </td> 
   <td> count (&lt; value &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>countall</strong>, count all<br /> </td> 
   <td> 모든 값 (null 값 및 중복 포함) 를 카운트합니다.<br /> </td> 
   <td> countall ()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>countdistinct</strong>, distinct count<br /> </td> 
   <td> 열에서 null 이 아닌 별개의 값을 카운트합니다.<br /> </td> 
   <td> Countdistinct (&lt; value &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>MAX</strong>, MAX<br /> </td> 
   <td> 숫자, 문자열 또는 날짜 열의 최대값을 반환합니다.<br /> </td> 
   <td> MAX (&lt; value &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>최소</strong>, 최소<br /> </td> 
   <td> 숫자, 문자열 또는 날짜 열의 최소값을 반환합니다.<br /> </td> 
   <td> 최소 (&lt; value &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>합계</strong>, 합계<br /> </td> 
   <td> 숫자 열에 있는 값의 합을 반환합니다.<br /> </td> 
   <td> sum (&lt; value &gt;)<br /> </td> 
  </tr> 
 </tbody> 
</table>

## 표현 {#representation}

표현 함수는 값을 정렬하는 데 사용됩니다.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>name</strong><br /> </td> 
   <td> <strong>description</strong><br /> </td> 
   <td> <strong>구문</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>DESC</strong><br /> </td> 
   <td> 내림차순 정렬 적용<br /> </td> 
   <td> desc (&lt; value 1 &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Orderby</strong><br /> </td> 
   <td> 파티션 내의 결과를 정렬합니다.<br /> </td> 
   <td> Orderby (&lt; value 1 &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Partitionby</strong><br /> </td> 
   <td> 테이블에 쿼리 결과를 표시합니다.<br /> </td> 
   <td> Partitionby (&lt; value 1 &gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>rownum</strong><br /> </td> 
   <td> 표 파티션 및 정렬 순서에 따라 행 번호를 생성합니다. 이 함수는 MySQL에서 지원되지 않습니다.<br /> </td> 
   <td> Rownum (partitionby (&lt; value 1 &gt;), orderby (&lt; value 1 &gt;))<br /> </td> 
  </tr> 
 </tbody> 
</table>

