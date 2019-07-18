---
title: 랜딩 페이지 공유
seo-title: 랜딩 페이지 공유
description: 랜딩 페이지 공유
seo-description: Adobe Campaign에서 랜딩 페이지를 테스트하고 게시하는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: FB 7 B 087 A -3292-496 C-BC 41-2 E 3012 BACF 59
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 채널
content-type: 참조
topic-tags: 랜딩 페이지
discoiquuid: f 7 d 4 bb 71-f 957-4 f 86-97 c 7-8 ac 0 a 0030026
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Sharing a landing page{#sharing-a-landing-page}

## About landing page publication {#about-landing-page-publication}

랜딩 페이지를 게시하기 전에 테스트를 수행해야 합니다. 실행을 확인하고 액세스 권한을 구성하고 랜딩 페이지 종료를 설정합니다. 이러한 단계는 사전 요구 사항이며 주의해서 실행해야 합니다.

## Testing the landing page {#testing-the-landing-page-}

랜딩 페이지는 플랫폼과 데이터에 영향을 주므로, 신중하게 실행해야 합니다. 이렇게 하려면:

1. Click the **[!UICONTROL Test]** button in the action bar of the landing page.
1. 테스트 화면에서 테스트 프로필을 선택하고 랜딩 페이지가 구독을 관리할 경우 테스트 서비스를 선택합니다.

   ![](assets/lp_test_2.png)

1. 필드에 데이터를 입력하고 옵션을 선택합니다.
1. 랜딩 페이지를 제출하고 데이터베이스에서 업데이트를 확인합니다.

   >[!CAUTION]
   >
   >양식을 제출하면 사용된 서비스 및 프로필이 업데이트됩니다.

1. 다양한 프로필 및 데이터로 이를 반복합니다.

   이 화면에서 랜딩 페이지 썸네일을 생성할 수도 있습니다.

## Setting up validity parameters {#setting-up-validity-parameters}

게시하기 전에 보안 이유와 플랫폼 성과를 위해 랜딩 페이지 속성에서 만료 날짜를 설정하는 것이 좋습니다. 선택한 날짜에 랜딩 페이지는 자동으로 게시 취소됩니다. 이렇게 하려면:

1. Edit the landing page properties accessed via the ![](assets/edit_darkgrey-24px.png) button in the landing page dashboard.

   ![](assets/lp_edit_properties_button.png)

1. Set up expiration date and time in the **[!UICONTROL Publication]** section: the landing page will automatically be unpublished on the specified date and therefore no longer be available.

   이 날짜와 시간에 고려될 시간대를 선택할 수 있습니다.

1. 활성 랜딩 페이지에 액세스하려고 할 때 방문자를 리디렉션할 리디렉션 URL를 정의합니다.

   ![](assets/lp_settings_general.png)

>[!CAUTION]
>
>배포 날짜 및 시간을 정의할 수도 있습니다. 그러면 랜딩 페이지가 지정된 날짜에 자동으로 게시됩니다.

## Publishing a landing page {#publishing-a-landing-page}

랜딩 페이지를 게시하면 라이브되며 방문자가 액세스할 수 있습니다.

You can unpublish or update and republish your landing page at any time, via the **[!UICONTROL Publish]** button. 그러나 다시 게시하지 못하고 랜딩 페이지가 아직 게시되지 않은 경우 첫 번째 버전은 온라인으로 유지됩니다.
