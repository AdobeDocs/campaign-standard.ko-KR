---
solution: Campaign Standard
product: campaign
title: Adobe Campaign Standard의 게재 기능 기본 정보
description: 게재 전송을 최적화하기 위해 Adobe Campaign Standard에서 제공하는 도구 및 게재 기능과 관련된 개념과 모범 사례에 대해 알아봅니다.
audience: sending
content-type: reference
topic-tags: sheduling-messages
context-tags: delivery,schedule,back
feature: 전달성
role: User
level: Intermediate
exl-id: 5e523519-7192-4031-9d96-559af23074d9
source-git-commit: aeeb6b4984b3bdd974960e8c6403876fdfedd886
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 8%

---

# 전달성의 정의{#about-deliverability}

게재 기능을 사용하면 바운스 기능을 통해 수신자의 받은 편지함에 도달하거나 스팸으로 표시되지 않고 캠페인이 성공했는지 측정할 수 있습니다. [게재가 중요한 이유를 알아봅니다](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/deliverability-strategy-and-definition.html#why-deliverability-matters).

보다 정확하게 말하면 이메일 게재 능력은 개인 이메일 주소를 통해 짧은 시간 내에 컨텐츠와 형식 측면에서 예상되는 품질로 메시지의 목적지에 도달할 수 있는 능력을 결정하는 일련의 특성입니다. <!--These characteristics fall into four main categories: data quality, message and content, sending infrastructure, and reputation. Together, they form the foundation of a successful email deliverability program.-->

게재 기능의 의미와 주요 게재 가능성 용어, 개념 및 접근 방법에 대한 자세한 내용은 [Adobe 게재 가능성 모범 사례 안내서](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=ko)를 참조하십시오.

## 게재 능력을 향상시키는 방법 {#deliverability-key-points}

게재 가능성 문제는 일반적으로 인터넷 서비스 제공업체 및 메일 서버 관리자가 구현하는 스팸으로부터 보호하는 조치와 연결됩니다.

* 성공적인 이메일 마케팅 캠페인을 디자인하는 방법에 대한 일반적인 권장 사항은 [게재 가능성 전략 및 정의](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/deliverability-strategy-and-definition.html)를 참조하십시오.

* Adobe Campaign 이메일의 게재 능력을 최적화하는 방법에 대한 자세한 내용은 이 섹션에 나열된 우수 사례를 사용하는 것이 좋습니다.

>[!NOTE]
>
>ISP는 스팸 메일로부터 고객을 보호하기 위해 새로운 정교한 필터링 기술을 지속적으로 개발해야 하므로, 이메일 게재 기능은 항상 변경되는 기준 및 규칙을 제공하는 것을 특징으로 합니다. 정기적으로 업데이트된 [Adobe 게재 가능성 모범 사례 안내서](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html)를 참조해야 합니다.

### 게재 가능성 비율

게재 가능성 비율은 게재 완료된 메시지 수와 비교하여 수신자의 받은 편지함에 히트한 메시지 수입니다. 게재 능력을 향상시키기 위해 이 비율을 높이는 작업을 할 수 있습니다.

Adobe Campaign을 사용하면 게재 가능한 비율은 많은 요인에 따라 달라집니다. 특히 다음과 같습니다.

* 인스턴스의 올바른 구성: 도움이 필요하면 Adobe 담당자에게 문의하십시오.
* 올바른 네트워크 구성: [이 섹션](../../sending/using/optimize-delivery.md#network-config) 및 [도메인 설정 및 전략](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/transition-process/infrastructure.html#domain-setup-and-strategy)을 참조하십시오.
* IP 주소 평판: [IP 전략](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/transition-process/infrastructure.html#ip-strategy)을 참조하십시오.
* 타겟팅된 주소의 품질: [격리 관리](../../sending/using/optimize-delivery.md#quarantine-management)를 참조하십시오.
* 낮은 [컴플레인](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/complaints.html) 및 [하드 바운스](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/bounces.html#hard-bounces) 비율.
* 메시지 콘텐츠: [전자 메일 콘텐츠 제어](../../sending/using/control-email-content.md)를 참조하십시오.
* 메시지 인증(SPF, DKIM, DMARC): [이 섹션](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/transition-process/infrastructure.html#authentication)을 참조하십시오.
* 보낸 사람 평판: 기본 ISP가 보낸 사람의 평판을 평가하는 방법에 대해 알려면 [이 섹션](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/internet-service-provider-specifics/overview.html)을 참조하십시오.

## 캠페인 게재 기능 도구 {#deliverability-tools}

Adobe Campaign은 플랫폼의 게재 성능을 추적하고 개선하기 위한 많은 도구를 제공합니다. 또한 이 페이지에서는 Campaign을 사용할 때 게재 능력을 최적화하기 위해 염두에 두어야 하는 주요 원칙을 강조 표시합니다.

### 메시지 작성

메시지를 구성, 디자인 및 테스트할 때 아래 나열된 섹션에 언급된 우수 사례를 따라야 합니다. Adobe Campaign에서 제공하는 모든 기능을 활용하면 게재 능력을 향상시킬 수 있습니다.

* [게재 모범 사례](../../sending/using/delivery-best-practices.md)
* [이메일 콘텐츠 제어](../../sending/using/control-email-content.md)
* [메시지 미리 보기](../../sending/using/previewing-messages.md)
* [증명 보내기](../../sending/using/sending-proofs.md)

### 이중 옵트인을 통해 동의 확인 {#double-opt-in}

잘못된 주소로 메시지를 보내지 않고, 부적절한 통신을 제한하며, 발신자의 평판을 향상시키려면, Adobe은 이중 옵트인 메커니즘을 구현하는 것이 좋습니다. 이렇게 하면 수신자가 의도적으로 구독했는지 확인할 수 있습니다.

자세한 내용은 [Campaign](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md)의 옵트인 및 옵트아웃 기본 정보 를 참조하십시오.

고객으로부터 데이터를 수집하는 모범 사례에 대한 자세한 내용은 [Adobe 게재 모범 사례 안내서](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/first-impressions/address-collection-and-list-growth.html#data-quality-and-hygiene)를 참조하십시오.

### 격리 관리 활용

Adobe Campaign은 일관되게 발생하는 스팸 불만, 하드 바운스 및 소프트 바운스를 수집하는 목록을 관리합니다.

게재 능력을 보호하기 위해 해당 목록에 있는 주소를 가진 수신자는 기본적으로 모든 향후 게재에서 제외됩니다. 이러한 연락처로 보내는 것은 보내는 신뢰도에 손상을 줄 수 있기 때문입니다.

일부 인터넷 액세스 제공 업체는 잘못된 주소의 비율이 너무 높은 경우 이메일을 자동으로 스팸으로 간주합니다. 따라서 격리 를 사용하면 이러한 제공 업체에 의해 차단 목록에 추가되지 않습니다.

자세한 정보는 다음 섹션을 참조하십시오.

* [게재 실패 이해](../../sending/using/understanding-delivery-failures.md)
* [격리 관리 이해](../../sending/using/understanding-quarantine-management.md)
* [격리와 차단 목록](../../sending/using/understanding-quarantine-management.md#quarantine-vs-denylist)

### 모니터링 및 보고 도구 사용

Adobe Campaign에서 제공하는 기능을 사용하여 게재 능력을 모니터링합니다.

Adobe Campaign에서는 내장된 실시간 지표 세트를 통해 게재가 어떻게 작동하는지 확인할 수 있습니다. <!--For example, you can check the number of messages that are successfully executed, sent and delivered. You can also verify the number of messages that have been opened and the number of messages/links that have been clicked.-->또한 게재 관련 통찰력을 향상하기 위해 완전히 사용자 지정 가능하고 실시간 보고서를 작성할 수 있습니다.

자세한 정보는 다음 섹션을 참조하십시오.

* [전달성 모니터링](../../sending/using/monitor-deliverability.md)

   <!--[Monitoring a delivery](../../sending/using/monitoring-a-delivery.md)-->
* [게재 실패 시 경고 받기](../../sending/using/receiving-alerts-when-failures-happen.md)
* [동적 보고서](../../reporting/using/about-dynamic-reports.md)

<!--## General recommendations

NOT SURE TO KEEP

Here are a few additional recommendations when it comes to deliverability.

### Send to valid addresses {#valid-addresses}

Spammers often use address generators based on lists of frequent names and first names; in addition, they rarely process technical notifications sent back by mail servers. A high rate of invalid addresses is often interpreted as a sign of spam.

Double opt-in mechanisms and effective handling of technical bounce messages make it possible to avoid this.

### Reduce complaint rate {#reduce-complaint-rate}

ISPs usually have a prominent means of reporting a received message as spam. This makes it possible to identify unreliable sources. By rapidly honoring opt-out requests, making regular use of a given list, verifying consent through a double opt-in system, and implementing feedback loops, you can reduce complaint rates.

<!--Sending to honeypot addresses {#honeypot-addresses}
ISPs and other organizations (refer to https://www.projecthoneypot.org/) make use of mailboxes that do not correspond to physical persons but are created simply to trick spammers. These so-called "honey pot" addresses are published on the Web in order to be collected by spambots and thus catch illegitimate senders. The use of a double opt-in mechanism precludes this sort of address being added to a list. When using a third-party list, you must be sure of the methods employed by its maintainer.-->

<!--## Sending on a regular basis {#regular-deliveries}

Spammers make programmed deliveries to maintain their reputation over time. They sometimes need to adapt their marketing plan to meet the best practices imposed by the ISPs and so, after a peak in reputation (ramp-up), they configure regular deliveries.-->
