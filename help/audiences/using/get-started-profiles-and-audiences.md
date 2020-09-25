---
title: 프로필 및 대상자 시작
description: Adobe Campaign의 프로필 및 고객 관리에 대해 자세히 알아보십시오. 타깃팅된 모집단을 정의하고 대상을 선택하고 수신자를 필터링하며 데이터를 수집하고 프로필을 업데이트합니다.
page-status-flag: never-activated
uuid: f4cb6c38-c8d1-44ec-93f0-d0f5f30a3d9a
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: about-profiles-and-audiences
discoiquuid: fb436b17-1fc3-4fc3-94b9-f09f8aaf9699
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 1a7e6bf967cb1745ea357ad7ee054dc42397f6e2
workflow-type: tm+mt
source-wordcount: '613'
ht-degree: 7%

---


# 프로필 및 대상자 시작{#about-profiles-and-audiences}

<table>
<tr>
<td><img src="assets/do-not-localize/icon_segment.svg" width="60px"><p><a href="#segmenting-targeting">세그먼트화 및 타깃팅</a></p></td>
<td><img src="assets/do-not-localize/icon_permission.svg" width="60px"><p><a href="#permission">허가 및 동의</a></p></td>
<td><img src="assets/do-not-localize/icon_privacy.svg" width="60px"><p><a href="#privacy">개인 정보 보호 규정 준수</a></p></td></tr>
</table>

캠페인 통합 고객 프로필을 사용하면 하나의 뷰에서 모든 채널에서 고객과의 모든 상호 작용을 추적할 수 있으므로 고객에게 연관성 있고 개인화된 메시지를 전달할 수 있습니다.

데이터베이스를 대상으로 세분화하여 마케팅 캠페인의 타겟을 최적화합니다.

서비스 및 랜딩 페이지를 사용하여 고객의 권한 및 동의를 관리하여 손쉽게 옵트인 및 옵트아웃 메커니즘을 설정할 수 있습니다.

## 세그먼트화 및 타깃팅 {#segmenting-targeting}

<img src="assets/do-not-localize/icon_segment.svg" width="60px">

캠페인 또는 메시지를 만들 때 캠페인 데이터베이스의 연락처에서 선택하거나 단순 또는 고급 기준을 사용하거나 대상을 선택하여 게재의 대상을 지정할 수 있습니다.

통합된 고객 프로파일 **,**&#x200B;맞춤형 세그먼트 **및** 관리 그룹을 사용하여 모든 채널에서 보다 효과적으로 고객을 식별할 수 **있습니다**. 고객, 관심사, 인구 통계, 채널 선호도를 파악하여 개인화된 경험을 손쉽게 제작할 수 있습니다.

Adobe Campaign은 풍부한 고객 프로파일을 실시간으로 작성하여 고객의 취향 변화에 따라 연관성 있고 개인화된 제안을 제공할 수 있습니다. 또한 Adobe Campaign은 고급 분석, 데이터 관리 및 타깃팅 기능을 통합하여 고객을 유치합니다.

**프로필은** 데이터베이스에 저장된 개별 연락처입니다. 각 프로필은 데이터베이스의 한 항목에 해당되며 이 항목에는 해당 프로파일을 타깃팅하고 자격을 부여하여 개별적으로 추적하기 위한 필요한 정보가 포함되어 있습니다.Adobe Campaign은 온라인 및 오프라인 채널에서 모든 인터랙션을 추적하고 하나의 프로필에 병합할 수 있습니다.

**대상은** 특정 기준이나 기준 세트를 기반으로 만들어진 프로필 목록입니다. 워크플로우 및 쿼리 편집기를 사용하여 보유한 정보, 활동 및 마케팅 내역에 따라 마케팅 캠페인이 타깃팅할 대상을 구성할 수 있습니다. 이렇게 하면 가입된 프로필을 필터링하거나, 샘플링하거나, 무제한 기준에 따라 타겟 대상을 만들 수 있습니다.

자세한 내용:

* [프로필 기본 정보](../../audiences/using/about-profiles.md)
* [활성 프로필](../../audiences/using/active-profiles.md)
* [테스트 프로필 관리](../../audiences/using/managing-test-profiles.md)
* [Campaign 데이터베이스 강화](../../audiences/using/enriching-campaign-database.md)
* [대상자 기본 정보](../../audiences/using/about-audiences.md)
* [메시지에서 대상자 선택](../../audiences/using/selecting-an-audience-in-a-message.md)
* [컨트롤 그룹 추가](../../sending/using/control-group.md)

## 허가 및 동의 {#permission}

<img src="assets/do-not-localize/icon_permission.svg"  width="60px">

대화 상대에게 메시지를 보내기 전에 대화 상대에게 권한이 있는지 확인해야 합니다. 그렇지 않은 경우 이메일이 스팸으로 표시되어 플랫폼 배포 기능에 영향을 줄 수 있습니다. 올바른 프로필 데이터베이스를 만들려면 이 권한을 첫 번째 단계로 확보하십시오.

Adobe Campaign에서는 **서비스** 및 [랜딩 페이지를](../../audiences/using/creating-a-service.md)통해 [손쉽게 옵트인 및 옵트아웃 메커니즘을 사용하여 연락처 정보를 업데이트하고 데이터베이스를 확대하는](../../channels/using/getting-started-with-landing-pages.md) 것이 좋습니다.

메시지에 **구독 취소 링크를** 제공하면 필요할 때 프로파일을에 차단 목록 추가할 수 있으므로 플랫폼 전달을 향상시킬 수 있습니다. For more on denylist management, refer to [About opt-in and opt-out in Campaign](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md).

>[!IMPORTANT]
>
>귀하는 [Adobe Campaign 허용 가능한 사용 정책을 존중해야 합니다](https://www.adobe.com/legal/terms/aup.html).

자세한 내용:

* [구독 기본 정보](../../audiences/using/about-subscriptions.md)
* [Campaign의 옵트인 및 옵트아웃 기본 정보](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md)

## 개인 정보 보호 규정 준수 {#privacy}

<img src="assets/do-not-localize/icon_privacy.svg" width="60px">

Adobe Campaign offers a set of tools to help you with your **Privacy Compliance** for GDPR, CCPA, and other privacy laws.

본 문서에서 [](https://helpx.adobe.com/kr/campaign/kb/campaign-privacy.html) 개인정보 보호 관리 및 액세스 권한, 잊혀질 권리, 동의, 데이터 유지 및 사용자 역할을 관리하기 위해 제공하는 기능에 대해 자세히 알아보십시오.

Campaign의 개인 정보 및 동의 및 관리 방법은 [이 섹션에 나와 있습니다](../../start/using/privacy.md). 또한 Adobe 서비스를 사용할 때 귀하의 개인정보 보호 규정 준수를 돕기 위해 최선의 방법을 찾을 수 있습니다.

## 추가 리소스

* [대상 서비스 사용](../../audiences/using/aep-about-audience-destinations-service.md)
* [Microsoft Dynamics 365를 사용한 작업](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md)
* [Adobe 공유 대상](../../integrating/using/sharing-audiences-with-audience-manager-or-people-core-service.md)
* [워크플로우를 사용하여 프로필 가져오기](../../automating/using/creating-import-workflow-templates.md)
* [프로필 및 대상 비디오](https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/profiles-and-audiences/creating-profiles-and-audiences.html)
