---
solution: Campaign Standard
product: campaign
title: 생일 게재
description: 이 예제는 생일 워크플로우입니다. 그 날 생일을 맞는 프로필로 매일 이메일이 전송됩니다.
audience: automating
content-type: reference
topic-tags: channel-activities
context-tags: delivery,workflow,main
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 69%

---


# 생일 게재 {#birthday-delivery}

![](assets/wkf_delivery_example_1.png)

이 예제는 생일 워크플로우입니다. 그 날 생일을 맞는 프로필로 매일 이메일이 전송됩니다.

워크플로우를 빌드하려면 다음 단계를 따르십시오.

* The [Scheduler](../../automating/using/scheduler.md) allows you to start the workflow every day at 8am.

   ![](assets/wkf_delivery_example_2.png)

* The [Query](../../automating/using/query.md) activity allows you to calculate the profiles who have provided an email and whose birthday it is on the current day, every time the workflow is executed. 생일 계산은 쿼리 편집 도구의 팔레트에서 사용할 수 있는 사전 정의된 필터를 사용하여 수행됩니다.

   ![](assets/wkf_delivery_example_3.png)

* 이메일 [배달이](../../automating/using/email-delivery.md) 반복됩니다. 전송은 월별로 집계됩니다. 따라서 한 달에 전송된 모든 이메일은 단일 보기로 집계됩니다. 따라서 1년 동안 365개의 게재가 실행되지만 Adobe Campaign 인터페이스에서 12개의 보기(**반복 실행**)로 다시 그룹화됩니다. 내역 및 보고서 세부 사항은 전송할 때마다 표시되지 않고 매월 표시됩니다.

   ![](assets/wkf_delivery_example_4.png)
