---
title: 개인 정보 요청 만들기
description: API를 사용하여 개인 정보 보호 요청을 만드는 방법 살펴보기
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
source-git-commit: aee0e0437cbfe578cb2f715a2433099c79dd1748

---


# 개인 정보 요청 만들기 {#creating-a-privacy-request}

>[!CAUTION]
>
>개인정보 [보호 핵심 서비스](https://adobe.io/apis/cloudplatform/gdpr.html) 통합은 모든 액세스 및 삭제 요청에 사용해야 하는 방법입니다. 19.4부터 액세스 및 삭제 요청에 대한 캠페인 API 및 인터페이스 사용은 더 이상 사용되지 않습니다. Campaign Standard의 가치 하락 및 제거 기능에 대한 자세한 내용은 [이 페이지를](https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html)참조하십시오.

개인 정보 요청은 POST 요청을 사용하여 **만들어집니다** .

요청을 만들기 전에 사용할 네임스페이스를 정의해야 합니다. 자세한 내용은 개인 정보 [관리 설명서를](https://helpx.adobe.com/campaign/kb/acs-privacy.html#ManagingPrivacyRequests)참조하십시오.

페이로드에는 다음 매개 변수가 포함되어야 합니다.

* **이름**:고유한 내부 이름
* **네임스페이스**:캠페인 표준 인터페이스에 구성된 네임스페이스 이름
* **rechationValue**:네임스페이스에 정의된 조정 키를 기반으로 하는 조정 값
* **레이블**:요청 레이블
* **유형**:요청 유형. 허용된 값은 "access" 또는 "delete"입니다.
* **규정**:규정 유형. 예:"GDPR", "CCPA". 이 매개 변수는 필수이며 Campaign Standard 19.4 릴리스를 시작할 수 있습니다. 이전 빌드에 있는 경우 페이로드에 추가할 필요가 없습니다.

<br/>

***샘플 요청***

이 POST 요청은 네임스페이스 AMCDS2에 정의된 이메일 조정 키를 기반으로 개인 정보 보호 요청을 만듭니다.

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
