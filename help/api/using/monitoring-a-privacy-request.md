---
title: 개인 정보 요청 모니터링
description: API를 사용하여 개인 정보 요청을 모니터링하는 방법 알아보기
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
old-role: Data Architect
role: Developer
level: Experienced
exl-id: 63864f0f-2c22-4a65-86ae-21897031f30a
TQID: https://experienceleague.adobe.com/VO2XcUgDBCaGtqXji550j770iijK8lr0SSw5J8VQtgk
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
feature_v2: id: b12f6872-9271-4369-85e5-86969a0b99a2
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 48
ht-degree: 16%

---

# 개인 정보 요청 모니터링 {#monitoring-a-privacy-request}

**GET** 요청을 사용하여 만들어진 개인 정보 보호 요청에 대한 정보를 모니터링할 수 있습니다.

상태 목록 설명은 [개인 정보 관리 설명서](../../start/using/privacy-requests.md)에서 사용할 수 있습니다.

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
