---
title: 사용자 지정 프로필 차원 만들기
description: 사용자 지정 프로필 데이터를 기반으로 사용자 지정 프로필 차원을 만드는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: f75e005b-5328-4c98-9e78-51d54fd0e246
contentOwner: sauviat
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


# 사용자 지정 프로필 차원 만들기{#creating-a-custom-profile-dimension}

프로필 사용자 지정 리소스 확장 중에 만든 사용자 지정 프로필 데이터를 기반으로 보고서를 만들고 관리할 수도 있습니다.

이 예에서는 세 가지 수준으로 나눌 사용자 지정 프로필 필드 **충성도 프로그램을** 만듭니다.금, 은, 동. 이 사용자 지정 프로필은 동적 보고서에서 사용자 지정 프로필 차원으로 사용할 수 있도록 확장됩니다.

* [1단계:새 프로필 필드 만들기](#step-1--create-a-new-profile-field)
* [2단계:프로필 필드를 사용하여 전송 로그 확장](#step-2--extend-the-sending-logs-with-the-profile-field)
* [3단계:충성도 프로그램에 등록한 전달 타깃팅 받는 사람 만들기](#step-3--create-a-delivery-targeting-recipients-enrolled-in-the-loyalty-program)
* [4단계:동적 보고서를 만들어 사용자 지정 프로필 차원으로 수신자를 필터링합니다.](#step-4--create-a-dynamic-report-to-filter-recipients-with-the-custom-profile-dimension)

## 1단계:새 프로필 필드 만들기 {#step-1--create-a-new-profile-field}

먼저 수신자에게 충성도 수준을 할당할 새 프로필 **필드 충성도 프로그램을** 만들어야 합니다.금, 은, 또는 동메달.

>[!NOTE]
>
>사용자 지정 리소스는 관리자만 관리할 수 있습니다.

이렇게 하려면 다음을 수행하십시오.

1. 고급 메뉴에서 &gt; **[!UICONTROL Administration]** &gt; **[!UICONTROL Development]** &gt; **[!UICONTROL Custom resources]** 사용자 **[!UICONTROL Profile (profile)]** 지정 리소스를 차례로 선택합니다.

   ![](assets/custom_profile_1.png)

1. 탭의 **[!UICONTROL Data structure]** 카테고리에서 **[!UICONTROL Fields]** **[!UICONTROL Add field]** 단추를 클릭합니다.

   ![](assets/custom_profile_2.png)

1. 을 **[!UICONTROL Label]**&#x200B;입력하고 **[!UICONTROL ID]** 사용자 지정 리소스를 **[!UICONTROL Type]**&#x200B;선택합니다. 여기서, 우리는 수상자가 금, 은, 동 중에서 선택할 **[!UICONTROL Text]** 수 있기 때문에 선택했습니다.

   ![](assets/custom_profile_3.png)

1. 아이콘을 클릭하여 필드를 정의합니다. ![](assets/custom_profile_22.png)

   ![](assets/custom_profile_12.png)

1. 여기서는 아이콘을 클릭하여 각 값을 확인하고 만들어 승인된 값을 지정해야 **[!UICONTROL Specify a list of authorized valued]** 합니다 **[!UICONTROL Create element]**.

   ![](assets/custom_profile_13.png)

1. 을 **[!UICONTROL Label]** 입력한 **[!UICONTROL Value]** 다음 을 클릭합니다 **[!UICONTROL Add]**. 이 예제의 경우 금, 은, 동 값을 만들어야 합니다. 완료되면 을 **[!UICONTROL Confirm]** 클릭합니다.

   ![](assets/custom_profile_14.png)

1. 탭을 **[!UICONTROL Screen definition]** 선택합니다. 드롭다운에서 **[!UICONTROL Detail screen configuration]** **[!UICONTROL Add personalized fields]** 섹션을 확인하여 프로필에 새 섹션을 만듭니다.

   ![](assets/custom_profile_4.png)

1. 단추를 클릭하여 새 섹션을 만듭니다. **[!UICONTROL Add an element]** 다음을 **[!UICONTROL Type]**&#x200B;선택합니다.이 **[!UICONTROL Input field]**&#x200B;새 섹션에 추가할 **[!UICONTROL Value]** **[!UICONTROL List]**&#x200B;필드를 선택합니다.

   ![](assets/custom_profile_5.png)

1. 필드의 섹션에 제목을 추가할 수도 **[!UICONTROL Customize the title of the section where the fields will be displayed]**&#x200B;있습니다.

   구성이 **[!UICONTROL Save]** 완료되면 을 클릭합니다.

   ![](assets/custom_profile_6.png)

1. 고급 메뉴에서 **[!UICONTROL Administration]** &gt; **[!UICONTROL Development]** &gt; **[!UICONTROL Publication]** 을 선택하여 사용자 지정 리소스 게시를 시작합니다.
1. 을 **[!UICONTROL Prepare publication]** 클릭하고 준비가 완료되면 **[!UICONTROL Publish]** 단추를 클릭합니다.

   ![](assets/custom_profile_7.png)

이제 새 프로필 필드를 사용하고 수신자가 선택할 준비가 되었습니다.

![](assets/custom_profile_8.png)

## 2단계:프로필 필드를 사용하여 전송 로그 확장 {#step-2--extend-the-sending-logs-with-the-profile-field}

프로필 필드가 생성되었으므로 프로필 필드를 확장하여 동적 보고서에 연결된 사용자 지정 프로필 차원을 만들어야 합니다.

프로필 필드를 사용하여 로그를 확장하기 전에 PII 창이 **[!UICONTROL Sending logs extension]** 탭에 액세스할 수 있도록 허용되었는지 확인하십시오. 자세한 내용은 이 [페이지를](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement)참조하십시오.

>[!NOTE]
>
>관리자는 프로필 필드만 사용하여 로그를 확장할 수 있습니다.

1. 고급 메뉴에서 &gt; **[!UICONTROL Administration]** &gt; **[!UICONTROL Development]** &gt; **[!UICONTROL Custom resources]** 사용자 **[!UICONTROL Profile (profile)]** 지정 리소스를 차례로 선택합니다.
1. 드롭다운을 **[!UICONTROL Sending logs extension]** 엽니다.
1. 단추를 **[!UICONTROL Create element]** 클릭합니다.

   ![](assets/custom_profile_9.png)

1. 이전에 만든 필드를 선택하고 을 **[!UICONTROL Confirm]**&#x200B;클릭합니다.
1. 사용자 지정 프로필 차원을 **[!UICONTROL Add this field in Dynamic reporting as a new dimension]** 만들려면 선택합니다.

   ![](assets/custom_profile_10.png)

   이 옵션은 PII 창이 수락된 경우에만 사용할 수 있습니다. 자세한 내용은 이 [페이지를](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement)참조하십시오.

1. 을 **[!UICONTROL Add]** 클릭한 다음 사용자 지정 리소스를 저장합니다.
1. 사용자 지정 리소스가 수정되었으므로 새 변경 내용을 구현하려면 이 리소스를 게시해야 합니다.

   고급 메뉴에서 **[!UICONTROL Administration]** &gt; **[!UICONTROL Development]** &gt; **[!UICONTROL Publication]** 을 선택하여 사용자 지정 리소스 게시를 시작합니다.

1. 을 **[!UICONTROL Prepare publication]** 클릭하고 준비가 완료되면 **[!UICONTROL Publish]** 단추를 클릭합니다.

   ![](assets/custom_profile_7.png)

이제 보고서에서 사용자 지정 프로필을 사용자 지정 프로필 특성으로 사용할 수 있습니다.

이제 필드를 만들고 이 프로필 필드를 사용하여 전송 로그가 확장되었으므로 게재 수신자를 타깃팅하기 시작할 수 있습니다.

## 3단계:충성도 프로그램에 등록한 전달 타깃팅 받는 사람 만들기 {#step-3--create-a-delivery-targeting-recipients-enrolled-in-the-loyalty-program}

프로필 필드가 게시되면 배달을 시작할 수 있습니다. 이 예에서는 충성도 프로그램에 등록한 모든 수신자를 타깃팅하고자 합니다.

1. 탭에서 을 **[!UICONTROL Marketing activities]** 클릭한 다음 **[!UICONTROL Create]** **[!UICONTROL Email]**&#x200B;선택합니다.
1. 이메일을 **[!UICONTROL Email type]** 선택한 다음 이메일 속성을 입력합니다.
1. 충성도 프로그램에 등록한 수신자를 타깃팅하려면 **[!UICONTROL Profiles (attributes)]** 활동을 드래그하여 놓습니다.
1. 드롭다운에서 이전에 만든 필드를 **[!UICONTROL Field]** 선택합니다.

   ![](assets/custom_profile_16.png)

1. 을 **[!UICONTROL Filter conditions]**&#x200B;선택합니다. 여기에서 세 가지 충성도 프로그램 수준 중 하나에 속하는 수신자를 타깃팅하고자 합니다.

   ![](assets/custom_profile_17.png)

1. 을 **[!UICONTROL Confirm]** 클릭한 다음 필터링을 완료하면 을 클릭합니다 **[!UICONTROL Next]**.
1. 메시지 내용, 보낸 사람 이름 및 제목을 정의하고 개인화합니다. 이메일 작성에 대한 자세한 내용은 이 [페이지를](../../designing/using/designing-content-in-adobe-campaign.md)참조하십시오.

   그런 다음 을 **[!UICONTROL Create]**&#x200B;클릭합니다.

1. 준비가 되면 메시지를 미리 보고 보낼 수 있습니다. 메시지를 준비하고 전송하는 방법에 대한 자세한 내용은 이 [페이지를](../../sending/using/preparing-the-send.md)참조하십시오.

선택한 수신자에게 이메일이 올바르게 전송되면 데이터 필터링을 시작하고 보고서를 통해 배달의 성공을 추적할 수 있습니다.

## 4단계:동적 보고서를 만들어 사용자 지정 프로필 차원으로 수신자를 필터링합니다. {#step-4--create-a-dynamic-report-to-filter-recipients-with-the-custom-profile-dimension}

배달을 보낸 후 **[!UICONTROL Profile]** 테이블에서 사용자 지정 프로필 차원을 사용하여 보고서를 분류할 수 있습니다.

1. 탭에서 기본 보고서를 **[!UICONTROL Reports]** 선택하거나 **[!UICONTROL Create]** 단추를 클릭하여 보고서를 처음부터 시작합니다.

   ![](assets/custom_profile_18.png)

1. 카테고리에서 을 **[!UICONTROL Dimensions]** 클릭한 다음 사용자 지정 **[!UICONTROL Profile]** 충성도 프로그램 **** 프로필 차원을 자유 형식 테이블로 드래그하여 놓습니다.

   ![](assets/custom_profile_19.png)

1. 데이터 필터링을 시작하려면 **[!UICONTROL Processed/Sent]** 및 **[!UICONTROL Open]** 지표를 드래그하여 놓습니다.

   ![](assets/custom_profile_20.png)

1. 필요한 경우 작업 영역에 시각화를 드래그하여 놓습니다.

   ![](assets/custom_profile_21.png)

**관련 항목:**

* [사용자 지정 프로필 데이터를 사용하여 통찰력 있는 보고서 만들기](https://helpx.adobe.com/campaign/kb/simplify-campaign-management.html#Reportandshareinsightswithallstakeholders)
