---
title: 포크
description: 분기 활동을 사용하면 여러 활동을 동시에 시작할 수 있는 아웃바운드 전환을 만들 수 있습니다.
page-status-flag: 활성화 안 함
uuid: e4eaf69b-84ee-4f79-8b80-99284697cd2c
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 자동화
content-type: reference
topic-tags: 실행 활동
discoiquuid: f8ffe7af-e18c-4599-8fd0-fcd192565323
context-tags: 포크,주
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 포크{#fork}

## 설명 {#description}

![](assets/fork.png)

활동을 통해 여러 활동을 동시에 시작하도록 아웃바운드 전환을 만들 수 있습니다. **[!UICONTROL Fork]**

## 사용 상황 {#context-of-use}

이 **[!UICONTROL Fork]** 활동을 통해 동일한 워크플로우 내에서 독립적으로 여러 가지 다른 활동을 수행할 수 있습니다.

## 구성 {#configuration}

1. 워크플로우를 워크플로우로 드래그하여 **[!UICONTROL Fork]** 놓을 수 있습니다.
1. 쿼리 등 앞에 오는 다른 활동에 연결합니다.
1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 엽니다.
1. 아웃바운드 전환 수를 생성, 삭제 또는 복제하여 지정합니다. 이름과 레이블을 여기에 지정할 수도 있습니다.
1. 활동 구성을 확인하고 워크플로우를 저장합니다.

## 예 {#example}

다음 예에서는 Adobe Campaign 데이터베이스에서 프로파일을 타깃팅하는 두 개의 쿼리 활동(이 경우 파리에 거주하는 여성)의 교차 영역을 보여줍니다. 따라서 포크 활동을 통해 여러 활동을 동시에 사용할 수 있습니다.계산된 모집단을 기억하도록 고객을 저장하고 각 세그먼트에 대한 타깃팅된 컨텐츠가 있는 두 개의 서로 다른 이메일을 모집단을 세그먼트화하는 것이 좋습니다. 첫 번째 메일은 18세에서 40세 사이의 파리의 여성들에게 발송되었고 또 다른 것은 40세 이상의 파리의 여성을 목표로 하는 것이다.

![](assets/wkf_fork_example.png)

