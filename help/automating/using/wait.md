---
solution: Campaign Standard
product: campaign
title: 대기
description: 대기 활동은 워크플로우 특정 부분의 실행을 잠시 미룹니다.
audience: automating
content-type: reference
topic-tags: execution-activities
context-tags: wait,main
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 100%

---


# 대기{#wait}

## 설명 {#description}

![](assets/wait.png)

**[!UICONTROL Wait]** 활동은 워크플로우 특정 부분의 실행을 잠시 미룹니다. 몇 초에서 몇 달까지 대기한 후 아웃바운드 전환을 활성화하여 그 다음으로 배치한 활동을 실행합니다.

## 사용의 컨텍스트 {#context-of-use}

**[!UICONTROL Wait]** 활동은 실행할 두 활동 사이에 일정 시간이 지나도록 하는 데 사용됩니다. 예를 들어 이메일 게재 활동 후 며칠 동안 대기하고, 후속 작업(리마인더 이메일, 대상자 만들기 등)을 수행하기 전에 대기 기간 동안 발생한 오픈 및 클릭을 분석하려 할 때 사용할 수 있습니다.

## 구성 {#configuration}

1. **[!UICONTROL Wait]** 활동을 워크플로우로 끌어서 놓습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업에서 ![](assets/edit_darkgrey-24px.png) 버튼을 사용하여 활동을 엽니다.
1. 활동의 인바운드 및 아웃바운드 전환이 활성화될 때까지의 대기 **[!UICONTROL Duration]**&#x200B;을(를) 지정합니다.

   지속 시간을 직접 입력하거나 해당 필드에 있는 선택기를 사용할 수 있습니다.

   ![](assets/wait_duration.png)

1. 활동 구성을 확인하고 워크플로우를 저장합니다.

## 예제 {#example}

다음 예제는 일반적인 사용 사례에서 **[!UICONTROL Wait]** 활동을 보여줍니다. 이벤트 초대 이메일을 전송합니다. 전송 24시간 후 이메일 게재 로그를 분석하여 첫 번째 이메일을 받았지만 등록하지 않은 사람에게 리마인더 이메일을 전송합니다.

워크플로우는 다음과 같이 표시됩니다.

![](assets/wait_example_workflow.png)

* 첫 번째 **[!UICONTROL Query]** 타겟은 초대 이메일을 보낼 프로필입니다.
* **[!UICONTROL Email delivery]**&#x200B;은(는) 선택한 프로필에 처음으로 초대장을 보냅니다.
* 24시간의 **[!UICONTROL Wait]** 활동으로 초대장 전송 시점과 나머지 워크플로우 사이에 대기 시간이 생깁니다.
* 두 번째 **[!UICONTROL Query]** 타겟은 첫 번째 이메일을 수신했지만 내부 구독 링크를 클릭하지 않은 프로필입니다.
* 두 번째 **[!UICONTROL Email delivery]**&#x200B;은(는) 선택한 사람들에게 초대 리마인더를 보냅니다.

