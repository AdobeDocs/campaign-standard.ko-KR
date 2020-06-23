---
title: Audience Destinations 서비스 정보
description: 대상 대상 서비스에 대해 자세히 알아보십시오.
page-status-flag: never-activated
uuid: b3996642-96ec-489e-b146-c8c2cb52aa32
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: managing-audiences
discoiquuid: 750ecd8d-67a5-4180-bfec-2a8e3098c812
context-tags: audience,wizard;audience,overview;delivery,audience,back
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: be7ab90583e9c6472fd2c86082e832432d0a32b9
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 4%

---


# Audience Destinations 서비스 정보 {#about-audiences}

>[!IMPORTANT]
>
>대상 대상 서비스는 현재 베타 버전이며 예고 없이 자주 업데이트될 수 있습니다. 이러한 기능에 액세스하려면 고객이 Azure(현재 북미 전용 베타 버전)에서 호스팅되어야 합니다. 액세스 권한을 원하는 경우 Adobe 고객 지원 센터에 문의하십시오.

복잡한 대용량 데이터 세트를 기반으로 [Adobe Experience Platform](https://docs.adobe.com/content/help/en/experience-platform/landing/home.html) 를 활용하여 고도로 타겟팅된 고객을 구축함으로써 고객 경험을 더욱 강화할 수 있습니다. Adobe Experience Platform은 Adobe Analytics을 비롯한 온라인 및 오프라인 소스에서 프로파일, 행동 및 다중 엔티티 데이터를 통합하여 고객의 전체 상황을 파악하고 고객 경험을 효과적으로 관리할 수 있도록 합니다.

그런 다음 Adobe Campaign Standard은 **대상** 서비스 **를 사용하여 여러 단계 및/또는 크로스 채널 캠페인 프로그램에 대해 Adobe Experience Platform에서**&#x200B;대상이라고하는 프로필 모음을 가져옵니다.

**대상은** 처음 세그먼트를 **작성하여**&#x200B;생성되며, 이는 본질적으로 Adobe Experience Platform의 고객 프로필 내에서 거의 모든 변수(예: 프로필, 이벤트, 다중 엔티티 데이터)를 기반으로 한 규칙 세트로, 다차원 타겟을 만듭니다. 실시간 고객 프로필 및 세그멘테이션 서비스에 대한 글로벌 개념은 다음 전용 문서에서 참조됩니다.

* [실시간 고객 프로필 개요](https://docs.adobe.com/content/help/ko-KR/experience-platform/profile/home.html)
* [세그멘테이션 서비스 개요](https://docs.adobe.com/content/help/en/experience-platform/segmentation/home.html)

세그먼트를 만든 후 [Campaign Standard 워크플로우에서 전달을 위한 대상으로 활성화할 수 있습니다](../../automating/using/aep-targeting-audiences.md). 또한 Adobe Experience Platform의 컨텍스트 데이터를 사용하여 동적 컨텐츠를 개인화하고 캠페인에 [추가할](../../automating/using/aep-personalizing-campaigns.md) 수 있습니다.

방법 비디오는 [이 단원에서도 사용할 수 있습니다](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/profiles-and-audiences/audience-destinations/audience-destinations-overview.html).

다음 섹션에 사용되는 용어:

* **프로필**: 프로파일은 소비자의 속성을 정의하는 데 사용되는 Experience Platform 표준 데이터 모델입니다. 또한 프로필은 개인 또는 장치와 관련된 이벤트 데이터와 속성의 집합일 수 있습니다.

   예: &quot;John Doe는 55세의 남성입니다.&quot;

* **세그먼트**: 속성과 이벤트 데이터를 모두 사용하여 데이터베이스의 프로필 하위 집합을 정의하는 규칙 집합입니다.

   예: &quot;남성 > 50세.&quot;

* **대상**: 세그먼트 규칙을 충족하는 프로필 컬렉션입니다.

   예: 데이터베이스에서 50세 이상의 모든 남성에게 해당하는 프로필 목록입니다.
