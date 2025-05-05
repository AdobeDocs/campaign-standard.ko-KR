---
title: Adobe Campaign Standard에서 이메일 콘텐츠 제어
description: 이메일 콘텐츠를 편집할 때 Adobe Campaign Standard의 전달성을 향상시키는 방법을 알아봅니다.
audience: sending
content-type: reference
topic-tags: sheduling-messages
context-tags: delivery,schedule,back
feature: Deliverability
role: User
level: Intermediate
exl-id: debbc70d-4094-44c0-b7cb-c999effda1a6
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '787'
ht-degree: 6%

---

# 이메일 콘텐츠 제어{#control-email-content}

<!--TO KEEP because specific to Campaign-->

이메일이 수신자에게 도달하고 이메일 게재 가능성을 높이려면 많은 규칙을 준수해야 합니다. 그렇지 않으면 특정 메시지의 콘텐츠가 스팸으로 감지될 수 있습니다. Adobe Campaign은 콘텐츠가 이러한 규칙을 준수하도록 하는 몇 가지 도구를 제공합니다.

메시지 콘텐츠를 디자인할 때는 아래 나열된 원칙을 따르십시오.

* [보낸 사람 이름 및 주소](#sender-name): 주소가 보낸 사람을 명시적으로 식별해야 합니다. 도메인은 발신자가 소유하고 등록해야 합니다. 도메인 레지스트리를 개인화하면 안 됩니다.
  <!--**Subject**: Avoid excessive capitalization and punctuation, and words that are frequently used by spammers ("Win", "Free", etc.).-->
* [Personalization 및 전송 시간 최적화](#perso-send-time-optimization): 콘텐츠를 개인화하고 받는 사람당 전송 시간을 정의하면 메시지가 열릴 가능성이 높아집니다.
* 이미지 및 텍스트: 적절한 텍스트/이미지 비율(예: 텍스트 60% 및 이미지 40%)을 준수합니다.
* [구독 취소 링크](#opt-out) 및 랜딩 페이지: 구독 취소 링크는 필수입니다. 표시 및 유효해야 하며 양식이 제대로 작동해야 합니다.
* 미리 보기: Adobe Campaign에서 제공하는 도구를 사용하여 이메일([스팸 방지 분석](#anti-spam-analysis), [이메일 렌더링](#message-responsiveness)) 내용을 확인하고 최적화합니다.

콘텐츠를 디자인할 때 게재 능력을 최적화하는 추가 팁은 [Adobe 게재 가능성 모범 사례 안내서](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/content-best-practices-for-optimal-delivery.html?lang=ko)를 참조하세요.

>[!NOTE]
>
>전자 메일 콘텐츠 편집에 대한 자세한 내용은 [전자 메일 Designer 개요](../../designing/using/designing-content-in-adobe-campaign.md) 및 [메시지 디자인 모범 사례](../../designing/using/designing-content-in-adobe-campaign.md#content-design-best-practices)를 참조하세요.

## 보낸 사람 이름 및 주소 {#sender-name}

특정 ISP는 메시지를 수락하기 전에 보낸 사람 주소(**[!UICONTROL From]**)의 유효성을 확인합니다. 잘못된 형식의 주소는 수신 서버에서 거부될 수 있습니다.

![](assets/delivery_content_edition16.png)

인스턴스 수준 또는 가장 자주 사용되는 시나리오에서 올바른 주소가 지정되었는지 확인해야 합니다. 이렇게 하려면 관리자에게 문의하십시오.

자세한 내용은 [전자 메일의 전자 메일 보낸 사람 정의](../../designing/using/subject-line.md#email-sender)를 참조하세요.

## Personalization 및 전송 시간 최적화 {#perso-send-time-optimization}

Adobe Campaign을 사용하면 수신자의 경험을 개선하여 이메일을 열 수 있으므로 메시지를 개인화할 수 있습니다. 자세한 내용은 [이 섹션](../../designing/using/personalization.md)을 참조하십시오.

메시지 열람률을 높이기 위해 수신자당 보내는 시간을 수동으로 정의할 수도 있습니다. 각 프로필은 가능한 한 지정된 날짜 및 시간에 메시지를 수신합니다. 자세한 내용은 [보내는 시간 최적화](../../sending/using/optimizing-the-sending-time.md)를 참조하세요.

## 옵트아웃 링크 및 양식 {#opt-out}

기본적으로 메시지를 분석할 때 유형화 규칙이 옵트아웃 링크가 포함되어 있는지 확인하고 누락된 경우 경고를 생성합니다. 링크 관리에 대한 자세한 내용은 [이 섹션](../../designing/using/links.md)을 참조하세요.

보낼 때마다 옵트아웃 링크가 제대로 작동하는지 확인해야 합니다. 예를 들어, [증명을 전송](../../sending/using/sending-proofs.md)할 때 링크가 유효한지, 양식이 온라인 상태인지, 그리고 유효성을 검사하는 것은 **[!UICONTROL No longer contact]** 상자를 확인합니다. 링크를 입력하거나 양식을 변경할 때 사람의 오류가 항상 발생할 수 있으므로 이 검사를 체계적으로 수행해야 합니다. 옵트인 및 옵트아웃 관리에 대한 자세한 내용은 [이 섹션](../../audiences/using/managing-opt-in-and-opt-out-in-campaign.md)을 참조하세요.

![](assets/optin_landingpage_3.png)

게재를 시작한 후 구독 취소와 관련하여 문제가 감지되면, 선택 사항을 확인할 수 없는 경우에도 옵트아웃 링크를 클릭하는 수신자에 대해 수동으로 구독 취소를 수행할 수 있습니다(예: 대량 업데이트 기능 사용).

일반적으로 옵트아웃하려는 수신자에게 이메일 주소 또는 이름 등의 필드를 작성하도록 요구하여 수신 거부를 방해해서는 안 됩니다. 구독 취소 랜딩 페이지에는 유효성 검사 버튼이 하나만 있어야 합니다.

추가 확인 요청은 신뢰할 수 없습니다. 사용자는 두 개의 이메일 주소를 동일한 상자로 리디렉션할 수 있습니다(예: firstname.lastname@club.com 및 firstname.lastname@internet-club.com). 프로필에서 첫 번째 주소만 기억할 수 있고 다른 주소로 보낸 메시지를 통해 구독을 취소하려는 경우 암호화된 식별자와 입력한 이메일 주소가 일치하지 않기 때문에 양식에서 이를 거부합니다.

## 스팸 차단 분석 {#anti-spam-analysis}

Adobe Campaign의 메시지 편집기는 **스팸 방지 분석**&#x200B;을 통합합니다. 이를 통해 메시지를 수신하면 사용되는 스팸 방지 도구로 인해 메시지가 스팸으로 간주될 위험이 있는지 여부를 확인하기 위해 전자 메일을 평가할 수 있습니다. 자세한 내용은 [메시지 미리 보기](../../sending/using/previewing-messages.md)를 참조하세요.

메시지 콘텐츠 편집기에서 **[!UICONTROL Preview]**&#x200B;을(를) 클릭합니다. 스팸 방지 확인도구가 이 메시지에 대한 높은 위험을 감지했는지 여부를 경고하는 메시지가 표시됩니다. 자세한 내용을 보려면 **[!UICONTROL Anti-spam analysis]**&#x200B;을(를) 클릭하십시오.

![](assets/sending_anti-spam_analysis.png)

## 이메일 렌더링 {#message-responsiveness}

메시지를 보내기 전에 다른 디바이스에서 메시지가 어떻게 표시되는지 확인하여 메시지 응답성을 테스트할 수 있습니다. 이는 다양한 웹 클라이언트, 웹 메일 및 디바이스에서 최적의 방식으로 표시되도록 하기 위한 것입니다.

![](assets/inbox_rendering_report_3.png)

이를 위해 Adobe Campaign은 렌더링을 캡처하여 전용 보고서에서 사용할 수 있도록 합니다. 이렇게 하면 수신되었을 수 있는 다른 컨텍스트에서 전송된 메시지를 미리 볼 수 있습니다.

자세한 내용은 [이메일 렌더링](../../sending/using/email-rendering.md)을 참조하십시오.
