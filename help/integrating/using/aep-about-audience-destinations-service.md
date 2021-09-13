---
title: Audience Destinations 서비스 기본 정보
description: Audience 대상 서비스에 대해 자세히 알아보십시오.
audience: audiences
content-type: reference
topic-tags: managing-audiences
context-tags: audience,wizard;audience,overview;delivery,audience,back
feature: Microsoft CRM Integration
role: Data Architect
level: Experienced
exl-id: 34235749-d056-4d4c-9939-7dc52f980a76
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 2%

---

# Audience Destinations 서비스 기본 정보 {#about-audiences}

>[!IMPORTANT]
>
>Audience Destinations 서비스는 현재 베타에 있으며, 예고 없이 자주 업데이트될 수 있습니다. 고객은 이러한 기능에 액세스하려면 Azure에서 호스팅(현재 북미 전용 베타 버전)해야 합니다. 액세스하려면 고객 지원 센터에 문의하십시오.

[Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html)을 활용하여 복잡하고 크기가 큰 데이터 세트를 기반으로 고도로 타깃팅된 대상을 구축함으로써 소비자 경험을 강화할 수 있습니다. Adobe Experience Platform은 Adobe Analytics을 비롯한 온라인 및 오프라인 소스에서 프로필, 행동 및 다중 엔티티 데이터를 통합하여 고객에 대한 360도 보기를 구축할 수 있도록 함으로써 고객 경험을 효과적으로 관리할 수 있습니다.

그런 다음 Adobe Campaign Standard은 **대상 대상** 서비스를 사용하여 Adobe Experience Platform에서 여러 단계 및/또는 크로스 채널 캠페인 프로그램을 위해 **대상**&#x200B;으로 알려진 프로필 컬렉션을 검색합니다.

**** 대상자는 처음 세그먼트 **를 작성하여** 만듭니다. 이 템플릿은 Adobe Experience Platform에서 고객 프로필 내의 거의 모든 변수(예: 프로필, 이벤트, 다중 엔티티 데이터)를 기반으로 한 규칙 세트로서 다차원 타겟을 만듭니다. 실시간 고객 프로필 및 세그멘테이션 서비스에 대한 글로벌 개념은 다음 전용 문서에서 참조됩니다.

* [실시간 고객 프로필 개요](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html)
* [세그먼테이션 서비스 개요](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html)

세그먼트가 만들어지면 [Campaign Standard 워크플로우](../../integrating/using/aep-targeting-audiences.md)에서 게재를 위한 대상으로 활성화할 수 있습니다. 또한 Adobe Experience Platform에서 [개인화](../../integrating/using/aep-personalizing-campaigns.md)에 컨텍스트 데이터를 사용하고 캠페인에 동적 콘텐츠를 추가할 수 있습니다.

![](assets/do-not-localize/how-to-video.png) 방법 비디오도  [이 섹션](https://experienceleague.adobe.com/docs/campaign-learn/campaign-standard-tutorials/profiles-and-audiences/audience-destinations/audience-destinations-overview.html)에서 사용할 수 있습니다.

다음 섹션에 사용되는 용어:

* **프로필**: 프로필은 소비자의 속성을 정의하는 데 사용되는 Experience Platform 표준 데이터 모델입니다. 프로필은 개인 및 장치와 관련된 이벤트 데이터 및 속성의 집합일 수도 있습니다.

   예: &quot;존 도는 55세의 남자입니다.&quot;

* **세그먼트**: 속성과 이벤트 데이터를 모두 사용하여 데이터베이스의 프로필 하위 집합을 정의하는 규칙 집합입니다.

   예: &quot;50세 이상의 남자&quot;

* **대상**: 세그먼트 규칙을 충족하는 프로필 컬렉션입니다.

   예: 데이터베이스의 모든 남성 50세 이상에 해당하는 프로필 목록입니다.
