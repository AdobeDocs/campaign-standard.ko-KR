---
title: 문제 해결
description: Campaign Standard API와 관련된 일반적인 문제에 대해 자세히 알아보십시오.
page-status-flag: never-activated
uuid: c7b9c171-0409-4707-9d45-3fa72aee8008
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: use-case--extending-the-api
discoiquuid: 304e7779-42d2-430a-9704-8c599a4eb1da
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: ab5725b326de2f1cb4c5d15d0d3c0303a6bf0f06

---


# 문제 해결 {#troubleshooting}

* **Adobe.io 콘솔로 이동할 때 다음 오류가 표시됩니다."Adobe I/O 콘솔은 기업 계정의 구성원을 선택할 수만 있습니다. 액세스 권한이 있다고 생각되는 경우 시스템 관리자에게 문의하십시오."**

관리하는 IMS 조직에만 API 키를 만들 수 있습니다. 이 메시지가 표시되고 API 키를 만들려면 IMS 조직의 관리자에게 문의하십시오.

* **Adobe.io에 대한 요청을 할 때 {"error_code":"403023","message":"프로필이 잘못되었습니다"}**

즉, 특정 Campaign 제품의 IMS 프로비저닝에 문제가 있습니다.IMS 팀이 해결해야 합니다.

자세한 내용은 토큰과 함께 IMS API를 호출하여 IMS 프로필의 모양을 확인할 수 있습니다.요청을 라우팅하려면 organization_id가 Adobe.io에 입력한 URL과 동일한 prodCtx가 있어야 합니다.
IMS 프로비저닝을 수정해야 하는 경우

```
-X GET https://mc.adobe.io/{ORGANIZATION}/campaign/profileAndServices/profile \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

다음 오류를 반환합니다.

```
{"error_code":"403023","message":"Profile is not valid"}
```

이 요청으로 IMS 프로필을 확인하십시오.

```
-X GET https://ims-na1.adobelogin.com/ims/profile/v1 \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

응답에서 ORGANIZATION_ID 값은 첫 번째 GET 요청에서 동일해야 합니다.

```
{
  "countryCode": "FR",
  "mrktPermEmail": null,
  "projectedProductContext": [
    {
    "prodCtx": {
      "statusCode": "ACTIVE",
      "ident": "ZQ9FRQK7BF09YXAESFY9DDQP1G",
      "modDts": 1448307260000,
      "organization_id": "actest",
      "owningEntity": "6096892F54B5819E0A4C98A2@AdobeOrg",
      "serviceCode": "dma_tartan",
      "label": "Adobe Marketing Cloud",
      "serviceLevel": "standard",
      "createDts": 1421181343000,
      "deal_id": " "
      }
    }
  ]
}
```

* **Adobe.io에 대한 요청을 할 때 {"code":500, "message":"Ook. 문제가 발생했습니다. URI를 확인하고 다시 시도하십시오."}**

Adobe.io는 유효하지 않은 URI를 선언합니다.요청하려는 URI가 유효하지 않을 가능성이 높습니다. Adobe.io에서 Campaign 서비스를 선택하면 가능한 organization_ids 목록이 있는 선택기가 표시됩니다. URL에 입력하는 것이 선택되었는지 확인해야 합니다.

* **Adobe.io에 대한 요청을 할 때 {"error_code":"401013","message":"Oauth 토큰이 잘못되었습니다"}**

토큰이 잘못되었거나(토큰을 생성하는 데 사용된 부적절한 IMS 호출) 토큰이 만료되었습니다.

* **작성 후 프로필이 표시되지 않음**

인스턴스 구성에 따라 생성된 프로파일을 orgUnit에 연결해야 **합니다**. 작성에서 이 필드를 추가하는 방법을 이해하려면 [이 섹션을](../../api/using/managing-profiles.md)참조하십시오.

<!-- * (error duplicate key : quand tu crées un profile qui existe déjà , il faut faire un patch pour updater le profile plutôt qu’un POST)

With Curl
List all profiles

Create a profile

Update the mobilePhone attribute of a profile

API Calls on Service

GET the list of services

-->

<!--

How to find and use a filter?
Error codes:

* PAtch sur Age = message d'erreur :
500
Cannot update the 'age' property that is read-only
'age' property is not valid for the 'profile' resource.
-->

<!--
How to filter a list of subscribed profiles with available profile filters ? by date (by les filtres dispo sur la ressource) ?

Pattern classique :

recupérer la liste des subscriptions filtrées d'un profile
1) get sur profile
2) recup PKey
3) get sur PKey
4) get sur href des subscriptions

Comment savoir quel filtre appliquer ?

1) get sur metadata de profile
2) retourne description de la collection subscription
3) get sur la valeur du champ resTarget
4) get sur le href dans filters
5) retourne les filtres applicables sur l'url des data.

-->
