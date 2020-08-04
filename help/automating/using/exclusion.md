---
title: 예외
description: 예외 활동을 사용하면 특정 기준에 따라 한 모집단에서 요소를 제외할 수 있습니다.
page-status-flag: never-activated
uuid: b79e7f73-37a0-4ec3-ac5a-5449dc1b1f22
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: d5312fcd-43ad-428e-bde9-90f062e9358c
context-tags: exclusion,main
internal: n
snippet: y
translation-type: ht
source-git-commit: 21faea89b3b38f3e667ed6c4de0be6d07f0b7197
workflow-type: ht
source-wordcount: '249'
ht-degree: 100%

---


# 예외{#exclusion}

## 설명 {#description}

![](assets/exclusion.png)

**[!UICONTROL Exclusion]** 활동을 통해 특정 기준에 따라 한 모집단에서 요소를 제외할 수 있습니다.

## 사용의 컨텍스트 {#context-of-use}

**[!UICONTROL Exclusion]** 활동은 기본적으로 인바운드 전환 모집단에서 추가적인 필터링을 수행하는 데 사용됩니다.

기본 집합은 인바운드 전환 간에 정의됩니다. 다른 인바운드 전환의 멤버는 기본 집합에서 제외됩니다. 제외 활동의 아웃바운드 전환에는 다른 인바운드 전환에서 발생하지 않은 기본 집합의 멤버만 포함됩니다.

## 구성 {#configuration}

1. **[!UICONTROL Exclusion]** 활동을 워크플로우로 끌어서 놓습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업에서 ![](assets/edit_darkgrey-24px.png) 버튼을 사용하여 활동을 엽니다.
1. 인바운드 전환에서 **[!UICONTROL Primary set]**&#x200B;을(를) 선택합니다. 요소가 제외되는 집합입니다. 다른 집합은 기본 집합에서 제외되기 전에 요소와 일치합니다.

   >[!NOTE]
   >
   >인바운드 전환에는 동일한 유형의 모집단이 포함되어야 합니다. 예를 들어 기본 집합에 테스트 프로필이 포함되어 있으면 다른 전환에도 테스트 프로필이 포함되어야 합니다.

1. 필요한 경우 활동의 [전환](../../automating/using/activity-properties.md)을 관리하여 아웃바운드 모집단에 대한 고급 옵션에 액세스합니다.
1. 활동 구성을 확인하고 워크플로우를 저장합니다.

## 예제 {#example}

다음 예제는 18세에서 27세 사이의 잘못된 이메일 주소를 가진 Adobe Campaign 데이터베이스의 프로필을 필터링하도록 구성된 두 개의 쿼리 활동을 보여줍니다. 이메일 주소가 잘못된 프로필은 첫 번째 집합에서 제외됩니다. 그런 다음 예를 들어 이메일을 보낼 수 있습니다.

![](assets/wkf_exclusion_example.png)

