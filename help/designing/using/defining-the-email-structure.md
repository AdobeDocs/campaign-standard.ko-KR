---
title: 이메일 구조 정의
seo-title: 이메일 구조 정의
description: 이메일 구조 정의
seo-description: Campaign에서 이메일 디자이너를 사용하여 이메일을 작성하고 컨텐츠 구성 요소로 채우는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: 6 EC 63 F 65-1425-4 C 28-84 E 8-B 09574458 DB 3
contentOwner: Sauviat
products: sg_ campaign/standard
audience: designing
content-type: 참조
topic-tags: editing-email-content
discoiquuid: 207 fdf 6 d -165 a -41 af-ad 53-ba 97 d 3403 b 62
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 7de6436bbd4f1cc5032e13414f7337f637bf608a

---


# Defining the email structure{#defining-the-email-structure}

## Editing the email structure {#editing-the-email-structure}

이메일 디자이너를 사용하면 이메일 구조를 손쉽게 정의할 수 있습니다. 드래그 앤 드롭 방식의 간단한 동작을 통해 구조적 요소를 추가하거나 이동할 수 있으므로 이메일 모양을 신속하게 디자인할 수 있습니다.

이메일 구조를 편집하려면:

1. 기존 콘텐트를 열거나 새 이메일 콘텐츠를 만듭니다.
1. Access the **[!UICONTROL Structure components]** by selecting the **+** icon on the left.

   ![](assets/email_designer_structure.png)

1. 이메일을 만드는 데 필요한 구조 구성 요소를 드래그하여 놓습니다.

   ![](assets/email_designer_structure_components.png)

   파란색 선은 구성 요소를 놓기 전에 정확한 위치를 구체화합니다. 다른 구성 요소 사이 또는 아래에 놓을 수 있지만 내부에 놓을 수는 없습니다.

   >[!NOTE]
   >
   >일단 이메일에 배치하면, 이미 컨텐츠 구성 요소가 있는 경우가 아니면 구성 요소를 이동하거나 제거할 수 없습니다.

1. 하나 이상의 열로 구성된 여러 구조 구성 요소를 사용할 수 있습니다.

   **[!UICONTROL n:n column]** 구성 요소를 선택하여 원하는 열 수 (3 ~ 10 개 사이) 를 정의합니다. 각 열 아래쪽의 화살표를 이동하여 각 열의 너비를 정의할 수도 있습니다.

   ![](assets/email_designer_n-n-column.png)

   >[!NOTE]
   >
   >각 열 크기는 구조 구성 요소의 전체 너비의 10%를 초과할 수 없습니다. 비어 있지 않은 열은 제거할 수 없습니다.

구조가 정의된 후에는 이메일 및 구성 요소를 이메일에 추가할 수 있습니다.

## Adding fragments and content components {#adding-fragments-and-content-components}

이메일 디자이너는 이메일에 구조 구성 요소를 추가한 후 콘텐츠를 정의할 수 있습니다. 이렇게 하려면 각 구조 구성 요소 내에 요소를 추가해야 합니다.

There are two categories of content elements that you can use: **fragments** and **content components**.

### About fragments {#about-fragments}

조각은 하나 이상의 이메일에서 참조할 수 있는 재사용 가능한 구성 요소입니다.

이메일 디자이너에서 조각을 가장 잘 사용하려면 다음을 수행하십시오.

* 나만의 단편 만들기 See [Creating a content fragment](../../designing/using/defining-the-email-structure.md#creating-a-content-fragment) and [Saving content as a fragment](../../designing/using/defining-the-email-structure.md#saving-content-as-a-fragment).
* 이메일에서 필요에 따라 여러 번 사용합니다. See [Inserting elements into an email](../../designing/using/defining-the-email-structure.md#inserting-elements-into-an-email).
* 조각을 편집하면 변경 사항이 동기화됩니다. 이러한 조각은 해당 조각이 들어 있는 모든 이메일 (아직 준비 또는 전송되지 않은 경우) 에 자동으로 전파됩니다.

이메일에 추가하면 조각이 기본적으로 잠깁니다. 특정 이메일에 대한 조각을 수정하려는 경우, 사용되는 이메일에서 원래 조각으로 동기화를 해제하여 동기화를 끊을 수 있습니다. 변경 사항이 더 이상 동기화되지 않습니다.

이메일 내의 조각을 잠금 해제하려면 해당 항목을 선택하고 컨텍스트 도구 모음에서 잠금 아이콘을 클릭합니다.

![](assets/des_unlocking_fragment.png)

이 조각은 더 이상 원본 조각에 연결되지 않은 독립 실행형 구성 요소가 됩니다. 그런 다음 다른 컨텐츠 구성 요소로 편집할 수 있습니다. See [About content components](../../designing/using/defining-the-email-structure.md#about-content-components).

### About content components {#about-content-components}

컨텐츠 구성 요소는 이메일에 배치한 후 편집할 수 있는 빈 구성 요소입니다.

구조 구성 요소에서 원하는 만큼 컨텐츠 구성 요소를 추가할 수 있습니다. 또한 구조 구성 요소나 다른 구조 구성 요소로 이동할 수도 있습니다.

다음은 이메일 디자이너의 사용 가능한 구성 요소 목록입니다.

* **[!UICONTROL Button]**

   If you need to use multiple buttons, rather than editing each button from scratch, you can duplicate the **[!UICONTROL Button]** component using the contextual toolbar.

   또한 단추를 다시 사용할 수 있는 단편으로 저장할 수도 있습니다. For more on this, see [Creating a content fragment](../../designing/using/defining-the-email-structure.md#creating-a-content-fragment) and [Saving content as a fragment](../../designing/using/defining-the-email-structure.md#saving-content-as-a-fragment).

* **[!UICONTROL Carousel]**

   For more on this, see [Using the carousel component](../../designing/using/defining-the-email-structure.md#using-the-carousel-component).

* **[!UICONTROL Divider]**
* **[!UICONTROL Html]**

   이 구성 요소를 사용하여 기존 HTML의 다른 부분을 복사합니다. 이렇게 하면 무료 모듈 HTML 구성 요소를 만들 수 있습니다.

   >[!NOTE]
   >
   >무료 HTML 구성 요소는 제한된 옵션을 사용하여 편집할 수 있습니다. If all styles are not inlined, make sure to add the proper CSS in the **head** section of the HTML code, otherwise the email will not be responsive. **[!UICONTROL Preview]** 단추를 사용하여 컨텐츠의 응답성을 테스트합니다 (메시지 [](../../sending/using/previewing-messages.md)미리 보기 참조).

* **[!UICONTROL Image]**
* **[!UICONTROL Social]**
* **[!UICONTROL Text]**

#### Using the carousel component {#using-the-carousel-component}

1. **[!UICONTROL Carousel]** 구성 요소를 구조 구성 요소 내에서 드래그하여 놓습니다.
1. 컴퓨터에서 이미지를 찾아 선택합니다.

   ![](assets/des_carousel_browse.png)

1. **[!UICONTROL Settings]** 창에서 회전판에서 원하는 축소판 수를 설정합니다.
1. 컴퓨터에서 폴백 이미지를 선택합니다.

   ![](assets/des_carousel_fallback.png)

   회전판 구성 요소는 모든 이메일 프로그램과 호환되지 않습니다. Carousel 이 이메일에서 지원되지 않을 때 대신 이미지를 표시하려면 폴백을 업로드합니다.

   >[!NOTE]
   >
   >회전판 구성 요소는 다음 이메일 플랫폼과 호환됩니다. Apple Mail 7, Apple Mail 8, Mac 용 Outlook 2011, Mac 용 Outlook 2016, Mozilla Thunderbird, iPad 및 iPad Mini iOS, iPhone iOS, Android, AOL (Chrome, Firefox 및 Safari).

1. Select **[!UICONTROL Fallback view]** to display the fallback image in the Email Designer.

### Inserting elements into an email {#inserting-elements-into-an-email}

이메일의 컨텐츠를 정의하려면 미리 배치한 구조 구성 요소에 컨텐츠 요소를 추가할 수 있습니다. See [Editing the email structure](../../designing/using/defining-the-email-structure.md#editing-the-email-structure).

1. Access the content elements by selecting the **+** icon on the left. [조각](../../designing/using/defining-the-email-structure.md#about-fragments) 또는 [컨텐츠 구성 요소를 선택합니다](../../designing/using/defining-the-email-structure.md#about-content-components).
1. 추가하려는 조각의 레이블이나 레이블을 이미 알고 있다면 해당 레이블을 검색할 수 있습니다.

   ![](assets/email_designer_fragmentsearch.png)

1. 팔레트 또는 컨텐츠 구성 요소를 팔레트의 구조 구성 요소로 드래그하여 놓습니다.

   ![](assets/email_designer_addfragment.png)

   요소가 이메일에 추가되면, 구조 구성 요소 내에서 또는 이메일의 다른 구조 구성 요소로 이동할 수 있습니다.

   ![](assets/email_designer_movefragment.png)

1. 이 이메일의 정확한 요구 사항에 맞게 요소를 편집합니다. 텍스트, 링크, 이미지 등을 추가할 수 있습니다.

   >[!NOTE]
   >
   >조각은 이메일에 추가될 때 기본적으로 잠깁니다. 특정 이메일에 대한 조각을 수정하려는 경우 원래 조각과의 동기화를 끊거나 조각에서 직접 변경할 수 있습니다. See [About fragments](../../designing/using/defining-the-email-structure.md#about-fragments).

1. 이메일에 추가해야 하는 모든 요소에 대해 이 절차를 반복합니다.
1. 이메일을 저장합니다.

이제 이메일 구조가 채워지면 각 컨텐츠 요소의 스타일을 편집할 수 있습니다. See [Editing an element](../../designing/using/editing-email-styles.md#editing-an-element).

>[!NOTE]
>
>조각이 수정되면 변경 사항이 사용되는 이메일에서 자동으로 전파됩니다. For more on this, see [About fragments](../../designing/using/defining-the-email-structure.md#about-fragments).

### Creating a content fragment {#creating-a-content-fragment}

하나 이상의 이메일에서 필요에 따라 고유한 컨텐츠 조각을 만들어 사용할 수 있습니다.

1. Go to **[!UICONTROL Resources]** &gt; **[!UICONTROL Content templates & fragments]** and click **[!UICONTROL Create]**.
1. Click the email label to access the **[!UICONTROL Properties]** tab of the Email Designer.
1. 인식 가능한 레이블을 지정하고 다음 매개 변수를 선택하여 새 이메일의 조각을 찾으십시오.

   * Because fragments are only compatible with emails, select **[!UICONTROL Delivery]** from the **[!UICONTROL Content type]** drop-down list.
   * Select **[!UICONTROL Fragment]** from the **[!UICONTROL HTML type]** drop-down list to be able to use this content as a fragment in your emails.
   ![](assets/email_designer_createfragment.png)

1. 필요한 경우 조각의 썸네일로 사용될 이미지를 설정할 수 있습니다. Select it from the **[!UICONTROL Thumbnail]** tab of the template properties.

   ![](assets/email_designer_createfragment_thumbnail.png)

   이 축소판은 이메일을 편집할 때 조각의 레이블 옆에 표시됩니다.

1. 변경 내용을 저장하여 주 작업 영역으로 돌아갑니다.
1. 필요에 따라 사용자 지정할 수 있는 구조 구성 요소와 컨텐츠 구성 요소를 추가합니다.
1. 편집된 조각을 저장합니다.

이제 조각을 이메일 디자이너로 작성한 이메일에 사용할 수 있습니다. It appears under the **[!UICONTROL Fragments]** section of the Palette.

>[!NOTE]
>
>이메일에서 사용되는 경우가 아니라면 조각 안에 개인화 필드를 삽입할 수 없습니다. 이렇게 하려면 이 조각의 잠금을 해제해야 합니다. See [About fragments](../../designing/using/defining-the-email-structure.md#about-fragments).

### Saving content as a fragment {#saving-content-as-a-fragment}

이메일 디자이너로 이메일을 편집할 때 해당 이메일의 일부를 조각으로 직접 저장할 수 있습니다.

>[!CAUTION]
>
>개인화 필드, 동적 컨텐츠 또는 다른 조각이 들어 있는 구조로 저장할 수 없습니다.

1. When editing an email in the Email Designer, select **[!UICONTROL Save as fragment]** from the main toolbar.

   ![](assets/email_designer_save-as-fragment.png)

1. 작업 영역에서 조각을 구성할 구조를 선택합니다.

   ![](assets/email_designer_save-as-fragment_select.png)

   >[!NOTE]
   >
   >서로 인접한 구조만 선택할 수 있습니다.

1. **[!UICONTROL Create]**&#x200B;을 클릭합니다.

1. Add a label and a description if needed, then click **[!UICONTROL Save]**.

   ![](assets/email_designer_save-as-fragment_popup.png)

1. To find the fragment that you just created, go to **[!UICONTROL Resources]** &gt; **[!UICONTROL Content templates & fragments]**.

   ![](assets/email_designer_save-as-fragment_list.png)

1. 새 조각을 사용하려면 이메일 콘텐트를 열고 조각 목록에서 선택합니다.

![](assets/email_designer_save-as-fragment_in-new-email.png)

<!--You need to copy-paste the HTML corresponding to the section that you want to save into a new fragment.

>[!NOTE]
>
>To do this, you need to be familiar with HTML code.

To save as a fragment some email content that you created, follow the steps below.

1. When editing an email in the Email Designer, select **[!UICONTROL Edit]** > **[!UICONTROL HTML]** to open the HTML version of that email.
1. Select and copy the HTML corresponding to the part that you want to save.
1. Go to **[!UICONTROL Resources]** > **[!UICONTROL Content templates & fragments]** and click **[!UICONTROL Create]**.
1. Click the email label to access the **[!UICONTROL Properties]** tab of the Email Designer and select **[!UICONTROL Fragment]** from the **[!UICONTROL HTML type]** drop-down list.
1. Select **[!UICONTROL Edit]** > **[!UICONTROL HTML]** to open the HTML version of the fragment.
1. Paste the HTML that you copied where appropriate.
1. Switch back to the **[!UICONTROL Edit]** view to check the result and save the new fragment.-->

