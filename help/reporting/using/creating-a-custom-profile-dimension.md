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
source-git-commit: 782a5f89b0361f1cbe59c9b353ca90dec90c3906

---


# 사용자 지정 프로필 차원 만들기{#creating-a-custom-profile-dimension}

프로필 사용자 지정 리소스 확장 기간 동안 생성된 사용자 지정 프로필 데이터를 기반으로 보고서를 만들고 관리할 수도 있습니다.

이 예에서는 세 가지 수준으로 나눌 사용자 지정 프로필 필드 **충성도 프로그램을** 만듭니다. 골드, 실버 및 브론즈. 이 사용자 지정 프로필은 동적 보고서에서 사용자 지정 프로필 차원으로 사용할 수 있게 확장됩니다.

* [1 단계: 새 프로필 필드 만들기](../../reporting/using/creating-a-custom-profile-dimension.md#step-1--create-a-new-profile-field)
* [2 단계: 프로필 필드를 사용하여 전송 로그 확장](../../reporting/using/creating-a-custom-profile-dimension.md#step-2--extend-the-sending-logs-with-the-profile-field)
* [3 단계: 충성도 프로그램에 등록된 배달 타깃팅 수신자 만들기](../../reporting/using/creating-a-custom-profile-dimension.md#step-3--create-a-delivery-targeting-recipients-enrolled-in-the-loyalty-program)
* [4 단계: 사용자 지정 프로필 차원으로 수신자를 필터링하는 동적 보고서 만들기](../../reporting/using/creating-a-custom-profile-dimension.md#step-4--create-a-dynamic-report-to-filter-recipients-with-the-custom-profile-dimension)

## 1 단계: 새 프로필 필드 만들기 {#step-1--create-a-new-profile-field}

먼저 받는 사람에게 충성도 수준을 지정할 새 프로필 필드 **충성도 프로그램을** 만들어야 합니다. 골드, 실버 또는 브론즈.

>[!NOTE]
>
>사용자 지정 리소스는 관리자만 관리할 수 있습니다.

이렇게 하려면:

1. 고급 메뉴에서 **[!UICONTROL Administration]** &gt; **[!UICONTROL Development]** &gt; **[!UICONTROL Custom resources]****[!UICONTROL Profile (profile)]** 사용자 지정 리소스를 선택합니다.

   ![](assets/custom_profile_1.png)

1. **[!UICONTROL Data structure]** 탭의 **[!UICONTROL Fields]** 카테고리에서 **[!UICONTROL Add field]** 단추를 클릭합니다.

   ![](assets/custom_profile_2.png)

1. 을 입력하고 **[!UICONTROL Label]****[!UICONTROL ID]** 사용자 지정 리소스를 **[!UICONTROL Type]**&#x200B;선택합니다. 골드, 실버 **[!UICONTROL Text]** 및 브론즈 중에서 선택할 수 있습니다.

   ![](assets/custom_profile_3.png)

1. ![](assets/custom_profile_22.png) 아이콘을 클릭하여 필드를 정의합니다.

   ![](assets/custom_profile_12.png)

1. 여기서는을 클릭하여 **[!UICONTROL Specify a list of authorized valued]** 인증 값을 지정하고를 클릭하여 각 값을 지정해야 **[!UICONTROL Create element]**&#x200B;합니다.

   ![](assets/custom_profile_13.png)

1. 을 입력한 **[!UICONTROL Label]****[!UICONTROL Value]****[!UICONTROL Add]**&#x200B;다음을 클릭합니다. 이 예에서는 골드, 실버 및 브론즈를 만들어야 합니다. 완료되면 **[!UICONTROL Confirm]** 클릭합니다.

   ![](assets/custom_profile_14.png)

1. **[!UICONTROL Screen definition]** 탭을 선택합니다. **[!UICONTROL Detail screen configuration]** 드롭다운 메뉴에서 **[!UICONTROL Add personalized fields]** 섹션을 선택하여 프로필에 새 섹션을 만듭니다.

   ![](assets/custom_profile_4.png)

1. **[!UICONTROL Add an element]** 단추를 클릭하여 새 섹션을 만듭니다. 다음을 선택합니다 **[!UICONTROL Type]**. **[!UICONTROL Input field]**, **[!UICONTROL Value]** or **[!UICONTROL List]**, then the field to add in this new section.

   ![](assets/custom_profile_5.png)

1. 필드의 섹션에 제목을 추가할 **[!UICONTROL Customize the title of the section where the fields will be displayed]**&#x200B;수도 있습니다.

   구성이 **[!UICONTROL Save]** 완료되면 클릭합니다.

   ![](assets/custom_profile_6.png)

1. 고급 메뉴에서 **[!UICONTROL Administration]** &gt; **[!UICONTROL Development]** &gt; **[!UICONTROL Publication]** 를 선택하여 사용자 지정 리소스 게시를 시작합니다.
1. 을 클릭하고 **[!UICONTROL Prepare publication]** 준비가 완료되면 **[!UICONTROL Publish]** 단추를 클릭합니다.

   ![](assets/custom_profile_7.png)

이제 받는 사람이 새 프로필 필드를 사용하고 선택할 수 있습니다.

![](assets/custom_profile_8.png)

## 2 단계: 프로필 필드를 사용하여 전송 로그 확장 {#step-2--extend-the-sending-logs-with-the-profile-field}

프로필 필드가 만들어지면 프로필 필드를 사용하여 보내기 로그를 확장하여 동적 보고서에서 관련 사용자 지정 프로필 차원을 만들어야 합니다.

프로필 필드로 로그를 확장하기 전에 PII 창이 **[!UICONTROL Sending logs extension]** 탭에 액세스할 수 있도록 허용되었는지 확인합니다. 이에 대한 자세한 내용은 이 [페이지를](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement)참조하십시오.

>[!NOTE]
>
>관리자는 프로필 필드로만 로그를 확장할 수 있습니다.

1. 고급 메뉴에서 **[!UICONTROL Administration]** &gt; **[!UICONTROL Development]** &gt; **[!UICONTROL Custom resources]****[!UICONTROL Profile (profile)]** 사용자 지정 리소스를 선택합니다.
1. 드롭다운을 **[!UICONTROL Sending logs extension]** 엽니다.
1. **[!UICONTROL Create element]** 단추를 클릭합니다.

   ![](assets/custom_profile_9.png)

1. 이전에 만든 필드를 선택하고 **[!UICONTROL Confirm]**&#x200B;를 클릭합니다.
1. 사용자 **[!UICONTROL Add this field in Dynamic reporting as a new dimension]** 지정 프로필 차원을 만들려면 확인하십시오.

   ![](assets/custom_profile_10.png)

   이 옵션은 PII 창이 허용된 경우에만 사용할 수 있습니다. 이에 대한 자세한 내용은 이 [페이지를](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement)참조하십시오.

1. 그런 **[!UICONTROL Add]** 다음 사용자 지정 리소스를 저장합니다.
1. 사용자 지정 리소스가 수정되었으므로 새 변경 사항을 구현하려면 이를 게시해야 합니다.

   고급 메뉴에서 **[!UICONTROL Administration]** &gt; **[!UICONTROL Development]** &gt; **[!UICONTROL Publication]** 를 선택하여 사용자 지정 리소스 게시를 시작합니다.

1. 을 클릭하고 **[!UICONTROL Prepare publication]** 준비가 완료되면 **[!UICONTROL Publish]** 단추를 클릭합니다.

   ![](assets/custom_profile_7.png)

이제 사용자 지정 프로필을 보고서에서 사용자 지정 프로필 차원으로 사용할 수 있습니다.

이제 필드를 만들고 이 프로필 필드로 로그를 전송하는 경우 배달에서 받는 사람 타깃팅을 시작할 수 있습니다.

## 3 단계: 충성도 프로그램에 등록된 배달 타깃팅 수신자 만들기 {#step-3--create-a-delivery-targeting-recipients-enrolled-in-the-loyalty-program}

프로필 필드가 게시되면 전달을 시작할 수 있습니다. 이 예에서는 충성도 프로그램에 등록된 모든 수신자를 타깃팅합니다.

1. **[!UICONTROL Marketing activities]** 탭에서 **[!UICONTROL Create]****[!UICONTROL Email]**&#x200B;아이콘을 클릭한 다음 선택합니다.
1. 을 선택하고 **[!UICONTROL Email type]** 이메일 속성을 입력합니다.
1. 충성도 프로그램에 등록된 수신자에게 **[!UICONTROL Profiles (attributes)]** 활동을 드래그하여 놓습니다.
1. 드롭다운에서 이전에 만든 필드를 선택합니다 **[!UICONTROL Field]** .

   ![](assets/custom_profile_16.png)

1. **[!UICONTROL Filter conditions]**&#x200B;을 선택합니다. 여기서는 세 가지 충성도 프로그램 수준 중 하나에 속하는 수신자를 타깃팅하려고 합니다.

   ![](assets/custom_profile_17.png)

1. 을 클릭하고 **[!UICONTROL Confirm]** 필터링을 완료한 다음을 클릭합니다 **[!UICONTROL Next]**.
1. 메시지 컨텐츠, 발신자 이름 및 제목을 정의하고 개인화합니다. 이메일 생성에 대한 자세한 내용은 이 [페이지를](../../designing/using/about-email-content-design.md#about-the-email-designer)참조하십시오.

   **[!UICONTROL Create]**&#x200B;그런 다음을 클릭합니다.

1. 준비가 되면 메시지를 미리 보고 보낼 수 있습니다. 메시지를 준비하고 보내는 방법에 대한 자세한 내용은 [이 페이지를](../../sending/using/preparing-the-send.md)참조하십시오.

이메일이 선택한 수신자에게 올바로 전송되면 데이터 필터링을 시작하고 보고서를 통해 전달 성공률을 추적할 수 있습니다.

## 4 단계: 사용자 지정 프로필 차원으로 수신자를 필터링하는 동적 보고서 만들기 {#step-4--create-a-dynamic-report-to-filter-recipients-with-the-custom-profile-dimension}

배달을 전송한 후 **[!UICONTROL Profile]** 테이블에서 사용자 지정 프로필 차원을 사용하여 보고서를 분류할 수 있습니다.

1. **[!UICONTROL Reports]** 탭에서 즉시 사용할 수 있는 보고서를 선택하거나 **[!UICONTROL Create]** 단추를 클릭하여 처음부터 새로 시작합니다.

   ![](assets/custom_profile_18.png)

1. **[!UICONTROL Dimensions]** 카테고리의를 클릭하고 **[!UICONTROL Profile]** 사용자 지정 **충성도 프로그램** 프로필 차원을 자유 형식 테이블로 끌어다 놓습니다.

   ![](assets/custom_profile_19.png)

1. **[!UICONTROL Processed/Sent]** AND **[!UICONTROL Open]** 지표를 드래그하여 놓아 데이터 필터링을 시작합니다.

   ![](assets/custom_profile_20.png)

1. 필요한 경우 작업 영역에서 시각화를 드래그하여 놓을 수 있습니다.

   ![](assets/custom_profile_21.png)

**관련 항목:**

* [사용자 지정 프로필 데이터를 사용하여 통찰력 있는 보고서 만들기](https://helpx.adobe.com/campaign/kb/simplify-campaign-management.html#Reportandshareinsightswithallstakeholders)
