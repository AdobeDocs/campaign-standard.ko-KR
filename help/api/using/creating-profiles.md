---
title: 프로필 만들기
description: API를 사용하여 프로파일을 만드는 방법에 대해 자세히 알아보십시오.
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


# 프로필 만들기 {#creating-profiles}

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
