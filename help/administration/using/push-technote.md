---
title: 푸시 알림 채널 예정된 변경 사항
description: 푸시 알림 채널 예정된 변경 사항
audience: channels
feature: Instance Settings
role: Admin
level: Experienced
hide: true
hidefromtoc: true
source-git-commit: f9a0d01196ac4c31e57ae14cdfa448a9ffd6106f
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 1%

---

# 푸시 알림 채널 예정된 변경 사항 {#push-upgrade}

Campaign을 사용하여 Android 및 iOS 디바이스에서 푸시 알림을 전송할 수 있습니다. 이를 수행하기 위해 Campaign은 특정 구독 서비스를 사용합니다. Android FCM(Firebase Cloud Messaging) 서비스에 대한 몇 가지 중요한 변경 사항은 2024년에 릴리스될 예정이며 Adobe Campaign 구현에 영향을 줍니다. 또한 iOS 앱의 경우 Adobe에서 관리자가 인증서를 구성할 수 있도록 하는 방법을 변경하고 있습니다.

## 변경 사항 {#push-changes}

### Android {#push-android}

서비스 개선을 위한 Google의 지속적인 노력의 일환으로 레거시 FCM API는에서 중단됩니다. **2024년 6월 20일**. 에서 Firebase Cloud Messaging HTTP 프로토콜에 대해 자세히 알아보기 [Google Firebase 설명서](https://firebase.google.com/docs/cloud-messaging/http-server-ref){target="_blank"}.

현재 Adobe Campaign Standard은 HTTP 레거시 API를 사용하여 Android 푸시 알림 메시지를 전송하고, 향후 몇 개월 이내에 HTTP v1 API로 업그레이드하도록 변경될 예정입니다.

### iOS {#push-ios}

또한 Adobe은 iOS 푸시 알림 채널용 Adobe Campaign Standard을 업그레이드하고 관리자가 iOS 애플리케이션에 대한 인증서를 구성할 수 있도록 하는 방식을 변경할 예정입니다. 관리자는 이제 Adobe Campaign Standard의 사용자 인터페이스를 통해 iOS 인증서를 업로드해야 합니다.

## 영향을 받습니까? {#push-impact}

Campaign Standard 사용자는 대상에 푸시 알림 메시지를 보내는 경우 영향을 받습니다.

## 마이그레이션 방법 {#push-migration}

이러한 업데이트는 모바일 채널 구성 및 권한 관리에 영향을 주므로 Campaign Standard 빌드 업그레이드가 필요합니다.

원활한 전환과정이 이루어질 수 있도록 자세한 안내는 곧 제공될 예정이다.

고객 지원 팀은 이 전환 전반에 걸쳐 여러분을 지원할 수 있습니다. 또한 전환에 대한 기술 측면과 모범 사례를 다루기 위해 웨비나와 활성화 세션을 호스팅할 수 있습니다.

그동안 Adobe Campaign Standard에서 현재 구성 및 맞춤화를 검토하는 것이 좋습니다. 필요한 경우 필요한 변경을 수행할 준비가 되었습니다.

당사의 지원 팀에 당면한 우려 사항이나 질문이 있는 경우 주저하지 말고 연락해 주십시오.
