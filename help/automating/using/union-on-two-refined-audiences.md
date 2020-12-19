---
solution: Campaign Standard
product: campaign
title: 정교화한 대상자 두 개 결합
description: 이 사용 사례는 두 개의 읽기 대상 활동 조합을 보여줍니다.
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: readAudience,main
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 58%

---


# 정교화한 대상자 두 개 결합 {#example--union-on-two-refined-audiences}

이 예제에 정의된 워크플로우는 두 **[!UICONTROL Read audience]** 활동의 결합을 보여줍니다. 이 워크플로우의 목표는 18세에서 30세 사이의 골드 또는 실버 멤버에게 이메일을 보내는 것입니다. 골드 및 실버 멤버를 추적하기 위해 특정 대상자를 시스템에 미리 만들어 놓았습니다.

워크플로우는 다음과 같이 디자인됩니다.

![](assets/readaudience_activity_example1.png)

* 첫 번째 [Gold 멤버 고객을 검색하고 18세에서 30세 사이의 프로필만 선택하여 이 대상자를 새로 고치는 대상](../../automating/using/read-audience.md) 활동 읽기
* 두 번째 **[!UICONTROL Read audience]** 활동으로 실버 멤버 대상자를 검색하고 18세에서 30세 사이의 프로필만 선택하여 정교화합니다.
* **[!UICONTROL Read audiences]** 활동 모두에서 모집단을 하나의 최종 모집단으로 통합하는 [Union](../../automating/using/union.md) 활동
* **[!UICONTROL Union]** 활동에서 오는 모집단에게 이메일을 보내는 [이메일 배달](../../automating/using/email-delivery.md) 활동.
