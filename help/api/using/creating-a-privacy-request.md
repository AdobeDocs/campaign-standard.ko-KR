---
title: 개인 정보 요청 만들기
description: API를 사용하여 개인 정보 보호 요청을 만드는 방법을 알아봅니다
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: Data Engineer
level: Experienced
exl-id: 06ad2e13-922b-4f35-8726-007427125c63
source-git-commit: e41667405b54a7ed0e02889e3002807e4bfd3a05
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 7%

---

# 개인 정보 요청 만들기 {#creating-a-privacy-request}

>[!CAUTION]
>
>다음 [개인 정보 보호 핵심 서비스](https://adobe.io/apis/cloudplatform/gdpr.html) 통합은 모든 액세스 및 삭제 요청에 사용해야 하는 방법입니다. <!--Starting 19.4, the use of the Campaign API and interface for access and delete requests is deprecated. For more on Campaign Standard deprecated and removed features, refer to [this page](../../rn/using/deprecated-features.md).-->

개인 정보 보호 요청은 **POST** 요청.

요청을 만들기 전에 사용할 네임스페이스를 정의해야 합니다. 자세한 내용은 [개인 정보 관리 설명서](../../start/using/privacy-requests.md).

페이로드에는 다음 매개 변수가 포함되어야 합니다.

* **이름**: 고유한 내부 이름
* **namespace**: Campaign Standard 인터페이스에 구성된 네임스페이스 이름
* **reconciliationValue**: 네임스페이스에 정의된 조정 키를 기반으로 하는 조정 값
* **레이블**: 요청 레이블
* **유형**: 요청 유형입니다. 허용되는 값은 &quot;access&quot; 또는 &quot;delete&quot;입니다.
* **규정**: 규정 유형. 예: &quot;GDPR&quot;, &quot;CCPA&quot;. 이 매개 변수는 필수 항목이며 Campaign Standard 19.4 릴리스부터 사용할 수 있습니다. 이전 빌드를 사용하는 경우 페이로드에 추가할 필요가 없습니다.

<br/>

***샘플 요청***

이 POST 요청은 AMCDS2 네임스페이스에 정의된 전자 메일 조정 키를 기반으로 개인 정보 보호 요청을 만듭니다.

```
-X POST https://mc.adobe.io/<ORGANIZATION>/campaign/privacy/privacyTool \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-H 'Content-Type: application/json;charset=utf-8'

{
"name":"PT11832",
"namespaceName": "AMCDS2",
"reconciliationValue": "customers@adobe.com",
"regulation": "gdpr",
"label":"Delete customers",
"type":"delete"
}
```

POST 요청에 대한 응답입니다.

```
{
    "PKey": "<PKEY>",
    "audit": "",
    "created": "2018-03-21 10:41:58.570Z",
    "desc": "",
    "gdprRequestData": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/head/privacyTool/<PKEY>/gdprRequestData/"
    },
    "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/privacy/privacyTool/<PKEY>",
    "label": "Delete customers",
    "lastModified": "2018-03-21 10:41:58.570Z",
    "name": "PT11832",
    "namespace": {
        "PKey": "<PKEY>",
        "title": "Doc (AMCDS2)"
    },
    "namespaceName": "AMCDS2",
    "reconciliationValue": "customers@adobe.com",
    "regulation": "gdpr",
    "retryCount": 0,
    "status": "new",
    "title": "Delete customers (PT11832)",
    "type": "delete"
}
```
