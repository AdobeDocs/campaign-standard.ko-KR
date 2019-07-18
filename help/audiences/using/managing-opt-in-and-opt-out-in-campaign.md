---
title: 캠페인에서 옵트인 및 옵트아웃 관리
seo-title: 캠페인에서 옵트인 및 옵트아웃 관리
description: 캠페인에서 옵트인 및 옵트아웃 관리
seo-description: Adobe Campaign에서 옵트인 및 옵트아웃을 관리하는 방법을 이해합니다.
page-status-flag: 정품 인증 안 함
uuid: AA 1801 EC -562 B -420 E -8 D 79-C 07 D 066 B 7 B 1 A
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 대상
content-type: 참조
topic-tags: understanding-opt-in-and-opt-out-processes
discoiquuid: 6 b 5680 f 2-bba 9-453 e-a 0 d 5-8 ca 69 dd 02001
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Managing opt-in and opt-out in Campaign{#managing-opt-in-and-opt-out-in-campaign}

## Managing opt-in and opt-out from a profile {#managing-opt-in-and-opt-out-from-a-profile}

Users can be opted in or out by an operator directly from the profile **[!UICONTROL General]** tab.

**[!UICONTROL No longer contact (blacklist)]** 섹션에서 선택한 확인란은 사용자가 그만두기로 선택한 채널에 해당합니다. 사용자의 요구 사항에 따라 채널을 선택합니다.

![](assets/optin_landingpage_3.png)

## Setting up opt-in and opt-out landing pages {#setting-up-opt-in-and-opt-out-landing-pages}

To give users the ability to opt in or opt out, you have to create and publish a **[!UICONTROL Profile acquisition]** landing page. 필요에 따라 채널을 선택할 수 있습니다. 이렇게 하려면 아래 단계를 따르십시오.

You can also set up a **[!UICONTROL BlackList]** landing page that will enable users to opt out from all deliveries. For more on this, refer to [Setting up a landing page to opt out from all deliveries](../../audiences/using/managing-opt-in-and-opt-out-in-campaign.md#setting-up-a-landing-page-to-opt-out-from-all-deliveries).

>[!NOTE]
>
>랜딩 페이지를 사용하여 서비스 구독을 활성화할 수도 있습니다. For more on this, refer to [this page](../../channels/using/designing-a-landing-page.md#linking-a-form-to-a-service).

1. **[!UICONTROL Profile acquisition]** 랜딩 페이지 만들기 ( [이 섹션](../../channels/using/about-landing-pages.md)참조).
1. 원하는 각 채널에 대한 랜딩 페이지 컨텐츠에 확인란을 추가한 다음 캠페인 데이터베이스의 해당 필드에 연결합니다.

   ![](assets/optin_landingpage_1.png)

1. 랜딩 페이지를 저장하고 게시합니다.
1. In the landing page, the checkboxes are already selected according to the profile **[!UICONTROL General]** tab. 사용자는 필요에 따라 채널을 선택하거나 선택 취소할 수 있으며 양식을 제출할 수 있습니다.

   ![](assets/optin_landingpage_2.png)

1. Once the form submitted, the profile **[!UICONTROL General]** tab is updated according to the user's selection.

   ![](assets/optin_landingpage_3.png)

### Setting up a landing page to opt out from all deliveries {#setting-up-a-landing-page-to-opt-out-from-all-deliveries}

To give users the ability to opt out from all deliveries, you have to create and publish a **[!UICONTROL BlackList]** landing page. For more on landing pages creation, refer to [this page](../../channels/using/about-landing-pages.md).

Once a user clicks on the landing page link, the **[!UICONTROL No longer contact (by any channel)]** option in the profile is automatically selected.

![](assets/blacklisting_allchannels.png)

