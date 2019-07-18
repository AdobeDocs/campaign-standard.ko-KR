---
title: 데이터베이스 구조 업데이트
seo-title: 데이터베이스 구조 업데이트
description: 데이터베이스 구조 업데이트
seo-description: Adobe Campaign 데이터베이스를 업데이트하는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: 6 c 802 f 4 f-d 298-4 ca 4-acdb -09 f 2 ad 3865 b 9
contentOwner: Sauviat
products: sg_ campaign/standard
audience: developing
content-type: 참조
topic-tags: adding-or-extending-a-resource
discoiquuid: 2448 B 126-66 B 8-4608-AA 6 C -8028 FB 1902 A 4
context-tags: deploy, main; Eventcusresource, 개요
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 806dc4736ffb395a0eea102090c688102478aaca

---


# Updating the database structure{#updating-the-database-structure}

데이터 모델을 효과적으로 수정하여 사용할 수 있으려면 데이터베이스 구조를 업데이트해야 합니다.

>[!NOTE]
>
>Adobe에서 수행한 자동 업데이트 동안 사용자 정의 리소스는 자동으로 새로 고쳐집니다.

## Publishing a custom resource {#publishing-a-custom-resource}

리소스에 수행한 변경 사항을 적용하려면 데이터베이스 업데이트를 수행해야 합니다.

>[!NOTE]
>
>이벤트에 사용된 사용자 정의 리소스의 필드를 수정하거나 삭제하면 해당 이벤트가 자동으로 게시 취소됩니다. See [Configuring Transactional messaging](../../administration/using/configuring-transactional-messaging.md).

1. From the advanced menu, via the Adobe Campaign logo, select **[!UICONTROL Administration]** &gt; **[!UICONTROL Development]**, then **[!UICONTROL Publishing]**.
1. By default, the option **[!UICONTROL Determine modifications since the last publication]** is checked, which means that only the changes carried out since the last update will be applied.

   >[!NOTE]
   >
   >The **[!UICONTROL Repair database structure]** reestablishes a correct configuration if the publication failed before completing. 사용자 지정 리소스를 사용하지 않고 데이터베이스에서 직접 수행한 모든 수정은 삭제됩니다.

   ![](assets/schema_extension_12.png)

1. **[!UICONTROL Prepare publication]** 단추를 클릭하여 분석을 시작합니다. 워크플로우가 인스턴스를 과도하게 사용하지 않으면 큰 테이블 업데이트가 수행해야 합니다.

   To learn more on the action to perform on the Profiles &amp; Services API, refer to [Publishing a resource with API extension](../../developing/using/updating-the-database-structure.md#publishing-a-resource-with-api-extension).

   ![](assets/schema_extension_13.png)

1. Once the publication has been carried out, click the **[!UICONTROL Publish]** button to apply your new configurations.
1. Once published, the **[!UICONTROL Summary]** pane of each resource indicates that the status is now **[!UICONTROL Published]** and specifies the date of the last publication.

   >[!NOTE]
   >
   >리소스를 새로 변경하는 경우 변경 사항이 적용되도록 이 작업을 반복해야 합니다.

   If resources have the **[!UICONTROL Pending re-draft]** status before publishing, then an additional message will appear inviting you to check your actions because publishing will result in definitive changes (deleting columns, tables...). To help you carry out this last change, an **[!UICONTROL SQL Script]** tab is available. 발행물 중에 실행되는 SQL 명령을 제공합니다.

   ![](assets/schema_extension_scriptsql.png)

   >[!NOTE]
   >
   >You can stop the Re-draft process by clicking the **[!UICONTROL Cancel re-draft]** button. 이 작업은 리소스 상태를 원래 상태로 되돌립니다.

1. If your publication failed, you can always go back to the previous publication by clicking **[!UICONTROL Back to latest successful publication]**.

   발행물을 실패 상태로 두면 인스턴스에 로그인하는 즉시 팝업 창이 열리므로 이 발행물을 수정할 수 있습니다. Your instance will not be upgrade with new product versions until your publication is fixed.

   ![](assets/schema_extension_31.png)

## Publishing a resource with API extension {#publishing-a-resource-with-api-extension}

다음과 같은 경우에 프로필 및 서비스 API를 만들 수 있습니다.

* When you extend the custom resources **[!UICONTROL Profiles]** or **[!UICONTROL Services]**, you can perform an update of the Profiles and Services API to integrate the fields declared in the custom resources extension.
* When you define a custom resource and you create a link between the resources **[!UICONTROL Profiles]** or **[!UICONTROL Services]** and the custom resource, you can perform an update to include the new resource in the API.

[발행] 화면에서 이 옵션을 선택할 수 있습니다.

* API가 아직 게시되지 않은 경우 (리소스를 확장하지 않았거나 이 리소스 또는 다른 리소스에 대해 이 옵션을 선택하지 않은 경우) 생성 여부를 선택할 수 있습니다.

   ![](assets/create-profile-and-services-api.png)

* API가 이미 게시된 경우 (이미 리소스를 확장하고 이 옵션을 한 번 선택하면) API 업데이트가 강제로 수행됩니다.

   실제로 일단 만들어지면 API를 다시 게시할 때마다 자동으로 업데이트됩니다. 이는 이 API의 프로필 또는 서비스 리소스를 중단하고 인스턴스를 훼손하지 않기 위한 것입니다.

Note that by default, the custom resource is integrated, but, for a specific behavior, if you don't want to publish this resource, you can select the option **[!UICONTROL Hide this resource from APIs]** available in the **[!UICONTROL Resource Properties]**.

![](assets/removefromextoption.png)

**[!UICONTROL Prepare Publication]** 이 단계 후에 Adobe Campaign는 현재 버전의 API와 탭에서 **[!UICONTROL Profiles & Services API Preview]**&#x200B;발행물 이후 향후 버전 간 델타를 표시합니다. API를 처음 확장하는 경우 Delta는 기본 사용자 지정 리소스 정의를 확장 기능과 비교합니다.

탭에 표시되는 정보는 다음 세 섹션으로 나뉩니다. 요소를 추가하거나 삭제하고 수정했습니다.

![](assets/extendpandsapi_diff.png)

발행 단계가 API 동작을 수정하며 도미노 효과의 주변 개발에 영향을 줄 수 있으므로, 델타 분석은 필수 단계입니다.

>[!NOTE]
>
>This publication updates the **[!UICONTROL profilesAndServicesExt]** API. **[!UICONTROL profilesAndServices]** API는 업데이트되지 않습니다.

For more information on the Adobe Campaign API, consult the dedicated Adobe Campaign documentation on [Adobe IO](https://docs.campaign.adobe.com/doc/standard/en/adobeio.html).
