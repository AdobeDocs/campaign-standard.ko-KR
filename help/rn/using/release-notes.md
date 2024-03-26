---
title: 최신 릴리스
description: 이 페이지에서는 최신 Campaign Standard 릴리스의 콘텐츠를 자세히 설명합니다
feature: Overview
role: User
level: Beginner
exl-id: e1f55a9b-be51-4f57-8719-fed7efc89113
source-git-commit: 26a1c36003645446fb8b827d76afba749d64e9f2
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 100%

---


# 최신 릴리스{#latest-release}

<!--
![Control Panel](assets/do-not-localize/cp-icon.png) **New Control Panel release**. [Learn more](https://experienceleague.adobe.com/docs/control-panel/using/release-notes.html){target="_blank"}.-->

## 릴리스 24.1 - 2024년 겨울 릴리스 {#winter-24}

### 개선 사항 {#e-rn-improvements}

Adobe Campaign Standard 24.1은 Android 푸시 알림 메시지 전송에 HTTP v1 API를 사용하여 예정된 FCM 변경 사항과의 호환성을 보장합니다. [이 기술 노트](../../administration/using/push-technote.md)에서 자세히 알아보십시오.

Adobe Campaign Standard 24.1이 이제 iOS 푸시 알림에 p8 인증서를 지원합니다. 이 변경 사항을 활성화하려면 구현을 조정해야 합니다. [이 기술 노트](../../administration/using/push-technote.md)에서 자세히 알아보십시오.

2024년 6월 1일부터 Google 및 Yahoo!는 발신자에게 원클릭 목록-구독 취소를 준수하도록 요구할 예정입니다. 이제 Campaign에서 이 기능을 기본 지원합니다. [이 섹션](../../administration/using/configuring-email-channel.md#email-channel-parameters)에서 자세히 알아보십시오.

### 수정 사항 {#e-rn-fixes}

* 바운스된 이메일 주소가 30일 후 격리에서 제거되지 않는 문제를 해결했습니다. (CAMP-52977)
* 오류 메시지(`division by zero`)가 표시되며 게재 경고 워크플로우가 중단되는 문제를 해결했습니다. (CAMP-49786)

