---
title: 도메인별 분류
description: 도메인별 분류 기본 보고서를 사용하면 각 고객의 도메인에 따라 게재 성능 데이터에 대해 알 수 있습니다.
audience: reporting
content-type: reference
topic-tags: list-of-reports
context-tags: deliveryDomainBreakdownReport,main;campaignDomainBreakdownReport,main;programDomainBreakdownReport,main
feature: Reporting
role: Leader
level: Intermediate
exl-id: 513d74ae-10c0-4d41-a7d1-8ed655e1a2d1
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 3%

---

# 도메인별 분류{#breakdown-by-domains}

이 보고서에는 이메일 게재 대상자에 표시되는 각 도메인에 대한 성능 데이터가 포함되어 있습니다. 캠페인 또는 프로그램 보고서인 경우 성능 데이터를 여러 대상에 사용할 수 있습니다. 이 데이터를 사용하면 특정 이벤트에 대한 응답으로 각 도메인의 동작을 분석할 수 있습니다. 예를 들어, 링크 표시,의 URL 차단 목록 등이 있습니다.

![](assets/delivery_reports_6.png)

테이블 **브로드캐스트 통계** 에는 다음과 같이 각 도메인에서 발생한 가능한 오류에 사용할 수 있는 데이터가 포함되어 있습니다.

* **처리/전송**: 보낸 이메일 수입니다.
* **배달됨**: 배달된 이메일 수입니다.
* **바운스 수 + 오류**: 배달할 수 없는 메시지 수입니다.
* **하드 바운스**: 잘못된 이메일 주소와 같은 총 영구 오류 수입니다.
* **소프트 바운스**: 전체 받은 편지함과 같은 총 임시 오류 수입니다.

두 번째 테이블 **통계 추적**&#x200B;에는 다음과 같이 수신자가 게재하기 위해 재활동을 수행할 수 있는 데이터가 포함되어 있습니다.

* **배달됨**: 배달된 이메일 수
* **열기**: 게재에서 메시지를 연 횟수입니다.
* **클릭**: 게재에서 콘텐츠를 클릭한 횟수입니다.
* **가입 해지됨**: 구독 링크에 대한 클릭 수입니다.
* **미러 페이지**: 미러 페이지 링크에 대한 클릭 수입니다.
* **차단 목록**: 이메일을 스팸 또는 정크 메일로 선언한 받는 사람 수입니다. [자세히 알아보기](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md)
