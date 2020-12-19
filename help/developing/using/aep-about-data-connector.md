---
solution: Campaign Standard
product: campaign
title: Adobe Experience Platform 데이터 커넥터 정보
description: XDM 스키마를 관리하여 Adobe Experience Platform에서 Campaign Standard 데이터를 사용할 수 있도록 합니다.
audience: administration
content-type: reference
topic-tags: configuring-channels
translation-type: tm+mt
source-git-commit: 2a92600df01fd3c78a2b35c8034a2ce347e5c1d8
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 5%

---


# Adobe Experience Platform 데이터 커넥터 정보 {#about-aep-data-connector}

>[!IMPORTANT]
>
>Adobe Experience Platform Data Connector는 현재 베타 버전으로, 사전 예고 없이 빈번하게 업데이트될 수 있습니다. 이러한 기능에 액세스하려면 고객이 Azure(현재 북미 전용 베타 버전)에서 호스팅되어야 합니다. 액세스하려면 Adobe 고객 지원 센터에 문의하십시오.

Adobe Experience Platform Data Connector는 기존 고객이 Adobe Experience Platform의 XDM(Experience Data Model) 데이터에 XTK 데이터(Campaign에서 인제스트된 데이터)를 매핑하여 Adobe Experience Platform에서 데이터를 사용할 수 있도록 도와줍니다.

커넥터는 **단방향**&#x200B;이며 Adobe Campaign Standard에서 Adobe Experience Platform으로 데이터를 보냅니다. 데이터는 Adobe Experience Platform에서 Adobe Campaign Standard으로 절대로 전송되지 않습니다.

Adobe Experience Platform 데이터 커넥터는 Adobe Campaign Standard 사용자 지정 리소스를 이해하고 고객의 전체 데이터 스키마가 Adobe Experience Platform 내에 있어야 하는 방법을 알고 있는 **데이터 엔지니어**&#x200B;를 위한 것입니다.

다음 섹션에서는 Campaign Standard과 Adobe Experience Platform 간의 데이터 매핑을 수행하는 주요 단계에 대해 설명합니다. XDM 스키마 및 데이터 세트 생성부터 시작합니다.

![](assets/do-not-localize/how-to-video.png) [비디오에서 이 기능 살펴보기](#video)

>[!NOTE]
>Adobe Experience Platform Data Connector를 구성하고 데이터를 Adobe Experience Platform으로 성공적으로 인제스트한 후에는 데이터를 실시간 고객 프로파일에 포함하려면 데이터 세트를 활성화해야 합니다.
>
>API 또는 Adobe Experience Platform 인터페이스를 통해 수행할 수 있습니다. 자세한 내용은 전용 문서를 참조하십시오.
>
>* [실시간 고객 프로파일에 대한 데이터 세트 활성화](https://docs.adobe.com/content/help/en/experience-platform/rtcdp/datasets/dataset.html)
>* [API를 사용하여 실시간 고객 프로필 및 ID 서비스에 대한 데이터 세트 구성](https://docs.adobe.com/content/help/en/experience-platform/catalog/api/getting-started.html)


## 주요 개념 {#key-concepts}

* 기본적으로 Campaign Standard에서 제공되는 필드에만 상자 외부의 매핑을 사용할 수 있습니다. 모든 사용자 정의 필드와 리소스를 수집하려면 각 고객이 자신의 고유한 매핑을 정의해야 합니다.

* Adobe Experience Platform 데이터 커넥터는 정기적으로 플랫폼을 통해 프로필 데이터를 &#x200B; 푸시합니다. 간격 기간은 15분입니다. 이 값은 [Adobe Experience Platform API](https://docs.adobe.com/content/help/en/experience-platform/ingestion/home.html)를 사용하여 수정할 수 있습니다.

* 데이터 엔지니어는 Campaign에서 Adobe Experience Platform으로 매핑을 게시, 수정 및 일시 중지할 수 있습니다.

* 모든 타깃팅 차원을 매핑할 수 있습니다. 단일 타깃팅 차원에 있는 모든 필드에 대해 하나의 매핑이 있는 것이 좋습니다.

* 채널 옵트인/옵트아웃을 비롯한 모든 프로필 업데이트는 일괄 업데이트의 일부입니다.

* Adobe Campaign Standard 또는 XDM 스키마 변경 사항을 수동으로 다시 매핑해야 &#x200B; 합니다.

* 추적 로그 및 Broadlog 데이터는 경험 이벤트로 Adobe Experience Platform에 자동으로 수집됩니다. 이 통합 내용은 Adobe Experience Platform으로 실시간으로 스트리밍됩니다.

* ECID(Experience Cloud ID 서비스)는 경험 이벤트로 기본적으로 전송되는 장치 식별자입니다.

   이 ID는 방문자에게 지정된 고유하고 지속적인 ID로서, 플랫폼 ID 서비스에서 동일한 방문자와 다른 Experience Cloud 솔루션에서 해당 데이터를 식별하는 데 사용할 수 있습니다. 자세한 내용은 [Experience Cloud ID 서비스 도움말](https://docs.adobe.com/content/help/en/id-service/using/home.html)을 참조하십시오.

   >[!NOTE]
   >
   >두 개 이상의 프로필이 동일한 장치를 공유하는 경우 통합 ID 서비스에서 이러한 두 프로필에 대해 ECID가 동일해야 합니다.

## 제한 사항 {#limitations}

* 구독 이벤트의 기본 전송은 지원되지 않습니다. 구독 이벤트를 전송하려면 Adobe Experience Platform에서 해당 XDM 및 데이터 세트를 만든 다음 이러한 데이터에 대한 사용자 지정 데이터 매핑을 구성할 수 있습니다.

* 개인 정보 요청(액세스 및 삭제 작업 모두)과 관련하여 고객은 [개인 정보 핵심 서비스](https://docs.adobe.com/content/help/en/experience-platform/privacy/home.html#how-to-use-privacy-service-to-manage-privacy-job-requests)를 통해 별도의 요청을 해야 합니다.캠페인 및 Adobe Experience Platform 캠페인 이에 대한 자세한 내용은 캠페인의 [개인 정보 요청 정보](https://experienceleague.adobe.com/docs/campaign-standard/using/getting-started/privacy/privacy-requests.html?lang=ko#getting-started) 및 [개인 정보 요청 관리](https://helpx.adobe.com/kr/campaign/kb/acs-privacy.html#ManagingPrivacyRequests)를 참조하십시오.

* 각 XDM 필드에 대해 DULE 레이블을 Adobe Experience Platform에서 지정해야 합니다. DULE 레이블을 적용하는 것은 고객의 책임입니다.

* 마케팅 작업에 대한 제한 사항은 Adobe Experience Platform에 DULE 레이블이 적용된 후에만 적용됩니다. 그 이전에는 모든 유형의 마케팅 작업에 모든 데이터를 사용할 수 있습니다.

* 15분마다 배치 작업이 실행 중이며 최근 배치 이후 변경된 레코드를 식별합니다. 모든 레코드가 동일한 타임스탬프에서 변경되면 성능 병목 현상이 모든 프로필의 수거를 관리하는 것처럼 나타날 수 있습니다

## 자습서 비디오 {#video}

이 비디오는 Adobe Experience Platform 데이터 커넥터에 대한 개요를 제공합니다.

https://video.tv.adobe.com/v/27304?quality=12&amp;captions=kor

Adobe Experience Platform 데이터 커넥터와 관련된 추가 비디오는 여기에서 [사용할 수 있습니다](https://docs.adobe.com/content/help/ko-KR/campaign-standard-learn/tutorials/administrating/adobe-experience-platform-data-connector/understanding-the-adobe-experience-platform-data-connector.html).
