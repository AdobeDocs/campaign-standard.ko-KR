---
title: 대기
description: 대기 활동은 워크플로우의 일부 실행을 일시적으로 중단합니다.
page-status-flag: 활성화 안 함
uuid: 396a3de1-6ffa-4385-ac9f-15fdeae5a366
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 자동화
content-type: reference
topic-tags: 실행 활동
discoiquuid: 377821e6-69f8-41cc-a1ad-8a2f5ed4d409
context-tags: wait,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 대기{#wait}

## 설명 {#description}

![](assets/wait.png)

워크플로우의 일부 실행이 일시적으로 **[!UICONTROL Wait]** 중단됩니다. 지연 후 몇 초에서 몇 달까지 길어질 수 있는 아웃바운드 전환을 활성화하며 이후에 배치된 활동을 실행합니다.

## 사용 상황 {#context-of-use}

이 **[!UICONTROL Wait]** 활동은 실행 중인 두 활동 사이에 일정한 시간이 경과하도록 허용하는 데 사용됩니다. 예를 들어 이메일 배달 활동 후 며칠 동안 기다리려면 이 기간 동안 생성된 열기 및 클릭 수를 분석하여 후속 작업(미리 알림 이메일, 대상자 만들기 등)을 수행합니다.

## 구성 {#configuration}

1. 워크플로우를 워크플로우로 드래그하여 **[!UICONTROL Wait]** 놓을 수 있습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 엽니다.
1. 활동의 인바운드 및 아웃바운드 전환 활성화 사이의 대기 **[!UICONTROL Duration]** 시간을 지정합니다.

   지속 시간을 수동으로 입력하거나 필드에 사용할 수 있는 선택기를 사용할 수 있습니다.

   ![](assets/wait_duration.png)

1. 활동 구성을 확인하고 워크플로우를 저장합니다.

## 예 {#example}

다음 예는 일반적인 사용 사례의 **[!UICONTROL Wait]** 활동을 보여줍니다. 이벤트에 대한 이메일 초대장이 전송됩니다. 전송 후 24시간 후에 이메일 배달 로그가 분석되고 첫 번째 이메일을 수신했지만 가입하지 않은 사람에게 알림 이메일이 전송됩니다.

워크플로우는 다음과 같이 표시됩니다.

![](assets/wait_example_workflow.png)

* 첫 번째 **[!UICONTROL Query]** 항목은 이메일 초대장을 보낼 프로필을 대상으로 합니다.
* 그러면 **[!UICONTROL Email delivery]** 선택한 프로필로 초대장이 처음 전송됩니다.
* 24h의 **[!UICONTROL Wait]** 활동은 초대장을 보낸 시간과 나머지 워크플로우 사이에 일시 중지됩니다.
* 두 번째 메일은 첫 번째 이메일을 수신했지만 구독 링크를 클릭하지 않은 프로필을 **[!UICONTROL Query]** 타깃팅합니다.
* 두 번째 **[!UICONTROL Email delivery]** 메시지는 선택한 사람들에게 초대장을 미리 보냅니다.

