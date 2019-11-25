---
title: 정렬
description: 정렬 작업을 수행하는 방법에 대한 자세한 내용
page-status-flag: never-activated
uuid: c7b9c171-0409-4707-9d45-3fa72aee8008
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
discoiquuid: 304e7779-42d2-430a-9704-8c599a4eb1da
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c0c0be79613f99a15676343d8ce10d335baf968a

---


# 정렬

정렬은 오름차순이나 내림차순으로 사용할 수 있습니다. 이렇게 하려면 요청에 **%20desc** 또는 **%20asc** 매개 변수를 사용하십시오.

필드를 정렬할 수 있는지 확인하려면 리소스 메타데이터에 "정렬 가능한" 매개 변수를 선택합니다. For more on this, refer to [this section](../../api/using/metadata-mechanism.md).

<br/>

***샘플 요청***

* GET 요청 샘플을 사용하여 알파벳순으로 정렬된 데이터베이스의 이메일을 검색합니다.

   ```
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/email/email?_order=email \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>'
   ```

   요청에 대한 응답입니다.

   ```
   {
   "content": [
       "adam@email.com",
       "allison.durance@example.com",
       "amy.dakota@mail.com",
       "andrea.johnson@mail.com",
       ...
   ]
   ...
   }
   ```

* 데이터베이스에서 이메일을 내림차순으로 검색하는 샘플 GET 요청.

   ```
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/email?_order=email%20desc \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>'
   ```

   요청에 대한 응답입니다.

   ```
   {
   "content": [
       "tombinder@example.com",
       "tombinder@example.com",
       "timross@example.com",
       "john.smith@example.com",
       ...
   ]
   }
   ```
