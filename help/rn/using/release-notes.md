---
title: 최신 릴리스
description: 이 페이지에서는 최신 Campaign Standard 릴리스의 콘텐츠를 자세히 설명합니다
feature: Overview
role: User
level: Beginner
exl-id: e1f55a9b-be51-4f57-8719-fed7efc89113
source-git-commit: f9bd5901d68c09ba20d5d48d263f4818c2e1e86a
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 69%

---


# 최신 릴리스{#latest-release}

![컨트롤 패널](assets/do-not-localize/cp-icon.png) **새로운 컨트롤 패널 릴리스**. [자세히 알아보기](https://experienceleague.adobe.com/docs/control-panel/using/release-notes.html?lang=ko){target="_blank"}.

## 릴리스 23.1 - 2023년 봄/여름 릴리스 {#apr-23}

### 개선 사항 {#e-rn-improvements}

* 푸시 메시지 서비스는 지원을 개선하기 위해 현대화되었습니다. (CAMP-47959)
* 더 나은 안정성을 제공하기 위해 SMS 메시징 서비스가 개선되었습니다. (CAMP-52217)
* Adobe은 애플리케이션의 전반적인 사용 편의성을 개선하기 위해 많은 액세스 가능성을 수정했습니다. 다음은 액세스 가능성 개선 몇 가지 예입니다.
   * 인터페이스의 키보드 액세스 가능성은 많은 화면에서 최적화되었습니다.
   * 터치 스크린 사용자를 위해 애플리케이션이 향상되었습니다.
   * 인터페이스에서 여러 항목의 색상이 변경되어 가시성을 개선했습니다.

### 기타 변경 사항 {#e-rn-changes}

* 기본 제공 **보고 보강 만들기 워크플로우**&#x200B;를 추가했습니다. 한 인스턴스에서 다른 인스턴스로 대상 매핑을 가져온 후 워크플로우를 실행하기만 하면 해당 보고 보강 항목을 가져올 수 있습니다. (CAMP-52452)

### 해결된 문제{#e-rn-patches}

* **핫 클릭** 보고서를 표시할 때 시간 초과 오류가 발생할 수 있는 문제를 해결했습니다. (CAMP-51582)
* **Places** 서비스와의 통합을 사용할 수 없는 문제를 해결했습니다. (CAMP-51923)
* 워크플로우 스케줄러가 제대로 작동하지 않는 문제를 해결했습니다. (CAMP-52003)
* 대량의 데이터가 있는 사용자 정의 동적 보고서의 PDF 버전을 볼 때 세부 분류가 표시되지 않는 문제를 해결했습니다. (CAMP-52178)
* 보고서에 액세스할 때 오류가 표시되는 문제를 해결했습니다. (CAMP-52500)
* **이 계정의 MTA 인스턴스 제한** SMS 커넥터 매개 변수를 SMS에만 적용하지 않고 전체 채널에 적용하는 문제를 해결했습니다. (CAMP-52640)
