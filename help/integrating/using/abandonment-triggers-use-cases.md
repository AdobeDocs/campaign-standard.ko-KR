---
title: 포기 트리거 활용 사례
seo-title: 포기 트리거 활용 사례
description: 포기 트리거 활용 사례
seo-description: Experience Cloud를 사용하여 이러한 다양한 사용 사례와 통합된 방법을 살펴보십시오.
page-status-flag: 정품 인증 안 함
uuid: 9 E 236165-AFD 5-4155-9151-C 1941 DC 0 AF 99
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 통합
content-type: 참조
topic-tags: working-with-campaign-and-triggers
discoiquuid: 1 B 9 AEEC 5-70 BB -4 D 72-A 3 E 9-12342 ABF 08 F 7
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 698466596fdacd005dc4d72b8071208c8c39f77d

---


# Abandonment Triggers use cases{#abandonment-triggers-use-cases}

이 섹션에서는 Adobe Campaign와 Experience Cloud 트리거 간의 통합을 사용하여 구현할 수 있는 다양한 사용 사례를 설명합니다. 다음 두 가지 사용 사례를 확인할 수 있습니다.

* [포기 트리거 탐색](../../integrating/using/abandonment-triggers-use-cases.md#browse-abandonment-trigger): 웹 사이트에서 방문을 포기한 고객에게 커뮤니케이션을 보냅니다.
* [검색 포기 트리거](../../integrating/using/abandonment-triggers-use-cases.md#search-abandonment-trigger): 웹 사이트에서 검색을 수행한 다음 구매하지 않은 방문자와 재방문합니다.

>[!NOTE]
>
>이 섹션에 설명된 사용 사례는 Experience Cloud 방문자 ID를 사용합니다. 또한 Experience Cloud 선언 ID를 사용하여 구현할 수도 있습니다. 해시 처리된 ID와 암호화된 ID도 지원됩니다. 암호화된 이메일 주소/모바일 번호를 직접 해독하여 캠페인에 존재하지 않는 프로필로 이메일/SMS를 보낼 수 있습니다. 그러나 이 경우 프로필 데이터를 사용한 개인화는 사용할 수 없습니다.

## Pre-requisites {#pre-requisites}

이러한 사례를 구현하려면 다음 솔루션/핵심 서비스에 액세스해야 합니다.

* Adobe Campaign
* Adobe Analytics Ultimate, Premium, Foundation, OD, Select, Prime, Mobile Apps, Select 또는 Standard.
* Experience Cloud 트리거 코어 서비스
* Experience Cloud DTM 핵심 서비스
* Experience Cloud 방문자 ID 및 Experience Cloud 사용자 코어 서비스

또한 작업 웹 사이트가 필요합니다.

For more information, refer to [Configuring solutions and services](../../integrating/using/configuring-triggers-in-experience-cloud.md#configuring-solutions-and-services).

## Browse abandonment Trigger {#browse-abandonment-trigger}

이 사용 사례에서는 클라이언트가 웹 사이트의 방문을 포기할 때마다 실행할 간단한 트리거를 만들게 됩니다. 이 예에서는 이미 DTM 이 데이터를 Adobe Analytics로 수집하고 푸시하고 모든 이벤트를 만들었다고 가정합니다.

### Creating an Experience Cloud Trigger {#creating-an-experience-cloud-trigger}

1. Select **[!UICONTROL Manage Triggers]** from the Experience Cloud Activation Core Service menu.

   ![](assets/trigger_uc_browse_1.png)

1. Choose a trigger type ( **[!UICONTROL Abandonment]** in our use case).

   ![](assets/trigger_uc_browse_2.png)

1. 이 경우 간단한 포기 트리거가 필요합니다. 비즈니스 목적은 여행 예약 웹 사이트를 탐색하는 방문자를 식별하고, "거래" 페이지를 살펴보고, 여행을 예약하지 않는 것입니다. Adobe는 이러한 고객을 식별한 후 짧은 시간 내에 고객에게 도달합니다. 이 예에서는 10 분 후에 트리거를 전송합니다.

   ![](assets/trigger_uc_browse_3.png)

### Using the trigger in Adobe Campaign {#using-the-trigger-in-adobe-campaign}

Experience Cloud 트리거를 만들었으므로 Adobe Campaign에서 사용할 수 있습니다.

Adobe Campaign 에서는 Experience Cloud에서 만든 트리거에 연결된 트리거를 만들어야 합니다.

1. To create the Trigger in Adobe Campaign, click the **[!UICONTROL Adobe Campaign]** logo, in the top left corner, then select **[!UICONTROL Marketing plans]** &gt; **[!UICONTROL Transactional messages]** &gt; **[!UICONTROL Experience Cloud triggers]**.

   ![](assets/remarketing_1.png)

1. **[!UICONTROL Create]**&#x200B;을 클릭합니다.
1. Select the Trigger you created earlier and click **[!UICONTROL Next]**.

   ![](assets/trigger_uc_browse_5.png)

1. **[!UICONTROL Email]** 채널과 **[!UICONTROL Real-time event]** 타깃팅 차원을 선택하고를 클릭합니다 **[!UICONTROL Create]**.

   ![](assets/trigger_uc_browse_6bis.png)

1. Adobe Campaign에 트리거를 게시합니다. 이 프로세스는 트랜잭션 메시지 템플릿을 자동으로 만듭니다.

   ![](assets/trigger_uc_browse_6.png)

1. To dislay the message template, click the **[!UICONTROL More]** button, on the top right, then click **[!UICONTROL Trigger Transactional Template]**.
1. 콘텐츠 및 발신자 세부 정보를 개인화할 수 있습니다.

   ![](assets/trigger_uc_browse_8.png)

1. 메시지 템플릿을 게시합니다. 트리거는 이제 라이브 및 기능적으로 실행됩니다.

   ![](assets/trigger_uc_browse_0.png)

### Running the scenario {#running-the-scenario}

1. 이 사용 사례는 Adobe Campaign로 고객에게 보낸 초기 이메일을 사용하여 시작됩니다.

   ![](assets/trigger_uc_browse_9.png)

1. 받는 사람이 이메일을 엽니다.

   ![](assets/trigger_uc_browse_10.png)

1. 웹 사이트로 연결되는 링크를 클릭합니다. 이 예에서 배너는 수신자를 여행 예약 웹 사이트의 홈 페이지로 가져옵니다.

   ![](assets/trigger_uc_browse_11.png)

1. 받는 사람이 "거래" 페이지로 이동했지만 갑자기 방문을 중지합니다. 10 분 기간이 지나면 Adobe Campaign에서 트랜잭션 메시지를 전송합니다.

   ![](assets/trigger_uc_browse_12.png)

1. 언제든지 Experience Cloud 로그를 확인하여 트리거를 발생시킨 횟수를 확인할 수 있습니다.

   ![](assets/trigger_uc_browse_13.png)

1. Adobe Campaign 트리거 보고서를 표시할 수도 있습니다.

   ![](assets/trigger_uc_browse_14.png)

## Search abandonment Trigger {#search-abandonment-trigger}

이 사용 사례에서는 여행 예약 웹 사이트를 방문하고, 대상을 검색하고, 성공적인 결과를 찾을 수 없고 그 이후에는 어떤 것도 예약하지 않은 방문자로 재참여를 유도하는 트리거를 만들게 됩니다. The general process is the same as in the previous use case (see [Browse abandonment Trigger](../../integrating/using/abandonment-triggers-use-cases.md#browse-abandonment-trigger)). 리마케팅 이메일 메시지를 개인화하는 방법을 집중적으로 살펴보겠습니다.

### Creating an Experience Cloud Trigger {#creating-an-experience-cloud-trigger-1}

이전 사용 사례에 설명된 단계에 따라 Experience Cloud 트리거를 만듭니다. See [Creating an Experience Cloud Trigger](../../integrating/using/abandonment-triggers-use-cases.md#creating-an-experience-cloud-trigger). 주요 차이는 트리거 정의입니다.

![](assets/trigger_uc_search_1.png)

**[!UICONTROL Include Meta Data]** 이 섹션에서는 Analytics에서 수집한 데이터를 트리거 페이로드로 전달할 수 있습니다. 이 예에서는 사용자 지정 Evar (예: evar 3) 를 만들어 방문자가 입력하는 검색어를 수집합니다. 그러면 이 용어가 동일한 방문자에게 전송되는 트랜잭션 이메일 메시지에 사용됩니다.

### Using the trigger in Adobe Campaign {#using-the-trigger-in-adobe-campaign-1}

1. 이전 사용 사례에 설명된 단계에 따라 Adobe Campaign에서 트리거를 만듭니다. See [Using the trigger in Adobe Campaign](../../integrating/using/abandonment-triggers-use-cases.md#using-the-trigger-in-adobe-campaign). 주요 차이는 Adobe Campaign에서 트리거 페이로드로 푸시된 메타 데이터를 액세스하고 사용하는 방법입니다.
1. In the Search Abandonment trigger you created in Adobe Campaign, click on the **[!UICONTROL Event content and enrichment]** icon to view the payload pushed to Adobe Campaign.

   ![](assets/trigger_uc_search_2.png)

1. As you can see, the custom eVar is passed in the Trigger payload and mapped to the **Event Context** table (ctx). 이제 IT에 액세스하여 트랜잭션 메시지를 개인화할 수 있습니다.

   ![](assets/trigger_uc_search_3.png)

1. 이 예에서는 대상 검색어와 이메일 본문에 대상 검색어를 포함하기로 합니다.

   ![](assets/trigger_uc_search_4.png)

1. When selecting a personalized field, look for your payload meta data in the **Transactional event** (rtEvent) table then in the **Event context** (ctx) sub table.

   ![](assets/trigger_uc_search_5.png)

### Running the scenario {#running-the-scenario-1}

1. 방문자가 여행 예약 웹 사이트를 방문하여 대상을 검색합니다. 이 예에서는 방문자가 일본으로 여행을 가려고 하는데 결과가 없습니다. 이 경우 이 방문자를 다시 방문하고 대체 여행 계획을 제안할 수 있는 기회입니다.

   ![](assets/trigger_uc_search_6.png)

   >[!NOTE]
   >
   >이 사용 사례에서는 방문자/받는 사람이 동일한 웹 사이트에서 보낸 이메일을 이미 열어 클릭한 것으로 가정합니다. 이를 통해 Visitorid를 사용하고 수집하고 수신자에게 매핑할 수 있습니다. 한 번만 수행하면 됩니다.

1. 잠시 후, 동일한 방문자/받는 사람이 재마케팅 메시지를 받습니다. 메시지에는 최근 검색된 대상이 포함됩니다.

   ![](assets/trigger_uc_search_7.png)

