---
title: 푸시 추적 구현
description: 이 문서를 사용하면 푸시 알림 추적이 iOS 및 Android에서 올바르게 구현되었는지 확인할 수 있습니다.
page-status-flag: never-activated
uuid: 961aaeb5-6948-4fd2-b8d7-de4510c10566
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: push-notifications
discoiquuid: 23b4212e-e878-4922-be20-50fb7fa88ae8
context-tags: mobileApp,overview
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 6c5cf90211451587537b9a6121430fc4f352384c
workflow-type: tm+mt
source-wordcount: '819'
ht-degree: 0%

---


# 푸시 추적 구현 {#push-tracking}

## 푸시 추적 정보 {#about-push-tracking}

푸시 알림이 완전히 개발되었는지 확인하려면 추적 부분이 올바르게 구현되었는지 확인해야 합니다.
이 경우 푸시 알림 구현의 첫 번째 부분을 이미 구현했다고 가정합니다.

* 앱 사용자 등록
* 푸시 알림 메시지 처리

푸시 추적은 다음 세 가지 유형으로 구분됩니다.

* **푸시 노출 횟수** - 푸시 알림이 장치에 전달되고 알림 센터에 앉아 있지만 전혀 만지지 않은 경우  이것은 임상으로 여겨진다.  대부분의 경우 노출 횟수는 배달된 번호와 동일하지 않을 경우 비슷해야 합니다. 장치가 메시지를 받고 해당 정보를 다시 서버로 전달했는지 확인합니다.

* **푸시 클릭** - 푸시 알림이 장치에 전달되고 사용자가 장치를 클릭한 경우  사용자가 알림을 보거나(다시 푸시 열기 추적으로 이동) 알림을 해지하려고 했습니다.

* **푸시 열기** - 푸시 알림이 장치에 전달되고 사용자가 알림을 클릭했을 때 앱이 열립니다.  이 방법은 푸시 클릭과 비슷하지만 알림이 해제된 경우 공개 푸시가 트리거되지 않습니다.

Campaign Standard 추적을 구현하려면 모바일 앱에 Mobile SDK가 포함되어야 합니다. 이러한 SDK는 Adobe Mobile Services에서 사용할 수 있습니다. For more on this, refer to this [page](../../administration/using/configuring-a-mobile-application.md).

추적 정보를 전송하려면 세 가지 변수를 보내야 합니다. Campaign Standard에서 받은 데이터의 일부인 두 개 및 노출 수, **클릭**&#x200B;또는 **열기** 여부를 나타내는 작업 변수 **가**&#x200B;있습니다.

| 변수 | 값 |
|:-:|:-:|
| broadlogId | 데이터의 _mId |
| deliveryId | 데이터의 _dId |
| 조치 | 열림 1개, 클릭은 2개, 임프레션은 7개 |

## Android용 구현 {#implementation-android}

### 푸시 노출 추적을 구현하는 방법 {#push-impression-tracking-android}

노출 횟수 추적의 경우 함수를 호출할 때 동작에 대해 값 &quot;7&quot;을 보내야 **[!UICONTROL trackAction()]** 합니다.

```
@Override
public void onMessageReceived(RemoteMessage remoteMessage) {
....{Handle push messages}....
  if (data.size() > 0) {
    String deliveryId = data.get("_dId");
    String messageId = data.get("_mId");
    HashMap<String, String> contextData = new HashMap<>();
    if (deliveryId != null && messageId != null) {
                contextData.put("deliveryId", deliveryId);
                contextData.put("broadlogId", messageId);
                contextData.put("action", "7");
                MobileCore.trackAction("tracking", contextData);
    }
  }
}
```

### 클릭 추적을 구현하는 방법 {#push-click-tracking-android}

클릭 추적의 경우 함수를 호출할 때 동작에 대해 값 &quot;2&quot;를 보내야 **[!UICONTROL trackAction()]** 합니다.

클릭을 추적하려면 두 가지 시나리오를 처리해야 합니다.

* 사용자가 알림을 확인하지만 지웁니다.
* 사용자가 알림을 보고 이를 클릭하여 열린 추적으로 전환합니다.

이를 처리하려면 다음 두 가지 인터페이스를 사용해야 합니다. 알림을 클릭할 때와 알림을 취소할 수 있는 경우입니다.

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

In order for the work **[!UICONTROL BroadcastReceiver]** you need to registered it to the **[!UICONTROL AndroidManifest.xml]**

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
  
        HashMap<String, Object> contextData = new HashMap<>();
  
        //We only send the click tracking since the user dismissed the notification
        if (deliveryId != null && messageId != null) {
            contextData.put("deliveryId", deliveryId);
            contextData.put("broadlogId", messageId);
            contextData.put("action", "1");
            MobileCore.trackAction("tracking", contextData);
        }
    }
}
```

### 개방형 추적을 구현하는 방법 {#push-open-tracking-android}

앱을 열려면 알림을 클릭해야 하므로 &quot;1&quot; 및 &quot;2&quot;를 보내야 합니다. 푸시 알림을 통해 앱을 시작/열지 않으면 추적 이벤트가 발생하지 않습니다.

열기를 추적하려면 의도를 만들어야 합니다. 의도 개체를 사용하면 특정 작업이 완료될 때 Android OS에서 메서드를 호출할 수 있습니다. 이 경우 알림을 클릭하여 앱을 엽니다.

이 코드는 클릭 노출 횟수 추적의 구현을 기반으로 합니다. 이제 **[!UICONTROL Intent]** 세트를 사용하여 추적 정보를 다시 Adobe Campaign Standard으로 보내야 합니다. 이 경우 앱을 앱의 특정 보기 **[!UICONTROL Open Intent]** 로 열도록 설정해야 합니다. 그러면 알림 데이터가 있는 onResume 메서드가 호출됩니다 **[!UICONTROL Intent Object]**.

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
        //Looks it was opened based on the notification, lets get the tracking we passed on.
        String deliveryId = data.getString("_dId");
        String messageId = data.getString("_mId");
  
        HashMap<String, Object> contextData = new HashMap<>();
  
        if (deliveryId != null && messageId != null) {
            contextData.put("deliveryId", deliveryId);
            contextData.put("broadlogId", messageId);
  
            //Send Click Tracking since the user did click on the notification
            contextData.put("action", "2");
            MobileCore.trackAction("tracking", contextData);
  
            //Send Open Tracking since the user opened the app
            contextData.put("action", "1");
            MobileCore.trackAction("tracking", contextData);
        }
    }
}
```

## iOS용 구현 {#implementation-iOS}

### 푸시 노출 추적을 구현하는 방법 {#push-impression-tracking-iOS}

노출 횟수 추적의 경우 함수를 호출할 때 동작에 대해 값 &quot;7&quot;을 보내야 **[!UICONTROL trackAction()]** 합니다.

iOS 알림의 작동 방식을 이해하려면 앱의 세 가지 상태를 자세히 설명해야 합니다.

* **전경**: 앱이 현재 활성화되어 있고 현재 화면에 있는 경우(전경).
* **배경**: is 앱이 화면에 표시되지 않지만 프로세스가 닫히지 않은 경우. 홈 단추를 두 번 클릭하면 일반적으로 백그라운드에 있는 모든 앱이 표시됩니다.
* **해제/폐쇄**: 프로세스가 중단된 앱

앱이 닫혀 있으면 Apple은 앱을 다시 시작할 때까지 앱을 호출하지 않습니다. 즉, iOS에서 알림을 받은 시점을 알 수 없습니다.

앱이 백그라운드에 있는 동안 **[!UICONTROL Impression]** 추적 작업을 계속 수행하기 위해 앱 **[!UICONTROL Content-Available]** 에 추적이 수행되어야 한다는 사실을 알리기 위해 전송해야 합니다.

>[!CAUTION]
>
>iOS 노출 추적은 정확하지 않으며 신뢰할 수 있는 것으로 간주해서는 안 됩니다.

다음 코드는 백그라운드 앱을 대상으로 합니다.

```
// In didReceiveRemoteNotification event handler in AppDelegate.m
  
//In order to handle push notification when only in background with content-available: 1
func application(_ application: UIApplication, didReceiveRemoteNotification userInfo: [AnyHashable : Any], fetchCompletionHandler completionHandler: @escaping (UIBackgroundFetchResult) -> Void) {
  
        //Check if the app is not in the foreground right now
        if(UIApplication.shared.applicationState != .active) {
            let deliveryId = userInfo["_dId"] as? String
            let broadlogId = userInfo["_mId"] as? String
            if (deliveryId != nil && broadlogId != nil) {
               ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"7"])
            }
        }
        completionHandler(UIBackgroundFetchResult.noData)
    }
```

다음 코드는 포그라운드 앱을 대상으로 합니다.

```
// This will get called when the app is in the foreground
  
func userNotificationCenter(_ center: UNUserNotificationCenter, willPresent notification: UNNotification, withCompletionHandler completionHandler: @escaping (UNNotificationPresentationOptions) -> Void) {
  
  
        let userInfo = notification.request.content.userInfo
        let deliveryId = userInfo["_dId"] as? String
        let broadlogId = userInfo["_mId"] as? String
        if (deliveryId != nil && broadlogId != nil) {
             ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"7"])
        }
        completionHandler([.alert,.sound])
    }
```

### 클릭 추적을 구현하는 방법 {#push-click-tracking-iOS}

클릭 추적의 경우 함수를 호출할 때 동작에 대해 값 &quot;2&quot;를 보내야 **[!UICONTROL trackAction()]** 합니다.

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

이제 푸시 알림을 전송할 때 카테고리를 추가해야 합니다. 이 경우 &quot;기본값&quot;이라고 합니다.

![](assets/tracking_push.png)

그런 다음 추적 정보 **[!UICONTROL Dismiss]** 를 처리하고 전송하려면 다음을 추가해야 합니다.

```
func userNotificationCenter(_ center: UNUserNotificationCenter, didReceive response: UNNotificationResponse, withCompletionHandler completionHandler: @escaping () -> Void) {
        let userInfo = response.notification.request.content.userInfo
        switch response.actionIdentifier {
        case UNNotificationDismissActionIdentifier:
            print("Dismiss Action")
            let deliveryId = userInfo["_dId"] as? String
            let broadlogId = userInfo["_mId"] as? String
            if (deliveryId != nil && broadlogId != nil) {
                ADBMobile.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
            }
        default:
            ////MORE CODE
        }
        completionHandler()
    }
```

### 개방형 추적을 구현하는 방법 {#push-open-tracking-iOS}

앱을 열려면 알림을 클릭해야 하므로 &quot;1&quot; 및 &quot;2&quot;를 보내야 합니다. 푸시 알림을 통해 앱을 시작/열지 않으면 추적 이벤트가 발생하지 않습니다.

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
            if (deliveryId != nil && broadlogId != nil) {
                ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
            }
        default:
            //This is to handle the tracking when the app opens
            let deliveryId = userInfo["_dId"] as? String
            let broadlogId = userInfo["_mId"] as? String
            if (deliveryId != nil && broadlogId != nil) {
                ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
                ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"1"])
            }
        }
        completionHandler()
    }
}
```
