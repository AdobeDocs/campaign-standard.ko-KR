---
title: 데이터 모델 구독 취소 이벤트
description: 데이터 모델에 대해 알아보기
audience: developing
content-type: reference
feature: Data Model
role: Developer
level: Experienced
exl-id: 508361d1-6a0b-4476-a058-4162fb3e8d5e
source-git-commit: a6471d2970a55373574301fb5d49ee73103fa870
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 58%

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
