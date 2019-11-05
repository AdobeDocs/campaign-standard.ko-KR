---
title: 예외
description: 제외 활동을 사용하면 특정 기준에 따라 한 모집단에서 요소를 제외할 수 있습니다.
page-status-flag: 활성화 안 함
uuid: b79e7f73-37a0-4ec3-ac5a-5449dc1b1f22
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 자동화
content-type: reference
topic-tags: 타깃팅 활동
discoiquuid: d5312fcd-43ad-428e-bde9-90f062e9358c
context-tags: 제외,기본
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 예외{#exclusion}

## 설명 {#description}

![](assets/exclusion.png)

활동을 **[!UICONTROL Exclusion]** 사용하면 특정 기준에 따라 한 모집단에서 요소를 제외할 수 있습니다.

## 사용 상황 {#context-of-use}

이 **[!UICONTROL Exclusion]** 활동은 기본적으로 인바운드 전환 모집단에서 추가적인 필터링을 수행하는 데 사용됩니다.

기본 세트는 인바운드 전환 중에 정의됩니다. 다른 인바운드 전환의 멤버는 기본 세트에서 제외됩니다. 제외 활동의 아웃바운드 전환에는 다른 인바운드 전환에서 발생하지 않은 기본 세트의 멤버만 포함됩니다.

## 구성 {#configuration}

1. 워크플로우를 워크플로우로 드래그하여 **[!UICONTROL Exclusion]** 놓을 수 있습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 엽니다.
1. 인바운드 전환 **[!UICONTROL Primary set]** 중에서 선택합니다. 요소가 제외되는 세트입니다. 다른 세트는 기본 세트에서 제외되기 전에 일치 요소를 설정합니다.

   >[!NOTE]
   >
   >인바운드 전환에는 동일한 유형의 모집단 이 포함되어야 합니다. 예를 들어, 기본 세트에 테스트 프로필이 포함되어 있으면 다른 전환에도 테스트 프로필이 포함되어야 합니다.

1. 필요한 경우 활동의 전환을 관리하여 [아웃바운드](../../automating/using/executing-a-workflow.md#managing-an-activity-s-outbound-transitions) 모형에 대한 고급 옵션에 액세스합니다.
1. 활동 구성을 확인하고 워크플로우를 저장합니다.

## 예 {#example}

다음 예에서는 18세에서 27세 사이이고 잘못된 이메일 주소를 가진 Adobe Campaign 데이터베이스에서 프로필을 필터링하도록 구성된 두 개의 쿼리 활동을 보여줍니다. 이메일 주소가 잘못된 프로필은 첫 번째 세트에서 제외됩니다. 그러면 예를 들어 이메일을 보낼 수 있습니다.

![](assets/wkf_exclusion_example.png)

