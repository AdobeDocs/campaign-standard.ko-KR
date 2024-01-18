---
title: 초기 릴리스 정보
description: 초기 릴리스 정보
feature: Overview
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 4b10eb63-3fea-438e-a1a7-25fbf7b0e5b0
source-git-commit: d6421cda301eed85fddf2df7b2d6fc2cf1db96b3
workflow-type: ht
source-wordcount: '140'
ht-degree: 100%

---


# 초기 릴리스 정보 {#e-new-release}

이 페이지에서는 다음 Campaign Standard 릴리스에 포함된 개선 사항 및 문제 해결에 대해 설명합니다.

>[!CAUTION]
>
> 이 콘텐츠는 단계 환경 업그레이드일까지 사전 통지 없이 변경될 수 있습니다. 자세한 내용은 [릴리스 계획 페이지](../../rn/using/release-planning.md)를 참조하세요.

## 릴리스 24.1 - 2024년 겨울 릴리스 {#winter-24}

### 개선 사항 {#e-rn-improvements}

Adobe Campaign Standard 24.1은 Android 푸시 알림 메시지 전송에 HTTP v1 API를 사용하여 예정된 FCM 변경 사항과의 호환성을 보장합니다. [이 기술 노트](../../administration/using/push-technote.md)에서 자세히 알아보십시오.

Adobe Campaign Standard 24.1이 이제 iOS 푸시 알림에 p8 인증서를 지원합니다. 이 변경 사항을 활성화하려면 구현을 조정해야 합니다. [이 기술 노트](../../administration/using/push-technote.md)에서 자세히 알아보십시오.


### 수정 사항 {#e-rn-fixes}

* 바운스된 이메일 주소가 30일 후 격리에서 제거되지 않는 문제를 해결했습니다. (CAMP-52977)
* 오류 메시지(`division by zero`)가 표시되며 게재 경고 워크플로우가 중단되는 문제를 해결했습니다. (CAMP-49786)
