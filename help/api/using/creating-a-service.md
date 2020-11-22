---
solution: Campaign Standard
product: campaign
title: 서비스 만들기
description: API를 사용하여 서비스를 만드는 방법을 알아봅니다.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 8%

---


# 서비스 만들기 {#creating-a-service}

서비스 생성은 서비스 리소스에 대한 **POST** 요청을 통해 수행됩니다.

특정 특성을 가진 서비스를 만들려면 페이로드에 추가합니다. 그렇지 않으면 새 서비스가 기본 서비스로 만들어집니다.

<br/>

***샘플 요청***

특정 특성을 가진 서비스를 만들기 위한 샘플 POST 요청.

```
-X POST https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/ \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
-i
-d {
-d "label": "My newsletter",
-d "messageType": "email",
-d "name": "email_newsletter",
-d "start": "2019-10-06"
-d }
```

업데이트된 특성을 사용하여 새로 만든 서비스를 반환합니다.

```
{
    "PKey": "<PKEY>",
    "builtIn": false,
    "created": "2019-09-26 12:00:37.005Z",
    "href": "https://mc.adobe.io/<ORGANIZATION>/profileAndServices/service/@NLscZuVHxdVu9rPftvrMWFfR1zRIxQGswSOmGLrK09JTF_iWhB0JCUHEndA_vvy__k9mzOYa5NVkcWDcrK8qGh0wygahX9kRcD44kiWWSEceShn3",
    "label": "My newsletter",
    ...
}
```
