---
title: Adobe Experience Platform SDK 및 Adobe Campaign 통합 FAQ
description: Adobe Experience Platform SDK 및 Adobe Campaign 통합 FAQ
page-status-flag: never-activated
uuid: 867b1c4b-4c79-4c52-9d0a-ef71993e50a2
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: configuring-channels
discoiquuid: 406c955a-b2d2-4099-9918-95f5fa966067
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5b99fb9fbf8bdac506aeb8a35f30a7ef33aaa7e6
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 3%

---


# Experience Platform SDK 통합 FAQ {#aep-faq}

Experience Platform SDK 응용 프로그램과 함께 푸시 알림 및 인앱 메시지를 전송하려면, 모바일 응용 프로그램을 Adobe Experience Platform SDK에 설정하고 Adobe Campaign에 구성해야 합니다.

아래 섹션에는 이 동기화에 대한 일반적인 질문이 나와 있습니다.

푸시 또는 인앱(In-App)에 대한 자세한 내용은 다음 FAQ를 참조하십시오.

* [푸시 알림 FAQ](../../channels/using/about-push-notifications.md#push-faq)
* [인앱 FAQ](../../channels/using/about-in-app-messaging.md#in-app-faq)
* [Launch 기술 워크플로우와 동기화 FAQ](../../administration/using/syncwithlaunch-faq.md)

## 시작하기 전에 유용한 리소스 {#resource-mobile-property}

Adobe Experience Platform SDK 및 Campaign Standard 통합에 대한 자세한 내용은 아래 리소스를 참조하십시오.

* 실행/모바일 [개요 비디오](https://www.adobe.com/experience-platform/launch.html#acpl-mobile-video)
* 시작/모바일 [팁 및 기법 가이드](https://www.adobe.com/content/dam/www/us/en/experience-platform/launch-tag-manager/pdfs/adobe-cloud-platform-launch-tips-and-tricks-sheet.pdf)

## Adobe Experience Platform SDK 통합을 Adobe Campaign Standard과 Adobe Campaign Classic에서 모두 사용할 수 있습니까? {#aep-validity}

예. Adobe Campaign Standard과 Adobe Campaign Classic에서 모두 [!DNL Adobe Experience Platform SDK] 통합할 수 있습니다. 통합을 활성화하려면 해당 **[!UICONTROL Extension]** 을 [!DNL Adobe Launch] 설치해야 합니다.

자세한 정보는 이 [페이지](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard)를 참조하십시오.

## Adobe Experience Platform SDK 통합이 Adobe Campaign에서 용이하게 하는 기능은 무엇입니까? {#aep-capabilities}

이러한 기능에 대한 자세한 내용은 아래 표를 참조하십시오.

![](assets/faq.png)

>[!NOTE]
>
>[!DNL Places] 통합에는 이벤트를 인앱 메시지(푸시 알림의 경우 N/A)의 트리거로 설정하여 데이터 및 로컬 알림 지원을 통해 프로필을 강화합니다. [!DNL Places] Refer to this [page](../../channels/using/preparing-and-sending-an-in-app-message.md) for more information. <br>[!DNL Places] 제한된 통합에는 데이터와 프로파일 강화가 [!DNL Places] 포함됩니다.

## Adobe Experience Platform SDK 통합이 Adobe Campaign Standard에서 용이하게 하는 사용 사례는? {#aep-use-cases}

지원되는 사용 사례는 다음과 같습니다.

* 캠페인 **[!UICONTROL Mobile Profile]** 에서 가져오기( **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile app (AEP SDK)]** > **[!UICONTROL Mobile Application subscribers]** 탭에서 ECID로 확인)
* Adobe Campaign **[!UICONTROL Mobile Profile]** 의 기능 강화(appSubscriberRcp 테이블 **[!UICONTROL Custom resource Extension]** 필요)
* 푸시 메시지 전송을 위한 푸시 토큰 확보(푸시 메시지를 수신하려면 사용자 옵트인 필요)
* 푸시 및 인앱 메시지 전송
* 푸시 및 인앱 메시지와의 사용자 상호 작용을 추적하고 해당 메시지에 대한 보고서를 제공합니다.

## Campaign에서 모바일 프로필을 획득하려면 어떻게 해야 합니까? {#mobile-profile-campaign}

이렇게 하려면 아래 절차를 따르십시오.

1. In **[!UICONTROL Mobile property]** 을 구성합니다 [!DNL Launch].
1. Adobe Campaign Standard 익스텐션을 설치합니다. 또한 Adobe Campaign Standard 확장 기능을 사용하려면 기본적으로 **[!UICONTROL Mobile Core]**&#x200B;에 설치되어 있는 **[!UICONTROL Profile]** 확장 기능과 **[!UICONTROL Lifecycle]** 익스텐션이 필요합니다 [!DNL Launch].
   * 사용자는 라이프사이클 이벤트의 빈도에 영향을 주는 **[!UICONTROL Mobile Core]** 확장 시 세션 시간 초과를 구성해야 합니다.
   * 확장이 구성되면 사용자는 iOS용 코드 및 Android용 Grade를 사용하여 모바일 앱에 적절한 종속성을 추가해야 합니다. 여기 [에 있는 길을 따라가세요](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard).
   * 항상 최신 버전의 라이브러리를 사용할 수 있습니다.
   * 모바일 앱에서 등록, **[!UICONTROL Campaign]****[!UICONTROL UserProfile]**, **[!UICONTROL Identity]**&#x200B;및 **[!UICONTROL Lifecycle]** 확장 **[!UICONTROL Signal]** 기능을 사용할 수 있습니다. 여기 [에 있는 길을 따라가세요](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard#register-the-campaign-standard-extension-with-mobile-core).
   * 익스텐션이 등록되면 ACPCore를 시작합니다. Android의 경우 setApplication onCreate()를 사용하십시오. Launch에서 모바일 속성에 대한 모바일 설치 지침에 제공된 지침을 따르십시오.
   * 다음 SDK API도 필요합니다. Android용 API와 iOS용 API에 대해 [여기](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle/lifecycle-extension-in-android) 설명된 대로 라이프사이클 시작 및 일시 중지 API를 구현합니다.
1. Adobe Campaign Standard **[!UICONTROL Mobile Property]** 에서 a를 구성합니다. 이 절차를 [따르십시오](../../administration/using/configuring-a-mobile-application.md#channel-specific-config).

## Campaign에서 모바일 프로필을 강화하려면 어떻게 해야 합니까? {#enrich-mobile-profile}

CollectPII 포스트백을 구성하고(이 [페이지](https://helpx.adobe.com/campaign/kb/config-app-in-launch.html#PIIpostback)참조) SDK에서 CollectPII API를 구현해야 합니다(이 [페이지](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/mobile-core-api-reference#collect-pii)참조).

## CollectPII 전화는 얼마나 자주 울려야 합니까? {#collect-pii}

CollectPII 호출의 목적은 캠페인의 모바일 프로필을 강화시키는 것입니다. 사용 사례와 비즈니스 요구 사항에 따라 고객이 프로필에 추가하고자 하는 의미 있는 정보가 새로 추가될 때마다 이러한 정보를 실행해야 합니다.

## 여러 트리거 이벤트에 대한 CollectPII 호출을 실행할 수 있습니까? {#collect-pii-calls}

예. 비즈니스의 필요에 따라, 앱에서 사용자 로그인에 대한 응답으로 CollectPII 호출을 실행하거나, 특정 또는 라이프사이클 이벤트나 지리적 위치 등을 입력하는 사용자를 구매할 수 있습니다. 요약하자면, 프로필 농축에 사용할 정보를 생성하는 앱과의 상호 작용입니다.

## 모든 모바일 이벤트에 대한 CollectPII 호출을 실행할 수 있습니까? {#collect-pii-events}

CollectPII 호출의 빈도와 디자인은 비즈니스 요구 사항에 따라 지정되어야 하며 DB에서 추가 로드를 생성하므로 맹목적으로 발사되어서는 안 됩니다.

### Campaign 또는 Launch에서 Adobe Experience Platform 앱에 액세스하려고 하면 사용할 수 없는 속성이 오류가 발생하는 경우가 있습니다. {#aep-error}

알려진 문제이며 토큰 만료 때문에 발생합니다. 로그인 후 로그인하십시오.

## Adobe Experience Platform SDK(이전의 SDK V5)에 대한 자세한 내용을 살펴보려면 유용한 리소스 권장 사항은 무엇입니까?{#resource-aep}

아래 리소스를 확인하십시오.

* Experience Platform SDK [설명서](https://aep-sdks.gitbook.io/docs/)
* 시작 및 Experience Platform SDK [설명서](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property)
* Experience Platform SDK [설명서로 업그레이드](https://aep-sdks.gitbook.io/docs/resources/upgrading-to-aep)
* Github Experience Platform SDK [설명서](https://github.com/Adobe-Marketing-Cloud/acp-sdks/)
