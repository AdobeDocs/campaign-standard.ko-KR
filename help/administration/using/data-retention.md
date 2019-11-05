---
title: 데이터 유지
description: null
page-status-flag: 활성화 안 함
uuid: d90852b4-e9f3-4187-bea-e748d16d1590
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 관리
content-type: reference
topic-tags: application-settings
discoiquuid: b791562b-6c51-447d-9e5b-bb77136f3dd8
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 데이터 유지{#data-retention}

Campaign의 표준 로그 테이블에는 사전 설정된 보존 기간이 있으며, 일반적으로 데이터 스토리지를 6개월 이내로 제한합니다.

다음은 표준 테이블에 대한 기본 보존 값입니다. 유지 구성은 구현 중에 Adobe 기술 관리자가 설정하며 고객 요구 사항에 따라 각 구현마다 값이 달라질 수 있습니다.

* **통합 추적**:6개월
* **배달 로그**:6개월
* **추적 로그**:6개월
* **이벤트**:1개월
* **이벤트 처리**&#x200B;통계:6개월
* **보관된 이벤트**:6개월
* **임시 개체**:7일
* **무시된 파이프라인 이벤트**:1개월
* **전달 경고**:1개월
* **내보내기 감사**:6개월

표준 워크플로우 기능을 사용하면 모든 사용자 정의 테이블에 대해 보존 기간을 설정할 수 있습니다.

Adobe 컨설턴트 또는 기술 관리자에게 연락하여 보존에 대한 자세한 내용을 살펴보거나 사용자 정의 표에 대한 보존을 설정해야 하는 경우
