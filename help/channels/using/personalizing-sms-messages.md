---
title: SMS 메시지 개인화
seo-title: SMS 메시지 개인화
description: SMS 메시지 개인화
seo-description: SMS 메시지를 개인화할 때 음소거 옵션의 특징을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: 123 fe 70 c-c 279-40 a 3-88 b 6-6 bfb 2453 ec 83
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 채널
content-type: 참조
topic-tags: sms-messages
discoiquuid: 7 c 64785 c-e 3 c 2-4 caa-a 547-002990 aae 3 f 9
delivercontext-tags: Deliverycreation, Wizard; delivery, smscontent, back; 전달, Smscontent, 뒤로
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: b0cf437ec97153b53bd4502171b24286abb25731

---


# Personalizing SMS messages{#personalizing-sms-messages}

The principles for personalizing SMS messages are the same as those for [emails](../../designing/using/inserting-a-personalization-field.md). 따라서 음성 변환 옵션은 인코딩에 영향을 주므로 보낼 SMS 메시지의 수는 알고 있어야 합니다. For more on this, refer to the [Transliteration and SMS length](../../administration/using/configuring-sms-channel.md#sms-encoding--length-and-transliteration) section.

여기에서, 번역이 선택되었는지 여부에 따라 동일한 수의 전송을 생성하지 않는 개인화 필드가 들어 있는 샘플 SMS 메시지가 표시됩니다.

**&lt; Firstname &gt; &lt; lastname &gt; 님, 지금 새 제품을 사용할 수 있습니다. Come and check them out in store!**

* ' John Smith'라는 이름의 수신자에게 특수 문자가 포함되어 있지 않으므로 Adobe Campaign 에서는 SMS 인코딩당 최대 160 자를 승인하는 GSM 인코딩을 선택합니다. 그러면 메시지가 한 부분으로 전송됩니다.
* ' raphaël forêt'라는 수신자의 경우,' ë'와'ê'문자는 GSM에서 인코딩할 수 없습니다. 음소거 활성화 여부에 따라 Adobe Campaign에서 다음 두 가지 비헤이비어를 선택할 수 있습니다.

   * 변환이'ë'이고'ê'가'e'로 대체되면, GSM 인코딩을 사용할 수 있으므로 최대 160 자까지 SMS에 사용할 수 있습니다. 이 메시지는 단일 SMS 메시지로 보내지지만 약간 변경됩니다.
   * 변환이 승인되지 않은 경우 Adobe Campaign에서 메시지를 이진 형식 (유니코드) 로 보내게 됩니다. 따라서 모든 문자가 이와 같이 전송됩니다. 유니코드의 SMS 메시지가 70 자로 제한되므로 Adobe Campaign에서 메시지를 두 부분으로 보내야 합니다.

>[!NOTE]
>
>최적의 인코딩을 자동으로 선택하는 알고리즘은 사례별로 각 메시지에 대해 독립적으로 실행됩니다. 유니코드 인코딩이 필요한 개인화된 메시지만 유니코드로 전송됩니다. 다른 모든 사용자는 GSM 인코딩을 사용합니다.

