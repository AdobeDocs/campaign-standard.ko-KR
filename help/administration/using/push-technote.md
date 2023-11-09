---
title: 푸시 알림 채널 예정된 변경 사항
description: 푸시 알림 채널 예정된 변경 사항
audience: channels
feature: Instance Settings
role: Admin
level: Experienced
hide: true
hidefromtoc: true
source-git-commit: 870b01f118974ed62755dd79143b990cfa2e4e85
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 0%

---

# 푸시 알림 채널 예정된 변경 사항 {#push-upgrade}

이 페이지에서는 Adobe Campaign Standard의 Android 및 iOS 푸시 알림 채널에 대해 예정된 변경 사항에 대해 설명합니다.

Adobe Campaign Standard 구현에 영향을 줄 수 있는 Android 및 iOS 장치 전반의 푸시 알림 채널에 대한 변경 사항과 관련하여 중요한 업데이트가 있습니다.

## Android {#push-android}

Google은 서비스 개선을 위한 Google의 지속적인 노력의 일환으로 Firebase Cloud Messaging HTTP 프로토콜을 변경하고 있습니다. 그 결과 2023년 6월 20일에 사용이 중단되었던 Firebase Cloud Messaging &quot;HTTP 레거시 API&quot;는 2024년 6월에 &quot;HTTP v1 API&quot;로 대체됩니다. (https://firebase.google.com/docs/cloud-messaging/http-server-ref). 현재 Adobe Campaign Standard은 HTTP 레거시 API를 사용하여 Android 푸시 알림 메시지를 전송하고, 향후 몇 개월 이내에 HTTP v1 API로 업그레이드하도록 변경될 예정입니다. Adobe이 이러한 업데이트에서 작동하면 이러한 변경 사항에 대한 자세한 정보가 제공됩니다.

## iOS {#push-ios}

또한 Adobe은 iOS 푸시 알림 채널용 Adobe Campaign Standard을 업그레이드하고 관리자가 iOS 애플리케이션에 대한 인증서를 구성할 수 있도록 하는 방식을 변경할 예정입니다. 관리자는 이제 Adobe Campaign Standard의 사용자 인터페이스를 통해 iOS 인증서를 업로드해야 합니다.

당사의 고객은 마케팅 캠페인 및 커뮤니케이션 요구 사항을 위해 이러한 서비스를 이용하고 있으며 귀하가 당사의 지속적인 계획 및 지원을 숙지하고 있는지 확인하고 싶어합니다.

## 뭐하는 거야?

* **제품 변경 사항**: Android/iOS 푸시 알림 채널에서 기술 스택 업그레이드를 지원하기 위한 제품 변경 작업.

* **자세한 지침**: 원활한 전환 프로세스를 촉진하기 위한 단계별 안내서와 기타 리소스를 제공합니다.

* **지원**: 이 전환 전반에 걸쳐 EMC 고객 지원 팀에서 도움을 드릴 수 있습니다. 또한 전환에 대한 기술 측면과 모범 사례를 다루기 위해 웨비나와 활성화 세션을 호스팅할 수 있습니다.

## 어떤 영향을 미칩니까?

* **최신 정보 수신**: 세부 전환 계획을 포함하여 더 이상 당사에서 커뮤니케이션을 할 수 없도록 받은 편지함을 주시하십시오.

* **현재 설정 검토**: 필요한 경우 변경할 수 있도록 Adobe Campaign Standard의 현재 구성 및 사용자 지정을 검토하십시오.

* **연락처**: 즉각적인 우려 사항이나 질문이 있는 경우 주저하지 말고 지원 팀에 문의하십시오.

## 다음 단계

앞으로 몇 주 이내에 타임라인 및 작업 항목 등 Android/iOS용 푸시 채널에 대해 예정된 변경 사항에 대한 자세한 내용을 공유할 예정입니다. 당사의 주요 목표는 귀하와 귀하의 팀이 최대한 원활하게 전환할 수 있도록 하는 것입니다.

이러한 변화에 적응하면서 이해해 주셔서 감사합니다. 여러분의 성공이 저희의 최우선 과제이며, 저희는 여러분을 지원하기 위해 최선을 다하고 있습니다.