---
title: AND-결합
description: AND 조인 활동을 사용하면 워크플로우의 여러 실행 분기를 동기화할 수 있습니다.
page-status-flag: 활성화 안 함
uuid: 9b54fd4c-9915-4 파섹
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 자동화
content-type: reference
topic-tags: 실행 활동
discoiquuid: 4b55efa2-65 파섹
context-tags: androin,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# AND-결합{#and-join}

## 설명 {#description}

![](assets/and_join.png)

이 **[!UICONTROL AND-join]** 활동을 통해 워크플로우의 여러 실행 분기를 동기화할 수 있습니다.

## 사용 상황 {#context-of-use}

모든 인바운드 전환이 활성화되면 활동이 아웃바운드 전환만 트리거됩니다(즉, 이전의 모든 활동이 완료된 후). **[!UICONTROL AND-join]**

## 구성 {#configuration}

1. 쿼리와 같은 여러 활동을 워크플로우에 드롭하여 두 개 이상의 다른 실행 분기를 형성할 수 있습니다.
1. 워크플로우를 워크플로우로 드래그하여 **[!UICONTROL AND-join]** 놓을 수 있습니다.
1. 동기화하려는 두 개의 서로 다른 분기 다음에 연결합니다.
1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 엽니다.
1. 아웃바운드 전환에서 유지할 기본 세트를 선택합니다. 세트를 선택하지 않으면 활동에서 무작위 모집단이 전송됩니다.
1. 활동 구성을 확인하고 워크플로우를 저장합니다.

## 예 {#example}

다음 예에서는 두 개의 워크플로우 분기가 **[!UICONTROL AND-join]** 활동과 결합되기 전에 보여 줍니다. 파일 추적은 **[!UICONTROL AND-join]** 활동의 세 가지 인바운드 전환이 활성화된 경우에만 수행할 수 있습니다.

![](assets/wkf_and-join_example.png)

