---
title: 프로필 업데이트
description: API로 프로필을 업데이트하는 방법에 대해 자세히 알아보십시오.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: Data Engineer
level: Experienced
exl-id: fa3796ee-a00c-4d70-bf3d-e8d2099f1116
source-git-commit: ee7539914aba9df9e7d46144e437c477a7e52168
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 4%

---

# 프로필 업데이트 {#updating-profiles}

프로필 업데이트는 **PATCH** 요청으로 수행됩니다.

`https://mc.adobe.io/<ORGANIZATION>/campaign/<apiName>/<resourceName>/<PKEY>`

1. 첫 번째 단계는 **프로필 검색**&#x200B;입니다.

1. 두 번째 요청에서 페이로드의 완료된 정보와 함께 프로필에서 **PATCH 요청**&#x200B;을 수행합니다.

1. PATCH 요청이 프로필을 업데이트했는지 확인하기 위해 최종 GET 요청을 수행할 수 있습니다.

<br/>

***샘플 요청***

프로필을 검색하기 위한 샘플 GET 요청.

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

&quot;phone&quot; 속성을 업데이트하기 위한 PATCH 요청.

```
-X PATCH https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-d '{"phone":"3301020304"}'
```

업데이트된 프로필을 검색하기 위해 PKEY 및 URL을 반환합니다.

```
{
    "PKey": "<PKEY>",
    "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/@2v1dr3ZKJveMDhAdh0MPnh9hNQQ93qb7AW6BNVVKknjwXvTZRBAgUqz1SNcB4ZndgjqOofx3BwBZYBftlmObISoM3rs"
}
```
