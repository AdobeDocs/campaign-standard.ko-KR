---
title: 워크플로우 세그먼트 기반 보고서 만들기
description: 보고서에 있는 워크플로우 세그먼트에 따라 게재의 성공을 확인하는 방법을 알아봅니다.
audience: reporting
content-type: reference
topic-tags: customizing-reports
feature: Reporting
role: Leader
level: Intermediate
exl-id: 514bffa0-2413-4212-b1b9-e070031c462f
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '624'
ht-degree: 2%

---

# 워크플로우 세그먼트 기반 보고서 만들기{#creating-a-report-workflow-segment}

>[!CAUTION]
> **[!UICONTROL Segment code]**은 이메일 및 SMS 게재만 타겟팅할 수 있습니다.

워크플로우를 만들고 모집단을 다른 타겟팅된 대상으로 필터링한 후 이 타겟팅 워크플로우에 정의된 세그먼트를 기반으로 마케팅 캠페인의 효율성을 측정할 수 있습니다.
보고서에서 이러한 세그먼트를 타깃팅하려면 다음을 수행하십시오.

* [1단계: 세그먼트로 프로필 사용자 지정 리소스 업데이트](#step-1--update-profiles-custom-resource-segments)
* [2단계: 세그먼트로 워크플로우 만들기](#step-2--create-a-workflow-segments)
* [3단계: 동적 보고서를 만들어 세그먼트 필터링](#step-3--create-a-dynamic-report-filter-segments)

>[!CAUTION]
>이러한 데이터를 수집하려면 동적 보고 사용 계약서를 승인해야 합니다.
>
>이 계약에 대한 자세한 내용은 다음을 참조하십시오 [페이지](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement).

## 1단계: 세그먼트로 프로필 사용자 지정 리소스 업데이트{#step-1--update-profiles-custom-resource-segments}

세그먼트 코드에 대해 보고하기 전에 **[!UICONTROL Profiles]** 저장할 세그먼트 코드의 사용자 지정 리소스입니다.

1. 고급 메뉴에서 Adobe Campaign 로고를 통해 을(를) 선택합니다 **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Custom resources]**&#x200B;를 선택한 다음, **[!UICONTROL Profile (profile)]** 리소스 를 참조하십시오.
1. 에서 **[!UICONTROL Sending logs extension]** 메뉴에서 **[!UICONTROL Data structure]** 탭, 확인 **[!UICONTROL Add segment code]** 타깃팅 워크플로우에서 세그먼트 코드를 저장하고 다이내믹 보고로 전송할 수 있도록 해줍니다.

   다음 **[!UICONTROL Segment code]** 다음에 사용 가능합니다. **[!UICONTROL Profile]** 보고서의 차원 섹션.

   ![](assets/report_segment_4.png)

1. 사용자 지정 리소스를 저장합니다.

1. 이제 사용자 지정 리소스를 게시해야 합니다.
고급 메뉴에서 **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Publishing]**.

   ![](assets/custom_profile_7.png)

1. 클릭 **[!UICONTROL Prepare publication]** 준비가 완료되면 **[!UICONTROL Publish]** 버튼을 클릭합니다. 사용자 지정 리소스에 대한 자세한 내용은 다음을 참조하십시오 [페이지](../../developing/using/updating-the-database-structure.md).

이제 세그먼트 코드로 워크플로우 만들기를 시작할 수 있습니다.

세그먼트 코드는 **[!UICONTROL Sending logs extension]**.

## 2단계: 세그먼트로 워크플로우 만들기 {#step-2--create-a-workflow-segments}

>[!NOTE]
>이메일 게재의 입력 전환이 비어 있는 경우, 기본적으로 이전 전환의 세그먼트 코드가 추가됩니다.

먼저 타겟팅된 모집단이 다른 워크플로우를 만들어야 합니다. 여기서는 대상자의 나이에 따라 개인화된 이메일을 보내려고 합니다. 한 게재는 20~30세 프로필에 대해, 30~40세 프로필에 대해 각각 제공됩니다.

1. 워크플로우를 만듭니다. 워크플로우를 만드는 방법에 대한 자세한 내용은 다음을 참조하십시오 [페이지](../../automating/using/building-a-workflow.md).

1. 추가 **[!UICONTROL Query]** 활동을 팔레트에서 끌어서 작업 영역에 놓아 놓습니다.

1. Target 프로필은 20~40세 사이이며 나중에 더 타겟팅된 모집단으로 분류할 수 있습니다.

   ![](assets/report_segment_1.png)

1. 추가 **[!UICONTROL Segmentation]** 활동을 통해 쿼리 결과를 두 개의 타깃팅된 모집단으로 분할합니다. 세그멘테이션에 대한 자세한 내용은 다음을 참조하십시오 [페이지](../../automating/using/segmentation.md).

1. 을(를) 두 번 클릭합니다. **[!UICONTROL Segmentation]** 활동을 구성하여 구성하도록 합니다. 다음 아이콘을 클릭하여 첫 번째 세그먼트 편집 **[!UICONTROL Edit properties]**.

   ![](assets/report_segment_7.png)

1. 20~30세 사이의 프로필 쿼리 및 클릭 **[!UICONTROL Confirm]** 완료 시.

   ![](assets/report_segment_8.png)

1. 클릭 **[!UICONTROL Add an element]** 두 번째 세그먼트를 만들고 30세에서 40세 사이의 프로필을 타겟팅하도록 위의 단계에 설명된 대로 구성합니다.

1. 편집 **[!UICONTROL Segment code]** 동적 보고를 통해 전달할 각 모집단에 대해 설명합니다.

   >[!NOTE]
   >이 단계는 필수입니다. 그렇지 않으면 어떤 세그먼트에 대해 보고할지 알 수 없습니다.

   ![](assets/report_segment_9.png)

1. 끌어서 놓기 **[!UICONTROL Email delivery]** 활동 을 만들 수 있습니다.

   ![](assets/report_segment_3.png)

1. 타겟팅된 다양한 모집단에 따라 게재를 개인화합니다. 전자 메일 만들기에 대한 자세한 내용은 다음을 참조하십시오 [페이지](../../designing/using/designing-content-in-adobe-campaign.md).

1. 워크플로우를 저장합니다.

1. 클릭 **[!UICONTROL Start]** 워크플로우가 준비되면 됩니다.

이제 보고서에 액세스하여 세그먼트 코드를 추적할 수 있습니다.

## 3단계: 동적 보고서를 만들어 세그먼트 필터링 {#step-3--create-a-dynamic-report-filter-segments}

워크플로우로 게재를 보낸 후, 워크플로우의 세그먼트 코드를 사용하여 보고서를 분류할 수 있습니다.

1. 에서 **[!UICONTROL Reports]** 탭에서 기본 제공 보고서를 선택하거나 **[!UICONTROL Create new project]** 단추를 눌러 처음부터 시작합니다.

   ![](assets/custom_profile_18.png)
1. 을(를) 끌어다 놓습니다 **[!UICONTROL Delivery]** 차원을 자유 형식 테이블에 추가합니다.

   ![](assets/report_segment_5.png)

1. 다른 지표를 테이블(예: )에 드래그하여 놓습니다 **[!UICONTROL Open]** 및 **[!UICONTROL Click]** 지표 를 사용하여 데이터 필터링을 시작합니다.
1. 에서 **[!UICONTROL Dimensions]** 카테고리에서 **[!UICONTROL Profile]** 차원을 드래그한 다음 **[!UICONTROL Segment code]** 타겟팅된 모집단에 따라 이메일 게재의 성공을 측정하기 위한 워크플로우 게재의 차원입니다.

   ![](assets/report_segment_6.png)

1. 필요한 경우 작업 공간에서 시각화를 끌어서 놓습니다.

   ![](assets/report_segment_10.png)
