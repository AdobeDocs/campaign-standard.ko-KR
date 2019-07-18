---
title: and-join
seo-title: and-join
description: and-join
seo-description: AND-Join 활동을 사용하면 워크플로우의 여러 실행 분기를 동기화할 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 9 B 54 FD 4 C -9915-400 F-A 494-74 E 52 C 329 B 8 A
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 실행 활동
discoiquuid: 4 b 55 EFA 2-652 e -4493-BFA 7-EAEE 59 B 383 CA
context-tags: Andjoin, Main
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: e384a0cef325bc01eb5ea050b0f3d926aea9a88f

---


# AND-join{#and-join}

## Description {#description}

![](assets/and_join.png)

**[!UICONTROL AND-join]** 활동을 통해 워크플로우의 여러 실행 분기를 동기화할 수 있습니다.

## Context of use {#context-of-use}

**[!UICONTROL AND-join]** 이 활동은 모든 인바운드 전환이 활성화되면, 즉 이전에 모든 활동이 완료되면 아웃바운드 전환만 트리거합니다.

## Configuration {#configuration}

1. 워크플로우에 쿼리와 같은 여러 활동을 놓아 두 개 이상의 다른 실행 분기를 형성합니다.
1. **[!UICONTROL AND-join]** 워크플로우를 워크플로우로 드래그하여 놓습니다.
1. 동기화하려는 두 개의 분기 이후에 연결하십시오.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. 아웃바운드 전환에 유지할 기본 세트를 선택합니다. 설정을 선택하지 않으면 활동에서 임의 모집단이 전송됩니다.
1. 활동의 구성을 확인하고 워크플로우를 저장합니다.

## Example {#example}

The following example shows two workflow branches before they are joined with the **[!UICONTROL AND-join]** activity. File extraction can only take place when the three inbound transitions of the **[!UICONTROL AND-join]** activity are enabled.

![](assets/wkf_and-join_example.png)

