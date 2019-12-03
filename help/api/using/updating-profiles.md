---
title: 프로필 업데이트
description: API를 사용하여 프로파일을 업데이트하는 방법에 대해 자세히 알아보십시오.
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
source-git-commit: aee0e0437cbfe578cb2f715a2433099c79dd1748

---


# 프로필 업데이트 {#updating-profiles}

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
