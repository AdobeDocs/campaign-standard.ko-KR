---
solution: Campaign Standard
product: campaign
title: 프로필 검색
description: API를 사용하여 프로파일을 검색하는 방법에 대해 자세히 알아보십시오.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 4%

---


# 프로필 검색 {#retrieving-profiles}

프로파일 검색 작업은 **GET** 요청으로 수행됩니다.

그런 다음 필터, 순서 지정 및 페이지 매김을 사용하여 검색을 세분화할 수 있습니다. 자세한 내용은 [추가 작업](../../api/using/sorting.md) 섹션을 참조하십시오.

<br/>

***샘플 요청***

* 모든 프로파일을 검색하기 위한 샘플 GET 요청.

   ```
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>'
   ```

   요청에 대한 응답입니다.

   ```
   {
       "content": [
           {
               "PKey": "<PKEY>",
               "firstName": "John",
               "lastName":"Doe",
               "birthDate": "1980-10-24",
               ...
           },
           ...
   }
   ```

* 처음 10개의 이메일 값을 검색하기 위한 샘플 GET 요청.

   ```
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/email?_lineCount=10 \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>'
   ```

   요청에 대한 응답입니다. &quot;다음&quot; 노드는 다음 이메일 값 10에 대한 액세스 권한을 제공하는 URL을 반환합니다.

   ```
   {
   "content": [
       "amy.dakota@mail.com",
       "kristen.smith@mail.com",
       "omalley@mail.com",
       "xander.harrys@mail.com",
       "jane.summer@mail.com",
       "gloria.boston@mail.com",
       "edward.snow@mail.com",
       "dorian.simons@mail.com",
       "peter.paolini@mail.com",
       "mingam+test08@adobe.com"
   ],
   "next": {
       "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/email?_lineCount=10&_
       lineStart=@Qy2MRJCS67PFf8soTf4BzF7BXsq1Gbkp_e5lLj1TbE7HJKqc"
   }
   }
   ```
