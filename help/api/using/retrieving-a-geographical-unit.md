---
title: 프로필의 지리 단위 검색
description: API를 사용하여 프로필의 지리 단위를 검색하는 방법에 대해 알아봅니다.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
old-role: Data Architect
role: Developer
level: Experienced
exl-id: 313dbb7f-9cf7-43d4-ab6d-f496b04d92b8
TQID: https://experienceleague.adobe.com/AbKgeqTiLog4vUuT17UEMAw4uf5a-z9DLSn0La-BWlY
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
feature_v2: id: b12f6872-9271-4369-85e5-86969a0b99a2
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 80
ht-degree: 12%

---

# 프로필의 지리 단위 검색 {#retrieving-geographical-unit}

1. 프로필 PKey에서 GET 요청을 수행하여 **geoUnit** URL을 검색합니다.
1. URL에 대해 GET 요청을 수행하여 지리적 단위에 대한 자세한 내용을 검색합니다.

<br/>

***샘플 요청***

프로필 레코드를 검색합니다.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/profile/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

프로필에 대한 geoUnit URL을 반환합니다.

```
{
  ...
  "geoUnit": {
    "PKey": "@zYV4vIjP1wpBebml6s71hjGiDhs4_gHgbC_UhuJFk8h7XTZxZ5QnZrPnQPEfB__TxwR2ge6sz61D8RR4zvD75CLDZtc<PKEY>",
    "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/orgUnitBase/<PKEY>",
    "title": "All (all)"
    },
  ...
}
```

자세한 정보를 검색하려면 URL에서 GET 요청을 수행하십시오.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/geoUnitBase/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

지리적 단위에 대한 세부 정보를 반환합니다.

```
{
  "PKey": "<PKEY>",
  "created": "2019-04-02 22:36:13.252Z",
  "desc": "Default geographical entity (accessible to everyone)",
  "label": "All",
  "lastModified": "2019-04-03 08:17:19.100Z",
  "name": "all",
  "parentTitle": "",
  "title": "All (all)"
}
```
