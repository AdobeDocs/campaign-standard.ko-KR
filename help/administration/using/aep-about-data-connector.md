---
title: Adobe Experience Platform 데이터 커넥터 정보
description: XDM 스키마를 관리하여 Adobe Experience Platform에서 Campaign Standard 데이터를 사용할 수 있도록 합니다.
page-status-flag: never-activated
uuid: 867b1c4b-4c79-4c52-9d0a-ef71993e50a2
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: configuring-channels
discoiquuid: 406c955a-b2d2-4099-9918-95f5fa966067
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 9388df151eabbc6f63461e854d0276c14d9ef93d

---


# Adobe Experience Platform 데이터 커넥터 정보 {#about-aep-data-connector}

>[!IMPORTANT]
>
>Adobe Experience Platform Data Connector는 현재 베타 버전으로, 예고 없이 자주 업데이트될 수 있습니다. 이러한 기능에 액세스하려면 고객이 Azure(현재 북미 전용 베타 버전)에서 호스팅되어야 합니다. 액세스하려면 Adobe 고객 지원 센터에 문의하십시오.

Adobe Experience Platform Data Connector를 사용하면 기존 고객이 Adobe Experience Platform에서 XTK 데이터(Campaign에서 인제스트된 데이터)를 XDM(Experience Data Model) 데이터에 매핑하여 Adobe Experience Platform에서 데이터를 사용할 수 있습니다.

커넥터는 **단방향** 연결로 Adobe Campaign Standard의 데이터를 Adobe Experience Platform으로 전송합니다. 데이터는 Adobe Experience Platform에서 Adobe Campaign Standard로 전송되지 않습니다.

Adobe Experience Platform Data Connector는 Adobe Campaign Standard 사용자 지정 리소스를 **** 이해하고 고객의 전체 데이터 스키마가 Adobe Experience Platform 내에 어떻게 존재해야 하는지 알고 있는 데이터 엔지니어를 위해 마련되었습니다.

다음 섹션에서는 Campaign Standard와 Adobe Experience Platform 간의 데이터 매핑을 수행하는 주요 단계에 대해 설명합니다. XDM 스키마와 데이터 세트 생성부터 시작됩니다.

사용 방법 비디오는 [이 페이지에서도](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/adobe-experience-platform-data-connector/understanding-the-adobe-experience-platform-data-connector.html)사용할 수 있습니다.

>[!NOTE]
>Adobe Experience Platform Data Connector가 구성되고 데이터가 Adobe Experience Platform에 성공적으로 수집되면 데이터가 실시간 고객 프로필에 포함되도록 데이터 세트를 활성화해야 합니다.
>
>API 또는 Adobe Experience Platform 인터페이스를 통해 수행할 수 있습니다. 자세한 내용은 전용 설명서를 참조하십시오.
>
>* [실시간 고객 프로파일에 대한 데이터 세트 활성화](https://docs.adobe.com/content/help/en/experience-platform/rtcdp/datasets/dataset.html)
>* [API를 사용하여 실시간 고객 프로필 및 ID 서비스에 대한 데이터 세트 구성](https://docs.adobe.com/content/help/en/experience-platform/catalog/api/getting-started.html)


## 주요 개념 {#key-concepts}

* 기본적으로 Campaign Standard에서 제공되는 필드에만 기본 매핑을 사용할 수 있습니다. 모든 사용자 지정 필드 및 리소스를 수집하려면 각 고객이 자신의 매핑을 정의해야 합니다.

* Adobe Experience Platform Data Connector는 정기적으로 플랫폼을 통해 프로필 데이터를 &#x200B; 푸시합니다. 간격 기간은 15분입니다. Adobe Experience Platform API를 사용하여 이 값을 수정할 [수 있습니다](https://docs.adobe.com/content/help/en/experience-platform/ingestion/home.html).

* 데이터 엔지니어는 Campaign에서 Adobe Experience Platform으로 매핑을 게시, 수정 및 일시 중지할 수 있습니다.

* 모든 타깃팅 차원을 매핑할 수 있습니다. 단일 타깃팅 차원에 있는 모든 필드에 대해 단일 매핑을 갖는 것이 좋습니다.

* 채널 옵트인/옵트아웃을 비롯한 모든 프로필 업데이트는 일괄 업데이트의 일부입니다.

* 모든 Adobe Campaign Standard 또는 XDM 스키마 변경 사항을 수동으로 다시 매핑해야 &#x200B; 합니다.

* 추적 로그 및 Broadlog 데이터는 경험 이벤트로 Adobe Experience Platform에 자동으로 수집됩니다. 이 인제스트는 Adobe Experience Platform으로 실시간으로 스트리밍됩니다.

* ECID(Experience Cloud ID Service)는 기본적으로 경험 이벤트와 함께 전송되는 장치 식별자입니다.

   이 ID는 방문자에게 지정된 고유하고 지속적인 ID로서, Platform Identity Service가 다른 Experience Cloud 솔루션에서 동일한 방문자와 해당 데이터를 식별하는 데 사용할 수 있습니다. 자세한 내용은 Experience Cloud ID 서비스 [도움말을 참조하십시오](https://docs.adobe.com/content/help/en/id-service/using/home.html).

   >[!NOTE]
   >
   >두 개 이상의 프로필이 동일한 장치를 공유하는 경우 통합 ID 서비스에서 두 프로필에 대해 ECID가 동일해야 합니다.

## 제한 사항 {#limitations}

* 구독 이벤트의 기본 전송은 지원되지 않습니다. 구독 이벤트를 전송하려면 Adobe Experience Platform에서 해당 XDM 및 데이터 세트를 만든 다음 이러한 데이터에 대한 사용자 지정 데이터 매핑을 구성할 수 있습니다.

* 개인정보 보호 요청(액세스 및 삭제 작업 모두)과 관련하여 고객은 별도의 요청을 해야 합니다.하나는 Privacy Core Service 통합을 통해 Campaign용( [이 섹션](https://helpx.adobe.com/campaign/kb/acs-privacy.html#righttoaccess)참조) 및 Adobe Experience Platform(개인정보 보호 서비스)을 통한 [것입니다](https://helpx.adobe.com/campaign/kb/acs-privacy.html#ccpa). 액세스 및 삭제 요청에 대한 자세한 내용은 [이 페이지를](https://helpx.adobe.com/campaign/kb/acs-privacy.html#righttoaccess)참조하십시오.

* 각 XDM 필드에 대해 DULE 레이블은 Adobe Experience Platform에서 수행해야 합니다. DULE 레이블을 적용하는 것은 고객의 책임입니다.

* 마케팅 작업에 대한 제한 사항은 DULE 레이블이 Adobe Experience Platform에 적용된 후에만 적용됩니다. 그 전에는 모든 유형의 마케팅 작업에 모든 데이터를 사용할 수 있습니다.

* 15분마다 배치 작업이 실행 중이며 최신 배치 이후 변경된 레코드를 식별합니다. 모든 레코드가 동일한 타임스탬프에서 변경되면 성능 병목 현상이 모든 프로파일의 통합 관리를 관리할 수 있습니다
