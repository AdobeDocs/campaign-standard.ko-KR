---
solution: Campaign Standard
product: campaign
title: 내부 알림 보내기
description: Adobe Campaign 사용자에게 실시간 시스템 알림을 보내는 방법에 대해 알아보십시오.
audience: administration
content-type: reference
topic-tags: application-settings
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 2%

---


# 내부 알림 보내기{#sending-internal-notifications}

Adobe Campaign은 애플리케이션에서 바로 중요한 시스템 활동에 대한 알림을 받을 수 있는 기능을 제공합니다. 실시간 알림은 관련 이해 관계자에게 정보를 알리고 사용자에게 애플리케이션 내에서 활동 알림에 즉시 대응할 수 있는 기능을 제공합니다. 그 결과 민첩성, 효율성 및 원활한 캠페인 실행이 입증되었습니다.

![](assets/pulse_3.png)

다음 개체에 대한 알림을 구성할 수 있습니다.

* **[!UICONTROL A/B Test emails]**:이메일 생성자 및 수정자에 변형이 선택되었거나(자동 모드) 변형을 선택해야 한다는 메시지가 표시됩니다(수동 모드). 알림을 클릭하면 해당 이메일이 표시됩니다. 기본 A/B 테스트 템플릿에서 기본적으로 알림이 활성화됩니다. 비활성화하려면 이메일 또는 이메일 템플릿의 속성을 편집하고 **일반 > 알림**&#x200B;에 있는 상자의 선택을 취소합니다. A/B 테스트 이메일에 대한 자세한 내용은 [AB 테스트 만들기](../../channels/using/designing-an-a-b-test-email.md)를 참조하십시오. 이메일 속성에 대한 자세한 내용은 [이메일 속성 목록](../../administration/using/configuring-email-channel.md#list-of-email-properties)을 참조하십시오.

   ![](assets/pulse_2.png)

* **[!UICONTROL Workflows]**:워크플로우에 오류가 발생할 때마다 선택한 보안 그룹의 각 구성원에게 알림(전자 메일 및 인앱 알림)이 표시됩니다. 알림 또는 이메일 링크를 클릭하면 해당 워크플로우가 표시됩니다. 기본 워크플로 템플릿에서는 기본적으로 알림이 비활성화됩니다. 활성화하려는 경우 워크플로우 또는 워크플로우 템플릿의 속성을 편집하고 **일반 > 실행 > 오류 관리 > 감독자**&#x200B;에서 보안 그룹을 추가합니다. 보안 그룹에 대한 자세한 내용은 [그룹 및 사용자 관리](../../administration/using/managing-groups-and-users.md)를 참조하십시오. 워크플로 속성에 대한 자세한 내용은 [워크플로 속성](../../automating/using/managing-execution-options.md)을 참조하십시오.

   ![](assets/pulse_1.png)
