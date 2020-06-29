---
title: 강화
description: 데이터 연계 강화 활동은 워크플로우에서 처리할 추가 데이터를 정의할 수 있는 고급 활동입니다.
page-status-flag: never-activated
uuid: 8c1693ef-1312-422c-b05d-263553113f8f
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: f67c1caf-3284-4c34-a5b0-8654a95640ae
context-tags: enrichment,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 87e0611fae0560aca276caa3c4cf793e9c095d72
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---


# 강화{#enrichment}

## 설명 {#description}

![](assets/enrichment.png)

활동은 **[!UICONTROL Enrichment]** 워크플로우에서 처리할 추가 데이터를 정의할 수 있는 고급 활동입니다.

## 사용 상황 {#context-of-use}

일반적으로 **[!UICONTROL Enrichment]** 활동은 타깃팅된 활동 후에 또는 파일을 가져온 후 타깃팅된 데이터를 사용할 수 있는 활동 전에 사용됩니다.

이 활동은 **[!UICONTROL Query]** 활동보다 더 진보적인 농축기능을 포함하고 있다. 일부 간단한 데이터 농축은 [쿼리 활동에서 직접 수행할 수 있습니다](../../automating/using/query.md#enriching-data).

활동을 사용하여 **[!UICONTROL Enrichment]** 인바운드 전환을 활용하고 추가 데이터로 출력 전환을 완료하도록 활동을 구성할 수 있습니다. 여러 세트에서 가져온 데이터를 결합하거나 임시 리소스에 대한 링크를 만들 수 있습니다.

**관련 항목**

* [사용 사례: 파일에 포함된 데이터로 프로파일 데이터](../../automating/using/enriching-profile-data-file.md)강화
* [사용 사례: 풍부한 필드가 포함된 이메일 보내기](../../automating/using/sending-email-enriched-fields.md)

## 구성 {#configuration}

활동을 **[!UICONTROL Enrichment]** 구성하려면:

1. 활동을 워크플로우로 드래그하여 **[!UICONTROL Enrichment]** 놓습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 활동을 엽니다.
1. 활동에 여러 개의 인바운드 전환이 있는 경우 해당 전환을 선택합니다 **[!UICONTROL Primary set]**. 이 활동에 구성된 추가 데이터는 아웃바운드 전환에서 이 기본 세트에 추가됩니다.

   기본 세트에 이미 추가 데이터가 포함되어 있는 경우 해당 데이터를 유지하거나 제거할 수 있습니다. 이 **[!UICONTROL Keep all additional data from the main set]** 옵션을 선택 취소하면 아웃바운드 전환 **[!UICONTROL Enrichment]** 에 구성된 추가 데이터만 유지됩니다.

1. 여러 개의 인바운드 전환이 있는 경우 활동의 **[!UICONTROL Advanced Relations]** 탭에서 기본 세트와 다른 인바운드 데이터 간의 관계를 정의합니다. 단추를 사용하여 여러 관계를 추가할 수 **[!UICONTROL Add element]** 있습니다.

   새 관계를 정의할 때 기본 세트에 연결할 인바운드 데이터 세트를 선택합니다. 그런 다음 관계식의 유형을 정의합니다. 인바운드 데이터와 데이터 모델에 따라 몇 가지 유형의 관계를 사용할 수 있습니다.

   * **[!UICONTROL 1 cardinality simple link]**: 들어오는 데이터의 각 레코드는 기본 세트에서 한 개의 레코드에만 연결됩니다. 기본 세트의 각 레코드에는 연결된 데이터에 하나의 연관된 레코드가 있습니다.
   * **[!UICONTROL N cardinality collection link]**: 연결된 데이터의 0, 1 이상(N) 레코드는 기본 세트의 1개 레코드에 연결할 수 있습니다.
   * **[!UICONTROL 0 or 1 cardinality simple link]**: 기본 세트의 레코드는 연결된 데이터의 0 또는 1 레코드와 연결할 수 있지만 하나 이하여야 합니다.
   가 정의된 **[!UICONTROL Cardinality]** 후 를 정의합니다 **[!UICONTROL Reconciliation criteria]**. 조정 기준 **[!UICONTROL Source expression]** 의 필드는 대상 리소스의 필드이거나 [표현식](../../automating/using/advanced-expression-editing.md) 또는 따옴표 사이에 직접 지정된 값일 수 있습니다.

   워크플로우 **[!UICONTROL Label]** 에서 나중에 손쉽게 식별할 수 **[!UICONTROL ID]** 있는 a와 를 정의합니다.

   >[!NOTE]
   >
   >기본 세트와 활동에 연결된 다른 인바운드 전환 사이의 관계만 정의할 수 **[!UICONTROL Enrichment]** 있습니다. 데이터베이스 리소스와의 관계를 정의하는 것이 간단한 경우인 경우 [조정](../../automating/using/reconciliation.md) 활동을 사용하십시오.

1. 활동의 탭에서 추가 데이터를 **[!UICONTROL Additional data]** 정의합니다. 기본 세트의 타깃팅 차원과 관련된 추가 데이터(단순 필드, 합계 및 컬렉션)를 정의하거나 활동의 **[!UICONTROL Advanced relations]** 탭에서 만든 링크를 기준으로 **[!UICONTROL Enrichment]** 정의할 수 있습니다.

   데이터 [를](../../automating/using/query.md#enriching-data) 농축합니다.

1. 활동 구성을 확인하고 워크플로우를 저장합니다.

이제 데이터 이후에 연결된 활동에 데이터를 사용할 수 있습니다 **[!UICONTROL Enrichment]**. 예를 들어, 이메일 컨텐츠의 개인화 필드 탐색기 **[!UICONTROL Additional data (targetData)]** 링크 아래에서 찾을 수 있습니다.
