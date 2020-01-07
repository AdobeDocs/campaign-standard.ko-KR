---
title: '"워크플로우 사용 사례:크로스 채널 전달"'
description: '"워크플로우 사용 사례:크로스 채널 전달"'
page-status-flag: never-activated
uuid: 396a3de1-6ffa-4385-ac9f-15fdeae5a366
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities
discoiquuid: 377821e6-69f8-41cc-a1ad-8a2f5ed4d409
context-tags: workflow,use-case,query,wait,delivery
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 8f0460eeadb388fef2a3304623086afd36e68962

---


# 워크플로우 사용 사례:크로스 채널 배달 만들기{#cross-channel-delivery}

이 문서에서는 표준 사용 사례를 통해 다음과 같은 Adobe Campaign 기능을 검색할 수 있습니다.크로스 채널 전달 워크플로우 만들기

여기서 목표는 데이터베이스의 받는 사람 중에서 대상을 선택하고 첫 번째 그룹에 이메일을 보내고 두 번째 그룹에 SMS 메시지를 보내기 위해 두 개의 다른 그룹으로 나누는 것입니다.

![](assets/wkf_segment_overview.png)

워크플로우와 Adobe Campaign에서 사용할 수 있는 다양한 채널에 대한 자세한 내용은 다음 문서를 참조하십시오.

* [워크플로우 살펴보기](../../automating/using/discovering-workflows.md)
* [소통 채널](../../channels/using/discovering-communication-channels.md)

## 워크플로우 만들기 {#creating-workflow}

지정된 그룹에 두 개의 다른 배달을 보내려면 먼저 대상을 정의해야 합니다.

이렇게 하려면 수신자를 식별하는 쿼리를 만들어야 하므로 워크플로우를 만들어야 합니다.

프로그램 또는 원하는 캠페인에서 새 워크플로우를 만듭니다.

1. 에서 **[!UICONTROL Marketing Activities]**을 클릭하고**[!UICONTROL Create]** 선택합니다 **[!UICONTROL Workflow]**.
1. 워크플로우 **[!UICONTROL New Workflow]**유형으로 선택하고 을 클릭합니다**[!UICONTROL Next]**.
1. 워크플로우의 속성을 입력하고 을 클릭합니다 **[!UICONTROL Create]**.

워크플로우 [](../../automating/using/building-a-workflow.md) 만들기에 대한 자세한 단계는 워크플로우 작성 섹션에 나와 있습니다.

## 쿼리 활동 만들기 {#creating-query-activity}

워크플로우가 만들어지면 해당 인터페이스에 액세스할 수 있습니다.

워크플로우에 쿼리 활동을 삽입하여 배달을 받을 프로파일을 타깃팅합니다.

1. > **[!UICONTROL Activities]**에서**[!UICONTROL Targeting]**&#x200B;드래그하여 **[!UICONTROL Query activity]**놓습니다.
1. 활동을 두 번 클릭합니다.
1. 탭에서 단축키를 **[!UICONTROL Target]**탐색하고[대상자](../../audiences/using/about-audiences.md)중 하나를 선택합니다.
1. 단축키를 편집 영역으로 드래그하여 놓습니다. 선택한 단축키 유형에 따라 창이 나타납니다.
1. 타깃팅 요소를 구성한 다음 쿼리를 확인합니다.

![](assets/wkf_segment_query.png)

하나 또는 여러 요소에 대해 쿼리를 만들 수 있습니다.

이 **[!UICONTROL Count]**단추를 사용하여 쿼리를 기준으로 타깃팅된 프로필 수를 예측할 수 있습니다.

쿼리 활동을 작성하기 위한 자세한 단계는 쿼리 [섹션에 나와](../../automating/using/query.md) 있습니다.

## 세그멘테이션 활동 만들기 {#creating-segmentation-activity}

질의 활동으로 대상이 식별되면, 대상을 두 개의 다른 모집단으로 세그먼트화하는 기준을 선택해야 합니다.한 사람은 이메일을 받고 다른 한 사람은 문자 메시지를 수신하게 됩니다.

쿼리의 업스트림 계산에서 하나 또는 여러 세그먼트를 만들려면 세그멘테이션 활동을 사용해야 합니다.

![](assets/wkf_segment_activity.png)

이메일 **그룹은** 이메일 주소가 정의되어 있지만 모바일 전화 번호가 없는 수신자를 타깃팅합니다. SMS **그룹에는** 모바일 전화 번호가 프로필에 저장된 수신자가 포함됩니다.

첫 번째 전환(이메일)을 구성하려면:

1. 탭에서 기본적으로 첫 번째 세그먼트가 **[!UICONTROL Segments]**있습니다. 속성을 편집하여 해당 세그먼트를 구성합니다.

   ![](assets/wkf_segment_properties.png)

1. 프로필의 필터링 기준을 **[!UICONTROL Email]**선택합니다.

   ![](assets/wkf_segment_email.png)

1. 화면에 표시되는 새 창에서 **[!UICONTROL Is not empty]**연산자를 선택합니다.

   ![](assets/wkf_segment_email_not_empty.png)

1. 두 번째 필터링 기준을 추가하고 **[!UICONTROL Mobile]**연산자를**[!UICONTROL Is empty]**&#x200B;선택합니다.

   ![](assets/wkf_segment_mobile_empty.png)

   이메일이 있지만 정의된 모바일 전화 번호가 아닌 쿼리에서 오는 모든 프로필은 이 전환입니다.

1. 워크플로우를 보다 명확하게 하기 위해 전환 레이블을 편집할 수 있습니다. 변경 사항을 확인합니다.

   ![](assets/wkf_segment_transition_label.png)

첫 번째 전환이 구성됩니다. 두 번째 전환(SMS)을 구성하려면:

1. 새 전환을 추가하려면 **[!UICONTROL Add an element]**단추를 클릭합니다.
1. 휴대폰 번호가 제공된 모든 프로파일을 검색할 수 있는 조건을 정의합니다. 이렇게 하려면 **[!UICONTROL Mobile]**논리 연산자가 있는**[!UICONTROL Is not empty]** 필드에 규칙을 만듭니다.

   ![](assets/wkf_segment_mobile_not_empty.png)

   모바일 전화 번호가 정의된 쿼리에서 들어오는 모든 프로필은 이 전환에서 가져옵니다.

1. 전환 레이블을 편집할 수 있습니다. 변경 사항을 확인합니다.

이제 두 번째 전환도 구성됩니다.

![](assets/wkf_segment_transitions.png)

세그멘테이션 활동을 작성하는 자세한 단계는 세그멘테이션 [섹션에](../../automating/using/segmentation.md) 설명되어 있습니다.

## 배달 만들기 {#creating-deliveries}

두 개의 전환이 이미 생성되었으므로 이제 두 가지 유형의 전달을 세그멘테이션 활동의 아웃바운드 전환에 추가해야 합니다.an and **[!UICONTROL Email delivery]**an**[!UICONTROL SMS delivery]**.

Adobe Campaign을 사용하면 워크플로우에 배달을 추가할 수 있습니다. 이렇게 하려면 워크플로우 활동 팔레트의 **[!UICONTROL Channels]**범주에서 배달을 선택합니다.

![](assets/wkf_segment_deliveries1.png)

이메일 배달을 만들려면

1. 첫 번째 세그먼트 **[!UICONTROL Email delivery]**다음에 를 드래그하여 놓습니다.
1. 활동을 두 번 클릭하여 편집합니다.
1. 을 **[!UICONTROL Simple email]**선택합니다.
1. 을 선택하고 **[!UICONTROL Add an outbound transition with the population]**클릭합니다**[!UICONTROL Next]**.

   ![](assets/wkf_segment_deliveries2.png)

   아웃바운드 전환을 사용하면 모집단 및 추적 로그를 복구할 수 있습니다. 예를 들어, 첫 번째 메일을 클릭하지 않은 사람에게 두 번째 메일을 보낼 수 있습니다.

1. 이메일 템플릿을 선택하고 을 **[!UICONTROL Next]**클릭합니다.
1. 이메일 속성을 입력하고 을 **[!UICONTROL Next]**클릭합니다.
1. 이메일 레이아웃을 만들려면 을 **[!UICONTROL Use the Email Designer]**선택합니다.
1. 컨텐츠를 편집하고 저장할 수 있습니다.
1. 메시지 대시보드의 **[!UICONTROL Schedule]**섹션에서 메시지를 보내기 전에**[!UICONTROL 요청 확인]**옵션을 선택 취소합니다.

이메일 활동을 작성하는 자세한 단계는 이메일 배달 [섹션에](../../automating/using/email-delivery.md) 설명되어 있습니다.

SMS 배달을 만들려면

1. 다른 세그먼트 **[!UICONTROL SMS delivery]**다음에 드래그하여 놓습니다.
1. 활동을 두 번 클릭하여 편집합니다.
1. 을 선택하고 **[!UICONTROL SMS]**클릭합니다**[!UICONTROL Next]**.
1. SMS 템플릿을 선택하고 을 **[!UICONTROL Next]**클릭합니다.
1. SMS 속성을 입력하고 을 **[!UICONTROL Next]**클릭합니다.
1. 컨텐츠를 편집하고 저장할 수 있습니다.

SMS 활동을 빌드하기 위한 자세한 단계는 SMS [배달](../../automating/using/sms-delivery.md) 섹션에 나와 있습니다.

게재를 만들고 편집한 후에는 워크플로우를 시작할 준비가 되었습니다.

![](assets/wkf_segment_deliveries.png)

## 워크플로우 실행 {#running-the-workflow}

워크플로우가 시작되면 쿼리 활동이 타깃팅한 모집단이 이메일 또는 SMS 배달을 수신하도록 세그먼트화됩니다.

워크플로우를 실행하려면 작업 표시줄에서 **[!UICONTROL Start]**단추를 클릭합니다.

Adobe Campaign 로고를 통해 **[!UICONTROL Marketing plans]**>**[!UICONTROL Marketing activities]** 고급 메뉴에서 게재에 액세스할 수 있습니다. 배달 단추를 클릭한 다음 **[!UICONTROL Reports]**단추를 클릭하여 받는 사람의 메시지 받은 편지함에 따라 배달 요약, 열림 비율 또는 이메일 렌더링과 같은[배달 보고서에](../../reporting/using/about-dynamic-reports.md#accessing-dynamic-reports)액세스합니다.