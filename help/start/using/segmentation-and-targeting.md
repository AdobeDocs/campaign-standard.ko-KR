---
title: 세분화 및 타겟팅
description: '"Adobe Campaign에서 프로필, 타깃팅 및 고객 제작에 대해 알아봅니다.고객을 구축하고, Adobe Experience Cloud 솔루션을 통해 고객을 공유하고, 마케팅 피로도를 방지할 수 있습니다."'
page-status-flag: never-activated
uuid: 71f53808-0309-49f6-a4ee-3446eac9758a
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: start
content-type: reference
topic-tags: about-adobe-campaign
discoiquuid: d8c8a318-9433-4aec-b378-fd0beb50e9fb
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 13430243e8f2840ca85e557798168f6380a7b0fa

---


# 세분화 및 타겟팅{#segmentation-and-targeting}

## 프로필 {#profiles}

Adobe Campaign의 유연한 데이터 모델을 사용하여 고객 프로필 데이터를 강화하고 새 특성 또는 표를 추가합니다. 그런 다음 이러한 고객 프로파일을 사용하여 세그멘테이션, 개인화 및 보고를 보다 정확하게 할 수 있습니다.

Adobe Campaign 프로필은 데이터베이스에 저장된 모든 연락처를 나타냅니다. 각 프로필은 데이터베이스의 한 항목에 해당되며 이 항목에는 해당 프로파일을 타깃팅하고 자격을 부여하며 개별적으로 추적하는 데 필요한 정보가 포함되어 있습니다. 즉, 프로필은 다음과 같습니다.클라이언트, 잠재 고객, 뉴스레터에 가입된 개인, 수신자, 사용자 또는 조직에 따라 다른 모든 명칭

고객 프로파일 기능은 모든 고객 데이터를 하나로 통합합니다.

![](assets/mkt_hist_view.png)

Adobe Campaign은 프로파일 획득을 위한 다양한 메커니즘을 제안합니다.온라인 [랜딩 페이지](../../channels/using/getting-started-with-landing-pages.md)수집, 수동 또는 [자동화된 가져오기 메커니즘](../../automating/using/about-data-import-and-export.md), Adobe Campaign 인터페이스의 [직접 입력](../../audiences/using/creating-profiles.md) , Campaign APIs Bulk를 통해 [](../../api/using/about-campaign-standard-apis.md)직접 생성

**관련 항목:**

* 프로필 섹션에서 다양한 유형의 프로파일에 대해 [알아봅니다](../../audiences/using/about-profiles.md) .
* **이 섹션에서** 조직의 활성 [프로필](../../audiences/using/active-profiles.md)수에 액세스합니다.
* 워크플로우 타깃팅 기능을 사용하여 데이터를 사용자 정의하고 계산, 집계, 중복 제거, 병합 등 복잡한 데이터 관리 작업을 처리하는 방법을 [알아봅니다.](../../automating/using/about-targeting-activities.md)

## Audiences {#audiences}

Adobe Campaign은 고객의 관심사와 연관성 있고 효과적인 메시지를 전달하고 고객의 참여를 효과적으로 유도하기 위해 고급 분석 및 타깃팅 기능을 통합합니다. 워크플로우 및 쿼리 편집기 덕분에, 보유한 정보, 활동, 언어, 선호도 또는 마케팅 내역에 따라 다른 캠페인에서 타깃팅할 대상을 만들 수 있습니다. 이렇게 하면 예를 들어 가입된 프로필을 필터링하거나 제한 없이 기준을 바탕으로 타겟 대상을 만들 수 있습니다.

대상은 [이 페이지에](../../audiences/using/about-audiences.md) 표시되며 대상 [섹션에 자세히](../../audiences/using/creating-audiences.md) 설명되어 있습니다.

**관련 항목:**

* 다국어 푸시 알림 [또는](../../channels/using/creating-a-multilingual-push-notification.md) [다국어 이메일을 전송하여 여러 지역의 다국어 사용자에게 전달하는 방법을 살펴볼 수 있습니다.](../../channels/using/creating-a-multilingual-email.md)
* 대상을 빌드하는 쿼리를 [만드는](../../audiences/using/creating-audiences.md#creating-query-audiences) 방법 살펴보기
* 워크플로우에서 목록 대상을 [만드는](../../audiences/using/creating-audiences.md#creating-list-audiences) 방법 살펴보기
* 워크플로우의 파일에서 [](../../audiences/using/creating-audiences.md#creating-file-audiences) 대상을 가져오는 방법 살펴보기
* Adobe Experience Cloud 솔루션을 통해 고객 [](../../audiences/using/creating-audiences.md#creating-experience-cloud-audiences) 공유

## 일반 데이터 보호 규정 {#general-data-protection-regulation}

GDPR은 데이터 보호 요구 사항을 통합하고 현대화한 유럽 연합의 새로운 개인 정보 보호 법입니다. GDPR은 EU에 거주하는 데이터 주체의 데이터를 보유하고 있는 Adobe Campaign 고객에게 적용됩니다. Adobe Campaign에서 이미 사용 가능한 개인 정보 보호 기능(동의 관리, 데이터 유지 설정 및 사용자 역할 포함) 이외에도 Adobe는 데이터 프로세서로서의 기능을 활용하여 특정 GDPR 요청에 대한 데이터 컨트롤러로서의 준비를 용이하게 합니다.

GDPR을 준수하는 데 도움이 되는 Adobe Campaign의 툴과 기능에 대한 자세한 내용은 이 [안내서를](https://docs.campaign.adobe.com/doc/standard/getting_started/en/ACS_GDPR.html) 참조하십시오.

## 피로 관리 {#fatigue-management}

유무 규칙을 통해 마케터는 과도한 요청된 프로파일을 캠페인에서 자동으로 제외시키는 글로벌 크로스채널 비즈니스 규칙을 설정할 수 있습니다.

피로 규칙을 구현하려면 프로필당 최대 메시지 수를 정의하고 규칙이 적용되는 기간을 선택합니다. 전달 준비 동안 이미 보낸 메시지 수에 따라 프로필이 해당되는 경우 전달에서 제외됩니다.

**관련 항목:**

* 샘플 세트를 통해 피로 규칙을 [디자인하는](../../administration/using/fatigue-rules.md#examples) 방법 살펴보기
* 유형 [규칙 작성 방법 살펴보기](../../administration/using/about-typology-rules.md)
* 필터 [규칙을](../../administration/using/filtering-rules.md) 사용하여 메시지 대상 세분화
