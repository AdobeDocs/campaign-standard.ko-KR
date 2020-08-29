---
title: 이메일 게재
description: 이메일 게재 활동을 통해 워크플로우에서 단일 이메일 또는 반복 이메일 전송을 구성할 수 있습니다.
page-status-flag: never-activated
uuid: 7de53431-84ae-4d21-8361-2775ad314ed2
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: channel-activities
discoiquuid: 5f288cf6-f8ff-4ac9-9c1a-8010260554bb
context-tags: delivery,workflow,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 15e5aebdd67e8f5ddee89506c0469a101d94d2e8
workflow-type: tm+mt
source-wordcount: '857'
ht-degree: 94%

---


# 이메일 게재{#email-delivery}

## 설명 {#description}

![](assets/email.png)

![](assets/recurrentemail.png)

**[!UICONTROL Email delivery]** 활동을 통해 워크플로우에서 이메일 전송을 구성할 수 있습니다. 한 번만 보내는 **단일 전송** 이메일일 수도 있고 **반복** 이메일일 수도 있습니다.

단일 전송 이메일은 표준 이메일이며 한 번 전송됩니다.

반복 이메일을 사용하면 정의된 기간 동안 동일한 이메일을 여러 타겟에 여러 번 보낼 수 있습니다. 필요한 보고서를 얻기 위해 기간별 게재를 집계할 수 있습니다.

## 사용의 컨텍스트 {#context-of-use}

**[!UICONTROL Email delivery]** 활동은 일반적으로 동일한 워크플로우에서 계산된 타겟으로 이메일 전송을 자동화하는 데 사용됩니다.

스케줄러에 연결하면 반복되는 이메일을 정의할 수 있습니다.

이메일 수신자는 쿼리, 교집합 등과 같은 타겟팅 활동을 통해 동일한 워크플로우에서 활동의 업스트림으로 정의됩니다.

메시지 준비는 워크플로우 실행 매개 변수에 따라 트리거됩니다. 메시지 대시보드에서 메시지를 보낼 수동 확인을 요청할지 여부를 선택할 수 있습니다(기본적으로 필요). 워크플로우를 수동으로 시작하거나 워크플로우에 스케줄러 활동을 배치하여 실행을 자동화할 수 있습니다.

**관련 항목:**

* [사용 사례: 일주일에 한 번 보내는 이메일 게재 만들기](../../automating/using/workflow-weekly-offer.md)
* [사용 사례: 위치별로 분류된 게재 만들기](../../automating/using/workflow-segmentation-location.md)
* [사용 사례: 보충 자료로 게재 만들기](../../automating/using/workflow-created-query-with-complement.md)
* [사용 사례: 열지 않은 사용자에게 새 게재를 보내는 워크플로우 재타겟팅](../../automating/using/workflow-cross-channel-retargeting.md)
* [사용 사례:생일 배달](../../automating/using/birthday-delivery.md)

## 구성 {#configuration}

1. **[!UICONTROL Email delivery]** 활동을 워크플로우로 끌어서 놓습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업에서 ![](assets/edit_darkgrey-24px.png) 버튼을 사용하여 활동을 엽니다.

   >[!NOTE]
   >
   >활동의 빠른 작업에서 ![](assets/dlv_activity_params-24px.png) 버튼을 통해 활동의 일반 속성 및 고급 옵션(게재 자체가 아님)에 액세스할 수 있습니다. 이 버튼은 **[!UICONTROL Email delivery]** 활동에만 해당됩니다. 이메일 대시보드의 작업 표시줄을 통해 이메일 속성에 액세스할 수 있습니다.

1. 이메일 전송 모드를 선택합니다.

   * **[!UICONTROL Email]**: 이메일을 한 번만 보냅니다. 활동에 아웃바운드 전환을 추가할지 여부를 여기에서 지정할 수 있습니다. 다양한 전환 유형은 이 절차의 7단계에서 자세히 설명합니다.
   * **[!UICONTROL Recurring email]**: **[!UICONTROL Scheduler]** 활동에 정의된 빈도에 따라 이메일을 여러 번 보냅니다. 전송 집계 기간을 선택합니다. 이를 통해 정의된 기간 동안 발생하는 모든 전송을 하나의 이메일로 다시 그룹화할 수 있습니다. 이 메일은 **반복 실행**&#x200B;이라고도 하며 애플리케이션의 마케팅 활동 목록에서 액세스할 수 있습니다.

      예를 들어 매일 전송되는 반복 생일 이메일의 경우 월별 전송을 집계하도록 선택할 수 있습니다. 이렇게 하면 이메일이 매일 전송되지만 매월 게재 보고서를 받을 수 있습니다.
   >[!NOTE]
   >
   >반복 배달은 **집계 기간을 기반으로 준비됩니다**. 예를 들어 집계 기간이 &quot;일별&quot;일 경우, 하루 한 번만 배달이 다시 준비됩니다. 이 워크플로우를 하루에 여러 번 호출하려는 경우 을 사용하십시오 [!UICONTROL No aggregation].

1. 이메일 유형을 선택합니다. 이메일 유형은 **[!UICONTROL Resources]** > **[!UICONTROL Templates]** > **[!UICONTROL Delivery templates]** 메뉴에 정의된 이메일 템플릿에서 가져옵니다.
1. 이메일의 일반 속성을 입력합니다. 기존 캠페인에 첨부할 수도 있습니다. 워크플로우의 게재 활동의 레이블은 이메일 레이블로 업데이트됩니다.
1. 이메일 콘텐츠를 정의합니다. [콘텐츠 편집](../../designing/using/designing-content-in-adobe-campaign.md)에 대한 섹션을 참조하십시오.
1. 기본적으로 **[!UICONTROL Email delivery]** 활동에는 아웃바운드 전환이 포함되지 않습니다. **[!UICONTROL Email delivery]** 활동에 아웃바운드 전환을 추가하려면 고급 활동 옵션의 ![](assets/dlv_activity_params-24px.png) 탭(활동의 빠른 작업에 있는 **[!UICONTROL General]** 버튼)으로 이동한 다음 옵션 중 하나를 선택합니다.

   * **[!UICONTROL Add outbound transition without the population]**: 인바운드 전환과 정확히 동일한 모집단을 포함하는 아웃바운드 전환을 생성할 수 있습니다.
   * **[!UICONTROL Add outbound transition with the population]**: 이메일을 전송한 모집단을 포함하는 아웃바운드 전환을 생성할 수 있습니다. 게재를 준비하는 동안 제외된 타겟 멤버(격리, 잘못된 이메일 등) 는 이 전환에서 제외됩니다.

1. 활동 구성을 확인하고 워크플로우를 저장합니다.

활동을 다시 열면 이메일 대시보드로 바로 이동합니다. 콘텐츠만 편집할 수 있습니다.

기본적으로 게재 워크플로우를 시작하면 메시지 준비만 트리거됩니다. 워크플로우가 시작된 후에도 워크플로우에서 만든 메시지 전송을 확인해야 합니다. 하지만 메시지가 워크플로우에서 생성된 경우에만 메시지 대시보드에서 **[!UICONTROL Request confirmation before sending messages]** 옵션을 비활성화할 수 있습니다. 이 옵션을 선택 해제하면 준비가 완료된 후 추가 통보 없이 메시지가 전송됩니다.

## 비고 {#remarks}

워크플로우 내에서 생성된 게재는 애플리케이션의 마케팅 활동 목록에서 액세스할 수 있습니다. 대시보드를 사용하여 워크플로우의 실행 상태를 볼 수 있습니다. 이메일 요약 창의 링크를 사용하면 연결된 요소(반복 이메일의 경우 워크플로우, 캠페인, 상위 게재)에 직접 액세스할 수 있습니다.

![](assets/wkf_display_recurrent_executions_2.png)

그러나 반복 게재 실행은 기본적으로 마스킹됩니다. 이를 보려면 마케팅 활동의 검색 패널에서 **[!UICONTROL Show recurring executions]** 옵션을 선택합니다.

![](assets/wkf_display_recurrent_executions.png)

마케팅 활동 목록에서 액세스하거나 관련 반복 실행을 통해 직접 액세스할 수 있는 상위 게재에서 (**[!UICONTROL Email delivery]** 활동이 구성되었을 때 지정된 집계 기간에 따라) 처리된 총 전송 수를 볼 수 있습니다. 이렇게 하려면 ![](assets/wkf_dlv_detail_button.png)을(를) 선택하여 상위 게재 **[!UICONTROL Deployment]** 블록의 세부 사항 보기를 엽니다.

![](assets/wkf_display_recurrent_executions_3.png)
