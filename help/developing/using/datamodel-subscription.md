---
title: DataModel 가입 이벤트
description: 데이터 모델에 대해 알아보기
audience: developing
content-type: reference
feature: Data Model
role: Developer
level: Experienced
exl-id: cf0fac4e-59fd-4d6e-a411-41361f45938d
source-git-commit: a6471d2970a55373574301fb5d49ee73103fa870
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 32%

---

# 구독 이벤트(nms:rtEvent)

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
        <td>ctx</td>
        <td>텍스트 컨텍스트</td>
        <td>항목 </td>
        <td> </td>
    </tr>
    <tr>
        <td>이메일</td>
        <td>이메일</td>
        <td>문자열(128)</td>
        <td> </td>
    </tr>
    <tr>
        <td>emailFormat</td>
        <td>이메일 포맷</td>
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
        <td>문자열 (32)</td>
        <td> </td>
    </tr>
    <tr>
        <td>serverUrl</td>
        <td>ServerUrl</td>
        <td>문자열 </td>
        <td> </td>
    </tr>
</table>

## 필터

이메일(byEmail)로

<table>
    <tr>
    <th>이름</th>
    <th>유형</th>
    </tr>
    <tr>
    <td>이메일</td>
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
        <td>상태</td>
        <td>열거</td>
        </tr>
        <tr>
        <td>유형</td>
        <td>문자열</td>
        </tr>
    </table>
