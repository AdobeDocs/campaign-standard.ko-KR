---
title: 이메일 스타일 관리
description: 이메일 Designer에서 이메일 스타일을 관리하는 방법을 알아봅니다.
audience: designing
content-type: reference
topic-tags: editing-email-content
feature: Email Design
role: User
level: Intermediate
exl-id: 8daeb12d-4170-464f-ba33-afb681f72a91
source-git-commit: 5435e1dbfbe08399c488322320ac5bb8e681a79d
workflow-type: tm+mt
source-wordcount: '1038'
ht-degree: 25%

---

# 이메일 스타일 관리 {#managing-styles}


이메일 Designer에서 요소를 선택할 때 선택한 콘텐츠 유형과 관련된 몇 가지 옵션이 **[!UICONTROL Settings]** 창에 표시됩니다. 이러한 옵션을 사용하여 전자 메일 스타일을 쉽게 변경할 수 있습니다.

## 요소 선택 {#selecting-an-element}

이메일 Designer 인터페이스에서 요소를 선택하기 위해 다음 중 하나를 수행할 수 있습니다.

* 이메일에서 바로 를 클릭합니다.
* 또는 왼쪽 **팔레트**&#x200B;에 있는 옵션에서 사용할 수 있는 구조 트리를 찾아보세요.

![](assets/des_tree_structure.png)

구조 트리를 탐색하면 보다 정확하게 선택할 수 있습니다. 다음 중 하나를 선택할 수 있습니다.

* 전체 구조 구성 요소
* 구조 구성 요소를 구성하는 열 중 하나,
* 또는 열 내부에 있는 구성 요소만 해당됩니다.

![](assets/des_tree_structure_selection.png)

열을 선택하기 위해 다음을 수행할 수도 있습니다.

1. 구조 구성 요소를 선택합니다(전자 메일에서 직접 또는 왼쪽 **팔레트**&#x200B;에서 사용할 수 있는 구조 트리 사용).
1. **상황별 도구 모음**&#x200B;에서 **[!UICONTROL Select a column]**&#x200B;을(를) 클릭하여 원하는 열을 선택합니다.

[이 섹션](#example--adjusting-vertical-alignment-and-padding)에서 예제를 참조하십시오.

## 스타일 설정 조정 {#adjusting-style-settings}

1. 이메일에서 요소를 선택합니다. 자세한 내용은 [요소 선택](#selecting-an-element)을 참조하세요.
1. 필요에 따라 설정을 조정합니다. 선택한 각 요소는 서로 다른 설정 세트를 제공합니다.

   배경 삽입, 크기 변경, 가로 또는 세로 정렬 수정, 색상 관리, [패딩 또는 여백](#selecting-an-element) 추가 등을 수행할 수 있습니다.

   이렇게 하려면 **[!UICONTROL Settings]** 창에 표시된 옵션을 사용하거나 [인라인 스타일 특성을 추가](#adding-inline-styling-attributes)하십시오.

   ![](assets/des_settings_pane.png)

1. 콘텐츠를 저장합니다.

## 패딩 및 여백 조정 {#about-padding-and-margin}

이메일 Designer 인터페이스를 사용하면 패딩 및 여백 설정을 빠르게 조정할 수 있습니다.

**[!UICONTROL Padding]**: 이 설정을 사용하면 요소의 테두리 내부에 있는 공간을 관리할 수 있습니다.

![](assets/des_padding.png)

예제:

* 패딩을 사용하여 이미지의 왼쪽과 오른쪽에 여백을 설정합니다.
* 위쪽 및 아래쪽 패딩을 사용하여 **[!UICONTROL Text]** 또는 **[!UICONTROL Divider]** 구성 요소에 더 많은 간격을 추가합니다.
* 구조 요소 내에서 열 사이의 테두리를 설정하려면 각 열의 패딩을 정의합니다.

**[!UICONTROL Margin]**: 이 설정을 사용하면 요소의 테두리와 다음 요소 사이의 공간을 관리할 수 있습니다.

![](assets/des_margin.png)

>[!NOTE]
>
>선택 항목(구조 구성 요소, 열 또는 콘텐츠 구성 요소)에 따라 결과가 동일하지 않습니다. Adobe 열 수준에서 **[!UICONTROL Padding]** 및 **[!UICONTROL Margin]** 매개 변수를 설정하는 것이 좋습니다.

**[!UICONTROL Padding]**&#x200B;과(와) **[!UICONTROL Margin]** 모두에 대해 잠금 아이콘을 클릭하여 위쪽 및 아래쪽 또는 오른쪽 및 왼쪽 매개 변수 간의 동기화를 중단합니다. 이렇게 하면 각 매개변수를 개별적으로 조정할 수 있습니다.

![](assets/des_padding_lock_icon.png)

## 스타일 정렬 {#about-alignment}

* **텍스트 정렬**: 마우스의 커서를 일부 텍스트에 놓고 상황에 맞는 도구 모음을 사용하여 정렬합니다.

  ![](assets/des_text_alignment.png)

* **가로 맞춤**&#x200B;은(는) 텍스트, 이미지 및 단추에 적용할 수 있습니다. 현재 **[!UICONTROL Divider]** 및 **[!UICONTROL Social]** 구성 요소에는 적용되지 않습니다.

  ![](assets/des_horizontal_alignment.png)

* **수직 정렬**&#x200B;을 설정하려면 구조 구성 요소 내의 열을 선택하고 [설정] 창에서 옵션을 선택하십시오.

  ![](assets/des_set_vertical_alignment.png)

## 배경 설정하기 {#about-backgrounds}

>[!CONTEXTUALHELP]
>id="ac_edition_backgroundimage"
>title="배경 설정"
>abstract="이메일 디자이너를 통해 콘텐츠의 배경색 또는 배경 이미지를 개인화할 수 있습니다. 배경 이미지는 모든 이메일 클라이언트에서 지원되지 않습니다."

이메일 디자이너로 배경을 설정할 때 Adobe에서 권장하는 방법은 다음과 같습니다.

1. 디자인에 필요한 경우 이메일 본문에 배경색을 적용합니다.
1. 대부분의 경우 열 수준에서 배경색을 설정합니다.
1. 이미지나 텍스트 구성 요소는 관리하기 어려우므로 배경색을 사용하지 마십시오.

다음은 사용할 수 있는 배경 설정입니다.

* 전체 전자 메일에 대해 **[!UICONTROL Background color]**&#x200B;을(를) 설정합니다. 왼쪽 팔레트에서 액세스할 수 있는 탐색 트리에서 본문 설정을 선택해야 합니다.

  ![](assets/des_background_body.png)

* **[!UICONTROL Viewport background color]**&#x200B;을(를) 선택하여 모든 구조 구성 요소에 대해 동일한 배경색을 설정합니다. 이 옵션을 사용하면 배경색과 다른 설정을 선택할 수 있습니다.

  ![](assets/des_background_viewport.png)

* 각 구조 구성 요소에 대해 서로 다른 배경색을 설정합니다. 왼쪽 팔레트에서 액세스할 수 있는 탐색 트리에서 구조를 선택하여 해당 구조에만 특정 배경색을 적용합니다.

  ![](assets/des_background_structure.png)

  뷰포트 배경색은 구조 배경색을 숨길 수 있으므로 설정하지 않도록 합니다.

* 구조 구성 요소의 콘텐츠에 대해 **[!UICONTROL Background image]**&#x200B;을(를) 설정합니다.

  ![](assets/des_background_image.png)

  >[!NOTE]
  >
  >일부 이메일 프로그램은 배경 이미지를 지원하지 않습니다. 지원되지 않는 경우에는 행 배경색이 대신 사용됩니다. 이미지를 표시할 수 없는 경우 적절한 대체 배경색을 선택해야 합니다.

* 열 수준에서 배경색을 설정합니다.

  ![](assets/des_background_column.png)

  >[!NOTE]
  >
  >이는 가장 일반적인 사용 사례입니다. Adobe는 열 수준에서 배경색을 설정할 것을 권장합니다. 이렇게 하면 전체 이메일 콘텐츠를 편집할 때 더 유연하게 작업할 수 있습니다.

  배경 이미지도 열 수준에서 설정할 수 있지만 이러한 방법은 거의 사용되지 않습니다.

### 예: 세로 정렬 및 패딩 조정 {#example--adjusting-vertical-alignment-and-padding}

3개의 열로 구성된 구조 구성 요소 내에서 패딩 및 수직 정렬을 조정하려고 합니다. 이렇게 하려면 아래 단계를 수행합니다.

1. 전자 메일에서 구조 구성 요소를 직접 선택하거나 왼쪽 **팔레트**&#x200B;에서 사용할 수 있는 구조 트리를 사용하십시오.
1. **상황별 도구 모음**&#x200B;에서 **[!UICONTROL Select a column]**&#x200B;을(를) 클릭하고 편집할 도구 모음을 선택하십시오. 구조 트리에서 선택할 수도 있습니다.

   ![](assets/des_selecting_column.png)

   해당 열에 대해 편집 가능한 매개 변수가 오른쪽의 **[!UICONTROL Settings]** 창에 표시됩니다.

1. **[!UICONTROL Vertical alignment]**&#x200B;에서 **[!UICONTROL Up]**&#x200B;을(를) 선택합니다.

   ![](assets/des_vertical_alignment.png)

   콘텐츠 구성 요소가 열 맨 위에 표시됩니다.

1. **[!UICONTROL Padding]**&#x200B;에서 열 내부의 위쪽 패딩을 정의합니다. 하단 패딩과의 동기화를 중단하려면 잠금 아이콘을 클릭합니다.

   해당 열의 왼쪽 및 오른쪽 패딩을 정의합니다.

   ![](assets/des_adjusting_padding.png)

1. 다른 열의 정렬 및 패딩을 조정하려면 이와 유사하게 진행합니다.

   ![](assets/des_adjusting_columns.png)

1. 변경 내용을 저장합니다.

## 링크 스타일링 {#about-styling-links}

이메일 디자이너에서 링크에 밑줄을 긋고 해당 색상과 대상을 선택할 수 있습니다.

1. 링크가 삽입된 구성 요소에서 링크의 레이블 텍스트를 선택합니다.

1. 구성 요소 설정에서 **[!UICONTROL Underline link]**&#x200B;을(를) 확인하여 링크의 레이블 텍스트에 밑줄을 긋습니다.

   ![](assets/stylelinks-selecttext.png)

1. 링크를 열 검색 컨텍스트를 선택하려면 **[!UICONTROL Target]**&#x200B;을(를) 선택하십시오.

   ![](assets/stylelinks-target.png)

1. 링크 색상을 변경하려면 **[!UICONTROL Link color]**&#x200B;을(를) 클릭합니다.

   ![](assets/stylelinks-colorpicker.png)

1. 필요한 색을 골라라.

   ![](assets/stylelinks-colorchanged.png)

1. 변경 내용을 저장합니다.

## 인라인 스타일 속성 추가 {#adding-inline-styling-attributes}

이메일 Designer 인터페이스에서 요소를 선택하고 사이드 패널에 해당 설정을 표시하면 해당 특정 요소에 대한 인라인 속성 및 해당 값을 사용자 지정할 수 있습니다.

1. 콘텐츠에서 요소를 선택합니다.
1. 사이드 패널에서 **[!UICONTROL Styles Inline]** 설정을 찾습니다.

   ![](assets/email_designer_inlineattributes.png)

1. 기존 특성의 값을 수정하거나 **+** 단추를 사용하여 새 특성을 추가하십시오. CSS와 호환되는 모든 속성과 값을 추가할 수 있습니다.

그런 다음 선택한 요소에 스타일이 적용됩니다. 하위 요소에 정의된 특정 스타일 속성이 없으면 상위 요소의 스타일이 상속됩니다.
