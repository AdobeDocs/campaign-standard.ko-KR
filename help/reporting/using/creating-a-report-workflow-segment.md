---
title: 워크플로우 세그먼트를 기반으로 보고서 만들기
seo-title: 워크플로우 세그먼트를 기반으로 보고서 만들기
description: 워크플로우 세그먼트를 기반으로 보고서 만들기
seo-description: 보고서에서 워크플로우의 세그먼트에 따라 배달의 성공 여부를 확인하는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: F 75 E 005 B -5328-4 C 98-9 E 78-51 D 54 FD 0 E 246
contentOwner: Beneat
products: sg_ campaign/standard
audience: 보고
content-type: 참조
topic-tags: 사용자 지정 보고서
discoiquuid: B 6 D 3 DE 63-3 Add -4881-8917-04 A 6 F 8 B 6 BE 4 D
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: c555c35004ffe3c3d7e2f845a3a2707b1985e190

---


# Creating a report based on workflow segments{#creating-a-report-workflow-segment}

워크플로우를 만들고 모집단을 다른 대상화된 대상에 필터링한 후 타깃팅 워크플로우에 정의된 세그먼트를 기반으로 마케팅 캠페인의 효율성을 측정할 수 있습니다.
보고서에서 이러한 세그먼트를 타깃팅하려면:

* [1 단계: 세그먼트를 사용하여 프로필 사용자 지정 리소스 업데이트](#step-1--update-profiles-custom-resource-segments)
* [2 단계: 세그먼트를 사용하여 워크플로우 만들기](#step-2--create-a-workflow-segments)
* [3 단계: 세그먼트를 필터링하는 동적 보고서 만들기](#step-3--create-a-dynamic-report-filter-segments)

>[!CAUTION]
>이러한 데이터를 수집하기 시작하려면 동적 보고 사용 계약을 수락해야 합니다.
>For more on this agreement, refer to this [page](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement).

## Step 1: Update Profiles custom resource with segments{#step-1--update-profiles-custom-resource-segments}

Before reporting on your segment code, you need to update your **[!UICONTROL Profiles]** custom resource for your segment codes to be stored.

1. From the advanced menu, via the Adobe Campaign logo, select **[!UICONTROL Administration]** &gt; **[!UICONTROL Development]** &gt; **[!UICONTROL Custom resources]**, then select the **[!UICONTROL Profile (profile)]** resource.
1. In the **[!UICONTROL Sending logs extension]** menu from the **[!UICONTROL Data structure]** tab, check **[!UICONTROL Add segment code]** to allow storage of your segment codes from targeting workflows and to send it to dynamic reporting.

   The **[!UICONTROL Segment code]** will then be available in the **[!UICONTROL Profile]** dimension section of your report.

   ![](assets/report_segment_4.png)

1. 사용자 지정 리소스를 저장합니다.

1. 이제 사용자 지정 리소스를 게시해야 합니다.
From the advanced menu, select **[!UICONTROL Administration]** &gt; **[!UICONTROL Development]** &gt; **[!UICONTROL Publishing]**.

   ![](assets/custom_profile_7.png)

1. Click **[!UICONTROL Prepare publication]** then when the preparation is done, click the **[!UICONTROL Publish]** button. For more information on custom resource, refer to this [page](../../developing/using/updating-the-database-structure.md).

이제 세그먼트 코드로 워크플로우 만들기를 시작할 수 있습니다.

Note that segment codes will be collected as soon as you enable the segment code in the **[!UICONTROL Sending logs extension]**.

## Step 2: Create a workflow with segments {#step-2--create-a-workflow-segments}

>[!NOTE]
>이메일 게재의 입력 전환이 비어 있으면 이전 전환의 세그먼트 코드가 기본적으로 추가됩니다.

먼저 타깃팅된 다른 모집단을 사용하여 워크플로우를 만들어야 합니다. 여기에는 고객의 연령에 따라 개인화된 이메일을 보내드립니다. 프로파일은 20 ~ 30 세, 프로파일은 30 ~ 40 세 범위에 해당합니다.

1. 워크플로우 구축 For more details on how to create your workflow, refer to this [page](../../automating/using/building-a-workflow.md).

1. Add a **[!UICONTROL Query]** activity by dragging it from the palette and dropping it in the workspace.

1. 20 ~ 40 세의 프로파일을 바탕으로 보다 타겟팅된 모집단으로 세분화할 수 있습니다.

   ![](assets/report_segment_1.png)

1. Add a **[!UICONTROL Segmentation]** activity to split your query results into two targeted populations. For more on segmentation, refer to this [page](../../automating/using/targeting-data.md#segmenting-data).

1. **[!UICONTROL Segmentation]** 활동을 두 번 클릭하여 구성합니다. Edit the first segment by clicking **[!UICONTROL Edit properties]**.

   ![](assets/report_segment_7.png)

1. Query profiles between the age of 20 to 30 and click **[!UICONTROL Confirm]** when done.

   ![](assets/report_segment_8.png)

1. Click **[!UICONTROL Add an element]** to create your second segment and configure it as described in the steps above to target profiles between the age of 30 to 40.

1. Edit the **[!UICONTROL Segment code]** for each population to be passed on through dynamic reporting.

   >[!NOTE]
   >이 단계는 필수입니다. 그렇지 않으면 보고할 세그먼트를 이해할 수 없습니다.

   ![](assets/report_segment_9.png)

1. Drag and drop an **[!UICONTROL Email delivery]** activity after your segments.

   ![](assets/report_segment_3.png)

1. 타깃팅된 다양한 모집단에 따라 게재를 개인화합니다. For more on email creation, refer to this [page](../../designing/using/about-email-content-design.md).

1. 워크플로우를 저장합니다.

1. Click **[!UICONTROL Start]** when your workflow is ready.

이제 보고서에 액세스하여 세그먼트 코드를 추적할 수 있습니다.

## Step 3: Create a dynamic report to filter segments {#step-3--create-a-dynamic-report-filter-segments}

워크플로우와 함께 배달을 전송한 후 워크플로우에서 세그먼트 코드를 사용하여 보고서를 분류할 수 있습니다.

1. **[!UICONTROL Reports]** 탭에서 즉시 사용할 수 있는 보고서를 선택하거나 **[!UICONTROL Create new project]** 단추를 클릭하여 처음부터 새로 시작합니다.

   ![](assets/custom_profile_18.png)
1. **[!UICONTROL Delivery]** 차원을 자유 형식 테이블로 드래그하여 놓습니다.

   ![](assets/report_segment_5.png)

1. **[!UICONTROL Open]** 데이터와 **[!UICONTROL Click]** 지표와 같은 다른 지표를 드래그 앤 드롭하여 데이터 필터링을 시작합니다.
1. **[!UICONTROL Dimensions]** 카테고리에서 **[!UICONTROL Profile]** 차원을 클릭한 다음 워크플로우의 게재에서 **[!UICONTROL Segment code]** 차원을 드래그하여 놓아 타깃팅된 모집단에 따라 이메일 게재의 성공을 측정합니다.

   ![](assets/report_segment_6.png)

1. 필요한 경우 작업 영역에서 시각화를 드래그하여 놓을 수 있습니다.

   ![](assets/report_segment_10.png)
