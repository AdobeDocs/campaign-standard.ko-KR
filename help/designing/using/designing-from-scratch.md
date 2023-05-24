---
title: 이메일 디자인 기초
description: 이메일 디자이너에서 이메일 콘텐츠를 처음부터 디자인하는 방법을 알아봅니다.
audience: designing
content-type: reference
topic-tags: editing-email-content
feature: Email Design
role: User
level: Beginner
exl-id: 052d24b7-d3e0-41d7-8b2c-92bd3addb3a2
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '1239'
ht-degree: 23%

---

# 이메일 디자인 기초 {#designing-an-email-content-from-scratch}

이메일 콘텐츠 에디션을 마스터하는 방법에 대해 알아봅니다. 이메일 디자이너를 사용하면 미리 정의된 고유한 콘텐츠로 시작하거나 포함하지 않고 이메일과 템플릿을 만들 수 있습니다.

이메일 디자이너를 사용하여 이메일 콘텐츠를 처음부터 만들고 디자인하는 주요 단계는 다음과 같습니다.

1. 이메일을 만들고 해당 콘텐츠를 엽니다.
1. 구조 구성 요소를 추가하여 이메일을 구성합니다. 다음을 참조하십시오 [이메일 구조 편집](#defining-the-email-structure).
1. 구조 구성 요소에 콘텐츠 구성 요소 및 조각을 삽입합니다. 다음을 참조하십시오 [조각 및 콘텐츠 구성 요소 추가](#defining-the-email-structure).
1. 이미지를 추가하고 이메일 텍스트를 편집합니다. 다음을 참조하십시오 [이미지 삽입](../../designing/using/images.md#inserting-images).
1. 개인화 필드, 링크 등을 추가하여 이메일을 개인화합니다. 다음을 참조하십시오 [개인화 필드 삽입](../../designing/using/personalization.md#inserting-a-personalization-field), [링크 삽입](../../designing/using/links.md#inserting-a-link) 및 [이메일에서 동적 콘텐츠 정의](../../designing/using/personalization.md#defining-dynamic-content-in-an-email).
1. 이메일의 제목 줄을 정의합니다. 다음을 참조하십시오 [이메일 제목란 개인화](../../designing/using/subject-line.md#defining-the-subject-line-of-an-email).
1. 이메일 미리 보기.
1. 콘텐츠를 저장하고 대상자를 정의하고 전송을 적절하게 예약했는지 확인한 후 메시지를 계속 진행합니다.

이것도 확인해 보세요 [소개 비디오](https://video.tv.adobe.com/v/22771/?autoplay=true&hidetitle=true).

>[!NOTE]
>
>이메일 콘텐츠를 처음부터 디자인하지 않으려면 기본 제공 콘텐츠 템플릿을 사용할 수 있습니다. 자세한 내용은 [콘텐츠 템플릿](../../designing/using/using-reusable-content.md#content-templates).

## 이메일 구조 정의 {#defining-the-email-structure}

>[!CONTEXTUALHELP]
>id="ac_structure_components"
>title="구조 구성 요소 정보"
>abstract="구조 구성 요소는 이메일 레이아웃을 정의합니다."

>[!CONTEXTUALHELP]
>id="ac_edition_columns"
>title="이메일 열 정의"
>abstract="이메일 디자이너를 통해 열 구조를 정의하여 이메일 레이아웃을 쉽게 정의할 수 있습니다."

이메일 디자이너를 통해 이메일 구조를 쉽게 정의할 수 있습니다. 간단한 드래그 앤 드롭 작업으로 구조 요소를 추가 및 이동하여 이메일 모양을 몇 초 이내에 디자인할 수 있습니다.

전자 메일 구조를 편집하려면:

1. 기존 콘텐츠를 열거나 새 이메일 콘텐츠를 만듭니다.
1. 액세스 **[!UICONTROL Structure components]** 을(를) 선택하여 **+** 왼쪽에 있는 아이콘.

   ![](assets/email_designer_structure.png)

1. 이메일 형태를 만드는 데 필요한 구조 구성 요소를 드래그 앤 드롭합니다.

   ![](assets/email_designer_structure_components.png)

   파란색 선은 구조 구성 요소를 놓기 전에 정확한 위치를 나타냅니다. 다른 구성 요소 위, 사이 또는 아래에 드롭할 수 있지만 안쪽에는 드롭할 수 없습니다.

   >[!NOTE]
   >
   >일부 이메일 프로그램에서는 열 스택이 호환되지 않을 수 있습니다. 지원되지 않을 경우, 열이 스택되지 않습니다.
   >
   >이메일에 배치되면 콘텐츠 구성 요소 또는 조각이 이미 내부에 배치되지 않은 한 구성 요소를 이동하거나 제거할 수 없습니다.

1. 하나 이상의 열로 구성된 여러 구조 구성 요소를 사용할 수 있습니다.

   다음 항목 선택 **[!UICONTROL n:n column]** 선택한 열의 수를 정의하는 구성 요소(3~10개). 각 열의 아래쪽에 있는 화살표를 이동하여 각 열의 폭을 정의할 수도 있습니다.

   ![](assets/email_designer_n-n-column.png)

   >[!NOTE]
   >
   >각 열 크기는 구조 구성 요소 전체 폭의 10% 이상이어야 합니다. 비어 있는 열만 제거할 수 있습니다.

구조가 정의되면 이메일에 콘텐츠 조각 및 구성 요소를 추가할 수 있습니다.

## 프리 헤더 사용 {#preheader}

>[!CONTEXTUALHELP]
>id="ac_edition_preheader"
>title="프리 헤더 사용"
>abstract="프리 헤더를 사용하여 더 높은 이메일 열람율을 전달하는 짧은 요약 텍스트를 구성할 수 있습니다."

프리 헤더는 받은 편지함에서 이메일을 볼 때 제목 줄 다음에 오는 짧은 요약 텍스트입니다. 프리 헤더는 더 높은 열기 속도를 제공합니다.

다음 항목 선택 **[!UICONTROL Preheader]** 편집 상자를 열고 콘텐츠를 완료합니다.

![](assets/email_designer_preheader.png)

다음을 추가할 수 있습니다. **[!UICONTROL Content block]**, a **[!UICONTROL Dynamic content]** 또는 **[!UICONTROL Personalization fields]** 를 추가합니다.

>[!NOTE]
>
>일부 이메일 프로그램에서는 프리 헤더가 호환되지 않을 수 있습니다. 지원되지 않을 경우, 프리 헤더가 표시되지 않습니다.

## 콘텐츠 구성 요소 사용 {#about-content-components}

>[!CONTEXTUALHELP]
>id="ac_content_components"
>title="콘텐츠 구성 요소 정보"
>abstract="콘텐츠 구성 요소는 이메일 작성 시 편집할 수 있는 빈 콘텐츠 플레이스홀더입니다."

콘텐츠 구성 요소는 이메일에 배치되면 편집할 수 있는 비어 있는 원시 구성 요소입니다.

구조 구성 요소에 원하는 만큼 콘텐츠 구성 요소를 추가할 수 있습니다. 구조 구성 요소 내부 또는 다른 구조 구성 요소로 이동할 수도 있습니다.

다음은 이메일 디자이너에서 사용할 수 있는 구성 요소 목록입니다.

### **[!UICONTROL Button]**

각 단추를 처음부터 편집하지 않고 여러 단추를 사용해야 하는 경우 **[!UICONTROL Button]** 상황별 도구 모음을 사용하는 구성 요소.

버튼을 재사용할 수 있는 조각으로 저장할 수도 있습니다. 자세한 내용은 [컨텐츠 조각 만들기](../../designing/using/using-reusable-content.md#creating-a-content-fragment) 및 [콘텐츠를 조각으로 저장](../../designing/using/using-reusable-content.md#saving-content-as-a-fragment).

선택 **[!UICONTROL Fallback view]** 이메일 디자이너에 대체 이미지를 표시합니다.

### **[!UICONTROL Text]**

이 구성 요소를 사용하여 이메일에 텍스트를 삽입합니다. 에서 텍스트의 색상, 스타일 및 크기를 조정할 수 있습니다 **[!UICONTROL Component Settings]**.

### **[!UICONTROL Divider]**

이 구성 요소를 사용하여 이메일에 구분선을 삽입합니다. 에서 줄바꿈의 색상, 스타일 및 크기를 선택할 수 있습니다 **[!UICONTROL Component Settings]**.

### **[!UICONTROL HTML]**

이 구성 요소를 사용하여 기존 HTML의 다른 부분을 복사하여 붙여넣습니다. 이를 통해 자유 모듈식 HTML 구성 요소를 만들 수 있습니다.

>[!NOTE]
>
>사용 가능한 HTML 구성 요소는 제한된 옵션을 사용하여 편집할 수 있습니다. 모든 스타일이 인라인 되어 있지 않으면 **head** HTML 섹션에 있는 마지막 항목이 될 필요가 없습니다. 사용 **[!UICONTROL Preview]** 콘텐츠의 응답성을 테스트하기 위한 버튼(참조 [메시지 미리 보기](../../sending/using/previewing-messages.md)).

단순히 이메일 디자이너를 준수하는 외부 콘텐츠를 만들려면, Adobe은 메시지를 처음부터 만들고 기존 이메일의 콘텐츠를 조각 및 구성 요소로 복사하는 것이 좋습니다.

다시 만들 수 없는 컨텐츠가 있는 경우 를 사용하여 원본 이메일에서 HTML 코드를 복사하여 붙여넣을 수 있습니다. **[!UICONTROL Html]** 컨텐츠 구성 요소입니다. 계속하기 전에 HTML을 숙지하십시오.

>[!NOTE]
>
>새 콘텐츠는 원본 이메일의 정확한 사본이 되지 않지만 아래 단계는 가능한 한 가까워지는 메시지를 만드는 과정을 안내합니다.

**콘텐츠를 복사하기 전에**

1. 원래 이메일에서 보낼 각 이메일에 고유한 섹션에서 재사용 가능한 섹션을 식별합니다.
1. 사용할 모든 이미지와 에셋을 저장합니다.
1. HTML에 익숙하다면 원래 HTML 콘텐츠를 다른 부분으로 분할하십시오.

### 비디오 {#video-settings}

>[!CONTEXTUALHELP]
>id="ac_edition_video"
>title="비디오 설정"
>abstract="이 구성 요소를 사용하여 비디오를 이메일에 삽입합니다. 비디오는 모든 이메일 클라이언트에서 작동하지 않습니다. 대체 이미지를 설정하는 것이 좋습니다."
>additional-url="https://www.emailonacid.com/blog/article/email-development/a_how_to_guide_to_embedding_html5_video_in_email/" text="추가 정보"

이메일의 구조 구성 요소에 비디오 구성 요소를 삽입하고 **[!UICONTROL Component Settings]**.

>[!NOTE]
>
>일부 이메일 프로그램에서는 비디오가 호환되지 않을 수 있습니다. 지원되지 않을 경우, 대체 항목이 표시됩니다.

### 이미지

이 구성 요소를 사용하여 이메일에 이미지를 삽입합니다.

이미지 구성 요소를 구조 구성 요소에 삽입하고 찾아보기를 클릭하여 컴퓨터에서 이미지 파일을 업로드합니다.

### **[!UICONTROL Social]**

이 구성 요소를 사용하여 이메일에 소셜 미디어 페이지에 대한 링크를 삽입합니다. 표시할 링크와 해당 아이콘 크기를 선택할 수 있습니다 **[!UICONTROL Component Settings]**.

### 캐러셀 {#carousel-settings}

>[!CONTEXTUALHELP]
>id="ac_edition_carousel"
>title="슬라이드 설정"
>abstract="슬라이드를 콘텐츠에 삽입하고 구성하는 방법에 대해 알아봅니다. 슬라이드는 모든 이메일 클라이언트에서 작동하지 않으며 지원되지 않는 경우 대체 이미지가 표시됩니다."

1. 을(를) 끌어다 놓습니다. **[!UICONTROL Carousel]** 구조 구성 요소 내의 구성 요소입니다.
1. 컴퓨터에서 이미지를 검색하여 선택하십시오.

   ![](assets/des_carousel_browse.png)

1. 다음에서 **[!UICONTROL Settings]** 창에서 회전판에 놓을 축소판 수를 설정합니다.
1. 컴퓨터에서 대체 이미지를 선택하십시오.

   ![](assets/des_carousel_fallback.png)

슬라이드 구성 요소는 일부 이메일 프로그램과 호환되지 않습니다. 이메일에서 캐러셀이 지원되지 않는 경우 이미지를 대신 표시하려면 폴백을 업로드하십시오.

>[!NOTE]
>
>슬라이드 구성 요소는 다음 이메일 플랫폼과 호환됩니다. Apple 메일 7, Apple 메일 8, Mac용 Outlook 2011, Mac용 Outlook 2016, Mozilla Thunderbird, iPad 및 iPad 미니 iOS, iPhone iOS, Android, AOL(Chrome, Firefox 및 Safari).

**관련 항목**:

- [이메일 만들기](../../channels/using/creating-an-email.md)
- [메시지에서 대상자 선택](../../audiences/using/selecting-an-audience-in-a-message.md)
- [메시지 예약](../../sending/using/about-scheduling-messages.md)
- [메시지 미리 보기](../../sending/using/previewing-messages.md)
- [이메일 렌더링](../../sending/using/email-rendering.md)
