---
title: 초기 릴리스 정보
description: 초기 릴리스 정보
feature: Overview
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 4b10eb63-3fea-438e-a1a7-25fbf7b0e5b0
source-git-commit: 20a59e064afeb93a2a6260439b09790692971071
workflow-type: ht
source-wordcount: '130'
ht-degree: 100%

---


# 초기 릴리스 정보 {#e-new-release}

이 페이지에서는 다음 Campaign Standard 릴리스에 포함된 개선 사항 및 문제 해결에 대해 설명합니다.

>[!CAUTION]
>
> 이 콘텐츠는 단계 환경 업그레이드일까지 사전 통지 없이 변경될 수 있습니다. 자세한 내용은 [릴리스 계획 페이지](../../rn/using/release-planning.md)를 참조하세요.

## 릴리스 22.3 - 2022년 가을/겨울 {#e-rn-2022}

<!--
### Improvement{#e-rn-improvements}


**Accessibility**

Campaign Standard 22.3 comes with accessibility fixes and improvements which facilitate users to navigate and get the most out of Adobe Campaign.

These capabilities are released in Limited Availability and rolled out to a set of customers only. To have these improvements enabled on your Campaign environment(s), contact your Adobe representative.
-->

### 보안 업데이트{#e-rn-security}

이 릴리스는 다음과 같은 보안 업그레이드와 함께 제공됩니다. Apache Tomcat이 v7.0에서 v8.0으로 업그레이드되었습니다.

### 수정 사항{#e-rn-fixes}

* 예약된 시간보다 1시간 전에 트리거된 예약된 보고서 문제를 수정했습니다. (CAMP-51502)
* 전송 로그(nms:broadLogRcp)와 일치하지 않는 게재 대시보드의 게재 표시기에 대한 문제를 해결했습니다. (CAMP-51127)
* ACS 커넥터(Prime Offer)에서 사용자 지정 리소스 확장을 할 수 없는 문제를 해결했습니다. (CAMP-51033)
* 지연을 방지하기 위해 개인 정보 보호 요청 응답에 대한 게시 프로세스를 개선했습니다. (CAMP-50613)