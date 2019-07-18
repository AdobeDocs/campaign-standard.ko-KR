---
title: SMS 메시지 만들기
seo-title: SMS 메시지 만들기
description: SMS 메시지 만들기
seo-description: 다음 단계에 따라 Adobe Campaign에서 단일 전송 SMS 메시지를 만듭니다.
page-status-flag: 정품 인증 안 함
uuid: 591 AE 97 E -2 D 19-4 F 93-BE 4 B-D 8 D 20 F 1 D 2 D 12
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 채널
content-type: 참조
topic-tags: sms-messages
discoiquuid: b 27381 a 9-19 e 5-4 b 65-b 194-c 72 f 475 ba 54 d
delivercontext-tags: Deliverycreation, 마법사
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: d50d486ed77cb7989df47133bb49fde3227ae3a5

---


# Creating an SMS message{#creating-an-sms-message}

SMS 배달을 만드는 것은 일반 이메일을 만드는 방법과 매우 유사합니다. 다음 단계는 이 채널에 적용되는 구성을 설명합니다. Refer to [Creating an email](../../channels/using/creating-an-email.md) for more information on other options.

Advanced SMS parameters are detailed in the [SMS configuration](../../administration/using/configuring-sms-channel.md) section.

휴대폰으로 SMS 메시지를 작성하여 보내려면 다음을 수행해야 합니다.

* A **[!UICONTROL Routing]** external account configured on the **[!UICONTROL Mobile (SMS)]** channel with the **[!UICONTROL Bulk delivery]** mode. For more on this, refer to the [Routing](../../administration/using/configuring-sms-channel.md#defining-an-sms-routing) section.
* 이 외부 계정에 올바르게 연결된 배달 템플릿입니다.

1. SMS 배달 만들기를 참조하십시오. You can do it from the Adobe Campaign [home page](../../start/using/interface-description.md#home-page), in a [campaign](../../start/using/marketing-activities.md#creating-a-marketing-activity) or in the [marketing activity list](../../start/using/programs-and-campaigns.md#creating-a-campaign).

   워크플로우에서 SMS 활동을 추가할 수도 있습니다. For more on this, refer to the [Workflows](../../automating/using/sms-delivery.md) guide.

   메시지를 만들 때 가장 중요한 단계를 안내하는 마법사가 표시됩니다. 마법사로 정의된 내용은 메시지 대시보드에서 나중에 편집할 수 있습니다.

1. 사용할 템플릿을 선택합니다. 기본 SMS 템플릿이나 자체 템플릿 중 하나를 선택할 수 있습니다.

   ![](assets/sms_creation_1.png)

   모바일 전화로 배달하려면 배달 템플릿이 SMS 라우팅 외부 계정에 올바르게 연결되어 있어야 합니다.

1. SMS의 일반 속성을 입력합니다.

   ![](assets/sms_creation_2.png)

   활동 레이블과 ID가 모두 인터페이스에 표시되지만 메시지 받는 사람에게는 표시되지 않습니다.

1. 타깃팅할 대상을 지정합니다. 규칙을 정의하고 결합하여 기존 대상을 선택하거나 모집단을 직접 타깃팅할 수 있습니다.

   ![](assets/sms_creation_3.png)

1. SMS에 콘텐츠를 추가합니다. You can also define the content by clicking the **[!UICONTROL Content]** section of the delivery dashboard, once the SMS creation is finalized. See [About SMS content design](../../designing/using/about-sms-and-push-content-design.md).

   SMS 메시지의 내용에 개인화 필드 또는 조건부 텍스트를 삽입한 경우 메시지의 길이가 받는 사람마다 다를 수 있습니다. 실제로 이러한 요인은 GSM 인코딩에 의해 고려되지 않는 문자를 도입할 수 있습니다. 이러한 이유로 개인화가 실행되면 메시지 길이를 평가해야 합니다. See [Personalizing SMS messages](../../channels/using/personalizing-sms-messages.md).

   ![](assets/sms_creation_4.png)

1. 메시지 만들기를 확인합니다. 그러면 해당 대시보드가 표시됩니다.
1. 전송을 예약합니다. SMS는 메시지 준비 직후 또는 예약된 날짜에 자동으로 전송할 수 있습니다. [예약 메시지를 참조하십시오](../../sending/using/about-scheduling-messages.md).
1. 메시지의 유효성을 분석하고, 개인화 및 타깃팅을 분석합니다.

   ![](assets/sms_creation_6.png)

   >[!NOTE]
   >
   >캠페인에서 오버레이된 프로필을 자동으로 제외시키는 글로벌 크로스채널 피로도 규칙을 설정할 수 있습니다. [피로 규칙을 참조하십시오](../../administration/using/fatigue-rules.md).

1. 메시지를 확인 및 확인하고 받은 편지함 렌더링을 모니터링할 수 있습니다. [전송 증명](../../sending/using/managing-test-profiles-and-sending-proofs.md#sending-proofs) 섹션을 참조하십시오.
1. 메시지 전송을 확인합니다. 전송은 정의한 일정에 따라 시작됩니다.

   ![](assets/sms_creation_7.png)

메시지가 전송됩니다. 메시지 대시보드 및 로그에서 배달을 확인할 수 있습니다.

전송이 완료되면 내장된 배달 보고서와 맞춤형 배달 보고서를 사용하여 메시지 효과를 측정할 수 있습니다.

**관련 항목:**

* [SMS 및 Push Content Edition 정보](../../designing/using/about-sms-and-push-content-design.md)
* [템플릿 관리](../../start/using/about-templates.md)
* [SMS 전달](https://helpx.adobe.com/campaign/kt/acs/using/acs-creating-a-sms-delivery-feature-video-use.html) 비디오 만들기

