---
title: Adobe Experience Platform 데이터 커넥터 기본 정보
description: XDM 스키마를 관리하여 Adobe Experience Platform에서 Campaign Standard 데이터를 사용할 수 있도록 합니다.
audience: administration
content-type: reference
topic-tags: configuring-channels
feature: Microsoft CRM Integration
role: Data Architect
level: Experienced
exl-id: f4fcf256-e030-4d7b-b4b7-2448acc2ae1c
hide: true
hidefromtoc: true
source-git-commit: 26394f3f6fd9b67996c30924c376533380e8f4d6
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 4%

---

# Adobe Experience Platform 데이터 커넥터 기본 정보 {#about-aep-data-connector}

>[!IMPORTANT]
>
>Adobe Experience Platform Data Connector는 현재 베타 버전이며 예고 없이 자주 업데이트될 수 있습니다. 이러한 기능에 액세스하려면 고객을 Azure(현재 북미 지역의 경우에만 베타 버전)에서 호스팅해야 합니다. 액세스하려면 Adobe 고객 지원 센터에 문의하십시오.

Adobe Experience Platform Data Connector는 XTK 데이터(Campaign에서 수집된 데이터)를 Adobe Experience Platform의 XDM(Experience Data Model) 데이터에 매핑하여 기존 고객이 Adobe Experience Platform에서 데이터를 사용할 수 있도록 지원합니다.

커넥터는 입니다. **단방향** Adobe Campaign Standard에서 Adobe Experience Platform으로 데이터를 전송합니다. 데이터는 Adobe Experience Platform에서 Adobe Campaign Standard으로 전송되지 않습니다.

Adobe Experience Platform Data Connector의 용도 **데이터 엔지니어** Adobe Campaign Standard 사용자 지정 리소스를 이해하고 고객의 전체 데이터 스키마가 Adobe Experience Platform 내부에 어떻게 있어야 하는지 이해합니다.

다음 섹션에서는 Campaign Standard과 Adobe Experience Platform 간에 데이터 매핑을 수행하는 주요 단계를 설명합니다. XDM 스키마 및 데이터 세트를 만드는 것부터 시작합니다.

![](assets/do-not-localize/how-to-video.png) [비디오에서 이 기능 살펴보기](#video)

>[!NOTE]
>Adobe Experience Platform 데이터 커넥터가 구성되고 데이터가 Adobe Experience Platform에 성공적으로 수집되면 데이터가 실시간 고객 프로필에 포함되도록 데이터 세트를 활성화해야 합니다.
>
>API 또는 Adobe Experience Platform 인터페이스를 통해 수행할 수 있습니다. 자세한 내용은 다음 전용 설명서를 참조하십시오.
>
>* [실시간 고객 프로필에 대한 데이터 세트 활성화](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/datasets/dataset.html)
>* [API를 사용하여 실시간 고객 프로필 및 ID 서비스에 대한 데이터 세트 구성](https://experienceleague.adobe.com/docs/experience-platform/catalog/api/getting-started.html)

## 주요 개념 {#key-concepts}

* 기본 Campaign Standard에서 기본적으로 제공되는 필드에만 기본 매핑을 사용할 수 있습니다. 모든 사용자 정의 필드 및 리소스를 수집하려면 각 고객이 고유한 매핑을 정의해야 합니다.

* Adobe Experience Platform 데이터 커넥터는 정기적으로 플랫폼을 통해 프로필 데이터를 푸시합니다&#x200B;. 간격은 15분입니다. 이 값은 다음을 사용하여 수정할 수 있습니다. [ADOBE EXPERIENCE PLATFORM API](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html).

* 데이터 엔지니어는 Campaign에서 Adobe Experience Platform으로의 매핑을 게시, 수정 및 일시 중지할 수 있습니다.

* 모든 타겟팅 차원을 매핑할 수 있습니다. 권장 사항은 단일 타겟팅 차원의 모든 필드에 대해 하나의 단일 매핑을 갖는 것입니다.

* 채널 옵트인/옵트아웃을 포함한 모든 프로필 업데이트는 배치 업데이트의 일부입니다.

* 모든 Adobe Campaign Standard 또는 XDM 스키마 변경 사항을 수동으로 다시 매핑해야 합니다&#x200B;.

* 추적 로그 및 Broadlog 데이터는 Adobe Experience Platform에 경험 이벤트로 자동으로 수집됩니다. 이 수집은 실시간으로 Adobe Experience Platform으로 스트리밍됩니다.

* Experience Cloud ID 서비스(ECID)는 기본적으로 Experience Events와 함께 전송되는 장치 식별자입니다.

  방문자에게 할당된 고유한 영구 ID이며, Platform ID 서비스에서 다른 Experience Cloud 솔루션에서 동일한 방문자와 해당 데이터를 식별하는 데 사용할 수 있습니다. 자세한 내용은 [Experience Cloud ID 서비스 도움말](https://experienceleague.adobe.com/docs/id-service/using/home.html).

  >[!NOTE]
  >
  >두 개 이상의 프로필이 동일한 장치를 공유하는 경우 통합 ID 서비스에서 이러한 두 프로필에 대해 ECID가 동일합니다.

## 제한 사항 {#limitations}

* 구독 이벤트의 기본 전송은 지원되지 않습니다. 구독 이벤트를 전송하기 위해 Adobe Experience Platform에서 해당 XDM 및 데이터 세트를 만든 다음 이러한 데이터에 대한 사용자 지정 데이터 매핑을 구성할 수 있습니다.

* 개인 정보 보호 요청(액세스 및 삭제 작업 모두)과 관련하여 고객은 [개인 정보 보호 핵심 서비스](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html#how-to-use-privacy-service-to-manage-privacy-job-requests): Campaign용 1개 및 Adobe Experience Platform용 1개 자세한 내용은 [개인 정보 보호 요청 정보](https://experienceleague.adobe.com/docs/campaign-standard/using/getting-started/privacy/privacy-requests.html?lang=ko#getting-started) 및 [개인 정보 보호 요청 관리](https://helpx.adobe.com/kr/campaign/kb/acs-privacy.html#ManagingPrivacyRequests) Campaign에서

* 각 XDM 필드에 대해 Adobe Experience Platform에서 DULE 레이블을 지정해야 합니다. DULE 레이블을 적용하는 것은 고객의 책임입니다.

* 마케팅 액션에 대한 제한 사항은 Adobe Experience Platform에서 DULE 레이블을 적용한 후에만 적용할 수 있습니다. 그 전에는 모든 유형의 마케팅 작업에 모든 데이터를 사용할 수 있습니다.

* 15분마다 일괄 처리 작업이 실행되고 최신 일괄 처리 이후 변경된 레코드를 식별합니다. 모든 레코드가 동일한 타임스탬프에서 변경되는 경우 성능 병목 현상이 나타나 모든 프로필의 수집을 관리할 수 있습니다

## 튜토리얼 비디오 {#video}

이 비디오는 Adobe Experience Platform 데이터 커넥터에 대한 개요를 제공합니다.

>[!VIDEO](https://video.tv.adobe.com/v/27304?quality=12&captions=eng)

Adobe Experience Platform 데이터 커넥터 관련 추가 비디오를 사용할 수 있습니다 [여기](https://experienceleague.adobe.com/docs/campaign-learn/campaign-standard-tutorials/administrating/adobe-experience-platform-data-connector/understanding-the-adobe-experience-platform-data-connector.html).
