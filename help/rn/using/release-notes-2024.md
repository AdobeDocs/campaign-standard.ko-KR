---
title: 2024년 릴리스 정보
description: 이 페이지에는 Adobe Campaign Standard의 2024년 릴리스가 모두 나열됩니다
feature: Overview
role: User
level: Beginner
exl-id: 26616ecc-a009-485c-b13d-d4e0c23969f2
source-git-commit: 85f3a3d8fe9e41eaa78fac955bc2d0f3f3d2c35e
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 96%

---

# 2024년 릴리스 정보 {#release-notes-2024}


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


## 릴리스 24.1 - 2024년 겨울 릴리스 {#winter-24}

### 개선 사항 {#e-rn-improvements}

* **Android 푸시 알림** - Adobe Campaign Standard 24.1은 예정된 FCM 변경 사항과의 호환성을 보장하기 위해 Android 푸시 알림 메시지 전송에 HTTP v1 API를 사용합니다. [이 기술 노트](../../administration/using/push-technote.md)에서 자세히 알아보십시오.

* **iOS 푸시 알림** - Adobe Campaign Standard 24.1이 이제 iOS 푸시 알림에 p8 인증서를 지원합니다. 이 변경 사항을 활성화하려면 구현을 조정해야 합니다. [이 기술 노트](../../administration/using/push-technote.md)에서 자세히 알아보십시오.

* **원클릭 목록-구독 취소** - 2024년 6월 1일부터 Google 및 Yahoo!는 발신자에게 원클릭 목록-구독 취소를 준수하도록 요구할 예정입니다. 이제 Campaign에서 이 기능을 기본 지원합니다. [이 섹션](../../administration/using/configuring-email-channel.md#list-of-email-smtp-parameters)에서 자세히 알아보십시오.

* **인프라** - Postgres 데이터베이스가 버전 11.22에서 버전 12.17로 업그레이드되었습니다.

* **CTA 추적** - 사용자가 개인화된 URL을 열고 클릭하면 이제 코딩된 개인화 URL이 아닌 완료된 개인화 URL을 추적합니다. 이 변경은 기본적으로 적용되지 않습니다. 사용자의 Campaign 인스턴스에 이 변경을 적용하려면 Adobe 담당자에게 문의하십시오.

* **개인화 필드 드롭다운** - 이제 Adobe Experience Manager에서 트랜잭션 이메일 메시지 템플릿을 만들 때 드롭다운 목록에서 개인화 필드를 선택할 수 있습니다. 이 변경은 기본적으로 적용되지 않습니다. 사용자의 Campaign 인스턴스에 이 변경을 적용하려면 Adobe 담당자에게 문의하십시오.

### 해결 사항 {#e-rn-fixes}

* 바운스된 이메일 주소가 30일 후 격리에서 제거되지 않는 문제를 해결했습니다. (CAMP-52977)
* 오류 메시지(`division by zero`)가 표시되며 게재 경고 워크플로가 중단되는 문제를 해결했습니다. (CAMP-49786)
