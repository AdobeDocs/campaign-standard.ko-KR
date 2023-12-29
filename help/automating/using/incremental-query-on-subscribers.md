---
title: 서비스의 구독자에 대한 증분 쿼리
description: 다음 예제에서는 서비스의 구독자를 필터링하도록 증분 쿼리 활동을 구성하는 방법을 보여줍니다.
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: incremental,main
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: c80ed1f6-ad8a-4448-a6df-b9881327228a
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 61%

---

# 서비스의 구독자에 대한 증분 쿼리 {#example--incremental-query-on-subscribers-to-a-service}

다음 예는 **실행 중인 뉴스레터** 서비스를 구독한 Adobe Campaign 데이터베이스의 프로필을 필터링하여 프로모션 코드가 포함된 환영 이메일을 보내는 **[!UICONTROL Incremental query]** 활동 구성을 보여줍니다.

워크플로우는 다음 요소로 구성됩니다.

![](assets/incremental_query_example1.png)

* A [스케줄러](../../automating/using/scheduler.md) 매주 월요일 오전 6시에 워크플로우를 실행하는 활동.

  ![](assets/incremental_query_example2.png)

* An [증분 쿼리](../../automating/using/incremental-query.md) 첫 번째 실행 시 현재 모든 구독자를 타겟으로 하며 다음 실행 시 해당 주의 새 구독자만 타겟으로 하는 활동.

  ![](assets/incremental_query_example3.png)

* An [이메일 게재](../../automating/using/email-delivery.md) 활동. 워크플로우는 일주일에 한 번 실행되지만, 전송된 이메일과 월별 결과를 집계하여 예를 들어 한 주가 아닌 한 달 보고서를 생성할 수 있습니다.

  이렇게 하려면 여기서 **[!UICONTROL Recurring email]**&#x200B;을(를) 생성하도록 선택하고 이메일 및 결과 **[!UICONTROL By month]**&#x200B;을(를) 다시 그룹화합니다.

  이메일의 콘텐츠를 정의하고 환영 프로모션 코드를 삽입합니다. 자세한 내용은 다음을 참조하십시오. [이메일 콘텐츠 정의](../../designing/using/personalization.md) 섹션.

그런 다음 워크플로우 실행을 시작합니다. 매주 새 구독자는 프로모션 코드와 함께 환영 이메일을 받게 됩니다.
