---
title: 사용자 지정 프로필 차원 만들기
seo-title: 사용자 지정 프로필 차원 만들기
description: 사용자 지정 프로필 차원 만들기
seo-description: 사용자 지정 프로필 데이터를 기반으로 사용자 지정 프로필 차원을 만드는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: F 75 E 005 B -5328-4 C 98-9 E 78-51 D 54 FD 0 E 246
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 보고
content-type: 참조
topic-tags: 사용자 지정 보고서
discoiquuid: B 6 D 3 DE 63-3 Add -4881-8917-04 A 6 F 8 B 6 BE 4 D
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: e9a4d99ddf311898c48b2b352fa13f5b59ed1fbe

---


# Creating a custom profile dimension{#creating-a-custom-profile-dimension}

프로필 사용자 지정 리소스 확장 기간 동안 생성된 사용자 지정 프로필 데이터를 기반으로 보고서를 만들고 관리할 수도 있습니다.

In this example, we want to create the custom profile field **Loyalty programs** which will be divided into three levels: gold, silver and bronze. 이 사용자 지정 프로필은 동적 보고서에서 사용자 지정 프로필 차원으로 사용할 수 있게 확장됩니다.

* [1 단계: 새 프로필 필드 만들기](../../reporting/using/creating-a-custom-profile-dimension.md#step-1--create-a-new-profile-field)
* [2 단계: 프로필 필드를 사용하여 전송 로그 확장](../../reporting/using/creating-a-custom-profile-dimension.md#step-2--extend-the-sending-logs-with-the-profile-field)
* [3 단계: 충성도 프로그램에 등록된 배달 타깃팅 수신자 만들기](../../reporting/using/creating-a-custom-profile-dimension.md#step-3--create-a-delivery-targeting-recipients-enrolled-in-the-loyalty-program)
* [4 단계: 사용자 지정 프로필 차원으로 수신자를 필터링하는 동적 보고서 만들기](../../reporting/using/creating-a-custom-profile-dimension.md#step-4--create-a-dynamic-report-to-filter-recipients-with-the-custom-profile-dimension)

## Step 1: Create a new profile field {#step-1--create-a-new-profile-field}

We first need to create the new profile field **Loyalty program** that will assign loyalty level to our recipients: gold, silver or bronze.

>[!NOTE]
>
>사용자 지정 리소스는 관리자만 관리할 수 있습니다.

이렇게 하려면:

1. From the advanced menu, select **[!UICONTROL Administration]** &gt; **[!UICONTROL Development]** &gt; **[!UICONTROL Custom resources]** then the **[!UICONTROL Profile (profile)]** custom resource.

   ![](assets/custom_profile_1.png)

1. **[!UICONTROL Data structure]** 탭의 **[!UICONTROL Fields]** 카테고리에서 **[!UICONTROL Add field]** 단추를 클릭합니다.

   ![](assets/custom_profile_2.png)

1. Enter the **[!UICONTROL Label]**, **[!UICONTROL ID]** and select the custom resource **[!UICONTROL Type]**. Here, we selected **[!UICONTROL Text]** since recipients will have the choice between gold, silver and bronze.

   ![](assets/custom_profile_3.png)

1. ![](assets/custom_profile_22.png) 아이콘을 클릭하여 필드를 정의합니다.

   ![](assets/custom_profile_12.png)

1. Here, we need to specify the authorized values by checking **[!UICONTROL Specify a list of authorized valued]** and create each value by clicking **[!UICONTROL Create element]**.

   ![](assets/custom_profile_13.png)

1. Enter the **[!UICONTROL Label]** and **[!UICONTROL Value]** then click **[!UICONTROL Add]**. 이 예에서는 골드, 실버 및 브론즈를 만들어야 합니다. Click **[!UICONTROL Confirm]** when done.

   ![](assets/custom_profile_14.png)

1. **[!UICONTROL Screen definition]** 탭을 선택합니다. **[!UICONTROL Detail screen configuration]** 드롭다운 메뉴에서 **[!UICONTROL Add personalized fields]** 섹션을 선택하여 프로필에 새 섹션을 만듭니다.

   ![](assets/custom_profile_4.png)

1. **[!UICONTROL Add an element]** 단추를 클릭하여 새 섹션을 만듭니다. Select the **[!UICONTROL Type]**: **[!UICONTROL Input field]**, **[!UICONTROL Value]** or **[!UICONTROL List]**, then the field to add in this new section.

   ![](assets/custom_profile_5.png)

1. You can also add a title to your section in the field **[!UICONTROL Customize the title of the section where the fields will be displayed]**.

   Click **[!UICONTROL Save]** when the configuration is done.

   ![](assets/custom_profile_6.png)

1. From the advanced menu, select **[!UICONTROL Administration]** &gt; **[!UICONTROL Development]** &gt; **[!UICONTROL Publication]** to start publishing your custom resource.
1. Click **[!UICONTROL Prepare publication]** then when the preparation is done, click the **[!UICONTROL Publish]** button.

   ![](assets/custom_profile_7.png)

이제 받는 사람이 새 프로필 필드를 사용하고 선택할 수 있습니다.

![](assets/custom_profile_8.png)

## Step 2: Extend the sending logs with the profile field {#step-2--extend-the-sending-logs-with-the-profile-field}

프로필 필드가 만들어지면 프로필 필드를 사용하여 보내기 로그를 확장하여 동적 보고서에서 관련 사용자 지정 프로필 차원을 만들어야 합니다.

Before extending the log with our profile field, make sure that the PII window was accepted to have access to the **[!UICONTROL Sending logs extension]** tab. For more on this, refer to this [page](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement).

>[!NOTE]
>
>관리자는 프로필 필드로만 로그를 확장할 수 있습니다.

1. From the advanced menu, select **[!UICONTROL Administration]** &gt; **[!UICONTROL Development]** &gt; **[!UICONTROL Custom resources]** then the **[!UICONTROL Profile (profile)]** custom resource.
1. Open the **[!UICONTROL Sending logs extension]** drop-down.
1. **[!UICONTROL Create element]** 단추를 클릭합니다.

   ![](assets/custom_profile_9.png)

1. Select your previously created field and click **[!UICONTROL Confirm]**.
1. Check **[!UICONTROL Add this field in Dynamic reporting as a new dimension]** to create your custom profile dimension.

   ![](assets/custom_profile_10.png)

   이 옵션은 PII 창이 허용된 경우에만 사용할 수 있습니다. For more on this, refer to this [page](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement).

1. Click **[!UICONTROL Add]** then save your custom resource.
1. 사용자 지정 리소스가 수정되었으므로 새 변경 사항을 구현하려면 이를 게시해야 합니다.

   From the advanced menu, select **[!UICONTROL Administration]** &gt; **[!UICONTROL Development]** &gt; **[!UICONTROL Publication]** to start publishing your custom resource.

1. Click **[!UICONTROL Prepare publication]** then when the preparation is done, click the **[!UICONTROL Publish]** button.

   ![](assets/custom_profile_7.png)

이제 사용자 지정 프로필을 보고서에서 사용자 지정 프로필 차원으로 사용할 수 있습니다.

이제 필드를 만들고 이 프로필 필드로 로그를 전송하는 경우 배달에서 받는 사람 타깃팅을 시작할 수 있습니다.

## Step 3: Create a delivery targeting recipients enrolled in the loyalty program {#step-3--create-a-delivery-targeting-recipients-enrolled-in-the-loyalty-program}

프로필 필드가 게시되면 전달을 시작할 수 있습니다. 이 예에서는 충성도 프로그램에 등록된 모든 수신자를 타깃팅합니다.

1. **[!UICONTROL Marketing activities]** 탭에서 **[!UICONTROL Create]****[!UICONTROL Email]**&#x200B;아이콘을 클릭한 다음 선택합니다.
1. Choose an **[!UICONTROL Email type]** then enter your email's properties.
1. To target recipient enrolled in the loyalty program, drag and drop the **[!UICONTROL Profiles (attributes)]** activity.
1. Select your previously created field from the **[!UICONTROL Field]** drop-down.

   ![](assets/custom_profile_16.png)

1. **[!UICONTROL Filter conditions]**&#x200B;을 선택합니다. 여기서는 세 가지 충성도 프로그램 수준 중 하나에 속하는 수신자를 타깃팅하려고 합니다.

   ![](assets/custom_profile_17.png)

1. Click **[!UICONTROL Confirm]** then when done filtering, click **[!UICONTROL Next]**.
1. 메시지 컨텐츠, 발신자 이름 및 제목을 정의하고 개인화합니다. For more information on email creation refer to this [page](../../designing/using/about-email-content-design.md#about-the-email-designer).

   **[!UICONTROL Create]**&#x200B;그런 다음을 클릭합니다.

1. 준비가 되면 메시지를 미리 보고 보낼 수 있습니다. For more information on how to prepare and send your message, refer to this [page](../../sending/using/preparing-the-send.md).

이메일이 선택한 수신자에게 올바로 전송되면 데이터 필터링을 시작하고 보고서를 통해 전달 성공률을 추적할 수 있습니다.

## Step 4: Create a dynamic report to filter recipients with the custom profile dimension {#step-4--create-a-dynamic-report-to-filter-recipients-with-the-custom-profile-dimension}

After sending your delivery, you can breakdown reports using your custom profile dimension from the **[!UICONTROL Profile]** table.

1. **[!UICONTROL Reports]** 탭에서 즉시 사용할 수 있는 보고서를 선택하거나 **[!UICONTROL Create]** 단추를 클릭하여 처음부터 새로 시작합니다.

   ![](assets/custom_profile_18.png)

1. **[!UICONTROL Dimensions]** 카테고리의를 클릭하고 **[!UICONTROL Profile]** 사용자 지정 **충성도 프로그램** 프로필 차원을 자유 형식 테이블로 끌어다 놓습니다.

   ![](assets/custom_profile_19.png)

1. **[!UICONTROL Processed/Sent]** AND **[!UICONTROL Open]** 지표를 드래그하여 놓아 데이터 필터링을 시작합니다.

   ![](assets/custom_profile_20.png)

1. 필요한 경우 작업 영역에서 시각화를 드래그하여 놓을 수 있습니다.

   ![](assets/custom_profile_21.png)

