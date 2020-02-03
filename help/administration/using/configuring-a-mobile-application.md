---
title: 모바일 애플리케이션 구성
description: SDK V4 또는 Experience Platform SDK 파섹
page-status-flag: never-activated
uuid: 63e1476a-7875-4f48-ba9e-97f1a0007e42
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: configuring-channels
discoiquuid: 2a14500f-5ede-4131-8b1a-b7fd65b7e3aa
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: aa1539a1fc5fd08e7cf4e081ae2517e39ddde121

---


# 모바일 애플리케이션 구성{#configuring-a-mobile-application}

푸시 알림 또는 인앱 메시지는 사용하려는 채널에 따라 먼저 Adobe Campaign Standard에서 구성해야 하는 모바일 애플리케이션에서 수신됩니다.

인앱 메시지와 푸시 알림을 전송하려면 Adobe Experience Platform SDK를 활용하여 모바일 애플리케이션을 Adobe Campaign에서 설정해야 합니다. Adobe [Experience Platform SDK 사용을 참조하십시오](#using-adobe-experience-platform-sdk).

모바일 애플리케이션이 Experience Cloud Mobile SDK V4 또는 Experience Platform SDK를 활용하여 Adobe Campaign에서 설정되면, 관리자가 [!UICONTROL Administration] > [!UICONTROL Channels] > [!UICONTROL Mobile app] 메뉴에서 이를 구성해야 합니다.

>[!CAUTION]
>
>푸시 알림 및 인앱 구현은 전문가 사용자가 수행해야 합니다. 도움이 필요한 경우 Adobe 계정 담당자 또는 Professional 서비스 파트너에게 문의하십시오.

모바일 애플리케이션이 설정되면 수집한 PII 데이터를 검색하여 데이터베이스에서 프로파일을 만들거나 업데이트할 수 있습니다. 자세한 내용은 다음 섹션을 참조하십시오.모바일 [애플리케이션 데이터를](../../channels/using/updating-profile-with-mobile-app-data.md)기반으로 프로파일 정보 생성 및 업데이트

Adobe Campaign Standard의 모바일 게재에 대한 일반적인 지침은 이 [페이지를 참조하십시오](https://helpx.adobe.com/campaign/kb/acs-mobile.html)

## Adobe Experience Platform SDK 사용 {#using-adobe-experience-platform-sdk}

>[!Note]
>
>Adobe Experience Platform SDK를 사용하여 Adobe Campaign Standard에서 지원되는 다양한 모바일 사용 사례에 대한 자세한 내용은 이 [페이지를](https://helpx.adobe.com/campaign/kb/configure-launch-rules-acs-use-cases.html)참조하십시오.

Experience Platform SDK 애플리케이션을 사용하여 푸시 알림 및 인앱 메시지를 전송하려면 Adobe Experience Platform Experience Platform Experience Platform Platform Launch에서 모바일 애플리케이션을 설정하고 Adobe Campaign에 구성해야 합니다. Experience Platform SDK를 사용하여 모바일 애플리케이션을 구성하는 자세한 단계는 이 [페이지를](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html)참조하십시오.

아래 절차에 따라 구성을 시작합니다.

1. 다음 **[!UICONTROL Mobile]**채널에 액세스할 수 있는지 확인합니다.Adobe Campaign의 푸시 알림 및 인앱 메시지 그렇지 않은 경우 계정 팀에 문의하십시오.

   ![](assets/launch_1.png)

1. 모바일 유형의 속성을 만들어 Experience Platform Launch에서 모바일 애플리케이션을 만듭니다. 자세한 내용은 Experience Platform [Launch 설명서를](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#create-a-new-mobile-property) 참조하십시오.
1. Experience Platform Launch에서 모바일 애플리케이션용 **[!UICONTROL Adobe Campaign Standard]**익스텐션을 설치합니다.

   익스텐션에 대한 자세한 내용은 Experience Platform [Launch 설명서를](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard) 참조하십시오.

1. Adobe Launch에서 응용 프로그램에 대한 규칙을 구성합니다. 론치에서 [응용 프로그램 구성을 참조하십시오.](https://helpx.adobe.com/campaign/kb/config-app-in-launch.html#Step1Createdataelements)
1. Adobe Campaign Standard에서 Adobe Launch 애플리케이션을 구성합니다. Adobe [Campaign에서 Adobe Launch 애플리케이션 설정을 참조하십시오](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html#SettingupyourAdobeLaunchapplicationinAdobeCampaign).
1. 모바일 애플리케이션 설정에 채널별 구성을 추가합니다. Adobe Campaign [의 채널별 애플리케이션 구성을 참조하십시오](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html#ChannelspecificapplicationconfigurationinAdobeCampaign).

   ![](assets/launch_2.png)
