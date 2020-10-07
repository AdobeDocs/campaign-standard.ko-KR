---
title: 프로필의 조직 단위 업데이트
description: API를 사용하여 프로필의 조직 구성 요소를 업데이트하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: c7b9c171-0409-4707-9d45-3fa72aee8008
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
discoiquuid: 304e7779-42d2-430a-9704-8c599a4eb1da
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 10%

---


# 프로필의 조직 단위 업데이트 {#managing-organizational-units}

1. 조직 단위 PKey를 검색하려면 **orgUnitBase** 리소스에서 GET 요청을 수행합니다.
1. 페이로드에서 원하는 조직 단위 PKey를 사용하여 프로필 PKey에서 PATCH 요청을 수행합니다.

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

모든 조직 단위를 반환합니다. 프로파일을 할당할 장치의 PKey를 검색합니다.

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

페이로드에서 원하는 조직 단위의 PKey를 사용하여 프로필에 PATCH 요청을 수행합니다.

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
