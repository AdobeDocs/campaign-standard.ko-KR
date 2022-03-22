---
title: 데이터 모델 프로필
description: 데이터 모델에 대해 알아보기
audience: developing
content-type: reference
feature: Data Model
role: Developer
level: Experienced
exl-id: 652c22a5-7fff-4d08-9396-f0b292aaca76
source-git-commit: a6471d2970a55373574301fb5d49ee73103fa870
workflow-type: tm+mt
source-wordcount: '1249'
ht-degree: 4%

---

# 프로필(nms:recipient)

## 개체 설명

<table>
               <tr>
                  <th>이름</th>
                  <th>레이블</th>
                  <th>유형(길이)</th>
                  <th>열거형 값</th>
               </tr>
               <tr>
                  <td>PKey</td>
                  <td>기본 리소스 ID</td>
                  <td>string </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>연령</td>
                  <td>연령</td>
                  <td>정수 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>appSubscription</td>
                  <td>애플리케이션 구독</td>
                  <td>컬렉션 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>firstDate</td>
                  <td>생년월일</td>
                  <td>날짜 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>blackList</td>
                  <td>더 이상 연락하지 않음(채널별로)</td>
                  <td>부울 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>blackListEmail</td>
                  <td>더 이상 전자 메일로 연락하지 않음</td>
                  <td>부울 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>blackListFax</td>
                  <td>더 이상 팩스로 연락하지 않음</td>
                  <td>부울 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>blackListMobile</td>
                  <td>더 이상 SMS로 연락하지 않습니다.</td>
                  <td>부울 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>blackListPhone</td>
                  <td>더 이상 전화로 연락하지 않음</td>
                  <td>부울 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>blackListPostalMail</td>
                  <td>더 이상 DM으로 연락하지 않음</td>
                  <td>부울 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>blackListPushnotification</td>
                  <td>푸시 알림으로 더 이상 연락하지 않음</td>
                  <td>부울 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>국가(국가)</td>
                  <td>국가</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>생성됨</td>
                  <td>생성됨</td>
                  <td>날짜 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>createdBy(userBase)</td>
                  <td>만든 사람</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>cryptedId</td>
                  <td>암호화된 ID</td>
                  <td>string </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>cusHobbieslink(cusHoblims)</td>
                  <td>CusHobieslink</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>cusLastTransactionDate</td>
                  <td>마지막 트랜잭션 날짜</td>
                  <td>날짜 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>cusTransactionslink</td>
                  <td>트랜잭션</td>
                  <td>컬렉션 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>도메인</td>
                  <td>이메일 도메인</td>
                  <td>문자열(255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>이메일</td>
                  <td>이메일</td>
                  <td>문자열(128)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>emailFormat</td>
                  <td>전자 메일 형식</td>
                  <td>열거형(바이트) </td>
                  <td>
                     <ul>
                        <li>텍스트 - 텍스트 - 1</li>
                        <li>HTML - html - 2</li>
                        <li>잘못된 값 - __Invalid_value__ - __Invalid_value__</li>
                        <li>알 수 없음 - 알 수 없음 - 0</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>emailStatus(addressStatus)</td>
                  <td>전자 메일에 대한 정보</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>excludeLogs</td>
                  <td>제외 로그</td>
                  <td>컬렉션 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>externalId</td>
                  <td>외부 리소스 ID</td>
                  <td>string(100) </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>팩스</td>
                  <td>팩스</td>
                  <td>문자열(32)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>firstName</td>
                  <td>이름</td>
                  <td>문자열(30)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>성별</td>
                  <td>성별</td>
                  <td>열거형(바이트) </td>
                  <td>
                     <ul>
                        <li>지정되지 않음 - 알 수 없음 - 0</li>
                        <li>남성 - 남성 - 1</li>
                        <li>여성 - 여성 - 2</li>
                        <li>잘못된 값 - __Invalid_value__ - __Invalid_value__</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>isExternal</td>
                  <td>외부 리소스임</td>
                  <td>부울 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>lastModified</td>
                  <td>마지막 수정일</td>
                  <td>날짜 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>lastName</td>
                  <td>성</td>
                  <td>문자열(50)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>위치</td>
                  <td>위치</td>
                  <td>항목 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>로그</td>
                  <td>게재 로그</td>
                  <td>컬렉션 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>middleName</td>
                  <td>중간 이름</td>
                  <td>문자열(30)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>mobilePhone</td>
                  <td>모바일</td>
                  <td>문자열(32)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>modifiedBy(userBase)</td>
                  <td>수정자</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>phone</td>
                  <td>전화</td>
                  <td>문자열(32)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>위치</td>
                  <td>위치</td>
                  <td>컬렉션 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>postalAddress</td>
                  <td>우편 주소</td>
                  <td>항목 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>인사말</td>
                  <td>제목</td>
                  <td>문자열(20)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>stateLink (state)</td>
                  <td>주/도</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>subHisto</td>
                  <td>구독 내역</td>
                  <td>컬렉션 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>구독</td>
                  <td>구독</td>
                  <td>컬렉션 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>축소판</td>
                  <td>썸네일</td>
                  <td>문자열(255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>timeZone</td>
                  <td>시간대</td>
                  <td>열거형(문자열) (64)</td>
                  <td>
                     <ul>
                        <li>(GMT-02:00) 중부-대서양 - 대서양_남부_조지아 - 대서양/남부_조지아</li>
                        <li>(GMT+02:00) 암만 - 아시아_암만 - 아시아/암만</li>
                        <li>(GMT-03:00) 브라시 - 아메리카_상파울루 - 아메리카/상파울루</li>
                        <li>(GMT+06:00) 아스타나, 다카 - 아시아_다카 - 아시아/다카</li>
                        <li>(GMT+06:00) 노보시스비르스크 - 아시아_노보시비르스크 - 아시아/노보시비르스크</li>
                        <li>(GMT+02:00) 윈트후크 - 아프리카_윈드후크 - 아프리카/윈드후크</li>
                        <li>(GMT+04:00) 코카서스, 에레반 - 아시아_예레반 - 아시아/예레반</li>
                        <li>(GMT-04:00) 마나우스 - 아메리카_마나우 - 아메리카/마나우스</li>
                        <li>(GMT+03:30) 테헤란 - 아시아_테헤란 - 아시아/테헤란</li>
                        <li>(GMT+12:00) 오클랜드, 웰링턴 - 퍼시픽_오클랜드 - 태평양/오클랜드</li>
                        <li>(GMT+02:00) 예루살렘 - 아시아-예루살렘 - 아시아/예루살렘</li>
                        <li>(GMT+03:00) 모스크바, 상트페테르부르크, 볼고그라드 - 유럽_모스크바 - 유럽/모스크바</li>
                        <li>(GMT+09:30) 아델라이드 - 오스트레일리아_애들레이드 - 오스트레일리아/애들레이드</li>
                        <li>(GMT+10:00) 캔버라, 멜버른, 시드니 - 오스트레일리아_캔버라 - 오스트레일리아/캔버라</li>
                        <li>(GMT+08:00) 퍼스 - 오스트레일리아_퍼스 - 오스트레일리아/퍼스</li>
                        <li>(GMT+09:00) 야쿠츠크 - 아시아_야쿠츠크 - 아시아/야쿠츠크</li>
                        <li>(GMT-10:00) 하와이 - 퍼시픽_호놀룰루 - 태평양/호놀룰루</li>
                        <li>(GMT+04:00) 바쿠 - 아시아-바쿠 - 아시아/바쿠</li>
                        <li>(GMT+10:00) 블라디보스토크 - 아시아_블라디보스토크 - 아시아/블라디보스토크</li>
                        <li>(GMT+09:00) 서울 - 아시아_서울 - 아시아/서울</li>
                        <li>(GMT+01:00) 사라예보, 스코플제, 소피아, 바르샤바, 자그레브 - 유럽_사라예보 - 유럽/사라예보</li>
                        <li>(GMT+04:00) 아부다비, 무스카트 - 아시아_무스카트 - 아시아/무스카트</li>
                        <li>(GMT+08:00) 쿠알라룸푸르, 싱가포르 - 아시아_쿠알라_룸푸르 - 아시아/쿠알라_룸푸르</li>
                        <li>(GMT+09:00) 오사카, 삿포로, 도쿄 - 아시아_도쿄 - 아시아/도쿄</li>
                        <li>(GMT+10:00) 브리즈번 - 오스트레일리아_브리즈번 - 오스트레일리아/브리즈번</li>
                        <li>(GMT+05:30) 스리자야와르데네푸라 - 아시아-콜롬보 - 아시아/콜롬보</li>
                        <li>(GMT+02:00) 하라레, 프레토리아 - 아프리카_하라레 - 아프리카/하라레</li>
                        <li>(GMT+08:00) 울란 바토르 - 아시아_울란_바토르 - 아시아/울란_바토르</li>
                        <li>(GMT-02:00) 그리니치 표준시 - 2시간 - Gmt_m2 - etc/GMT+2</li>
                        <li>(GMT-03:00) 그리니치 표준시 - 3시간 - Gmt_m3 - etc/GMT+3</li>
                        <li>(GMT-01:00) 그리니치 표준시 - 1시간 - Gmt_m1 - etc/GMT+1</li>
                        <li>(GMT-06:00) 그리니치 표준시 - 6시간 - Gmt_m6 - etc/GMT+6</li>
                        <li>(GMT-07:00) 그리니치 표준시 - 7시간 - Gmt_m7 - etc/GMT+7</li>
                        <li>(GMT-04:00) 그리니치 표준시 - 4시간 - Gmt_m4 - etc/GMT+4</li>
                        <li>(GMT) 카사블랑카 - 아프리카 카사블랑카 - 아프리카/카사블랑카</li>
                        <li>(GMT+05:30) 콜카타, 첸나이, 뭄바이, 뉴델리 - 아시아_콜카타 - 아시아/콜카타</li>
                        <li>(GMT-11:00) 그리니치 표준시 - 11시간 - Gmt_m11 - etc/GMT+11</li>
                        <li>(GMT-09:00) 그리니치 표준시 - 9시간 - Gmt_m9 - etc/GMT+9</li>
                        <li>(GMT-03:30) 뉴펀들랜드 - 아메리카_세인트 존스 - 아메리카/세인트 존스</li>
                        <li>(GMT+03:00) 그리니치 표준시 + 3시간 - Gmt_p3 - etc/GMT-3</li>
                        <li>(GMT-04:30) 카라카스 - 아메리카_카라카스 - 아메리카/카라카스</li>
                        <li>(GMT+01:00) 암스테르담, 베를린, 베르네, 로마, 스톡홀름 - 비엔나 - 유럽_베를린 - 유럽/베를린</li>
                        <li>(GMT-07:00) 치와와, 라파스, 마사틀란 - 아메리카_치와와 - 아메리카/치와와</li>
                        <li>(GMT+03:00) 나이로비 - 아프리카_나이로비 - 아프리카/나이로비</li>
                        <li>(GMT-04:00) 아순시온 - 아메리카_아순시온 - 아메리카/아순시온</li>
                        <li>(GMT+03:00) 바그다드 - 아시아_바그다드 - 아시아/바그다드</li>
                        <li>(GMT-10:00) 그리니치 표준시 - 10시간 - Gmt_m10 - 기타/GMT+10</li>
                        <li>(GMT-03:00) 그린란드 - 아메리카_고드탭 - 아메리카/고드탭</li>
                        <li>(GMT+02:00) 다마 - 아시아_다마스쿠스 - 아시아/다마스쿠스</li>
                        <li>(GMT-11:00) 사모아 - 태평양 사모아 - 태평양/사모아</li>
                        <li>(GMT-05:00) 보고타, 리마, 퀴토 - 아메리카_보고타 - 아메리카/보고타</li>
                        <li>(GMT+01:00) 브뤼셀, 코펜하겐, 마드리드, 파리 - 유럽_파리 - 유럽/파리</li>
                        <li>(GMT+08:00) 베이징, 충칭, 홍콩, 우루무치 - 아시아_상하이 - 아시아/상하이</li>
                        <li>(GMT+12:00) 피지 - 태평양 피지 - 태평양/피지</li>
                        <li>(GMT+02:00) 아테네, 이스탄불, 민스크 - 유럽_아테네 - 유럽/아테네</li>
                        <li>(GMT+04:00) 트빌리시 - 아시아_트빌리시 - 아시아/트빌리시</li>
                        <li>잘못된 값 - __Invalid_value__ - __Invalid_value__</li>
                        <li>(GMT+05:45) 카트만두 - 아시아-카트만두 - 아시아/카트만두</li>
                        <li>(GMT-05:00) 인디애나(동부) - 아메리카_인디애나폴리스 - 아메리카/인디애나폴리스</li>
                        <li>(GMT-01:00) 카보베르데 제도 - 애틀랜틱_케이프_베르데 - 대서양/케이프_베르데</li>
                        <li>(GMT+04:00) 포트루이스 - 인디언_모리셔스 - 인도/모리셔스</li>
                        <li>(GMT+08:00) 타이베이 - 아시아_타이베이 - 아시아/타이베이</li>
                        <li>(GMT+06:30) 랑군 - 아시아_랑군 - 아시아/랑군</li>
                        <li>(GMT+11:00) 마가단, 솔로몬 제도, 뉴칼레도니아 - 태평양 과달카날 - 태평양/과달카날</li>
                        <li>(GMT+02:00) 카이로 - 아프리카_카이로 - 아프리카/카이로</li>
                        <li>(GMT+05:00) 이어카테린부르크 - 아시아_예카테린부르크 - 아시아/예카테린부르크</li>
                        <li>(GMT+08:00) 이쿠츠크 - 아시아_이르쿠츠크 - 아시아/이르쿠츠크</li>
                        <li>(GMT+10:00) 구안, 포트 모레스비 - 태평양/구안</li>
                        <li>(GMT-04:00) 대서양 표준시(캐나다) - 아메리카_핼리팩스 - 아메리카/핼리팩스</li>
                        <li>(GMT) 그리니치 표준시 - GMT - GMT</li>
                        <li>기본값 - 없음 - 없음</li>
                        <li>(GMT-04:00) 라파스 - 아메리카_라_파즈 - 아메리카/라_파즈</li>
                        <li>(GMT-06:00) 과달라하라, 멕시코, 몬테레이 - 아메리카_멕시코_시티 - 아메리카/멕시코_시티</li>
                        <li>(GMT+09:30) 다윈 - 오스트레일리아_다윈 - 오스트레일리아/다윈</li>
                        <li>(GMT-05:00) est(미국 및 캐나다) - America_New_York - 미국/뉴욕</li>
                        <li>(GMT-05:00) 그리니치 표준시 - 5시간 - Gmt_m5 - etc/GMT+5</li>
                        <li>(GMT+05:00) 이슬라마바드, 카라치, 타칭트 - 아시아_카라치 - 아시아/카라치</li>
                        <li>(GMT+03:00) 코웨이트, 리야드 - 아시아_리야드 - 아시아/리야드</li>
                        <li>(GMT-08:00) 그리니치 표준시 - 8시간 - Gmt_m8 - 기타/GMT+8</li>
                        <li>(GMT-01:00) 아조레스 - 대서양_아조레스 - 대서양/아조레스</li>
                        <li>(GMT+07:00) 방콕, 하노이, 자카르타 - 아시아_방콕 - 아시아/방콕</li>
                        <li>(GMT) 모노비아 - 아프리카_모노비아 - 아프리카/몬로비아</li>
                        <li>(GMT-09:00) 알래스카 - 아메리카 앵커리지 - 아메리카/앵커리지</li>
                        <li>(GMT+01:00) 베오그라드, 브라티슬라바, 부다페스트, 류블랴나, 프라하 - 유럽_베오그라드 - 유럽/베오그라드</li>
                        <li>(GMT) 레이키야비크 - 애틀랜틱_레이키야비크 - 애틀랜틱/레이키야비크</li>
                        <li>(GMT+02:00) 부카레스트 - 유럽_부카레스트 - 유럽/부카레스트</li>
                        <li>(GMT+05:00) 그리니치 표준시 + 5시간 - Gmt_p5 - etc/GMT-5</li>
                        <li>(GMT+04:00) 그리니치 표준시 + 4시간 - Gmt_p4 - etc/GMT-4</li>
                        <li>(GMT+07:00) 그리니치 표준시 + 7시간 - Gmt_p7 - etc/GMT-7</li>
                        <li>(GMT+06:00) 그리니치 표준시 + 6시간 - Gmt_p6 - etc/GMT-6</li>
                        <li>(GMT+01:00) 그리니치 표준시 + 1시간 - Gmt_p1 - 기타/GMT-1</li>
                        <li>(GMT-08:00) 태평양(미국 및 캐나다) - 아메리카_로스앤젤레스 - 아메리카/로스앤젤레스</li>
                        <li>(GMT+02:00) 그리니치 표준시 + 2시간 - Gmt_p2 - etc/GMT-2</li>
                        <li>(GMT+07:00) 크라스노아르스크 - 아시아_크라스노야르스크 - 아시아/크라스노야르스크</li>
                        <li>(GMT+09:00) 그리니치 표준시 + 9시간 - Gmt_p9 - etc/GMT-9</li>
                        <li>(GMT+08:00) 그리니치 표준시 + 8시간 - Gmt_p8 - 기타/GMT-8</li>
                        <li>(GMT+10:00) 호바트 - 오스트레일리아_호바트 - 오스트레일리아/호바트</li>
                        <li>(GMT+13:00) 누쿠알로파 - 퍼시픽_통가타푸 - 태평양/통가타푸</li>
                        <li>(GMT-06:00) 중앙 아메리카 - 아메리카_레지나 - 아메리카/레지나</li>
                        <li>(GMT-03:00) 부에노스아이레스, 카이엔, 포르탈레자 - 아메리카_부에노스아이레스 - 아메리카/부에노스아이레스</li>
                        <li>(GMT-07:00) 록키 산맥(미국 및 캐나다) - 아메리카_덴버 - 아메리카/덴버</li>
                        <li>(GMT+01:00) 중앙 아프리카 - 서부 - 아프리카_루란다 - 아프리카/루란다</li>
                        <li>(GMT+02:00) 헬싱키, 키예프, 리가, 소피아, 탈린, 빌뉴스 - 유럽_헬싱키 - 유럽/헬싱키</li>
                        <li>(GMT) 그리니치 표준시: 더블린, 에딘버러, 리스본, 런던 - 유럽_런던 - 유럽/런던</li>
                        <li>(GMT-07:00) 애리조나 - 아메리카 피닉스 - 아메리카/피닉스</li>
                        <li>(GMT+02:00) 베이루트 - 아시아_베이루트 - 아시아/베이루트</li>
                        <li>(GMT+04:30) 카불 - 아시아_카불 - 아시아/카불</li>
                        <li>(GMT-06:00) 센터(미국 및 캐나다) - 아메리카_시카고 - 아메리카/시카고</li>
                        <li>(GMT+11:00) 그리니치 표준시 + 11시간 - Gmt_p11 - etc/GMT-11</li>
                        <li>(GMT+10:00) 그리니치 표준시 + 10시간 - Gmt_p10 - etc/GMT-10</li>
                        <li>(GMT+13:00) 그리니치 표준시 + 13시간 - Gmt_p13 - etc/GMT-13</li>
                        <li>(GMT+12:00) 그리니치 표준시 + 12시간 - Gmt_p12 - etc/GMT-12</li>
                        <li>(GMT-04:00) 산티아고 - 아메리카_산티아고 - 아메리카/산티아고</li>
                        <li>(GMT-03:00) 몬테비디오 - 아메리카_몬테비디오 - 아메리카/몬테비디오</li>
                        <li>(GMT-04:00) 쿠이아바 - 아메리카_쿠이아바바 - 아메리카/쿠이아바바</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>title</td>
                  <td>프로필</td>
                  <td>문자열(255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>추적</td>
                  <td>추적 로그</td>
                  <td>컬렉션 </td>
                  <td> </td>
               </tr>
            </table>


## 필터


생일(생일)

<table>
<tr>
<th>이름</th>
<th>유형</th>
</tr>
<tr>
<td>includeStart</td>
<td>부울</td>
</tr>
<tr>
<td>previousUnitsValue</td>
<td>정수</td>
</tr>
<tr>
<td>nextUnitsValue</td>
<td>정수</td>
</tr>
<tr>
<td>endDay</td>
<td>날짜</td>
</tr>
<tr>
<td>정밀도</td>
<td>열거형</td>
</tr>
<tr>
<td>relativeValue</td>
<td>string</td>
</tr>
<tr>
<td>월</td>
<td>날짜</td>
</tr>
<tr>
<td>연산자</td>
<td>열거형</td>
</tr>
<tr>
<td>includeEnd</td>
<td>부울</td>
</tr>
<tr>
<td>endMonth</td>
<td>날짜</td>
</tr>
<tr>
<td>유형</td>
<td>열거형</td>
</tr>
<tr>
<td>일</td>
<td>날짜</td>
</tr>
</table>

전자 메일(byEmail)

<table>
<tr>
<th>이름</th>
<th>유형</th>
</tr>
<tr>
<td>이메일</td>
<td>string</td>
</tr>
</table>

키 기준(byKeysProfile)

<table>
<tr>
<th>이름</th>
<th>유형</th>
</tr>
<tr>
<td>이메일</td>
<td>string</td>
</tr>
</table>

이름 또는 이메일(byText)

<table>
<tr>
<th>이름</th>
<th>유형</th>
</tr>
<tr>
<td>텍스트</td>
<td>string</td>
</tr>
</table>

정적 대상(byStaticAudience)별

<table>
<tr>
<th>이름</th>
<th>유형</th>
</tr>
<tr>
<td>대상자</td>
<td>링크</td>
</tr>
</table>

클릭됨(hasClickedDelivery)

<table>
<tr>
<th>이름</th>
<th>유형</th>
</tr>
<tr>
<td>게재</td>
<td>링크</td>
</tr>
</table>

열림(hasOpenDelivery)

<table>
<tr>
<th>이름</th>
<th>유형</th>
</tr>
<tr>
<td>게재</td>
<td>링크</td>
</tr>
</table>

프로필(프로필)

<table>
<tr>
<th>이름</th>
<th>유형</th>
</tr>
<tr>
<td>프로필</td>
<td>링크</td>
</tr>
</table>

Received(hasReceivedDelivery)

<table>
<tr>
<th>이름</th>
<th>유형</th>
</tr>
<tr>
<td>게재</td>
<td>링크</td>
</tr>
</table>

구독자(구독자)

<table>
<tr>
<th>이름</th>
<th>유형</th>
</tr>
<tr>
<td>서비스</td>
<td>링크</td>
</tr>
</table>
