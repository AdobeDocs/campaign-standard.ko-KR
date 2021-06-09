---
solution: Campaign Standard
product: campaign
title: 경험 데이터 모델 개요
description: XDM(Experience Data Model)은 Adobe Experience Platform 솔루션 및 제품에서 사용할 수 있도록 데이터를 수집할 수 있는 표준 데이터 스키마 세트입니다.
audience: administration
content-type: reference
topic-tags: configuring-channels
feature: Microsoft CRM 통합
role: Data Architect
level: Experienced
exl-id: cc1aa669-30cd-4ea4-9fab-4d1b6c373744
source-git-commit: 92365fe416fced72e7ad5818da0dbed5d8f52f15
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# 경험 데이터 모델 개요 {#experience-data-model-overview}

>[!IMPORTANT]
>
>Adobe Experience Platform Data Connector는 현재 베타 버전으로, 예고 없이 자주 업데이트될 수 있습니다. 고객은 이러한 기능에 액세스하려면 Azure에서 호스팅(현재 북미 전용 베타 버전)해야 합니다. 액세스하려면 고객 지원 센터에 문의하십시오.

XDM(Experience Data Model)은 Adobe Experience Platform 솔루션 및 제품에서 사용할 수 있도록 데이터를 수집할 수 있는 표준 데이터 스키마 세트입니다.

XDM 스키마 만들기 및 관리는 전용 API 또는 XDM 사용자 인터페이스에서 사용할 수 있습니다.

## XDM 작업 공간 {#xdm-workspace}

XDM Workspace 는 데이터 스키마를 보고, 만들고, 확장하는 기능을 제공합니다.

XDM 사용자 인터페이스에 액세스하려면 Adobe Experience Platform을 엽니다. XDM 스키마를 만들거나 확장하려면 데이터 모델 창으로 이동합니다.

전체 [XDM 작업 공간 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html)를 참조하십시오.

![](assets/aep_xdmworkspace.png)

## XDM API {#xdm-api}

XDM 스키마 API를 통해 다음 작업을 수행할 수 있습니다.

* 기존 스키마 목록 보기
* 특정 스키마 보기 기존 스키마 확장
* 확장에 필드 추가
* 새 스키마 만들기 및 업데이트
* 스키마 설명자 보기
* 스키마 설명자 만들기, 업데이트 및 삭제

API 호출을 조작하는 모든 세부 사항은 [개발자 안내서](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html)에서 확인할 수 있습니다.
