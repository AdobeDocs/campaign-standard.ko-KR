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
source-wordcount: '171'
ht-degree: 9%

---


# 시드 멤버(nms:seedMember)

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
                  <td>국가(국가)</td>
                  <td>국가</td>
                  <td>link </td>
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
                  <td>email</td>
                  <td>이메일</td>
                  <td>문자열(128)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>emailRendering</td>
                  <td>전자 메일 렌더링</td>
                  <td>boolean </td>
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
                  <td>지리적 단위</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>isExternal</td>
                  <td>외부 리소스임</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>lastModified</td>
                  <td>마지막으로 수정한 날짜</td>
                  <td>date </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>위치</td>
                  <td>위치</td>
                  <td>item </td>
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
                  <td>item </td>
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
                  <td>nms_recipient</td>
                  <td>프로필</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>nms_rtEvent</td>
                  <td>이벤트</td>
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
                  <td>전화</td>
                  <td>전화</td>
                  <td>문자열(32)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>증명</td>
                  <td>증명</td>
                  <td>boolean </td>
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
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>sms</td>
                  <td>모바일</td>
                  <td>문자열(255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>stateLink(state)</td>
                  <td>주</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>targetData</td>
                  <td>익스텐션</td>
                  <td>문자열 </td>
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
                  <td>boolean </td>
                  <td> </td>
               </tr>
            </table>

## 필터

이벤트 유형(byEventType)

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

사용별(사용별)

<table>
        <tr>
        <th>이름</th>
        <th>유형</th>
        </tr>
        <tr>
        <td>트랩</td>
        <td>boolean</td>
        </tr>
        <tr>
        <td>emailRendering</td>
        <td>boolean</td>
        </tr>
        <tr>
        <td>증명</td>
        <td>boolean</td>
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
    <td>link</td>
    </tr>
</table>