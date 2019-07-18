---
title: wait
seo-title: wait
description: wait
seo-description: 대기 활동은 워크플로우에서 일시적으로 일시 중단됩니다.
page-status-flag: 정품 인증 안 함
uuid: 396 a 3 de 1-6 ffa -4385-ac 9 f -15 fdeae 5 a 366
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 실행 활동
discoiquuid: 377821 E 6-69 F 8-41 CC-A 1 AD -8 A 2 F 5 ED 4 D 409
context-tags: Wait, Main
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: e384a0cef325bc01eb5ea050b0f3d926aea9a88f

---


# Wait{#wait}

## Description {#description}

![](assets/wait.png)

**[!UICONTROL Wait]** 워크플로우는 워크플로우에서 일시적으로 일시 중단됩니다. 몇 초에서 몇 개월 사이의 지연 후에 아웃바운드 전환을 활성화합니다. 이 경우 이후에 배치된 활동이 실행됩니다.

## Context of use {#context-of-use}

**[!UICONTROL Wait]** 활동은 실행되는 두 활동 간에 특정 시간을 통과시키는 데 사용됩니다. 예를 들어 이메일 배달 활동 후 며칠 후에 기다렸다가 후속 작업 (미리 알림 이메일, 대상자 만들기 등) 를 수행하기 전에 이 기간 동안 생성된 열기 및 클릭을 분석하십시오.

## Configuration {#configuration}

1. **[!UICONTROL Wait]** 워크플로우를 워크플로우로 드래그하여 놓습니다.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. Specify the **[!UICONTROL Duration]** of the wait between when the inbound and outbound transitions of the activity are activated.

   수동으로 기간을 입력하거나 필드에서 사용할 수 있는 선택기를 사용할 수 있습니다.

   ![](assets/wait_duration.png)

1. 활동의 구성을 확인하고 워크플로우를 저장합니다.

## Example {#example}

The following example illustrates the **[!UICONTROL Wait]** activity in a typical use case. 이벤트에 대한 이메일 초대장이 전송됩니다. 전송 후 24 시간 후에 이메일 배달 로그가 분석되고 첫 번째 이메일을 받은 사람에게 알림 이메일이 전송되지만 등록하지 않았습니다.

워크플로우는 다음과 같이 표시됩니다.

![](assets/wait_example_workflow.png)

* A first **[!UICONTROL Query]** targets the profiles that will be sent the email invitation.
* An **[!UICONTROL Email delivery]** sends the invitation for the first time to the profiles selected.
* **[!UICONTROL Wait]** 24 H의 활동은 초대장을 보낼 때와 나머지 워크플로우 사이에 일시 중지를 가져옵니다.
* A second **[!UICONTROL Query]** targets the profiles that received the first email but did not click on the subscription link inside.
* A second **[!UICONTROL Email delivery]** sends a reminder of the invitation to the people selected.

