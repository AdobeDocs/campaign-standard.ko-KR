---
title: 모바일 애플리케이션 구성
description: Experience Platform SDK를 사용하여 푸시 알림 또는 인앱 메시지를 보내도록 Adobe Campaign을 구성하는 방법에 대해 알아봅니다
audience: administration
feature: Instance Settings
role: Admin
level: Experienced
exl-id: 5f9a8e84-a362-42b6-8bd2-e5d56214c1db
source-git-commit: 58b07f023f52e2bf4972b4a86bf4412f613f38da
workflow-type: tm+mt
source-wordcount: '1307'
ht-degree: 2%

---

# 모바일 애플리케이션 구성{#configuring-a-mobile-application}

## Adobe Experience Platform SDK를 사용하여 모바일 애플리케이션 구성 {#using-adobe-experience-platform-sdk}

>[!IMPORTANT]
>
> Adobe Experience Platform Launch은 Adobe Experience Platform의 데이터 수집 기술군으로 새롭게 브랜딩되었습니다. 그 결과 제품 설명서에 몇 가지 용어 변경 사항이 적용되었습니다. 용어 변경에 대한 통합 참고 자료는 [다음 문서](https://experienceleague.adobe.com/docs/experience-platform/tags/term-updates.html?lang=ko){target="_blank"}를 참조하십시오.

푸시 알림 및 인앱 구현은 전문가 사용자가 수행해야 합니다. 도움이 필요하면 Adobe 계정 담당자 또는 전문 서비스 파트너에게 문의하십시오.

Experience Platform SDK 애플리케이션을 사용하여 푸시 알림 및 인앱 메시지를 전송하려면 모바일 애플리케이션을 데이터 수집 UI에서 설정하고 Adobe Campaign에서 구성해야 합니다.

모바일 애플리케이션이 설정되면 수집한 PII 데이터를 검색하여 데이터베이스에서 프로필을 만들거나 업데이트할 수 있습니다. 자세한 내용은 다음 섹션을 참조하십시오. [모바일 응용 프로그램 데이터를 기반으로 프로필 정보 만들기 및 업데이트](../../channels/using/updating-profile-with-mobile-app-data.md).

Adobe Experience Platform SDK를 사용하여 Adobe Campaign Standard에서 지원되는 다양한 모바일 사용 사례에 대한 자세한 내용은 이 [페이지](../../administration/using/supported-mobile-use-cases.md)를 참조하세요.

구성을 완료하려면 다음 단계를 완료하십시오.

1. Adobe Campaign에서 다음에 액세스할 수 있는지 확인합니다.
   * **[!UICONTROL Push notification]**
   * **[!UICONTROL In-App message]**
   * **[!UICONTROL Adobe Places]**

   그렇지 않은 경우 계정 팀에 문의하십시오.

1. 사용자에게 Adobe Campaign Standard에 필요한 권한이 있는지, Adobe Experience Platform에 있는 태그가 있는지 확인합니다.

   * Adobe Campaign Standard에서 IMS 사용자가 표준 사용자 및 관리자 제품 프로필의 일부인지 확인합니다. 이 단계에서는 사용자가 Adobe Campaign Standard에 로그인하고, Experience Platform SDK 모바일 앱 페이지로 이동하고, 데이터 수집 UI에서 만든 모바일 앱 속성을 볼 수 있습니다.

   * 데이터 수집 UI에서 IMS 사용자가 Experience Platform Launch 제품 프로필의 일부인지 확인합니다.
이 단계에서는 사용자가 데이터 수집 UI에 로그인하여 속성을 만들고 볼 수 있습니다. 데이터 수집 UI의 제품 프로필에 대한 자세한 내용은 [제품 프로필 만들기](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/manage-permissions.html?lang=ko#gain-admin-rights-for-a-tags-product-profile)를 참조하십시오. 제품 프로필에 회사 또는 속성에 대해 설정된 권한이 없어야 하지만 사용자는 계속 로그인할 수 있어야 합니다.

   확장 설치, 앱 게시, 환경 구성 등과 같은 추가 작업을 완료하려면 제품 프로필에서 권한을 설정해야 합니다.

1. 데이터 수집 UI에서 **[!UICONTROL Mobile property]**&#x200B;을(를) 만듭니다. 자세한 내용은 [모바일 속성 설정](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property)을 참조하십시오.

1. 데이터 수집 UI에서 **[!UICONTROL Extensions]** 탭을 클릭하고 **[!UICONTROL Catalog]**(으)로 이동한 다음 **[!UICONTROL Adobe Campaign Standard]** 확장을 검색합니다. 자세한 내용은 [Adobe Campaign Standard](https://developer.adobe.com/client-sdks/documentation/adobe-campaign-standard)을 참조하세요.

1. Campaign Standard에서 위치 사용 사례를 지원하려면 데이터 수집 UI에 **[!UICONTROL Places]** 확장을 설치하십시오. 이 [페이지](https://developer.adobe.com/client-sdks/solution/places)를 참조하세요.

1. Adobe Campaign Standard에서 데이터 수집 UI에서 만든 모바일 속성을 구성합니다. [Adobe Campaign에서 Adobe Experience Platform Launch 애플리케이션 설정](../../administration/using/configuring-a-mobile-application.md#set-up-campaign)을 참조하세요.

1. 모바일 애플리케이션 설정에 채널별 구성을 추가합니다.
자세한 내용은 [Adobe Campaign의 채널별 애플리케이션 구성](../../administration/using/configuring-a-mobile-application.md#channel-specific-config)을 참조하십시오.

1. 필요한 경우 태그 속성을 삭제할 수 있습니다.
자세한 내용은 [응용 프로그램 삭제](../../administration/using/configuring-a-mobile-application.md#delete-app)를 참조하세요.

## Launch 기술 워크플로우에서 모바일 앱 AEPSDK 동기화 {#aepsdk-workflow}

이제 데이터 수집 UI에서 모바일 속성을 만들고 구성한 후 **[!UICONTROL Sync Mobile app AEPSDK from Launch]** 기술 워크플로는 Adobe Campaign Standard에서 가져온 태그 모바일 속성을 동기화합니다.

기본적으로 기술 워크플로우는 15분마다 시작됩니다. 필요한 경우 수동으로 다시 시작할 수 있습니다.

1. Adobe Campaign Standard의 고급 메뉴에서 **[!UICONTROL Administration]** > **[!UICONTROL Application Settings]** > **[!UICONTROL Workflows]**&#x200B;을(를) 선택합니다.
1. **[!UICONTROL Sync Mobile app AEPSDK from Launch (syncWithLaunch)]** 워크플로를 엽니다.

   ![](assets/launch_10.png)

1. **[!UICONTROL Scheduler]** 활동을 클릭합니다.

1. **[!UICONTROL Immediate execution]**&#x200B;을(를) 선택합니다.

   ![](assets/launch_11.png)

이제 워크플로우가 다시 시작되고 Adobe Campaign Standard에서 가져온 태그 모바일 속성을 동기화합니다.

## Adobe Campaign에서 애플리케이션 설정 {#set-up-campaign}

Campaign에서 태그 모바일 속성을 사용하려면 Adobe Campaign에서도 이 속성을 구성해야 합니다. Adobe Campaign에서 IMS 사용자가 표준 사용자 및 관리자 제품 프로필의 일부인지 확인합니다.

기술 워크플로우가 실행되고 태그 모바일 속성이 Adobe Campaign에 동기화될 때까지 기다려야 합니다. 그런 다음 Adobe Campaign에서 구성할 수 있습니다.

Launch 기술 워크플로우에서 모바일 앱 AEPSDK를 동기화하는 방법에 대한 자세한 내용은 이 [섹션](../../administration/using/configuring-a-mobile-application.md#aepsdk-workflow)을 참조하세요.

>[!NOTE]
>
>기본적으로 조직 단위가 ALL로 설정된 관리자는 모바일 애플리케이션을 편집할 수 있습니다.

1. 고급 메뉴에서 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile app (AEP SDK)]**&#x200B;을(를) 선택합니다.

   ![](assets/launch.png)

1. 데이터 수집 UI에서 생성한 모바일 애플리케이션을 선택합니다.
해당 **[!UICONTROL Property Status]**&#x200B;은(는) **[!UICONTROL Ready to configure]**&#x200B;이어야 합니다.

   >[!NOTE]
   >
   >기본적으로 데이터 수집 UI에서 생성된 모바일 애플리케이션 목록을 검색하려면 Campaign Standard은 NmsServer_URL 옵션에 정의된 값을 사용하여 일치하는 속성을 찾습니다.
   >
   >경우에 따라 모바일 애플리케이션에 대한 Campaign 엔드포인트는 NmsServer_URL에 정의된 엔드포인트와 다를 수 있습니다. 이 경우 `Launch_URL_Campaign` 옵션에서 끝점을 정의합니다. Campaign은 이 옵션의 값을 사용하여 데이터 수집 UI에서 일치하는 속성을 찾습니다.

   ![](assets/launch_4.png)

1. **[!UICONTROL Access Authorization]** 섹션에서 모바일 응용 프로그램의 조직 단위를 변경하여 이 모바일 응용 프로그램에 대한 액세스를 특정 조직 단위로 제한할 수 있습니다. 자세한 정보는 이 페이지 를 참조하십시오.

   여기에서 관리자는 드롭다운에서 하위 조직 단위를 선택하여 하위 조직 단위를 할당할 수 있습니다.

   ![](assets/launch_12.png)

1. Adobe Experience Platform의 태그와 Campaign을 연결하려면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

1. 모바일 앱의 상태가 **[!UICONTROL Ready to Configure]**&#x200B;에서 **[!UICONTROL Configured]**(으)로 변경되었는지 확인하십시오.

   Campaign 확장에 pkey가 성공적으로 설정되었다고 표시되면 Campaign에서 속성이 성공적으로 설정되었는지 확인할 수도 있습니다.

   ![](assets/launch_5.png)

1. 이 구성을 적용하려면 변경 사항을 데이터 수집 UI에 게시해야 합니다.

   자세한 내용은 [Publish 구성](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/#publish-the-configuration)을 참조하세요.

## Adobe Campaign의 채널별 애플리케이션 구성 {#channel-specific-config}

이제 모바일 애플리케이션을 Campaign에서 푸시 알림 또는 인앱 게재를 위해 사용할 준비가 되었습니다. 이제 필요한 경우 인앱 메시지를 트리거하는 이벤트를 만들거나 푸시 인증서를 업로드하도록 추가로 구성할 수 있습니다.

1. 고급 메뉴에서 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile app (AEP SDK)]**&#x200B;을(를) 선택합니다.

1. 데이터 수집 UI에서 만들고 구성한 모바일 애플리케이션을 선택합니다.

1. **[!UICONTROL Mobile application properties]** 탭에서 모바일 응용 프로그램에서 인앱 메시지에 사용할 수 있는 이벤트를 추가할 수 있습니다.

1. 이벤트를 구성하려면 **[!UICONTROL Create Element]**&#x200B;을(를) 클릭합니다.

   ![](assets/launch_6.png)

1. 이름과 설명을 입력합니다.

   ![](assets/launch_7.png)

1. **[!UICONTROL Add]**&#x200B;를 클릭합니다.

   이제 인앱 메시지를 만들 때 트리거 탭에서 이벤트를 사용할 수 있습니다. 자세한 내용은 [인앱 메시지 준비 및 보내기](../../channels/using/preparing-and-sending-an-in-app-message.md)를 참조하십시오.

1. 모바일 응용 프로그램 대시보드의 **[!UICONTROL Device-specific settings]** 섹션에서 각 장치에 대해 응용 프로그램 세부 정보를 제공합니다.

   +++*  iOS용

     다음 애플리케이션 세부 정보를 입력합니다.

      * **앱 ID(iOS 번들 ID)**: 번들 ID에 대한 자세한 내용은 [Apple 설명서](https://developer.apple.com/documentation/appstoreconnectapi/bundle_ids){target="_blank"}를 참조하세요.
      * **iOS 인증서(P8) 파일**: .p8 인증 키를 끌어서 놓습니다. .p8 인증 파일을 생성하는 방법에 대한 지침은 [Apple 개발자 계정](https://developer.apple.com/account/ios/authkey/create){target="_blank"}을 참조하세요.
      * **키 ID**: 키 ID에 대한 자세한 내용은 [Apple 설명서](https://developer.apple.com/help/account/manage-keys/get-a-key-identifier/){target="_blank"}를 참조하세요.
      * **iOS 팀 ID**: iOS 팀 ID에 대한 자세한 내용은 [Apple 설명서](https://developer.apple.com/help/account/manage-your-team/locate-your-team-id/){target="_blank"}를 참조하십시오.

        ![](assets/mobile_app_ios_config.png)
   +++

   +++*  Android용

     다음 애플리케이션 세부 정보를 입력합니다.

      * **앱 ID(Android 패키지 이름)**: 패키지 이름에 대한 자세한 내용은 [Android 설명서](https://support.google.com/admob/answer/9972781?hl=en#:~:text=The%20package%20name%20of%20an,supported%20third%2Dparty%20Android%20stores){target="_blank"}를 참조하십시오.
      * **Android 키(Json) 파일**: .json 개인 키 파일을 끌어서 놓습니다. .json 개인 키 파일을 생성하는 방법에 대한 지침은 [Firebase용 개발자 설명서](https://firebase.google.com/docs/admin/setup#initialize_the_sdk_in_non-google_environments){target="_blank"}를 참조하십시오.

        ![](assets/mobile_app_android_config.png)
   +++

1. 인증서가 업로드되면 업로드가 성공했음을 알리고 인증서의 만료 날짜를 표시하는 메시지가 표시됩니다.

1. 구독자 목록과 이러한 구독자에 대한 다른 정보(예: 알림에서 옵트아웃했는지 여부)를 보려면 **[!UICONTROL Mobile application subscribers]** 탭을 클릭하십시오.

## 애플리케이션 삭제 중 {#delete-app}

>[!CAUTION]
>
>응용 프로그램을 삭제하면 되돌릴 수 없습니다.

응용 프로그램을 삭제하려면 [모바일 속성 삭제](https://developer.adobe.com/client-sdks/documentation/adobe-campaign-standard/#deleting-mobile-properties-in-the-data-collection-ui)의 단계를 완료하십시오.

애플리케이션이 삭제되면 Adobe Campaign에서 애플리케이션의 속성 상태가 Launch에서 삭제됨으로 올바르게 업데이트되었는지 확인합니다.

Adobe Campaign에서 애플리케이션을 클릭하면 Campaign에서 삭제 를 클릭하여 Adobe Campaign에서 이 애플리케이션을 완전히 제거하도록 선택할 수 있습니다.

![](assets/launch_9.png)
