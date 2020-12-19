---
solution: Campaign Standard
product: campaign
title: Campaign-Target 통합 구성
description: Adobe Campaign에서 다이내믹 컨텐츠 사용을 시작하기 위해 Adobe Target 통합을 구성하는 방법을 알아봅니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-target
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 4%

---


# Campaign-Target 통합 구성{#configuring-the-campaign-target-integration}

Adobe Campaign과 Adobe Target 간의 통합을 통해 전달에 동적 컨텐츠를 삽입할 수 있습니다.

Adobe Campaign에서 Adobe Target과 통합 기능을 사용하려면 먼저 구성이 필요하며 기능 관리자가 관리해야 합니다.

이 절차에는 다음 요소가 필요합니다.

* Adobe Experience Cloud 테넌트
* Adobe Target 테넌트
* Adobe Campaign와의 연결을 설정하기 위해 지정된 Adobe Target rawbox

1. 고급 메뉴의 왼쪽 위 모서리에 있는 Adobe Campaign 로고를 통해 **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** > **[!UICONTROL Options]**&#x200B;를 선택합니다.
1. Adobe Target에 대한 서버 및 테넌트 옵션을 구성하려면 다음 필드에 그에 따라 입력합니다.

   * **[!UICONTROL TNT_TenantName]**:adobe target 테넌트의 이름입니다. 이 값은 Adobe Target **[!UICONTROL Client]**&#x200B;의 이름에 해당합니다.
   * **[!UICONTROL TNT_EdgeServer]**:통합에 사용되는 Adobe Target 서버. 이 옵션은 기본적으로 이미 제공됩니다. 이 값은 Adobe Target **[!UICONTROL Server Domain]**&#x200B;에 해당하고 그 뒤에 **/m2** 값이 옵니다. 예:**tt.omtrdc.net/m2**.

   ![](assets/tar_options.png)

이제 사용자는 Adobe Target을 통해 제공되는 단계에서 동적 이미지를 추가할 수 있습니다.
