---
solution: Campaign Standard
product: campaign
title: '재사용 가능한 콘텐츠 만들기 및 사용 '
description: 이메일 디자이너를 사용하여 재사용 가능한 이메일 콘텐츠 작성을 시작합니다.
audience: designing
content-type: reference
topic-tags: editing-email-content
feature: 이메일 디자인
role: User
level: Intermediate
exl-id: 64c3d3dd-0c41-4dbc-abcd-9ddea23759f4
source-git-commit: aeeb6b4984b3bdd974960e8c6403876fdfedd886
workflow-type: tm+mt
source-wordcount: '1821'
ht-degree: 1%

---

# 재사용 가능한 콘텐츠 만들기 및 사용 {#using-reusable-content}

이메일 콘텐츠 버전을 마스터하는 방법을 알아봅니다. 이메일 디자이너를 사용하면 사전 정의된 컨텐츠로 템플릿 및 조각을 만들고 다음 게재에 재사용할 수 있습니다.

## 템플릿을 사용하여 이메일 디자인 {#designing-templates}

>[!NOTE]
>
> Adobe Campaign Standard에서는 **리소스** > **템플릿** 메뉴에서 액세스할 수 있는 다양한 유형의 템플릿을 만들 수 있습니다. 이메일 디자이너에 사용되는 템플릿은 콘텐츠 템플릿입니다. 자세한 내용은 [템플릿 정보](../../start/using/marketing-activity-templates.md)를 참조하십시오.

![](assets/do-not-localize/how-to-video.png) [비디오에서 템플릿을 만드는 방법을 알아봅니다](#video)

### 콘텐츠 템플릿 기본 정보 {#content-templates}

[이메일 디자이너](../../designing/using/designing-content-in-adobe-campaign.md) 홈 페이지의 **[!UICONTROL Templates]** 탭에서 제공하는 HTML 콘텐츠를 관리할 수 있습니다.

기본 이메일 콘텐츠 템플릿에는 Behance 아티스트가 디자인한 18개의 모바일 최적화 레이아웃과 4개의 동급 최강의 반응형 템플릿이 포함되어 있습니다. 이는 고객 환영 메시지, 뉴스레터, 재참여 이메일 등과 같은 가장 최근의 용도에 해당합니다. 이메일 디자인 프로세스를 처음부터 쉽게 간소화하기 위해 브랜드의 콘텐츠를 통해 손쉽게 사용자 지정할 수 있습니다.

![](assets/template_content.png)

HTML 콘텐츠 템플릿은 [고급 메뉴](../../start/using/interface-description.md#advanced-menu)의 **[!UICONTROL Resources]** > **[!UICONTROL Content templates & fragments]** 화면에서 액세스할 수 있습니다. 여기에서 랜딩 페이지 콘텐츠 템플릿, 이메일 콘텐츠 템플릿 및 조각도 관리할 수 있습니다.

![](assets/content_templates_list.png)

기본 컨텐츠 템플릿은 읽기 전용입니다. 이러한 템플릿 중 하나를 편집하려면 먼저 원하는 템플릿을 복제해야 합니다.

새 템플릿이나 조각을 만들고 고유한 콘텐츠를 정의할 수 있습니다. 자세한 내용은 [컨텐츠 템플릿 만들기](#creating-a-content-template) 및 [컨텐츠 조각 만들기](#creating-a-content-fragment)를 참조하십시오.

이메일 디자이너를 사용하여 컨텐츠를 편집할 때 컨텐츠를 조각 또는 템플릿으로 저장하여 컨텐츠 템플릿을 만들 수도 있습니다. 자세한 내용은 [컨텐츠를 템플릿](#saving-content-as-template) 및 [컨텐츠를 조각](../../designing/using/using-reusable-content.md#saving-content-as-a-fragment)으로 저장 을 참조하십시오.

**관련 항목:**

* 콘텐츠 편집에 대한 자세한 내용은 [전자 메일 콘텐츠 디자인 정보](../../designing/using/designing-content-in-adobe-campaign.md)를 참조하십시오.

### 컨텐츠 템플릿 만들기 {#creating-a-content-template}

자신만의 콘텐츠 템플릿을 만들어 필요에 따라 여러 번 사용할 수 있습니다.

다음 예제에서는 이메일 콘텐츠 템플릿을 만드는 방법을 보여줍니다.

1. **[!UICONTROL Resources]** > **[!UICONTROL Content templates & fragments]** 로 이동하고 **[!UICONTROL Create]** 를 클릭합니다.
1. 전자 메일 레이블을 클릭하여 전자 메일 디자이너의 **[!UICONTROL Properties]** 탭에 액세스합니다.
1. 인식할 수 있는 레이블을 지정하고 다음 매개 변수를 선택하여 이 템플릿을 이메일에서 사용할 수 있습니다.

   * **[!UICONTROL Content type]** 드롭다운 목록에서 **[!UICONTROL Shared]** 또는 **[!UICONTROL Delivery]** 을 선택합니다.
   * **[!UICONTROL HTML type]** 드롭다운 목록에서 **[!UICONTROL Template]** 을 선택합니다.

   ![](assets/email_designer_create-template.png)

1. 필요한 경우 템플릿의 축소판으로 사용할 이미지를 설정할 수 있습니다. 템플릿 속성의 **[!UICONTROL Thumbnail]** 탭에서 선택합니다.

   ![](assets/email_designer_create-template_thumbnail.png)

   이 축소판은 [이메일 디자이너](../../designing/using/designing-content-in-adobe-campaign.md) 홈 페이지의 **[!UICONTROL Templates]** 탭에 표시됩니다.

1. **[!UICONTROL Properties]** 탭을 닫고 기본 작업 공간으로 돌아갑니다.
1. 필요에 따라 사용자 지정할 수 있는 구조 구성 요소 및 컨텐츠 구성 요소를 추가합니다.
   >[!NOTE]
   >
   > 콘텐츠 템플릿 내에 개인화 필드 또는 조건부 콘텐츠를 삽입할 수 없습니다.
1. 편집하고 나면 템플릿을 저장합니다.

이제 이메일 디자이너를 사용하여 만든 모든 이메일에서 이 템플릿을 사용할 수 있습니다. [이메일 디자이너](../../designing/using/designing-content-in-adobe-campaign.md) 홈 페이지의 **[!UICONTROL Templates]** 탭에서 선택합니다.

![](assets/content_template_new.png)

### 컨텐츠를 템플릿으로 저장 {#saving-content-as-template}

이메일 디자이너를 사용하여 이메일을 편집할 때 해당 전자 메일의 콘텐츠를 템플릿으로 직접 저장할 수 있습니다.

<!--[!CAUTION]
>
>You cannot save as template a structure containing personalization fields or dynamic content.-->

1. 이메일 디자이너 기본 도구 모음에서 **[!UICONTROL Save as template]** 을 선택합니다.

   ![](assets/email_designer_save-as-template.png)

1. 필요한 경우 레이블과 설명을 추가한 다음 **[!UICONTROL Save]** 을 클릭합니다.

   ![](assets/email_designer_save-as-template_creation.png)

1. 방금 만든 템플릿을 찾으려면 **[!UICONTROL Resources]** > **[!UICONTROL Content templates & fragments]**&#x200B;로 이동합니다.

1. 새 템플릿을 사용하려면 [이메일 디자이너](../../designing/using/designing-content-in-adobe-campaign.md) 홈 페이지의 **[!UICONTROL Templates]** 탭에서 선택합니다.

   ![](assets/content_template_new.png)

### 조각 및 구성 요소로 템플릿 만들기 {#template-fragments-components}

이제 이메일 디자이너를 사용하여 이메일 템플릿을 만들 수 있습니다. 콘텐츠 구성 요소를 사용하여 이메일의 다른 섹션을 반영하고 설정을 조정하여 원래 뉴스레터에 최대한 근접하게 만듭니다. 마지막으로 방금 만든 조각을 삽입합니다.

1. 이메일 디자이너를 사용하여 템플릿을 만듭니다. 자세한 내용은 [콘텐츠 템플릿](#content-templates)을 참조하십시오.
1. 템플릿의 머리글, 바닥글 및 본문에 해당하는 몇 가지 구조 구성 요소를 템플릿에 삽입합니다. 구조 구성 요소 추가에 대한 자세한 내용은 [이메일 디자이너를 사용하여 이메일 구조 편집](../../designing/using/designing-from-scratch.md#defining-the-email-structure)을 참조하십시오.
1. 뉴스레터 본문을 만드는 데 필요한 만큼 컨텐츠 구성 요소를 삽입합니다. 매월 업데이트할 이메일의 편집 가능한 콘텐츠가 됩니다.

   ![](assets/des_loading_compatible_fragment_5.png)

   HTML 코드에 익숙한 경우 Adobe은 **[!UICONTROL Html]** 구성 요소를 활용하여 원래 이메일의 보다 복잡한 요소를 복사하여 붙여넣을 수 있습니다. 나머지 컨텐츠에는 **[!UICONTROL Button]**, **[!UICONTROL Image]** 또는 **[!UICONTROL Text]** 등의 다른 구성 요소를 사용하십시오. 자세한 내용은 [컨텐츠 구성 요소 정보](../../designing/using/designing-from-scratch.md#about-content-components)를 참조하십시오.

   >[!NOTE]
   >
   >**[!UICONTROL Html]** 구성 요소를 사용하면 제한된 옵션으로 편집할 수 있는 구성 요소가 만들어집니다. 이 구성 요소를 선택하기 전에 HTML 코드를 처리하는 방법을 알고 있어야 합니다.

1. 콘텐츠 구성 요소를 조정하여 원본 이메일과 최대한 일치시킵니다.

   ![](assets/des_loading_compatible_fragment_6.png)

   스타일 설정 및 인라인 속성 관리에 대한 자세한 내용은 [전자 메일 스타일 편집](../../designing/using/styles.md)을 참조하십시오.

1. 이전에 만든 두 조각(머리글 및 바닥글)을 원하는 구조 구성 요소에 삽입합니다.

   ![](assets/des_loading_compatible_fragment_10.png)

1. 템플릿을 저장합니다.

이제 이메일 디자이너 내에서 이 템플릿을 완전히 관리하여 매월 수신자에게 보낼 뉴스레터를 만들고 업데이트할 수 있습니다.

사용하려면 이메일을 만들고 방금 만든 콘텐츠 템플릿을 선택합니다.

**관련 항목**:

* [이메일 만들기](../../channels/using/creating-an-email.md)
* [이메일 디자이너 소개 비디오](../../designing/using/designing-content-in-adobe-campaign.md#video)
* [이메일 콘텐츠를 처음부터 디자인하기](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch)

### 튜토리얼 비디오 {#video}

이 비디오에서는 자신만의 템플릿을 만드는 방법을 보여줍니다.

>[!VIDEO](https://video.tv.adobe.com/v/23106?quality=12)

추가 Campaign Standard 방법 동영상은 [여기](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/overview.html?lang=ko)에 있습니다.

## 조각 정보 {#about-fragments}

>[!CONTEXTUALHELP]
>id="ac_fragments"
>title="조각 정보"
>abstract="조각은 하나 이상의 이메일에서 참조할 수 있는 재사용 가능한 콘텐츠 블록입니다."

조각은 하나 이상의 이메일에서 참조할 수 있는 재사용 가능한 구성 요소입니다.
**리소스** > **컨텐츠 조각 및 템플릿** 아래의 인터페이스에서 찾을 수 있습니다.

이메일 디자이너에서 조각을 가장 잘 사용하려면

* 자체 조각을 만듭니다. [컨텐츠 조각 만들기](#creating-a-content-fragment) 및 [컨텐츠를 조각](#saving-content-as-a-fragment)으로 저장 을 참조하십시오.
* 이메일에 필요한 만큼 많이 사용합니다. [전자 메일](#inserting-elements-into-an-email)에 요소 삽입 을 참조하십시오.
* 조각을 편집할 때 변경 사항이 동기화됩니다. 준비되거나 아직 전송되지 않은 경우 해당 조각을 포함하는 모든 이메일에 자동으로 전파됩니다.

전자 메일에 추가되면 기본적으로 조각이 잠깁니다. 특정 이메일에 대한 조각을 수정하려면 조각이 사용된 이메일에서 조각의 잠금을 해제하여 원래 조각과의 동기화를 중단할 수 있습니다. 변경 사항은 더 이상 동기화되지 않습니다.

이메일 내에서 조각의 잠금을 해제하려면 이메일 을 선택하고 컨텍스트 도구 모음에서 잠금 아이콘을 클릭합니다.

![](assets/des_unlocking_fragment.png)

해당 조각은 원래 조각에 더 이상 연결되지 않은 독립형 구성 요소가 됩니다. 그런 다음 다른 컨텐츠 구성 요소로 편집할 수 있습니다. [컨텐츠 구성 요소 정보](../../designing/using/designing-from-scratch.md#about-content-components)를 참조하십시오.

### 이메일에 조각 삽입 {#inserting-elements-into-an-email}

전자 메일의 콘텐츠를 정의하기 위해 미리 배치한 구조 구성 요소에 콘텐츠 요소를 추가할 수 있습니다. [전자 메일 구조 편집](../../designing/using/designing-from-scratch.md#defining-the-email-structure)을 참조하십시오.

1. 왼쪽의 **+** 아이콘을 선택하여 컨텐츠 요소에 액세스합니다. [조각](#about-fragments) 또는 [컨텐츠 구성 요소](../../designing/using/designing-from-scratch.md#about-content-components)를 선택합니다.
1. 추가하려는 조각의 레이블이나 부분을 이미 알고 있는 경우 해당 레이블을 검색할 수 있습니다.

   ![](assets/email_designer_fragmentsearch.png)

1. 팔레트에서 조각 또는 콘텐츠 구성 요소를 이메일의 구조 구성 요소로 끌어다 놓습니다.

   ![](assets/email_designer_addfragment.png)

   요소를 이메일에 추가하면 구조 구성 요소 내부 또는 이메일의 다른 구조 구성 요소로 이동할 수 있습니다.

   ![](assets/email_designer_movefragment.png)

1. 이 이메일의 정확한 요구 사항에 맞게 요소를 편집합니다. 텍스트, 링크, 이미지 등을 추가할 수 있습니다.

   >[!NOTE]
   >
   >조각은 전자 메일에 추가할 때 기본적으로 잠깁니다. 특정 이메일에 대한 조각을 수정하려면 원래 조각과의 동기화를 중단하거나 조각에서 직접 변경할 수 있습니다. [조각 정보](#about-fragments)를 참조하십시오.

1. 전자 메일에 추가해야 하는 모든 요소에 대해 이 절차를 반복합니다.
1. 이메일을 저장합니다.

이제 이메일 구조가 채워지므로 각 콘텐츠 요소의 스타일을 편집할 수 있습니다. [요소 편집](../../designing/using/styles.md)을 참조하십시오.

>[!NOTE]
>
>조각이 수정되면 변경 사항은 조각이 사용되는 이메일에 자동으로 전파됩니다. 자세한 내용은 [조각 정보](#about-fragments)를 참조하십시오.

### 컨텐츠 조각 만들기 {#creating-a-content-fragment}

자신만의 컨텐츠 조각을 만들어 하나 이상의 이메일에서 필요에 따라 사용할 수 있습니다.

1. **[!UICONTROL Resources]** > **[!UICONTROL Content templates & fragments]** 로 이동하고 **[!UICONTROL Create]** 를 클릭합니다.
1. 전자 메일 레이블을 클릭하여 전자 메일 디자이너의 **[!UICONTROL Properties]** 탭에 액세스합니다.
1. 인식할 수 있는 레이블을 지정하고 다음 매개 변수를 선택하여 이메일 컨텐츠를 편집할 때 조각을 찾습니다.

   * 조각은 이메일와만 호환되므로 **[!UICONTROL Content type]** 드롭다운 목록에서 **[!UICONTROL Delivery]**&#x200B;을(를) 선택합니다.
   * **[!UICONTROL HTML type]** 드롭다운 목록에서 **[!UICONTROL Fragment]** 을 선택하여 이 컨텐츠를 조각으로 사용할 수 있습니다.

   ![](assets/email_designer_createfragment.png)

1. 필요한 경우 조각의 축소판으로 사용할 이미지를 설정할 수 있습니다. 템플릿 속성의 **[!UICONTROL Thumbnail]** 탭에서 선택합니다.

   ![](assets/email_designer_createfragment_thumbnail.png)

   이메일을 편집할 때 조각의 레이블 옆에 이 축소판이 표시됩니다.

1. **[!UICONTROL Properties]** 탭을 닫고 기본 작업 공간으로 돌아갑니다.
1. 필요에 따라 사용자 지정할 수 있는 구조 구성 요소 및 컨텐츠 구성 요소를 추가합니다.

   >[!CAUTION]
   >
   >조각은 개인화 필드, 동적 콘텐츠 또는 다른 조각을 포함할 수 없습니다.
   >
   >빈 구조 구성 요소가 있는 조각 컨텐츠로 저장하지 마십시오. >조각을 삽입하면 편집할 수 없습니다.
   >
   >[모바일 보기](../../designing/using/plain-text-html-modes.md#switching-to-mobile-view)는 조각에서 사용할 수 없습니다.

1. 편집되면 조각을 저장합니다.

이제 이메일 디자이너를 사용하여 만든 모든 이메일에서 이 조각을 사용할 수 있습니다. 팔레트의 **[!UICONTROL Fragments]** 섹션 아래에 나타납니다.

>[!NOTE]
>
>개인화 필드를 이메일에서 사용하고 잠금이 해제된 경우가 아니면 조각 내에 삽입할 수 없습니다. [조각 정보](#about-fragments)를 참조하십시오.

### 컨텐츠를 조각으로 저장 {#saving-content-as-a-fragment}

이메일 디자이너를 사용하여 이메일을 편집할 때 해당 이메일의 일부를 조각으로 직접 저장할 수 있습니다.

* 개인화 필드, 동적 컨텐츠 또는 다른 조각을 포함하는 구조는 조각으로 저장할 수 없습니다.
* 서로 인접한 구조만 선택할 수 있습니다.
<!-- - You cannot select an empty structure.-->

1. 이메일 디자이너에서 이메일을 편집할 때 기본 도구 모음에서 **[!UICONTROL Save as fragment]** 을 선택합니다.

   ![](assets/email_designer_save-as-fragment.png)

1. 작업 공간에서 조각을 작성할 구조를 선택합니다.

   ![](assets/email_designer_save-as-fragment_select.png)

   >[!NOTE]
   >
   >서로 인접하고 개인화 필드, 동적 콘텐츠 또는 다른 조각을 포함하지 않는 구조를 선택해야 합니다.
   <!--You cannot select an empty structure.-->

1. **[!UICONTROL Create]**&#x200B;를 클릭합니다.

1. 필요한 경우 레이블과 설명을 추가한 다음 **[!UICONTROL Save]** 을 클릭합니다.

   ![](assets/email_designer_save-as-fragment_popup.png)

1. 방금 만든 조각을 찾으려면 **[!UICONTROL Resources]** > **[!UICONTROL Content templates & fragments]** 로 이동합니다.

   ![](assets/email_designer_save-as-fragment_list.png)

1. 새 조각을 사용하려면 이메일 컨텐츠를 열고 조각 목록에서 선택합니다.

![](assets/email_designer_save-as-fragment_in-new-email.png)

>[!NOTE]
>[모바일 보기](../../designing/using/plain-text-html-modes.md#switching-to-mobile-view)는 조각에서 사용할 수 없습니다. 이메일 모바일 보기를 편집하려면 컨텐츠를 조각으로 저장하기 전에 이 작업을 수행하십시오.

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

이메일 디자이너를 사용하여 재사용 가능한 각 섹션에 대한 조각을 만듭니다. 이 예에서는 두 개의 조각을 만듭니다. 머리글과 바닥글에 대해 각각 하나씩, 그런 다음 기존 컨텐츠의 관련 부품을 이러한 조각에 복사할 수 있습니다.

이렇게 하려면 아래 단계를 수행합니다:

1. Adobe Campaign에서 **[!UICONTROL Resources]** > **[!UICONTROL Content templates & fragments]** 로 이동하여 헤더에 대한 조각을 만듭니다. 자세한 내용은 [컨텐츠 조각 만들기](#creating-a-content-fragment)를 참조하십시오.
1. 조각에 필요한 만큼 구조 구성 요소를 추가합니다.

   ![](assets/des_loading_compatible_fragment_1.png)

1. 구조에 이미지 및 텍스트 구성 요소를 삽입합니다.

   ![](assets/des_loading_compatible_fragment_2.png)

1. 해당 이미지를 업로드하고 텍스트를 입력하고 설정을 조정합니다.

   ![](assets/des_loading_compatible_fragment_3.png)

1. 조각을 저장합니다.
1. 바닥글을 만들고 저장하려면 유사하게 진행하십시오.

   ![](assets/des_loading_compatible_fragment_4.png)

이제 조각을 템플릿에서 사용할 준비가 되었습니다.
