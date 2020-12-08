---
solution: Campaign Standard
product: campaign
title: 리소스 삭제
description: '리소스 삭제 방법 알아보기 '
audience: developing
content-type: reference
topic-tags: adding-or-extending-a-resource
translation-type: tm+mt
source-git-commit: a51943e4da04f5d19aaecdfcf956f5c4f3d804c8
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 14%

---


# 리소스 삭제{#deleting-a-resource}

리소스를 삭제하려면 해당 리소스가 **[!UICONTROL Draft]**&#x200B;이어야 합니다. 다음과 같은 경우 리소스가 **[!UICONTROL Draft]** 상태입니다.

* 방금 작성되었으며 아직 게시되지 않았습니다.
* 이미 게시된 경우 리소스를 다시 작성해야 합니다.

>[!IMPORTANT]
>
>사용자 지정 리소스의 초안 작성 및 삭제는 다른 리소스에 영향을 줄 수 있는 민감한 작업입니다. 이러한 작업은 전문가 사용자만 수행해야 합니다.

게시된 리소스를 다시 초안하고 삭제하려면

1. 다시 작성할 리소스를 선택합니다.
1. 작업 모음에서 **[!UICONTROL Re-draft]** 버튼을 클릭합니다.

   ![](assets/schema_extension_uc26.png)

1. **[!UICONTROL Ok]**&#x200B;을(를) 클릭합니다.

   >[!IMPORTANT]
   >
   >이 작업은 최종적입니다.수정 내용이 게시되면 리소스의 데이터베이스 테이블 또는 열 및 해당 데이터가 영구적으로 삭제되며, 이로 인해 다른 사용자 지정 리소스에서 링크가 끊길 수 있습니다. 리소스 정의만 사용할 수 있습니다.

   ![](assets/schema_extension_uc27.png)

   >[!NOTE]
   >
   >기본 제공 **프로필(프로필)** 리소스의 확장을 다시 초안하는 경우, 정의한 대로 **테스트 프로필(seedMember)** 확장 구문도 다시 작성해야 합니다. 프로필 리소스 확장에 대한 자세한 내용은 [이 섹션](../../developing/using/extending-the-profile-resource-with-a-new-field.md)을 참조하십시오.

1. 리소스를 게시합니다. 자세한 내용은 [사용자 지정 리소스 게시](../../developing/using/updating-the-database-structure.md#publishing-a-custom-resource)를 참조하십시오.

   그런 다음 리소스는 **초안** 모드로 전환되며 활성화 상태는 **[!UICONTROL Inactive]**&#x200B;입니다.

1. **[!UICONTROL List]** 모드에서 삭제할 리소스를 선택한 다음 ![](assets/delete_darkgrey-24px.png) **[!UICONTROL Delete element]** 아이콘을 클릭합니다.

   ![](assets/schema_extension_uc28.png)

리소스가 데이터 모델에서 삭제됩니다.

>[!NOTE]
>
>이벤트에 사용된 사용자 지정 리소스의 필드를 수정하거나 삭제하면 해당 이벤트의 게시는 자동으로 취소됩니다. [트랜잭션 이벤트](../../channels/using/publishing-transactional-event.md#unpublishing-an-event)의 게시 취소를 참조하십시오.
