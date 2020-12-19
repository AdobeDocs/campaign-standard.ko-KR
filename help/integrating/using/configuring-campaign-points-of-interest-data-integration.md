---
solution: Campaign Standard
product: campaign
title: Campaign-Points of Interest 데이터 통합 구성
description: Adobe Campaign에서 관심 영역 데이터 기능을 구성하여 사용자의 위치를 기반으로 개인화된 메시지를 전송하는 방법을 알아봅니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-analytics-for-mobile
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '1340'
ht-degree: 3%

---


# Campaign-Points of Interest 데이터 통합 구성{#configuring-campaign-points-of-interest-data-integration}

## Adobe Experience Platform SDK {#configuring-campaign-poi-aep-sdk}와 캠페인 관심 영역 데이터 통합 구성

>[!NOTE]
>
>모바일 애플리케이션은 Adobe Experience Platform SDK를 사용하여 Adobe Campaign Standard에서 이미 구성되어야 합니다. 자세한 내용은 이 [페이지](https://helpx.adobe.com/kr/campaign/kb/configuring-app-sdk.html)를 참조하십시오.

위치 데이터를 수집하는 데 사용되는 모바일 응용 프로그램은 Adobe Campaign 인터페이스에서 **administrator**&#x200B;에 의해 구성해야 합니다.

Adobe Experience Platform SDK로 구성된 모바일 애플리케이션에서 Adobe Experience Platform Location Services를 사용할 수 있으려면 다음을 수행해야 합니다.

1. Adobe Experience Platform Launch의 모바일 앱 구성에 **[!UICONTROL Places]** 및 **[!UICONTROL Places Monitor]** 확장을 추가합니다. Adobe Campaign에서 모바일 애플리케이션을 설정합니다. Adobe Experience Platform Launch[에 위치 확장 설치 및 ](https://docs.adobe.com/content/help/en/places/using/places-ext-aep-sdks/places-extension/places-extension.html#install-the-places-extension-in-adobe-experience-platform-launch)Experience Platform Launch[에 위치 모니터 확장 설치를 참조하십시오.](https://docs.adobe.com/content/help/en/places/using/places-ext-aep-sdks/places-monitor-extension/using-places-monitor-extension.html#install-the-places-monitor-extension-in-experience-platform-launch)

1. 익스텐션이 설정되면 **[!UICONTROL Adobe Experience Platform Launch]** 내에 데이터 요소를 만들어 이러한 익스텐션에서 데이터를 검색합니다. 데이터 요소를 만들려면 이 [페이지](https://helpx.adobe.com/campaign/kb/config-app-in-launch.html#Step1Createdataelements)를 참조하십시오.

1. 그런 다음 **[!UICONTROL Adobe Experience Platform Launch]**&#x200B;에서 관심 사항과 Adobe Campaign 사이의 모바일 사용 사례를 지원하는 규칙을 만들어야 합니다.\
   사용자가 지리적 제약을 받는 **[!UICONTROL Point of Interest]**&#x200B;에 들어갈 때 이 규칙이 트리거됩니다. 규칙을 만들려면 이 [페이지](https://helpx.adobe.com/campaign/kb/config-app-in-launch.html#Locationpostback)를 참조하십시오.

1. 위치에서 **[!UICONTROL Points of Interest]**&#x200B;을(를) 정의합니다. [관심 영역 만들기](https://docs.adobe.com/content/help/en/places/using/poi-mgmt-ui/create-a-poi-ui.html)를 참조하십시오.

1. Adobe Campaign에서 모바일 응용 프로그램 및 수집된 위치 데이터에 액세스해야 합니다. 위치 데이터[ 및 ](#accessing-mobile-apps-used-to-collect-location-data)수집된 위치 데이터 액세스[를 참조하십시오.](#accessing-collected-location-data)

## SDK V4 {#configuring-campaign-poi-sdkv4}을(를) 사용하여 캠페인 관심 영역 데이터 통합 구성

위치 데이터를 수집하는 데 사용되는 모바일 응용 프로그램은 Adobe Campaign 인터페이스에서 **administrator**&#x200B;에 의해 구성해야 합니다.

SDK V4로 구성된 모바일 애플리케이션에서 관심 영역 데이터 기능을 사용하려면 다음을 수행해야 합니다.

1. 모바일용 Adobe Analytics을 이용할 수 있습니다. 자세한 내용은 라이선스 계약서를 확인하거나 Adobe 계정 관리자에게 문의하십시오.
1. Adobe Campaign에서 모바일 애플리케이션을 설정합니다. [Campaign](#setting-up-a-mobile-app-in-campaign)에서 모바일 앱 설정을 참조하십시오.
1. Adobe Mobile Services 인터페이스에서 모바일 애플리케이션을 설정합니다. 이렇게 하면 Adobe Mobile Services에서 수집한 데이터가 Adobe Campaign으로 전송되도록 할 수 있습니다. Adobe Mobile Services[에서 모바일 앱 구성을 참조하십시오.](#configuring-a-mobile-app-in-adobe-mobile-services)
1. 모바일 응용 프로그램의 특정 설정을 수행합니다.

   * Adobe Mobile Services 인터페이스에서 다운로드한 구성 파일을 모바일 응용 프로그램과 함께 패키징합니다.
   * Experience Cloud Mobile SDK를 모바일 애플리케이션에 통합합니다. [SDK를 모바일 응용 프로그램에 통합하기를 참조하십시오](#integrating-the-sdk-into-a-mobile-application).

1. Adobe Mobile Services 인터페이스에서 관심 영역을 정의합니다. [Adobe Mobile Services에 대한 관심 영역 정의](#defining-points-of-interest-in-adobe-mobile-services)를 참조하십시오.
1. 모바일 애플리케이션의 가입자로부터 수집할 데이터를 정의합니다. [가입자의 관심 영역 데이터 수집](#collecting-subscribers--points-of-interest-data)을 참조하십시오.
1. Adobe Campaign에서 모바일 응용 프로그램 및 수집된 위치 데이터에 액세스해야 합니다. 위치 데이터[ 및 ](#accessing-mobile-apps-used-to-collect-location-data)수집된 위치 데이터 액세스[를 참조하십시오.](#accessing-collected-location-data)

### SDK V4 {#setting-up-a-mobile-app-in-campaign}을 사용하여 Adobe Campaign에서 모바일 앱 설정

Adobe Campaign에서 관심 영역 데이터를 수집하려면 Adobe Campaign에서 데이터를 수신할 모바일 애플리케이션을 구성해야 합니다.

1. 왼쪽 상단 모서리에서 **[!UICONTROL Adobe Campaign]** 로고를 클릭한 다음 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile app]**&#x200B;을(를) 선택합니다.
1. **[!UICONTROL Create]**&#x200B;을 클릭하여 응용 프로그램을 설정합니다.
1. **[!UICONTROL Application name]** 필드에 이름을 입력하고 **[!UICONTROL Create]**&#x200B;을 클릭합니다.

   **[!UICONTROL Device-specific settings]** 섹션을 채우지 마십시오. 이는 푸시 알림을 수신하는 애플리케이션을 구성하는 경우에만 적용됩니다.

**[!UICONTROL Mobile application properties]** 섹션에서 두 개의 URL이 나열됩니다.**[!UICONTROL Collect PII endpoint]** 및 **[!UICONTROL Location Services endpoint]**. Adobe Mobile Services 인터페이스에서 사용됩니다. Adobe Mobile Services[에서 모바일 앱 구성을 참조하십시오.](#configuring-a-mobile-app-in-adobe-mobile-services)

* **[!UICONTROL Collect PII endpoint]** URL은 모바일 응용 프로그램이 시작될 때 사용자의 Experience Cloud ID 및 등록 토큰을 수집하는 데 사용됩니다. 사용자가 이메일, 이름, 성 등과 같은 자격 증명을 사용하여 응용 프로그램에 로그인하면 이 데이터도 수집되어 사용자의 등록 토큰을 Adobe Campaign 프로필과 조정하는 데 사용됩니다.
* **[!UICONTROL Location Services endpoint]** URL은 관심 지점에서 사용자의 위도, 경도 및 반경 등의 위치 데이터를 수집하는 데 사용됩니다.

이제 Adobe Mobile Services](#configuring-a-mobile-app-in-adobe-mobile-services) 섹션에서 [모바일 앱 구성에 설명된 대로 Adobe Mobile Services에서 이러한 값을 사용하여 구성을 완료할 수 있습니다.

![](assets/poi_mobile_app_properties.png)

### Adobe Mobile Services {#configuring-a-mobile-app-in-adobe-mobile-services}에서 V4 모바일 앱 구성

Adobe Mobile Services에서 수집한 데이터를 Adobe Campaign으로 전송하려면 Mobile Services 인터페이스에서 포스트백을 구성해야 합니다.

Adobe Campaign에 설정된 모바일 응용 프로그램 매개 변수에서 찾을 수 있는 특정 정보가 필요합니다([Campaign](#setting-up-a-mobile-app-in-campaign)에서 모바일 앱 설정 참조).

* **[!UICONTROL IMS Organization ID]**
* **[!UICONTROL Collect PII Endpoint]**
* **[!UICONTROL Location Services endpoint]**

다음 구성을 수행하려면 Adobe Analytics에 액세스할 수 있어야 합니다. Adobe Analytics 사용자가 아닌 경우 Adobe Campaign 관리자에게 문의하십시오.

1. [mobilemarketing.adobe.com](https://mobilemarketing.adobe.com/)에 로그인합니다.
1. 애플리케이션을 만들거나 기존 애플리케이션을 선택합니다.
1. **[!UICONTROL Manage App Settings]** 페이지로 이동합니다.
1. **방문자 ID 서비스** 섹션에서 **활성화**&#x200B;를 선택하고 드롭다운 목록에서 조직을 선택합니다. **저장**&#x200B;을 클릭합니다.

   >[!CAUTION]
   >
   >이 조직은 Adobe Campaign 인스턴스에서 사용하는 조직과 동일해야 합니다.

1. **[!UICONTROL Manage Postbacks]**&#x200B;을(를) 클릭합니다.
1. 포스트백을 만듭니다.

   * **[!UICONTROL Postback Type]**(으)로 **[!UICONTROL PII]**&#x200B;을 선택합니다.
   * **[!UICONTROL URL]** 필드에서 Adobe Campaign 인터페이스에서 구성한 모바일 응용 프로그램의 **[!UICONTROL Collect PII Endpoint]** URL을 복사한 후 서버 이름 앞에 추가합니다. [Campaign](#setting-up-a-mobile-app-in-campaign)에서 모바일 앱 설정을 참조하십시오.
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

   * **컨텐트 유형**&#x200B;을 **[!UICONTROL application/json]**&#x200B;으로 설정합니다.
   * **포스트백을 트리거하는 데이터 태그는 무엇입니까?**&#x200B;를 제외한 모든 이벤트(일반적으로  **[!UICONTROL Launched]** 및 **[!UICONTROL exists]**)를 선택합니다.
   * **[!UICONTROL Save & Activate]**&#x200B;을(를) 클릭합니다.

1. 두 번째 포스트백을 만듭니다.

   * **[!UICONTROL Postback Type]**(으)로 **[!UICONTROL Postback]**&#x200B;을 선택합니다.
   * **[!UICONTROL URL]** 필드에서 Adobe Campaign 인터페이스에서 구성한 모바일 응용 프로그램의 **[!UICONTROL Location Services Endpoint]** URL을 복사한 후 서버 이름 앞에 추가합니다. [Campaign](#setting-up-a-mobile-app-in-campaign)에서 모바일 앱 설정을 참조하십시오.
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

   * **컨텐트 유형**&#x200B;을 **[!UICONTROL application/json]**&#x200B;으로 설정합니다.
   * **포스트백을 트리거하는 데이터 태그는 무엇입니까?**&#x200B;를  **[!UICONTROL campaign.test]** 선택하고 를  **[!UICONTROL exists]**&#x200B;선택합니다.
   * **[!UICONTROL Save & Activate]**&#x200B;을(를) 클릭합니다.

>[!NOTE]
>
>포스트백 구성에 대한 자세한 내용은 [Adobe Mobile Services 설명서](https://docs.adobe.com/content/help/en/mobile-services/using/manage-app-settings-ug/configuring-app/signals.html)를 참조하십시오.

### SDK를 모바일 응용 프로그램 {#integrating-the-sdk-into-a-mobile-application}에 통합

Mobile 핵심 서비스의 SDK(소프트웨어 개발 키트)는 모바일 애플리케이션을 Adobe Campaign에 쉽게 통합합니다.

이 단계는 이 [페이지](https://helpx.adobe.com/kr/campaign/kb/configuring-app-sdkv4.html)에 설명되어 있습니다.

### Adobe Mobile Services에 대한 관심 영역 정의 {#defining-points-of-interest-in-adobe-mobile-services}

위치 데이터를 수집하는 데 사용되는 관심 영역을 정의하려면

1. Adobe Mobile Services 인터페이스로 이동합니다.
1. 애플리케이션을 추가합니다.

   Mobile Services에서 응용 프로그램을 관리하는 방법에 대한 자세한 내용은 [Adobe Mobile Services 설명서](https://docs.adobe.com/content/help/en/mobile-services/using/manage-apps-ug/t-new-app.html)를 참조하십시오.

1. 관심 영역을 정의합니다.

   관심 영역 관리에 대한 자세한 내용은 [Adobe Mobile Services 설명서](https://docs.adobe.com/content/help/en/mobile-services/using/location-ug/t-manage-points.html)를 참조하십시오.

### 가입자의 관심 영역 데이터 수집 중 {#collecting-subscribers--points-of-interest-data}

특정 사용자 지정 리소스를 사용하면 응용 프로그램의 구독자로부터 수집할 데이터를 정의할 수 있습니다.

이 단계는 [SDK V4](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html) 페이지를 사용하여 모바일 응용 프로그램 구성에 설명되어 있습니다.


## 위치 데이터를 수집하는 데 사용되는 모바일 앱에 액세스 {#accessing-mobile-apps-used-to-collect-location-data}

Adobe Campaign에서 성공적으로 만든 응용 프로그램에 액세스하려면:

1. 왼쪽 위 모서리에서 **[!UICONTROL Adobe Campaign]** 로고를 클릭합니다.
1. SDK에 따라 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile app (SDK v4)]** 또는 **[!UICONTROL Mobile app (AEP SDK)]**&#x200B;을 선택합니다.
1. 목록에서 모바일 애플리케이션을 선택하여 속성을 표시합니다.

   ![](assets/poi_mobile_app_subscribers.png)

응용 프로그램의 구독자 목록도 **[!UICONTROL Mobile application subscribers]** 탭에 표시됩니다. 구독자는 모바일 장치에 응용 프로그램을 설치한 모든 사용자입니다. Adobe Campaign 데이터베이스 프로필은 등록 토큰으로 식별됩니다.

## 수집된 위치 데이터 {#accessing-collected-location-data} 액세스

설정이 완료되면 수집된 관심 영역 데이터가 각 프로필의 **[!UICONTROL Places]** 탭에 나열됩니다. 목록에 액세스하려면:

1. 프로필을 선택합니다.
1. 오른쪽에 있는 **[!UICONTROL Edit profile properties]** 단추를 클릭합니다.
1. **[!UICONTROL Places]** 탭을 선택합니다. 

   ![](assets/poi_profile_places.png)

현재 프로필에 대해 수집된 관심 영역 데이터가 나열됩니다. 위치 데이터는 6개월 동안 Adobe Campaign 데이터베이스에 저장됩니다.

프로필 액세스 및 편집에 대한 자세한 내용은 [프로필](../../audiences/using/about-profiles.md)을 참조하십시오.
