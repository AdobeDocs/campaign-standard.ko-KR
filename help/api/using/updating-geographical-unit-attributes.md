---
title: 지리 단위 특성 업데이트
description: API를 사용하여 지리 단위 속성을 업데이트하는 방법을 알아봅니다
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: Data Engineer
level: Experienced
exl-id: 86810821-6f62-46ab-ba0b-2175797fe9dd
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 11%

---

# 지리 단위 특성 업데이트 {#managing-geographical-units}

1. 에 대한 GET 요청 수행 **geoUnitBase** 지리적 단위 PKey를 검색하는 리소스입니다.
1. 페이로드에서 업데이트할 속성을 사용하여 지리적 단위에 대한 PATCH 요청을 수행합니다.

<br/>

***샘플 요청***

지리 단위 목록을 검색합니다.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/geoUnitBase/ \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

모든 지리 단위를 반환합니다. 원하는 장치의 PKey를 검색합니다.

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

페이로드에서 업데이트할 속성을 사용하여 지리적 단위에 대한 PATCH 요청을 수행합니다.

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
