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
source-wordcount: '77'
ht-degree: 6%

---


# 구독 이벤트(nms:rtEvent)

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
        <td>ctx</td>
        <td>이벤트 컨텍스트</td>
        <td>item </td>
        <td> </td>
    </tr>
    <tr>
        <td>email</td>
        <td>이메일</td>
        <td>문자열(128)</td>
        <td> </td>
    </tr>
    <tr>
        <td>emailFormat</td>
        <td>이메일 형식</td>
        <td>열거형(바이트) </td>
        <td>
            <ul>
            <li>텍스트 - 텍스트 - 1</li>
            <li>HTML - html - 2</li>
            <li>잘못된 값 - __Invalid_value__ - __Invalid_value__</li>
            <li>알 수 없음 - 알 수 없음 - 0</li>
            </ul>
        </td>
    </tr>
    <tr>
        <td>eventHistoId</td>
        <td>보관된 이벤트 ID</td>
        <td>정수 </td>
        <td> </td>
    </tr>
    <tr>
        <td>mobilePhone</td>
        <td>모바일 번호</td>
        <td>문자열(32)</td>
        <td> </td>
    </tr>
    <tr>
        <td>serverUrl</td>
        <td>서버 URL</td>
        <td>문자열 </td>
        <td> </td>
    </tr>
</table>

## 필터

이메일(이메일)

<table>
    <tr>
    <th>이름</th>
    <th>유형</th>
    </tr>
    <tr>
    <td>email</td>
    <td>문자열</td>
    </tr>
</table>

상태 또는 유형별(byStatusOrType)

<table>
        <tr>
        <th>이름</th>
        <th>유형</th>
        </tr>
        <tr>
        <td>status</td>
        <td>열거형</td>
        </tr>
        <tr>
        <td>type</td>
        <td>문자열</td>
        </tr>
    </table>