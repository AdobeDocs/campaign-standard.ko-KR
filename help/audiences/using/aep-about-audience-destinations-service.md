---
title: 대상 대상 서비스 정보
description: 대상 대상 서비스에 대한 자세한 내용을 살펴보십시오.
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
source-git-commit: ff3b41589f47e7697a69bb68824aefd4d9036793

---


# 대상 대상 서비스 정보 {#about-audiences}

>[!IMPORTANT]
>
>대상 서비스는 현재 베타 버전으로, 예고 없이 빈번한 업데이트가 적용될 수 있습니다. 이러한 기능에 액세스하려면 고객이 Azure(현재 북미 전용 베타 버전)에서 호스팅되어야 합니다. 액세스하려면 Adobe 고객 지원 센터에 문의하십시오.

AEP(Adobe Experience Platform) [를](https://www.adobe.io/apis/experienceplatform/home.html) 활용하여 복잡한 대용량 데이터 세트를 기반으로 고도로 타겟팅된 고객을 구축하여 고객 경험을 강화합니다. Adobe Experience Platform은 Adobe Analytics를 비롯한 온라인 및 오프라인 소스에서 프로파일, 행동 및 다중 엔티티 데이터를 통합하여 고객의 전체 상황을 파악하고 고객 경험을 효과적으로 관리할 수 있도록 지원합니다.

그런 다음 Adobe Campaign Standard는 **대상** 대상 서비스를 사용하여 AEP에서 **여러 단계 및/또는 크로스 채널 캠페인 프로그램을 위해**&#x200B;대상이라고 하는 프로필 컬렉션을 검색합니다.

**대상은** AEP의 고객 프로필 내에서 기본적으로 거의 모든 변수(예: 프로필, 이벤트, 다중 개체 데이터)를 기반으로 한 규칙 집합인 **세그먼트를**&#x200B;처음으로 작성하여 다차원 타겟을 만듭니다. 통합 프로필 및 세그멘테이션 서비스에 대한 글로벌 개념은 [이러한 전용 문서에서](https://www.adobe.io/apis/experienceplatform/home/profile-identity-segmentation.html)참조할 수 있습니다.

세그먼트가 만들어지면 Campaign Standard 워크플로우에서 [전달을 위한 대상으로 활성화할 수](../../automating/using/aep-targeting-audiences.md)있습니다. 또한 Adobe Experience Platform의 컨텍스트 데이터를 사용하여 원하는 경우 동적 컨텐츠를 [개인화하고](../../automating/using/aep-personalizing-campaigns.md) 캠페인에 추가할 수 있습니다.

데모 비디오도 [이 섹션에서](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/profiles-and-audiences/audience-destinations/audience-destinations-overview.html)사용할 수 있습니다.

다음 섹션에서 사용되는 용어:

* **프로필**:프로파일은 소비자의 속성을 정의하는 데 사용되는 경험 플랫폼 표준 데이터 모델입니다. 또한 프로필은 개인 및 장치와 관련된 이벤트 데이터 및 속성의 집합일 수 있습니다.

   예:&quot;John Doe는 55세의 남성입니다.&quot;

* **세그먼트**:속성과 이벤트 데이터를 모두 사용하여 데이터베이스의 프로파일 하위 집합을 정의하는 규칙 집합.

   예:&quot;남성 > 50세.&quot;

* **대상**:세그먼트 규칙을 만족하는 프로파일 컬렉션입니다.

   예:데이터베이스에서 50세 이상의 모든 남성에게 해당하는 프로파일 목록입니다.
