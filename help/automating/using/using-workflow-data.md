---
title: 워크플로우 데이터 사용
description: 가져오거나 타게팅한 데이터를 사용할 수 있는 다양한 가능성을 살펴볼 수 있습니다.
page-status-flag: 활성화 안 함
uuid: 3dd66aeb-3a26-4214-b6a0-242c2b7fbc49
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 자동화
content-type: reference
topic-tags: workflow-general-operation
discoiquuid: 90b250f1-f32d-4256-83ea-4c0627628610
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 워크플로우 데이터 사용{#using-workflow-data}

데이터가 식별되고 준비되면 다음 컨텍스트에서 사용할 수 있습니다.

* 이 **[!UICONTROL Update data]** 활동을 통해 데이터베이스의 필드에 대한 대량 업데이트를 수행할 수 있습니다.
* 이 **[!UICONTROL Save audience]** 활동을 사용하면 기존 대상을 업데이트하거나 워크플로에서 업스트림 계산된 모집단에서 새 대상자를 만들 수 있습니다. 이 활동에서 만들거나 업데이트한 대상은 **목록** 또는 파일 **대상입니다** . 또한 이 활동을 통해 프로파일을 Adobe Experience Cloud 대상/세그먼트로 내보낼 수 있습니다.
* 이 **[!UICONTROL Subscription Services]** 활동을 통해 프로파일을 대량으로 가져와 서비스에 가입하거나 서비스에서 가입을 해지할 수 있습니다.
* 이 **[!UICONTROL Extract file]** 활동을 통해 외부 파일 형식으로 Adobe Campaign의 데이터를 내보낼 수 있습니다.

프로필 대상을 정의한 후, 여러 활동을 사용하여 배달을 만들고 전송할 수 있습니다.

* 이 **[!UICONTROL Email delivery]** 활동을 통해 워크플로우에서 이메일 전송을 구성할 수 있습니다. 이 이메일은 **한 번의** 전송으로 한 번만 전송되거나 **반복되는** 이메일이 될 수 있습니다.
* 이 **[!UICONTROL SMS delivery]** 활동을 통해 워크플로우에서 SMS 전송을 구성할 수 있습니다. SMS를 **한 번만 전송하거나** 반복되는 **SMS가 될 수 있습니다** .
* 이 **[!UICONTROL Mobile app delivery]** 활동을 통해 워크플로우에서 푸시 알림 전송을 구성할 수 있습니다. 이는 **단일 전송** 알림일 수 있으며 한 번만 전송되거나 **반복되는** 알림일 수 있습니다.

