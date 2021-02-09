---
title: Dynamics 365 셀프 서비스 앱과 Adobe Campaign Standard 통합 이용
description: Dynamics 365 셀프 서비스 앱과 Adobe Campaign Standard 통합
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-microsoft-dynamics-365
translation-type: tm+mt
source-git-commit: 974ae83a746c81b417e287fc2665dfa5982eff85
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 0%

---


# Microsoft Dynamics 365 셀프 서비스 앱과 Adobe Campaign Standard 통합 액세스

이 구성을 사용하려면 조직의 Experience Cloud(EC) 관리자와 함께 작업해야 합니다. 셀프 서비스 통합 애플리케이션 인터페이스에 액세스할 수 있도록 하는 데 필요한 초기 단계입니다. 도구에 액세스하면 데이터에 대한 연결을 설정하고 Adobe Campaign과 Microsoft Dynamics 365 간의 데이터 흐름을 구성합니다.

>[!NOTE]
>
>Adobe 담당자에게 연락하여 Adobe Campaign Standard 조직 및 인스턴스 이름을 제공해야 합니다. 조직에 대해 통합 앱을 활성화하도록 요청하는 티켓을 기록합니다.

## 제품 프로필 추가

이 섹션에서는 Microsoft Dynamics 365 셀프 서비스 앱과 Adobe Campaign Standard 통합에 대한 액세스 권한을 부여하는 방법을 알아봅니다. Adobe Experience Cloud에서 조직에 대한 액세스 권한이 있는 사용자는 아래 단계에 따라 사용자에게 액세스 권한을 부여하지 않는 한 통합 셀프 서비스 앱에 액세스할 수 없습니다.

>[!IMPORTANT]
>
> 이러한 단계는 조직의 Experience Cloud에서 **Administrator** 역할이 필요합니다.


1. https://experience.adobe.com/으로 이동하여 Adobe Experience Cloud에 로그인합니다.
1. **Admin Console**&#x200B;에 액세스합니다.

   ![](assets/do-not-localize/d365-to-acs-access-3.png)

1. Experience Cloud 솔루션에 액세스하려면 **[!UICONTROL Products]**&#x200B;을 클릭합니다.

   ![](assets/do-not-localize/d365-to-acs-access-6.png)


   >[!IMPORTANT]
   >
   >이 섹션의 나머지 단계는 각 캠페인 인스턴스(개발, 텍스트, 프로덕션)에 대해 수행됩니다.

1. 구성할 첫 번째 인스턴스를 클릭합니다.

   ![](assets/do-not-localize/d365-to-acs-access-6.png)

   인스턴스 페이지는 다음과 같아야 합니다.

   ![](assets/do-not-localize/d365-to-acs-access-8.png)

1. **[!UICONTROL New Profile]** 단추를 클릭하고 다음 이름의 새 항목을 추가합니다.**Campaign Standard - your-prod-instance-name - D365/ACS 통합**

   * 목록에 이 항목이 표시되면 계속할 필요가 없습니다. 왼쪽 메뉴에서 **Adobe Campaign Standard**&#x200B;을 클릭하고 다른 캠페인 인스턴스를 확인합니다.

   * &quot;your-prod-instance-name&quot;을 인스턴스의 실제 이름으로 바꾸십시오.

1. 기본값을 사용하여 **[!UICONTROL Permission Group]** 드롭다운을 떠날 수 있습니다.

1. 항목이 다음과 유사한 경우 **[!UICONTROL Done]** 단추를 클릭합니다.

   ![](assets/do-not-localize/d365-to-acs-access-14.png)

   새 제품 프로필이 추가되었습니다.

   ![](assets/do-not-localize/d365-to-acs-access-15.png)

## 사용자에게 액세스 권한 부여 {#add-users-to-profile}

**[!UICONTROL Products]** 페이지에서 캠페인 인스턴스를 선택하고 아래 단계를 수행합니다.

1. 이전에 만든 새 프로필을 클릭합니다. **Campaign Standard - your-prod-instance-name - D365/ACS 통합**

   ![](assets/do-not-localize/d365-to-acs-access-15.png)

1. **[!UICONTROL Developers]** 탭을 클릭합니다.

   ![](assets/do-not-localize/d365-to-acs-access-18.png)

1. **[!UICONTROL Add Developer]** 단추를 클릭합니다.

1. 추가할 사용자의 이름 또는 이메일 주소를 입력합니다.  사용자와 일치하는 결과를 선택합니다.

   사용자가 조직에 처음으로 추가된 경우 상세내역을 입력합니다.

1. **[!UICONTROL Save]**&#x200B;을 클릭하여 확인합니다.
