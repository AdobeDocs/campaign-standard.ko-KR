---
title: Experience Data Model 개요
description: XDM(Experience Data Model)은 Adobe Experience Platform 솔루션 및 제품과 함께 사용하기 위해 데이터를 수집할 수 있는 표준 데이터 스키마 세트입니다.
audience: administration
content-type: reference
topic-tags: configuring-channels
feature: Microsoft CRM Integration
old-role: Data Architect
role: Developer
level: Experienced
exl-id: cc1aa669-30cd-4ea4-9fab-4d1b6c373744
hide: true
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
  - id: f5407121-8933-4ac3-8e06-a9b692a4e88a
    internal-label: Campaign Standard
feature_v2:
  - id: d5ef99fa-df0c-4153-bf94-105ad0724167
    internal-label: Integrations
subfeature_v2:
  - id: dd99420f-367d-4a14-bbc4-5140615992c2
    internal-label: Microsoft CRM integration
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: bb37e2bfbc52de1b0cc03f0f8e03985caff5e5b0
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%
---
# Experience Data Model 개요 {#experience-data-model-overview}

>[!IMPORTANT]
>
>Adobe Experience Platform Data Connector는 현재 베타 버전이며 예고 없이 자주 업데이트될 수 있습니다. 이러한 기능에 액세스하려면 고객을 Azure(현재 북미 지역의 경우에만 베타 버전)에서 호스팅해야 합니다. 액세스하려면 Adobe 고객 지원 센터에 문의하십시오.

XDM(Experience Data Model)은 Adobe Experience Platform 솔루션 및 제품과 함께 사용하기 위해 데이터를 수집할 수 있는 표준 데이터 스키마 세트입니다.

XDM 스키마의 생성 및 관리는 전용 API 또는 XDM 사용자 인터페이스를 통해 사용할 수 있습니다.

## XDM 작업 영역 {#xdm-workspace}

XDM Workspace은 데이터 스키마를 보고, 만들고, 확장할 수 있는 기능을 제공합니다.

XDM 사용자 인터페이스에 액세스하려면 Adobe Experience Platform을 엽니다. XDM 스키마를 생성하거나 확장하려면 데이터 모델 창으로 이동합니다.

전체 [XDM Workspace 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html)를 참조하세요.

![](assets/aep_xdmworkspace.png)

## XDM API {#xdm-api}

XDM 스키마 API를 통해 다음 작업을 수행할 수 있습니다.

* 기존 스키마 목록 보기
* 특정 스키마 보기 기존 스키마 확장
* 확장에 필드 추가
* 새 스키마 만들기 및 업데이트
* 스키마 설명자 보기
* 스키마 설명자 만들기, 업데이트 및 삭제

API 호출 조작에 대한 모든 세부 정보는 [개발자 안내서](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html)에서 확인할 수 있습니다.
