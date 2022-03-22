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
source-wordcount: '208'
ht-degree: 16%

---

# 대상(nms:audience)

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
                  <td>audienceDataSchema</td>
                  <td>데이터 스키마</td>
                  <td>문자열(255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>audienceMetadata</td>
                  <td>AudienceMetadata</td>
                  <td>문자열(255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>collectLineNumber</td>
                  <td>라인 번호를 ID로 사용</td>
                  <td>부울 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>count</td>
                  <td>카운트</td>
                  <td>정수 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>countDate</td>
                  <td>카운트 날짜</td>
                  <td>날짜 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>countPreview</td>
                  <td>CountPreview</td>
                  <td>항목 </td>
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
                  <td>doNotPersist</td>
                  <td>이 작업의 내역 표시 안 함</td>
                  <td>부울 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>errorLimit</td>
                  <td>중단하기 전 오류</td>
                  <td>정수 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>expirationDate</td>
                  <td>만료 날짜</td>
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
                  <td>jobLogs</td>
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
                  <td>lastModified</td>
                  <td>마지막 수정일</td>
                  <td>날짜 </td>
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
                  <td>조직 단위</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>rejectFilename</td>
                  <td>거부 파일</td>
                  <td>string </td>
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
                  <td>소스 Id</td>
                  <td>정수 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>title</td>
                  <td>대상자</td>
                  <td>문자열(255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>유형</td>
                  <td>유형</td>
                  <td>열거형(문자열)(100)</td>
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
                  <td>여기서</td>
                  <td>쿼리 정의</td>
                  <td>항목 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>워크플로우(워크플로우)</td>
                  <td>워크플로우</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
            </table>

## 필터

차원(byFilteringResource)을 필터링하여

<table>
    <tr>
    <th>이름</th>
    <th>유형</th>
    </tr>
    <tr>
    <td>filteringResource</td>
    <td>string</td>
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

유형별로(byType)

<table>
    <tr>
    <th>이름</th>
    <th>유형</th>
    </tr>
    <tr>
    <td>유형</td>
    <td>열거형</td>
    </tr>
    <tr>
    <td>isAMC</td>
    <td>string</td>
    </tr>
</table>
