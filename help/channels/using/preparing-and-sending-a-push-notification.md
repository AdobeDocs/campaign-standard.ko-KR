---
title: 푸시 알림 만들기 및 보내기
description: Adobe Campaign에서 단일 전송 푸시 알림을 만들려면 다음 단계를 따르십시오.
audience: channels
content-type: reference
topic-tags: push-notifications
context-tags: delivery,mobileAppContent,back
feature: Push
role: User
level: Intermediate
exl-id: 41b83014-aea9-4ec2-b20e-c0a05bcad503
source-git-commit: affd4f9716235a283df20de5539e43c4832762f7
workflow-type: tm+mt
source-wordcount: '841'
ht-degree: 3%

---

# 푸시 알림 준비 및 보내기{#preparing-and-sending-a-push-notification}

## 알림 준비 {#preparing-the-notification}

Adobe Campaign을 사용하여 푸시 알림을 만드는 단계는 다음과 같습니다.

1. **[!UICONTROL Marketing activities]** 창에서 [새 마케팅 활동을 만듭니다](../../start/using/marketing-activities.md#creating-a-marketing-activity).

   단일 푸시 알림은 [campaign](../../start/using/marketing-activities.md#creating-a-marketing-activity) 또는 Adobe Campaign [홈 페이지](../../start/using/interface-description.md#home-page)에서도 만들 수 있습니다.

   워크플로우에서 푸시 알림 게재 활동을 사용할 수도 있습니다. 이 활동은 [푸시 알림 배달](../../automating/using/push-notification-delivery.md) 섹션에 표시됩니다.

1. **[!UICONTROL Push notification]**&#x200B;을(를) 선택합니다.
1. 템플릿을 선택합니다.

   ![](assets/push_notif_type.png)

   기본적으로 다음 두 템플릿 중 하나를 선택할 수 있습니다.

   * **[!UICONTROL Send push to Campaign profiles]**: 이 템플릿을 사용하여 모바일 애플리케이션을 구독하고 푸시 알림을 받도록 선택한 Adobe Campaign CRM 프로필을 타깃팅합니다. 받는 사람의 이름과 같은 푸시 알림에 [개인화](../../designing/using/personalization.md#inserting-a-personalization-field) 필드를 삽입할 수 있습니다.
   * **[!UICONTROL Send push to app subscribers]**: 이 템플릿을 사용하여 응용 프로그램에서 알림을 받도록 선택한 모든 알려진 익명의 모바일 응용 프로그램 사용자에게 푸시 알림을 보냅니다. 모바일 애플리케이션에서 수집한 데이터를 사용하여 이러한 메시지를 개인화할 수 있습니다.

   다국어 템플릿을 선택할 수도 있습니다. 자세한 내용은 [다국어 푸시 알림 만들기](../../channels/using/creating-a-multilingual-push-notification.md)를 참조하세요.

   템플릿에 대한 자세한 내용은 [템플릿 관리](../../start/using/marketing-activity-templates.md) 섹션을 참조하십시오.

1. 푸시 알림 속성을 입력하고 **[!UICONTROL Associate a Mobile App to a delivery]** 필드에서 모바일 앱을 선택합니다.

   드롭다운에 SDK V4 및 Experience Platform SDK 애플리케이션이 모두 표시됩니다.

   ![](assets/push_notif_properties.png)

   푸시 알림을 캠페인에 연결할 수 있습니다. 이렇게 하려면 이미 생성된 캠페인에서 선택합니다.

1. 다음 화면에서는 특정 모바일 애플리케이션을 구독한 모든 VIP 고객과 같은 대상을 지정할 수 있습니다. 자세한 내용은 [대상자 만들기](../../audiences/using/creating-audiences.md)를 참조하십시오.

   대상자는 이전 단계에서 선택한 모바일 애플리케이션을 기반으로 자동으로 필터링됩니다.

   ![](assets/push_notif_audience.png)

1. 이제 푸시 알림을 사용자 지정할 수 있습니다. 먼저 메시지 스타일을 선택하십시오. **[!UICONTROL Alert/Message/Badge]** 또는 **[!UICONTROL Silent push]**. 푸시 알림 유형은 [푸시 알림 정보](../../channels/using/about-push-notifications.md) 섹션에 설명되어 있습니다.

   푸시 알림의 콘텐츠를 편집하고 고급 옵션을 정의합니다. [푸시 알림 사용자 지정](../../channels/using/customizing-a-push-notification.md)을 참조하세요.

   ![](assets/push_notif_content.png)

   여기에 구성된 푸시 알림 콘텐츠 및 옵션은 페이로드 형태로 모바일 앱에 전달됩니다. 페이로드의 자세한 구조는 [Campaign Standard 푸시 알림 페이로드 구조 이해](../../administration/using/push-payload.md) 기술 문서에 설명되어 있습니다.

1. **[!UICONTROL Create]**&#x200B;를 클릭합니다.

   ![](assets/push_notif_content_2.png)

1. 알림을 보내기 전에 테스트 프로필로 테스트한 다음 게재를 보내기 전에 수신자에게 표시되는 내용을 정확히 확인할 수 있습니다. 게재 요약에서 **[!UICONTROL Audiences]**&#x200B;을(를) 선택하고 **[!UICONTROL Test profiles]** 탭을 클릭합니다.

   테스트 전송에 대한 자세한 내용은 [테스트 프로필](../../sending/using/sending-proofs.md)을 참조하세요.

1. 테스트 프로필을 선택하고 **[!UICONTROL Preview]**&#x200B;을(를) 클릭하여 알림을 표시합니다. 콘텐츠는 테스트 프로필 데이터로 개인화됩니다.
1. 다른 장치에서 푸시 알림 레이아웃을 확인합니다. iPhone, Android phone, iPad 또는 Android tablet을 선택하여 렌더링을 미리 봅니다.

   ![](assets/push_notif_preview.png)

1. **[!UICONTROL Estimated Payload Size]**&#x200B;은(는) 테스트 프로필 데이터를 기반으로 한 예상 값입니다. 실제 페이로드 크기는 다를 수 있습니다. 메시지의 제한은 4KB입니다.

   >[!CAUTION]
   >
   >페이로드 크기가 4KB 제한을 초과할 경우 메시지가 전달되지 않습니다.

개인화 데이터는 메시지 크기에 영향을 줍니다.

## 알림 보내기 {#sending-the-notification}

대상 기준을 정의하여 Adobe Campaign에서 선택한 대상으로 푸시 알림을 보낼 수 있습니다. 아래 예제의 경우, 선택한 대상자는 4명의 타겟팅된 모바일 앱 구독자로 구성됩니다.

1. 대상을 계산하고 알림을 생성하려면 **[!UICONTROL Prepare]**&#x200B;을(를) 클릭하십시오.

   ![](assets/push_send_1.png)

1. 준비가 완료되면 **[!UICONTROL Deployment]** 창에 **[!UICONTROL Target]** 및 **[!UICONTROL To deliver]** KPI가 표시됩니다. **[!UICONTROL Deployment]** 창 아래쪽에 있는 ![](assets/lp_link_properties.png) 단추를 클릭하여 볼 수 있는 예외 항목이 있으므로 **[!UICONTROL To deliver]** 수가 **[!UICONTROL Targeted]** 수보다 적습니다.

   ![](assets/push_send_2.png)

1. **[!UICONTROL Exclusion logs]** 탭에서 보낸 대상에서 제외된 모든 메시지 목록과 이 제외 이유를 확인할 수 있습니다.

   여기에서 모바일 앱 구독자 중 한 명은 차단 목록에 추가하다에 있고 다른 구독자는 프로필이 중복되어 있어 제외되었음을 알 수 있습니다.

   ![](assets/push_send_5.png)

1. 제외된 메시지의 양을 표시하려면 **[!UICONTROL Exclusion causes]** 탭을 클릭하십시오.

   ![](assets/push_send_7.png)

1. 이제 **[!UICONTROL Confirm]**&#x200B;을(를) 클릭하여 푸시 알림 전송을 시작할 수 있습니다.
1. 메시지 대시보드 및 로그를 통해 게재 상태를 확인합니다. 자세한 내용은 [메시지 보내기](../../sending/using/confirming-the-send.md) 및 [게재 로그](../../sending/using/monitoring-a-delivery.md#delivery-logs)를 참조하세요.

   이 예에서는 메시지 대시보드에 Adobe Campaign이 두 개의 푸시 알림을 전송하려고 시도했음을 보여 줍니다(하나는 디바이스에 성공적으로 배달되고 다른 하나는 실패함). 게재 오류가 발생한 이유를 확인하려면 **[!UICONTROL Deployment]** 창 아래쪽에 있는 ![](assets/lp_link_properties.png) 단추를 클릭하십시오.

   ![](assets/push_send_4.png)

1. **[!UICONTROL Deployment]** 창에서 **[!UICONTROL Sending logs]** 탭을 클릭하여 보낸 푸시 알림 및 해당 상태 목록에 액세스합니다. 이 게재의 경우 한 개의 푸시 알림이 성공적으로 전송된 반면 다른 알림은 잘못된 장치 토큰으로 인해 실패했습니다. 그런 다음 이 가입자는 추가 게재에서 차단 목록에 추가하다에 추가됩니다.

   >[!NOTE]
   >
   >Adobe Campaign 다운스트림에 오류가 있을 수 있습니다. apns 및 fcm과 같은 공급자로부터 오류가 발생하는 경우 그 이유도 반영할 것이다. 공급자 오류에 대한 자세한 내용은 [Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CommunicatingwithAPNs.html) 및 [Android](https://firebase.google.com/docs/cloud-messaging/http-server-ref) 설명서를 참조하십시오.

   ![](assets/push_send_6.png)

이제 동적 보고서를 사용하여 푸시 알림 전달의 영향을 측정할 수 있습니다.

**관련 항목:**

* [푸시 알림 보고서](../../reporting/using/push-notification-report.md)
* [워크플로우 내에서 푸시 알림 보내기](../../automating/using/push-notification-delivery.md)
