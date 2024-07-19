---
title: 보내기 전 확인
audience: delivery
content-type: reference
topic-tags: deliveries-best-practices
index: y
description: "메시지가 준비되면 전송하기 전에 모든 검사를 수행하는 방법에 대해 알아봅니다."
feature: Deliverability
role: User
level: Intermediate
exl-id: dfc5fc00-87aa-4d22-ad7c-cc0ba1ee21be
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 15%

---

# 보내기 전에 모든 확인 수행 {#perform-all-checks}

메시지가 준비되면 모든 디바이스에서 해당 콘텐츠가 올바르게 표시되고 잘못된 개인화 또는 링크가 끊어지는 등의 오류가 없는지 확인합니다.

메시지를 보내기 전에 매개 변수 및 구성이 게재와 일치하는지 확인하십시오.

## 유효성 검사가 중요한 이유 {#validation-is-key}

게재를 보내기 전에 받는 사람이 실제로 보낼 메시지를 받게 해야 합니다. 이렇게 하려면 메시지 콘텐츠 및 게재 매개 변수의 유효성을 검사해야 합니다.

이 단계를 통해 가능한 오류를 감지하고 수정한 후 주 타겟에 전달할 수 있습니다.

게재 유효성 검사 단계는 [이 섹션](../../sending/using/get-started-sending-messages.md#prepare-test-send)에 표시됩니다.

## 이메일 렌더링 {#email-rendering}

**[!UICONTROL Send]** 버튼을 누르기 전에 메시지가 다양한 웹 클라이언트, 웹 메일 및 디바이스에서 최적의 방식으로 표시되는지 확인하십시오.

이를 위해 Adobe Campaign은 렌더링을 캡처하여 전용 보고서에서 사용할 수 있도록 합니다. 이렇게 하면 수신되었을 수 있는 다른 컨텍스트에서 전송된 메시지를 미리 볼 수 있습니다.

**팁**:

* 웹 메일, 메시지 서비스, 모바일 등 수신 가능한 다양한 컨텍스트에서 전송된 메시지를 볼 수 있습니다.

* 이메일 렌더링 기능은 이메일 캠페인이 주요 ISP(인터넷 서비스 공급자) 및 웹 메일 서비스의 필터를 성공적으로 통과했는지 여부를 식별하는 데 중요합니다. 이러한 도구는 테스트 받은 편지함 네트워크로 전자 메일의 사전 사본을 보내므로 이러한 서비스에서 메시지가 표시되거나 렌더링되는 방법을 알 수 있습니다. 또한 게재 능력을 향상시키는 것을 신속하게 식별하고 수정하는 데 도움이 되는 보고서 및 코드 수정 옵션이 포함될 수 있습니다.

자세한 내용은 [이 섹션](../../sending/using/email-rendering.md)을 참조하세요.

## 증명 메시지 {#proof-messages}

증명을 보내면 옵트아웃 링크, 미러 페이지 및 기타 링크를 확인하고, 메시지의 유효성을 검사하고, 이미지가 표시되는지 확인하고, 가능한 오류를 감지하는 등의 작업을 수행할 수 있습니다. 다른 장치에서 디자인과 렌더링을 확인할 수도 있습니다.

자세한 내용은 [이 섹션](../../sending/using/sending-proofs.md)을 참조하세요.

## A/B 테스트 게재 설정 {#a-b-testing-deliveries}

이메일 게재에 대한 콘텐츠가 여러 개 있는 경우 A/B 테스트를 사용하여 타겟팅된 모집단에 가장 큰 영향을 주는 버전을 확인할 수 있습니다.

**팁**:

* 일부 수신자에게 다른 버전 보내기

* 성공률이 가장 높은 프로그램을 선택하여 나머지 타겟으로 보냅니다.

자세한 내용은 [이 섹션](../../channels/using/designing-an-a-b-test-email.md)을 참조하세요.
