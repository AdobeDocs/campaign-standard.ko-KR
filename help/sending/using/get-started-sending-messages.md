---
title: 테스트 및 보내기 시작
description: 메시지 준비, 테스트, 예약, 전송 및 모니터링
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
source-git-commit: 4ae70ca95cb282a694c41361d859b19385db5673
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 11%

---


# 테스트 및 보내기 시작 {#about-sending-messages-with-campaign}

<table>
<tr>
<td><img src="assets/do-not-localize/icon_prepare.svg" width="60px"><p><a href="#prepare-test-send">준비 및 테스트</a></p></td>
<td><img src="assets/do-not-localize/icon_send.svg" width="60px"><p><a href="#send-track-messages">전송, 모니터링 및 추적</a></p></td>
<td><img src="assets/do-not-localize/icon_deliverability.svg" width="60px"><p><a href="#improve-deliverability">전달 가능성 지침</a></p></td></tr>
</table>

타겟을 정의하고 메시지 내용을 만들었으면 게재 컨텐츠, 개인화, 렌더링 및 구성을 준비하고 테스트해야 합니다. 따라서 메시지를 기본 타겟으로 보내기 전에 모든 것이 올바른지 확인할 수 있습니다. 이를 위해 미리 보기, 증명 자료, 이메일 제목 테스트 또는 이메일 렌더링과 같은 다양한 기능을 사용할 수 있습니다.

마케팅 캠페인이 실행되고 다른 메시지가 전송되면 로그를 사용하여 모니터링하여 캠페인의 성공을 확인하고 수신자에 대한 추적 정보를 검색합니다.

마지막으로, Campaign Standard에서 제공되는 전달 가능성 지침 및 도구를 활용하여 배달된 메시지 수를 개선하고 성공적인 마케팅 캠페인을 보장합니다.

## 준비 및 테스트 {#prepare-test-send}

<img src="assets/do-not-localize/icon_prepare.svg" width="60px">

Campaign Standard **메시지 준비** 기능은 대상, 개인화 및 메시지의 유효성을 분석합니다. 이 단계 중 검색된 오류는 나중에 계속 진행하려면 먼저 수정해야 합니다.

**다양한 기능을 사용하여 메시지 미리 보기 및 테스트** :교정을 보내 프로파일 또는 태그된 프로파일을 테스트하고, 이메일의 주제 라인을 테스트하며, 메시지 렌더링을 확인하여 다양한 웹 클라이언트, 웹 메일 및 디바이스에서 최적의 방식으로 표시되도록 할 수 있습니다.

Campaign 예약 기능을 활용하여 메시지가 언제 전송될지 정의할 수 있습니다. 예를 들어, 수신자의 시간대에서 전송을 조정하고, 전송 시간을 최적화하거나, 전송 날짜를 계산할 수 있습니다.

유형 **을 사용하여 준비** 동안 메시지가 유효한지, 피로, 제어 및 타깃팅 규칙을 통해 품질 기준을 충족하는지 확인합니다. 예를 들어 이메일에 항상 제목 줄이 포함되어 있는지 확인하거나 메시지 받는 사람 중에서 구독하지 않은 사람을 제외합니다.

자세한 내용:

* [보내기 준비](../../sending/using/preparing-the-send.md)
* [메시지 미리 보기](../../sending/using/previewing-messages.md)
* [증명 보내기](../../sending/using/sending-proofs.md)
* [이메일 렌더링](../../sending/using/email-rendering.md)
* [메시지 예약](../../sending/using/about-scheduling-messages.md)
* [유형화 및 유형화 규칙 기본 정보](../../sending/using/about-typology-rules.md)

## 전송, 모니터링 및 추적 {#send-track-messages}

<img src="assets/do-not-localize/icon_send.svg"  width="60px">

메시지가 준비되면 전송 및 액세스 로그와 보고서를 확인하여 전달을 **모니터링하고 캠페인의 성공을 측정할** 수 있습니다. Adobe Campaign은 또한 배송 성공 또는 실패를 추적할 수 있는 이메일 경고 시스템과 검역 관리 기능을 제공합니다.

**세션 및 영구 쿠키를 사용하여 추적 정보(클릭된 URL, 미러 페이지, 열린 메시지..)를 검색하여 메시지 수신자의 동작을** 추적합니다.

마지막으로, 이메일 BCC를 통해 플랫폼에서 보낸 이메일 **사본을** 유지하도록 Adobe Campaign을 구성할 수 있습니다. 특히, 조직에서 모든 아웃바운드 이메일 메시지를 규정 준수를 위해 보관해야 하는 경우 이 기능을 활성화할 수 있습니다.

자세한 내용:

* [보내기 확인](../../sending/using/confirming-the-send.md)
* [메시지 추적](../../sending/using/tracking-messages.md)
* [이메일 숨은 참조를 통해 보관](../../sending/using/archiving.md)
* [게재 모니터링](../../sending/using/monitoring-a-delivery.md)
* [게재 실패 이해](../../sending/using/understanding-delivery-failures.md)
* [격리 관리 이해](../../sending/using/understanding-quarantine-management.md)

## 전달 가능성 지침 {#improve-deliverability}

<img src="assets/do-not-localize/icon_deliverability.svg"  width="60px">

전달 기능을 사용하면 바운싱 또는 스팸으로 표시되지 않고도 수신자의 받은 편지함에 도달하는 캠페인의 성공을 측정할 수 있습니다.

Campaign Standard은 배달된 메시지의 수를 향상시키는 데 도움이 되는 몇 가지 **전달 가능 도구를** 제공합니다.전달 시간 보고서, 전송 시간 최적화, 메시지 미리 보기, 이메일 렌더링, 격리 관리 등

자세한 내용:

* [게재 기능 기본 정보](../../sending/using/about-deliverability.md)
* [게재 기능 모니터링](../../sending/using/monitor-deliverability.md)
* [평판 개선](../../sending/using/improving-reputation.md)
* [기술 추천](../../sending/using/technical-recommendations.md)
* [Control Delivery throughput](../../reporting/using/delivery-throughput.md)

## 추가 리소스

* [A/B 테스트 이메일 디자인](../../channels/using/designing-an-a-b-test-email.md)
* [테스트 보내기, 준비 및 이메일 보내기(비디오)](https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/communication-channels/email/sending-test-preparing-sending-email.html)
* [이메일 전달 및 보고서 검토(비디오)](https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/communication-channels/email/reviewing-personalized-email-delivery-and-reports.html)
* [이메일 시작하기](https://helpx.adobe.com/kr/campaign/kb/acs-get-started-with-emails.html)
* [전달 모범 사례](../../sending/using/delivery-best-practices.md)
* [컨트롤 그룹 추가](../../sending/using/control-group.md)
