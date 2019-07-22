---
title: 캠페인 관심 영역 데이터 통합 구성
seo-title: 캠페인 관심 영역 데이터 통합 구성
description: 캠페인 관심 영역 데이터 통합 구성
seo-description: Adobe Campaign의 관심 영역 데이터 기능을 구성하여 가입자의 위치를 기반으로 개인화된 메시지를 전송하는 방법을 살펴볼 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 0689 A 06 C-CC 1 A -442 F -95 B 8-A 07 FCEC 85 D 79
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 통합
content-type: 참조
topic-tags: working-with-campaign-and-analytics-for-mobile
discoiquuid: A 967 C 6 CC-C 53 B -41 B 4-866 B -90860 D 78 F 463
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 84fc114152385063ef07927e37d71f0c660225cf

---


# Configuring Campaign-Points of Interest data integration{#configuring-campaign-points-of-interest-data-integration}

## Configuring Campaign-Points of Interest data integration using SDK V4 {#configuring-campaign-poi-sdkv4}

The mobile applications used to collect location data must be configured by an **administrator** in the Adobe Campaign interface.

SDK v 4로 구성된 모바일 애플리케이션에서 관심 영역 데이터 기능을 사용하려면 다음을 수행해야 합니다.

1. 모바일용 Adobe Analytics에 액세스할 수 있습니다. 자세한 내용은 라이선스 계약을 확인하거나 Adobe 계정 관리자에게 문의하십시오.
1. Adobe Campaign에서 모바일 애플리케이션을 설정합니다. See [Setting up a mobile app in Campaign](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#setting-up-a-mobile-app-in-campaign).
1. Adobe Mobile Services 인터페이스에서 모바일 애플리케이션을 설정합니다. 이렇게 하면 Adobe Mobile Services에서 수집한 데이터가 Adobe Campaign로 전송되도록 할 수 있습니다. See [Configuring a mobile app in Adobe Mobile Services](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#configuring-a-mobile-app-in-adobe-mobile-services).
1. 모바일 응용 프로그램의 특정 설정을 수행합니다.

   * Adobe Mobile Services 인터페이스에서 다운로드한 구성 파일을 모바일 응용 프로그램과 패키지화합니다.
   * 모바일 애플리케이션에 Experience Cloud Mobile SDK 통합 See [Integrating the SDK into a mobile application](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#integrating-the-sdk-into-a-mobile-application).

1. Adobe Mobile Services 인터페이스에 관심 영역을 정의합니다. See [Defining Points of Interest in Adobe Mobile Services](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#defining-points-of-interest-in-adobe-mobile-services).
1. 모바일 애플리케이션 구독자로부터 수집할 데이터를 정의합니다. See [Collecting subscribers' Points of interest data](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#collecting-subscribers--points-of-interest-data).
1. Adobe Campaign에서 모바일 응용 프로그램 및 수집된 위치 데이터에 액세스해야 합니다. See [Accessing mobile apps used to collect location data](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#accessing-mobile-apps-used-to-collect-location-data) and [Accessing collected location data](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#accessing-collected-location-data).

### Setting up a mobile app in Adobe Campaign using SDK V4 {#setting-up-a-mobile-app-in-campaign}

Adobe Campaign를 사용하여 관심 영역 데이터를 수집하려면 Adobe Campaign 이 데이터를 수신할 모바일 애플리케이션을 구성해야 합니다.

1. Click the **[!UICONTROL Adobe Campaign]** logo, in the top left corner, then select **[!UICONTROL Administration]** &gt; **[!UICONTROL Channels]** &gt; **[!UICONTROL Mobile app]**.
1. Click **[!UICONTROL Create]** to set up an application.
1. **[!UICONTROL Application name]** 필드에 이름을 입력하고 **[!UICONTROL Create]**&#x200B;를 클릭합니다.

   **[!UICONTROL Device-specific settings]** 섹션을 채우지 마십시오. 이것은 푸시 알림을 수신하는 응용 프로그램을 구성하는 경우에만 적용됩니다.

**[!UICONTROL Mobile application properties]** 이 섹션에서는 두 URL 이 나열됩니다. **[!UICONTROL Collect PII endpoint]** **[!UICONTROL Location Services endpoint]** And. Adobe Mobile Services 인터페이스에서 사용됩니다. See [Configuring a mobile app in Adobe Mobile Services](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#configuring-a-mobile-app-in-adobe-mobile-services).

* The **[!UICONTROL Collect PII endpoint]** URL is used to collect the users' Experience Cloud IDs and registration tokens from the mobile application when it is launched. 사용자가 이메일, 이름, 성 등과 같은 자격 증명을 사용하여 애플리케이션에 로그인하면, 이 데이터도 수집되어 Adobe Campaign 프로필과 사용자의 등록 토큰을 조정하는 데 사용됩니다.
* **[!UICONTROL Location Services endpoint]** URL는 관심 영역에서 사용자의 위도, 경도 및 반경과 같은 위치 데이터를 수집하는 데 사용됩니다.

You can now use these values in Adobe Mobile Services to finish the configuration, as explained in the [Configuring a mobile app in Adobe Mobile Services](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#configuring-a-mobile-app-in-adobe-mobile-services) section.

![](assets/poi_mobile_app_properties.png)

### Configuring a V4 mobile app in Adobe Mobile Services {#configuring-a-mobile-app-in-adobe-mobile-services}

Adobe Mobile Services에서 수집한 데이터를 Adobe Campaign로 전송하려면 Mobile Services 인터페이스에서 포스트백을 구성해야 합니다.

You will need specific information that you can find in the mobile application parameters set in Adobe Campaign (see [Setting up a mobile app in Campaign](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#setting-up-a-mobile-app-in-campaign)):

* **[!UICONTROL IMS Organization ID]**
* **[!UICONTROL Collect PII Endpoint]**
* **[!UICONTROL Location Services endpoint]**

다음 구성을 수행하려면 Adobe Analytics에 대한 액세스 권한이 있어야 합니다. Adobe Analytics 사용자가 아닌 경우 Adobe Campaign 관리자에게 문의하십시오.

1. [mobilemarketing.adobe.com](http://mobilemarketing.adobe.com/)에 로그인합니다.
1. 애플리케이션을 만들거나 기존 애플리케이션을 선택합니다.
1. **[!UICONTROL Manage App Settings]** 페이지로 이동합니다.
1. In the **Visitor ID Service ** section, check **Enable** and select your organization from the drop-down list. ****&#x200B;저장을 클릭합니다.

   >[!CAUTION]
   >
   >이 조직은 Adobe Campaign 인스턴스에서 사용하는 것과 동일해야 합니다.

1. **[!UICONTROL Manage Postbacks]**&#x200B;을 클릭합니다.
1. 포스트백을 만듭니다.

   * Select **[!UICONTROL PII]** as the **[!UICONTROL Postback Type]**.
   * **[!UICONTROL URL]** 이 필드에 Adobe Campaign 인터페이스에서 구성한 모바일 응용 프로그램의 **[!UICONTROL Collect PII Endpoint]** URL 앞에 서버 이름을 복사합니다. See [Setting up a mobile app in Campaign](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#setting-up-a-mobile-app-in-campaign).
   * **[!UICONTROL Post Body]** 필드를 다음과 같이 입력합니다.

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

   * **컨텐츠 유형을** 다음으로 **[!UICONTROL application/json]**&#x200B;설정합니다.
   * In the **Which Data Tags Trigger the Postback?**, select any event, typically **[!UICONTROL Launched]** and **[!UICONTROL exists]**.
   * **[!UICONTROL Save & Activate]**&#x200B;을 클릭합니다.

1. 두 번째 포스트백을 만듭니다.

   * Select **[!UICONTROL Postback]** as the **[!UICONTROL Postback Type]**.
   * **[!UICONTROL URL]** 이 필드에 Adobe Campaign 인터페이스에서 구성한 모바일 응용 프로그램의 **[!UICONTROL Location Services Endpoint]** URL 앞에 서버 이름을 복사합니다. See [Setting up a mobile app in Campaign](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#setting-up-a-mobile-app-in-campaign).
   * **[!UICONTROL Post Body]** 필드를 다음과 같이 입력합니다.

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

   * **컨텐츠 유형을** 다음으로 **[!UICONTROL application/json]**&#x200B;설정합니다.
   * In the **Which Data Tags Trigger the Postback?**, select **[!UICONTROL campaign.test]** and **[!UICONTROL exists]**.
   * **[!UICONTROL Save & Activate]**&#x200B;을 클릭합니다.

>[!NOTE]
>
>For detailed information on configuring postbacks, refer to the [Adobe Mobile Services documentation](https://marketing.adobe.com/resources/help/en_US/mobile/signals_.html).

### Integrating the SDK into a mobile application {#integrating-the-sdk-into-a-mobile-application}

모바일 코어 서비스 SDK (Software Development Kit) 를 사용하면 모바일 애플리케이션을 Adobe Campaign에 쉽게 통합할 수 있습니다.

This step is described in this [page](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html).

### Defining Points of Interest in Adobe Mobile Services {#defining-points-of-interest-in-adobe-mobile-services}

위치 데이터를 수집하는 데 사용되는 관심 영역을 정의하려면:

1. Adobe Mobile Services 인터페이스로 이동합니다.
1. 애플리케이션을 추가합니다.

   For more information on managing applications in Mobile Services, refer to the [Adobe Mobile Services documentation](https://marketing.adobe.com/resources/help/en_US/mobile/t_new_app.html).

1. 관심 영역을 정의합니다.

   For more information on managing Points of Interest, refer to the [Adobe Mobile Services documentation](https://marketing.adobe.com/resources/help/en_US/mobile/t_manage_points.html).

### Collecting subscribers' Points of interest data {#collecting-subscribers--points-of-interest-data}

특정 사용자 지정 리소스를 사용하면 애플리케이션 구독자로부터 수집할 데이터를 정의할 수 있습니다.

This step is described in the [Configuring a mobile application using SDK V4](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html) page.

## Configuring Campaign-Points of Interest data integration with Adobe Experience Platform SDKs {#configuring-campaign-poi-aep-sdk}

>[!NOTE]
>
>Adobe Experience Platform SDK를 사용하여 이미 Adobe Campaign Standard에서 모바일 애플리케이션을 구성해야 합니다. For the detailed steps, refer to this [page](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html).

The mobile applications used to collect location data must be configured by an **administrator** in the Adobe Campaign interface.

Adobe Experience Platform SDK로 구성된 모바일 애플리케이션과 함께 Adobe Experience Platform 위치 서비스를 사용하려면 다음을 수행해야 합니다.

1. Add the **[!UICONTROL Places]** and **[!UICONTROL Places Monitor]** extensions to your mobile app configuration in Adobe Experience Platform Launch. Adobe Campaign에서 모바일 애플리케이션을 설정합니다. See [Install the Places extension in Adobe Experience Platform Launch](https://placesdocs.com/places-services-by-adobe-documentation/configure-places-in-the-sdk/places-extension#install-the-places-extension-in-adobe-experience-platform-launch) and [Install the Places Monitor extension in Experience Platform Launch](https://placesdocs.com/places-services-by-adobe-documentation/configure-places-in-the-sdk/places-monitor-extension/using-the-places-monitor-extension).

1. Once your extensions are set up, create data elements within **[!UICONTROL Adobe Experience Platform Launch]** to retrieve data from these extensions.

1. Then, in **[!UICONTROL Adobe Experience Platform Launch]**, you need to create rules to support mobile use cases between Point of Interests and Adobe Campaign.\
   This rule will be triggered when a user enters a geo-fenced **[!UICONTROL Point of Interest]**. Refer to this [page](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html#Locationpostback) to create your rule.

1. 장소에 관심 영역 정의 See [Create a Point of Interest](https://placesdocs.com/places-services-by-adobe-documentation/places-database-management-1/managing-pois-in-the-places-ui#create-a-poi).

1. Adobe Campaign에서 모바일 응용 프로그램 및 수집된 위치 데이터에 액세스해야 합니다. See [Accessing mobile apps used to collect location data](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#accessing-mobile-apps-used-to-collect-location-data) and [Accessing collected location data](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#accessing-collected-location-data).

## Accessing mobile apps used to collect location data {#accessing-mobile-apps-used-to-collect-location-data}

Adobe Campaign에서 성공적으로 만든 애플리케이션에 액세스하려면:

1. Click the **[!UICONTROL Adobe Campaign]** logo, in the top left corner.
1. **[!UICONTROL Administration]** &gt; **[!UICONTROL Channels]** &gt; **[!UICONTROL Mobile app (SDK v4)]** 또는 SDK에 **[!UICONTROL Mobile app (AEP SDK)]** 따라 선택합니다.
1. 목록에서 모바일 애플리케이션을 선택하여 속성을 표시합니다.

   ![](assets/poi_mobile_app_subscribers.png)

응용 프로그램의 구독자 목록도 표시됩니다. 구독자는 모바일 장치에 애플리케이션을 설치한 모든 사용자입니다. Adobe Campaign 데이터베이스 프로필은 등록 토큰으로 식별됩니다.

## Accessing collected location data {#accessing-collected-location-data}

Once the setup is done, the collected Points of Interest data is listed in the **[!UICONTROL Places]** tab of each profile. 목록에 액세스하려면:

1. 프로필을 선택합니다.
1. Click the **[!UICONTROL Edit profile properties]** button on the right.
1. **[!UICONTROL Places]** 탭을 선택합니다.

   ![](assets/poi_profile_places.png)

현재 프로필에 대한 수집된 관심 영역 데이터가 나열됩니다. 위치 데이터는 6 개월간 Adobe Campaign 데이터베이스에 저장됩니다.

For more information on accessing and editing profiles, see [Profiles](../../audiences/using/about-profiles.md).
