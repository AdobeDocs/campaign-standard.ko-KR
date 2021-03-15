---
solution: Campaign Standard
product: campaign
title: 카운팅
description: 카운트 작업을 수행하는 방법을 알아봅니다.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: 데이터 엔지니어
level: 경험
translation-type: tm+mt
source-git-commit: 088b49931ee5047fa6b949813ba17654b1e10d60
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 3%

---


# 카운팅

Adobe Campaign REST API는 요청에 있는 레코드 수를 계산할 수 있습니다. 이렇게 하려면 **count** 노드에서 반환되는 URL을 사용합니다.

<br/>

***샘플 요청***

&quot;sms&quot;에 해당하는 **messageType** 값이 있는 모든 서비스를 카운트하려면 **byChannel** 필터로 GET 요청을 수행하십시오.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/byChannel?channel=sms \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

필터에 해당하는 서비스를 반환합니다.

```
{
    "content": [
        {
            ...
            "messageType": "sms",
            "mode": "newsletter",
            "name": "SVC6",
            ...
        },
        ...
    ],
    "count": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/byChannel/_count?channel=sms&_lineStart=@iKTZ2q3IiSEDqZ5Nw1vdoGnQCqF-8DAUJRaVwR9obqqTxhMy"
    },
    "serverSidePagination": true
}
```

결과 수를 검색하려면 **count** 노드의 URL에 GET 요청을 수행합니다.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/byChannel/_count?channel=sms&_lineStart=@iKTZ2q3IiSEDqZ5Nw1vdoGnQCqF-8DAUJRaVwR9obqqTxhMy \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

레코드 수를 반환합니다.

```
{
    "count": 26
}
```

