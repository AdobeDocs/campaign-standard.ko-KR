---
solution: Campaign Standard
product: campaign
title: 워크플로우 실행 기본 정보
description: 워크플로우 실행에 대한 자세한 내용을 살펴보십시오.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
context-tags: workflow,overview;workflow,main
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 8%

---


# 워크플로우 실행 기본 정보 {#about-workflow-execution}

워크플로우는 항상 수동으로 시작됩니다. 그러나, 시작한 후에는 [스케줄러](../../automating/using/scheduler.md) 활동에 지정된 정보에 따라 비활성 상태로 유지될 수 있습니다.

>[!CAUTION]
>
> Adobe에서는 고객이 워크플로우 실행에 우선 순위를 지정하고 인스턴스 전체에서 지속적으로 최대 성능을 내기 위해 최대 20개의 동시 워크플로우 실행을 실행할 것을 권장합니다. 20개 이상의 동시 워크플로우 실행을 계획할 수 있으며 기본적으로 순차적으로 실행됩니다. 고객 지원 센터에 티켓을 제출하여 동시 작업 과정 실행 최대 수에 대한 기본 설정을 조정할 수 있습니다.

실행 관련 작업(시작, 중지, 일시 중지 등) **비동기** 프로세스:명령이 저장되고 서버에서 해당 명령을 적용할 수 있게 되면 효과가 적용됩니다.

워크플로우에서 각 활동의 결과는 일반적으로 화살표를 통해 다음 활동으로 보내집니다.

전환이 대상 활동에 연결되어 있지 않으면 종료되지 않습니다.

![](assets/wkf_execution_1.png)

>[!NOTE]
>
>종료되지 않은 전환이 포함된 워크플로우는 계속 실행할 수 있습니다.경고 메시지가 생성되고 워크플로우가 전환에 도달하면 일시 정지되지만 오류가 생성되지 않습니다. 또한 디자인을 완전히 마치지 않고도 워크플로우를 시작할 수 있으며 작업을 진행하면서 완료할 수 있습니다.

활동이 실행되면 전환에서 전송된 레코드 수가 활동 위에 표시됩니다.

![](assets/wkf_transition_count.png)

전환을 열어 워크플로우를 실행하는 중 또는 후에 전송된 데이터가 올바른지 확인할 수 있습니다. 데이터와 데이터 구조를 볼 수 있습니다.

기본적으로 워크플로우의 마지막 전환 세부 사항만 액세스할 수 있습니다. 이전 활동의 결과에 액세스하려면 워크플로우를 시작하기 전에 워크플로우 속성의 **[!UICONTROL Execution]** 섹션에서 **[!UICONTROL Keep interim results]** 옵션을 선택해야 합니다.

>[!NOTE]
>
>이 옵션은 많은 메모리를 사용하며 작업 과정을 구성하고 제대로 구성되고 작동하는지 확인하기 위해 설계되었습니다. 프로덕션 인스턴스에서 선택하지 않은 상태로 둡니다.

전환이 열리면 **[!UICONTROL Label]**&#x200B;을 편집하거나 **[!UICONTROL Segment code]**&#x200B;을(를) 해당 전환에 연결할 수 있습니다. 이렇게 하려면 해당 필드를 편집하고 수정 내용을 확인합니다.

Campaign Standard REST API를 사용하면 **시작**, **일시 중지**, **다시 시작** 및 **중지**&#x200B;워크플로우를 수행할 수 있습니다. REST 호출에 대한 자세한 내용과 예는 [API 설명서에서 찾을 수 있습니다.](../../api/using/controlling-a-workflow.md)
