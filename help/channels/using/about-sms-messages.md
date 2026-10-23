---
title: SMS 메시지 기본 정보
description: Adobe Campaign SMS 채널의 주요 특성을 알아봅니다.
audience: channels
content-type: reference
topic-tags: sms-messages
delivercontext-tags: deliveryCreation,wizard;delivery,smsContent,back
feature: SMS
role: User
level: Beginner
exl-id: a7f22d92-dbf9-4c2b-8fc1-1e31d1e5e79c
TQID: 'https://experienceleague.adobe.com/d0IcWAf5j-JUAKKeC84Fxm-mZsfuMJ2k6GmhQfdQeFk'
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
  - id: f5407121-8933-4ac3-8e06-a9b692a4e88a
    internal-label: Campaign Standard
feature_v2:
  - id: a4671286-a59f-47e3-b97b-90627a1977d5
    internal-label: Communication channels
subfeature_v2:
  - id: b1bd1421-1927-4c59-9bc6-ce292360e43b
    internal-label: SMS Messaging
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
source-git-commit: bb37e2bfbc52de1b0cc03f0f8e03985caff5e5b0
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 29%
---
# SMS 메시지 기본 정보{#about-sms-messages}

Adobe Campaign을 사용하면 SMS(Short Message Service) 메시지를 전달할 수 있습니다.

>[!NOTE]
>
>SMS 채널은 추가 기능입니다. 사용권 계약을 확인하십시오.

SMS 메시지의 경우 텍스트 포맷으로만 메시지를 만들고 수정하고 개인화할 수 있습니다. SMS 메시지를 보내기 전에 미리 볼 수도 있습니다.

SMS 메시지의 길이는 GSM 인코딩인 경우에는 160자로 제한되고, 유니코드인 경우에는 70자만 됩니다. 그러나 특정 특수 문자는 메시지 길이에 영향을 줄 수 있습니다. 자세한 내용은 [SMS 인코딩](../../administration/using/configuring-sms-channel.md#sms-encoding--length-and-transliteration) 섹션을 참조하세요.

SMS 메시지는 **[!UICONTROL Marketing activities]** 메뉴, 캠페인 또는 워크플로에서 만들 수 있습니다. [SMS 메시지 만들기](../../channels/using/creating-an-sms-message.md)를 참조하세요.

휴대폰에 SMS 메시지를 게재하려면 다음이 필요합니다.

* **[!UICONTROL Bulk delivery]**&#x200B;모드로 **[!UICONTROL Mobile (SMS)]** 채널에 구성된&#x200B;**[!UICONTROL Routing]** 외부 계정입니다. 자세한 내용은 [라우팅 섹션](../../administration/using/configuring-sms-channel.md#defining-an-sms-routing)을 참조하십시오.
* 이 외부 계정에 올바르게 연결된 게재 템플릿입니다.

**관련 항목:**

* [템플릿 관리](../../start/using/marketing-activity-templates.md)
* [SMS 구성](../../administration/using/configuring-sms-channel.md#defining-an-sms-routing)
* [SMS 보고서](../../reporting/using/sms-report.md)
* [Campaign Standard Mobile 안내서](../../channels/using/get-started-communication-channels.md)

## SMS 게재 템플릿 {#sms-delivery-template}

Adobe Campaign은 모바일 장치용 게재 템플릿을 제공합니다. 이 템플릿은 **[!UICONTROL Mobile (SMS)]** 채널에 사용된 외부 계정에 올바르게 연결되어야 합니다. 액세스 및 수정하려면 다음과 같이 하십시오.

1. 고급 메뉴에서 **[!UICONTROL Resources]** > **[!UICONTROL Templates]** > **[!UICONTROL Delivery templates]**&#x200B;을(를) 선택합니다.
1. 마우스를 **[!UICONTROL Send via SMS]** 템플릿 위로 가져간 다음 **요소 복제** 옵션을 선택합니다.
1. 새 템플릿을 선택합니다.
1. **[!UICONTROL Edit properties]** 버튼을 클릭합니다.
1. 템플릿 속성의 **[!UICONTROL Advanced parameters]** 섹션에서 템플릿이 SMS를 게재하는 데 사용할 외부 계정에 연결되어 있는지 확인하십시오.

   ![](assets/sms_template.png)

**관련 항목:**

* [템플릿 관리](../../start/using/marketing-activity-templates.md)
