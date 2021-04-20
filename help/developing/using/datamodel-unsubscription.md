---
solution: Campaign Standard
product: campaign
title: DataModel
description: 데이터 모델에 대한 자세한 내용
audience: developing
content-type: reference
feature: Data Model
role: Developer
level: Experienced
translation-type: tm+mt
source-git-commit: 088b49931ee5047fa6b949813ba17654b1e10d60
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 5%

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
                  <td>False</td>
                  <td>문자열</td>
                  <td>False</td>
               </tr>
               <tr>
                  <td>ctx</td>
                  <td>False</td>
                  <td>item</td>
                  <td>False</td>
               </tr>
               <tr>
                  <td>email</td>
                  <td>False</td>
                  <td>문자열</td>
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
                  <td>문자열</td>
                  <td>False</td>
               </tr>
               <tr>
                  <td>serverUrl</td>
                  <td>True</td>
                  <td>문자열</td>
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
    <td>email</td>
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
        <td>status</td>
        <td>열거형</td>
        </tr>
        <tr>
        <td>type</td>
        <td>문자열</td>
        </tr>
    </table>