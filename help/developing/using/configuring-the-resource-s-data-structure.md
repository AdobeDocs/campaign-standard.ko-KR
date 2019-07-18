---
title: 리소스 데이터 구조 구성
seo-title: 리소스 데이터 구조 구성
description: 리소스 데이터 구조 구성
seo-description: 데이터 구조를 구성하는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: 60 FE 80 C 0-9 DF 6-4808-A 432-60 A 1977216 EA
contentOwner: Sauviat
products: sg_ campaign/standard
audience: developing
content-type: 참조
topic-tags: adding-or-extending-a-resource
discoiquuid: 4 F 22 EE 35-1 D 5 F -4 c 75-95 B 4-3 E 38 B 85 DE 26 E
context-tags: Cusresource, main
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: a12df43de55dedf388a397fbf4670d99e3ea7f3d

---


# Configuring the resource's data structure{#configuring-the-resource-s-data-structure}

새 사용자 지정 리소스를 만든 후 데이터 구조를 구성해야 합니다.

When editing the resource, in the **[!UICONTROL Data structure]** tab, you can add:

* [필드](../../developing/using/configuring-the-resource-s-data-structure.md#adding-fields-to-a-resource)
* [식별 키](../../developing/using/configuring-the-resource-s-data-structure.md#defining-identification-keys)
* [색인](../../developing/using/configuring-the-resource-s-data-structure.md#defining-indexes)
* [링크](../../developing/using/configuring-the-resource-s-data-structure.md#defining-links-with-other-resources)
* [로그 보내기](../../developing/using/configuring-the-resource-s-data-structure.md#defining-sending-logs-extension)

## Adding fields to a resource {#adding-fields-to-a-resource}

상자에 새 필드를 추가하여 박스 데이터 모델의 일부가 아닌 데이터를 저장할 수 있습니다.

1. **[!UICONTROL Create element]** 단추를 사용하여 필드를 만듭니다.
1. 레이블, ID, 필드 유형을 지정하고 이 필드에 대해 허가된 최대 길이를 정의합니다.

   **[!UICONTROL ID]** 필드는 필수 필드이며 추가된 각 필드에 대해 고유해야 합니다.

   >[!NOTE]
   >
   >**[!UICONTROL Label]** 필드를 비워 두면 ID에서 자동으로 완성됩니다.

   ![](assets/schema_extension_4.png)

1. To modify one of the fields, check the **[!UICONTROL Edit Properties]** button.

   ![](assets/schema_extension_24.png)

1. **[!UICONTROL Field definition]** 화면에서 대상 및 타깃팅에 사용할 카테고리를 정의하거나 설명을 추가할 수 있습니다.

   ![](assets/schema_extension_5.png)

1. Check the **[!UICONTROL Specify a list of authorized values]** option if you need to define values that will be offered to the user (enumeration values).

   Then, click **[!UICONTROL Create element]** and specify a **[!UICONTROL Label]** and **[!UICONTROL Value]**. 필요한 만큼 값을 추가합니다.

1. Once you have added your fields, check the **[!UICONTROL Add audit fields]** box to include fields detailing the creation date, the user that created the resource, the date, and the author of the last modification.
1. **[!UICONTROL Add access authorization management fields]** 특정 리소스에 대한 액세스 권한이 있는 사람을 설명하는 필드를 포함하려면 상자를 선택합니다.

   이러한 필드는 데이터베이스 업데이트가 수행된 후 표시할 수 있는 데이터 및 메타데이터에 나타납니다. For more on this, refer to the [Updating the database structure](../../developing/using/updating-the-database-structure.md) section.

1. **[!UICONTROL Add automatic ID]** 필드를 확인하여 ID를 자동으로 생성합니다. 기존 개체는 비어 있는 상태로 유지됩니다.
1. To modify the way in which the name of the resource elements will appear in the lists and creation steps, check the **[!UICONTROL Personalize the resource title]** box. 이 리소스에 대해 만든 필드를 선택합니다.

   ![](assets/schema_extension_18.png)

이제 리소스 필드가 정의됩니다.

## Defining identification keys {#defining-identification-keys}

각 리소스에는 고유 키가 하나 이상 있어야 합니다. 예를 들어 두 제품이 구매 테이블에서 동일한 ID를 가질 수 없도록 키를 지정할 수 있습니다.

1. Specify it in the **[!UICONTROL Automatic primary key]** section the size for the storage if you would like to have a technical key automatically and incrementally generated.

   ![](assets/schema_extension_6.png)

1. **[!UICONTROL Create element]** 단추를 사용하여 키를 만듭니다.

   **[!UICONTROL Label]** And **[!UICONTROL ID]** 필드는 기본적으로 완료되지만 편집할 수 있습니다.

1. To define the elements making up this key, click **[!UICONTROL Create element]** and select the fields that you created for this resource.

   ![](assets/schema_extension_7.png)

   Created keys are displayed in the **[!UICONTROL Custom keys]** section.

이제 리소스에 대한 식별 키가 만들어집니다.

## Defining indexes {#defining-indexes}

인덱스는 하나 또는 여러 개의 리소스 필드를 참조할 수 있습니다. 인덱스를 사용하면 데이터베이스를 보다 쉽게 복구하기 위해 데이터베이스를 정렬할 수 있습니다. SQL 쿼리의 성능을 최적화합니다.

색인 정의는 권장되지만 필수는 아닙니다.

1. **[!UICONTROL Create element]** 단추를 사용하여 색인을 만듭니다.

   ![](assets/schema_extension_26.png)

1. **[!UICONTROL Label]** And **[!UICONTROL ID]** 필드는 기본적으로 완료되지만 편집할 수 있습니다.
1. 이 색인을 구성하는 요소를 정의하려면 이 리소스에 대해 만든 필드를 선택합니다.

   ![](assets/schema_extension_27.png)

1. **[!UICONTROL Confirm]**&#x200B;을 클릭합니다.

The indexes that were created appear in the list in the **[!UICONTROL Index]** section.

## Defining links with other resources {#defining-links-with-other-resources}

링크 세부 사항은 한 테이블에 다른 표가 있는 연관입니다.

1. **[!UICONTROL Create element]** 단추를 사용하여 대상 리소스에 대한 링크를 만듭니다.
1. **[!UICONTROL Select a target resource]**&#x200B;을 클릭합니다.

   ![](assets/schema_extension_28.png)

1. 리소스는 알파벳 순으로 표시되며 이름별로 필터링할 수 있습니다. 기술 이름이 대괄호로 표시됩니다.

   Select an element from the list and click **[!UICONTROL Confirm]**.

   ![](assets/schema_extension_9.png)

1. Select the **[!UICONTROL Link type]** according to cardinality. 선택한 카디널리티 유형에 따라 레코드가 삭제되거나 중복되는 경우의 동작은 달라질 수 있습니다.

   다양한 링크 유형은 다음과 같습니다.

   * **[!UICONTROL 1 cardinality simple link]**: 소스 테이블 한 개가 대상 테이블에 대해 가장 하나의 해당 발생을 가질 수 있습니다.
   * **[!UICONTROL N cardinality collection link]**: 소스 테이블 한 번 발생에는 몇 가지 해당 대상 테이블이 있을 수 있지만, 대상 테이블 한 개가 소스 테이블의 해당 발생을 가장 한 개 이상 가질 수 있습니다.
   * **[!UICONTROL 0 or 1 cardinality simple link]**: 소스 테이블 한 번 발생 시 해당 대상 테이블 중 가장 하나의 해당 발생이나 없음 중 하나만 있을 수 있습니다. Note that this kind of **[!UICONTROL Link type]** can cause performance issue.
   ![](assets/schema_extension_29.png)

1. **[!UICONTROL New link]** 화면에서 **[!UICONTROL Label]** 및 **[!UICONTROL ID]** 필드는 기본적으로 완료되지만 편집할 수 있습니다.

   >[!CAUTION]
   >
   >만든 후에는 링크의 이름을 변경할 수 없습니다. 링크의 이름을 변경하려면 링크를 삭제하고 다시 만들어야 합니다.

1. **[!UICONTROL Category for the audience and targeting]** 목록을 사용하면 이 링크를 카테고리에 할당하여 쿼리 편집기 도구에서 더 볼 수 있습니다.
1. If needed, the **[!UICONTROL Reverse link definition]** section allows you to display the label and ID of the resource in the targeted resource.
1. Define the behavior of the records referenced by the link in the **[!UICONTROL Behavior if deleted/duplicated]** section.

   기본적으로, Target 레코드는 링크가 더 이상 참조되지 않을 때 삭제됩니다.

   ![](assets/schema_extension_16.png)

1. **[!UICONTROL Join definition]** 섹션에서 기본 **[!UICONTROL Use the primary keys to make the join]** 옵션을 선택했지만 두 옵션 중 하나를 선택할 수 있습니다.

   * **[!UICONTROL Use the primary key to make the join]**: 이 가입 참여 정의를 사용하면 프로필 기본 키를 사용하여 구매의 기본 키와 조정할 수 있습니다.
   * **[!UICONTROL Define specific join conditions]**: 이 가입 참여 정의를 사용하면 두 리소스 모두에 참여할 필드를 수동으로 선택할 수 있습니다. Please note that if data are not correctly configured, the **Purchase** record will not be visible.
   ![](assets/schema_extension_17.png)

The links created are displayed in the list in the **[!UICONTROL Links]** section.

**예: 생성된 리소스를'Profiles'리소스와 연결**

In this example, we want to link a new resource **Purchase** with the **Profiles **custom resource:

1. Create your new **Purchase** resource.
1. **프로필** 사용자 지정 리소스와 연결하려면 탭에서 **[!UICONTROL Links]** 섹션을 펼친 **[!UICONTROL Data structure]****[!UICONTROL Create element]**&#x200B;다음을 클릭합니다.
1. Select the target resource, here **[!UICONTROL Profiles (profile)]**.
1. In this example, keep the default **[!UICONTROL 1 cardinality simple link]** Link type selected.

   ![](assets/custom_resource_link_to_profile_2.png)

1. Choose a join definition, here keep the default **[!UICONTROL Use the primary key to make the join]**.

   ![](assets/custom_resource_link_to_profile_3.png)

1. If needed, you can define a detail screen to be able to edit **Purchase** and link it to a profile.

   **[!UICONTROL Detail screen configuration]** 섹션을 펼친 다음, **[!UICONTROL Define a detail screen]** 리소스의 각 요소에 해당하는 화면을 구성하려면을 (를) 선택합니다. 이 확인란을 선택하지 않으면 리소스에 대한 세부 사항 보기에 액세스할 수 없습니다.

1. **[!UICONTROL Create element]**&#x200B;을 클릭합니다.
1. Select your linked resource and click **[!UICONTROL Add]**.

   Your new resource will then be available in the advanced menu by selecting **[!UICONTROL Client data]** &gt; **[!UICONTROL Purchase]**.

   ![](assets/custom_resource_link_to_profile_4.png)

1. Once your configuration is done, click **[!UICONTROL Confirm]**.

   이제 새 리소스를 게시할 수 있습니다.

By adding this link, a **Purchase** tab is added to the profiles detail screen from the **[!UICONTROL Profiles & audiences]** &gt; **[!UICONTROL Profiles]** menu. Please note that this is specific to the **[!UICONTROL Profile]** resource.

![](assets/custom_resource_link_to_profile.png)

## Defining sending logs extension {#defining-sending-logs-extension}

전송 로그 확장 기능을 사용하면 다음을 수행할 수 있습니다.

* to extend dynamic report capabilities by **adding profile custom fields**
* to extend the sending logs data with **segment code and profile data**

**세그먼트 코드로 확장**

사용자는 워크플로우 엔진에서 나오는 세그먼트 코드를 사용하여 로그를 확장할 수 있습니다.

세그먼트 코드는 워크플로우로 정의해야 합니다.

To activate this extension, check the option **[!UICONTROL Add segment code]**.

![](assets/sendinglogsextension_1.png)

For more information on segment code, refer to the [Segmentation](../../automating/using/segmentation.md) section.

**프로필 필드를 사용한 확장**

>[!NOTE]
>
>관리자가 사용자 정의 필드로 프로필 리소스를 확장했어야 합니다.

![](assets/sendinglogsextension_2.png)

Click **[!UICONTROL Add field]** and select any custom field from the profile resource.

In order to generate a new sub-dimension linked to the Profile dimension, check the **[!UICONTROL Add this field in Dynamic reporting as a new dimension]** option.

![](assets/sendinglogsextension_3.png)

동적 보고에서 사용자 지정 필드 차원을 자유 형식 테이블로 드래그 앤 드롭할 수 있습니다.

For more information on Dynamic Reporting, refer to the [List of components](../../reporting/using/list-of-components-.md).

>[!CAUTION]
>
>동적 보고에 전송된 필드 수는 20 개로 제한됩니다.

## Editing resource properties {#editing-resource-properties}

In the custom resource screen, the **[!UICONTROL Summary]** pane indicates the status of the newly created resource. 액세스 및 일반 속성을 관리할 수 있습니다.

![](assets/schema_extension_3.png)

1. **[!UICONTROL Edit properties]** 단추를 클릭하여 설명을 추가합니다.

   ![](assets/schema_extension_30.png)

1. 필요한 경우 리소스의 레이블과 ID를 수정합니다.
1. 이 리소스에 대한 액세스를 특정 조직 단위로 제한하려면 여기에 지정합니다. 허가된 유닛의 사용자만 애플리케이션에서 이 리소스를 사용할 수 있습니다.
1. 수정 내용을 저장합니다.

수정 사항이 저장됩니다. 리소스를 적용하려면 리소스를 다시 게시해야 합니다.

## Generating a unique ID for profiles and custom resources {#generating-a-unique-id-for-profiles-and-custom-resources}

기본적으로 프로필 및 사용자 지정 리소스에는 만들 때 비즈니스 ID가 없습니다. 요소를 만들 때 고유 ID를 자동으로 생성하는 옵션을 활성화할 수 있습니다. 이 ID를 사용하여 다음 작업을 수행할 수 있습니다.

* 외부 툴에서 내보낸 기록을 손쉽게 식별할 수 있습니다.
* 다른 애플리케이션에서 처리된 업데이트된 데이터를 가져올 때 레코드를 조정합니다.

프로필 및 사용자 지정 리소스만 사용할 수 있습니다.

1. 프로필 리소스에 대한 확장을 만들거나 새 리소스를 만듭니다.
1. In the data structure definition, check the **[!UICONTROL Add automatic ID field]** option, under the **[!UICONTROL Fields]** section.
1. 리소스에 수정한 내용을 저장하고 게시합니다. API를 통해 만든 요소에 이 메커니즘을 적용하려면 API를 확장하는 옵션을 선택합니다.

The **[!UICONTROL ACS ID]** field is now available and automatically populated when new elements are created manually, from the API, or inserted from an import workflow. ACS ID 필드는 UUID 필드이며 인덱스가 지정됩니다.

When exporting profiles or custom resources, you can now add the **[!UICONTROL ACS ID]** column if it has been enabled for that resource. 외부 도구에서 이 ID를 재사용하여 레코드를 식별할 수 있습니다.

![](assets/export_id_field.png)

다른 응용 프로그램 (예: CRM) 에서 처리/업데이트한 데이터를 다시 가져올 때 이 고유 ID를 사용하여 쉽게 조정할 수 있습니다.

>[!NOTE]
>
>The **[!UICONTROL ACS ID]** field is not updated for profiles or elements created before activating the option. 새 레코드만 ACS ID가 있습니다. 이 필드는 읽기 전용 모드입니다. 수정할 수는 없습니다.

