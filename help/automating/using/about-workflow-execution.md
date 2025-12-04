---
title: 워크플로 실행 기본 정보
description: 워크플로우 실행에 대해 자세히 알아봅니다.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
context-tags: workflow,overview;workflow,main
feature: Workflows
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: 3b95fc66-d6f4-44b2-be33-925c1109a57f
source-git-commit: b3f3309a252971dc527d44913b7918abeea704d9
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 8%

---

# 워크플로 실행 기본 정보 {#about-workflow-execution}

워크플로우는 항상 수동으로 시작됩니다. 그러나 시작한 후에는 [스케줄러](../../automating/using/scheduler.md) 활동에 지정된 정보에 따라 비활성 상태로 유지될 수 있습니다.

>[!IMPORTANT]
>
> Adobe에서는 고객이 20개 이상의 활성 워크플로우 실행을 동시에 실행하지 않도록 하고, 시간에 따라 워크플로우 실행의 우선 순위를 지정하고 분산하도록 권장합니다. 자세한 내용은 [이 페이지](../../automating/using/best-practices-workflows.md)에 제공된 모범 사례를 참조하세요.

실행 관련 작업(시작, 중지, 일시 중지 등)은 **비동기** 프로세스입니다. 명령이 저장되며 서버에서 해당 명령을 적용할 수 있게 되면 적용됩니다.

워크플로우에서 각 활동의 결과는 일반적으로 화살표로 표시되는 전환을 통해 다음 활동으로 전송됩니다.

대상 활동에 연결되어 있지 않은 전환은 종료되지 않습니다.

![](assets/wkf_execution_1.png)

>[!NOTE]
>
>종료되지 않은 전환이 포함된 워크플로우는 계속 실행할 수 있습니다. 경고 메시지가 생성되고 전환에 도달하면 워크플로가 일시 중지되지만 오류가 생성되지 않습니다. 또한 설계를 완전히 완료하지 않고 워크플로우를 시작할 수 있으며 작업을 진행할 때 완료할 수 있습니다.

활동이 실행되면 전환에서 전송된 레코드 수가 활동 위에 표시됩니다.

![](assets/wkf_transition_count.png)

전환을 열어 워크플로를 실행하는 중 또는 후에 전송된 데이터가 올바른지 확인할 수 있습니다. 데이터 및 데이터 구조를 볼 수 있습니다.

기본적으로 워크플로우의 마지막 전환에 대한 세부 정보에만 액세스할 수 있습니다. 이전 활동의 결과에 액세스하려면 워크플로우를 시작하기 전에 워크플로우 속성의 **[!UICONTROL Keep interim results]** 섹션에서 **[!UICONTROL Execution]** 옵션을 선택해야 합니다.

>[!NOTE]
>
>이 옵션은 많은 메모리를 소모하며 워크플로우를 구성하고 워크플로우가 올바르게 구성 및 작동하는지 확인할 수 있도록 설계되었습니다. 프로덕션 인스턴스에서 선택하지 않은 상태로 둡니다.

전환이 열려 있으면 해당 **[!UICONTROL Label]**&#x200B;을(를) 편집하거나 **[!UICONTROL Segment code]**&#x200B;을(를) 연결할 수 있습니다. 이렇게 하려면 해당 필드를 편집하고 수정 사항을 확인하십시오.

Campaign Standard REST API를 사용하면 워크플로우를 **시작**, **일시 중지**, **다시 시작** 및 **중지**&#x200B;할 수 있습니다. [API 설명서에서 REST 호출에 대한 자세한 내용과 예를 찾을 수 있습니다.](../../api/using/controlling-a-workflow.md)
