---
title: Adobe Experience Platform SDK를 사용하여 Adobe Campaign Standard에서 지원되는 모바일 사용 사례
description: 모바일 사용 사례를 지원하는 방법을 알아봅니다
audience: channels
feature: Instance Settings
role: Admin
level: Experienced
exl-id: 3cd8d756-a271-4e53-8ed0-984ce20298bc
source-git-commit: 7767b39a48502f97e2b3af9d21a3f49b9283ab2e
workflow-type: tm+mt
source-wordcount: '949'
ht-degree: 0%

---

# Adobe Campaign Standard에서 지원하는 모바일 사용 사례 {#mobile-use-cases}

이 페이지에서는에서 지원되는 모든 모바일 사용 사례 목록을 찾을 수 있습니다. [!DNL Adobe Campaign Standard] 사용 [!DNL Adobe Experience Platform SDKs]. 이러한 사용 사례를 지원하는 데 설치 및 구성이 포함됩니다 [!DNL Adobe Experience Platform SDKs], [!DNL tags in Adobe Experience Platform], 및 [!DNL Adobe Campaign Standard]. 자세한 내용은 다음을 참조하십시오 [페이지](../../administration/using/configuring-a-mobile-application.md).

Adobe Campaign Standard은 다음 사용 사례를 지원합니다.

* [Campaign Standard에 모바일 프로필 등록](../../administration/using/supported-mobile-use-cases.md#register-mobile-profile)
* [Campaign Standard에 푸시 토큰 보내기](../../administration/using/supported-mobile-use-cases.md#send-push-token)
* [애플리케이션의 사용자 지정 데이터로 모바일 프로필 보강](../../administration/using/supported-mobile-use-cases.md#enrich-mobile-profile-custom)
* [애플리케이션의 라이프사이클 데이터를 사용하여 모바일 프로필을 보강합니다](../../administration/using/supported-mobile-use-cases.md#enrich-mobile-profile-lifecycle)
* [푸시 알림과의 사용자 상호 작용 추적](../../administration/using/supported-mobile-use-cases.md#track-user-push)
* [모바일 앱에서 사용자 지정 이벤트를 구현하여 인앱 메시지를 트리거합니다](../../administration/using/supported-mobile-use-cases.md#custom-event-inapp)
* [인앱 메시지를 기반으로 하는 프로필 템플릿에 대한 추가 인증을 위한 링크 필드 설정](../../administration/using/supported-mobile-use-cases.md#linkage-fields-inapp)

이러한 사용 사례를 구성하려면 다음 확장이 필요합니다.

* **[!DNL Adobe Campaign Standard]** <br>Campaign Standard 확장을 설치하고 구성하려면 다음을 참조하십시오 [데이터 수집 UI에서 Campaign Standard 확장 구성](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard#configure-the-campaign-standard-extension-in-experience-platform-launch).
* **[!DNL Mobile Core]**: 자동으로 설치됩니다. <br>Mobile Core 확장에 대한 자세한 내용은 다음을 참조하십시오. [Mobile Core](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core).
* **[!DNL Profile]**: 자동으로 설치됩니다. <br>프로필 확장에 대한 자세한 내용은 [프로필](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/profile).

## Campaign Standard에 모바일 프로필 등록 {#register-mobile-profile}

### iOS 사용 {#register-mobile-profile-ios}

iOS에서 다음을 수행합니다 [!DNL Experience Platform APIs] 필수 여부:

* **[!UICONTROL Lifecycle Start]**: 앱이 시작될 때와 앱이 포그라운드에 있을 때 이 문제가 발생합니다.
* **[!UICONTROL Lifecycle Pause]**: 앱이 백그라운드에 있을 때.

자세한 내용은 [iOS의 라이프사이클 확장](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle/lifecycle-extension-in-ios).

다음은 iOS에서 이 사용 사례를 구현하는 샘플입니다.

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

### Android에서 {#register-mobile-profile-android}

Android에서 다음을 수행합니다 [!DNL Experience Platform APIs] 필수 여부:

* **[!UICONTROL OnResume]**
* **[!UICONTROL OnPause]**

자세한 내용은 [Android의 라이프사이클 확장](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle/lifecycle-extension-in-android).

다음은 Android에서 이 사용 사례를 위한 샘플 구현입니다.

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

## Adobe Campaign Standard에 푸시 토큰 보내기 {#send-push-token}

### iOS 사용 {#send-push-token-ios}

iOS에서 다음을 수행합니다 [!DNL Experience Platform SDK] 필수 여부:

* **[!UICONTROL setPushIdentifier]** <br>자세한 내용은 [setPushIdentifier](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard/adobe-campaign-standard-api-reference#setpushidentifier).

다음은 iOS의 이 사용 사례에 대한 샘플 구현입니다.

```
func application(_ application: UIApplication, didRegisterForRemoteNotificationsWithDeviceToken deviceToken: Data) {
  
 // Register Device Token
 ACPCore.setPushIdentifier(deviceToken)
```

### Android에서 {#send-push-token-android}

Android에서 다음을 수행합니다 [!DNL Experience Platform SDK] 필수 여부:

* **[!UICONTROL setPushIdentifier]** <br>자세한 내용은 [setPushIdentifier](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard/adobe-campaign-standard-api-reference#setpushidentifier).

다음은 Android에서 이 사용 사례에 대한 샘플 구현입니다.

```
@Override
public void onNewToken(String token) {
    Log.d(TAG, "Refreshed token: " + token);
    MobileCore.setPushIdentifier(token);
}
```

## 애플리케이션의 사용자 지정 데이터로 모바일 프로필 보강 {#enrich-mobile-profile-custom}

이 사용 사례가 작동하려면 PII 포스트백에 대한 규칙을 만들어야 합니다. 자세한 내용은 [PII 포스트백](../../administration/using/configuring-rules-launch.md#pii-postback).

### iOS 사용 {#enrich-mobile-profile-custom-ios}

iOS에서 다음을 수행합니다 [!DNL Experience Platform API] 필수 여부:

* collectPII <br> 자세한 내용은 collectPII를 참조하십시오.

다음은 iOS에서 이 사용 사례를 구현하는 샘플입니다.

```
ACPCore.collectPii(["pushPlatform":"apns", "email":email, "firstName":firstName, "lastName":lastName])
```

### Android에서 {#enrich-mobile-profile-custom-android}

Android에서 다음을 수행합니다 [!DNL Experience Platform API] 필수 여부:

* collectPII <br> 자세한 내용은 collectPII를 참조하십시오.

다음은 Android에서 이 사용 사례를 위한 샘플 구현입니다.

```
HashMap<String, String> data = new HashMap<>();
data.put("pushPlatform", "gcm");
data.put("firstName", firstNameText); 
data.put("lastName", lastNameText); 
data.put("email", emailText); 
MobileCore.collectPii(data);
```

## 애플리케이션의 라이프사이클 데이터를 사용하여 모바일 프로필을 보강합니다 {#enrich-mobile-profile-lifecycle}

이 사용 사례가 작동하려면 PII 포스트백에 대한 규칙을 만들어야 합니다. 자세한 내용은 [PII 포스트백](../../administration/using/configuring-rules-launch.md#pii-postback).

>[!NOTE]
>
>Adobe Campaign은 사용자 지정 데이터 또는 라이프사이클 데이터와 모바일 앱을 구분하지 않습니다. 두 유형의 데이터를 모두 모바일 앱의 이벤트에 대한 응답으로 collectPii 포스트백 규칙을 사용하여 서버로 전송할 수 있습니다.

### iOS 사용 {#enrich-mobile-profile-lifecycle-ios}

iOS에서 다음을 수행합니다 [!DNL Experience Platform APIs] 필수 여부:

* **[!UICONTROL Lifecycle Start]**: 앱이 시작될 때와 앱이 포그라운드에 있을 때 이 문제가 발생합니다.
* **[!UICONTROL Lifecycle Pause]**: 앱이 백그라운드에 있을 때.

자세한 내용은 [iOS의 라이프사이클 확장](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle/lifecycle-extension-in-ios).

다음은 iOS에서 이 사용 사례를 구현하는 샘플입니다.

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

### Android에서 {#enrich-mobile-profile-lifecycle-android}

Android에서 다음을 수행합니다 [!DNL Experience Platform APIs] 필수 여부:

* **[!UICONTROL OnResume]**
* **[!UICONTROL OnPause]**

자세한 내용은 [Android의 라이프사이클 확장](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle/lifecycle-extension-in-android).

다음은 Android에서 이 사용 사례를 위한 샘플 구현입니다.

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

## 푸시 알림과의 사용자 상호 작용 추적 {#track-user-push}

푸시 알림 추적 포스트백 규칙을 만들어야 합니다. 자세한 내용은 [푸시 알림 추적 포스트백](../../administration/using/configuring-rules-launch.md#push-tracking-postback).

### iOS 사용 {#track-user-push-ios}

iOS에서 다음을 수행합니다 [!DNL Experience Platform SDK] 필수 여부:

* **[!UICONTROL trackAction]**. 자세한 내용은 [앱 작업 추적](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/mobile-core-api-reference#track-app-actions).

다음은 iOS에서 이 사용 사례를 구현하는 샘플입니다.

```
let deliveryId = userInfo["_dId"] as? String
let broadlogId = userInfo["_mId"] as? String
if (deliveryId != nil && broadlogId != nil) {
    ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
}
```

### Android에서 {#track-user-push-android}

Android에서 다음을 수행합니다 [!DNL Experience Platform SDK] 필수 여부:

* **[!UICONTROL trackAction]**
자세한 내용은 [앱 작업 추적](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/mobile-core-api-reference#track-app-actions).

다음은 Android에서 이 사용 사례를 위한 샘플 구현입니다.

```
contextData.put("deliveryId", deliveryId);
contextData.put("broadlogId", messageId);
contextData.put("action", "2");
MobileCore.trackAction("tracking", contextData);
```

## 애플리케이션에서 사용자 지정 이벤트를 구현하여 인앱 메시지를 트리거합니다 {#custom-event-inapp}

### iOS 사용 {#custom-event-inapp-ios}

iOS에서 다음을 수행합니다 [!DNL Experience Platform SDK] 필수 여부:

* **[!UICONTROL trackAction]**. 자세한 내용은 [앱 작업 추적](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/mobile-core-api-reference#track-app-actions).

다음은 iOS에서 이 사용 사례를 구현하는 샘플입니다.

```
ACPCore.trackAction(mobileEventName, data: [:] )
```

### Android에서 {#custom-event-inapp-android}

Android에서 다음을 수행합니다 [!DNL Experience Platform SDK] 필수 여부:

* **[!UICONTROL trackAction]**
자세한 내용은 [앱 작업 추적](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/mobile-core-api-reference#track-app-actions).

다음은 Android에서 이 사용 사례를 위한 샘플 구현입니다.

```
MobileCore.trackAction(mobileEventText, new HashMap<String,String>());
```

## 추가 인증을 위한 링크 필드 설정 {#linkage-fields-inapp}

### iOS 사용 {#linkage-fields-inapp-ios}

iOS의 인앱 메시지를 기반으로 하는 프로필 템플릿에 대한 추가 인증에 대한 링크 필드를 설정하려면 다음을 수행하십시오 [!DNL Experience Platform SDK] 필수 여부:

* 링크 필드 설정 <br>자세한 내용은 [링크 필드 설정](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard/adobe-campaign-standard-api-reference#set-linkage-fields).
* 링크 필드 재설정 <br>자세한 내용은 [링크 필드 재설정](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard/adobe-campaign-standard-api-reference#reset-linkage-fields).

다음은 iOS과 함께 이 사용 사례의 샘플 구현입니다.

링크 필드를 설정하려면 다음을 수행하십시오.

```
var linkageFields = [String: String]()
linkageFields["cusEmail"] = "john.doe@email.com"
ACPCampaign.setLinkageFields(linkageFields)
```

링크 필드를 재설정하려면 다음을 수행하십시오.

```
ACPCampaign.resetLinkageFields(linkageFields)
```

### Android에서 {#linkage-fields-inapp-android}

Android에서 인앱 메시지를 기반으로 하는 프로필 템플릿에 대한 추가 인증에 대한 링크 필드를 설정하려면 다음 Experience Platform SDK가 필요합니다.

* 링크 필드 설정 <br>자세한 내용은 [링크 필드 설정](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard/adobe-campaign-standard-api-reference#set-linkage-fields).
* 링크 필드 재설정 <br>자세한 내용은 [링크 필드 재설정](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard/adobe-campaign-standard-api-reference#reset-linkage-fields).

다음은 Android에서 이 사용 사례의 샘플 구현입니다.

링크 필드를 설정하려면 다음을 수행하십시오.

```
HashMap<String, String> linkageFields = new HashMap<String, String>();
linkageFields.put("cusEmail", "john.doe@email.com");
Campaign.setLinkageFields(linkageFields);
```

링크 필드를 재설정하려면 다음을 수행하십시오.

```
Campaign.resetLinkageFields()
```
