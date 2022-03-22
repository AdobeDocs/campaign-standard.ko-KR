---
title: 데이터 모델 프로그램
description: 데이터 모델에 대해 알아보기
audience: developing
content-type: reference
feature: Data Model
role: Developer
level: Experienced
exl-id: b05dc67a-6447-4d22-99f2-8a14a0ee46d2
source-git-commit: a6471d2970a55373574301fb5d49ee73103fa870
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 21%

---

# 프로그램(nms:program)

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
                  <td>활동</td>
                  <td>활동</td>
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
                  <td>desc</td>
                  <td>설명</td>
                  <td>문자열(512)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>end</td>
                  <td>종료일</td>
                  <td>날짜 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>geoUnit(geoUnitBase)</td>
                  <td>지리적 단위</td>
                  <td>링크 </td>
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
                  <td>조직 단위</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>parent(programBase)</td>
                  <td>상위 프로그램</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>realtimeReport</td>
                  <td>실시간 보고서</td>
                  <td>항목 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>start</td>
                  <td>시작일</td>
                  <td>날짜 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>상태</td>
                  <td>상태</td>
                  <td>열거형(바이트) </td>
                  <td>
                     <ul>
                        <li>시작됨 - 시작됨 - 1</li>
                        <li>편집 - 편집 - 0</li>
                        <li>완료됨 - 완료됨 - 2</li>
                        <li>잘못된 값 - __Invalid_value__ - __Invalid_value__</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>템플릿(프로그램)</td>
                  <td>프로그램 템플릿</td>
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
                  <td>title</td>
                  <td>프로그램</td>
                  <td>문자열(255)</td>
                  <td> </td>
               </tr>
            </table>

## 필터

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
</table>

기간별(기간별)

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

하위 프로그램 포함(withParent)

<table>
        <tr>
        <th>이름</th>
        <th>유형</th>
        </tr>
        <tr>
        <td>withParent</td>
        <td>부울</td>
        </tr>
    </table>

적합한 부모(적격 부모)만

<table>
    <tr>
    <th>이름</th>
    <th>유형</th>
    </tr>
    <tr>
    <td>프로그램</td>
    <td>링크</td>
    </tr>
</table>

지정된 기간에 대해 계획됨(계획별)

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
