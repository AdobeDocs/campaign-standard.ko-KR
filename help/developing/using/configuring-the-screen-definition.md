---
title: 화면 정의 구성
description: 리소스 데이터 구조를 기반으로 새로운 Adobe Campaign 화면을 정의하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: 40848197-b1a0-4018-bfc3-7df64fb83307
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: adding-or-extending-a-resource
discoiquuid: 9dabb328-ac0c-49fd-8996-8d56341ee7ac
context-tags: cusResource,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 8852adb5edeb42eba1acf2911c988071104f1401

---


# 화면 정의 구성{#configuring-the-screen-definition}

리소스를 만들거나 기존 리소스에 새 필드를 추가할 때 인터페이스에 표시할 방법을 정의할 수 있습니다.

워크플로우, 대상 및 REST API를 통해 리소스를 채우고 해당 데이터에 액세스할 수 있으므로 이 단계는 필수가 아닙니다.

탭에서 다음을 수행할 수 **[!UICONTROL Screen definition]** 있습니다.

* 탐색 창에서 사용자 지정 리소스에 대한 액세스 추가
* 리소스를 구성하는 요소 목록이 표시되는 방식을 개인화합니다.
* 리소스의 각 요소에 대한 세부 사항 보기가 표시되는 방식을 정의합니다.

## 탐색 메뉴에서 액세스 활성화 {#enabling-access-from-the-navigation-menu}

리소스에 전용 화면이 포함되도록 하려면 탐색 메뉴에서 사용할 수 있도록 할 수 있습니다.

1. 리소스의 **[!UICONTROL Screen definition]** 탭에서 **[!UICONTROL Navigation]** 섹션을 펼칩니다.
1. 탐색 창에서 이 리소스에 대한 액세스를 허용하려면 **[!UICONTROL Add an entry in the 'Client data' section]** 상자를 선택합니다.

   ![](assets/schema_extension_19.png)

리소스는 **[!UICONTROL Client data]** 섹션 내의 하위 항목으로 나타납니다.

## 기본 목록 구성 정의 {#defining-the-default-list-configuration}

화면 정의의 **[!UICONTROL List configuration]** 섹션에서는 리소스 개요에 기본적으로 표시되는 열과 정보를 정의할 수 있습니다.

1. 리소스 열이 표시되는 방식을 정의하려면 **[!UICONTROL Customize the list configuration]** 상자를 선택합니다.
1. 이 **[!UICONTROL Create element]** 단추를 사용하여 만든 필드에서 필드를 선택합니다.
1. 만든 필드가 목록에 표시됩니다. 레이블과 너비를 편집할 수 있습니다.

   ![](assets/schema_extension_20.png)

1. 섹션에서 **[!UICONTROL Simple search]** 을 **[!UICONTROL Specify the fields to be taken into account in the search]** 선택하여 검색에 포함할 필드를 정의합니다.

   >[!IMPORTANT]
   >
   >이 구성은 기본 검색에 사용되는 필드를 대체합니다.

1. 섹션에서 **[!UICONTROL Advanced filtering]** **[!UICONTROL Add search fields]** 상자를 선택하여 단순 검색 필드 이외의 필드를 추가합니다. 예를 들어, 사용자가 만든 필드에서 &quot;날짜&quot; 필드를 선택하면 사용자는 날짜만 참조하는 검색을 수행할 수 있습니다.
1. 두 검색 유형의 필드 순서를 수정할 수 있습니다.
1. 고급 검색의 경우 연결된 리소스에 연결된 필드를 추가할 수 있습니다. 이러한 필터는 생성된 화면의 **[!UICONTROL Search]** 메뉴에 나타납니다.

이제 리소스의 개요 화면이 정의됩니다.

## 세부 정보 화면 구성 정의 {#defining-the-detail-screen-configuration}

화면 정의의 **[!UICONTROL Detail screen configuration]** 섹션에서는 리소스의 각 요소의 세부 사항 화면에 표시될 열과 정보를 정의할 수 있습니다.

1. 섹션을 **[!UICONTROL Detail screen configuration]** 펼쳐서 **[!UICONTROL Define a detail screen]** 리소스의 각 요소에 해당하는 화면을 구성하는 방법을 확인합니다. 이 확인란을 선택하지 않으면 이 리소스의 세부 사항 보기에 액세스할 수 없습니다.
1. 한 번의 클릭으로 사용자 지정 리소스의 모든 필드를 추가할 수 있습니다. 이렇게 하려면 ![](assets/addallfieldsicon.png) 아이콘을 클릭하거나 **[!UICONTROL Add an element]** 단추를 사용합니다.
1. 이 리소스에 대해 만들어진 요소에서 요소를 선택하고 필드 유형을 지정합니다.

   * **[!UICONTROL Input field]**:는 편집 가능한 필드입니다.
   * **[!UICONTROL Value]**:는 읽기 전용 필드입니다.
   * **[!UICONTROL List]**:는 테이블입니다.
   * **[!UICONTROL Separator]**:요소를 카테고리로 분할합니다.
   ![](assets/schema_extension_23.png)

1. 추가된 요소가 목록에 표시됩니다. 레이블을 편집할 수 있습니다.

   ![](assets/schema_extension_22.png)

1. 요소를 다른 카테고리로 분할하는 데 필요한 만큼 **[!UICONTROL Separator]** 추가합니다.

   이를 통해 창을 보다 효율적으로 구성할 수 있도록 구분 기호를 표시할 수 있습니다.

   ![](assets/schema_extension_25.png)

이제 리소스의 세부 정보 화면이 구성됩니다.

## 데이터 섹션의 작업 {#actions-on-data-section}

이러한 설정을 사용하면 사용자 정의 리소스 화면에 제어 막대를 표시할 수 있습니다. 다음 세 가지 옵션을 사용할 수 있습니다.

![](assets/schema_extension_actions.png)

* **[!UICONTROL Authorize creating]**:이 옵션을 사용하면 리소스의 요소 생성을 활성화할 수 있습니다. 따라서 사용자는 레코드를 추가할 수 있습니다.

   >[!NOTE]
   >
   >이 옵션을 사용하려면 먼저 리소스에 연결된 세부 정보 화면을 활성화해야 합니다.

* **[!UICONTROL Authorize duplicating]**:이 옵션을 사용하면 사용자 지정 리소스에 연결된 중복 레코드를 활성화할 수 있습니다.
* **[!UICONTROL Authorize deleting]**:이 옵션을 사용하면 사용자 지정 리소스에 연결된 레코드 삭제를 활성화할 수 있습니다.
