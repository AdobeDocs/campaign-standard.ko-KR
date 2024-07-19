---
title: Campaign-Points of Interest 데이터 통합 구성
description: Adobe Campaign에서 관심 영역 데이터 기능을 구성하여 구독자의 위치에 따라 개인화된 메시지를 보내는 방법을 알아봅니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-analytics-for-mobile
feature: Audiences
role: Data Architect
level: Intermediate
exl-id: b097b3fa-f949-446e-ad44-cc6ca025ee55
source-git-commit: 6b683ccd93e10f78ff643eed9f374a794c085cb1
workflow-type: tm+mt
source-wordcount: '1252'
ht-degree: 1%

---

# Campaign-Points of Interest 데이터 통합 구성{#configuring-campaign-points-of-interest-data-integration}

## Adobe Experience Platform SDK와 Campaign-Points of Interest 데이터 통합 구성 {#configuring-campaign-poi-aep-sdk}

>[!NOTE]
>
>모바일 애플리케이션은 이미 Adobe Experience Platform SDK를 사용하여 Adobe Campaign Standard에 구성되어야 합니다. 자세한 단계는 이 [페이지](https://helpx.adobe.com/kr/campaign/kb/configuring-app-sdk.html)를 참조하세요.

위치 데이터를 수집하는 데 사용되는 모바일 응용 프로그램은 Adobe Campaign 인터페이스에서 **관리자**&#x200B;가 구성해야 합니다.

Adobe Experience Platform SDK로 구성된 모바일 애플리케이션에서 Adobe Experience Platform 위치 서비스를 사용하려면 다음을 수행해야 합니다.

1. 데이터 수집 UI에서 모바일 앱 구성에 **[!UICONTROL Places]** 확장을 추가합니다. Adobe Campaign에서 모바일 애플리케이션을 설정합니다. [위치 확장 설치](https://developer.adobe.com/client-sdks/solution/places)를 참조하십시오.

1. 확장이 설정되면 데이터 수집 UI 내에서 데이터 요소를 만들어 이러한 확장에서 데이터를 검색합니다. 이 [페이지](https://helpx.adobe.com/campaign/kb/config-app-in-launch.html#Step1Createdataelements)를 참조하여 데이터 요소를 만드십시오.

1. 그런 다음 데이터 수집 UI에서 관심 포인트와 Adobe Campaign 간 모바일 사용 사례를 지원하는 규칙을 만들어야 합니다.\
   이 규칙은 사용자가 지역 기반 **[!UICONTROL Point of Interest]**&#x200B;을(를) 입력할 때 트리거됩니다. 규칙을 만들려면 이 [페이지](https://helpx.adobe.com/campaign/kb/config-app-in-launch.html#Locationpostback)를 참조하세요.

1. 위치에 **[!UICONTROL Points of Interest]**&#x200B;을(를) 정의합니다. [관심 영역 만들기](https://experienceleague.adobe.com/docs/places/using/poi-mgmt-ui/create-a-poi-ui.html)를 참조하세요.

1. Adobe Campaign에서 모바일 애플리케이션 및 수집된 위치 데이터에 액세스해야 합니다. [위치 데이터를 수집하는 데 사용되는 모바일 앱에 액세스](#accessing-mobile-apps-used-to-collect-location-data) 및 [수집된 위치 데이터에 액세스](#accessing-collected-location-data)를 참조하십시오.

## SDK V4를 사용하여 Campaign-Points of Interest 데이터 통합 구성 {#configuring-campaign-poi-sdkv4}

위치 데이터를 수집하는 데 사용되는 모바일 응용 프로그램은 Adobe Campaign 인터페이스에서 **관리자**&#x200B;가 구성해야 합니다.

SDK V4로 구성된 모바일 애플리케이션에 관심 영역 데이터 기능을 사용하려면 다음을 수행해야 합니다.

1. Adobe Analytics for Mobile에 액세스할 수 있습니다. 자세한 내용은 라이선스 계약을 확인하거나 Adobe 계정 담당자에게 문의하십시오.
1. Adobe Campaign에서 모바일 애플리케이션을 설정합니다. [Campaign에서 모바일 앱 설정](#setting-up-a-mobile-app-in-campaign)을 참조하세요.
1. Adobe Mobile Services 인터페이스에서 모바일 애플리케이션을 설정합니다. 이렇게 하면 Adobe Mobile Services에서 수집한 데이터를 Adobe Campaign으로 보낼 수 있습니다. [Adobe Mobile Services에서 모바일 앱 구성](#configuring-a-mobile-app-in-adobe-mobile-services)을 참조하십시오.
1. 모바일 애플리케이션의 특정 설정을 수행합니다.

   * Adobe Mobile Services 인터페이스에서 다운로드한 구성 파일을 모바일 애플리케이션과 패키징합니다.
   * Experience Cloud Mobile SDK를 모바일 애플리케이션에 통합합니다. [모바일 애플리케이션에 SDK 통합](#integrating-the-sdk-into-a-mobile-application)을 참조하십시오.

1. Adobe Mobile Services 인터페이스에서 관심 영역을 정의합니다. [Adobe Mobile Services의 관심 영역 정의](#defining-points-of-interest-in-adobe-mobile-services)를 참조하세요.
1. 모바일 애플리케이션의 구독자로부터 수집하려는 데이터를 정의합니다. [구독자의 관심 영역 데이터 수집](#collecting-subscribers--points-of-interest-data)을 참조하세요.
1. Adobe Campaign에서 모바일 애플리케이션 및 수집된 위치 데이터에 액세스해야 합니다. [위치 데이터를 수집하는 데 사용되는 모바일 앱에 액세스](#accessing-mobile-apps-used-to-collect-location-data) 및 [수집된 위치 데이터에 액세스](#accessing-collected-location-data)를 참조하십시오.

### SDK V4를 사용하여 Adobe Campaign에서 모바일 앱 설정 {#setting-up-a-mobile-app-in-campaign}

Adobe Campaign을 사용하여 관심 영역 데이터를 수집하려면 Adobe Campaign에서 데이터를 수신할 모바일 애플리케이션을 구성해야 합니다.

1. 왼쪽 상단 모서리에서 **Adobe** 로고를 클릭한 다음 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile app]**&#x200B;을(를) 선택합니다.
1. 응용 프로그램을 설정하려면 **[!UICONTROL Create]**&#x200B;을(를) 클릭하십시오.
1. **[!UICONTROL Application name]** 필드에 이름을 입력하고 **[!UICONTROL Create]**&#x200B;을(를) 클릭합니다.

   **[!UICONTROL Device-specific settings]** 섹션을 채우지 마십시오. 푸시 알림을 수신하는 애플리케이션 구성에만 적용됩니다.

**[!UICONTROL Mobile application properties]** 섹션에는 **[!UICONTROL Collect PII endpoint]** 및 **[!UICONTROL Location Services endpoint]** URL이 두 개 나열됩니다. Adobe Mobile Services 인터페이스에서 사용됩니다. [Adobe Mobile Services에서 모바일 앱 구성](#configuring-a-mobile-app-in-adobe-mobile-services)을 참조하십시오.

* **[!UICONTROL Collect PII endpoint]** URL은 시작할 때 모바일 애플리케이션에서 사용자의 Experience Cloud ID와 등록 토큰을 수집하는 데 사용됩니다. 사용자가 이메일, 이름, 성 등의 자격 증명을 사용하여 애플리케이션에 로그인할 때 이 데이터도 수집되어 사용자의 등록 토큰을 Adobe Campaign 프로필과 조정하는 데 사용됩니다.
* **[!UICONTROL Location Services endpoint]** URL은 관심 영역에서 사용자의 위도, 경도 및 반경과 같은 위치 데이터를 수집하는 데 사용됩니다.

이제 [Adobe Mobile Services에서 모바일 앱 구성](#configuring-a-mobile-app-in-adobe-mobile-services) 섹션에 설명된 대로 Adobe Mobile Services에서 이러한 값을 사용하여 구성을 완료할 수 있습니다.

![](assets/poi_mobile_app_properties.png)

### Adobe Mobile Services에서 V4 모바일 앱 구성 {#configuring-a-mobile-app-in-adobe-mobile-services}

Adobe Mobile Services에서 수집한 데이터를 Adobe Campaign으로 보내려면 Mobile Services 인터페이스에서 포스트백을 구성해야 합니다.

Adobe Campaign에 설정된 모바일 애플리케이션 매개 변수에서 찾을 수 있는 특정 정보가 필요합니다([Campaign에서 모바일 앱 설정](#setting-up-a-mobile-app-in-campaign) 참조).

* **[!UICONTROL IMS Organization ID]**
* **[!UICONTROL Collect PII Endpoint]**
* **[!UICONTROL Location Services endpoint]**

다음 구성을 수행하려면 Adobe Analytics에 대한 액세스 권한이 있어야 합니다. Adobe Analytics 사용자가 아닌 경우 Adobe Campaign 관리자에게 문의하십시오.

1. [mobilemarketing.adobe.com](https://mobilemarketing.adobe.com/)에 로그인합니다.
1. 응용 프로그램을 만들거나 기존 응용 프로그램을 선택합니다.
1. **[!UICONTROL Manage App Settings]** 페이지로 이동합니다.
1. **방문자 ID 서비스** 섹션에서 **활성화**&#x200B;를 선택하고 드롭다운 목록에서 조직을 선택합니다. **저장**&#x200B;을 클릭합니다.

   >[!CAUTION]
   >
   >이 조직은 Adobe Campaign 인스턴스에서 사용하는 조직과 동일해야 합니다.

1. **[!UICONTROL Manage Postbacks]**&#x200B;를 클릭합니다.
1. 포스트백을 만듭니다.

   * **[!UICONTROL PII]**&#x200B;을(를) **[!UICONTROL Postback Type]**(으)로 선택합니다.
   * **[!UICONTROL URL]** 필드에서 Adobe Campaign 인터페이스에서 구성한 모바일 응용 프로그램의 **[!UICONTROL Collect PII Endpoint]** URL을 서버 이름 앞에 복사합니다. [Campaign에서 모바일 앱 설정](#setting-up-a-mobile-app-in-campaign)을 참조하세요.
   * 다음과 같이 **[!UICONTROL Post Body]** 필드를 채웁니다.

     iOS의 경우

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

     Android의 경우

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

   * **콘텐츠 형식**&#x200B;을(를) **[!UICONTROL application/json]**(으)로 설정합니다.
   * **에서 포스트백을 트리거하는 데이터 태그는 무엇입니까?**, 모든 이벤트를 선택합니다(일반적으로 **[!UICONTROL Launched]** 및 **[!UICONTROL exists]**).
   * **[!UICONTROL Save & Activate]**&#x200B;를 클릭합니다.

1. 두 번째 포스트백을 만듭니다.

   * **[!UICONTROL Postback]**&#x200B;을(를) **[!UICONTROL Postback Type]**(으)로 선택합니다.
   * **[!UICONTROL URL]** 필드에서 Adobe Campaign 인터페이스에서 구성한 모바일 응용 프로그램의 **[!UICONTROL Location Services Endpoint]** URL을 서버 이름 앞에 복사합니다. [Campaign에서 모바일 앱 설정](#setting-up-a-mobile-app-in-campaign)을 참조하세요.
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

   * **콘텐츠 형식**&#x200B;을(를) **[!UICONTROL application/json]**(으)로 설정합니다.
   * **에서 포스트백을 트리거하는 데이터 태그는 무엇입니까?**, **[!UICONTROL campaign.test]** 및 **[!UICONTROL exists]**&#x200B;을(를) 선택하십시오.
   * **[!UICONTROL Save & Activate]**&#x200B;를 클릭합니다.

>[!NOTE]
>
>포스트백 구성에 대한 자세한 내용은 [Adobe Mobile Services 문서](https://experienceleague.adobe.com/docs/mobile-services/using/manage-app-settings-ug/configuring-app/signals.html)를 참조하세요.

### 모바일 애플리케이션에 SDK 통합 {#integrating-the-sdk-into-a-mobile-application}

Mobile Core Service의 SDK(소프트웨어 개발 키트)를 사용하면 모바일 애플리케이션을 Adobe Campaign에 쉽게 통합할 수 있습니다.

이 단계는 이 [페이지](https://helpx.adobe.com/kr/campaign/kb/configuring-app-sdkv4.html)에 설명되어 있습니다.

### Adobe Mobile Services의 관심 영역 정의 {#defining-points-of-interest-in-adobe-mobile-services}

위치 데이터를 수집하는 데 사용되는 관심 영역을 정의하려면 다음을 수행합니다.

1. Adobe Mobile Services 인터페이스로 이동합니다.
1. 애플리케이션을 추가합니다.

   Mobile Services에서 응용 프로그램을 관리하는 방법에 대한 자세한 내용은 [Mobile Services Adobe](https://experienceleague.adobe.com/docs/mobile-services/using/manage-apps-ug/t-new-app.html)을 참조하세요.

1. 관심 영역을 정의합니다.

   관심 영역 관리에 대한 자세한 내용은 [Adobe Mobile Services 설명서](https://experienceleague.adobe.com/docs/mobile-services/using/location-ug/t-manage-points.html)를 참조하세요.

### 구독자의 관심 영역 데이터 수집 {#collecting-subscribers--points-of-interest-data}

특정 사용자 지정 리소스를 사용하면 애플리케이션 구독자로부터 수집하려는 데이터를 정의할 수 있습니다.

이 단계는 [SDK를 사용하여 모바일 애플리케이션 구성](https://helpx.adobe.com/kr/campaign/kb/configuring-app-sdkv4.html) 페이지에 설명되어 있습니다.

## 위치 데이터 수집에 사용되는 모바일 앱에 액세스 {#accessing-mobile-apps-used-to-collect-location-data}

Adobe Campaign에서 성공적으로 생성된 애플리케이션에 액세스하려면 다음을 수행하십시오.

1. 왼쪽 상단 모서리에서 **Adobe** 로고를 클릭합니다.
1. SDK에 따라 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile app (SDK v4)]** 또는 **[!UICONTROL Mobile app (AEP SDK)]**&#x200B;을(를) 선택합니다.
1. 목록에서 모바일 애플리케이션을 선택하여 해당 속성을 표시합니다.

   ![](assets/poi_mobile_app_subscribers.png)

응용 프로그램의 구독자 목록도 **[!UICONTROL Mobile application subscribers]** 탭에 표시됩니다. 구독자는 모바일 장치에 애플리케이션을 설치한 모든 사용자입니다. Adobe Campaign 데이터베이스 프로필은 등록 토큰으로 식별됩니다.

## 수집된 위치 데이터 액세스 {#accessing-collected-location-data}

설정이 완료되면 수집된 관심 영역 데이터가 각 프로필의 **[!UICONTROL Places]** 탭에 나열됩니다. 목록에 액세스하려면:

1. 프로필을 선택합니다.
1. 오른쪽의 **[!UICONTROL Edit profile properties]** 단추를 클릭합니다.
1. **[!UICONTROL Places]** 탭을 선택합니다. 

   ![](assets/poi_profile_places.png)

현재 프로필에 대해 수집된 관심 영역 데이터가 나열됩니다. 위치 데이터는 6개월 동안 Adobe Campaign 데이터베이스에 저장됩니다.

프로필 액세스 및 편집에 대한 자세한 내용은 [프로필](../../audiences/using/about-profiles.md)을 참조하세요.
