---
title: 워크플로우 구축
seo-title: 워크플로우 구축
description: 워크플로우 구축
seo-description: 이 섹션에서는 새 작업 과정을 만드는 기본 원칙과 우수 사례를 자세히 설명합니다.
page-status-flag: 정품 인증 안 함
uuid: 11374 F 64-8 D 34-40 DA -937 B -09 F 419250 F 4 C
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: workflow-general-operation
discoiquuid: c 26 fcb 0 e -19 d 5-4 bd 5-b 7 d 6-2 d 22 ce 92 ad 90
context-tags: Workflow, Wizard; 워크플로우, 기본
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: bb65cbf808a95e8b42b2a682b7c0a9cc6225d920

---


# 워크플로우 구축{#building-a-workflow}

이 섹션에서는 새 워크플로우를 만드는 기본 원칙과 우수 사례를 자세히 설명합니다.

* 워크플로우 만들기를 참조하십시오.
* 활동 추가 및 연결.
* 활동 구성을 참조하십시오.

## 워크플로우 만들기 {#creating-a-workflow}

프로그램, 캠페인 또는 마케팅 활동 목록에서 워크플로우를 만들 수 있습니다.

마케팅 활동 만들기는 마케팅 활동 [만들기](../../start/using/marketing-activities.md#creating-a-marketing-activity) 섹션에 자세히 설명되어 있습니다.

1. 워크플로우 유형 마케팅 활동을 만들었으면 사용할 템플릿을 선택합니다.

   ![](assets/workflow_creation_1.png)

   >[!NOTE]
   >
   >각 마케팅 활동은 기본적으로 여러 유형을 제공합니다. 이를 통해 필요에 따라 특정 매개 변수를 미리 구성할 수 있습니다. 자세한 내용은 템플릿 [관리](../../start/using/about-templates.md) 섹션을 참조하십시오.

1. 워크플로우의 일반 속성을 입력합니다.

   ![](assets/workflow_creation_2.png)

   **레이블** 필드에 이름을 입력하고 ID를 수정할 수 있습니다. 활동 이름과 ID가 인터페이스에 표시되지만 메시지 받는 사람이 볼 수 없습니다.

   >[!NOTE]
   >
   >마케팅 활동 목록에서 상위 캠페인 내에 워크플로우를 만들 수 있습니다. 이미 만들어진 캠페인을 선택하여 이 워크플로우를 캠페인에 연결할 수 있습니다.

   사용자가 캠페인 컨텐츠에서 볼 수 있는 설명을 추가할 수 있습니다.

   Adobe는 예상한 방식으로 수행하지 않는 경우 더 쉽게 찾고 문제를 해결할 수 있도록 하기 때문에 워크플로우에 적절한 이름과 레이블을 제공할 것을 권장합니다. 워크플로우의 설명 필드를 채워 연산자가 작업을 쉽게 이해할 수 있도록 프로세스를 요약합니다.

1. 활동 만들기를 확인하면 해당 활동에 대한 대시보드가 표시됩니다. 이에 대한 자세한 내용은 [워크플로우 인터페이스](../../automating/using/workflow-interface.md) 섹션을 참조하십시오.

**관련 항목:**

[워크플로우](https://helpx.adobe.com/campaign/kt/acs/using/acs-create-workflow-feature-video-use.html) 비디오 만들기

## 활동 추가 및 연결 {#adding-and-linking-activities}

이제 다양한 활동을 정의하고 다이어그램에서 함께 링크해야 합니다.

>[!NOTE]
>
>팔레트가 표시되지 않으면 도구 모음의 첫 번째 단추를 클릭하여 표시합니다.

활동은 팔레트의 여러 섹션 내에서 범주별로 그룹화됩니다.

* 첫 번째 섹션에는 타깃팅 활동이 포함됩니다.
* 두 번째 섹션에는 다른 활동을 조정하는 데 주로 사용되는 실행 활동이 포함됩니다.
* 세 번째 섹션에는 여러 채널에서 메시지를 전송하는 데 사용할 수 있는 활동이 포함되어 있습니다. 이 섹션의 활동은 인스턴스에서 활성화된 채널에 따라 달라질 수 있습니다.
* 네 번째 섹션에는 파일 조작 및 데이터 관리 활동이 포함되어 있습니다.

다이어그램을 만들려면:

1. 팔레트에서 활동을 끌어 다이어그램에 놓아 활동을 추가합니다.

   예를 들어 **시작** 활동을 추가한 다음 다이어그램에 **이메일 게재** 활동을 추가합니다.

1. 활동 **시작을** 드래그하여 **이메일 게재** 활동에 놓아 활동을 연결합니다.

   >[!NOTE]
   >
   >이전 활동 전환 끝에 새 활동을 배치하여 활동을 이전 활동에 자동으로 연결할 수 있습니다.

1. 필요한 활동을 추가하고 함께 연결하여 워크플로우를 완료합니다.

   >[!NOTE]
   >
   >기존 활동을 복사하여 복사하여 복제할 수도 있습니다. 이렇게 하면 원래 정의된 설정을 유지합니다. 이에 대한 자세한 내용은 워크플로우 활동 [복제를](../../automating/using/workflow-interface.md#duplicating-workflow-activities)참조하십시오.

워크플로우 활동을 함께 연결하면 원하는 **레이블로** 전환율을 개인화할 수 있습니다. 이렇게 하려면 전환을 두 번 클릭하여 속성에 액세스합니다.

또한 **[!UICONTROL Targeting]****[!UICONTROL Data management (ETL)]** , 활동을 통해 아웃바운드 전환을 위한 **세그먼트 코드를** 정의할 수 있습니다. 그런 다음 이러한 세그먼트 코드를 기반으로 보고서를 만들어 광고 캠페인의 효율성을 측정할 수 있습니다. For more on this, refer to [this section](../../reporting/using/creating-a-report-workflow-segment.md).

**워크플로우 사용 사례:**

* [사용 사례: 일주일에 한 번 이메일 배달 만들기](../../automating/using/workflow-weekly-offer.md)
* [사용 사례: 위치에서 세그먼트화된 배달 만들기](../../automating/using/workflow-segmentation-location.md)
* [사용 사례: 보완을 통한 전달 창출](../../automating/using/workflow-created-query-with-complement.md)
* [사용 사례: 새 배달을 오프닝으로 전송하는 재타깃팅 워크플로우](../../automating/using/workflow-cross-channel-retargeting.md)

## 활동 구성 {#configuring-activities}

기본적으로 활동은 설정되지 않고 데이터가 구성되지 않은 경우 올바르게 처리되지 않습니다. 각 활동에는 아웃바운드 전환, 레이블 등과 같은 일반 옵션과 특정 구성을 관리하는 여러 개의 탭이 포함되어 있습니다.

1. 모든 활동이 올바르게 연결되어 있는지 확인합니다. 일부 활동은 올바른 구성 옵션을 제공하기 위해 들어오는 데이터의 구조 또는 특성을 감지해야 합니다.
1. 활동을 두 번 클릭하거나 해당 활동을 선택하고 **[!UICONTROL Edit]** 컨텍스트 작업을 클릭하여 구성 창을 엽니다.
1. 활동 레이블을 편집합니다.
1. 데이터를 처리하는 데 필요한 모든 옵션을 정의합니다. 각 활동에 대한 가능한 옵션을 알려면 이 설명서의 활동 특정 섹션을 참조하십시오.
1. 활동을 저장하고 워크플로우의 각 활동에 대해 이러한 작업을 반복합니다.
1. 워크플로우를 저장합니다.
