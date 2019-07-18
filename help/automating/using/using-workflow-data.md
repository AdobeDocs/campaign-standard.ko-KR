---
title: 워크플로우 데이터 사용
seo-title: 워크플로우 데이터 사용
description: 워크플로우 데이터 사용
seo-description: 가져오거나 타깃팅한 데이터를 소비할 수 있는 다양한 가능성을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: 3 dd 66 AEB -3 A 26-4214-B 6 A 0-242 C 2 B 7 FBC 49
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: workflow-general-operation
discoiquuid: 90 B 250 F 1-F 32 D -4256-83 EA -4 C 0627628610
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Using workflow data{#using-workflow-data}

데이터가 식별되고 준비되면 다음 컨텍스트에서 사용할 수 있습니다.

* **[!UICONTROL Update data]** 활동을 통해 데이터베이스의 필드에 대해 대량 업데이트를 수행할 수 있습니다.
* **[!UICONTROL Save audience]** 활동을 사용하면 기존 대상을 업데이트하거나 워크플로우의 계산된 업스트림 목록에서 새 대상을 만들 수 있습니다. The audiences created or updated from this activity are **List** or **File** audiences. 이 활동을 통해 프로파일을 Adobe Experience Cloud 대상/세그먼트로 내보낼 수도 있습니다.
* **[!UICONTROL Subscription Services]** 활동을 통해 일괄적으로 프로필을 가져와 서비스에 구독하거나 서비스에서 가입을 해지할 수 있습니다.
* **[!UICONTROL Extract file]** 활동을 통해 Adobe Campaign의 데이터를 외부 파일 양식으로 내보낼 수 있습니다.

프로필 타겟을 정의한 후 몇 가지 활동을 사용하여 배달을 만들고 보낼 수 있습니다.

* **[!UICONTROL Email delivery]** 활동을 통해 워크플로우에서 이메일을 보내도록 구성할 수 있습니다. This can be a **single send** email and sent just once, or it can be a **recurring** email.
* **[!UICONTROL SMS delivery]** 활동을 통해 워크플로우에서 SMS 전송을 구성할 수 있습니다. This can be a **single send** SMS and sent just once, or it can be a **recurring** SMS.
* **[!UICONTROL Mobile app delivery]** 활동을 통해 워크플로우에서 푸시 알림 전송을 구성할 수 있습니다. This can be a **single send** notification and sent just once, or it can be a **recurring** notification.

