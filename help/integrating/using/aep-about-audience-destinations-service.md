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
source-git-commit: 26394f3f6fd9b67996c30924c376533380e8f4d6
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 2%

---

# Audience Destinations 서비스 기본 정보 {#about-audiences}

>[!IMPORTANT]
>
>Audience Destinations 서비스는 현재 베타 버전이며, 예고 없이 자주 업데이트될 수 있습니다. 이러한 기능에 액세스하려면 고객을 Azure(현재 북미 지역의 경우에만 베타 버전)에서 호스팅해야 합니다. 액세스하려면 Adobe 고객 지원 센터에 문의하십시오.

을 활용하여 소비자 경험을 강화할 수 있습니다. [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html) 대규모의 복잡한 데이터 세트를 기반으로 고도로 타깃팅된 대상을 구축할 수 있습니다. Adobe Experience Platform은 Adobe Analytics을 포함하여 온라인과 오프라인 소스 간에 프로필, 행동 및 다중 엔티티 데이터를 통합하여 고객에 대한 360도 뷰를 작성하는 데 도움이 되므로 고객 경험을 효과적으로 관리할 수 있습니다.

그런 다음 Adobe Campaign Standard은 **Audience 대상** 프로필 컬렉션을 검색하는 서비스, 예: **대상**, Adobe Experience Platform에서 다단계 및/또는 크로스채널 캠페인 프로그램에 사용됩니다.

**대상** 첫 번째 빌드에서 생성됨 **세그먼트**&#x200B;는 본질적으로 다차원 타겟을 만들기 위해 Adobe Experience Platform의 고객 프로필 내에 있는 거의 모든 변수(예: 프로필, 이벤트, 다중 엔티티 데이터)를 기반으로 하는 규칙 세트입니다. 실시간 고객 프로필 및 세분화 서비스에 대한 글로벌 개념은 다음 전용 문서에서 참조됩니다.

* [실시간 고객 프로필 개요](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html)
* [세그먼테이션 서비스 개요](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html)

세그먼트가 만들어지면에서 게재 대상자로 활성화할 수 있습니다 [Campaign Standard 워크플로](../../integrating/using/aep-targeting-audiences.md). 또한 Adobe Experience Platform의 컨텍스트 데이터를 사용하여 [개인화](../../integrating/using/aep-personalizing-campaigns.md) 캠페인에 다이내믹한 콘텐츠를 추가합니다.

![](assets/do-not-localize/how-to-video.png) 방법 비디오는에서 사용할 수 있습니다. [이 섹션](https://experienceleague.adobe.com/docs/campaign-learn/campaign-standard-tutorials/profiles-and-audiences/audience-destinations/audience-destinations-overview.html).

다음 섹션에 사용되는 용어:

* **프로필**: 프로필은 소비자의 속성을 정의하는 데 사용되는 Experience Platform 표준 데이터 모델입니다. 프로필은 사용자 및/또는 디바이스와 관련된 이벤트 데이터 및 속성의 집계일 수도 있습니다.

  예: &quot;John Doe는 55세 남성입니다.&quot;

* **세그먼트**: 속성 및 이벤트 데이터를 모두 사용하여 데이터베이스에서 프로필의 하위 집합을 정의하는 규칙 세트입니다.

  예: &quot;남성 > 50세&quot;

* **대상자**: 세그먼트 규칙을 충족하는 프로필 컬렉션입니다.

  예: 데이터베이스의 모든 남성 > 50세에 해당하는 프로필 목록.
