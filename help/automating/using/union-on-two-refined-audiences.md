---
title: 정교화한 두 대상자 결합
description: 이 사용 사례는 두 대상자 읽기 활동의 결합을 보여줍니다.
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: readAudience,main
feature: Workflows
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: 6261f800-11bd-4b02-a587-49ddb0da240f
TQID: 'https://experienceleague.adobe.com/NZA7DqSxrgPvNPfo4dgWvyJaOp-2Ma07MZJuHff3sAA'
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
  - id: f5407121-8933-4ac3-8e06-a9b692a4e88a
    internal-label: Campaign Standard
feature_v2:
  - id: a658c786-869b-4194-a780-2594d663adda
    internal-label: Data management
subfeature_v2:
  - id: fcb46c0f-76e1-48bc-9dd0-fcf9d97526cf
    internal-label: Workflows
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
source-git-commit: bb37e2bfbc52de1b0cc03f0f8e03985caff5e5b0
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 43%
---
# 정교화한 두 대상자 결합 {#example--union-on-two-refined-audiences}

이 예제에 정의된 워크플로는 두 **[!UICONTROL Read audience]** 활동의 결합을 보여줍니다. 이 워크플로우의 목표는 18세에서 30세 사이의 골드 또는 실버 멤버에게 이메일을 보내는 것입니다. 골드 및 실버 멤버를 추적하기 위해 특정 대상자를 시스템에 미리 만들어 놓았습니다.

워크플로는 다음과 같이 디자인됩니다.

![](assets/readaudience_activity_example1.png)

* 골드 멤버 대상자를 검색하고 18세에서 30세 사이의 프로필만 선택하여 정교화하는 첫 번째 [대상자 읽기](../../automating/using/read-audience.md) 활동.
* 두 번째 **[!UICONTROL Read audience]** 활동으로 실버 멤버 대상자를 검색하고 18세에서 30세 사이의 프로필만 선택하여 정교화합니다.
* 두 **[!UICONTROL Read audiences]** 활동의 모집단을 하나의 최종 모집단으로 통합하는 [Union](../../automating/using/union.md) 활동입니다.
* **[!UICONTROL Union]** 활동에서 만든 모집단에 전자 메일을 보내는 [전자 메일 게재](../../automating/using/email-delivery.md) 활동.
