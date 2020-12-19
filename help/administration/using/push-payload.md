---
solution: Campaign Standard
product: campaign
title: Campaign Standard 푸시 알림 페이로드 구조 이해
description: 이 문서는 모바일 애플리케이션에서 받은 페이로드의 구조를 설명하기 위한 것입니다.
audience: channels
content-type: reference
topic-tags: push-notifications
context-tags: mobileApp,overview
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '1148'
ht-degree: 3%

---


#  푸시 알림 페이로드 구조 이해{#push-payload}

Adobe Campaign을 사용하면 iOS 및 Android 모바일 디바이스에서 개인화된 푸시 알림을 모바일 애플리케이션(모바일 앱)으로 전송할 수 있습니다.

모바일 앱에서 수신되는 모든 푸시 알림은 알림 푸시 알림이 전송될 경우 푸시 알림을 표시하기 위해 앱에서 사용하는 일부 정보를 포함하고 특히 자동 푸시 알림이 전송될 경우 약간의 추가 계산을 수행할 수 있습니다.

이 정보는 푸시 알림이 수신되었음을 나타내는 이벤트 핸들러의 모바일 앱 코드로 수신됩니다. Adobe Campaign Standard에서 푸시 알림을 전송할 때 모바일 앱에서 수신한 정보에는 Campaign Standard에서 제공하는 일부 기능을 이용하는 데 사용할 수 있는 Campaign Standard 특정 정보가 포함될 수 있습니다. 또한 페이로드에는 모바일 앱에서 사용할 수 있는 사용자 지정 데이터가 포함될 수 있습니다.

이 문서에서는 푸시 알림이 Adobe Campaign Standard에서 앱으로 성공적으로 전송될 때 모바일 앱에서 받은 페이로드 구조에 대해 설명합니다.

>[!NOTE]
>
>페이로드 구조는 모바일 앱 유형(예: iOS 앱, FCM 지원 Android 앱)에 따라 달라집니다.

## 푸시 페이로드 구조 {#push-payload-structure}

이 섹션에서는 다양한 모바일 플랫폼에 대한 샘플 페이로드 구조에 대해 자세히 설명하고 여기에 포함된 주요 속성에 대해 설명합니다. 푸시 알림이 수신되었음을 나타내는 이벤트 핸들러의 모바일 앱 코드에서 받은 페이로드 구조입니다.

페이로드 특성 및 값은 푸시 알림 고급 옵션에 제공된 구성에 따라 달라집니다. 또한 이 섹션에서는 Campaign Standard에서 옵션을 구성할 때 페이로드가 변경되는 방식을 확인하기 위해 Campaign Standard UI에서 이러한 구성과 페이로드의 속성 간 매핑을 제공합니다.

### iOS 모바일 앱의 경우 {#payload-structure-ios}

**Adobe Campaign에서 iOS 앱으로 전송된 샘플 페이로드:**

```
{

    "aps":{

            "alert":{

                    "body":"This is the content of my push notification",

                    "title":"Push Notification Title"

            },

            "content-available":1,

            "category":"NEW_MESSAGE_CATEGORY",

            "badge":2,

            "mutable-content":1,

            "sound":"default"

        },

    "custom_field1":"custom_value1",

    "custom_field2":"custom_value2",

    "media-attachment-url":"https://2.img-dpreview.com/files/p/articles/9440145363/Creative_Cloud.jpeg",

    "uri":"https://mydeeplinkurl.com",

    "_dId":"56c4",

    "_mId":"h138a"} 
```

**iOS APNS 테스터와 함께 사용할  [JSON 샘플 페이로드](https://pushtry.com/)**

```
{

  "aps": {

    "alert": {

      "title": "Push Notification Title",

      "body": "body of push"

    },

    "badge": 33,

    "sound": "default"

  },

  "custom_field1": "custom_value1",

  "uri": "https://mydeeplinkurl.com"

}
```

페이로드의 가장 중요한 부분은 aps 사전이 있는데, 여기에는 Apple에서 정의한 키가 포함되어 있으며, 알림을 받는 시스템이 사용자에게 어떻게 경고할지를 결정하는 데 사용됩니다(있는 경우). 이 섹션에는 모바일 앱에서 푸시 알림의 동작을 설정하는 데 사용되는 사전 정의된 키가 포함되어 있습니다.

앱 내의 속성에 대한 자세한 내용은 Apple 개발자 문서에서 확인할 수 있습니다.[원격 알림 페이로드 만들기](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html#//apple_ref/doc/uid/TP40008194-CH10-SW1).

### Android 앱의 경우 {#payload-structure-android}

**Adobe Campaign에서 Android 앱으로 보내는 샘플 페이로드**

```
{

  "collapseKey": "1476005",

  "priority": "high",

  "data": {

    "_dId": "d57fd6",

    "_mId": "h1685a5",

    "body": "adobe body 123",

    "category": "adobe category 123",

    "custom key 1": "value 1",

    "custom key 2": "test value 2",

    "custom key 3": "foo bar android",

    "media-attachment-url": "http://adobegiphy.com?test=123",

    "sound": "http://testcampaign.instance.com/r/?id=s1685a5,d57fd6,d57ff5",

    "title": "adobe title 123",

    "uri": "http://testcampaign.instance.com/r/?id=d1685a5,d57fd6,d57ff6",

    "badge": 1817

  }

}
```

**Google FCM 테스터를 사용하는  [JSON 샘플 페이로드](https://pushtry.com/)**

```
{

  "to": "<==========ENTER your device token==============>",

  "collapseKey": "1476005",

  "priority": "high",

  "data": {

    "_dId": "d57fd6",

    "_mId": "h1685a5",

    "title": "adobe title 123",

    "body": "adobe body 123",

    "category": "adobe category 123",

    "custom key 1": "value 1",

    "custom key 2": "test value 2",

    "custom key 3": "foo bar android",

    "media-attachment-url": "http://adobegiphy.com?test=123",

    "sound": "http://testcampaign.instance.com/r/?id=s1685a5,d57fd6,d57ff5",

    "uri": "http://testcampaign.instance.com/r/?id=d1685a5,d57fd6,d57ff6",

    "badge": 1817

  }

}
```

페이로드에는 사용자 지정 키/값 쌍을 비롯한 모든 푸시 알림 전달 콘텐츠를 포함하는 데이터 메시지가 포함되어 있으며, 필요에 따라 다른 비즈니스 논리를 추가하기 위해 클라이언트 앱이 푸시 알림을 빌드하고 표시하는 메시지를 처리해야 합니다.

android 페이로드의 측면을 이해하려면 [메시징 개념 및 옵션(fcm)](https://firebase.google.com/docs/cloud-messaging/concept-options)을 참조하십시오.

>[!NOTE]
>
>Android 페이로드에서 알림 메시지에 대한 지원이 2018년 1월 현재 삭제되어 사용자가 앱과 상호 작용할 필요 없이 앱을 켜고 모바일 앱에 컨트롤을 전달할 수 있습니다.

### Campaign Standard 구성과 페이로드 특성 간의 매핑 {#mapping-payload}

| 캠페인 구성 | iOS의 영향을 받은 속성 | Android의 영향을 받은 속성 | 설명 |
|:-:|:-:|:-:|:-:|
| 메시지 제목 <br>메시지 본문 | 경고 → 제목 <br> 경고 → 본문 | 제목 <br>본문 | 이 데이터에는 경고 메시지의 세부 사항이 포함됩니다.<br>제목 및 본문 키는 경고의 내용을 제공합니다. |
| 사운드 재생 | 사운드 | 사운드 | 경고로 재생할 사용자 정의 사운드. |
| 배지의 값 | 배지 | 배지 | 앱의 아이콘을 배지하는 데 사용할 정수 값입니다. |
| 딥 링크 추가 | uri | NA | 딥 링크를 사용하면 웹 브라우저 페이지를 여는 대신 사용자를 애플리케이션 내에 있는 콘텐츠로 직접 불러옵니다. |
| 카테고리 | category | category | 원격 알림과 함께 사용자 지정 작업을 표시하려면 <br>카테고리 키는 시스템이 경고 인터페이스에서 해당 카테고리에 대한 작업을 단추로 표시하는 데 도움이 됩니다. |
| 사용자 정의 필드 | custom_field1, custom_field2... | custom_field1, custom_field2... | 앱에 전송하려는 모든 사용자 지정 데이터. |
| 리치 미디어 컨텐츠 URL(이미지, gif, 오디오 및 비디오 파일)<br>(iOS 10 이상에만 해당) | media-attachment-url | NA | 알림에 리치 컨텐츠를 추가할 미디어 파일의 URL. <br>이 URL에 대한 값을 제공하면 mutable-content 플래그가 페이로드로 자동으로 전송됩니다. <br> (iOS 10 이상에만 해당) |
| 변경 가능한 컨텐츠 <br>(iOS 10 이상에만 적용 가능) | mutable-content | NA | 앱의 알림 서비스 익스텐션은 mutable-content 키로 모든 원격 알림을 &quot;차단&quot;하며 요청 페이로드의 컨텐츠를 처리/조작할 수 있도록 해주므로 이를 사용하여 알림을 사용자 정의할 수 있습니다. 이 기능의 사용 사례로는 여러 미디어 다운로드 및 표시, 푸시 페이로드에 있는 암호화된 데이터를 해독하는 작업이 있습니다. 자세한 내용은 [원격 알림의 페이로드 수정](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html)에 있습니다. <br>(iOS 10 이상에만 해당) |
| 사용 가능한 컨텐츠 | 컨텐츠 사용 가능 | NA | 이 옵션을 선택하면 iOS 앱이 백그라운드/일시 중단 상태에 있을 때 이를 활성화할 수 있습니다. 깨면 앱이 백그라운드에서 실행되며 푸시 알림 데이터 페이로드를 수신하는 적절한 이벤트 핸들러는 제어권을 가지며 사용자 지정 푸시 알림을 빌드하고 동일하게 표시하는 것을 비롯하여 모든 계산을 위해 데이터를 사용할 수 있음을 의미합니다. 추가 정보는 알림 배달](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html)과 함께 [절전 모드 해제 앱에서 찾을 수 있습니다. |
| 리치 미디어 컨텐츠 URL(이미지 파일)<br>(Android에만 해당) | NA | media-attachment-url | 알림에 리치 컨텐츠를 추가할 이미지 파일의 URL. |
| NA | _mId<br>_dId | _mId <br>_dId | broadlogId 및 deliveryId의 값입니다.<br>이 속성은 앱이 푸시 알림을 클릭/연 시간을 추적하기 위해 추적 포스트백을 호출하려는 경우에 필요합니다. 이 정보는 사용자의 개입 없이 앱 서버에서 내부적으로 계산되고 전송됩니다.<br>포스트백에 대한 정보는 이 페이지에서 찾을 수  [있습니다](https://helpx.adobe.com/campaign/kb/config-app-in-launch.html#PIIpostback). |

### 모바일 앱 코드 {#payload-information}에서 페이로드 정보를 검색하는 방법

앱 서버에서 보내는 페이로드 정보는 푸시 알림이 수신되었음을 나타내는 이벤트 핸들러의 모바일 앱 코드에 의해 수신됩니다. 이 이벤트는 작업 중인 모바일 플랫폼에 따라 다르며 앱이 전경 또는 백그라운드에서 실행되고 있는지에 따라 달라집니다. 다음 설명서는 사용 사례를 기반으로 처리할 이벤트 핸들러를 식별하는 데 도움이 됩니다.

* iOS 애플리케이션:[원격 알림](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/HandlingRemoteNotifications.html)의 **원격 알림 처리** 섹션
* Android 애플리케이션:[Android 클라이언트 앱에서 메시지 수신](https://firebase.google.com/docs/cloud-messaging/android/receive)

**iOS 모바일 앱용 샘플**

```
 - (void)application:(UIApplication *)application

didReceiveRemoteNotification:(NSDictionary *)userInfo {

    

    NSDictionary *apsDict = [userInfo objectForKey:@"aps"];

    NSDictionary *alertDict = [apsDict objectForKey:@"alert"];

    NSString *title = [alertDict objectForKey:@"title"];

    NSString *body = [alertDict objectForKey:@"body"];

    NSString *category = [apsDict objectForKey:@"category"];

    NSString *deliveryId = userInfo[@"_dId"];

    NSString *broadlogId = userInfo[@"_mId"];

    NSString *mediaAttachmentURL = userInfo[@"media-attachment-url"];

    NSString *deeplinkURL = userInfo[@"uri"];

    NSString *customValue1 = userInfo[@"custom_field1"];   

}
```

**Android Mobile FCM 앱용 샘플**

```
public void onMessageReceived(RemoteMessage message) {

    Map<String, String> dataMap = message.getData();

     

    String title = dataMap.get("title");

    String body = dataMap.get("body");

    String category = dataMap.get("category");

    String deliveryId = dataMap.get("_dId");

    String broadlogId = dataMap.get("_mId");

    String mediaAttachmentURL = dataMap.get("media-attachment-url");

    String deeplinkURL = dataMap.get("uri");

    String customValue1 = dataMap.get("custom_field1");

}
```
