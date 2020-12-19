---
solution: Campaign Standard
product: campaign
title: 연령 그룹에 따른 세분화
description: 이 페이지에서는 연령 그룹에 따라 데이터베이스 프로필의 세그먼트를 제공합니다. 워크플로우의 목표는 각 나이 그룹에 대해 특정 이메일을 보내는 것입니다.
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

* 워크플로우의 실행 날짜를 지정하는 [스케줄러 활동](../../automating/using/segmentation.md).
* 생일 및 이메일 주소를 입력한 사람의 프로필을 대상으로 하는 [쿼리](../../automating/using/query.md) 활동.
* 다른 아웃바운드 전환으로 구분된 3개의 세그먼트를 만드는 [세그멘테이션](../../automating/using/segmentation.md) 활동:32세 이상의 18-25-year, 26-32-year 이전 버전 및 프로파일 세그먼트는 다음 매개 변수에 따라 정의됩니다.

   ![](assets/wkf_segment_example_3.png)

   * 세그먼트의 나이 그룹을 정의하는 나이 필터

      ![](assets/wkf_segment_new_segment.png)

   * 100의 제한&#x200B;**[!UICONTROL Maximum size]**&#x200B;에 연결된 유형 제한&#x200B;**[!UICONTROL Random sampling]**

      ![](assets/wkf_segment_example_1.png)

* 세그먼트당 [이메일 배달](../../automating/using/email-delivery.md) 활동.
