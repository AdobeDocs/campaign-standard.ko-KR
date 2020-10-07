---
title: DataModel
description: 데이터 모델에 대한 자세한 내용
uuid: 99277e46-e4f7-49a9-ba27-b878780f90da
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
discoiquuid: 6e21db35-daf9-4edb-977a-6ef606db0e4d
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 6%

---


# 배달(nms:배달)

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
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>PKey</td>
                  <td>기본 리소스 ID</td>
                  <td>문자열 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>abTesting</td>
                  <td>A/B 테스트</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>advanced</td>
                  <td>고급 전달</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>advancedParameters</td>
                  <td>고급 매개 변수</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>aemContents</td>
                  <td>Adobe Experience Manager 콘텐츠</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>alertMessage</td>
                  <td>경고 메시지</td>
                  <td>문자열 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>alertMode</td>
                  <td>경고 유형</td>
                  <td>문자열 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>첨부</td>
                  <td>첨부 파일</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>branding(brandingBase)</td>
                  <td>브랜드</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>broadLogs</td>
                  <td>게재 로그</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>builtIn</td>
                  <td>내장된 애플리케이션 객체</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>campaign(campaignBase)</td>
                  <td>캠페인</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>cmsAccount(extAccountAEMBase)</td>
                  <td>Adobe Experience Manager 계정</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>명령</td>
                  <td>명령</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>content</td>
                  <td>컨텐츠</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>contentSource</td>
                  <td>콘텐츠 소스</td>
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
                  <td>문자열 </td>
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
                  <td>deliveryMode</td>
                  <td>배달 모드</td>
                  <td>열거형(바이트) </td>
                  <td>
                     <ul>
                        <li>대량 배달 - 벌크 - 1</li>
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
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>desk</td>
                  <td>설명</td>
                  <td>문자열(512)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>emailPreview</td>
                  <td>이메일 미리 보기</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>excludeLogs</td>
                  <td>제외 로그</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>제외</td>
                  <td>제외 원인</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>실행</td>
                  <td>배달 실행 매개 변수</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>executionType</td>
                  <td>실행 유형</td>
                  <td>열거형(바이트) </td>
                  <td>
                     <ul>
                        <li>고유 - 1Time - 0</li>
                        <li>연속 - 연속 - 1</li>
                        <li>메시지 센터 - 메시지 센터 - 2</li>
                        <li>잘못된 값 - __Invalid_value__ - __Invalid_value__</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>forecastLogs</td>
                  <td>ForecastLog</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>geoUnit(geoUnitBase)</td>
                  <td>지리적 단위</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>hasAttachments</td>
                  <td>첨부 파일 추가</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>아이콘</td>
                  <td>아이콘</td>
                  <td>열거형(바이트) </td>
                  <td>
                     <ul>
                        <li>트랜잭션 이메일 - 이메일 번개 - 60</li>
                        <li>팩스 - 팩스 - 4</li>
                        <li>모바일(SMS) - sms - 1</li>
                        <li>반복 이메일 - 이메일 새로 고침 - 30</li>
                        <li>DM - 종이 - 3</li>
                        <li>전화 - 전화 - 2</li>
                        <li>기타 - 기타 - 120</li>
                        <li>반복 SMS - smsRefresh - 31</li>
                        <li>모바일 애플리케이션 - 푸시 알림 - 40</li>
                        <li>트랜잭션 SMS - smsLightning - 61</li>
                        <li>이메일 - 이메일 - 0</li>
                        <li>잘못된 값 - __Invalid_value__ - __Invalid_value__</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>isExternal</td>
                  <td>외부 리소스임</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>isMaster</td>
                  <td>기본</td>
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
                  <td>반복</td>
                  <td>게재</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>직업</td>
                  <td>Job</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>jobLogs</td>
                  <td>로그</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>까피스</td>
                  <td>지표</td>
                  <td>item </td>
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
                  <td>logicalStatus</td>
                  <td>실행 상태</td>
                  <td>열거형(문자열)(255)</td>
                  <td>
                     <ul>
                        <li>진행 중 - 시작됨 - 시작됨</li>
                        <li>편집 - 에디션 - 에디션</li>
                        <li>완료 - 완료 - 완료</li>
                        <li>경고 - 경고 - 경고</li>
                        <li>오류 - 오류 - 오류</li>
                        <li>잘못된 값 - __Invalid_value__ - __Invalid_value__</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>mailParameters</td>
                  <td>이메일 헤더 매개 변수</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>mainDate</td>
                  <td>날짜</td>
                  <td>date </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>매핑(deliveryMapping)</td>
                  <td>대상 매핑</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>master(deliveryBase)</td>
                  <td>기본 인스턴스</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>masterKpi</td>
                  <td>기본 지표</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>messageType</td>
                  <td>채널</td>
                  <td>열거형(바이트) </td>
                  <td>
                     <ul>
                        <li>팩스 - 팩스 - 4</li>
                        <li>모바일(SMS) - sms - 1</li>
                        <li>이메일 - 이메일 - 0</li>
                        <li>전화 - 전화 - 2</li>
                        <li>DM - 종이 - 3</li>
                        <li>모바일 애플리케이션 - 푸시 알림 - 40</li>
                        <li>기타 - 기타 - 120</li>
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
                  <td>offerManagement</td>
                  <td>오퍼 관리</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>orgUnit(orgUnitBase)</td>
                  <td>조직 단위</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>parent(deliveryBase)</td>
                  <td>상위 배달</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>우선 순위</td>
                  <td>배달 우선 순위</td>
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
                  <td>program(programBase)</td>
                  <td>프로그램</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>교정본</td>
                  <td>교정본</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>pushNotificationPreview</td>
                  <td>푸시 알림 미리 보기</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>pushnotification매개 변수</td>
                  <td>PushNotification 매개 변수</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>realtimeReport</td>
                  <td>실시간 보고서</td>
                  <td>item </td>
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
                  <td>문자열 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>scenario</td>
                  <td>배달 템플릿 매개 변수</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>예약</td>
                  <td>배달 예약</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>smsParameters</td>
                  <td>SMS 매개 변수</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>smsPreview</td>
                  <td>SMS 미리 보기</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>state</td>
                  <td>상태</td>
                  <td>열거형(바이트) </td>
                  <td>
                     <ul>
                        <li>시작 보류 중 - 시작 보류 중 - 51</li>
                        <li>준비 완료 - 45</li>
                        <li>재시도 보류 - 재시도 보류 중 - 61</li>
                        <li>진행 중 다시 시도 - retryInProgress - 62</li>
                        <li>실패 - 실패 - 87</li>
                        <li>진행 중 - 시작됨 - 55</li>
                        <li>타깃팅 보류 중 - targetPrepPending - 11</li>
                        <li>개인화 보류 중 - messagePrepPending - 21</li>
                        <li>일시 중지됨 - 일시 중지됨 - 75</li>
                        <li>편집 - 에디션 - 0</li>
                        <li>완료 - 완료 - 95</li>
                        <li>진행 중 카운팅 - targetSelection - 12</li>
                        <li>메시지 종결 - messageReady - 25</li>
                        <li>개인화 또는 계산 실패 - 준비오류 - 37</li>
                        <li>중지됨 - 취소됨 - 85</li>
                        <li>개인화 진행 중 - messagePreparation - 22</li>
                        <li>Target 준비 - targetReady - 15</li>
                        <li>잘못된 값 - __Invalid_value__ - __Invalid_value__</li>
                        <li>중재 진행 중 - targetArbitration - 13</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>target</td>
                  <td>전달 대상 인구</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>template(deliveryTemplateSummary)</td>
                  <td>배달 템플릿</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>축소판</td>
                  <td>배달 축소판</td>
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
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>trackingLogs</td>
                  <td>추적 로그</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>trackingUrl</td>
                  <td>추적된 URL</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>triggerMessage</td>
                  <td>트랜잭션 메시지의 매개 변수</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>분류(typicalBase)</td>
                  <td>분류</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>workflow(workflowBase)</td>
                  <td>타깃팅 워크플로우</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>workflowStatus</td>
                  <td>워크플로우 상태</td>
                  <td>열거형(문자열)(255)</td>
                  <td>
                     <ul>
                        <li>진행 중 - 시작됨 - 시작됨</li>
                        <li>편집 - 에디션 - 에디션</li>
                        <li>완료 - 완료 - 완료</li>
                        <li>경고 - 경고 - 경고</li>
                        <li>오류 - 오류 - 오류</li>
                        <li>잘못된 값 - __Invalid_value__ - __Invalid_value__</li>
                     </ul>
                  </td>
               </tr>
            </table>

## 필터

채널 유형별(채널별)

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

실행 유형별(byExecutionType)

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

논리적 상태 기준(byLogicalStatus)

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
    <tr>
    <td>mc</td>
    <td>문자열</td>
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
    <td>문자열</td>
    </tr>
</table>

기간별(StartPeriod)

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
    <td>timePeriod</td>
    <td>문자열</td>
    </tr>
</table>

게시 상태별(PublicationStatus)

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

상태별(주별)

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
    <td>following</td>
    <td>boolean</td>
    </tr>
</table>

고급 배달 포함(고급 포함)

<table>
    <tr>
    <th>이름</th>
    <th>유형</th>
    </tr>
    <tr>
    <td>advanced</td>
    <td>boolean</td>
    </tr>
</table>

이기종 목록에서 연속 배달 포함(연속 포함)

<table>
    <tr>
    <th>이름</th>
    <th>유형</th>
    </tr>
    <tr>
    <td>withContinuous</td>
    <td>boolean</td>
    </tr>
</table>

교정본 포함(FCP 포함)

<table>
    <tr>
    <th>이름</th>
    <th>유형</th>
    </tr>
    <tr>
    <td>withFCP</td>
    <td>boolean</td>
    </tr>
</table>

해당 기간 동안 계획(계획별)

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

주어진 기간 동안(달력별)

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

최신 기능 보기(showOb)

<table>
    <tr>
    <th>이름</th>
    <th>유형</th>
    </tr>
    <tr>
    <td>ob</td>
    <td>boolean</td>
    </tr>
</table>