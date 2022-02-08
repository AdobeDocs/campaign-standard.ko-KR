---
title: 푸시 추적 구현
description: 푸시 알림 추적이 iOS 및 Android에서 올바르게 구현되었는지 확인하는 방법을 알아봅니다
audience: channels
feature: Instance Settings
role: Admin
level: Experienced
exl-id: b983d0a3-c345-44d4-bc82-202bf6ed26ab
source-git-commit: bfba6b156d020e8d2656239e713d2d24625bda54
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 0%

---

# 로컬 추적 구현 {#local-tracking}

## 로컬 추적 기본 정보 {#about-local-tracking}

이 페이지에서 로컬 알림 추적이 올바르게 구현되었는지 확인하는 방법을 알아봅니다. 이는 로컬 알림이 이미 구성되었음을 의미합니다.

로컬 알림 추적은 다음 세 가지 유형으로 분할할 수 있습니다.

* **로컬 노출 횟수** - 로컬 알림이 장치에 전달되어 알림 센터에 있지만 전혀 터치하지 않은 경우 대부분의 경우, 노출 횟수는 전달된 숫자와 동일하지 않은 경우 유사해야 합니다. 이렇게 하면 장치가 메시지를 받고 해당 정보를 다시 서버로 전달합니다.

* **로컬 클릭** - 로컬 알림이 장치에 전달되고 사용자가 알림을 클릭한 경우 사용자는 알림을 보거나(이 알림이 로컬 열린 추적으로 이동) 알림을 해지하려고 했습니다.

* **로컬 열기** - 로컬 알림이 장치에 전달되고 사용자가 알림을 클릭하여 애플리케이션을 연 경우 알림이 무시되면 로컬 열기가 트리거되지 않는다는 점을 제외하면 로컬 클릭과 유사합니다.

Adobe Campaign Standard에 대한 추적을 구현하려면 모바일 애플리케이션에서 Mobile SDK를 애플리케이션에 포함해야 합니다. 이러한 SDK는에서 사용할 수 있습니다. [!DNL Adobe Mobile Services].

추적 정보를 전송하려면 다음 세 가지 변수를 보내야 합니다. 두 항목은 Adobe Campaign에서 받은 데이터의 일부이며, 다른 변수는 노출, 클릭 또는 열기 여부를 나타내는 작업 변수입니다.

| 변수 | 값 |
| :-: | :-: |
| deliveryId | `deliveryId` 수신되는 데이터( `_dld` 가 사용됨) |
| broadlogId | `broadlogId` 수신되는 데이터( `_mld` 가 사용됨) |
| 작업 | &quot;1&quot;(열림), &quot;2&quot;(클릭) 및 &quot;7&quot;(노출) |

## 로컬 노출 추적 구현 {#implement-local-impression-tracking}

Adobe Experience Platform Mobile SDK는 추가 구성 없이 Android와 iOS 모두에 대한 노출 이벤트를 자동으로 전송합니다.

## 클릭 추적 구현 {#implementing-click-tracking}

클릭 추적의 경우 호출 시 작업에 대해 값 &quot;2&quot;를 전송해야 합니다 `collectMessageInfo()` 또는 `trackAction()` 함수 위에 있어야 합니다.

### Android용 {#implement-click-tracking-android}

클릭 수를 추적하려면 두 가지 시나리오를 구현해야 합니다.

* 사용자는 알림을 보지만 지웁니다.

   해지 시나리오의 경우 클릭을 추적하려면 브로드캐스트 수신기를 추가합니다 `NotificationDismissalHandler` 아래의 제품에서 사용할 수 있습니다.

   ```
   <receiver
   android:name="com.adobe.marketing.mobile.NotificationDismissalHandler">
   </receiver>
   ```

* 사용자가 알림을 보고 클릭하면 열린 추적이 됩니다.

   이 시나리오는 클릭 및 열기를 생성합니다. 이 클릭을 추적하면 열기를 추적하는 데 필요한 구현의 일부가 됩니다. 자세한 내용은 [공개 추적 구현](#implement-open-tracking).

### iOS용 {#implement-click-tracking-ios}

클릭 추적 정보를 보내려면 다음을 추가해야 합니다.

```
class NotificationDelegate: NSObject, UNUserNotificationCenterDelegate {

   func userNotificationCenter(_ center: UNUserNotificationCenter, didReceive response: UNNotificationResponse, withCompletionHandler completionHandler: @escaping () -> Void) {
        let userInfo = response.notification.request.content.userInfo
        switch response.actionIdentifier {
        case UNNotificationDismissActionIdentifier:
            print("Dismiss Action")
            let deliveryId = userInfo["deliveryId"] as? String
            let broadlogId = userInfo["broadlogId"] as? String
            if (deliveryId != nil && broadlogId != nil) {
                
                //If you are using ACPCore v2.3.0 or later, use the next line.
                
                ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
                
                //Else comment out the above line and uncomment the line below
                
                // ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
            }
        default:
            
            ////MORE CODE
        }
        completionHandler()
    }
}
```

## 개방형 추적 구현 {#implement-open-tracking}

응용 프로그램을 열려면 알림을 클릭해야 하므로 &quot;1&quot; 및 &quot;2&quot;를 보내야 합니다. 애플리케이션이 로컬 알림을 통해 시작/열리지 않으면 추적 이벤트가 발생하지 않습니다.

### Android용 {#implement-open-tracking-android}

열기를 추적하려면 의도를 만들어야 합니다. 의도 개체를 사용하면 특정 작업이 완료되면 Android OS에서 메서드를 호출할 수 있습니다. 이 경우 알림을 클릭하여 앱을 엽니다.

이 코드는 클릭 노출 추적 구현을 기반으로 합니다. 이제 의도가 설정된 경우 추적 정보를 다시 Adobe Campaign으로 보내야 합니다. 이 경우 Android View([!DNL Activity])을 클릭하여 알림을 트리거한 페이지를 사용자가 클릭했을 때 전경으로 가져오거나 엽니다. 의 의도 개체 [!DNL Activity] 열기 수를 추적하는 데 사용할 수 있는 알림 데이터를 포함합니다.

MainActivity.java(확장) [!DNL Activity])

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

        //Opened based on the notification, you must get the tracking that was passed on.

        Map<String, String> notificationData = (Map<String, Object>)data.getSerializableExtra("NOTIFICATION_USER_INFO");
        String deliveryId = (String)notificationData.get("deliveryId");
        String messageId = (String)notificationData.get("broadlogId");

        if (deliveryId != null && messageId != null) {
            HashMap<String, String> contextData = new HashMap<>();
            contextData.put("deliveryId", deliveryId);
            contextData.put("broadlogId", messageId);
 
            //Send click tracking since the user did click on the notification

            contextData.put("action", "2");

            //If you are using ACPCore v1.4.0 or later, use the next line.
    
            MobileCore.collectMessageInfo(contextData);

            //Else comment out the above line and uncomment the line below

            // MobileCore.trackAction("tracking", contextData);
 
            //Send open tracking since the user opened the app

            contextData.put("action", "1");

            //If you are using  ACPCore v1.4.0 or later, use the next line.

            MobileCore.collectMessageInfo(contextData);

            //Else comment out the above line and uncomment the line below

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
 
    //Called when user clicks the local notification or also called from willPresent()

    func userNotificationCenter(_ center: UNUserNotificationCenter, didReceive response: UNNotificationResponse, withCompletionHandler completionHandler: @escaping () -> Void) {
 
        let userInfo = response.notification.request.content.userInfo
        os_log("App push data %{public}@, in userNotificationCenter:didReceive()", type: .debug, userInfo)
        switch response.actionIdentifier {
        case UNNotificationDismissActionIdentifier:

            //This is to handle the Dismiss action

            let deliveryId = userInfo["deliveryId"] as? String
            let broadlogId = userInfo["broadlogId"] as? String
            if (deliveryId != nil && broadlogId != nil) {

                //If you are using ACPCore v2.3.0 or later, use the next line.

                ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])

                //Else comment out the above line and uncomment the line below

                // ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
            }
        default:
            //This is to handle the tracking when the app opens
            let deliveryId = userInfo["deliveryId"] as? String
            let broadlogId = userInfo["broadlogId"] as? String
            if (deliveryId != nil && broadlogId != nil) {

               //If you are using ACPCore v2.3.0 or later, use the next line.

               ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
               ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"1"])

               //Else comment out the above line and uncomment the line below

               // ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
               // ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"1"])
            }
        }
        completionHandler()
    }
}
```
