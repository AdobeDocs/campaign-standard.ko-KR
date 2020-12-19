---
solution: Campaign Standard
product: campaign
title: '이메일 디자인 기초 '
description: 이메일 디자이너의 이메일 컨텐츠를 처음부터 디자인하여 이메일을 디자인하는 방법을 살펴볼 수 있습니다.
audience: designing
content-type: reference
topic-tags: editing-email-content
translation-type: tm+mt
source-git-commit: 2d28048590b52b81f27cd1cfe10be029bbc35197
workflow-type: tm+mt
source-wordcount: '1239'
ht-degree: 2%

---


# 이메일 디자인 기초 {#designing-an-email-content-from-scratch}

이메일 컨텐츠 에디션을 마스터하는 방법을 살펴볼 수 있습니다. 이메일 디자이너는 사전 정의된 컨텐츠를 사용하거나 사용하지 않고 이메일 및 템플릿을 만들 수 있습니다.

이메일 디자이너를 사용하여 이메일 컨텐츠를 처음부터 만들고 디자인하는 주요 단계는 다음과 같습니다.

1. 이메일을 만들어 컨텐츠를 엽니다.
1. 구조 구성 요소를 추가하여 이메일 모양을 만듭니다. [이메일 구조 편집](#defining-the-email-structure)을 참조하십시오.
1. 구조 구성 요소에 컨텐츠 구성 요소 및 조각을 삽입합니다. [조각 및 콘텐츠 구성 요소 추가](#defining-the-email-structure)를 참조하십시오.
1. 이미지를 추가하고 이메일 텍스트를 편집합니다. [이미지 삽입](../../designing/using/images.md#inserting-images)을(를) 참조하십시오.
1. 개인화 필드, 링크 등을 추가하여 이메일을 개인화합니다. [개인화 필드 삽입](../../designing/using/personalization.md#inserting-a-personalization-field), [링크 삽입](../../designing/using/links.md#inserting-a-link) 및 [이메일](../../designing/using/personalization.md#defining-dynamic-content-in-an-email)에서 동적 컨텐츠 정의를 참조하십시오.
1. 이메일의 제목 줄을 정의합니다. [이메일 제목 줄 맞춤화를 참조하십시오](../../designing/using/subject-line.md#defining-the-subject-line-of-an-email).
1. 이메일 미리 보기.
1. 컨텐트를 저장하고 대상을 정의하고 전송을 적절하게 예약했는지 확인한 후 메시지를 계속 진행합니다.

이 [소개 비디오](https://video.tv.adobe.com/v/22771/?autoplay=true&hidetitle=true&captions=kor)도 확인할 수 있습니다.

>[!NOTE]
>
>이메일 컨텐츠를 처음부터 디자인하지 않으려면 바로 사용 가능한 컨텐츠 템플릿을 사용할 수 있습니다. 자세한 내용은 [콘텐츠 템플릿](../../designing/using/using-reusable-content.md#content-templates)을 참조하십시오.

## 이메일 구조 정의 {#defining-the-email-structure}

>[!CONTEXTUALHELP]
>id="ac_structure_components"
>title="구조 구성 요소 정보"
>abstract="구조 구성 요소는 이메일의 레이아웃을 정의합니다."

>[!CONTEXTUALHELP]
>id="ac_edition_columns"
>title="이메일 열 정의"
>abstract="이메일 디자이너를 사용하면 열 구조를 정의하여 이메일의 레이아웃을 쉽게 정의할 수 있습니다."

이메일 디자이너를 사용하면 이메일의 구조를 쉽게 정의할 수 있습니다. 간단한 드래그 앤 드롭 동작으로 구조 요소를 추가하고 이동하여 신속하게 이메일 모양을 디자인할 수 있습니다.

이메일 구조를 편집하려면:

1. 기존 컨텐츠를 열거나 새 이메일 컨텐츠를 만듭니다.
1. 왼쪽의 **+** 아이콘을 선택하여 **[!UICONTROL Structure components]**&#x200B;에 액세스합니다.

   ![](assets/email_designer_structure.png)

1. 이메일을 구성하는 데 필요한 구조 구성 요소를 드래그하여 놓습니다.

   ![](assets/email_designer_structure_components.png)

   파란색 선은 구조 구성 요소를 놓기 전에 정확한 위치를 재구성합니다. 위의 다른 구성 요소 간 또는 아래에 놓을 수 있지만 안으로는 놓을 수 없습니다.

   >[!NOTE]
   >
   >열 스택은 모든 이메일 프로그램과 호환되지 않습니다. 지원되지 않는 경우 열이 누적되지 않습니다.
   >
   >이메일에 배치하면 이미 안에 배치된 컨텐츠 구성 요소나 조각이 없는 한 구성 요소를 이동하거나 제거할 수 없습니다.

1. 하나 이상의 열로 구성된 여러 구조 구성 요소를 사용할 수 있습니다.

   **[!UICONTROL n:n column]** 구성 요소를 선택하여 원하는 열 수(3에서 10 사이)를 정의합니다. 각 열 아래쪽에서 화살표를 이동하여 각 열의 너비를 정의할 수도 있습니다.

   ![](assets/email_designer_n-n-column.png)

   >[!NOTE]
   >
   >각 열 크기는 구조 구성 요소의 전체 너비의 10% 미만일 수 없습니다. 비어 있지 않은 열은 제거할 수 없습니다.

구조가 정의되면 컨텐츠 조각과 구성 요소를 이메일에 추가할 수 있습니다.

## 사전 헤더 사용 {#preheader}

>[!CONTEXTUALHELP]
>id="ac_edition_preheader"
>title="사전 헤더 사용"
>abstract="사전 헤더를 사용하면 이메일의 공개 비율이 높은 짧은 요약 텍스트를 구성할 수 있습니다."

사전 헤더는 받은 편지함에서 이메일을 볼 때 제목 줄 뒤에 오는 간단한 요약 텍스트입니다. 프리헤더는 열린 비율이 높습니다.

**[!UICONTROL Preheader]** 편집 상자를 선택하고 컨텐츠를 완료합니다.

![](assets/email_designer_preheader.png)

사전 헤더 컨텐츠에 **[!UICONTROL Content block]**, **[!UICONTROL Dynamic content]** 또는 **[!UICONTROL Personalization fields]**&#x200B;를 추가할 수 있습니다.

>[!NOTE]
>
>사전 헤더는 모든 이메일 프로그램과 호환되지 않습니다. 지원되지 않는 경우 미리 헤더가 표시되지 않습니다.

## 내용 구성 요소 사용 {#about-content-components}

>[!CONTEXTUALHELP]
>id="ac_content_components"
>title="컨텐츠 구성 요소 정보"
>abstract="컨텐츠 구성 요소는 이메일을 만들기 위해 편집할 수 있는 빈 컨텐츠 자리 표시자입니다."

컨텐츠 구성 요소는 원시 빈 구성 요소로서, 이메일로 한 번 편집하면 됩니다.

구조 구성 요소에서 원하는 만큼 컨텐츠 구성 요소를 추가할 수 있습니다. 구조 구성 요소 안이나 다른 구조 구성 요소로 이동할 수도 있습니다.

이메일 디자이너의 사용 가능한 구성 요소 목록은 다음과 같습니다.

### **[!UICONTROL Button]**

각 단추를 처음부터 편집하지 않고 여러 단추를 사용해야 하는 경우 상황에 맞는 도구 모음을 사용하여 **[!UICONTROL Button]** 구성 요소를 복제할 수 있습니다.

단추를 다시 사용할 수 있는 조각에 저장할 수도 있습니다. 이에 대한 자세한 내용은 [컨텐츠 조각 만들기](../../designing/using/using-reusable-content.md#creating-a-content-fragment) 및 [컨텐츠를 조각](../../designing/using/using-reusable-content.md#saving-content-as-a-fragment)으로 저장을 참조하십시오.

이메일 디자이너에서 대체 이미지를 표시하려면 **[!UICONTROL Fallback view]**&#x200B;을 선택합니다.

### **[!UICONTROL Text]**

이 구성 요소를 사용하여 이메일에 텍스트를 삽입합니다. **[!UICONTROL Component Settings]**&#x200B;에서 텍스트의 색상, 스타일 및 크기를 조정할 수 있습니다.

### **[!UICONTROL Divider]**

이 구성 요소를 사용하여 이메일에 분할선을 삽입합니다. **[!UICONTROL Component Settings]**&#x200B;에서 줄바꿈 줄의 색상, 스타일 및 크기를 선택할 수 있습니다.

### **[!UICONTROL HTML]**

이 구성 요소를 사용하여 기존 HTML의 다른 부분을 복사하여 붙여넣습니다. 이렇게 하면 무료로 모듈화된 HTML 구성 요소를 만들 수 있습니다.

>[!NOTE]
>
>무료 HTML 구성 요소는 제한된 옵션으로 편집할 수 있습니다. 모든 스타일이 인라인되지 않은 경우 HTML 코드의 **head** 섹션에 올바른 CSS를 추가해야 합니다. 그렇지 않으면 이메일이 응답적이지 않습니다. **[!UICONTROL Preview]** 단추를 사용하여 내용의 응답성을 테스트합니다([메시지 미리 보기](../../sending/using/previewing-messages.md) 참조).

간단하게 이메일 디자이너와 호환되는 외부 컨텐츠를 만들려면 Adobe은 메시지를 처음부터 만들고 기존 이메일의 컨텐츠를 조각 및 구성 요소로 복사하는 것이 좋습니다.

다시 만들 수 없는 컨텐츠가 있는 경우 **[!UICONTROL Html]** 컨텐츠 구성 요소를 사용하여 원본 이메일의 HTML 코드를 복사하여 붙여넣을 수 있습니다. 계속하기 전에 HTML에 익숙해야 합니다.

>[!NOTE]
>
>새 컨텐츠는 원본 이메일의 정확한 사본이 아니지만, 아래 단계를 통해 가능한 한 가까운 메시지를 만들 수 있습니다.

**컨텐츠를 복사하기 전**

1. 원본 이메일에서 전송할 각 이메일에 대해 고유한 섹션에서 재사용 가능한 섹션을 식별합니다.
1. 사용하려는 모든 이미지와 에셋을 저장합니다.
1. HTML에 익숙한 경우 원본 HTML 컨텐츠를 다른 부분으로 분할합니다.

### 비디오 {#video-settings}

>[!CONTEXTUALHELP]
>id="ac_edition_video"
>title="비디오 설정"
>abstract="이 구성 요소를 사용하여 이메일에 비디오를 삽입합니다. 일부 이메일 클라이언트에서 비디오가 작동하지 않습니다. 대체 이미지를 설정하는 것이 좋습니다."
>additional-url="https://www.emailonacid.com/blog/article/email-development/a_how_to_guide_to_embedding_html5_video_in_email/" text="추가 정보"

비디오 구성 요소를 이메일의 구조 구성 요소에 삽입하고 **[!UICONTROL Component Settings]**&#x200B;에 비디오 링크를 입력합니다.

>[!NOTE]
>
>비디오는 일부 이메일 프로그램과 호환되지 않습니다. 지원되지 않는 경우 폴백이 표시됩니다.

### 이미지

이 구성 요소를 사용하여 이메일에 이미지를 삽입합니다.

이미지 구성 요소를 구조 구성 요소에 삽입하고 찾아보기를 클릭하여 컴퓨터에서 이미지 파일을 업로드합니다.

### **[!UICONTROL Social]**

이 구성 요소를 사용하여 이메일에 소셜 미디어 페이지에 대한 링크를 삽입합니다. 표시할 링크와 **[!UICONTROL Component Settings]**&#x200B;에서 해당 아이콘의 크기를 선택할 수 있습니다.

### 회전판 {#carousel-settings}

>[!CONTEXTUALHELP]
>id="ac_edition_carousel"
>title="회전판 설정"
>abstract="Carousel을 컨텐츠에 삽입하고 구성하는 방법에 대해 알아보십시오.Carousel은 모든 이메일 클라이언트에서 작동하지 않으며, 지원되지 않는 경우에 대비한 이미지가 표시됩니다."

1. **[!UICONTROL Carousel]** 구성 요소를 구조 구성 요소 안으로 드래그하여 놓습니다.
1. 컴퓨터에서 이미지를 찾아 선택합니다.

   ![](assets/des_carousel_browse.png)

1. **[!UICONTROL Settings]** 창에서 회전판에서 원하는 축소판 수를 설정합니다.
1. 컴퓨터에서 대체 이미지를 선택합니다.

   ![](assets/des_carousel_fallback.png)

Carousel 구성 요소는 모든 이메일 프로그램과 호환되지 않습니다. 캐러셀이 이메일에서 지원되지 않는 경우 대신 이미지를 표시하도록 폴백을 업로드합니다.

>[!NOTE]
>
>회전판 구성 요소는 다음 이메일 플랫폼과 호환됩니다.Apple Mail 7, Apple Mail 8, Mac용 Outlook 2011, Mac용 Outlook 2016, Mozilla Thunderbird, iPad 및 iPad mini iOS, iPhone iOS, Android, AOL(Chrome, Firefox 및 Safari).

**관련 항목**:

- [전자 메일 만들기](../../channels/using/creating-an-email.md)
- [메시지에서 대상자 선택](../../audiences/using/selecting-an-audience-in-a-message.md)
- [메시지 예약](../../sending/using/about-scheduling-messages.md)
- [메시지 미리 보기](../../sending/using/previewing-messages.md)
- [이메일 렌더링](../../sending/using/email-rendering.md)
