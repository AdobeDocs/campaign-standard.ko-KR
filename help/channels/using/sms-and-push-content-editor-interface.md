---
title: SMS 및 푸시 콘텐츠 편집기 인터페이스
description: 편집기의 다양한 섹션을 사용하여 SMS와 푸시 콘텐츠를 수정하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: 4af5d247-555b-45c5-95a7-cb27f356b5a0
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: editing-sms-and-push-content
discoiquuid: 4e214eb9-d299-4095-b786-8d1de9b1c8a2
context-tags: delivery,smsContent,back
internal: n
snippet: y
translation-type: ht
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e
workflow-type: ht
source-wordcount: '330'
ht-degree: 100%

---


# SMS 및 푸시 콘텐츠 편집기 인터페이스{#sms-and-push-content-editor-interface}

SMS 및 푸시 콘텐츠 편집기는 메시지를 보고 편집할 수 있는 두 개의 서로 다른 섹션으로 구성되어 있습니다.

1. **작업 모음**&#x200B;에는 페이지에 대한 일반 옵션이 포함되어 있습니다. 여기에서 개인화 필드 또는 콘텐츠 블록을 삽입하고, 조건부 텍스트를 추가하고, SMS 콘텐츠를 미리 볼 수 있습니다. [SMS 및 푸시 콘텐츠 편집기 작업 표시줄](#sms-and-push-content-editor-action-bar)을 참조하십시오.
1. 화면의 **편집 영역**&#x200B;에서 텍스트 메시지를 직접 입력하고 개인화를 삽입할 위치를 선택할 수 있습니다. [SMS 및 푸시 콘텐츠 편집 모드](#sms-and-push-content-edition-modes)를 참조하십시오.

## SMS 및 푸시 콘텐츠 편집기 작업 표시줄 {#sms-and-push-content-editor-action-bar}

작업 모음에는 만들어지는 콘텐츠와 상호 작용할 수 있는 여러 개의 버튼이 포함되어 있습니다.

<table> 
 <thead> 
  <tr> 
   <th> 아이콘<br /> </th> 
   <th> 버튼 이름<br /> </th> 
   <th> 채널<br /> </th> 
   <th> 설명<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <img height="21px" src="assets/viewon_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">미리 보기</span> <br /> </td> 
   <td> SMS만 해당<br /> </td> 
   <td> 수신자에 대해 이메일이 어떻게 렌더링되는지 볼 수 있습니다. <a href="../../sending/using/previewing-messages.md">메시지 미리 보기</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/undo_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">실행 취소</span> <br /> </td> 
   <td> SMS 및 푸시<br /> </td> 
   <td> 마지막으로 수행된 작업을 취소합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/redo_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">다시 실행</span> <br /> </td> 
   <td> SMS 및 푸시<br /> </td> 
   <td> 취소한 마지막 작업을 다시 실행합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/personalization_field_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">개인화 필드 삽입</span> <br /> </td> 
   <td> SMS 및 푸시<br /> </td> 
   <td> 데이터베이스의 필드를 콘텐츠에 추가할 수 있습니다. <a href="../../designing/using/personalization.md#inserting-a-personalization-field" target="_blank">개인화 필드 삽입</a>을 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/personalization_block_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">콘텐츠 블록 삽입</span> <br /> </td> 
   <td> SMS 및 푸시<br /> </td> 
   <td> 콘텐츠에 개인화 블록을 추가할 수 있습니다. <a href="../../designing/using/personalization.md#adding-a-content-block" target="_blank">콘텐츠 블록 추가</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/dynamiccontent_24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">다이내믹 텍스트 활성화</span> <br /> </td> 
   <td> SMS 및 푸시<br /> </td> 
   <td> 콘텐츠에 다이내믹 텍스트를 삽입할 수 있습니다. <a href="../../channels/using/defining-dynamic-text.md" target="_blank">다이내믹 텍스트 정의</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/dynamiccontentdisable_24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">다이내믹 텍스트 비활성화</span> <br /> </td> 
   <td> SMS 및 푸시<br /> </td> 
   <td> 다이내믹 텍스트를 삭제할 수 있습니다.<br /> </td> 
  </tr> 
 </tbody> 
</table>

## SMS 및 푸시 콘텐츠 편집 모드 {#sms-and-push-content-edition-modes}

SMS 및 푸시 콘텐츠 편집기는 다음과 같은 기능을 제공합니다.

* 텍스트 입력.
* 개인화 필드 추가. 자세한 내용은 [개인화 필드 삽입](../../designing/using/personalization.md#inserting-a-personalization-field)을 참조하십시오.
* 콘텐츠 블록 추가. 자세한 내용은 [콘텐츠 블록 추가](../../designing/using/personalization.md#adding-a-content-block)를 참조하십시오.
* 다이내믹 텍스트 추가. 자세한 내용은 [다이내믹 텍스트 정의](../../channels/using/defining-dynamic-text.md)를 참조하십시오.
* SMS 발신자명 개인화(SMS만 해당). 자세한 내용은 [SMS 구성](../../administration/using/configuring-sms-channel.md#configuring-sms-properties)을 참조하십시오.

