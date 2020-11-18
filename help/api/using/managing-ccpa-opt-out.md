---
title: CPA 옵트아웃 관리
description: API를 사용하여 CPA 옵트아웃을 관리하는 방법 살펴보기
page-status-flag: never-activated
uuid: c7b9c171-0409-4707-9d45-3fa72aee8008
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
discoiquuid: 304e7779-42d2-430a-9704-8c599a4eb1da
translation-type: tm+mt
source-git-commit: 9240686a36146b45de6dfd07fc50a71fab663001
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 4%

---


# CPA 옵트아웃 관리 {#managing-ccpa-optout}

cpaOptOut 프로필 속성과 &quot; **true&quot; 또는 &quot;false&quot; 값을 사용하여 프로필의 CPA 옵트아웃 상태를** 모니터링하고 관리할 수 있습니다.

`"ccpaOptOut": <value>`

* **true**: 개인 정보의 판매를 금하다.
* **false**:개인 정보의 판매를 승인합니다.

>[!CAUTION]
>
>&quot;CPA 옵트아웃&quot; 속성은 19.4에서만 사용할 수 있습니다. 19.3 환경의 경우 프로필 리소스를 확장하고 부울 필드를 추가해야 합니다. 이 필드는 선택한 레이블과 함께 API에 추가됩니다. &quot;CPA를 위한 옵트아웃&quot;을 사용하는 것이 좋습니다.
>
>자세한 내용은 개인 정보 [관리 요청 설명서를 참조하십시오](../../start/using/privacy-requests.md#sale-of-personal-information-ccpa).

<br/>

***샘플 요청***

* 프로필의 CPA 옵트아웃 상태를 검색하기 위한 샘플 GET 요청.

   ```
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profilesAndServices/profile/<PKEY> \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>' \
   -H 'Content-Type: application/json;charset=utf-8'
   ```

   GET 요청에 대한 응답입니다.

   ```
   {
   "PKey": "<PKEY>",
     "ccpaOptOut": false,
     "firstName": "John",
     "lastName": "Doe",
   ...
   }
   ```

* CPA 옵트아웃을 위해 프로필을 표시하는 샘플 POST 요청입니다.

   ```
   -X POST https://mc.adobe.io/<ORGANIZATION>/campaign/profilesAndServices/profile/ \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>' \
   -H 'Content-Type: application/json;charset=utf-8'
   -i
   -d {
   -d  "firstName": "John",
   -d  "lastName": "Doe",
   -d  "email": "jdoe@mail.com",
   -d  "ccpaOptOut": true
   -d }'
   ```

   GET 요청에 대한 응답입니다.

   ```
   {
       ...
       "email": "john.doe@mail.com",
       "firstName": "John",
       "lastName": "Doe",
       "ccpaOptOut": true,
       ...
   }
   ```

* CPA 옵트아웃을 위한 프로필을 업데이트하기 위한 샘플 PATCH 요청.

   ```
   -X PATCH https://mc.adobe.io/<ORGANIZATION>/campaign/profilesAndServices/profile/<PKEY> \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>' \
   -H 'Content-Type: application/json;charset=utf-8'
   -i
   -d {
   -d  "ccpaOptOut": true
   -d }'
   ```

   GET 요청에 대한 응답입니다.

   ```
   {
       ...
       "email": "john.doe@mail.com",
       "firstName": "John",
       "lastName": "Doe",
       "ccpaOptOut": true,
       ...
   }
   ```
