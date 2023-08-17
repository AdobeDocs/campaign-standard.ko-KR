---
title: 데이터 모델 랜딩 페이지
description: 데이터 모델에 대해 알아보기
audience: designing
content-type: reference
topic-tags: editing-sms-and-push-content
context-tags: delivery,smsContent,back
feature: Data Model
role: Developer
level: Experienced
exl-id: bd12a214-5998-4fb9-9f54-0c886067b58b
source-git-commit: a6471d2970a55373574301fb5d49ee73103fa870
workflow-type: tm+mt
source-wordcount: '1728'
ht-degree: 8%

---

# 랜딩 페이지(nms:landingPage)

## 개체 설명

<table>
      <tr>
         <th>이름</th>
         <th>레이블</th>
         <th>유형(길이)</th>
         <th>열거 값</th>
      </tr>
      <tr>
         <td>PKey</td>
         <td>기본 리소스 ID</td>
         <td>문자열 </td>
         <td> </td>
      </tr>
      <tr>
         <td>additionalData</td>
         <td>추가 데이터</td>
         <td>컬렉션 </td>
         <td> </td>
      </tr>
      <tr>
         <td>additionalLanguage</td>
         <td>기타 언어</td>
         <td>항목 </td>
         <td> </td>
      </tr>
      <tr>
         <td>allowNonIdentifiedTarget</td>
         <td>미확인 방문자 승인</td>
         <td>부울 </td>
         <td> </td>
      </tr>
      <tr>
         <td>브랜딩(brandingBase)</td>
         <td>브랜드</td>
         <td>링크 </td>
         <td> </td>
      </tr>
      <tr>
         <td>기본 제공</td>
         <td>기본 제공 애플리케이션 오브젝트</td>
         <td>부울 </td>
         <td> </td>
      </tr>
      <tr>
         <td>cache</td>
         <td>캐시</td>
         <td>문자열 </td>
         <td> </td>
      </tr>
      <tr>
         <td>campaign(campaignBase)</td>
         <td>캠페인</td>
         <td>링크 </td>
         <td> </td>
      </tr>
      <tr>
         <td>closedLog</td>
         <td>'랜딩 페이지 닫힘' 로그</td>
         <td>문자열 </td>
         <td> </td>
      </tr>
      <tr>
         <td>contextResourceType</td>
         <td>ContextResourceType</td>
         <td>문자열 </td>
         <td> </td>
      </tr>
      <tr>
         <td>생성됨</td>
         <td>제작일</td>
         <td>date </td>
         <td> </td>
      </tr>
      <tr>
         <td>createdBy (userBase)</td>
         <td>제작자</td>
         <td>링크 </td>
         <td> </td>
      </tr>
      <tr>
         <td>cryptKey</td>
         <td>AES 암호화 키</td>
         <td>문자열(64)</td>
         <td> </td>
      </tr>
      <tr>
         <td>defaultLanguage</td>
         <td>기본 언어</td>
         <td>열거형(문자열)(255)</td>
         <td>
            <ul>
               <li>그리스어 - 엘 - 엘</li>
               <li>영어 - en - en</li>
               <li>중국어 - zh - zh</li>
               <li>프랑스어(프랑스) - fr_FR - fr_FR</li>
               <li>베트남어 - vi - vi</li>
               <li>포르투갈어(포르투갈) - pt_PT - pt_PT</li>
               <li>이탈리아어(이탈리아) - it_IT - it_IT</li>
               <li>이탈리아어 - it - it</li>
               <li>네덜란드어(벨기에) - nl_BE - nl_BE</li>
               <li>노르웨이어(노르웨이) - no_NO - no_NO</li>
               <li>네덜란드어(네덜란드) - nl_NL - nl_NL</li>
               <li>아랍어 - ar - ar</li>
               <li>영어(미국) - en_US - en_US</li>
               <li>아일랜드어 - ga - ga</li>
               <li>체코어 - cs - cs</li>
               <li>에스토니아어 - et - et</li>
               <li>인도네시아어 - id - id</li>
               <li>스페인어 - es - es</li>
               <li>러시아 - ru - ru</li>
               <li>네덜란드어 - nl - nl</li>
               <li>왈롱 - wa - wa</li>
               <li>포르투갈어 - pt - pt</li>
               <li>프랑스어(벨기에) - fr_BE - fr_BE</li>
               <li>라트비아어 - lv - lv</li>
               <li>리투아니아어 - lt - lt</li>
               <li>태국어 - 목 - 목</li>
               <li>영어(영국) - en_GB - en_GB</li>
               <li>프랑스어 - fr - fr</li>
               <li>포르투갈어(브라질) - pt_BR - pt_BR</li>
               <li>독일어 - de - de</li>
               <li>덴마크어 - da - da</li>
               <li>핀란드어 - fi - fi</li>
               <li>헝가리어 - hu - hu</li>
               <li>스웨덴어(핀란드) - sv_FI - sv_FI</li>
               <li>일본어 - ja - ja</li>
               <li>히브리어 - 그</li>
               <li>한국어 - ko - ko</li>
               <li>스웨덴어 - sv</li>
               <li>스웨덴 (스웨덴어) - sv_SE - sv_SE</li>
               <li>슬로바키아어 - sk - sk</li>
               <li>몰타어 - mt - mt</li>
               <li>이탈리아어(스위스) - it_CH - it_CH</li>
               <li>폴란드어 - pl - pl</li>
               <li>슬로베니아 - sl - sl</li>
               <li>잘못된 값 - __Invalid_value__ - __Invalid_value__</li>
            </ul>
         </td>
      </tr>
      <tr>
         <td>defaultOrigin(게재)</td>
         <td>트래픽 소스</td>
         <td>링크 </td>
         <td> </td>
      </tr>
      <tr>
         <td>desc</td>
         <td>설명</td>
         <td>문자열(512)</td>
         <td> </td>
      </tr>
      <tr>
         <td>designLanguage</td>
         <td>디자인 언어</td>
         <td>열거형(문자열)(255)</td>
         <td>
            <ul>
               <li>그리스어 - 엘 - 엘</li>
               <li>영어 - en - en</li>
               <li>중국어 - zh - zh</li>
               <li>프랑스어(프랑스) - fr_FR - fr_FR</li>
               <li>베트남어 - vi - vi</li>
               <li>포르투갈어(포르투갈) - pt_PT - pt_PT</li>
               <li>이탈리아어(이탈리아) - it_IT - it_IT</li>
               <li>이탈리아어 - it - it</li>
               <li>네덜란드어(벨기에) - nl_BE - nl_BE</li>
               <li>노르웨이어(노르웨이) - no_NO - no_NO</li>
               <li>네덜란드어(네덜란드) - nl_NL - nl_NL</li>
               <li>아랍어 - ar - ar</li>
               <li>영어(미국) - en_US - en_US</li>
               <li>아일랜드어 - ga - ga</li>
               <li>체코어 - cs - cs</li>
               <li>에스토니아어 - et - et</li>
               <li>인도네시아어 - id - id</li>
               <li>스페인어 - es - es</li>
               <li>러시아 - ru - ru</li>
               <li>네덜란드어 - nl - nl</li>
               <li>왈롱 - wa - wa</li>
               <li>포르투갈어 - pt - pt</li>
               <li>프랑스어(벨기에) - fr_BE - fr_BE</li>
               <li>라트비아어 - lv - lv</li>
               <li>리투아니아어 - lt - lt</li>
               <li>태국어 - 목 - 목</li>
               <li>영어(영국) - en_GB - en_GB</li>
               <li>프랑스어 - fr - fr</li>
               <li>포르투갈어(브라질) - pt_BR - pt_BR</li>
               <li>독일어 - de - de</li>
               <li>덴마크어 - da - da</li>
               <li>핀란드어 - fi - fi</li>
               <li>헝가리어 - hu - hu</li>
               <li>스웨덴어(핀란드) - sv_FI - sv_FI</li>
               <li>일본어 - ja - ja</li>
               <li>히브리어 - 그</li>
               <li>한국어 - ko - ko</li>
               <li>스웨덴어 - sv</li>
               <li>스웨덴 (스웨덴어) - sv_SE - sv_SE</li>
               <li>슬로바키아어 - sk - sk</li>
               <li>몰타어 - mt - mt</li>
               <li>이탈리아어(스위스) - it_CH - it_CH</li>
               <li>폴란드어 - pl - pl</li>
               <li>슬로베니아 - sl - sl</li>
               <li>잘못된 값 - __Invalid_value__ - __Invalid_value__</li>
            </ul>
         </td>
      </tr>
      <tr>
         <td>dynamicService</td>
         <td>다이내믹 서비스</td>
         <td>부울 </td>
         <td> </td>
      </tr>
      <tr>
         <td>종료</td>
         <td>만료일</td>
         <td>date </td>
         <td> </td>
      </tr>
      <tr>
         <td>errorContextResourceType</td>
         <td>ErrorContextResourceType</td>
         <td>문자열 </td>
         <td> </td>
      </tr>
      <tr>
         <td>errorPage</td>
         <td>오류 페이지</td>
         <td>항목 </td>
         <td> </td>
      </tr>
      <tr>
         <td>geoUnit(geoUnitBase)</td>
         <td>지리적 단위</td>
         <td>링크 </td>
         <td> </td>
      </tr>
      <tr>
         <td>htmlPage</td>
         <td>페이지</td>
         <td>컬렉션 </td>
         <td> </td>
      </tr>
      <tr>
         <td>identificationByUrlParam</td>
         <td>URL 매개 변수로 식별</td>
         <td>부울 </td>
         <td> </td>
      </tr>
      <tr>
         <td>inactiveUrlRedirection</td>
         <td>리디렉션 URL</td>
         <td>문자열(4096)</td>
         <td> </td>
      </tr>
      <tr>
         <td>isExternal</td>
         <td>외부 리소스임</td>
         <td>부울 </td>
         <td> </td>
      </tr>
      <tr>
         <td>isTemplate</td>
         <td>템플릿</td>
         <td>부울 </td>
         <td> </td>
      </tr>
      <tr>
         <td>작업</td>
         <td>작업</td>
         <td>컬렉션 </td>
         <td> </td>
      </tr>
      <tr>
         <td>작업 로그</td>
         <td>로그</td>
         <td>컬렉션 </td>
         <td> </td>
      </tr>
      <tr>
         <td>label</td>
         <td>레이블</td>
         <td>문자열(128)</td>
         <td> </td>
      </tr>
      <tr>
         <td>마지막 수정일</td>
         <td>마지막 수정일</td>
         <td>date </td>
         <td> </td>
      </tr>
      <tr>
         <td>loadingFilter(queryFilterBase)</td>
         <td>키 로드 중</td>
         <td>링크 </td>
         <td> </td>
      </tr>
      <tr>
         <td>loadingFilterMapping</td>
         <td>로드 키의 매개 변수</td>
         <td>컬렉션 </td>
         <td> </td>
      </tr>
      <tr>
         <td>logicalStatus</td>
         <td>실행 상태</td>
         <td>열거형(문자열)(255)</td>
         <td>
            <ul>
               <li>진행 중 - 시작됨 - 시작됨</li>
               <li>편집 - 편집 - 편집</li>
               <li>완료됨 - 완료됨 - 완료됨</li>
               <li>경고 - 경고 - 경고</li>
               <li>오류 - 오류 - 오류</li>
               <li>잘못된 값 - __Invalid_value__ - __Invalid_value__</li>
            </ul>
         </td>
      </tr>
      <tr>
         <td>messageAction</td>
         <td>메시지 보내기 시작</td>
         <td>부울 </td>
         <td> </td>
      </tr>
      <tr>
         <td>messageActionDelivery(deliveryMCTemplateBase)</td>
         <td>트랜잭션 메시지</td>
         <td>링크 </td>
         <td> </td>
      </tr>
      <tr>
         <td>modifiedBy(userBase)</td>
         <td>수정자</td>
         <td>링크 </td>
         <td> </td>
      </tr>
      <tr>
         <td>이름</td>
         <td>ID</td>
         <td>문자열(64)</td>
         <td> </td>
      </tr>
      <tr>
         <td>orgUnit(orgUnitBase)</td>
         <td>조직 유닛</td>
         <td>링크 </td>
         <td> </td>
      </tr>
      <tr>
         <td>미리 채우기</td>
         <td>방문자 데이터 미리 로드</td>
         <td>부울 </td>
         <td> </td>
      </tr>
      <tr>
         <td>프로그램(programBase)</td>
         <td>프로그램</td>
         <td>링크 </td>
         <td> </td>
      </tr>
      <tr>
         <td>publicUrl</td>
         <td>공개 URL</td>
         <td>문자열 </td>
         <td> </td>
      </tr>
      <tr>
         <td>발행일</td>
         <td>게시일</td>
         <td>date </td>
         <td> </td>
      </tr>
      <tr>
         <td>조정 필터(queryFilterBase)</td>
         <td>조정 키</td>
         <td>링크 </td>
         <td> </td>
      </tr>
      <tr>
         <td>조정 필터 매핑</td>
         <td>조정 키 매개 변수</td>
         <td>컬렉션 </td>
         <td> </td>
      </tr>
      <tr>
         <td>reconciliationUpdateStrategy</td>
         <td>전략 업데이트</td>
         <td>열거형(바이트) </td>
         <td>
            <ul>
               <li>업데이트 - updateTarget - 1</li>
               <li>승인되지 않음 - 승인되지 않음 - 0</li>
               <li>잘못된 값 - __Invalid_value__ - __Invalid_value__</li>
            </ul>
         </td>
      </tr>
      <tr>
         <td>서비스(serviceBase)</td>
         <td>구독 서비스</td>
         <td>링크 </td>
         <td> </td>
      </tr>
      <tr>
         <td>specificAction</td>
         <td>특정 작업</td>
         <td>열거형(바이트) </td>
         <td>
            <ul>
               <li>블랙리스트 - 블랙리스트 - 3</li>
               <li>특정 작업 없음 - 없음 - 0</li>
               <li>구독 취소 - 구독 취소 - 2</li>
               <li>잘못된 값 - __Invalid_value__ - __Invalid_value__</li>
               <li>구독 - 구독 - 1</li>
            </ul>
         </td>
      </tr>
      <tr>
         <td>시작</td>
         <td>배포일</td>
         <td>date </td>
         <td> </td>
      </tr>
      <tr>
         <td>상태</td>
         <td>상태</td>
         <td>열거형(바이트) </td>
         <td>
            <ul>
               <li>편집 - 편집 - 0</li>
               <li>게시 실패 - 실패 - 99</li>
               <li>닫힘 - 닫힘 - 20</li>
               <li>잘못된 값 - __Invalid_value__ - __Invalid_value__</li>
               <li>온라인 - 열림 - 10</li>
            </ul>
         </td>
      </tr>
      <tr>
         <td>targetResource</td>
         <td>타겟팅 차원</td>
         <td>문자열(255)</td>
         <td> </td>
      </tr>
      <tr>
         <td>템플릿(랜딩 페이지)</td>
         <td>랜딩 페이지 템플릿</td>
         <td>링크 </td>
         <td> </td>
      </tr>
      <tr>
         <td>testUrl</td>
         <td>테스트 URL</td>
         <td>문자열 </td>
         <td> </td>
      </tr>
      <tr>
         <td>축소판</td>
         <td>썸네일</td>
         <td>문자열(255)</td>
         <td> </td>
      </tr>
      <tr>
         <td>시간대</td>
         <td>시간대</td>
         <td>열거형(문자열) (64)</td>
         <td>
            <ul>
               <li>(GMT-02:00) 중앙-대서양 - 대서양_남부_조지아 - 대서양/남부_조지아</li>
               <li>(GMT+02:00) 암만 - 아시아 암만 - 아시아/암만</li>
               <li>(GMT-03:00) 브라시 - 아메리카_상파울루 - 아메리카/상파울루</li>
               <li>(GMT+06:00) 아스타나, 다카 - 아시아 다카 - 아시아/다카</li>
               <li>(GMT+06:00) 노보시비르스크 - 아시아_노보시비르스크 - 아시아/노보시비르스크</li>
               <li>(GMT+02:00) 빈트후크 - 아프리카 빈트후크 - 아프리카/빈트후크</li>
               <li>(GMT+04:00) 코카서스, 에레반 - 아시아_예레반 - 아시아/예레반</li>
               <li>(GMT-04:00) 마노스 - 아메리카 마노스 - 아메리카/마노스</li>
               <li>(GMT+03:30) 테헤란 - 아시아_테헤란 - 아시아/테헤란</li>
               <li>(GMT+12:00) 오클랜드, 웰링턴 - 태평양 오클랜드 - 태평양/오클랜드</li>
               <li>(GMT+02:00) 예루살렘 - 아시아_예루살렘 - 아시아/예루살렘</li>
               <li>(GMT+03:00) 모스크바, 상트페테르부르크, 볼고그라드 - 유럽_모스크바 - 유럽/모스크바</li>
               <li>(GMT+09:30) 아델라이드 - 오스트레일리아 아델라이드 - 오스트레일리아/아델라이드</li>
               <li>(GMT+10:00) 캔버라, 멜버른, 시드니 - 오스트레일리아 캔버라 - 오스트레일리아/캔버라</li>
               <li>(GMT+08:00) 퍼스 - 오스트레일리아_퍼스 - 오스트레일리아/퍼스</li>
               <li>(GMT+09:00) 야쿠츠크 - 아시아 야쿠츠크 - 아시아/야쿠츠크</li>
               <li>(GMT-10:00) 하와이 - 태평양 호놀룰루 - 태평양/호놀룰루</li>
               <li>(GMT+04:00) 바쿠 - 아시아 바쿠 - 아시아/바쿠</li>
               <li>(GMT+10:00) 블라디보스토크 - 아시아_블라디보스토크 - 아시아/블라디보스토크</li>
               <li>(GMT+09:00) 서울 - 아시아_서울 - 아시아/서울</li>
               <li>(GMT+01:00) 사라예보, 스코플레, 소피아, 바르샤바, 자그레브 - 유럽_사라예보 - 유럽/사라예보</li>
               <li>서버 시간대 - _server_ - _server_</li>
               <li>(GMT+04:00) 아부다비, 무스카트 - 아시아_무스카트 - 아시아/무스카트</li>
               <li>(GMT+08:00) 쿠알라룸푸르, 싱가포르 - 아시아_쿠알라룸푸르 - 아시아/쿠알라룸푸르</li>
               <li>(GMT+09:00) 오사카, 삿포로, 도쿄 - 아시아 도쿄 - 아시아/도쿄</li>
               <li>(GMT+10:00) 브리즈번 - 오스트레일리아 브리즈번 - 오스트레일리아/브리즈번</li>
               <li>(GMT+05:30) 스리자야와르데네푸라 - 아시아 콜롬비아 - 아시아/콜롬비아</li>
               <li>(GMT+02:00) 하라레, 프리토리아 - 아프리카_하라레 - 아프리카/하라레</li>
               <li>(GMT+08:00) 오울란바토르 - 아시아_울란바토르 - 아시아/울란바토르</li>
               <li>(GMT-02:00) 그리니치 표준시 마이너스 2시간 - Gmt_m2 - 기타/GMT+2</li>
               <li>(GMT-03:00) 그리니치 표준시 마이너스 3시간 - Gmt_m3 - 기타/GMT+3</li>
               <li>(GMT-01:00) 그리니치 표준시 마이너스 1시간 - Gmt_m1 - 기타/GMT+1</li>
               <li>(GMT-06:00) 그리니치 표준시 마이너스 6시간 - Gmt_m6 - 기타/GMT+6</li>
               <li>(GMT-07:00) 그리니치 표준시 마이너스 7시간 - Gmt_m7 - 기타/GMT+7</li>
               <li>(GMT-04:00) 그리니치 표준시 마이너스 4시간 - Gmt_m4 - 기타/GMT+4</li>
               <li>(GMT) 카사블랑카 - 아프리카_카사블랑카 - 아프리카/카사블랑카</li>
               <li>(GMT+05:30) 콜카타, 첸나이, 뭄바이, 뉴델리 - 아시아-콜카타 - 아시아/콜카타</li>
               <li>(GMT-11:00) 그리니치 표준시 마이너스 11시간 - Gmt_m11 - 기타/GMT+11</li>
               <li>(GMT-09:00) 그리니치 표준시 마이너스 9시간 - Gmt_m9 - 기타/GMT+9</li>
               <li>(GMT-03:30) 뉴펀들랜드 - 아메리카_세인트_존스 - 아메리카/세인트_존스</li>
               <li>기본값 - _inherit_ - _inherit_</li>
               <li>(GMT+03:00) 그리니치 표준시 플러스 3시간 - Gmt_p3 - 기타/GMT-3</li>
               <li>(GMT-04:30) 카라카스 - 아메리카_카라카스 - 아메리카/카라카스</li>
               <li>(GMT+01:00) 암스테르담, 베를린, 베른, 로마, 스톡홀름, 비엔나 - 유럽_베를린 - 유럽/베를린</li>
               <li>(GMT-07:00) 치와와, 라파스, 마사틀란 - 아메리카 치와와 - 아메리카/치와와</li>
               <li>(GMT+03:00) 나이로비 - 아프리카 나이로비 - 아프리카/나이로비</li>
               <li>(GMT-04:00) 아순시온 - 아메리카_아순시온 - 아메리카/아순시온</li>
               <li>(GMT+03:00) 바그다드 - 아시아 바그다드 - 아시아/바그다드</li>
               <li>(GMT-10:00) 그리니치 표준시 마이너스 10시간 - Gmt_m10 - 기타/GMT+10</li>
               <li>(GMT-03:00) 그린란드 - 아메리카_고드호프 - 아메리카/고드호프</li>
               <li>(GMT+02:00) 다마스 - 아시아_다마스쿠스 - 아시아/다마스쿠스</li>
               <li>(GMT-11:00) 사모아 - 태평양 사모아 - 태평양/사모아</li>
               <li>(GMT-05:00) 보고타, 리마, 키토 - 아메리카_보고타 - 아메리카/보고타</li>
               <li>(GMT+01:00) 브뤼셀, 코펜하겐, 마드리드, 파리 - 유럽_파리 - 유럽/파리</li>
               <li>(GMT+08:00) 베이징, 충칭, 홍콩, 우루무치 - 아시아-상하이 - 아시아/상하이</li>
               <li>(GMT+12:00) 피지 - 태평양 피지 - 태평양/피지</li>
               <li>(GMT+02:00) 아테네, 이스탄불, 민스크 - 유럽_아테네 - 유럽/아테네</li>
               <li>(GMT+04:00) 트빌리시 - 아시아_트빌리시 - 아시아/트빌리시</li>
               <li>잘못된 값 - __Invalid_value__ - __Invalid_value__</li>
               <li>(GMT+05:45) 카트만두 - 아시아_카트만두 - 아시아/카트만두</li>
               <li>(GMT-05:00) 인디애나(동부) - 아메리카_인디애나폴리스 - 아메리카/인디애나폴리스</li>
               <li>(GMT-01:00) 카보베르데 제도 - 대서양_카보베르데 - 대서양/카보베르데</li>
               <li>(GMT+04:00) 포트루이스 - 인도령 모리셔스 - 인도령/모리셔스</li>
               <li>(GMT+08:00) 타이베이 - 아시아 타이베이 - 아시아/타이베이</li>
               <li>데이터베이스의 시간대 - _wdbc_ - _wdbc_</li>
               <li>(GMT+06:30) 랑군 - 아시아 랑군 - 아시아/랑군</li>
               <li>(GMT+11:00) 마가단, 솔로몬 제도, 뉴칼레도니아 - 태평양 과달카날 - 태평양/과달카날</li>
               <li>(GMT+02:00) 카이로 - 아프리카 카이로 - 아프리카/카이로</li>
               <li>(GMT+05:00) 이카테린부르크 - 아시아_예카테린부르크 - 아시아/예카테린부르크</li>
               <li>(GMT+08:00) 이르쿠츠크 - 아시아_이르쿠츠크 - 아시아/이르쿠츠크</li>
               <li>(GMT+10:00) 괌, 포트 모르즈비 - 태평양 괌 - 태평양/괌</li>
               <li>(GMT-04:00) 대서양 표준시(캐나다) - 아메리카_핼리팩스 - 아메리카/핼리팩스</li>
               <li>(GMT) 그리니치 표준시 - GMT</li>
               <li>(GMT-04:00) 라파스 - 아메리카_라파스 - 아메리카/라파스</li>
               <li>연산자 시간대 - _login_ - _login_</li>
               <li>(GMT-06:00) 과달라하라, 멕시코, 몬테레이 - 아메리카_멕시코_시티 - 아메리카/멕시코_시티</li>
               <li>(GMT+09:30) 다윈 - 오스트레일리아_다윈 - 오스트레일리아/다윈</li>
               <li>(GMT-05:00) 동부(미국 및 캐나다) - America_New_York - 아메리카/뉴욕</li>
               <li>(GMT-05:00) 그리니치 표준시 마이너스 5시간 - Gmt_m5 - 기타/GMT+5</li>
               <li>(GMT+05:00) 이슬라마바드, 카라치, 타켄트 - 아시아 카라치 - 아시아/카라치</li>
               <li>(GMT+03:00) 코웨이트, 리야드 - 아시아 리야드 - 아시아/리야드</li>
               <li>(GMT-08:00) 그리니치 표준시 마이너스 8시간 - Gmt_m8 - 기타/GMT+8</li>
               <li>(GMT-01:00) 아조레스 - 대서양 아조레스 - 대서양/아조레스</li>
               <li>(GMT+07:00) 방콕, 하노이, 자카르타 - 아시아 방콕 - 아시아/방콕</li>
               <li>(GMT) 몬로비아 - 아프리카_몬로비아 - 아프리카/몬로비아</li>
               <li>(GMT-09:00) 알래스카 - 아메리카_앵커리지 - 아메리카/앵커리지</li>
               <li>(GMT+01:00) 베오그라드, 브라티슬라바, 부다페스트, 류블랴나, 프라하 - 유럽_베오그라드 - 유럽/베오그라드</li>
               <li>(GMT) 레이캬비크 - 대서양 레이캬비크 - 대서양/레이캬비크</li>
               <li>(GMT+02:00) 부카레스트 - 유럽_부카레스트 - 유럽/부카레스트</li>
               <li>(GMT+05:00) 그리니치 표준시 플러스 5시간 - Gmt_p5 - 기타/GMT-5</li>
               <li>(GMT+04:00) 그리니치 표준시 플러스 4시간 - Gmt_p4 - 기타/GMT-4</li>
               <li>(GMT+07:00) 그리니치 표준시 플러스 7시간 - Gmt_p7 - 기타/GMT-7</li>
               <li>(GMT+06:00) 그리니치 표준시 플러스 6시간 - Gmt_p6 - 기타/GMT-6</li>
               <li>(GMT+01:00) 그리니치 표준시 플러스 1시간 - Gmt_p1 - 기타/GMT-1</li>
               <li>(GMT-08:00) 태평양(미국 및 캐나다) - 아메리카_로스앤젤레스 - 아메리카/로스앤젤레스</li>
               <li>(GMT+02:00) 그리니치 표준시 플러스 2시간 - Gmt_p2 - 기타/GMT-2</li>
               <li>(GMT+07:00) 크라스노이아르스크 - 아시아_크라스노야르스크 - 아시아/크라스노야르스크</li>
               <li>(GMT+09:00) 그리니치 표준시 플러스 9시간 - Gmt_p9 - 기타/GMT-9</li>
               <li>(GMT+08:00) 그리니치 표준시 플러스 8시간 - Gmt_p8 - 기타/GMT-8</li>
               <li>(GMT+10:00) 호바트 - 오스트레일리아_호바트 - 오스트레일리아/호바트</li>
               <li>(GMT+13:00) 누쿠알로파 - 태평양 통가타푸 - 태평양/통가타푸</li>
               <li>(GMT-06:00) 중앙 아메리카 - 아메리카_리자이나 - 아메리카/리자이나</li>
               <li>(GMT-03:00) 부에노스아이레스, 카옌, 포르탈레자 - 아메리카_부에노스아이레스 - 아메리카/부에노스아이레스</li>
               <li>(GMT-07:00) 로키 산맥(미국 및 캐나다) - 아메리카_덴버 - 아메리카/덴버</li>
               <li>(GMT+01:00) 중앙 아프리카 - 서부 - 아프리카_루안다 - 아프리카/루안다</li>
               <li>(GMT+02:00) 헬싱키, 키예프, 리가, 소피아, 탈린, 빌뉴스 - 유럽_헬싱키 - 유럽/헬싱키</li>
               <li>(GMT) 그리니치 표준시: 더블린, 에든버러, 리스본, 런던 - 유럽_런던 - 유럽/런던</li>
               <li>(GMT-07:00) 애리조나 - 아메리카_피닉스 - 아메리카/피닉스</li>
               <li>(GMT+02:00) 베이루트 - 아시아 베이루트 - 아시아/베이루트</li>
               <li>(GMT+04:30) 카불 - 아시아_카불 - 아시아/카불</li>
               <li>(GMT-06:00) 센터(미국 및 캐나다) - 아메리카_시카고 - 아메리카/시카고</li>
               <li>(GMT+11:00) 그리니치 표준시 플러스 11시간 - Gmt_p11 - 기타/GMT-11</li>
               <li>(GMT+10:00) 그리니치 표준시 플러스 10시간 - Gmt_p10 - 기타/GMT-10</li>
               <li>(GMT+13:00) 그리니치 표준시 플러스 13시간 - Gmt_p13 - 기타/GMT-13</li>
               <li>(GMT+12:00) 그리니치 표준시 플러스 12시간 - Gmt_p12 - 기타/GMT-12</li>
               <li>(GMT-04:00) 산티아고 - 아메리카_산티아고 - 아메리카/산티아고</li>
               <li>(GMT-03:00) 몬테비데오 - 아메리카_몬테비데오 - 아메리카/몬테비데</li>
               <li>(GMT-04:00) 쿠이아바 - 아메리카 쿠이아바 - 아메리카/쿠이아바</li>
            </ul>
         </td>
      </tr>
      <tr>
         <td>title</td>
         <td>랜딩 페이지</td>
         <td>문자열(255)</td>
         <td> </td>
      </tr>
      <tr>
         <td>trackingEnable</td>
         <td>로그 응답</td>
         <td>부울 </td>
         <td> </td>
      </tr>
      <tr>
         <td>trackingUrlName</td>
         <td>추적 URL 이름</td>
         <td>문자열 </td>
         <td> </td>
      </tr>
      <tr>
         <td>유형</td>
         <td>유형</td>
         <td>열거형(바이트) </td>
         <td>
            <ul>
               <li>일반 - 일반 - 0</li>
               <li>서비스 구독 취소 - 구독 취소 - 3</li>
               <li>블랙리스트 - 블랙리스트 - 4</li>
               <li>잘못된 값 - __Invalid_value__ - __Invalid_value__</li>
               <li>고객 확보 - 고객 확보 - 1</li>
               <li>서비스 구독 - 구독 - 2</li>
            </ul>
         </td>
      </tr>
      <tr>
         <td>uuid</td>
         <td>보안 ID</td>
         <td>문자열 </td>
         <td> </td>
      </tr>
      <tr>
         <td>webTrackingEnable</td>
         <td>웹 추적 활성화</td>
         <td>부울 </td>
         <td> </td>
      </tr>
   </table>

## 필터

논리 상태별(byLogicalStatus)

<table>
    <tr>
    <th>이름</th>
    <th>유형</th>
    </tr>
    <tr>
    <td>상태</td>
    <td>열거</td>
    </tr>
</table>

이름 또는 레이블 기준(byText)

<table>
    <tr>
    <th>이름</th>
    <th>유형</th>
    </tr>
    <tr>
    <td>텍스트</td>
    <td>문자열</td>
    </tr>
</table>

상태별(byState)

<table>
    <tr>
    <th>이름</th>
    <th>유형</th>
    </tr>
    <tr>
    <td>상태</td>
    <td>열거</td>
    </tr>
</table>

리소스 타겟팅(byTargetResource)

<table>
<tr>
<th>이름</th>
<th>유형</th>
</tr>
<tr>
<td>targetResource</td>
<td>문자열</td>
</tr>
</table>

고급 랜딩 페이지 포함(고급 포함)

<table>
    <tr>
    <th>이름</th>
    <th>유형</th>
    </tr>
    <tr>
    <td>고급</td>
    <td>부울</td>
    </tr>
</table>

다른 유형의 목록에서 연속 게재 포함(withContinuous)

<table>
        <tr>
        <th>이름</th>
        <th>유형</th>
        </tr>
        <tr>
        <td>withContinuous</td>
        <td>부울</td>
        </tr>
    </table>

지정된 기간 동안 표시(byCalendar)

<table>
        <tr>
        <th>이름</th>
        <th>유형</th>
        </tr>
        <tr>
        <td>startDate</td>
        <td>date</td>
        </tr>
        <tr>
        <td>endDate</td>
        <td>date</td>
        </tr>
    </table>

지정된 기간 동안 게시됨(byPlanning)

<table>
    <tr>
    <th>이름</th>
    <th>유형</th>
    </tr>
    <tr>
    <td>startDate</td>
    <td>date</td>
    </tr>
    <tr>
    <td>endDate</td>
    <td>date</td>
    </tr>
</table>
