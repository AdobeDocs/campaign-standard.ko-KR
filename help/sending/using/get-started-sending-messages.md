---
title: 테스트 및 보내기 시작
description: 메시지 준비, 테스트, 예약, 전송 및 모니터링
audience: sending
content-type: reference
topic-tags: about-sending-messages-with-campaign
role: User
level: Intermediate
exl-id: bcb28ef5-5cad-43c1-b11b-080abc791a72
source-git-commit: 6530ca1726a2aff18c5be9566d8008c317918e64
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 11%

---

# 테스트 및 보내기 시작 {#about-sending-messages-with-campaign}

<table>
<tr>
<td><img src="assets/do-not-localize/icon_prepare.svg" width="60px"><p><a href="#prepare-test-send">준비 및 테스트</a></p></td>
<td><img src="assets/do-not-localize/icon_send.svg" width="60px"><p><a href="#send-track-messages">전송, 모니터링 및 추적</a></p></td>
<td><img src="assets/do-not-localize/icon_deliverability.svg" width="60px"><p><a href="#improve-deliverability">게재 기능 지침</a></p></td></tr>
</table>

타겟을 정의하고 메시지 콘텐츠를 만든 후에는 게재의 콘텐츠, 개인화, 렌더링 및 구성을 준비하고 테스트해야 합니다. 이렇게 하면 메시지를 기본 타겟에게 보내기 전에 모든 것이 올바른지 확인할 수 있습니다. 이를 위해 미리 보기, 증명, 이메일 분야별 과제 테스트 또는 이메일 렌더링 등 다양한 기능을 사용할 수 있습니다.

마케팅 캠페인이 실행되고 서로 다른 메시지가 전송되면 로그를 사용하여 모니터링하여 캠페인의 성공을 확인하고 수신자에 대한 추적 정보를 검색합니다.

마지막으로, Campaign Standard에서 사용할 수 있는 게재 가능성 지침 및 도구를 활용하여 전달된 메시지 수를 개선하고 성공적인 마케팅 캠페인을 보장합니다.

![](assets/do-not-localize/how-to-video.png) [비디오에서 테스트 이메일을 보내고, 이메일 게재를 준비하고 보내는 방법을 알아봅니다](#video)

## 준비 및 테스트 {#prepare-test-send}

<img src="assets/do-not-localize/icon_prepare.svg" width="60px">

Campaign Standard **메시지 준비** 은 대상, 개인화 및 메시지의 유효성을 분석합니다. 이 단계에서 감지된 오류를 수정한 후에 계속 진행해야 합니다.

**미리 보기 및 테스트** 다양한 기능을 사용하여 메시지를 작성합니다. 증명을 전송하여 프로필 또는 타겟팅된 프로필을 테스트하고, 전자 메일의 제목 줄을 테스트하고, 메시지 렌더링을 확인하여 다양한 웹 클라이언트, 웹 메일 및 디바이스에서 최적의 방식으로 표시되는지 확인합니다.

Campaign 예약 기능을 활용하여 메시지를 보낼 시기를 정의합니다. 예를 들어 수신자의 시간대에 맞게 전송을 조정하거나 전송 시간을 최적화하거나 전송 날짜를 계산할 수 있습니다.

사용 **유형화** 피로, 제어 및 타기팅 규칙을 통해 메시지가 유효하고 품질 기준을 충족하는지 여부를 준비하는 동안 확인합니다. 예를 들어 이메일에 항상 제목 줄이 포함되어 있는지 확인하거나 메시지 수신자에서 구독 취소자를 제외합니다.

자세한 내용:

* [보내기 준비](../../sending/using/preparing-the-send.md)
* [메시지 미리 보기](../../sending/using/previewing-messages.md)
* [증명 보내기](../../sending/using/sending-proofs.md)
* [이메일 렌더링](../../sending/using/email-rendering.md)
* [메시지 예약](../../sending/using/about-scheduling-messages.md)
* [유형화 및 유형화 규칙 기본 정보](../../sending/using/about-typology-rules.md)

## 전송, 모니터링 및 추적 {#send-track-messages}

<img src="assets/do-not-localize/icon_send.svg"  width="60px">

메시지가 준비되면 로그 및 보고서 전송 및 액세스를 확인할 수 있습니다. **게재 모니터링** 캠페인의 성공을 측정합니다. 또한 Adobe Campaign은 이메일 경고 시스템을 제공하여 게재 성공 또는 실패와 격리 관리 기능을 추적합니다.

**비헤이비어 추적** 세션 및 영구 쿠키를 사용하여 추적 정보(클릭한 URL, 미러 페이지, 열린 메시지...)를 검색하는 메시지 수신자

마지막으로, Adobe Campaign을 구성하여 **이메일 사본 보관** 이메일 BCC를 통해 플랫폼에서 전송됩니다. 특히 규정 준수를 위해 모든 아웃바운드 이메일 메시지를 보관해야 하는 경우 이 기능을 활성화할 수 있습니다.

자세한 내용:

* [보내기 확인](../../sending/using/confirming-the-send.md)
* [메시지 추적](../../sending/using/tracking-messages.md)
* [이메일 숨은 참조를 통해 보관](../../sending/using/archiving.md)
* [게재 모니터링](../../sending/using/monitoring-a-delivery.md)
* [게재 실패 이해](../../sending/using/understanding-delivery-failures.md)
* [격리 관리 이해](../../sending/using/understanding-quarantine-management.md)

## 게재 기능 지침 {#improve-deliverability}

<img src="assets/do-not-localize/icon_deliverability.svg"  width="60px">

전달성을 사용하면 캠페인이 바운스 없이 또는 스팸으로 표시되지 않고 수신자의 받은 편지함에 도달했는지 측정할 수 있습니다.

Campaign Standard은 다음을 제공합니다. **전달성 도구** 게재율 보고서, 전송 시간 최적화, 메시지 미리 보기, 이메일 렌더링, 격리 관리 등 성공적으로 게재된 메시지 수를 개선하는 데 도움이 됩니다.

자세한 내용:

* [게재 기능 기본 정보](../../sending/using/about-deliverability.md)
* [전달성 모니터링](../../sending/using/monitor-deliverability.md)
* [Adobe 전달성 모범 사례 안내서](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=ko)
* [게재 처리량 제어](../../reporting/using/delivery-throughput.md)

## 추가 리소스

* [A/B 테스트 이메일 디자인](../../channels/using/designing-an-a-b-test-email.md)
* [메시지 시작](../../channels/using/key-steps-to-send-a-message.md)
* [게재 모범 사례](../../sending/using/delivery-best-practices.md)
* [컨트롤 그룹 추가](../../sending/using/control-group.md)

## 튜토리얼 비디오 {#video}

이 비디오는 테스트 이메일을 보내고, 준비한 다음 Campaign Standard에서 이메일 게재를 보내는 방법을 보여 줍니다.

>[!VIDEO](https://video.tv.adobe.com/v/24013/)

추가 Campaign Standard 방법 비디오를 사용할 수 있습니다 [여기](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/overview.html?lang=ko).
