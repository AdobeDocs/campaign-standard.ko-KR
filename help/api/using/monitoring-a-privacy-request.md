---
title: 개인 정보 요청 모니터링
description: API를 사용하여 개인 정보 보호 요청을 모니터링하는 방법을 알아봅니다
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: Data Engineer
level: Experienced
exl-id: 63864f0f-2c22-4a65-86ae-21897031f30a
source-git-commit: 013293fce8a923e771e10585c41e4ad482003080
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 16%

---

# 개인 정보 요청 모니터링 {#monitoring-a-privacy-request}

생성된 개인 정보 보호 요청에 대한 정보를 **GET** 요청.

상태 목록 설명은 [개인 정보 관리 설명서](../../start/using/privacy-requests.md).

<br/>

***샘플 요청***

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/privacy/privacyTool \
-H 'Authorization: Bearer <ACCESS_TOKEN>'
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-H 'Content-Type: application/json;charset=utf-8'
```

GET 요청에 대한 응답입니다.

```
{
            "PKey": "<PKEY>",
            "audit": "",
            "created": "2018-03-09 12:28:37.319Z",
            "desc": "",
            "gdprRequestData": {
                "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/privacy/privacyTool/<PKEY>/gdprRequestData/"
            },
            "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/privacy/privacyTool/<PKEY>",
            "label": "Delete customer profile",
            "lastModified": "2018-03-09 12:39:21.232Z",
            "name": "GDPR6",
            "namespace": {
                "PKey": "<PKEY>",
                "title": "Email (defaultNamespace1)"
            },
            "namespaceName": "defaultNamespace1",
            "reconciliationValue": "customers@adobe.com",
            "regulation": "gdpr",
            "retryCount": 0,
            "status": "errorDataNotFound",
            "title": "Delete customer profile (GDPR6)",
            "type": "delete"
        }
```
