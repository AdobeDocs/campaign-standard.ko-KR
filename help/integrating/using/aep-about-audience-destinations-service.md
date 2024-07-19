---
title: Audience Destinations 서비스 기본 정보
description: Audience Destinations 서비스에 대해 자세히 알아보십시오.
audience: audiences
content-type: reference
topic-tags: managing-audiences
context-tags: audience,wizard;audience,overview;delivery,audience,back
feature: Microsoft CRM Integration
role: Data Architect
level: Experienced
exl-id: 34235749-d056-4d4c-9939-7dc52f980a76
hide: true
hidefromtoc: true
source-git-commit: 376f00576ca1d0dfb536b29dbf25d88f7c93b9a8
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 2%

---

# Audience Destinations 서비스 기본 정보 {#about-audiences}

>[!IMPORTANT]
>
>Audience Destinations 서비스는 이제 더 이상 사용되지 않습니다. 사용 중단되는 기능은 계속 사용할 수 있지만 더 이상 향상 또는 지원되지 않습니다. 자세히 알아보기 [이 페이지에서](../../rn/using/deprecated-features.md)

[Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html)을(를) 활용하여 크고 복잡한 데이터 세트를 기반으로 고도로 타깃팅된 대상을 빌드하여 소비자 경험을 강화할 수 있습니다. Adobe Experience Platform은 Adobe Analytics을 포함하여 온라인과 오프라인 소스 간에 프로필, 행동 및 다중 엔티티 데이터를 통합하여 고객에 대한 360도 뷰를 작성하는 데 도움이 되므로 고객 경험을 효과적으로 관리할 수 있습니다.

그런 다음 Adobe Campaign Standard은 **Audience Destinations** 서비스를 사용하여 여러 단계 및/또는 크로스채널 캠페인 프로그램을 위해 Adobe Experience Platform에서 **Audiences**(으)로 알려진 프로필 컬렉션을 검색합니다.

**대상**&#x200B;은(는) 다차원 대상을 만들기 위해 Adobe Experience Platform의 고객 프로필 내에 있는 사실상 모든 변수(예: 프로필, 이벤트, 다중 엔터티 데이터)를 기반으로 하는 규칙 집합인 **세그먼트**&#x200B;을(를) 처음 빌드하여 만듭니다. 실시간 고객 프로필 및 세분화 서비스에 대한 글로벌 개념은 다음 전용 문서에서 참조됩니다.

* [실시간 고객 프로필 개요](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html)
* [세그먼테이션 서비스 개요](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html)

세그먼트가 만들어지면 [Campaign Standard 워크플로](../../integrating/using/aep-targeting-audiences.md)에서 게재 대상으로 활성화할 수 있습니다. 또한 Adobe Experience Platform의 컨텍스트 데이터를 사용하여 [개인화](../../integrating/using/aep-personalizing-campaigns.md)하고 캠페인에 다이내믹 콘텐츠를 추가할 수 있습니다.

![](assets/do-not-localize/how-to-video.png) 방법 비디오는 [이 섹션](https://experienceleague.adobe.com/docs/campaign-learn/campaign-standard-tutorials/profiles-and-audiences/audience-destinations/audience-destinations-overview.html)에서도 사용할 수 있습니다.

다음 섹션에 사용되는 용어:

* **프로필**: 프로필은 소비자의 특성을 정의하는 데 사용되는 Experience Platform 표준 데이터 모델입니다. 프로필은 사용자 및/또는 디바이스와 관련된 이벤트 데이터 및 속성의 집계일 수도 있습니다.

  예: &quot;John Doe는 55세 남성입니다.&quot;

* **세그먼트**: 특성과 이벤트 데이터를 모두 사용하여 데이터베이스에서 프로필의 하위 집합을 정의하는 규칙 집합입니다.

  예: &quot;남성 > 50세&quot;

* **대상**: 세그먼트 규칙을 충족하는 프로필 컬렉션입니다.

  예: 데이터베이스의 모든 남성 > 50세에 해당하는 프로필 목록.
