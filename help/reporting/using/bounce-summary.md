---
title: 이탈 요약
description: 즉시 사용 가능한 바운스 요약 보고서를 사용하여 전송된 캠페인의 상태와 오류가 발생했을 수 있는 오류에 대해 알아봅니다.
page-status-flag: 활성화 안 함
uuid: 90087311-4236-4df9-ae7d-4a15c00c70ab
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 보고
content-type: reference
topic-tags: 보고서 목록
discoiquuid: 5ae561b4-03cf-4541-87ff-47f1027d53b8
context-tags: bounceReport,main;campaignDistributionReport,main;programDistributionReport,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 이탈 요약{#bounce-summary}

이 보고서는 바운스 자동 처리와 배달 중에 발생한 전체 하드 및 소프트 오류에 대해 자세히 설명합니다.

![](assets/campaign_reports_bounces.png)

각 표는 요약 번호와 차트로 표시됩니다. 각 시각화 설정에 세부 정보가 표시되는 방식을 변경할 수 있습니다.

**5번 재 분할은** 격리조치가 가장 많은 5개의 운송물을 나열합니다.

바운스 **이유** 테이블에는 각 전달에 대한 바운스를 발생시킨 오류 유형에 사용할 수 있는 데이터가 포함됩니다.

* **[!UICONTROL User unknown]**:배달을 잘못된 이메일 주소로 보낼 때 생성되는 오류 유형입니다.
* **[!UICONTROL Invalid domain]**:도메인이 잘못되었거나 더 이상 존재하지 않는 이메일 주소로 배달을 보낼 때 생성되는 오류 유형입니다.
* **[!UICONTROL Unreachable]**:메시지 배달 문자열에서 발생한 오류 유형입니다. 예를 들어 SMTP 릴레이 장애, 도메인에 일시적으로 접근할 수 없음 등이 있습니다.
* **[!UICONTROL Account disabled]**:배달이 더 이상 존재하지 않는 이메일 주소로 전송될 때 생성되는 오류 유형입니다.
* **[!UICONTROL Mailbox full]**:받는 사람의 받은 편지함이 가득 찰 때 생성되는 오류 유형입니다. 이 오류가 생성되기 전에 메시지를 전달하려고 5번 시도합니다.
* **[!UICONTROL Not connected]**:받는 사람의 휴대 전화기가 꺼져 있거나 메시지가 전송될 때 네트워크에 연결되지 않은 경우 생성되는 오류 유형입니다.

   >[!NOTE]
   >
   >이러한 유형의 오류는 모바일 채널의 전달에만 해당됩니다.

* **[!UICONTROL Refused]**:ISP(인터넷 서비스 공급자)가 주소를 거부할 때 생성되는 오류 유형입니다. 예를 들어, 스팸 방지 소프트웨어에서 보안 규칙을 적용한 경우

도메인 **다시 파티션** 테이블은 받는 사람 도메인에 따라 배달 중에 발생하는 전체 문제를 표시합니다.
