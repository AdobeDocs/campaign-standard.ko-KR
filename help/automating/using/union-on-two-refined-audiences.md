---
title: 정교화한 두 대상자 결합
description: 이 사용 사례에서는 두 읽기 대상 활동의 결합을 보여줍니다.
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: readAudience,main
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: 6261f800-11bd-4b02-a587-49ddb0da240f
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 58%

---

# 정교화한 두 대상자 결합 {#example--union-on-two-refined-audiences}

이 예제에 정의된 워크플로우는 두 **[!UICONTROL Read audience]** 활동의 결합을 보여줍니다. 이 워크플로우의 목표는 18세에서 30세 사이의 골드 또는 실버 멤버에게 이메일을 보내는 것입니다. 골드 및 실버 멤버를 추적하기 위해 특정 대상자를 시스템에 미리 만들어 놓았습니다.

워크플로우는 다음과 같이 디자인됩니다.

![](assets/readaudience_activity_example1.png)

* 첫 번째 [대상자 읽기](../../automating/using/read-audience.md) 활동은 골드 멤버 대상자를 검색하고 18세에서 30세 사이의 프로필만 선택하여 정교화합니다.
* 두 번째 **[!UICONTROL Read audience]** 활동으로 실버 멤버 대상자를 검색하고 18세에서 30세 사이의 프로필만 선택하여 정교화합니다.
* A [결합](../../automating/using/union.md) 두 가지 모두에서 모집단을 결합하는 활동 **[!UICONTROL Read audiences]** 활동을 하나의 최종 모집단으로 만듭니다.
* An [이메일 게재](../../automating/using/email-delivery.md) 에서 만든 모집단에 이메일을 보내는 활동 **[!UICONTROL Union]** 활동.
