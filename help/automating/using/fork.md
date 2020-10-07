---
title: 포크
description: 포크 활동을 사용하면 아웃바운드 전환을 만들어서 여러 활동을 동시에 시작할 수 있습니다.
page-status-flag: never-activated
uuid: e4eaf69b-84ee-4f79-8b80-99284697cd2c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities
discoiquuid: f8ffe7af-e18c-4599-8fd0-fcd192565323
context-tags: fork,main
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 100%

---


# 포크{#fork}

## 설명 {#description}

![](assets/fork.png)

**[!UICONTROL Fork]** 활동을 사용하면 아웃바운드 전환을 만들어서 여러 활동을 동시에 시작할 수 있습니다.

## 사용의 컨텍스트 {#context-of-use}

**[!UICONTROL Fork]** 활동을 사용하면 동일한 워크플로우 내에서 독립적으로 여러 가지 다른 활동을 수행할 수 있습니다.

## 구성 {#configuration}

1. **[!UICONTROL Fork]** 활동을 워크플로우로 끌어서 놓습니다.
1. 쿼리와 같은 앞에 오는 다른 활동과 연결합니다.
1. 활동을 선택한 다음 나타나는 바로 가기의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 활동을 엽니다.
1. 아웃바운드 전환 수를 만들기, 삭제 또는 복제하여 지정합니다. 이름과 레이블을 지정할 수도 있습니다.
1. 활동 구성을 확인하고 워크플로우를 저장합니다.

## 예제 {#example}

다음 예제에서는 Adobe Campaign 데이터베이스에서 프로필을 타겟팅하는 두 개의 쿼리 활동(이 경우 파리에 거주하는 여성)의 교차를 보여줍니다. 따라서 포크 활동을 사용하면 여러 활동을 동시에 사용할 수 있습니다. 하나는 계산된 모집단을 기억하도록 대상자를 저장하는 것이고 다른 하나는 각 세그먼트에 타겟팅된 콘텐츠로 두 개의 다른 전자 메일을 전송하도록 모집단을 세그먼트화하는 것입니다. 첫 전자 메일은 18세에서 40세 사이의 파리의 여성들에게 발송됐으며 다른 전자 메일은 40세 이상의 파리의 여성을 타겟팅합니다.

![](assets/wkf_fork_example.png)

