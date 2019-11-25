---
title: 개인 정보 관리
description: API를 사용한 개인 정보 관리에 대한 자세한 내용
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
source-git-commit: c0c0be79613f99a15676343d8ce10d335baf968a

---


# 개인 정보 관리 {#privacy-management}

Campaign Standard API는 GDPR 및 CCPA와 같은 개인 정보 보호 규정과 관련된 요청의 자동 프로세스를 허용하는 기능을 제공합니다.

수행할 수 있는 작업은 다음과 같습니다.

* 새로운 개인 정보 보호 요청 만들기,
* 개인 정보 보호 요청 모니터링,
* 개인 정보 데이터 파일 검색,
* 프로필의 CCPA 옵트아웃 상태를 관리합니다.

개인 정보 API 끝점은 **/privacy/privacyTool입니다**. 개인정보 보호도구 리소스 설명 및 관련 필터는 리소스 메타데이터에서 사용할 수 있습니다. 메타데이터 [메커니즘을 참조하십시오](../../api/using/metadata-mechanism.md).

CPA 옵트아웃은 cpaOptOut 프로필 속성을 사용하여 **관리됩니다** .

Adobe Campaign Standard 및 개인 정보 보호에 대한 자세한 내용은 [전용 설명서를](https://helpx.adobe.com/campaign/kb/acs-privacy.html)참조하십시오.

## 개인 정보 요청 만들기 {#creating-a-privacy-request}

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

## 개인 정보 요청 모니터링

GET 요청을 사용하여 생성된 개인 정보 요청에 대한 정보를 모니터링할 **수** 있습니다.

상태 목록 설명은 개인 정보 [관리 문서에서](https://helpx.adobe.com/campaign/kb/acs-privacy.html#ManagingPrivacyRequests)사용할 수 있습니다.

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

## 개인 정보 데이터 파일 검색

>[!CAUTION]
>
>개인정보 [보호 핵심 서비스](https://adobe.io/apis/cloudplatform/gdpr.html) 통합은 모든 액세스 및 삭제 요청에 사용해야 하는 방법입니다. 19.4부터 액세스 및 삭제 요청에 대한 캠페인 API 및 인터페이스 사용은 더 이상 사용되지 않습니다. Campaign Standard의 가치 하락 및 제거 기능에 대한 자세한 내용은 [이 페이지를](https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html)참조하십시오.

조정 값에 연결된 모든 정보가 포함된 파일을 검색하려면 다음 3단계 절차를 따르십시오.

1. POST **요청을 수행하여** 속성 **type="access"**&#x200B;로 새 요청을 만듭니다 [.](#creating-a-privacy-request)새 개인 정보 요청만들기를 참조하십시오.

1. GET **요청을** 수행하여 요청에 대한 정보를 검색합니다.

1. 반환된 개인 정보 **RequestData URL에 대해 POST****** 요청을 수행하고 페이로드 내에 개인 정보 요청 내부 이름을 사용하여 데이터 파일을 검색합니다. 예:{"name":"PT17"}.

<br/>

***샘플 요청***

type="access" 특성을 사용하여 개인 정보 요청을 만듭니다.

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
"type":"access"
}
```

<!-- + réponse -->

GET 요청을 수행하여 요청에 대한 정보를 검색합니다.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/privacy/privacyTool \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-H 'Content-Type: application/json;charset=utf-8'
```

연결된 URL과 함께 privacyRequestData 속성을 반환합니다.

```
{
    ...
    "name": "PR2",
    "namespace": ...,
    "namespaceName": "defaultNamespace1",
    "privacyRequestData": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/privacy/privacyTool/<PKEY>/privacyRequestData/"
    },
    "reconciliationValue": "johndoe@mail.com",
    "regulation": "gdpr",
    "retryCount": 0,
    "status": "complete",
    "title": "EPR (PR2)",
    "type": "access"
    ...
},
```

privacyRequestData URL에 대한 POST 요청을 수행하고 페이로드 내에 요청 내부 이름을 사용합니다.

```
-X POST https://mc.adobe.io/<ORGANIZATION>/campaign/privacy/privacyTool/<PKEY>/privacyRequestData \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-H 'Content-Type: application/json;charset=utf-8'
-d '{"name": "PR1"}'
```

파일 내용을 반환합니다.

```
"{data:<gdprRequestData _cs=\" ()\" id=\"8565163\" reconciliationValue=\"'customer@adobe.com'\">\n  <table name=\"nms:recipient\">\n    <rowId='8569152'\n\t\tlastName='customer'\n\t\tfirstName='customer'\n\t\tgender='1'\n\t\temail='customer@adobe.com'\n\t\tcreatedBy-id='8565162'\n\t\tmodifiedBy-id='8565162'\n\t\tlastModified='2018-03-15 13:54:28.708Z'\n\t\tcreated='2018-03-15 13:54:28.708Z'\n\t\tthumbnail='/nl/img/thumbnails/defaultProfil.png'\n\t\temailFormat='2'</row>\n  </table>\n  <table name=\"nms:broadLogRcp\">\n    <row>deliveryLabel='Send via email'\n\t\tdeliveryType='0'\n\t\tcontactDate='2018-03-15 13:58:31.667Z'\n\t\tid='8003'\n\t\taddress='customer@adobe.com'\n\t\tstatus='1'\n\t\tmsg-id='1194'\n\t\teventDate='2018-03-15 13:58:34.726Z'\n\t\tlastModified='2018-03-15 13:59:02.008Z'\n\t\tvariant='default'\n\t\tdelivery-id='8569153'\n\t\tpublicId='1'\n\t\tprofile-id='8569152'</row>\n  </table>\n  <table name=\"nms:trackingLogRcp\">\n    <row>deliveryLabel='Send via email'\n\t\tdeliveryType='0'\n\t\tcontactDate='2018-03-15 13:58:31.667Z'\n\t\turlLabel='Open'\n\t\turlSource=''\n\t\tuserAgent='-1178080215'\n\t\ttrackedDevice='pc'\n\t\tid='5000'\n\t\tlogDate='2018-03-15 14:00:51.650Z'\n\t\tsourceType='html'\n\t\tuserAgent='-1178080215'\n\t\turl-id='1'\n\t\tdelivery-id='8569153'\n\t\tbroadLog-id='8003'\n\t\trecipient-id='8569152'</row>\n    <row>deliveryLabel='Send via email'\n\t\tdeliveryType='0'\n\t\tcontactDate='2018-03-15 13:58:31.667Z'\n\t\turlLabel='Open'\n\t\turlSource=''\n\t\tuserAgent='0'\n\t\ttrackedDevice=''\n\t\tid='6000'\n\t\tlogDate='2018-03-15 16:00:41.110Z'\n\t\tsourceType='html'\n\t\turl-id='1'\n\t\tdelivery-id='8569153'\n\t\tbroadLog-id='8003'\n\t\trecipient-id='8569152'</row>\n  </table>\n</gdprRequestData>}"
```

## CPA 옵트아웃 관리

cpaOptOut 프로필 속성 및 "true" 또는 " **false" 값을 사용하여 프로필의** CCPA 옵트아웃 상태를 모니터링하고 관리할 수 있습니다.

`"ccpaOptOut": <value>`

* **true**: 개인 정보의 판매를 금지하다.
* **false**:개인 정보의 판매를 승인합니다.

>[!CAUTION]
>
>"CPA 옵트아웃" 속성은 19.4부터 사용할 수 있습니다.19.3 환경의 경우 프로필 리소스를 확장하고 부울 필드를 추가해야 합니다. 이 필드는 선택한 레이블과 함께 API에 추가됩니다. "CCPA에 대한 옵트아웃"을 사용하는 것이 좋습니다.
>
>자세한 내용은 개인 정보 [관리 설명서를](https://helpx.adobe.com/campaign/kb/acs-privacy.html#ccpa)참조하십시오.

<br/>

***샘플 요청***

* 프로필의 CCPA 옵트아웃 상태를 검색하기 위한 샘플 GET 요청.

   ```
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profilesAndServices/profile/<PKEY> \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>' \
   -H 'Content-Type: application/json;charset=utf-8'
   ```

   GET 요청에 대한 응답입니다.

   ```
   {
   "PKey": "<PKEY>",
     "ccpaOptOut": false,
     "firstName": "John",
     "lastName": "Doe",
   ...
   }
   ```

* CPA 옵트아웃을 위해 프로필을 표시하는 샘플 POST 요청.

   ```
   -X POST https://mc.adobe.io/<ORGANIZATION>/campaign/profilesAndServices/profile/ \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>' \
   -H 'Content-Type: application/json;charset=utf-8'
   -i
   -d {
   -d  "firstName": "John",
   -d  "lastName": "Doe",
   -d  "email": "jdoe@mail.com",
   -d  "ccpaOptOut": true
   -d }'
   ```

   GET 요청에 대한 응답입니다.

   ```
   {
       ...
       "email": "john.doe@mail.com",
       "firstName": "John",
       "lastName": "Doe",
       "ccpaOptOut": true,
       ...
   }
   ```

* CPA 옵트아웃을 위한 프로파일 업데이트를 위한 샘플 패치 요청

   ```
   -X PATCH https://mc.adobe.io/<ORGANIZATION>/campaign/profilesAndServices/profile/<PKEY> \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>' \
   -H 'Content-Type: application/json;charset=utf-8'
   -i
   -d {
   -d  "ccpaOptOut": true
   -d }'
   ```

   GET 요청에 대한 응답입니다.

   ```
   {
       ...
       "email": "john.doe@mail.com",
       "firstName": "John",
       "lastName": "Doe",
       "ccpaOptOut": true,
       ...
   }
   ```
