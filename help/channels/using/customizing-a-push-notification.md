---
title: 푸시 알림 사용자 정의
description: 다양한 고급 옵션을 사용하여 푸시 알림을 사용자 지정하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: 8cf74cad-b1ba-4aad-83bd-7289cb22d5f4
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: push-notifications
discoiquuid: dc944c85-2059-46df-b396-676fe3617dd1
context-tags: delivery,mobileAppContent,back
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 78800930d78179c1e390313c35f70627b5df0769

---


# 푸시 알림 사용자 정의{#customizing-a-push-notification}

푸시 알림을 세밀하게 조정하기 위해 Adobe Campaign을 사용하면 푸시 알림을 디자인하는 동안 일련의 고급 옵션에 액세스할 수 있습니다.

Adobe Campaign에서 모바일 애플리케이션을 구성하려면 다음 기술 문서 Campaign Standard 푸시 알림 [페이로드 구조 이해를 참조하십시오](https://helpx.adobe.com/campaign/kb/understanding-campaign-standard-push-notifications-payload-struc.html).

![](assets/push_notif_advanced.png)

**관련 컨텐츠:**

* [푸시 알림 보고서](../../reporting/using/push-notification-report.md)
* [워크플로우 내에서 푸시 알림 보내기](../../automating/using/push-notification-delivery.md)

## 사운드 재생 {#play-a-sound}

이 기능을 **[!UICONTROL Play a sound]** 사용하면 앱이 실행되지 않을 때 푸시 알림을 전달하여 장치에서 사운드를 재생할 수 있습니다.

사운드는 푸시 알림을 사용자에게 경고하여 더 많은 가시성을 제공합니다. 모바일 앱에 사운드를 포함하려면:

1. 푸시 알림을 열고 **[!UICONTROL Advanced options]** 섹션에 액세스합니다.
1. 알림을 받을 때 모바일 장치에서 재생할 사운드 파일의 확장명 없이 파일 이름을 **[!UICONTROL Play a sound]** 필드에 입력합니다.

   지원되는 미디어 포맷에 대한 자세한 내용은 Apple 및 [Android](https://support.apple.com/kb/PH16864?locale=en_US) 설명서를 [참조하십시오](https://developer.android.com/guide/topics/media/media-formats.html) .

   ![](assets/push_notif_advanced_7.png)

1. 파일이 모바일 응용 프로그램 패키지에 정의된 경우 알림을 전달할 때 사운드 파일이 재생됩니다. 그렇지 않으면 장치의 기본 사운드가 재생됩니다.

그러면 사용자가 푸시 알림과 휴대폰이 음소거 되지 않은 경우에만 사운드를 수신하게 됩니다.

## 배지 값 새로 고침 {#refresh-the-badge-value}

배지는 새 읽지 않은 정보의 수를 애플리케이션 아이콘에 직접 표시하는 데 사용됩니다. 사용자가 응용 프로그램에서 새 컨텐츠를 열거나 읽으면 배지 값이 사라집니다.

장치에서 알림을 받으면 관련 앱에 대한 배지 값을 새로 고치거나 추가할 수 있습니다. 서버측에서 배지 값을 전송하려면

1. 푸시 알림을 열고 **[!UICONTROL Advanced options]** 섹션에 액세스합니다.
1. 배지 값은 정수여야 하며 다음과 같은 다양한 방법으로 업데이트할 수 있습니다.

   * 배지를 새로 고치려면 **[!UICONTROL Value of the badge]** 필드에 0을 입력합니다. 애플리케이션 아이콘에서 배지가 제거됩니다.
   * 배지 값을 추가하려면 **[!UICONTROL Value of the badge]** 필드에 숫자를 입력합니다. 이 번호는 사용자가 푸시 알림을 받자마자 배지에 자동으로 표시됩니다.
   * 필드가 비어 있거나 정수가 들어 있지 않으면 배지 값이 변경되지 않습니다.
   여기서는 사용자가 애플리케이션에 새로운 정보를 가지고 있음을 알리기 위해 **[!UICONTROL Value of the badge]** 필드에 1을 입력합니다.

   ![](assets/push_notif_advanced_8.png)

1. 메시지를 전송하면 사용자는 푸시 알림을 수신하게 되며 응용 프로그램은 자동으로 새 배지 값을 표시합니다.

   ![](assets/push_notif_advanced_1.png)

## 기본값 추가 {#add-a-deeplink}

시각화를 사용하면 사용자를 웹 브라우저 페이지를 여는 대신 애플리케이션 내에 있는 컨텐츠로 직접 가져올 수 있습니다.

정의에는 사용자 정의 인앱 경험을 위한 개인화 데이터가 포함될 수 있습니다. 예를 들어, 수신자의 이름은 응용 프로그램이 수신자에게 보내는 페이지에 자동으로 입력됩니다.

푸시 알림에 기본값을 추가하려면:

1. 푸시 알림을 열고 **[!UICONTROL Advanced options]** 섹션에 액세스합니다.
1. 필드에 링크를 **[!UICONTROL Add a deeplink]** 입력합니다.

   ![](assets/push_notif_advanced_3.png)

1. 메시지를 전송한 후 사용자는 푸시 알림을 수신하게 되고 클릭유도문안(예: 클릭유도문안) 단추를 누르는 등 알림과 상호 작용하여 앱의 특정 페이지에 액세스합니다.

   ![](assets/push_notif_advanced_4.png)

## 작업 정의 {#define-an-action}

모바일 애플리케이션에서 사용 가능한 경우 카테고리 ID를 추가한 다음 작업 단추를 표시할 수 있습니다. 이러한 알림을 통해 사용자는 애플리케이션을 열거나 탐색하지 않고도 알림에 응답하여 다른 작업을 보다 신속하게 수행할 수 있습니다.

사용자의 휴대폰에 표시되는 대화 상자를 계속 진행하려면 결정이 필요합니다. 사용자가 작업 중 하나를 선택하면 시스템은 연결된 작업을 수행할 수 있도록 응용 프로그램에 알립니다.

푸시 알림에 카테고리를 추가하려면:

1. 푸시 알림을 열고 **[!UICONTROL Advanced options]** 섹션에 액세스합니다.
1. 푸시 알림을 수신할 때 실행 가능한 단추를 표시하려면 **[!UICONTROL Category]** 필드에 사전 정의된 범주 이름을 입력합니다.

   모바일 응용 프로그램 개발자는 응용 프로그램에서 카테고리 ID와 단추의 예상 동작을 정의해야 합니다. 자세한 내용은 Apple 개발자 설명서 [(카테고리](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/SupportingNotificationsinYourApp.html) 구성 및 실행 가능한 알림&#x200B;**섹션) 또는** Android 개발자 [설명서를](https://developer.android.com/guide/topics/ui/notifiers/notifications.html)참조하십시오.

   ![](assets/push_notif_advanced_9.png)

1. 푸시 알림을 전송한 후 사용자는 푸시 알림을 수신하게 되며 이전에 구성된 실행 가능한 버튼을 사용하여 조치를 취해야 합니다.

   ![](assets/push_notif_actionable_buttons.png)

사용자의 작업에 따라 관련 작업을 수행할 수 있도록 응용 프로그램에 알림이 표시됩니다.

## 만료 날짜 추가 {#add-expiration-date}

만료 날짜를 푸시 알림으로 설정하면 메시지가 더 이상 Apple(APNS) 또는 Android(FCM)에서 전송되지 않는 특정 만료[날짜를](https://developer.apple.com/documentation/usernotifications/setting_up_a_remote_notification_server/sending_notification_requests_to_apns)설정할[수 있습니다](https://firebase.google.com/docs/cloud-messaging/concept-options).

푸시 알림에 만료 날짜를 추가하려면:

1. 옵션을 **[!UICONTROL Expire message]** 선택합니다.

   >[!NOTE]
   >
   >이 **[!UICONTROL Expire message]** 옵션을 선택하면 지속 시간이 자동으로 0으로 설정됩니다. 값을 변경하지 않으면 APNS와 FCM 모두 메시지를 즉시 전송하려고 시도합니다. 실패하면 메시지가 다시 전송되지 않습니다.

1. 필드에서 푸시 알림의 유효성을 **[!UICONTROL Duration]** 선택합니다.

   ![](assets/push_expiration.png)

1. 푸시 알림을 전송한 후에도 전화가 켜져 있지 않거나 신호가 없어서 사용자가 바로 받지 못한 경우, 푸시 메시지가 만료 날짜 시간 슬롯 내에 계속 전송됩니다.

푸시 알림이 만료 날짜 이전에 전송되지 않은 경우 무시됩니다.

## 사용자 정의 필드 추가 {#add-custom-fields}

사용자 지정 필드를 사용하면 사용자 지정 데이터를 페이로드의 키 값 쌍 형식으로 전달할 수 있습니다. 이 옵션을 사용하여 사전 정의된 키를 넘어 응용 프로그램에 추가 데이터를 전달할 수 있습니다.

이렇게 하려면 다음을 수행하십시오.

1. 푸시 알림을 열고 **[!UICONTROL Advanced options]** 섹션에 액세스합니다.
1. 범주에서 **[!UICONTROL Custom fields]** **[!UICONTROL Add an element]** 단추를 클릭합니다.
1. 각 키와 **[!UICONTROL Keys]** 연결된 을 **[!UICONTROL Values]** 입력한 다음

   ![](assets/push_notif_advanced_10.png)

1. 사용자 정의 필드의 처리 및 용도는 전적으로 모바일 앱에 달려 있습니다. 아래 푸시 알림에서, 앱에서 푸시 알림의 단추 레이블을 표시하기 위해 사용자 정의 필드를 사용했습니다.

   ![](assets/push_notif_actionable_buttons.png)

## 리치 미디어 컨텐츠 추가 {#add-rich-media-content}

리치 미디어 컨텐츠를 사용하면 사용자의 참여도가 향상되어 사용자가 푸시 알림을 보다 많이 열 수 있습니다.

알림 자체에서 재생되거나 표시되는 이미지, gif, 오디오 또는 비디오 파일을 포함할 수 있습니다. 앱 사용자는 애플리케이션을 열지 않고도 볼 수 있습니다.

푸시 알림에 리치 미디어를 포함하려면:

1. 푸시 알림을 열고 **[!UICONTROL Advanced options]** 섹션에 액세스합니다.
1. 각 형식에 대한 **[!UICONTROL Rich media content URL]** 필드에 파일의 URL을 입력합니다.iOS 및 Android.

   iOS 10 이상의 경우 이미지, gif, 오디오 및 비디오 파일을 삽입할 수 있습니다. 이전 iOS 버전의 경우 푸시 알림이 리치 컨텐츠 없이 표시됩니다. iOS 장치의 Adobe Campaign 푸시 알림에서 이미지를 표시하는 방법에 대한 자세한 내용은 이 [페이지를](https://helpx.adobe.com/campaign/kb/display-image-push.html)참조하십시오.

   Android의 경우 이미지만 포함할 수 있습니다.

   ![](assets/push_notif_advanced_6.png)

1. 메시지를 보낸 후 사용자는 푸시 알림을 받게 되고 리치 미디어 컨텐츠를 볼 수 있습니다.

   ![](assets/push_notif_advanced_2.png)

## iOS에 대한 알림 동작 변경 {#change-the-notification-behavior-for-ios}

![](assets/push_notif_advanced_5.png)

iOS 10 이상의 경우 푸시 알림 **[!UICONTROL Advanced options]** 섹션에서 두 개의 추가 옵션을 사용할 수 있습니다. **[!UICONTROL Mutable content]** 및 **[!UICONTROL Content available]** Adobe

옵션이 선택되어 있고 리치 미디어 컨텐츠 URL이 추가되면 mutable-content 플래그가 푸시 페이로드에서 전송되며 iOS SDK에서 제공하는 알림 서비스 애플리케이션 익스텐션으로 푸시 알림 컨텐츠가 수정될 수 있습니다. **[!UICONTROL Mutable content]** 자세한 내용은 Apple 개발자 [설명서를](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html)참조하십시오.

그런 다음 모바일 앱 확장을 활용하여 Adobe Campaign에서 전송된 푸시 알림의 내용 또는 프레젠테이션을 추가로 수정할 수 있습니다. 예를 들어 사용자는 이 옵션을 사용하여 다음을 수행할 수 있습니다.

* 암호화된 형식으로 배달된 데이터 암호 해독
* 이미지 또는 기타 미디어 파일을 다운로드하고 알림에 첨부 파일로 추가
* 알림의 본문 또는 제목 텍스트 변경
* 알림에 스레드 식별자 추가

이 **[!UICONTROL Content available]** 확인란을 선택하면 푸시 페이로드에서 사용 가능한 콘텐츠 플래그가 전송되어 앱이 푸시 알림을 받는 즉시 깨지도록 합니다. 즉, 앱이 페이로드 데이터에 액세스할 수 있습니다. 이 기능은 앱이 백그라운드에서 실행되고 사용자 상호 작용(예: 푸시 알림 탭)이 없어도 작동하지만 앱이 실행되고 있지 않은 경우에는 적용되지 않습니다. 자세한 내용은 Apple 개발자 설명서를 [참조하십시오](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html).

## Android에 대한 알림 동작 변경 {#change-the-notification-behavior-for-android}

Android의 경우 리치 미디어 컨텐츠 URL 필드에 파일의 URL을 입력할 **수** 있습니다. 반면 Android의 경우 iOS 버전에서는 이미지, gif, 오디오 또는 비디오 파일을 포함할 수 없습니다.

이 **[!UICONTROL High priority]** 확인란을 사용하여 푸시 알림에 대한 높은 우선 순위 또는 일반적인 우선 순위를 설정할 수 있습니다. 메시지 우선 순위에 대한 자세한 내용은 Google 개발자 [설명서를](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message)참조하십시오.

![](assets/push_notif_advanced_11.png)

