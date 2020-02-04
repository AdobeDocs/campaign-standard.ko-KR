---
title: 조직 단위
description: 조직의 단위를 사용하여 사용자의 액세스 수준을 정의합니다.
page-status-flag: never-activated
uuid: 8c82ffea-cef4-4a89-b823-d8b7bae1db4f
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: users-and-security
discoiquuid: 6f60c653-1d12-4d27-9bc8-ce8c19bca466
context-tags: orgUnit,overview;orgUnit,main;geoUnit,overview;geoUnit,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e31e8c63fa94d190211c7a51e7f1091657c9f479

---


# 조직 단위{#organizational-units}

## 단위 정보 {#about-units}

플랫폼의 각 개체 및 사용자는 조직 구성 요소에 연결됩니다. 이 단위를 사용하면 사용자에게 필터링된 보기를 제공하기 위해 계층 구조를 정의할 수 있습니다. 사용자의 단위는 서로 다른 플랫폼 개체에 대한 액세스 수준을 정의합니다.

>[!IMPORTANT]
>
>사용자가 어떤 장치에도 연결되어 있지 않으면 해당 사용자는 Adobe Campaign에 연결할 수 없습니다. 특정 사용자 또는 사용자 그룹에 대한 액세스를 제한하려면 **[!UICONTROL All]**장치에 연결하지 마십시오.
>
>기본적으로 조직 구성 **[!UICONTROL All (all)]**단위는**[!UICONTROL Administrators]** 보안 그룹에 할당됩니다. 읽기 전용이므로 수정할 수 없습니다.

사용자는 상위 단위의 모든 객체에 대한 읽기 전용 액세스 권한을 가집니다. 그는 자기 부대의 모든 물건과 아동 부대의 모든 물건들을 읽고 쓸 수 있다. 사용자는 병렬 분기에서 객체에 액세스할 수 없습니다.

기본적으로 단위만 사용할 수 **[!UICONTROL All]**있습니다.

사용자에게 조직 구성 단위가 할당되면 이 단위는 사용자가 만든 개체에 항상 적용됩니다.

![](assets/user_management_2.png)

>[!NOTE]
>
>사용자가 여러 장치에 연결된 여러 그룹에 있으면 특정 규칙이 적용됩니다. 자세한 내용은 그룹 및 [사용자](../../administration/using/managing-groups-and-users.md) 관리 섹션을 참조하십시오.

## 단위 만들기 및 관리 {#creating-and-managing-units}

조직 단위를 사용하면 사용자가 연결된 조직에 따라 인스턴스를 필터링할 수 있습니다. 이 단위는 지역, 국가 또는 심지어 브랜드를 나타낼 수 있습니다.

여기에서 이전에 두 명의 사용자에게 서로 다른 역할을 가진 보안 그룹을 만들었습니다.한 사용자에게 관리자 및 Geometrixx 보안 그룹이 할당되고, 다른 사용자는 보안 그룹 Standard 사용자 및 Geometrixx Clothing [에 속합니다. 자세한 내용은 보안 그룹 만들기 및 사용자](../../administration/using/managing-groups-and-users.md#creating-a-security-group-and-assigning-users) 지정을 참조하십시오.

이제 Geometrixx Clothing 및 Geometrixx 보안 그룹을 위한 구성 단위를 만들어야 합니다.

1. Adobe Campaign 고급 메뉴에서 **[!UICONTROL Administration]**>**[!UICONTROL Users & security]** > **[!UICONTROL Organizational units]**을 선택합니다.
1. 을 **[!UICONTROL Create]**클릭하여 조직 구성 단위 구성을 시작합니다.

   ![](assets/manage_units_1.png)

1. 기본값과 Geometrixx **[!UICONTROL Label]****[!UICONTROL ID]** 로 변경합니다.
1. 그런 다음 이 장치를 상위 장치에 연결합니다. 여기, 우리가 **[!UICONTROL All]**선택했어요.

   ![](assets/manage_units_2.png)

1. 마지막으로 보안 그룹에 새 조직 구성 단위 지정을 **[!UICONTROL Create]**시작하려면 을 클릭합니다.
1. Geometrixx Clothing 유닛에 대해 동일한 절차를 따르십시오. 단, 상위 유닛은 이전에 만든 유닛인 Geometrixx이어야 합니다.

   ![](assets/manage_units_3.png)

서로 다른 장치를 다른 보안 그룹에 할당하는 효과를 보기 위해 관리자 및 Geometrixx 그룹에 할당된 사용자는 두 개의 이메일 템플릿을 만들어 표준 사용자에게 할당된 다른 사용자와 Geometrixx Clothes가 액세스할 수 있거나 액세스할 수 없는 사항을 확인합니다.

1. 고급 메뉴에서 **[!UICONTROL Resources]**>**[!UICONTROL Templates]** > **[!UICONTROL Delivery Templates]**를 선택합니다.
1. 기존 템플릿을 복제하여 필요에 따라 개인화합니다. 자세한 내용은 템플릿 [정보](../../start/using/marketing-activity-templates.md) 섹션을 참조하십시오.
1. 템플릿이 만들어지면 **[!UICONTROL Edit properties]**아이콘을 선택하여 템플릿에 단위를 지정합니다.

   ![](assets/manage_units_6.png)

1. 드롭다운 **[!UICONTROL Access authorization]**메뉴에서 조직 단위를 선택합니다.

   여기서는 이전에 만든 조직 구성 단위인 Geometrixx를 사용하여 하나의 템플릿을 만듭니다.

   ![](assets/manage_units_5.png)

1. 동일한 절차에 따라 이전에 만든 Geometrixx Clothing 조직 구성 요소에 할당된 두 번째 템플릿을 만듭니다.

표준 사용자 및 Geometrixx Clothing 그룹에 할당된 사용자는 두 템플릿을 모두 볼 수 있습니다. 조직 단위의 계층 구조 때문에 Geometrixx Clothing 유닛에 연결된 템플릿을 읽고 쓸 수 있으며 Geometrixx 유닛에 연결된 템플릿에 대한 읽기 전용 액세스만 받게 됩니다.

![](assets/manage_units_7.png)

Geometrixx Clothing 단위는 Geometrixx의 하위 단위이므로 사용자가 Geometrixx 템플릿을 수정하려고 하면 다음 메시지가 나타납니다.

![](assets/manage_units_8.png)

조직 구성 단위는 프로파일과 같은 다양한 기능에 대한 액세스를 제한할 수 있습니다. 예를 들어 Geometrixx Clothing 사용자가 **[!UICONTROL Profiles]**탭에 액세스하는 경우 Geometrixx Clothing 조직 구성 단위를 사용하여 프로필에 완전히 액세스하고 수정할 수 있습니다.

Geometrixx 조직 구성 단위의 프로필은 읽기 전용이지만 사용자가 하나의 프로필을 수정하려고 하면 다음 오류가 표시됩니다. **[!UICONTROL You do not have the rights needed to modify the 'profile' resource of ID]**Adobe

![](assets/manage_units_10.png)

## 파티션 프로필 {#partitioning-profiles}

조직에서 서로 다른 브랜드에서 연락하는 프로필을 분리해야 하는 경우 조직의 단위로 프로필을 분할할 수 있습니다.

기본적으로 조직의 단위 필드는 프로필에서 사용할 수 없으므로 추가해야 합니다.

조직 구성 단위가 없는 프로필은 사용자가 액세스할 수 없습니다.

>[!IMPORTANT]
>
>프로필을 가져오기 전에 이 옵션을 추가하는 것이 좋습니다. 고객 데이터베이스를 이미 가져온 경우 이미 가져온 프로필의 조직 단위 값을 설정하기 위해 업데이트가 필요합니다.

1. 고급 메뉴에서 Adobe Campaign 로고를 통해 관리 > 개발 **> 사용자 지정 리소스를**&#x200B;선택합니다.
1. 프로필을 **선택하거나** 새 사용자 지정 리소스를 만들어 프로필을 확장합니다.
1. 액세스 권한 **권한 관리 필드** 추가 상자를 선택하여 프로필 확장명에 조직 단위를 **추가합니다** .

   ![](assets/user_management_9.png)

1. 클릭 **[!UICONTROL Save]**.
1. 사용자 지정 리소스를 다시 게시하여 구조를 업데이트합니다. 게시 프로세스에 대한 자세한 내용은 구조 [업데이트](../../developing/using/data-model-concepts.md) 섹션을 참조하십시오.

조직 단위 필드는 **[!UICONTROL Access authorization]**섹션의 프로필에 추가됩니다.

![](assets/user_management_10.png)

**관련 항목**:

* [단위 정보](../../administration/using/organizational-units.md#about-units)
* [액세스 관리 기본 정보](../../administration/using/about-access-management.md)

