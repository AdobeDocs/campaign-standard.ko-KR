---
title: '이메일 디자인 기초 '
description: 이메일 디자이너의 이메일 컨텐츠를 처음부터 디자인하는 방법을 살펴볼 수 있습니다.
page-status-flag: never-activated
uuid: 571ffc01-6e41-4501-9094-2f812b041a10
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: editing-email-content
discoiquuid: 39b86fda-7766-4e5f-ab48-bcc536ab66b3
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '1241'
ht-degree: 2%

---


# 이메일 디자인 기초 {#designing-an-email-content-from-scratch}

이메일 컨텐츠 에디션을 마스터하는 방법을 살펴보십시오. 이메일 디자이너는 사전 정의된 컨텐츠로 시작하거나 사용하지 않고 이메일 및 템플릿을 만들 수 있습니다.

이메일 디자이너를 사용하여 이메일 컨텐츠를 처음부터 만들고 디자인하는 주요 단계는 다음과 같습니다.

1. 이메일을 만들어 내용을 엽니다.
1. 구조 구성 요소를 추가하여 이메일 모양을 만듭니다. 이메일 [구조 편집을 참조하십시오](#defining-the-email-structure).
1. 구조 구성 요소에 컨텐츠 구성 요소 및 조각을 삽입합니다. 조각 및 [컨텐츠 구성 요소 추가를 참조하십시오](#defining-the-email-structure).
1. 이미지를 추가하고 이메일 텍스트를 편집합니다. 이미지 [삽입을 참조하십시오](../../designing/using/images.md#inserting-images).
1. 개인화 필드, 링크 등을 추가하여 이메일을 개인화합니다. 개인화 필드 [삽입](../../designing/using/personalization.md#inserting-a-personalization-field), 링크 [삽입 및](../../designing/using/links.md#inserting-a-link) 이메일에 동적 컨텐트 [정의를 참조하십시오](../../designing/using/personalization.md#defining-dynamic-content-in-an-email).
1. 이메일의 제목 줄을 정의합니다. See [Personalizing the subject line of an email](../../designing/using/subject-line.md#defining-the-subject-line-of-an-email).
1. 이메일 미리 보기.
1. 컨텐츠를 저장하고 대상을 정의하고 전송을 올바르게 예약했는지 확인한 후 메시지를 계속 진행합니다.

이 [소개 비디오도 확인할 수 있습니다](https://video.tv.adobe.com/v/22771/?autoplay=true&hidetitle=true&captions=kor).

>[!NOTE]
>
>이메일 컨텐츠를 처음부터 디자인하지 않으려면 바로 사용 가능한 컨텐츠 템플릿을 사용할 수 있습니다. 자세한 내용은 [컨텐츠 템플릿을 참조하십시오](../../designing/using/using-reusable-content.md#content-templates).

## 이메일 구조 정의 {#defining-the-email-structure}

>[!CONTEXTUALHELP]
>id="ac_structure_components"
>title="구조 구성 요소 정보"
>abstract="구조 구성 요소는 이메일의 레이아웃을 정의합니다."

>[!CONTEXTUALHELP]
>id="ac_edition_columns"
>title="이메일 열 정의"
>abstract="이메일 디자이너를 사용하면 열 구조를 정의하여 이메일의 레이아웃을 쉽게 정의할 수 있습니다."

이메일 디자이너는 이메일의 구조를 쉽게 정의할 수 있도록 해줍니다. 간단한 드래그 앤 드롭 동작으로 구조적 요소를 추가하고 이동하여 몇 초 안에 이메일 모양을 디자인할 수 있습니다.

이메일 구조를 편집하려면:

1. 기존 컨텐츠를 열거나 새 이메일 컨텐츠를 만듭니다.
1. 왼쪽에 있는 **[!UICONTROL Structure components]** + **아이콘을 선택하여** 에액세스합니다.

   ![](assets/email_designer_structure.png)

1. 이메일을 구성하는 데 필요한 구조 구성 요소를 드래그하여 놓습니다.

   ![](assets/email_designer_structure_components.png)

   파란색 선은 구조 구성 요소를 놓치기 전에 정확한 위치를 재구성합니다. 위에, 다른 구성 요소 사이 또는 아래에 놓을 수 있지만 내부에 놓을 수는 없습니다.

   >[!NOTE]
   >
   >열 스택은 일부 이메일 프로그램과 호환되지 않습니다. 지원되지 않는 열은 스택되지 않습니다.
   >
   >이메일에 배치하면 이미 컨텐츠 구성 요소나 안에 배치된 조각이 없는 한 구성 요소를 이동하거나 제거할 수 없습니다.

1. 하나 이상의 열로 구성된 여러 구조 구성 요소를 사용할 수 있습니다.

   구성 요소를 **[!UICONTROL n:n column]** 선택하여 선택한 열 수(3과 10 사이)를 정의합니다. 각 열 아래쪽에서 화살표를 이동하여 각 열의 너비를 정의할 수도 있습니다.

   ![](assets/email_designer_n-n-column.png)

   >[!NOTE]
   >
   >각 열 크기는 구조 구성 요소의 전체 너비의 10% 미만일 수 없습니다. 비어 있지 않은 열은 제거할 수 없습니다.

구조를 정의하면 컨텐츠 조각 및 구성 요소를 이메일에 추가할 수 있습니다.

## 프리헤더 사용 {#preheader}

>[!CONTEXTUALHELP]
>id="ac_edition_preheader"
>title="프리헤더 사용"
>abstract="사전 헤더를 사용하면 짧은 요약 텍스트를 구성하여 이메일의 공개 비율을 높일 수 있습니다."

사전 헤더는 받은 편지함에서 이메일을 볼 때 제목 줄 뒤에 오는 간단한 요약 텍스트입니다. 프리헤더는 더 높은 공개 비율을 제공합니다.

편집 상자를 **[!UICONTROL Preheader]** 선택하고 컨텐츠를 완료합니다.

![](assets/email_designer_preheader.png)

사전 헤더 컨텐츠 **[!UICONTROL Content block]**&#x200B;에 하나 **[!UICONTROL Dynamic content]** 또는 **[!UICONTROL Personalization fields]** 를 추가할 수 있습니다.

>[!NOTE]
>
>사전 헤더는 모든 이메일 프로그램과 호환되지 않습니다. 지원되지 않는 경우 미리 머리글이 표시되지 않습니다.


## 컨텐츠 구성 요소 사용 {#about-content-components}

>[!CONTEXTUALHELP]
>id="ac_content_components"
>title="컨텐츠 구성 요소 정보"
>abstract="컨텐츠 구성 요소는 이메일을 만들기 위해 편집할 수 있는 빈 컨텐츠 자리 표시자입니다."

컨텐츠 구성 요소는 원시 빈 구성 요소로서, 한 번 이메일에 배치되면 편집할 수 있습니다.

구조 구성 요소에서 원하는 만큼 컨텐츠 구성 요소를 추가할 수 있습니다. 구조 구성 요소 안이나 다른 구조 구성 요소로 이동할 수도 있습니다.

이메일 디자이너의 사용 가능한 구성 요소 목록은 다음과 같습니다.

### **[!UICONTROL Button]**

각 단추를 처음부터 편집하지 않고 여러 단추를 사용해야 하는 경우 컨텍스트 도구 모음을 사용하여 구성 **[!UICONTROL Button]** 요소를 복제할 수 있습니다.

단추를 다시 사용할 수 있는 조각으로 저장할 수도 있습니다. 자세한 내용은 컨텐츠 조각 [만들기](../../designing/using/using-reusable-content.md#creating-a-content-fragment) 및 컨텐츠 [를 조각으로 저장을 참조하십시오](../../designing/using/using-reusable-content.md#saving-content-as-a-fragment).

이메일 디자이너 **[!UICONTROL Fallback view]** 에 대체 이미지를 표시하려면 선택합니다.

### **[!UICONTROL Text]**

    이 구성 요소를 사용하여 이메일에 텍스트를 삽입합니다. **[!UICONTROL Component Settings]**에서 텍스트의 색상, 스타일 및 크기를 조정할 수 있습니다.

### **[!UICONTROL Divider]**

    이 구성 요소를 사용하여 이메일에 분할된 줄을 삽입합니다. **[!UICONTROL Component Settings]**에서 줄바꿈 줄의 색상, 스타일 및 크기를 선택할 수 있습니다.

### **[!UICONTROL Html]**

이 구성 요소를 사용하여 기존 HTML의 다른 부분을 복사하여 붙여넣습니다. 이를 통해 무료 모듈식 HTML 구성 요소를 만들 수 있습니다.

>[!NOTE]
>
>무료 HTML 구성 요소는 제한된 옵션으로 편집할 수 있습니다. 모든 스타일이 인라인되지 않은 경우 HTML 코드의 **헤드** 섹션에 올바른 CSS를 추가해야 이메일이 응답성이 적용되지 않습니다. 이 **[!UICONTROL Preview]** 단추를 사용하여 컨텐츠의 응답성을 테스트합니다(메시지 [미리 보기 참조](../../sending/using/previewing-messages.md)).

간단하게 이메일 디자이너와 호환되는 외부 컨텐츠를 만들려면 메시지를 처음부터 만들고 기존 이메일의 내용을 조각 및 구성 요소로 복사하는 것이 좋습니다.

다시 만들 수 없는 컨텐츠가 있는 경우 컨텐츠 구성 요소를 사용하여 원본 이메일의 HTML 코드를 복사하여 붙여넣을 수 **[!UICONTROL Html]** 있습니다. 계속하기 전에 HTML에 익숙해야 합니다.

<!-- A full example is presented below. -->

>[!NOTE]
>
>새 컨텐츠는 원본 이메일의 정확한 사본이 되지는 않지만, 아래 단계는 가능한 한 가까운 메시지 작성을 안내해 줍니다.

    **컨텐츠를 복사하기 전에**
    
    1. 원본 이메일에서 전송할 각 이메일에 대해 고유한 섹션에서 재사용 가능한 섹션을 확인합니다.
    1. 사용할 모든 이미지 및 에셋을 저장합니다.
    1. HTML에 익숙한 경우 원본 HTML 내용을 다른 부분으로 분할합니다.

### 비디오 {#video-settings}

>[!CONTEXTUALHELP]
>id="ac_edition_video"
>title="비디오 설정"
>abstract="이 구성 요소를 사용하여 이메일에 비디오를 삽입합니다. 일부 이메일 클라이언트에서 비디오가 작동하지 않습니다. 대체 이미지를 설정하는 것이 좋습니다."
>additional-url="https://www.emailonacid.com/blog/article/email-development/a_how_to_guide_to_embedding_html5_video_in_email/" text="추가 정보"


비디오 구성 요소를 이메일의 구조 구성 요소에 삽입하고 에 비디오 링크를 입력합니다 **[!UICONTROL Component Settings]**.

>[!NOTE]
>
>비디오는 일부 이메일 프로그램과 호환되지 않습니다. 지원되지 않는 경우 폴백이 표시됩니다.

### 이미지

이 구성 요소를 사용하여 이메일에 이미지를 삽입합니다.

이미지 구성 요소를 구조 구성 요소에 삽입하고 찾아보기를 클릭하여 컴퓨터에서 이미지 파일을 업로드합니다.

### **[!UICONTROL Social]**

이 구성 요소를 사용하여 이메일에 소셜 미디어 페이지에 대한 링크를 삽입합니다. 표시할 링크와 해당 아이콘의 크기를 선택할 수 있습니다 **[!UICONTROL Component Settings]**.

### 회전판 {#carousel-settings}

>[!CONTEXTUALHELP]
>id="ac_edition_carousel"
>title="회전판 설정"
>abstract="컨텐츠에 회전판을 삽입하고 구성하는 방법에 대해 학습합니다.일부 이메일 클라이언트에서 회전판을 사용할 수 없으며 지원되지 않는 경우에 대비한 이미지가 표시됩니다."

1. 구성 요소를 구조 구성 요소 안에 **[!UICONTROL Carousel]** 드래그하여 놓습니다.
1. 컴퓨터에서 이미지를 찾아 선택합니다.

   ![](assets/des_carousel_browse.png)

1. 회전판에서 원하는 축소판 수를 **[!UICONTROL Settings]** 설정합니다.
1. 컴퓨터에서 대체 이미지를 선택합니다.

   ![](assets/des_carousel_fallback.png)

회전판 구성 요소는 일부 이메일 프로그램과 호환되지 않습니다. 회전판이 이메일에서 지원되지 않는 경우 대신 이미지를 표시하는 대비책을 업로드합니다.

>[!NOTE]
>
>회전판 구성 요소는 다음 이메일 플랫폼과 호환됩니다.Apple Mail 7, Apple Mail 8, Mac용 Outlook 2011, Mac용 Outlook 2016, Mozilla Thunderbird, iPad 및 iPad mini iOS, iPhone iOS, Android, AOL(Chrome, Firefox 및 Safari).

**관련 항목**:

- [전자 메일 만들기](../../channels/using/creating-an-email.md)
- [메시지에서 대상자 선택](../../audiences/using/selecting-an-audience-in-a-message.md)
- [메시지 예약](../../sending/using/about-scheduling-messages.md)
- [메시지 미리 보기](../../sending/using/previewing-messages.md)
- [이메일 렌더링](../../sending/using/email-rendering.md)
