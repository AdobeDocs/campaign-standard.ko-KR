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
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 23%

---

# SMS 메시지 기본 정보{#about-sms-messages}

Adobe Campaign에서 SMS(Short Message Service) 메시지를 게재할 수 있습니다.

>[!NOTE]
>
>SMS 채널은 추가 기능입니다. 사용권 계약을 확인하십시오.

SMS 메시지의 경우 텍스트 형식으로만 메시지를 만들고, 수정하고, 개인화할 수 있습니다. SMS 메시지를 보내기 전에 미리 볼 수도 있습니다.

SMS 메시지의 길이는 GSM 인코딩의 경우 160자로 제한되고, 유니코드에 있는 경우에는 70자만 제한됩니다. 그러나 특정 특수 문자는 메시지 길이에 영향을 줄 수 있습니다. 자세한 내용은 [SMS 인코딩](../../administration/using/configuring-sms-channel.md#sms-encoding--length-and-transliteration) 섹션을 참조하십시오.

SMS 메시지는 **[!UICONTROL Marketing activities]** 메뉴, 캠페인 또는 워크플로우에서 만들 수 있습니다. [SMS 메시지 만들기](../../channels/using/creating-an-sms-message.md) 를 참조하십시오.

필요한 휴대폰에 SMS 메시지를 전달하려면 다음을 수행하십시오.

* **[!UICONTROL Bulk delivery]**&#x200B;모드로 **[!UICONTROL Mobile (SMS)]** 채널에 구성된&#x200B;**[!UICONTROL Routing]** 외부 계정입니다. 자세한 내용은 [라우팅 섹션](../../administration/using/configuring-sms-channel.md#defining-an-sms-routing)을 참조하십시오.
* 이 외부 계정에 올바르게 연결된 게재 템플릿입니다.

**관련 항목:**

* [템플릿 관리](../../start/using/marketing-activity-templates.md)
* [SMS 구성](../../administration/using/configuring-sms-channel.md#defining-an-sms-routing)
* [SMS 보고서](../../reporting/using/sms-report.md)
* [Campaign Standard Mobile 안내서](https://helpx.adobe.com/kr/campaign/kb/acs-mobile.html)

## SMS 게재 템플릿 {#sms-delivery-template}

Adobe Campaign은 모바일 장치용 게재 템플릿을 제공합니다. 이 템플릿은 **[!UICONTROL Mobile (SMS)]** 채널에 사용되는 외부 계정에 올바르게 연결되어 있어야 합니다. 액세스하여 수정하려면 다음을 수행합니다.

1. 고급 메뉴에서 **[!UICONTROL Resources]** > **[!UICONTROL Templates]** > **[!UICONTROL Delivery templates]**&#x200B;를 선택합니다.
1. 마우스를 **[!UICONTROL Send via SMS]** 템플릿 위로 가져간 후 **중복 요소** 옵션을 선택합니다.
1. 새 템플릿을 선택합니다.
1. **[!UICONTROL Edit properties]** 버튼을 클릭합니다.
1. 템플릿 속성의 **[!UICONTROL Advanced parameters]** 섹션에서 템플릿이 SMS 전달에 사용할 외부 계정에 연결되어 있는지 확인합니다.

   ![](assets/sms_template.png)

**관련 항목:**

* [템플릿 관리](../../start/using/marketing-activity-templates.md)
