---
title: SMS 메시지 기본 정보
description: Adobe Campaign에서 SMS 채널의 주요 특성을 살펴볼 수 있습니다.
page-status-flag: never-activated
uuid: 14dc7434-8171-4ad1-9540-52ca637659a9
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: sms-messages
discoiquuid: 6134fe72-77de-4fd0-b794-4d966effaccf
delivercontext-tags: deliveryCreation,wizard;delivery,smsContent,back
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 501ba6f97a86076116d4d84f43df674536e12f6a

---


# SMS 메시지 기본 정보{#about-sms-messages}

Adobe Campaign을 사용하면 SMS(Short Message Service) 메시지를 전달할 수 있습니다.

>[!NOTE]
>
>SMS 채널은 추가 기능입니다. 사용권 계약을 확인하십시오.

SMS 메시지의 경우 텍스트 형식으로만 메시지를 만들고 수정하고 개인화할 수 있습니다. SMS 메시지를 보내기 전에 미리 볼 수도 있습니다.

SMS 메시지의 길이는 GSM 인코딩의 경우 160자로 제한되며 유니코드의 경우 70자만 제한됩니다. 하지만 특정 특수 문자는 메시지 길이에 영향을 줄 수 있습니다. 자세한 내용은 SMS [인코딩](../../administration/using/configuring-sms-channel.md#sms-encoding--length-and-transliteration) 섹션을 참조하십시오.

SMS 메시지는 **[!UICONTROL Marketing activities]**메뉴, 캠페인 또는 워크플로우에서 만들 수 있습니다. SMS 메시지[만들기를 참조하십시오](../../channels/using/creating-an-sms-message.md).

SMS 메시지를 휴대폰에 전달하려면 다음을 수행하십시오.

* 모드로 채널에 구성된 **[!UICONTROL Routing]**외부 계정**[!UICONTROL Mobile (SMS)]** **[!UICONTROL Bulk delivery]**. 자세한 내용은 라우팅[섹션을 참조하십시오](../../administration/using/configuring-sms-channel.md#defining-an-sms-routing).
* 이 외부 계정에 올바르게 연결된 배달 템플릿입니다.

**관련 항목:**

* [템플릿 관리](../../start/using/marketing-activity-templates.md)
* [SMS 구성](../../administration/using/configuring-sms-channel.md#defining-an-sms-routing)
* [SMS 보고서](../../reporting/using/sms-report.md)
* [Campaign Standard 모바일 안내서](https://helpx.adobe.com/campaign/kb/acs-mobile.html)

## SMS 배달 템플릿 {#sms-delivery-template}

Adobe Campaign은 모바일 장치용 게재 템플릿을 제공합니다. 이 템플릿은 채널에 사용된 외부 계정에 올바르게 연결되어 있어야 합니다. **[!UICONTROL Mobile (SMS)]**액세스하여 수정하려면:

1. 고급 **[!UICONTROL Resources]**메뉴에서 >**[!UICONTROL Templates]** > **[!UICONTROL Delivery templates]**을 선택합니다.
1. 마우스로 **[!UICONTROL Send via SMS]**템플릿 위로 마우스를 가져간 다음 요소**&#x200B;복제&#x200B;**옵션을 선택합니다.
1. 새 템플릿을 선택합니다.
1. 단추를 **[!UICONTROL Edit properties]**클릭합니다.
1. 템플릿 속성의 **[!UICONTROL Advanced parameters]**섹션에서 템플릿이 SMS를 전달하는 데 사용할 외부 계정에 연결되어 있는지 확인합니다.

   ![](assets/sms_template.png)

**관련 항목:**

* [템플릿 관리](../../start/using/marketing-activity-templates.md)
