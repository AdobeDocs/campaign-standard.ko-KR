---
title: 프로필 만들기
description: API를 사용하여 프로필을 만드는 방법을 자세히 알아봅니다.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: Data Engineer
level: Experienced
exl-id: 69e8d034-6bdd-4b82-bcd7-1ef4be0a59b3
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 3%

---

# 프로필 만들기 {#creating-profiles}

프로필 만들기는 프로필 리소스에 대한 **POST** 요청을 사용하여 수행됩니다.

>[!CAUTION]
>
>생성된 프로필에 <b>orgUnit</b>을(를) 연결하려면 이 필드로 프로필 리소스를 확장해야 하며, 확장이 게시된 후 <b>ProfileAndServicesExt</b> 종단점에 대해 POST 요청을 수행해야 합니다.
>
>프로필의 리소스 확장에 대한 자세한 내용은 <a href="https://helpx.adobe.com/campaign/standard/administration/using/organizational-units.html#partitioning-profiles">캠페인 설명서</a>를 참조하십시오.

<br/>

***샘플 요청***

이메일 &quot;john.doe@mail.com&quot;을 사용하여 프로필을 만들기 위한 샘플 POST 요청.

```
-X POST https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-i
-d '{"email":"john.doe@mail.com"}'
```

새로 만든 프로필을 &quot;john.doe@mail.com&quot; 이메일 주소와 함께 반환합니다.

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
