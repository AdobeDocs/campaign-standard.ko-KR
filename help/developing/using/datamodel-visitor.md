---
title: 데이터 모델 방문자
description: 데이터 모델에 대해 알아보기
audience: developing
content-type: reference
feature: Data Model
role: Developer
level: Experienced
exl-id: 20dafd81-8546-450a-87a0-59a2509efb7a
source-git-commit: a6471d2970a55373574301fb5d49ee73103fa870
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 34%

---

# 방문자(nms:visitor)

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
        <td>댓글</td>
        <td>레퍼러 댓글</td>
        <td>문자열(255)</td>
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
        <td>게재(게재)</td>
        <td>게재</td>
        <td>링크 </td>
        <td> </td>
    </tr>
    <tr>
        <td>deliveryId</td>
        <td>마지막 게재 ID</td>
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
        <td>이름</td>
        <td>이름</td>
        <td>문자열(30)</td>
        <td> </td>
    </tr>
    <tr>
        <td>forwardUrl</td>
        <td>전달 URL</td>
        <td>문자열(255)</td>
        <td> </td>
    </tr>
    <tr>
        <td>geoUnit(geoUnitBase)</td>
        <td>지리적 단위</td>
        <td>링크 </td>
        <td> </td>
    </tr>
    <tr>
        <td>마지막 수정일</td>
        <td>마지막 수정일</td>
        <td>일자 </td>
        <td> </td>
    </tr>
    <tr>
        <td>성</td>
        <td>성</td>
        <td>문자열(50)</td>
        <td> </td>
    </tr>
    <tr>
        <td>modifiedBy(userBase)</td>
        <td>수정자</td>
        <td>링크 </td>
        <td> </td>
    </tr>
    <tr>
        <td>orgUnit(orgUnitBase)</td>
        <td>조직 유닛</td>
        <td>링크 </td>
        <td> </td>
    </tr>
    <tr>
        <td>원본</td>
        <td>원본</td>
        <td>열거형(바이트) </td>
        <td>
            <ul>
            <li>정의되지 않음 - 정의되지 않음 - 0</li>
            <li>잘못된 값 - __Invalid_value__ - __Invalid_value__</li>
            </ul>
        </td>
    </tr>
    <tr>
        <td>수신자 (recipient)</td>
        <td>확인된 프로필</td>
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
        <td>레퍼러 이름</td>
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
        <td>레퍼러 성</td>
        <td>레퍼러 성</td>
        <td>문자열(50)</td>
        <td> </td>
    </tr>
    <tr>
        <td>referrerRcp (recipient)</td>
        <td>레퍼러</td>
        <td>링크 </td>
        <td> </td>
    </tr>
    <tr>
        <td>제목</td>
        <td>레이블</td>
        <td>문자열(255)</td>
        <td> </td>
    </tr>
</table>

## 필터

성, 이름 또는 이메일(byText)별</p>

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
