---
title: API 액세스 설정
description: Campaign Standard API에 대한 액세스 권한을 설정하는 방법을 알아봅니다.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: Data Engineer
level: Experienced
exl-id: efbbd0cd-9c56-4ad0-8bcb-efba4b63c28b
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 1%

---

# API 액세스 설정 {#setting-up-api-access}

Adobe Campaign Standard API 액세스는 아래 단계를 통해 설정됩니다. 이러한 각 단계는 [Adobe IO 설명서](https://www.adobe.io/authentication/auth-methods.html#!AdobeDocs/adobeio-auth/master/AuthenticationOverview/ServiceAccountIntegration.md)에 자세히 설명되어 있습니다.

>[!IMPORTANT]
>
>Adobe IO에서 인증서를 관리하려면 조직에 <b>시스템 관리자</b> 권한이 있거나 Admin Console에 [개발자 계정](https://helpx.adobe.com/enterprise/using/manage-developers.html)</a>이 있는지 확인하십시오.

1. **디지털 인증서가 있는지** 확인하거나 필요한 경우 디지털 인증서를 만듭니다. 인증서와 함께 제공된 공개 및 개인 키는 다음 단계에 필요합니다.
1. **Adobe Campaign Service** Adobe IO에 대한 새로운 통합을 만들고 구성합니다. 그러면 자격 증명이 생성됩니다(API 키, 클라이언트 암호...).
1. **이전에 생성된 자격 증명에서 JWT(JSON 웹 토큰)** 을 만들고 개인 키로 서명합니다. JWT는 Adobe이 ID를 확인하고 API에 대한 액세스 권한을 부여하는 데 필요한 모든 ID 및 보안 정보를 인코딩합니다.
1. **POST 요청을 통해 액세스** 토큰과 JWT를 교환합니다. 이 액세스 토큰은 API 요청의 각 헤더에서 사용해야 합니다.

보안 서비스 간 Adobe I/O API 세션을 설정하려면 Adobe 서비스에 대한 모든 요청은 인증 헤더에 아래 정보를 포함해야 합니다.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

* **&lt;organization>**: 개인 조직 ID이며, 각 인스턴스에 대해 Adobe이 하나의 조직 ID를 제공합니다.

   * &lt;organization> : 프로덕션 인스턴스,
   * &lt;organization-mkt-stage>: 스테이지 인스턴스입니다.

   조직 ID 값을 얻으려면 관리자 또는 Adobe 기술 담당자에게 문의하십시오. 새 통합을 생성할 때 라이센스 목록에서 Adobe I/O으로 검색할 수도 있습니다( <a href="https://www.adobe.io/authentication.html">Adobe IO 설명서</a> 참조).

* **&lt;access_token>**: POST 요청을 통해 JSON 웹 토큰을 교환할 때 검색된 개인 액세스 토큰입니다.

* **&lt;api_key>**: 개인 API 키 를 참조하십시오. Adobe Campaign 서비스에 대한 새 통합을 만든 후 Adobe I/O에 제공됩니다.

   ![대체 텍스트](assets/tenant.png)

## 문제 해결

AdobeIO 통합 중에 다음 오류가 표시되는 경우:

```
{ 
"code": 502, 
"message": "Oops. Something went wrong. Check your URI and try again." 
}
```


CNAME 매개 변수가 올바르게 만들어졌는지 확인하려면 관리자 또는 Adobe 기술 담당자에게 문의하십시오.
