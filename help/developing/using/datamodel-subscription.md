---
title: DataModel 가입 이벤트
description: 데이터 모델에 대해 알아보기
audience: developing
content-type: reference
feature: Data Model
role: Developer
level: Experienced
exl-id: cf0fac4e-59fd-4d6e-a411-41361f45938d
TQID: 'https://experienceleague.adobe.com/XssYu0sntbeCRq1uNe6MhztLtISXoJiOefIOnjqIaoQ'
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
  - id: f5407121-8933-4ac3-8e06-a9b692a4e88a
    internal-label: Campaign Standard
feature_v2:
  - id: a658c786-869b-4194-a780-2594d663adda
    internal-label: Data management
subfeature_v2:
  - id: a1681cd8-6b2e-4955-9113-33b5f7a22b8c
    internal-label: Data model architecture
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: bb37e2bfbc52de1b0cc03f0f8e03985caff5e5b0
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 33%
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
        <td>이벤트 컨텍스트</td>
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
