---
title: 데이터 모델
description: 데이터 모델에 대해 알아보기
audience: developing
content-type: reference
feature: Data Model
role: Developer
level: Experienced
exl-id: 20dafd81-8546-450a-87a0-59a2509efb7a
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 5%

---

# 방문자(nms:visitor)

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
        <td>댓글</td>
        <td>레퍼러 주석</td>
        <td>문자열(255)</td>
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
        <td>게재(게재)</td>
        <td>게재</td>
        <td>링크 </td>
        <td> </td>
    </tr>
    <tr>
        <td>deliveryId</td>
        <td>마지막 게재의 ID</td>
        <td>정수 </td>
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
        <td>externalId</td>
        <td>외부 ID</td>
        <td>문자열(64)</td>
        <td> </td>
    </tr>
    <tr>
        <td>firstName</td>
        <td>이름</td>
        <td>문자열(30)</td>
        <td> </td>
    </tr>
    <tr>
        <td>forwardUrl</td>
        <td>Url 전달</td>
        <td>문자열(255)</td>
        <td> </td>
    </tr>
    <tr>
        <td>geoUnit(geoUnitBase)</td>
        <td>지리 단위</td>
        <td>링크 </td>
        <td> </td>
    </tr>
    <tr>
        <td>lastModified</td>
        <td>마지막 수정 날짜</td>
        <td>날짜 </td>
        <td> </td>
    </tr>
    <tr>
        <td>lastName</td>
        <td>성</td>
        <td>문자열(50)</td>
        <td> </td>
    </tr>
    <tr>
        <td>modifiedBy(userBase)</td>
        <td>수정한 사람</td>
        <td>링크 </td>
        <td> </td>
    </tr>
    <tr>
        <td>orgUnit(orgUnitBase)</td>
        <td>조직 단위</td>
        <td>링크 </td>
        <td> </td>
    </tr>
    <tr>
        <td>원본</td>
        <td>Origin</td>
        <td>열거형(바이트) </td>
        <td>
            <ul>
            <li>정의되지 않음 - 정의되지 않음 - 0</li>
            <li>잘못된 값 - __Invalid_value__ - __Invalid_value__</li>
            </ul>
        </td>
    </tr>
    <tr>
        <td>수신자(수신자)</td>
        <td>식별된 프로필</td>
        <td>링크 </td>
        <td> </td>
    </tr>
    <tr>
        <td>recipientId</td>
        <td>프로필 ID</td>
        <td>정수 </td>
        <td> </td>
    </tr>
    <tr>
        <td>referrerEmail</td>
        <td>레퍼러 이메일</td>
        <td>문자열(128)</td>
        <td> </td>
    </tr>
    <tr>
        <td>referrerFirstName</td>
        <td>레퍼러 이름</td>
        <td>문자열(30)</td>
        <td> </td>
    </tr>
    <tr>
        <td>referrerId</td>
        <td>레퍼러 ID</td>
        <td>정수 </td>
        <td> </td>
    </tr>
    <tr>
        <td>referrerLastName</td>
        <td>레퍼러 성</td>
        <td>문자열(50)</td>
        <td> </td>
    </tr>
    <tr>
        <td>referrerRcp(recipient)</td>
        <td>레퍼러</td>
        <td>링크 </td>
        <td> </td>
    </tr>
    <tr>
        <td>title</td>
        <td>레이블</td>
        <td>문자열(255)</td>
        <td> </td>
    </tr>
</table>

## 필터

성, 이름 또는 전자 메일(byText)</p>

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
