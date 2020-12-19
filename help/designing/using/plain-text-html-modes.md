---
solution: Campaign Standard
product: campaign
title: 일반 텍스트, HTML 및 모바일 이메일 포맷 편집
description: 일반 텍스트 및 HTML 모드 살펴보기
audience: designing
content-type: reference
topic-tags: editing-email-content
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '776'
ht-degree: 0%

---


# 일반 텍스트, HTML 및 모바일 이메일 형식 편집 {#plain-text-and-html-modes}

이메일 디자이너를 사용하면 여러 이메일 렌더링을 편집할 수 있습니다. 이메일의 텍스트 버전을 생성하고, 이메일의 HTML 소스를 편집하고, 모바일 보기용 이메일을 디자인할 수 있습니다.

## {#generating-a-text-version-of-the-email} 이메일의 텍스트 버전 생성

기본적으로 **[!UICONTROL Plain text]** 버전의 이메일은 자동으로 생성되고 **[!UICONTROL Edit]** 버전과 동기화됩니다.

HTML 버전에 추가된 개인화 필드 및 컨텐츠 블록도 일반 텍스트 버전과 동기화됩니다.

>[!NOTE]
>
>일반 텍스트 버전에서 내용 블록을 사용하려면 HTML 코드가 포함되어 있지 않아야 합니다.

HTML 버전과 다른 일반 텍스트 버전을 사용하려면 전자 메일의 **[!UICONTROL Plain text]** 보기에서 **[!UICONTROL Sync with HTML]** 스위치를 클릭하여 이 동기화를 비활성화할 수 있습니다.

![](assets/email_designer_textversion.png)

그런 다음 원하는 대로 일반 텍스트 버전을 편집할 수 있습니다.

>[!NOTE]
>
>동기화가 비활성화되어 있는 동안 **[!UICONTROL Plain text]** 버전을 편집하는 경우 다음에 **[!UICONTROL Sync with HTML]** 옵션을 활성화하면 일반 텍스트 버전에서 변경한 모든 내용이 HTML 버전으로 대체됩니다. **[!UICONTROL Plain text]** 보기에서 변경한 내용은 **[!UICONTROL HTML]** 보기에 반영될 수 없습니다.

## HTML {#editing-an-email-content-source-in-html}에서 이메일 컨텐츠 소스 편집

고급 사용자 및 디버깅의 경우 HTML에서 바로 이메일 컨텐츠를 보고 편집할 수 있습니다.

이메일의 HTML 버전을 편집하는 방법은 다음과 같습니다.

* 전체 이메일의 HTML 버전을 열려면 **[!UICONTROL Edit]** > **[!UICONTROL HTML]**&#x200B;을 선택합니다.

   ![](assets/email_designer_html1.png)

* WYSIWYG 인터페이스에서 요소를 선택하고 **[!UICONTROL Source code]** 아이콘을 클릭합니다.

   선택한 요소의 소스만 표시됩니다. 선택한 요소가 **[!UICONTROL HTML]** 컨텐츠 구성 요소인 경우 소스 코드를 편집할 수 있습니다. 다른 구성 요소는 읽기 전용 모드이지만 이메일의 전체 HTML 버전에서 계속 편집할 수 있습니다.

   ![](assets/email_designer_html2.png)

HTML을 수정하면 이메일의 응답성이 끊어질 수 있습니다. **[!UICONTROL Preview]** 단추를 사용하여 테스트해야 합니다. [메시지 미리 보기](../../sending/using/previewing-messages.md)를 참조하십시오.

## 모바일 렌더링을 위한 이메일 디자인 {#switching-to-mobile-view}

모바일용 모든 스타일 옵션을 개별적으로 편집하여 이메일의 반응형 디자인을 세밀하게 조정할 수 있습니다. 예를 들어, 여백과 패딩을 조정하고, 더 작거나 큰 글꼴 크기를 사용하거나, 버튼을 변경하거나, 이메일의 모바일 버전에 맞는 다른 배경색을 적용할 수 있습니다.

모든 스타일 옵션은 모바일 보기에서 사용할 수 있습니다. 이메일 디자이너 스타일 설정이 이 페이지 앞에 표시됩니다.

1. 이메일을 만들고 컨텐츠 편집을 시작합니다. 자세한 내용은 [처음부터 이메일 컨텐츠 디자인](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch)을 참조하십시오.
1. 전용 모바일 보기에 액세스하려면 **[!UICONTROL Switch to mobile view]** 단추를 선택합니다.

   ![](assets/email_designer_mobile_view_switch.png)

   이메일의 모바일 버전이 표시됩니다. 여기에는 데스크톱 보기에 정의된 모든 구성 요소 및 스타일이 포함되어 있습니다.

1. 배경색, 정렬, 패딩, 여백, 글꼴 모음, 텍스트 색상 등 모든 스타일 설정을 개별적으로 편집할 수 있습니다.

   ![](assets/email_designer_mobile_view.png)

1. 모바일 보기에서 스타일 설정을 편집할 때 수정 내용은 모바일 디스플레이에만 적용됩니다.

   예를 들어 이미지 크기를 줄이고 녹색 배경을 추가하고 모바일 보기에서 패딩을 변경합니다.

   ![](assets/email_designer_mobile_view_change.png)

1. 모바일 장치에 표시될 때 구성 요소를 숨길 수 있습니다. 이렇게 하려면 **[!UICONTROL Display options]**&#x200B;에서 **[!UICONTROL Show only on desktop devices]**&#x200B;을 선택합니다.

   데스크톱 장치에서 이 구성 요소를 숨기도록 선택할 수도 있습니다. 즉, 모바일 장치에만 표시됩니다. 이렇게 하려면 **[!UICONTROL Show only on mobile devices]**&#x200B;을 선택합니다.

   예를 들어, 이 옵션을 사용하면 모바일 장치에 특정 이미지를 표시하고 데스크톱 장치에 다른 이미지를 표시할 수 있습니다.

   모바일 또는 데스크탑 보기에서 이 옵션을 설정할 수 있습니다.

   ![](assets/email_designer_mobile_hide.png)

1. **[!UICONTROL Switch to mobile view]** 단추를 다시 클릭하여 표준 데스크톱 보기로 돌아갑니다. 방금 변경한 스타일이 반영되지 않습니다.

   ![](assets/email_designer_mobile_view_desktop_no-change.png)

   >[!NOTE]
   >
   >유일한 예외는 **[!UICONTROL Style inline]** 설정입니다. 스타일 인라인 설정 변경 사항은 표준 데스크톱 보기에도 적용됩니다.

1. 텍스트 편집, 새 이미지 업로드, 새 구성 요소 추가 등 이메일의 구조 또는 컨텐트에 대한 기타 변경 사항 는 표준 뷰에도 적용됩니다.

   예를 들어 모바일 보기로 돌아가 텍스트를 편집하고 이미지를 바꿀 수 있습니다.

   ![](assets/email_designer_mobile_view_change_content.png)

1. **[!UICONTROL Switch to mobile view]** 단추를 다시 클릭하여 표준 데스크톱 보기로 돌아갑니다. 변경 사항이 반영됩니다.

   ![](assets/email_designer_mobile_view_desktop_content-change.png)

1. 모바일 보기에서 스타일을 제거하면 데스크톱 모드에서 적용된 스타일로 돌아갑니다.

   예를 들어 모바일 보기에서 단추에 녹색 배경색을 적용합니다.

   ![](assets/email_designer_mobile_view_background_mobile.png)

1. 데스크탑 보기로 전환하고 동일한 단추에 회색 배경을 적용합니다.

   ![](assets/email_designer_mobile_view_background_desktop.png)

1. 모바일 보기로 다시 전환한 다음 **[!UICONTROL Background color]** 설정을 비활성화합니다.

   ![](assets/email_designer_mobile_view_background_mobile_disabled.png)

   이제 데스크톱 보기에 정의된 배경색이 적용됩니다.회색으로 바뀝니다(비어 있지 않음).

   유일한 예외는 **[!UICONTROL Border color]** 설정입니다. 모바일 보기에서 비활성화하면 데스크톱 보기에 테두리 색상이 정의되어 있어도 테두리가 더 이상 적용되지 않습니다.

>[!NOTE]
>
>모바일 보기는 [fragments](../../designing/using/using-reusable-content.md#about-fragments)에서 사용할 수 없습니다.
