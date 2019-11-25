---
title: 필수 읽기
description: API를 사용하기 전에 반드시 읽어야 합니다.
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


# 필수 읽기 {#must-read}

## 기술 요구 사항

* Adobe Campaign API 파섹
* 구현할 사용 사례가 Adobe Campaign API에서 허용하는 비율에 맞게 정렬되어 있는 경우 항상 Adobe 기술 담당자에게 문의하십시오.
* Adobe IO 액세스를 설정하려면 특정 권한이 필요합니다. 문제가 있으면 Adobe 지원 센터에 문의하십시오.

## 리소스 표현

모든 API 리소스는 URL **확장자를** 가진 JSON이나 HTTP 수락 헤더 내에서 사용할 수 있습니다.

`GET /profileAndServices/<resourceName>.json`

>[!NOTE]
>
>URL에 확장자가 없는 경우 **json 형식은 컨텐츠 유형의 기본** 형식입니다.

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

* URL을 직접 만들지 마십시오. 모든 URL은 API에서 반환됩니다. 하지만 최상위 리소스 이름을 기반으로 URL을 작성할 수 있습니다.

* 예제를 보여주는 자동 기본 키(PKey) 값은 다른 특정 배포에서 작동하지 않습니다. Adobe Campaign API에서 만듭니다.

* Adobe Campaign에서 생성된 자동 기본 키 값은 외부 데이터베이스 또는 웹 사이트에 저장할 수 없습니다. 데이터베이스 정의에서 특정 키 필드를 생성하여 개발 중에 사용해야 합니다.

## 사용자 정의 키 {#custom-keys}

프로필 리소스가 사용자 지정 키 필드로 확장된 경우 Adobe Campaign에서 생성된 자동 기본 키 대신 이 필드를 키로 사용할 수 있습니다.

`GET /.../profileAndServicesExt/profile/<customKey>`

키 값이 원본 키와 다른 경우 또는 Adobe에서 제공한 키 대신 고유한 비즈니스 키를 URI로 사용하는 경우에는 패치 작업을 사용하여 사용자 지정 키를 수정할 수 없습니다.

사용자 지정 키를 사용하여 **최상위 프로필 리소스만** 사용합니다. URL 파섹

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

프로필의 구독 목록을 반환합니다.

```
"service": {
"PKey": "<PKEY>",
"href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/<PKEY>",
"label": "Sport Newsletter",
"name": "SVC1",
"title": "Sport Newsletter (SVC1)"
}
```
