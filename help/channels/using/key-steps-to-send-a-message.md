---
title: 메시지 보내기 주요 단계
description: Adobe Campaign으로 메시지를 만들고 전송하기 위해 따라야 하는 단계입니다.
audience: channels
content-type: reference
topic-tags: about-communication-channels
feature: Overview
role: User
level: Beginner
exl-id: a903d7e2-7654-46b3-bc61-4653a065faad
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 14%

---

# 메시지를 보내는 주요 단계{#key-steps-to-send-a-message}

이 섹션에서는 Adobe Campaign Standard을 사용하여 타겟팅된 대상자에게 개인화된 메시지를 만들고 전송하는 방법을 알아봅니다.

각 통신 채널을 만들고 구성하는 방법에 대한 특정 정보는 다음 섹션에서 확인할 수 있습니다.

* [이메일 만들기](../../channels/using/creating-an-email.md)
* [SMS 만들기](../../channels/using/creating-an-sms-message.md)
* [DM 게재 만들기](../../channels/using/creating-the-direct-mail.md)
* [푸시 알림 만들기](../../channels/using/preparing-and-sending-a-push-notification.md).
* [인앱 메시지 준비 및 보내기](../../channels/using/preparing-and-sending-an-in-app-message.md)

게재 모범 사례에 대해 알아보려면 [게재 우수 사례](../../sending/using/delivery-best-practices.md) 섹션을 참조하십시오.

## 메시지 만들기

Campaign Standard [마케팅 활동](../../start/using/marketing-activities.md)을 활용하여 이메일, SMS, DM, 푸시 알림 또는 인앱 메시지를 만듭니다.

![](assets/marketing-activities.png)

마케팅 활동 목록 또는 [전용 활동](../../automating/using/about-channel-activities.md)을 사용하는 워크플로우에서 메시지를 만들 수 있습니다.

![](assets/steps-channel.png)

## 대상자 정의

메시지의 수신자를 정의합니다. 이렇게 하려면 왼쪽 창의 [쿼리 편집기](../../automating/using/editing-queries.md)를 사용하여 데이터베이스에 포함된 데이터를 필터링하고 규칙을 만들어 대상을 타깃팅하십시오.

사용할 수 있는 대상의 유형은 다음과 같습니다.

* **[!UICONTROL Target]** 이메일의 주요 타겟이고
* **[!UICONTROL Test profiles]** 은 이메일을 테스트하고 유효성을 검사하는 데 사용되는 프로필입니다( [테스트 프로필 관리](../../audiences/using/managing-test-profiles.md) 참조).

![](assets/steps-audience.png)

## 콘텐츠 디자인 및 개인화

**[!UICONTROL Content]** 블록에서 데이터베이스의 필드를 사용하여 메시지 콘텐츠를 디자인하고 개인화합니다. 특정 채널에 대한 컨텐츠를 디자인하는 방법에 대한 자세한 내용은 이 페이지의 상단에 나열된 섹션을 참조하십시오.

![](assets/steps-content.png)

## 준비 및 테스트

[](../../sending/using/preparing-the-send.md) 메시지를 준비합니다. 이 프로세스는 대상 모집단을 계산하고 개인화된 메시지를 준비합니다.

![](assets/steps-prepare.png)

**Campaign Standard 기능을 사용하여 메시지를** 보내기 전에 메시지를 확인하고 테스트합니다. 미리 보기, 전자 메일 렌더링, 교정 등 이 작업에 대한 자세한 정보는 [이 섹션](../../sending/using/previewing-messages.md)을 참조하십시오.

메시지를 보낼 시점을 정의하려면 **[!UICONTROL Schedule]** 블록을 사용합니다( [메시지 예약](../../sending/using/about-scheduling-messages.md) 참조).

![](assets/steps-schedule.png)

## 보내기 및 추적

메시지가 준비되면 전송을 확인할 수 있습니다. **[!UICONTROL Deployment]** 블록에 전송 진행 상황과 결과가 표시됩니다.

![](assets/steps-send.png)

메시지 전달을 모니터링하는 데 도움이 되는 몇 가지 로그를 사용할 수 있습니다( [게재](../../sending/using/monitoring-a-delivery.md) 모니터링 참조). Campaign Standard의 [추적 기능](../../sending/using/tracking-messages.md) 덕분에 게재 수신자의 동작을 추적할 수도 있습니다.

![](../../sending/using/assets/tracking_logs.png)

다양한 지표 및 차트를 통해 메시지의 효율성과 보내기 및 캠페인의 진화를 측정합니다( [보고서 액세스](../../reporting/using/about-dynamic-reports.md) 참조).

![](assets/steps-reports.png)
