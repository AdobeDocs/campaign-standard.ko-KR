---
solution: Campaign Standard
product: campaign
title: 메시지 보내기 주요 단계
description: Adobe Campaign으로 메시지를 만들고 전송하기 위해 따라야 하는 단계입니다.
audience: channels
content-type: reference
topic-tags: about-communication-channels
feature: 개요
role: 비즈니스 전문가
level: 초급
translation-type: tm+mt
source-git-commit: a7a1aa2841410674597264927325c073fef4ce26
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 12%

---


# 메시지 보내기 주요 단계{#key-steps-to-send-a-message}

이 섹션에서는 Adobe Campaign Standard을 사용하여 개인화된 메시지를 만들고 타깃팅된 대상자에게 보내는 방법을 알아봅니다.

각 통신 채널을 만들고 구성하는 방법에 대한 특정 정보는 다음 섹션에서 사용할 수 있습니다.

* [이메일 만들기](../../channels/using/creating-an-email.md)
* [SMS 만들기](../../channels/using/creating-an-sms-message.md)
* [DM 게재 만들기](../../channels/using/creating-the-direct-mail.md)
* [푸시 알림](../../channels/using/preparing-and-sending-a-push-notification.md) 만들기.
* [인앱 메시지 준비 및 보내기](../../channels/using/preparing-and-sending-an-in-app-message.md)

배달 우수 사례에 대해 알아보려면 [배달 우수 사례](../../sending/using/delivery-best-practices.md) 섹션을 참조하십시오.

## 메시지 만들기

Campaign Standard [마케팅 활동](../../start/using/marketing-activities.md)을 활용하여 이메일, SMS, DM, 푸시 알림 또는 인앱 메시지를 만듭니다.

![](assets/marketing-activities.png)

메시지는 마케팅 활동 목록 또는 [전용 활동](../../automating/using/about-channel-activities.md)을 사용하는 워크플로우에서 만들 수 있습니다.

![](assets/steps-channel.png)

## 대상 정의

메시지 받는 사람을 정의합니다. 이렇게 하려면 왼쪽 창에서 [쿼리 편집기](../../automating/using/editing-queries.md)를 사용하여 데이터베이스에 포함된 데이터를 필터링하고 대상을 대상으로 하는 규칙을 만듭니다.

사용할 수 있는 대상 유형은 다음과 같습니다.

* **[!UICONTROL Target]** 는 이메일의 주요 대상이며
* **[!UICONTROL Test profiles]** 은 이메일을 테스트하고 확인하는 데 사용되는 프로필입니다(테스트 프로필  [관리](../../audiences/using/managing-test-profiles.md) 참조).

![](assets/steps-audience.png)

## 컨텐츠 디자인 및 개인화

**[!UICONTROL Content]** 블록에서 데이터베이스의 필드를 사용하여 메시지 내용을 디자인하고 개인화합니다. 특정 채널의 컨텐츠를 디자인하는 방법에 대한 자세한 내용은 이 페이지 맨 위에 있는 섹션을 참조하십시오.

![](assets/steps-content.png)

## 준비 및 테스트

[메시지](../../sending/using/preparing-the-send.md) 를 준비합니다. 이 프로세스는 목표 인구를 계산하고 개인화된 메시지를 준비합니다.

![](assets/steps-prepare.png)

**Campaign Standard 기능을 사용하여 메시지를** 보내기 전에 메시지를 확인하고 테스트합니다.미리 보기, 이메일 렌더링, 언어 교정 등 이 작업에 대한 자세한 정보는 [이 섹션](../../sending/using/previewing-messages.md)을 참조하십시오.

**[!UICONTROL Schedule]** 블록을 사용하여 메시지가 전송될 시기를 정의합니다([메시지 예약](../../sending/using/about-scheduling-messages.md) 참조).

![](assets/steps-schedule.png)

## 보내기 및 추적

메시지가 준비되면 전송을 확인할 수 있습니다. **[!UICONTROL Deployment]** 블록에 전송 진행 상황과 결과가 표시됩니다.

![](assets/steps-send.png)

메시지 배달을 모니터링하는 데 도움이 되는 여러 로그를 사용할 수 있습니다( [배달](../../sending/using/monitoring-a-delivery.md) 모니터링 참조). 또한 Campaign Standard의 [추적 기능](../../sending/using/tracking-messages.md) 덕분에 배달 받는 사람의 동작을 추적할 수도 있습니다.

![](../../sending/using/assets/tracking_logs.png)

다양한 지표와 차트를 통해 메시지의 효과와 센드 및 캠페인의 진화를 측정할 수 있습니다([보고서 액세스](../../reporting/using/about-dynamic-reports.md) 참조).

![](assets/steps-reports.png)
