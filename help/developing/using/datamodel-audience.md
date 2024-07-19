---
title: 데이터 모델 대상
description: 데이터 모델에 대해 알아보기
audience: developing
content-type: reference
feature: Data Model
role: Developer
level: Experienced
exl-id: 53da6c4e-d4fb-4677-acff-744e3eb10960
source-git-commit: a6471d2970a55373574301fb5d49ee73103fa870
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 36%

---

# 대상(nms:audience)

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
                  <td>aamMappingId</td>
                  <td>Audience Manager 매핑 ID</td>
                  <td>문자열(100)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>amcDataSource(amcDataSourceBase)</td>
                  <td>AMC 데이터 소스</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>audienceData</td>
                  <td>선택한 모집단 미리 보기</td>
                  <td>컬렉션 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>audience데이터 스키마</td>
                  <td>데이터 스키마</td>
                  <td>문자열(255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>audienceMeta</td>
                  <td>대상 메타데이터</td>
                  <td>문자열(255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>collectLineNumber</td>
                  <td>줄 번호를 ID로 사용</td>
                  <td>부울 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>count</td>
                  <td>횟수</td>
                  <td>정수 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>countDate</td>
                  <td>날짜 계산</td>
                  <td>일자 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>countView</td>
                  <td>CountPreview</td>
                  <td>항목 </td>
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
                  <td>desc</td>
                  <td>설명</td>
                  <td>문자열(512)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>doNotPersist</td>
                  <td>이 작업을 기록하지 않음</td>
                  <td>부울 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>errorLimit</td>
                  <td>중단 전 오류</td>
                  <td>정수 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>expirationDate</td>
                  <td>만료 일자</td>
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
                  <td>hasSchema</td>
                  <td>HasSchema</td>
                  <td>부울 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>isAMC</td>
                  <td>Adobe Marketing Cloud 대상</td>
                  <td>부울 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>isExternal</td>
                  <td>외부 리소스임</td>
                  <td>부울 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>작업 로그</td>
                  <td>로그</td>
                  <td>컬렉션 </td>
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
                  <td>rejectFile</td>
                  <td>거부 프로필</td>
                  <td>문자열 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>sharedAudience</td>
                  <td>공유 대상자의 이름</td>
                  <td>항목 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>소스</td>
                  <td>소스</td>
                  <td>항목 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>sourceId</td>
                  <td>소스 ID</td>
                  <td>정수 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>제목</td>
                  <td>대상자</td>
                  <td>문자열(255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>유형</td>
                  <td>유형</td>
                  <td>열거형(문자열) (100)</td>
                  <td>
                     <ul>
                        <li>쿼리 - 쿼리 - 쿼리</li>
                        <li>목록 - 목록 - 목록</li>
                        <li>파일 - 파일 - 파일</li>
                        <li>잘못된 값 - __Invalid_value__ - __Invalid_value__</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>위치</td>
                  <td>쿼리 정의</td>
                  <td>항목 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>워크플로(워크플로)</td>
                  <td>워크플로</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
            </table>

## 필터

차원 필터링(byFilteringResource)

<table>
    <tr>
    <th>이름</th>
    <th>유형</th>
    </tr>
    <tr>
    <td>filteringResource</td>
    <td>문자열</td>
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

유형별(byType)

<table>
    <tr>
    <th>이름</th>
    <th>유형</th>
    </tr>
    <tr>
    <td>유형</td>
    <td>열거</td>
    </tr>
    <tr>
    <td>isAMC</td>
    <td>문자열</td>
    </tr>
</table>
