---
title: 보내기 준비
seo-title: 보내기 준비
description: 보내기 준비
seo-description: 보내기 전에 준비를 정의하는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: 1038 DAE 2-164 C -4579-9294-BDF 2 A 4 EB 12 D 6
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 전송
content-type: 참조
topic-tags: preparing-and-testing-messages
discoiquuid: 003 ABC 83-7 F 07-471 F-AB 2 F -1 D 352 D 22 C 26 F
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Preparing the send{#preparing-the-send}

준비는 Target 모집단을 계산하고 타겟에 포함된 각 프로필에 대한 메시지 컨텐츠를 생성하는 단계에 해당합니다. Once preparation is finished, the messages are ready to be sent, either immediately or at [the scheduled date and time](../../sending/using/about-scheduling-messages.md).

1. To start preparing the send, click the **Prepare** button located in the action bar.

   ![](assets/preparing_delivery_2.png)

1. **[!UICONTROL Deployment]** 블록은 준비 진행률을 표시한 다음 준비 통계를 보여 줍니다. 타깃팅된 메시지 수, 전송할 메시지 수 등

   타깃팅된 모집단의 크기에 따라 이 작업은 다소 시간이 걸릴 수 있습니다.

   ![](assets/preparing_delivery.png)

1. Stop the preparation at any time using the **Stop** button, located in the action bar.

   준비 단계에서 메시지가 전송되지 않습니다. 따라서 아무런 영향을 주지 않고 이 작업을 시작하거나 중단할 수 있습니다.

   ![](assets/preparing_delivery_6.png)

1. 전달 준비 단계 동안 메시지가 자동으로 저장됩니다. If you need to make any changes to your message's schedule after the preparation step, you will need to make sure that you click the **[!UICONTROL Prepare]** button again for those changes to be taken into account. For more information on how to schedule a message, refer to this [page](../../sending/using/about-scheduling-messages.md).

   ![](assets/preparing_delivery_5.png)

1. 준비 로그를 보려면 블록 오른쪽 하단에 있는 단추를 클릭합니다.

   ![](assets/preparing_delivery_4.png)

1. **[!UICONTROL Deployment]** 창이 열리고 오류를 수정한 다음 준비를 다시 시작합니다.

   마지막 로그 메시지에는 오류 메시지와 오류 수가 표시됩니다. 특정 아이콘에 발생한 오류 유형이 표시됩니다. 노란색 아이콘은 중요하지 않은 처리 오류를 나타냅니다. 빨간색 아이콘은 배달을 시작할 수 없는 치명적인 오류를 나타냅니다.

   ![](assets/preparing_delivery_3.png)

1. 메시지 전송을 확인하기 전에 준비 통계를 확인합니다. If the number of messages to send does not correspond to your configuration, edit the targeted population (see [Selecting an audience in a message](../../audiences/using/selecting-an-audience-in-a-message.md)) and restart the preparation.

준비가 완료되면 메시지를 보낼 준비가 된 것입니다. For more on this, see [Confirming send](../../sending/using/confirming-the-send.md).

**유형 규칙 규칙**

Adobe Campaign 에는 메시지 준비 중에 적용되는 일련의 빌드 유형 규칙이 포함되어 있습니다. 메시지를 유효하고 품질 기준을 충족하는지 확인하는 데 사용됩니다. See [Typologies](../../administration/using/about-typology-rules.md). 예를 들어, 고유한 유형 지정 규칙을 정의하여 캠페인에서 오버레이된 프로필을 자동으로 제외시키는 글로벌 크로스 채널 피로도 규칙을 설정할 수 있습니다. [피로 규칙을 참조하십시오](../../administration/using/fatigue-rules.md).

**SMS 메시지 검사**

SMS 메시지의 내용에 개인화 필드 또는 조건부 텍스트를 삽입한 경우 이러한 요인은 GSM 인코딩에 의해 고려되지 않는 문자를 도입할 수 있습니다. 준비가 완료되면 메시지 길이가 모니터링되고 제한을 전달한 경우 경고 메시지가 표시됩니다.

For more on this, refer to the [SMS encoding, length and transliteration](../../administration/using/configuring-sms-channel.md#sms-encoding--length-and-transliteration) and [Personalizing SMS messages](../../channels/using/personalizing-sms-messages.md) sections.
