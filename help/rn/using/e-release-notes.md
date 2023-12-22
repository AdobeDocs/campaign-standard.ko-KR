---
title: 초기 릴리스 정보
description: 초기 릴리스 정보
feature: Overview
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 4b10eb63-3fea-438e-a1a7-25fbf7b0e5b0
source-git-commit: 602aca18af81625b9756a8f2020b5bc636199b96
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 68%

---


# 초기 릴리스 정보 {#e-new-release}

이 페이지에서는 다음 Campaign Standard 릴리스에 포함된 개선 사항 및 문제 해결에 대해 설명합니다.

>[!CAUTION]
>
> 이 콘텐츠는 단계 환경 업그레이드일까지 사전 통지 없이 변경될 수 있습니다. 자세한 내용은 [릴리스 계획 페이지](../../rn/using/release-planning.md)를 참조하세요.

## 릴리스 24.1 - 2024년 겨울 릴리스 {#winter-24}

>[!AVAILABILITY]
>
>이 릴리스는 일부 조직에만 적용될 수 있습니다(제한 공개). 자세한 내용은 Adobe 담당자에게 문의하세요.

### 개선 사항 {#e-rn-improvements}

Adobe Campaign Standard 24.1은 HTTP v1 API를 사용하여 Android 푸시 알림 메시지를 보내어 예정된 FCM 변경 사항과의 호환성을 보장합니다. [이 기술 노트](../../administration/using/push-technote.md)에서 자세히 알아보십시오.


### 수정 사항 {#e-rn-fixes}

* 게재 경고 워크플로우를 중지하는 문제를 해결했습니다. 다음 오류가 발생했습니다. `division by zero`. (CAMP-49786)
