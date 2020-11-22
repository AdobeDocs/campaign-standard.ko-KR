---
solution: Campaign Standard
product: campaign
title: Adobe Campaign Standard에서 이메일 컨텐츠 제어
description: 이메일 컨텐츠를 편집할 때 Adobe Campaign Standard의 전달 가능성을 향상시키는 방법을 살펴볼 수 있습니다.
audience: sending
content-type: reference
topic-tags: sheduling-messages
context-tags: delivery,schedule,back
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '741'
ht-degree: 7%

---


# 이메일 콘텐츠 제어{#control-email-content}

이메일 배달율을 향상시키고 이메일을 수신자에게 전달하려면 일정 수의 규칙을 준수해야 합니다.

* **보낸 사람 이름 및 주소**:주소는 발신자를 명시적으로 식별해야 합니다. 이 도메인은 발신자가 소유해야 하며 발신자에게 등록되어 있어야 합니다. 도메인 레지스트리를 민영화해서는 안 됩니다.
* **제목**:과도한 대문자화 및 구두점, 스패머가 자주 사용하는 단어(&quot;Win&quot;, &quot;Free&quot; 등)는 피하십시오.
* **이메일**&#x200B;개인화:이메일을 개인화하면 메시지가 열릴 가능성이 높아집니다.
* **이미지 및 텍스트**:적절한 텍스트/이미지 비율(예: 60% 텍스트 및 40% 이미지)을 준수합니다.
* **구독 취소 링크 및 랜딩 페이지**:구독 취소 링크는 필수적입니다. 반드시 표시되고 유효해야 하며, 양식이 제대로 작동하는지 확인해야 합니다.
* **Adobe Campaign이 제공하는 툴을** 사용하여 이메일 컨텐츠를 최적화할 수 있습니다(전달 분석, 스팸 방지 분석).

이메일 컨텐츠 편집에 대한 자세한 내용은 [이메일 디자이너 개요](../../designing/using/designing-content-in-adobe-campaign.md) 및 [메시지 디자인 모범 사례를 참조하십시오](../../designing/using/designing-content-in-adobe-campaign.md#content-design-best-practices).

## 보낸 사람 이름 및 주소 {#sender-name}

일부 ISP는 메시지를 승인하기 전에 보낸 사람 주소(보낸 사람 주소)의 유효성을 확인합니다. 형식이 잘못되면 수신 서버에서 주소가 거부될 수 있습니다. 올바른 주소가 인스턴스 수준 또는 가장 자주 사용되는 시나리오에서 제공되는지 확인해야 합니다. 관리자에게 문의하십시오.

![](assets/delivery_content_edition16.png)

자세한 내용은 보낸 사람 이름 [개인화를 참조하십시오](../../designing/using/personalization.md#personalizing-the-sender).

## 제목 {#subject-line}

이메일을 편집할 때 다른 제목 줄을 시도해 보고 보내기 전에 공개 비율을 예측할 수 있습니다. 자세한 내용은 이메일 [의 제목 줄 테스트를 참조하십시오](../../sending/using/testing-subject-line-email.md).

![](assets/predictive_subject_line_example.png)

이메일의 제목 줄 정의에 대한 자세한 내용은 [이 섹션을 참조하십시오](../../designing/using/subject-line.md).

## Send time optimization {#send-time-optimization}

메시지의 성공률을 높이기 위해 수신자당 전송 시간을 수동으로 정의할 수 있습니다. 각 프로필은 가능한 한 지정된 날짜와 시간에 메시지를 수신합니다.

자세한 내용은 전송 시간 [최적화를 참조하십시오](../../sending/using/optimizing-the-sending-time.md).

## 옵트아웃 링크 및 양식 {#opt-out}

기본적으로 메시지를 분석할 때 유형 분류 규칙은 옵트아웃 링크가 포함되었는지 여부를 확인하고 누락된 경우 경고를 생성합니다.

보낼 때마다 옵트아웃 링크가 제대로 작동하는지 확인해야 합니다. 예를 들어 증거를 전송할 때 링크가 유효한지, 양식이 오프라인 상태인지, 양식의 유효성을 검사하면 더 이상 연락처 없음 상자의 값이 선택되어 있는지 확인합니다. 링크를 입력할 때 또는 양식을 변경할 때 사용자 오류가 항상 가능하므로 이 확인을 체계적으로 해야 합니다.

배달을 시작한 후 가입 해소와 관련하여 문제가 발견되더라도 옵트아웃 링크를 클릭하는 수신자에 대해 수동으로(예: 일괄 업데이트 기능 사용) 가입 해지를 수행할 수 있습니다. 수신자가 선택을 확인할 수 없는 경우에도 마찬가지입니다.

일반적으로 이메일 주소 또는 이름과 같은 필드를 채우도록 요구함으로써 수신을 거부하려는 수신자의 수신을 막으려고 하지 마십시오. 구독 취소 랜딩 페이지에는 하나의 유효성 확인 단추만 있어야 합니다. 추가 확인을 요청하는 것은 믿을 수 없습니다.사용자는 동일한 상자로 리디렉션되는 두 개의 이메일 주소를 가질 수 있습니다(예:firstname.lastname@club.com 및 firstname.lastname@internet-club.com). 프로필에서 첫 번째 주소만 기억할 수 있고 다른 주소로 전송된 메시지를 통해 가입을 해지하려는 경우 암호화된 식별자와 입력한 이메일 주소가 일치하지 않으므로 이 양식이 거부됩니다.

## 스팸 방지 분석 {#anti-spam-analysis}

Adobe Campaign의 메시지 편집기는 **스팸 방지 분석** 기능과 통합되어 있으므로 이메일 점수를 매겨 수신 시 사용되는 스팸 방지 도구에 의해 스팸으로 간주되는 위험을 메시지가 발생하는지를 판단할 수 있습니다. For more on this, see [Previewing messages](../../sending/using/previewing-messages.md).

메시지 내용 편집기에서 을 클릭합니다 **[!UICONTROL Preview]**. 스팸 방지 검사에서 이 메시지의 위험성이 높은 경우 경고 메시지가 표시됩니다. 세부 사항 **[!UICONTROL Anti-spam analysis]** 을 보려면 을 클릭합니다.

![](assets/sending_anti-spam_analysis.png)

## 메시지 응답성 확인 {#message-responsiveness}

메시지를 보내기 전에 메시지가 다른 장치에서 어떻게 보이는지 확인할 수 있습니다. 이는 다양한 웹 클라이언트, 웹 메일 및 장치에서 최적의 방식으로 표시되도록 하기 위한 것입니다.

이를 위해 Adobe Campaign은 렌더링을 캡처하여 전용 보고서에서 사용할 수 있도록 합니다. 이렇게 하면 수신되었을 수 있는 다른 컨텍스트에서 전송된 메시지를 미리 볼 수 있습니다.

자세한 내용은 [이메일 렌더링](../../sending/using/email-rendering.md)을 참조하십시오.

![](assets/inbox_rendering_report_3.png)
