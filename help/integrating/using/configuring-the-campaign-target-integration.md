---
title: Campaign-Target 통합 구성
description: Adobe Campaign에서 다이내믹 콘텐츠를 사용하기 시작하도록 Adobe Target 통합을 구성하는 방법에 대해 알아봅니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-target
feature: Triggers
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: d382bfdd-418d-46c1-98dd-df8626f85cac
TQID: https://experienceleague.adobe.com/trfuEp6pEd2jFADsK6NMw6tx8ASi86ZFur56AjwnpWQ
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 184
ht-degree: 5%

---

# Campaign-Target 통합 구성{#configuring-the-campaign-target-integration}

Adobe Campaign과 Adobe Target을 통합하면 게재에 동적 콘텐츠를 삽입할 수 있습니다.

Adobe Target과의 통합 기능을 사용하려면 먼저 Adobe Campaign에서 구성이 필요하며, 기능 관리자가 관리해야 합니다.

이 절차에는 다음 요소가 필요합니다.

* Adobe Experience Cloud 테넌트
* Adobe Target 테넌트
* Adobe Campaign과의 연결을 설정하기 위해 지정된 Adobe Target rawbox

1. 고급 메뉴에서 왼쪽 상단 모서리의 Adobe Campaign 로고를 통해 **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** > **[!UICONTROL Options]**&#x200B;을(를) 선택합니다.
1. Adobe Target에 대한 서버 및 테넌트 옵션을 구성하려면 다음 필드에 적절하게 을(를) 입력합니다.

   * **[!UICONTROL TNT_TenantName]**: Adobe Target 테넌트의 이름입니다. 이 값은 Adobe Target **[!UICONTROL Client]**&#x200B;의 이름에 해당합니다.
   * **[!UICONTROL TNT_EdgeServer]**: 통합에 사용되는 Adobe Target 서버입니다. 이 옵션은 이미 기본적으로 제공됩니다. 이 값은 Adobe Target **[!UICONTROL Server Domain]** 다음에 **/m2** 값이 옵니다. 예: **tt.omtrdc.net/m2**.

   ![](assets/tar_options.png)

이제 사용자는 Adobe Target을 사용하여 게재에 동적 이미지를 추가할 수 있습니다.
