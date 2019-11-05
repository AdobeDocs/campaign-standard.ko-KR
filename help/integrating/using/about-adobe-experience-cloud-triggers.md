---
title: Adobe Experience Cloud 트리거 기본 정보
description: Adobe Analytics를 사용하여 고객의 특정 행동을 추적하면 Adobe Campaign에서 개인화된 이메일을 고객에게 보낼 수 있습니다.
page-status-flag: 활성화 안 함
uuid: 0aa4bd6e-1bb5-4d0b-913b-eca93f050acd
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 통합
content-type: reference
topic-tags: 작업-with-campaign-and-triggers
discoiquuid: e526b205-2d01-4a8b-9685-ba1d9a1f459f
context-tags: 트리거,개요;트리거,기본
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# Adobe Experience Cloud 트리거 기본 정보{#about-adobe-experience-cloud-triggers}

Adobe Experience Cloud 활성화 핵심 서비스와 Adobe Campaign 간의 통합을 **[!UICONTROL Triggers]** 통해 Adobe Analytics를 통해 웹 사이트에서 추적되는 특정 행동에 대한 반응으로 개인화된 이메일을 고객에게 보낼 수 있습니다(15분 이내).

Adobe Experience Cloud에서는 모니터링하려는 고객 행동(예: 웹 사이트에서 방문을 포기하고 웹 사이트에서 검색을 했지만 구매하지 않은 클라이언트 또는 세션이 만료된 클라이언트)을 정의하는 서로 다른 트리거를 정의합니다. 트리거를 만들 때 트리거의 조건과 이벤트에서 Adobe Campaign으로 전송되는 데이터를 정의합니다.

 Adobe Campaign에서 이전에 만든 트리거를 선택하고 데이터 마트 데이터로 이벤트 데이터를 보완하며 해당 트리거에 연결된 트랜잭션 메시지 템플릿을 정의합니다. 예를 들어 클라이언트가 웹 사이트에서 자신의 방문을 중단할 경우 이벤트가 Adobe Campaign으로 전송되어 15분 이내에 클라이언트에 전송된 리마케팅 이메일을 통해 이 이벤트를 활용할 수 있습니다.

**관련 항목:**

* 다양한 유형의 트리거에 대해 알아봅니다.Adobe [Experience Cloud 설명서](https://marketing.adobe.com/resources/help/en_US/mcloud/triggers.html).
* 사이트 활동 [기반의 리마케팅 메시지 트리거 비디오를](https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html#step-two) 시청하십시오.
* 두 가지 포기 [트리거 사용 사례를](../../integrating/using/abandonment-triggers-use-cases.md)살펴보십시오.

## 사용자 프로세스 트리거 {#triggers-user-process}

>[!CAUTION]
>
>주 사용자 단계를 실행하기 전에 기능을 구성해야 합니다. 자세한 내용은 기능 [활성화,](../../integrating/using/configuring-triggers-in-experience-cloud.md#activating-the-functionality)솔루션 및 서비스 [구성](../../integrating/using/configuring-triggers-in-experience-cloud.md#configuring-solutions-and-services) 및 Campaign에서 매핑된 [트리거 만들기를 참조하십시오](../../integrating/using/using-triggers-in-campaign.md#creating-a-mapped-trigger-in-campaign).

Adobe Campaign에서 사용자 프로세스의 주요 단계는 다음과 같습니다.

1. 기존 Adobe Experience Cloud 트리거에 연결된 트리거 이벤트를 만듭니다.
1. 트리거 이벤트를 게시합니다.
1. 트랜잭션 메시지 템플릿의 컨텐츠를 정의합니다.
1. 템플릿을 테스트합니다(테스트 프로필을 만들고 증명 보내기).
1. 트랜잭션 메시지 템플릿을 게시합니다.

전체 사용 사례는 [이 섹션에](../../integrating/using/abandonment-triggers-use-cases.md)설명되어 있습니다.

## 중요 정보 {#important-notes}

다음은 트리거 - 캠페인 통합을 사용하기 전에 고려해야 할 몇 가지 중요한 노트입니다.

* 트리거에는 푸시 알림이 지원되지 않습니다. 이메일 및 SMS만 지원됩니다.
* 이메일 ID, 페이지 이름 등과 같은 Analytics를 통해 캡처된 메타 데이터로 트리거를 보완할 수 있습니다.
* Campaign Standard에 저장된 프로필에 트리거를 조정하고 프로필 필드를 사용하여 메시지를 개인화할 수 있습니다.
* 트리거가 수신되면 처리 및 조정되고 발송됩니다. 받은 트리거의 볼륨, 템플릿에 사용된 개인화 필드의 수에 따라 약 5~15분이 소요됩니다.

>[!NOTE]
>
>모범 사례 및 기술 제한에 대한 자세한 내용은 트리거 [우수 사례 및 제한을](../../integrating/using/configuring-triggers-in-experience-cloud.md#triggers-best-practices-and-limitations)참조하십시오.

