---
title: 이탈 요약
description: 바운스 요약 보고서를 통해, 전송된 캠페인의 상태와 발생할 수 있는 오류에 대해 알아보십시오.
audience: reporting
content-type: reference
topic-tags: list-of-reports
context-tags: bounceReport,main;campaignCirculationReport,main;programCirculationReport,main
feature: Reporting
role: Leader
level: Intermediate
exl-id: 03ea2f20-959c-497e-bd71-4e77132d712e
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 1%

---

# 이탈 요약{#bounce-summary}

이 보고서는 반송 자동 처리뿐만 아니라 게재 중에 발생한 전체 하드 및 소프트 오류에 대해 자세히 설명합니다(참조) [게재 실패 이해](../../sending/using/understanding-delivery-failures.md)).

![](assets/campaign_reports_bounces.png)

각 테이블은 요약 번호와 차트로 표시됩니다. 세부 사항이 각각의 시각화 설정에 표시되는 방식을 변경할 수 있습니다.

**플롭 5 재분할** 격리 수가 가장 많은 5개의 게재를 나열합니다.

다음 **바운스 원인** 테이블에는 각 게재에 대해 바운스를 초래한 오류 유형에 사용할 수 있는 데이터가 포함되어 있습니다.

* **[!UICONTROL User unknown]**: 잘못된 이메일 주소로 게재를 보낼 때 생성되는 오류 유형입니다.
* **[!UICONTROL Invalid domain]**: 도메인이 잘못되었거나 더 이상 존재하지 않는 이메일 주소로 게재를 보낼 때 생성되는 오류 유형입니다.
* **[!UICONTROL Unreachable]**: 일시적으로 연결할 수 없는 도메인 등, 메시지 게재 문자열에서 발생한 오류 유형입니다.
* **[!UICONTROL Account disabled]**: 더 이상 존재하지 않는 이메일 주소로 게재를 전송할 때 발생하는 오류 유형입니다.
* **[!UICONTROL Mailbox full]**: 수신자의 받은 편지함이 가득 찰 때 생성되는 오류 유형입니다. 이 오류가 생성되기 전에 메시지를 전달하려고 5번 시도합니다.
* **[!UICONTROL Not connected]**: 메시지를 전송할 때 수신자의 휴대폰이 꺼져 있거나 네트워크에 연결되어 있지 않은 경우 발생하는 오류 유형입니다.

  >[!NOTE]
  >
  >이 유형의 오류는 모바일 채널의 게재에만 관련이 있습니다.

* **[!UICONTROL Refused]**: 인터넷 서비스 공급자(ISP)가 주소를 거부하면 생성되는 오류 유형입니다. 예를 들어 보안 규칙이 스팸 방지 소프트웨어에 의해 적용된 경우.

다음 **도메인 재분할** 표에는 수신자 도메인에 따라 게재 중에 발생하는 전반적인 문제가 표시됩니다.
