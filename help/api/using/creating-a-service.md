---
title: API를 사용하여 서비스 만들기
description: API를 사용하여 서비스를 만드는 방법을 알아봅니다
feature: API
old-role: Data Architect
role: Developer
level: Experienced
exl-id: 91bbce9e-a618-4be2-840b-c7d021271f4e
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
  - id: f5407121-8933-4ac3-8e06-a9b692a4e88a
    internal-label: Campaign Standard
feature_v2:
  - id: b12f6872-9271-4369-85e5-86969a0b99a2
    internal-label: APIs
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: bb37e2bfbc52de1b0cc03f0f8e03985caff5e5b0
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%
---
# API를 사용하여 서비스 만들기{#creating-a-service-api}

서비스 리소스에서 **POST** 요청을 사용하여 서비스를 만듭니다.

특정 특성을 사용하여 서비스를 만들려면 해당 특성을 페이로드에 추가하십시오. 그렇지 않으면 기본 서비스와 함께 새 서비스가 만들어집니다.

<br/>

***샘플 요청***

특정 속성을 사용하여 서비스를 만들기 위한 샘플 POST 요청.

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

업데이트된 속성으로 새로 생성된 서비스를 반환합니다.

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
