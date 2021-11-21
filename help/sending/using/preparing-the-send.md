---
title: 보내기 준비
description: 보내기 전에 준비를 정의하는 방법을 알아봅니다.
audience: sending
content-type: reference
topic-tags: preparing-and-testing-messages
feature: Send Time Optimization
role: User
level: Intermediate
exl-id: 0140c41a-7255-4b77-a1b7-c6f7b1135e51
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 2%

---

# 보내기 준비{#preparing-the-send}

준비가 대상 모집단을 계산하고 대상에 포함된 각 프로필에 대한 메시지 콘텐츠를 생성하는 단계에 해당합니다. 준비가 완료되면 즉시 또는 즉시 메시지를 보낼 수 있습니다 [예약된 날짜 및 시간](../../sending/using/about-scheduling-messages.md).

1. 보내기 준비를 시작하려면 **준비** 작업 표시줄에 있는 단추입니다.

   ![](assets/preparing_delivery_2.png)

1. 다음 **[!UICONTROL Deployment]** 블록은 준비 진행률을 표시한 다음 준비 통계를 표시합니다. 타겟팅된 메시지 수, 전송할 메시지 수 등

   타겟팅된 모집단의 크기에 따라 이 작업은 시간이 좀 걸릴 수 있습니다.

   ![](assets/preparing_delivery.png)

1. 언제든지 을 사용하여 준비를 중지합니다 **정지** 버튼을 클릭합니다.

   준비 단계 동안 메시지가 전송되지 않습니다. 따라서 어떤 것이든 영향을 주지 않고 이 작업을 시작하거나 중지할 수 있습니다.

   ![](assets/preparing_delivery_6.png)

1. 게재 준비 중에 메시지가 자동으로 저장됩니다. 준비 단계 후에 메시지 일정을 변경해야 하는 경우, **[!UICONTROL Prepare]** 다시 단추를 클릭하여 이러한 변경 사항을 고려합니다. 메시지 예약 방법에 대한 자세한 내용은 다음을 참조하십시오 [페이지](../../sending/using/about-scheduling-messages.md).

   ![](assets/preparing_delivery_5.png)

1. 준비 로그를 보려면 블록의 오른쪽 하단에 있는 버튼을 클릭합니다.

   ![](assets/preparing_delivery_4.png)

1. 다음 **[!UICONTROL Deployment]** 창이 열리면 오류를 수정한 다음 준비를 다시 시작합니다.

   마지막 로그 메시지에는 오류 메시지와 오류 수가 표시됩니다. 특정 아이콘에는 발생한 오류 유형이 표시됩니다. 노란색 아이콘은 중요하지 않은 처리 오류를 나타내며, 빨간색 아이콘은 게재를 시작할 수 없는 중요한 오류를 나타냅니다.

   ![](assets/preparing_delivery_3.png)

1. 메시지 전송을 확인하기 전에 준비 통계를 확인하십시오. 전송할 메시지 수가 구성에 맞지 않는 경우 타겟팅된 모집단을 편집합니다( [메시지에서 대상자 선택](../../audiences/using/selecting-an-audience-in-a-message.md))를 클릭한 후 준비를 다시 시작합니다.

준비가 완료되면 메시지를 보낼 수 있습니다. 자세한 내용은 [보내기 확인](../../sending/using/confirming-the-send.md).

**유형화 규칙**

Adobe Campaign에는 메시지를 준비하는 동안 적용되는 기본 제공 유형화 규칙 세트가 포함되어 있습니다. 메시지가 유효하고 품질 기준을 충족하는지 확인하는 데 사용됩니다. 자세한 내용은 [유형화](../../sending/using/about-typology-rules.md). 예를 들어, 유형화 규칙을 정의하여 캠페인에서 과하게 요청된 프로필을 자동으로 제외하는 전역 크로스 채널 피로도 규칙을 설정할 수 있습니다. [피로도 규칙](../../sending/using/fatigue-rules.md)을 참조하십시오.

**SMS 메시지 확인**

개인화 필드 또는 조건부 텍스트를 SMS 메시지의 콘텐츠에 삽입한 경우, 이러한 요소에 GSM 인코딩에서 고려하지 않는 문자가 들어갈 수 있습니다. 준비가 실행되면 메시지 길이가 모니터링되고, 제한 값을 통과하면 경고 메시지가 표시됩니다.

자세한 내용은 [SMS 인코딩, 길이 및 변환](../../administration/using/configuring-sms-channel.md#sms-encoding--length-and-transliteration) 및 [SMS 메시지 개인화](../../channels/using/personalizing-sms-messages.md) 섹션에 자세히 설명되어 있습니다.
