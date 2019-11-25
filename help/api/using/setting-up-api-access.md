---
title: API 액세스 설정
description: Campaign Standard API에 대한 액세스를 설정하는 방법을 알아봅니다.
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


# API 액세스 설정 {#setting-up-api-access}

Adobe Campaign Standard API 액세스는 아래 단계를 통해 설정됩니다. 이러한 각 단계는 Adobe IO [설명서에서](https://www.adobe.io/authentication/auth-methods.html#!AdobeDocs/adobeio-auth/master/AuthenticationOverview/ServiceAccountIntegration.md)자세히 설명합니다.

>[!CAUTION]
>
>Adobe IO에서 인증서를 관리하려면 <b>조직 또는</b> 개발자 계정에 <a href="https://helpx.adobe.com/enterprise/using/manage-developers.html">대한 시스템 관리자</a> 권한이 있어야 합니다.

1. **디지털 인증서가**&#x200B;있는지 확인하거나 필요한 경우 디지털 인증서를 만듭니다. 다음 단계에서는 인증서와 함께 제공된 공개 및 개인 키가 필요합니다.
1. **Adobe IO에서 Adobe Campaign** Service에 대한 새로운 통합을 만들어 구성합니다. 자격 증명이 생성됩니다(API 키, 클라이언트 암호...).
1. **이전에 생성된 자격 증명에서 JWT(JSON Web Token)** 를 만들어 개인 키로 서명합니다. JWT는 Adobe가 ID를 확인하고 API에 대한 액세스 권한을 부여하는 데 필요한 모든 ID 및 보안 정보를 인코딩합니다.
1. **POST 요청을 통해 JWT를 액세스** 토큰으로 교환합니다. 이 액세스 토큰은 API 요청의 각 헤더에서 사용해야 합니다.

안전한 Service-to-Service Adobe I/O API 세션을 설정하려면 Adobe 서비스에 대한 모든 요청은 인증 헤더에 아래 정보가 포함되어야 합니다.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

* **&lt;조직&gt;**:이것은 귀하의 개인 조직 ID이며, Adobe가 각 인스턴스에 대해 하나의 조직 ID를 제공합니다.

   * &lt;조직&gt;:프로덕션 인스턴스,
   * &lt;ORGANIZATION-mkt-stage&gt;:스테이지 인스턴스.
   조직 ID 값을 얻으려면 관리자 또는 Adobe 기술 담당자에게 문의하십시오. 또한 새로운 통합을 만들 때 Adobe I/O로 가져올 수 있습니다(라이선스 목록 참조). Adobe IO <a href="https://www.adobe.io/authentication.html">설명서</a>참조).

* **&lt;ACCESS_TOKEN&gt;**:POST 요청을 통해 JSON 웹 토큰을 교환할 때 검색된 개인 액세스 토큰입니다.

* **&lt;API_KEY&gt;**:개인 API 키 Adobe Campaign Service에 대한 새 통합을 만든 후 Adobe I/O에서 제공됩니다.

   ![대체 텍스트](assets/tenant.png)
