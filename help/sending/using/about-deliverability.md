---
solution: Campaign Standard
product: campaign
title: Adobe Campaign Standard 제공 정보
description: 전달 능력과 관련된 개념과 모범 사례뿐만 아니라 Adobe Campaign Standard에서 배달 전송을 최적화하기 위해 제공하는 도구에 대해 알아봅니다.
audience: sending
content-type: reference
topic-tags: sheduling-messages
context-tags: delivery,schedule,back
feature: Deliverability
role: Business Practitioner
level: Intermediate
translation-type: tm+mt
source-git-commit: fb9a6218bb754f803affde1fdf6c6fc01570126f
workflow-type: tm+mt
source-wordcount: '749'
ht-degree: 6%

---


# 제공 가능 여부{#about-deliverability}

전달 기능을 사용하면 바운싱 또는 스팸으로 표시되지 않고도 수신자의 받은 편지함에 도달하는 캠페인의 성공을 측정할 수 있습니다. [탁월한 전달이 중요한 이유](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/deliverability-strategy-and-definition.html#why-deliverability-matters) 살펴보기

보다 정확하게 말하자면, 이메일 전달 기능은 컨텐츠 및 형식 측면에서 예상되는 품질과 함께, 짧은 시간 내에 개인 이메일 주소를 통해 해당 대상에 도달할 수 있는 메시지 기능을 결정하는 일련의 특성을 의미합니다.<!--These characteristics fall into four main categories: data quality, message and content, sending infrastructure, and reputation. Together, they form the foundation of a successful email deliverability program.-->

제공 기능에 대한 자세한 내용과 주요 전달 조건, 개념 및 접근 방법에 대한 자세한 내용을 살펴보려면 [Adobe 제공 우수 사례 가이드](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html)를 참조하십시오.

## 제공 능력을 향상시키는 방법 {#deliverability-key-points}

제공 가능성 문제는 일반적으로 인터넷 서비스 제공업체와 메일 서버 관리자가 구현한 스팸으로부터 보호하기 위한 조치와 연결됩니다.

* 성공적인 이메일 마케팅 캠페인을 디자인하는 방법에 대한 일반적인 권장 사항은 [배달 가능성 전략 및 정의](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/deliverability-strategy-and-definition.html)를 참조하십시오.

* Adobe Campaign 이메일의 전달 가능성을 최적화하는 방법에 대한 자세한 권장 사항을 보려면 이 섹션에 나열된 최상의 방법을 사용하는 것이 좋습니다.

>[!NOTE]
>
>ISP는 고객을 스팸으로부터 보호하기 위해 새로운 고급 필터링 기술을 지속적으로 개발해야 하기 때문에 이메일 전달은 항상 변화하는 기준과 규칙에 따라 결정됩니다. 정기적으로 업데이트되는 [Adobe 제공 우수 사례 가이드](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html)를 참조해야 합니다.

### 배달 가능 비율

배달율은 배달된 메시지 수와 비교하여 받는 사람의 받은 편지함을 히트한 메시지 수입니다. 택배 능력을 개선하기 위해, 당신은 이 비율을 증가시키는 데 노력할 수 있다.

Adobe Campaign을 사용하면 다음과 같은 여러 요인에 따라 배달 방법이 달라집니다.

* 인스턴스의 올바른 구성:도움이 필요하면 Adobe 담당자에게 문의하십시오.
* 올바른 네트워크 구성:[이 섹션](../../sending/using/optimize-delivery.md#network-config) 및 [도메인 설정 및 전략](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/transition-process/infrastructure.html#domain-setup-and-strategy)을 참조하십시오.
* IP 주소 평판:[IP 전략](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/transition-process/infrastructure.html#ip-strategy)을 참조하십시오.
* 타깃팅된 주소의 품질:[격리 관리](../../sending/using/optimize-delivery.md#quarantine-management)를 참조하십시오.
* [불만 사항](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/complaints.html) 및 [하드 바운스](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/bounces.html#hard-bounces) 비율이 낮습니다.
* 메시지 내용:[이메일 컨텐트 제어](../../sending/using/control-email-content.md)를 참조하십시오.
* 메시지 인증(SPF, DKIM, DMARC):[이 섹션](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/transition-process/infrastructure.html#authentication)을 참조하십시오.
* 보낸 사람 의견:기본 ISP가 보낸 사람의 명성을 평가하는 방법에 대해 알려면 [이 섹션](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/internet-service-provider-specifics/overview.html)을 참조하십시오.

## 캠페인 제공 도구 {#deliverability-tools}

Adobe Campaign은 플랫폼의 제공 성능을 추적하고 개선하는 다양한 툴을 제공합니다. 또한 이 페이지에서는 Campaign 사용 시 전달 가능성을 최적화하기 위해 고려해야 하는 주요 원칙을 강조 표시합니다.

### 메시지를 주의 깊게 작성

메시지를 구성, 디자인 및 테스트할 때는 아래 나열된 섹션에 설명된 우수 사례를 따라야 합니다. Adobe Campaign에서 제공하는 모든 기능을 활용하면 제공 능력을 향상시킬 수 있습니다.

* [게재 모범 사례](../../sending/using/delivery-best-practices.md)
* [이메일 콘텐츠 제어](../../sending/using/control-email-content.md)
* [메시지 미리 보기](../../sending/using/previewing-messages.md)
* [증명 보내기](../../sending/using/sending-proofs.md)

### 이중 옵트인 {#double-opt-in}을 통해 동의 확인

잘못된 주소로 메시지를 보내지 않고, 부적절한 통신을 제한하며, 발신자의 명성을 높이기 위해, Adobe은 이중 옵트인 메커니즘을 구현할 것을 권장합니다. 이렇게 하면 수신자가 의도적으로 가입했는지 확인할 수 있습니다.

이에 대한 자세한 내용은 [캠페인 옵트인 및 옵트아웃 정보를 참조하십시오](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md).

고객으로부터 데이터를 수집할 때의 모범 사례에 대한 자세한 내용은 [Adobe 제공 우수 사례 가이드](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/first-impressions/address-collection-and-list-growth.html#data-quality-and-hygiene)를 참조하십시오.

### 격리 관리 활용

Adobe Campaign은 일관되게 발생하는 스팸 불만, 하드 바운스 및 소프트 바운스 수를 수집하는 목록을 관리합니다.

배달 능력을 보호하기 위해 해당 목록에 있는 주소를 가진 수신자는 이러한 연락처로 보내는 것이 사용자의 전송 명성을 손상시킬 수 있으므로 기본적으로 이후의 모든 배달에서 제외됩니다.

일부 인터넷 액세스 제공 업체는 잘못된 주소의 비율이 너무 높은 경우 이메일을 자동으로 스팸으로 간주합니다. 따라서 격리 기능을 사용하면 이러한 제공자가에 추가하는 것을 차단 목록 방지할 수 있습니다.

자세한 내용은 다음 섹션을 참조하십시오.

* [게재 실패 이해](../../sending/using/understanding-delivery-failures.md)
* [격리 관리 이해](../../sending/using/understanding-quarantine-management.md)
* [격리 대 차단 목록](../../sending/using/understanding-quarantine-management.md#quarantine-vs-denylist)

### 모니터링 및 보고 툴 사용

Adobe Campaign에서 제공하는 기능을 사용하여 제공 여부를 모니터링할 수 있습니다.

Adobe Campaign을 사용하면 내장된 실시간 표시기를 통해 배달이 어떻게 수행되는지 확인할 수 있습니다. <!--For example, you can check the number of messages that are successfully executed, sent and delivered. You can also verify the number of messages that have been opened and the number of messages/links that have been clicked.-->또한 필요에 따라 변경 가능한 실시간 보고서를 작성하여 게재에 대한 인사이트를 향상시킬 수 있습니다.

자세한 내용은 다음 섹션을 참조하십시오.

* [게재 기능 모니터링](../../sending/using/monitor-deliverability.md)

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
