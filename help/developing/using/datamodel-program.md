---
title: DataModel 프로그램
description: 데이터 모델에 대해 알아보기
audience: developing
content-type: reference
feature: Data Model
role: Developer
level: Experienced
exl-id: b05dc67a-6447-4d22-99f2-8a14a0ee46d2
source-git-commit: a6471d2970a55373574301fb5d49ee73103fa870
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 31%

---

# 프로그램(nms:program)

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
                  <td>활동</td>
                  <td>활동</td>
                  <td>컬렉션 </td>
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
                  <td>제작일</td>
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
                  <td>마지막 수정</td>
                  <td>일자 </td>
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
                  <td>상위(programBase)</td>
                  <td>상위 프로그램</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>실시간 보고서</td>
                  <td>실시간 보고서</td>
                  <td>항목 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>시작</td>
                  <td>시작일</td>
                  <td>일자 </td>
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
                  <td>제목</td>
                  <td>프로그램</td>
                  <td>문자열(255)</td>
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

기간별(기간별)

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
    <td>timePeriod</td>
    <td>문자열</td>
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

하위 프로그램 포함(withParent)

<table>
        <tr>
        <th>이름</th>
        <th>유형</th>
        </tr>
        <tr>
        <td>함께 상위</td>
        <td>부울</td>
        </tr>
    </table>

적격 상위(적격 상위)만

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

지정된 기간 동안 계획됨(byPlanning)

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

지정된 기간 동안 표시(byCalendar)

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
