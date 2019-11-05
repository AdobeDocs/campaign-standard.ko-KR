---
title: Campaign-Target 통합 구성
description: Adobe Campaign에서 동적 컨텐츠 사용을 시작하도록 Adobe Target 통합을 구성하는 방법을 알아봅니다.
page-status-flag: 활성화 안 함
uuid: 0df5701c-dc26-4c30-9af9-ebf92815d90c
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 통합
content-type: reference
topic-tags: working-with-campaign-and-target
discoiquuid: f7fb2084-dd6f-4aa2-940f-e4871314635
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# Campaign-Target 통합 구성{#configuring-the-campaign-target-integration}

Adobe Campaign과 Adobe Target 간의 통합을 통해 전달에 동적 컨텐츠를 삽입할 수 있습니다.

Adobe Target과 통합 기능을 사용하려면 먼저 Adobe Campaign에서 구성이 필요하며 기능 관리자가 관리해야 합니다.

이 절차에는 다음 요소가 필요합니다.

* Adobe Experience Cloud 임차인
* Adobe Target 임차인
* Adobe Campaign과의 연결을 설정하기 위해 지정된 Adobe Target rawbox

1. 고급 메뉴에서 왼쪽 상단에 있는 Adobe Campaign 로고를 통해 **[!UICONTROL Administration]** &gt; **[!UICONTROL Application settings]** &gt; **[!UICONTROL Options]**&#x200B;을 선택합니다.
1. Adobe Target에 대한 서버 및 테넌트 옵션을 구성하려면 다음 필드를 그에 따라 채웁니다.

   * **[!UICONTROL TNT_TenantName]**:Adobe Target 임차인의 이름입니다. 이 값은 Adobe Target의 이름에 해당합니다 **[!UICONTROL Client]**.
   * **[!UICONTROL TNT_EdgeServer]**:통합에 사용되는 Adobe Target 서버. 이 옵션은 기본적으로 이미 제공됩니다. 이 값은 Adobe Target에 **[!UICONTROL Server Domain]**&#x200B;대응하고 **/m2** 값에 해당합니다. 예:tt.omtrdc.net/m2 ****.
   ![](assets/tar_options.png)

이제 사용자는 Adobe Target을 통해 전달에 동적 이미지를 추가할 수 있습니다.
