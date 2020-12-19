---
solution: Campaign Standard
product: campaign
title: 반드시 알아야 할 사항
description: API를 사용하려면 먼저 읽어야 합니다.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---


# {#must-read} 읽어야 함

## 기술 요구 사항

* Adobe Campaign API는 서버에 대해서만 사용해야 합니다.
* 구현하려는 사용 사례가 Adobe Campaign API에서 허용하는 비율에 맞게 정렬되어 있는 경우 Adobe 기술 담당자에게 항상 문의하십시오.
* Adobe IO 액세스를 설정하려면 특정 권한이 필요합니다. 문제가 발생하면 Adobe 지원에 문의하십시오.

## 리소스 표현

모든 API 리소스는 **JSON**&#x200B;에서 URL 확장자를 사용하거나 HTTP 수락 헤더 내에서 사용할 수 있습니다.

`GET /profileAndServices/<resourceName>.json`

>[!NOTE]
>
>URL에 확장이 없는 경우 **json 형식은 컨텐츠 유형에 대한 기본**&#x200B;입니다.

<br/>

***요청 샘플***

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile.json \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

## 기본 키 및 URL

* 스스로 URL을 만들지 마십시오. 모든 URL은 API에서 반환됩니다. 하지만 최상위 리소스 이름을 기반으로 URL을 작성할 수 있습니다.

* 예제를 보여주는 자동 기본 키(PKey) 값은 다른 특정 배포에서는 작동하지 않습니다. Adobe Campaign API를 통해 만들어집니다.

* Adobe Campaign에서 생성된 자동 기본 키 값은 외부 데이터베이스 또는 웹 사이트에 저장할 수 없습니다. 데이터베이스 정의에서 특정 키 필드를 생성하여 개발하는 동안 사용해야 합니다.

## 사용자 지정 키 {#custom-keys}

프로필 리소스가 사용자 지정 키 필드로 확장되면 Adobe Campaign에서 생성한 자동 기본 키 대신 이 필드를 키로 사용할 수 있습니다.

`GET /.../profileAndServicesExt/profile/<customKey>`

키 값이 원본 키와 다르거나 자체 비즈니스 키를 Adobe에서 제공하는 키 대신 URI로 사용하는 경우에는 PATCH 작업을 사용하여 사용자 지정 키를 수정할 수 없습니다.

**최상위 프로필 리소스**&#x200B;에만 사용자 지정 키를 사용합니다. URL은 API에서 반환되며 사용자가 직접 작성해서는 안 됩니다.

<br/>

***샘플 요청***

사용자 지정 키를 사용하여 프로필의 구독을 검색하려면 사용자 지정 키에 GET 작업을 수행하십시오.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/profile/<customKey> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

반환된 구독 URL에 대해 GET 요청을 수행합니다.

```
-X GET <SUBSCRIPTION_URL> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

프로필에 대한 구독 목록을 반환합니다.

```
"service": {
"PKey": "<PKEY>",
"href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/<PKEY>",
"label": "Sport Newsletter",
"name": "SVC1",
"title": "Sport Newsletter (SVC1)"
}
```
