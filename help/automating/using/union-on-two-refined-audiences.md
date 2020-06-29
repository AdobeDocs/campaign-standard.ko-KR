---
title: 세련된 두 고객을 위한 결합
description: 이 사용 사례는 두 개의 읽기 대상 활동의 결합을 보여줍니다.
page-status-flag: never-activated
uuid: 58c54e71-f4a7-4ae9-80a3-33c379ab1db9
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: 674684e5-8830-4d2f-ba97-59ed4ba7422f
context-tags: readAudience,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 7ffa48365875883a98904d6b344ac005afe26e18
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---


# 세련된 두 고객을 위한 결합 {#example--union-on-two-refined-audiences}

이 예제에 정의된 워크플로우는 두 **[!UICONTROL Read audience]** 활동의 결합을 보여줍니다. 이 워크플로우의 목표는 18세에서 30세 사이의 골드 또는 실버 멤버에게 이메일을 보내는 것입니다. Gold 및 Silver 멤버를 추적하기 위해 특정 대상이 이미 시스템에 생성되었습니다.

워크플로우는 다음과 같이 설계되었습니다.

![](assets/readaudience_activity_example1.png)

* Gold 멤버 고객을 [검색하고 18세에서 30세 사이의 프로파일만을 선택하여 재평가하는 최초의 대상](../../automating/using/read-audience.md) 읽기 활동입니다.
* 실버 멤버 대상을 검색하고 18세에서 30세 사이의 프로파일만 선택하여 재정의하는 두 번째 **[!UICONTROL Read audience]** 활동입니다.
* 두 활동 [에서 하나의 최종 인구로 인구를 통합하는 연합](../../automating/using/union.md) **[!UICONTROL Read audiences]** 활동.
* 활동에서 오는 모집단에게 이메일을 보내는 [이메일 배달](../../automating/using/email-delivery.md) **[!UICONTROL Union]** 활동.
