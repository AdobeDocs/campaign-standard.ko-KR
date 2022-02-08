---
title: 조직 단위
description: 조직 단위를 사용하여 사용자의 액세스 수준을 정의합니다
audience: administration
feature: Access Management
role: Admin
level: Experienced
exl-id: fbab695a-2672-4183-8c3b-78af7aefd5b1
source-git-commit: bfba6b156d020e8d2656239e713d2d24625bda54
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 4%

---

# 조직 단위{#organizational-units}

## 단위 정보 {#about-units}

플랫폼의 각 개체 및 사용자는 조직 단위에 연결되어 있습니다. 이 단위를 사용하면 필터링된 보기를 사용자에게 제공하기 위해 계층적 구조를 정의할 수 있습니다. 사용자의 단위는 서로 다른 플랫폼 객체에 대한 액세스 레벨을 정의합니다.

>[!IMPORTANT]
>
>사용자가 어떤 단위에 연결되어 있지 않으면 해당 사용자는 Adobe Campaign에 연결할 수 없습니다. 특정 사용자 또는 사용자 그룹에 대한 액세스를 제한하려면 **[!UICONTROL All]** 단위: 옵션을 추가하는 것이 좋습니다 **권한 부여 관리 필드에 액세스** 프로필을 가져오기 전에 자세한 정보는 이 [섹션](../../administration/using/organizational-units.md#partitioning-profiles)을 참조하십시오.
>
>**[!UICONTROL All (all)]** 조직 단위는 기본적으로 **[!UICONTROL Administrators]** 보안 그룹에 할당되어 있습니다. 이는 읽기 전용이므로 수정할 수 없습니다.

사용자는 상위 단위의 모든 객체에 대해 읽기 전용 액세스 권한을 가집니다. 이러한 사용자는 단위 및 하위 단위의 모든 객체에 대한 읽기 및 쓰기 액세스 권한을 가집니다. 사용자는 병렬 분기에 있는 객체에 액세스할 수 없습니다.

기본적으로 **[!UICONTROL All]** 판매량도 가능합니다

사용자에게 조직 단위가 할당되면 이 단위가 항상 사용자가 만든 객체에 적용됩니다.

![](assets/user_management_2.png)

>[!NOTE]
>
>사용자가 여러 단위에 연결된 여러 그룹에 있으면 특정 규칙이 적용됩니다. 자세한 내용은 [그룹 및 사용자 관리](../../administration/using/managing-groups-and-users.md) 섹션을 참조하십시오.

## 단위 생성 및 관리 {#creating-and-managing-units}

조직 단위를 사용하면 사용자가 연결된 조직에 따라 인스턴스를 필터링할 수 있습니다. 이 단위는 인스턴스에서 지역, 국가 또는 브랜드도 나타낼 수 있습니다.

여기에서는 이전에 두 사용자에게 다른 역할을 가진 보안 그룹을 만들었습니다. 한 사용자에게 보안 그룹 관리자 및 Geometrixx이 할당되고 다른 사용자는 보안 그룹에 속합니다. 표준 사용자 및 Geometrixx 의류 참조 [보안 그룹 만들기 및 사용자 할당](../../administration/using/managing-groups-and-users.md#creating-a-security-group-and-assigning-users) 전체 예제의 경우

이제 Geometrixx 의류 및 Geometrixx 보안 그룹의 조직 단위를 만들어야 합니다.

1. Adobe 캠페인 고급 메뉴에서 **[!UICONTROL Administration]** > **[!UICONTROL Users & security]** > **[!UICONTROL Organizational units]**.
1. 클릭 **[!UICONTROL Create]** 조직 단위 구성을 시작하려면 다음을 수행하십시오.

   ![](assets/manage_units_1.png)

1. 기본값 변경 **[!UICONTROL Label]** 및 **[!UICONTROL ID]** Geometrixx에 연결할 수도 있습니다.
1. 그런 다음 이 장치를 상위 장치에 연결합니다. 여기에서는 **[!UICONTROL All]**.

   ![](assets/manage_units_2.png)

1. 마지막으로 **[!UICONTROL Create]** 새 조직 단위를 보안 그룹에 할당하려면 다음을 수행합니다.
1. Geometrixx 의류 단위에 대해 동일한 절차를 수행합니다. 단, 상위 단위가 이전에 생성한 단위인 Geometrixx이어야 합니다.

   ![](assets/manage_units_3.png)

다른 단위를 다른 보안 그룹에 할당하는 효과를 보기 위해 관리자 및 Geometrixx 그룹에 할당된 사용자는 두 개의 이메일 템플릿을 만들어 표준 사용자 및 Geometrixx Clothes에 할당된 다른 사용자가 액세스할 수 있거나 액세스할 수 없는 사용자를 확인합니다.

1. 고급 메뉴에서 **[!UICONTROL Resources]** > **[!UICONTROL Templates]** > **[!UICONTROL Delivery Templates]**.
1. 기존 템플릿을 복제하고 필요에 따라 개인화합니다. 자세한 내용은 [템플릿 기본 정보](../../start/using/marketing-activity-templates.md) 섹션을 참조하십시오.
1. 템플릿을 만들 때 **[!UICONTROL Edit properties]** 아이콘을 사용하여 템플릿에 장치를 할당할 수 있습니다.

   ![](assets/manage_units_6.png)

1. 에서 **[!UICONTROL Access authorization]** 드롭다운 메뉴에서 조직 단위를 선택합니다.

   여기에서는 이전에 만든 조직 단위 Geometrixx으로 하나의 템플릿을 만듭니다.

   ![](assets/manage_units_5.png)

1. 동일한 절차에 따라 이전에 만든 Geometrixx 의류 조직 단위에 할당된 두 번째 템플릿을 만듭니다.

에 지정된 사용자 **표준 사용자** 및 **Geometrixx 의류** 그룹은 두 템플릿을 모두 볼 수 있습니다. 조직 단위의 계층 구조 때문에 Geometrixx 의류 단위에 연결된 템플릿에 대한 읽기 및 쓰기 액세스 권한을 가지며 Geometrixx 단위에 연결된 템플릿에 대한 읽기 전용 액세스 권한만 갖게 됩니다.

![](assets/manage_units_7.png)

Geometrixx 의류 단위는 Geometrixx의 하위 단위이므로 사용자가 Geometrixx 템플릿을 수정하려고 하면 다음 메시지가 나타납니다.

![](assets/manage_units_8.png)

조직 단위는 프로필과 같은 다양한 기능에 대한 액세스를 제한할 수 있습니다. 예를 들어 Geometrixx Clothes 사용자가 **[!UICONTROL Profiles]** Geometrixx 의류 조직 단위를 사용하여 프로필에 완전히 액세스하고 수정할 수 있습니다.

Geometrixx 조직 단위가 있는 프로필은 읽기 전용이지만 사용자가 하나의 프로필을 수정하려고 하면 다음 오류가 표시됩니다. **[!UICONTROL You do not have the rights needed to modify the 'profile' resource of ID]**.

![](assets/manage_units_10.png)

## 프로필 파티션 나누기 {#partitioning-profiles}

>[!IMPORTANT]
>
>조직 단위가 없는 프로필은 사용자가 액세스할 수 없으므로 프로필을 가져오기 전에 이 옵션을 추가하는 것이 좋습니다.
>
>고객 데이터베이스를 이미 가져온 경우 이미 가져온 프로필에서 조직 단위 값을 설정하려면 업데이트가 필요합니다.

조직에서 각 브랜드에서 연락한 프로필을 분리해야 하는 경우 조직 단위로 프로필을 분할할 수 있습니다.

기본적으로 조직 단위 필드는 프로필에 사용할 수 없으므로 추가해야 합니다.

1. 고급 메뉴에서 Adobe Campaign 로고를 통해 을(를) 선택합니다 **관리 > 개발 > 사용자 지정 리소스**.
1. 선택 **프로필** 또는 새 사용자 지정 리소스를 만들어 프로필을 확장합니다. 프로필 확장 방법에 대한 자세한 내용은 다음을 참조하십시오 [페이지](../../developing/using/extending-the-profile-resource-with-a-new-field.md#step-1--extend-the-profile-resource).
1. 을(를) 확인합니다. **액세스 권한 부여 관리 필드 추가** 상자에서 **프로필** 확장.

   ![](assets/user_management_9.png)

1. **[!UICONTROL Save]**&#x200B;를 클릭합니다.
1. 사용자 지정 리소스를 다시 게시하여 구조를 업데이트합니다. 게시 프로세스에 대한 자세한 내용은 [구조 업데이트](../../developing/using/updating-the-database-structure.md) 섹션을 참조하십시오.

조직 단위 필드는 **[!UICONTROL Access authorization]** 섹션을 참조하십시오.

![](assets/user_management_10.png)

**관련 항목**:

* [단위 정보](../../administration/using/organizational-units.md#about-units)
* [액세스 관리 기본 정보](../../administration/using/about-access-management.md)
