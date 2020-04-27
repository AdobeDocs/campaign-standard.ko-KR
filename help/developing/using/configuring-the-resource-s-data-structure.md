---
title: 리소스의 데이터 구조 구성
description: 데이터 구조를 구성하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: 60fe80c0-9df6-4808-a432-60a1977216ea
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: adding-or-extending-a-resource
discoiquuid: 4f22ee35-1d5f-4c75-95b4-3e38b85de26e
context-tags: cusResource,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 6cf00f9b9bafdd54d8424a353b33dc689c0f59aa

---


# 리소스의 데이터 구조 구성{#configuring-the-resource-s-data-structure}

새 사용자 지정 리소스를 만든 후 데이터 구조를 구성해야 합니다.

리소스를 편집할 때 **[!UICONTROL Data structure]** 탭에서 다음을 추가할 수 있습니다.

* [필드](#adding-fields-to-a-resource)
* [식별 키](#defining-identification-keys)
* [인덱스](#defining-indexes)
* [링크](#defining-links-with-other-resources)
* [로그 보내기](#defining-sending-logs-extension)

## 리소스에 필드 추가 {#adding-fields-to-a-resource}

새로운 필드를 리소스에 추가하여 기본 데이터 모델의 일부가 아닌 데이터를 저장할 수 있습니다.

1. 이 **[!UICONTROL Create element]** 단추를 사용하여 필드를 만듭니다.
1. 레이블, ID, 필드 유형을 지정하고 이 필드에 대해 허가된 최대 길이를 정의합니다.

   필드는 필수 항목이며 추가된 각 필드에 대해 고유해야 합니다. **[!UICONTROL ID]**

   >[!NOTE]
   >
   >최대 30자를 사용합니다.

   ![](assets/schema_extension_4.png)

1. 필드 중 하나를 수정하려면 **[!UICONTROL Edit Properties]** 단추를 선택합니다.

   ![](assets/schema_extension_24.png)

1. 화면에서 대상 및 타깃팅에 사용할 범주를 정의하거나 설명을 추가할 수도 있습니다. **[!UICONTROL Field definition]**

   ![](assets/schema_extension_5.png)

1. 사용자에게 제공할 값(열거형 값)을 정의해야 하는 경우 **[!UICONTROL Specify a list of authorized values]** 옵션을 선택합니다.

   그런 다음 을 **[!UICONTROL Create element]** 클릭하고 **[!UICONTROL Label]** 및 를 **[!UICONTROL Value]**&#x200B;지정합니다. 필요한 만큼 값을 추가합니다.

1. 필드를 추가한 후, 작성 날짜, 리소스를 만든 사용자, 날짜 및 마지막 수정 내용의 작성자를 설명하는 필드를 포함하려면 **[!UICONTROL Add audit fields]** 확인란을 선택합니다.
1. 특정 리소스에 대한 액세스 권한이 있는 사람을 설명하는 필드를 포함하려면 **[!UICONTROL Add access authorization management fields]** 확인란을 선택합니다.

   이러한 필드는 데이터베이스 업데이트가 수행되면 표시할 수 있는 데이터 및 메타데이터에 나타납니다. 자세한 내용은 데이터베이스 구조 [업데이트](../../developing/using/updating-the-database-structure.md) 섹션을 참조하십시오.

1. ID를 자동으로 생성하려면 **[!UICONTROL Add automatic ID]** 필드를 선택합니다. 기존 엔티티는 여전히 비어 있습니다. 자세한 내용은 프로필 및 사용자 [지정 리소스에](../../developing/using/configuring-the-resource-s-data-structure.md#generating-a-unique-id-for-profiles-and-custom-resources)대한 고유 ID 생성을 참조하십시오.
1. 목록 및 작성 단계에서 리소스 요소의 이름이 표시되는 방식을 수정하려면 **[!UICONTROL Customize the title of the resource elements]** 상자를 선택합니다. 이 리소스에 대해 만든 필드에서 필드를 선택합니다.

   ![](assets/schema_extension_18.png)

   >[!NOTE]
   >
   >이 옵션을 선택하지 않으면 이 테이블의 모든 엔티티를 나열할 때 자동 기본 키(엔티티가 테이블에 추가될 때마다 자동으로 생성됨)가 사용됩니다.

이제 리소스의 필드가 정의됩니다.

## ID 키 정의 {#defining-identification-keys}

각 리소스에는 하나 이상의 고유 키가 있어야 합니다. 예를 들어 두 제품이 구매 테이블에서 동일한 ID를 가질 수 없도록 키를 지정할 수 있습니다.

1. 기술 키를 자동으로 점진적으로 생성하려는 경우 **[!UICONTROL Automatic primary key]** 섹션에서 스토리지 크기를 지정합니다.

   ![](assets/schema_extension_6.png)

1. 단추를 사용하여 **[!UICONTROL Create element]** 키를 만듭니다.

   및 **[!UICONTROL Label]** **[!UICONTROL ID]** 필드는 기본적으로 완료되지만 편집할 수 있습니다.

   >[!NOTE]
   >
   >최대 30자를 사용합니다.

1. 이 키를 구성하는 요소를 정의하려면 을 클릭하고 이 리소스에 대해 만든 필드를 **[!UICONTROL Create element]** 선택합니다.

   ![](assets/schema_extension_7.png)

   생성된 키는 **[!UICONTROL Custom keys]** 섹션에 표시됩니다.

이제 리소스에 대한 ID 키가 만들어집니다.

>[!NOTE]
>
>식별 키를 만들 때의 모범 사례에 대한 자세한 내용은 이 [섹션을](../../developing/using/data-model-best-practices.md#keys)참조하십시오.

## 인덱스 정의 {#defining-indexes}

인덱스는 하나 또는 여러 리소스 필드를 참조할 수 있습니다. 인덱스를 사용하면 데이터베이스를 통해 레코드를 보다 쉽게 복구할 수 있습니다. SQL 쿼리의 성능을 최적화합니다.

인덱스를 정의하는 것은 권장되지만 필수는 아닙니다.

1. 이 **[!UICONTROL Create element]** 단추를 사용하여 색인을 만듭니다.

   ![](assets/schema_extension_26.png)

1. 및 **[!UICONTROL Label]** **[!UICONTROL ID]** 필드는 기본적으로 완료되지만 편집할 수 있습니다.

   >[!NOTE]
   >
   >최대 30자를 사용합니다.

1. 이 색인을 구성하는 요소를 정의하려면 이 리소스에 대해 만든 필드 중에서 필드를 선택합니다.

   ![](assets/schema_extension_27.png)

1. 클릭 **[!UICONTROL Confirm]**.

만들어진 인덱스가 **[!UICONTROL Index]** 섹션의 목록에 나타납니다.

>[!NOTE]
>
>색인을 만들 때의 우수 사례에 대한 자세한 내용은 이 [섹션을](../../developing/using/data-model-best-practices.md#indexes)참조하십시오.

## 다른 리소스와 링크 정의 {#defining-links-with-other-resources}

링크는 한 테이블에 다른 테이블과 연결되어 있는 연결에 대해 자세히 설명합니다.

1. 단추를 사용하여 타겟 리소스에 대한 링크를 만듭니다. **[!UICONTROL Create element]**
1. 클릭 **[!UICONTROL Select a target resource]**.

   ![](assets/schema_extension_28.png)

1. 리소스는 알파벳 순서로 표시되며 이름으로 필터링할 수 있습니다. 그들의 기술 이름은 대괄호로 표시됩니다.

   목록에서 요소를 선택하고 을 **[!UICONTROL Confirm]**&#x200B;클릭합니다.

   ![](assets/schema_extension_9.png)

1. 카디널리티에 따라 를 **[!UICONTROL Link type]** 선택합니다. 선택한 카디널리티 유형에 따라 레코드가 삭제되거나 중복되는 경우의 동작이 달라질 수 있습니다.

   다양한 링크 유형은 다음과 같습니다.

   * **[!UICONTROL 1 cardinality simple link]**:소스 테이블 중 한 개는 대상 테이블에 해당하는 항목을 최대 한 개 가질 수 있습니다.
   * **[!UICONTROL N cardinality collection link]**:소스 테이블 일수에 따라 타겟 테이블에 몇 가지 해당 항목이 있을 수 있지만, 타겟 테이블 일수에 관계없이 소스 테이블에 해당하는 항목이 한 개 이상 있을 수 있습니다.
   * **[!UICONTROL 0 or 1 cardinality simple link]**:소스 테이블 중 한 가지에는 대상 테이블에 해당하는 항목이 하나 이상 있거나 없을 수 있습니다. 이러한 유형의 경우 성능 문제가 발생할 **[!UICONTROL Link type]** 수 있습니다.
   ![](assets/schema_extension_29.png)

1. 화면에서 **[!UICONTROL New link]** 및 **[!UICONTROL Label]** **[!UICONTROL ID]** 필드는 기본적으로 완료되지만 편집할 수 있습니다.

   >[!NOTE]
   >
   >최대 30자를 사용합니다.

   >[!IMPORTANT]
   >
   >만든 후에는 링크 이름을 변경할 수 없습니다. 링크 이름을 변경하려면 링크를 삭제하고 다시 만들어야 합니다.

1. 이 **[!UICONTROL Category for the audience and targeting]** 목록을 사용하면 이 링크를 카테고리에 할당하여 쿼리 편집기 도구에서 보다 쉽게 볼 수 있습니다.
1. 필요한 경우 **[!UICONTROL Reverse link definition]** 섹션에서 타깃팅된 리소스에 있는 리소스의 레이블과 ID를 표시할 수 있습니다.
1. 섹션의 링크에서 참조하는 레코드의 동작을 정의합니다. **[!UICONTROL Behavior if deleted/duplicated]**

   기본적으로 대상 레코드는 더 이상 링크에서 참조되지 않으면 삭제됩니다.

   ![](assets/schema_extension_16.png)

1. 섹션에서 기본 **[!UICONTROL Join definition]** **[!UICONTROL Use the primary keys to make the join]** 옵션이 선택되지만 다음 두 옵션 중 하나를 선택할 수 있습니다.

   * **[!UICONTROL Use the primary key to make the join]**:이 조인 정의를 사용하면 프로필 기본 키를 사용하여 구매의 기본 키와 조정할 수 있습니다.
   * **[!UICONTROL Define specific join conditions]**:이 조인 정의를 사용하면 두 리소스를 모두 연결할 필드를 수동으로 선택할 수 있습니다. 데이터가 올바르게 구성되지 않으면 구매 **레코드가** 표시되지 않습니다.
   ![](assets/schema_extension_17.png)

만들어진 링크는 **[!UICONTROL Links]** 섹션의 목록에 표시됩니다.

>[!NOTE]
>
>색인을 만들 때의 우수 사례에 대한 자세한 내용은 이 [섹션을](../../developing/using/data-model-best-practices.md#links)참조하십시오.

**예:생성된 리소스를 &#39;프로필&#39; 리소스와 연결**

이 예에서는 새 리소스 Purchase를 프로필 **사용자** 지정 리소스와 연결하려고 **** 합니다.

1. 새 구매 **리소스를 만듭니다** .
1. 프로필 사용자 지정 **리소스와 연결하려면** 탭에서 **[!UICONTROL Links]** 섹션을 펼친 후 **[!UICONTROL Data structure]** 을 **[!UICONTROL Create element]**&#x200B;클릭합니다.
1. 여기에서 대상 리소스를 선택합니다 **[!UICONTROL Profiles (profile)]**.
1. 이 예에서는 기본 링크 유형을 **[!UICONTROL 1 cardinality simple link]** 선택된 상태로 유지합니다.

   ![](assets/custom_resource_link_to_profile_2.png)

1. 조인 정의를 선택하고 기본값을 그대로 **[!UICONTROL Use the primary key to make the join]**&#x200B;둡니다.

   ![](assets/custom_resource_link_to_profile_3.png)

1. 필요한 경우 세부 사항 화면을 정의하여 구매를 편집하고 **프로필에** 연결할 수 있습니다.

   섹션을 **[!UICONTROL Detail screen configuration]** 펼쳐서 **[!UICONTROL Define a detail screen]** 리소스의 각 요소에 해당하는 화면을 구성하는 방법을 확인합니다. 이 확인란을 선택하지 않으면 이 리소스의 세부 사항 보기에 액세스할 수 없습니다.

1. 클릭 **[!UICONTROL Create element]**.
1. 연결된 리소스를 선택하고 을 **[!UICONTROL Add]**&#x200B;클릭합니다.

   그런 다음 **[!UICONTROL Client data]** > **[!UICONTROL Purchase]**&#x200B;을 선택하여 고급 메뉴에서 새 리소스를 사용할 수 있습니다.

   ![](assets/custom_resource_link_to_profile_4.png)

1. 구성이 완료되면 을 **[!UICONTROL Confirm]**&#x200B;클릭합니다.

   이제 새 리소스를 게시할 수 있습니다.

이 링크를 추가하면 **>** 메뉴에서 구매 **[!UICONTROL Profiles & audiences]** **[!UICONTROL Profiles]** 탭이 프로필 세부 사항 화면에 추가됩니다. 이는 **[!UICONTROL Profile]** 리소스에 따라 다릅니다.

![](assets/custom_resource_link_to_profile.png)

## 전송 로그 확장 정의 {#defining-sending-logs-extension}

전송 로그 익스텐션을 사용하면 다음 작업을 수행할 수 있습니다.

* 프로필 사용자 지정 필드를 **추가하여 동적 보고서 기능을 확장하려면**
* to extend sending logs data with **segment code and profile data**

**세그먼트 코드로 확장**

사용자는 워크플로우 엔진에서 생성된 세그먼트 코드를 사용하여 로그를 확장할 수 있습니다.

세그먼트 코드는 워크플로우에 정의해야 합니다.

이 확장을 활성화하려면 옵션을 **[!UICONTROL Add segment code]**&#x200B;선택합니다.

![](assets/sendinglogsextension_1.png)

세그먼트 코드에 대한 자세한 내용은 세그멘테이션 [섹션을 참조하십시오](../../automating/using/segmentation.md) .

**프로필 필드를 사용하여 확장**

>[!NOTE]
>
>관리자는 사용자 정의 필드로 프로필 리소스를 확장해야 합니다.

![](assets/sendinglogsextension_2.png)

프로필 리소스에서 사용자 정의 필드를 **[!UICONTROL Add field]** 클릭하고 선택합니다.

프로파일 차원에 연결된 새 하위 차원을 생성하려면 **[!UICONTROL Add this field in Dynamic reporting as a new dimension]** 옵션을 선택합니다.

![](assets/sendinglogsextension_3.png)

동적 보고에서 사용자 지정 필드 차원을 자유 형식 테이블로 드래그하여 놓을 수 있습니다.

동적 보고에 대한 자세한 내용은 구성 요소 [목록을 참조하십시오](../../reporting/using/list-of-components-.md).

>[!IMPORTANT]
>
>동적 보고로 전송된 필드 수는 20개로 제한됩니다.

## 리소스 속성 편집 {#editing-resource-properties}

사용자 지정 리소스 화면에서 **[!UICONTROL Summary]** 창은 새로 만든 리소스의 상태를 나타냅니다. 액세스 및 일반 속성을 관리할 수 있습니다.

![](assets/schema_extension_3.png)

1. 설명을 추가하려면 **[!UICONTROL Edit properties]** 단추를 클릭합니다.

   ![](assets/schema_extension_30.png)

1. 필요한 경우 리소스의 레이블과 ID를 수정합니다.

   >[!NOTE]
   >
   >최대 30자를 사용합니다.

1. 이 리소스에 대한 액세스를 특정 조직 단위로 제한해야 하는 경우 여기에서 지정합니다. 인가된 장치의 사용자만 응용 프로그램에서 이 리소스로 작업할 수 있습니다.
1. 수정 내용을 저장합니다.

수정 내용이 저장됩니다. 리소스를 적용하려면 리소스를 다시 게시해야 합니다.

## 프로필 및 사용자 지정 리소스에 대한 고유 ID 생성 {#generating-a-unique-id-for-profiles-and-custom-resources}

기본적으로 프로필 및 사용자 지정 리소스는 만들 때 비즈니스 ID가 없습니다. 요소를 만들 때 자동으로 고유 ID를 생성하는 옵션을 활성화할 수 있습니다. 이 ID를 사용하여 다음을 수행할 수 있습니다.

* 외부 툴에서 내보낸 레코드를 손쉽게 식별할 수 있습니다.
* 다른 애플리케이션에서 처리된 업데이트된 데이터를 가져올 때 레코드를 조정합니다.

프로필 및 사용자 지정 리소스에만 사용할 수 있습니다.

1. 프로필 리소스에 대한 확장 기능을 만들거나 새 리소스를 만듭니다.
1. 데이터 구조 정의에서 섹션 아래의 **[!UICONTROL Add automatic ID field]** 옵션을 선택합니다 **[!UICONTROL Fields]** .

   ![](assets/option_id_field.png)

   >[!NOTE]
   >
   >새 레코드에만 ACS ID가 있습니다. 이 옵션을 활성화하기 전에 생성된 프로필 또는 요소에 대해서는 필드가 비어 있는 상태로 유지됩니다. **[!UICONTROL ACS ID]**

1. 리소스에 대한 수정 내용을 저장하고 게시합니다. API를 통해 만든 요소에 이 메커니즘을 적용하려면 API를 확장하는 옵션을 선택합니다.

이제 이 **[!UICONTROL ACS ID]** 필드를 사용할 수 있으며, API에서 또는 가져오기 워크플로우에서 새 요소를 수동으로 만들거나 삽입할 때 자동으로 채워집니다. ACS ID 필드는 UUID 필드이며 인덱싱됩니다.

이제 프로필 또는 사용자 지정 리소스를 내보낼 때 해당 리소스에 대해 활성화된 경우 **[!UICONTROL ACS ID]** 열을 추가할 수 있습니다. 외부 도구에서 이 ID를 다시 사용하여 레코드를 식별할 수 있습니다.

![](assets/export_id_field.png)

다른 응용 프로그램(예: CRM)에서 처리/업데이트된 데이터를 다시 가져올 때 이 고유 ID로 쉽게 조정할 수 있습니다.

>[!NOTE]
>
>옵션을 활성화하기 전에 생성된 프로필 또는 요소에 대해서는 필드가 업데이트되지 않습니다. **[!UICONTROL ACS ID]** 새 레코드에만 ACS ID가 있습니다.
>
>이 필드는 읽기 전용 모드입니다. 수정할 수 없습니다.
