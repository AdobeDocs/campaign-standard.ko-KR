---
title: 배달 전 중복 항목 식별
description: 다음 예에서는 이메일을 보내기 전에 대상의 중복 제거를 제외할 수 있는 데이터 중복 제거를 보여 줍니다. 즉, 동일한 프로필에 여러 번 통신을 보내지 않습니다.
page-status-flag: never-activated
uuid: 11a22a9c-3bfe-4953-8a52-2f4e93c128fb
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: e7a5e1e7-4680-46c7-98b8-0a47bb7be2b8
context-tags: dedup,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 7ffa48365875883a98904d6b344ac005afe26e18
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---


# 배달 전 중복 항목 식별 {#identifying-duplicates-before-a-delivery}

다음 예에서는 이메일을 보내기 전에 대상의 중복 제거를 제외할 수 있는 데이터 중복 제거를 보여 줍니다. 즉, 동일한 프로필에 여러 번 통신을 보내지 않습니다.

워크플로우는 다음과 같이 구성됩니다.

![](assets/deduplication_example_workflow.png)

* 이메일 [대상을 정의할](../../automating/using/query.md) 수 있는 쿼리입니다. 여기서 워크플로우는 1년 이상 클라이언트 데이터베이스에 있었던 18세에서 25세 사이의 모든 프로필을 대상으로 합니다.

   ![](assets/deduplication_example_query.png)

* 데이터 [중복 제거](../../automating/using/deduplication.md) 활동으로서 이전 질문의 중복 항목을 식별할 수 있습니다. 이 예에서는 각 복제에 대해 하나의 레코드만 저장됩니다. 중복된 항목은 이메일 주소를 사용하여 식별됩니다. 즉, 각 이메일 주소가 타깃팅에 표시되도록 한 번만 이메일 배달을 보낼 수 있습니다.

   선택한 데이터 중복 제거 방법입니다 **[!UICONTROL Non-empty value]**. 이 기능을 사용하면 중복 레코드 중에서 **이름이** 제공된 레코드에 우선 순위가 지정되도록 할 수 있습니다. 이메일 컨텐츠의 개인화 필드에 이름을 사용하는 경우 더욱 일관됩니다.

   또한 중복 항목을 유지하고 나열할 수 있도록 추가 전환이 추가됩니다.

   ![](assets/deduplication_example_dedup.png)

* 데이터 중복 제거 [의 기본 아웃바운드 전환 이후 이메일](../../automating/using/email-delivery.md) 전달
* 데이터 중복 제거 [를 추가로 전환하여 중복](../../automating/using/save-audience.md) 대상의 중복 항목을 저장한 후 대상 **을** 저장하는 활동입니다. 이 대상자는 모든 이메일 배달에서 구성원을 직접 제외하는 데 재사용할 수 있습니다.
