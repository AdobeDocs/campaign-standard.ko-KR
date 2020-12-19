---
solution: Campaign Standard
product: campaign
title: 데이터 보강
description: 데이터 보강 활동은 워크플로우에서 처리할 추가 데이터를 정의할 수 있는 고급 활동입니다.
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: enrichment,main
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 96%

---


# 데이터 보강{#enrichment}

## 설명 {#description}

![](assets/enrichment.png)

**[!UICONTROL Enrichment]** 활동은 워크플로우에서 처리할 추가 데이터를 정의할 수 있는 고급 활동입니다.

## 사용의 컨텍스트 {#context-of-use}

일반적으로 **[!UICONTROL Enrichment]** 활동은 타겟팅 활동 다음이나 파일을 가져온 후 타겟팅된 데이터를 사용할 수 있는 활동 전에 사용됩니다.

이 활동은 **[!UICONTROL Query]** 활동보다 더 많은 고급 데이터 보강 기능을 포함하고 있습니다. 일부 간단한 데이터 보강은 [쿼리 활동](../../automating/using/query.md#enriching-data)에서 직접 수행할 수 있습니다.

**[!UICONTROL Enrichment]** 활동을 사용하여 인바운드 전환을 활용하고 추가 데이터로 출력 전환을 완료하도록 활동을 구성할 수 있습니다. 여러 세트에서 가져온 데이터를 결합하거나 임시 리소스에 대한 링크를 만들 수 있습니다.

**관련 항목**

* [사용 사례:파일에 포함된 데이터로 프로필 데이터를 풍성하게 합니다](../../automating/using/enriching-profile-data-file.md).
* [사용 사례:풍부한 필드가 포함된 이메일 보내기](../../automating/using/sending-email-enriched-fields.md)

## 구성 {#configuration}

**[!UICONTROL Enrichment]** 활동을 구성하는 방법:

1. **[!UICONTROL Enrichment]** 활동을 워크플로우로 끌어다 놓습니다.
1. 활동을 선택한 다음 나타나는 바로 가기의 ![](assets/edit_darkgrey-24px.png) 버튼을 사용하여 엽니다.
1. 활동에 여러 개의 인바운드 전환이 있는 경우 **[!UICONTROL Primary set]**&#x200B;을(를) 선택합니다 . 이 활동에 구성된 추가 데이터는 아웃바운드 전환의 기본 세트에 추가됩니다.

   기본 세트에 이미 추가 데이터가 포함되어 있는 경우 해당 데이터를 유지하거나 제거할 수 있습니다. **[!UICONTROL Keep all additional data from the main set]** 옵션을 선택 취소하면 **[!UICONTROL Enrichment]**&#x200B;에 구성된 추가 데이터만 아웃바운드 전환에 유지됩니다.

1. 여러 개의 인바운드 전환이 있는 경우 활동의 **[!UICONTROL Advanced Relations]** 탭에서 기본 세트와 다른 인바운드 데이터 간의 관계를 정의합니다. **[!UICONTROL Add element]** 버튼을 사용하여 여러 관계를 추가할 수 있습니다.

   새 관계를 정의할 때 기본 세트에 연결할 인바운드 데이터 세트를 선택합니다. 그런 다음 관계의 유형을 정의합니다. 인바운드 데이터와 데이터 모델에 따라 다음과 같은 몇 가지 유형의 관계를 사용할 수 있습니다.

   * **[!UICONTROL 1 cardinality simple link]**: 들어오는 데이터의 각 레코드는 기본 세트에서 1개의 레코드에만 연결됩니다. 기본 세트의 각 레코드에는 연결된 데이터에 하나의 연관된 레코드가 있습니다.
   * **[!UICONTROL N cardinality collection link]**: 연결된 데이터에서 0개, 1개 또는 그 이상의 레코드는 기본 세트의 1개 레코드에 연결할 수 있습니다.
   * **[!UICONTROL 0 or 1 cardinality simple link]**: 기본 세트의 레코드는 연결된 데이터의 0개 또는 1개 레코드와 연결할 수 있지만 1개 이하여야 합니다.

   **[!UICONTROL Cardinality]**&#x200B;가 정의되면 **[!UICONTROL Reconciliation criteria]**&#x200B;을(를) 정의합니다. 조정 기준의 **[!UICONTROL Source expression]**&#x200B;는 대상 리소스의 필드이거나 [표현식](../../automating/using/advanced-expression-editing.md) 또는 따옴표 사이에 직접 지정된 값일 수 있습니다.

   나중에 워크플로우에서 손쉽게 식별할 수 있는&#x200B;**[!UICONTROL Label]**&#x200B;와(과) **[!UICONTROL ID]**&#x200B;을(를) 정의합니다.

   >[!NOTE]
   >
   >기본 세트와 **[!UICONTROL Enrichment]** 활동에 연결된 다른 인바운드 전환 사이의 관계만 정의할 수 있습니다. 데이터베이스 리소스와의 관계를 정의하는 것이 간단한 경우, [조정](../../automating/using/reconciliation.md) 활동을 사용하십시오.

1. 활동의 **[!UICONTROL Additional data]** 탭에서 추가 데이터를 정의합니다. 기본 세트의 타겟팅 차원과 관련된 추가 데이터(단순 필드, 집계 및 컬렉션)나 **[!UICONTROL Enrichment]** 활동의 **[!UICONTROL Advanced relations]** 탭에서 만든 링크를 기준으로 정의할 수 있습니다.

   [데이터 보강](../../automating/using/query.md#enriching-data) 섹션을 참조하십시오.

1. 활동 구성을 확인하고 워크플로우를 저장합니다.

이제 **[!UICONTROL Enrichment]** 이후에 연결된 활동의 데이터를 사용할 수 있습니다 . 예를 들어, 전자 메일 콘텐츠의 개인화 필드 탐색기에 **[!UICONTROL Additional data (targetData)]** 링크 아래에서 찾을 수 있습니다.
