---
title: 데이터 모델
description: 데이터 모델에 대해 알아보기
audience: developing
content-type: reference
feature: Data Model
role: Developer
level: Experienced
exl-id: 9b522c84-e296-47c7-9588-2e5ed08ab631
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 10%

---

# 초기 멤버(nms:seedMember)

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
                  <td>국가(국가)</td>
                  <td>국가</td>
                  <td>링크 </td>
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
                  <td>emailRendering</td>
                  <td>이메일 렌더링</td>
                  <td>부울 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>팩스</td>
                  <td>팩스</td>
                  <td>문자열(32)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>geoUnit(geoUnitBase)</td>
                  <td>지리 단위</td>
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
                  <td>lastModified</td>
                  <td>마지막 수정 날짜</td>
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
                  <td>Marketing Cloud ID</td>
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
                  <td>문자열(32)</td>
                  <td> </td>
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
                  <td>조직 단위</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>phone</td>
                  <td>전화</td>
                  <td>문자열(32)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>증명</td>
                  <td>증명</td>
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
                  <td>주/도</td>
                  <td>링크 </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>targetData</td>
                  <td>확장</td>
                  <td>string </td>
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

이벤트 유형(byEventType) 기준

<table>
        <tr>
        <th>이름</th>
        <th>유형</th>
        </tr>
        <tr>
        <td>eventType</td>
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

사용 기준(사용 기준)

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
        <td>emailRendering</td>
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
