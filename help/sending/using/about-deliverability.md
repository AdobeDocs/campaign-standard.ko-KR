---
title: Adobe Campaign Standard의 제공 정보
description: 배달 능력과 관련된 개념과 모범 사례뿐만 아니라 배달 전송을 최적화하기 위해 Adobe Campaign Standard이 제공하는 도구에 대해 알아봅니다.
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
source-git-commit: df70a2165c5d3a4b553565d9a91ec3f8da1b44aa
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 6%

---


# 게재 기능 기본 정보{#about-deliverability}

전달 기능을 사용하면 바운싱 또는 스팸으로 표시되지 않고도 수신자의 받은 편지함에 도달하는 캠페인의 성공을 측정할 수 있습니다.

배달 가능 비율은 많은 요인, 특히

* 인스턴스의 올바른 구성
* 귀하의 IP 주소 평판
* 타깃팅된 주소의 품질
* 불만 및 이탈률 감소
* 메시지 내용
* 메시지 인증(SPF, DKIM, DMARC)
* 보낸 사람 평판

## 확인할 주요 사항 {#deliverability-key-points}

Adobe Campaign 이메일의 전달 가능성을 최적화하려면 아래 나열된 우수 사례를 사용하는 것이 좋습니다. 제공 능력 문제는 일반적으로 인터넷 서비스 제공업체와 메일 서버 관리자가 시행하는 스팸으로부터 보호하는 조치와 관련이 있습니다.

이메일 전달 능력은 메시지 수신, 이메일 주소를 통해, 짧은 시간 내에, 그리고 컨텐츠 및 형식 측면에서 예상되는 품질을 결정하는 일련의 특성입니다. 이러한 특성은 다음 네 가지 주요 카테고리로 분류됩니다.데이터 품질, 메시지 및 컨텐츠, 전송 인프라 및 명성을 높일 수 있습니다. 이들은 성공적인 이메일 전달 프로그램의 기반이 됩니다.

배달율은 받는 사람에게 성공적으로 배달된 이메일의 수입니다.
배달이 잘 되는지 확인할 수 있는 주요 사항 목록이 있습니다.

## 전달 기능 툴 {#deliverability-tools}

먼저, Campaign Standard과 함께 제공되는 제공 툴에 대한 설명서를 참조하기 시작합니다.
* [전달 모범 사례](https://helpx.adobe.com/kr/campaign/kb/delivery-best-practices.html)
* [보낸 사람 이름 맞춤화](../../designing/using/personalization.md#personalizing-the-sender)
* [이메일의 제목란 테스트](../../sending/using/testing-subject-line-email.md)
* [보내는 시각 최적화](../../sending/using/optimizing-the-sending-time.md)
* [메시지 미리 보기](../../sending/using/previewing-messages.md)
* [이메일 렌더링](../../sending/using/email-rendering.md)
* [게재 모니터링](../../sending/using/monitoring-a-delivery.md)
* [게재 실패 시 경고 받기](../../sending/using/receiving-alerts-when-failures-happen.md)
* [게재 실패 이해](../../sending/using/understanding-delivery-failures.md)
* [격리 관리 이해](../../sending/using/understanding-quarantine-management.md)
* [격리 대 차단 목록](../../sending/using/understanding-quarantine-management.md#quarantine-vs-denylist)
* [동적 보고서](../../reporting/using/about-dynamic-reports.md)

## 네트워크 구성 확인 {#network-configuration}

스팸들은 그들의 실체를 숨기려고 노력하고 그 결과 그들의 서버를 식별하기 어렵게 만들었다. 서버의 ID를 숨기려고 하지 않는 합법적인 네트워크 구성은 대량의 이메일을 전송하는 데 반드시 필요합니다.

## 유효한 주소로 전송 {#valid-addresses}

주소 생성기는 자주 이름과 성명 목록을 기반으로 사용한다.또한 메일 서버에서 발송한 기술 알림은 거의 처리되지 않습니다. 잘못된 주소의 비율이 높은 것은 종종 스팸의 신호로 해석됩니다. 이중 옵트인 메커니즘과 효과적인 기술 바운스 메시지 처리를 통해 이러한 문제를 방지할 수 있습니다.

## 불만률 감소 {#reduce-complaint-rate}

ISP는 일반적으로 수신한 메시지를 스팸으로 보고하는 중요한 방법을 가지고 있습니다. 이렇게 하면 신뢰할 수 없는 출처를 파악할 수 있다. 옵트아웃 요청을 신속하게 준수하고, 지정된 목록을 정기적으로 사용하고, 이중 옵트인 시스템을 통해 동의 여부를 확인하고, 피드백 루프를 구현함으로써 불만율을 줄일 수 있습니다.

## 허니포트 주소로 보내기 {#honeypot-addresses}

ISP와 기타 조직(https://www.projecthoneypot.org/ 참조)은 실제 인력에 해당되지 않지만 단순히 스패머를 조작할 목적으로 생성된 사서함을 사용합니다. 이른바 &#39;허니 포트&#39;라는 주소는 스팸보트가 정해서 불법 송신자를 잡기 위해 웹에 게시된다. 이중 옵트인 메커니즘의 사용은 목록에 추가되는 이러한 종류의 주소를 사용하지 못하게 합니다. 타사 목록을 사용할 때는 해당 관리자가 사용하는 방법을 반드시 확인해야 합니다.

## 메시지 내용 적용 {#adapt-message-content}

특정 메시지의 콘텐츠는 특정 필터를 스팸으로 감지할 수 있습니다. 특정 단어의 사용, 제목 줄 및 메시지 내에 느낌표를 사용하는 경우, 스팸의 등장으로 읽습니다. 스팸 차단 필터가 불쾌한 텍스트를 자동으로 분석하지 않도록 텍스트를 이미지로 바꾸기 위해 스팸 메일을 보내는 사람도 알려져 있다. 이에 대한 응답으로, 비율이 높은 메시지(HTML 형식)나 이미지가 첨부 파일로 차단될 수 있습니다.

## 정기적으로 전송 {#regular-deliveries}

스팸들은 오랜 시간 동안 명성을 유지하기 위해 프로그램 배달을 한다. 경우에 따라 ISP가 부과한 모범 사례를 충족하기 위해 마케팅 계획을 조정해야 하며 평판이 최고(경사)된 후에는 정기적으로 배송을 구성해야 합니다.
