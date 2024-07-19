---
title: 푸시 추적 구현
description: 푸시 알림 추적이 iOS 및 Android에서 올바르게 구현되었는지 확인하는 방법을 알아봅니다
audience: channels
feature: Instance Settings
role: Admin
level: Experienced
exl-id: 950d24e2-358f-44f8-98ea-643be61d4573
source-git-commit: 1346f7d833515fb2e6feabb39d199ffd5610c88e
workflow-type: tm+mt
source-wordcount: '932'
ht-degree: 0%

---

# 푸시 추적 구현 {#push-tracking}

## 푸시 추적 기본 정보 {#about-push-tracking}

푸시 알림이 완전히 개발되었는지 확인하려면 모든 푸시 알림에 추적이 활성화되어 있지 않으므로 추적 부분이 올바르게 구현되었는지 확인해야 합니다. 이 기능을 사용하려면 개발자가 추적이 활성화된 게재를 식별해야 합니다. Adobe Campaign Standard은 두 개의 값 **on** 또는 **off**&#x200B;이(가) 있는 `_acsDeliveryTracking` 플래그를 보냅니다. 앱 개발자는 변수가 **on**(으)로 설정된 게재에만 추적 요청을 전송해야 합니다.

>[!IMPORTANT]
>
>21.1 릴리스 이전에 설정된 게재 또는 사용자 지정 템플릿을 사용하는 게재에는 이 변수를 사용할 수 없습니다.

푸시 추적은 다음 세 가지 유형으로 구분됩니다.

* **푸시 노출 수** - 푸시 알림이 장치에 정상적으로 전달된 경우 사용자 상호 작용 없이 알림 센터에 상주합니다.

* **푸시 클릭** - 푸시 알림이 장치에 전달되고 사용자가 장치를 클릭한 경우.  사용자는 알림을 보거나(푸시 오픈 추적으로 이동) 알림을 해지하려고 했습니다.

* **열기 푸시** - 푸시 알림이 장치에 전달되고 사용자가 알림을 클릭하여 앱을 열 때. 알림이 해제된 경우 푸시 열기 가 트리거되지 않는다는 점을 제외하면 푸시 클릭과 유사합니다.

Campaign Standard 추적을 구현하려면 모바일 앱에 Adobe Experience Platform SDK가 포함되어야 합니다. 이러한 SDK는 [Adobe Experience Platform SDK 설명서](https://github.com/Adobe-Marketing-Cloud/acp-sdks)에서 사용할 수 있습니다.

추적 정보를 전송하려면 세 가지 변수를 전송해야 합니다. Campaign Standard에서 받은 데이터의 일부인 두 개와 **노출**, **클릭** 또는 **열기**&#x200B;인지 여부를 나타내는 작업 변수입니다.

| 변수 | 값 |
|:-:|:-:|
| broadlogId | 데이터의 _mId |
| deliveryId | 데이터의 ID(_dId) |
| 작업 | 열기용은 &quot;1&quot;, 클릭용은 &quot;2&quot;, 노출용은 &quot;7&quot; |

## Android 구현 {#implementation-android}

### 푸시 노출 추적을 구현하는 방법 {#push-impression-tracking-android}

노출 추적의 경우 `collectMessageInfo()` 또는 `trackAction()` 함수를 호출할 때 작업에 대한 값 &quot;7&quot;을 보내야 합니다.

21.1 릴리스 이전에 만든 게재 또는 사용자 지정 템플릿을 사용한 게재의 경우 이 [섹션](../../administration/using/push-tracking.md#about-push-tracking)을 참조하세요.

```
@Override
public void onMessageReceived(RemoteMessage remoteMessage) {
....{Handle push messages}....
  if (data.size() > 0) {
    String deliveryId = data.get("_dId");
    String messageId = data.get("_mId");
    String acsDeliveryTracking = data.get("_acsDeliveryTracking");
 
    /*
    This is to handle deliveries created before 21.1 release or deliveries with custom template
    where acsDeliveryTracking is not available.
    */
    if( acsDeliveryTracking == null ) {
        acsDeliveryTracking = "on";
    }
 
    HashMap<String, String> contextData = new HashMap<>();
    if( deliveryId != null && messageId != null && acsDeliveryTracking.equals("on")) {
      contextData.put("deliveryId", deliveryId);
      contextData.put("broadlogId", messageId);
      contextData.put("action", "7");

    //If you are using ACPCore v1.4.0 or later, use the next line.
      
      MobileCore.collectMessageInfo(contextData);
      
    //Else comment out the above line and uncomment the line below
        
    //MobileCore.trackAction("tracking", contextData) ;
    }
  }
}
```

### 클릭 추적을 구현하는 방법 {#push-click-tracking-android}

클릭 추적의 경우 `collectMessageInfo()` 또는 `trackAction()` 함수를 호출할 때 작업에 대한 값 &quot;2&quot;를 보내야 합니다.
클릭을 추적하려면 다음 두 가지 시나리오를 처리해야 합니다.

* 사용자에게 알림이 표시되지만 지워집니다.
* 사용자는 알림을 보고 클릭하여 열린 추적으로 전환합니다.

이를 처리하려면 두 가지 의도(알림을 클릭하는 의도 및 알림을 무시하는 의도)를 사용해야 합니다.

21.1 릴리스 이전에 만든 게재 또는 사용자 지정 템플릿을 사용한 게재의 경우 이 [섹션](../../administration/using/push-tracking.md#about-push-tracking)을 참조하세요.

**[!UICONTROL MyFirebaseMessagingService.java]**

```
private void sendNotification(Map<String, String> data) {
    Intent openIntent = new Intent(this, CollectPIIActivity.class);
    Intent dismissIntent = new Intent(this, NotificationDismissedReceiver.class);
    openIntent.addFlags(Intent.FLAG_ACTIVITY_CLEAR_TOP);
  
    //put the data map into the intent to track clickthroughs
    Bundle pushData = new Bundle();
    Set<String> keySet = data.keySet();
    for (String key : keySet) {
        pushData.putString(key, data.get(key));
    }
    openIntent.putExtras(pushData);
    dissmissIntent.putExtras(pushData);
  
  
    PendingIntent pendingIntent = PendingIntent.getActivity(this, 0, openIntent,
        PendingIntent.FLAG_UPDATE_CURRENT);
    PendingIntent onDismissPendingIntent = PendingIntent.getBroadcast(this.getApplicationContext(), 0, dismissIntent, 0);
  
    //<BUILD NOTIFICATION using notification builder>
    //Add both Intents to the notification
    notificationBuilder.setContentIntent(pendingIntent);
    notificationBuilder.setDeleteIntent(onDismissPendingIntent);
}
```

**[!UICONTROL BroadcastReceiver]**&#x200B;이(가) 작동하려면 **[!UICONTROL AndroidManifest.xml]**&#x200B;에 등록해야 합니다.

```
<manifest>
    <application>
        <receiver android:name=".NotificationDismissedReceiver">
        </receiver>
    </application>
</manifest>
```

NotificationDismessedReceiver.java

```
public class NotificationDismissedReceiver extends BroadcastReceiver {
    private static final String TAG = NotificationDismissedReceiver.class.getSimpleName();
    @Override
    public void onReceive(Context context, Intent intent) {
        Bundle data = intent.getExtras();
        String deliveryId = data.getString("_dId");
        String messageId = data.getString("_mId");
        String acsDeliveryTracking = data.get("_acsDeliveryTracking");
         
        /*
        This is to handle deliveries created before 21.1 release or deliveries with custom template
        where acsDeliveryTracking is not available.
        */
        if( acsDeliveryTracking == null ) {
            acsDeliveryTracking = "on";
        }
 
        HashMap<String, Object> contextData = new HashMap<>();
 
        //We only send the click tracking since the user dismissed the notification
        if (deliveryId != null && messageId != null && acsDeliveryTracking.equals("on")) {
            contextData.put("deliveryId", deliveryId);
            contextData.put("broadlogId", messageId);
            contextData.put("action", "2");
            
        //If you are using ACPCore v1.4.0 or later, use the next line.
        
            MobileCore.collectMessageInfo(contextData);
            
        //Else comment out the above line and uncomment the line below
        
            //MobileCore.trackAction("tracking", contextData);
        }
    }
}
```

### 개방형 추적을 구현하는 방법 {#push-open-tracking-android}

사용자가 알림을 클릭하여 앱을 열어야 하므로 &quot;1&quot; 및 &quot;2&quot;를 전송해야 합니다. 푸시 알림을 통해 앱을 실행/열지 않은 경우 추적 이벤트가 발생하지 않습니다.

열기를 추적하려면 Intent를 만들어야 합니다. 의도 개체를 사용하면 특정 작업이 수행될 때 Android OS에서 메서드를 호출할 수 있습니다. 이 경우 알림을 클릭하여 앱을 엽니다.

이 코드는 클릭 노출 추적 구현을 기반으로 합니다. **[!UICONTROL Intent]**&#x200B;이(가) 설정되면 이제 추적 정보를 Adobe Campaign Standard으로 다시 보내야 합니다. 이 경우 앱의 특정 보기로 열도록 **[!UICONTROL Open Intent]**&#x200B;을(를) 설정해야 합니다. 이렇게 하면 **[!UICONTROL Intent Object]**&#x200B;에 알림 데이터가 있는 onResume 메서드가 호출됩니다.

21.1 릴리스 이전에 만든 게재 또는 사용자 지정 템플릿을 사용한 게재의 경우 이 [섹션](../../administration/using/push-tracking.md#about-push-tracking)을 참조하세요.

```
@Override
protected void onResume() {
    super.onResume();
    handleTracking();
}
 
 
private void handleTracking() {
    //Check to see if this view was opened based on a notification
    Intent intent = getIntent();
    Bundle data = intent.getExtras();
 
    if (data != null) {
        //This was opened based on the notification, you need to get the tracking that was passed on.
        String deliveryId = data.getString("_dId");
        String messageId = data.getString("_mId");
        String acsDeliveryTracking = data.get("_acsDeliveryTracking");
        /*
        This is to handle deliveries created before 21.1 release or deliveries with custom template
        where acsDeliveryTracking is not available.
        */
        if( acsDeliveryTracking == null) {
            acsDeliveryTracking = "on";
        }
 
        HashMap<String, String> contextData = new HashMap<>();
 
        if (deliveryId != null && messageId != null && acsDeliveryTracking.equals("on")) {
            contextData.put("deliveryId", deliveryId);
            contextData.put("broadlogId", messageId);
            contextData.put("action", "2");
            
            //Send Click Tracking since the user did click on the notification
              
                //If you are using ACPCore v1.4.0 or later, use the next line.

                MobileCore.collectMessageInfo(contextData);
                  
                //Else comment out the above line and uncomment the line below
        
                //MobileCore.trackAction("tracking", contextData);
 
                //Send Open Tracking since the user opened the app
            
                contextData.put("action", "1");
                
                //If you are using ACPCore v1.4.0 or later, use the next line.

                MobileCore.collectMessageInfo(contextData);
                //Else comment out the above line and uncomment the line below
        
                //MobileCore.trackAction("tracking", contextData);
        }
    }
}
```

## iOS 구현 {#implementation-iOS}

### 푸시 노출 추적을 구현하는 방법 {#push-impression-tracking-iOS}

노출 추적의 경우 `collectMessageInfo()` 또는 `trackAction()` 함수를 호출할 때 작업에 대한 값 &quot;7&quot;을 보내야 합니다.

iOS 알림의 작동 방식을 이해하려면 앱의 세 가지 상태를 자세히 설명해야 합니다.

* **전경**: 앱이 현재 활성화되어 있고 현재 화면(전경)에 있는 경우.
* **백그라운드**: is 앱이 화면에 없지만 프로세스가 닫히지 않은 경우. 홈 버튼을 두 번 클릭하면 일반적으로 배경에 있는 모든 앱이 표시됩니다.
* **꺼짐/닫힘**: 프로세스가 중단된 앱입니다.

앱이 백그라운드에 있는 동안 **[!UICONTROL Impression]** 추적이 계속 작동하려면 **[!UICONTROL Content-Available]**&#x200B;을(를) 보내 앱에 추적이 수행되어야 함을 알려주어야 합니다.

>[!CAUTION]
>
> 앱을 닫으면 Apple은 앱을 다시 실행할 때까지 앱을 호출하지 않습니다. 즉, iOS에서 알림이 언제 수신되었는지 알 수 없습니다. </br> 이러한 이유로 iOS 노출 추적이 정확하지 않을 수 있으므로 신뢰할 수 없는 것으로 간주해서는 안 됩니다.

21.1 릴리스 이전에 만든 게재 또는 사용자 지정 템플릿을 사용한 게재의 경우 이 [섹션](../../administration/using/push-tracking.md#about-push-tracking)을 참조하세요.

다음 코드는 백그라운드 앱을 대상으로 합니다.

```
// In didReceiveRemoteNotification event handler in AppDelegate.m
 
//In order to handle push notification when only in background with content-available: 1
func application(_ application: UIApplication, didReceiveRemoteNotification userInfo: [AnyHashable : Any], fetchCompletionHandler completionHandler: @escaping (UIBackgroundFetchResult) -> Void) {
 
        //Check if the app is not in the foreground right now
        if(UIApplication.shared.applicationState != .active) {
            let deliveryId = userInfo["_dId"] as? String
            let broadlogId = userInfo["_mId"] as? String
            let acsDeliveryTracking = userInfo["_acsDeliveryTracking"] as? String
            /*
            This is to handle deliveries created before 21.1 release or deliveries with custom template where acsDeliveryTracking is not available.
            */
            if( acsDeliveryTracking == nil ) {
                acsDeliveryTracking = "on";
            }
            if (deliveryId != nil && broadlogId != nil && acsDeliveryTracking?.caseInsensitiveCompare("on") == ComparisonResult.orderedSame) {

            //If you are using ACPCore v2.3.0 or later, use the next line.

                ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"7"])
                
            //Else comment out the above line and uncomment the line below
        
                //ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"7"])
            }
        }
        completionHandler(UIBackgroundFetchResult.noData)
    }
```

다음 코드는 전경 앱을 대상으로 합니다.

```
// This will get called when the app is in the foreground
 
func userNotificationCenter(_ center: UNUserNotificationCenter, willPresent notification: UNNotification, withCompletionHandler completionHandler: @escaping (UNNotificationPresentationOptions) -> Void) {
 
 
        let userInfo = notification.request.content.userInfo
        let deliveryId = userInfo["_dId"] as? String
        let broadlogId = userInfo["_mId"] as? String
        let acsDeliveryTracking = userInfo["_acsDeliveryTracking"] as? String
        /*
        This is to handle deliveries created before 21.1 release or deliveries with custom template where acsDeliveryTracking is not available.
        */
        if( acsDeliveryTracking == nil ) {
            acsDeliveryTracking = "on";
        }
        if (deliveryId != nil && broadlogId != nil && acsDeliveryTracking?.caseInsensitiveCompare("on") == ComparisonResult.orderedSame) {

            //If you are using ACPCore v2.3.0 or later, use the next line.

                ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"7"])
                
            //Else comment out the above line and uncomment the line below
        
                //ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"7"])        
            }
        completionHandler([.alert,.sound])
    }
```

### 클릭 추적을 구현하는 방법 {#push-click-tracking-iOS}

클릭 추적의 경우 `collectMessageInfo()` 또는 `trackAction()` 함수를 호출할 때 작업에 대한 값 &quot;2&quot;를 보내야 합니다.
21.1 릴리스 이전에 만든 게재 또는 사용자 지정 템플릿을 사용한 게재의 경우 이 [섹션](../../administration/using/push-tracking.md#about-push-tracking)을 참조하세요.

```
// AppDelegate.swift
...
import os.log
import UserNotifications
...
  
func registerForPushNotifications() {
        let center = UNUserNotificationCenter.current()
        center.delegate = notificationDelegate
        //Here we are creating a new Category that allows us to handle Dismiss Actions
        let defaultCategory = UNNotificationCategory(identifier: "DEFAULT", actions: [], intentIdentifiers: [], options: .customDismissAction)
        //Add it to our array of Category, in this case we only have one
        center.setNotificationCategories([defaultCategory])
        center.requestAuthorization(options: [.alert, .sound, .badge]) {
            (granted, error) in
            os_log("Permission granted: %{public}@", type:. debug, granted.description)
            if error != nil {
                return
            }
            if granted {
                os_log("Notifications allowed", type: .debug)
            }
            else {
                os_log("Notifications denied", type: .debug)
            }
  
            // 2. Attempt registration for remote notifications on the main thread
            DispatchQueue.main.async {
                UIApplication.shared.registerForRemoteNotifications()
            }
        }
    }
```

이제 푸시 알림을 보낼 때 범주를 추가해야 합니다. 이 경우에는 &quot;DEFAULT&quot;라고 합니다.

![](assets/tracking_push.png)

**[!UICONTROL Dismiss]**&#x200B;을(를) 처리하고 추적 정보를 보내려면 다음을 추가해야 합니다.

```
func userNotificationCenter(_ center: UNUserNotificationCenter, didReceive response: UNNotificationResponse, withCompletionHandler completionHandler: @escaping () -> Void) {
        let userInfo = response.notification.request.content.userInfo
        switch response.actionIdentifier {
        case UNNotificationDismissActionIdentifier:
            print("Dismiss Action")
            let deliveryId = userInfo["_dId"] as? String
            let broadlogId = userInfo["_mId"] as? String
            let acsDeliveryTracking = userInfo["_acsDeliveryTracking"] as? String
            /*
            This is to handle deliveries created before 21.1 release or deliveries with custom template where acsDeliveryTracking is not available.
            */
            if( acsDeliveryTracking == nil ) {
                acsDeliveryTracking = "on";
            }
            if (deliveryId != nil && broadlogId != nil && acsDeliveryTracking?.caseInsensitiveCompare("on") == ComparisonResult.orderedSame) {

            //If you are using ACPCore v2.3.0 or later, use the next line.

                ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
                
            //Else comment out the above line and uncomment the line below
        
                //ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])   
            }
        default:
            ////MORE CODE
        }
        completionHandler()
    }
```

### 개방형 추적을 구현하는 방법 {#push-open-tracking-iOS}

사용자가 알림을 클릭하여 앱을 열어야 하므로 &quot;1&quot; 및 &quot;2&quot;를 전송해야 합니다. 푸시 알림을 통해 앱을 실행/열지 않은 경우 추적 이벤트가 발생하지 않습니다.

21.1 릴리스 이전에 만든 게재 또는 사용자 지정 템플릿을 사용한 게재의 경우 이 [섹션](../../administration/using/push-tracking.md#about-push-tracking)을 참조하세요.

```
import Foundation
import UserNotifications
import UserNotificationsUI
 
class NotificationDelegate: NSObject, UNUserNotificationCenterDelegate {
 
    // Called when user clicks the push notification or also called from willPresent()
    func userNotificationCenter(_ center: UNUserNotificationCenter, didReceive response: UNNotificationResponse, withCompletionHandler completionHandler: @escaping () -> Void) {
 
        let userInfo = response.notification.request.content.userInfo
        os_log("App push data %{public}@, in userNotificationCenter:didReceive()", type: .debug, userInfo)
        switch response.actionIdentifier {
        case UNNotificationDismissActionIdentifier:
            //This is to handle the Dismiss Action
            let deliveryId = userInfo["_dId"] as? String
            let broadlogId = userInfo["_mId"] as? String
            let acsDeliveryTracking = userInfo["_acsDeliveryTracking"] as? String
            /*
            This is to handle deliveries created before 21.1 release or deliveries with custom template where acsDeliveryTracking is not available.
            */
            if( acsDeliveryTracking == nil ) {
                acsDeliveryTracking = "on";
            }
            if (deliveryId != nil && broadlogId != nil && acsDeliveryTracking?.caseInsensitiveCompare("on") == ComparisonResult.orderedSame) {

            //If you are using ACPCore v2.3.0 or later, use the next line.

                ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
                
            //Else comment out the above line and uncomment the line below
        
                //ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])

            }
        default:
            //This is to handle the tracking when the app opens
            let deliveryId = userInfo["_dId"] as? String
            let broadlogId = userInfo["_mId"] as? String
            let acsDeliveryTracking = userInfo["_acsDeliveryTracking"] as? String
            /*
            This is to handle deliveries created before 21.1 release or deliveries with custom template where acsDeliveryTracking is not available.
            */
            if( acsDeliveryTracking == nil ) {
                acsDeliveryTracking = "on";
            }
            if (deliveryId != nil && broadlogId != nil && acsDeliveryTracking?.caseInsensitiveCompare("on") == ComparisonResult.orderedSame) {
            //If you are using ACPCore v2.3.0 or later, use the next line.

                ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
                
            //Else comment out the above line and uncomment the line below
        
                //ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])                
                
            //If you are using ACPCore v2.3.0 or later, use the next line.

                ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"1"])
                
            //Else comment out the above line and uncomment the line below
        
                //ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"1"])
                
            }
        }
        completionHandler()
    }
}
```
