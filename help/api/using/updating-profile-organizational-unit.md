---
title: 프로필의 조직 단위 업데이트
description: API를 사용하여 프로필의 조직 단위를 업데이트하는 방법을 알아봅니다.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: Data Engineer
level: Experienced
exl-id: 6ce49aeb-a113-43ee-bfe3-f26a4a9e2a56
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 10%

---

# 프로필의 조직 단위 업데이트 {#managing-organizational-units}

1. 에 대한 GET 요청 수행 **orgUnitBase** 조직 단위 PKey를 검색하는 리소스
1. 페이로드에 원하는 조직 단위 PKey를 사용하여 프로필 PKey에 대한 PATCH 요청을 수행합니다.

<br/>

***샘플 요청***

조직 단위 목록을 검색합니다.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/orgUnitBase/ \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

모든 조직 단위를 반환합니다. 프로필을 할당할 장치의 PKey를 검색합니다.

```
{
  "PKey": "<PKEY>",
  "created": "2019-04-02 22:36:13.252Z",
  "desc": "",
  "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/orgUnitBase/<PKEY>",
  "label": "Brand 4",
  "lastModified": "2019-04-03 07:34:56.579Z",
  "name": "brand4",
  "parentTitle": "All (all)",
  "title": "Brand 4 (brand1)"
},
```

페이로드에서 원하는 조직 단위의 PKey를 사용하여 프로필에 대한 PATCH 요청을 수행합니다.

```
-X PATCH https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/profile/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
-i
-d {
-d "orgUnit":{
-d    "PKey":"<PKEY>"
-d  }
-d }
```

<!-- + réponse -->
