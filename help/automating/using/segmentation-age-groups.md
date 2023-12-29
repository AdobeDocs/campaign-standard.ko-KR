---
title: 연령 그룹에 따른 세분화
description: 이 페이지에는 연령 그룹에 따른 데이터베이스 프로필의 세그먼테이션이 표시됩니다. 워크플로우의 목표는 각 연령 그룹에 대해 특정 이메일을 보내는 것입니다.
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: segmentation,main
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: dab7ef86-4776-48f4-be9a-37de316e0dd9
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 51%

---

# 연령 그룹에 따른 세분화 {#segmentation-age-groups}

다음 예제에서는 나이 그룹에 따라 데이터베이스 프로필을 세분화하는 방법을 보여줍니다.

워크플로우의 목표는 각 나이 그룹에 대해 특정 이메일을 보내는 것입니다. 이 워크플로우는 테스트 캠페인의 일부이므로, 각 세그먼트는 임의로 선택한 최대 100개의 프로필만 포함할 수 있습니다. 제한되어 있고 대표적인 대상자를 사용하기 위해서입니다. 

![](assets/wkf_segment_example_4.png)

워크플로우는 다음 요소로 구성됩니다.

* A [스케줄러 활동](../../automating/using/segmentation.md) 워크플로우의 실행 날짜를 지정합니다.
* A [쿼리](../../automating/using/query.md) 활동은 생일 및 이메일 주소를 입력한 사람의 프로필을 타겟팅합니다.
* A [세분화](../../automating/using/segmentation.md) 활동은 3개의 세그먼트(18~25세, 26~32세 및 32세가 넘는 프로필)를 만들어 다양한 아웃바운드 전환으로 나눕니다. 세그먼트는 다음 매개 변수에 따라 정의됩니다.

  ![](assets/wkf_segment_example_3.png)

   * 세그먼트의 나이 그룹을 정의하는 나이 필터

     ![](assets/wkf_segment_new_segment.png)

   * 100의 제한&#x200B;**[!UICONTROL Maximum size]**&#x200B;에 연결된 유형 제한&#x200B;**[!UICONTROL Random sampling]**

     ![](assets/wkf_segment_example_1.png)

* An [이메일 게재](../../automating/using/email-delivery.md) 세그먼트당 활동.
