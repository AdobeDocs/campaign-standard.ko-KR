---
solution: Campaign Standard
product: campaign
title: 마케팅 기록 활용
description: 프로필의 마케팅 내역을 활용하는 방법을 살펴볼 수 있습니다.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 10%

---


# 마케팅 기록 활용 {#interacting-with-marketing-history}

**내역** 끝점을 사용하면 프로필의 마케팅 내역과 상호 작용할 수 있습니다.
예를 들어 이 방법으로 프로파일에 전송된 배달을 위해 미러 페이지를 쉽게 검색할 수 있습니다. 이렇게 하려면 아래 단계를 수행합니다:

1. **내역** 끝점과 프로필의 기본 키로 GET을 수행합니다.
1. 반환된 **events** href에 대해 GET 요청을 수행합니다.
1. 이 보고서는 **mirrorPage** 노드의 미러 페이지에 대한 링크가 있는 프로필의 이벤트 목록을 반환합니다.

<br/>

***샘플 요청***

GET 요청을 사용하여 프로필의 마케팅 내역을 검색합니다.

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

&quot;mirrorPage&quot; 노드의 미러 페이지에 대한 링크가 있는 프로필의 이벤트 목록을 반환합니다.

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
