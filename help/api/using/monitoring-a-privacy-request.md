---
solution: Campaign Standard
product: campaign
title: 개인 정보 보호 요청 모니터링
description: API를 사용하여 개인 정보 요청을 모니터링하는 방법 학습
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 25%

---


# 개인 정보 보호 요청 모니터링 {#monitoring-a-privacy-request}

생성된 개인 정보 요청에 대한 정보는 **GET** 요청을 사용하여 모니터링할 수 있습니다.

상태 목록 설명은 개인 정보 [관리 문서에서 확인할 수 있습니다](https://helpx.adobe.com/kr/campaign/kb/acs-privacy.html#ManagingPrivacyRequests).

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
