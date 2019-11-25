---
title: DataModel
description: 데이터 모델에 대한 자세한 내용
uuid: 99277e46-e4f7-49a9-ba27-b878780f90da
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
discoiquuid: 6e21db35-daf9-4edb-977a-6ef606db0e4d
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 6263623a5a8999c475255709a7d0150437e68c0b

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
        <td>문자열 </td>
        <td> </td>
    </tr>
    <tr>
        <td>comment</td>
        <td>레퍼러 주석</td>
        <td>문자열(255)</td>
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
        <td>배달(배달)</td>
        <td>전달</td>
        <td>link </td>
        <td> </td>
    </tr>
    <tr>
        <td>deliveryId</td>
        <td>마지막 배달의 ID</td>
        <td>정수 </td>
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
        <td>앞으로 url</td>
        <td>문자열(255)</td>
        <td> </td>
    </tr>
    <tr>
        <td>geoUnit(geoUnitBase)</td>
        <td>지리적 단위</td>
        <td>link </td>
        <td> </td>
    </tr>
    <tr>
        <td>lastModified</td>
        <td>마지막으로 수정한 날짜</td>
        <td>date </td>
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
        <td>link </td>
        <td> </td>
    </tr>
    <tr>
        <td>orgUnit(orgUnitBase)</td>
        <td>조직 구성 단위</td>
        <td>link </td>
        <td> </td>
    </tr>
    <tr>
        <td>기원</td>
        <td>출처</td>
        <td>열거형(바이트) </td>
        <td>
            <ul>
            <li>정의되지 않음 - 0</li>
            <li>잘못된 값 - __Invalid_value__ - __Invalid_value__</li>
            </ul>
        </td>
    </tr>
    <tr>
        <td>수신자(수신자)</td>
        <td>식별된 프로필</td>
        <td>link </td>
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
        <td>referrerRcp(수신자)</td>
        <td>레퍼러</td>
        <td>link </td>
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

성, 이름 또는 이메일(텍스트별)</p>

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