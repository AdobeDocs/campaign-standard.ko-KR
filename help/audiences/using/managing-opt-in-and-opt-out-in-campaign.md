---
title: Campaign에서 옵트인 및 옵트아웃 관리
description: Adobe Campaign에서 옵트인 및 옵트아웃을 관리하는 방법을 이해합니다.
audience: audiences
content-type: reference
topic-tags: understanding-opt-in-and-opt-out-processes
feature: Audiences
role: User
level: Intermediate
exl-id: 4aeb90c5-f5b5-4cfe-93fb-2fd01fb8d70e
source-git-commit: 8be43668d1a4610c3388ad27e493a689925dc88c
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 8%

---

# Campaign에서 옵트인 및 옵트아웃 관리{#managing-opt-in-and-opt-out-in-campaign}

## 프로필에서 옵트인 및 옵트아웃 관리 {#managing-opt-in-and-opt-out-from-a-profile}

**[!UICONTROL General]** 프로필 탭에서 연산자가 직접 사용자를 옵트인하거나 옵트아웃할 수 있습니다.

**[!UICONTROL No longer contact (on denylist)]** 섹션에서 선택한 확인란은 사용자가 옵트아웃하도록 선택한 채널에 해당합니다. 사용자의 필요에 따라 채널을 선택합니다.

![](assets/optin_landingpage_3.png)

## 옵트인 및 옵트아웃 랜딩 페이지 설정 {#setting-up-opt-in-and-opt-out-landing-pages}

사용자에게 옵트인 또는 옵트아웃 기능을 부여하려면 **[!UICONTROL Profile acquisition]** 랜딩 페이지를 만들어 게시해야 합니다. 그런 다음 필요에 따라 채널을 선택할 수 있습니다. 이렇게 하려면 아래 단계를 수행합니다.

사용자가 모든 게재에서 옵트아웃할 수 있도록 **[!UICONTROL Denylist]** 랜딩 페이지를 설정할 수도 있습니다. 자세한 내용은 [모든 게재에서 옵트아웃할 랜딩 페이지 설정](#setting-up-a-landing-page-to-opt-out-from-all-deliveries)을 참조하세요.

>[!NOTE]
>
>랜딩 페이지를 사용하여 서비스 구독을 활성화할 수도 있습니다. 자세한 정보는 이 [페이지](../../channels/using/configuring-landing-page.md#linking-a-landing-page-to-a-service)를 참조하십시오.

1. **[!UICONTROL Profile acquisition]** 랜딩 페이지를 만듭니다([이 섹션](../../channels/using/getting-started-with-landing-pages.md) 참조).
1. 원하는 각 채널의 랜딩 페이지 컨텐츠에 확인란을 추가한 다음 Campaign 데이터베이스의 해당 필드에 연결합니다.

   ![](assets/optin_landingpage_1.png)

1. 랜딩 페이지를 저장하고 게시합니다.
1. 랜딩 페이지에서 **[!UICONTROL General]** 프로필 탭에 따라 확인란이 이미 선택되었습니다. 사용자는 필요에 따라 채널을 선택 또는 선택 취소하고 양식을 제출할 수 있습니다.

   ![](assets/optin_landingpage_2.png)

1. 양식을 제출하면 사용자의 선택에 따라 **[!UICONTROL General]** 프로필 탭이 업데이트됩니다.

   ![](assets/optin_landingpage_3.png)

### 모든 게재에서 옵트아웃하는 랜딩 페이지 설정 {#setting-up-a-landing-page-to-opt-out-from-all-deliveries}

사용자에게 모든 게재에서 옵트아웃할 수 있는 기능을 제공하려면 **[!UICONTROL Denylist]** 랜딩 페이지를 만들고 게시해야 합니다. 랜딩 페이지 만들기에 대한 자세한 정보는 [이 페이지](../../channels/using/getting-started-with-landing-pages.md)를 참조하세요.

사용자가 랜딩 페이지 링크를 클릭하면 프로필의 **[!UICONTROL No longer contact (by any channel)]** 옵션이 자동으로 선택됩니다.

![](assets/blocklisting_allchannels.png)
