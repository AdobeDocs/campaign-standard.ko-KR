---
title: 워크플로우 제어
description: API를 사용하여 워크플로우를 제어하는 방법을 알아봅니다.
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
source-git-commit: aee0e0437cbfe578cb2f715a2433099c79dd1748

---


# 워크플로우 제어 {#controlling-a-workflow}

워크플로우 ID와 필요한 실행 명령이 포함된 POST 요청을 통해 REST API에서 직접 워크플로우를 제어할 수 있습니다.

`POST https://mc.adobe.io/<ORGANIZATION>/campaign/workflow/execution/<workflowID>/commands`

>[!CAUTION]
>
>워크플로우 ID가 Adobe Campaign에서 변경되면 API 요청이 더 이상 작동하지 않습니다.

다음 네 가지 실행 명령을 사용하여 워크플로우를 제어할 수 있습니다.

* 시작
* 일시 중지
* 다시 시작
* 중지

실행 명령에 대한 자세한 내용은 Campaign [설명서를](https://helpx.adobe.com/campaign/standard/automating/using/executing-a-workflow.html)참조하십시오.

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

* 워크플로우 중지

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
