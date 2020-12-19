---
solution: Campaign Standard
product: campaign
title: 이메일 스타일 관리
description: 이메일 디자이너에서 이메일 스타일을 관리하는 방법을 알아봅니다.
audience: designing
content-type: reference
topic-tags: editing-email-content
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '1052'
ht-degree: 1%

---


# 이메일 스타일 관리 {#managing-styles}


이메일 디자이너의 요소를 선택할 때 선택한 컨텐츠 유형과 관련된 몇 가지 옵션이 **[!UICONTROL Settings]** 창에 표시됩니다. 이러한 옵션을 사용하여 이메일 스타일을 손쉽게 변경할 수 있습니다.

## {#selecting-an-element} 요소 선택

이메일 디자이너 인터페이스에서 요소를 선택하려면 다음 중 하나를 수행합니다.

* 이메일에서 직접 을 클릭하고
* 또는 왼쪽 **팔레트**&#x200B;에 있는 옵션에서 사용할 수 있는 구조 트리를 찾아봅니다.

![](assets/des_tree_structure.png)

구조 트리를 탐색하면 보다 정확하게 선택할 수 있습니다. 다음 중 하나를 선택할 수 있습니다.

* 전체 구조 구성 요소
* 구조 구성 요소를 구성하는 열 중 하나,
* 열 내에 있는 구성 요소만 포함할 수 있습니다.

![](assets/des_tree_structure_selection.png)

열을 선택하려면 다음을 수행할 수도 있습니다.

1. 구조 구성 요소를 선택합니다(이메일에서 직접 또는 왼쪽 **팔레트**&#x200B;에서 사용할 수 있는 구조 트리 사용).
1. **상황에 맞는 도구 모음**&#x200B;에서 **[!UICONTROL Select a column]**&#x200B;를 클릭하여 원하는 열을 선택합니다.

[이 섹션](#example--adjusting-vertical-alignment-and-padding)에서 예제를 참조하십시오.

## 스타일 설정 조정 중 {#adjusting-style-settings}

1. 이메일에서 요소를 선택합니다. 자세한 내용은 [요소 선택](#selecting-an-element)을 참조하십시오.
1. 필요에 따라 설정을 조정합니다. 선택한 각 요소는 서로 다른 설정 세트를 제공합니다.

   배경을 삽입하거나 크기를 변경하고 가로 또는 세로 정렬을 수정하고 색상을 관리하며 [패딩 또는 여백](#selecting-an-element) 등을 추가할 수 있습니다.

   이렇게 하려면 **[!UICONTROL Settings]** 창 또는 [인라인 스타일 특성 추가](#adding-inline-styling-attributes)에 표시된 옵션을 사용합니다.

   ![](assets/des_settings_pane.png)

1. 컨텐츠를 저장합니다.

## 패딩 및 여백 {#about-padding-and-margin} 조정

이메일 디자이너 인터페이스를 사용하면 패딩 및 여백 설정을 신속하게 조정할 수 있습니다.

**[!UICONTROL Padding]**:이 설정을 사용하면 요소의 테두리 내에 있는 공간을 관리할 수 있습니다.

![](assets/des_padding.png)

예제:

* 이미지 왼쪽 및 오른쪽 측면에 여백을 설정하려면 패딩을 사용합니다.
* 위쪽 및 아래쪽 패딩을 사용하여 **[!UICONTROL Text]** 또는 **[!UICONTROL Divider]** 구성 요소에 간격을 더 추가합니다.
* 구조 요소 내의 열 사이의 테두리를 설정하려면 각 열에 대한 패딩을 정의합니다.

**[!UICONTROL Margin]**:이 설정을 사용하면 요소의 테두리와 다음 요소 사이의 공간을 관리할 수 있습니다.

![](assets/des_margin.png)

>[!NOTE]
>
>선택 항목(구조 구성 요소, 열 또는 컨텐츠 구성 요소)에 따라 결과가 같지 않습니다. Adobe에서는 열 수준에서 **[!UICONTROL Padding]** 및 **[!UICONTROL Margin]** 매개 변수를 설정하는 것이 좋습니다.

**[!UICONTROL Padding]** 및 **[!UICONTROL Margin]** 모두에 대해 잠금 아이콘을 클릭하여 위쪽과 아래쪽 또는 오른쪽 및 왼쪽 매개 변수 간의 동기화를 중단합니다. 이를 통해 각 매개 변수를 별도로 조정할 수 있습니다.

![](assets/des_padding_lock_icon.png)

## 스타일 정렬 {#about-alignment}

* **텍스트 정렬**:텍스트 위에 마우스 커서를 놓고 상황에 맞는 툴바를 사용하여 텍스트를 정렬할 수 있습니다.

   ![](assets/des_text_alignment.png)

* **가로** 정렬을 텍스트, 이미지 및 단추에 적용할 수 있으며 현재  **[!UICONTROL Divider]** 및  **[!UICONTROL Social]** 구성 요소에 적용되지 않습니다.

   ![](assets/des_horizontal_alignment.png)

* **세로 정렬**&#x200B;을 설정하려면 구조 구성 요소 내의 열을 선택하고 설정 창에서 옵션을 선택합니다.

   ![](assets/des_set_vertical_alignment.png)

## 배경 {#about-backgrounds} 설정

>[!CONTEXTUALHELP]
>id="ac_edition_backgroundimage"
>title="배경 설정"
>abstract="전자 메일 디자이너를 사용하면 컨텐츠의 배경색 또는 배경 이미지를 맞춤화할 수 있습니다. 배경 이미지는 일부 전자 메일 클라이언트에서 지원되지 않습니다."
>additional-url="https://docs.google.com/spreadsheets/d/1TLo62YKm3tThUWDOIliCQFWs3dpNjpDfw6DdTr1oGOw/edit#gid=0" text="추가 정보"

이메일 디자이너에서 배경을 설정하는 방법은 Adobe에서 다음을 권장합니다.

1. 디자인에 필요한 경우 이메일 본문에 배경색을 적용합니다.
1. 대부분의 경우 열 수준에서 배경색을 설정합니다.
1. 관리하기가 어려우므로 이미지 또는 텍스트 구성 요소에 배경색을 사용하지 마십시오.

다음은 사용할 수 있는 배경 설정입니다.

* 전체 이메일에 대해 **[!UICONTROL Background color]**&#x200B;을 설정합니다. 왼쪽 팔레트에서 액세스할 수 있는 탐색 트리에서 본문 설정을 선택해야 합니다.

   ![](assets/des_background_body.png)

* **[!UICONTROL Viewport background color]**&#x200B;을 선택하여 모든 구조 구성 요소에 대해 동일한 배경색을 설정합니다. 이 옵션을 사용하면 배경색에서 다른 설정을 선택할 수 있습니다.

   ![](assets/des_background_viewport.png)

* 각 구조 구성 요소에 대해 다른 배경색을 설정합니다. 왼쪽 팔레트에서 액세스할 수 있는 탐색 트리에서 구조를 선택하여 해당 구조에만 특정 배경색을 적용합니다.

   ![](assets/des_background_structure.png)

   구조 배경색을 숨길 수 있으므로 뷰포트 배경색을 설정하지 마십시오.

* 구조 구성 요소의 내용에 대해 **[!UICONTROL Background image]**&#x200B;을 설정합니다.

   ![](assets/des_background_image.png)

   >[!NOTE]
   >
   >일부 이메일 프로그램은 배경 이미지를 지원하지 않습니다. 지원되지 않는 경우 행 배경색이 대신 사용됩니다. 이미지를 표시할 수 없는 경우 적절한 폴백 배경색을 선택해야 합니다.

* 열 수준에서 배경색을 설정합니다.

   ![](assets/des_background_column.png)

   >[!NOTE]
   >
   >가장 일반적인 사용 사례입니다. Adobe에서는 전체 이메일 컨텐츠를 편집할 때 유연성을 높일 수 있도록 열 수준에서 배경색을 설정하는 것이 좋습니다.

   열 수준에서 배경 이미지를 설정할 수도 있지만 거의 사용되지 않습니다.

### 예:세로 정렬 및 패딩 조정 &lt;a0//>{#example--adjusting-vertical-alignment-and-padding}

3개의 열로 구성된 구조 구성 요소 내에서 패딩 및 세로 정렬을 조정할 수 있습니다. 이렇게 하려면 아래 단계를 수행합니다:

1. 이메일에서 직접 구조 구성 요소를 선택하거나 왼쪽 **팔레트**&#x200B;에서 사용할 수 있는 구조 트리를 사용합니다.
1. **상황에 맞는 도구 모음**&#x200B;에서 **[!UICONTROL Select a column]**&#x200B;를 클릭하고 편집할 도구 모음을 선택합니다. 구조 트리에서 선택할 수도 있습니다.

   ![](assets/des_selecting_column.png)

   해당 열의 편집 가능한 매개 변수는 오른쪽의 **[!UICONTROL Settings]** 창에 표시됩니다.

1. **[!UICONTROL Vertical alignment]** 아래에서 **[!UICONTROL Up]**&#x200B;을 선택합니다.

   ![](assets/des_vertical_alignment.png)

   컨텐츠 구성 요소가 열 상단에 표시됩니다.

1. **[!UICONTROL Padding]** 아래에서 열 안의 위쪽 패딩을 정의합니다. 잠금 아이콘을 클릭하여 아래쪽 패딩과의 동기화를 중단합니다.

   해당 열의 왼쪽 및 오른쪽 패딩을 정의합니다.

   ![](assets/des_adjusting_padding.png)

1. 다른 열의 정렬 및 패딩을 조정하려면 비슷하게 진행하십시오.

   ![](assets/des_adjusting_columns.png)

1. 변경 내용을 저장합니다.

## 링크 스타일 지정 {#about-styling-links}

링크에 밑줄을 그고 이메일 디자이너에서 링크의 색상과 대상을 선택할 수 있습니다.

1. 링크가 삽입되는 구성 요소에서 링크의 레이블 텍스트를 선택합니다.

1. 구성 요소 설정에서 **[!UICONTROL Underline link]**&#x200B;을 선택하여 링크의 레이블 텍스트에 밑줄을 표시합니다.

   ![](assets/stylelinks-selecttext.png)

1. 링크를 열 검색 컨텍스트를 선택하려면 **[!UICONTROL Target]**&#x200B;을 선택합니다.

   ![](assets/stylelinks-target.png)

1. 링크의 색상을 변경하려면 **[!UICONTROL Link color]**&#x200B;을 클릭합니다.

   ![](assets/stylelinks-colorpicker.png)

1. 필요한 색상을 선택하십시오.

   ![](assets/stylelinks-colorchanged.png)

1. 변경 내용을 저장합니다.

## 인라인 스타일 특성 추가 {#adding-inline-styling-attributes}

이메일 디자이너 인터페이스에서 요소를 선택하고 사이드 패널에 요소를 표시하는 경우 해당 특정 요소에 대한 인라인 속성과 해당 값을 사용자 지정할 수 있습니다.

1. 컨텐츠에서 요소를 선택합니다.
1. 사이드 패널에서 **[!UICONTROL Styles Inline]** 설정을 찾습니다.

   ![](assets/email_designer_inlineattributes.png)

1. 기존 속성의 값을 수정하거나 **+** 단추를 사용하여 새 속성을 추가합니다. CSS와 호환되는 모든 속성과 값을 추가할 수 있습니다.

그러면 스타일이 선택한 요소에 적용됩니다. 자식 요소에 특정 스타일 속성이 정의되지 않은 경우 상위 요소의 스타일이 상속됩니다.
