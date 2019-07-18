---
title: 내부 알림 전송
seo-title: 내부 알림 전송
description: 내부 알림 전송
seo-description: Adobe Campaign 사용자에게 실시간 시스템 알림을 보내는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: F 196 F 025-DBB 9-4268-9 D 7 D-FF 626994 B 447
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 관리
content-type: 참조
topic-tags: application-settings
discoiquuid: 4 D 51229 A -745 A -4 F 24-B 1 C 2-22 FA 203 B 499 C
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 6a877d878f01fa1e541dc20b8b0941602113d15b

---


# Sending internal notifications{#sending-internal-notifications}

Adobe Campaign 에서는 애플리케이션 내에서 바로 중요한 시스템 활동에 대한 알림을 받을 수 있습니다. 실시간 알림은 관련 이해 관계자가 정보를 알리고 애플리케이션 내에서 활동 알림을 즉시 실행할 수 있는 기능을 사용자에게 제공합니다. 이러한 결과를 통해 민첩성, 효율성 및 캠페인을 보다 원활하게 실행할 수 있습니다.

![](assets/pulse_3.png)

다음 개체에 대한 알림을 구성할 수 있습니다.

* **[!UICONTROL A/B Test emails]**: 이메일 작성자와 수정자에게 변형을 선택했거나 (자동 모드) 변형을 선택해야 한다는 메시지가 표시됩니다 (수동 모드). 알림을 클릭하면 해당 이메일이 표시됩니다. 알림은 기본적으로 제공되는 A/B 테스트 템플릿에서 활성화됩니다. If you want to deactivate them, edit the properties of the email or the email template and uncheck the box located under **General &gt; Notifications**. For more information on A/B Test emails, refer to [Creating an AB Test](../../channels/using/designing-an-a-b-test-email.md). For more on email properties, refer to [List of email properties](../../administration/using/configuring-email-channel.md#list-of-email-properties).

   ![](assets/pulse_2.png)

* **[!UICONTROL Workflows]**: 워크플로우가 오류이면 선택한 보안 그룹의 각 구성원이 알림 (이메일 및 인앱 알림) 됩니다. 알림 또는 이메일 링크를 클릭하면 해당 워크플로우가 표시됩니다. 기본적으로 즉시 사용 가능한 워크플로우 템플릿에서 알림이 비활성화됩니다. If you want to activate them, edit the properties of the workflow or workflow template and add a security group under **General &gt; Execution &gt; Error management &gt; Supervisors**. For more information on security groups, refer to [Managing groups and users](../../administration/using/managing-groups-and-users.md). For more on workflow properties, refer to [Workflow properties](../../automating/using/executing-a-workflow.md#workflow-properties).

   ![](assets/pulse_1.png)

