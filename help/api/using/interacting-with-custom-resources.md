---
title: 사용자 지정 리소스와 상호 작용
description: API를 통한 사용자 지정 리소스 관리에 대해 자세히 알아보기/
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
old-role: Data Architect
role: Developer
level: Experienced
exl-id: 19bfeecb-da60-479c-a929-0cfb72ef59e3
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
  - id: f5407121-8933-4ac3-8e06-a9b692a4e88a
    internal-label: Campaign Standard
feature_v2:
  - id: b12f6872-9271-4369-85e5-86969a0b99a2
    internal-label: APIs
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: bb37e2bfbc52de1b0cc03f0f8e03985caff5e5b0
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 0%
---
# 사용자 지정 리소스와 상호 작용 {#interacting-with-custom-resources}

**/customResources** 끝점을 사용하면 REST의 Campaign 사용자 지정 리소스를 표시할 수 있습니다. 이 API를 기반으로 사용자 지정 엔티티와 외부 엔드포인트 간의 통합을 사용할 수 있습니다.

/customResources 끝점의 동작은 /profileAndServices 끝점과 동일합니다.

이 API 내에 노출되는 사용자 지정 리소스는 다음과 같습니다.

* /profileAndServicesExt 아래에 노출되지 않은 모든 엔터티
* 프로필에 연결되어 있지 않은 모든 엔티티와 이러한 엔티티의 경우 1차 하위 구성요소 및 손자
* 기본적으로 연결되어 있지 않은 모든 엔티티와 그 자식 및 손자

>[!NOTE]
>/profileAndServicesExt에서 사용할 수 있는 사용자 지정 리소스는 /customResources API에 노출되지 않습니다.


다음은 사용자 지정 리소스에서 메타데이터를 검색하는 예입니다.

```
GET /customResources/resourceType/<customResourceName>
```

만들기, 업데이트 또는 삭제를 수행하려면 GET, POST, PATCH, DELETE을 사용합니다.

```
POST /customResources/<customResourceName>
```

>[!NOTE]
>개인 정보 보호 API 끝점 및 워크플로(/privacy/privacyTool)는 프로필 엔티티에 연결되어 있지 않은 사용자 지정 리소스를 관리하지 않습니다.
>이러한 사용자 지정 리소스에 대한 모든 PII를 관리 및 정리할 책임이 있습니다. 개인 정보 보호 도구에 대한 자세한 내용을 보려면 [여기를 클릭](../../api/using/creating-a-privacy-request.md)하세요.
