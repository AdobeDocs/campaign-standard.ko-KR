---
title: 워크플로우 실행 기본 정보
description: 워크플로우 실행에 대해 자세히 알아봅니다.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
context-tags: workflow,overview;workflow,main
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: 3b95fc66-d6f4-44b2-be33-925c1109a57f
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 8%

---

# 워크플로우 실행 기본 정보 {#about-workflow-execution}

워크플로우는 항상 수동으로 시작됩니다. 그러나 일단 시작되면, [스케줄러](../../automating/using/scheduler.md) 활동.

>[!CAUTION]
>
> Adobe은 고객이 워크플로우 실행에 우선 순위를 지정하고 최대 20개의 동시 워크플로우 실행을 실행하여 인스턴스 전체에서 일관되게 최대 성능을 구현할 것을 권장합니다. 20개 이상의 동시 워크플로우 실행을 계획할 수 있으며 기본적으로 순차적으로 실행됩니다. 고객 지원 센터에 티켓을 제출하여 최대 동시 실행 워크플로우의 수에 대한 기본 설정을 조정할 수 있습니다.

실행 관련 작업(시작, 중지, 일시 중지 등) is **비동기** 프로세스: 명령이 저장되고 서버가 해당 명령을 적용할 수 있게 되면 그 효과가 나타납니다.

워크플로우에서 각 활동의 결과는 일반적으로 화살표로 표시되는 전환을 통해 다음 활동으로 전송됩니다.

전환이 대상 활동에 연결되어 있지 않으면 종료되지 않습니다.

![](assets/wkf_execution_1.png)

>[!NOTE]
>
>종료되지 않은 전환이 포함된 워크플로우는 계속 실행할 수 있습니다. 경고 메시지가 생성되며 워크플로우가 전환에 도달하면 일시 중지되지만 오류가 생성되지 않습니다. 또한 디자인을 완전히 완료하지 않고 워크플로우를 시작하고 작업을 완료할 수 있습니다.

활동이 실행되면 전환에서 전송된 레코드 수가 활동 위에 표시됩니다.

![](assets/wkf_transition_count.png)

전환을 열어 워크플로우를 실행하는 중 또는 후에 전송된 데이터가 올바른지 확인할 수 있습니다. 데이터 및 데이터 구조를 볼 수 있습니다.

기본적으로 워크플로우의 마지막 전환 세부 사항만 액세스할 수 있습니다. 이전 활동의 결과에 액세스하려면 다음을 확인해야 합니다 **[!UICONTROL Keep interim results]** 옵션 **[!UICONTROL Execution]** 섹션을 참조하십시오.

>[!NOTE]
>
>이 옵션은 많은 메모리를 소모하며 워크플로우를 구성하고 올바르게 구성 및 작동하도록 설계되었습니다. 프로덕션 인스턴스에서 선택하지 않은 상태로 둡니다.

전환이 열리면 다음을 편집할 수 있습니다 **[!UICONTROL Label]** 또는 링크 **[!UICONTROL Segment code]** 바로 그거야 이렇게 하려면 해당 필드를 편집하고 수정 내용을 확인합니다.

Campaign Standard REST API를 사용하여 다음을 수행할 수 있습니다 **start**, **pause**, **다시 시작** 및 **stop** 워크플로우. REST 호출에 대한 자세한 내용과 예를 [API 설명서.](../../api/using/controlling-a-workflow.md)
