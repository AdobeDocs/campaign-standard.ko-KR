---
solution: Campaign Standard
product: campaign
title: Adobe Campaign Standard에서 이메일 컨텐츠 제어
description: 이메일 컨텐츠를 편집할 때 Adobe Campaign Standard의 전달 가능성을 향상시키는 방법을 알아봅니다.
audience: sending
content-type: reference
topic-tags: sheduling-messages
context-tags: delivery,schedule,back
translation-type: tm+mt
source-git-commit: 1e7359db2de1a9c420af33ac85c0597c098ae3f8
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 8%

---


# 이메일 콘텐츠 제어{#control-email-content}

이메일 전달 비율을 향상시키고 이메일이 수신자에게 전달되도록 하려면 일정 수의 규칙을 준수해야 합니다.

* **보낸 사람 이름 및 주소**:주소는 발신자를 명시적으로 식별해야 합니다. 도메인을 소유해야 하며 발신자에게 등록되어 있어야 합니다. 도메인 레지스트리를 민영화하지 않아야 합니다.
* **제목**:과도한 대문자 및 구두점, 스패머가 자주 사용하는 단어(&quot;Win&quot;, &quot;무료&quot; 등)를 피하십시오.
* **이메일** 개인화:이메일을 개인화하면 메시지가 열릴 가능성이 높아집니다.
* **이미지 및 텍스트**:적절한 텍스트/이미지 비율(예: 60% 텍스트 및 40% 이미지)을 준수합니다.
* **구독 취소 링크 및 랜딩 페이지**:구독 취소 링크는 필수입니다. 표시 및 유효해야 하며 양식이 제대로 작동하는지 확인해야 합니다.
* **Adobe Campaign** 에서 제공하는 툴을 사용하여 이메일 컨텐츠를 최적화할 수 있습니다(전달 분석, 스팸 방지 분석).

이메일 컨텐츠 편집에 대한 자세한 내용은 [이메일 디자이너 개요](../../designing/using/designing-content-in-adobe-campaign.md) 및 [메시지 디자인 모범 사례](../../designing/using/designing-content-in-adobe-campaign.md#content-design-best-practices)를 참조하십시오.

## 보낸 사람 이름 및 주소 {#sender-name}

특정 ISP는 메시지를 승인하기 전에 보낸 사람 주소(보낸 사람)의 유효성을 확인합니다. 형식이 잘못된 주소는 수신 서버에서 거부될 수 있습니다. 올바른 주소가 인스턴스 수준 또는 가장 자주 사용하는 시나리오에서 제공되는지 확인해야 합니다. 관리자에게 문의하십시오.

![](assets/delivery_content_edition16.png)

자세한 내용은 [보낸 사람 이름](../../designing/using/personalization.md#personalizing-the-sender) 개인 지정을 참조하십시오.

## 전송 시간 최적화 {#send-time-optimization}

메시지의 성공률을 높이기 위해 수신자별 전송 시간을 수동으로 정의할 수 있습니다. 각 프로필은 가능한 한 지정된 날짜와 시간에 메시지를 수신합니다.

자세한 내용은 [전송 시간 최적화](../../sending/using/optimizing-the-sending-time.md)를 참조하십시오.

## 옵트아웃 링크 및 양식 {#opt-out}

기본적으로 메시지를 분석하면 유형 분류 규칙이 옵트아웃 링크가 포함되었는지 여부를 확인하고 누락되면 경고를 생성합니다.

보낼 때마다 옵트아웃 링크가 제대로 작동하는지 확인해야 합니다. 예를 들어 증명 자료를 보낼 때 링크가 유효한지, 양식이 오프라인 상태인지, 이 변경 내용의 유효성을 검사하면 더 이상 연락처 없음 상자의 값이 확인됩니다. 링크를 입력하거나 양식을 변경할 때 항상 인적 오류가 가능하므로 이 확인을 체계적으로 해야 합니다.

배달을 시작한 후 가입 해지에 대한 문제가 발견되더라도 옵트아웃 링크를 클릭하는 수신자에 대해 수동으로(예: 대량 업데이트 기능 사용) 가입 해지를 수행할 수 있습니다. 수신자는 선택을 확인할 수 없습니다.

일반적으로 이메일 주소 또는 이름과 같은 필드를 채우도록 요구함으로써 수신을 거부하려는 수신자의 방해가 되지 않도록 합니다. 구독 취소 랜딩 페이지에는 하나의 유효성 확인 단추만 있어야 합니다. 추가 확인 요청을 신뢰할 수 없습니다.사용자는 동일한 상자로 리디렉션된 두 개의 이메일 주소를 가질 수 있습니다(예:firstname.lastname@club.com 및 firstname.lastname@internet-club.com)을 참조하십시오. 프로필이 첫 번째 주소만 기억할 수 있고 다른 주소로 보낸 메시지를 통해 구독을 취소하려는 경우, 암호화된 식별자와 입력한 이메일 주소가 일치하지 않기 때문에 양식이 거부됩니다.

## 스팸 방지 분석 {#anti-spam-analysis}

Adobe Campaign의 메시지 편집기는 수신 시 사용되는 스팸 방지 도구에 의해 메시지가 스팸으로 간주될 수 있는 위험을 발생시키는지 여부를 결정하기 위해 이메일을 수신할 수 있는 **스팸 방지 분석**&#x200B;을 통합합니다. 자세한 내용은 [메시지 미리 보기](../../sending/using/previewing-messages.md)를 참조하십시오.

메시지 내용 편집기에서 **[!UICONTROL Preview]**&#x200B;을 클릭합니다. 스팸 방지 검사에서 이 메시지의 위험성이 높은 경우 경고 메시지가 표시됩니다. 세부 사항을 보려면 **[!UICONTROL Anti-spam analysis]**&#x200B;을 클릭합니다.

![](assets/sending_anti-spam_analysis.png)

## 메시지 응답성 확인 중 {#message-responsiveness}

메시지를 보내기 전에 메시지가 다른 장치에서 어떻게 보이는지 확인할 수 있습니다. 이는 다양한 웹 클라이언트, 웹 메일 및 장치에서 최적의 방법으로 표시되도록 하기 위한 것입니다.

이를 위해 Adobe Campaign은 렌더링을 캡처하여 전용 보고서에서 사용할 수 있도록 합니다. 이렇게 하면 수신되었을 수 있는 다른 컨텍스트에서 전송된 메시지를 미리 볼 수 있습니다.

자세한 내용은 [이메일 렌더링](../../sending/using/email-rendering.md)을 참조하십시오.

![](assets/inbox_rendering_report_3.png)
