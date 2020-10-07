---
title: 보내기 전 확인
seo-title: 보내기 전 확인
page-status-flag: never-activated
uuid: a540efc7-105d-4c7f-a2ee-ade4d22b3445
contentOwner: sauviat
products: SG_CAMPAIGN/CLASSIC
audience: delivery
content-type: reference
topic-tags: deliveries-best-practices
discoiquuid: 0cbc4e92-482f-4dac-a1fb-b738e7127938
index: y
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 15%

---


# 보내기 전에 모든 확인 수행 {#perform-all-checks}

메시지가 준비되면, 모든 장치에서 해당 컨텐츠가 올바르게 표시되는지 확인하고, 개인화나 깨진 링크 등의 오류를 포함하지 마십시오.

메시지를 보내기 전에 매개 변수 및 구성이 전달과 일치하는지 확인하십시오.

## 유효성 검사가 중요한 이유 {#validation-is-key}

배달을 보내기 전에 받는 사람이 실제로 보내려는 메시지를 받게 해야 합니다. 이렇게 하려면 메시지 내용 및 배달 매개 변수의 유효성을 확인해야 합니다.

이 단계를 통해 가능한 오류를 감지하여 주 타겟으로 전달하기 전에 수정할 수 있습니다.

배달을 확인하는 단계는 이 섹션 [에 나와 있습니다](../../sending/using/get-started-sending-messages.md#prepare-test-send).

## 전자 메일 렌더링 {#email-rendering}

**[!UICONTROL Send]** 버튼을 누르기 전에 메시지가 다양한 웹 클라이언트, 웹 메일 및 디바이스에서 최적의 방식으로 표시되는지 확인하십시오.

이를 위해 Adobe Campaign은 렌더링을 캡처하여 전용 보고서에서 사용할 수 있도록 합니다. 이렇게 하면 수신되었을 수 있는 다른 컨텍스트에서 전송된 메시지를 미리 볼 수 있습니다.

**팁**:

* 수신될 수 있는 다른 컨텍스트에서 보낸 메시지를 볼 수 있습니다.웹메일, 메시지 서비스, 모바일 등

* 이메일 렌더링 기능은 이메일 캠페인이 주요 ISP(Internet Service Providers)와 웹 메일 서비스의 필터를 성공적으로 통과하는지 여부를 식별하기 위해 중요합니다. 이러한 도구는 이메일의 시험판 사본을 테스트 받은 편지함의 네트워크로 전송하므로, 이러한 서비스에서 메시지가 어떻게 표시되거나 렌더링되는지 확인할 수 있습니다. 또한 보고서 및 코드 교정 옵션을 포함하여 빠르게 식별하고 전달을 개선하는 수정 사항을 만들 수 있습니다.

이 섹션 [에서 자세히 알아보십시오](../../sending/using/email-rendering.md).

## 증명 메시지 {#proof-messages}

교정본을 전송하면 옵트아웃 링크, 미러 페이지 및 기타 링크를 확인하고, 메시지를 확인하고, 이미지가 표시되는지 확인하고, 가능한 오류 감지 등을 수행할 수 있습니다. 또한 다양한 디바이스에서 디자인과 렌더링을 확인할 수 있습니다.

이 섹션 [에서 자세히 알아보십시오](../../sending/using/sending-proofs.md).

## A/B 테스트 배달 설정 {#a-b-testing-deliveries}

이메일 전달에 필요한 컨텐츠가 여러 개 있는 경우 A/B 테스트를 사용하여 타깃팅된 모집단에게 가장 큰 영향을 미치는 버전을 확인할 수 있습니다.

**팁**:

* 수신자의 일부에게 다른 버전 보내기

* 성공률이 가장 높은 타겟을 선택하고 나머지 타겟으로 보냅니다.

이 섹션 [에서 자세히 알아보십시오](../../channels/using/designing-an-a-b-test-email.md).

