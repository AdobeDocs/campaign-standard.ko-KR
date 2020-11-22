---
solution: Campaign Standard
product: campaign
title: 연령 그룹에 따른 세분화
description: 이 페이지에서는 연령 그룹에 따라 데이터베이스 프로필의 세그먼테이션을 제공합니다. 워크플로우의 목표는 각 나이 그룹에 대해 특정 이메일을 보내는 것입니다.
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: segmentation,main
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 66%

---


# 연령 그룹에 따른 세분화 {#segmentation-age-groups}

다음 예제에서는 나이 그룹에 따라 데이터베이스 프로필을 세분화하는 방법을 보여줍니다.

워크플로우의 목표는 각 나이 그룹에 대해 특정 이메일을 보내는 것입니다. 이 워크플로우는 테스트 캠페인의 일부이므로, 각 세그먼트는 임의로 선택한 최대 100개의 프로필만 포함할 수 있습니다. 제한되어 있고 대표적인 대상자를 사용하기 위해서입니다. 

![](assets/wkf_segment_example_4.png)

워크플로우는 다음 요소로 구성됩니다.

* A [Scheduler activity](../../automating/using/segmentation.md) to specify the workflow&#39;s execution date.
* A [Query](../../automating/using/query.md) activity to target profiles of people whose birthday and email address have been entered.
* A [Segmentation](../../automating/using/segmentation.md) activity to create 3 segments divided into different outbound transitions: 18-25-year old, 26-32-year old and profiles that are over 32 years old. 세그먼트는 다음 매개 변수에 따라 정의됩니다.

   ![](assets/wkf_segment_example_3.png)

   * 세그먼트의 나이 그룹을 정의하는 나이 필터

      ![](assets/wkf_segment_new_segment.png)

   * 100의 제한&#x200B;**[!UICONTROL Maximum size]**&#x200B;에 연결된 유형 제한&#x200B;**[!UICONTROL Random sampling]**

      ![](assets/wkf_segment_example_1.png)

* 세그먼트별 [이메일 배달](../../automating/using/email-delivery.md) 활동.
