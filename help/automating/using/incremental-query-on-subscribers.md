---
title: 서비스의 구독자에 대한 증분 쿼리
description: 다음 예에서는 서비스에 가입자를 필터링하기 위해 증분 쿼리 활동을 구성하는 방법을 보여 줍니다.
page-status-flag: never-activated
uuid: 73b42422-e815-43ef-84c0-97c4433ccc98
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: 80961e73-42ec-463a-8496-cff69fab0475
context-tags: incremental,main
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 67%

---


# 서비스의 구독자에 대한 증분 쿼리 {#example--incremental-query-on-subscribers-to-a-service}

다음 예는 **실행 중인 뉴스레터** 서비스를 구독한 Adobe Campaign 데이터베이스의 프로필을 필터링하여 프로모션 코드가 포함된 환영 이메일을 보내는 **[!UICONTROL Incremental query]** 활동 구성을 보여줍니다.

워크플로우는 다음 요소로 구성됩니다.

![](assets/incremental_query_example1.png)

* A [Scheduler](../../automating/using/scheduler.md) activity, to execute the workflow every Monday at 6 am.

   ![](assets/incremental_query_example2.png)

* An [Incremental query](../../automating/using/incremental-query.md) activity, which targets all of the current subscribers during the first execution, then only the new subscribers of that week during the following executions.

   ![](assets/incremental_query_example3.png)

* 이메일 [배달](../../automating/using/email-delivery.md) 활동. 워크플로우는 일주일에 한 번 실행되지만, 전송된 이메일과 월별 결과를 집계하여 예를 들어 한 주가 아닌 한 달 보고서를 생성할 수 있습니다.

   이렇게 하려면 여기서 **[!UICONTROL Recurring email]**&#x200B;을(를) 생성하도록 선택하고 이메일 및 결과 **[!UICONTROL By month]**&#x200B;을(를) 다시 그룹화합니다.

   이메일의 내용을 정의하고 환영 프로모션 코드를 삽입합니다. 자세한 내용은 [이메일 컨텐츠](../../designing/using/personalization.md) 정의 섹션을 참조하십시오.

그런 다음 워크플로우 실행을 시작합니다. 매주 새 구독자는 프로모션 코드와 함께 환영 이메일을 받게 됩니다.
