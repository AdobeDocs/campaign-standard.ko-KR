---
title: 교차
description: 교차 활동을 사용하면 활동에서 서로 다른 인바운드 모집단에 공통되는 요소만 유지할 수 있습니다.
page-status-flag: 활성화 안 함
uuid: a60f9811-0158-44b3-952b-392685c006cc
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 자동화
content-type: reference
topic-tags: 타깃팅 활동
discoiquuid: 7a107d6b-edc3-44c3-bbb7-ba3dec8e43f9
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 교차{#intersection}

## 설명 {#description}

![](assets/intersection.png)

활동을 **[!UICONTROL Intersection]** 통해 활동에서 서로 다른 인바운드 모집단에 공통되는 요소만 유지할 수 있습니다.

## 사용 상황 {#context-of-use}

이 **[!UICONTROL Intersection]** 활동은 일반적으로 인바운드 전환에서 모집단을 추가로 필터링하는 데 사용됩니다.

## 구성 {#configuration}

1. 워크플로우를 워크플로우로 드래그하여 **[!UICONTROL Intersection]** 놓을 수 있습니다.
1. 쿼리 등 앞에 오는 다른 활동에 연결합니다.
1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 엽니다.
1. 다음을 **[!UICONTROL Reconciliation type]**&#x200B;선택합니다.

   * **[!UICONTROL Keys only]**:기본 모드. 활동은 서로 다른 인바운드 전환의 요소가 동일한 키를 가질 때 한 요소만 유지합니다.
   * **[!UICONTROL All shared columns]**:데이터는 인바운드 전환과 공통으로 열을 기준으로 조정됩니다. 따라서 비교를 위해 기본 세트를 선택해야 합니다. 인바운드 모집단 타깃팅 차원이 다른 경우 이 옵션을 사용할 수 있습니다.
   * **[!UICONTROL A selection of columns]**:데이터 조정을 적용할 열 목록을 정의하려면 이 옵션을 선택합니다. 먼저 기본 세트(소스 데이터가 포함된 세트)를 선택한 다음 조인에 사용할 필드를 지정해야 합니다.

1. 모든 인바운드 전환에 있는 추가 데이터만 유지하려면 **[!UICONTROL Use common additional data only]** 상자를 선택합니다.
1. 필요한 경우 활동의 전환을 관리하여 [아웃바운드](../../automating/using/executing-a-workflow.md#managing-an-activity-s-outbound-transitions) 모형에 대한 고급 옵션에 액세스합니다.
1. 활동 구성을 확인하고 워크플로우를 저장합니다.

## 예 {#example}

다음 예는 두 쿼리 활동 간의 교차를 보여줍니다. 여기에서 Adobe Campaign 데이터베이스를 살펴보고 18세에서 27세 사이의 프로필 및 이메일 주소가 각각 제공된 프로필을 검색하는 데 사용됩니다.

![](assets/wkf_intersection_example.png)

