---
solution: Campaign Standard
product: campaign
title: 메타데이터 메커니즘
description: 메타데이터 메커니즘에 대해 자세히 알아보십시오.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: 데이터 엔지니어
level: 경험
translation-type: tm+mt
source-git-commit: 088b49931ee5047fa6b949813ba17654b1e10d60
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 2%

---


# 메타데이터 메커니즘 {#metadata-mechanism}

GET 요청에서 **resourceType**&#x200B;을(를) 사용하여 리소스 메타데이터를 검색할 수 있습니다.

`GET /profileAndServices/resourceType/<resourceName>`

응답은 리소스에서 기본 메타데이터를 반환합니다(다른 모든 필드는 설명적이거나 내부적입니다).

* **Content** 노드는 리소스의 필드를 반환합니다. **content** 노드의 각 필드에 대해 다음 필드를 찾을 수 있습니다.

   * &quot;apiName&quot;:API에 사용되는 속성의 이름입니다.
   * &quot;type&quot;:높은 수준의 형식 정의입니다(문자열, 숫자, 링크, 컬렉션, 열거형..).
   * &quot;dataPolicy&quot;:필드의 값은 주어진 정책 규칙을 따라야 합니다. 예를 들어 dataPolicy 규칙이 &quot;email&quot;로 설정된 경우 값은 유효한 이메일이어야 합니다. PATCH 또는 POST 중에 dataPolicy는 값을 확인하거나 변형할 값을 수정할 수 있습니다(예: smartCase).
   * &quot;카테고리&quot;:는 쿼리 편집기에서 필드의 범주를 지정합니다.
   * &quot;resType&quot;:이 기술 유형은 다음과 같습니다.

      &quot;type&quot;이 &quot;link&quot; 또는 &quot;collection&quot; 값으로 완료되면 resTarget 값은 링크가 타깃팅한 리소스의 이름입니다.
&quot;type&quot;이 &quot;enumeration&quot; 값으로 완료되면 &quot;values&quot; 필드가 추가되고 각 열거형 값은 **values** 노드에 자세히 표시됩니다.

* **필터** 노드는 연결된 필터를 검색할 URL을 반환합니다. 필터에 대한 자세한 내용은 [이 섹션](../../api/using/filtering.md) 섹션을 참조하십시오.

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
