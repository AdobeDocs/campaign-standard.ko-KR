---
title: CCPA 옵트아웃 관리
description: API를 사용하여 CCPA 옵트아웃을 관리하는 방법 알아보기
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: Data Engineer
level: Experienced
exl-id: bfc52511-f66f-4948-a939-d0d77e8ef03c
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 4%

---

# CCPA 옵트아웃 관리 {#managing-ccpa-optout}

프로필의 CCPA 옵트아웃 상태는 **ccpaOptOut** 프로필 속성 및 &quot;true&quot; 또는 &quot;false&quot; 값:

`"ccpaOptOut": <value>`

* **true**: 개인 정보 판매를 금하고 있다.
* **false**: 개인 정보의 판매를 승인합니다.

>[!CAUTION]
>
>CCPA 옵트아웃 속성은 19.4부터 만 사용할 수 있습니다. 19.3 환경의 경우 프로필 리소스를 확장하고 부울 필드를 추가해야 합니다. 이 필드는 선택한 레이블이 있는 API에 추가됩니다. &quot;CCPA용 옵트아웃&quot;을 사용하는 것이 좋습니다.
>
>자세한 내용은 [개인 정보 보호 요청 관리 설명서](../../start/using/privacy-requests.md#sale-of-personal-information-ccpa).

<br/>

***샘플 요청***

* 프로필의 CCPA 옵트아웃 상태를 검색하기 위한 샘플 GET 요청.

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

* CCPA 옵트아웃에 대한 프로필을 표시하기 위한 샘플 POST 요청.

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

* CCPA 옵트아웃용 프로필을 업데이트하기 위한 샘플 PATCH 요청.

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
