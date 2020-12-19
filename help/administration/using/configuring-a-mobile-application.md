---
solution: Campaign Standard
product: campaign
title: 모바일 애플리케이션 구성
description: SDK V4 또는 Experience Platform SDK를 사용하여 푸시 알림 또는 인앱 메시지를 전송하도록 Adobe Campaign을 구성하는 방법을 살펴볼 수 있습니다.
audience: administration
content-type: reference
topic-tags: configuring-channels
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '1283'
ht-degree: 7%

---


# 모바일 애플리케이션 구성{#configuring-a-mobile-application}

## Adobe Experience Platform SDK {#using-adobe-experience-platform-sdk}를 사용하여 모바일 응용 프로그램 구성

>[!IMPORTANT]
>
>푸시 알림 및 인앱 구현은 전문가 사용자가 수행해야 합니다. 도움이 필요한 경우 Adobe 계정 담당자 또는 전문 서비스 파트너에게 문의하십시오.

Experience Platform SDK 응용 프로그램을 사용하여 푸시 알림 및 인앱 메시지를 전송하려면 모바일 응용 프로그램을 Adobe Experience Platform Experience Platform Experience Platform Launch에서 설정하고 Adobe Campaign에 구성해야 합니다.

더 이상 사용되지 않는 기능 Mobile 버전 4 SDK에 대한 자세한 내용은 이 [페이지](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4-deprecated.html)를 참조하십시오.

모바일 응용 프로그램이 설정되면 수집한 PII 데이터를 검색하여 데이터베이스에서 프로파일을 만들거나 업데이트할 수 있습니다. 자세한 내용은 다음 섹션을 참조하십시오.[모바일 응용 프로그램 데이터](../../channels/using/updating-profile-with-mobile-app-data.md)에 따라 프로필 정보를 만들고 업데이트합니다.

Adobe Experience Platform SDK를 사용하여 Adobe Campaign Standard에서 지원되는 다양한 모바일 사용 사례에 대한 자세한 내용은 이 [페이지](https://helpx.adobe.com/kr/campaign/kb/configure-launch-rules-acs-use-cases.html)를 참조하십시오.

구성을 완료하려면 다음 단계를 완료하십시오.

1. Adobe Campaign에서 다음 항목에 액세스할 수 있는지 확인합니다.
   * **[!UICONTROL Push notification]**
   * **[!UICONTROL In-App message]**
   * **[!UICONTROL Adobe Places]**

   없는 경우 계정 팀에 문의하십시오.

1. Adobe Campaign Standard 및 Experience Platform Launch에서 필요한 권한이 있는지 확인합니다.
   * Adobe Campaign Standard에서 IMS 사용자가 표준 사용자 및 관리자 제품 프로필의 일부인지 확인하십시오. 이 단계에서는 사용자가 Adobe Campaign Standard에 로그인하고 Experience Platform SDK 모바일 앱 페이지로 이동하여 Experience Platform Launch에서 만든 모바일 앱 속성을 볼 수 있습니다.

   * Experience Platform Launch에서 IMS 사용자가 Experience Platform Launch 제품 프로필에 포함되어 있는지 확인합니다.
이 단계에서는 사용자가 Experience Platform Launch에 로그인하여 속성을 만들고 볼 수 있습니다. Experience Platform Launch의 제품 프로필에 대한 자세한 내용은 제품 프로필 만들기를 참조하십시오. 제품 프로필에는 회사 또는 속성에 설정된 권한이 없지만 사용자는 계속 로그인할 수 있어야 합니다.

   확장 설치, 앱 게시, 환경 구성 등과 같은 추가 작업을 완료하려면 제품 프로필에서 권한을 설정해야 합니다.

1. Experience Platform Launch에서 **[!UICONTROL Mobile property]**&#x200B;을(를) 만듭니다. 자세한 내용은 [모바일 속성 설정](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property)을 참조하십시오.

1. Experience Platform Launch에서 **[!UICONTROL Extensions]** 탭을 클릭하고 **[!UICONTROL Catalog]**&#x200B;로 이동한 다음 **[!UICONTROL Adobe Campaign Standard]** 확장을 검색합니다. 자세한 내용은 [Adobe Campaign Standard](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard)을 참조하십시오.

1. Campaign Standard에서 위치 사용 사례를 지원하려면 **[!UICONTROL Places]** 확장 및 **[!UICONTROL Places Monitor]** 확장을 설치합니다.
   * Experience Platform Launch에 **[!UICONTROL Places]** 확장을 설치합니다. 이 [페이지](https://docs.adobe.com/content/help/ko-KR/places/using/places-ext-aep-sdks/places-extension/places-extension.html)를 참조하십시오.
   * Experience Platform Launch에 **[!UICONTROL Places Monitor]** 확장을 설치합니다. 이 [페이지](https://docs.adobe.com/content/help/en/places/using/places-ext-aep-sdks/places-monitor-extension/using-places-monitor-extension.html)를 참조하십시오.

1. Adobe Campaign Standard에서 Experience Platform Launch에서 만든 모바일 속성을 구성합니다. Adobe Campaign[에서 Adobe Experience Platform Launch 응용 프로그램 설정을 참조하십시오.](../../administration/using/configuring-a-mobile-application.md#set-up-campaign)

1. 모바일 애플리케이션 설정에 채널별 구성을 추가합니다.
자세한 내용은 [Adobe Campaign의 채널별 애플리케이션 구성](../../administration/using/configuring-a-mobile-application.md#channel-specific-config)을 참조하십시오.

1. 필요한 경우 Experience Platform Launch 속성을 삭제할 수 있습니다.
자세한 내용은 [Experience Platform Launch 응용 프로그램 삭제](../../administration/using/configuring-a-mobile-application.md#delete-app)를 참조하십시오.

## Launch 기술 워크플로우에서 모바일 앱 AEPSDK 동기화 {#aepsdk-workflow}

Experience Platform Launch에서 모바일 속성을 만들고 구성한 후 이제 **[!UICONTROL Sync Mobile app AEPSDK from Launch]** 기술 워크플로우가 Adobe Campaign Standard에 가져온 Adobe Launch 모바일 속성을 동기화합니다.

기본적으로 기술 워크플로우는 15분마다 시작됩니다. 필요한 경우 수동으로 다시 시작할 수 있습니다.

1. Adobe Campaign Standard의 고급 메뉴에서 **[!UICONTROL Administration]** > **[!UICONTROL Application Settings]** > **[!UICONTROL Workflows]**&#x200B;를 선택합니다.
1. **[!UICONTROL Sync Mobile app AEPSDK from Launch (syncWithLaunch)]** 작업 과정을 엽니다.

   ![](assets/launch_10.png)

1. **[!UICONTROL Scheduler]** 활동을 클릭합니다.

1. **[!UICONTROL Immediate execution]**&#x200B;을(를) 선택합니다.

   ![](assets/launch_11.png)

이제 워크플로우가 다시 시작되고 Adobe Campaign Standard에 가져온 Adobe Launch 모바일 속성을 동기화합니다.

## Adobe Campaign {#set-up-campaign}에서 Adobe Experience Platform Launch 응용 프로그램 설정

Campaign에서 Experience Platform Launch 모바일 속성을 사용하려면 Adobe Campaign에서 이 속성을 구성해야 합니다. Adobe Campaign에서 IMS 사용자가 표준 사용자 및 관리자 제품 프로필의 일부인지 확인하십시오.

Launch 모바일 속성을 Adobe Campaign에 실행하고 동기화할 때까지 기술 워크플로우를 기다려야 합니다. 그런 다음 Adobe Campaign에서 구성할 수 있습니다.

Launch 기술 워크플로우에서 모바일 앱 AEPSDK 동기화에 대한 자세한 내용은 이 [섹션](../../administration/using/configuring-a-mobile-application.md#aepsdk-workflow)을 참조하십시오.

>[!NOTE]
>
>기본적으로 조직 구성 단위를 ALL로 설정한 관리자는 모바일 애플리케이션을 편집할 수 있습니다.

1. 고급 메뉴에서 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile app (AEP SDK)]**&#x200B;를 선택합니다.

   ![](assets/launch.png)

1. Experience Platform Launch에서 만든 모바일 응용 프로그램을 선택합니다.
**[!UICONTROL Property Status]**&#x200B;은(는) **[!UICONTROL Ready to configure]**&#x200B;이어야 합니다.

   >[!NOTE]
   >
   >기본적으로 Adobe Launch에서 만든 모바일 응용 프로그램 목록을 검색하려면 Campaign Standard은 NmsServer_URL 옵션에 정의된 값을 사용하여 일치하는 속성을 찾습니다.
   >
   >경우에 따라 모바일 응용 프로그램에 대한 캠페인 끝점이 NmsServer_URL에 정의된 것과 다를 수 있습니다. 이 경우 Launch_URL_Campaign 옵션에서 끝점을 정의합니다. 캠페인은 Adobe 론치에서 일치하는 속성을 찾기 위해 이 옵션의 값을 사용합니다.

   ![](assets/launch_4.png)

1. **[!UICONTROL Access Authorization]** 섹션 아래에 있는 모바일 애플리케이션의 조직 단위를 변경하여 이 모바일 애플리케이션에 대한 액세스를 특정 조직 단위로 제한할 수 있습니다. 자세한 정보는 이 페이지를 참조하십시오.

   여기에서 관리자는 드롭다운에서 하위 조직 단위를 선택하여 할당할 수 있습니다.

   ![](assets/launch_12.png)

1. 캠페인과 Experience Platform Launch 간의 연결을 만들려면 **[!UICONTROL Save]**&#x200B;을 클릭합니다.

1. 모바일 앱의 상태가 **[!UICONTROL Ready to Configure]**&#x200B;에서 **[!UICONTROL Configured]**(으)로 변경되었는지 확인합니다.

   Experience Platform Launch 캠페인 확장 프로그램에서 키가 성공적으로 설정되었다고 표시되면 속성이 Campaign에서 성공적으로 설정되었는지 확인할 수도 있습니다.

   ![](assets/launch_5.png)

1. 이 구성을 적용하려면 변경 사항을 Experience Platform Launch에 게시해야 합니다.

   자세한 내용은 [게시 구성](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#publish-configuration)을 참조하십시오.

## Adobe Campaign {#channel-specific-config}의 채널별 응용 프로그램 구성

이제 모바일 응용 프로그램이 푸시 알림 또는 인앱 전달을 위해 Campaign에서 사용할 준비가 되었습니다. 이제 인앱 메시지를 트리거하는 이벤트를 만들고 푸시 인증서를 업로드하는 데 필요한 경우 추가로 구성할 수 있습니다.

1. 고급 메뉴에서 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile app (AEP SDK)]**&#x200B;를 선택합니다.

1. Experience Platform Launch에서 만들고 구성한 모바일 응용 프로그램을 선택합니다.

1. **[!UICONTROL Mobile application properties]** 탭에서 인앱 메시지에 대해 모바일 응용 프로그램에서 사용할 수 있는 이벤트를 추가할 수 있습니다.

1. 이벤트를 구성하려면 **[!UICONTROL Create Element]**&#x200B;을 클릭합니다.

   ![](assets/launch_6.png)

1. 이름과 설명을 입력합니다.

   ![](assets/launch_7.png)

1. **[!UICONTROL Add]**&#x200B;을(를) 클릭합니다.

   이제 인앱 메시지를 만들 때 트리거 탭에서 이벤트를 사용할 수 있습니다. 자세한 내용은 [인앱 메시지 준비 및 보내기](../../channels/using/preparing-and-sending-an-in-app-message.md)를 참조하십시오.

1. 모바일 응용 프로그램 대시보드의 **[!UICONTROL Device-specific settings]** 섹션에서 각 장치에 대해 iOS용 인증서 및 Android용 서버 키를 비롯한 응용 프로그램 세부 정보를 제공합니다.

   인증서가 업로드되면 업로드가 성공했음을 알리는 메시지가 표시되고 인증서의 만료 날짜가 표시됩니다.

   >[!NOTE]
   >
   >Adobe Campaign Standard에서 인증서를 성공적으로 추가한 후에는 하나의 APNS 플랫폼(프로덕션 또는 샌드박스)만 MCPNS 앱에 추가할 수 있으므로 설정을 다시 변경할 수 없게 됩니다.

   ![](assets/launch_8.png)

1. **[!UICONTROL Mobile application subscribers]** 탭을 클릭하여 구독자 목록과 이들 구독자에 대한 기타 정보(예: 사용자가 알림 대상에서 제외했는지 여부)를 확인합니다.

## Adobe Experience Platform Launch 응용 프로그램 {#delete-app} 삭제

Experience Platform Launch 응용 프로그램 삭제는 되돌릴 수 없습니다.

>[!CAUTION]
>
>Experience Platform Launch 응용 프로그램 삭제는 되돌릴 수 없습니다.

Experience Platform Launch 응용 프로그램을 삭제하려면 [모바일 속성 삭제](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard#deleting-mobile-properties-in-experience-platform-launch)의 단계를 완료하십시오.

애플리케이션이 삭제된 후 Adobe Campaign에서 애플리케이션의 속성 상태가 론치에서 삭제됨으로 올바르게 업데이트되었는지 확인합니다.

Adobe Campaign에서 애플리케이션을 클릭하면 캠페인에서 삭제를 클릭하여 Adobe Campaign에서 이 애플리케이션을 완전히 제거하도록 선택할 수 있습니다.

![](assets/launch_9.png)
