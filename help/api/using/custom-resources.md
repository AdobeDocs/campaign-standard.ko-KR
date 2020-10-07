---
title: 사용자 정의 리소스
description: API를 사용한 사용자 정의 리소스 관리에 대한 자세한 내용/
page-status-flag: never-activated
uuid: c7b9c171-0409-4707-9d45-3fa72aee8008
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
discoiquuid: 304e7779-42d2-430a-9704-8c599a4eb1da
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 5%

---


# 사용자 정의 리소스 {#custom-resources}

Adobe Campaign은 서로 다른 리소스를 통해 데이터를 정의하는 사전 정의된 데이터 모델을 제공합니다. 리소스를 확장하여 사용자 정의 필드나 구매 또는 제품 테이블과 같은 사용자 정의 테이블을 추가하여 제공되는 데이터 모델을 보강할 수 있습니다.

사용자 지정 리소스는 **/profileAndServicesExt** 끝점과 사용자 지정 리소스 이름을 사용하여 API를 통해 액세스할 수 있습니다.

`https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/<resourceName>/`

>[!NOTE]
>
>기본적으로 제공되지 않는 리소스의 경우 리소스 이름 앞에 <b>&quot;cus&quot;</b> 접두어를 항상 사용하십시오.

프로필 테이블에 연결되어 있는 경우 사용자 지정 리소스로 모든 작업을 수행할 수 있습니다. 예를 들어 아래 표 구조를 고려해 보겠습니다.

![대체 텍스트](assets/cusresources.png)

이 경우 ProfileTable에 연결된 한 **Transaction**, **TransactionDetails** 및 **제품****테이블의 모든 리소스를 사용할 수** 있습니다.

<br/>

***샘플 요청***

확장 profileAndServicesExt 리소스에 액세스하기 위한 샘플 GET 요청입니다.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/\
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
```

연결된 모든 사용자 지정 리소스 목록을 반환합니다. 그런 다음 리소스 URL을 사용하여 이 설명서에 설명된 모든 API 작업을 수행할 수 있습니다.

```
{
"apiName": "resourceType",
"cusProduct": {
        "content": ...,
        "data": "/profileAndServicesExt/cusProduct/",
        "help": "Product",
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/cusProduct/metadata",
        "name": "cusProduct",
        "type": "collection"
    },
"cusTransaction": {
        "content": ...,
        "data": "/profileAndServicesExt/cusTransaction/",
        "help": "Product",
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/cusTransaction/metadata",
        "name": "cusProduct",
        "type": "collection"
    },
    ...
}
```

데이터 모델 익스텐션에 대한 자세한 내용은 캠페인 설명서를 참조하십시오.

* [데이터 모델 기본 개념](../../developing/using/data-model-concepts.md)
* [API 확장](../../developing/using/about-extending-the-api.md)
* [다른 리소스와의 링크 정의](https://helpx.adobe.com/campaign/standard/developing/using/configuring-the-resource-s-data-structure.html#defining-links-with-other-resources)
