---
title: DataModel 시드 멤버
description: 데이터 모델에 대해 알아보기
audience: developing
content-type: reference
feature: Data Model
role: Developer
level: Experienced
exl-id: 9b522c84-e296-47c7-9588-2e5ed08ab631
TQID: https://experienceleague.adobe.com/lfD2ncth570TSScQZE3UiO3ikqqxpjf4CVd7PvuAFXs
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 182
ht-degree: 46%

---

# 초기 멤버(nms:seedMember)

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
                  <td>국가(국가)</td>
                  <td>국가</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>생성됨</td>
                  <td>생성일</td>
                  <td>날짜 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>createdBy (userBase)</td>
                  <td>생성자</td>
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
                  <td>이메일</td>
                  <td>이메일</td>
                  <td>문자열(128)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>전자 메일 렌더링</td>
                  <td>이메일 렌더링</td>
                  <td>부울 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>팩스</td>
                  <td>팩스</td>
                  <td>문자열 (32)</td>
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
                  <td>마지막 수정일</td>
                  <td>마지막 수정일</td>
                  <td>날짜 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>위치</td>
                  <td>위치</td>
                  <td>항목 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>marketingCloudId</td>
                  <td>MARKETING CLOUD ID</td>
                  <td>문자열(256)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>mobileApp</td>
                  <td>모바일 애플리케이션</td>
                  <td>항목 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>mobilePhone</td>
                  <td>모바일</td>
                  <td>문자열 (32)</td>
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
                  <td>nms_recipient</td>
                  <td>프로필</td>
                  <td>항목 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>nms_rtEvent</td>
                  <td>이벤트</td>
                  <td>항목 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>orgUnit(orgUnitBase)</td>
                  <td>조직 유닛</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>전화</td>
                  <td>휴대폰</td>
                  <td>문자열 (32)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>증명</td>
                  <td>교정쇄</td>
                  <td>부울 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>pushNotification</td>
                  <td>푸시 알림</td>
                  <td>문자열(255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>registrationToken</td>
                  <td>등록 토큰</td>
                  <td>문자열(256)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>sampleData</td>
                  <td>샘플 데이터</td>
                  <td>부울 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>sms</td>
                  <td>모바일</td>
                  <td>문자열(255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>stateLink (state)</td>
                  <td>상태</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>targetData</td>
                  <td>확장</td>
                  <td>문자열 </td>
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
                  <td>테스트 프로필</td>
                  <td>문자열(255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>트랩</td>
                  <td>트랩</td>
                  <td>부울 </td>
                  <td> </td>
               </tr>
            </table>

## 필터

이벤트 유형별(byEventType)

<table>
        <tr>
        <th>이름</th>
        <th>유형</th>
        </tr>
        <tr>
        <td>eventType</td>
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

사용별(사용별)

<table>
        <tr>
        <th>이름</th>
        <th>유형</th>
        </tr>
        <tr>
        <td>트랩</td>
        <td>부울</td>
        </tr>
        <tr>
        <td>전자 메일 렌더링</td>
        <td>부울</td>
        </tr>
        <tr>
        <td>증명</td>
        <td>부울</td>
        </tr>
    </table>

테스트 프로필(프로필)

<table>
    <tr>
    <th>이름</th>
    <th>유형</th>
    </tr>
    <tr>
    <td>seedMember</td>
    <td>링크</td>
    </tr>
</table>
