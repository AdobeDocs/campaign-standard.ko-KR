---
title: DataModel 서비스
description: 데이터 모델에 대해 알아보기
audience: developing
content-type: reference
feature: Data Model
role: Developer
level: Experienced
exl-id: a326b38f-ca88-4a44-a7c2-b6e34497a364
source-git-commit: a6471d2970a55373574301fb5d49ee73103fa870
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 39%

---

# 서비스(nms:service)

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
                  <td>기본 제공</td>
                  <td>기본 제공 애플리케이션 오브젝트</td>
                  <td>부울 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>생성됨</td>
                  <td>생성일</td>
                  <td>일자 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>createdBy (userBase)</td>
                  <td>제작자</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>cusPrice</td>
                  <td>가격</td>
                  <td>정수 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>desc</td>
                  <td>설명</td>
                  <td>문자열(512)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>종료</td>
                  <td>종료 일자</td>
                  <td>일자 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>geoUnit(geoUnitBase)</td>
                  <td>지리적 단위</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>history</td>
                  <td>구독 내역</td>
                  <td>컬렉션 </td>
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
                  <td>레이블</td>
                  <td>레이블</td>
                  <td>문자열(128)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>마지막 수정일</td>
                  <td>마지막 수정일</td>
                  <td>일자 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>limitedDuration</td>
                  <td>제한된 기간</td>
                  <td>부울 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>mainDate</td>
                  <td>일자</td>
                  <td>날짜(255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>messageType</td>
                  <td>채널</td>
                  <td>열거형(바이트) </td>
                  <td>
                     <ul>
                        <li>모바일(SMS) - sms - 1</li>
                        <li>이메일 - 이메일 - 0</li>
                        <li>잘못된 값 - __Invalid_value__ - __Invalid_value__</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>모드</td>
                  <td>모드</td>
                  <td>열거형(바이트) </td>
                  <td>
                     <ul>
                        <li>바이럴 - 바이럴 - 1</li>
                        <li>뉴스레터 - 뉴스레터 - 0</li>
                        <li>잘못된 값 - __Invalid_value__ - __Invalid_value__</li>
                     </ul>
                  </td>
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
                  <td>publicLabel</td>
                  <td>서비스 레이블</td>
                  <td>문자열(128)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>시작</td>
                  <td>시작 일자</td>
                  <td>일자 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>subLandingPage(landingPageSubscriptionBase)</td>
                  <td>구독 랜딩 페이지</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>subScenario(deliveryMCTemplateBase)</td>
                  <td>구독 확인</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>subSceneEventType</td>
                  <td>하위 시나리오 이벤트 유형</td>
                  <td>문자열 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>구독</td>
                  <td>구독</td>
                  <td>컬렉션 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>targetResource</td>
                  <td>타겟팅 차원</td>
                  <td>문자열(255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>템플릿(서비스)</td>
                  <td>서비스 템플릿</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>축소판</td>
                  <td>썸네일</td>
                  <td>문자열(255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>제목</td>
                  <td>서비스</td>
                  <td>문자열(255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>unsubLandingPage (landingPageUnsubscriptionBase)</td>
                  <td>구독 취소 랜딩 페이지</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>unsubScenario (deliveryMCTemplateBase)</td>
                  <td>구독 취소 확인</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>unsubScenarEventType</td>
                  <td>UnsubScenarEventType</td>
                  <td>문자열 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>validityDuration</td>
                  <td>유효 기간</td>
                  <td>번호 </td>
                  <td> </td>
               </tr>
            </table>

## 필터

지정된 기간 동안 사용 가능(byPlanning)

<table>
    <tr>
    <th>이름</th>
    <th>유형</th>
    </tr>
    <tr>
    <td>startDate</td>
    <td>일자</td>
    </tr>
    <tr>
    <td>endDate</td>
    <td>일자</td>
    </tr>
</table>

채널 유형별(byChannel)

<table>
<tr>
<th>이름</th>
<th>유형</th>
</tr>
<tr>
<td>channel</td>
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
