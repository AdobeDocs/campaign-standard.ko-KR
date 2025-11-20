---
title: 최신 릴리스 정보
description: 이 페이지에서는 최신 Campaign Standard 릴리스의 콘텐츠를 자세히 설명합니다
feature: Overview
role: User
level: Beginner
exl-id: e1f55a9b-be51-4f57-8719-fed7efc89113
source-git-commit: c1f64589578c144a9b8eb879684f27834efaf8d8
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 100%

---


# 최신 릴리스 정보 {#latest-release}

<!--
## Release notes {#e-new-release}


This section lists improvements and changes included in the next Campaign Standard release.

>[!CAUTION]
>
>This content is subject to changes without prior notice until the stage environments upgrade date. Learn more in the [Release planning page](../../rn/using/release-planning.md).

-->

## 릴리스 25.2 - 2025년 여름 릴리스 {#summer-25}

### 보안 수정 사항 {#summer-25-security}

* 이번 릴리스에서는 보안 수정 사항이 적용됩니다.
* 이 릴리스에서 제공되는 보안 업그레이드: PostgreSQL 14.18, Azure 인스턴스를 CentOS에서 Rocky로 마이그레이션.

### 기타 해결 사항 {#summer-25-fixes}

* 시스템 안정성을 높이기 위해 시퀀스 소진 처리를 개선했습니다. (CAMP-57281)
* 전반적인 제품 안정화 업데이트. (CAMP-57339)
* 동적 보고 기능을 개선하여 견고성을 높이고 데이터 불일치를 줄였습니다. (CAMP-58157)
* 드롭다운 메뉴가 텍스트를 올바르게 둘러싸지 않는 문제를 해결했습니다. (CAMP-57360)
* 사용자가 2년 넘게 지난 데이터를 쿼리하지 못하도록 보고 기능을 업데이트했습니다. (CAMP-59262)

## 릴리스 25.1.2 {#25.1.2}

### 보안 수정 사항 {#25.1.2-security}

* 이번 릴리스에서는 보안 수정 사항이 적용됩니다.
* 이 릴리스에서 제공되는 보안 업그레이드: Apache Tomcat이 v10.1.36으로 업그레이드되었습니다.

### 기타 해결 사항 {#25.1.2-fixes}

* 사용자가 IMS를 통해 로그인하지 못하는 결과로 이어질 수 있는 토큰 구문 분석 문제를 해결했습니다. (CAMP-57337)
* 시스템 안정성을 높이기 위해 자동 시퀀스 ID 생성 메커니즘을 개선했습니다. (CAMP-57281)

## 릴리스 25.1 - 2025년 겨울 릴리스 {#winter-25}

### 보안 수정 사항 {#winter-25-security}

* 이번 릴리스에서는 보안 수정 사항이 적용됩니다.
* 이 릴리스에서는 다음 보안 업그레이드가 제공됩니다. Apache Tomcat이 v10.1.33으로 업그레이드되었습니다.

### 기타 해결 사항 {#winter-25-fixes}


* 구독 요약 화면의 &#39;데이터 스키마&#39; URL 수정(CAMP-56168, CAMP-56296)
* **즉시 전송할 메시지** 옵션을 사용할 때 피로도 규칙을 무시하는 문제 해결(CAMP-56866, CAMP-57033)
* 템플릿 중복 문제 해결(CAMP-56340)
* Adobe Experience Manager 템플릿에서 동적 URL이 사용된 경우의 추적 회귀 문제 해결(CAMP-51932)
* 과금 프로세스의 성능 문제 해결(CAMP-56796)
* JSSP 웹 페이지의 `>` 문자와 관련된 HTML 인코딩 문제 해결(CAMP-56497)
* 동적 보고에서 **선택한 행에 표시** 옵션을 사용할 때의 문제 해결(CAMP-55895)

