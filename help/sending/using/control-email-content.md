---
title: Adobe Campaign Standard에서 이메일 컨텐츠 제어
description: 이메일 컨텐츠를 편집할 때 Adobe Campaign Standard의 전달 기능을 향상시키는 방법을 살펴볼 수 있습니다.
page-status-flag: never-activated
uuid: 286fceee-65a9-4cb9-b205-9ce5d024675c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sheduling-messages
discoiquuid: 9c7fd670-bba9-4f3c-8cb1-87397a1acd27
context-tags: delivery,schedule,back
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: f0580e1ab75d4250bfb1cb801ff08b31b91cdc5a

---


# 이메일 컨텐츠 제어{#control-email-content}

이메일 배달율을 향상시키고 이메일을 수신자에게 전달하려면 일정 수의 규칙을 준수해야 합니다.

* **보낸 사람 이름 및 주소**:주소는 발신자를 명시적으로 식별해야 합니다. 도메인은 발신자가 소유해야 하며 발신자에게 등록되어 있어야 합니다. 도메인 레지스트리를 민영화해서는 안 됩니다.
* **제목**:과도한 대문자화 및 구두점과 스팸자가 자주 사용하는 단어("Win", "Free" 등)를 피하십시오.
* **이메일**&#x200B;개인화:이메일을 개인화하면 메시지가 열릴 가능성이 높아집니다.
* **이미지 및 텍스트**:텍스트/이미지 비율이 적당합니다(예: 60% 텍스트 및 40% 이미지).
* **구독 취소 링크 및 랜딩 페이지**:구독 취소 링크는 필수입니다. 이 형식은 표시되고 유효해야 하며, 반드시 작동해야 합니다.
* **Adobe Campaign에서 제공하는 툴을** 사용하여 이메일 컨텐츠를 최적화할 수 있습니다(전달 분석, 스팸 방지 분석).

이메일 컨텐츠 편집에 대한 자세한 내용은 이메일 [디자이너 개요](../../designing/using/designing-content-in-adobe-campaign.md) 및 [메시지 디자인 모범 사례를](../../designing/using/overview.md#content-design-best-practices)참조하십시오.

## 보낸 사람 이름 및 주소 {#sender-name}

특정 ISP는 메시지를 수락하기 전에 보낸 사람 주소(보낸 사람)의 유효성을 확인합니다. 형식이 잘못되면 수신 서버에서 주소가 거부될 수 있습니다. 올바른 주소가 인스턴스 수준 또는 가장 자주 사용되는 시나리오에서 제공되는지 확인해야 합니다. 관리자에게 문의하십시오.

![](assets/delivery_content_edition16.png)

자세한 내용은 발신자 이름 [개인화를](../../designing/using/personalization.md#personalizing-the-sender)참조하십시오.

## 제목 {#subject-line}

이메일을 편집할 때 다른 제목 줄을 시도해 보고 보내기 전에 공개 비율을 예측할 수 있습니다. 자세한 내용은 [이메일의](../../sending/using/testing-subject-line-email.md)제목 줄 테스트를 참조하십시오.

![](assets/predictive_subject_line_example.png)

이메일의 제목 줄 정의에 대한 자세한 내용은 [이 섹션을](../../designing/using/subject-line.md)참조하십시오.

## 전송 시간 최적화 {#send-time-optimization}

메시지의 성공률을 향상시키려면 수신자당 전송 시간을 수동으로 정의할 수 있습니다. 각 프로필은 가능한 한 지정된 날짜와 시간에 메시지를 수신합니다.

자세한 내용은 전송 [시간](../../sending/using/optimizing-the-sending-time.md)최적화를 참조하십시오.

## 옵트아웃 링크 및 양식 {#opt-out}

기본적으로 메시지를 분석할 때 유형 분류 규칙은 옵트아웃 링크가 포함되었는지 여부를 확인하고 누락된 경우 경고를 생성합니다.

보낼 때마다 옵트아웃 링크가 제대로 작동하는지 확인해야 합니다. 예를 들어, 증명을 보낼 때 링크가 유효한지, 양식이 온라인 상태인지, 양식의 유효성을 검사하면 더 이상 연락처 없음 상자의 값이 선택되어 있는지 확인합니다. 링크를 입력하거나 양식을 변경할 때 항상 인적 오류가 발생할 수 있으므로 이 확인을 체계적으로 해야 합니다.

배달을 시작한 후 가입 취소와 관련하여 문제가 발견되더라도, 옵트아웃 링크를 클릭하는 수신자에 대해 수동으로(예: 대량 업데이트 기능 사용) 가입 해제를 수행할 수 있습니다.

일반적으로 이메일 주소 또는 이름과 같은 필드를 채우도록 요구하여 수신을 거부하려는 수신자의 방식을 방해하지 마십시오. 구독 취소 랜딩 페이지에는 유효성 검사 단추가 하나만 있어야 합니다. 추가 확인 요청은 신뢰성이 없습니다.사용자는 두 개의 이메일 주소를 동일한 상자로 리디렉션할 수 있습니다(예:firstname.lastname@club.com 및 firstname.lastname@internet-club.com). 프로필에서 첫 번째 주소만 기억할 수 있고 다른 주소로 전송된 메시지를 통해 구독을 취소하려면, 암호화된 식별자와 입력한 이메일 주소가 일치하지 않기 때문에 양식이 거부됩니다.

## 스팸 방지 분석 {#anti-spam-analysis}

Adobe Campaign의 메시지 편집기는 **이메일에 점수를 매기도록 하는 스팸 방지 분석과** 통합되어 있어, 메시지가 수신에 사용된 스팸 방지 툴에 의해 스팸으로 간주될 위험을 발생시키는지 여부를 결정할 수 있습니다. 자세한 내용은 메시지 [미리 보기를](../../sending/using/previewing-messages.md)참조하십시오.

메시지 내용 편집기에서 을 클릭합니다 **[!UICONTROL Preview]**. 스팸 방지 검사에서 이 메시지의 위험성이 높은 경우 경고 메시지가 표시됩니다. 세부 사항을 **[!UICONTROL Anti-spam analysis]** 보려면 을 클릭합니다.

![](assets/sending_anti-spam_analysis.png)

## 메시지 응답성 확인 {#message-responsiveness}

메시지를 보내기 전에 메시지가 다른 장치에서 어떻게 보이는지 확인할 수 있습니다. 이는 다양한 웹 클라이언트, 웹 메일 및 장치에서 최적의 방식으로 표시되도록 하기 위한 것입니다.

이를 위해 Adobe Campaign은 렌더링을 캡처하여 전용 보고서에서 사용할 수 있도록 합니다. 이렇게 하면 메시지를 수신할 수 있는 다른 컨텍스트에서 메시지를 미리 볼 수 있습니다.

자세한 내용은 이메일 [렌더링을](../../sending/using/email-rendering.md)참조하십시오.

![](assets/inbox_rendering_report_3.png)
