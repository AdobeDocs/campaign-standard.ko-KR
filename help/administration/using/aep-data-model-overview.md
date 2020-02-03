---
title: 경험 데이터 모델 개요
description: XDM(Experience Data Model)은 Adobe Experience Platform 솔루션 및 제품과 함께 사용하기 위해 데이터를 인제스트할 수 있는 데이터 스키마의 표준 세트입니다.
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
source-git-commit: 67223cf8eed46e2431c03674bd837262e37c7473

---


# 경험 데이터 모델 개요 {#experience-data-model-overview}

>[!IMPORTANT]
>
>Campaign Standard Data Service는 현재 베타 버전으로, 예고 없이 자주 업데이트될 수 있습니다. 이러한 기능에 액세스하려면 고객이 Azure(현재 북미 전용 베타 버전)에서 호스팅되어야 합니다. 액세스하려면 Adobe 고객 지원 센터에 문의하십시오.

XDM(Experience Data Model)은 Adobe Experience Platform 솔루션 및 제품과 함께 사용하기 위해 데이터를 인제스트할 수 있는 데이터 스키마의 표준 세트입니다.

XDM 스키마 생성 및 관리는 전용 API 또는 XDM 사용자 인터페이스를 통해 사용할 수 있습니다.

## XDM 작업 영역 {#xdm-workspace}

XDM 작업 공간에서는 데이터 스키마를 보고, 만들고, 확장할 수 있습니다.

XDM 사용자 인터페이스에 액세스하려면 Adobe Experience Platform을 엽니다. 데이터 모델 창으로 이동하여 XDM 스키마를 만들거나 확장합니다.

전체 XDM [작업 영역 설명서를](https://www.adobe.io/apis/experienceplatform/home/xdm/xdmservices.html#!api-specification/markdown/narrative/technical_overview/schema_registry/xdm_system/xdm_system_in_experience_platform.md)참조하십시오.

![](assets/aep_xdmworkspace.png)

## XDM API {#xdm-api}

XDM 스키마 API를 통해 다음 작업을 수행할 수 있습니다.

* 기존 스키마 목록 보기
* 특정 스키마 보기 기존 스키마 확장
* 확장명에 필드 추가
* 새 스키마 만들기 및 업데이트
* 스키마 설명자 보기
* 스키마 설명자 만들기, 업데이트 및 삭제

API 호출 조작에 대한 모든 세부 사항은 개발자 안내서를 [참조하십시오](https://www.adobe.io/apis/experienceplatform/home/xdm/xdmservices.html#!api-specification/markdown/narrative/technical_overview/schema_registry/schema_registry_developer_guide.md).
