---
title: 사용자 정의 프로필 차원 만들기
description: 사용자 지정 프로필 데이터를 기반으로 사용자 지정 프로필 차원을 만드는 방법을 알아봅니다.
audience: reporting
content-type: reference
topic-tags: customizing-reports
feature: Reporting
role: Leader
level: Intermediate
exl-id: 98516af1-d4dd-4c1f-b360-f19208c22f82
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '813'
ht-degree: 5%

---

# 사용자 정의 프로필 차원 만들기{#creating-a-custom-profile-dimension}

프로필 사용자 지정 리소스 확장 중에 생성된 사용자 지정 프로필 데이터를 기반으로 보고서를 만들고 관리할 수도 있습니다.

이 예제에서는 사용자 정의 프로필 필드를 만들려고 합니다 **충성도 프로그램** 세 가지 수준으로 분할됩니다. 금, 은, 동. 그러면 이 사용자 지정 프로필을 확장하여 동적 보고서에서 사용자 지정 프로필 차원으로 사용할 수 있습니다.

* [1단계: 새 프로필 필드 만들기](#step-1--create-a-new-profile-field)
* [2단계: 프로필 필드로 전송 로그 확장](#step-2--extend-the-sending-logs-with-the-profile-field)
* [3단계: 충성도 프로그램에 등록된 게재 타깃팅 수신자를 만듭니다](#step-3--create-a-delivery-targeting-recipients-enrolled-in-the-loyalty-program)
* [4단계: 사용자 지정 프로필 차원으로 수신자를 필터링하는 동적 보고서 만들기](#step-4--create-a-dynamic-report-to-filter-recipients-with-the-custom-profile-dimension)

## 1단계: 새 프로필 필드 만들기 {#step-1--create-a-new-profile-field}

먼저 새 프로필 필드를 만들어야 합니다 **충성도 프로그램** 수신자에게 충성도 수준을 할당합니다. 금, 은, 동.

>[!NOTE]
>
>사용자 지정 리소스는 관리자만 관리할 수 있습니다.

방법은 다음과 같습니다.

1. 고급 메뉴에서 **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Custom resources]** 그러면 **[!UICONTROL Profile (profile)]** 사용자 지정 리소스 를 참조하십시오.

   ![](assets/custom_profile_1.png)

1. 에서 **[!UICONTROL Data structure]** 탭, **[!UICONTROL Fields]** 카테고리에서 **[!UICONTROL Add field]** 버튼을 클릭합니다.

   ![](assets/custom_profile_2.png)

1. 을(를) 입력합니다. **[!UICONTROL Label]**, **[!UICONTROL ID]** 사용자 지정 리소스를 선택합니다. **[!UICONTROL Type]**. 여기에서는 **[!UICONTROL Text]** 금, 은, 동 중에서 선택할 수 있기 때문입니다.

   ![](assets/custom_profile_3.png)

1. 을(를) 클릭합니다. ![](assets/custom_profile_22.png) 아이콘을 클릭하여 필드를 정의합니다.

   ![](assets/custom_profile_12.png)

1. 여기서는 다음을 확인하여 승인된 값을 지정해야 합니다 **[!UICONTROL Specify a list of authorized valued]** 을(를) 클릭하여 각 값을 만듭니다. **[!UICONTROL Create element]**.

   ![](assets/custom_profile_13.png)

1. 을(를) 입력합니다. **[!UICONTROL Label]** 및 **[!UICONTROL Value]** 을 클릭한 다음 **[!UICONTROL Add]**. 이 예에서는 금, 은 및 청동 값을 만들어야 합니다. 완료하면 **[!UICONTROL Confirm]**&#x200B;을 클릭합니다.

   ![](assets/custom_profile_14.png)

1. **[!UICONTROL Screen definition]** 탭을 선택합니다. 에서 **[!UICONTROL Detail screen configuration]** 드롭다운, 확인 **[!UICONTROL Add personalized fields]** 섹션에 새로운 섹션을 추가합니다.

   ![](assets/custom_profile_4.png)

1. 을(를) 클릭합니다. **[!UICONTROL Add an element]** 새 섹션을 만드는 단추입니다. 을(를) 선택합니다 **[!UICONTROL Type]**: **[!UICONTROL Input field]**, **[!UICONTROL Value]** 또는 **[!UICONTROL List]**&#x200B;를 입력한 다음 이 새 섹션에 추가할 필드를 추가합니다.

   ![](assets/custom_profile_5.png)

1. 필드의 섹션에 제목을 추가할 수도 있습니다 **[!UICONTROL Customize the title of the section where the fields will be displayed]**.

   클릭 **[!UICONTROL Save]** 구성이 완료되면

   ![](assets/custom_profile_6.png)

1. 고급 메뉴에서 **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Publication]** 사용자 지정 리소스 게시를 시작하려면 다음을 수행하십시오.
1. 클릭 **[!UICONTROL Prepare publication]** 준비가 완료되면 **[!UICONTROL Publish]** 버튼을 클릭합니다.

   ![](assets/custom_profile_7.png)

이제 새 프로필 필드를 사용할 준비가 되었습니다. 수신자가 새 프로필 필드를 선택할 수 있습니다.

![](assets/custom_profile_8.png)

## 2단계: 프로필 필드로 전송 로그 확장 {#step-2--extend-the-sending-logs-with-the-profile-field}

프로필 필드가 만들어졌으므로 이제 프로필 필드로 전송 로그를 확장하여 동적 보고서에 연결된 사용자 지정 프로필 차원을 만들어야 합니다.

프로필 필드로 로그를 확장하기 전에 PII 창이 **[!UICONTROL Sending logs extension]** 탭. 자세한 정보는 이 [페이지](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement)를 참조하십시오.

>[!NOTE]
>
>관리자는 프로필 필드만 사용하여 로그를 확장할 수 있습니다.

1. 고급 메뉴에서 **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Custom resources]** 그러면 **[!UICONTROL Profile (profile)]** 사용자 지정 리소스 를 참조하십시오.
1. 를 엽니다. **[!UICONTROL Sending logs extension]** 드롭다운.
1. **[!UICONTROL Create element]** 버튼을 클릭합니다.

   ![](assets/custom_profile_9.png)

1. 앞에서 만든 필드를 선택하고 을(를) 클릭합니다 **[!UICONTROL Confirm]**.
1. 확인 **[!UICONTROL Add this field in Dynamic reporting as a new dimension]** 사용자 지정 프로필 차원을 만들려면

   ![](assets/custom_profile_10.png)

   이 옵션은 PII 창이 수락된 경우에만 사용할 수 있습니다. 자세한 정보는 이 [페이지](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement)를 참조하십시오.

1. 클릭 **[!UICONTROL Add]** 그런 다음 사용자 지정 리소스를 저장합니다.
1. 사용자 지정 리소스가 수정되었으므로 새 변경 사항을 구현하려면 이 리소스를 게시해야 합니다.

   고급 메뉴에서 **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Publication]** 사용자 지정 리소스 게시를 시작하려면 다음을 수행하십시오.

1. 클릭 **[!UICONTROL Prepare publication]** 준비가 완료되면 **[!UICONTROL Publish]** 버튼을 클릭합니다.

   ![](assets/custom_profile_7.png)

이제 사용자 지정 프로필을 보고서에서 사용자 지정 프로필 차원으로 사용할 수 있습니다.

필드가 만들어졌고 전송 로그가 이 프로필 필드로 확장되었으므로 이제 게재에서 수신자 타겟팅을 시작할 수 있습니다.

## 3단계: 충성도 프로그램에 등록된 게재 타깃팅 수신자를 만듭니다 {#step-3--create-a-delivery-targeting-recipients-enrolled-in-the-loyalty-program}

프로필 필드가 게시되면 게재를 시작할 수 있습니다. 이 예에서는 충성도 프로그램에 등록된 모든 수신자를 타겟팅하려고 합니다.

1. **[!UICONTROL Marketing activities]** 탭에서 **[!UICONTROL Create]**&#x200B;을(를) 클릭한 다음 **[!UICONTROL Email]**&#x200B;을(를) 선택합니다.
1. 선택 **[!UICONTROL Email type]** 그런 다음 전자 메일 속성을 입력합니다.
1. 충성도 프로그램에 등록된 수신자를 타겟팅하려면 **[!UICONTROL Profiles (attributes)]** 활동.
1. 에서 앞에서 만든 필드를 선택합니다 **[!UICONTROL Field]** 드롭다운.

   ![](assets/custom_profile_16.png)

1. 을(를) 선택합니다 **[!UICONTROL Filter conditions]**. 여기에서는 세 가지 충성도 프로그램 수준 중 하나에 속하는 수신자를 타겟팅하려고 합니다.

   ![](assets/custom_profile_17.png)

1. 클릭 **[!UICONTROL Confirm]** 필터링을 수행한 후 을(를) 클릭합니다. **[!UICONTROL Next]**.
1. 메시지 콘텐츠, 보낸 사람 이름 및 제목을 정의하고 개인화합니다. 전자 메일 만들기에 대한 자세한 내용은 다음을 참조하십시오 [페이지](../../designing/using/designing-content-in-adobe-campaign.md).

   그런 다음 **[!UICONTROL Create]**.

1. 준비가 되면 메시지를 미리 보고 전송할 수 있습니다. 메시지를 준비하고 전송하는 방법에 대한 자세한 내용은 다음을 참조하십시오 [페이지](../../sending/using/preparing-the-send.md).

선택한 수신자에게 이메일이 올바르게 전송되면 데이터 필터링을 시작하고 보고서를 통해 게재의 성공을 추적할 수 있습니다.

## 4단계: 사용자 지정 프로필 차원으로 수신자를 필터링하는 동적 보고서 만들기 {#step-4--create-a-dynamic-report-to-filter-recipients-with-the-custom-profile-dimension}

게재를 보낸 후, **[!UICONTROL Profile]** 테이블.

1. 에서 **[!UICONTROL Reports]** 탭에서 기본 제공 보고서를 선택하거나 **[!UICONTROL Create]** 단추를 눌러 처음부터 시작합니다.

   ![](assets/custom_profile_18.png)

1. 에서 **[!UICONTROL Dimensions]** 카테고리 **[!UICONTROL Profile]** 그런 다음 사용자 지정 항목을 드래그하여 놓습니다 **충성도 프로그램** 프로필 차원을 자유 형식 테이블에 추가할 수 있습니다.

   ![](assets/custom_profile_19.png)

1. 을(를) 끌어다 놓습니다 **[!UICONTROL Processed/Sent]** 및 **[!UICONTROL Open]** 지표 를 사용하여 데이터 필터링을 시작합니다.

   ![](assets/custom_profile_20.png)

1. 필요한 경우 작업 공간에서 시각화를 끌어서 놓습니다.

   ![](assets/custom_profile_21.png)

**관련 항목:**

* [사용자 지정 프로필 데이터를 사용하여 통찰력 있는 보고서 만들기](https://helpx.adobe.com/campaign/kb/simplify-campaign-management.html#Reportandshareinsightswithallstakeholders)
