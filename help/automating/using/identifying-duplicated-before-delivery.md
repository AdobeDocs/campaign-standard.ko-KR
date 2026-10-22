---
title: 게재 전 중복 확인
description: 다음의 예제에서는 이메일을 보내기 전에 타겟의 중복을 제외할 수 있는 중복 제거를 보여줍니다. 즉, 동일한 프로필에 커뮤니케이션을 여러 번 보내지 않습니다.
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: dedup,main
feature: Workflows
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: a09b101b-f76f-4377-9854-1fcffaad4f9a
TQID: 'https://experienceleague.adobe.com/4t0TujgM3kHTT36-Gy2lmiVQIRMy3OeChAw-Xx5MnWY'
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
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: bb37e2bfbc52de1b0cc03f0f8e03985caff5e5b0
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 79%
---
# 게재 전 중복 확인 {#identifying-duplicates-before-a-delivery}

다음의 예제에서는 이메일을 보내기 전에 타겟의 중복을 제외할 수 있는 중복 제거를 보여줍니다. 즉, 동일한 프로필에 커뮤니케이션을 여러 번 보내지 않습니다.

워크플로는 다음과 같이 구성됩니다.

![](assets/deduplication_example_workflow.png)

* 전자 메일 대상을 정의할 수 있는 [쿼리](../../automating/using/query.md). 여기서 워크플로는 1년 이상 클라이언트 데이터베이스에 있었던 18세에서 25세 사이의 모든 프로필을 타겟으로 합니다.

  ![](assets/deduplication_example_query.png)

* 이전 쿼리에서 얻은 중복을 식별할 수 있는 [중복 제거](../../automating/using/deduplication.md) 활동. 이 예제에서는 각 중복에 대해 하나의 레코드만 저장됩니다. 중복은 이메일 주소를 사용하여 식별됩니다. 즉, 이메일 게재는 각 이메일 주소가 타겟팅에 포함될 때마다 한 번만 전송될 수 있습니다.

  선택한 데이터 중복 제거 방법은 **[!UICONTROL Non-empty value]**&#x200B;입니다. 이를 사용하면 중복 시 유지한 레코드 중에서 **이름**&#x200B;이 제공된 레코드에 우선 순위가 부여되도록 할 수 있습니다. 이메일 콘텐츠의 개인화 필드에 이름을 사용할 경우 더욱 일관성 있게 됩니다.

  또한 중복을 유지하고 나열할 수 있도록 추가 전환이 추가되었습니다.

  ![](assets/deduplication_example_dedup.png)

* 중복 제거의 기본 아웃바운드 전환 후 배치되는 [이메일 게재](../../automating/using/email-delivery.md).
* 중복 제거의 추가 전환 후 [대상자 저장](../../automating/using/save-audience.md) 활동을 배치하여 **중복** 대상자에서 중복을 저장합니다. 이 대상자는 모든 이메일 게재에서 멤버를 직접 제외하는 데 재사용할 수 있습니다.
