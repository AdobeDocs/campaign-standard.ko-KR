---
title: Campaign-Points of Interest 데이터 통합 구성
description: Adobe Campaign의 관심 영역 데이터 기능을 구성하여 구독자의 위치를 기반으로 개인화된 메시지를 전송하는 방법을 살펴볼 수 있습니다.
page-status-flag: never-activated
uuid: 0689a06c-cc1a-442f-95b8-a07fcec85d79
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-analytics-for-mobile
discoiquuid: a967c6cc-c53b-41b4-866b-90860d78f463
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: fc9c6371732aa0eba9e675d2709cd62c25b27b96

---


# Campaign-Points of Interest 데이터 통합 구성{#configuring-campaign-points-of-interest-data-integration}

## Adobe Experience Platform SDK와 캠페인 관심 영역 데이터 통합 구성 {#configuring-campaign-poi-aep-sdk}

>[!NOTE]
>
>모바일 애플리케이션은 Adobe Experience Platform SDK를 사용하여 Adobe Campaign Standard에서 이미 구성되어야 합니다. 자세한 내용은 이 [페이지를](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html)참조하십시오.

위치 데이터를 수집하는 데 사용되는 모바일 애플리케이션은 **관리자가** Adobe Campaign 인터페이스에서 구성해야 합니다.

Adobe Experience Platform SDK 파섹

1. Adobe Experience Platform Launch에서 모바일 앱 구성에 **[!UICONTROL Places]** 및 **[!UICONTROL Places Monitor]** 확장을 추가합니다. Adobe Campaign에서 모바일 애플리케이션을 설정합니다. Adobe [Experience Platform Launch에서 위치 확장](https://docs.adobe.com/content/help/en/places/using/places-ext-aep-sdks/places-extension/places-extension.html#install-the-places-extension-in-adobe-experience-platform-launch) 설치 및 [Experience Platform Launch에서 위치 모니터 확장 설치를 참조하십시오](https://docs.adobe.com/content/help/en/places/using/places-ext-aep-sdks/places-monitor-extension/using-places-monitor-extension.html#install-the-places-monitor-extension-in-experience-platform-launch).

1. 익스텐션이 설정되면 데이터 요소를 만들어 이러한 익스텐션에서 데이터를 **[!UICONTROL Adobe Experience Platform Launch]** 검색합니다. 데이터 요소를 만들려면 이 [페이지를](https://helpx.adobe.com/campaign/kb/config-app-in-launch.html#Step1Createdataelements) 참조하십시오.

1. 그런 **[!UICONTROL Adobe Experience Platform Launch]**&#x200B;다음 관심 영역과 Adobe Campaign 간의 모바일 사용 사례를 지원하는 규칙을 만들어야 합니다.\
   이 규칙은 사용자가 지리적 울타리로 들어갈 때 트리거됩니다 **[!UICONTROL Point of Interest]**. 규칙을 만들려면 이 [페이지를](https://helpx.adobe.com/campaign/kb/config-app-in-launch.html#Locationpostback) 참조하십시오.

1. 위치에서 **[!UICONTROL Points of Interest]** 사용자 정의 관심 [영역 만들기를 참조하십시오](https://docs.adobe.com/content/help/en/places/using/poi-mgmt-ui/create-a-poi-ui.html).

1. Adobe Campaign에서 모바일 애플리케이션 및 수집된 위치 데이터에 액세스해야 합니다. 위치 [데이터를](#accessing-mobile-apps-used-to-collect-location-data) 수집하는 데 사용되는 모바일 앱 액세스 및 [수집된 위치 데이터](#accessing-collected-location-data)액세스를 참조하십시오.

## SDK V4를 사용하여 캠페인 관심 영역 데이터 통합 구성 {#configuring-campaign-poi-sdkv4}

위치 데이터를 수집하는 데 사용되는 모바일 애플리케이션은 **관리자가** Adobe Campaign 인터페이스에서 구성해야 합니다.

SDK V4로 구성된 모바일 애플리케이션에서 관심 영역 데이터 기능을 사용하려면 다음을 수행해야 합니다.

1. 모바일용 Adobe Analytics에 액세스할 수 있습니다. 자세한 내용은 라이선스 계약서를 확인하거나 Adobe 계정 담당자에게 문의하십시오.
1. Adobe Campaign에서 모바일 애플리케이션을 설정합니다. Campaign [에서 모바일 앱 설정을 참조하십시오](#setting-up-a-mobile-app-in-campaign).
1. Adobe Mobile Services 인터페이스에서 모바일 애플리케이션을 설정합니다. 이렇게 하면 Adobe Mobile Services에서 수집한 데이터가 Adobe Campaign으로 전송되도록 할 수 있습니다. Adobe [Mobile Services에서 모바일 앱 구성을 참조하십시오](#configuring-a-mobile-app-in-adobe-mobile-services).
1. 모바일 응용 프로그램의 특정 설정을 수행합니다.

   * Adobe Mobile Services 인터페이스에서 다운로드한 구성 파일을 모바일 응용 프로그램과 함께 패키징합니다.
   * Experience Cloud Mobile SDK를 모바일 애플리케이션에 통합합니다. SDK [를 모바일 애플리케이션에](#integrating-the-sdk-into-a-mobile-application)통합을 참조하십시오.

1. Adobe Mobile Services 인터페이스에서 관심 영역을 정의합니다. Adobe [Mobile Services의 관심 영역 정의를 참조하십시오](#defining-points-of-interest-in-adobe-mobile-services).
1. 모바일 애플리케이션의 가입자로부터 수집할 데이터를 정의합니다. 가입자의 [관심 영역 데이터](#collecting-subscribers--points-of-interest-data)수집을 참조하십시오.
1. Adobe Campaign에서 모바일 애플리케이션 및 수집된 위치 데이터에 액세스해야 합니다. 위치 [데이터를](#accessing-mobile-apps-used-to-collect-location-data) 수집하는 데 사용되는 모바일 앱 액세스 및 [수집된 위치 데이터](#accessing-collected-location-data)액세스를 참조하십시오.

### SDK V4를 사용하여 Adobe Campaign에서 모바일 앱 설정 {#setting-up-a-mobile-app-in-campaign}

Adobe Campaign을 사용하여 관심 영역 데이터를 수집하려면 Adobe Campaign에서 데이터를 수신할 모바일 애플리케이션을 구성해야 합니다.

1. 왼쪽 상단 모서리에서 **[!UICONTROL Adobe Campaign]** 로고를 클릭한 다음 **[!UICONTROL Administration]** &gt; **[!UICONTROL Channels]** &gt; **[!UICONTROL Mobile app]**&#x200B;를 선택합니다.
1. 애플리케이션을 **[!UICONTROL Create]** 설정하려면 을 클릭합니다.
1. 필드에 이름을 **[!UICONTROL Application name]** 입력하고 을 클릭합니다 **[!UICONTROL Create]**.

   섹션을 채우지 **[!UICONTROL Device-specific settings]** 마십시오. 이는 푸시 알림을 수신하는 애플리케이션을 구성하는 경우에만 적용됩니다.

이 **[!UICONTROL Mobile application properties]** 섹션에는 두 개의 URL이 나열됩니다. **[!UICONTROL Collect PII endpoint]** 및 **[!UICONTROL Location Services endpoint]** Adobe Adobe Mobile Services 인터페이스에서 사용됩니다. Adobe [Mobile Services에서 모바일 앱 구성을 참조하십시오](#configuring-a-mobile-app-in-adobe-mobile-services).

* URL은 **[!UICONTROL Collect PII endpoint]** 실행 시 모바일 애플리케이션에서 사용자의 Experience Cloud ID 및 등록 토큰을 수집하는 데 사용됩니다. 사용자가 이메일, 이름, 성 등과 같은 자격 증명을 사용하여 응용 프로그램에 로그인하면 이 데이터도 수집되어 사용자의 등록 토큰을 Adobe Campaign 프로필과 조정하는 데 사용됩니다.
* URL은 **[!UICONTROL Location Services endpoint]** 사용자의 위도, 경도 및 관심 영역에서 반경 등의 위치 데이터를 수집하는 데 사용됩니다.

이제 Adobe Mobile Services의 모바일 앱 구성 섹션에 설명된 대로 Adobe Mobile [Services에서 이러한 값을 사용하여 구성을 완료할 수](#configuring-a-mobile-app-in-adobe-mobile-services) 있습니다.

![](assets/poi_mobile_app_properties.png)

### Adobe Mobile Services에서 V4 모바일 앱 구성 {#configuring-a-mobile-app-in-adobe-mobile-services}

Adobe Mobile Services에서 수집한 데이터를 Adobe Campaign으로 전송하려면 Mobile Services 인터페이스에서 포스트백을 구성해야 합니다.

Adobe Campaign에 설정된 모바일 애플리케이션 매개 변수에서 찾을 수 있는 특정 정보가 필요합니다(Campaign에서 [모바일 앱 설정 참조](#setting-up-a-mobile-app-in-campaign)).

* **[!UICONTROL IMS Organization ID]**
* **[!UICONTROL Collect PII Endpoint]**
* **[!UICONTROL Location Services endpoint]**

다음 구성을 수행하려면 Adobe Analytics에 액세스할 수 있어야 합니다. Adobe Analytics 사용자가 아닌 경우 Adobe Campaign 관리자에게 문의하십시오.

1. mobilemarketing. [adobe.com에](https://mobilemarketing.adobe.com/)로그인합니다.
1. 애플리케이션을 만들거나 기존 애플리케이션을 선택합니다.
1. 페이지로 **[!UICONTROL Manage App Settings]** 이동합니다.
1. 방문자 **ID 서비스** 섹션에서 **활성화를** 선택하고 드롭다운 목록에서 조직을 선택합니다. 저장을 **클릭합니다**.

   >[!CAUTION]
   >
   >이 조직은 Adobe Campaign 인스턴스에서 사용하는 조직과 동일해야 합니다.

1. Click **[!UICONTROL Manage Postbacks]**.
1. 포스트백을 만듭니다.

   * 로 **[!UICONTROL PII]** 선택합니다 **[!UICONTROL Postback Type]**.
   * 이 **[!UICONTROL URL]** 필드에서 Adobe Campaign 인터페이스에서 구성한 모바일 응용 프로그램의 URL과 **[!UICONTROL Collect PII Endpoint]** 서버 이름을 차례로 복사합니다. Campaign [에서 모바일 앱 설정을 참조하십시오](#setting-up-a-mobile-app-in-campaign).
   * 다음과 같이 **[!UICONTROL Post Body]** 필드를 채웁니다.

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
   * 포스트백을 트리거하는 데이터 태그는 **무엇입니까?**&#x200B;를 선택한 경우, 일반적으로 **[!UICONTROL Launched]** 및 **[!UICONTROL exists]**&#x200B;를 선택합니다.
   * Click **[!UICONTROL Save & Activate]**.

1. 두 번째 포스트백을 만듭니다.

   * 로 **[!UICONTROL Postback]** 선택합니다 **[!UICONTROL Postback Type]**.
   * 이 **[!UICONTROL URL]** 필드에서 Adobe Campaign 인터페이스에서 구성한 모바일 응용 프로그램의 URL과 **[!UICONTROL Location Services Endpoint]** 서버 이름을 차례로 복사합니다. Campaign [에서 모바일 앱 설정을 참조하십시오](#setting-up-a-mobile-app-in-campaign).
   * 다음과 같이 **[!UICONTROL Post Body]** 필드를 채웁니다.

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
   * 포스트백을 트리거하는 데이터 태그는 **무엇입니까?**&#x200B;을 선택하고 **[!UICONTROL campaign.test]** and를 **[!UICONTROL exists]**&#x200B;선택합니다.
   * Click **[!UICONTROL Save & Activate]**.

>[!NOTE]
>
>포스트백 구성에 대한 자세한 내용은 Adobe Mobile [Services 설명서를](https://marketing.adobe.com/resources/help/en_US/mobile/signals_.html)참조하십시오.

### 모바일 애플리케이션에 SDK 통합 {#integrating-the-sdk-into-a-mobile-application}

Mobile 코어 서비스의 SDK(소프트웨어 개발 키트)는 모바일 애플리케이션을 Adobe Campaign에 쉽게 통합합니다.

이 단계는 이 [페이지에](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html)설명되어 있습니다.

### Adobe Mobile Services의 관심 영역 정의 {#defining-points-of-interest-in-adobe-mobile-services}

위치 데이터를 수집하는 데 사용되는 관심 영역을 정의하려면

1. Adobe Mobile Services 인터페이스로 이동합니다.
1. 애플리케이션을 추가합니다.

   Mobile Services에서 응용 프로그램을 관리하는 방법에 대한 자세한 내용은 Adobe Mobile [Services 설명서를](https://marketing.adobe.com/resources/help/en_US/mobile/t_new_app.html)참조하십시오.

1. 관심 영역을 정의합니다.

   관심 영역 관리에 대한 자세한 내용은 Adobe Mobile [Services 설명서를 참조하십시오](https://marketing.adobe.com/resources/help/en_US/mobile/t_manage_points.html).

### 가입자의 관심 영역 데이터 수집 {#collecting-subscribers--points-of-interest-data}

특정 사용자 지정 리소스를 사용하면 애플리케이션의 구독자로부터 수집할 데이터를 정의할 수 있습니다.

이 단계는 SDK V4 [를 사용하여 모바일 애플리케이션 구성](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html) 페이지에서 설명합니다.


## 위치 데이터를 수집하는 데 사용되는 모바일 앱 액세스 {#accessing-mobile-apps-used-to-collect-location-data}

Adobe Campaign에서 성공적으로 생성된 애플리케이션에 액세스하려면

1. 왼쪽 상단 모서리에서 로고를 클릭합니다. **[!UICONTROL Adobe Campaign]**
1. &gt; **[!UICONTROL Administration]** &gt; **[!UICONTROL Channels]** &gt; **[!UICONTROL Mobile app (SDK v4)]** 또는 SDK에 따라 **[!UICONTROL Mobile app (AEP SDK)]** 선택합니다.
1. 목록에서 모바일 애플리케이션을 선택하여 속성을 표시합니다.

   ![](assets/poi_mobile_app_subscribers.png)

애플리케이션의 구독자 목록도 **[!UICONTROL Mobile application subscribers]** 탭에 표시됩니다. 구독자는 모바일 장치에 응용 프로그램을 설치한 모든 사용자입니다. Adobe Campaign 데이터베이스 프로필은 등록 토큰으로 식별됩니다.

## 수집된 위치 데이터 액세스 {#accessing-collected-location-data}

설정이 완료되면 수집된 관심 영역 데이터가 각 프로필의 **[!UICONTROL Places]** 탭에 나열됩니다. 목록에 액세스하려면

1. 프로필을 선택합니다.
1. 오른쪽에 있는 **[!UICONTROL Edit profile properties]** 단추를 클릭합니다.
1. 탭을 **[!UICONTROL Places]** 선택합니다.

   ![](assets/poi_profile_places.png)

현재 프로필에 대해 수집된 관심 영역 데이터가 나열됩니다. 위치 데이터는 6개월 동안 Adobe Campaign 데이터베이스에 저장됩니다.

프로필 액세스 및 편집에 대한 자세한 내용은 프로필을 [참조하십시오](../../audiences/using/about-profiles.md).
