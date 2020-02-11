---
title: SMS 메시지 만들기
description: 다음 단계에 따라 Adobe Campaign에서 단일 전송 SMS 메시지를 만듭니다.
page-status-flag: never-activated
uuid: 591ae97e-2d19-4f93-be4b-d8d20f1d2d12
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: sms-messages
discoiquuid: b27381a9-19e5-4b65-b194-c72f475ba54d
delivercontext-tags: deliveryCreation,wizard
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 07d68b5bf8d800ebd95919f491e98f1b7a015705

---


# SMS 메시지 만들기{#creating-an-sms-message}

SMS 배달을 만드는 것은 일반 이메일을 만드는 것과 매우 유사합니다. 다음 단계에서는 이 채널과 관련된 구성을 설명합니다. 다른 [옵션에 대한 자세한 내용은 이메일](../../channels/using/creating-an-email.md) 만들기를 참조하십시오.

고급 SMS 매개 변수는 SMS [구성](../../administration/using/configuring-sms-channel.md) 섹션에 자세히 설명되어 있습니다.

SMS 메시지를 만들어 휴대폰에 보내려면 다음이 필요합니다.

* 모드로 채널에 구성된 **[!UICONTROL Routing]** 외부 계정 **[!UICONTROL Mobile (SMS)]** **[!UICONTROL Bulk delivery]** . 자세한 내용은 라우팅 [섹션을 참조하십시오](../../administration/using/configuring-sms-channel.md#defining-an-sms-routing) .
* 이 외부 계정에 올바르게 연결된 배달 템플릿입니다.

1. SMS 전달 만들기 Adobe Campaign [홈 페이지](../../start/using/interface-description.md#home-page), [캠페인](../../start/using/marketing-activities.md#creating-a-marketing-activity) 또는 [마케팅 활동 목록에서](../../start/using/programs-and-campaigns.md#creating-a-campaign)이 작업을 수행할 수 있습니다.

   워크플로우에서 SMS 활동을 추가할 수도 있습니다. 자세한 내용은 워크플로우 [안내서를 참조하십시오](../../automating/using/sms-delivery.md) .

   메시지를 만들 때 가장 중요한 단계를 안내하는 마법사가 표시됩니다. 마법사를 통해 정의된 내용은 메시지 대시보드에서 계속 편집할 수 있습니다.

1. 사용할 템플릿을 선택합니다. 기본 SMS 템플릿 또는 고유한 템플릿 중 하나를 선택할 수 있습니다.

   ![](assets/sms_creation_1.png)

   휴대 전화로 배달하려면 배달 템플릿이 SMS 라우팅 외부 계정에 올바르게 연결되어 있어야 합니다.

1. SMS의 일반 속성을 입력합니다.

   ![](assets/sms_creation_2.png)

   활동 레이블과 해당 ID는 모두 인터페이스에 표시되지만 메시지 수신자는 볼 수 없습니다.

1. 타깃팅할 대상을 지정합니다. 규칙을 정의 및 결합하여 기존 대상자를 선택하거나 인구를 직접 타깃팅할 수 있습니다.

   ![](assets/sms_creation_3.png)

1. SMS에 컨텐츠 추가 SMS 만들기가 완료되면 배달 대시보드의 **[!UICONTROL Content]** 섹션을 클릭하여 컨텐츠를 정의할 수도 있습니다. SMS [컨텐츠 디자인](../../channels/using/about-sms-and-push-content-design.md)정보를 참조하십시오.

   개인화 필드 또는 조건부 텍스트를 SMS 메시지의 내용에 삽입한 경우 메시지 길이는 받는 사람마다 다를 수 있습니다. 실제로, 이러한 요소들은 GSM 인코딩에 의해 고려되지 않는 문자를 도입할 수 있습니다. 개인화가 수행되면 메시지 길이를 평가해야 하는 이유입니다. See [Personalizing SMS messages](../../channels/using/personalizing-sms-messages.md).

   ![](assets/sms_creation_4.png)

1. 메시지 작성을 확인합니다. 그러면 대시보드가 표시됩니다.
1. 전송을 예약합니다. SMS는 메시지 준비 직후에 수동으로 전송하거나 예약된 날짜에 자동으로 전송할 수 있습니다. 메시지 [예약을](../../sending/using/about-scheduling-messages.md)참조하십시오.
1. 메시지를 준비하여 유효성, 개인화 및 타겟팅을 분석합니다.

   ![](assets/sms_creation_6.png)

   >[!NOTE]
   >
   >캠페인에서 과다 복제된 프로파일을 자동으로 제외시키는 글로벌 크로스 채널 피로 규칙을 설정할 수 있습니다. 피로 [규칙을](../../administration/using/fatigue-rules.md)참조하십시오.

1. 교정본을 보내 메시지를 확인 및 확인하고 받은 편지함 렌더링을 모니터링할 수 있습니다. 전송 [증명](../../sending/using/sending-proofs.md) 섹션을 참조하십시오.
1. 메시지 전송을 확인합니다. 전송은 정의한 일정에 따라 시작됩니다.

   ![](assets/sms_creation_7.png)

메시지가 전송됩니다. 메시지 대시보드 및 로그를 통해 전달을 확인할 수 있습니다.

전송이 완료되면 내장 또는 사용자 지정 배달 보고서를 사용하여 메시지의 영향을 측정할 수 있습니다.

**관련 항목:**

* [SMS 및 푸시 컨텐츠 에디션 정보](../../channels/using/about-sms-and-push-content-design.md)
* [템플릿 관리](../../start/using/marketing-activity-templates.md)
* [SMS 전달](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/communication-channels/mobile/sms/sms-delivery.html) 비디오 만들기

