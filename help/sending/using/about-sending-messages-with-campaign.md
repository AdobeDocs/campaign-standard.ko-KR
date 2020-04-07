---
title: Campaign에서 메시지 보내기 기본 정보
description: 메시지를 테스트하고 전송하는 다양한 단계를 살펴볼 수 있습니다.
page-status-flag: never-activated
uuid: 58666444-6e7c-4049-b2d2-8b26eabf5a82
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: about-sending-messages-with-campaign
discoiquuid: ae2eba1c-24ad-4839-afa9-5a2975570d9b
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e6c43770755e59bf2a2d49540a052ac0bd2a2438

---


# Campaign에서 메시지 보내기 기본 정보{#about-sending-messages-with-campaign}

타겟을 정의하고 메시지 컨텐츠를 만들었다면 컨텐츠, 개인화, 렌더링 및 구성을 테스트 및 승인하고 메시지를 기본 타겟으로 보내기 전에 모든 것이 올바른지 확인해야 합니다.

이를 위해 우수 사례는 다음과 같습니다.

* 전송 준비:이 단계에서는 전송할 메시지를 분석하고 준비할 수 있습니다. 메시지 준비는 대상, 개인화 및 메시지의 유효성을 분석합니다. 이 단계 중 감지된 오류는 나중에 다시 진행하기 전에 수정해야 합니다. 필요한 만큼 메시지 준비를 시작할 수 있습니다. For more on message preparation, refer to [this section](../../sending/using/preparing-the-send.md).

   >[!NOTE]
   >
   >캠페인에서 과다 복제된 프로파일을 자동으로 제외시키는 글로벌 크로스 채널 피로 규칙을 설정할 수 있습니다. 피로 [규칙을](../../sending/using/fatigue-rules.md)참조하십시오.

* 테스트 프로필을 사용하여 메시지를 미리 봅니다. For more on previewing messages, refer to [this section](../../sending/using/previewing-messages.md).
* 테스트 메시지로 교정본을 보냅니다. For more on proofs, refer to [this  section](../../sending/using/sending-proofs.md).
* 메시지 렌더링을 확인합니다.메시지가 다양한 웹 클라이언트, 웹 메일 및 장치에서 최적의 방식으로 표시되는지 확인하십시오. 이메일 렌더링에 대한 자세한 내용은 [이 섹션을](../../sending/using/email-rendering.md)참조하십시오.

그런 다음 다음을 수행할 수 있습니다.

* 전송을 예약합니다.메시지가 전송될 시기를 정의할 수 있습니다. 예를 들어 수신자의 시간대로 전송을 조정하고 전송 시간을 최적화하거나 전송 날짜를 계산할 수 있습니다. 자세한 내용은 [이 섹션을](../../sending/using/about-scheduling-messages.md)참조하십시오.
* 메시지 보내기:메시지가 준비되면 전송을 시작할 수 있습니다. 그런 다음 액세스 로그와 보고서를 사용하여 메시지 전달을 모니터링하고 캠페인의 성공을 측정할 수 있습니다. Adobe Campaign은 배달 성공 또는 실패를 추적할 수 있는 이메일 알림 시스템을 제공합니다. 자세한 내용은 [이 페이지를](../../sending/using/confirming-the-send.md)참조하십시오.

## 관련 항목

| 유용한 페이지 | 추가 리소스 |
|---|---|
| [전달 능력 최적화](../../sending/using/about-deliverability.md) | [피로 관리](../../sending/using/fatigue-rules.md) |
| [게재 모니터링](../../audiences/using/creating-profiles.md) | [A/B 테스트 이메일 디자인](../../channels/using/designing-an-a-b-test-email.md) |
| [오류가 발생하면 알림 받기](../../sending/using/receiving-alerts-when-failures-happen.md) | [게재 모니터링](../../sending/using/monitoring-a-delivery.md) |
| [컨트롤 그룹 만들기](../../automating/using/workflow-control-group.md) | [오류가 발생하면 알림 받기](../../sending/using/receiving-alerts-when-failures-happen.md) |
| [Control Delivery throughput](../../reporting/using/delivery-throughput.md) | [게재 모니터링](../../sending/using/monitoring-a-delivery.md) |