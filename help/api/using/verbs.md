---
solution: Campaign Standard
product: campaign
title: GET/POST/PATCH/DELETE 동사
description: Campaign Standard API에 사용되는 동사에 대해 자세히 알아보십시오.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---


# GET / POST / PATCH / DELETE 동사 {#verbs}

자원에 대한 작업을 수행하는 데 사용할 수 있는 동사는 다음과 같습니다.

* `GET`:한 요소 또는 요소 모음을 검색합니다.
* `POST`:매개 변수를 사용하여 리소스를 만듭니다.
* `PATCH`:매개 변수를 사용하여 리소스를 업데이트합니다.
* `DELETE`:리소스를 삭제합니다.

<!-- ajouter codes retour -->

<br/>

***샘플 요청***

* 프로필 컬렉션에 대한 샘플 GET 요청.


   ```
   $curl  
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>'
   ```

   프로파일 배열을 반환합니다.


   ```
   {
       "content": [
           {
               "PKey": "<PKEY>",
               "firstName": "Olivia",
               "lastName": "Varney",
               "birthDate": "1977-09-°4",
               "email": "o.varney@mail.com",
           },
           {
               "PKey": "<PKEY>",
               "firstName": "John",
               "lastName": "Doe",
               "birthDate": "1985-08-17",
               "email": "johndoe@mail.com",
           }
       ],
   }
   ```

* 특정 프로필의 샘플 GET 요청.


   ```
   $curl  
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY> \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>'
   ```

   요청된 프로파일을 반환합니다.


   ```
   {
       "PKey": "<PKEY>",
       "firstName": "John",
       "lastName": "Doe",
       "birthDate": "1985-08-17",
       "email": "johndoe@mail.com",
       ...
   }
   ```

* 프로파일을 만들기 위한 샘플 POST 요청.


   ```
   -X POST https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>' \
   -d '{"lastName":"Doe"}'
   ```

   기본 필드가 있는 프로파일을 반환합니다.

   ```
   {
       "PKey": "<PKEY>",
       "firstName": "John",
       "lastName": "Doe",
       "birthDate": "1985-08-17",
       "email": "johndoe@mail.com",
   }
   ```

* 프로파일 업데이트를 위한 샘플 PATCH 요청.

   ```
   -X PATCH https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY> \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>' \
   -d '{"firstName":"Mark"',"lastName":"Smith"}'
   ```

   업데이트된 프로파일을 검색할 PKEY 및 URL을 반환합니다.

   ```
   {
       "PKey": "<PKEY>",
       "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY>"
   }
   ```

* 프로필 삭제를 위한 샘플 DELETE 요청.

   ```
   -X DELETE https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY> \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>'
   ```

   요청은 200개의 응답을 반환하여 프로필이 삭제되었음을 확인합니다.
