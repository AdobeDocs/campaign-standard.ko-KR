---
title: 세분화 및 타깃팅
seo-title: 세분화 및 타깃팅
description: 세분화 및 타깃팅
seo-description: '" Campaign에서 프로파일, 타깃팅 및 고객 제작에 대한 자세한 내용: 고객을 구축하고, Adobe Experience Cloud 솔루션을 통해 연락처를 공유하고, 마케팅 피로도를 피합니다. "'
page-status-flag: 정품 인증 안 함
uuid: 71 F 53808-0309-49 F 6-A 4 EE -3446 EAC 9758 A
contentOwner: Sauviat
products: sg_ campaign/standard
audience: start
content-type: 참조
topic-tags: about-adobe-campaign
discoiquuid: D 8 C 8 A 318-9433-4 AEC-B 378-FD 0 BEB 50 E 9 FB
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Segmentation and targeting{#segmentation-and-targeting}

## Profiles {#profiles}

Adobe Campaign의 유연한 데이터 모델을 사용하여 고객 프로파일 데이터를 강화하고 새로운 속성이나 표를 추가할 수 있습니다. 그런 다음 이러한 고객 프로파일을 사용하여 보다 정확한 세분화, 개인화 및 보고를 수행할 수 있습니다.

Adobe Campaign 프로필은 데이터베이스에 저장된 모든 연락처를 나타냅니다. 각 프로필은 해당 프로필에 필요한 정보를 포함하는 데이터베이스에 있는 하나의 항목에 해당하며, 이를 대상으로 지정하고 개별적으로 추적하게 됩니다. 즉, 프로필은 클라이언트, 잠재 고객, 뉴스레터, 수신자, 사용자 또는 조직에 따라 다른 액면가를 구독한 개인 사용자

고객 프로파일 기능은 모든 고객 데이터를 통합하여

![](assets/mkt_hist_view.png)

Adobe Campaign proposes various mechanisms for profile acquisition: collecting data online via [landing pages](../../channels/using/about-landing-pages.md), manual or [automated import mechanisms](../../automating/using/about-data-import-and-export.md), [direct input](../../audiences/using/creating-profiles.md) in the Adobe Campaign interface, bulk creation through [Campaign APIs](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html).

**관련 항목:**

* [프로필](../../audiences/using/about-profiles.md) 섹션에서 다양한 유형의 프로파일에 대해 알아보십시오.
* Access the number of **Active Profiles** in your organization in [this section](../../audiences/using/active-profiles.md).
* Learn how to customize your data, handle complex data management tasks, such as calculations, aggregates, de-dupes, and merges, using [workflow targeting capabilities](../../automating/using/about-targeting-activities.md)

## Audiences {#audiences}

고객의 관심사와 연관성 있고 효과적인 메시지를 전달하고 고객의 참여를 효과적으로 유도할 수 있도록 Adobe Campaign는 고급 분석 기능과 타겟팅 기능을 통합합니다. 워크플로우 및 쿼리 편집기에서는 사용자가 보유한 정보에 따라, 해당 활동, 해당 활동, 언어, 환경 설정 또는 마케팅 내역에 따라 타게팅되는 대상을 만들 수 있습니다. 예를 들어, 가입된 프로필을 필터링하거나, 무제한의 조건으로 타겟 대상을 만들 수 있습니다.

Audiences are presented [in this page](../../audiences/using/about-audiences.md) and detailed in the [Audiences](../../audiences/using/creating-audiences.md) section.

**관련 항목:**

* [다국어 푸시 알림](../../channels/using/creating-a-multilingual-push-notification.md) 또는 [다국어 이메일을 전송하여 여러 지역의 다국어 고객에게 도달하는 방법 학습](../../channels/using/creating-a-multilingual-email.md)
* Learn how to [create queries](../../audiences/using/creating-audiences.md#creating-query-audiences) to build audiences
* Learn how to [create list audiences](../../audiences/using/creating-audiences.md#creating-list-audiences) in a workflow
* Learn how to [import an audience from a file](../../audiences/using/creating-audiences.md#creating-file-audiences) in a workflow
* Learn how to [share audiences](../../audiences/using/creating-audiences.md#creating-experience-cloud-audiences) with Experience Cloud solutions

## General Data Protection Regulation {#general-data-protection-regulation}

GDPR는 데이터 보호 요구 사항을 통합하고 현대화한 유럽 연합의 새로운 개인 정보 보호 법입니다. GDPR는 EU의 데이터 주체에 대한 데이터를 보유한 Adobe Campaign 고객에게 적용됩니다. Adobe Campaign (동의 관리, 데이터 유지 설정 및 사용자 역할 포함) 에서 이미 사용할 수 있는 개인정보 보호 기능 이외에도, Adobe는 특정 GDPR 요청에 대한 데이터 관리자로서 귀하의 준비를 용이하게 하기 위해 데이터 처리자의 역할에서 이 기회를 포착하고 있습니다.

Refer to this [guide](https://docs.campaign.adobe.com/doc/standard/getting_started/en/ACS_GDPR.html) to learn more about the tools and functionalities that Adobe Campaign provides to help you become GDPR compliant.

## Fatigue management {#fatigue-management}

피로 규칙을 통해 마케터는 캠페인에서 요청되지 않은 프로필을 자동으로 제외시키는 글로벌 크로스채널 비즈니스 규칙을 설정할 수 있습니다.

피로도 규칙을 구현하려면 프로필당 최대 메시지 수를 정의하고 규칙이 적용될 기간을 선택합니다. 배달 준비 중에, 프로필은 이미 전송된 메시지의 수에 따라 해당하는 경우 배달에서 제외됩니다.

**관련 항목:**

* Learn how to [design fatigue rules](../../administration/using/fatigue-rules.md#examples) through a set of samples
* Learn how to create [typology rules](../../administration/using/about-typology-rules.md)
* [필터 규칙을](../../administration/using/filtering-rules.md) 사용하여 메시지 대상 세분화
