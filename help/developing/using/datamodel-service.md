---
title: 데이터 모델
description: 데이터 모델에 대해 알아보기
audience: developing
content-type: reference
feature: Data Model
role: Developer
level: Experienced
exl-id: a326b38f-ca88-4a44-a7c2-b6e34497a364
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 7%

---

# 서비스(nms:service)

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
                  <td>기본 제공</td>
                  <td>기본 제공 애플리케이션 개체</td>
                  <td>부울 </td>
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
                  <td>작성자</td>
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
                  <td>end</td>
                  <td>종료 날짜</td>
                  <td>날짜 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>geoUnit(geoUnitBase)</td>
                  <td>지리 단위</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>역사</td>
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
                  <td>label</td>
                  <td>레이블</td>
                  <td>문자열(128)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>lastModified</td>
                  <td>마지막 수정 날짜</td>
                  <td>날짜 </td>
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
                  <td>날짜</td>
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
                        <li>바이러스 - 바이러스 - 1</li>
                        <li>뉴스레터 - 뉴스레터 - 0</li>
                        <li>잘못된 값 - __Invalid_value__ - __Invalid_value__</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>modifiedBy(userBase)</td>
                  <td>수정한 사람</td>
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
                  <td>조직 단위</td>
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
                  <td>start</td>
                  <td>시작 날짜</td>
                  <td>날짜 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>subLandingPage (landingPageSubscriptionBase)</td>
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
                  <td>subScenarioEventType</td>
                  <td>SubScenarioEventType</td>
                  <td>string </td>
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
                  <td>축소판</td>
                  <td>문자열(255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>title</td>
                  <td>서비스</td>
                  <td>문자열(255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>UnlightlandingPage (landingPageUnsubscriptionBase)</td>
                  <td>구독 취소 랜딩 페이지</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>PurchaseScenario(deliveryMCTemplateBase)</td>
                  <td>구독 취소 확인</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>PurchaseScenarioEventType</td>
                  <td>PurchaseScenarioEventType</td>
                  <td>string </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>validityDuration</td>
                  <td>유효 기간</td>
                  <td>number </td>
                  <td> </td>
               </tr>
            </table>

## 필터

지정된 기간(계획별) 동안 사용 가능

<table>
    <tr>
    <th>이름</th>
    <th>유형</th>
    </tr>
    <tr>
    <td>startDate</td>
    <td>날짜</td>
    </tr>
    <tr>
    <td>endDate</td>
    <td>날짜</td>
    </tr>
</table>

채널 유형별로(채널별로)

<table>
<tr>
<th>이름</th>
<th>유형</th>
</tr>
<tr>
<td>channel</td>
<td>열거형</td>
</tr>
</table>

이름 또는 레이블별(byText)

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

타겟팅 리소스(byTargetResource)별

<table>
<tr>
<th>이름</th>
<th>유형</th>
</tr>
<tr>
<td>targetResource</td>
<td>string</td>
</tr>
</table>
