---
title: '재사용 가능한 컨텐츠 만들기 및 사용 '
seo-title: 재사용 가능한 컨텐츠 만들기 및 사용
description: 재사용 가능한 컨텐츠 만들기 및 사용
seo-description: 이메일 디자이너를 사용하여 재사용 가능한 이메일 컨텐츠 작성을 시작합니다.
page-status-flag: 활성화 안 함
uuid: 571ffc01-6e41-4501-9094-2f812b041a10
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 디자인
content-type: reference
topic-tags: editing-email-content
discoiquuid: 39b86fda-7766-4e5f-ab48-bcc536ab66b3
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: a7de545e9eec675444245576cddc6eaf8dce05f4

---

# 재사용 가능한 컨텐츠 만들기 및 사용 {#using-reusable-content}

이메일 컨텐츠 에디션을 마스터하는 방법을 살펴보십시오. 이메일 디자이너를 사용하면 사전 정의된 컨텐츠로 템플릿과 조각을 만들어 다음 게재에 재사용할 수 있습니다.

## 템플릿을 사용하여 디자인 {#designing-templates}

>[!NOTE]
>
> Adobe Campaign Standard에서는 리소스 &gt; 템플릿 메뉴에서 액세스할 수 있는 다양한 유형의 템플릿을 **만들** 수 **** 있습니다. 이메일 디자이너에서 사용되는 템플릿은 컨텐츠 템플릿입니다. 자세한 내용은 템플릿 [정보를](../../start/using/about-templates.md)참조하십시오.

### 컨텐츠 템플릿 {#content-templates}

이메일 디자이너 홈 페이지의 **[!UICONTROL Templates]** 탭에서 제공되는 HTML 콘텐츠를 관리할 [수](../../designing/using/overview.md) 있습니다. 다양한 템플릿은 여러 유형의 요소를 다양하게 조합하여 제공합니다. 예를 들어 '페더' 템플릿에는 여백이 있지만 '아스트로' 템플릿에는 여백이 없습니다. 자세한 내용은 컨텐츠 [템플릿을](../../designing/using/using-reusable-content.md#content-templates)참조하십시오.

![](assets/template_content.png)

기본 템플릿에서 이메일을 작성하는 방법에 대한 자세한 내용은 이메일 [디자이너를 참조하십시오](../../designing/using/quick-start.md#building-content-from-an-out-of-the-box-template).

### 컨텐츠 템플릿 만들기 {#creating-a-content-template}

필요에 따라 여러 번 사용할 수 있도록 고유한 컨텐츠 템플릿을 만들 수 있습니다.

다음 예는 이메일 컨텐츠 템플릿을 만드는 방법을 보여줍니다.

1. &gt; **[!UICONTROL Resources]** 로 **[!UICONTROL Content templates & fragments]** 이동한 다음 을 클릭합니다 **[!UICONTROL Create]**.
1. 이메일 디자이너의 **[!UICONTROL Properties]** 탭에 액세스하려면 이메일 레이블을 클릭합니다.
1. 인식할 수 있는 레이블을 지정하고 이 템플릿을 이메일에 사용할 수 있도록 다음 매개 변수를 선택합니다.

   * **[!UICONTROL Shared]** **[!UICONTROL Delivery]** **[!UICONTROL Content type]** 드롭다운 목록에서 또는 을 선택합니다.
   * 드롭다운 **[!UICONTROL Template]** 목록에서 **[!UICONTROL HTML type]** 선택합니다.
   ![](assets/email_designer_create-template.png)

1. 필요한 경우 템플릿의 축소판으로 사용할 이미지를 설정할 수 있습니다. 템플릿 속성의 **[!UICONTROL Thumbnail]** 탭에서 선택합니다.

   ![](assets/email_designer_create-template_thumbnail.png)

   이 축소판은 이메일 디자이너 **[!UICONTROL Templates]** 홈 페이지의 [탭에](../../designing/using/overview.md#about-the-email-designer) 표시됩니다.

1. 탭을 **[!UICONTROL Properties]** 닫아서 주 작업 영역으로 돌아갑니다.
1. 필요에 따라 사용자 정의할 수 있는 구조 구성 요소 및 컨텐츠 구성 요소를 추가합니다.
   >[!NOTE]
   >
   > 콘텐츠 템플릿 내에는 개인화 필드 또는 조건부 콘텐츠를 삽입할 수 없습니다.
1. 편집한 후에는 템플릿을 저장합니다.

이제 이메일 디자이너와 함께 작성된 모든 이메일에서 이 템플릿을 사용할 수 있습니다. 이메일 디자이너 홈 페이지의 **[!UICONTROL Templates]** 탭에서 [선택합니다](../../designing/using/overview.md#about-the-email-designer) .

![](assets/content_template_new.png)

### 컨텐츠를 템플릿으로 저장 {#saving-content-as-template}

이메일 디자이너에서 이메일을 편집할 때 해당 이메일의 컨텐츠를 템플릿으로 직접 저장할 수 있습니다.

<!--[!CAUTION]
>
>You cannot save as template a structure containing personalization fields or dynamic content.-->

1. 이메일 **[!UICONTROL Save as template]** 디자이너 기본 도구 모음에서 선택합니다.

   ![](assets/email_designer_save-as-template.png)

1. 필요한 경우 레이블과 설명을 추가한 다음 을 클릭합니다 **[!UICONTROL Save]**.

   ![](assets/email_designer_save-as-template_creation.png)

1. 방금 만든 템플릿을 찾으려면 **[!UICONTROL Resources]** &gt; **[!UICONTROL Content templates & fragments]**&#x200B;로 이동합니다.

1. 새 템플릿을 사용하려면 이메일 디자이너 홈 페이지의 **[!UICONTROL Templates]** 탭에서 [템플릿을](../../designing/using/overview.md#about-the-email-designer) 선택합니다.

   ![](assets/content_template_new.png)

### 조각 및 구성 요소로 템플릿 만들기 {#template-fragments-components}

이제 이메일 디자이너에서 이메일 템플릿을 만들 수 있습니다. 컨텐츠 구성 요소를 사용하여 이메일의 다양한 섹션을 반영하고 설정을 조정하여 원본 뉴스레터에 최대한 가깝게 만듭니다. 마지막으로 방금 만든 조각을 삽입합니다.

1. 이메일 디자이너를 사용하여 템플릿을 만듭니다. 자세한 내용은 컨텐츠 [템플릿을](../../designing/using/using-reusable-content.md#content-templates)참조하십시오.
1. 템플릿의 머리글, 바닥글 및 본문에 해당하는 몇 가지 구조 구성 요소를 템플릿에 삽입합니다. 구조 구성 요소 추가에 대한 자세한 내용은 이메일 [디자이너를 사용하여 이메일 구조 편집을 참조하십시오](../../designing/using/designing-from-scratch.md#defining-the-email-structure).
1. 필요한 만큼 컨텐츠 구성 요소를 삽입하여 뉴스레터의 본문을 만듭니다. 매월 업데이트되는 이메일의 편집 가능한 컨텐츠가 됩니다.

   ![](assets/des_loading_compatible_fragment_5.png)

   HTML 코드에 익숙한 경우 원본 이메일의 보다 복잡한 요소를 복사하여 붙여넣을 수 있는 구성 요소를 활용하는 것이 좋습니다. **[!UICONTROL Html]** 기타 구성 요소( **[!UICONTROL Button]**&#x200B;예: **[!UICONTROL Image]** 또는 **[!UICONTROL Text]** 나머지 컨텐츠)를 사용합니다. 자세한 내용은 컨텐츠 구성 [요소](../../designing/using/designing-from-scratch.md#about-content-components)정보를 참조하십시오.

   >[!NOTE]
   >
   >구성 **[!UICONTROL Html]** 요소를 사용하면 제한된 옵션으로 편집할 수 있는 구성 요소가 생성됩니다. 이 구성 요소를 선택하기 전에 HTML 코드를 처리하는 방법을 알고 있어야 합니다.

1. 컨텐츠 구성 요소를 최대한 원본 이메일에 맞게 조정할 수 있습니다.

   ![](assets/des_loading_compatible_fragment_6.png)

   스타일 설정 및 인라인 속성 관리에 대한 자세한 내용은 이메일 [스타일](../../designing/using/styles.md)편집을 참조하십시오.

1. 이전에 만든 두 조각(머리글과 바닥글)을 원하는 구조 구성 요소에 삽입합니다.

   ![](assets/des_loading_compatible_fragment_10.png)

1. 템플릿을 저장합니다.

이제 이메일 디자이너 내에서 이 템플릿을 완전히 관리하여 매달 수신자에게 보낼 뉴스레터를 만들고 업데이트할 수 있습니다.

사용하려면 이메일을 만들고 방금 만든 컨텐츠 템플릿을 선택합니다.

**관련 항목**:

* [이메일 만들기](../../channels/using/creating-an-email.md)
* [이메일 디자이너를 위한 소개 비디오](https://video.tv.adobe.com/v/22771/?autoplay=true&hidetitle=true&captions=kor)
* [처음부터 이메일 컨텐츠 디자인](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch)

## 조각 정보 {#about-fragments}

조각은 하나 이상의 이메일에서 참조할 수 있는 재사용 가능한 구성 요소입니다.
이러한 템플릿은 리소스 &gt; 컨텐츠 **조각** 및 **템플릿**&#x200B;아래의 인터페이스에서 찾을 수 있습니다.

이메일 디자이너에서 조각을 가장 잘 사용하려면

* 고유한 조각을 만듭니다. 컨텐츠 [조각](../../designing/using/using-reusable-content.md#creating-a-content-fragment) 만들기 및 [컨텐츠를 조각으로](../../designing/using/using-reusable-content.md#saving-content-as-a-fragment)저장을 참조하십시오.
* 이메일에 필요한 만큼 사용할 수 있습니다. 이메일에 [요소](../../designing/using/using-reusable-content.md#inserting-elements-into-an-email)삽입을 참조하십시오.
* 조각을 편집할 때 변경 사항이 동기화됩니다.이러한 구성 요소는 해당 조각을 포함하는 모든 이메일에 자동으로 전파됩니다(준비 또는 전송되지 않은 경우).

이메일에 추가하면 조각은 기본적으로 잠깁니다. 특정 이메일에 대한 조각을 수정하려면 사용된 이메일에서 조각을 잠금 해제하여 원래 조각과의 동기화를 해제할 수 있습니다. 변경 내용이 더 이상 동기화되지 않습니다.

이메일 내의 단편을 잠금 해제하려면 해당 단편을 선택하고 컨텍스트 도구 모음에서 잠금 아이콘을 클릭합니다.

![](assets/des_unlocking_fragment.png)

이 조각은 더 이상 원본 조각에 연결되지 않은 독립 실행형 구성 요소가 됩니다. 그런 다음 다른 컨텐츠 구성 요소로 편집할 수 있습니다. 컨텐츠 [구성 요소](../../designing/using/designing-from-scratch.md#about-content-components)정보를 참조하십시오.

### 이메일에 조각 삽입 {#inserting-elements-into-an-email}

이메일의 컨텐츠를 정의하려면 이전에 배치한 구조 구성 요소에 컨텐츠 요소를 추가할 수 있습니다. 이메일 [구조](../../designing/using/designing-from-scratch.md#defining-the-email-structure)편집을 참조하십시오.

1. 왼쪽에서 **+** 아이콘을 선택하여 컨텐츠 요소에 액세스합니다. 조각 [또는 컨텐츠](../../designing/using/using-reusable-content.md#about-fragments) 구성 [요소를](../../designing/using/designing-from-scratch.md#about-content-components)선택합니다.
1. 추가하려는 조각 레이블의 레이블이나 부분을 이미 알고 있는 경우 해당 레이블을 검색할 수 있습니다.

   ![](assets/email_designer_fragmentsearch.png)

1. 팔레트에서 이메일의 구조 구성 요소로 조각 또는 컨텐츠 구성 요소를 드래그하여 놓습니다.

   ![](assets/email_designer_addfragment.png)

   요소가 이메일에 추가되면 구조 구성 요소 내부 또는 이메일의 다른 구조 구성 요소로 이동할 수 있습니다.

   ![](assets/email_designer_movefragment.png)

1. 이 이메일의 정확한 요구 사항에 맞게 요소를 편집합니다. 텍스트, 링크, 이미지 등을 추가할 수 있습니다.

   >[!NOTE]
   >
   >조각은 이메일에 추가될 때 기본적으로 잠깁니다. 특정 이메일에 대한 조각을 수정하려는 경우 원본 조각과의 동기화를 중단하거나 조각에서 직접 변경을 수행할 수 있습니다. 조각 [정보를](../../designing/using/using-reusable-content.md#about-fragments)참조하십시오.

1. 이메일에 추가해야 하는 모든 요소에 대해 이 절차를 반복합니다.
1. 이메일 저장

이메일 구조가 채워지면 각 컨텐츠 요소의 스타일을 편집할 수 있습니다. 요소 [편집을 참조하십시오](../../designing/using/styles.md#editing-an-element).

>[!NOTE]
>
>조각을 수정하면 변경 사항이 사용된 이메일에 자동으로 전파됩니다. 자세한 내용은 조각 [정보를](../../designing/using/using-reusable-content.md#about-fragments)참조하십시오.

### 컨텐츠 조각 만들기 {#creating-a-content-fragment}

필요에 따라 하나 이상의 이메일에서 사용할 컨텐츠 조각을 직접 만들 수 있습니다.

1. &gt; **[!UICONTROL Resources]** 로 **[!UICONTROL Content templates & fragments]** 이동한 다음 을 클릭합니다 **[!UICONTROL Create]**.
1. 이메일 디자이너의 **[!UICONTROL Properties]** 탭에 액세스하려면 이메일 레이블을 클릭합니다.
1. 인식 가능한 레이블을 지정하고 이메일 컨텐츠를 편집할 때 조각을 찾으려면 다음 매개 변수를 선택합니다.

   * 조각은 이메일만 호환되므로 **[!UICONTROL Delivery]** 드롭다운 **[!UICONTROL Content type]** 목록에서 선택합니다.
   * 이 컨텐츠를 조각으로 사용할 수 **[!UICONTROL Fragment]** 있도록 **[!UICONTROL HTML type]** 드롭다운 목록에서 선택합니다.
   ![](assets/email_designer_createfragment.png)

1. 필요한 경우 조각의 축소판으로 사용할 이미지를 설정할 수 있습니다. 템플릿 속성의 **[!UICONTROL Thumbnail]** 탭에서 선택합니다.

   ![](assets/email_designer_createfragment_thumbnail.png)

   이 축소판은 이메일을 편집할 때 조각 레이블 옆에 표시됩니다.

1. 탭을 **[!UICONTROL Properties]** 닫아서 주 작업 영역으로 돌아갑니다.
1. 필요에 따라 사용자 정의할 수 있는 구조 구성 요소 및 컨텐츠 구성 요소를 추가합니다.

   >[!NOTE]
   >
   >조각에는 개인화 필드, 동적 컨텐츠 또는 다른 조각을 포함할 수 없습니다.
   >조각에서 [모바일 보기를](../../designing/using/styles.md#switching-to-mobile-view) 사용할 수 없습니다.

1. 편집한 후에는 조각을 저장합니다.

이제 이 조각은 이메일 디자이너와 함께 빌드된 모든 이메일에서 사용할 수 있습니다. 팔레트의 섹션 아래에 나타납니다 **[!UICONTROL Fragments]** .

>[!NOTE]
>
>개인화 필드는 이메일에서 사용하고 잠금 해제하지 않는 한 조각 내에 삽입할 수 없습니다. 조각 [정보를](../../designing/using/using-reusable-content.md#about-fragments)참조하십시오.

### 컨텐츠를 조각으로 저장 {#saving-content-as-a-fragment}

이메일 디자이너에서 이메일을 편집할 때 해당 이메일의 일부를 조각으로 직접 저장할 수 있습니다.

* 개인화 필드, 동적 컨텐츠 또는 다른 조각을 포함하는 구조는 조각으로 저장할 수 없습니다.
* 서로 인접한 구조물만 선택할 수 있습니다.
<!-- - You cannot select an empty structure.-->

1. 이메일 디자이너에서 이메일을 편집할 때 기본 도구 모음에서 **[!UICONTROL Save as fragment]** 을 선택합니다.

   ![](assets/email_designer_save-as-fragment.png)

1. 작업 공간에서 조각을 구성할 구조를 선택합니다.

   ![](assets/email_designer_save-as-fragment_select.png)

   >[!NOTE]
   >
   >개인화 필드, 동적 컨텐츠 또는 다른 조각을 포함하지 않는 구조를 선택해야 합니다.
   <!--You cannot select an empty structure.-->

1. Click **[!UICONTROL Create]**.

1. 필요한 경우 레이블과 설명을 추가한 다음 을 클릭합니다 **[!UICONTROL Save]**.

   ![](assets/email_designer_save-as-fragment_popup.png)

1. 방금 생성한 조각을 찾으려면 **[!UICONTROL Resources]** &gt; **[!UICONTROL Content templates & fragments]**&#x200B;로 이동합니다.

   ![](assets/email_designer_save-as-fragment_list.png)

1. 새 조각을 사용하려면 이메일 컨텐츠를 열고 조각 목록에서 선택합니다.

![](assets/email_designer_save-as-fragment_in-new-email.png)

>[!NOTE]
>조각에서 [모바일 보기를](../../designing/using/styles.md#switching-to-mobile-view) 사용할 수 없습니다. 이메일 모바일 보기를 편집하려면 컨텐츠를 조각으로 저장하기 전에 먼저 편집합니다.

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

## 조각을 사용하여 재사용 가능한 머리글 및 바닥글 만들기 {#header-footer-fragments}

이메일 디자이너를 사용하여 재사용 가능한 각 섹션의 조각을 만듭니다. 이 예에서는 두 개의 조각을 만듭니다.하나는 머리글에 대한 것이고 하나는 바닥글에 대한 것입니다. 그런 다음 기존 컨텐츠의 관련 부품을 이러한 조각으로 복사할 수 있습니다.

이렇게 하려면 아래 절차를 따르십시오.

1. Adobe Campaign에서 **[!UICONTROL Resources]** &gt;로 이동하여 **[!UICONTROL Content templates & fragments]** 헤더의 조각을 만듭니다. 자세한 내용은 컨텐츠 [조각](../../designing/using/using-reusable-content.md#creating-a-content-fragment)만들기를 참조하십시오.
1. 조각에 필요한 만큼 구조 구성 요소를 추가합니다.

![](assets/des_loading_compatible_fragment_1.png)

1. 구조에 이미지 및 텍스트 구성 요소를 삽입합니다.

![](assets/des_loading_compatible_fragment_2.png)

1. 해당 이미지를 업로드하고 텍스트를 입력하고 설정을 조정합니다.

![](assets/des_loading_compatible_fragment_3.png)

1. 조각을 저장합니다.
1. 바닥글을 만들어 저장하려면 비슷하게 진행하십시오.

![](assets/des_loading_compatible_fragment_4.png)

이제 템플릿에서 조각을 사용할 준비가 되었습니다.
