---
title: Adobe Campaign Standard 푸시 알림의 이미지 표시
description: iOS 장치에서 Adobe Campaign 푸시 알림의 이미지를 표시하는 방법을 알아봅니다
audience: channels
feature: Instance Settings
role: Admin
level: Experienced
exl-id: 474c8002-4263-4617-9480-6a9b603bde8e
source-git-commit: 7767b39a48502f97e2b3af9d21a3f49b9283ab2e
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 12%

---

# iOS 이미지 및 비디오 추가 {#image-push}

>[!NOTE]
>
>이 문서는 iOS 장치에만 적용됩니다.

이 문서에서는 Adobe Campaign Standard iOS 푸시 알림의 이미지를 표시하는 방법을 알아봅니다.

## 1단계: 푸시 알림 설정 {#set-up-push}

푸시 알림은 Experience Platform SDK에서 지원됩니다.

푸시 알림을 받는 모바일 애플리케이션은 Adobe Campaign 인터페이스에서 관리자가 구성해야 합니다.

Adobe Campaign 및 Adobe Mobile Services를 모두 구성하면 캠페인에 모바일 애플리케이션의 데이터를 사용할 수 있습니다. 자세한 정보는 이 [페이지](../../administration/using/configuring-a-mobile-application.md)를 참조하십시오.

Experience Cloud SDK 애플리케이션을 사용하여 푸시 알림을 전송하려면 데이터 수집 UI에서 모바일 앱을 설정하고 Adobe Campaign에서 구성해야 합니다. 자세한 정보는 이 [페이지](../../administration/using/configuring-a-mobile-application.md#channel-specific-config)를 참조하십시오.

## 2단계: Adobe Campaign에서 푸시 알림 사용자 지정 {#customize-push}

푸시 알림을 세밀하게 조정하기 위해 Adobe Campaign에서는 푸시 알림을 디자인하는 동안 고급 옵션 집합에 액세스할 수 있습니다.

1. 푸시 알림을 만듭니다. 자세한 정보는 이 [페이지](../../channels/using/preparing-and-sending-a-push-notification.md)를 참조하십시오.

1. 푸시 알림 콘텐츠 페이지에서 **[!UICONTROL Advanced options]** 섹션에 액세스합니다.

1. **[!UICONTROL Rich media content URL]** 필드에 파일의 URL을 입력합니다.
iOS 10 이상의 경우 이미지, gif, 오디오 및 비디오 파일을 삽입할 수 있습니다.

   ![](assets/push_notif_advanced_6.png)

1. 푸시 알림을 미리 보고 저장합니다.

## 3단계: 모바일 애플리케이션 코드 조정 {#mobile-app-code}

Adobe Campaign에서 푸시 알림을 사용자 지정한 후에는 디바이스에 이미지를 표시하도록 모바일 애플리케이션을 구성해야 합니다.

>[!NOTE]
>
>응용 프로그램이 Objective-C에 있는 경우 다음 [설명서](https://experienceleague.adobe.com/docs/mobile-services/ios/messaging-ios/push-messaging/c-set-up-rich-push-notif-ios.html?lang=ko)를 참조하세요.

앱이 [!DNL Swift]에 있는 경우 아래 단계를 수행합니다.

1. [!DNL Xcode] 프로젝트를 엽니다.

1. [!DNL Xcode] 프로젝트에서 **[!UICONTROL File]** > **[!UICONTROL New]** > **[!UICONTROL Target]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Notification Service Extension]**&#x200B;을(를) 선택합니다.

   ![](assets/push_notif_advanced_12.png)

1. **NotificationService.swift** 파일 클래스가 만들어졌는지 확인하십시오.

1. 이 클래스를 편집하고 기본 콘텐츠를 다음으로 바꿉니다.
이렇게 하면 응용 프로그램에서 이미지 URL을 사용하여 들어오는 매개 변수를 처리하고 구문 분석한 다음 로컬로 복사한 다음 푸시 알림에서 표시할 수 있습니다.

   ```
   import UserNotifications
   
   class NotificationService: UNNotificationServiceExtension {
   
   var contentHandler: ((UNNotificationContent) -> Void)?
   var bestAttemptContent: UNMutableNotificationContent?
   
   override func didReceive(_ request: UNNotificationRequest, withContentHandler contentHandler: @escaping (UNNotificationContent) -> Void) {
       self.contentHandler = contentHandler
       bestAttemptContent = (request.content.mutableCopy() as? UNMutableNotificationContent)
   
       if let bestAttemptContent = bestAttemptContent {
           var urlString:String? = nil
           if let urlImageString = request.content.userInfo["media-attachment-url"] as? String {
               urlString = urlImageString
           }
   
           if urlString != nil, let fileUrl = URL(string: urlString!) {
               print("fileUrl: \(fileUrl)")
   
               // Download the attachment
               URLSession.shared.downloadTask(with: fileUrl) { (location, response, error) in
                   if let location = location {
                       // Move temporary file to remove .tmp extension
                       if (error == nil) {
                           let tmpDirectory = NSTemporaryDirectory()
                           let tmpFile = "file://".appending(tmpDirectory).appending(fileUrl.lastPathComponent)
                           let tmpUrl = URL(string: tmpFile)!
                           try! FileManager.default.moveItem(at: location, to: tmpUrl)
   
                           // Add the attachment to the notification content
                           if let attachment = try? UNNotificationAttachment(identifier: fileUrl.lastPathComponent, url: tmpUrl) {
                               bestAttemptContent.attachments = [attachment]
                               }
                       }
                       if(error != nil) {
                           print("Failed to download attachment: \(error.debugDescription)")
                       }
                   }
                   // Serve the notification content
                   contentHandler(bestAttemptContent)
               }.resume()
           }
       }
   }
   
   override func serviceExtensionTimeWillExpire() {
       // Called just before the extension will be terminated by the system.
       // Use this as an opportunity to deliver your "best attempt" at modified content, otherwise the original push payload will be used.
       if let contentHandler = contentHandler, let bestAttemptContent = bestAttemptContent {
           contentHandler(bestAttemptContent)
       }
   }
   
   }
   ```

알림이 전송되는 동안 모바일은 다음 페이로드를 수신해야 합니다.

이미지 URL은 주요 media-attachment-url과 매핑됩니다. 이미지를 다운로드하고 표시하기 위해 애플리케이션 코드 관점에서 처리해야 하는 키/값 쌍입니다.

```
userInfo: [AnyHashable("media-attachment-url"): https://pbs.twimg.com/profile_images/876737835314950144/zPTs9b7o.jpg, AnyHashable("_dId"): 1de3ef93, AnyHashable("_mId"): h280a5, AnyHashable("aps"): {
 
    alert =     {
 
        body = "Message Body here";
 
        title = "This a push from Campaign";
 
    };
 
    badge = 1;
 
    "mutable-content" = 1;
 
}]
```

## 4단계: 푸시 전송 테스트 {#test-send-push}

이제 애플리케이션 빌드를 테스트하고 위의 2단계에서 만든 배달을 테스트할 수 있습니다. 푸시 알림 준비 및 전송에 대한 자세한 내용은 이 [페이지](../../channels/using/preparing-and-sending-a-push-notification.md)를 참조하세요.

![](assets/push_notif_advanced_34.png)
