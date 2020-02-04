---
title: 리소스 삭제
description: '리소스 삭제 방법 학습 '
page-status-flag: never-activated
uuid: 5de27589-6fa5-412c-8e5a-a4976de05715
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: adding-or-extending-a-resource
discoiquuid: 0130733d-4e3f-40cd-b959-56381f2c8f44
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 6f7f4f3d81f4e6a540b3317f283c1e2311ccc65a

---


# 리소스 삭제{#deleting-a-resource}

리소스를 삭제하려면 해당 리소스가 A여야 합니다 **[!UICONTROL Draft]**. 다음과 같은 경우 리소스가**[!UICONTROL Draft]** 상태입니다.

* 방금 작성되었으며 아직 게시되지 않았습니다.
* 이미 게시된 경우 리소스를 다시 작성해야 합니다.

>[!CAUTION]
>
>사용자 정의 리소스의 초안 작성 및 삭제는 다른 리소스에 영향을 줄 수 있는 민감한 작업입니다. 이러한 작업은 전문가 사용자만 수행해야 합니다.

게시된 리소스를 다시 초안하고 삭제하려면

1. 다시 작성할 리소스를 선택합니다.
1. 작업 표시줄에서 **[!UICONTROL Re-draft]**단추를 클릭합니다.

   ![](assets/schema_extension_uc26.png)

1. 클릭 **[!UICONTROL Ok]**.

   >[!IMPORTANT]
   >
   >이 작업은 결정적입니다.수정 내용이 게시되면 리소스의 데이터베이스 테이블 또는 열 및 해당 데이터가 영구적으로 삭제되며, 이로 인해 다른 사용자 지정 리소스에서 링크가 끊길 수 있습니다. 리소스 정의만 사용할 수 있게 됩니다.

   ![](assets/schema_extension_uc27.png)

   >[!NOTE]
   >
   >기본 프로필(프로필) **** 리소스의 익스텐션을 다시 초안하는 경우, 정의한 테스트 프로필(seedMember) **** 익스텐션도 다시 작성해야 합니다. 프로필 리소스 확장에 대한 자세한 내용은 [이 섹션을](../../developing/using/extending-the-profile-resource-with-a-new-field.md)참조하십시오.

1. 리소스를 게시합니다. 자세한 내용은 사용자 [지정 리소스](../../developing/using/updating-the-database-structure.md#publishing-a-custom-resource)게시를 참조하십시오.

   그런 다음 리소스가 초안 **모드로** 전환되고 활성화 상태가 **[!UICONTROL Inactive]**됩니다.

1. 모드에서 삭제할 리소스를 선택한 다음 **[!UICONTROL List]**![](assets/delete_darkgrey-24px.png)**[!UICONTROL Delete element]** 아이콘을 클릭합니다.

   ![](assets/schema_extension_uc28.png)

리소스가 데이터 모델에서 삭제됩니다.

>[!NOTE]
>
>이벤트에 사용된 사용자 지정 리소스의 필드를 수정하거나 삭제하면 해당 이벤트의 게시를 자동으로 취소됩니다. See [Configuring transactional messaging](../../administration/using/configuring-transactional-messaging.md).

