---
title: 도메인별 분류
description: 기본적으로 제공되는 도메인별 분류 보고서를 사용하면 각 고객의 도메인에 따라 배달된 성능 데이터에 대해 알 수 있습니다.
page-status-flag: never-activated
uuid: 75a64c81-325b-422f-b6ef-deb06eec7f7b
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: reporting
content-type: reference
topic-tags: list-of-reports
discoiquuid: 2ce174f9-5d7d-48b9-9235-6bf3e238ff37
context-tags: deliveryDomainBreakdownReport,main;campaignDomainBreakdownReport,main;programDomainBreakdownReport,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 1f15e28bed22e3defb29f16875fcf4c07f4af5a3
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 3%

---


# 도메인별 분류{#breakdown-by-domains}

이 보고서에는 대상이 이메일 배달을 위해 나타내는 각 도메인에 대한 성능 데이터가 포함됩니다. 캠페인 또는 프로그램 보고서인 경우 성능 데이터를 여러 대상에 사용할 수 있습니다. 이 데이터를 사용하면 특정 이벤트에 대한 반응으로 각 도메인의 동작을 분석할 수 있습니다. 예를 들어 링크 표시, 차단 목록에 추가된 URL 등이 있습니다.

![](assets/delivery_reports_6.png)

브로드캐스트 **통계** 테이블에는 다음과 같이 각 도메인에서 발생하는 오류에 대해 사용 가능한 데이터가 포함됩니다.

* **처리/전송**:보낸 이메일 수입니다.
* **배달됨**:배달된 이메일 수입니다.
* **바운스 수 + 오류**:배달할 수 없는 메시지 수입니다.
* **하드 바운스**:잘못된 이메일 주소와 같은 총 영구 오류 수입니다.
* **소프트 바운스**:전체 받은 편지함과 같은 총 임시 오류 수입니다.

두 번째 테이블인 **추적 통계에는**&#x200B;받는 사람이 배달할 재작업에 사용할 수 있는 다음과 같은 데이터가 포함됩니다.

* **배달됨**:배달된 이메일 수
* **열기**:배달에서 메시지를 연 횟수입니다.
* **다음을 클릭합니다**.게재에서 컨텐츠를 클릭한 횟수입니다.
* **구독 취소**:구독 링크에 대한 클릭 수입니다.
* **미러 페이지**:미러 페이지 링크에 대한 클릭 수입니다.
* **차단 목록에 추가된**:이메일을 스팸 또는 정크 메일로 선언한 받는 사람 수입니다. [자세히 알아보기](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md)

