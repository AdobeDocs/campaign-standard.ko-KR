---
title: API를 사용하여 프로필 만들기
description: API를 사용하여 프로필을 만드는 방법을 자세히 알아봅니다.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: Data Engineer
level: Experienced
exl-id: 69e8d034-6bdd-4b82-bcd7-1ef4be0a59b3
source-git-commit: a6471d2970a55373574301fb5d49ee73103fa870
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 0%

---

# API를 사용하여 프로필 만들기 {#creating-profiles-api}

프로필 만들기는 **POST** 프로필 리소스에 대한 요청.

>[!CAUTION]
>
>을(를) 연관시키려면 <b>orgUnit</b> 생성된 프로필의 경우, 이 필드로 프로필 리소스를 확장해야 하며, 확장이 게시된 후 <b>ProfileAndServicesExt</b> 엔드포인트.
>
>프로필의 리소스 확장에 대한 자세한 내용은 <a href="https://helpx.adobe.com/campaign/standard/administration/using/organizational-units.html#partitioning-profiles">Campaign 설명서</a>.

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
