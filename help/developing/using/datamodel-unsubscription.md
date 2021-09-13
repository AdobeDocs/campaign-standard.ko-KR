---
title: 데이터 모델
description: 데이터 모델에 대해 알아보기
audience: developing
content-type: reference
feature: Data Model
role: Developer
level: Experienced
exl-id: 508361d1-6a0b-4476-a058-4162fb3e8d5e
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 5%

---

# 구독 취소 이벤트(nms:rtEvent)

## 개체 설명

<table>
               <tr>
                  <th>이름</th>
                  <th>읽기 전용</th>
                  <th>유형</th>
                  <th>필수 여부</th>
               </tr>
               <tr>
                  <td>PKey</td>
                  <td>False</td>
                  <td>string</td>
                  <td>False</td>
               </tr>
               <tr>
                  <td>ctx</td>
                  <td>False</td>
                  <td>항목</td>
                  <td>False</td>
               </tr>
               <tr>
                  <td>이메일</td>
                  <td>False</td>
                  <td>string</td>
                  <td>False</td>
               </tr>
               <tr>
                  <td>emailFormat</td>
                  <td>False</td>
                  <td>열거형</td>
                  <td>False</td>
               </tr>
               <tr>
                  <td>mobilePhone</td>
                  <td>False</td>
                  <td>string</td>
                  <td>False</td>
               </tr>
               <tr>
                  <td>serverUrl</td>
                  <td>True</td>
                  <td>string</td>
                  <td>False</td>
               </tr>
            </table>

## 필터

byEmail

<table>
    <tr>
    <th>이름</th>
    <th>유형</th>
    </tr>
    <tr>
    <td>이메일</td>
    <td>string</td>
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
        <td>열거형</td>
        </tr>
        <tr>
        <td>유형</td>
        <td>string</td>
        </tr>
    </table>
