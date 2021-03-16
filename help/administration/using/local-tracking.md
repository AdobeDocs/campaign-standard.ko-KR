---
solution: Campaign Standard
product: campaign
title: 푸시 추적 구현
description: 이 문서에서는 푸시 알림 추적이 iOS 및 Android에서 올바르게 구현되었는지 확인할 수 있습니다.
audience: channels
content-type: reference
topic-tags: push-notifications
context-tags: mobileApp,overview
feature: 인스턴스 설정
role: 관리자
level: 경험
translation-type: tm+mt
source-git-commit: a7a1aa2841410674597264927325c073fef4ce26
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 0%

---


# 로컬 추적 구현 {#local-tracking}

## 로컬 추적 정보 {#about-local-tracking}

이 페이지에서 로컬 알림 추적이 올바르게 구현되었는지 확인하는 방법을 알아봅니다. 이것은 로컬 알림이 이미 구성되었음을 의미합니다.

로컬 알림 추적 기능은 다음 3가지 유형으로 분할할 수 있습니다.

* **로컬 노출 횟수**  - 로컬 알림이 장치에 전달되고 알림 센터에 앉아 있지만 전혀 수정하지 않은 경우 대부분의 경우, 노출 횟수는 배달된 숫자와 동일하지 않을 경우 비슷해야 합니다. 장치가 메시지를 받았는지 확인하고 해당 정보를 다시 서버로 보냅니다.

* **로컬 클릭**  - 로컬 알림이 장치에 전달되고 사용자가 알림을 클릭한 경우입니다. 사용자가 알림을 보거나(나중에 로컬 열기 추적 기능으로 이동) 알림을 해지하려고 했습니다.

* **로컬 열기**  - 로컬 알림이 장치에 전달되고 사용자가 알림을 클릭하면 애플리케이션이 열립니다. 이 방법은 로컬 클릭과 유사하지만, 알림이 무시될 경우 로컬 열기 열기가 트리거되지 않습니다.

Adobe Campaign Standard에 대한 추적을 구현하려면 모바일 응용 프로그램에 Mobile SDK가 포함되어야 합니다. 이러한 SDK는 [!DNL Adobe Mobile Services]에서 사용할 수 있습니다.

추적 정보를 전송하려면 3개의 변수를 전송해야 합니다.2는 Adobe Campaign에서 받은 데이터의 일부이며 다른 2는 노출, 클릭 또는 열기인지를 지정하는 작업 변수입니다.

| 변수 | 값 |
| :-: | :-: |
| deliveryId | `deliveryId` 들어오는 데이터에서(사용하는 위치 `_dld` 의 푸시 추적과 유사) |
| broadlogId | `broadlogId` 들어오는 데이터에서(사용하는 위치 `_mld` 의 푸시 추적과 유사) |
| 액션 | 열기는 &quot;1&quot;, 클릭은 &quot;2&quot;, 임프레션은 &quot;7&quot; |

## 로컬 노출 추적 구현 {#implement-local-impression-tracking}

Adobe Experience Platform Mobile SDK는 추가 구성 없이 Android와 iOS 모두에 대해 노출 이벤트를 자동으로 전송합니다.

## 클릭 추적 구현 {#implementing-click-tracking}

클릭 추적의 경우 `collectMessageInfo()` 또는 `trackAction()` 함수를 호출할 때 동작에 대해 값 &quot;2&quot;를 보내야 합니다.

### Android {#implement-click-tracking-android}의 경우

클릭을 추적하려면 2개의 시나리오를 처리해야 합니다.

* 사용자가 알림을 볼 수 있지만 지웁니다.

   해고가 발생할 경우 클릭을 추적하려면 응용 프로그램 모듈의 AndroidManifest 파일에 브로드캐스트 수신기 `NotificationDismissalHandler`을(를) 추가합니다.

   ```
   <receiver
   android:name="com.adobe.marketing.mobile.NotificationDismissalHandler">
   </receiver>
   ```

* 사용자가 알림을 보고 이를 클릭하면 열린 추적이 표시됩니다.

   이 시나리오는 클릭과 열기를 생성합니다. 이 클릭을 추적하는 것은 열기를 추적하는 데 필요한 구현의 일부가 됩니다. [오픈 추적 구현](#implement-open-tracking)을 참조하십시오.

### iOS {#implement-click-tracking-ios}의 경우

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

## 열기 추적 구현 {#implement-open-tracking}

사용자가 응용 프로그램을 열려면 알림을 클릭해야 하므로 &quot;1&quot; 및 &quot;2&quot;를 보내야 합니다. 로컬 알림을 통해 응용 프로그램을 시작/열지 않으면 추적 이벤트가 발생하지 않습니다.

### Android {#implement-open-tracking-android}의 경우

열기를 추적하려면 의도를 만들어야 합니다. 의도 개체를 사용하면 특정 작업이 완료되면 Android OS에서 메서드를 호출할 수 있습니다. 이 경우 알림을 클릭하여 앱을 열 수 있습니다.

이 코드는 클릭 노출 추적 구현을 기반으로 합니다. 이제 의도가 설정되어 있으므로 추적 정보를 다시 Adobe Campaign으로 보내야 합니다. 이 경우 사용자가 클릭한 결과 알림을 트리거한 Android 보기([!DNL Activity])가 열리거나 전경으로 표시됩니다. [!DNL Activity]의 intent 객체에는 열기를 추적하는 데 사용할 수 있는 알림 데이터가 포함되어 있습니다.

MainActivity.java(extends [!DNL Activity])

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

        //Opened based on the notification, you need to get the tracking that was passed on.

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

### iOS {#implement-open-tracking-ios}의 경우

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
