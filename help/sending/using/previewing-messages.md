---
title: 메시지 미리 보기
description: 콘텐츠 편집기 또는 이메일 디자이너에서 메시지를 미리 보는 방법을 알아봅니다.
audience: sending
content-type: reference
topic-tags: preparing-and-testing-messages
feature: Seed Address
role: User
level: Intermediate
exl-id: ac8c1265-f530-4438-ab2d-3ca17615ca85
source-git-commit: ee7539914aba9df9e7d46144e437c477a7e52168
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 15%

---

# 게재 미리 보기 {#previewing-messages}

## 전자 메일 미리 보기 {#previewing-emails}

Campaign Standard을 사용하면 메시지를 보내기 전에 미리 볼 수 있으므로 개인화와 수신자가 보게 되는 방식을 확인할 수 있습니다.

메시지 미리 보기는 메시지 대상에 추가하는 **테스트 프로필**&#x200B;을 사용하여 수행됩니다.

**이메일** 메시지의 경우 Campaign Standard을 사용하면 테스트 프로필이 아닌 타겟팅된 프로필을 사용하여 메시지를 미리 볼 수 있습니다. 이를 통해 특정 프로필에서 받게 될 메시지의 정확한 모습을 확인할 수 있습니다. 자세한 내용은 [타겟팅된 프로필을 사용하여 이메일 메시지 테스트](../../sending/using/testing-messages-using-target.md)를 참조하십시오.

테스트 프로필을 사용하여 메시지를 미리 보려면 다음 단계를 수행합니다.

1. [이메일 디자이너](../../designing/using/designing-content-in-adobe-campaign.md)에서 **[!UICONTROL Preview]** 단추를 클릭합니다.

   ![](assets/sending_preview.png)

   데스크탑 보기와 전자 메일의 응답형 모바일 보기가 나란히 표시됩니다.

1. 각 미리 보기 중에 자동 스팸 방지 검사가 수행됩니다. 경고에 대한 자세한 내용을 보려면 **[!UICONTROL Anti-spam analysis]** 단추를 클릭하십시오.

   ![](assets/sending_anti-spam_analysis.png)

1. **[!UICONTROL Change profile]** 단추를 선택하여 개인화 요소를 테스트할 테스트 프로필을 선택합니다.

   ![](assets/sending_test-profile.png)

1. **[!UICONTROL Preview]** 모드를 종료하려면 화면 왼쪽 상단에 있는 **[!UICONTROL Edit]** 버튼을 클릭합니다.

   ![](assets/sending_preview_edit.png)

**관련 항목**

* [테스트 프로필 관리](../../audiences/using/managing-test-profiles.md)
* [타기팅된 프로필을 사용한 이메일 메시지 테스트](../../sending/using/testing-messages-using-target.md)
* [증명 보내기](../../sending/using/sending-proofs.md)

## SMS 메시지 미리 보기 {#previewing-sms}

**SMS** 메시지의 경우, Campaign Standard에서 테스트 프로필을 사용하여 메시지를 미리 볼 수 있습니다. 이를 통해 특정 프로필에서 받게 될 메시지의 정확한 모습을 확인할 수 있습니다. 자세한 내용은 [테스트 프로필 관리](../../audiences/using/managing-test-profiles.md)를 참조하십시오.

테스트 프로필을 사용하여 SMS 메시지를 미리 보려면 다음 단계를 수행합니다.

1. SMS 메시지의 **[!UICONTROL Properties]** 을(를) 입력하고 대상자를 선택하면 게재를 개인화할 수 있습니다. 자세한 내용은 [섹션](../../channels/using/personalizing-sms-messages.md)을 참조하십시오.

   ![](assets/sms_preview.png)

1. 콘텐츠를 개인화한 후 **[!UICONTROL Create]** 을 클릭하여 **[!UICONTROL Summary]** 창에 액세스합니다.

1. **[!UICONTROL Summary]** 창에서 **[!UICONTROL Content]** 을 클릭하여 게재 미리 보기를 시작합니다.

   ![](assets/sms_preview_2.png)

1. 도구 모음에서 **[!UICONTROL Preview]** 을 클릭합니다.

   ![](assets/sms_preview_3.png)

1. **[!UICONTROL Change profile]** 을 클릭하여 테스트 프로필을 선택하고 **[!UICONTROL Confirm]** 을 클릭합니다.

   ![](assets/sms_preview_4.png)

이제 선택한 테스트 프로필에 따라 메시지의 정확한 표시를 볼 수 있습니다.

**관련 항목**

* [SMS 메시지 기본 정보](../../channels/using/about-sms-messages.md)
* [SMS 메시지 만들기](../../channels/using/creating-an-sms-message.md)
* [SMS 메시지 개인화](../../channels/using/personalizing-sms-messages.md)

## 푸시 알림 미리 보기 {#previewing-push}

**푸시 알림**&#x200B;의 경우 Campaign Standard에서 테스트 프로필을 사용하여 메시지를 미리 볼 수 있습니다. 이를 통해 특정 프로필에서 받게 될 메시지의 정확한 모습을 확인할 수 있습니다. 자세한 내용은 [테스트 프로필 관리](../../audiences/using/managing-test-profiles.md)를 참조하십시오.

테스트 프로필을 사용하여 푸시 알림을 미리 보려면 다음 단계를 수행합니다.

1. 푸시 알림의 **[!UICONTROL Properties]** 을 입력하고 대상을 선택하면 게재를 개인화할 수 있습니다. 자세한 내용은 [푸시 알림 사용자 정의](../../channels/using/customizing-a-push-notification.md)를 참조하십시오.

1. 콘텐츠를 개인화한 후 미리 보기 창에서 장치 및 OS에 따라 푸시 알림의 렌더링을 직접 확인할 수 있습니다.

   ![](assets/push_preview.png)

1. 테스트 프로필을 사용하여 푸시 알림을 미리 보려면 **[!UICONTROL Preview with test profile]** 을 클릭합니다.

   ![](assets/push_preview_2.png)

1. 테스트 프로필을 선택하고 **[!UICONTROL Confirm]** 을 선택합니다.

이제 선택한 테스트 프로필에 따라 메시지의 정확한 표시를 볼 수 있습니다.

![](assets/push_preview_3.png)

**관련 항목**

* [푸시 알림 기본 정보](../../channels/using/about-push-notifications.md)
* [푸시 알림 준비 및 보내기](../../channels/using/preparing-and-sending-a-push-notification.md)
* [푸시 알림 사용자 정의](../../channels/using/customizing-a-push-notification.md)

## 인앱 메시지 미리 보기 {#previewing-in-app}

**In-App**&#x200B;의 경우 Campaign Standard을 통해 테스트 프로필을 사용하여 메시지를 미리 볼 수 있습니다. 이를 통해 특정 프로필에서 받게 될 메시지의 정확한 모습을 확인할 수 있습니다. 자세한 내용은 [테스트 프로필 관리](../../audiences/using/managing-test-profiles.md)를 참조하십시오.

테스트 프로필을 사용하여 인앱 메시지를 미리 보려면 다음 단계를 수행합니다.

1. 인앱 메시지의 **[!UICONTROL Properties]**&#x200B;을 입력하고 대상을 선택하고 **[!UICONTROL Triggers]**&#x200B;을(를) 설정하면 게재를 개인화할 수 있습니다. 자세한 내용은 [인앱 메시지 사용자 지정](../../channels/using/customizing-an-in-app-message.md)을 참조하십시오.

1. 콘텐츠를 개인화한 후 미리 보기 창에서 장치 및 OS에 따라 인앱 메시지 렌더링을 직접 확인할 수 있습니다.

   ![](assets/in_app_preview.png)

1. 테스트 프로필을 사용하여 인앱 메시지를 미리 보려면 **[!UICONTROL Preview]** 을 클릭합니다.

   ![](assets/in_app_preview_2.png)

1. 테스트 프로필을 선택하고 **[!UICONTROL Confirm]** 을 선택합니다.

이제 선택한 테스트 프로필에 따라 메시지의 정확한 표시를 볼 수 있습니다.

![](assets/in_app_preview_3.png)

**관련 항목**

* [인앱 메시지 기본 정보](../../channels/using/about-in-app-messaging.md)
* [인앱 메시지 준비 및 보내기](../../channels/using/preparing-and-sending-an-in-app-message.md)
* [인앱 메시지 사용자 정의](../../channels/using/customizing-an-in-app-message.md)
