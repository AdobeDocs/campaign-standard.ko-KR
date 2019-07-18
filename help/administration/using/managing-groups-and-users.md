---
title: 그룹 및 사용자 관리
seo-title: 그룹 및 사용자 관리
description: 그룹 및 사용자 관리
seo-description: 보안 그룹을 만들고 사용자를 관리하는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: B 3 A 3 A 2 E 3-9 D 69-4231-B 724-8 F 37419 F 7 A 61
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 관리
content-type: 참조
topic-tags: 사용자 및 보안
discoiquuid: 12 F 896 AB-EE 79-4 D 96-976 D-CF 34643491 B 4
context-tags: 사용자, 개요; user, main; 보안, 개요; 보안, 기본
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: a12df43de55dedf388a397fbf4670d99e3ea7f3d

---


# Managing groups and users{#managing-groups-and-users}

## About security groups {#about-security-groups}

보안 그룹은 조직 내에서 동일한 역할과 권한을 공유하는 사용자 집합입니다.

사용자는 항상 보안 그룹에 연결되어 있어야 합니다. 이를 통해 특정 역할 및 조직 단위를 할당할 수 있습니다.

For more information on roles, the tables in the following page present the different operations available according to a user's role(s): [Adobe Campaign Standard authorizations](https://docs.campaign.adobe.com/doc/standard/en/Technotes/AdobeCampaign-ACSRights.pdf).

기본 보안 그룹은 다음과 같습니다.

* **[!UICONTROL Administrators]**
* **[!UICONTROL Delivery supervisors]**
* **[!UICONTROL Message Center agents]**
* **[!UICONTROL Standard Users]**
* **[!UICONTROL Workflow supervisors]**

사용자가 보안 그룹에 연결되지 않은 경우 Adobe Campaign에 액세스할 수 없게 됩니다.

To restrict a user's access, do not add the user to the Campaign Standard users group as this is linked to **[!UICONTROL All]** organizational unit.

## Creating a security group and assigning users {#creating-a-security-group-and-assigning-users}

>[!CAUTION]
>
>관리 콘솔에서 보안 그룹은 프로필이라고 합니다.

기본 그룹이 사용자를 관리하기에 충분하지 않은 경우 자체 보안 그룹을 만들 수 있습니다. Adobe Campaign 관리 메뉴와 관리 콘솔에 대한 액세스 권한이 있는 관리자가 관리할 수 있습니다. For more information on the Admin console, refer to this [documentation](https://helpx.adobe.com/enterprise/managing/user-guide.html).

여기에서는 먼저 사용자에게 기본 사용자를 위한 두 개의 표준 사용자 및 관리자를 지정해야 합니다. 이러한 보안 그룹은 Adobe Campaign의 일부 기능을 제한합니다. 표준 사용자는 Adobe Campaign에 대한 기본 액세스 권한을 가지며 관리자는 예를 들어 관리 메뉴에 액세스할 수 있습니다.

Admin Console의 보안 그룹에 대한 변경 사항은 사용자가 Adobe Campaign에 로그인하는 즉시 동기화됩니다.

그런 다음 표준 사용자 및 관리자의 조직 구성에 따라 일부 액세스를 제한하는 Geometrixx 및 Geometrixx Clothing의 보안 그룹을 만듭니다.

![](assets/ootb_security_group_1.png)

사용자에게 기본 보안 그룹 중 하나를 할당해야 합니다.

1. In the Admin console, select your instance then the **Users** tab.

   ![](assets/manage_security_group_2.png)

1. **[!UICONTROL Add user]** 단추를 클릭하고 사용자의 이메일 주소를 입력합니다.
1. **[!UICONTROL Assign Products]** 탭에서 인스턴스와 즉시 사용 가능한 보안 **[!UICONTROL Administrators]** 그룹을 드롭다운 목록에서 선택합니다. 이렇게 하면 사용자가 관리 메뉴를 액세스하고 다음 보안 그룹을 만들 수 있습니다.

   ![](assets/ootb_security_group_2.png)

1. Click **[!UICONTROL Save]** and follow the same procedures to assign the **[!UICONTROL Standard Users]** out-of-the-box security group to your new user.

   ![](assets/ootb_security_group_3.png)

Once your two users are attached to the **[!UICONTROL Administrators]** and **[!UICONTROL Standard users]** out-of-the-box security groups which assign roles to our users, the Administrator user can now create the two security groups **Geometrixx** and **Geometrixx Clothes** that will assign organizational units to our users in addition to the out-of-the-box security groups.

1. In the Admin console, select your instance then the **Products** tab.
1. **[새 프로필** ] 단추를 클릭하여 **Geometrixx** 보안 그룹을 만듭니다.

   ![](assets/create_security_1.png)

1. Type the **[!UICONTROL Profile name]** by following this exact syntax: **[!UICONTROL Campaign Standard- instance name - ID of the security group]** and click **[!UICONTROL Done]**.

   그러면 선택한 ID가 Adobe Campaign에서 보안 그룹을 만드는 동안 사용됩니다.

   >[!NOTE]
   >
   >If the above syntax doesn't seem to work with an older instance, it needs to be replaced by **[!UICONTROL Campaign - instance name - ID of the security group]**.

   ![](assets/manage_security_group_1.png)

1. Then, follow the same procedures to create the **Geometrixx Clothes** security group.
1. Assign your security group to your user by selecting the **[!UICONTROL Users]** tab.

   ![](assets/manage_security_group_2.png)

1. Click your previously created user then the ![](assets/managing_security_group_10.png) icon in the **[!UICONTROL Products]** category.

   Select **[!UICONTROL Edit products assigned directly]** to start assigning new security group to your user.

   ![](assets/manage_security_group_8.png)

1. **[!UICONTROL Assign Products]** 탭에서 인스턴스를 선택한 다음 드롭다운 목록에서 이전에 만든 보안 그룹 Geometrixx를 선택하여 관리자 사용자에게 할당합니다.

   **[!UICONTROL Save]**&#x200B;을 클릭합니다.

   ![](assets/manage_security_group_3.png)

   사용자가 여러 그룹에 있는 경우:

   * 다른 그룹의 역할이 누적됩니다. 여기서 사용자는 두 개의 다른 그룹에 있습니다. 이것은 판매량에 대해 다른 역할을 할 것입니다.
   * It is the unit that is the highest in the hierarchy that will be used (see example in the [Organizational units](../../administration/using/organizational-units.md) section).
   * 단위가 동일한 동등한 수준을 가지고 있고 계층의 분기 분기에 있는 경우 사용자는 더 이상 연결할 수 없게 됩니다.

1. 동일한 절차에 따라 Geometrixx Clothing Security Group를 표준 사용자에게 할당합니다.

   ![](assets/manage_security_group_9.png)

새로 만든 보안 그룹이 이제 관리 콘솔에서 만들어집니다. 완전히 동기화하려면 Adobe Campaign에서 만들어야 합니다.

관리자 사용자는 조직 단위를 할당하는 데 사용되는 보안 그룹 세트를 만들어야 합니다. Geometrixx 및 Geometrixx Clothing. To learn how to create organizational units, see [Creating and managing units](../../administration/using/organizational-units.md#creating-and-managing-units) .

1. Click the **[!UICONTROL Adobe Campaign]** logo, in the top left corner, then select **[!UICONTROL Administration > Users & Security > Security groups]**.
1. Create your new security group and specify its **[!UICONTROL Label]** and **[!UICONTROL ID]**.

   ID는 Admin Console에서 선택한 ID와 동일해야 합니다.

1. **[!UICONTROL User access]** 필드에서 조직 단위를 할당합니다. Here, the Geometrixx security group is assigned the **[!UICONTROL All]** organizational unit.

   ![](assets/manage_security_group_6.png)

1. 또한 보안 그룹에 역할을 할당할 수도 있습니다. In our case, this step is not needed since the out-of-the-box security groups **[!UICONTROL Administrators]** and **[!UICONTROL Standard users]** are used to assign roles.
1. 동일한 절차에 따라 마지막 보안 Geometrixx 옷을 만들고 Geometrixx Clothing 조직 단위를 할당하십시오.

   ![](assets/manage_security_group_7.png)

이제 사용자가 보안 그룹에 할당되고 Adobe Campaign에 연결할 수 있습니다.

>[!CAUTION]
>
>관리 콘솔에서 사용자가 보안 그룹에서 제거되면 Adobe Campaign 보안 그룹의 일부이며 더 이상 Adobe Campaign에 로그인할 수 없게 됩니다. 이 경우 관리 콘솔에서 사용자의 이메일 주소를 제거하여 민감한 정보를 받지 않도록 합니다.

