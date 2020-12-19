---
solution: Campaign Standard
product: campaign
title: 지리 단위 특성 업데이트
description: API를 사용하여 지리적 단위 속성을 업데이트하는 방법 알아보기
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 11%

---


# 지리 단위 특성 업데이트 {#managing-geographical-units}

1. 지리적 단위 PKey를 검색하려면 **geoUnitBase** 리소스에서 GET 요청을 수행합니다.
1. 페이로드에서 업데이트할 속성을 사용하여 지리학적 단위로 PATCH 요청을 수행합니다.

<br/>

***샘플 요청***

지리적 단위 목록을 읽어들입니다.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/geoUnitBase/ \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

모든 지리적 단위를 반환합니다. 원하는 단위의 PKey를 검색합니다.

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

페이로드에서 업데이트할 속성을 사용하여 지리학적 단위로 PATCH 요청을 수행합니다.

```
-X PATCH https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/orgUnitBase/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
-i
-d {
-d "label":"Asia",
-d "name":"asia"
-d }
```

<!-- + réponse -->
