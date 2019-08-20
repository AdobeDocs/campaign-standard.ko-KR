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
source-git-commit: 888cf4cd7bfa7f82bfe70c408f8c2785c51c36e2

---


# 리소스 데이터 구조 구성{#configuring-the-resource-s-data-structure}

새 사용자 지정 리소스를 만든 후 데이터 구조를 구성해야 합니다.

리소스를 편집할 때 **[!UICONTROL Data structure]** 탭에서 다음을 추가할 수 있습니다.

* [필드](../../developing/using/configuring-the-resource-s-data-structure.md#adding-fields-to-a-resource)
* [식별 키](../../developing/using/configuring-the-resource-s-data-structure.md#defining-identification-keys)
* [색인](../../developing/using/configuring-the-resource-s-data-structure.md#defining-indexes)
* [링크](../../developing/using/configuring-the-resource-s-data-structure.md#defining-links-with-other-resources)
* [로그 보내기](../../developing/using/configuring-the-resource-s-data-structure.md#defining-sending-logs-extension)

## 리소스에 필드 추가 {#adding-fields-to-a-resource}

상자에 새 필드를 추가하여 박스 데이터 모델의 일부가 아닌 데이터를 저장할 수 있습니다.

1. **[!UICONTROL Create element]** 단추를 사용하여 필드를 만듭니다.
1. 레이블, ID, 필드 유형을 지정하고 이 필드에 대해 허가된 최대 길이를 정의합니다.

   **[!UICONTROL ID]** 필드는 필수 필드이며 추가된 각 필드에 대해 고유해야 합니다.

   >[!NOTE]
   >
   >**[!UICONTROL Label]** 필드를 비워 두면 ID에서 자동으로 완성됩니다.
   >최대 30 자를 사용하는 것이 좋습니다.

   ![](assets/schema_extension_4.png)

1. 필드 중 하나를 수정하려면 **[!UICONTROL Edit Properties]** 단추를 선택합니다.

   ![](assets/schema_extension_24.png)

1. **[!UICONTROL Field definition]** 화면에서 대상 및 타깃팅에 사용할 카테고리를 정의하거나 설명을 추가할 수 있습니다.

   ![](assets/schema_extension_5.png)

1. 사용자에게 제공할 값을 정의해야 하는 경우 **[!UICONTROL Specify a list of authorized values]** 옵션을 선택합니다 (열거형 값).

   그런 다음 AND를 **[!UICONTROL Create element]** 클릭하여 **[!UICONTROL Label]** AND **[!UICONTROL Value]**&#x200B;를 지정합니다. 필요한 만큼 값을 추가합니다.

1. 필드를 추가한 후에는 작성 날짜, 리소스를 만든 사용자, 날짜 및 마지막 수정 작성자를 포함하는 필드를 포함하려면 **[!UICONTROL Add audit fields]** 상자를 선택합니다.
1. **[!UICONTROL Add access authorization management fields]** 특정 리소스에 대한 액세스 권한이 있는 사람을 설명하는 필드를 포함하려면 상자를 선택합니다.

   이러한 필드는 데이터베이스 업데이트가 수행된 후 표시할 수 있는 데이터 및 메타데이터에 나타납니다. 이에 대한 자세한 내용은 데이터베이스 구조 [업데이트](../../developing/using/updating-the-database-structure.md) 섹션을 참조하십시오.

1. **[!UICONTROL Add automatic ID]** 필드를 확인하여 ID를 자동으로 생성합니다. 기존 개체는 비어 있는 상태로 유지됩니다.
1. 목록 및 작성 단계에서 리소스 요소의 이름이 표시되는 방식을 수정하려면 **[!UICONTROL Personalize the resource title]** 상자를 선택합니다. 이 리소스에 대해 만든 필드를 선택합니다.

   ![](assets/schema_extension_18.png)

이제 리소스 필드가 정의됩니다.

## 식별 키 정의 {#defining-identification-keys}

각 리소스에는 고유 키가 하나 이상 있어야 합니다. 예를 들어 두 제품이 구매 테이블에서 동일한 ID를 가질 수 없도록 키를 지정할 수 있습니다.

1. 기술 키를 자동으로 및 증분 생성하려는 경우 **[!UICONTROL Automatic primary key]** 저장소 크기를 섹션에 지정합니다.

   ![](assets/schema_extension_6.png)

1. **[!UICONTROL Create element]** 단추를 사용하여 키를 만듭니다.

   **[!UICONTROL Label]** And **[!UICONTROL ID]** 필드는 기본적으로 완료되지만 편집할 수 있습니다.

   >[!NOTE]
   >
   >최대 30 자를 사용하는 것이 좋습니다.

1. 이 키를 구성하는 요소를 정의하려면 이 리소스에 대해 만든 필드를 클릭하고 **[!UICONTROL Create element]** 선택합니다.

   ![](assets/schema_extension_7.png)

   생성된 키가 **[!UICONTROL Custom keys]** 섹션에 표시됩니다.

이제 리소스에 대한 식별 키가 만들어집니다.

## 색인 정의 {#defining-indexes}

인덱스는 하나 또는 여러 개의 리소스 필드를 참조할 수 있습니다. 인덱스를 사용하면 데이터베이스를 보다 쉽게 복구하기 위해 데이터베이스를 정렬할 수 있습니다. SQL 쿼리의 성능을 최적화합니다.

색인 정의는 권장되지만 필수는 아닙니다.

1. **[!UICONTROL Create element]** 단추를 사용하여 색인을 만듭니다.

   ![](assets/schema_extension_26.png)

1. **[!UICONTROL Label]** And **[!UICONTROL ID]** 필드는 기본적으로 완료되지만 편집할 수 있습니다.

   >[!NOTE]
   >
   >최대 30 자를 사용하는 것이 좋습니다.

1. 이 색인을 구성하는 요소를 정의하려면 이 리소스에 대해 만든 필드를 선택합니다.

   ![](assets/schema_extension_27.png)

1. **[!UICONTROL Confirm]**&#x200B;을 클릭합니다.

만들어진 인덱스가 **[!UICONTROL Index]** 섹션의 목록에 나타납니다.

## 다른 리소스와 링크 정의 {#defining-links-with-other-resources}

링크 세부 사항은 한 테이블에 다른 표가 있는 연관입니다.

1. **[!UICONTROL Create element]** 단추를 사용하여 대상 리소스에 대한 링크를 만듭니다.
1. **[!UICONTROL Select a target resource]**&#x200B;을 클릭합니다.

   ![](assets/schema_extension_28.png)

1. 리소스는 알파벳 순으로 표시되며 이름별로 필터링할 수 있습니다. 기술 이름이 대괄호로 표시됩니다.

   목록에서 요소를 선택하고 **[!UICONTROL Confirm]**&#x200B;를 클릭합니다.

   ![](assets/schema_extension_9.png)

1. 기호에 **[!UICONTROL Link type]** 따라를 선택합니다. 선택한 카디널리티 유형에 따라 레코드가 삭제되거나 중복되는 경우의 동작은 달라질 수 있습니다.

   다양한 링크 유형은 다음과 같습니다.

   * **[!UICONTROL 1 cardinality simple link]**: 소스 테이블 한 개가 대상 테이블에 대해 가장 하나의 해당 발생을 가질 수 있습니다.
   * **[!UICONTROL N cardinality collection link]**: 소스 테이블 한 번 발생에는 몇 가지 해당 대상 테이블이 있을 수 있지만, 대상 테이블 한 개가 소스 테이블의 해당 발생을 가장 한 개 이상 가질 수 있습니다.
   * **[!UICONTROL 0 or 1 cardinality simple link]**: 소스 테이블 한 번 발생 시 해당 대상 테이블 중 가장 하나의 해당 발생이나 없음 중 하나만 있을 수 있습니다. 이 종류의 경우 성능 **[!UICONTROL Link type]** 문제가 발생할 수 있습니다.
   ![](assets/schema_extension_29.png)

1. **[!UICONTROL New link]** 화면에서 **[!UICONTROL Label]** 및 **[!UICONTROL ID]** 필드는 기본적으로 완료되지만 편집할 수 있습니다.

   >[!NOTE]
   >
   >최대 30 자를 사용하는 것이 좋습니다.

   >[!CAUTION]
   >
   >만든 후에는 링크의 이름을 변경할 수 없습니다. 링크의 이름을 변경하려면 링크를 삭제하고 다시 만들어야 합니다.

1. **[!UICONTROL Category for the audience and targeting]** 목록을 사용하면 이 링크를 카테고리에 할당하여 쿼리 편집기 도구에서 더 볼 수 있습니다.
1. 필요한 경우 **[!UICONTROL Reverse link definition]** 이 섹션에서는 타깃팅된 리소스에 리소스의 레이블과 ID를 표시할 수 있습니다.
1. 섹션의 링크에서 참조하는 레코드의 동작을 **[!UICONTROL Behavior if deleted/duplicated]** 정의합니다.

   기본적으로, Target 레코드는 링크가 더 이상 참조되지 않을 때 삭제됩니다.

   ![](assets/schema_extension_16.png)

1. **[!UICONTROL Join definition]** 섹션에서 기본 **[!UICONTROL Use the primary keys to make the join]** 옵션을 선택했지만 두 옵션 중 하나를 선택할 수 있습니다.

   * **[!UICONTROL Use the primary key to make the join]**: 이 가입 참여 정의를 사용하면 프로필 기본 키를 사용하여 구매의 기본 키와 조정할 수 있습니다.
   * **[!UICONTROL Define specific join conditions]**: 이 가입 참여 정의를 사용하면 두 리소스 모두에 참여할 필드를 수동으로 선택할 수 있습니다. 데이터가 올바르게 구성되지 않으면 **구매** 레코드가 표시되지 않습니다.
   ![](assets/schema_extension_17.png)

만들어진 링크가 **[!UICONTROL Links]** 섹션의 목록에 표시됩니다.

**예: 생성된 리소스를'Profiles'리소스와 연결**

이 예에서는 새 리소스 **구매를** **프로필** 사용자 지정 리소스와 연결합니다.

1. 새 **구매** 리소스를 만듭니다.
1. **프로필** 사용자 지정 리소스와 연결하려면 탭에서 **[!UICONTROL Links]** 섹션을 펼친 **[!UICONTROL Data structure]****[!UICONTROL Create element]**&#x200B;다음을 클릭합니다.
1. 여기에서 타겟 리소스를 선택합니다 **[!UICONTROL Profiles (profile)]**.
1. 이 예에서는 기본 **[!UICONTROL 1 cardinality simple link]** 링크 유형을 선택된 상태로 유지합니다.

   ![](assets/custom_resource_link_to_profile_2.png)

1. 참여 정의를 선택합니다. 기본값을 **[!UICONTROL Use the primary key to make the join]**&#x200B;유지합니다.

   ![](assets/custom_resource_link_to_profile_3.png)

1. 필요한 경우 세부 사항 화면을 정의하여 **구매를** 편집하고 프로필에 연결할 수 있습니다.

   **[!UICONTROL Detail screen configuration]** 섹션을 펼친 다음, **[!UICONTROL Define a detail screen]** 리소스의 각 요소에 해당하는 화면을 구성하려면을 (를) 선택합니다. 이 확인란을 선택하지 않으면 리소스에 대한 세부 사항 보기에 액세스할 수 없습니다.

1. **[!UICONTROL Create element]**&#x200B;을 클릭합니다.
1. 연결된 리소스를 선택하고 **[!UICONTROL Add]**&#x200B;를 클릭합니다.

   그런 다음 **[!UICONTROL Client data]** &gt; **[!UICONTROL Purchase]**&#x200B;를 선택하여 고급 메뉴에서 새 리소스를 사용할 수 있습니다.

   ![](assets/custom_resource_link_to_profile_4.png)

1. 구성이 **[!UICONTROL Confirm]**&#x200B;완료되면을 클릭합니다.

   이제 새 리소스를 게시할 수 있습니다.

이 링크를 추가하면 &gt; 메뉴에서 프로필 세부 사항 화면에 **구매** 탭이 **[!UICONTROL Profiles & audiences]****[!UICONTROL Profiles]** 추가됩니다. 이것은 리소스에 따라 **[!UICONTROL Profile]** 다릅니다.

![](assets/custom_resource_link_to_profile.png)

## Send 로그 확장 정의 {#defining-sending-logs-extension}

전송 로그 확장 기능을 사용하면 다음을 수행할 수 있습니다.

* 프로필 사용자 지정 필드를 **추가하여 동적 보고서 기능을 확장하려면**
* 세그먼트 코드 및 프로필 데이터를 사용하여 **데이터 전송을 확장하려면**

**세그먼트 코드로 확장**

사용자는 워크플로우 엔진에서 나오는 세그먼트 코드를 사용하여 로그를 확장할 수 있습니다.

세그먼트 코드는 워크플로우로 정의해야 합니다.

이 확장을 활성화하려면 옵션을 **[!UICONTROL Add segment code]**&#x200B;선택합니다.

![](assets/sendinglogsextension_1.png)

세그먼트 코드에 대한 자세한 내용은 [세그멘테이션](../../automating/using/segmentation.md) 섹션을 참조하십시오.

**프로필 필드를 사용한 확장**

>[!NOTE]
>
>관리자가 사용자 정의 필드로 프로필 리소스를 확장했어야 합니다.

![](assets/sendinglogsextension_2.png)

프로필 리소스에서 사용자 지정 필드를 클릭하여 **[!UICONTROL Add field]** 선택합니다.

프로필 차원에 연결된 새 하위 차원을 생성하려면 **[!UICONTROL Add this field in Dynamic reporting as a new dimension]** 옵션을 선택합니다.

![](assets/sendinglogsextension_3.png)

동적 보고에서 사용자 지정 필드 차원을 자유 형식 테이블로 드래그 앤 드롭할 수 있습니다.

동적 보고에 대한 자세한 내용은 구성 요소 [목록을](../../reporting/using/list-of-components-.md)참조하십시오.

>[!CAUTION]
>
>동적 보고에 전송된 필드 수는 20 개로 제한됩니다.

## 리소스 속성 편집 {#editing-resource-properties}

사용자 지정 리소스 화면에서 **[!UICONTROL Summary]** 창은 새로 만든 리소스의 상태를 나타냅니다. 액세스 및 일반 속성을 관리할 수 있습니다.

![](assets/schema_extension_3.png)

1. **[!UICONTROL Edit properties]** 단추를 클릭하여 설명을 추가합니다.

   ![](assets/schema_extension_30.png)

1. 필요한 경우 리소스의 레이블과 ID를 수정합니다.

   >[!NOTE]
   >
   >최대 30 자를 사용하는 것이 좋습니다.

1. 이 리소스에 대한 액세스를 특정 조직 단위로 제한하려면 여기에 지정합니다. 허가된 유닛의 사용자만 애플리케이션에서 이 리소스를 사용할 수 있습니다.
1. 수정 내용을 저장합니다.

수정 사항이 저장됩니다. 리소스를 적용하려면 리소스를 다시 게시해야 합니다.

## 프로필 및 사용자 지정 리소스에 대한 고유 ID 생성 {#generating-a-unique-id-for-profiles-and-custom-resources}

기본적으로 프로필 및 사용자 지정 리소스에는 만들 때 비즈니스 ID가 없습니다. 요소를 만들 때 고유 ID를 자동으로 생성하는 옵션을 활성화할 수 있습니다. 이 ID를 사용하여 다음 작업을 수행할 수 있습니다.

* 외부 툴에서 내보낸 기록을 손쉽게 식별할 수 있습니다.
* 다른 애플리케이션에서 처리된 업데이트된 데이터를 가져올 때 레코드를 조정합니다.

프로필 및 사용자 지정 리소스만 사용할 수 있습니다.

1. 프로필 리소스에 대한 확장을 만들거나 새 리소스를 만듭니다.
1. 데이터 구조 정의에서 섹션 아래에 **[!UICONTROL Add automatic ID field]** 있는 옵션을 **[!UICONTROL Fields]** 선택합니다.
1. 리소스에 수정한 내용을 저장하고 게시합니다. API를 통해 만든 요소에 이 메커니즘을 적용하려면 API를 확장하는 옵션을 선택합니다.

이제 새 요소가 수동으로, API에서 또는 가져오기 워크플로우에서 삽입되면 **[!UICONTROL ACS ID]** 필드를 사용할 수 있고 자동으로 채워집니다. ACS ID 필드는 UUID 필드이며 인덱스가 지정됩니다.

프로필 또는 사용자 지정 리소스를 내보낼 때 해당 리소스에 대해 활성화된 **[!UICONTROL ACS ID]** 경우 열을 추가할 수 있습니다. 외부 도구에서 이 ID를 재사용하여 레코드를 식별할 수 있습니다.

![](assets/export_id_field.png)

다른 응용 프로그램 (예: CRM) 에서 처리/업데이트한 데이터를 다시 가져올 때 이 고유 ID를 사용하여 쉽게 조정할 수 있습니다.

>[!NOTE]
>
>옵션을 활성화하기 전에 만든 프로필 또는 요소에 대해서는 **[!UICONTROL ACS ID]** 필드가 업데이트되지 않습니다. 새 레코드만 ACS ID가 있습니다. 이 필드는 읽기 전용 모드입니다. 수정할 수는 없습니다.

