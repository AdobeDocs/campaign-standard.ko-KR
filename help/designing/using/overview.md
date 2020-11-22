---
solution: Campaign Standard
product: campaign
title: 이메일 디자이너 사용
description: 이메일 디자이너와 이메일 디자인 컨텐츠를 구현하는 방법을 살펴보십시오.
audience: designing
content-type: reference
topic-tags: editing-email-content
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 88%

---


# 이메일 디자이너 사용 {#email-designer}

## 이메일 디자이너 개요 {#about-the-email-designer}

이메일 디자이너를 사용하면 이메일 콘텐츠를 만들고 이메일 콘텐츠 템플릿을 사용할 수 있습니다. 간단한 이메일, 트랜잭션 이메일, A/B 테스트 이메일, 다국어 이메일 및 반복 이메일과 호환됩니다.

이메일 디자이너를 시작하려면 이메일 디자이너의 일반적인 기능과 이메일을 처음부터 디자인하거나 템플릿을 사용하는 방법을 설명하는 이 [비디오 세트](https://docs.adobe.com/content/help/ko-KR/campaign-learn/campaign-standard-tutorials/designing-content/email-designer/email-designer-overview.html#GettingStarted)를 시청하십시오.

### 이메일 디자이너 홈페이지 {#email-designer-home-page}

[이메일을 만들때](../../channels/using/creating-an-email.md) 이메일 콘텐츠를 선택하면 **[!UICONTROL Email Designer]** 홈 페이지가 자동으로 표시됩니다.

![](assets/email_designer_home_page.png)

이 **[!UICONTROL Properties]** 탭에서는 레이블, 보낸 사람의 주소 및 이름 또는 이메일 제목과 같은 이메일 세부 사항을 편집할 수 있습니다. 화면 상단에 있는 이메일 레이블을 클릭하여 이 탭에 액세스할 수도 있습니다.

![](assets/email_designer_home_properties.png)

탭 **[!UICONTROL Templates]** 을 사용하면 기본 제공 HTML 콘텐츠 또는 이미 만든 템플릿 중에서 선택하여 이메일 디자인을 신속하게 시작할 수 있습니다. [콘텐츠 템플릿](../../designing/using/using-reusable-content.md#content-templates)을 참조하십시오.

![](assets/email_designer_home_templates.png)

이 **[!UICONTROL Learn & support]** 탭에서는 관련 설명서 및 자습서에 손쉽게 액세스할 수 있습니다.

![](assets/email_designer_home_support.png)

템플릿을 선택하지 않으면 이메일 디자이너 홈페이지에서 콘텐츠 디자인을 시작할 방법을 선택할 수도 있습니다.

* **[!UICONTROL Create]** 단추를 클릭하여 새 콘텐츠를 처음부터 시작합니다. [이메일 콘텐츠를 처음부터 디자인하기](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch)를 참조하십시오.
* 컴퓨터에서 파일을 업로드하려면 **[!UICONTROL Upload]** 단추를 클릭합니다. [파일에서 콘텐트 가져오기](../../designing/using/using-existing-content.md#importing-content-from-a-file)를 참조하십시오.
* URL에서 기존 콘텐츠를 검색하려면 **[!UICONTROL Import from URL]** 단추를 클릭합니다. [URL에서 콘텐트 가져오기](../../designing/using/using-existing-content.md#importing-content-from-a-url)를 참조하십시오.

### 이메일 디자이너 인터페이스 {#email-designer-interface}

이메일 디자이너는 콘텐츠의 모든 측면을 제작, 편집 및 사용자 정의할 수 있는 다양한 옵션을 제공합니다.

인터페이스는 서로 다른 기능을 제공하는 여러 영역으로 구성됩니다.

![](assets/email_designer_overview.png)

**팔레트** (1)에서 사용할 수 있는 요소에서 구조 구성 요소 및 콘텐츠 조각을 기본 **작업 영역** (2)로 끌어서 놓습니다. **작업 영역** (2)에서 구성 요소 또는 요소를 선택하고 **설정** 창 (3)에서 기본 스타일 및 표시 특성을 사용자 지정합니다.

기본 **도구 모음** (4)에서 더 많은 일반 옵션 및 설정에 액세스할 수 있습니다.

>[!NOTE]
>
>**설정** 창은 화면 해상도 및 표시에 따라 왼쪽으로 이동할 수 있습니다.

![](assets/email_designer_toolbar.png)

편집기 인터페이스의 **상황별 도구 모음**&#x200B;은 선택한 영역에 따라 다양한 기능을 제공합니다. 여기에는 동작 버튼과 텍스트 스타일을 변경할 수 있는 버튼이 포함되어 있습니다. 수행한 수정 사항은 항상 선택한 영역에 적용됩니다.

### 용어 {#terminology}

**템플릿**: 템플릿은 여러 게재에 대해 작성하고 재사용할 수 있는 이메일 구조입니다.

**조각**: 조각은 하나 이상의 이메일에서 참조할 수 있는 재사용 가능한 구성 요소입니다.

**구조 구성 요소**: 이메일의 레이아웃을 정의하는 구조 구성 요소입니다

**콘텐츠 구성 요소**: 콘텐츠 구성 요소는 이메일에 배치되면 편집할 수 있는 비어 있는 원시 구성 요소입니다.

### 콘텐츠 디자인 모범 사례 {#content-design-best-practices}

이메일 디자이너를 적절하게 사용하고 최상의 이메일을 만들려면 다음 원칙을 적용하는 것이 좋습니다.

* HTML의 &lt;head> 섹션에서 별도의 CSS 및 CSS가 아닌 인라인 스타일을 사용합니다. 인라인 스타일링을 사용하여 콘텐츠 조각 저장 및 재사용을 최적화합니다.

   [인라인 스타일 속성 추가](../../designing/using/styles.md#adding-inline-styling-attributes)를 참조하십시오.

* HTML 내용이 포함된 ZIP 파일을 가져오는 경우 일반 CSS를 사용합니다. SCSS 스타일 시트는 지원되지 않습니다.

* 콘텐츠 조각을 만들어 재사용하여 마케팅 캠페인 전반에서 일관성을 유지함으로써 브랜딩을 손쉽게 조정할 수 있습니다.

   [콘텐츠 조각 만들기](../../designing/using/using-reusable-content.md#creating-a-content-fragment)를 참조하십시오.

* **이메일 콘텐츠**&#x200B;를 편집할 때:

   메시지를 보내기 전에 미리 봅니다. Adobe Campaign은 Litmus를 사용하여 이메일 렌더링을 테스트할 수 있는 방법을 제공합니다. 자세한 내용은 [이메일 렌더링](../../sending/using/email-rendering.md)을 참조하십시오.

메시지에 대한 자세한 디자인 및 일반 우수 사례는 다음 섹션에 나와 있습니다. [전달 모범 사례](../../sending/using/delivery-best-practices.md)

### 이메일 디자이너 제한 사항 {#email-designer-limitations}

* 조각에서 개인화 필드를 사용할 수 없습니다. 조각에 대한 자세한 내용은 [이 섹션](../../designing/using/using-reusable-content.md#about-fragments)을 참조하십시오.

<!--* You cannot save directly as a fragment some content of an email that you are editing within the Email Designer. You need to copy-paste the HTML corresponding to that content into a new fragment. For more on this, see [Saving content as a fragment](../../designing/using/using-reusable-content.md#saving-content-as-a-fragment).-->
* 스타일을 편집할 때 대부분의 이메일 클라이언트는 공식적으로 지원하는 웹 글꼴만 사용할 수 있습니다.
* 향후 재사용을 위해 스타일을 테마로 저장할 수 없습니다. 그러나 CSS 스타일은 콘텐츠 템플릿 또는 이메일에 저장할 수 있습니다. 스타일에 대한 자세한 내용은 [이 섹션](../../designing/using/styles.md)을 참조하십시오.
* 레퍼러 메타 태그는 이메일 디자이너에서 지원되지 않습니다.
* 유니코드 문자 집합의 기본 다국어 평면에 포함되지 않은 문자를 2바이트(16비트)로 저장할 수 없으며 2UTF-16자로 인코딩해야 합니다. 이러한 문자에는 일부 CJK 비디오, 대부분의 이모지 및 일부 언어가 포함됩니다.
이러한 문자는 동적 텍스트에서 일부 비호환성 문제를 일으킬 수 있습니다. 메시지를 보내기 전에 강력한 테스트를 수행해야 합니다.

### 조각 업데이트 {#email-designer-updates}

이메일 디자이너는 지속적으로 개선되고 있습니다. 처음부터 이메일 콘텐츠를 직접 만든 경우, 기본 제공 템플릿에서 또는 조각을 만든 경우, 다음에 콘텐츠를 열 때 다음과 같은 업데이트 메시지를 받게 됩니다.

![](assets/email_designer_fragment_patch_message.png)

CSS 충돌 문제와 같은 문제를 방지하려면 콘텐츠를 최신 버전으로 업데이트하는 것이 좋습니다. **[!UICONTROL Update now]**&#x200B;을(를) 클릭합니다.

콘텐츠 업데이트 중에 오류가 발생하면 이 업데이트를 다시 실행하기 전에 HTML을 확인하고 수정하십시오.

조각에 대해서는 다음을 참고하십시오.

* 새 이메일 또는 템플릿에 조각을 추가하려는 경우 이 메시지가 표시되면 먼저 이 조각을 업데이트해야 합니다.

* 여러 조각이 있는 경우 이메일 콘텐츠에서 사용할 각 조각을 업데이트해야 합니다.

* 아직 준비되지 않은 현재 이메일 메시지에 영향을 주지 않도록 일부 조각을 업데이트하지 않도록 선택할 수 있습니다.

* 업데이트되지 않은 조각을 사용하고 있는 이메일을 보낼 수는 있으나, 해당 조각은 편집할 수는 없습니다.

* 이미 준비된 이메일에 사용된 조각을 업데이트하면 해당 이메일에 영향을 주지 않습니다.