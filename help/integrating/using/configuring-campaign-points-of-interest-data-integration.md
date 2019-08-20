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
source-git-commit: d857bee3e7cb54ec179a73d9c256a14771cbd474

---


# 캠페인 관심 영역 데이터 통합 구성{#configuring-campaign-points-of-interest-data-integration}

## Adobe Experience Platform SDK와 캠페인 관심 영역 데이터 통합 구성 {#configuring-campaign-poi-aep-sdk}

>[!NOTE]
>
>Adobe Experience Platform SDK를 사용하여 이미 Adobe Campaign Standard에서 모바일 애플리케이션을 구성해야 합니다. 자세한 단계는 이 [페이지를](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html)참조하십시오.

위치 데이터를 수집하는 데 사용되는 모바일 애플리케이션은 Adobe Campaign 인터페이스에서 **관리자가** 구성해야 합니다.

Adobe Experience Platform SDK로 구성된 모바일 애플리케이션과 함께 Adobe Experience Platform 위치 서비스를 사용하려면 다음을 수행해야 합니다.

1. Adobe Experience Platform Launch에서 모바일 앱 구성에 **[!UICONTROL Places]** 및 **[!UICONTROL Places Monitor]** 익스텐션을 추가할 수 있습니다. Adobe Campaign에서 모바일 애플리케이션을 설정합니다. Adobe Experience Platform에 위치 확장 [설치](https://placesdocs.com/places-services-by-adobe-documentation/configure-places-in-the-sdk/places-extension#install-the-places-extension-in-adobe-experience-platform-launch) 및 [Experience Platform Launch에서 장소 모니터 확장 설치를 참조하십시오](https://placesdocs.com/places-services-by-adobe-documentation/configure-places-in-the-sdk/places-monitor-extension/using-the-places-monitor-extension).

1. 익스텐션이 설정되면 해당 **[!UICONTROL Adobe Experience Platform Launch]** 익스텐션에서 데이터를 검색할 데이터 요소를 만듭니다. 데이터 요소를 만들려면 이 [페이지를](https://helpx.adobe.com/campaign/kb/config-app-in-launch.html#Step1Createdataelements) 참조하십시오.

1. 그런 다음, 관심 **[!UICONTROL Adobe Experience Platform Launch]**&#x200B;영역 및 Adobe Campaign 간의 모바일 사용 사례를 지원하는 규칙을 만들어야 합니다.\
   이 규칙은 사용자가 geo-fenced에 들어올 때 **[!UICONTROL Point of Interest]**&#x200B;트리거됩니다. 규칙을 만들려면 이 [페이지를](https://helpx.adobe.com/campaign/kb/config-app-in-launch.html#Locationpostback) 참조하십시오.

1. **[!UICONTROL Points of Interest]** 어디에서나 사용자 정의 관심 영역 [만들기를](https://placesdocs.com/places-services-by-adobe-documentation/places-database-management-1/managing-pois-in-the-places-ui#create-a-poi)참조하십시오.

1. Adobe Campaign에서 모바일 응용 프로그램 및 수집된 위치 데이터에 액세스해야 합니다. 위치 [데이터를](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#accessing-mobile-apps-used-to-collect-location-data) 수집하고 수집된 위치 데이터에 [액세스하는 데 사용되는 모바일 앱 액세스를 참조하십시오](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#accessing-collected-location-data).

## SDK v 4를 사용하여 캠페인 관심 영역 데이터 통합 구성 {#configuring-campaign-poi-sdkv4}

위치 데이터를 수집하는 데 사용되는 모바일 애플리케이션은 Adobe Campaign 인터페이스에서 **관리자가** 구성해야 합니다.

SDK v 4로 구성된 모바일 애플리케이션에서 관심 영역 데이터 기능을 사용하려면 다음을 수행해야 합니다.

1. 모바일용 Adobe Analytics에 액세스할 수 있습니다. 자세한 내용은 라이선스 계약을 확인하거나 Adobe 계정 관리자에게 문의하십시오.
1. Adobe Campaign에서 모바일 애플리케이션을 설정합니다. 캠페인에서 모바일 앱 [설정을 참조하십시오](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#setting-up-a-mobile-app-in-campaign).
1. Adobe Mobile Services 인터페이스에서 모바일 애플리케이션을 설정합니다. 이렇게 하면 Adobe Mobile Services에서 수집한 데이터가 Adobe Campaign로 전송되도록 할 수 있습니다. Adobe Mobile Services에서 모바일 앱 [구성을 참조하십시오](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#configuring-a-mobile-app-in-adobe-mobile-services).
1. 모바일 응용 프로그램의 특정 설정을 수행합니다.

   * Adobe Mobile Services 인터페이스에서 다운로드한 구성 파일을 모바일 응용 프로그램과 패키지화합니다.
   * 모바일 애플리케이션에 Experience Cloud Mobile SDK 통합 모바일 애플리케이션에 SDK [통합을 참조하십시오](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#integrating-the-sdk-into-a-mobile-application).

1. Adobe Mobile Services 인터페이스에 관심 영역을 정의합니다. Adobe Mobile Services에서 관심 [영역 정의를 참조하십시오](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#defining-points-of-interest-in-adobe-mobile-services).
1. 모바일 애플리케이션 구독자로부터 수집할 데이터를 정의합니다. 구독자 관심 영역 데이터 [수집을 참조하십시오](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#collecting-subscribers--points-of-interest-data).
1. Adobe Campaign에서 모바일 응용 프로그램 및 수집된 위치 데이터에 액세스해야 합니다. 위치 [데이터를](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#accessing-mobile-apps-used-to-collect-location-data) 수집하고 수집된 위치 데이터에 [액세스하는 데 사용되는 모바일 앱 액세스를 참조하십시오](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#accessing-collected-location-data).

### SDK v 4를 사용하여 Adobe Campaign에서 모바일 앱 설정 {#setting-up-a-mobile-app-in-campaign}

Adobe Campaign를 사용하여 관심 영역 데이터를 수집하려면 Adobe Campaign 이 데이터를 수신할 모바일 애플리케이션을 구성해야 합니다.

1. 왼쪽 위 모서리에서 **[!UICONTROL Adobe Campaign]** 로고를 클릭한 다음 **[!UICONTROL Administration]** &gt; **[!UICONTROL Channels]****[!UICONTROL Mobile app]**&#x200B;를 선택합니다.
1. 을 **[!UICONTROL Create]** 클릭하여 애플리케이션을 설정합니다.
1. **[!UICONTROL Application name]** 필드에 이름을 입력하고 **[!UICONTROL Create]**&#x200B;를 클릭합니다.

   **[!UICONTROL Device-specific settings]** 섹션을 채우지 마십시오. 이것은 푸시 알림을 수신하는 응용 프로그램을 구성하는 경우에만 적용됩니다.

**[!UICONTROL Mobile application properties]** 이 섹션에서는 두 URL 이 나열됩니다. **[!UICONTROL Collect PII endpoint]** **[!UICONTROL Location Services endpoint]** And. Adobe Mobile Services 인터페이스에서 사용됩니다. Adobe Mobile Services에서 모바일 앱 [구성을 참조하십시오](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#configuring-a-mobile-app-in-adobe-mobile-services).

* URL는 **[!UICONTROL Collect PII endpoint]** 모바일 응용 프로그램이 시작될 때 사용자의 Experience Cloud ID와 등록 토큰을 수집하는 데 사용됩니다. 사용자가 이메일, 이름, 성 등과 같은 자격 증명을 사용하여 애플리케이션에 로그인하면, 이 데이터도 수집되어 Adobe Campaign 프로필과 사용자의 등록 토큰을 조정하는 데 사용됩니다.
* **[!UICONTROL Location Services endpoint]** URL는 관심 영역에서 사용자의 위도, 경도 및 반경과 같은 위치 데이터를 수집하는 데 사용됩니다.

이제 Adobe Mobile Services에서 모바일 앱 [구성](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#configuring-a-mobile-app-in-adobe-mobile-services) 섹션에 설명된 대로, Adobe Mobile Services에서 이러한 값을 사용하여 구성을 완료할 수 있습니다.

![](assets/poi_mobile_app_properties.png)

### Adobe Mobile Services에서 v 4 모바일 앱 구성 {#configuring-a-mobile-app-in-adobe-mobile-services}

Adobe Mobile Services에서 수집한 데이터를 Adobe Campaign로 전송하려면 Mobile Services 인터페이스에서 포스트백을 구성해야 합니다.

Adobe Campaign에 설정된 모바일 애플리케이션 매개 변수에서 찾을 수 있는 특정 정보가 필요합니다 (캠페인의 모바일 앱 [설정 참조](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#setting-up-a-mobile-app-in-campaign)).

* **[!UICONTROL IMS Organization ID]**
* **[!UICONTROL Collect PII Endpoint]**
* **[!UICONTROL Location Services endpoint]**

다음 구성을 수행하려면 Adobe Analytics에 대한 액세스 권한이 있어야 합니다. Adobe Analytics 사용자가 아닌 경우 Adobe Campaign 관리자에게 문의하십시오.

1. [mobilemarketing.adobe.com](http://mobilemarketing.adobe.com/)에 로그인합니다.
1. 애플리케이션을 만들거나 기존 애플리케이션을 선택합니다.
1. **[!UICONTROL Manage App Settings]** 페이지로 이동합니다.
1. **방문자 ID 서비스** 섹션에서 **활성화** 여부를 확인하고 드롭다운 목록에서 조직을 선택합니다. ****&#x200B;저장을 클릭합니다.

   >[!CAUTION]
   >
   >이 조직은 Adobe Campaign 인스턴스에서 사용하는 것과 동일해야 합니다.

1. **[!UICONTROL Manage Postbacks]**&#x200B;을 클릭합니다.
1. 포스트백을 만듭니다.

   * 으로 선택합니다 **[!UICONTROL PII]****[!UICONTROL Postback Type]**.
   * **[!UICONTROL URL]** 이 필드에 Adobe Campaign 인터페이스에서 구성한 모바일 응용 프로그램의 **[!UICONTROL Collect PII Endpoint]** URL 앞에 서버 이름을 복사합니다. 캠페인에서 모바일 앱 [설정을 참조하십시오](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#setting-up-a-mobile-app-in-campaign).
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
   * 포스트백을 **트리거하는 데이터 태그에서**, select any event, typically **[!UICONTROL Launched]** and **[!UICONTROL exists]**.
   * **[!UICONTROL Save & Activate]**&#x200B;을 클릭합니다.

1. 두 번째 포스트백을 만듭니다.

   * 으로 선택합니다 **[!UICONTROL Postback]****[!UICONTROL Postback Type]**.
   * **[!UICONTROL URL]** 이 필드에 Adobe Campaign 인터페이스에서 구성한 모바일 응용 프로그램의 **[!UICONTROL Location Services Endpoint]** URL 앞에 서버 이름을 복사합니다. 캠페인에서 모바일 앱 [설정을 참조하십시오](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#setting-up-a-mobile-app-in-campaign).
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
   * 포스트백을 **트리거하는 데이터 태그에서**, select **[!UICONTROL campaign.test]** and **[!UICONTROL exists]**.
   * **[!UICONTROL Save & Activate]**&#x200B;을 클릭합니다.

>[!NOTE]
>
>포스트백 구성에 대한 자세한 내용은 [Adobe Mobile Services 설명서를](https://marketing.adobe.com/resources/help/en_US/mobile/signals_.html)참조하십시오.

### 모바일 애플리케이션에 SDK 통합 {#integrating-the-sdk-into-a-mobile-application}

모바일 코어 서비스 SDK (Software Development Kit) 를 사용하면 모바일 애플리케이션을 Adobe Campaign에 쉽게 통합할 수 있습니다.

이 단계는 이 [페이지에 설명되어](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html)있습니다.

### Adobe Mobile Services에서 관심 영역 정의 {#defining-points-of-interest-in-adobe-mobile-services}

위치 데이터를 수집하는 데 사용되는 관심 영역을 정의하려면:

1. Adobe Mobile Services 인터페이스로 이동합니다.
1. 애플리케이션을 추가합니다.

   Mobile Services에서 응용 프로그램을 관리하는 방법에 대한 자세한 내용은 [Adobe Mobile Services 설명서를](https://marketing.adobe.com/resources/help/en_US/mobile/t_new_app.html)참조하십시오.

1. 관심 영역을 정의합니다.

   관심 영역 관리에 대한 자세한 내용은 [Adobe Mobile Services 설명서를](https://marketing.adobe.com/resources/help/en_US/mobile/t_manage_points.html)참조하십시오.

### 가입자의 관심 영역 데이터 수집 {#collecting-subscribers--points-of-interest-data}

특정 사용자 지정 리소스를 사용하면 애플리케이션 구독자로부터 수집할 데이터를 정의할 수 있습니다.

이 단계는 SDK [v 4](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html) 페이지를 사용하여 모바일 애플리케이션 구성에서 설명합니다.


## 위치 데이터를 수집하는 데 사용된 모바일 앱 액세스 {#accessing-mobile-apps-used-to-collect-location-data}

Adobe Campaign에서 성공적으로 만든 애플리케이션에 액세스하려면:

1. 왼쪽 위 모서리에서 **[!UICONTROL Adobe Campaign]** 로고를 클릭합니다.
1. **[!UICONTROL Administration]** &gt; **[!UICONTROL Channels]** &gt; **[!UICONTROL Mobile app (SDK v4)]** 또는 SDK에 **[!UICONTROL Mobile app (AEP SDK)]** 따라 선택합니다.
1. 목록에서 모바일 애플리케이션을 선택하여 속성을 표시합니다.

   ![](assets/poi_mobile_app_subscribers.png)

응용 프로그램의 구독자 목록이 **[!UICONTROL Mobile application subscribers]** 탭에도 표시됩니다. 구독자는 모바일 장치에 애플리케이션을 설치한 모든 사용자입니다. Adobe Campaign 데이터베이스 프로필은 등록 토큰으로 식별됩니다.

## 수집된 위치 데이터에 액세스 {#accessing-collected-location-data}

설정이 완료되면 수집된 관심 영역 데이터가 각 프로필의 **[!UICONTROL Places]** 탭에 나열됩니다. 목록에 액세스하려면:

1. 프로필을 선택합니다.
1. 오른쪽에 있는 **[!UICONTROL Edit profile properties]** 버튼을 클릭합니다.
1. **[!UICONTROL Places]** 탭을 선택합니다.

   ![](assets/poi_profile_places.png)

현재 프로필에 대한 수집된 관심 영역 데이터가 나열됩니다. 위치 데이터는 6 개월간 Adobe Campaign 데이터베이스에 저장됩니다.

프로필 액세스 및 편집에 대한 자세한 내용은 [프로필을](../../audiences/using/about-profiles.md)참조하십시오.
