---
title: Campaign-Target 통합 구성
description: Adobe Campaign에서 동적 콘텐츠 사용을 시작하도록 Adobe Target 통합을 구성하는 방법을 알아봅니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-target
feature: Triggers
role: Data Architect
level: Intermediate
exl-id: d382bfdd-418d-46c1-98dd-df8626f85cac
source-git-commit: ee7539914aba9df9e7d46144e437c477a7e52168
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 4%

---

# Campaign-Target 통합 구성{#configuring-the-campaign-target-integration}

Adobe Campaign과 Adobe Target 간의 통합을 통해 게재에 동적 콘텐츠를 삽입할 수 있습니다.

Adobe Campaign에서 Adobe Target과의 통합 기능을 사용하려면 먼저 구성이 필요하며 기능 관리자가 관리해야 합니다.

이 절차에는 다음 요소가 필요합니다.

* Adobe Experience Cloud 테넌트
* Adobe Target 테넌트
* Adobe Campaign과의 연결을 설정하기 위해 지정된 Adobe Target rawbox

1. 고급 메뉴에서 왼쪽 상단 모서리의 Adobe Campaign 로고를 통해 을(를) 선택합니다 **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** > **[!UICONTROL Options]**.
1. Adobe Target에 대한 서버 및 테넌트 옵션을 구성하려면 다음 필드를 그에 따라 입력합니다.

   * **[!UICONTROL TNT_TenantName]**: Adobe Target 임차인의 이름입니다. 이 값은 Adobe Target의 이름에 해당합니다 **[!UICONTROL Client]**.
   * **[!UICONTROL TNT_EdgeServer]**: 통합에 사용되는 Adobe Target 서버입니다. 이 옵션은 기본적으로 이미 제공됩니다. 이 값은 Adobe Target에 해당합니다 **[!UICONTROL Server Domain]**, 그 다음 **/m2** 값. 예: **tt.omtrdc.net/m2**.

   ![](assets/tar_options.png)

이제 사용자는 Adobe Target을 사용하여 게재에서 동적 이미지를 추가할 수 있습니다.
