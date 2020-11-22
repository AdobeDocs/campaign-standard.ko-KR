---
solution: Campaign Standard
product: campaign
title: Campaign에서 트리거 사용
description: null
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-triggers
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '725'
ht-degree: 87%

---


# Campaign에서 트리거 사용{#using-triggers-in-campaign}

## Campaign에서 매핑된 트리거 만들기 {#creating-a-mapped-trigger-in-campaign}

Adobe Experience Cloud(**[!UICONTROL Triggers]** 핵심 서비스)에서 미리 모니터링할 동작을 정의함을 확인해야 합니다. 자세한 내용은 [Adobe Experience Cloud 설명서](https://docs.adobe.com/content/help/ko-KR/core-services/interface/activation/triggers.html)를 참조하십시오. 트리거를 정의할 때 별칭을 활성화해야 합니다. Adobe Experience Cloud에 각 동작(검색/양식 포기, 제품 추가/삭제, 세션 만료 등)에 대한 새로운 트리거가 추가되어야 합니다.

이제 기존 Adobe Experience Cloud 트리거를 기반으로 Adobe Campaign에서 트리거 이벤트를 만들어야 합니다.

이 [비디오를](https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html#step-two) 보면서 Adobe Campaign에서 트리거를 설정하는 방법을 이해할 수 있습니다.

이 작업을 수행하는 단계는 다음과 같습니다.

1. 왼쪽 상단 모서리에서 **[!UICONTROL Adobe Campaign]** 로고를 클릭한 다음 **[!UICONTROL Marketing plans]** > **[!UICONTROL Transactional messages]** > **[!UICONTROL Experience Cloud Triggers]**&#x200B;을(를) 선택합니다.

   ![](assets/remarketing_1.png)

1. **[!UICONTROL Create]** 버튼을 클릭합니다. 열려 있는 만들기 마법사는 Adobe Experience Cloud에 정의된 모든 트리거의 목록을 표시합니다. **[!UICONTROL Fired by Analytics]** 열에는 Adobe Experience Cloud 트리거에서 Campaign으로 보낸 이벤트 수가 표시됩니다. Experience Cloud 인터페이스에서 만들어진 트리거의 매핑입니다.

   ![](assets/remarketing_2.png)

1. 사용할 Adobe Experience Cloud 트리거를 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.
1. 트리거의 일반 속성을 구성합니다. 마법사의 이 단계에서는 트리거에 사용할 채널과 타겟팅 차원도 지정합니다( [타겟팅 차원 및 리소스](../../automating/using/query.md#targeting-dimensions-and-resources)참조). 그런 다음 트리거 만들기를 확인합니다.
1. 페이로드 콘텐츠를 보려면 **[!UICONTROL Event content and enrichment]** 필드 오른쪽에 있는 버튼을 클릭합니다. 또한 이 화면에서는 Adobe Campaign 데이터베이스에 저장된 프로필 데이터로 이벤트 데이터를 보강할 수 있습니다. 데이터 보강은 표준 트랜잭션 메시지와 같은 방식으로 수행됩니다.

   ![](assets/remarketing_3.png)

1. **[!UICONTROL Transactional message validity duration]** 필드에서는 Analytics에서 이벤트를 보낸 후 메시지가 유효한 기간을 정의합니다. 기간이 2일로 정의된 경우, 해당 기간이 지난 후에는 더 이상 메시지가 전송되지 않습니다. 몇 개의 메시지가 대기 중인 경우, 일정 시간 후에 재개하면 해당 메시지가 전송되지 않도록 합니다.

   ![](assets/remarketing_4.png)

1. 이제 트리거를 게시할 수 있습니다. 자세한 내용은 Campaign [에서 트리거 게시를 참조하십시오](../../integrating/using/using-triggers-in-campaign.md#publishing-trigger-in-campaign).

## Campaign에서 트리거 게시 {#publishing-trigger-in-campaign}

기존 Adobe Experience Cloud 트리거를 기반으로 Adobe Campaign에서 트리거 이벤트를 만든 후 게시해야 합니다.

1. 이전에 만든 트리거에서 단추를 클릭하여 트리거 이벤트 게시를 시작합니다. **[!UICONTROL Publish]**

   ![](assets/trigger_publish_1.png)

1. 아래에서 트리거 게시의 진행 상태를 확인할 수 있습니다 **[!UICONTROL Publication]**.

   ![](assets/trigger_publish_2.png)

1. 게시가 완료되면 아래에 다음 메시지가 나타납니다 **[!UICONTROL Publication]**.

   ![](assets/trigger_publish_3.png)

1. 트리거 이벤트를 게시한 후에도 트리거 스키마를 변경해야 하는 경우, **[!UICONTROL Update schema]** 버튼을 클릭하여 최신 변경 사항을 재개합니다.

   이 작업은 트리거 및 트랜잭션 메시지를 게시 취소하므로 나중에 다시 게시해야 합니다.

   ![](assets/trigger_publish_4.png)

1. Click **[!UICONTROL Show Trigger in Experience Cloud]** button allows you to view the trigger definition in Adobe Experience Cloud.

이벤트가 게시되면 새 이벤트에 연결된 트랜잭션 템플릿이 자동으로 만들어집니다. 그런 다음 방금 만들어진 템플릿을 수정하고 게시해야 합니다. 자세한 내용은 [템플릿 편집](../../start/using/marketing-activity-templates.md) 섹션을 참조하십시오.

## 트랜잭션 메시지 템플릿 편집 {#editing-the-transactional-message-template}

트리거 이벤트를 만들고 게시하면 해당 트랜잭션 템플릿이 자동으로 만들어집니다. 자세한 내용은 [캠페인에서 매핑된 트리거 만들기](#creating-a-mapped-trigger-in-campaign) 섹션을 참조하십시오.

이벤트가 트랜잭션 메시지 전송을 트리거하려면 템플릿을 개인화한 다음 테스트하여 게시해야 합니다. 이러한 단계는 표준 트랜잭션 메시지와 동일합니다. 자세한 내용은 [트랜잭션 템플릿](../../channels/using/event-transactional-messages.md#personalizing-a-transactional-message) 섹션을 참조하십시오.

>[!NOTE]
>
>템플릿 게시를 취소하면 자동으로 트리거 이벤트가 게시 취소됩니다.

콘텐츠를 편집할 때 Analytics 트리거에서 보낸 정보를 기반으로 개인화 필드를 추가할 수 있습니다. Adobe Campaign 프로필 데이터를 사용하여 이벤트 데이터를 보강할 경우 이 정보를 기반으로 메시지를 개인화할 수 있습니다. 메시지를 개인화하려면 **[!UICONTROL Transactional event]** > **[!UICONTROL Event context]**&#x200B;을(를) 선택하고 필드를 선택합니다.

![](assets/remarketing_8.png)

## 보고서에 액세스 {#accessing-the-reports}

Adobe Campaign에서 전용 트리거 보고서를 보려면 이전에 만든 트리거 이벤트를 열고 **[!UICONTROL Show trigger report]**&#x200B;을(를) 클릭합니다.

![](assets/remarketing_9.png)

이 보고서는 처리된 이벤트 수를 Analytics에서 보낸 이벤트 수와 비교하여 보여줍니다. 또한 모든 최근 트리거 목록이 표시됩니다.

![](assets/trigger_uc_browse_14.png)

