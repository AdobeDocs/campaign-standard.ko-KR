---
title: 마케팅 기록 활용
description: 프로필의 마케팅 기록과 상호 작용하는 방법 알아보기
feature: API
old-role: Data Architect
role: Developer
level: Experienced
exl-id: 67282d21-b4ed-4af5-b751-848a6d705118
TQID: https://experienceleague.adobe.com/C5r-qK6kpvssv6eFdJNuOw61OXFapg8L8hrlxyb0vcA
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
feature_v2: id: b12f6872-9271-4369-85e5-86969a0b99a2
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 147
ht-degree: 0%

---

# 마케팅 기록 활용{#interacting-with-marketing-history}

**history** 끝점을 사용하면 프로필의 마케팅 기록과 상호 작용할 수 있습니다.
예를 들어 이 방법으로 프로필로 전송된 게재에 대한 미러 페이지를 쉽게 검색할 수 있습니다. 이렇게 하려면 아래 단계를 수행합니다.

1. **history** 엔드포인트와 프로필의 기본 키로 GET을 수행합니다.
1. 반환된 **events** href에서 GET 요청을 수행합니다.
1. **mirrorPage** 노드의 미러 페이지에 연결된 프로필에 대한 이벤트 목록을 반환합니다.

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
