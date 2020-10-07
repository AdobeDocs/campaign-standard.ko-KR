---
title: 게재 전 중복 식별
description: 다음의 예제에서는 이메일을 보내기 전에 타겟의 중복을 제외할 수 있는 중복 제거를 보여줍니다. 즉, 동일한 프로필에 커뮤니케이션을 여러 번 보내지 않습니다.
page-status-flag: never-activated
uuid: 11a22a9c-3bfe-4953-8a52-2f4e93c128fb
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: e7a5e1e7-4680-46c7-98b8-0a47bb7be2b8
context-tags: dedup,main
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 78%

---


# 게재 전 중복 식별 {#identifying-duplicates-before-a-delivery}

다음의 예제에서는 이메일을 보내기 전에 타겟의 중복을 제외할 수 있는 중복 제거를 보여줍니다. 즉, 동일한 프로필에 커뮤니케이션을 여러 번 보내지 않습니다.

워크플로우는 다음과 같이 구성됩니다.

![](assets/deduplication_example_workflow.png)

* A [Query](../../automating/using/query.md) which allows you to define the target of the email. 여기서 워크플로우는 1년 이상 클라이언트 데이터베이스에 있었던 18세에서 25세 사이의 모든 프로필을 타겟으로 합니다.

   ![](assets/deduplication_example_query.png)

* A [Deduplication](../../automating/using/deduplication.md) activity, which allows you to identify the duplicates that come from the preceding query. 이 예제에서는 각 중복에 대해 하나의 레코드만 저장됩니다. 중복은 이메일 주소를 사용하여 식별됩니다. 즉, 이메일 게재는 각 이메일 주소가 타겟팅에 포함될 때마다 한 번만 전송될 수 있습니다.

   선택한 데이터 중복 제거 방법은 **[!UICONTROL Non-empty value]**&#x200B;입니다. 이를 사용하면 중복 시 유지한 레코드 중에서 **이름**&#x200B;이 제공된 레코드에 우선 순위가 부여되도록 할 수 있습니다. 이메일 콘텐츠의 개인화 필드에 이름을 사용할 경우 더욱 일관성 있게 됩니다.

   또한 중복을 유지하고 나열할 수 있도록 추가 전환이 추가되었습니다.

   ![](assets/deduplication_example_dedup.png)

* An [Email delivery](../../automating/using/email-delivery.md) placed after the main outbound transition of the deduplication.
* A [Save audience](../../automating/using/save-audience.md) activity placed after the additional transition of the deduplication to save the duplicates in a **Duplicates** audience. 이 대상자는 모든 이메일 게재에서 멤버를 직접 제외하는 데 재사용할 수 있습니다.
