---
title: 내부 알림 보내기
description: Adobe Campaign 사용자에게 실시간 시스템 알림을 보내는 방법 알아보기
audience: administration
role: Admin
level: Experienced
exl-id: 7e04275a-5413-4f03-b18c-b64ab482d7d5
source-git-commit: bfba6b156d020e8d2656239e713d2d24625bda54
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 2%

---

# 내부 알림 보내기{#sending-internal-notifications}

Adobe Campaign에서는 중요한 시스템 활동에 대한 알림을 애플리케이션 내에서 직접 받을 수 있습니다. 실시간 알림은 관련 이해 당사자에게 정보를 제공하고 애플리케이션 내에서 활동 알림에 대해 즉각적이고 직접적으로 작업할 수 있는 기능을 사용자에게 제공합니다. 팀의 결과는 캠페인의 고급 민첩성, 효율성 및 더 원활한 실행입니다.

![](assets/pulse_3.png)

다음 객체에 대한 알림을 구성할 수 있습니다.

* **[!UICONTROL A/B Test emails]**: 이메일 생성자 및 수정자에게 변형이 선택되었음(자동 모드) 또는 변형을 선택해야 한다는 알림(수동 모드)이 표시됩니다. 알림을 클릭하면 해당 이메일이 표시됩니다. 알림은 기본적으로 기본 제공 A/B 테스트 템플릿에서 활성화됩니다. 비활성화하려면 이메일 또는 이메일 템플릿의 속성을 편집하고 아래에 있는 상자를 선택 취소합니다 **일반 > 알림**. A/B 테스트 이메일에 대한 자세한 내용은 다음을 참조하십시오. [AB 테스트 만들기](../../channels/using/designing-an-a-b-test-email.md). 이메일 속성에 대한 자세한 내용은 [이메일 속성 목록](../../administration/using/configuring-email-channel.md#list-of-email-properties).

  ![](assets/pulse_2.png)

* **[!UICONTROL Workflows]**: 워크플로우가 오류일 때마다 선택한 보안 그룹의 각 구성원에게 알림(이메일 및 인앱 알림)이 표시됩니다. 알림 또는 이메일 링크를 클릭하면 해당 워크플로우가 표시됩니다. 알림은 기본적으로 기본 워크플로우 템플릿에서 비활성화됩니다. 이를 활성화하려면 워크플로 또는 워크플로 템플릿의 속성을 편집하고 아래에 보안 그룹을 추가합니다. **일반 > 실행 > 오류 관리 > 감독자**. 보안 그룹에 대한 자세한 내용은 [그룹 및 사용자 관리](../../administration/using/managing-groups-and-users.md). 워크플로우 속성에 대한 자세한 내용은 다음을 참조하십시오. [워크플로우 속성](../../automating/using/managing-execution-options.md).

  ![](assets/pulse_1.png)
