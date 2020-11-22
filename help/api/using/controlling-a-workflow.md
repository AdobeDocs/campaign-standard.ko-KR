---
solution: Campaign Standard
product: campaign
title: 워크플로우 제어
description: API를 사용하여 워크플로우를 제어하는 방법을 알아봅니다.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 9%

---


# 워크플로우 제어 {#controlling-a-workflow}

워크플로우 ID와 필요한 실행 명령이 포함된 POST 요청을 통해 REST API에서 직접 워크플로우를 제어할 수 있습니다.

`POST https://mc.adobe.io/<ORGANIZATION>/campaign/workflow/execution/<workflowID>/commands`

>[!CAUTION]
>
>Adobe Campaign에서 워크플로우 ID가 변경되면 API 요청은 더 이상 작동하지 않습니다.

워크플로우를 제어하는 데 다음 네 가지 실행 명령을 사용할 수 있습니다.

* 시작
* 일시 정지
* 다시 시작
* 정지

실행 명령에 대한 자세한 내용은 [캠페인 설명서를 참조하십시오](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/executing-a-workflow/about-workflow-execution.html).

<br/>

***샘플 요청***

* 워크플로우 시작

   ```
   -X POST https://mc.adobe.io/<ORGANIZATION>/campaign/workflow/execution/<workflowID>/commands \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>' \
   -i
   -d '{"method":"start"}'
   ```

   <!-- + réponse -->

* 워크플로우를 중지합니다.

   ```
   -X POST https://mc.adobe.io/<ORGANIZATION>/campaign/workflow/execution/<workflowID>/commands \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>' \
   -i
   -d '{"method":"stop"}'
   ```

   <!-- + réponse -->
