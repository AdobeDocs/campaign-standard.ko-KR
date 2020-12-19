---
solution: Campaign Standard
product: campaign
title: 워크플로우 세그먼트 기반 보고서 만들기
description: 보고서에서 워크플로우 세그먼트에 따라 배달의 성공을 확인하는 방법을 알아봅니다.
audience: reporting
content-type: reference
topic-tags: customizing-reports
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '617'
ht-degree: 2%

---


# 워크플로우 세그먼트 기반 보고서 만들기{#creating-a-report-workflow-segment}

워크플로우를 만들고 모집단을 다른 타깃팅된 대상자로 필터링한 후 이 타깃팅 워크플로우에 정의된 세그먼트를 기반으로 마케팅 캠페인의 효율성을 측정할 수 있습니다.
보고서에서 이러한 세그먼트를 타깃팅하려면:

* [1단계:세그먼트가 있는 프로필 사용자 지정 리소스 업데이트](#step-1--update-profiles-custom-resource-segments)
* [2단계:세그먼트가 있는 워크플로우 만들기](#step-2--create-a-workflow-segments)
* [3단계:세그먼트를 필터링하는 동적 보고서 만들기](#step-3--create-a-dynamic-report-filter-segments)

>[!CAUTION]
>이러한 데이터 수집을 시작하려면 동적 보고 사용 계약을 승인해야 합니다.
>이 계약에 대한 자세한 내용은 이 [페이지](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement)를 참조하십시오.

## 1단계:세그먼트{#step-1--update-profiles-custom-resource-segments}으로 프로필 사용자 지정 리소스 업데이트

세그먼트 코드에 대해 보고하기 전에 세그먼트 코드가 저장되도록 **[!UICONTROL Profiles]** 사용자 지정 리소스를 업데이트해야 합니다.

1. 고급 메뉴에서 Adobe Campaign 로고를 통해 **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Custom resources]**&#x200B;를 선택한 다음 **[!UICONTROL Profile (profile)]** 리소스를 선택합니다.
1. **[!UICONTROL Data structure]** 탭의 **[!UICONTROL Sending logs extension]** 메뉴에서 **[!UICONTROL Add segment code]**&#x200B;를 선택하여 타깃팅 워크플로우에서 세그먼트 코드를 저장할 수 있도록 하고 이를 동적 보고로 보냅니다.

   그러면 보고서의 **[!UICONTROL Profile]** 차원 섹션에서 **[!UICONTROL Segment code]**&#x200B;을 사용할 수 있습니다.

   ![](assets/report_segment_4.png)

1. 사용자 지정 리소스를 저장합니다.

1. 이제 사용자 지정 리소스를 게시해야 합니다.
고급 메뉴에서 **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Publishing]**&#x200B;를 선택합니다.

   ![](assets/custom_profile_7.png)

1. **[!UICONTROL Prepare publication]**&#x200B;을 클릭한 다음 준비가 완료되면 **[!UICONTROL Publish]** 단추를 클릭합니다. 사용자 지정 리소스에 대한 자세한 내용은 이 [페이지](../../developing/using/updating-the-database-structure.md)를 참조하십시오.

이제 세그먼트 코드로 워크플로우 만들기를 시작할 수 있습니다.

세그먼트 코드는 **[!UICONTROL Sending logs extension]**&#x200B;에서 세그먼트 코드를 활성화하는 즉시 수집됩니다.

## 2단계:{#step-2--create-a-workflow-segments} 세그먼트가 있는 워크플로우 만들기

>[!NOTE]
>이메일 배달의 입력 전환이 비어 있으면 이전 전환의 세그먼트 코드가 기본적으로 추가됩니다.

먼저 타게팅된 모집단 수가 다른 워크플로우를 만들어야 합니다. 다음은 대상자의 연령에 따라 개인화된 이메일을 보내려는 경우한 제품은 20~30년 된 프로파일에, 30~40년 된 프로파일에 대한 배송됩니다.

1. 워크플로우를 만듭니다. 워크플로우를 만드는 방법에 대한 자세한 내용은 이 [페이지](../../automating/using/building-a-workflow.md)를 참조하십시오.

1. 팔레트에서 **[!UICONTROL Query]** 활동을 드래그하여 작업 공간에 놓습니다.

1. 20~40세 사이의 Target 프로파일을 나중에 보다 타깃팅된 모집단으로 분류할 수 있습니다.

   ![](assets/report_segment_1.png)

1. **[!UICONTROL Segmentation]** 활동을 추가하여 쿼리 결과를 2개의 타깃팅된 모집단으로 분할합니다. 세그멘테이션에 대한 자세한 내용은 이 [페이지](../../automating/using/segmentation.md)를 참조하십시오.

1. **[!UICONTROL Segmentation]** 활동을 두 번 클릭하여 구성합니다. **[!UICONTROL Edit properties]**&#x200B;을 클릭하여 첫 번째 세그먼트를 편집합니다.

   ![](assets/report_segment_7.png)

1. 20세에서 30세 사이의 쿼리 프로필을 확인하고 완료되면 **[!UICONTROL Confirm]**&#x200B;을 클릭합니다.

   ![](assets/report_segment_8.png)

1. **[!UICONTROL Add an element]**&#x200B;을 클릭하여 두 번째 세그먼트를 만들고 위의 단계에 설명된 대로 구성하여 30세에서 40세 사이의 프로필을 타깃팅합니다.

1. 동적 보고를 통해 전달될 각 모집단에 대해 **[!UICONTROL Segment code]**&#x200B;을 편집합니다.

   >[!NOTE]
   >이 단계는 필수입니다. 그렇지 않으면 어떤 세그먼트가 보고될지 알 수 없습니다.

   ![](assets/report_segment_9.png)

1. 세그먼트 뒤에 **[!UICONTROL Email delivery]** 활동을 드래그하여 놓습니다.

   ![](assets/report_segment_3.png)

1. 서로 다른 타깃팅된 모집단에 따라 게재를 개인화합니다. 이메일 만들기에 대한 자세한 내용은 이 [페이지](../../designing/using/designing-content-in-adobe-campaign.md)를 참조하십시오.

1. 워크플로우를 저장합니다.

1. 워크플로우가 준비되면 **[!UICONTROL Start]**&#x200B;을 클릭합니다.

이제 보고서에 액세스하여 세그먼트 코드를 추적할 수 있습니다.

## 3단계:동적 보고서를 만들어 세그먼트 {#step-3--create-a-dynamic-report-filter-segments} 필터링

워크플로우로 배달을 보낸 후 워크플로우에서 세그먼트 코드를 사용하여 보고서를 분류할 수 있습니다.

1. **[!UICONTROL Reports]** 탭에서 기본 보고서를 선택하거나 **[!UICONTROL Create new project]** 단추를 클릭하여 보고서를 처음부터 시작합니다.

   ![](assets/custom_profile_18.png)
1. **[!UICONTROL Delivery]** 차원을 자유 형식 테이블로 드래그하여 놓습니다.

   ![](assets/report_segment_5.png)

1. 데이터 필터링을 시작하려면 **[!UICONTROL Open]** 및 **[!UICONTROL Click]** 지표와 같은 다른 지표를 테이블에 드래그 앤 드롭합니다.
1. **[!UICONTROL Dimensions]** 범주에서 **[!UICONTROL Profile]** 차원을 클릭한 다음 워크플로우의 배달에서 **[!UICONTROL Segment code]** 차원을 드래그하여 놓아 대상 모집단에 따라 이메일 배달의 성공을 측정합니다.

   ![](assets/report_segment_6.png)

1. 필요한 경우 작업 공간에 시각화를 드래그하여 놓습니다.

   ![](assets/report_segment_10.png)
