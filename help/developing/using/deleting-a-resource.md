---
title: 리소스 삭제
description: 리소스 삭제 방법 알아보기
audience: developing
content-type: reference
topic-tags: adding-or-extending-a-resource
feature: Data Model
role: Developer
level: Experienced
exl-id: 4ddfdbcc-a154-4c10-a97e-73ad888d1f1f
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 16%

---

# 리소스 삭제{#deleting-a-resource}

리소스를 삭제하려면 해당 리소스는 **[!UICONTROL Draft]**. 리소스가 다음 위치에 있습니다. **[!UICONTROL Draft]** 상태:

* 방금 만들어졌고 아직 게시되지 않았습니다.
* 이미 게시된 경우 리소스를 다시 작성해야 합니다.

>[!IMPORTANT]
>
>사용자 지정 리소스를 다시 작성하고 삭제하는 것은 다른 리소스에 영향을 줄 수 있는 중요한 작업입니다. 이러한 작업은 전문가 사용자만 수행해야 합니다.

게시된 리소스를 다시 초안 작성 및 삭제하려면

1. 초안을 다시 작성할 리소스를 선택합니다.
1. 작업 모음에서 **[!UICONTROL Re-draft]** 버튼을 클릭합니다.

   ![](assets/schema_extension_uc26.png)

1. **[!UICONTROL Ok]**&#x200B;를 클릭합니다.

   >[!IMPORTANT]
   >
   >이 작업은 확정적입니다. 수정 사항이 게시되면 리소스의 데이터베이스 테이블 또는 열 및 해당 데이터가 영구적으로 삭제되므로 다른 사용자 지정 리소스에서 링크가 끊어질 수 있습니다. 리소스 정의만 계속 사용할 수 있습니다.

   ![](assets/schema_extension_uc27.png)

   >[!NOTE]
   >
   >기본 제공 확장의 초안을 다시 만드는 경우 **프로필(프로필)** 자원, 또한 모든 초안을 다시 작성해야 합니다. **테스트 프로필(seedMember)** 확장 기능을 정의했을 수 있습니다. 프로필 리소스 확장에 대한 자세한 내용은 [이 섹션](../../developing/using/extending-the-profile-resource-with-a-new-field.md).

1. 리소스를 게시합니다. 자세한 단계는 를 참조하십시오. [사용자 지정 리소스 게시](../../developing/using/updating-the-database-structure.md#publishing-a-custom-resource).

   그런 다음 리소스는 **초안** 모드 및 활성화 상태는 입니다. **[!UICONTROL Inactive]**.

1. 위치 **[!UICONTROL List]** 모드를 클릭하고 삭제할 리소스를 선택한 다음 ![](assets/delete_darkgrey-24px.png) **[!UICONTROL Delete element]** 아이콘.

   ![](assets/schema_extension_uc28.png)

리소스가 데이터 모델에서 삭제됩니다.

>[!NOTE]
>
>이벤트에 사용된 사용자 지정 리소스의 필드를 수정하거나 삭제하면 해당 이벤트의 게시는 자동으로 취소됩니다. 다음을 참조하십시오 [트랜잭션 이벤트 게시 취소](../../channels/using/publishing-transactional-event.md#unpublishing-an-event).
