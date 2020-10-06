---
title: Adobe Experience Cloud 트리거 기본 정보
description: 이제 Adobe Analytics로 고객의 특정 행동을 추적하여 Adobe Campaign에서 고객에게 개인화된 이메일을 보낼 수 있습니다.
page-status-flag: never-activated
uuid: 0aa4bd6e-1bb5-4d0b-913b-eca93f050acd
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-triggers
discoiquuid: e526b205-2d01-4a8b-9685-ba1d9a1f459f
context-tags: trigger,overview;trigger,main
internal: n
snippet: y
translation-type: ht
source-git-commit: 1e790f550f6eb84954f199caeda88a8fd90dfd85
workflow-type: ht
source-wordcount: '475'
ht-degree: 100%

---


# Adobe Experience Cloud 트리거 기본 정보{#about-adobe-experience-cloud-triggers}

Experience Cloud Activation 핵심 서비스 **[!UICONTROL Triggers]**&#x200B;와(과) Adobe Campaign 간의 통합을 통해 Adobe Analytics가 웹 사이트에서 추적한 특정 행동에 반응하여 고객에게 개인화된 이메일을 보낼 수 있습니다.

Adobe Experience Cloud에서 모니터링하려는 고객 행동(예: 웹사이트 방문을 중단한 고객이나 웹사이트에서 검색을 했지만 구매하지 않은 고객, 심지어 세션이 만료된 고객까지)에 대해 다양한 트리거를 정의합니다. 트리거를 만들 때는 트리거의 조건과 해당 이벤트 시 Adobe Campaign으로 전송할 데이터(pload)를 정의합니다.

Adobe Campaign에서 이전에 만든 트리거를 선택하고, 데이터마트 데이터로 이벤트 데이터를 강화하며, 해당 트리거에 연결된 트랜잭션 메시지 템플릿을 정의합니다. 예를 들어, 고객이 웹사이트 방문을 중단하면 Adobe Campaign으로 이벤트를 전송하여 15분 내로 해당 고객에게 보낼 리마케팅 이메일에 활용할 수 있습니다.

다음 다이어그램은 이 통합이 작동하는 방식을 자세히 설명합니다.

![](assets/triggers_diagram.png)

**관련 항목:**

* [Adobe Experience Cloud 설명서](https://docs.adobe.com/content/help/ko-KR/core-services/interface/activation/triggers.html)에서 트리거의 여러 유형에 대해 알아봅니다.
* [사이트 활동에 기반한 리마케팅 메시지 트리거](https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html#step-two) 비디오를 시청합니다.
* 두 가지 [중단 트리거 사용 사례](../../integrating/using/abandonment-triggers-use-cases.md)를 살펴봅니다.

## 사용자 프로세스 트리거{#triggers-user-process}

>[!CAUTION]
>
>주요 사용자 단계를 실행하기에 앞서 기능을 구성해야 합니다. 이에 대한 자세한 내용은 [기능 활성화](../../integrating/using/configuring-triggers-in-experience-cloud.md#activating-the-functionality), [솔루션 및 서비스 구성](../../integrating/using/configuring-triggers-in-experience-cloud.md#configuring-solutions-and-services) 및 [Campaign에서 매핑된 트리거 만들기](../../integrating/using/using-triggers-in-campaign.md#creating-a-mapped-trigger-in-campaign)를 참조하십시오.

Adobe Campaign 내 사용자 프로세스의 주요 단계는 다음과 같습니다.

1. 기존 Adobe Experience Cloud 트리거에 연결된 트리거 이벤트를 만듭니다.
1. 트리거 이벤트를 게시합니다.
1. 트랜잭션 메시지 템플릿의 콘텐츠를 정의합니다.
1. 템플릿을 테스트합니다(테스트 프로필을 만들어 증명 보내기).
1. 트랜잭션 메시지 템플릿을 게시합니다.

[이 섹션](../../integrating/using/abandonment-triggers-use-cases.md)에서 사용 사례 전체에 대한 설명을 볼 수 있습니다.

## 중요 정보 {#important-notes}

다음은 트리거-캠페인 통합을 사용하기 전에 고려해야 할 몇 가지 중요한 정보입니다.

* 푸시 알림은 트리거에 대해 지원되지 않습니다. 이메일 및 SMS만 지원됩니다.
* 이메일 ID, 페이지 이름 등 Analytics를 통해 캡처한 메타 데이터로 트리거를 보강할 수 있습니다.
* Campaign Standard에 저장된 프로필로 트리거를 조정하고 해당 프로필의 필드를 사용하여 메시지를 개인화할 수 있습니다.
* 트리거를 받는 즉시 처리 및 조정하고 전송합니다. 받은 트리거의 양, 템플릿에 사용한 개인화 필드 수에 따라 5~15분 정도 걸릴 수 있습니다.

>[!NOTE]
>
>모범 사례 및 기술 제한에 대한 자세한 내용은 [트리거 모범 사례 및 제한 사항](../../integrating/using/configuring-triggers-in-experience-cloud.md#triggers-best-practices-and-limitations)을 참조하십시오.

