---
title: 인앱 메시지 기본 정보
description: 인앱 메시지를 사용하여 모바일 애플리케이션 내에 메시지 또는 경고를 표시합니다.
page-status-flag: never-activated
uuid: 6784cdfc-6db9-41dd-9fbb-2e756a5bcb5f
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: in-app-messaging
discoiquuid: a4168cfb-22bf-4ab3-b9d8-6e76e1bdc055
context-tags: delivery,triggers,back
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 4efc42fd6b656c7723ed52f704c801113f9b3817
workflow-type: tm+mt
source-wordcount: '930'
ht-degree: 28%

---


# 인앱 메시지 기본 정보{#about-in-app-messaging}

인앱 메시지는 사용자가 모바일 애플리케이션 내에서 활성 상태일 때 메시지를 표시할 수 있는 메시지 채널입니다. 이 메시지 유형은 사용자 전화의 알림 센터로 전달되는 푸시 알림과 상호 보완적으로 사용할 수 있습니다. 푸시 알림 채널에 대한 자세한 내용은 이 [섹션](../../channels/using/about-push-notifications.md)을 참조하십시오.

이 채널을 사용하려면 모바일 애플리케이션을 Adobe Experience Platform SDK와 통합해야 합니다. Adobe Campaign에서 인앱 게재를 사용하려면 해당 앱을 Adobe Experience Platform Launch에서 활성화해야 합니다.

![](assets/launch_campaign.png)

Experience Platform SDK를 활용하는 모바일 애플리케이션에서 인앱 메시지를 보내기에 앞서 다음 사전 요구 사항을 충족해야 합니다.

1. Adobe Campaign에서 **[!UICONTROL In-App]** 채널에 액세스할 수 있는지 확인합니다. 이 채널에 액세스할 수 없는 경우 계정 팀에 문의하십시오.

1. Adobe Campaign Standard와 Experience Cloud SDK 애플리케이션을 함께 사용하는 모바일 사용 사례를 활용하려면 Adobe Experience Platform Launch에서 모바일 앱을 제작하고 Adobe Campaign Standard에서 구성해야 합니다. 단계별 안내서는 이 [페이지](https://helpx.adobe.com/kr/campaign/kb/configuring-app-sdk.html)를 참조하십시오.

1. 구성하고 나면 이제 인앱 메시지를 준비할 수 있습니다. 자세한 정보는 이 [페이지](../../channels/using/preparing-and-sending-an-in-app-message.md#preparing-your-in-app-message)를 참조하십시오.

1. 그런 다음 [인앱 메시지](../../channels/using/customizing-an-in-app-message.md)를 보낼지 [로컬 알림 메시지 유형 사용자 정의](../../channels/using/customizing-an-in-app-message.md#customizing-a-local-notification-message-type)를 보낼지 결정할 수 있습니다.

1. 이제 게재를 보낼 준비가 되었습니다. 자세한 내용은 이 [페이지](../../channels/using/preparing-and-sending-an-in-app-message.md#sending-your-in-app-message)를 참조하십시오.

**관련 컨텐츠:**

* [인앱 보고서](../../reporting/using/in-app-report.md)
* [Adobe Campaign Standard에서 지원되는 모바일 사용 사례](https://helpx.adobe.com/kr/campaign/kb/configure-launch-rules-acs-use-cases.html)
* [Campaign Standard Mobile 안내서](https://helpx.adobe.com/kr/campaign/kb/acs-mobile.html)

## 인앱 FAQ {#in-app-faq}

### Adobe Campaign Standard의 인앱 채널에 대해 자세히 알아보려면 유용한 리소스 권장 사항은 무엇입니까? {#resources-inapp}

아래 리소스를 확인하십시오.

* [비디오 Tutorials](https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/communication-channels/mobile/in-app/in-app-message-overview.html)
* [블로그 게시물](https://theblog.adobe.com/get-more-out-of-the-new-in-app-message-channel-from-adobe-campaign/)
* [커뮤니티 페이지](https://experienceleaguecommunities.adobe.com/t5/adobe-campaign-standard/ct-p/adobe-campaign-standard-community)

### Campaign 확장 API setLinkageField 및 resetLinkageField의 목적은 무엇입니까? {#extensions-apis}

인앱 메시지는 Campaign에서 SDK로 가져오므로 PII 데이터가 포함된 인앱 메시지가 악의적인 사용자에게 노출되지 않도록 하는 안전한 메커니즘을 제공하고자 합니다. 따라서, Adobe는 장치에 메시지를 안전하게 배달할 수 있도록 다음 메커니즘을 제공합니다.

* 고객은 이 특정 정보가 안전하게 전달되도록 하려면 모바일 프로필 필드(appSubscriberRcp 테이블) 필드를 [개인] 및 [민감도]로 표시합니다.
* 이렇게 표시된 필드는 추가 보안 메커니즘을 내장된 프로필 템플릿(appSubscriber 템플릿 또는 Broadcast 템플릿 아님)에서만 사용할 수 있습니다.
* 프로필 템플릿을 사용하여 작성한 메시지는 사용자가 앱에 로그인한 경우에만 제공됩니다.
* 이러한 안전한 핸드셰이크를 원활하게 하려면 모바일 앱 개발자는 setLinkageField API를 사용하여 추가 인증 세부 사항을 전달해야 합니다. 링크 필드는 appSubscriberRcp 테이블을 확장하면서 Mobile Profile과 CRM Profile 간의 링크로 식별되는 필드입니다.
* 사용자가 resetLinkageField를 사용하여 앱에서 로그아웃하면 장치에 저장된 인앱 메시지를 플러시하고 resetLinkagefields를 플러시해야 합니다. 따라서 다른 사용자가 앱에 로그인하면 이전 사용자에 대한 메시지가 표시되지 않습니다.
* 이 보안 메커니즘 클라이언트 측 [을 구현하려면 모바일 SDK API를](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard/adobe-campaign-standard-api-reference) 참조하십시오.

### Campaign에서 인앱 보고를 활성화하려면 어떻게 해야 합니까? {#enable-inapp-reporting}

인앱 추적 포스트백을 구성해야 합니다. 지침은 [여기에서 확인할 수 있습니다](https://helpx.adobe.com/campaign/kb/config-app-in-launch.html#InApptrackingpostback).

로컬 알림 추적을 구현하려면 이 [페이지를 참조하십시오](../../administration/using/local-tracking.md).

### 인앱 채널에 사용할 수 있는 보고서는 무엇입니까? {#report-inapp}

기본 보고서는 인앱 채널에 대해 Adobe Campaign에서 사용할 수 있습니다. 이 [설명서를 참조하십시오](../../reporting/using/in-app-report.md).

각 In-App 지표가 계산되는 방법을 이해하려면 이 [페이지를](../../reporting/using/indicator-calculation.md#in-app-delivery) 참조하십시오.

### In-App에 대해 Push와 유사한 다중 언어 컨텐츠 변형을 지원합니까? {#multilingual-inapp}

이제 인앱 메시지에 사용할 수 있는 다중 언어 템플릿이 없습니다.

하지만, 목적이 영어 이외의 언어로 인앱 메시지를 보내는 것인 경우 해당 컨텐츠를 사용 가능한 텍스트 상자에 직접 붙여넣을 수 있습니다.

![](assets/faq_inapp.png)

### 캠페인 개인화 필드를 사용자 지정 HTML에 추가할 수 있습니까? {#custom-html-inapp}

아니요, 아직 지원되지 않습니다.

### 경고 메시지를 구성했지만 장치에 표시되지 않습니다. {#alert-message}

경고 메시지의 경우 [해제] 단추를 하나 이상 선택해야 합니다(주 또는 보조 단추에는 작업 해제). 그렇지 않으면 메시지를 저장할 수 있지만 수신되지 않습니다.

### 로컬 알림 iOS 사용자 지정 사운드가 재생되지 않는 경우; 기본 사운드가 재생됩니까? {#local-notification-sound}

iOS에서 사용자 정의 사운드의 경우 로컬 알림을 만들 때 확장자와 함께 파일 이름을 제공해야 합니다(예: sound.caf). 이 확장을 제공하지 않으면 기본 사운드가 사용됩니다.

### 인앱 메시지에서는 링크가 지원됩니까? {#inapp-deeplinks}

예, 기본 링크는 인앱 메시지에서 지원됩니다. 링크는 다음을 포함해야 합니다.

* 배달 추적이 제대로 작동하도록 하기 위해 배달 추적을 비활성화해야 한다고 말하는 언어입니다.
* 링크 추적을 수행할 수 있는 파트너로 분기를 추가합니다. 분기 및 Adobe Campaign Standard 통합에 대한 자세한 내용은 이 [페이지를 참조하십시오](https://help.branch.io/using-branch/docs/adobe-campaign-standard-1).

### 사용자가 푸시 알림에서 앱을 실행할 때 인앱 메시지가 트리거될 수 있습니까? {#inapp-push-trigger}

예, 이 메시지들은 데이지 체인 메시지라고도 합니다. 아래 절차를 따르십시오.

1. 인앱 메시지 만들기.

1. 사용자 지정 이벤트를 정의하고 이 IAM(예: &quot;가을 미리보기 푸시로부터 트리거&quot;

1. 푸시 메시지를 작성할 때, 값을 IAM을 트리거하는 이벤트로 설정할 수 있는 사용자 지정 변수를 정의합니다(예: 키 = &quot;inappkey&quot; 및 value = &quot;가을 미리보기 푸시에서 트리거&quot;).

1. 모바일 앱 코드에서 다음과 같이 이벤트 트리거를 구현합니다.

   ![](assets/faq_inapp_2.png)
