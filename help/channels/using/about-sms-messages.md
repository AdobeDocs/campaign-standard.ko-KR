---
title: SMS 메시지 정보
seo-title: SMS 메시지 정보
description: SMS 메시지 정보
seo-description: Adobe Campaign에서 SMS 채널의 주요 특징을 살펴볼 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 14 DC 7434-8171-4 AD 1-9540-52 CA 637659 A 9
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 채널
content-type: 참조
topic-tags: sms-messages
discoiquuid: 6134 fe 72-77 de -4 fd 0-b 794-4 d 966 effaccf
delivercontext-tags: Deliverycreation, Wizard; 전달, Smscontent, 뒤로
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: b0cf437ec97153b53bd4502171b24286abb25731

---


# About SMS messages{#about-sms-messages}

Adobe Campaign를 사용하면 SMS (Short Message Service) 메시지를 전달할 수 있습니다.

>[!NOTE]
>
>SMS 채널은 Add-on 입니다. 사용권 계약을 확인하십시오.

SMS 메시지의 경우 텍스트 형식으로만 메시지를 만들고 수정하며 개인화할 수 있습니다. SMS 메시지를 전송하기 전에 미리 볼 수도 있습니다.

SMS 메시지의 길이는 GSM 인코딩에 있는 경우 160 자로 제한됩니다. 유니코드를 사용하는 경우 70 자만 허용됩니다. 그러나 특정 특수 문자는 메시지 길이에 영향을 줄 수 있습니다. For more on this, refer to the [SMS encoding](../../administration/using/configuring-sms-channel.md#sms-encoding--length-and-transliteration) section.

SMS messages can be created from the **[!UICONTROL Marketing activities]** menu, from a campaign, or in a workflow, see [Creating an SMS message](../../channels/using/creating-an-sms-message.md).

필요한 모바일 휴대폰에 SMS 메시지를 전달하는 방법은 다음과 같습니다.

* A **[!UICONTROL Routing]** external account configured on the **[!UICONTROL Mobile (SMS)]** channel with the **[!UICONTROL Bulk delivery]** mode. For more on this, refer to the [Routing](../../administration/using/configuring-sms-channel.md#defining-an-sms-routing) section.
* 이 외부 계정에 올바르게 연결된 배달 템플릿입니다.

**관련 항목:**

* [템플릿 관리](../../start/using/about-templates.md)
* [SMS 구성](../../administration/using/configuring-sms-channel.md#defining-an-sms-routing)

## SMS delivery template {#sms-delivery-template}

Adobe Campaign는 모바일 장치용 게재 템플릿을 제공합니다. This template must be correctly linked to the external account used for the **[!UICONTROL Mobile (SMS)]** channel. To access and modify it:

1. Select **[!UICONTROL Resources]** &gt; **[!UICONTROL Templates]** &gt; **[!UICONTROL Delivery templates]** from the advanced menu.
1. Hover over the **[!UICONTROL Send via SMS]** template with the mouse and select the **Duplicate element** option.
1. 새 템플릿을 선택합니다.
1. **[!UICONTROL Edit properties]** 단추를 클릭합니다.
1. In the **[!UICONTROL Advanced parameters]** section of the template properties, make sure that the template is linked to the external account to be used for delivering SMS.

   ![](assets/sms_template.png)

**관련 항목:**

* [템플릿 관리](../../start/using/about-templates.md)

