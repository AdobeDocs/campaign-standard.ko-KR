---
title: Campaign-Points of Interest 데이터 통합 구성
description: Adobe Campaign의 관심 영역 데이터 기능을 구성하여 사용자의 위치를 기반으로 개인화된 메시지를 전송하는 방법을 살펴볼 수 있습니다.
page-status-flag: never-activated
uuid: 0689a06c-cc1a-442f-95b8-a07fcec85d79
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-analytics-for-mobile
discoiquuid: a967c6cc-c53b-41b4-866b-90860d78f463
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '1340'
ht-degree: 3%

---


# Campaign-Points of Interest 데이터 통합 구성{#configuring-campaign-points-of-interest-data-integration}

## Adobe Experience Platform SDK와 캠페인 관심 영역 데이터 통합 구성 {#configuring-campaign-poi-aep-sdk}

>[!NOTE]
>
>모바일 애플리케이션은 Adobe Experience Platform SDK를 사용하여 Adobe Campaign Standard에서 이미 구성되어야 합니다. For the detailed steps, refer to this [page](https://helpx.adobe.com/kr/campaign/kb/configuring-app-sdk.html).

위치 데이터를 수집하는 데 사용되는 모바일 응용 프로그램은 **관리자가** Adobe Campaign 인터페이스에서 구성해야 합니다.

Adobe Experience Platform SDK로 구성된 모바일 애플리케이션에서 Adobe Experience Platform 위치 서비스를 사용할 수 있으려면 다음을 수행해야 합니다.

1. Adobe Experience Platform Launch에서 모바일 앱 구성에 **[!UICONTROL Places]** 및 **[!UICONTROL Places Monitor]** 확장 기능을 추가합니다. Adobe Campaign에서 모바일 애플리케이션 설정 Adobe Experience Platform Launch [에서 위치 확장](https://docs.adobe.com/content/help/en/places/using/places-ext-aep-sdks/places-extension/places-extension.html#install-the-places-extension-in-adobe-experience-platform-launch) 설치 및 Experience Platform Launch [에서 위치 모니터 확장 설치](https://docs.adobe.com/content/help/en/places/using/places-ext-aep-sdks/places-monitor-extension/using-places-monitor-extension.html#install-the-places-monitor-extension-in-experience-platform-launch)를 참조하십시오.

1. 익스텐션이 설정되면 해당 익스텐션에서 데이터 요소 **[!UICONTROL Adobe Experience Platform Launch]** 를 만들어 데이터를 검색할 수 있습니다. 데이터 요소를 만들려면 이 [페이지를](https://helpx.adobe.com/campaign/kb/config-app-in-launch.html#Step1Createdataelements) 참조하십시오.

1. 그런 다음 관심 영역 **[!UICONTROL Adobe Experience Platform Launch]**&#x200B;과 Adobe Campaign 간에 모바일 사용 사례를 지원하는 규칙을 만들어야 합니다.\
   이 규칙은 사용자가 지리적 울타리로 들어갈 때 트리거됩니다 **[!UICONTROL Point of Interest]**. 규칙을 만들려면 이 [페이지를](https://helpx.adobe.com/campaign/kb/config-app-in-launch.html#Locationpostback) 참조하십시오.

1. 장소 **[!UICONTROL Points of Interest]** 에서 사용자 정의 관심 [영역 만들기를 참조하십시오](https://docs.adobe.com/content/help/en/places/using/poi-mgmt-ui/create-a-poi-ui.html).

1. Adobe Campaign에서 모바일 응용 프로그램과 수집된 위치 데이터에 액세스해야 합니다. 위치 데이터 [를 수집하는 데 사용되는 모바일 앱](#accessing-mobile-apps-used-to-collect-location-data) 액세스 및 [수집된 위치 데이터 액세스를 참조하십시오](#accessing-collected-location-data).

## SDK V4를 사용하여 캠페인 관심 영역 데이터 통합 구성 {#configuring-campaign-poi-sdkv4}

위치 데이터를 수집하는 데 사용되는 모바일 응용 프로그램은 **관리자가** Adobe Campaign 인터페이스에서 구성해야 합니다.

SDK V4로 구성된 모바일 애플리케이션에서 관심 영역 데이터 기능을 사용하려면 다음을 수행해야 합니다.

1. 모바일용 Adobe Analytics 이용 자세한 내용은 라이선스 계약서를 확인하거나 Adobe 계정 관리자에게 문의하십시오.
1. Adobe Campaign에서 모바일 애플리케이션 설정 Campaign [에서 모바일 앱 설정을 참조하십시오](#setting-up-a-mobile-app-in-campaign).
1. Adobe Mobile Services 인터페이스에서 모바일 애플리케이션을 설정합니다. Adobe Mobile Services에서 수집한 데이터가 Adobe Campaign으로 전송되도록 할 수 있습니다. Adobe [Mobile Services에서 모바일 앱 구성을 참조하십시오](#configuring-a-mobile-app-in-adobe-mobile-services).
1. 모바일 응용 프로그램의 특정 설정을 수행합니다.

   * Adobe Mobile Services 인터페이스에서 다운로드한 구성 파일을 모바일 응용 프로그램과 함께 패키징합니다.
   * Experience Cloud Mobile SDK를 모바일 애플리케이션에 통합합니다. 모바일 [애플리케이션에 SDK 통합을 참조하십시오](#integrating-the-sdk-into-a-mobile-application).

1. Adobe Mobile Services 인터페이스에서 관심 영역을 정의합니다. Adobe [Mobile Services의 관심 영역 정의를 참조하십시오](#defining-points-of-interest-in-adobe-mobile-services).
1. 모바일 애플리케이션의 가입자로부터 수집할 데이터를 정의합니다. 가입자 [관심 영역 데이터 수집을 참조하십시오](#collecting-subscribers--points-of-interest-data).
1. Adobe Campaign에서 모바일 응용 프로그램과 수집된 위치 데이터에 액세스해야 합니다. 위치 데이터 [를 수집하는 데 사용되는 모바일 앱](#accessing-mobile-apps-used-to-collect-location-data) 액세스 및 [수집된 위치 데이터 액세스를 참조하십시오](#accessing-collected-location-data).

### SDK V4를 사용하여 Adobe Campaign에서 모바일 앱 설정 {#setting-up-a-mobile-app-in-campaign}

Adobe Campaign에서 관심 영역 데이터를 수집할 수 있으려면, Adobe Campaign에서 데이터를 받을 모바일 애플리케이션을 구성해야 합니다.

1. 왼쪽 상단 모서리에서 **[!UICONTROL Adobe Campaign]** 로고를 클릭한 다음 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile app]**&#x200B;을(를) 선택합니다.
1. 애플리케이션 **[!UICONTROL Create]** 을 설정하려면 을 클릭합니다.
1. 필드에 이름을 **[!UICONTROL Application name]** 입력하고 을 클릭합니다 **[!UICONTROL Create]**.

   섹션을 채우지 **[!UICONTROL Device-specific settings]** 마십시오. 푸시 알림을 수신하는 응용 프로그램 구성에만 적용됩니다.

섹션에서 두 **[!UICONTROL Mobile application properties]** 개의 URL이 나열됩니다. **[!UICONTROL Collect PII endpoint]** 및 **[!UICONTROL Location Services endpoint]**. Adobe Mobile Services 인터페이스에서 사용됩니다. Adobe [Mobile Services에서 모바일 앱 구성을 참조하십시오](#configuring-a-mobile-app-in-adobe-mobile-services).

* 이 **[!UICONTROL Collect PII endpoint]** URL은 모바일 응용 프로그램이 시작될 때 사용자의 Experience Cloud ID 및 등록 토큰을 수집하는 데 사용됩니다. 사용자가 이메일, 이름, 성 등과 같은 자격 증명을 사용하여 응용 프로그램에 로그인하면 이 데이터도 수집되어 사용자의 등록 토큰을 Adobe Campaign 프로필과 조정하는 데 사용됩니다.
* 이 **[!UICONTROL Location Services endpoint]** URL은 관심 영역에서 사용자의 위도, 경도 및 반경과 같은 위치 데이터를 수집하는 데 사용됩니다.

Adobe Mobile Services의 모바일 앱 구성 섹션에 설명된 대로 Adobe Mobile Services에서 이 값을 사용하여 구성을 [완료할 수](#configuring-a-mobile-app-in-adobe-mobile-services) 있습니다.

![](assets/poi_mobile_app_properties.png)

### Adobe Mobile Services에서 V4 모바일 앱 구성 {#configuring-a-mobile-app-in-adobe-mobile-services}

Adobe Mobile Services에서 수집한 데이터를 Adobe Campaign으로 전송하려면 Mobile Services 인터페이스에서 포스트백을 구성해야 합니다.

Adobe Campaign의 모바일 애플리케이션 매개 변수 설정에서 찾을 수 있는 특정 정보가 필요합니다(Campaign에서 [모바일 앱 설정 참조](#setting-up-a-mobile-app-in-campaign)).

* **[!UICONTROL IMS Organization ID]**
* **[!UICONTROL Collect PII Endpoint]**
* **[!UICONTROL Location Services endpoint]**

다음 구성을 수행하려면 Adobe Analytics에 액세스할 수 있어야 합니다. Adobe Analytics 사용자가 아닌 경우 Adobe Campaign 관리자에게 문의하십시오.

1. mobilemarketing.adobe.com [에 로그인합니다](https://mobilemarketing.adobe.com/).
1. 애플리케이션을 만들거나 기존 애플리케이션을 선택합니다.
1. Go to the **[!UICONTROL Manage App Settings]** page.
1. 방문자 **ID 서비스** 섹션에서 **활성화를** 선택하고 드롭다운 목록에서 조직을 선택합니다. **저장**&#x200B;을 클릭합니다.

   >[!CAUTION]
   >
   >이 조직은 Adobe Campaign 인스턴스에서 사용하는 조직과 동일해야 합니다.

1. **[!UICONTROL Manage Postbacks]**&#x200B;을(를) 클릭합니다.
1. 포스트백을 만듭니다.

   * 로 **[!UICONTROL PII]** 선택합니다 **[!UICONTROL Postback Type]**.
   * 이 **[!UICONTROL URL]** 필드에서, 서버 이름 앞에 있는 Adobe Campaign 인터페이스에 구성된 모바일 응용 프로그램의 **[!UICONTROL Collect PII Endpoint]** URL을 복사합니다. Campaign [에서 모바일 앱 설정을 참조하십시오](#setting-up-a-mobile-app-in-campaign).
   * 다음과 같이 **[!UICONTROL Post Body]** 필드를 입력합니다.

      iOS의 경우:

      ```
      {
      "userKey": "{userKey}",
      "pushPlatform":"apns",
      "marketingCloudId":"{%mcid%}",
      "cusEmail":"{email}",
      "cusFirstName":"{firstName}",
      "cusLastName":"{lastName}"
      }
      ```

      Android의 경우:

      ```
      {
      "userKey": "{userKey}",
      "pushPlatform":"gcm",
      "marketingCloudId":"{%mcid%}",
      "cusEmail":"{email}",
      "cusFirstName":"{firstName}",
      "cusLastName":"{lastName}"
      }
      ```

   * 컨텐츠 **유형을** 로 설정합니다 **[!UICONTROL application/json]**.
   * 포스트백을 트리거하는 **데이터 태그에서는?**, select any event, generally **[!UICONTROL Launched]** and **[!UICONTROL exists]**.
   * **[!UICONTROL Save & Activate]**&#x200B;을(를) 클릭합니다.

1. 두 번째 포스트백을 만듭니다.

   * 로 **[!UICONTROL Postback]** 선택합니다 **[!UICONTROL Postback Type]**.
   * 이 **[!UICONTROL URL]** 필드에서, 서버 이름 앞에 있는 Adobe Campaign 인터페이스에 구성된 모바일 응용 프로그램의 **[!UICONTROL Location Services Endpoint]** URL을 복사합니다. Campaign [에서 모바일 앱 설정을 참조하십시오](#setting-up-a-mobile-app-in-campaign).
   * 다음과 같이 **[!UICONTROL Post Body]** 필드를 입력합니다.

      ```
      {
      "locationData":{
      "distances":"{a.loc.dist}",
      "poiLabel":"{a.loc.poi}",
      "latitude.a":"{a.loc.lat.a}",
      "latitude.b":"{a.loc.lat.b}",
      "latitude.c":"{a.loc.lat.c}",
      "longitude.a":"{a.loc.lon.a}",
      "longitude.b":"{a.loc.lon.b}",
      "longitude.c":"{a.loc.lon.c}",
      "appId":"{a.appid}",
      "marketingCloudId":"{mid}"
      }
      }
      ```

   * 컨텐츠 **유형을** 로 설정합니다 **[!UICONTROL application/json]**.
   * 포스트백을 트리거하는 **데이터 태그에서는?**, select **[!UICONTROL campaign.test]** and **[!UICONTROL exists]**.
   * **[!UICONTROL Save & Activate]**&#x200B;을(를) 클릭합니다.

>[!NOTE]
>
>포스트백 구성에 대한 자세한 내용은 [Adobe Mobile Services 설명서를 참조하십시오](https://docs.adobe.com/content/help/en/mobile-services/using/manage-app-settings-ug/configuring-app/signals.html).

### 모바일 애플리케이션에 SDK 통합 {#integrating-the-sdk-into-a-mobile-application}

모바일 코어 서비스의 SDK(Software Development Kit)는 모바일 애플리케이션을 Adobe Campaign에 쉽게 통합할 수 있도록 해줍니다.

이 단계는 이 [페이지에 설명되어 있습니다](https://helpx.adobe.com/kr/campaign/kb/configuring-app-sdkv4.html).

### Adobe Mobile Services의 관심 영역 정의 {#defining-points-of-interest-in-adobe-mobile-services}

위치 데이터를 수집하는 데 사용되는 관심 영역을 정의하려면

1. Adobe Mobile Services 인터페이스로 이동합니다.
1. 애플리케이션을 추가합니다.

   Mobile Services에서 응용 프로그램을 관리하는 방법에 대한 자세한 내용은 [Adobe Mobile Services 설명서를 참조하십시오](https://docs.adobe.com/content/help/en/mobile-services/using/manage-apps-ug/t-new-app.html).

1. 관심 영역을 정의합니다.

   관심 영역 관리에 대한 자세한 내용은 [Adobe Mobile Services 설명서를 참조하십시오](https://docs.adobe.com/content/help/en/mobile-services/using/location-ug/t-manage-points.html).

### 가입자의 관심 영역 데이터 수집 {#collecting-subscribers--points-of-interest-data}

특정 사용자 지정 리소스를 사용하면 응용 프로그램의 구독자로부터 수집할 데이터를 정의할 수 있습니다.

이 단계는 SDK V4 [를 사용하여 모바일 애플리케이션 구성 페이지에서 설명합니다](https://helpx.adobe.com/kr/campaign/kb/configuring-app-sdkv4.html) .


## 위치 데이터를 수집하는 데 사용되는 모바일 앱 액세스 {#accessing-mobile-apps-used-to-collect-location-data}

Adobe Campaign에서 성공적으로 생성된 응용 프로그램에 액세스하려면:

1. Click the **[!UICONTROL Adobe Campaign]** logo, in the top left corner.
1. > **[!UICONTROL Administration]****[!UICONTROL Channels]** > **[!UICONTROL Mobile app (SDK v4)]** 또는 SDK에 따라 **[!UICONTROL Mobile app (AEP SDK)]** 선택합니다.
1. 목록에서 모바일 애플리케이션을 선택하여 속성을 표시합니다.

   ![](assets/poi_mobile_app_subscribers.png)

애플리케이션의 구독자 목록도 **[!UICONTROL Mobile application subscribers]** 탭에 표시됩니다. 구독자는 모바일 장치에 응용 프로그램을 설치한 모든 사용자입니다. Adobe Campaign 데이터베이스 프로필은 등록 토큰으로 식별됩니다.

## 수집된 위치 데이터 액세스 {#accessing-collected-location-data}

설정이 완료되면 수집된 관심 영역 데이터가 각 프로필의 **[!UICONTROL Places]** 탭에 나열됩니다. 목록에 액세스하려면

1. 프로필을 선택합니다.
1. 오른쪽에 있는 **[!UICONTROL Edit profile properties]** 단추를 클릭합니다.
1. **[!UICONTROL Places]** 탭을 선택합니다. 

   ![](assets/poi_profile_places.png)

현재 프로필에 대해 수집된 관심 영역 데이터가 나열됩니다. 위치정보는 6개월간 Adobe Campaign 데이터베이스에 저장된다.

프로필 액세스 및 편집에 대한 자세한 내용은 [프로필을 참조하십시오](../../audiences/using/about-profiles.md).
