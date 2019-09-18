---
title: 포기 트리거 사용 사례
seo-title: 포기 트리거 사용 사례
description: 포기 트리거 사용 사례
seo-description: Experience Cloud Triggers 통합을 사용하는 방법을 알아봅니다.
page-status-flag: 활성화 안 함
uuid: 9e236165-afd5-4155-9151-c1941dc0af99
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 통합
content-type: reference
topic-tags: 작업-with-campaign-and-triggers
discoiquuid: 1b9aeec5-70bb-4d72-a3e9-12342abf08f7
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 4b69c92a8c877ecaf05e87b728009104066a38dc

---


# 포기 트리거 사용 사례{#abandonment-triggers-use-cases}

이 섹션에서는 Adobe Campaign과 Experience Cloud 트리거 간의 통합을 사용하여 구현할 수 있는 다양한 사용 사례를 제공합니다. 다음 두 가지 사용 사례를 확인할 수 있습니다.

* [포기 트리거 찾아보기](../../integrating/using/abandonment-triggers-use-cases.md#browse-abandonment-trigger):웹 사이트에서 방문을 포기한 고객에게 메시지를 보냅니다.
* [검색 포기 트리거](../../integrating/using/abandonment-triggers-use-cases.md#search-abandonment-trigger):웹 사이트에서 검색을 했지만 구매하지 않은 방문자와 다시 연결할 수 있습니다.

>[!NOTE]
>
>이 섹션에 설명된 사용 사례는 Experience Cloud 방문자 ID에 의존합니다. 또한 Experience Cloud 선언된 ID로 구현할 수도 있습니다. 해시되고 암호화된 선언된 ID도 지원됩니다. 암호화된 이메일 주소/모바일 번호를 직접 해독하여 이메일/SMS를 Campaign에 존재하지 않는 프로필로 보낼 수 있습니다. 하지만 이 경우 프로필 데이터를 사용한 개인화는 사용할 수 없습니다.

## 전제 조건 {#pre-requisites}

이러한 사용 사례를 구현하려면 다음 솔루션/핵심 서비스에 액세스할 수 있어야 합니다.

* Adobe Campaign
* Adobe Analytics Ultimate, Premium, Foundation, OD, Select, Prime, Mobile Apps, Select 또는 Standard.
* Experience Cloud 트리거 핵심 서비스
* Experience Cloud DTM 코어 서비스
* Experience Cloud 방문자 ID 및 Experience Cloud 사용자 코어 서비스

또한 웹 사이트가 필요합니다.

자세한 내용은 솔루션 [및 서비스](../../integrating/using/configuring-triggers-in-experience-cloud.md#configuring-solutions-and-services)구성을 참조하십시오.

## 포기 트리거 찾아보기 {#browse-abandonment-trigger}

이 사용 사례에서는 클라이언트가 웹 사이트의 방문을 중단할 때마다 실행되는 간단한 트리거를 만듭니다. 이 예에서는 DTM이 이미 데이터를 수집 및 Adobe Analytics로 푸시하고 있으며 모든 이벤트를 만들었다고 가정합니다.

### Experience Cloud 트리거 만들기 {#creating-an-experience-cloud-trigger}

1. Experience **[!UICONTROL Manage Triggers]** Cloud 활성화 코어 서비스 메뉴에서 선택합니다.

   ![](assets/trigger_uc_browse_1.png)

1. 트리거 유형(사용 **[!UICONTROL Abandonment]** 사례에서)을 선택합니다.

   ![](assets/trigger_uc_browse_2.png)

1. 이 사용 사례의 경우 간단한 포기 트리거가 필요합니다. 비즈니스 목적은 여행 예약 웹 사이트를 탐색하는 방문자를 식별하고 "거래" 페이지를 확인하되 여행을 예약하지 않는 것입니다. 이 고객을 식별하면 짧은 시간 내에 고객에게 다시 연락하고 싶습니다. 이 예에서는 10분 후에 트리거를 보내도록 선택합니다.

   ![](assets/trigger_uc_browse_3.png)

### Adobe Campaign에서 트리거 사용 {#using-the-trigger-in-adobe-campaign}

Adobe Experience Cloud Trigger를 만들었으므로 Adobe Campaign에서 사용해 보겠습니다.

Adobe Campaign에서 Experience Cloud에서 만든 트리거에 연결된 트리거를 만들어야 합니다.

1. Adobe Campaign에서 트리거를 만들려면 **[!UICONTROL Adobe Campaign]** 로고를 클릭하고 왼쪽 상단 모서리에서 **[!UICONTROL Marketing plans]** &gt; **[!UICONTROL Transactional messages]** &gt; **[!UICONTROL Experience Cloud triggers]**&#x200B;을 선택합니다.

   ![](assets/remarketing_1.png)

1. Click **[!UICONTROL Create]**.
1. 이전에 만든 트리거를 선택하고 을 **[!UICONTROL Next]**&#x200B;클릭합니다.

   ![](assets/trigger_uc_browse_5.png)

1. 채널과 **[!UICONTROL Email]** 타깃팅 **[!UICONTROL Real-time event]** 차원을 선택하고 을 클릭합니다 **[!UICONTROL Create]**.

   ![](assets/trigger_uc_browse_6bis.png)

1. Adobe Campaign에서 트리거를 게시합니다. 이 프로세스는 트랜잭션 메시지 템플릿을 자동으로 만듭니다.

   ![](assets/trigger_uc_browse_6.png)

1. 메시지 템플릿을 표시하려면 오른쪽 상단에서 **[!UICONTROL More]** 단추를 클릭한 다음 을 클릭합니다 **[!UICONTROL Trigger Transactional Template]**.

1. 컨텐츠 및 발신자 세부 사항을 개인화합니다.

   ![](assets/trigger_uc_browse_8.png)

1. 메시지 템플릿을 게시합니다. 이제 트리거가 실시간으로 작동합니다.

   ![](assets/trigger_uc_browse_0.png)

### 시나리오 실행 {#running-the-scenario}

1. 이 사용 사례는 Adobe Campaign을 통해 고객에게 보낸 초기 이메일에서 시작됩니다.

   ![](assets/trigger_uc_browse_9.png)

1. 수신자가 이메일을 엽니다.

   ![](assets/trigger_uc_browse_10.png)

1. 웹 사이트로 연결되는 링크를 클릭합니다. 이 예에서는 배너가 받는 사람을 여행 예약 웹 사이트의 홈 페이지로 가져옵니다.

   ![](assets/trigger_uc_browse_11.png)

1. 수신자는 "거래" 페이지로 이동하지만 갑자기 방문을 중지합니다. 10분 기간이 지나면 Adobe Campaign에서 트랜잭션 메시지 전송을 트리거합니다.

   ![](assets/trigger_uc_browse_12.png)

1. 언제든지 Experience Cloud 로그를 확인하여 트리거가 실행된 횟수를 확인할 수 있습니다.

   ![](assets/trigger_uc_browse_13.png)

1. Adobe Campaign 트리거 보고서를 표시할 수도 있습니다.

   ![](assets/trigger_uc_browse_14.png)

## 검색 포기 트리거 {#search-abandonment-trigger}

이 사용 사례에서는 여행 예약 웹 사이트를 방문하고, 대상을 검색하고, 성공적인 결과를 찾지 못했으며, 그 이후에 예약하지 않은 방문자와 다시 연결할 수 있는 트리거를 만들 것입니다. 일반 프로세스는 이전 사용 사례와 동일합니다(검색 포기 트리거 [참조](../../integrating/using/abandonment-triggers-use-cases.md#browse-abandonment-trigger)). 리마케팅 이메일 메시지를 개인화하는 방법에 초점을 맞출 것입니다.

### Experience Cloud 트리거 만들기 {#creating-an-experience-cloud-trigger-1}

Experience Cloud Trigger를 만들려면 이전 사용 사례에 설명된 단계를 따르십시오. Experience [Cloud 트리거 만들기를 참조하십시오](../../integrating/using/abandonment-triggers-use-cases.md#creating-an-experience-cloud-trigger). 주요 차이점은 트리거 정의입니다.

![](assets/trigger_uc_search_1.png)

이 **[!UICONTROL Include Meta Data]** 섹션에서는 Analytics에서 수집한 데이터를 트리거 페이로드로 전달할 수 있습니다. 이 예에서는 사용자 지정 eVar(예: eVar 3)를 만들어 방문자가 입력하는 검색어를 수집합니다. 이 용어는 동일한 방문자에게 전송되는 트랜잭션 이메일 메시지에서 사용됩니다.

### Adobe Campaign에서 트리거 사용 {#using-the-trigger-in-adobe-campaign-1}

1. Adobe Campaign에서 트리거를 만들려면 이전 사용 사례에 설명된 단계를 따르십시오. Adobe [Campaign에서 트리거 사용을 참조하십시오](../../integrating/using/abandonment-triggers-use-cases.md#using-the-trigger-in-adobe-campaign). 주요 차이점은 Adobe Campaign에서 트리거 페이로드에서 푸시된 메타 데이터에 액세스하고 사용하는 방법입니다.
1. Adobe Campaign에서 만든 검색 포기 트리거에서 아이콘을 클릭하여 Adobe Campaign으로 푸시된 페이로드를 봅니다. **[!UICONTROL Event content and enrichment]**

   ![](assets/trigger_uc_search_2.png)

1. 보시다시피 사용자 지정 eVar가 트리거 페이로드에서 전달되고 이벤트 컨텍스트 **테이블(ctx** )에 매핑됩니다. 이제 Adobe는 이를 통해 트랜잭션 메시지를 개인화할 수 있습니다.

   ![](assets/trigger_uc_search_3.png)

1. 이 예에서는 대상 검색어를 제목 줄뿐만 아니라 이메일 본문에도 포함하도록 선택합니다.

   ![](assets/trigger_uc_search_4.png)

1. 개인화된 필드를 선택할 때 페이로드 메타 데이터를 트랜잭션 이벤트 **(rtEvent) 테이블에서 찾은 다음 이벤트 컨텍스트** (ctx **)** 하위 테이블에서 찾습니다.

   ![](assets/trigger_uc_search_5.png)

### 시나리오 실행 {#running-the-scenario-1}

1. 방문자는 여행 예약 웹 사이트를 방문하여 대상을 검색합니다. 이 예에서는 방문자가 일본 여행을 찾고 있지만 결과를 찾지 못했습니다. 이 기회를 통해 이 방문자에게 다시 연락하여 대체 여행 계획을 추천할 수 있습니다.

   ![](assets/trigger_uc_search_6.png)

   >[!NOTE]
   >
   >이 사용 사례에서는 방문자/수신자가 동일한 웹 사이트에서 보낸 이메일을 이미 열고 클릭했다고 가정합니다. 이를 통해 VisitorID를 사용하고 수집하여 수신자에게 매핑할 수 있습니다. 한 번만 하면 돼

1. 잠시 후 동일한 방문자/수신자가 리마케팅 메시지를 받습니다. 메시지에 최근에 검색된 대상이 포함됩니다.

   ![](assets/trigger_uc_search_7.png)

