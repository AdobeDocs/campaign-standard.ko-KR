---
solution: Campaign Standard
product: campaign
title: 푸시 추적 구현
description: 이 문서를 사용하면 푸시 알림 추적이 iOS 및 Android에서 올바르게 구현되었는지 확인할 수 있습니다.
audience: channels
content-type: reference
topic-tags: push-notifications
context-tags: mobileApp,overview
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 0%

---


# 로컬 추적 구현 {#local-tracking}

## 로컬 추적 정보 {#about-local-tracking}

이 페이지에서 로컬 알림 추적이 올바르게 구현되었는지 확인하는 방법을 알아봅니다. 이는 로컬 알림이 이미 구성되었음을 의미합니다.

로컬 알림 추적은 다음 세 가지 유형으로 나눌 수 있습니다.

* **로컬 노출 횟수** - 로컬 알림이 장치에 전달되고 알림 센터에 앉아 있지만 전혀 터치되지 않은 경우 대부분의 경우, 노출 횟수는 배달된 번호와 동일하지 않을 경우 비슷해야 합니다. 장치가 메시지를 받았는지 확인하고 해당 정보를 다시 서버로 전달합니다.

* **로컬 클릭** - 로컬 알림이 장치에 전달되고 사용자가 장치를 클릭한 경우 사용자가 알림을 보거나(다시 로컬 열기 추적으로 이동) 알림을 해지하려고 했습니다.

* **로컬 열기** - 로컬 알림이 장치에 전달되고 사용자가 알림을 클릭하면 응용 프로그램이 열립니다. 이 동작은 로컬 클릭과 유사하지만, 알림이 무시되면 로컬 열린 열기가 트리거되지 않습니다.

Adobe Campaign Standard에 대한 추적을 구현하려면 모바일 응용 프로그램에 Mobile SDK가 포함되어야 합니다. 이러한 SDK는 [!DNL Adobe Mobile Services]

추적 정보를 전송하려면 세 가지 변수가 필요합니다.두 가지는 Adobe Campaign에서 받은 데이터의 일부이고 다른 하나는 노출, 클릭 또는 열기인지를 지정하는 작업 변수입니다.

| 변수 | 값 |
| :-: | :-: |
| deliveryId | 들어오는 데이터의 &quot;deliveryId&quot;(&quot;_dld&quot;가 사용되는 푸시 추적과 유사) |
| broadlogId | 들어오는 데이터의 &quot;broadlogId&quot;(&quot;_mld&quot;가 사용되는 푸시 추적과 유사) |
| 조치 | &quot;1&quot; for Open, &quot;2&quot; for Click, &quot;7&quot; for Impression |

## 로컬 노출 추적 구현 {#implement-local-impression-tracking}

노출 추적을 수행하려면 collectMessageInfo() 또는 trackAction() 함수를 호출할 때 동작에 대한 값 &quot;7&quot;을 전송해야 합니다.

### Android용 {#implement-local-impression-tracking-android}

Adobe Experience Platform 모바일 SDK는 로컬 알림을 트리거할 때 노출 횟수 추적을 시작합니다.

### iOS용 {#implement-local-impression-tracking-ios}

노출 횟수 추적을 구현하는 방법을 설명하려면 애플리케이션의 세 가지 상태를 이해해야 합니다.

* **전경**:애플리케이션이 현재 활성 상태이고 전경의 화면에 있는 경우

* **배경**:응용 프로그램이 화면에 표시되지 않지만 프로세스를 닫지 않은 경우입니다. 홈 단추를 두 번 클릭하면 일반적으로 백그라운드에서 모든 애플리케이션이 표시됩니다.

* **해제/종료**:응용 프로그램의 프로세스가 종료된 경우. 애플리케이션이 닫혀 있으면 Apple은 애플리케이션을 다시 시작할 때까지 해당 애플리케이션을 호출하지 않습니다. 즉, iOS에서 알림을 받은 시점을 절대로 알 수 없습니다.

애플리케이션이 백그라운드에 있는 동안 노출 횟수 추적이 계속 작동하도록 하려면 &quot;컨텐츠 사용 가능&quot;을 전송하여 애플리케이션에서 추적을 수행해야 함을 알려야 합니다.

Adobe Experience Platform 모바일 SDK는 로컬 알림을 트리거할 때 노출 횟수 추적을 시작합니다.

>[!CAUTION]
>
>iOS 노출 횟수 추적은 정확하지 않으며 안전하게 볼 수 없습니다.

## 클릭 추적 구현 {#implementing-click-tracking}

클릭 추적의 경우 collectMessageInfo() 또는 trackAction() 함수를 호출할 때 동작에 대한 값 &quot;2&quot;를 보내야 합니다.

### Android용 {#implement-click-tracking-android}

클릭을 추적하려면 두 가지 시나리오를 처리해야 합니다.

* 사용자가 알림을 확인하지만 지웁니다.

* 사용자가 알림을 보고 클릭하면 열린 추적이 됩니다.

클릭의 첫 번째 시나리오는 Adobe Experience Platform Mobile SDK에 의해 추적됩니다.

### iOS용 {#implement-click-tracking-ios}

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

그런 다음 해고를 처리하고 추적 정보를 전송하려면 다음을 추가해야 합니다.

```
func userNotificationCenter(_ center: UNUserNotificationCenter, didReceive response: UNNotificationResponse, withCompletionHandler completionHandler: @escaping () -> Void) {
        let userInfo = response.notification.request.content.userInfo
        switch response.actionIdentifier {
        case UNNotificationDismissActionIdentifier:
            print("Dismiss Action")
            let deliveryId = userInfo["deliveryId"] as? String
            let broadlogId = userInfo["broadlogId"] as? String
            if (deliveryId != nil && broadlogId != nil) {
                // If you're using  ACPCore v2.3.0 or later, use the line below.
                ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
                // Else comment out the above line and uncomment the line below
                // ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
            }
        default:
            ////MORE CODE
        }
        completionHandler()
    }
```

## 개방형 추적 구현 {#implement-open-tracking}

사용자가 알림을 클릭해야 애플리케이션을 열 수 있으므로 &quot;1&quot; 및 &quot;2&quot;를 보내야 합니다. 로컬 알림을 통해 응용 프로그램을 시작/열지 않으면 추적 이벤트가 발생하지 않습니다.

### Android용 {#implement-open-tracking-android}

열린 상태를 추적하려면 의도를 만들어야 합니다. 의도 개체를 사용하면 특정 작업이 완료되면 Android OS에서 메서드를 호출할 수 있습니다. 이 경우 알림을 클릭하여 앱을 엽니다.

이 코드는 클릭 노출 횟수 추적의 구현을 기반으로 합니다. 이제 의도가 설정된 추적 정보를 Adobe Campaign으로 다시 보내야 합니다. 이 경우 알림을 트리거한 Android View([!DNL Activity])는 사용자가 클릭함으로 인해 열리거나 전경 상태로 표시됩니다. 의 의도 개체에는 열린 것을 추적하는 데 사용할 수 있는 알림 데이터가 [!DNL Activity] 포함되어 있습니다.

MainActivity.java(확장 [!DNL Activity])

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
        Map<String, String> notificationData = (Map<String, Object>)data.getSerializableExtra("NOTIFICATION_USER_INFO");
        String deliveryId = (String)notificationData.get("deliveryId");
        String messageId = (String)notificationData.get("broadlogId");
  
  
  
        if (deliveryId != null && messageId != null) {
            HashMap<String, String> contextData = new HashMap<>();
            contextData.put("deliveryId", deliveryId);
            contextData.put("broadlogId", messageId);
  
            //Send Click Tracking since the user did click on the notification
            contextData.put("action", "2");
            // If you're using  ACPCore v1.4.0 or later, use the next line.
            MobileCore.collectMessageInfo(contextData);
            // Else comment out the above line and uncomment the line below
            // MobileCore.trackAction("tracking", contextData);
  
            //Send Open Tracking since the user opened the app
            contextData.put("action", "1");
            // If you're using  ACPCore v1.4.0 or later, use the next line.
            MobileCore.collectMessageInfo(contextData);
            // Else comment out the above line and uncomment the line below
            // MobileCore.trackAction("tracking", contextData);
        }
    }
}
```

### iOS용 {#implement-open-tracking-ios}

```
import os.log
import Foundation
import UserNotifications
import UserNotificationsUI
import ACPCore
  
class NotificationDelegate: NSObject, UNUserNotificationCenterDelegate {
  
    // Called when user clicks the local notification or also called from willPresent()
    func userNotificationCenter(_ center: UNUserNotificationCenter, didReceive response: UNNotificationResponse, withCompletionHandler completionHandler: @escaping () -> Void) {
  
        let userInfo = response.notification.request.content.userInfo
        os_log("App push data %{public}@, in userNotificationCenter:didReceive()", type: .debug, userInfo)
        switch response.actionIdentifier {
        case UNNotificationDismissActionIdentifier:
            //This is to handle the Dismiss Action
            let deliveryId = userInfo["deliveryId"] as? String
            let broadlogId = userInfo["broadlogId"] as? String
            if (deliveryId != nil && broadlogId != nil) {
            // If you're using  ACPCore v2.3.0 or later, use the line below.
                ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
            // Else comment out the above line and uncomment the line below
            // ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
            }
        default:
            //This is to handle the tracking when the app opens
            let deliveryId = userInfo["deliveryId"] as? String
            let broadlogId = userInfo["broadlogId"] as? String
            if (deliveryId != nil && broadlogId != nil) {
               // If you're using  ACPCore v2.3.0 or later, use the line below.
               ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
               ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"1"])
               // Else comment out the above line and uncomment the line below
               // ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
               // ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"1"])
            }
        }
        completionHandler()
    }
}
```
