---
solution: Campaign Standard
product: campaign
title: 추가 데이터를 사용하여 이메일 개인화
description: 이 사용 사례에서는 쿼리에 다른 유형의 추가 데이터를 추가하고 이메일의 개인화 필드로 사용하는 방법을 설명합니다.
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: query,main
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 86%

---


# 추가 데이터를 사용하여 이메일 개인화 {#example--personalizing-an-email-with-additional-data}

다음 예제에서는 쿼리에 다양한 유형의 데이터를 추가하여 이메일의 개인화 필드로 사용하는 방법을 보여줍니다. 활동에 의해 타깃팅된 데이터를 보강하는 방법에 대한 자세한 내용은 **[!UICONTROL Query]** 이 섹션을 참조하십시오 [](../../automating/using/query.md#enriching-data).

이 예제에서는 [사용자 정의 리소스](../../developing/using/data-model-concepts.md)를 사용합니다.

* 각 프로필의 충성도 포인트를 저장하는 필드를 추가할 수 있도록 **프로필** 리소스를 확장했습니다.
* 데이터베이스의 프로필에서 수행한 모든 구매를 확인하는 **트랜잭션** 리소스를 만들었습니다. 각 트랜잭션에 대해 날짜, 가격, 구매 제품이 저장됩니다.
* 구매할 수 있는 제품을 참조하는 **제품** 리소스를 만들었습니다.

하나 이상의 트랜잭션이 저장된 프로필로 이메일을 보내는 것이 목표입니다. 고객은 이 이메일을 통해 마지막으로 수행한 트랜잭션과 모든 트랜잭션에 대한 개요를 받아 볼 수 있습니다. 여기에는 구매한 제품 수, 총 지출액, 총 누적 충성도 포인트 등이 표시됩니다.

워크플로우는 다음과 같이 표시됩니다.

![](assets/enrichment_example1.png)

1. Add a [Query](../../automating/using/query.md) activity, which allows you to target the profiles that have carried out at least one transaction.

   ![](assets/enrichment_example2.png)

1. 쿼리의 **[!UICONTROL Additional data]** 탭에서 최종 이메일에 표시할 여러 데이터를 정의합니다.

   * 충성도 포인트에 해당하는 **프로필** 차원의 단순 필드. [단순 필드 추가](../../automating/using/query.md#adding-a-simple-field) 섹션을 참조하십시오.
   * 트랜잭션 컬렉션에 기반한 2가지 합계: 구매한 제품 수 및 총 지출 금액. 합계 구성 창의 **[!UICONTROL Data]** 탭에서 **개수** 및 **총합** 합계를 사용하여 추가할 수 있습니다. [합계 추가](../../automating/using/query.md#adding-an-aggregate) 섹션을 참조하십시오.
   * 유효한 최근 트랜잭션의 지출 금액, 날짜 및 제품을 반환하는 컬렉션.

      이를 위해 컬렉션 구성 창의 **[!UICONTROL Data]** 탭에서 표시할 여러 필드를 추가해야 합니다.

      가장 최근 트랜잭션만 반환하려면 **[!UICONTROL Number of lines to return]**&#x200B;에 &quot;1&quot;을 입력하고, **[!UICONTROL Sort]** 탭에서 컬렉션의 **날짜** 필드에 내림차순 정렬을 적용해야 합니다.

      [컬렉션 추가](../../automating/using/query.md#adding-a-collection) 및 [추가 데이터 정렬](../../automating/using/query.md#sorting-additional-data) 섹션을 참조하십시오.
   ![](assets/enrichment_example4.png)

1. 해당 활동의 아웃바운드 전환을 통해 데이터가 올바르게 전송되었는지 확인하려면 처음에 (**[!UICONTROL Email delivery]** 활동 없이) 워크플로우를 시작한 뒤 쿼리의 아웃바운드 전환을 엽니다.

   ![](assets/enrichment_example5.png)

1. 이메일 [배달](../../automating/using/email-delivery.md) 활동을 추가합니다. 이메일 콘텐츠에서 쿼리에서 계산한 데이터에 해당하는 개인화 필드를 삽입합니다. 개인화 필드 탐색기의 **[!UICONTROL Additional data (targetData)]** 링크를 통해 찾을 수 있습니다.

   ![](assets/enrichment_example3.png)

이제 워크플로우를 실행할 준비가 되었습니다. 쿼리에서 타겟팅한 프로필은 트랜잭션에서 계산된 데이터가 포함된 개인적인 이메일을 수신하게 됩니다.
