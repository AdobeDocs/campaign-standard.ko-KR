---
title: 최신 릴리스 정보
description: 이 페이지에서는 최신 Campaign Standard 릴리스의 콘텐츠를 자세히 설명합니다
feature: Overview
role: User
level: Beginner
exl-id: e1f55a9b-be51-4f57-8719-fed7efc89113
source-git-commit: 44c436a74a0a4aa688427bfb36d506566d57ac3a
workflow-type: tm+mt
source-wordcount: '387'
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

**릴리스 24.2 - 2024년 여름 릴리스**

* **릴리스 날짜**: 2024년 8월(제한 공개) - [자세히 알아보기](../../rn/using/release-planning.md).

* **OAuth 서버 간 자격 증명으로 마이그레이션**

  이 버전부터 서비스 계정(JWT) 자격 증명이 Adobe에 의해 더 이상 사용되지 않으며, Adobe 솔루션 및 앱과 Campaign 아웃바운드 통합이 이제 OAuth 서버 간 자격 증명을 사용합니다. Adobe은 Campaign-Analytics 통합 또는 Experience Cloud Triggers 통합과 같은 아웃바운드 통합을 위해 JWT를 OAuth로 마이그레이션합니다.

  Campaign과 인바운드 통합을 구현했으며 [Campaign API](../../api/using/get-started-apis.md)를 사용하는 경우 [이 설명서](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/){target="_blank"}에서 설명하는 대로 기술 계정을 마이그레이션해야 합니다. 기존 서비스 계정(JWT) 자격 증명은 **2025년 1월 27일**&#x200B;부터 사용할 수 없습니다.


## 릴리스 24.1 - 2024년 겨울 릴리스 {#winter-24}

### 개선 사항 {#e-rn-improvements}

* **Android 푸시 알림** - Adobe Campaign Standard 24.1은 예정된 FCM 변경 사항과의 호환성을 보장하기 위해 Android 푸시 알림 메시지 전송에 HTTP v1 API를 사용합니다. [이 기술 노트](../../administration/using/push-technote.md)에서 자세히 알아보십시오.

* **iOS 푸시 알림** - Adobe Campaign Standard 24.1이 이제 iOS 푸시 알림에 p8 인증서를 지원합니다. 이 변경 사항을 활성화하려면 구현을 조정해야 합니다. [이 기술 노트](../../administration/using/push-technote.md)에서 자세히 알아보십시오.

* **원클릭 목록-구독 취소** - 2024년 6월 1일부터 Google 및 Yahoo!는 발신자에게 원클릭 목록-구독 취소를 준수하도록 요구할 예정입니다. 이제 Campaign에서 이 기능을 기본 지원합니다. [이 섹션](../../administration/using/configuring-email-channel.md#list-of-email-smtp-parameters)에서 자세히 알아보십시오.

* **인프라** - Postgres 데이터베이스가 버전 11.22에서 버전 12.17로 업그레이드되었습니다.

* **CTA 추적** - 사용자가 개인화된 URL을 열고 클릭하면 이제 코딩된 개인화 URL이 아닌 완료된 개인화 URL을 추적합니다. 이 변경은 기본적으로 적용되지 않습니다. 사용자의 Campaign 인스턴스에 이 변경을 적용하려면 Adobe 담당자에게 문의하십시오.

* **개인화 필드 드롭다운** - 이제 Adobe Experience Manager에서 트랜잭션 이메일 메시지 템플릿을 만들 때 드롭다운 목록에서 개인화 필드를 선택할 수 있습니다. 이 변경은 기본적으로 적용되지 않습니다. 사용자의 Campaign 인스턴스에 이 변경을 적용하려면 Adobe 담당자에게 문의하십시오.

### 수정 사항 {#e-rn-fixes}

* 바운스된 이메일 주소가 30일 후 격리에서 제거되지 않는 문제를 해결했습니다. (CAMP-52977)
* 오류 메시지(`division by zero`)가 표시되며 게재 경고 워크플로우가 중단되는 문제를 해결했습니다. (CAMP-49786)

