---
title: 인앱 메시지 사용자 지정
description: 다양한 옵션을 사용하여 인앱 메시지를 사용자 지정하는 방법을 배웁니다.
page-status-flag: never-activated
uuid: 1d9c08ed-4de5-440d-bf51-4a437eec67d5
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: in-app-messaging
discoiquuid: c9c3e033-e319-447b-8d87-ff7dd4941876
context-tags: delivery,inAppContent,back
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 9c812b0b622b82ba7aa382f04edb7a2a3f717cd4
workflow-type: tm+mt
source-wordcount: '1080'
ht-degree: 100%

---


# 인앱 메시지 사용자 지정{#customizing-an-in-app-message}

인앱 메시지를 세밀하게 조정하려면 Adobe Campaign을 사용하여 인앱을 디자인하는 동안 고급 옵션 세트에 액세스할 수 있습니다.

인앱 콘텐츠 편집기를 사용하면 다음의 두 가지 인앱 메시지 모드 중에서 선택할 수 있습니다.

* [메시지 템플릿](#customizing-with-a-message-template): 이 템플릿을 사용하면 이미지 또는 비디오 및 작업 버튼을 사용하여 인앱을 완벽하게 사용자 지정할 수 있습니다.
* [사용자 지정 메시지](#customizing-with-a-custom-html-message): 이 템플릿을 사용하면 사용자 지정 HTML을 가져올 수 있습니다.

![](assets/inapp_customize_1.png)

>[!NOTE]
>
> 인앱 메시지 렌더링은 Android API 19 이상 버전에서만 지원됩니다.

**관련 항목:**

* [인앱 메시지 보내기](../../channels/using/preparing-and-sending-an-in-app-message.md#sending-your-in-app-message)
* [인앱 보고](../../reporting/using/in-app-report.md)
* [로컬 알림 추적 구현](../../administration/using/local-tracking.md)

## 메시지 템플릿으로 사용자 지정 {#customizing-with-a-message-template}

### 레이아웃 {#layout}

**[!UICONTROL Layout]** 드롭다운은 메시징 요구 사항에 따라 선택할 수 있는 4가지 옵션을 제공합니다.

* **[!UICONTROL Full page]**: 이러한 유형의 레이아웃은 대상 디바이스의 전체 화면을 포함합니다.

   미디어(이미지, 비디오), 텍스트 및 버튼 구성 요소를 지원합니다.

* **[!UICONTROL Large modal]**: 이 레이아웃은 큰 경고 스타일 창에 나타나며 백그라운드에서 애플리케이션이 계속 표시됩니다.

   미디어(이미지, 비디오), 텍스트 및 버튼 구성 요소를 지원합니다.

* **[!UICONTROL Small modal]**: 이 레이아웃은 작은 경고 유형 창으로 나타나며 백그라운드에서 애플리케이션이 계속 표시됩니다.

   미디어(이미지, 비디오), 텍스트 및 버튼 구성 요소를 지원합니다.

* **[!UICONTROL Alert]**: 이 유형의 레이아웃은 기본 OS 경고 메시지로 표시됩니다.

   텍스트 및 버튼 구성 요소만 지원할 수 있습니다.

* **[!UICONTROL Local notification]**: 이 유형의 레이아웃은 배너 메시지로 표시됩니다.

   사운드, 텍스트 및 대상만 지원할 수 있습니다. 로컬 알림에 대한 자세한 내용은 [로컬 알림 메시지 유형 사용자 지정](#customizing-a-local-notification-message-type)을 참조하십시오.

휴대폰, 태블릿, 플랫폼(예: Android 또는 iOS)과 같은 다양한 디바이스와 방향(예: 컨텐츠 편집기의 오른쪽 창에서 가로 또는 세로)에서 각 유형의 레이아웃을 미리 볼 수 있습니다.

![](assets/inapp_customize_4.png)

### 미디어 {#media}

**[!UICONTROL Media]** 드롭다운을 사용하면 인앱 메시지에 미디어를 추가하여 최종 사용자를 위한 매력적인 경험을 만들 수 있습니다.

1. 이미지와 비디오 중에서 **[!UICONTROL Media Type]**&#x200B;을 선택합니다.
1. **[!UICONTROL Image]** 미디어 유형의 경우, 지원되는 형식을 기준으로 **[!UICONTROL Media URL]** 필드에 URL을 입력합니다.

   필요한 경우 장치가 오프라인 상태인 경우, 사용할 수 **[!UICONTROL Bundled image]**&#x200B;로 가는 경로를 입력할 수도 있습니다.

   ![](assets/inapp_customize_5.png)

1. **[!UICONTROL Video]** 미디어 유형의 경우, **[!UICONTROL Media URL]** 필드에 URL을 입력합니다.

   그런 다음 대상 디바이스에서 비디오를 다운로드하는 동안 또는 사용자가 재생 버튼을 누를 때까지 사용할 **[!UICONTROL Video poster]**&#x200B;을(를) 입력합니다.

   ![](assets/inapp_customize_6.png)

### 텍스트 {#text}

필요한 경우 인앱 메시지에 메시지 제목과 콘텐츠를 추가할 수도 있습니다. 더 나은 인앱 메시지의 개인화를 위해 콘텐츠에 다양한 개인화 필드, 콘텐츠 블록 및 동적 텍스트를 추가할 수 있습니다.

1. **[!UICONTROL Text]** 드롭다운에서 **[!UICONTROL Message title]** 필드에 제목을 추가합니다.

   ![](assets/inapp_customize_9.png)

1. **[!UICONTROL Message content]** 필드에 콘텐츠를 추가합니다.
1. 텍스트를 추가로 개인화하려면 ![](assets/edit_darkgrey-24px.png) 아이콘을 클릭하여 개인화 필드를 추가합니다.

   ![](assets/inapp_customize_8.png)

1. 메시지 콘텐츠를 입력하고 필요한 경우에는 개인화 필드를 추가합니다.

   개인화 필드에 대한 자세한 내용은 이 [섹션](../../designing/using/personalization.md#inserting-a-personalization-field)을 참조하십시오.

   ![](assets/inapp_customize_10.png)

1. 미리 보기 창에서 메시지 콘텐츠를 확인합니다.

   ![](assets/inapp_customize_11.png)

### 버튼 {#buttons}

인앱 메시지에 최대 2개의 버튼을 추가할 수 있습니다.

1. **[!UICONTROL Buttons]** 드롭다운에서 **[!UICONTROL Primary]** 카테고리에 첫 번째 버튼의 텍스트를 입력합니다.

   ![](assets/inapp_customize_12.png)

1. **[!UICONTROL Dismiss]**&#x200B;와(과) **[!UICONTROL Redirect]**&#x200B;의 두 작업 중 어느 작업을 기본 버튼에 할당할지 선택합니다.
1. 필요한 경우, **[!UICONTROL Secondary]** 카테고리에서 텍스트를 입력하여 인앱에 두 번째 버튼을 추가합니다.
1. 두 번째 버튼에 연결된 작업을 선택합니다.
1. **[!UICONTROL Redirect]** 작업을 선택한 경우, **[!UICONTROL Destination URL]** 필드에 웹 URL이나 딥 링크를 입력합니다.

   ![](assets/inapp_customize_13.png)

1. **[!UICONTROL Redirect]** 작업을 선택한 경우, **[!UICONTROL Destination URL]** 필드에 웹 URL이나 딥 링크를 입력합니다.
1. 미리 보기 창에서나 미리 보기 버튼을 클릭하여 메시지 콘텐츠를 확인합니다.

   [인앱 메시지 미리 보기](#previewing-the-in-app-message) 페이지를 참조하십시오 .

   ![](assets/inapp_customize_11.png)

### 설정 {#settings}

1. **[!UICONTROL Settings]** 카테고리에서 배경색의 명암을 선택합니다.
1. 사용자에게 인앱 메시지를 취소할 수 있는 방법을 제공하기 위해 **[!UICONTROL Show close button]** 옵션을 사용하여 닫기 버튼의 표시 여부를 선택합니다.
1. 버튼 맞춤이 **[!UICONTROL Button alignment]** 옵션을 사용하여 가로 또는 세로로 표시되는지 선택합니다.
1. 인앱 메시지가 몇 초 후 자동으로 취소되는지 여부를 선택합니다.

   ![](assets/inapp_customize_7.png)

## 로컬 알림 메시지 유형 사용자 지정 {#customizing-a-local-notification-message-type}

로컬 알림은 특정 시간과 이벤트에 따라 앱에 의해서만 트리거할 수 있습니다. 로컬 알림은 인터넷에 접속하지 않고도 앱에서 발생하는 일을 사용자에게 알립니다.
로컬 알림을 추적하는 방법을 배우려면 이 [페이지](../../administration/using/local-tracking.md)를 참조하십시오.

로컬 알림을 사용자 지정하는 방법:

1. **[!UICONTROL Content]** 페이지에서 **[!UICONTROL Layout]** 카테고리에 **[!UICONTROL Local notification]**&#x200B;을(를) 선택합니다

   ![](assets/inapp_customize_17.png)

1. **[!UICONTROL Text]** 카테고리 아래에 **[!UICONTROL Message title]**(와)과 **[!UICONTROL Message content]**&#x200B;을(를) 입력합니다.

   ![](assets/inapp_customize_18.png)

1. **[!UICONTROL Advanced option]** 카테고리 아래에 **[!UICONTROL Wait to display]** 필드에서 이벤트가 트리거 될 때 로컬 알림이 화면에 표시되는 시간을 선택합니다.
1. **[!UICONTROL Sound]** 필드에서는 로컬 알림을 받을 때 모바일 디바이스에서 재생할 사운드 파일의 파일 이름을 확장자 포함하여 입력합니다.

   모바일 애플리케이션 패키지에 파일이 정의된 경우, 알림을 게재할 때 사운드 파일이 재생됩니다. 정의되지 않은 경우, 디바이스의 기본 사운드가 재생됩니다.

   ![](assets/inapp_customize_19.png)

1. 사용자가 **[!UICONTROL Deeplink URL]** 필드에서 로컬 알림과 상호 작용할 때 리디렉션할 대상을 지정합니다.
1. 페이로드에서 사용자 지정 데이터를 키-값 쌍 형태로 전달하려면 로컬 알림에 사용자 지정 필드를 추가할 수 있습니다. **[!UICONTROL Custom fields]** 카테고리에서 **[!UICONTROL Create an element]** 버튼을 클릭합니다.
1. **[!UICONTROL Keys]**&#x200B;을(를) 입력한 후 각 키와 연관된 **[!UICONTROL Values]**&#x200B;을(를) 입력합니다.

   사용자 지정 필드의 처리 및 용도는 전적으로 모바일 앱에 따라 다릅니다.

1. **[!UICONTROL Apple options]** 카테고리에서는 Apple 모바일 애플리케이션에서 사용 가능한 경우 **[!UICONTROL Category]** 필드를 채워 사용자 지정 작업에 대한 카테고리 ID를 추가합니다.

## 사용자 지정 HTML 메시지로 사용자 지정 {#customizing-with-a-custom-html-message}

>[!NOTE]
>
>사용자 지정 HTML 메시지는 콘텐츠 개인화를 지원하지 않습니다.

**[!UICONTROL Custom message]** 모드에서는 사전 구성된 HTML 메시지 중 하나를 직접 가져올 수 있습니다.

이렇게 하려면 컴퓨터에서 파일을 끌어다 놓거나 선택하기만 하면 됩니다.

파일에는 **샘플 파일 다운로드** 옵션을 클릭하여 찾을 수 있는 특정 레이아웃이 있어야 합니다.

![](assets/inapp_customize_16.png)

Adobe Campaign에서 성공적으로 가져오기 위한 사용자 지정 HTML 요구 사항 목록을 찾을 수도 있습니다.

![](assets/inapp_customize_3.png)

HTML을 가져온 후에는 여러 디바이스의 미리 보기 창에서 미리 볼 수 있습니다.

## 인앱 메시지 미리 보기 {#previewing-the-in-app-message}

인앱 메시지를 보내기 전에 테스트 프로필로 테스트하여 대상 고객이 게재를 받을 때 보게 될 내용을 확인할 수 있습니다.

1. **[!UICONTROL Preview]** 버튼을 클릭합니다.

   ![](assets/inapp_sending_2.png)

1. **[!UICONTROL Select a test profile]** 버튼을 클릭하고 테스트 프로필 중 하나를 선택하여 게재 미리 보기를 시작합니다. 테스트 프로필에 대한 자세한 내용은 이 [섹션](../../audiences/using/managing-test-profiles.md)을 참조하십시오.
1. Android나 iPhone, 심지어 태블릿과 같은 다양한 디바이스에서 메시지를 확인할 수 있습니다. 개인화 필드가 올바른 데이터를 검색하고 있는지 확인할 수도 있습니다.

   ![](assets/inapp_sending_3.png)

1. 이제 메시지를 전송하고 게재 보고서를 통해 그 효과를 측정할 수 있습니다. 보고와 관련한 자세한 정보는 [이 섹션](../../reporting/using/in-app-report.md)을 참조하십시오.
