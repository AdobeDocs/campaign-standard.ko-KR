---
solution: Campaign Standard
product: campaign
title: API 액세스 설정
description: Campaign Standard API에 대한 액세스를 설정하는 방법을 알아봅니다.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 1%

---


# API 액세스 설정 {#setting-up-api-access}

Adobe Campaign Standard API 액세스는 아래 단계를 통해 설정됩니다. 이러한 각 단계는 [Adobe IO 설명서에 자세히 설명되어 있습니다](https://www.adobe.io/authentication/auth-methods.html#!AdobeDocs/adobeio-auth/master/AuthenticationOverview/ServiceAccountIntegration.md).

>[!IMPORTANT]
>
>Adobe IO에서 인증서를 관리하려면 조직 또는 <b>개발자 계정에</b> 대한 시스템 관리자 [권한이 있어야 합니다. 관리 콘솔에서는](https://helpx.adobe.com/enterprise/using/manage-developers.html)</a> 개발자 계정이관리되어야 합니다.

1. **디지털 인증서가 있는지**&#x200B;확인하거나 필요한 경우 디지털 인증서를 만듭니다. 인증서와 함께 제공된 공개 및 개인 키는 다음 단계에 필요합니다.
1. **Adobe IO에서 Adobe Campaign 서비스에** 대한 새로운 통합을 만들고 구성합니다. 그러면 자격 증명이 생성됩니다(API 키, 클라이언트 암호...).
1. **이전에 생성된 자격 증명에서 JWT(JSON Web Token)** 을 만들어 개인 키로 서명합니다. JWT는 Adobe이 ID를 확인하고 API에 대한 액세스 권한을 부여하는 데 필요한 모든 ID 및 보안 정보를 인코딩합니다.
1. **POST 요청을 통해 JWT를 액세스 토큰과** 교환합니다. 이 액세스 토큰은 API 요청의 각 헤더에서 사용해야 합니다.

안전한 서비스 간 Adobe I/O API 세션을 설정하려면 Adobe 서비스에 대한 모든 요청은 인증 헤더에 아래 정보가 포함되어야 합니다.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

* **&lt;조직>**:개인 조직 ID이며, 각 인스턴스에 대해 Adobe에서 하나의 조직 ID가 제공됩니다.

   * &lt;조직>:프로덕션 인스턴스,
   * &lt;ORGANIZATION-mkt-stage>:스테이지 인스턴스.

   조직 ID 값을 얻으려면 관리자 또는 Adobe 기술 담당자에게 문의하십시오. 새 통합을 만들 때 Adobe I/O로 가져올 수도 있습니다(라이선스 목록에서 <a href="https://www.adobe.io/authentication.html">Adobe IO 설명서</a>참조).

* **&lt;ACCESS_TOKEN>**:POST 요청을 통해 JSON 웹 토큰을 교환할 때 검색된 개인 액세스 토큰입니다.

* **&lt;API_KEY>**:개인 API 키. Adobe Campaign 서비스에 대한 새로운 통합을 만든 후 Adobe I/O에서 제공됩니다.

   ![대체 텍스트](assets/tenant.png)

## 문제 해결

AdobeIO를 통합하는 동안 다음 오류가 표시되는 경우:

```
{ 
"code": 502, 
"message": "Oops. Something went wrong. Check your URI and try again." 
}
```


CNAME 매개 변수가 올바르게 작성되었는지 확인하려면 관리자 또는 Adobe 기술 담당자를 참조하십시오.