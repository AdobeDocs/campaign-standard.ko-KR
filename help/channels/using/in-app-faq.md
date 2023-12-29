---
title: 인앱 FAQ
description: 인앱 메시지에 대한 FAQ
audience: channels
content-type: reference
topic-tags: in-app-messaging
context-tags: delivery,triggers,back
feature: In App
role: User
exl-id: 0101773d-b109-49a3-89d4-b4bb226d9ebd
source-git-commit: 597ece8d833a216f0540f801461b08fdc9865024
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 0%

---

# 인앱 FAQ {#in-app-faq}

## Adobe Campaign Standard의 인앱 채널에 대해 자세히 알아볼 수 있는 유용한 리소스 권장 사항은 무엇입니까? {#resources-inapp}

아래 리소스를 확인하십시오.

* [비디오 Tutorials](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/communication-channels/mobile/in-app/in-app-message-overview.html)
* [블로그 게시물](https://theblog.adobe.com/get-more-out-of-the-new-in-app-message-channel-from-adobe-campaign/)
* [커뮤니티 페이지](https://experienceleaguecommunities.adobe.com/t5/adobe-campaign-standard/ct-p/adobe-campaign-standard-community)

## Campaign 확장 API setLinkageField 및 resetLinkageField의 목적은 무엇입니까? {#extensions-apis}

인앱 메시지는 Campaign에서 SDK에 의해 가져오므로, PII 데이터가 포함된 인앱 메시지가 악의적인 손에 들어가지 않도록 하는 보안 메커니즘을 제공하려고 합니다. 따라서 디바이스로의 메시지 보안 전달을 보장하기 위해 다음과 같은 메커니즘이 마련되어 있습니다.

* 고객은 모바일 프로필 필드(appSubscriberRcp 테이블) 필드를 개인적이며 특정 정보가 안전하게 전달되도록 하려는 경우 민감으로 표시합니다.
* 이렇게 표시된 필드는 추가 보안 메커니즘이 내장된 프로필 템플릿(appSubscriber 템플릿 또는 브로드캐스트 템플릿 아님)에서만 사용할 수 있습니다.
* 프로필 템플릿을 사용하여 작성한 메시지는 사용자가 앱에 로그인한 경우에만 제공될 수 있습니다.
* 이 안전한 핸드셰이크를 용이하게 하기 위해 모바일 앱 개발자는 setLinkageField API를 사용하여 추가 인증 세부 정보를 전달해야 합니다. 연결 필드는 appSubscriberRcp 테이블을 확장하는 동안 모바일 프로필과 CRM 프로필 간의 링크로 식별되는 필드입니다.
* 사용자가 resetLinkageField를 사용하여 앱에서 로그아웃할 때 디바이스에 저장된 인앱 메시지 및 resetLinkagefields를 플러시해야 합니다. 이렇게 하면 다른 사용자가 앱에 로그인하는 경우 이전 사용자를 위한 메시지가 표시되지 않습니다.
* 을(를) 참조하십시오 [모바일 SDK API](https://developer.adobe.com/client-sdks/documentation/adobe-campaign-standard/api-reference/) 이 보안 메커니즘을 구현하려면 client side를 사용하십시오.

## Campaign에서 인앱 보고를 활성화하려면 어떻게 해야 합니까? {#enable-inapp-reporting}

인앱 추적 포스트백을 구성해야 합니다. 지침을 찾을 수 있음 [여기](../../administration/using/configuring-rules-launch.md#inapp-tracking-postback).

로컬 알림 추적을 구현하려면 다음을 참조하십시오. [페이지](../../administration/using/local-tracking.md).

## 인앱 채널에 사용할 수 있는 보고서 {#report-inapp}

Adobe Campaign for In-App channel에서 기본 보고서를 사용할 수 있습니다. 다음을 참조하십시오. [설명서](../../reporting/using/in-app-report.md).

이 항목 보기 [페이지](../../reporting/using/indicator-calculation.md#in-app-delivery) 를 사용하여 각 인앱 지표를 계산하는 방법을 이해할 수 있습니다.

## 푸시와 유사한 인앱에 대한 다국어 콘텐츠 변형을 지원합니까? {#multilingual-inapp}

현재 인앱 메시지에 사용할 수 있는 다국어 템플릿이 없습니다.

그러나 인앱 메시지를 영어 이외의 언어로 보내는 것이 목적인 경우 콘텐츠를 사용 가능한 텍스트 상자에 직접 붙여넣을 수 있습니다.

![](assets/faq_inapp.png)

## Campaign 개인화 필드를 사용자 지정 HTML에 추가할 수 있습니까? {#custom-html-inapp}

아니요. 아직 지원되지 않습니다.

## 경고 메시지를 구성했지만 장치에 표시되지 않습니다. {#alert-message}

경고 메시지의 경우 하나 이상의 해제 버튼(기본 또는 보조에 해제 작업이 있어야 함)이 필요합니다. 그렇지 않으면 메시지를 저장할 수는 있지만 수신되지 않습니다.

## 로컬 알림 iOS 사용자 정의 사운드가 재생되지 않는 경우 기본 사운드가 재생됩니까? {#local-notification-sound}

iOS에서 사용자 정의 사운드의 경우 로컬 알림을 생성할 때 확장자가 인 파일 이름을 제공해야 합니다(예: sound.caf). 이 확장이 제공되지 않으면 기본 사운드가 사용됩니다.

## 인앱 메시지에서 딥링크가 지원됩니까? {#inapp-deeplinks}

예. 딥링크는 인앱 메시지에서 지원됩니다. 딥링크는 다음을 포함해야 합니다.

* 딥링크가 작동하려면 게재 추적을 비활성화해야 한다는 언어입니다.
* 딥링크 추적을 수행할 수 있는 파트너로서 Branch와 함께 Appsflyer를 제공합니다. 분기 및 Adobe Campaign Standard 통합에 대한 자세한 내용은 다음을 참조하십시오. [페이지](https://help.branch.io/using-branch/docs/adobe-campaign-standard-1).

## 사용자가 푸시 알림에서 앱을 실행할 때 인앱 메시지가 트리거될 수 있습니까? {#inapp-push-trigger}

예. 이러한 메시지는 데이지 체인 메시지라고도 합니다. 아래 프로세스를 따르십시오.

1. 인앱 메시지를 만듭니다.

1. 사용자 지정 이벤트를 정의하고 이 IAM에 대한 이벤트 트리거로 선택합니다(예: &quot;Trigger from fall preview Push&quot;).

1. 푸시 메시지를 작성할 때 IAM을 트리거하는 데 사용되는 이벤트로 값을 설정할 수 있는 사용자 지정 변수를 정의합니다(예: 키 = &quot;inappkey&quot; 및 값 = &quot;Trigger from fall preview Push&quot;).

1. 모바일 앱 코드에서 다음과 같이 이벤트 트리거를 구현합니다.

   ![](assets/faq_inapp_2.png)
