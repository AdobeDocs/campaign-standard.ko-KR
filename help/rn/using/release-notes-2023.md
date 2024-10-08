---
title: 2023년 릴리스 정보
description: 이 페이지에는 Adobe Campaign Standard의 2023년 릴리스 전체 목록이 있습니다.
feature: Overview
role: User
level: Beginner
exl-id: 5817c4d2-4788-4695-bf9a-ec04cc042190
source-git-commit: 30e96494dd7fa3313601e48deeec8ef98dcdce85
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 100%

---

# 2023년 릴리스 정보 {#release-notes-2023}

## 릴리스 23.2 - 2023년 가을/겨울 릴리스 {#fall-23}

>[!AVAILABILITY]
>
>이 릴리스는 일부 조직에만 적용될 수 있습니다(제한 공개). 자세한 내용은 Adobe 담당자에게 문의하세요.

### 개선 사항 {#fall-23-rn-improvements}

* **Adobe Experience Manager와 통합**. 이제 Adobe Experience Manager에서 트랜잭션 메시지에 개인화된 게재 템플릿을 만들 때 드롭다운에서 Campaign Standard에 정의된 개인화 필드를 선택해 사용할 수 있습니다. [자세히 알아보기](../../integrating/using/creating-email-experience-manager.md)

* **쿠키 만료** - 이제 기본 쿠키 만료가 6개월로 설정되어 프랑스 데이터 보호 기관(CNIL) 권장 사항을 준수합니다.

* **프로필 검색 개선** - 프로필 검색이 최적화되어 검색 시간 초과를 줄일 수 있습니다.

* **지역화** - 메시지를 받을 프로필 그룹을 참조할 때 &quot;대상자&quot;라는 용어의 번역이 다음 언어의 모든 Digital Experience 제품에서 일치합니다.

   * 독일어: Zielgruppe
   * 포르투갈어(브라질): público-alvo
   * 스페인어: público destinatario

  이러한 변경 사항은 다음 UI 및 설명서 릴리스를 통해 점진적으로 적용됩니다.


### 기타 변경 사항 {#fall-23-rn-other-changes}

* 이제 트랜잭션 메시징에서 쉼표로 구분된 여러 선호도를 사용할 수 있습니다. [자세히 알아보기](../../sending/using/managing-typologies.md)

### 수정 사항 {#fall-23-rn-fixes}

* 대규모 워크플로를 사용할 때 성능 문제를 초래할 수 있는 회귀 문제를 해결했습니다. (CAMP-53369)
* 워크플로 이메일 경고 또는 알림의 링크가 작동하지 않는 문제를 해결했습니다. (CAMP-51874)

## 릴리스 23.1 - 2023년 봄/여름 릴리스 {#apr-23}

### 개선 사항 {#e-rn-improvements}

* 푸시 메시지 서비스의 지원을 개선하기 위해 서비스를 최신화했습니다. (CAMP-47959)
* SMS 메시지 서비스의 안정성을 개선했습니다. (CAMP-52217)
* Adobe는 애플리케이션의 전반적인 사용 편의성을 개선하기 위해 접근성 관련 여러 가지를 수정했습니다. 다음은 접근성 개선의 몇 가지 예시입니다.
   * 다양한 화면에서 인터페이스의 키보드 접근성을 최적화했습니다.
   * 터치 스크린 사용자의 애플리케이션 사용성을 개선했습니다.
   * 인터페이스 전반적으로 여러 항목의 색상을 변경하여 가시성을 높였습니다.

### 기타 변경 사항 {#e-rn-changes}

* 기본 제공 **보고 보강 만들기 워크플로**&#x200B;를 추가했습니다. 한 인스턴스에서 다른 인스턴스로 대상 매핑을 가져온 후 워크플로를 실행하기만 하면 해당 보고 보강 항목을 가져올 수 있습니다. (CAMP-52452)

### 해결한 문제{#e-rn-patches}

* **핫 클릭** 보고서를 표시할 때 시간 초과 오류가 발생할 수 있는 문제를 해결했습니다. (CAMP-51582)
* **Places** 서비스와의 통합을 사용할 수 없는 문제를 해결했습니다. (CAMP-51923)
* 워크플로 스케줄러가 제대로 작동하지 않는 문제를 해결했습니다. (CAMP-52003)
* 대량의 데이터가 있는 사용자 정의 동적 보고서의 PDF 버전을 볼 때 세부 분류가 표시되지 않는 문제를 해결했습니다. (CAMP-52178)
* 보고서에 액세스할 때 오류가 표시되는 문제를 해결했습니다. (CAMP-52500)
* **이 계정의 MTA 인스턴스 제한** SMS 커넥터 매개 변수를 SMS에만 적용하지 않고 전체 채널에 적용하는 문제를 해결했습니다. (CAMP-52640)
