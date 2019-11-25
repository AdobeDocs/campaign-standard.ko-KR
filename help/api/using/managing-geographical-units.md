---
title: 지리적 단위 관리
description: API를 사용하여 지리적 단위를 관리하는 방법을 알아봅니다.
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


# 지리적 단위 관리 {#managing-geographical-units}

>[!CAUTION]
>
>지리적 단위 기능은 Campaign Standard 18.7 릴리스에서 더 이상 사용되지 않습니다.
따라서 새 Campaign Standard 인스턴스와 지리적 단위를 만들지 않은 기존 인스턴스는 18.7 릴리스부터 이 기능을 구현할 수 없습니다.
자세한 내용은 더 이상 사용되지 않는 <a href="https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html">기능</a> 페이지를 참조하십시오.

geoUnit **Base** 종단점을 사용하면 지리적 단위와 상호 작용하여 속성을 업데이트하거나 프로필 단위를 업데이트할 수 있습니다.

프로필 **리소스를** 확장할 때 지리적 단위 필드가 프로필에 추가됩니다. 따라서 항상 profileAndServicesExt **끝점을 사용하여 지리적** 단위와 상호 작용해야 합니다. 프로필의 리소스 확장에 대한 자세한 내용은 Campaign [설명서를 참조하십시오](https://helpx.adobe.com/campaign/standard/administration/using/organizational-units.html#partitioning-profiles).

## 프로필의 지리적 단위 검색

1. 프로필 PKey에서 GET 요청을 수행하여 geoUnit URL을 **검색합니다** .
1. URL에서 GET 요청을 수행하여 지리적 단위에 대한 자세한 내용을 검색합니다.

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

URL에서 GET 요청을 수행하여 자세한 정보를 검색합니다.

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

## 프로필의 지리적 단위 업데이트

1. 지리적 단위 PKey를 검색하려면 **geoUnitBase** 리소스에서 GET 요청을 수행합니다.
1. 페이로드에서 원하는 지리적 단위 PKey를 사용하여 프로필 PKey에서 PATCH 요청을 수행합니다.

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

페이로드에서 원하는 지리적 단위의 PKey를 사용하여 프로파일에서 PATCH 요청을 수행합니다.

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

## 지역 단위 속성 갱신

1. 지리적 단위 PKey를 검색하려면 **geoUnitBase** 리소스에서 GET 요청을 수행합니다.
1. 페이로드에서 업데이트할 속성을 사용하여 지리적으로 PATCH 요청을 수행합니다.

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

페이로드에서 업데이트할 속성을 사용하여 지리적으로 PATCH 요청을 수행합니다.

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
