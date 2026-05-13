---
title: 조직 단위 특성 업데이트
description: 조직 단위 특성을 업데이트하는 방법을 알아봅니다
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
old-role: Data Architect
role: Developer
level: Experienced
exl-id: 90841afd-ebc2-4b6a-895e-a96ef65740d7
TQID: https://experienceleague.adobe.com/VxXrw8RbDRqNAy14j-302n0mjx0JBOSvsjwfSjAqKAI
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
feature_v2: id: b12f6872-9271-4369-85e5-86969a0b99a2
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 84
ht-degree: 0%

---

# 조직 단위 특성 업데이트 {#updating-organizational-unit-attributes}

1. **orgUnitBase** 리소스에서 GET 요청을 수행하여 조직 단위 PKey를 검색합니다.
1. 조직 구성 단위에서 페이로드에 업데이트할 속성을 사용하여 PATCH 요청을 수행합니다.

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

모든 조직 단위를 반환합니다. 원하는 장치의 PKey를 검색합니다.

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

조직 구성 단위에서 페이로드에 업데이트할 속성을 사용하여 PATCH 요청을 수행합니다.

```
-X PATCH https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/orgUnitBase/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
-i
-d {
-d "label":"brand1",
-d "name":"brand1"
-d }
```

<!-- + réponse -->
