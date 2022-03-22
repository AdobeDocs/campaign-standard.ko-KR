---
title: 데이터 모델 전달
description: 데이터 모델에 대해 알아보기
audience: developing
content-type: reference
feature: Data Model
role: Developer
level: Experienced
exl-id: aea3e72d-8e89-46c7-a796-bf856414c654
source-git-commit: a6471d2970a55373574301fb5d49ee73103fa870
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 13%

---

# 배달(nms:delivery)

## 개체 설명

<table>
               <tr>
                  <th>이름</th>
                  <th>레이블</th>
                  <th>유형(길이)</th>
                  <th>열거형 값</th>
               </tr>
               <tr>
                  <td>FCP</td>
                  <td>증명</td>
                  <td>부울 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>PKey</td>
                  <td>기본 리소스 ID</td>
                  <td>string </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>abTesting</td>
                  <td>A/B 테스트</td>
                  <td>항목 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>고급</td>
                  <td>고급 게재</td>
                  <td>부울 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>advancedParameters</td>
                  <td>고급 매개 변수</td>
                  <td>항목 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>aemContents</td>
                  <td>Adobe Experience Manager 콘텐츠</td>
                  <td>컬렉션 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>alertMessage</td>
                  <td>경고 메시지</td>
                  <td>string </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>alertMode</td>
                  <td>경고 유형</td>
                  <td>string </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>첨부 파일</td>
                  <td>첨부된 파일</td>
                  <td>컬렉션 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>브랜딩(brandingBase)</td>
                  <td>브랜드</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>broadLogs</td>
                  <td>게재 로그</td>
                  <td>컬렉션 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>기본 제공</td>
                  <td>기본 제공 애플리케이션 개체</td>
                  <td>부울 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>campaign (campaignBase)</td>
                  <td>캠페인</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>cmsAccount(extAccountAEMBase)</td>
                  <td>Adobe Experience Manager 계정</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>명령</td>
                  <td>명령</td>
                  <td>항목 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>콘텐츠</td>
                  <td>콘텐츠</td>
                  <td>항목 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>contentSource</td>
                  <td>컨텐츠 소스</td>
                  <td>열거형(바이트) </td>
                  <td>
                     <ul>
                        <li>Adobe Experience Manager - aem - 1</li>
                        <li>Adobe Campaign - 캠페인 - 0</li>
                        <li>잘못된 값 - __Invalid_value__ - __Invalid_value__</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>contextResourceType</td>
                  <td>리소스 유형</td>
                  <td>string </td>
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
                  <td>deliveryMode</td>
                  <td>게재 모드</td>
                  <td>열거형(바이트) </td>
                  <td>
                     <ul>
                        <li>대량 게재 - 벌크 - 1</li>
                        <li>중간 소싱 - 중간 소싱 - 4</li>
                        <li>설명 - 설명 - 2</li>
                        <li>잘못된 값 - __Invalid_value__ - __Invalid_value__</li>
                        <li>외부 - 외부 - 0</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>deliveryProvider(extAccountBase)</td>
                  <td>라우팅</td>
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
                  <td>emailPreview</td>
                  <td>이메일 미리 보기</td>
                  <td>항목 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>excludeLogs</td>
                  <td>제외 로그</td>
                  <td>컬렉션 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>제외</td>
                  <td>제외 원인</td>
                  <td>컬렉션 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>실행</td>
                  <td>게재 실행 매개 변수</td>
                  <td>항목 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>executionType</td>
                  <td>실행 유형</td>
                  <td>열거형(바이트) </td>
                  <td>
                     <ul>
                        <li>고유 - 1회 - 0</li>
                        <li>연속 - 연속 - 1</li>
                        <li>메시지 센터 - 메시지 센터 - 2</li>
                        <li>잘못된 값 - __Invalid_value__ - __Invalid_value__</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>forecastLogs</td>
                  <td>ForecastLog</td>
                  <td>컬렉션 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>geoUnit(geoUnitBase)</td>
                  <td>지리적 단위</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>hasAttachments</td>
                  <td>첨부된 파일 추가</td>
                  <td>부울 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>아이콘</td>
                  <td>아이콘</td>
                  <td>열거형(바이트) </td>
                  <td>
                     <ul>
                        <li>트랜잭션 이메일 - emailLightning - 60</li>
                        <li>팩스 - 팩스 - 4</li>
                        <li>Mobile (SMS) - sms - 1</li>
                        <li>반복 이메일 - e-메일 새로 고침 - 30</li>
                        <li>DM - 용지 - 3</li>
                        <li>전화 - 전화 - 2</li>
                        <li>기타 - 기타 - 120</li>
                        <li>반복 SMS - sms 새로 고침 - 31</li>
                        <li>Mobile 애플리케이션 - pushNotification - 40</li>
                        <li>트랜잭션 SMS - sms 번개 - 61</li>
                        <li>이메일 - 이메일 - 0</li>
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
                  <td>isMaster</td>
                  <td>기본</td>
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
                  <td>반복</td>
                  <td>게재</td>
                  <td>컬렉션 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>작업</td>
                  <td>작업</td>
                  <td>컬렉션 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>jobLogs</td>
                  <td>로그</td>
                  <td>컬렉션 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>kpi</td>
                  <td>지표</td>
                  <td>항목 </td>
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
                  <td>마지막 수정일</td>
                  <td>날짜 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>logicalStatus</td>
                  <td>실행 상태</td>
                  <td>열거형(문자열) (255)</td>
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
                  <td>mailParameters</td>
                  <td>전자 메일 헤더 매개 변수</td>
                  <td>항목 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>mainDate</td>
                  <td>날짜</td>
                  <td>날짜 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>매핑(deliveryMapping)</td>
                  <td>대상 매핑</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>master(deliveryBase)</td>
                  <td>기본 인스턴스</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>masterKpi</td>
                  <td>기본 지표</td>
                  <td>항목 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>messageType</td>
                  <td>채널</td>
                  <td>열거형(바이트) </td>
                  <td>
                     <ul>
                        <li>팩스 - 팩스 - 4</li>
                        <li>Mobile (SMS) - sms - 1</li>
                        <li>이메일 - 이메일 - 0</li>
                        <li>전화 - 전화 - 2</li>
                        <li>DM - 용지 - 3</li>
                        <li>Mobile 애플리케이션 - pushNotification - 40</li>
                        <li>기타 - 기타 - 120</li>
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
                  <td>offerManagement</td>
                  <td>오퍼 관리</td>
                  <td>항목 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>orgUnit(orgUnitBase)</td>
                  <td>조직 단위</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>parent(deliveryBase)</td>
                  <td>상위 게재</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>우선순위</td>
                  <td>게재 우선 순위</td>
                  <td>열거형(바이트) </td>
                  <td>
                     <ul>
                        <li>높음 - 20</li>
                        <li>잘못된 값 - __Invalid_value__ - __Invalid_value__</li>
                        <li>일반 - 일반 - 10</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>프로그램(programBase)</td>
                  <td>프로그램</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>증명</td>
                  <td>증명</td>
                  <td>컬렉션 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>pushNotificationPreview</td>
                  <td>푸시 알림 미리 보기</td>
                  <td>항목 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>pushnotificationParameters</td>
                  <td>PushNotification 매개 변수</td>
                  <td>항목 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>realtimeReport</td>
                  <td>실시간 보고서</td>
                  <td>항목 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>resourceVersion</td>
                  <td>리소스 버전</td>
                  <td>문자열(255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>ribbonMessage</td>
                  <td>리본 메시지</td>
                  <td>string </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>시나리오</td>
                  <td>게재 템플릿 매개 변수</td>
                  <td>항목 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>예약</td>
                  <td>게재 예약</td>
                  <td>항목 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>smsParameters</td>
                  <td>SMS 매개 변수</td>
                  <td>항목 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>smsPreview</td>
                  <td>SMS 미리 보기</td>
                  <td>항목 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>state</td>
                  <td>상태</td>
                  <td>열거형(바이트) </td>
                  <td>
                     <ul>
                        <li>시작 보류 - startPending - 51</li>
                        <li>제공 준비 - 준비 - 45</li>
                        <li>다시 시도 보류 - 다시 시도 보류 중 - 61</li>
                        <li>다시 시도 진행 - retryInProgress - 62</li>
                        <li>실패 - 실패 - 87</li>
                        <li>진행 중 - 시작됨 - 55</li>
                        <li>타깃팅 보류 중 - targetPrepPending - 11</li>
                        <li>Personalization 보류 중 - messagePrepPending - 21</li>
                        <li>일시 중지됨 - 일시 중지됨 - 75</li>
                        <li>편집 - 편집 - 0</li>
                        <li>완료 - 완료 - 95</li>
                        <li>진행 중 카운팅 - targetSelection - 12</li>
                        <li>메시지 완료 - messageReady - 25</li>
                        <li>Personalization 또는 개수 실패 - preparationError - 37</li>
                        <li>중지됨 - 취소됨 - 85</li>
                        <li>Personalization 진행 중 - messagePreparation - 22</li>
                        <li>Target 준비 - targetReady - 15</li>
                        <li>잘못된 값 - __Invalid_value__ - __Invalid_value__</li>
                        <li>중재 진행 중 - targetRe중재 - 13</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>타겟</td>
                  <td>게재 대상 모집단</td>
                  <td>항목 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>템플릿(deliveryTemplateSummary)</td>
                  <td>게재 템플릿</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>축소판</td>
                  <td>게재 축소판</td>
                  <td>문자열(255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>title</td>
                  <td>게재</td>
                  <td>문자열(255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>추적</td>
                  <td>추적 매개 변수</td>
                  <td>항목 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>trackingLogs</td>
                  <td>추적 로그</td>
                  <td>컬렉션 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>trackingUrl</td>
                  <td>추적된 URL</td>
                  <td>컬렉션 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>triggerMessage</td>
                  <td>트랜잭션 메시지의 매개 변수</td>
                  <td>항목 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>유형화(typologyBase)</td>
                  <td>유형화</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>workflow(workflowBase)</td>
                  <td>타겟팅 워크플로우</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>workflowStatus</td>
                  <td>워크플로우 상태</td>
                  <td>열거형(문자열) (255)</td>
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
            </table>

## 필터

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

실행 유형별로(byExecutionType)

<table>
    <tr>
    <th>이름</th>
    <th>유형</th>
    </tr>
    <tr>
    <td>executionType</td>
    <td>열거형</td>
    </tr>
</table>

논리 상태(byLogicalStatus) 기준

<table>
    <tr>
    <th>이름</th>
    <th>유형</th>
    </tr>
    <tr>
    <td>state</td>
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
    <tr>
    <td>mc</td>
    <td>string</td>
    </tr>
</table>

기간별(기간별)

<table>
    <tr>
    <th>이름</th>
    <th>유형</th>
    </tr>
    <tr>
    <td>timePeriod</td>
    <td>string</td>
    </tr>
</table>

기간별(byStartPeriod)

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
    <td>timePeriod</td>
    <td>string</td>
    </tr>
</table>

게시 상태(byPublicationStatus)별

<table>
    <tr>
    <th>이름</th>
    <th>유형</th>
    </tr>
    <tr>
    <td>pStatus</td>
    <td>열거형</td>
    </tr>
</table>

상태 기준(byState)

<table>
    <tr>
    <th>이름</th>
    <th>유형</th>
    </tr>
    <tr>
    <td>state</td>
    <td>열거형</td>
    </tr>
</table>

후속 메시지(showFollowing)

<table>
    <tr>
    <th>이름</th>
    <th>유형</th>
    </tr>
    <tr>
    <td>다음</td>
    <td>부울</td>
    </tr>
</table>

고급 게재 포함(고급 포함)

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

이종 목록에서 연속적인 게재 포함(연속적 포함)

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

증명 포함(FCP 포함)

<table>
    <tr>
    <th>이름</th>
    <th>유형</th>
    </tr>
    <tr>
    <td>withFCP</td>
    <td>부울</td>
    </tr>
</table>

지정된 기간(계획별) 동안 계획됨

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

지정된 기간(달력) 동안 존재함

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

즉시 사용 가능한 항목 표시(showOob)

<table>
    <tr>
    <th>이름</th>
    <th>유형</th>
    </tr>
    <tr>
    <td>ob</td>
    <td>부울</td>
    </tr>
</table>
