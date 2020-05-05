---
title: 워크플로우 구축
description: 이 섹션에서는 새 워크플로우를 만들기 위한 주요 원칙과 우수 사례를 자세히 설명합니다.
page-status-flag: never-activated
uuid: 11374f64-8d34-40da-937b-09f419250f4c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: workflow-general-operation
discoiquuid: c26fcb0e-19d5-4bd5-b7d6-2d22ce92ad90
context-tags: workflow,wizard;workflow,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 68e825bc3b6b7f94f61875e7da2bc8f63f06d9cb

---


# 워크플로우 구축{#building-a-workflow}

이 섹션에서는 새 워크플로우를 만들기 위한 주요 원칙과 우수 사례를 자세히 설명합니다.

## 워크플로우 작업 원칙{#workflow-operating-principles}

워크플로우는 구성 가능한 **일련의 활동입니다**. 각 활동에는 프로세스에서 특정 역할이 있습니다. 각 활동의 결과는 화살표로 표시된 **전환으로**&#x200B;다음 활동에 전달됩니다.

한 활동과 다른 활동 간에 교환된 데이터 유형은 다음 활동이 구성되는 방식에 영향을 줄 수 있습니다. 예를 들어, 이메일 배달 활동 전에 모집단이 설정된 경우 해당 이메일의 대상이 될 수 있습니다.

워크플로우를 실행하기 전 또는 후에 활동을 열어 매개 변수를 확인하거나 편집할 수 있습니다.

전환을 열어 워크플로우를 실행하는 동안 또는 이후에 전송된 데이터가 올바른지 확인할 수 있습니다. 전환의 세부 사항 보기에 액세스하려면 워크플로우 속성 섹션 **[!UICONTROL Keep interim results]** 에서 옵션 **[!UICONTROL Execution]** 을 선택해야 합니다.

![](assets/workflow_overview.png)


## 워크플로우 만들기 {#creating-a-workflow}

프로그램, 캠페인 또는 마케팅 활동 목록에서 워크플로우를 만들 수 있습니다.

마케팅 활동 만들기에 대해서는 마케팅 활동 [만들기](../../start/using/marketing-activities.md#creating-a-marketing-activity) 섹션에서 자세히 설명합니다.

1. 워크플로우 유형 마케팅 활동을 만들기 시작하면 사용할 템플릿을 선택합니다.

   ![](assets/workflow_creation_1.png)

   >[!NOTE]
   >
   >각 마케팅 활동에서는 기본적으로 여러 유형을 제공합니다. 필요에 따라 특정 매개 변수를 미리 구성할 수 있습니다. 자세한 내용은 템플릿 [관리](../../start/using/marketing-activity-templates.md) 섹션을 참조하십시오.

1. 워크플로우의 일반 속성을 입력합니다.

   ![](assets/workflow_creation_2.png)

   레이블 필드에 이름을 **입력하고** ID를 수정할 수 있습니다. 활동 이름 및 해당 ID는 인터페이스에 표시되지만 메시지 수신자는 이를 볼 수 없습니다.

   >[!NOTE]
   >
   >마케팅 활동 목록에서 상위 캠페인 내에서 워크플로우를 만들 수 있습니다. 이미 만들어진 워크플로우를 선택하여 이 워크플로우를 캠페인에 연결할 수 있습니다.

   사용자가 캠페인 컨텐츠에서 볼 수 있는 설명을 추가할 수 있습니다.

   이를 통해 예상 방식으로 작동하지 않는 사용자를 쉽게 찾고 해결할 수 있으므로, Adobe에서는 워크플로우에 적합한 이름과 레이블을 지정하는 것이 좋습니다. 연산자가 쉽게 이해할 수 있도록 수행할 프로세스를 요약하려면 워크플로우의 설명 필드를 입력합니다.

1. 활동을 만들고 해당 활동에 대한 대시보드가 표시되는지 확인합니다. 자세한 내용은 워크플로우 인터페이스 [섹션을 참조하십시오](../../automating/using/workflow-interface.md) .

1. 워크플로우를 구성할 준비가 되면 **[!UICONTROL Edit properties]** 단추를 클릭하여 추가 옵션에 액세스할 수 있습니다. 예를 들어 모든 워크플로우의 활동에서 기본적으로 사용할 특정 시간대를 정의할 수 있습니다. 기본적으로 워크플로우의 시간대는 현재 캠페인 연산자에 대해 정의된 시간대입니다.

   ![](assets/workflow_properties.png)

**관련 항목:**

* [워크플로우](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/workflow-general-operation/building-a-workflow.html) 비디오 만들기
* [워크플로우 속성](../../automating/using/executing-a-workflow.md#workflow-properties)

## 활동 추가 및 연결 {#adding-and-linking-activities}

이제 다양한 활동을 정의하고 이를 다이어그램에 함께 연결해야 합니다.

>[!NOTE]
>
>팔레트가 표시되지 않으면 도구 모음의 첫 번째 단추를 클릭하여 표시합니다.

활동은 팔레트의 여러 섹션 내에서 범주별로 그룹화됩니다.

* 첫 번째 섹션에는 [타깃팅 활동이 포함됩니다.](../../automating/using/about-targeting-activities.md)
* 두 번째 섹션에는 다른 활동을 조정하는 데 주로 사용되는 [실행 활동이](../../automating/using/about-execution-activities.md)포함되어 있습니다.
* 세 번째 섹션에는 여러 [채널에서 메시지를 보내는 데 사용할 수 있는 활동이 포함되어 있습니다](../../automating/using/about-channel-activities.md). 이 섹션의 활동은 인스턴스에 대해 활성화된 채널에 따라 달라질 수 있습니다.
* 네 번째 섹션에는 [파일 조작 및 데이터 관리 활동이 포함되어 있습니다](../../automating/using/about-data-management-activities.md).

다이어그램을 만들려면:

1. 팔레트에서 활동을 드래그하고 다이어그램에 놓아 활동을 추가합니다.

   예를 들어 시작 **[활동을](../../automating/using/start-and-end.md)**추가한 다음 다이어그램에**[&#x200B;이메일 배달](../../automating/using/email-delivery.md)** 활동을 추가합니다.

1. 활동 **시작** 전환 **을 드래그하여 이메일 배달** 활동에 놓아 활동을 함께 연결합니다.

   >[!NOTE]
   >
   >이전 전환 끝에 새 활동을 배치하여 활동을 이전 활동에 자동으로 연결할 수 있습니다.

1. 필요한 활동을 추가하고 이러한 활동을 연결하여 워크플로우를 완료할 수 있습니다.

   >[!NOTE]
   >
   >기존 활동을 복사하여 붙여넣을 수도 있습니다. 이렇게 하면 원래 정의된 설정을 유지합니다. 자세한 내용은 워크플로우 활동 [중복을 참조하십시오](../../automating/using/workflow-interface.md#duplicating-workflow-activities).

워크플로우 활동이 서로 연결되면 원하는 **레이블로** 전환율을 개인화할 수 있습니다. 이렇게 하려면 전환 효과를 두 번 클릭하여 해당 속성에 액세스합니다.

또한, **[!UICONTROL Targeting]** 및 **[!UICONTROL Data management (ETL)]** 활동을 통해 아웃바운드 전환 **에 대한 세그먼트 코드를** 정의할 수 있습니다. 그런 다음 마케팅 캠페인의 효율성을 측정하기 위해 이러한 세그먼트 코드를 기반으로 보고서를 만들 수 있습니다. For more on this, refer to [this section](../../reporting/using/creating-a-report-workflow-segment.md).

**워크플로우 활용 사례:**

* [사용 사례: 일주일에 한 번 이메일 전달 만들기](../../automating/using/workflow-weekly-offer.md)
* [사용 사례: 위치에 세그먼트화된 배달 만들기](../../automating/using/workflow-segmentation-location.md)
* [사용 사례: 보충으로 배달 만들기](../../automating/using/workflow-created-query-with-complement.md)
* [사용 사례: 따개가 아닌 사람에게 새 배달을 보내는 다시 타깃팅 워크플로우](../../automating/using/workflow-cross-channel-retargeting.md)

## 활동 구성 {#configuring-activities}

기본적으로 활동은 설정되지 않으며, 데이터가 구성되지 않은 경우 올바로 처리되지 않습니다. 각 활동에는 특정 구성 및 아웃바운드 전환, 레이블 등과 같은 활동 일반 옵션을 관리하는 여러 개의 탭이 있습니다.

1. 모든 활동이 올바르게 연결되어 있는지 확인합니다. 일부 활동은 올바른 구성 옵션을 제공하기 위해 들어오는 데이터의 구조나 특성을 감지해야 합니다.
1. 활동을 두 번 클릭하거나 활동을 선택하고 컨텍스트 동작을 클릭하여 해당 구성 창을 엽니다. **[!UICONTROL Edit]**
1. 활동의 레이블을 편집합니다.
1. 데이터를 처리하는 데 필요한 다양한 옵션을 모두 정의합니다. 각 활동에 대해 가능한 옵션을 알아보려면 이 설명서의 활동 특정 섹션을 참조하십시오.
1. 활동을 저장하고 워크플로우의 각 활동에 대해 이러한 작업을 반복합니다.
1. 워크플로우를 저장합니다.
