---
title: Adobe Campaign에서 컨텐츠 디자인
description: 처음부터 이메일 컨텐츠 제작, HTML 가져오기 또는 기존 템플릿 활용
page-status-flag: never-activated
uuid: 8f73407f-ab90-46bc-aeb6-bd87fcb0404c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: about-content-design
discoiquuid: 20800cde-50ad-4d2b-a2f9-812258bec665
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5636b2ab5a673b0a52158b1a5411e090e4b45ca7
workflow-type: tm+mt
source-wordcount: '1138'
ht-degree: 4%

---


# Campaign 이메일 디자이너{#designing-content-in-adobe-campaign}

Adobe Campaign에서 이메일을 만든 후에는 해당 컨텐츠를 정의해야 합니다.

이메일 디자이너는 드래그 앤 드롭 인터페이스에서 개인화된 매력적인 이메일을 만들 수 있습니다. 처음부터 빈 화면으로 시작하거나 기존 컨텐츠 조각 또는 템플릿을 활용하는 경우 홍보 또는 거래 방식으로 모든 이메일 콘텐츠를 디자인하고 세부적으로 조정할 수 있습니다.

반응형 디자인에 최적화된 HTML을 전달하기 위해 구축된 이메일 디자이너는 가시성 조건과 동적 컨텐츠를 사용자 인터페이스를 통해 이메일, 템플릿 또는 단편에 손쉽게 정의하고 적용할 수 있습니다. 버튼을 클릭하면 드래그 앤 드롭 인터페이스와 HTML 코드 간에 원활하게 전환할 수 있습니다.

이메일 디자이너를 사용하면 이메일 컨텐츠를 만들고 이메일 컨텐츠 템플릿을 사용할 수 있습니다. 간단한 이메일, 트랜잭션 이메일, A/B 테스트 이메일, 다국어 이메일 및 반복 이메일과 호환됩니다.

이메일 디자이너를 시작하려면 이메일 디자이너의 일반적인 기능과 이메일 [을 처음부터 디자인하거나 템플릿을 사용하는 방법을 설명하는 이 비디오](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/designing-content/email-designer/email-designer-overview.html#GettingStarted) 세트를 시청하십시오.

<!--The Email Designer has more features than the Legacy Editor and is backward compatible.-->

* 이메일 컨텐츠를 만드는 방법을 알아보려면 이메일 디자이너 [로 시작을 참조하십시오](../../designing/using/quick-start.md).
* 이메일 디자이너에 대한 개요는 이메일 디자이너 [사용을 참조하십시오](../../designing/using/designing-content-in-adobe-campaign.md).
* 콘텐츠 제작에 대한 자세한 내용:
   * 처음부터 이메일 [디자인을 참조하십시오](../../designing/using/designing-from-scratch.md).
   * 기존 컨텐츠 사용을 참조하십시오 [](../../designing/using/using-existing-content.md).
   * Creative Cloud 통합 기능을 사용하면 [멀티 솔루션 이메일 디자인을 참조하십시오](../../designing/using/using-integrations.md).
* 개인화에 대한 자세한 내용은 개인화를 [참조하십시오](../../designing/using/personalization.md).

이메일을 만들 때 사전 정의된 템플릿을 사용하거나 다른 소스에서 기존 컨텐츠를 로드하도록 선택할 수 있습니다. 기존 [컨텐츠 선택을 참조하십시오](../../designing/using/using-existing-content.md#selecting-an-existing-content).

마케팅 캠페인의 효율성을 높이려면 컨텐츠를 개인화합니다. 개인화 필드 [삽입](../../designing/using/personalization.md#inserting-a-personalization-field) 및 컨텐츠 블록 [추가를 참조하십시오](../../designing/using/personalization.md#adding-a-content-block).

각 프로필에 따라 달라지는 동적 컨텐츠를 정의할 수도 있습니다. 이메일 [에서 동적 컨텐츠 정의](../../designing/using/personalization.md#defining-dynamic-content-in-an-email) 및 랜딩 페이지에서 [동적 컨텐츠 정의를 참조하십시오](../../channels/using/designing-a-landing-page.md#defining-dynamic-content-in-a-landing-page).

메시지와 랜딩 페이지를 링크 및 이미지로 향상시킬 수 있습니다. 링크 [삽입](../../designing/using/links.md#inserting-a-link) 및 이미지 [삽입을 참조하십시오](../../designing/using/images.md#inserting-images).

## 이메일 디자이너 인터페이스 {#email-designer-interface}

이메일 디자이너는 컨텐츠의 모든 측면을 제작, 편집 및 사용자 정의할 수 있는 다양한 옵션을 제공합니다.

인터페이스는 서로 다른 기능을 제공하는 여러 영역으로 구성됩니다.

![](assets/email_designer_overview.png)

팔레트 **(1)에서 사용할 수 있는 요소** 에서 구조 구성 요소 및 컨텐츠 조각을 기본 작업 **공간** (2)으로 드래그하여 놓습니다. 작업 공간(2)에서 구성 요소 또는 요소를 **선택하고 설정** 창( **3)에서** 기본 스타일 및 표시 특성을 사용자정의합니다.

기본 도구 모음 **(4)에서 더 많은 일반 옵션** 및 설정에 액세스할 수 있습니다.

>[!NOTE]
>
>설정 **** 창은 화면 해상도 및 표시에 따라 왼쪽으로 이동할 수 있습니다.

![](assets/email_designer_toolbar.png)

편집기 인터페이스 **의 상황에 맞는 도구** 모음은 선택한 영역에 따라 다양한 기능을 제공합니다. 여기에는 동작 버튼과 텍스트 스타일을 변경할 수 있는 버튼이 포함되어 있습니다. 수행한 수정 사항은 항상 선택한 영역에 적용됩니다.

### 이메일 디자이너 홈 페이지 {#email-designer-home-page}

이메일 [을 만들](../../channels/using/creating-an-email.md)때 이메일 컨텐츠를 선택하면 **[!UICONTROL Email Designer]** 홈 페이지가 자동으로 표시됩니다.

![](assets/email_designer_home_page.png)

이 **[!UICONTROL Properties]** 탭에서는 레이블, 보낸 사람의 주소 및 이름 또는 이메일 제목과 같은 이메일 세부 사항을 편집할 수 있습니다. 화면 상단에 있는 이메일 레이블을 클릭하여 이 탭에 액세스할 수도 있습니다.

![](assets/email_designer_home_properties.png)

탭 **[!UICONTROL Templates]** 을 사용하면 곧바로 사용할 수 있는 HTML 컨텐츠 또는 이미 만든 템플릿 중에서 선택하여 이메일 디자인을 신속하게 시작할 수 있습니다. 컨텐츠 [템플릿을 참조하십시오](../../designing/using/using-reusable-content.md#content-templates).

![](assets/email_designer_home_templates.png)

이 **[!UICONTROL Learn & support]** 탭에서는 관련 설명서 및 자습서에 손쉽게 액세스할 수 있습니다.

![](assets/email_designer_home_support.png)

템플릿을 선택하지 않으면 이메일 디자이너 홈 페이지에서 컨텐츠 디자인을 시작할 방법을 선택할 수도 있습니다.

* 단추를 클릭하여 새 컨텐츠를 처음부터 시작합니다. **[!UICONTROL Create]** 이메일 [컨텐츠를 처음부터 디자인하기를 참조하십시오](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch).
* 컴퓨터에서 파일을 업로드하려면 **[!UICONTROL Upload]** 단추를 클릭합니다. 파일에서 [콘텐트 가져오기를 참조하십시오](../../designing/using/using-existing-content.md#importing-content-from-a-file).
* URL에서 기존 컨텐츠를 검색하려면 **[!UICONTROL Import from URL]** 단추를 클릭합니다. URL [에서 콘텐트 가져오기를 참조하십시오](../../designing/using/using-existing-content.md#importing-content-from-a-url).

## 용어 {#terminology}

**템플릿**:템플릿은 여러 게재에 대해 작성하고 재사용할 수 있는 이메일 구조입니다.

**조각**:조각은 하나 이상의 이메일에서 참조할 수 있는 재사용 가능한 구성 요소입니다.

**구조 구성 요소**:이메일의 레이아웃을 정의하는 구조 요소입니다.

**컨텐츠 구성 요소**:컨텐츠 구성 요소는 원시 빈 구성 요소로서, 한 번 이메일에 배치되면 편집할 수 있습니다.

## 컨텐츠 디자인 모범 사례 {#content-design-best-practices}

이메일 디자이너를 적절하게 사용하고 최상의 이메일을 만들려면 다음 원칙을 적용하는 것이 좋습니다.

* HTML의 &lt;head> 섹션에서 별도의 CSS 및 CSS가 아닌 인라인 스타일을 사용할 수 있습니다. 인라인 스타일링을 사용하여 컨텐츠 조각 저장 및 재사용을 최적화할 수 있습니다.

   인라인 [스타일 속성 추가를 참조하십시오](../../designing/using/styles.md#adding-inline-styling-attributes).

* HTML 내용이 포함된 ZIP 파일을 가져오는 경우 일반 CSS를 사용합니다. SCSS 스타일 시트는 지원되지 않습니다.

* 컨텐츠 조각을 만들어 재사용하여 마케팅 캠페인 전반에서 일관성을 유지함으로써 브랜딩을 손쉽게 조정할 수 있습니다.

   컨텐츠 조각 [만들기를 참조하십시오](../../designing/using/using-reusable-content.md#creating-a-content-fragment).

* 이메일 **컨텐츠를 편집할 때**:

   메시지를 보내기 전에 미리 볼 수 있습니다. Adobe Campaign은 리트머스 를 사용하여 이메일 렌더링을 테스트할 수 있는 방법을 제공합니다. 자세한 내용은 [이메일 렌더링을 참조하십시오](../../sending/using/email-rendering.md).

메시지에 대한 자세한 디자인 및 일반 우수 사례는 다음 섹션에 나와 있습니다. [전달 모범 사례](../../sending/using/delivery-best-practices.md).

### 조각 업데이트 {#email-designer-updates}

이메일 디자이너는 지속적으로 개선되고 있습니다. 처음부터 이메일 컨텐츠를 직접 작성한 경우, 곧바로 사용할 수 있는 템플릿에서 또는 조각을 만든 경우, 다음에 컨텐트를 열 때 다음 업데이트 메시지를 받게 됩니다.

![](assets/email_designer_fragment_patch_message.png)

Adobe은 CSS 충돌 문제와 같은 문제를 방지하려면 컨텐츠를 최신 버전으로 업데이트하는 것이 좋습니다. **[!UICONTROL Update now]**&#x200B;을(를) 클릭합니다.

컨텐츠 업데이트 중에 오류가 발생하면 이 업데이트를 다시 실행하기 전에 HTML을 확인하고 수정하십시오.

조각에 대해서는 다음을 참고하십시오.

* 새 이메일 또는 템플릿에 조각을 추가하려는 경우 이 메시지가 표시되면 먼저 이 조각을 업데이트해야 합니다.

* 여러 조각이 있는 경우 이메일 컨텐츠에서 사용할 각 조각을 업데이트해야 합니다.

* 아직 준비되지 않은 현재 이메일 메시지에 영향을 주지 않도록 일부 조각을 업데이트하지 않도록 선택할 수 있습니다.

* 업데이트되지 않은 조각을 이미 사용하고 있지만 해당 조각을 편집할 수 없는 이메일을 보낼 수 있습니다.

* 이미 준비된 이메일에 사용된 조각을 업데이트하면 해당 이메일에 영향을 주지 않습니다.

## 이메일 디자이너 제한 사항 {#email-designer-limitations}

* 조각에서 개인화 필드를 사용할 수 없습니다. For more on fragments, see [this section](../../designing/using/using-reusable-content.md#about-fragments).

<!--* You cannot save directly as a fragment some content of an email that you are editing within the Email Designer. You need to copy-paste the HTML corresponding to that content into a new fragment. For more on this, see [Saving content as a fragment](../../designing/using/using-reusable-content.md#saving-content-as-a-fragment).-->

* 스타일을 편집할 때는 대부분의 이메일 클라이언트가 공식적으로 지원하는 웹 글꼴만 사용할 수 있습니다.
* 향후 재사용을 위해 스타일을 테마로 저장할 수 없습니다. 그러나 CSS 스타일은 컨텐츠 템플릿 또는 이메일에 저장할 수 있습니다. For more on styles, see [this section](../../designing/using/styles.md).

**관련 항목**

* [전자 메일 만들기](../../channels/using/creating-an-email.md)
* [랜딩 페이지 디자인](../../channels/using/designing-a-landing-page.md)
* [SMS 메시지 만들기](../../channels/using/creating-an-sms-message.md)
* [푸시 알림 만들기 및 전송](../../channels/using/preparing-and-sending-a-push-notification.md)
