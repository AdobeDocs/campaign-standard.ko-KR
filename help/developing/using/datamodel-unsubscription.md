---
title: 데이터 모델 구독 취소 이벤트
description: 데이터 모델에 대해 알아보기
audience: developing
content-type: reference
feature: Data Model
role: Developer
level: Experienced
exl-id: 508361d1-6a0b-4476-a058-4162fb3e8d5e
TQID: 'https://experienceleague.adobe.com/VuhZ3s5VTH3MFPuqzr18GBMmyaPxD2uQEdJAsMIOlf0'
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
source-wordcount: '54'
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
