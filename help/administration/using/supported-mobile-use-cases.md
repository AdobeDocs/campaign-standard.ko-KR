---
title: Adobe Experience Platform SDK를 사용하여 Adobe Campaign Standard에서 지원하는 모바일 사용 사례
description: 모바일 사용 사례를 지원하는 방법 알아보기
audience: channels
feature: Instance Settings
role: Admin
level: Experienced
exl-id: 3cd8d756-a271-4e53-8ed0-984ce20298bc
source-git-commit: 597ece8d833a216f0540f801461b08fdc9865024
workflow-type: tm+mt
source-wordcount: '852'
ht-degree: 0%

---

# Adobe Campaign Standard에서 지원하는 모바일 사용 사례 {#mobile-use-cases}

이 페이지에서는 [!DNL Adobe Experience Platform SDKs]을(를) 사용하여 [!DNL Adobe Campaign Standard]에서 지원되는 모든 모바일 사용 사례 목록을 확인할 수 있습니다. 이러한 사용 사례를 지원하려면 [!DNL Adobe Experience Platform SDKs], [!DNL tags in Adobe Experience Platform] 및 [!DNL Adobe Campaign Standard]을(를) 설치하고 구성해야 합니다. 자세한 내용은 이 [페이지](../../administration/using/configuring-a-mobile-application.md)를 참조하세요.

Adobe Campaign Standard은 다음과 같은 사용 사례를 지원합니다.

* [Campaign Standard에서 모바일 프로필 등록](../../administration/using/supported-mobile-use-cases.md#register-mobile-profile)
* [푸시 토큰을 Campaign Standard으로 보내기](../../administration/using/supported-mobile-use-cases.md#send-push-token)
* [애플리케이션의 사용자 정의 데이터로 모바일 프로필 강화](../../administration/using/supported-mobile-use-cases.md#enrich-mobile-profile-custom)
* [애플리케이션의 라이프사이클 데이터를 사용하여 모바일 프로필 강화](../../administration/using/supported-mobile-use-cases.md#enrich-mobile-profile-lifecycle)
* [푸시 알림과 사용자 상호 작용 추적](../../administration/using/supported-mobile-use-cases.md#track-user-push)
* [모바일 앱에서 사용자 지정 이벤트를 구현하여 인앱 메시지 트리거](../../administration/using/supported-mobile-use-cases.md#custom-event-inapp)
* [인앱 메시지를 기반으로 하는 프로필 템플릿에 대한 추가 인증을 위한 링크 필드 설정](../../administration/using/supported-mobile-use-cases.md#linkage-fields-inapp)

이러한 사용 사례를 구성하려면 다음 확장이 필요합니다.

* **[!DNL Adobe Campaign Standard]** <br>Campaign Standard 확장을 설치하고 구성하려면 [데이터 수집 UI에서 Campaign Standard 확장 구성](https://developer.adobe.com/client-sdks/documentation/adobe-campaign-standard/#configure-the-campaign-standard-extension)을 참조하십시오.
* **[!DNL Mobile Core]**(자동으로 설치됨) <br>Mobile Core 확장에 대한 자세한 내용은 [Mobile Core](https://developer.adobe.com/client-sdks/documentation/mobile-core/)를 참조하십시오.
* **[!DNL Profile]**(자동으로 설치됨) <br>프로필 확장에 대한 자세한 내용은 [프로필](https://developer.adobe.com/client-sdks/documentation/profile/)을 참조하세요.

## Campaign Standard에서 모바일 프로필 등록 {#register-mobile-profile}

### iOS 사용 {#register-mobile-profile-ios}

iOS에서 다음 [!DNL Experience Platform APIs]이(가) 필요합니다.

* **[!UICONTROL Lifecycle Start]** 앱이 시작되고 앱이 포그라운드에 있을 때.
* 백그라운드에 앱이 있을 때 **[!UICONTROL Lifecycle Pause]**.

자세한 내용은 [iOS의 라이프사이클 확장](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/ios/)을 참조하십시오.

다음은 iOS에 대한 이 사용 사례의 샘플 구현입니다.

```
 func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?) -> Bool {
  
  
 ACPCore.setLogLevel(.debug)
 appId = SettingsBundle.getLaunchAppId()
   
 //===== START Set up Adobe SDK =====
 ACPCore.configure(withAppId: appId)
   
 ACPCampaign.registerExtension()
 ACPIdentity.registerExtension()
 ACPLifecycle.registerExtension()
 ACPUserProfile.registerExtension()
 ACPSignal.registerExtension()
 ACPCore.start()
 ACPCore.lifecycleStart(nil)
   
 return true
 }
  
func applicationDidEnterBackground(_ application: UIApplication) {
 ACPCore.lifecyclePause()
 }
   
 func applicationDidBecomeActive(_ application: UIApplication) {
 // Workaround until jira AMSDK-7411 is fixed.
 sleep(2)
 ACPCore.lifecycleStart(nil)
 }
```

### Android 사용 {#register-mobile-profile-android}

Android에서 다음 [!DNL Experience Platform APIs]이(가) 필요합니다.

* **[!UICONTROL OnResume]**
* **[!UICONTROL OnPause]**

자세한 내용은 [Android의 라이프사이클 확장](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/android/)을 참조하십시오.

다음은 Android의 이 사용 사례에 대한 샘플 구현입니다.

```
@Override
  
public void onResume() {
 super.onResume();
 MobileCore.setApplication(getApplication());
 MobileCore.lifecycleStart(null);
 handleOpenTracking();
 }
  
 @Override
 public void onPause() {
 super.onPause();
 MobileCore.lifecyclePause();
 }
```

## 푸시 토큰을 Adobe Campaign Standard으로 보내기 {#send-push-token}

### iOS 사용 {#send-push-token-ios}

iOS에서 다음 [!DNL Experience Platform SDK]이(가) 필요합니다.

* **[!UICONTROL setPushIdentifier]** <br>자세한 내용은 [setPushIdentifier](https://developer.adobe.com/client-sdks/documentation/adobe-campaign-standard/api-reference/)를 참조하십시오.

다음은 iOS의 이 사용 사례에 대한 샘플 구현입니다.

```
func application(_ application: UIApplication, didRegisterForRemoteNotificationsWithDeviceToken deviceToken: Data) {
  
 // Register Device Token
 ACPCore.setPushIdentifier(deviceToken)
```

### Android 사용 {#send-push-token-android}

Android에서 다음 [!DNL Experience Platform SDK]이(가) 필요합니다.

* **[!UICONTROL setPushIdentifier]** <br>자세한 내용은 [setPushIdentifier](https://developer.adobe.com/client-sdks/documentation/adobe-campaign-standard/api-reference/)를 참조하십시오.

다음은 Android의 이 사용 사례에 대한 샘플 구현입니다.

```
@Override
public void onNewToken(String token) {
    Log.d(TAG, "Refreshed token: " + token);
    MobileCore.setPushIdentifier(token);
}
```

## 애플리케이션의 사용자 정의 데이터로 모바일 프로필 강화 {#enrich-mobile-profile-custom}

이 사용 사례가 작동하려면 PII 포스트백에 대한 규칙을 만들어야 합니다. 자세한 내용은 [PII 포스트백](../../administration/using/configuring-rules-launch.md#pii-postback)을 참조하세요.

### iOS 사용 {#enrich-mobile-profile-custom-ios}

iOS에서 다음 [!DNL Experience Platform API]이(가) 필요합니다.

* collectPII <br> 자세한 내용은 collectPII를 참조하십시오.

다음은 iOS에 대한 이 사용 사례의 샘플 구현입니다.

```
ACPCore.collectPii(["pushPlatform":"apns", "email":email, "firstName":firstName, "lastName":lastName])
```

### Android 사용 {#enrich-mobile-profile-custom-android}

Android에서 다음 [!DNL Experience Platform API]이(가) 필요합니다.

* collectPII <br> 자세한 내용은 collectPII를 참조하십시오.

다음은 Android의 이 사용 사례에 대한 샘플 구현입니다.

```
HashMap<String, String> data = new HashMap<>();
data.put("pushPlatform", "gcm");
data.put("firstName", firstNameText); 
data.put("lastName", lastNameText); 
data.put("email", emailText); 
MobileCore.collectPii(data);
```

## 애플리케이션의 라이프사이클 데이터를 사용하여 모바일 프로필 강화 {#enrich-mobile-profile-lifecycle}

이 사용 사례가 작동하려면 PII 포스트백에 대한 규칙을 만들어야 합니다. 자세한 내용은 [PII 포스트백](../../administration/using/configuring-rules-launch.md#pii-postback)을 참조하세요.

>[!NOTE]
>
>Adobe Campaign은 모바일 앱에서 사용자 지정 데이터 또는 라이프사이클 데이터를 구분하지 않습니다. 두 유형의 데이터는 모바일 앱의 이벤트에 대한 응답으로 collectPii 포스트백 규칙을 사용하여 서버로 전송할 수 있습니다.

### iOS 사용 {#enrich-mobile-profile-lifecycle-ios}

iOS에서 다음 [!DNL Experience Platform APIs]이(가) 필요합니다.

* **[!UICONTROL Lifecycle Start]** 앱이 시작되고 앱이 포그라운드에 있을 때.
* 백그라운드에 앱이 있을 때 **[!UICONTROL Lifecycle Pause]**.

자세한 내용은 [iOS의 라이프사이클 확장](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/ios/)을 참조하십시오.

다음은 iOS에 대한 이 사용 사례의 샘플 구현입니다.

```
func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?) -> Bool {
  
  
 ACPCore.setLogLevel(.debug)
 appId = SettingsBundle.getLaunchAppId()
   
 //===== START Set up Adobe SDK =====
 ACPCore.configure(withAppId: appId)
   
 ACPCampaign.registerExtension()
 ACPIdentity.registerExtension()
 ACPLifecycle.registerExtension()
 ACPUserProfile.registerExtension()
 ACPSignal.registerExtension()
 ACPCore.start()
 ACPCore.lifecycleStart(nil)
   
 return true
 }
  
func applicationDidEnterBackground(_ application: UIApplication) {
 ACPCore.lifecyclePause()
 }
   
 func applicationDidBecomeActive(_ application: UIApplication) {
 // Workaround until jira AMSDK-7411 is fixed.
 sleep(2)
 ACPCore.lifecycleStart(nil)
 }
```

### Android 사용 {#enrich-mobile-profile-lifecycle-android}

Android에서 다음 [!DNL Experience Platform APIs]이(가) 필요합니다.

* **[!UICONTROL OnResume]**
* **[!UICONTROL OnPause]**

자세한 내용은 [Android의 라이프사이클 확장](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/android/)을 참조하십시오.

다음은 Android의 이 사용 사례에 대한 샘플 구현입니다.

```
@Override
  
public void onResume() {
 super.onResume();
 MobileCore.setApplication(getApplication());
 MobileCore.lifecycleStart(null);
 handleOpenTracking();
 }
  
 @Override
 public void onPause() {
 super.onPause();
 MobileCore.lifecyclePause();
 }
```

## 푸시 알림과 사용자 상호 작용 추적 {#track-user-push}

푸시 알림 추적 포스트백에 대한 규칙을 만들어야 합니다. 자세한 내용은 [푸시 알림 추적 포스트백](../../administration/using/configuring-rules-launch.md#push-tracking-postback)을 참조하세요.

### iOS 사용 {#track-user-push-ios}

iOS에서 다음 [!DNL Experience Platform SDK]이(가) 필요합니다.

* **[!UICONTROL trackAction]**. 자세한 내용은 [앱 작업 추적](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackaction)을 참조하세요.

다음은 iOS에 대한 이 사용 사례의 샘플 구현입니다.

```
let deliveryId = userInfo["_dId"] as? String
let broadlogId = userInfo["_mId"] as? String
if (deliveryId != nil && broadlogId != nil) {
    ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
}
```

### Android 사용 {#track-user-push-android}

Android에서 다음 [!DNL Experience Platform SDK]이(가) 필요합니다.

* **[!UICONTROL trackAction]**
자세한 내용은 [앱 작업 추적](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackaction)을 참조하십시오.

다음은 Android의 이 사용 사례에 대한 샘플 구현입니다.

```
contextData.put("deliveryId", deliveryId);
contextData.put("broadlogId", messageId);
contextData.put("action", "2");
MobileCore.trackAction("tracking", contextData);
```

## 인앱 메시지를 트리거하기 위해 애플리케이션에서 사용자 지정 이벤트 구현 {#custom-event-inapp}

### iOS 사용 {#custom-event-inapp-ios}

iOS에서 다음 [!DNL Experience Platform SDK]이(가) 필요합니다.

* **[!UICONTROL trackAction]**. 자세한 내용은 [앱 작업 추적](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackaction)을 참조하세요.

다음은 iOS에 대한 이 사용 사례의 샘플 구현입니다.

```
ACPCore.trackAction(mobileEventName, data: [:] )
```

### Android 사용 {#custom-event-inapp-android}

Android에서 다음 [!DNL Experience Platform SDK]이(가) 필요합니다.

* **[!UICONTROL trackAction]**
자세한 내용은 [앱 작업 추적](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackaction)을 참조하십시오.

다음은 Android의 이 사용 사례에 대한 샘플 구현입니다.

```
MobileCore.trackAction(mobileEventText, new HashMap<String,String>());
```

## 추가 인증을 위한 연계 필드 설정 {#linkage-fields-inapp}

### iOS 사용 {#linkage-fields-inapp-ios}

iOS에서 인앱 메시지를 기반으로 하는 프로필 템플릿에 대한 추가 인증을 위해 연결 필드를 설정하려면 다음 [!DNL Experience Platform SDK]이(가) 필요합니다.

* 연결 필드 설정 <br>자세한 내용은 [연결 필드 설정](https://developer.adobe.com/client-sdks/documentation/adobe-campaign-standard/api-reference/#setlinkagefields)을 참조하십시오.
* 연결 필드 재설정 <br>자세한 내용은 [연결 필드 재설정](https://developer.adobe.com/client-sdks/documentation/adobe-campaign-standard/api-reference/#setlinkagefields)을 참조하세요.

다음은 iOS과 관련된 이 사용 사례의 샘플 구현입니다.

연계 필드를 설정하려면 다음을 수행합니다.

```
var linkageFields = [String: String]()
linkageFields["cusEmail"] = "john.doe@email.com"
ACPCampaign.setLinkageFields(linkageFields)
```

링크 필드를 재설정하려면 다음을 수행하십시오.

```
ACPCampaign.resetLinkageFields(linkageFields)
```

### Android 사용 {#linkage-fields-inapp-android}

Android의 인앱 메시지를 기반으로 하는 프로필 템플릿에 대한 추가 인증을 위해 연결 필드를 설정하려면 다음 Experience Platform SDK가 필요합니다.

* 연결 필드 설정 <br>자세한 내용은 [연결 필드 설정](https://developer.adobe.com/client-sdks/documentation/adobe-campaign-standard/api-reference/#setlinkagefields)을 참조하십시오.
* 연결 필드 재설정 <br>자세한 내용은 [연결 필드 재설정](https://developer.adobe.com/client-sdks/documentation/adobe-campaign-standard/api-reference/#resetlinkagefields)을 참조하세요.

다음은 Android과 관련된 이 사용 사례의 샘플 구현입니다.

연계 필드를 설정하려면 다음을 수행합니다.

```
HashMap<String, String> linkageFields = new HashMap<String, String>();
linkageFields.put("cusEmail", "john.doe@email.com");
Campaign.setLinkageFields(linkageFields);
```

링크 필드를 재설정하려면 다음을 수행하십시오.

```
Campaign.resetLinkageFields()
```
