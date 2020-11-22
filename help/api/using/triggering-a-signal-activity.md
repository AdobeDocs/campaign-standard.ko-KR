---
solution: Campaign Standard
product: campaign
title: 신호 활동 트리거
description: API를 사용하여 신호 활동을 트리거하는 방법을 알아봅니다.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 2%

---


# 신호 활동 트리거 {#triggering-a-signal-activity}

Adobe Campaign Standard 워크플로우에서는 하나 이상의 **외부 신호** 활동이 있을 수 있습니다. 이러한 활동은 트리거되기를 기다리는 &#39;청취자&#39;입니다.

Campaign Standard API를 사용하면 **외부 신호** 활동을 트리거하여 워크플로우를 호출할 수 있습니다. API 호출에는 워크플로우의 이벤트 변수(타깃팅할 대상 이름, 가져올 파일 이름, 메시지 컨텐츠의 일부 등)로 인제스트될 매개 변수가 포함될 수 있습니다. 이렇게 하면 캠페인 자동화를 외부 시스템과 쉽게 통합할 수 있습니다.

>[!NOTE]
>
>외부 신호 활동은 10분마다 이상 트리거할 수 없으며 대상 워크플로우가 이미 실행되고 있어야 합니다.

워크플로우를 트리거하려면 아래 단계를 따르십시오.

1. 외부 신호 활동 트리거 URL을 검색하기 위해 워크플로우에서 **GET** 요청을 수행합니다.

   `GET https://mc.adobe.io/<ORGANIZATION>/campaign/workflow/execution/<workflowID>`

1. 반환된 URL에 **POST** 요청을 수행하여 신호 활동을 트리거하고 페이로드에 **&quot;source&quot;** 매개 변수를사용합니다. 이 속성은 필수이며, 트리거 요청 소스를 표시할 수 있습니다.

매개 변수를 사용하여 워크플로우를 호출하려면 **&quot;parameters&quot; 속성을 사용하여 페이로드에** 추가합니다. 구문은 매개 변수의 이름 뒤에 해당 값이 옵니다(다음 유형이 지원됩니다. **문자열**, **번호**, **부울** 및 **날짜/시간**).

```
  -X POST <TRIGGER_URL>
  -H 'Authorization: Bearer <ACCESS_TOKEN>' \
  -H 'Cache-Control: no-cache' \
  -H 'X-Api-Key: <API_KEY>' \
  -H 'Content-Type: application/json;charset=utf-8' \
  -H 'Content-Length:79' \
  -i
  -d {
  -d    "source":"<SOURCE>",
  -d    "parameters":{
  -d      "<PARAMETER_NAME":"<PARAMETER_VALUE>",
  -d      "<PARAMETER_NAME":"<PARAMETER_VALUE>",
  -d      "<PARAMETER_NAME":"<PARAMETER_VALUE>",  
  -d      "<PARAMETER_NAME":"<PARAMETER_VALUE>"
  -d    }
  -d }
```

>[!NOTE]
>
>페이로드에 매개 변수를 추가할 때는 **이름** 및 **유형** 값이 외부 신호 활동에서 선언된 정보와 일치하는지 확인하십시오. 게다가 페이로드 크기는 64Ko를 초과할 수 없습니다.

<br/>

***샘플 요청***

워크플로우에서 GET 요청을 수행합니다.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/workflow/execution/<workflowID> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

워크플로우 신호 활동 및 관련 트리거 url을 반환합니다.

```
{
"PKey": "<PKEY>",
"activities": {
  "activity": {
    "signal1": {
      ...
      "trigger": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/workflow/execution/<PKEY>/activities/activity/<PKEY>/trigger/"
        },
        ...
      }
    }
  }
}
```

신호 활동을 트리거하려면 &quot;소스&quot;를 사용하여 트리거 url에 POST 요청을 수행합니다. 매개 변수를 사용하여 워크플로우를 호출하려면 &quot;매개 변수&quot; 속성을 추가합니다.

```
-X POST https://mc.adobe.io/<ORGANIZATION>/campaign/workflow/execution/<PKEY>/activities/activity/<PKEY>/trigger \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-i
-d '{
-d "source":"API",
-d "parameters":{
-d    "audience":"audience",
-d    "email":"anna.varney@mail.com",
-d    "template":"05",
-d    "contentURL":"http://www.adobe.com",
-d    "test":"true",
-d    "segmentCode":"my segment",
-d    "attribute":"2019-04-03 08:17:19.100Z"}
-d  }'
```

<!-- + réponse -->

외부 신호 활동에서 매개 변수 중 하나를 선언하지 않으면 POST 요청은 아래 오류를 반환하여 누락된 매개 변수를 가리킵니다.

```
RST-360011 An error has occurred - please contact your administrator.
'contentURL' parameter isn't defined in signal activity.
XTK-170006 Unable to parse expression 'HandleTrigger(@name, $(source), $({parameters}))'.
RST-360000 Error while assessing 'HandleTrigger(@name, $(source), $({parameters}))' expression ('xtk:workflow:execution/activities/signal/trigger' resource)
```
