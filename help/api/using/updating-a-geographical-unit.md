---
solution: Campaign Standard
product: campaign
title: 프로필의 지리 단위 업데이트
description: API를 사용하여 지리적 단위를 관리하는 방법을 알아봅니다.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 10%

---


# 프로필의 지리 단위 업데이트 {#updating-a-geographical-unit}

1. 지리적 단위 PKey를 검색하려면 **geoUnitBase** 리소스에 대해 GET 요청을 수행합니다.
1. 페이로드에서 원하는 지리적 단위 PKey를 사용하여 프로필 PKey에 PATCH 요청을 수행합니다.

<br/>

***샘플 요청***

지리적 단위 목록을 검색합니다.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/geoUnitBase/ \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

모든 지리적 단위를 반환합니다. 프로파일을 할당할 장치의 PKey를 검색합니다.

```
{
 "PKey": "<PKEY>",
 "created": "2019-04-06 22:36:19.089Z",
 "desc": "",
 "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/geoUnitBase/<PKEY>",
 "label": "Europe",
 "lastModified": "2019-04-06 22:36:19.086Z",
 "name": "eu",
 "parentTitle": "All (all)",
 "title": "Europe (eu)"
},
```

페이로드에서 원하는 지리적 단위의 PKey를 사용하여 프로필에 PATCH 요청을 수행합니다.

```
-X PATCH https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/profile/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
-i
-d {
-d "geoUnit":{
-d    "PKey":"<PKEY>"
-d  }
-d }
```

<!-- + réponse -->
