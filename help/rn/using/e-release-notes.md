---
title: 초기 릴리스 정보
description: 초기 릴리스 정보
feature: Overview
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 4b10eb63-3fea-438e-a1a7-25fbf7b0e5b0
source-git-commit: 46c5454ad712910c88bfda7c067fda0337b043d9
workflow-type: ht
source-wordcount: '235'
ht-degree: 100%

---


# 초기 릴리스 정보 {#e-new-release}

이 페이지에서는 다음 Campaign Standard 릴리스에 포함된 개선 사항 및 문제 해결에 대해 설명합니다.

>[!CAUTION]
>
> 이 콘텐츠는 단계 환경 업그레이드일까지 사전 통지 없이 변경될 수 있습니다. 자세한 내용은 [릴리스 계획 페이지](../../rn/using/release-planning.md)를 참조하세요.

## 릴리스 23.2 - 2023년 가을/겨울 릴리스 {#fall-23}

>[!AVAILABILITY]
>
>이 릴리스는 일부 조직에만 적용될 수 있습니다(제한 공개). 자세한 내용은 Adobe 담당자에게 문의하세요.

### 개선 사항 {#e-rn-improvements}

* **Adobe Experience Manager와 통합**. 이제 Adobe Experience Manager에서 트랜잭션 메시지에 개인화된 게재 템플릿을 만들 때 드롭다운에서 Campaign Standard에 정의된 개인화 필드를 선택해 사용할 수 있습니다.

* **쿠키 만료** - 이제 기본 쿠키 만료가 6개월로 설정되어 프랑스 데이터 보호 기관(CNIL) 권장 사항을 준수합니다.

* **프로필 검색 개선** - 프로필 검색이 최적화되어 검색 시간 초과를 줄일 수 있습니다.

* **지역화** - 메시지를 받을 프로필 그룹을 참조할 때 &quot;대상자&quot;라는 용어의 번역이 다음 언어의 모든 Digital Experience 제품에서 일치합니다.

   * 독일어: Zielgruppe
   * 포르투갈어(브라질): público-alvo
   * 스페인어: público destinatario

  이러한 변경 사항은 다음 UI 및 설명서 릴리스를 통해 점진적으로 적용됩니다.

### 기타 변경 사항 {#e-rn-other-changes}

* 이제 트랜잭션 메시징에서 쉼표로 구분된 여러 선호도를 사용할 수 있습니다.

### 수정 사항 {#e-rn-fixes}

* 대규모 워크플로우를 사용할 때 성능 문제를 초래할 수 있는 회귀 문제를 해결했습니다. (CAMP-53369)
* 워크플로우 경고 또는 알림의 이메일 링크가 작동하지 않는 문제를 해결했습니다. (CAMP-51874)
