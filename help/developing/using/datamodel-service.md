---
title: DataModel
description: 데이터 모델에 대한 자세한 내용
uuid: 99277e46-e4f7-49a9-ba27-b878780f90da
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
discoiquuid: 6e21db35-daf9-4edb-977a-6ef606db0e4d
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c7e83d7d5130ce93b880e4835e634dad03504ebb

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
                  <td>문자열 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>builtIn</td>
                  <td>내장된 애플리케이션 객체</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>created</td>
                  <td>작성일</td>
                  <td>date </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>createdBy(userBase)</td>
                  <td>작성자</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>cusPrice</td>
                  <td>가격</td>
                  <td>정수 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>desk</td>
                  <td>설명</td>
                  <td>문자열(512)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>end</td>
                  <td>종료 날짜</td>
                  <td>date </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>geoUnit(geoUnitBase)</td>
                  <td>지리적 단위</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>history</td>
                  <td>구독 내역</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>isExternal</td>
                  <td>외부 리소스임</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>isTemplate</td>
                  <td>템플릿</td>
                  <td>boolean </td>
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
                  <td>마지막으로 수정한 날짜</td>
                  <td>date </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>limitedDuration</td>
                  <td>제한된 기간</td>
                  <td>boolean </td>
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
                  <td>mode</td>
                  <td>모드</td>
                  <td>열거형(바이트) </td>
                  <td>
                     <ul>
                        <li>입소문 - 입소문 - 1</li>
                        <li>뉴스레터 - 뉴스레터 - 0</li>
                        <li>잘못된 값 - __Invalid_value__ - __Invalid_value__</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>modifiedBy(userBase)</td>
                  <td>수정한 사람</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>name</td>
                  <td>ID</td>
                  <td>문자열(64)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>orgUnit(orgUnitBase)</td>
                  <td>조직 구성 단위</td>
                  <td>link </td>
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
                  <td>date </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>subLandingPage (landingPageSubscriptionBase)</td>
                  <td>구독 랜딩 페이지</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>subScenario(deliveryMCTemplateBase)</td>
                  <td>구독 확인</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>subScenarioEventType</td>
                  <td>SubScenarioEventType</td>
                  <td>문자열 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>구독</td>
                  <td>구독</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>targetResource</td>
                  <td>타깃팅 차원</td>
                  <td>문자열(255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>템플릿(서비스)</td>
                  <td>서비스 템플릿</td>
                  <td>link </td>
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
                  <td>ManigularLandingPage (landingPageUnsubscriptionBase)</td>
                  <td>구독 취소 랜딩 페이지</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>ManigularScenario(deliveryMCTemplateBase)</td>
                  <td>구독 취소 확인</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>MigratorScenarioEventType</td>
                  <td>MigrantScenarioEventType</td>
                  <td>문자열 </td>
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

주어진 기간 동안 사용 가능(계획별)

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

채널 유형별(채널별)

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

이름 또는 레이블별(텍스트별)

<table>
<tr>
<th>이름</th>
<th>유형</th>
</tr>
<tr>
<td>text</td>
<td>문자열</td>
</tr>
</table>

타깃팅 리소스별(TargetResource)

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