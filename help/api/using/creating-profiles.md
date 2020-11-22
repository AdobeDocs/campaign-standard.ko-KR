---
solution: Campaign Standard
product: campaign
title: 프로필 만들기
description: API를 사용하여 프로파일을 만드는 방법에 대해 자세히 알아보십시오.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 3%

---


# 프로필 만들기 {#creating-profiles}

프로필 만들기는 프로필 리소스에 대한 **POST** 요청을 사용하여 수행됩니다.

>[!CAUTION]
>
>생성된 프로필에 <b>orgUnit</b> 을 연결하려면 프로필 리소스를 이 필드로 확장해야 하며, 확장자가 게시된 후에는 ProfileAndServicesExt <b>끝점에서 POST 요청을</b> 수행해야 합니다.
>
>프로필의 리소스 확장명에 대한 자세한 내용은 <a href="https://helpx.adobe.com/campaign/standard/administration/using/organizational-units.html#partitioning-profiles">캠페인 설명서를 참조하십시오</a>.

<br/>

***샘플 요청***

이메일 &quot;john.doe@mail.com&quot;으로 프로파일을 만들기 위한 샘플 POST 요청입니다.

```
-X POST https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-i
-d '{"email":"john.doe@mail.com"}'
```

새로 만든 프로필을 &quot;john.doe@mail.com&quot; 이메일 주소로 반환합니다.

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
