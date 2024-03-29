---
title: API 액세스 설정
description: Campaign Standard API에 대한 액세스를 설정하는 방법을 알아봅니다.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: Data Engineer
level: Experienced
exl-id: efbbd0cd-9c56-4ad0-8bcb-efba4b63c28b
source-git-commit: 7ca7e9bd9541a4db708565e65e2ff87e44393238
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 10%

---

# API 액세스 설정 {#setting-up-api-access}

Adobe Campaign Standard API 액세스는 아래 단계를 통해 설정됩니다. 이러한 각 단계는 [Adobe Developer 설명서](https://developer.adobe.com/developer-console/docs/guides/#!AdobeDocs/adobeio-auth/master/AuthenticationOverview/ServiceAccountIntegration.md).

>[!IMPORTANT]
>
>에서 인증서를 관리하려면 [Adobe Developer](https://developer.adobe.com/), 다음을 확인하십시오. **시스템 관리자** 조직 또는 a에 대한 권한 [개발자 계정](https://helpx.adobe.com/enterprise/using/manage-developers.html) Admin Console.

1. **디지털 인증서가 있는지 확인**&#x200B;또는 필요한 경우 만드십시오. 인증서와 함께 제공되는 공개 및 개인 키는 다음 단계에서 필요합니다.
1. **Adobe Campaign 서비스에 대한 새 통합 만들기** 위치: [Adobe Developer](https://developer.adobe.com/) 및 를 구성합니다. 그러면 자격 증명이 생성됩니다(API 키, 클라이언트 암호...).
1. **JSON 웹 토큰(JWT) 생성** 이전에 생성한 자격 증명에서 개인 키로 서명합니다. JWT는 Adobe이 사용자의 ID를 확인하고 API에 대한 액세스 권한을 부여하는 데 필요한 모든 ID 및 보안 정보를 인코딩합니다.

   >[!AVAILABILITY]
   >
   >현재 JWT(JSON 웹 토큰)의 지원 종료를 준비하고 있으며, 이를 OAuth로 대체하는 과정이 진행 중입니다. Campaign의 예정된 릴리스 내에서 이 전환을 점진적으로 수행하며, 설명서에 이러한 업데이트를 반영하여 업데이트합니다.

1. **JWT를 액세스 토큰으로 교환** POST 요청을 통해 이 액세스 토큰은 API 요청의 각 헤더에서 사용해야 합니다.

보안 서비스 간 Adobe I/O API 세션을 설정하려면 Adobe 서비스에 대한 모든 요청에서 아래 정보를 인증 헤더에 포함해야 합니다.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

* **&lt;organization>**: 개인 조직 ID이며, 각 인스턴스에 대해 Adobe이 제공한 조직 ID가 하나입니다.

   * &lt;organization> : 프로덕션 인스턴스,
   * &lt;organization-mkt-stage>: 스테이지 인스턴스

  조직 ID 값을 얻으려면 관리자 또는 Adobe 기술 담당자에게 문의하십시오. 라이선스 목록에서 새 통합을 만들 때 Adobe I/O으로 검색할 수도 있습니다( <a href="https://developer.adobe.com/developer-console/docs/guides/authentication/">Adobe Developer 설명서</a>).

* **&lt;access_token>**: POST 요청을 통해 JSON 웹 토큰을 교환할 때 검색된 개인 액세스 토큰입니다.

* **&lt;api_key>**: 개인 API 키. Adobe Campaign 서비스에 대한 새 통합을 만든 후 Adobe I/O에서 제공합니다.

  ![대체 텍스트](assets/tenant.png)

## 문제 해결

AdobeIO 통합 중에 다음 오류가 나타나면

```
{ 
"code": 502, 
"message": "Oops. Something went wrong. Check your URI and try again." 
}
```


CNAME 매개 변수가 올바르게 생성되었는지 확인하려면 관리자 또는 Adobe 기술 담당자에게 문의하십시오.
