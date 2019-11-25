---
title: 메타데이터 메커니즘
description: 메타데이터 메커니즘에 대한 자세한 내용을 살펴보십시오.
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


# 메타데이터 메커니즘 {#metadata-mechanism}

GET 요청에서 resourceType **을 사용하여 리소스** 메타데이터를 검색할 수 있습니다.

`GET /profileAndServices/resourceType/<resourceName>`

응답은 리소스에서 기본 메타데이터를 반환합니다(다른 모든 필드는 설명적이거나 내부적입니다).

* 컨텐츠 **노드는** 리소스의 필드를 반환합니다. 컨텐츠 **** 노드의 각 필드에 대해 다음 필드를 찾을 수 있습니다.

   * "apiName":API에 사용되는 속성의 이름입니다.
   * "type":이것은 높은 수준의 형식 정의(문자열, 숫자, 링크, 컬렉션, 열거형..)입니다.
   * "dataPolicy":필드의 값은 지정된 정책 규칙을 따라야 합니다. 예를 들어 dataPolicy 규칙이 "email"로 설정된 경우 값은 유효한 이메일이어야 합니다. PATCH 또는 POST 동안 dataPolicy는 값을 확인하거나 변환할 값을 수정할 수 있습니다(예: smartCase).
   * "카테고리":쿼리 편집기에서 필드의 카테고리를 지정합니다.
   * "resType":기술 유형입니다.

      "type"이 "link" 또는 "collection" 값으로 완료되면 resTarget 값은 링크를 기준으로 타깃팅된 리소스의 이름입니다.
"type"이 "enumeration" 값과 함께 완료되면 "values" 필드가 추가되고 각 열거형 값은 **값** 노드에 자세히 설명되어 있습니다.

* 필터 **노드는** URL을 반환하여 연결된 필터를 검색합니다. For more on filters, refer to [this section](../../api/using/filtering.md) section.

<!-- créer une section au même niveau sur les liens -->
<!-- dans l'exemple: birthdate, email +  mettre 2 liens : un de type 1-1 , 1-N
si on prend l'exemple de l'org unit, on aura un bon exemple lien -->
<!-- plus reparler du node Data -->

<br/>

***샘플 요청***

리소스에 대해 GET 요청을 수행합니다.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/resourceType/profile \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

프로필 리소스의 전체 설명을 반환합니다.

```
{
...
"content": {
  "email": {...},
    ...
    },
"data": "/profileAndServices/profile/",
"filters": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/resourceType/<PKEY>"
    },
"help": "Identified profiles",
"href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/metadata",
"label": "Profiles",
"mandatory": false,
"name": "profile",
"pkgStatus": "never",
"readOnly": false,
"schema": "nms:recipient",
"type": "item"
}
```
