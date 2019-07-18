---
title: 보낸 사람 개인화
seo-title: 보낸 사람 개인화
description: 보낸 사람 개인화
seo-description: 메시지 발신자의 이름이나 주소를 개인화하는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: 7 aa 08 d 5 d -9 e 6 c -4 dac-bff 8-6 fde 85368 c 2 d
contentOwner: Sauviat
products: sg_ campaign/standard
audience: designing
content-type: 참조
topic-tags: 맞춤형 컨텐츠
discoiquuid: 49532 F 6 B -3 CD 0-4 D 03-932 E-BCB 7 D 05 C 74 D 4
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Personalizing the sender{#personalizing-the-sender}

## Email sender {#email-sender}

To define the name of the sender which will appear in the header of messages sent, go the **[!UICONTROL Properties]** tab of the Email Designer home page (accessible through the home icon).

![](assets/delivery_content_edition16.png)

* **[!UICONTROL From: name]** 이 필드에서 발신자 이름을 입력할 수 있습니다. By default, the default **Sender name** block is automatically entered in the field. Adobe Campaign refers to the email channel configuration (from the advanced menu **[!UICONTROL Administration > Channels > Email > Email accounts]** via the Adobe Campaign logo) to designate this sender.

   **발신자 이름** 블록을 클릭하여 발신자 이름을 변경할 수 있습니다. 그런 다음 필드를 편집할 수 있게 되며 사용할 이름을 입력할 수 있습니다.

   이 필드는 개인화할 수 있습니다. 이렇게 하려면 발신자 이름 아래에 있는 아이콘을 클릭하여 개인화 필드, 컨텐츠 블록 및 동적 컨텐츠를 추가할 수 있습니다.

* The **[!UICONTROL From: email address]** field cannot be edited from this section. 대시보드에서 이메일의 속성을 편집하여 변경할 수 있습니다. For more on this, see [List of email advanced parameters](../../administration/using/configuring-email-channel.md#advanced-parameters).

>[!NOTE]
>
>헤더 매개 변수는 비어 있으면 안 됩니다. 보낸 사람의 주소는 이메일을 보낼 수 있도록 허용해야 합니다 (RFC 표준). Adobe Campaign는 입력한 이메일 주소의 구문을 확인합니다.

**관련 항목:**

* [개인화 필드 삽입](../../designing/using/inserting-a-personalization-field.md)
* [컨텐츠 블록 추가](../../designing/using/adding-a-content-block.md)
* [이메일에서 동적 컨텐츠 정의](../../designing/using/defining-dynamic-content-in-an-email.md)

## SMS sender {#sms-sender}

SMS 보낸 사람의 이름을 개인화할 수 있습니다. For more on this, refer to the [SMS configuration](../../administration/using/configuring-sms-channel.md#configuring-sms-properties) section.
