---
title: fork
seo-title: fork
description: fork
seo-description: Fork Activity를 사용하면 아웃바운드 전환을 만들어 동시에 여러 활동을 시작할 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: E 4 EAF 69 B -84 EE -4 F 79-8 B 80-99284697 CD 2 C
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 실행 활동
discoiquuid: F 8 FFE 7 AF-E 18 C -4599-8 FD 0-FCD 192565323
context-tags: fork, main
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: e384a0cef325bc01eb5ea050b0f3d926aea9a88f

---


# Fork{#fork}

## Description {#description}

![](assets/fork.png)

**[!UICONTROL Fork]** 활동을 통해 아웃바운드 전환을 만들어 동시에 여러 활동을 시작할 수 있습니다.

## Context of use {#context-of-use}

**[!UICONTROL Fork]** 활동을 통해 동일한 워크플로우 내에서 독립적인 여러 활동을 수행할 수 있습니다.

## Configuration {#configuration}

1. **[!UICONTROL Fork]** 워크플로우를 워크플로우로 드래그하여 놓습니다.
1. 쿼리 등의 다른 활동 (예: 쿼리) 에 연결합니다.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. 아웃바운드 전환 수를 만들거나 삭제하거나 복제하여 지정합니다. 이름과 레이블을 속성에 매핑할 수도 있습니다.
1. 활동의 구성을 확인하고 워크플로우를 저장합니다.

## Example {#example}

다음 예는 Adobe Campaign 데이터베이스에서 프로파일을 타깃팅하는 두 개의 쿼리 활동 (이 경우, 파리에 거주하는 여성) 의 교차점을 보여줍니다. 따라서 분기 활동은 여러 활동을 동시에 사용할 수 있도록 해줍니다. 하나는 계산된 모집단을 기억하도록 대상을 저장하고 다른 하나는 모집단을 세그먼트화하여 각 세그먼트에 대한 타깃팅된 컨텐츠가 포함된 두 개의 다른 이메일을 보냅니다. 첫 번째 이메일은 18 세에서 40 세 사이의 파리 여성 및 40 세 이상의 파리 여성을 대상으로 한 것입니다.

![](assets/wkf_fork_example.png)

