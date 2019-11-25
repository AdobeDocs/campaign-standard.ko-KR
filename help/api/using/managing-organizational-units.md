---
title: 조직 단위 관리
description: API를 사용하여 조직 구성 요소를 관리하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: c7b9c171-0409-4707-9d45-3fa72aee8008
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
discoiquuid: 304e7779-42d2-430a-9704-8c599a4eb1da
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c0c0be79613f99a15676343d8ce10d335baf968a

---


# 조직 단위 관리 {#managing-organizational-units}

orgUnitBase **종단점을** 사용하면 조직 단위와 상호 작용하여 해당 속성을 업데이트하거나 프로필의 조직 단위를 업데이트할 수 있습니다. Campaign의 조직 단위에 대한 자세한 내용은 캠페인 [설명서를 참조하십시오](https://helpx.adobe.com/campaign/standard/administration/using/organizational-units.html).

프로필 **리소스를 확장할 때 조직** 단위 필드가 프로필에 추가됩니다. 따라서 항상 profileAndServicesExt **끝점을 사용하여 지리적** 단위와 상호 작용해야 합니다. 프로필의 리소스 확장에 대한 자세한 내용은 Campaign [설명서를 참조하십시오](https://helpx.adobe.com/campaign/standard/administration/using/organizational-units.html#partitioning-profiles).

## 프로필의 조직 단위 검색

1. 프로필 PKey에서 GET 요청을 수행하여 orgUnit URL을 **검색합니다** .
1. URL에서 GET 요청을 수행하여 조직 단위에 대한 자세한 내용을 검색합니다.

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

프로필에 대한 orgUnit URL을 반환합니다.

```
{
  ...
  "orgUnit": {
    "PKey": "<PKEY>",
    "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/orgUnitBase/<PKEY>",
    "title": "All (all)"
    },
  ...
}
```

URL에서 GET 요청을 수행하여 자세한 정보를 검색합니다.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/orgUnitBase/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

조직 단위에 대한 세부 정보를 반환합니다.

```
{
  "PKey": "<PKEY>",
  "created": "2019-04-02 22:36:13.252Z",
  "desc": "",
  "label": "Brand 4",
  "lastModified": "2019-04-03 08:17:19.100Z",
  "name": "brand4",
  "parentTitle": "All (all)",
  "title": "Brand 4 (brand4)"
}
```

## 프로필의 조직 구성 단위 업데이트

1. orgUnitBase **리소스에서 GET** 요청을 수행하여 조직 단위 PKey를 검색합니다.
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

페이로드에서 원하는 조직 단위의 PKey를 사용하여 프로파일에서 PATCH 요청을 수행합니다.

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

## 조직 단위 속성 업데이트

1. orgUnitBase **리소스에서 GET** 요청을 수행하여 조직 단위 PKey를 검색합니다.
1. 페이로드에서 업데이트할 속성을 사용하여 조직 구성 단위의 PATCH 요청을 수행합니다.

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

모든 조직 단위를 반환합니다. 원하는 단위의 PKey를 검색합니다.

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

페이로드에서 업데이트할 속성을 사용하여 조직 구성 단위의 PATCH 요청을 수행합니다.

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
