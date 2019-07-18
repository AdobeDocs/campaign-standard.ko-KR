---
title: 푸시 알림 준비 및 전송
seo-title: 푸시 알림 준비 및 전송
description: 푸시 알림 준비 및 전송
seo-description: 다음 단계에 따라 Adobe Campaign에서 단일 전송 푸시 알림을 만듭니다.
page-status-flag: 정품 인증 안 함
uuid: 01997725-CA 0 A -420 C -9 E 81-5 EA 801652 F 87
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 채널
content-type: 참조
topic-tags: 푸시 알림
discoiquuid: EC 930 CD 4-6365-4 E 54-Babe -9 DC 2 EED 041 FC
context-tags: delivery, mobileappcontent, back
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 6df0e764750a31f29d6fe3ec4d92e19b3f07f728

---


# Preparing and sending a push notification{#preparing-and-sending-a-push-notification}

## Preparing the notification {#preparing-the-notification}

Adobe Campaign를 사용하여 푸시 알림을 만드는 단계는 다음과 같습니다.

1. **[!UICONTROL Marketing activities]** 창에서 새 마케팅 활동을 [만듭니다](../../start/using/marketing-activities.md#creating-a-marketing-activity).

   Note that a single push notification can also be created from a [campaign](../../start/using/marketing-activities.md#creating-a-marketing-activity) or from the Adobe Campaign [home page](../../start/using/interface-description.md#home-page).

   워크플로우에서 푸시 알림 전송 활동을 사용할 수도 있습니다. This activity is presented in the [Push notification delivery](../../automating/using/push-notification-delivery.md) section.

1. **[!UICONTROL Push notification]** Select.
1. 템플릿을 선택합니다.

   ![](assets/push_notif_type.png)

   기본적으로 다음 두 템플릿 중 하나를 선택할 수 있습니다.

   * **[!UICONTROL Send push to Campaign profiles]**: 이 템플릿을 사용하여 모바일 애플리케이션을 구독하고 푸시 알림 수신에 동의한 Adobe Campaign CRM 프로필을 타게팅합니다. You can insert [personalization](../../designing/using/inserting-a-personalization-field.md) fields into your push notification, such as the recipient's first name.
   * **[!UICONTROL Send push to app subscribers]**: 이 템플릿을 사용하여 애플리케이션에서 알림을 받도록 선택한 모든 알려진 익명 모바일 애플리케이션 사용자에게 푸시 알림을 전송할 수 있습니다. 모바일 애플리케이션에서 수집한 데이터로 이러한 메시지를 개인화할 수 있습니다.
   다국어 템플릿을 선택할 수도 있습니다. For more information, refer to [Creating a multilingual push notification](../../channels/using/creating-a-multilingual-push-notification.md).

   For more on templates, refer to the [Managing templates](../../start/using/about-templates.md) section.

1. Enter your push notification properties and select your mobile app in the **[!UICONTROL Associate a Mobile App to a delivery]** field.

   드롭다운에는 SDK v 4 및 Experience Platform SDK 애플리케이션이 모두 표시됩니다.

   ![](assets/push_notif_properties.png)

   푸시 알림을 캠페인에 연결할 수 있습니다. 이렇게 하려면 이미 만들어진 캠페인에서 선택합니다.

1. 다음 화면에서 대상자를 지정할 수 있습니다. 예를 들어 특정 모바일 애플리케이션을 구독한 모든 VIP 고객을 지정할 수 있습니다. For more on this, see [Creating audiences](../../audiences/using/creating-audiences.md).

   대상은 이전 단계에서 선택한 모바일 애플리케이션을 기반으로 자동으로 필터링됩니다.

   ![](assets/push_notif_audience.png)

1. 이제 푸시 알림을 사용자 정의할 수 있습니다. First, choose the message style: **[!UICONTROL Alert/Message/Badge]** or **[!UICONTROL Silent push]**. The push notification types are described in the [About push notifications](../../channels/using/about-push-notifications.md) section.

   푸시 알림의 내용을 편집하고 고급 옵션을 정의합니다. See [Customizing a push notification](../../channels/using/customizing-a-push-notification.md).

   ![](assets/push_notif_content.png)

   여기에 구성된 푸시 알림 컨텐츠 및 옵션은 페이로드 형식으로 모바일 앱에 전달됩니다. The detailed structure of the payload is described in the [Understanding ACS push notifications payload structure](https://helpx.adobe.com/campaign/kb/understanding-campaign-standard-push-notifications-payload-struc.html) technote.

1. **[!UICONTROL Create]**&#x200B;을 클릭합니다.

   ![](assets/push_notif_content_2.png)

1. 알림을 보내기 전에 테스트 프로필로 테스트한 다음 배달을 보내기 전에 받는 사람이 보게 될 내용을 정확히 확인할 수 있습니다. Select **[!UICONTROL Audiences]** from your delivery summary and click the **[!UICONTROL Test profiles]** tab.

   For more on sending tests, refer to [Test profiles](../../sending/using/managing-test-profiles-and-sending-proofs.md).

1. Select your test profiles and click **[!UICONTROL Preview]** to display the notification: content is personalized with the test profile data.
1. 다른 장치에서 푸시 알림 레이아웃을 확인합니다. 렌더링을 미리 보려면 iPhone, Android 폰, iPad 또는 Android 태블릿을 선택합니다.

   ![](assets/push_notif_preview.png)

1. The **[!UICONTROL Estimated Payload Size]** is an estimate based on test profile data. 실제 페이로드 크기는 다를 수 있습니다. 메시지 제한은 4 KB 입니다.

   >[!CAUTION]
   >
   >페이로드 크기가 4 KB 제한을 초과하는 경우 메시지가 배달되지 않습니다. 개인화 데이터는 메시지 크기에 영향을 줍니다.

## Sending the notification {#sending-the-notification}

푸시 알림은 대상 기준을 정의하여 Adobe Campaign에서 선택한 대상자에게 보낼 수 있습니다. 아래의 예에서, 선택된 대상자는 4 개의 타깃팅된 모바일 앱 가입자로 구성됩니다.

1. Click **[!UICONTROL Prepare]** to compute the target and generate the notifications.

   ![](assets/push_send_1.png)

1. Once the preparation has finished successfully, the **[!UICONTROL Deployment]** window presents the following KPIs: **[!UICONTROL Target]** and **[!UICONTROL To deliver]**. Note that the **[!UICONTROL To deliver]** count is lower than the **[!UICONTROL Targeted]** one due to exclusions which can be viewed by clicking ![](assets/lp_link_properties.png) button at the bottom of the **[!UICONTROL Deployment]** window.

   ![](assets/push_send_2.png)

1. **[!UICONTROL Exclusion logs]** 탭에서, 전송된 Target에서 제외된 모든 메시지 목록과 이 제외의 이유를 찾을 수 있습니다.

   여기에서, 주소가 블랙리스트에 추가되어 있고 프로필이 중복되었기 때문에 모바일 앱 구독자 중 한 명이 제외되었습니다.

   ![](assets/push_send_5.png)

1. Click the **[!UICONTROL Exclusion causes]** tab to display the volume of excluded messages.

   ![](assets/push_send_7.png)

1. You can now click **[!UICONTROL Confirm]** to start sending push notifications.
1. 메시지 대시보드 및 로그에서 배달 상태를 확인합니다. For more on this, see [Sending messages](../../sending/using/confirming-the-send.md) and [Delivery logs](../../sending/using/monitoring-a-delivery.md#delivery-logs).

   이 예에서 메시지 대시보드에는 Adobe Campaign 이 두 개의 푸시 알림을 전송하려고 시도했다는 메시지가 표시됩니다. One were delivered successfully to the device and another one failed. To know why the delivery has errors, click the ![](assets/lp_link_properties.png) button at the bottom of the **[!UICONTROL Deployment]** window.

   ![](assets/push_send_4.png)

1. **[!UICONTROL Deployment]** 창에서 **[!UICONTROL Sending logs]** 탭을 클릭하여 전송된 푸시 알림 및 해당 상태 목록에 액세스합니다. 이 게시에 대해 한 푸시 알림이 성공적으로 전송되었지만 잘못된 장치 토큰으로 인해 다른 알림이 전송되었습니다. 이 구독자는 추후 배달을 통해 블랙리스트에 추가됩니다.

   >[!NOTE]
   >
   >Adobe Campaign에 다운스트림으로 실패하는 원인은 없습니다. APNS 및 FCM와 같은 제공업체의 오류가 발생하는 경우 이러한 이유도 반영됩니다. For more information on provider failures, you can refer to the [Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CommunicatingwithAPNs.html) and [Android](https://firebase.google.com/docs/cloud-messaging/http-server-ref) documentation.

   ![](assets/push_send_6.png)

이제 동적 보고서를 통해 푸시 알림 전달 효과를 측정할 수 있습니다.

**관련 항목:**

* [푸시 알림 보고서](../../reporting/using/push-notification-report.md)
* [워크플로우 내에서 푸시 알림 전송](../../automating/using/push-notification-delivery.md)

