---
title: 프로필 관리
description: API를 사용하여 프로파일을 관리하는 방법에 대해 자세히 알아보십시오.
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


# 프로필 관리 {#managing-profiles}

## 프로파일 검색

프로필 검색은 GET **요청을 사용하여** 수행됩니다.

그런 다음 필터, 순서 지정 및 페이지 매김을 사용하여 검색을 세분화할 수 있습니다. 자세한 내용은 추가 작업 [섹션을](../../api/using/sorting.md) 참조하십시오.

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

   요청에 대한 응답입니다. "다음" 노드는 10개의 다음 이메일 값에 액세스할 수 있는 URL을 반환합니다.

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

## 프로필 업데이트

프로파일 업데이트는 PATCH **요청을 통해 수행됩니다** .

`https://mc.adobe.io/<ORGANIZATION>/campaign/<apiName>/<resourceName>/<PKEY>`

1. 첫 번째 단계는 프로파일을 **가져오는 것입니다**.

1. 두 번째 요청에서, Adobe는 **페이로드의 완료된 정보와 함께 프로필에 대한 PATCH 요청을** 수행합니다.

1. PATCH 요청이 프로필을 업데이트했는지 확인하기 위해 최종 GET 요청을 수행할 수 있습니다.

<br/>

***샘플 요청***

프로파일 검색을 위한 샘플 GET 요청.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY>\
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
            "firstName": "Amy",
            "lastName":"Dakota",
            "birthDate": "1980-10-24",
            ...
        }
    ]
}
```

"phone" 속성을 업데이트하는 패치 요청.

```
-X PATCH https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-d '{"phone":"3301020304"}'
```

업데이트된 프로파일을 검색할 PKEY 및 URL을 반환합니다.

```
{
    "PKey": "<PKEY>",
    "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/@2v1dr3ZKJveMDhAdh0MPnh9hNQQ93qb7AW6BNVVKknjwXvTZRBAgUqz1SNcB4ZndgjqOofx3BwBZYBftlmObISoM3rs"
}
```

## 프로필 만들기

프로필 만들기는 프로필 리소스의 **POST** 요청을 사용하여 수행됩니다.

>[!CAUTION]
>
>orgUnit을 <b>생성된 프로필에</b> 연결하려면 프로필 리소스를 이 필드로 확장해야 하며, 확장자가 게시된 후에는 ProfileAndServicesExt <b>끝점에서 POST 요청을 수행해야 합니다</b> .
>
>프로필의 리소스 확장에 대한 자세한 내용은 Campaign <a href="https://helpx.adobe.com/campaign/standard/administration/using/organizational-units.html#partitioning-profiles">설명서를 참조하십시오</a>.

<br/>

***샘플 요청***

"john.doe@mail.com" 이메일을 사용하여 프로파일을 만들기 위한 샘플 POST 요청.

```
-X POST https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-i
-d '{"email":"john.doe@mail.com"}'
```

새로 만든 프로필을 "john.doe@mail.com" 이메일 주소로 반환합니다.

```
{
    "PKey": "<PKEY>",
    "firstName": "John",
    "lastName":"Doe",
    "birthDate": "1980-10-24",
    "email": "john.doe@mail.com",
    ...
}
```
