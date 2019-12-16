---
title: 워크플로우 세그먼트 기반 보고서 만들기
description: 보고서에서 워크플로우 세그먼트에 따라 게재의 성공을 확인하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: f75e005b-5328-4c98-9e78-51d54fd0e246
contentOwner: beneat
products: SG_CAMPAIGN/STANDARD
audience: reporting
content-type: reference
topic-tags: customizing-reports
discoiquuid: b6d3de63-3add-4881-8917-04a6f8b6be4d
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 1b70e18be29fd48d102313f6d741e9ffe053cc34

---


# 워크플로우 세그먼트 기반 보고서 만들기{#creating-a-report-workflow-segment}

워크플로우를 만들고 인구를 다른 타깃팅된 대상으로 필터링한 후 이 타깃팅 워크플로우에 정의된 세그먼트를 기반으로 마케팅 캠페인의 효율성을 측정할 수 있습니다.
보고서에서 이러한 세그먼트를 타게팅하려면:

* [1단계:세그먼트로 프로필 사용자 지정 리소스 업데이트](#step-1--update-profiles-custom-resource-segments)
* [2단계:세그먼트가 있는 워크플로우 만들기](#step-2--create-a-workflow-segments)
* [3단계:동적 보고서를 만들어 세그먼트 필터링](#step-3--create-a-dynamic-report-filter-segments)

>[!CAUTION]
>이러한 데이터 수집을 시작하려면 동적 보고 사용 계약을 수락해야 합니다.
>본 계약에 대한 자세한 내용은 이 [페이지를](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement)참조하십시오.

## 1단계:세그먼트로 프로필 사용자 지정 리소스 업데이트{#step-1--update-profiles-custom-resource-segments}

세그먼트 코드에 대해 보고하기 전에 세그먼트 코드가 저장될 사용자 지정 리소스를 업데이트해야 합니다. **[!UICONTROL Profiles]**

1. 고급 메뉴에서 Adobe Campaign 로고를 통해 **[!UICONTROL Administration]** &gt; **[!UICONTROL Development]** &gt; **[!UICONTROL Custom resources]**&#x200B;을 선택한 다음 **[!UICONTROL Profile (profile)]** 리소스를 선택합니다.
1. 탭의 **[!UICONTROL Sending logs extension]** 메뉴에서 **[!UICONTROL Data structure]** 세그먼트 코드의 저장 **[!UICONTROL Add segment code]** 허용을 선택하고 이를 동적 보고로 보냅니다.

   그런 **[!UICONTROL Segment code]** 다음 보고서의 **[!UICONTROL Profile]** 차원 섹션에서 사용할 수 있습니다.

   ![](assets/report_segment_4.png)

1. 사용자 지정 리소스를 저장합니다.

1. 이제 사용자 지정 리소스를 게시해야 합니다.
고급 메뉴에서 **[!UICONTROL Administration]** &gt; **[!UICONTROL Development]** &gt; **[!UICONTROL Publishing]**&#x200B;를 선택합니다.

   ![](assets/custom_profile_7.png)

1. 을 **[!UICONTROL Prepare publication]** 클릭하고 준비가 완료되면 **[!UICONTROL Publish]** 단추를 클릭합니다. 사용자 지정 리소스에 대한 자세한 내용은 이 [페이지를](../../developing/using/updating-the-database-structure.md)참조하십시오.

이제 세그먼트 코드로 워크플로우를 만들 수 있습니다.

세그먼트 코드는 에서 세그먼트 코드를 활성화하면 바로 수집됩니다 **[!UICONTROL Sending logs extension]**.

## 2단계:세그먼트가 있는 워크플로우 만들기 {#step-2--create-a-workflow-segments}

>[!NOTE]
>이메일 배달의 입력 전환이 비어 있으면 이전 전환의 세그먼트 코드가 기본적으로 추가됩니다.

먼저 타깃팅된 모집단과 다른 워크플로우를 만들어야 합니다. 고객 연령에 따라 개인화된 이메일을 보내려고 합니다.한 제품은 20~30년 프로파일을 바탕으로 전달되며, 한 제품은 30~40년 프로파일을 바탕으로 판매됩니다.

1. 워크플로우 구축 워크플로우를 만드는 방법에 대한 자세한 내용은 이 [페이지를](../../automating/using/building-a-workflow.md)참조하십시오.

1. 팔레트에서 **[!UICONTROL Query]** 활동을 드래그하여 작업 공간에 놓습니다.

1. 20~40년 된 프로파일을 타겟팅하여 더 많은 타겟팅된 모집단으로 세분화할 수 있습니다.

   ![](assets/report_segment_1.png)

1. 활동을 추가하여 쿼리 결과를 두 개의 타깃팅된 모집단으로 분할합니다. **[!UICONTROL Segmentation]** 세그멘테이션에 대한 자세한 내용은 이 [페이지를](../../automating/using/targeting-data.md#segmenting-data)참조하십시오.

1. 활동을 두 번 클릭하여 **[!UICONTROL Segmentation]** 구성합니다. 을 클릭하여 첫 번째 세그먼트를 편집합니다 **[!UICONTROL Edit properties]**.

   ![](assets/report_segment_7.png)

1. 20세에서 30세 사이의 쿼리 프로필을 확인하고 **[!UICONTROL Confirm]** 완료되면 클릭합니다.

   ![](assets/report_segment_8.png)

1. 두 번째 세그먼트를 **[!UICONTROL Add an element]** 만들고 위 단계에 설명된 대로 구성하여 30세에서 40세 사이의 프로파일을 타깃팅합니다.

1. 동적 보고를 통해 전달될 각 모집단 **[!UICONTROL Segment code]** 수를 편집합니다.

   >[!NOTE]
   >이 단계는 필수입니다. 그렇지 않으면 어떤 세그먼트를 보고해야 하는지 이해할 수 없습니다.

   ![](assets/report_segment_9.png)

1. 세그먼트 후에 **[!UICONTROL Email delivery]** 활동을 드래그하여 놓습니다.

   ![](assets/report_segment_3.png)

1. 타깃팅된 모집단에 따라 게재를 개인화합니다. 이메일 생성에 대한 자세한 내용은 이 [페이지를](../../designing/using/designing-content-in-adobe-campaign.md)참조하십시오.

1. 워크플로우를 저장합니다.

1. 워크플로우가 준비되면 **[!UICONTROL Start]** 클릭합니다.

이제 보고서에 액세스하여 세그먼트 코드를 추적할 수 있습니다.

## 3단계:동적 보고서를 만들어 세그먼트 필터링 {#step-3--create-a-dynamic-report-filter-segments}

워크플로우와 함께 배달을 보낸 후 워크플로우에서 세그먼트 코드를 사용하여 보고서를 분류할 수 있습니다.

1. 탭에서 기본 보고서를 **[!UICONTROL Reports]** 선택하거나 **[!UICONTROL Create new project]** 단추를 클릭하여 보고서를 처음부터 시작합니다.

   ![](assets/custom_profile_18.png)
1. 자유 형식 테이블로 **[!UICONTROL Delivery]** 차원을 드래그하여 놓습니다.

   ![](assets/report_segment_5.png)

1. 데이터 필터링을 시작하려면 표 **[!UICONTROL Open]** 및 **[!UICONTROL Click]** 지표와 같은 다른 지표를 끌어다 놓습니다.
1. 카테고리에서 **[!UICONTROL Dimensions]** 차원을 클릭한 다음 **[!UICONTROL Profile]** **[!UICONTROL Segment code]** 차원을 워크플로우 전달에 끌어다 놓아 타깃팅된 모집단에 따라 이메일 게재의 성공을 측정할 수 있습니다.

   ![](assets/report_segment_6.png)

1. 필요한 경우 작업 영역에 시각화를 드래그하여 놓습니다.

   ![](assets/report_segment_10.png)
