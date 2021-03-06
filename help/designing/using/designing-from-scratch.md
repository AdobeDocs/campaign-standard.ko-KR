---
title: '이메일 디자인 기초 '
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
ht-degree: 2%

---

# 이메일 디자인 기초 {#designing-an-email-content-from-scratch}

이메일 콘텐츠 버전을 마스터하는 방법을 알아봅니다. 이메일 디자이너를 사용하면 사전 정의된 콘텐츠를 사용하거나 사용하지 않고 이메일 및 템플릿을 만들 수 있습니다.

이메일 디자이너를 사용하여 이메일 콘텐츠를 처음부터 만들고 디자인하는 주요 단계는 다음과 같습니다.

1. 이메일을 만들고 해당 콘텐츠를 엽니다.
1. 구조 구성 요소를 추가하여 전자 메일 모양을 지정합니다. 자세한 내용은 [전자 메일 구조 편집](#defining-the-email-structure).
1. 구조 구성 요소에 컨텐츠 구성 요소 및 조각을 삽입합니다. 자세한 내용은 [조각 및 컨텐츠 구성 요소 추가](#defining-the-email-structure).
1. 이미지를 추가하고 전자 메일의 텍스트를 편집합니다. 자세한 내용은 [이미지 삽입](../../designing/using/images.md#inserting-images).
1. 개인화 필드, 링크 등을 추가하여 이메일을 개인화합니다. 자세한 내용은 [개인화 필드 삽입](../../designing/using/personalization.md#inserting-a-personalization-field), [링크 삽입](../../designing/using/links.md#inserting-a-link) 및 [이메일에서 동적 콘텐츠 정의](../../designing/using/personalization.md#defining-dynamic-content-in-an-email).
1. 이메일의 제목란을 정의합니다. 자세한 내용은 [이메일 제목란 개인화](../../designing/using/subject-line.md#defining-the-subject-line-of-an-email).
1. 이메일 미리 보기.
1. 콘텐츠를 저장하고, 대상자를 정의하고 전송을 적절하게 예약했는지 확인한 후 메시지를 계속 진행합니다.

이 체크 아웃도 가능합니다 [소개 비디오](https://video.tv.adobe.com/v/22771/?autoplay=true&hidetitle=true).

>[!NOTE]
>
>이메일 콘텐츠를 처음부터 디자인하지 않으려면 기본 제공 콘텐츠 템플릿을 사용할 수 있습니다. 자세한 내용은 [콘텐츠 템플릿](../../designing/using/using-reusable-content.md#content-templates).

## 전자 메일 구조 정의 {#defining-the-email-structure}

>[!CONTEXTUALHELP]
>id="ac_structure_components"
>title="구조 구성 요소 정보"
>abstract="구조 구성 요소는 이메일의 레이아웃을 정의합니다."

>[!CONTEXTUALHELP]
>id="ac_edition_columns"
>title="이메일 열 정의"
>abstract="이메일 디자이너를 사용하면 열 구조를 정의하여 이메일 레이아웃을 쉽게 정의할 수 있습니다."

이메일 디자이너를 사용하면 이메일 구조를 쉽게 정의할 수 있습니다. 간단한 드래그 앤 드롭 작업으로 구조 요소를 추가 및 이동하면 몇 초 이내에 이메일 모양을 디자인할 수 있습니다.

전자 메일 구조를 편집하려면 다음을 수행하십시오.

1. 기존 콘텐츠를 열거나 새 이메일 콘텐츠를 만듭니다.
1. 액세스 권한 **[!UICONTROL Structure components]** 다음을 선택하여 **+** 아이콘을 클릭합니다.

   ![](assets/email_designer_structure.png)

1. 전자 메일 모양을 만드는 데 필요한 구조 구성 요소를 끌어다 놓습니다.

   ![](assets/email_designer_structure_components.png)

   파란색 선은 구조 구성 요소를 삭제하기 전에 정확한 위치를 구체화합니다. 위, 다른 구성 요소 사이 또는 아래에 놓을 수 있지만 내부에 놓을 수는 없습니다.

   >[!NOTE]
   >
   >열 스택은 모든 이메일 프로그램과 호환되지 않습니다. 지원되지 않는 경우에는 열이 스택되지 않습니다.
   >
   >전자 메일에 배치되면 이미 내부에 컨텐츠 구성 요소나 조각을 배치하지 않은 한 구성 요소를 이동하거나 제거할 수 없습니다.

1. 하나 이상의 열로 구성된 몇 가지 구조 구성 요소를 사용할 수 있습니다.

   을(를) 선택합니다 **[!UICONTROL n:n column]** 구성 요소를 사용하여 선택한 열 수를 정의합니다(3과 10 사이). 각 열의 맨 아래에서 화살표를 이동하여 각 열의 너비를 정의할 수도 있습니다.

   ![](assets/email_designer_n-n-column.png)

   >[!NOTE]
   >
   >각 열 크기는 구조 구성 요소의 전체 너비의 10% 이하일 수 없습니다. 비어 있지 않은 열은 제거할 수 없습니다.

구조가 정의되면 컨텐츠 조각 및 구성 요소를 이메일에 추가할 수 있습니다.

## 사전 헤더 사용 {#preheader}

>[!CONTEXTUALHELP]
>id="ac_edition_preheader"
>title="사전 헤더 사용"
>abstract="사전 헤더를 사용하면 이메일에 대한 열기 수가 더 높은 짧은 요약 텍스트를 구성할 수 있습니다."

사전 헤더는 받은 편지함에서 전자 메일을 볼 때 제목란을 따르는 간단한 요약 텍스트입니다. preheader가 더 높은 공개 비율을 전달합니다.

을(를) 선택합니다 **[!UICONTROL Preheader]** 편집 상자를 열고 컨텐츠를 완료합니다.

![](assets/email_designer_preheader.png)

을(를) 추가할 수 있습니다 **[!UICONTROL Content block]**, **[!UICONTROL Dynamic content]** 또는 **[!UICONTROL Personalization fields]** 를 입력합니다.

>[!NOTE]
>
>preheader가 모든 이메일 프로그램과 호환되지 않습니다. 지원되지 않는 경우 preheader가 표시되지 않습니다.

## 컨텐츠 구성 요소 사용 {#about-content-components}

>[!CONTEXTUALHELP]
>id="ac_content_components"
>title="컨텐츠 구성 요소 정보"
>abstract="콘텐츠 구성 요소는 이메일을 만들기 위해 편집할 수 있는 빈 콘텐츠 자리 표시자입니다."

컨텐츠 구성 요소는 이메일에 배치되면 편집할 수 있는 비어 있는 원시 구성 요소입니다.

구조 구성 요소에 원하는 만큼 콘텐츠 구성 요소를 추가할 수 있습니다. 구조 구성 요소 내부 또는 다른 구조 구성 요소로 이동할 수도 있습니다.

다음은 이메일 디자이너에서 사용할 수 있는 구성 요소 목록입니다.

### **[!UICONTROL Button]**

각 단추를 처음부터 편집하지 않고 여러 단추를 사용해야 하는 경우 **[!UICONTROL Button]** 구성 요소를 사용할 수 있습니다.

단추를 조각에 저장하여 재사용할 수도 있습니다. 자세한 내용은 [컨텐츠 조각 만들기](../../designing/using/using-reusable-content.md#creating-a-content-fragment) 및 [컨텐츠를 조각으로 저장](../../designing/using/using-reusable-content.md#saving-content-as-a-fragment).

선택 **[!UICONTROL Fallback view]** 전자 메일 디자이너에서 대체 이미지를 표시하려면

### **[!UICONTROL Text]**

이 구성 요소를 사용하여 전자 메일에 텍스트를 삽입합니다. 에서 텍스트의 색상, 스타일 및 크기를 조정할 수 있습니다 **[!UICONTROL Component Settings]**.

### **[!UICONTROL Divider]**

이 구성 요소를 사용하여 이메일에 분할선을 삽입합니다. 줄바꿈 선의 색상, 스타일 및 크기를 선택할 수 있습니다 **[!UICONTROL Component Settings]**.

### **[!UICONTROL HTML]**

이 구성 요소를 사용하여 기존 HTML의 다른 부분을 복사하여 붙여넣습니다. 이렇게 하면 무료 모듈식 HTML 구성 요소를 만들 수 있습니다.

>[!NOTE]
>
>무료 HTML 구성 요소는 제한된 옵션으로 편집할 수 있습니다. 모든 스타일이 삽입되지 않은 경우 **헤드** HTML 코드의 섹션, 그렇지 않으면 이메일이 응답하지 않습니다. 를 사용하십시오 **[!UICONTROL Preview]** 컨텐츠의 응답성을 테스트하기 위한 단추( 참조) [메시지 미리 보기](../../sending/using/previewing-messages.md)).

이메일 디자이너와 호환되는 외부 콘텐츠를 만들기만 한다면 메시지를 처음부터 만들고 기존 이메일의 컨텐츠를 조각 및 구성 요소로 복사하는 것이 좋습니다.

다시 생성할 수 없는 컨텐츠가 있는 경우 를 사용하여 원래 이메일에서 HTML 코드를 복사하여 붙여넣을 수 있습니다. **[!UICONTROL Html]** 컨텐츠 구성 요소입니다. 계속하기 전에 HTML을 잘 알고 있는지 확인하십시오.

>[!NOTE]
>
>새 컨텐츠는 원래 이메일의 정확한 사본이 아니지만 아래 단계는 최대한 가까운 메시지 작성을 안내합니다.

**컨텐츠를 복사하기 전에**

1. 원본 이메일에서 전송할 각 이메일에 고유한 섹션에서 재사용 가능한 섹션을 식별합니다.
1. 사용하려는 모든 이미지 및 자산을 저장합니다.
1. HTML에 익숙하다면 원본 HTML 컨텐츠를 다른 부분으로 분할하십시오.

### 비디오 {#video-settings}

>[!CONTEXTUALHELP]
>id="ac_edition_video"
>title="비디오 설정"
>abstract="이 구성 요소를 사용하여 이메일에 비디오를 삽입합니다. 모든 이메일 클라이언트는 비디오가 작동하지 않습니다. 대체 이미지를 설정하는 것이 좋습니다."
>additional-url="https://www.emailonacid.com/blog/article/email-development/a_how_to_guide_to_embedding_html5_video_in_email/" text="추가 정보"

비디오 구성 요소를 이메일의 구조 구성 요소에 삽입하고 비디오 링크를 **[!UICONTROL Component Settings]**.

>[!NOTE]
>
>비디오는 모든 이메일 프로그램과 호환되지 않습니다. 지원되지 않는 경우 폴백이 표시됩니다.

### 이미지

이 구성 요소를 사용하여 이메일에 이미지를 삽입합니다.

이미지 구성 요소를 구조 구성 요소에 삽입하고 찾아보기 를 클릭하여 컴퓨터에서 이미지 파일을 업로드합니다.

### **[!UICONTROL Social]**

이 구성 요소를 사용하여 이메일에 소셜 미디어 페이지에 대한 링크를 삽입합니다. 표시할 링크와 아이콘 크기를 선택할 수 있습니다 **[!UICONTROL Component Settings]**.

### 회전판 {#carousel-settings}

>[!CONTEXTUALHELP]
>id="ac_edition_carousel"
>title="회전 메뉴 설정"
>abstract="컨텐츠에 회전판을 삽입하고 구성하는 방법을 알아봅니다.회전판이 모든 이메일 클라이언트에서 작동하지 않고, 지원되지 않는 경우 대체 이미지가 표시됩니다."

1. 을(를) 끌어다 놓습니다 **[!UICONTROL Carousel]** 구성 요소를 생성하지 않습니다.
1. 컴퓨터에서 이미지를 찾아 선택합니다.

   ![](assets/des_carousel_browse.png)

1. 에서 **[!UICONTROL Settings]** 회전판에서 원하는 축소판 그림 수를 설정합니다.
1. 컴퓨터에서 대체 이미지를 선택합니다.

   ![](assets/des_carousel_fallback.png)

회전 메뉴 구성 요소는 모든 이메일 프로그램과 호환되지 않습니다. 이메일에서 회전판이 지원되지 않는 경우 이미지를 표시하려면 대체 항목을 업로드하십시오.

>[!NOTE]
>
>회전판 구성 요소는 다음 이메일 플랫폼과 호환됩니다. Apple Mail 7, Apple Mail 8, Outlook 2011 for Mac, Mac용 Outlook 2016, Mozilla Thunderbird, iPad 및 iPad mini iOS, iPhone iOS, Android, AOL(Chrome, Firefox 및 Safari).

**관련 항목**:

- [이메일 만들기](../../channels/using/creating-an-email.md)
- [메시지에서 대상자 선택](../../audiences/using/selecting-an-audience-in-a-message.md)
- [메시지 예약](../../sending/using/about-scheduling-messages.md)
- [메시지 미리 보기](../../sending/using/previewing-messages.md)
- [이메일 렌더링](../../sending/using/email-rendering.md)
