---
title: Audience Manager 또는 People 핵심 서비스와 대상 공유
seo-title: Audience Manager 또는 People 핵심 서비스와 대상 공유
description: Audience Manager 또는 People 핵심 서비스와 대상 공유
seo-description: 다양한 Adobe Experience Cloud 솔루션에서 고객을 가져오거나 내보내는 방법을 살펴볼 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: A 3701 E 72-5846-4241-afee-D 713 B 499 A 27 A
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 통합
content-type: 참조
topic-tags: working-with-campaign-and-audience-manager-or-people-core-service
discoiquuid: 77 AF 0772-52 B 5-46 BC-A 964-675 B 45965524
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 698466596fdacd005dc4d72b8071208c8c39f77d

---


# Sharing audiences with Audience Manager or People core service{#sharing-audiences-with-audience-manager-or-people-core-service}

## Importing an audience {#importing-an-audience}

사용자 핵심 서비스 통합을 통해 기술 워크플로우를 통해 대상을 Adobe Campaign로 직접 가져와 데이터베이스를 강화할 수 있습니다. For more information on audience sharing in People core service, refer to this [documentation](https://marketing.adobe.com/resources/help/en_US/mcloud/t_publish_audience_segment.html).

Importing audiences/segments from People core service in Adobe Campaign can be carried out from the **[!UICONTROL Audiences]** menu only by users connected via IMS (authentication via Adobe ID).

1. **[!UICONTROL Audiences]** 메뉴로 이동합니다.
1. In the action bar, select **[!UICONTROL Create]** to be taken to the screen to create an audience.
1. 새 대상자의 레이블을 지정합니다.
1. Set the audience **[!UICONTROL Type]** to **[!UICONTROL Experience Cloud]** to indicate that the audience being created is an audience that was imported from People core service.
1. **[!UICONTROL Name of the shared audience]** 필드에서 가져올 대상을 선택합니다. 세그먼트만 가져올 수 있습니다. 키-값 쌍, 특성 및 규칙이 포함된 세부적인 데이터는 지원되지 않습니다.

   ![](assets/aam_import_audience.png)

1. **[!UICONTROL Shared Data Source]**&#x200B;해당 항목을 선택합니다.

   If the selected data source is configured to use an encryption algorithm, an additional option offers you the possibility to **[!UICONTROL Force reconciliation with a profile]**. Check this option if the **[!UICONTROL Channel]** field of the data source is set to Email or Mobile (SMS) and if you want to leverage profile data.

   If you do not select the **[!UICONTROL Force reconciliation with a profile]** and if **[!UICONTROL Channel]** is set in AMC Data source to Email or Mobile (SMS) then all the encrypted declared IDs are decrypted. An audience of type **File** with a list of all the email addresses/mobile phone numbers is created/updated. 이렇게 하면 해당 프로필이 캠페인에서 존재하지 않더라도 이 통합을 통해 공유 대상을 가져오는 동안 이메일 주소/휴대폰 번호가 손실되지 않습니다. 이러한 유형의 대상은 워크플로우를 사용하여 수동으로 조정해야 하므로 직접 사용할 수 없습니다.

1. 대상을 만들기 위해 확인합니다.

   그런 다음 기술 워크플로우를 통해 대상을 가져옵니다. ID (' 방문자 ID'또는'선언된 ID ') 를 프로필 차원과 중재할 수 있었던 레코드로 구성됩니다. Adobe Campaign에서 인식할 수 없는 사람 핵심 서비스 세그먼트의 ID는 가져오지 않습니다.

이제 Adobe Campaign 데이터베이스에서 대상을 가져옵니다. People 코어 서비스 또는 Audience Manager에서 세그먼트를 직접 가져오는 경우 가져오기 프로세스는 24-36 시간이 소요됩니다. 이 기간 이후에는 Adobe Campaign에서 신규 고객을 찾아 사용할 수 있습니다.

>[!NOTE]
>
>Adobe Analytics에서 Adobe Campaign로 대상을 가져오는 경우 이러한 대상을 먼저 People 핵심 서비스 또는 Audience Manager에서 공유해야 합니다. 이 프로세스는 12-24 시간이 소요되며, 캠페인과 24-36 시간 동기화에 추가해야 합니다. 이 경우 대상 공유 기간은 최대 60 시간까지 걸릴 수 있습니다. For more information on Adobe Analytics audience sharing in People Core service and Audience manager, refer to this [documentation](https://marketing.adobe.com/resources/help/en_US/mcloud/t_publish_audience_segment.html).

## Exporting an audience {#exporting-an-audience}

An audience can be exported from Adobe Campaign to Audience Manager or People core service using a workflow and the **[!UICONTROL Save audience]** activity.

이것은 IMS (Adobe ID를 통한 인증) 를 통해 연결된 사용자만 새 워크플로우에서 수행할 수 있습니다.

1. 프로그램, 캠페인 또는 마케팅 활동 목록에서 새 워크플로우를 만듭니다.
1. 사용할 수 있는 다양한 활동을 사용하여 프로필 세트를 타깃팅합니다.
1. After the targeting, drag and drop a **[!UICONTROL Save audience]** activity into the workflow, then open it.
1. **[!UICONTROL Share in Adobe Experience Cloud]** Select.

   ![](assets/aam_save_audience_activity.png)

1. Specify the audience using the **[!UICONTROL Shared audience]** field. 창이 열리면 기존 대상을 선택하거나 새 대상을 만들 수 있습니다.

   * 기존 대상을 선택하면 새 레코드만 대상에 추가됩니다.
   * To export your profile list into a new audience, complete the **[!UICONTROL Segment name]** field then click **[!UICONTROL Create]** before selecting the newly created audience.
   ![](assets/aam_save_audience_segment_picker.png)

   중재하고 교환하려면 레코드에 Adobe Experience Cloud ID (' 방문자 ID'또는'선언된 ID ') 가 있어야 합니다. 대상을 가져오거나 내보낼 때 중재되지 않은 레코드는 무시됩니다.

1. 완료하려면 화면 오른쪽 상단에 있는 확인 표시를 클릭합니다.
1. **[!UICONTROL Shared Data Source]**&#x200B;해당 항목을 선택합니다.
1. If you like, check the **[!UICONTROL Generate an outbound transition]** box to use the profiles that were exported. 조정할 수 있는 프로필만 내보냅니다.
1. 활동의 구성을 확인하고 워크플로우를 저장합니다.
1. 워크플로우를 시작하여 고객을 내보낼 수 있습니다. Adobe Campaign와 사용자 핵심 서비스 간의 동기화는 몇 시간 정도 걸릴 수 있습니다.

Adobe Campaign와 사용자 핵심 서비스 간의 동기화는 24-36 시간 걸립니다. 이 기간 이후에는 핵심 서비스에서 새로운 고객을 찾아 다른 Adobe Experience Cloud 솔루션에서 재사용할 수 있습니다. For more information on using an Adobe Campaign shared audience in Adobe People core service, refer to this [documentation](https://marketing.adobe.com/resources/help/en_US/mcloud/t_audience_create.html).

**관련 항목:**

* [워크플로우](../../automating/using/workflow-data-and-processes.md)
* [대상](../../audiences/using/about-audiences.md)

