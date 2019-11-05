---
title: SMS 메시지 개인화
description: SMS 메시지를 개인화할 때 문법 변환 옵션의 정확성을 살펴볼 수 있습니다.
page-status-flag: 활성화 안 함
uuid: 123fe70c-c279-40a3-88b6-6bfb2453ec83
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 채널
content-type: reference
topic-tags: sms 메시지
discoiquuid: 7c64785c-e3c2-4caa-a547-002990aae3f9
delivercontext-tags: deliveryCreation,wizard;delivery,smsContent,back;delivery,smsContent,back
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# SMS 메시지 개인화{#personalizing-sms-messages}

SMS 메시지를 개인화하는 원칙은 [이메일과](../../designing/using/personalization.md#inserting-a-personalization-field)동일합니다. 그럼에도 불구하고 이러한 옵션이 인코딩에 영향을 줄 수 있으므로 전송할 SMS 메시지 수에 영향을 줄 수 있으므로 음역 옵션을 알고 있어야 합니다. 자세한 내용은 Translation and SMS [길이](../../administration/using/configuring-sms-channel.md#sms-encoding--length-and-transliteration) 섹션을 참조하십시오.

여기서는 개인화 필드가 포함된 샘플 SMS 메시지를 사용합니다. 이 메시지는 음역 선택 여부에 따라 동일한 수의 전송을 생성하지 않습니다.

**&lt; FirstName &gt; &lt; LastName &gt; 님, 이제 새로운 제품을 사용할 수 있습니다. 와서 가게에 가서 확인해 보세요!**

* 'John Smith'라는 받는 사람에 대해 특수 문자가 없으므로 Adobe Campaign은 SMS 메시지당 최대 160자를 인증하는 GSM 인코딩을 선택합니다. 따라서 메시지는 한 부분으로 전송됩니다.
* '라팔 포레'라는 이름의 수신자는 '레크'와 '려'를 GSM으로 인코딩할 수 없습니다. Adobe Campaign은 번역 활성화 여부에 따라 다음 두 가지 비헤이비어 중에서 선택할 수 있습니다.

   * 음역을 '레크'로 인가된 경우 'e'로 대체되므로 GSM 인코딩을 사용할 수 있으며 SMS에서 최대 160자까지 사용할 수 있습니다. 이 메시지는 단일 SMS 메시지로 전송되지만 약간 변경됩니다.
   * 음역 지정이 인증되지 않은 경우 Adobe Campaign은 메시지를 바이너리 형식(유니코드)으로 전송하도록 선택합니다.따라서 모든 문자가 그대로 전송됩니다. 유니코드의 SMS 메시지는 70자로 제한되므로 Adobe Campaign은 두 부분으로 메시지를 보내야 합니다.

>[!NOTE]
>
>최적의 인코딩을 자동으로 선택하는 알고리즘은 대소문자를 구분하여 각 메시지에 개별적으로 실행됩니다. 이렇게 하면 유니코드 인코딩이 필요한 개인화된 메시지만 유니코드로 전송됩니다.다른 모든 프로그램은 GSM 인코딩을 사용합니다.

## SMS 보낸 사람 {#sms-sender}

SMS 발신자의 이름을 개인화할 수 있습니다. 자세한 내용은 SMS [구성](../../administration/using/configuring-sms-channel.md#configuring-sms-properties) 섹션을 참조하십시오.
