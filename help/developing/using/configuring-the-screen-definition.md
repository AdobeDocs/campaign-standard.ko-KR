---
title: 화면 정의 구성
seo-title: 화면 정의 구성
description: 화면 정의 구성
seo-description: 리소스 데이터 구조를 기반으로 새 Adobe Campaign 화면을 정의하는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: 40848197-B 1 A 0-4018-BFC 3-7 DF 64 FB 83307
contentOwner: Sauviat
products: sg_ campaign/standard
audience: developing
content-type: 참조
topic-tags: adding-or-extending-a-resource
discoiquuid: 9 DABB 328-AC 0 C -49 FD -8996-8 D 56341 EE 7 AC
context-tags: Cusresource, main
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: b3291f7c0cbede6a3180ad4a4ab8a365720f5031

---


# Configuring the screen definition{#configuring-the-screen-definition}

리소스를 만들거나 새 필드를 기존 리소스에 추가할 때 인터페이스에 표시할 방법을 정의할 수 있습니다.

워크플로우, 대상 및 REST API를 통해 리소스를 채우고 데이터에 액세스할 수 있으므로 이 단계는 필수가 아닙니다.

**[!UICONTROL Screen definition]** 탭에서 다음을 수행할 수 있습니다.

* 탐색 창에서 사용자 정의 리소스에 액세스 추가
* 리소스를 구성하는 요소 목록이 표시되는 방법 개인화
* 리소스의 각 요소 세부 사항 보기가 표시되는 방식을 정의합니다.

## Enabling access from the navigation menu {#enabling-access-from-the-navigation-menu}

리소스에 전용 화면을 포함하려면 탐색 메뉴에서 해당 화면을 사용할 수 있게 할 수 있습니다.

1. From the **[!UICONTROL Screen definition]** tab of the resource, unfold the **[!UICONTROL Navigation]** section.
1. Check the **[!UICONTROL Add an entry in the 'Client data' section]** box to allow access to this resource from the navigation pane.

   ![](assets/schema_extension_19.png)

The resource will appear as a sub-entry within the **[!UICONTROL Client data]** section.

## Defining the default list configuration {#defining-the-default-list-configuration}

The **[!UICONTROL List configuration]** section of the screen definition lets you define the columns and information that will be displayed by default in the overview of a resource.

1. Check the **[!UICONTROL Customize the list configuration]** box to define the way the columns of the resource are displayed.
1. **[!UICONTROL Create element]** 단추를 사용하여 만든 필드를 선택합니다.
1. 만들어진 필드가 목록에 표시됩니다. 레이블 및 너비를 편집할 수 있습니다.

   ![](assets/schema_extension_20.png)

1. **[!UICONTROL Simple search]** 섹션에서를 **[!UICONTROL Specify the fields to be taken into account in the search]** 확인하여 검색에 포함할 필드를 정의합니다.

   >[!CAUTION]
   >
   >이 구성은 기본 검색에 사용된 필드를 대체합니다.

1. **[!UICONTROL Advanced filtering]** 섹션에서 **[!UICONTROL Add search fields]** 간단한 검색 필드 이외의 필드를 추가하려면 상자를 선택합니다. 예를 들어 사용자가 만든 필드에서 "날짜" 필드를 선택하면 해당 날짜만 참조하는 검색을 수행할 수 있습니다.
1. 두 검색 유형에 대한 필드 순서를 수정할 수 있습니다.
1. 고급 검색의 경우 연결된 리소스에 연결된 필드를 추가할 수 있습니다. These filters appear in the **[!UICONTROL Search]** menu of the generated screen.

이제 리소스의 개요 화면이 정의됩니다.

## Defining the detail screen configuration {#defining-the-detail-screen-configuration}

The **[!UICONTROL Detail screen configuration]** section of the screen definition lets you define the columns and information that will be displayed in the detail screen of each element of the resource.

1. **[!UICONTROL Detail screen configuration]** 섹션을 펼친 다음, **[!UICONTROL Define a detail screen]** 리소스의 각 요소에 해당하는 화면을 구성하려면을 (를) 선택합니다. 이 확인란을 선택하지 않으면 리소스에 대한 세부 사항 보기에 액세스할 수 없습니다.
1. 한 번의 클릭으로 사용자 정의 리소스의 모든 필드를 추가할 수 있습니다. To do this, click the ![](assets/addallfieldsicon.png) icon or use the **[!UICONTROL Add an element]** button.
1. 이 리소스에 대해 만든 요소를 선택하고 필드 유형을 지정합니다.

   * **[!UICONTROL Input field]**: 편집 가능한 필드입니다.
   * **[!UICONTROL Value]**: 은 읽기 전용 필드입니다.
   * **[!UICONTROL List]**: 는 표입니다.
   * **[!UICONTROL Separator]**: 요소를 카테고리로 분할합니다.
   ![](assets/schema_extension_23.png)

1. 추가된 요소가 목록에 표시됩니다. 레이블을 편집할 수 있습니다.

   ![](assets/schema_extension_22.png)

1. Add as many **[!UICONTROL Separator]** as needed to split your elements into different categories.

   따라서 구분 기호를 표시하여 창을 보다 잘 구성할 수 있습니다.

   ![](assets/schema_extension_25.png)

이제 리소스의 세부 사항 화면이 구성됩니다.

## Actions on data section {#actions-on-data-section}

이러한 설정을 통해 사용자 지정 리소스 화면에 제어 막대를 표시할 수 있습니다. 다음 세 가지 옵션을 사용할 수 있습니다.

![](assets/schema_extension_actions.png)

* **[!UICONTROL Authorize creating]**: 이 옵션을 사용하면 리소스의 요소 만들기를 활성화할 수 있습니다. 따라서 사용자는 레코드를 추가할 수 있습니다.

   >[!NOTE]
   >
   >이 옵션을 사용하려면 먼저 리소스에 연결된 세부 정보 화면을 활성화해야 합니다.

* **[!UICONTROL Authorize duplicating]**: 이 옵션을 사용하면 사용자 지정 리소스에 연결된 레코드 복제를 활성화할 수 있습니다.
* **[!UICONTROL Authorize deleting]**: 이 옵션을 사용하면 사용자 지정 리소스에 연결된 레코드 삭제를 활성화할 수 있습니다.

