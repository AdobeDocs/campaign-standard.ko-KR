---
title: 데이터 모델 구독 취소 이벤트
description: 데이터 모델에 대해 알아보기
audience: developing
content-type: reference
feature: Data Model
role: Developer
level: Experienced
exl-id: 508361d1-6a0b-4476-a058-4162fb3e8d5e
TQID: https://experienceleague.adobe.com/VuhZ3s5VTH3MFPuqzr18GBMmyaPxD2uQEdJAsMIOlf0
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 54
ht-degree: 59%

---

# 구독 취소 이벤트(nms:rtEvent)

## 개체 설명

<table>
               <tr>
                  <th>이름</th>
                  <th>읽기 전용</th>
                  <th>유형</th>
                  <th>필수</th>
               </tr>
               <tr>
                  <td>PKey</td>
                  <td>거짓</td>
                  <td>문자열</td>
                  <td>거짓</td>
               </tr>
               <tr>
                  <td>ctx</td>
                  <td>거짓</td>
                  <td>항목</td>
                  <td>거짓</td>
               </tr>
               <tr>
                  <td>이메일</td>
                  <td>거짓</td>
                  <td>문자열</td>
                  <td>거짓</td>
               </tr>
               <tr>
                  <td>emailFormat</td>
                  <td>거짓</td>
                  <td>열거</td>
                  <td>거짓</td>
               </tr>
               <tr>
                  <td>mobilePhone</td>
                  <td>거짓</td>
                  <td>문자열</td>
                  <td>거짓</td>
               </tr>
               <tr>
                  <td>serverUrl</td>
                  <td>참</td>
                  <td>문자열</td>
                  <td>거짓</td>
               </tr>
            </table>

## 필터

이메일

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

byStatusOrType

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
