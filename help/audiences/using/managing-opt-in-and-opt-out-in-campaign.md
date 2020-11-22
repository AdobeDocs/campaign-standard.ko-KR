---
solution: Campaign Standard
product: campaign
title: Campaign에서 옵트인 및 옵트아웃 관리
description: Adobe Campaign에서 옵트인 및 옵트아웃을 관리하는 방법을 이해합니다.
audience: audiences
content-type: reference
topic-tags: understanding-opt-in-and-opt-out-processes
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 8%

---


# Campaign에서 옵트인 및 옵트아웃 관리{#managing-opt-in-and-opt-out-in-campaign}

## 프로필에서 옵트인 및 옵트아웃 관리 {#managing-opt-in-and-opt-out-from-a-profile}

사용자는 프로필 **[!UICONTROL General]** 탭에서 직접 연산자에 의해 옵트인되거나 옵트아웃될 수 있습니다.

이 **[!UICONTROL No longer contact (on denylist)]** 섹션에서 선택한 확인란은 사용자가 그만두기로 선택한 채널에 해당됩니다. 사용자의 요구 사항에 따라 채널을 선택합니다.

![](assets/optin_landingpage_3.png)

## 옵트인 및 옵트아웃 랜딩 페이지 설정 {#setting-up-opt-in-and-opt-out-landing-pages}

사용자에게 옵트인 또는 옵트아웃 기능을 제공하려면 **[!UICONTROL Profile acquisition]** 랜딩 페이지를 만들고 게시해야 합니다. 그러면 필요에 따라 채널을 선택할 수 있게 됩니다. 이렇게 하려면 아래 단계를 수행합니다.

사용자가 모든 배달에서 옵트아웃할 수 있도록 하는 **[!UICONTROL Denylist]** 랜딩 페이지를 설정할 수도 있습니다. 자세한 내용은 랜딩 페이지 [설정을 참조하여 모든 배달에서 제외합니다](#setting-up-a-landing-page-to-opt-out-from-all-deliveries).

>[!NOTE]
>
>랜딩 페이지를 사용하여 서비스 구독을 활성화할 수도 있습니다. 자세한 정보는 이 [페이지](../../channels/using/configuring-landing-page.md#linking-a-landing-page-to-a-service)를 참조하십시오.

1. 랜딩 **[!UICONTROL Profile acquisition]** 페이지를 만듭니다( [이 섹션 참조](../../channels/using/getting-started-with-landing-pages.md)).
1. 원하는 각 채널에 대한 랜딩 페이지 컨텐츠에 확인란을 추가한 다음 캠페인 데이터베이스의 해당 필드에 연결합니다.

   ![](assets/optin_landingpage_1.png)

1. 랜딩 페이지를 저장하고 게시합니다.
1. 랜딩 페이지에서 확인란은 프로필 **[!UICONTROL General]** 탭에 따라 이미 선택되어 있습니다. 사용자는 필요에 따라 채널을 선택하거나 선택 취소하고 양식을 제출할 수 있습니다.

   ![](assets/optin_landingpage_2.png)

1. 양식이 제출되면 사용자의 선택에 따라 프로필 **[!UICONTROL General]** 탭이 업데이트됩니다.

   ![](assets/optin_landingpage_3.png)

### 모든 배달에서 옵트아웃할 랜딩 페이지 설정 {#setting-up-a-landing-page-to-opt-out-from-all-deliveries}

사용자에게 모든 게재에서 옵트아웃할 수 있는 권한을 제공하려면 **[!UICONTROL Denylist]** 랜딩 페이지를 만들고 게시해야 합니다. 랜딩 페이지 만들기에 대한 자세한 내용은 [이 페이지를 참조하십시오](../../channels/using/getting-started-with-landing-pages.md).

사용자가 랜딩 페이지 링크를 클릭하면 프로필의 **[!UICONTROL No longer contact (by any channel)]** 옵션이 자동으로 선택됩니다.

![](assets/blocklisting_allchannels.png)

