---
title: 바운스 요약
seo-title: 바운스 요약
description: 바운스 요약
seo-description: 바운스 요약 보고서를 사용하면 전송된 캠페인과 오류의 상태에 대해 알 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 90087311-4236-4 DF 9-AE 7 D -4 A 15 C 00 C 70 AB
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 보고
content-type: 참조
topic-tags: list-of-reports
discoiquuid: 5 AE 561 B 4-03 CF -4541-87 FF -47 F 1027 D 53 B 8
context-tags: Bouncereport, Main; Campaigncirculationreport, main; Programcirculationreport, main
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 77b0933bcd004cedc6a58f80717a4284b284e0cd

---


# Bounce summary{#bounce-summary}

이 보고서는 배달하는 동안 발생한 전반적인 하드 및 소프트 오류와 바운스 자동 처리를 자세히 설명합니다.

![](assets/campaign_reports_bounces.png)

각 표는 요약 번호와 차트로 표시됩니다. 각 시각화 설정에 세부 사항이 표시되는 방식을 변경할 수 있습니다.

**Flop 5 재파티션에** 가장 많은 수의 쿼리로 5 개 배달이 나열됩니다.

**바운스 이유** 표에는 각 배달에 대한 바운스 원인이 되는 오류 유형에 사용할 수 있는 데이터가 포함되어 있습니다.

* **[!UICONTROL User unknown]**: 배달이 잘못된 이메일 주소로 전송될 때 생성되는 오류 유형입니다.
* **[!UICONTROL Invalid domain]**: 도메인이 잘못되었거나 더 이상 존재하지 않는 이메일 주소로 배달될 때 생성되는 오류 유형입니다.
* **[!UICONTROL Unreachable]**: 메시지 배달 문자열에서 발생한 오류 유형입니다. 예를 들어 SMTP 릴레이 사고, 일시적으로 연결할 수 없는 도메인 등이 있습니다.
* **[!UICONTROL Account disabled]**: 더 이상 존재하지 않는 이메일 주소로 배달을 전송할 때 생성되는 오류 유형입니다.
* **[!UICONTROL Mailbox full]**: 수신자의 받은 편지함이 꽉 찰 때 생성되는 오류 유형입니다. 이 오류가 발생하기 전에 메시지를 전달하려는 시도가 5 개 있습니다.
* **[!UICONTROL Not connected]**: 수신자의 휴대 전화기가 꺼져 있거나 메시지가 전송될 때 네트워크에 연결되지 않은 경우 생성되는 오류 유형입니다.

   >[!NOTE]
   >
   >이러한 유형의 오류는 모바일 채널을 통한 전달에만 국한됩니다.

* **[!UICONTROL Refused]**: ISP (Internet Service Provider) 에서 주소를 거부할 때 생성되는 오류 유형입니다. 예를 들어 스팸 소프트웨어가 보안 규칙을 적용한 경우

**도메인 재파티션** 테이블은 수신자 도메인에 따라 배달하는 동안 발생한 전반적인 문제를 표시합니다.
