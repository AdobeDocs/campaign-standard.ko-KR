---
title: Campaign-Audience Manager 또는 핵심 서비스 통합 정보
seo-title: Campaign-Audience Manager 또는 핵심 서비스 통합 정보
description: Campaign-Audience Manager 또는 핵심 서비스 통합 정보
seo-description: Audience Manager/People 핵심 서비스 통합을 통해 다른 Adobe Experience Cloud 솔루션 내에서 대상 또는 세그먼트를 공유할 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 39 E 3 C 78 E-CCCD -4823-AFE 9-ABC 7 F 8 AEF 034
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 통합
content-type: 참조
topic-tags: working-with-campaign-and-audience-manager-or-people-core-service
discoiquuid: BF 718329-F 181-46 F 7-80 A 2-B 525 A 8 Dee 46 D
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# About Campaign-Audience Manager or People core service integration{#about-campaign-audience-manager-or-people-core-service-integration}

Adobe Campaign를 사용하면 다른 Adobe Experience Cloud 애플리케이션과 고객/세그먼트를 교환하고 공유할 수 있습니다. Integrating **Adobe Campaign** with **People core service** (also known as **Profiles &amp; Audiences core service**) or Adobe Audience Manager allows you to:

* 다른 Adobe Experience Cloud 솔루션의 고객/세그먼트를 Adobe Campaign로 가져올 수 있습니다. Audiences can be imported from the **[!UICONTROL Audiences]** menu in Adobe Campaign.
* 대상을 공유 대상/세그먼트로 내보냅니다. 이러한 대상은 사용자가 사용하는 다양한 Adobe Experience Cloud 솔루션에서 사용할 수 있습니다. Audiences can be exported after targeting activities in a workflow, using the **[!UICONTROL Save audience]** activity.

통합은 다음 두 가지 유형의 Adobe Experience Cloud ID를 지원합니다.

* **방문자 ID**: 이 유형의 ID를 사용하면 Adobe Experience Cloud 방문자를 Adobe Campaign 프로필로 조정할 수 있습니다.
* **선언된 ID**: 이 유형의 ID를 사용하면 Adobe Campaign 데이터베이스의 프로필로 모든 유형의 데이터를 조정할 수 있습니다. 이 통합은 일반 선언된 ID, 해시된 선언된 ID 및 암호화된 선언된 ID를 지원합니다.

   암호화를 사용하면 암호화 알고리즘을 지정하여 선언된 ID를 사용하여 데이터 소스 (예: PII) 에서 암호화된 데이터를 공유할 수 있습니다.

   예를 들어 암호화된 이메일 주소 또는 SMS 번호를 해독할 수 있는 기능을 사용하면 Adobe Campaign 데이터베이스에 프로필이 없더라도 사용자에게 트리거 메시지를 보낼 수 있습니다.

>[!CAUTION]
>
>교환된 데이터에 따라 Adobe Campaign에서 대상을 가져오는 것은 법적 제한의 대상이 될 수 있습니다.

