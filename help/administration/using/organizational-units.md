---
title: 조직 단위
seo-title: 조직 단위
description: 조직 단위
seo-description: 조직 단위로 사용자의 액세스 수준을 정의할 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 8 c 82 ffea-cef 4-4 a 89-b 823-d 8 b 7 bae 1 db 4 f
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 관리
content-type: 참조
topic-tags: 사용자 및 보안
discoiquuid: 6 F 60 c 653-1 D 12-4 D 27-9 BC 8-CE 8 C 19 BCA 466
context-tags: Orgunit, 개요; orgunit, main; Geounit, Overview; geounit, main
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: a12df43de55dedf388a397fbf4670d99e3ea7f3d

---


# Organizational units{#organizational-units}

## About units {#about-units}

플랫폼의 각 개체 및 사용자는 조직 단위에 연결되어 있습니다. 이 단위를 사용하면 사용자에게 필터링된 보기를 제공하기 위해 계층 구조를 정의할 수 있습니다. 사용자 단위는 다른 플랫폼 개체에 대한 액세스 수준을 정의합니다.

>[!CAUTION]
>
>사용자가 어떤 단위에도 연결되지 않은 경우 해당 사용자는 Adobe Campaign에 연결할 수 없습니다. If you would like to restrict access for a particular user or group of users, do not link it to the **[!UICONTROL All]** unit.

사용자는 상위 단위의 모든 개체에 대한 읽기 전용 액세스 권한을 갖습니다. 그는 단위와 하위 단위의 모든 오브젝트를 읽고 쓸 수 있습니다. 사용자는 병렬 분기에서 개체에 액세스할 수 없습니다.

By default, only the **[!UICONTROL All]** units are available.

사용자에게 조직 단위가 할당되면 이 단위는 항상 사용자가 만든 개체에 적용됩니다.

![](assets/user_management_2.png)

>[!NOTE]
>
>사용자가 다른 단위에 연결된 여러 그룹에 있는 경우 특정 규칙이 적용됩니다. For more information, refer to the [Managing groups and users](../../administration/using/managing-groups-and-users.md) section.

## Creating and managing units {#creating-and-managing-units}

조직 단위를 사용하면 사용자가 연결되어 있는 조직에 따라 인스턴스를 필터링할 수 있습니다. 이 단위는 해당 지역의 지역, 국가 또는 브랜드를 나타낼 수 있습니다.

Here, we previously created security groups with different roles to two users: one user is assigned the security groups Administrators and Geometrixx, the other user belongs to the security groups Standard user and Geometrixx Clothes See [Creating a security group and assigning users](../../administration/using/managing-groups-and-users.md#creating-a-security-group-and-assigning-users) for the full example.

이제 Geometrixx Clothing 및 Geometrixx 보안 그룹을 위한 조직 구성 요소를 만들어야 합니다.

1. From Adobe campaign advanced menu, select **[!UICONTROL Administration]** &gt; **[!UICONTROL Users & security]** &gt; **[!UICONTROL Organizational units]**.
1. Click **[!UICONTROL Create]** to start configuring your organizational unit.

   ![](assets/manage_units_1.png)

1. Change the default **[!UICONTROL Label]** and **[!UICONTROL ID]** to Geometrixx.
1. 그런 다음 이 단위를 상위 단위에 연결합니다. **[!UICONTROL All]**&#x200B;여기에서 선택했습니다.

   ![](assets/manage_units_2.png)

1. Finally, click **[!UICONTROL Create]** to start assigning your new organizational unit to security group.
1. Geometrixx 의류 단위와 동일한 절차를 따르십시오. 단, 상위 단위는 이전에 생성된 단위인 Geometrixx 여야 합니다.

   ![](assets/manage_units_3.png)

다른 보안 그룹에 다른 단위를 할당함으로써 미치는 영향을 확인하기 위해 관리자 및 Geometrixx 그룹에 지정된 사용자가 두 개의 이메일 템플릿을 만들어 표준 사용자와 Geometrixx 옷에 할당된 다른 사용자가 액세스할 수 있는지 또는 액세스할 수 없는지 확인합니다.

1. From the advanced menu, select **[!UICONTROL Resources]** &gt; **[!UICONTROL Templates]** &gt; **[!UICONTROL Delivery Templates]**.
1. 기존 템플릿을 복제하고 필요에 따라 개인화합니다. For more on this, refer to the [About templates](../../start/using/about-templates.md) section.
1. When the template is created, select the **[!UICONTROL Edit properties]** icon to assign units to your template.

   ![](assets/manage_units_6.png)

1. **[!UICONTROL Access authorization]** 드롭다운 메뉴에서 조직 단위를 선택합니다.

   이전에 만든 조직 단위의 Geometrixx를 사용하여 하나의 템플릿을 만듭니다.

   ![](assets/manage_units_5.png)

1. 동일한 절차에 따라 이전에 만든 Geometrixx Clothing 조직 단위에 지정된 두 번째 템플릿을 만듭니다.

표준 사용자와 Geometrixx 의류 그룹에 할당된 사용자가 두 템플릿을 모두 볼 수 있습니다. 조직 단위의 계층 구조 때문에, Geometrixx 옷 단위와 연결된 템플릿을 읽고 쓰기 권한을 가지며 Geometrixx 단위에 연결된 템플릿에 대한 읽기 전용 액세스 권한만 갖게 됩니다.

![](assets/manage_units_7.png)

Geometrixx 옷 단위는 Geometrixx의 하위 단위이므로 사용자가 Geometrixx 템플릿을 수정하려고 하면 다음 메시지가 표시됩니다.

![](assets/manage_units_8.png)

조직 단위는 프로필과 같은 다른 기능에 대한 액세스를 제한할 수 있습니다. For example, if our Geometrixx Clothes user access the **[!UICONTROL Profiles]** tab, he will be able to fully access and modify the profiles with the Geometrixx Clothes organizational unit.

Whereas the profiles with the Geometrixx organizational unit will be read only, the following error will appear if our user tries to modify one profile: **[!UICONTROL You do not have the rights needed to modify the 'profile' resource of ID]**.

![](assets/manage_units_10.png)

## Partitioning profiles {#partitioning-profiles}

조직에서 각 브랜드가 접하는 프로파일을 분리해야 하는 경우 조직 단위로 프로파일을 분할할 수 있습니다.

기본적으로 조직 단위 필드는 프로필에서 사용할 수 없으므로 추가해야 합니다.

조직 단위 없는 프로필은 사용자가 액세스할 수 없습니다.

>[!CAUTION]
>
>프로필을 가져오기 전에 이 옵션을 추가하는 것이 좋습니다. 고객 데이터베이스를 이미 가져온 경우 이미 가져온 프로필에서 조직 단위 값을 설정하려면 업데이트가 필요합니다.

1. From the advanced menu, via the Adobe Campaign logo, select **Administration &gt; Development &gt; Custom resources**.
1. **프로필을** 선택하거나 새 사용자 지정 리소스를 만들어 프로필을 확장합니다.
1. Check the **Add access authorization management fields** box to add the organizational units in the **Profile** extension.

   ![](assets/user_management_9.png)

1. **[!UICONTROL Save]**&#x200B;을 클릭합니다.
1. 사용자 지정 리소스를 다시 게시하여 구조를 업데이트합니다. For more information about the publication process, refer to [Updating the structure](../../developing/using/data-model-concepts.md) section.

The organizational unit field is added to your profiles in the **[!UICONTROL Access authorization]** section.

![](assets/user_management_10.png)

**관련 항목**:

* [단위 정보](../../administration/using/organizational-units.md#about-units)
* [액세스 관리 정보](../../administration/using/about-access-management.md)

