---
title: 2024년 릴리스 정보
description: 이 페이지에는 Adobe Campaign Standard의 2024년 릴리스가 모두 나열됩니다
feature: Overview
role: User
level: Beginner
source-git-commit: c70e3058f75ba2b11a8311628198e5c02d489964
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 93%

---

# 2024년 릴리스 정보 {#release-notes-2024}

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

