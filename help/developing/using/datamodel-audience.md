---
solution: Campaign Standard
product: campaign
title: DataModel
description: 데이터 모델에 대한 자세한 내용
audience: developing
content-type: reference
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 5%

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
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>audienceData</td>
                  <td>선택한 모집단 미리 보기</td>
                  <td>collection </td>
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
                  <td>boolean </td>
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
                  <td>date </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>countPreview</td>
                  <td>CountPreview</td>
                  <td>item </td>
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
                  <td>desk</td>
                  <td>설명</td>
                  <td>문자열(512)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>doNotPersist</td>
                  <td>이 작업의 내역 표시 안 함</td>
                  <td>boolean </td>
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
                  <td>hasSchema</td>
                  <td>HasSchema</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>isAMC</td>
                  <td>Adobe Marketing Cloud 대상</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>isExternal</td>
                  <td>외부 리소스임</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>jobLogs</td>
                  <td>로그</td>
                  <td>collection </td>
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
                  <td>조직 단위</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>rejectFilename</td>
                  <td>거부 파일</td>
                  <td>문자열 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>sharedAudience</td>
                  <td>공유 대상의 이름</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>소스</td>
                  <td>소스</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>sourceId</td>
                  <td>소스 ID</td>
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
                  <td>type</td>
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
                  <td>where</td>
                  <td>쿼리 정의</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>워크플로우(워크플로우)</td>
                  <td>워크플로우</td>
                  <td>link </td>
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

유형별(유형별)

<table>
    <tr>
    <th>이름</th>
    <th>유형</th>
    </tr>
    <tr>
    <td>type</td>
    <td>열거형</td>
    </tr>
    <tr>
    <td>isAMC</td>
    <td>문자열</td>
    </tr>
</table>