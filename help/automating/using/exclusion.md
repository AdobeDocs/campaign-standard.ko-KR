---
title: 제외
seo-title: 제외
description: 제외
seo-description: 제외 활동을 사용하면 특정 기준에 따라 한 모집단에서 요소를 제외할 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: b 79 e 7 f 73-37 a 0-4 ec 3-ac 5 a -5449 dc 1 b 1 f 22
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 타깃팅 활동
discoiquuid: D 5312 FCD -43 AD -428 E-BDE 9-90 F 062 E 9358 C
context-tags: 제외, 기본
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: e384a0cef325bc01eb5ea050b0f3d926aea9a88f

---


# Exclusion{#exclusion}

## Description {#description}

![](assets/exclusion.png)

**[!UICONTROL Exclusion]** 활동을 통해 특정 기준에 따라 한 모집단에서 요소를 제외할 수 있습니다.

## Context of use {#context-of-use}

**[!UICONTROL Exclusion]** 활동은 기본적으로 인바운드 전환 모집단에 대한 추가 필터링을 수행하는 데 사용됩니다.

기본 세트는 인바운드 전환 간에 정의됩니다. 다른 인바운드 전환 구성원은 기본 세트에서 제외됩니다. 제외 활동의 아웃바운드 전환에는 다른 인바운드 변환에서 발생하지 않은 기본 세트의 구성원만 포함됩니다.

## Configuration {#configuration}

1. **[!UICONTROL Exclusion]** 워크플로우를 워크플로우로 드래그하여 놓습니다.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. Select the **[!UICONTROL Primary set]** from the inbound transitions. 이것은 요소가 제외되는 세트입니다. 다른 세트는 기본 세트에서 제외되기 전에 요소를 일치시킵니다.

   >[!NOTE]
   >
   >인바운드 전환은 동일한 유형의 모집단을 포함해야 합니다. 예를 들어 기본 세트에 테스트 프로필이 포함된 경우 다른 전환 과정에도 테스트 프로필이 포함되어야 합니다.

1. If needed, manage the activity's [Transitions](../../automating/using/executing-a-workflow.md#managing-an-activity-s-outbound-transitions) to access the advanced options for the outbound population.
1. 활동의 구성을 확인하고 워크플로우를 저장합니다.

## Example {#example}

다음 예에서는 Adobe Campaign 데이터베이스에서 18 ~ 27 세 사이에 있고 잘못된 이메일 주소가 있는 프로필을 필터링하도록 구성된 두 개의 쿼리 활동을 보여줍니다. 이메일 주소가 잘못된 프로필은 첫 번째 세트에서 제외됩니다. 예를 들어 이메일을 보낼 수 있습니다.

![](assets/wkf_exclusion_example.png)

