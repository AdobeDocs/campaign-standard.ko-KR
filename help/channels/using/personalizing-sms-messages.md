---
solution: Campaign Standard
product: campaign
title: SMS 메시지 개인화
description: SMS 메시지를 개인화할 때 음역 옵션의 특수성을 살펴봅니다.
audience: channels
content-type: reference
topic-tags: sms-messages
delivercontext-tags: deliveryCreation,wizard;delivery,smsContent,back;delivery,smsContent,back
feature: SMS
role: User
level: Intermediate
exl-id: 6c01662e-1e19-4cec-aa21-6e84b9b7a677
source-git-commit: aeeb6b4984b3bdd974960e8c6403876fdfedd886
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 100%

---

# SMS 메시지 개인화{#personalizing-sms-messages}

SMS 메시지를 개인화하는 원칙은 [이메일](../../designing/using/personalization.md#inserting-a-personalization-field)과 동일합니다. 그럼에도 불구하고 음역 옵션이 인코딩에 영향을 줄 수 있고 전송할 SMS 메시지 수에 영향을 줄 수 있기 때문에 반드시 알고 있어야 합니다. 자세한 내용은 [음역 및 SMS 길이](../../administration/using/configuring-sms-channel.md#sms-encoding--length-and-transliteration) 섹션을 참조하십시오.

여기에서는 음역 선택 여부에 따라 동일한 수의 전송을 생성하지 않는 개인화 필드가 포함된 샘플 SMS 메시지를 사용합니다.

**&lt; FirstName > &lt; LastName > 님, 이제 새 제품을 사용할 수 있습니다. 스토어로 가서 확인하십시오.**

* &#39;John Smith&#39;라는 이름의 수신자의 경우 특수 문자가 없으므로 Adobe Campaign은 SMS 메시지당 최대 160자를 승인하는 GSM 인코딩을 선택합니다. 따라서 메시지는 단일 부분으로 전송됩니다.
* &#39;Raphaël Forêt&#39;라는 이름의 수신자의 경우 &#39;ë&#39; 및 &#39;ê&#39;를 GSM로 인코딩할 수 없습니다. Adobe Campaign은 음역을 활성화했는지 여부에 따라 다음 두 가지 동작 중에서 선택할 수 있습니다.

   * 음역이 승인된 경우 &#39;ë&#39; 및 &#39;ê&#39;가 &#39;e&#39;로 대체되므로 GSM 인코딩을 사용할 수 있으며 SMS에는 최대 160자를 사용할 수 있습니다. 이 메시지는 단일 SMS 메시지로 전송되지만 약간 변경됩니다.
   * 음역이 승인되지 않은 경우 Adobe Campaign에서 메시지를 이진 포맷(유니코드)으로 보내도록 선택합니다. 따라서 모든 문자가 그대로 전송됩니다. 유니코드의 SMS 메시지는 70자로 제한되므로 Adobe Campaign에서 메시지를 두 부분으로 보내야 합니다.

>[!NOTE]
>
>최적의 인코딩을 자동으로 선택하는 알고리즘은 개별적으로 각 메시지에 대해 독립적으로 실행됩니다. 이렇게 하면 유니코드 인코딩이 필요한 개인화된 메시지만 유니코드로 전송됩니다. 나머지는 모두 GSM 인코딩을 사용하게 됩니다.

## SMS 발신자 {#sms-sender}

>[!IMPORTANT]
>
>해당 국가의 발신자 주소 수정에 대한 법률을 확인하십시오. 또한 SMS 서비스 공급자에게 문의하여 이 기능을 제공하는지 확인하십시오.

**[!UICONTROL From]** 옵션을 사용하면 문자열을 사용하여 SMS 메시지의 발신자명을 개인화할 수 있습니다. 발신자명이란 수신자의 휴대전화에서 SMS 메시지를 보낸 사람으로 표시되는 이름입니다.

이 필드가 비어 있는 경우 외부 계정에서 제공하는 소스 번호가 표시됩니다. 소스 번호가 제공되지 않는 경우 짧은 코드가 사용됩니다. SMS 게재와 관련된 외부 계정은 [SMS 라우팅 정의 ](../../administration/using/configuring-sms-channel.md#defining-an-sms-routing) 섹션에 나와 있습니다.

![](assets/sms_creation_8.png)



