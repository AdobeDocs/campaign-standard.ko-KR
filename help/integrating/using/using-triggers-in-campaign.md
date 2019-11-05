---
title: Campaign에서 트리거 사용
description: null
page-status-flag: 활성화 안 함
uuid: d844d013-b38a-4e69-9df5-0edc01fa9c6e
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 통합
content-type: reference
topic-tags: 작업-with-campaign-and-triggers
discoiquuid: a524c700-bad6-4fcf-857a-c31bfae4d30c
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# Campaign에서 트리거 사용{#using-triggers-in-campaign}

## Campaign에서 매핑된 트리거 만들기 {#creating-a-mapped-trigger-in-campaign}

Adobe Experience Cloud( **[!UICONTROL Triggers]** 핵심 서비스)에서 미리 모니터링할 동작을 정의해야 합니다. 자세한 내용은 Adobe Experience Cloud [설명서를](https://marketing.adobe.com/resources/help/en_US/mcloud/triggers.html)참조하십시오. 트리거를 정의할 때 별칭을 활성화해야 합니다. 각 동작(탐색/양식 포기, 제품 추가/삭제, 세션 만료 등)에 대해 Adobe Experience Cloud에 새 트리거를 추가해야 합니다.

이제 기존 Adobe Experience Cloud 트리거를 기반으로 Adobe Campaign에서 트리거 이벤트를 만들어야 합니다.

이 [비디오를](https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html#step-two) 통해 Adobe Campaign에서 트리거를 설정하는 방법을 이해할 수 있습니다.

이 문제를 해결하는 단계는 다음과 같습니다.

1. 왼쪽 상단 모서리에서 **[!UICONTROL Adobe Campaign]** 로고를 클릭한 다음 **[!UICONTROL Marketing plans]** &gt; **[!UICONTROL Transactional messages]** &gt; **[!UICONTROL Experience Cloud Triggers]**&#x200B;를 선택합니다.

   ![](assets/remarketing_1.png)

1. 단추를 **[!UICONTROL Create]** 클릭합니다. 여는 만들기 마법사에 Adobe Experience Cloud에 정의된 모든 트리거의 목록이 표시됩니다. 이 **[!UICONTROL Fired by Analytics]** 열에는 Adobe Experience Cloud 트리거에서 Campaign으로 보낸 이벤트 수가 표시됩니다. 이는 Experience Cloud 인터페이스에서 생성된 트리거의 매핑을 의미합니다.

   ![](assets/remarketing_2.png)

1. 사용할 Adobe Experience Cloud 트리거를 선택하고 **[!UICONTROL Next]**&#x200B;클릭합니다.
1. 트리거의 일반 속성을 구성합니다. 마법사의 이 단계에서 트리거에 사용할 채널과 타깃팅 차원도 지정합니다( [타깃팅 차원 및 리소스](../../automating/using/query.md#targeting-dimensions-and-resources)참조). 그런 다음 트리거 생성을 확인합니다.
1. 페이로드 컨텐츠를 보려면 **[!UICONTROL Event content and enrichment]** 필드 오른쪽에 있는 단추를 클릭합니다. 또한 이 화면에서는 Adobe Campaign 데이터베이스에 저장된 프로필 데이터로 이벤트 데이터를 보완할 수 있습니다. 농축은 표준 트랜잭션 메시지와 같은 방식으로 수행됩니다.

   ![](assets/remarketing_3.png)

1. 필드에서 Analytics에서 이벤트를 보낸 후 메시지가 유효한 기간을 정의합니다. **[!UICONTROL Transactional message validity duration]** 기간이 2일인 경우 해당 기간이 지난 후 메시지가 더 이상 전송되지 않습니다. 여러 메시지를 일시 중단하면 일정 기간 후에 다시 시작하면 해당 메시지가 전송되지 않습니다.

   ![](assets/remarketing_4.png)

1. Analytics에 성향 점수가 정의된 경우( [Experience Cloud 설명서](https://marketing.adobe.com/resources/help/en_US/insight/client/c_visitor_propensity.html)참조) 고객이 가까운 시일 내에 웹 사이트로 돌아올 가능성이 높은 경우 메시지를 보내지 않도록 선택할 수 있습니다. 점수 및 임계값은 페이로드 컨텐츠에서 사용할 수 있으므로 해당 값을 사용하여 메시지를 개인화할 수 있습니다. 이 옵션을 사용하려면 화면 하단에 있는 상자를 선택합니다. 가까운 시일 내에 사이트를 다시 방문할 가능성이 높은 고객은 메시지를 받지 못합니다.
1. 트리거 이벤트 게시를 시작하려면 **[!UICONTROL Publish]** 단추를 클릭합니다.
1. 트리거 이벤트를 게시한 후에도 트리거 스키마를 변경해야 하는 경우 **[!UICONTROL Update schema]** 단추를 클릭하여 최신 변경 내용을 검색합니다.

   이 작업은 트리거 및 트랜잭션 메시지의 게시를 취소합니다. 나중에 다시 게시해야 합니다.

   ![](assets/remarketing_11.png)

이 **[!UICONTROL Show Trigger in Experience Cloud]** 단추를 사용하면 Adobe Experience Cloud에서 트리거 정의를 볼 수 있습니다.

이벤트가 게시되면 새 이벤트에 연결된 트랜잭션 템플릿이 자동으로 만들어집니다. 그런 다음 방금 만든 템플릿을 수정하고 게시해야 합니다. 자세한 내용은 템플릿 [편집](../../start/using/about-templates.md) 섹션을 참조하십시오.

## 트랜잭션 메시지 템플릿 편집 {#editing-the-transactional-message-template}

트리거 이벤트를 만들고 게시하면 해당 트랜잭션 템플릿이 자동으로 만들어집니다. 자세한 내용은 캠페인에서 [매핑된 트리거 만들기 섹션을 참조하십시오](#creating-a-mapped-trigger-in-campaign) .

이벤트가 트랜잭션 메시지 전송을 트리거하려면 템플릿을 개인화한 다음 테스트하여 게시해야 합니다. 이러한 단계는 표준 트랜잭션 메시지의 경우와 동일합니다. 자세한 내용은 트랜잭션 템플릿 [섹션을](../../channels/using/event-transactional-messages.md#personalizing-a-transactional-message) 참조하십시오.

>[!NOTE]
>
>템플릿을 게시 취소하는 경우 트리거 이벤트가 자동으로 게시 취소됩니다.

컨텐츠를 편집할 때 Analytics 트리거에서 보낸 정보를 기반으로 개인화 필드를 추가할 수 있습니다. Adobe Campaign 프로필 데이터를 사용하여 이벤트 데이터를 강화할 경우 이 정보를 기반으로 메시지를 개인화할 수 있습니다. 메시지를 개인화하려면 **[!UICONTROL Transactional event]** &gt; **[!UICONTROL Event context]** 을 선택하고 필드를 선택합니다.

![](assets/remarketing_8.png)

## 보고서 액세스 {#accessing-the-reports}

Adobe Campaign에서 전용 트리거 보고서를 보려면 이전에 만든 트리거 이벤트를 열고 을 **[!UICONTROL Show trigger report]**&#x200B;클릭합니다.

![](assets/remarketing_9.png)

이 보고서는 Analytics에서 보낸 이벤트 수와 비교하여 처리된 이벤트 수를 보여줍니다. 또한 모든 최근 트리거의 목록이 표시됩니다.

![](assets/trigger_uc_browse_14.png)

