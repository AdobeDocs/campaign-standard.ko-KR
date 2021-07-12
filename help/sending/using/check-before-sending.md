---
solution: Campaign Standard
product: campaign
title: 보내기 전 확인
audience: delivery
content-type: reference
topic-tags: deliveries-best-practices
index: y
description: '"메시지가 준비되면 보내기 전에 모든 검사를 수행하는 방법을 배웁니다."'
feature: 전달성
role: User
level: Intermediate
exl-id: dfc5fc00-87aa-4d22-ad7c-cc0ba1ee21be
source-git-commit: aeeb6b4984b3bdd974960e8c6403876fdfedd886
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 16%

---

# 보내기 전에 모든 검사를 수행합니다. {#perform-all-checks}

메시지가 준비되면, 모든 장치에서 해당 콘텐츠가 올바르게 표시되는지 확인하고 잘못된 개인화 또는 끊어진 링크와 같은 오류가 없는지 확인합니다.

메시지를 보내기 전에 매개 변수 및 구성이 게재와 일치하는지 확인하십시오.

## 유효성 검사가 중요한 이유 {#validation-is-key}

게재를 보내기 전에 수신자가 실제로 보낼 메시지를 수신하는지 확인해야 합니다. 이렇게 하려면 메시지 콘텐츠 및 게재 매개 변수의 유효성을 검사해야 합니다.

이 단계를 사용하면 주요 타겟에게 전달하기 전에 가능한 오류를 감지하고 수정할 수 있습니다.

게재 유효성 검사 단계는 이 섹션 [에 나와 있습니다.](../../sending/using/get-started-sending-messages.md#prepare-test-send)

## 이메일 렌더링 {#email-rendering}

**[!UICONTROL Send]** 버튼을 누르기 전에 메시지가 다양한 웹 클라이언트, 웹 메일 및 디바이스에서 최적의 방식으로 표시되는지 확인하십시오.

이를 위해 Adobe Campaign은 렌더링을 캡처하여 전용 보고서에서 사용할 수 있도록 합니다. 이렇게 하면 수신되었을 수 있는 다른 컨텍스트에서 전송된 메시지를 미리 볼 수 있습니다.

**팁**:

* 수신되었을 수 있는 다른 컨텍스트에서 전송된 메시지를 볼 수 있습니다. 웹 메일, 메시지 서비스, 모바일 등

* 이메일 렌더링 기능은 이메일 캠페인이 주요 ISP(Internet Service Providers) 및 웹 메일 서비스의 필터를 성공적으로 통과하는지 여부를 식별하는 데 중요합니다. 이러한 도구는 전자 메일의 사전 플라이트 사본을 테스트 받은 편지함 네트워크에 보내어, 이 서비스에서 메시지가 어떻게 표시되거나 렌더링되는지 확인할 수 있습니다. 또한 게재 능력을 향상시키는 데 도움이 되는 보고서 및 코드 수정 옵션이 포함되어 있을 수 있습니다.

이 섹션](../../sending/using/email-rendering.md)에서 추가 [을 알아보십시오.

## 증명 메시지 {#proof-messages}

증명을 보내면 옵트아웃 링크, 미러 페이지 및 기타 모든 링크를 확인하고, 메시지를 확인하고, 이미지가 표시되는지 확인하고, 가능한 오류 감지 등을 수행할 수 있습니다. 다른 장치에서 디자인과 렌더링을 확인할 수도 있습니다.

이 섹션](../../sending/using/sending-proofs.md)에서 추가 [을 알아보십시오.

## A/B 테스트 게재 설정 {#a-b-testing-deliveries}

이메일 게재에 대한 여러 컨텐츠가 있는 경우 A/B 테스트를 사용하여 타겟팅된 모집단에 가장 큰 영향을 주는 버전을 확인할 수 있습니다.

**팁**:

* 일부 수신자에게 다른 버전을 보냅니다

* 성공률이 가장 높은 대상자를 선택하고 나머지 타겟으로 보냅니다

이 섹션](../../channels/using/designing-an-a-b-test-email.md)에서 추가 [을 알아보십시오.
