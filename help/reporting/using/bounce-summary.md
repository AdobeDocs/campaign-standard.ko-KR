---
title: 이탈 요약
description: 즉시 사용할 수 있는 바운스 요약 보고서에서 전송된 캠페인의 상태와 오류가 발생했을 수 있는 경우에 대해 알아보십시오.
page-status-flag: never-activated
uuid: 90087311-4236-4df9-ae7d-4a15c00c70ab
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: reporting
content-type: reference
topic-tags: list-of-reports
discoiquuid: 5ae561b4-03cf-4541-87ff-47f1027d53b8
context-tags: bounceReport,main;campaignCirculationReport,main;programCirculationReport,main
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 8%

---


# 이탈 요약{#bounce-summary}

이 보고서에는 반송 자동 처리뿐만 아니라 게재 중에 발생한 전체 하드 및 소프트 오류에 대해 자세히 설명되어 있습니다.

![](assets/campaign_reports_bounces.png)

각 표는 요약 번호와 차트로 표시됩니다. 각각의 시각화 설정에 세부 정보가 표시되는 방식을 변경할 수 있습니다.

**5번 재 분할로** 인해 검역량이 가장 많은 5개 배달이 나열됩니다.

바운스 **이유** 테이블에는 각 전달에 대한 바운스를 발생시킨 오류 유형에 사용할 수 있는 데이터가 포함됩니다.

* **[!UICONTROL User unknown]**:배달을 잘못된 이메일 주소로 보낼 때 생성되는 오류 유형입니다.
* **[!UICONTROL Invalid domain]**:도메인이 잘못되었거나 더 이상 존재하지 않는 이메일 주소로 배달을 보낼 때 생성되는 오류 유형입니다.
* **[!UICONTROL Unreachable]**:도메인에 일시적으로 접근할 수 없는 등 메시지 배달 문자열에서 발생한 오류 유형입니다.
* **[!UICONTROL Account disabled]**:배달을 더 이상 존재하지 않는 이메일 주소로 보낼 때 생성되는 오류 유형입니다.
* **[!UICONTROL Mailbox full]**:받는 사람의 받은 편지함이 가득 찰 때 생성되는 오류 유형입니다. 이 오류가 생성되기 전에 메시지를 전달하려는 5번의 시도가 있습니다.
* **[!UICONTROL Not connected]**:받는 사람의 휴대 전화기가 꺼져 있거나 메시지가 전송되는 시간에 네트워크에 연결되지 않을 때 생성되는 오류 유형입니다.

   >[!NOTE]
   >
   >이 유형의 오류는 모바일 채널에서의 배달에만 적용됩니다.

* **[!UICONTROL Refused]**:ISP(인터넷 서비스 공급자)가 주소를 거부할 때 생성되는 오류 유형입니다. 예를 들어, 보안 규칙이 스팸 방지 소프트웨어에 의해 적용된 경우

도메인 **재파티션** 테이블은 받는 사람 도메인에 따라 배달 중에 발생하는 전체 문제를 표시합니다.
