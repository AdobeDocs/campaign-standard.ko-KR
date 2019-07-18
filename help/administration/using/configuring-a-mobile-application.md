---
title: 모바일 애플리케이션 구성
seo-title: 모바일 애플리케이션 구성
description: 모바일 애플리케이션 구성
seo-description: SDK v 4 또는 Experience Platform SDK를 사용하여 푸시 알림 또는 인앱 메시지를 보내도록 Adobe Campaign를 구성하는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: 63 E 1476 A -7875-4 F 48-BA 9 E -97 F 1 A 0007 E 42
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 관리
content-type: 참조
topic-tags: 채널 구성
discoiquuid: 2 A 14500 F -5 EDE -4131-8 B 1 A-B 7 FD 65 B 7 E 3 AA
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 4d148014d1b90712e78b8af17d7ddee2659329ed

---


# Configuring a mobile application{#configuring-a-mobile-application}

사용하려는 채널에 따라 먼저 Adobe Mobile Services에서 구성해야 하는 모바일 애플리케이션에서 푸시 알림 또는 인앱 메시지가 전송됩니다.

* 인앱 메시지와 푸시 알림을 전송하려면 Adobe Experience Platform SDK를 활용하여 Adobe Campaign에서 모바일 애플리케이션을 설정해야 합니다. See [Using Adobe Experience Platform SDK](#using-adobe-experience-platform-sdk).

* 푸시 알림만 전송하려면 SDK v 4를 사용하여 Adobe Campaign와 Adobe Mobile Service 간의 통합을 구성할 수 있습니다. See [Using SDK V4](#using-sdk-v4).

After your mobile applications are set up in Adobe Campaign by leveraging the Experience Cloud Mobile SDK V4 or Experience Platform SDK, they need to be configured by an administrator under the [!UICONTROL Administration] &gt; [!UICONTROL Channels] &gt; [!UICONTROL Mobile app] menu.

>[!CAUTION]
>
>푸시 알림과 인앱 구현은 전문가 사용자가 수행해야 합니다. 도움이 필요한 경우 Adobe 계정 담당자 또는 전문 서비스 파트너에 문의하십시오.

## Using Adobe Experience Platform SDK {#using-adobe-experience-platform-sdk}

Experience Platform SDK 애플리케이션을 사용하여 푸시 알림 및 인앱 메시지를 전송하려면 Adobe Experience Platform Experience Platform Launch 및 Adobe Campaign에서 모바일 애플리케이션을 설정해야 합니다. For the detailed steps to configure your mobile application using Experience Platform SDK, refer to this [page](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html).

아래 절차에 따라 구성을 시작하십시오.

1. **[!UICONTROL Mobile]** 채널에 액세스할 수 있는지 확인합니다. Adobe Campaign의 푸시 알림 및 인앱 메시지. 그렇지 않은 경우 계정 팀에 문의하십시오.

   ![](assets/launch_1.png)

1. 모바일 유형의 속성을 만들어 경험 플랫폼 Launch에서 모바일 애플리케이션을 제작할 수 있습니다. For more info, refer to the [Experience Platform Launch](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#create-a-new-mobile-property) documentation.
1. Install the **[!UICONTROL Adobe Campaign (Beta)]** extension for your mobile application in Experience Platform Launch:

   For more information on extensions, refer to the [Experience Platform Launch](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard-beta) documentation.

1. Configure rules for your application in Adobe Launch, see [Configuring your application in Launch](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html#ConfiguringyourapplicationinLaunch)
1. Configure your Adobe Launch application in Adobe Campaign Standard, see [Setting up your Adobe Launch application in Adobe Campaign](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html#SettingupyourAdobeLaunchapplicationinAdobeCampaign) .
1. Add channel specific configuration to your Mobile Application set-up, see [Channel-specific application configuration in Adobe Campaign](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html#ChannelspecificapplicationconfigurationinAdobeCampaign) .

   ![](assets/launch_2.png)

## Using SDK V4 {#using-sdk-v4}

푸시 알림은 인앱과 달리 SDK v 4 및 Adobe Experience Platform SDK에서 지원됩니다. For the detailed steps to use push notifications with your mobile app, refer to this [page](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html).

푸시 알림을 수신하는 모바일 애플리케이션은 Adobe Campaign 인터페이스에서 관리자가 구성해야 합니다. Adobe Campaign와 Adobe Mobile Services를 모두 구성하면 캠페인에 대한 모바일 애플리케이션의 데이터를 사용할 수 있습니다.

푸시 알림을 보내려면 다음을 수행해야 합니다.

1. Make sure you can access the **[!UICONTROL Mobile app]** channel in Adobe Campaign.
1. 모바일 애플리케이션 구성:

   * [Adobe Campaign](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html#SettingupamobileapplicationinAdobeCampaign).
   * [Adobe Mobile Services](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html#ConfiguringamobileapplicationinAdobeMobileServices).

1. 모바일 응용 프로그램의 특정 설정을 수행합니다.

   * Adobe Mobile Services 인터페이스에서 다운로드한 구성 파일을 모바일 응용 프로그램과 패키지화합니다.
   * 모바일 애플리케이션에 Experience Cloud Mobile SDK 통합

1. 애플리케이션 구독자로부터 수집할 데이터를 정의합니다. Adobe Campaign 데이터베이스에 프로필이 있는 모바일 응용 프로그램 구독자는 정의한 기준을 기반으로 조정됩니다.

   For more on this, refer to this [page](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html#Collectingsubscribersdatafromamobileapplication) .

1. 장치에서 모바일 애플리케이션을 실행하고 로그인하여 설정이 성공적으로 완료되었는지 확인합니다. 알림 수신을 선택해야 합니다.
1. Then, in Adobe Campaign's advanced menu, select **[!UICONTROL Administration]** &gt; **[!UICONTROL Channels]** &gt; **[!UICONTROL Mobile app]**.
1. 목록에서 모바일 애플리케이션을 선택하여 속성을 표시합니다. 구독 정보가 구독자 목록 아래에 표시됩니다.

   ![](assets/push_notif_mobile_app.png)

1. To check the mobile applications a profile has subscribed to, in the **[!UICONTROL Profiles & Audiences > Profiles]** menu, select a profile and click the **[!UICONTROL Edit profile properties]** button on the right. The mobile applications are listed in the **[!UICONTROL Mobile App Subscriptions]** tab.

   ![](assets/push_notif_subscriptions.png)
