---
title: 프로필 및 대상자 시작
description: 타기팅된 모집단을 정의하고 대상자를 선택하며 수신자를 필터링하고 데이터를 수집하며 프로필을 업데이트합니다.
audience: audiences
content-type: reference
topic-tags: about-profiles-and-audiences
feature: Profiles
role: User
level: Beginner
exl-id: b4de2f1a-09ec-486d-b1ef-66208cbe211f
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '591'
ht-degree: 10%

---

# 프로필 및 대상자 시작{#about-profiles-and-audiences}

<table>
<tr>
<td><img src="assets/do-not-localize/icon_segment.svg" width="60px"><p><a href="#segmenting-targeting">세그먼트화 및 타겟팅</a></p></td>
<td><img src="assets/do-not-localize/icon_permission.svg" width="60px"><p><a href="#permission">권한 및 동의</a></p></td>
<td><img src="assets/do-not-localize/icon_privacy.svg" width="60px"><p><a href="#privacy">개인정보 규정 준수</a></p></td></tr>
</table>

캠페인 통합 고객 프로필을 사용하면 하나의 보기에서 모든 채널에 있는 고객과의 모든 상호 작용을 추적할 수 있으므로 고객에게 연관성 있고 개인화된 메시지를 전달할 수 있습니다.

데이터베이스를 대상으로 세분화하여 마케팅 캠페인의 타겟을 최적화합니다.

서비스 및 랜딩 페이지를 사용하여 고객의 권한 및 동의를 관리하여 손쉽게 옵트인 및 옵트아웃 메커니즘을 설정할 수 있습니다.

## 세그먼트화 및 타겟팅 {#segmenting-targeting}

<img src="assets/do-not-localize/icon_segment.svg" width="60px">

캠페인이나 메시지를 만들 때 Campaign 데이터베이스의 연락처 중에서 선택하거나 단순 또는 고급 기준을 사용하거나 대상을 선택하여 게재 대상을 지정할 수 있습니다.

**통합 고객 프로필**, **사용자 지정된 세그먼트** 및 **제어 그룹**&#x200B;을 사용하여 모든 채널에서 고객을 보다 효과적으로 식별합니다. 고객, 관심 분야, 인구 통계 및 채널 환경 설정을 알고 있으면 눈에 띄는 개인화된 경험을 더 쉽게 만들 수 있습니다.

Adobe Campaign은 실시간으로 풍부한 고객 프로필을 빌드하여 고객의 환경 설정이 변경될 때 보다 관련성이 높고 개인화된 오퍼를 제공할 수 있습니다. 또한 Adobe Campaign은 고급 분석, 데이터 관리 및 타기팅 기능을 통합하여 대상자를 구성합니다.

**프로필**&#x200B;은(는) 데이터베이스에 저장된 개별 연락처입니다. 각 프로필은 데이터베이스의 한 항목에 해당하며, 이 항목에는 해당 프로필이 타겟팅되고 자격이 부여되고 개별적으로 추적되는 데 필요한 정보가 포함되어 있습니다. Adobe Campaign은 온라인 및 오프라인 채널 모두에서 모든 상호 작용을 추적하고 이를 단일 프로필에 병합할 수 있습니다.

**대상**&#x200B;은(는) 특정 기준이나 기준 집합을 기반으로 만들어진 프로필 목록입니다. 워크플로우 및 쿼리 편집기를 사용하여 보유하고 있는 정보, 활동 및 마케팅 내역에 따라 마케팅 캠페인이 타겟팅할 대상을 구성할 수 있습니다. 이렇게 하면 구독한 프로필, 샘플을 필터링하거나 기준을 제한 없이 타겟 대상을 만들 수 있습니다.

자세한 내용:

* [프로필 기본 정보](../../audiences/using/about-profiles.md)
* [활성 프로필](../../audiences/using/active-profiles.md)
* [테스트 프로필 관리](../../audiences/using/managing-test-profiles.md)
* [Campaign 데이터베이스 강화](../../audiences/using/enriching-campaign-database.md)
* [대상자 기본 정보](../../audiences/using/about-audiences.md)
* [메시지에서 대상자 선택](../../audiences/using/selecting-an-audience-in-a-message.md)
* [컨트롤 그룹 추가](../../sending/using/control-group.md)

## 권한 및 동의 {#permission}

<img src="assets/do-not-localize/icon_permission.svg"  width="60px">

연락처에 메시지를 보내기 전에 연락처의 권한을 받았는지 확인해야 합니다. 그렇지 않으면 이메일이 스팸으로 표시될 수 있으며 이는 플랫폼 전달성에 영향을 미칩니다. 정상적인 프로필 데이터베이스를 빌드하려면 첫 번째 단계로 이 권한을 보호하십시오.

Campaign을 사용할 때는 **쉬운 옵트인 및 옵트아웃 메커니즘**&#x200B;부터 [서비스](../../audiences/using/creating-a-service.md)까지 및 [랜딩 페이지](../../channels/using/getting-started-with-landing-pages.md)를 사용하여 연락처 정보를 업데이트하고 데이터베이스를 확장하는 것이 좋습니다.

차단 목록에 추가하다 메시지에 **구독 취소 링크**&#x200B;를 제공하면 필요할 때 프로필에 추가하여 플랫폼 전달성을 향상시킬 수 있습니다. [차단 목록 및 관리에 대한 자세한 내용은 Campaign의 옵트아웃 정보](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md)를 참조하세요.

>[!IMPORTANT]
>
>[Adobe Campaign 허용 사용 정책](https://www.adobe.com/legal/terms/aup.html)을 준수해야 합니다.

자세한 내용:

* [구독 기본 정보](../../audiences/using/about-subscriptions.md)
* [Campaign의 옵트인 및 옵트아웃 기본 정보](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md)

## 개인정보 규정 준수 {#privacy}

<img src="assets/do-not-localize/icon_privacy.svg" width="60px">

Adobe Campaign은 GDPR, CCPA 및 기타 개인 정보 보호법에 대한 **개인 정보 보호 규정 준수**&#x200B;을 지원하는 도구를 제공합니다.

개인 정보 관리 및 액세스 권한, 잊혀질 권리, 동의, 데이터 보존 및 사용자 역할을 관리하는 데 제공하는 기능에 대해 이 [이 문서](https://helpx.adobe.com/kr/campaign/kb/campaign-privacy.html)에서 자세히 알아보세요.

Campaign의 개인 정보 및 동의와 이를 관리하는 방법은 [이 섹션](../../start/using/privacy.md)에 나와 있습니다. 또한 서비스를 사용할 때 개인 정보 보호 규정을 준수하는 데 도움이 되는 모범 사례를 확인할 수 있습니다.

## 추가 리소스

* [Adobe Experience Platform 대상자를 Campaign으로 수집](../../integrating/using/ingest-aep-data.md)
* [Microsoft Dynamics 365 작업](../../integrating/using/d365-acs-get-started.md)
* [공유 대상자 Adobe](../../integrating/using/sharing-audiences-with-audience-manager-or-people-core-service.md)
* [워크플로우를 사용하여 프로필 가져오기](../../automating/using/creating-import-workflow-templates.md)
* [프로필 및 대상자 비디오](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/profiles-and-audiences/creating-profiles-and-audiences.html?lang=ko)
