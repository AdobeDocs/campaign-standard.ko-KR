---
title: 캠페인 타겟 통합 구성
seo-title: 캠페인 타겟 통합 구성
description: 캠페인 타겟 통합 구성
seo-description: Adobe Campaign에서 동적 컨텐츠 사용을 시작하도록 Adobe Target 통합을 구성하는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: 0 df 5701 c-dc 26-4 c 30-9 af 9-ebf 92815 d 90 c
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 통합
content-type: 참조
topic-tags: working-with-campaign-and-target
discoiquuid: F 7 FB 2084-DD 6 F -4 AA 2-940 F-E 48713146635
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 698466596fdacd005dc4d72b8071208c8c39f77d

---


# Configuring the Campaign-Target integration{#configuring-the-campaign-target-integration}

Adobe Campaign와 Adobe Target 간의 통합을 통해 다이내믹한 컨텐츠를 게재에 삽입할 수 있습니다.

구성은 Adobe Target에서 Adobe Target와 통합된 기능을 사용하기 위해 먼저 필요하며 기능 관리자가 관리해야 합니다.

다음 요소는 이 절차를 위해 필요합니다.

* Adobe Experience Cloud 임차인
* Adobe Target 임차인
* Adobe Campaign 과의 연결을 설정하기 위해 지정된 Adobe Target rawbox

1. From the advanced menu, via the Adobe Campaign logo in the top left corner, select **[!UICONTROL Administration]** &gt; **[!UICONTROL Application settings]** &gt; **[!UICONTROL Options]**.
1. Adobe Target에 대한 서버 및 테넌트 옵션을 구성하려면 다음 필드를 적절하게 입력합니다.

   * **[!UICONTROL TNT_TenantName]**: Adobe Target 임차인의 이름입니다. This value corresponds to the name of the Adobe Target **[!UICONTROL Client]**.
   * **[!UICONTROL TNT_EdgeServer]**: 통합에 사용되는 Adobe Target 서버입니다. 이 옵션은 기본적으로 이미 제공됩니다. This value corresponds to the Adobe Target **[!UICONTROL Server Domain]**, followed by the **/m2** value. For example: **tt.omtrdc.net/m2**.
   ![](assets/tar_options.png)

이제 사용자는 Adobe Target를 사용하여 게시에 동적 이미지를 추가할 수 있습니다.
