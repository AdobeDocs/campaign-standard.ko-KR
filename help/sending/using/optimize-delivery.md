---
title: 메시지 게재 최적화
audience: delivery
content-type: reference
topic-tags: deliveries-best-practices
index: y
description: 전송 프로세스 업스트림을 보호하고 최적화하는 방법을 알아봅니다.
feature: Deliverability
role: User
level: Intermediate
exl-id: 28b0cf6d-c1f1-4d55-b9bc-0d6bfb063471
source-git-commit: 13d419c5fc51845ee14f8a3b288f4c467e0a60d9
workflow-type: tm+mt
source-wordcount: '727'
ht-degree: 4%

---

# 게재 최적화 {#optimize-delivery}

게재 만들기를 시작하기 전에 전송 프로세스 업스트림을 보호하고 최적화하는 몇 가지 작업을 수행할 수 있습니다.

다음 섹션에서는 Adobe Campaign의 최적 구성을 위한 모범 사례 및 권장 절차에 대해 설명합니다. 이러한 방법을 수행하면 다운스트림에 직면할 수 있는 문제가 최소화됩니다.

## 플랫폼 성능

서버 성능에 직접적인 영향을 주고 플랫폼 속도가 느려질 수 있는 요소는 다음과 같습니다.

* 개인화 요소 수 및 유형: 이메일의 개인화는 각 수신자에 대해 데이터베이스에서 데이터를 가져옵니다. 개인화 요소가 많으면 게재를 준비하는 데 필요한 데이터의 양이 증가합니다.  [이 섹션](../../designing/using/personalization.md)에서 전자 메일 개인화에 대해 자세히 알아보기

* 서버 로드: Campaign이 여러 작업을 동시에 처리할 때 성능이 저하될 수 있습니다. 서버는 모든 게재에 대해 들어오는 모든 데이터와 나가는 데이터를 조정하여 데이터가 정확하고 정시에 도착하는지 확인해야 합니다.

  **팁** - 이를 방지하려면 최상의 성능을 보장하도록 팀의 다른 구성원과 게재 일정을 조정하십시오.

* [워크플로우 실행](../../automating/using/about-workflow-execution.md): 플랫폼 성능 문제를 방지하려면 워크플로우를 모니터링해야 합니다. [이 페이지의 &#x200B;](../../automating/using/monitoring-workflow-execution.md)에 나열된 지침을 따르십시오. 자세한 내용은 [워크플로우 모범 사례](../../automating/using/best-practices-workflows.md) 섹션을 참조하세요.

* [Campaign Campaign 컨트롤 패널 기능](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/key-features.html?lang=ko)을 활용하여 [성능 모니터링](https://experienceleague.adobe.com/docs/control-panel/using/performance-monitoring/about-performance-monitoring.html?lang=ko) 기능을 사용하여 플랫폼을 모니터링할 수 있습니다.

## 네트워크 구성 확인 {#network-config}

대량의 이메일을 처리할 때 게재를 최적화하고 스패머로 오인되지 않도록 하려면 서버 ID를 숨기려 하지 않는 합법적인 네트워크 구성이 있는지 확인하십시오.

**팁**: 브랜드 웹 사이트에 해당하는 투명한 발신자 주소를 사용하십시오. 예를 들어, 여행사 회사는 발렌티노 호텔 체인을 관리합니다. 이 도메인은 웹 사이트의 valentino.com 도메인을 소유합니다. 파리의 발렌티노 호텔을 홍보하기 위해 paris.valentino.com 하위 도메인을 사용합니다. 따라서 관련 발신자 주소는 hotel@paris.valentino.com일 수 있습니다.

## 전달성 관리 {#deliverability-management}

바운스되지 않거나 스팸으로 표시되지 않고 수신자의 받은 편지함에 도달하려면 메시지의 게재 가능성을 개선해야 합니다.

* 전달성이란 무엇입니까?

   * 이메일은 수신자 서버에서 수락할 수 있는 이메일 기능을 결정하는 요인을 말합니다. ISP(인터넷 서비스 공급자)는 스팸으로 식별되는 이메일을 필터링하거나 이미지가 다운로드되지 않도록 차단합니다. 특정 도메인에서 너무 많은 이메일을 보내고 있다고 판단되면 해당 발신자로부터 받을 이메일 수에 대한 제한을 설정합니다.

   * 이메일의 전달성을 확인할 때는 데이터 품질, 메시지 및 콘텐츠, 전송 인프라, 신뢰도 등 네 가지 주요 카테고리에 중점을 두어야 합니다. 이 항목에 대한 자세한 내용은 [이 섹션](../../sending/using/about-deliverability.md)을 참조하세요.

* 새 플랫폼을 시작할 때 [이 페이지](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/transition-process/switching-email-platforms.html?lang=ko#transition-process)에 설명된 권장 사항을 적용하십시오.

* 도움이 필요하면 Adobe 담당자에게 문의하십시오.

## 격리 관리 {#quarantine-management}

좋은 방역 관리 프로세스를 유지하는 것이 최선의 이익입니다.

새 플랫폼에서 이메일을 보내기 시작할 때 정규화된 주소가 아닌 주소 목록을 사용할 수 있습니다. 잘못된 주소 또는 허니팟 주소(스패머를 속이기 위해 만들어진 사서함)로 보내는 경우 플랫폼의 신뢰도가 떨어지기 시작합니다. 훌륭한 격리 관리 프로세스는 주소 품질을 유지하고, 인터넷 액세스 제공업체의 차단 목록에 추가하다를 피하고, 오류율을 낮추어 게재 및 처리 속도를 높이는 데 도움이 됩니다.

**팁**

* 주소가 격리된 수신자는 기본적으로 게재 분석 중에 제외됩니다. 이 수신자는 타겟팅되지 않습니다. 이렇게 하면 오류율이 게재 속도에 중요한 영향을 미치므로 게재 속도가 빨라집니다. 예를 들어 받은 편지함이 가득 찼거나 주소가 없는 경우 이메일 주소를 격리할 수 있습니다. [자세히 알아보기](../../sending/using/understanding-quarantine-management.md#identifying-quarantined-addresses)

* Adobe Campaign은 반환된 오류 유형에 따라 잘못된 주소를 관리합니다. 이 작업에 대한 자세한 정보는 [이 섹션](../../sending/using/understanding-quarantine-management.md)을 참조하십시오.

* 일부 인터넷 액세스 제공 업체는 잘못된 주소의 비율이 너무 높은 경우 이메일을 자동으로 스팸으로 간주합니다. 따라서 이러한 공급자에 의해 차단 목록에 추가하다에 추가되는 것을 피할 수 있습니다.

* 또한 격리 관리를 통해 잘못된 전화번호를 게재에서 제외하여 SMS 전송 비용을 줄일 수 있습니다.

## 이중 옵트인 메커니즘 {#double-opt-in}

잘못된 주소로 메시지를 보내지 않도록 하고 부적절한 통신을 제한하며 보낸 사람의 평판을 향상시키기 위해 Adobe은 구독 후 확인을 위해 이중 옵트인 메커니즘을 구현하는 것을 권장합니다. 이렇게 하면 수신자가 의도적으로 가입했는지 확인하는 데 도움이 됩니다.

이 메커니즘을 구현하기 위한 자세한 내용은 [이 섹션](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md)에 요약되어 있습니다.

[프로필 및 대상자 시작](../../audiences/using/get-started-profiles-and-audiences.md)에서 자세히 알아보세요.
