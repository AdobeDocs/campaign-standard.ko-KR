---
solution: Campaign Standard
product: campaign
title: 메시지 전달 최적화
audience: delivery
content-type: reference
topic-tags: deliveries-best-practices
index: y
description: 업스트림 전송 프로세스를 안전하게 최적화하는 방법을 살펴볼 수 있습니다.
feature: 게재 가능성
role: 비즈니스 전문가
level: 중간
translation-type: tm+mt
source-git-commit: fb9a6218bb754f803affde1fdf6c6fc01570126f
workflow-type: tm+mt
source-wordcount: '754'
ht-degree: 6%

---


# 게재 최적화 {#optimize-delivery}

게재 생성을 시작하기 전에 몇 가지 조치를 수행하여 전송 프로세스를 보호하고 최적화할 수 있습니다.

다음 섹션에서는 Adobe Campaign의 최적의 구성을 위한 모범 사례 및 권장 절차를 간략히 설명합니다. 이러한 방법을 따르면 다운스트림에 직면할 수 있는 문제를 최소화할 수 있습니다.

## 플랫폼 성능

몇 가지 요소가 서버 성능에 직접적으로 영향을 주고 플랫폼을 느리게 할 수 있습니다.

* 개인화 요소의 수 및 유형:이메일의 개인화는 각 수신자에 대한 데이터를 데이터베이스에서 가져옵니다. 개인화 요소가 많이 있는 경우 전달을 준비하는 데 필요한 데이터의 양이 증가합니다.  [이 섹션](../../designing/using/personalization.md)에서 이메일 개인화에 대한 자세한 내용

* 서버 로드:캠페인이 동시에 여러 가지 작업을 처리할 때 성능이 느려질 수 있습니다. 데이터가 올바르고 제시간에 맞는지 확인하기 위해 서버는 모든 배달에 대해 들어오는 데이터와 나가는 모든 데이터를 조정해야 합니다.

   **팁**  - 이를 방지하려면 팀의 다른 구성원과 배달 예약을 조정하여 최상의 성과를 보장합니다.

* [워크플로우 실행](../../automating/using/about-workflow-execution.md):플랫폼 성능 문제가 발생하지 않도록 워크플로우를 모니터링하는 것이 중요합니다. 이 페이지](../../automating/using/monitoring-workflow-execution.md)에 나열된 지침을 따르십시오. [ [워크플로 우수 사례](../../automating/using/best-practices-workflows.md) 섹션에서 자세한 내용을 알아보십시오.

* [캠페인 제어 패널 기능](https://docs.adobe.com/content/help/en/control-panel/using/discover-control-panel/key-features.html)을 활용하여 [성능 모니터링](https://docs.adobe.com/content/help/en/control-panel/using/performance-monitoring/about-performance-monitoring.html) 기능을 사용하여 플랫폼을 모니터링할 수 있습니다.

## 네트워크 구성 {#network-config} 확인 중

대량의 이메일을 처리할 때 배달을 최적화하고 스패머로 오인되지 않도록 서버 ID를 숨기려고 하지 않는 적절한 네트워크 구성이 있는지 확인하십시오.

**팁**:브랜드의 웹 사이트에 해당하는 투명한 보낸 사람 주소를 사용합니다. 예를 들어, 여행사 회사는 발렌티노 호텔 체인을 관리하고 있다. 자체 웹사이트에 발렌티노.com 도메인을 보유하고 있다. 파리의 발렌티노 호텔을 홍보하기 위해, 파리.발렌티노.com 하위 도메인을 사용한다. 따라서 관련 보낸 사람 주소는 hotel@paris.valentino.com일 수 있습니다.

## 게재 기능 관리 {#deliverability-management}

통통 또는 스팸으로 표시되지 않고 수신자의 받은 편지함에 도달하려면 메시지 전달 비율을 향상시켜야 합니다.

* 배달능력이란 무엇입니까?

   * 받는 사람의 서버에서 받을 수 있는 기능을 결정하는 이메일 요인을 나타냅니다. ISP(Internet Service Providers)는 스팸으로 식별되는 이메일을 필터링하거나 이미지 다운로드를 차단합니다. 특정 도메인이 너무 많은 이메일을 보내는 것으로 판단되면 해당 보낸 사람으로부터 받을 이메일 수에 제한을 설정합니다.

   * 이메일 수신 여부를 확인할 때는 다음 4가지 주요 카테고리에 주력해야 합니다.데이터 품질, 메시지 및 컨텐츠, 전송 인프라 및 명성을 높일 수 있습니다. 이 주제에 대한 자세한 내용은 [이 섹션](../../sending/using/about-deliverability.md)을 참조하십시오.

* 새 플랫폼을 시작할 때 [이 페이지](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/transition-process/switching-email-platforms.html#transition-process)에 대한 자세한 권장 사항을 적용합니다.

* 도움이 필요하면 Adobe 담당자에게 문의하십시오.

## 격리 관리 {#quarantine-management}

우수한 검역 관리 과정을 유지하는 것이 귀하의 최대 관심사다.

새 플랫폼에서 이메일을 전송하기 시작할 때 자격이 완전히 없는 주소 목록을 사용할 수 있습니다. 잘못된 주소 또는 허니포트 주소(스패머를 조작하기 위해 만든 사서함만)로 보내는 경우 플랫폼의 명성은 낮아집니다. 철저한 격리 관리 프로세스를 통해 다음과 같은 이점을 얻을 수 있습니다.주소 품질을 유지할 수 있고 인터넷 액세스 제공업체의를 차단 목록 방지할 수 있으며 오류 속도를 줄이고 전달 및 처리량을 가속화할 수 있습니다.

**팁**

* 주소가 격리된 받는 사람은 배달 분석 중에 기본적으로 제외됩니다.타깃팅되지 않습니다. 이를 통해 게재 속도를 높일 수 있습니다. 오류율은 게재 속도에 상당한 영향을 미치기 때문입니다. 받은 편지함이 가득 찼거나 주소가 없는 경우 이메일 주소를 격리할 수 있습니다. [자세히 알아보기](../../sending/using/understanding-quarantine-management.md#identifying-quarantined-addresses)

* Adobe Campaign은 반환된 오류 유형에 따라 잘못된 주소를 관리합니다. 이 작업에 대한 자세한 정보는 [이 섹션](../../sending/using/understanding-quarantine-management.md)을 참조하십시오.

* 일부 인터넷 액세스 제공 업체는 잘못된 주소의 비율이 너무 높은 경우 이메일을 자동으로 스팸으로 간주합니다. 따라서 격리 기능을 사용하면 이러한 제공자가에 추가하는 것을 차단 목록 방지할 수 있습니다.

* 검역관리 역시 잘못된 전화 번호를 배달에서 제외함으로써 SMS를 보내는 비용을 줄이는 데 도움이 될 것이다.

## 이중 옵트인 메커니즘 {#double-opt-in}

잘못된 주소로 메시지를 보내지 않고, 부적절한 통신을 제한하며, 발신자의 명성을 높이기 위해, Adobe은 구독 후 확인을 위해 이중 옵트인 메커니즘을 구현할 것을 권장합니다. 이렇게 하면 수신자가 의도적으로 구독할 수 있습니다.

이 메커니즘을 구현하는 방법에 대한 자세한 내용은 [이 섹션](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md)에 설명되어 있습니다.

[프로필 및 대상 시작](../../audiences/using/get-started-profiles-and-audiences.md)에서 자세한 내용을 알아보십시오.
