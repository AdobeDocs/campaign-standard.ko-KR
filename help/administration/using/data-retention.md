---
solution: Campaign Standard
product: campaign
title: 데이터 유지
description: null
audience: administration
content-type: reference
topic-tags: application-settings
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 64%

---


# 데이터 유지{#data-retention}

Campaign의 표준 로그 테이블에는 사전 설정된 보존 기간이 있으므로 일반적으로 데이터 스토리지를 6개월 이내로 제한합니다.

다음은 표준 테이블의 기본 보존 값입니다. 보존 구성은 구현 중에 Adobe 기술 관리자가 설정하며 고객 요구 사항에 따라 각 구현마다 값이 달라질 수 있습니다.

* **통합 추적**: 6개월
* **게재 로그**: 6개월
* **추적 로그**: 6개월
* **이벤트**: 1개월
* **이벤트 처리 통계**: 6개월
* **보관된 이벤트**: 6개월
* **임시 엔터티**: 7일
* **무시된 파이프라인 이벤트**: 1개월
* **게재 경고**: 1개월
* **내보내기 감사**: 6개월

표준 워크플로우 기능을 사용하면 모든 사용자 정의 테이블에 대해 보존 기간을 설정할 수 있습니다.

Adobe 컨설턴트 또는 기술 관리자에게 문의하여 보존에 대한 자세한 내용을 확인하거나 사용자 지정 테이블에 대한 보존을 설정해야 합니다.
