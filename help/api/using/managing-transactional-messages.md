---
solution: Campaign Standard
product: campaign
title: 트랜잭션 메시지 관리
description: API를 사용하여 트랜잭션 메시지를 관리하는 방법을 알아봅니다.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
translation-type: tm+mt
source-git-commit: fc755f3176622e1faf08ccfa4236e016110f9a68
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 3%

---


# 트랜잭션 메시지 관리 {#managing-transactional-messages}

## 트랜잭션 메시지 기본 정보

트랜잭션 이벤트를 만들고 게시한 후에는 이 이벤트의 트리거를 웹 사이트에 통합해야 합니다.

>[!NOTE]
>
>이벤트 구성은 [이 섹션](../../channels/using/configuring-transactional-event.md)에 나와 있습니다.

예를 들어 고객이 장바구니에서 제품을 구매하기 전에 웹 사이트를 떠날 때마다 &quot;장바구니 포기&quot; 이벤트를 트리거해야 합니다. 이렇게 하려면 웹 개발자가 REST 트랜잭션 메시지 API를 사용해야 합니다.

1. 개발자는 트랜잭션 이벤트](#sending-a-transactional-event)의 [전송을 트리거하는 POST 메서드에 따라 요청을 보냅니다.
1. POST 요청에 대한 응답에는 개발자가 GET 요청을 통해 하나 이상의 요청을 전송할 수 있는 기본 키가 포함되어 있습니다. 이렇게 하면 [이벤트 상태](#transactional-event-status)를 얻을 수 있습니다.

## 트랜잭션 이벤트 {#sending-a-transactional-event} 전송

트랜잭션 이벤트는 다음 URL 구조를 가진 POST 요청을 통해 전송됩니다.

```
POST https://mc.adobe.io/<ORGANIZATION>/campaign/<transactionalAPI>/<eventID>
```

* **&lt;organization>**:개인 조직 ID. [이 섹션](../../api/using/must-read.md)을 참조하십시오.

* **&lt;transactionalapi>**:트랜잭션 메시지 API 종료 지점.

   트랜잭션 메시지 API 끝점의 이름은 인스턴스 구성에 따라 다릅니다. &quot;mc&quot; 값 다음에 개인 조직 ID에 해당합니다. 조직 ID로 &quot;geometrixx&quot;를 사용하는 Geometrixx 회사의 예를 살펴보겠습니다. 이 경우 POST 요청은 다음과 같습니다.

   `POST https://mc.adobe.io/geometrixx/campaign/mcgeometrixx/<eventID>`

   (트랜잭션 메시지 API 끝점은 API 미리 보기 중에도 볼 수 있습니다.)

* **&lt;eventid>**:전송할 이벤트 유형입니다. 이 ID는 이벤트 구성을 만들 때 생성됩니다([이 섹션](../../channels/using/configuring-transactional-event.md#creating-an-event) 참조).

### POST 요청 헤더

요청에는 &quot;Content-Type:application/json&quot; 헤더.

**utf-8**&#x200B;과 같은 문자 집합을 추가해야 합니다. 이 값은 사용 중인 REST 응용 프로그램에 따라 다릅니다.

```
-X POST \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-H 'Content-Type: application/json;charset=utf-8' \
-H 'Content-Length:79' \
```

### POST 요청 본문

이벤트 데이터는 JSON POST 본문 내에 포함되어 있습니다. 이벤트 구조는 해당 정의에 따라 달라집니다. 리소스 정의 화면의 API 미리 보기 단추는 요청 샘플을 제공합니다. [이 섹션](../../channels/using/publishing-transactional-event.md#previewing-and-publishing-the-event)을 참조하십시오.

이벤트에 연결된 트랜잭션 메시지 전송을 관리하기 위해 이벤트 컨텐츠에 다음 선택적 매개 변수를 추가할 수 있습니다.

* **만료** (선택 사항):이 날짜 이후에는 트랜잭션 이벤트 전송이 취소됩니다.
* **예약됨** (선택 사항):이 날짜부터 트랜잭션 이벤트가 처리되고 트랜잭션 메시지가 전송됩니다.

>[!NOTE]
>
>&quot;만료&quot; 및 &quot;예약&quot; 매개 변수의 값은 ISO 8601 형식을 따릅니다. ISO 8601은 대문자인 &quot;T&quot;를 사용하여 날짜 및 시간을 구분합니다. 더 나은 가독성을 위해 입력이나 출력에서 제거할 수 있습니다.

### POST 요청에 대한 응답

POST 응답은 만들 때 트랜잭션 이벤트 상태를 반환합니다. 현재 상태(이벤트 데이터, 이벤트 상태..)를 검색하려면 GET 요청에서 POST 응답으로 반환된 기본 키를 사용합니다.

`GET https://mc.adobe.io/<ORGANIZATION>/campaign/<transactionalAPI>/<eventID>/`

<br/>

***샘플 요청***

이벤트 전송을 위한 POST 요청.

```
-X POST https://mc.adobe.io/<ORGANIZATION>/campaign/mcAdobe/EVTcartAbandonment \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-H 'Content-Type: application/json;charset=utf-8' \
-H 'Content-Length:79'

{
  "email":"test@example.com",
  "scheduled":"2017-12-01 08:00:00.768Z",
  "expiration":"2017-12-31 08:00:00.768Z",
  "ctx":
  {
    "cartAmount": "$ 125",
    "lastProduct": "Leather motorbike jacket",
    "firstName": "Jack"
  }
}
```

POST 요청에 대한 응답입니다.

```
{
  "PKey":"<PKEY>",
  "ctx":
  {
    "cartAmount": "",
    "lastProduct": "",
    "firstName": ""
  }
  "email":"",
  "scheduled":"2017-12-01 08:00:00.768Z",
  "expiration":"2017-12-31 08:00:00.768Z",
  "href": "mcAdobe/EVTcartAbandonment/<PKEY>",
  "serverUrl":" https://myserver.com ",
  "status":"pending",
  "type":""
}
```

### 트랜잭션 이벤트 상태 {#transactional-event-status}

응답에서 &quot;상태&quot; 필드를 사용하여 이벤트가 처리되었는지 여부를 알 수 있습니다.

* **보류 중**:이벤트가 보류 중입니다. 트리거된 경우 이벤트가 이 상태를 유지합니다.
* **처리**:이벤트가 배달 보류 중입니다. 메시지가 메시지로 변환되고 메시지가 전송됩니다.
* **일시 중지됨**:이벤트 프로세스가 일시 중지됩니다. 더 이상 처리되지 않지만 Adobe Campaign 데이터베이스의 대기열에 보관됩니다. 이 작업에 대한 자세한 정보는 [이 섹션](../../channels/using/publishing-transactional-message.md#suspending-a-transactional-message-publication)을 참조하십시오.
* **처리됨**:이벤트가 처리되고 메시지가 성공적으로 전송되었습니다.
* **무시됨**:이 이벤트는 배달 과정에서 무시되었습니다. 이 경우 일반적으로 주소가 격리될 때 사용됩니다.
* **deliveryFailed**:이벤트를 처리하는 동안 배달 오류가 발생했습니다.
* **routingFailed**:라우팅 단계가 실패했습니다. 지정된 이벤트 유형을 찾을 수 없는 경우 이 문제가 발생할 수 있습니다.
* **tooOld**:이벤트를 처리할 수 있기 전에 만료됨 - 여러 가지 이유로 인해 전송이 여러 번 실패하는 경우(이 경우 이벤트가 더 이상 최신 상태가 되지 않는 경우) 또는 서버가 오버로드된 후 이벤트를 더 이상 처리할 수 없는 경우 등이 발생할 수 있습니다.
* **targetingFailed**:Campaign Standard이 메시지 타깃팅에 사용되는 링크를 강화하지 못했습니다.
