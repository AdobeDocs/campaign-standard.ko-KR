---
title: 마케팅 기록 활용
description: 프로필의 마케팅 기록과 상호 작용하는 방법 알아보기
feature: API
role: Data Engineer
level: Experienced
exl-id: 67282d21-b4ed-4af5-b751-848a6d705118
source-git-commit: 64f24fb692754973331b4fb2f7b95e9a6f31cd0d
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# 마케팅 기록 활용{#interacting-with-marketing-history}

다음 **history** 엔드포인트를 사용하면 프로필의 마케팅 기록과 상호 작용할 수 있습니다.
예를 들어 이 방법으로 프로필로 전송된 게재에 대한 미러 페이지를 쉽게 검색할 수 있습니다. 이렇게 하려면 아래 단계를 수행합니다.

1. 를 사용하여 GET 수행 **history** 엔드포인트 및 프로필의 기본 키.
1. 에 대한 GET 요청 수행 **events** href가 반환되었습니다.
1. 프로필에 대한 이벤트 목록과 의 미러 페이지에 대한 링크를 반환합니다. **mirrorPage** 노드.

<br/>

***샘플 요청***

GET 요청으로 프로필의 마케팅 내역을 검색합니다.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/history/"<PKEY>" \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

&quot;events&quot; 노드는 프로필의 이벤트에 액세스할 수 있는 URL을 반환합니다.

```
{
  "PKey": "<PKEY>",
  "firstName": "John",
  "lastName":"Doe",
  "birthDate": "1980-10-24",
  "events": {
    "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/history/<PKEY>/events/",
    "metadata": "subHisto"
    },
}
```

반환된 이벤트 href에 대해 GET 요청을 수행합니다.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/history/<PKEY>/events \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

&quot;mirrorPage&quot; 노드의 미러 페이지에 대한 링크가 있는 프로필에 대한 이벤트 목록을 반환합니다.

```
    {
      "PKey": "<PKEY>",
      "category": "email",
      "date": "2018-05-17 08:44:49.366Z",
      "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/history/<PKEY>/events/<PKEY>",
      "label": "Send via email",
      "mirrorPage": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/history/<PKEY>/events/<PKEY>/mirrorPage/"
      },
      "type": "outbound"
    }
```
