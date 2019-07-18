---
title: 랜딩 페이지 컨텐츠 편집기 인터페이스
seo-title: 랜딩 페이지 컨텐츠 편집기 인터페이스
description: 랜딩 페이지 컨텐츠 편집기 인터페이스
seo-description: 작업 표시기와 같이 편집기의 다양한 섹션을 사용하여 랜딩 페이지 컨텐츠를 수정하는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: 53729 a 68-EED 2-4 c 5 d-bc 14-02 c 80 e 897 c 44
contentOwner: Sauviat
products: sg_ campaign/standard
audience: designing
content-type: 참조
topic-tags: editing-landing-page-content
discoiquuid: 08 E 2 BBDA-E 409-467 F-B 462-D 74256 DC 6 EBC
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 76c3d473f6cc7e825fdabadeec2405cb5c13abd1

---


# Landing page content editor interface{#landing-page-content-editor-interface}

랜딩 페이지 컨텐츠 편집기를 사용하면 Adobe Campaign에서 컨텐츠를 쉽게 정의, 수정 및 개인화할 수 있습니다. To access it, click the **[!UICONTROL Content]** block in a landing page dashboard.

컨텐츠 편집기는 세 개의 서로 다른 섹션으로 구성됩니다. 이러한 섹션에서는 컨텐츠를 보고 편집할 수 있습니다.

![](assets/des_lp_content_8.png)

1. The **palette** on the left-hand side of the screen allows you to modify the general options linked to a selected block. 수정할 수 있는 옵션은 다음과 같습니다. 배경색, 테두리, 텍스트 정렬, 가시성 조건 등 See [Inserting a personalization field](../../designing/using/inserting-a-personalization-field.md).
1. **작업 모음에는** 페이지에 대한 일반 옵션이 포함되어 있습니다. 템플릿을 선택하고 표시 모드를 변경할 수 있습니다. [랜딩 페이지 편집기 작업 막대를 참조하십시오](../../designing/using/landing-page-content-editor-interface.md#landing-page-editor-action-bar).
1. The main **editing zone** allows you to directly interact with the content using the contextual toolbar: insert a link into an image, change the font, delete a field, etc. [랜딩 페이지 편집기 도구 모음을 참조하십시오](../../designing/using/landing-page-content-editor-interface.md#landing-page-editor-toolbar).

## Landing page editor action bar {#landing-page-editor-action-bar}

작업 모음에는 만들어지는 내용과 상호 작용할 수 있는 여러 버튼이 포함되어 있습니다.

![](assets/des_lp_content_9.png)

<table> 
 <thead> 
  <tr> 
   <th> Icon<br /> </th> 
   <th> Button name<br /> </th> 
   <th> Channel<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <img height="21px" src="assets/download_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">콘텐트 변경</span><br /> </td> 
   <td> Landing page and email<br /> </td> 
   <td> 즉시 사용 가능한 컨텐츠를 선택하거나 직접 HTML 콘텐츠를 가져올 수 있습니다. Refer to <a href="../../designing/using/selecting-an-existing-content.md">Loading an existing content</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/undo_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">실행 취소</span><br /> </td> 
   <td> All<br /> </td> 
   <td> Cancels the last action carried out.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/redo_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">재실행</span><br /> </td> 
   <td> All<br /> </td> 
   <td> Redoes the last action that you canceled.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/display_block_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">블록 표시</span><br /> </td> 
   <td> Landing page and email<br /> </td> 
   <td> Allows you to show the boxes around the content blocks (corresponds to the <strong>&lt;div&gt;</strong> HTML tag).<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/code_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">소스 표시</span><br /> </td> 
   <td> Landing page and email<br /> </td> 
   <td> Allows you to show the HTML source code of the page.<br /> </td> 
  </tr> 
 </tbody> 
</table>

## Landing page editor toolbar {#landing-page-editor-toolbar}

The toolbar is a **contextual element** of the editor interface that offers various functionalities depending on the zone selected. 여기에는 텍스트 스타일을 변경할 수 있는 작업 단추와 단추가 포함되어 있습니다. 수행된 수정 사항은 선택한 영역에 항상 적용됩니다. 블록을 선택하고 나면 이 블록을 삭제하거나 복제할 수 있습니다. 블록 내에서 텍스트를 선택한 다음 링크로 변환하거나 굵게 만들 수 있습니다.

![](assets/delivery_content_17.png)

>[!CAUTION]
>
>특정 도구 모음 기능을 사용하여 HTML 콘텐츠의 서식을 지정할 수 있습니다. However, if the page contains a CSS style sheet, the **instructions** from the style sheet may prove to take **priority** over the instructions specified via the toolbar.

<table> 
 <thead> 
  <tr> 
   <th> Icon<br /> </th> 
   <th> Button name<br /> </th> 
   <th> Context<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <img height="21px" src="assets/link_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">외부 URL에 연결</span><br /> </td> 
   <td> Any element<br /> </td> 
   <td> URL에 링크를 추가할 수 있습니다. Details of how to configure a link are presented in the <a href="../../designing/using/inserting-a-link.md">Inserting a link</a> section.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/linkpage_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">랜딩 페이지에 연결</span><br /> </td> 
   <td> Any element<br /> </td> 
   <td> Adobe Campaign 랜딩 페이지에 액세스할 수 있습니다. Details of how to configure a link are presented in the <a href="../../designing/using/inserting-a-link.md">Inserting a link</a> section.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/link_subscribe_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">구독 링크</span><br /> </td> 
   <td> Any element<br /> </td> 
   <td> 서비스 구독 링크를 삽입할 수 있습니다. Details of how to configure a link are presented in the <a href="../../designing/using/inserting-a-link.md">Inserting a link</a> section.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/link_unsubscribe_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">구독 취소 링크</span><br /> </td> 
   <td> Any element<br /> </td> 
   <td> 서비스 구독 취소 링크를 삽입할 수 있습니다. Details of how to configure a link are presented in the <a href="../../designing/using/inserting-a-link.md">Inserting a link</a> section.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/linkoff_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">링크 제거</span><br /> </td> 
   <td> Link<br /> </td> 
   <td> Allows you to delete the link, as well as all the configurations linked to it, after confirming.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/personalization_field_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">개인화 필드 삽입</span><br /> </td> 
   <td> Text element<br /> </td> 
   <td> 데이터베이스의 필드를 컨텐츠에 추가할 수 있습니다. Refer to <a href="../../designing/using/inserting-a-personalization-field.md">Inserting a personalization field</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/personalization_block_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">컨텐츠 블록 삽입</span><br /> </td> 
   <td> Text element<br /> </td> 
   <td> 컨텐츠에 개인화 블록을 추가할 수 있습니다. Refer to <a href="../../designing/using/adding-a-content-block.md">Adding a content block</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/dynamiccontent_24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">동적 컨텐츠 활성화</span><br /> </td> 
   <td> Text element<br /> </td> 
   <td> 컨텐츠에 동적 컨텐트를 삽입할 수 있습니다. Refer to <a href="../../designing/using/defining-dynamic-content-in-a-landing-page.md">Defining dynamic content</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/dynamiccontentdisable_24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">동적 컨텐츠 비활성화</span><br /> </td> 
   <td> Text element<br /> </td> 
   <td> Allows you to delete dynamic content.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/increase_fontsize_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">글꼴 확대</span><br /> </td> 
   <td> Text element<br /> </td> 
   <td> Increases the size of the selected text (adds <strong>&lt;span style="font-size:"&gt;</strong>).<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/decrease_fontsize_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">글꼴 축소</span><br /> </td> 
   <td> Text element<br /> </td> 
   <td> Reduces the size of the selected text (adds <strong>&lt;span style="font-size:"&gt;</strong>).<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/textbold_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">bold</span><br /> </td> 
   <td> Text element<br /> </td> 
   <td> Adds the bold style to the selected text (wraps the text with the <strong>&lt;strong&gt;</strong><strong>&lt;/strong&gt;</strong> tags).<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/textitalic_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">italic</span><br /> </td> 
   <td> Text element<br /> </td> 
   <td> Adds the italic style to the selected text (wraps the text with the <strong>&lt;em&gt;</strong><strong>&lt;/em&gt;</strong> tags).<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/textunderline_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">underline</span><br /> </td> 
   <td> Text element<br /> </td> 
   <td> Underlines the selected text (wraps the selected text with the <strong>&lt;span style="text-decoration: underline;"&gt;</strong> tag).<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/colorselector_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">배경색 변경</span><br /> </td> 
   <td> Text element<br /> </td> 
   <td> Allows you to change the background color of the block selected (adds style="background-color: rgba(170, 86, 255, 0.87)).<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/textcolor_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">글꼴 색상 변경</span><br /> </td> 
   <td> Text element<br /> </td> 
   <td> Allows you to change the color of all the text in the block or just the text selected in the block (<strong>&lt;span style="color: #56ff56;"&gt;</strong>).<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/image_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">이미지</span><br /> </td> 
   <td> Block containing an image<br /> </td> 
   <td> Allows you to insert an image from a file saved locally.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/delete_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">delete</span><br /> </td> 
   <td> Any block<br /> </td> 
   <td> Deletes the block and its content.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/duplicate_fontsize_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">복제</span><br /> </td> 
   <td> Any block<br /> </td> 
   <td> Duplicates the block including any styles linked to it.<br /> </td> 
  </tr> 
 </tbody> 
</table>

