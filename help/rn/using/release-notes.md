---
title: 최신 릴리스 정보
description: 이 페이지에서는 최신 Campaign Standard 릴리스의 콘텐츠를 자세히 설명합니다
feature: Overview
role: User
level: Beginner
exl-id: e1f55a9b-be51-4f57-8719-fed7efc89113
source-git-commit: c2d2f3843801d108f007fea52a76e41abe16d76c
workflow-type: ht
source-wordcount: '390'
ht-degree: 100%

---


# 최신 릴리스 정보 {#latest-release}

<!--
![Control Panel](assets/do-not-localize/cp-icon.png) **New Control Panel release**. [Learn more](https://experienceleague.adobe.com/docs/control-panel/using/release-notes.html){target="_blank"}.-->


## 초기 릴리스 정보 {#e-new-release}

이 섹션에는 다음 Campaign Standard 릴리스에 포함된 개선 사항 및 변경 사항의 목록이 있습니다.

>[!CAUTION]
>
>이 콘텐츠는 단계 환경 업그레이드일까지 사전 통지 없이 변경될 수 있습니다. 자세한 내용은 [릴리스 계획 페이지](../../rn/using/release-planning.md)를 참조하십시오.

### 릴리스 25.1 - 2025년 겨울 릴리스 {#winter-25}

#### 보안 수정 사항 {#winter-25-security}

* 이번 릴리스에서는 보안 수정 사항이 적용됩니다.
* 이 릴리스에서는 다음 보안 업그레이드가 제공됩니다. Apache Tomcat이 v10.1.33으로 업그레이드되었습니다.

#### 기타 수정 사항 {#winter-25-fixes}

* 템플릿 중복 문제 해결(CAMP-56340)
* Adobe Experience Manager 템플릿에서 동적 URL이 사용된 경우의 추적 회귀 문제 해결(CAMP-51932)
* 과금 프로세스의 성능 문제 해결(CAMP-56796)
* JSSP 웹 페이지의 `>` 문자와 관련된 HTML 인코딩 문제 해결(CAMP-56497)
* 동적 보고에서 **선택한 행에 표시** 옵션을 사용할 때의 문제 해결(CAMP-55895)


## 릴리스 24.2 - 2024년 여름 릴리스(LA) {#summer-24}

### 개선 사항 {#summer-24-rn-improvements}

**OAuth 서버 간 자격 증명으로 마이그레이션**

이 버전부터 서비스 계정(JWT) 자격 증명이 Adobe에 의해 더 이상 사용되지 않으며, Adobe 솔루션 및 앱과 Campaign 아웃바운드 통합이 이제 OAuth 서버 간 자격 증명을 사용합니다. Adobe은 Campaign-Analytics 통합 또는 Experience Cloud Triggers 통합과 같은 아웃바운드 통합을 위해 JWT를 OAuth로 마이그레이션합니다.

Campaign과 인바운드 통합을 구현했으며 [Campaign API](../../api/using/get-started-apis.md)를 사용하는 경우 [이 설명서](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/){target="_blank"}에서 설명하는 대로 기술 계정을 마이그레이션해야 합니다. 기존 서비스 계정(JWT) 자격 증명은 **2025년 1월 27일**&#x200B;부터 사용할 수 없습니다.

### 해결 사항 {#summer-24-rn-fixes}

* 예약한 시간 전에 워크플로 스케줄러가 시작되는 문제를 해결했습니다. (CAMP-55412)
* 트랜잭션 푸시 알림에서 사용자 정의 필드를 복제할 때 오류가 발생하는 문제를 해결했습니다. (CAMP-54459)
* 인앱 메시지에 대한 시간 및 날짜 스케줄러의 사용에 영향을 주는 문제를 해결했습니다. (CAMP-54495)
* 사용자 정의 추적 별칭 기능을 사용하고 전체 링크가 동적일 때 추적이 작동하지 않는 문제를 해결했습니다. (CAMP-56044)
* 검색을 사용하여 특정 템플릿을 찾을 때 제한된 수의 템플릿만 표시되는 문제를 해결했습니다. (CAMP-55273)
* 기본 언어 드롭다운 목록에 en_kz(영어 - 카자흐스탄) 및 en_ua(영어 - 우크라이나) 언어를 추가했습니다. (CAMP-55336)
* 스케줄러 설정에서 시간 조정 버튼이 작동하지 않는 문제를 해결했습니다. (CAMP-53602)
* 스케줄러 설정의 시간 조정 막대와 관련된 몇 가지 사용자 인터페이스 문제를 해결했습니다. (CAMP-55291)
