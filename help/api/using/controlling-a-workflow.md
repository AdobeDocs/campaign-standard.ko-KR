---
title: 워크플로 제어
description: API를 사용하여 워크플로우를 제어하는 방법을 알아봅니다.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
old-role: Data Architect
role: Developer
level: Experienced
exl-id: 79eacc31-d5a2-4e13-aa0b-744d7ab7004f
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
  - id: f5407121-8933-4ac3-8e06-a9b692a4e88a
    internal-label: Campaign Standard
feature_v2:
  - id: b12f6872-9271-4369-85e5-86969a0b99a2
    internal-label: APIs
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: bb37e2bfbc52de1b0cc03f0f8e03985caff5e5b0
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 9%
---
# 워크플로 제어 {#controlling-a-workflow}

워크플로 ID 및 필수 실행 명령이 포함된 POST 요청을 통해 REST API에서 직접 워크플로를 제어할 수 있습니다.

`POST https://mc.adobe.io/<ORGANIZATION>/campaign/workflow/execution/<workflowID>/commands`

>[!CAUTION]
>
>Adobe Campaign에서 워크플로우 ID를 변경하면 API 요청이 더 이상 작동하지 않습니다.

워크플로를 제어하는 데 사용할 수 있는 네 가지 실행 명령은 다음과 같습니다.

* 시작
* 일시 정지
* 다시 시작
* 정지

실행 명령에 대한 자세한 내용은 [Campaign 설명서](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/executing-a-workflow/about-workflow-execution.html)를 참조하세요.

<br/>

***샘플 요청***

* 워크플로우를 시작합니다.

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
