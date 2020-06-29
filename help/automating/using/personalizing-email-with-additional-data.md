---
title: 추가 데이터를 사용하여 이메일 개인화
description: 이 사용 사례에서는 쿼리에 다른 유형의 추가 데이터를 추가하고 이메일의 개인화 필드로 사용하는 방법을 설명합니다.
page-status-flag: never-activated
uuid: b3c629fa-370e-481c-b347-fcf9f5a5e847
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: 8d46ce28-0101-4f13-865a-2208ed6d6139
context-tags: query,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 2d994d85f126951215f1227301599c554c1f12c8
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 0%

---


# 추가 데이터를 사용하여 이메일 개인화 {#example--personalizing-an-email-with-additional-data}

다음 예에서는 쿼리에 다른 유형의 추가 데이터를 추가하고 이메일의 개인화 필드로 사용하는 방법을 보여 줍니다. 활동에 의해 타깃팅된 데이터를 보강하는 방법에 대한 자세한 내용은 **[!UICONTROL Query]** 이 섹션을 참조하십시오 [](../../automating/using/query.md#enriching-data).

이 예에서는 [사용자 지정 리소스가](../../developing/using/data-model-concepts.md) 사용됩니다.

* 각 프로파일의 **충성도 지점을 저장할 수 있는 필드를 추가하기 위해 프로필** 리소스가 확장되었습니다.
* 트랜잭션 **리소스가 생성되었고 데이터베이스의 프로필에서 수행한 모든 구매를 식별합니다** . 구매한 날짜, 가격 및 제품은 각 거래에 대해 저장됩니다.
* 제품 **리소스를 만들고** 구매할 수 있는 제품을 참조합니다.

하나 이상의 트랜잭션이 저장된 프로필로 이메일을 보내는 것이 목표입니다. 클라이언트는 이 이메일을 통해 마지막으로 수행된 트랜잭션과 모든 거래에 대한 개요를 알 수 있습니다. 구매한 제품 수, 총 체류 시간, 누적된 총 충성도 포인트 수에 대한 미리 알림

워크플로우는 다음과 같이 표시됩니다.

![](assets/enrichment_example1.png)

1. 하나 이상의 트랜잭션을 수행한 프로파일을 타깃팅할 수 있는 [쿼리](../../automating/using/query.md) 활동을 추가합니다.

   ![](assets/enrichment_example2.png)

   쿼리의 **[!UICONTROL Additional data]** 탭에서 최종 이메일에 표시할 다른 데이터를 정의합니다.

   * 충성도 포인트에 해당하는 **프로필** 차원의 단순 필드. 간단한 필드 [추가 섹션을](../../automating/using/query.md#adding-a-simple-field) 참조하십시오.
   * 트랜잭션 수집에 기반한 2개의 집계: 구매한 제품 수 및 총 지출 금액. 합계 구성 창의 **[!UICONTROL Data]** 탭에서 **수** 및 합계 **합계를 사용하여 추가할 수** 있습니다. 집계 [추가 섹션을](../../automating/using/query.md#adding-an-aggregate) 참조하십시오.
   * 사용한 금액, 날짜 및 영향을 받은 마지막 거래의 제품을 반환하는 컬렉션입니다.

      이렇게 하려면 컬렉션 구성 창의 **[!UICONTROL Data]** 탭에서 표시할 다른 필드를 추가해야 합니다.

      가장 최근 거래만 반환하려면 에 대해 &quot;1&quot;을 **[!UICONTROL Number of lines to return]** 입력하고 **탭에서 컬렉션의** 날짜 **[!UICONTROL Sort]** 필드에 내림차순 정렬을 적용해야 합니다.

      컬렉션 [추가](../../automating/using/query.md#adding-a-collection) 및 [추가 데이터](../../automating/using/query.md#sorting-additional-data) 정렬 섹션을 참조하십시오.
   ![](assets/enrichment_example4.png)

   활동이 아웃바운드 전환으로 데이터가 올바르게 전송되었는지 확인하려는 경우 처음(활동 없이) 워크플로우를 시작하고 쿼리의 아웃바운드 전환을 엽니다. **[!UICONTROL Email delivery]**

   ![](assets/enrichment_example5.png)

1. 이메일 [배달](../../automating/using/email-delivery.md) 활동을 추가합니다. 이메일 컨텐츠에서 쿼리에 계산된 데이터에 해당하는 개인화 필드를 삽입합니다. 개인화 필드 탐색기의 **[!UICONTROL Additional data (targetData)]** 링크를 통해 찾을 수 있습니다.

   ![](assets/enrichment_example3.png)

이제 워크플로우를 실행할 준비가 되었습니다. 쿼리에 타깃팅된 프로필은 해당 거래에서 계산된 데이터가 포함된 개인화된 이메일을 수신하게 됩니다.
