---
title: 생일 게재
description: 이 예제는 생일 워크플로우입니다. 그 날 생일을 맞는 프로필로 매일 이메일이 전송됩니다.
audience: automating
content-type: reference
topic-tags: channel-activities
context-tags: delivery,workflow,main
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: 535ddbce-d8ba-4578-9e37-10604291c95d
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 69%

---

# 생일 게재 {#birthday-delivery}

![](assets/wkf_delivery_example_1.png)

이 예제는 생일 워크플로우입니다. 그 날 생일을 맞는 프로필로 매일 이메일이 전송됩니다.

워크플로우를 빌드하려면 다음 단계를 수행합니다.

* [스케줄러](../../automating/using/scheduler.md)를 사용하면 매일 오전 8시에 워크플로우를 시작할 수 있습니다.

   ![](assets/wkf_delivery_example_2.png)

* [Query](../../automating/using/query.md) 활동을 사용하면 워크플로우를 실행할 때마다 이메일을 제공한 프로필 및 생일이 현재 날짜인 프로필을 계산할 수 있습니다. 생일 계산은 쿼리 편집 도구의 팔레트에서 사용할 수 있는 사전 정의된 필터를 사용하여 수행됩니다.

   ![](assets/wkf_delivery_example_3.png)

* [이메일 배달](../../automating/using/email-delivery.md)은(는) 반복됩니다. 전송은 월별로 집계됩니다. 따라서 한 달에 전송된 모든 이메일은 단일 보기로 집계됩니다. 따라서 1년 동안 365개의 게재가 실행되지만 Adobe Campaign 인터페이스에서 12개의 보기(**반복 실행**)로 다시 그룹화됩니다. 내역 및 보고서 세부 사항은 전송할 때마다 표시되지 않고 매월 표시됩니다.

   ![](assets/wkf_delivery_example_4.png)
