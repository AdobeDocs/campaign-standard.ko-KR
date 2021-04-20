---
solution: Campaign Standard
product: campaign
title: AND-결합
description: AND-결합 활동을 사용하면 워크플로우의 여러 실행 분기를 동기화할 수 있습니다.
audience: automating
content-type: reference
topic-tags: execution-activities
context-tags: andjoin,main
feature: Workflows
role: Data Architect
level: Intermediate
translation-type: tm+mt
source-git-commit: 088b49931ee5047fa6b949813ba17654b1e10d60
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 98%

---


# AND-결합{#and-join}

## 설명 {#description}

![](assets/and_join.png)

**[!UICONTROL AND-join]** 활동을 사용하면 워크플로우의 여러 실행 분기를 동기화할 수 있습니다.

## 사용의 컨텍스트 {#context-of-use}

**[!UICONTROL AND-join]** 활동은 모든 인바운드 전환이 활성화되었을 때, 즉 앞선 활동이 모두 완료된 다음에만 아웃바운드 전환을 트리거합니다.

## 구성 {#configuration}

1. 워크플로우에 쿼리 등 여러 활동을 드롭하여 두 개 이상의 실행 분기를 만듭니다.
1. **[!UICONTROL AND-join]** 활동을 워크플로우로 끌어서 놓습니다.
1. 동기화하려는 서로 다른 두 분기 뒤에 연결합니다.
1. 활동을 선택한 다음 나타나는 빠른 작업에서 ![](assets/edit_darkgrey-24px.png) 버튼을 사용하여 활동을 엽니다.
1. 아웃바운드 전환에서 남겨 둘 기본 세트를 선택합니다. 선택한 세트가 없으면 활동에서 무작위 모집단이 전송됩니다.
1. 활동 구성을 확인하고 워크플로우를 저장합니다.

## 예제 {#example}

다음 예제에서는 **[!UICONTROL AND-join]** 활동으로 결합되기 전의 두 워크플로우 분기를 보여줍니다. **[!UICONTROL AND-join]** 활동의 세 인바운드 전환이 활성화된 경우에만 파일 추출을 수행할 수 있습니다.

![](assets/wkf_and-join_example.png)

