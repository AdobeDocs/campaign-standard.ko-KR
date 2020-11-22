---
solution: Campaign Standard
product: campaign
title: 보내기 준비
description: 보내기 전에 준비 사항을 정의하는 방법을 알아봅니다.
audience: sending
content-type: reference
topic-tags: preparing-and-testing-messages
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 2%

---


# 보내기 준비{#preparing-the-send}

준비는 대상 모집단을 계산하고 대상에 포함된 각 프로필에 대한 메시지 내용을 생성하는 단계에 해당합니다. 준비가 완료되면 즉시 또는 예약된 날짜 및 시간 [에 메시지를 보낼 준비가 됩니다](../../sending/using/about-scheduling-messages.md).

1. 보내기 준비를 시작하려면 작업 표시줄에서 **준비** 단추를 클릭합니다.

   ![](assets/preparing_delivery_2.png)

1. 이 **[!UICONTROL Deployment]** 블록에는 준비 진행률이 표시된 다음 준비 통계가 표시됩니다.대상 메시지 수, 보낼 메시지 수 등

   타깃팅된 모집단 크기에 따라 이 작업은 시간이 걸릴 수 있습니다.

   ![](assets/preparing_delivery.png)

1. 작업 표시줄의 [ **중지** ] 단추를 사용하여 언제든지 준비를 중지합니다.

   준비 단계에서 메시지가 전송되지 않습니다. 따라서 어떤 것에 영향을 주지 않고 이 작업을 시작하거나 중지할 수 있습니다.

   ![](assets/preparing_delivery_6.png)

1. 배달 준비 중에 메시지가 자동으로 저장됩니다. 준비 단계 후에 메시지 일정을 변경해야 하는 경우 변경 사항을 고려하기 위해 **[!UICONTROL Prepare]** 단추를 다시 클릭해야 합니다. For more information on how to schedule a message, refer to this [page](../../sending/using/about-scheduling-messages.md).

   ![](assets/preparing_delivery_5.png)

1. 준비 로그를 보려면 블록의 오른쪽 하단에 있는 단추를 클릭합니다.

   ![](assets/preparing_delivery_4.png)

1. 창이 **[!UICONTROL Deployment]** 열리고 오류를 수정한 다음 준비를 다시 시작합니다.

   마지막 로그 메시지에는 오류 메시지와 오류 수가 표시됩니다. 특정 아이콘에 발생한 오류 유형이 표시됩니다.노란색 아이콘은 중요하지 않은 처리 오류를 나타내며 빨간색 아이콘은 배달을 시작할 수 없는 중요한 오류를 나타냅니다.

   ![](assets/preparing_delivery_3.png)

1. 메시지를 보내기 전에 준비 통계를 확인하십시오. 보낼 메시지 수가 구성에 맞지 않으면 타깃팅된 모집단(메시지에서 [대상자 선택 참조](../../audiences/using/selecting-an-audience-in-a-message.md))을 편집하고 준비를 다시 시작하십시오.

준비가 완료되면 메시지를 보낼 준비가 됩니다. 자세한 내용은 전송 [확인을 참조하십시오](../../sending/using/confirming-the-send.md).

**유형화 규칙**

Adobe Campaign은 메시지 준비 중에 적용되는 빌드-인 유형 분류 규칙 세트를 제공합니다. 메시지가 유효한지, 품질 기준을 충족하는지 확인하는 데 사용됩니다. 유형 [지정](../../sending/using/about-typology-rules.md)참조 예를 들어, 고유한 유형 규칙을 정의할 수 있습니다. 이 경우 과잉 통합 프로파일을 캠페인에서 자동으로 제외시키는 전역 크로스 채널 피로 규칙을 설정할 수 있습니다. [피로도 규칙](../../sending/using/fatigue-rules.md)을 참조하십시오.

**SMS 메시지 확인**

개인화 필드 또는 조건부 텍스트를 SMS 메시지의 컨텐츠에 삽입한 경우 이러한 요소는 GSM 인코딩에 의해 고려되지 않은 문자를 가져올 수 있습니다. 준비가 실행되면 메시지 길이가 모니터링되고 제한 사항을 통과하면 경고 메시지가 표시됩니다.

자세한 내용은 [SMS 인코딩, 길이 및 번역](../../administration/using/configuring-sms-channel.md#sms-encoding--length-and-transliteration) 및 [SMS 메시지 개인화](../../channels/using/personalizing-sms-messages.md) 섹션을 참조하십시오.
