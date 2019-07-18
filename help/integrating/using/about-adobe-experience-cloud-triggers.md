---
title: Adobe Experience Cloud 트리거 정보
seo-title: Adobe Experience Cloud 트리거 정보
description: Adobe Experience Cloud 트리거 정보
seo-description: Adobe Analytics를 통해 고객의 특정 행동을 추적하면 Adobe Campaign에서 고객에게 개인화된 이메일을 보낼 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 0 AA 4 BD 6 E -1 BB 5-4 D 0 B -913 B-ECA 93 F 050 ACD
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 통합
content-type: 참조
topic-tags: working-with-campaign-and-triggers
discoiquuid: E 526 B 205-2 D 01-4 A 8 B -9685-BA 1 D 9 A 1 F 459 F
context-tags: 트리거, 개요; 트리거, 기본
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: cb6396228e42f99f7e184a82e6c894b09a164cd9

---


# About Adobe Experience Cloud Triggers{#about-adobe-experience-cloud-triggers}

Integration between the Experience Cloud Activation core service **[!UICONTROL Triggers]** and Adobe Campaign allows you to send personalized emails to your customers as a reaction to specific behaviors that are tracked on your website by Adobe Analytics (within 15 minutes).

Adobe Experience Cloud 에서는 웹 사이트에서 방문을 포기한 모든 클라이언트, 웹 사이트에서 검색을 수행했지만 구매가 끝난 클라이언트 또는 세션이 만료된 클라이언트를 비롯하여 모니터링하려는 고객 행동을 정의합니다. 트리거를 만들 때 트리거의 조건과 이벤트 (pload) 에 전송될 데이터를 Adobe Campaign에 정의합니다.

Adobe Campaign에서 이전에 만든 트리거를 선택하면 datamart 데이터를 사용하여 이벤트 데이터를 강화하고 해당 트리거에 연결된 트랜잭션 메시지 템플릿을 정의합니다. 예를 들어 클라이언트가 웹 사이트에서 방문을 포기하는 경우 Adobe Campaign로 이벤트가 전송되어 15 분 내에 클라이언트에 전송되는 재마케팅 이메일을 통해 이 이벤트를 활용할 수 있습니다.

**관련 항목:**

* Learn about the different types of triggers: [Adobe Experience Cloud documentation](https://marketing.adobe.com/resources/help/en_US/mcloud/triggers.html).
* Watch the [Trigger Remarketing Messages based on Site Activity](https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html#step-two) video.
* Discover our two [Abandonment Triggers use cases](../../integrating/using/abandonment-triggers-use-cases.md).

## Triggers user process {#triggers-user-process}

>[!CAUTION]
>
>기본 사용자 단계를 실행하기 전에 기능을 구성해야 합니다. For more on this refer to [Activating the functionality](../../integrating/using/configuring-triggers-in-experience-cloud.md#activating-the-functionality), [Configuring solutions and services](../../integrating/using/configuring-triggers-in-experience-cloud.md#configuring-solutions-and-services) and [Creating a mapped trigger in Campaign](../../integrating/using/using-triggers-in-campaign.md#creating-a-mapped-trigger-in-campaign).

Adobe Campaign의 사용자 프로세스의 주요 단계는 다음과 같습니다.

1. 기존 Adobe Experience Cloud 트리거에 연결된 트리거 이벤트를 만듭니다.
1. 트리거 이벤트를 게시합니다.
1. 트랜잭션 메시지 템플릿의 컨텐츠를 정의합니다.
1. 템플릿을 테스트합니다 (테스트 프로필 만들기 및 증명 전송).
1. 트랜잭션 메시지 템플릿을 게시합니다.

Complete use cases are described in [this section](../../integrating/using/abandonment-triggers-use-cases.md).

## Important notes {#important-notes}

다음은 트리거 - 캠페인 통합을 사용하기 전에 고려해야 할 몇 가지 중요한 노트입니다.

* 푸시 알림은 트리거에 대해 지원되지 않습니다. 이메일과 SMS만 지원됩니다.
* 이메일 ID, 페이지 이름 등과 같은 분석을 통해 캡처한 메타 데이터로 트리거를 보강할 수 있습니다.
* 트리거를 Campaign Standard에 저장된 프로필에 조정하고 프로필의 필드를 사용하여 메시지를 개인화할 수 있습니다.
* 트리거가 수신되면, 이 트리거를 처리 및 조정하고 발송합니다. 수신된 트리거 볼륨, 템플릿에 사용된 개인화 필드의 수에 따라 약 5 ~ 15 분 정도가 소요됩니다.

>[!NOTE]
>
>For more on best practices and technical limitations, refer to [Triggers best practices and limitations](../../integrating/using/configuring-triggers-in-experience-cloud.md#triggers-best-practices-and-limitations).

