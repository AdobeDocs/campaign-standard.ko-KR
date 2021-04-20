---
solution: Campaign Standard
product: campaign
title: '기존 콘텐츠를 사용한 이메일 디자인 '
description: 이메일 디자이너의 기존 컨텐츠 이메일 컨텐츠를 사용하여 이메일을 디자인하는 방법을 살펴볼 수 있습니다.
audience: designing
content-type: reference
topic-tags: editing-email-content
feature: Email Design
role: Business Practitioner
level: Intermediate
translation-type: tm+mt
source-git-commit: 088b49931ee5047fa6b949813ba17654b1e10d60
workflow-type: tm+mt
source-wordcount: '1217'
ht-degree: 5%

---

# 기존 컨텐츠 {#designing-using-existing-content}을(를) 사용하여 디자인

## 기존 내용 선택{#selecting-an-existing-content}

Adobe Campaign에는 시작할 수 있도록 미리 정의된 컨텐츠 세트가 포함되어 있습니다. 이러한 메시지 중 하나를 사용하거나, Adobe Campaign 외부에서 전송해야 할 메시지 내용을 준비하는 경우 컴퓨터 또는 URL에서 가져올 수 있습니다.

이메일 또는 랜딩 페이지를 만들 때 다른 소스에서 기존 컨텐츠를 로드하도록 선택할 수 있습니다.

>[!NOTE]
>
>아래 이미지는 [이메일 디자이너](../../designing/using/designing-content-in-adobe-campaign.md)를 사용하여 기존 컨텐츠를 로드하는 방법을 보여줍니다.

1. 이메일 또는 랜딩 페이지를 만든 후 해당 컨텐츠를 엽니다.
1. 홈 아이콘을 클릭하여 **[!UICONTROL Email Designer]** 홈 페이지에 액세스합니다.

   ![](assets/des_loading_1.png)

1. 로드할 컨텐츠의 소스를 선택합니다.

   * [컨텐츠 템플릿](../../designing/using/using-reusable-content.md#content-templates):탭을  **[!UICONTROL Templates]** 클릭합니다.
   * [처음부터](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch) 새로 시작하는 컨텐츠:단추를  **[!UICONTROL Create]** 클릭합니다.
   * [컴퓨터의 콘텐트를 ZIP 또는 HTML 파일로 저장](#importing-content-from-a-file):단추를  **[!UICONTROL Upload]** 클릭합니다.
   * [기존 URL의 컨텐츠](#importing-content-from-a-url) (이메일만 해당):단추를  **[!UICONTROL Import from URL]** 클릭합니다.

   ![](assets/des_loading_2.png)

1. 컨텐츠를 로드합니다. 선택한 컨텐츠가 현재 컨텐츠를 대체합니다.

   컨텐츠를 가져온 후에는 편집하고 개인화할 수 있습니다.

   >[!NOTE]
   >
   >[이메일 디자이너](../../designing/using/designing-content-in-adobe-campaign.md)는 특정 태깅을 사용합니다. Campaign에 업로드된 표준 HTML 컨텐츠는 예상 태깅과 일치해야 이메일 디자이너의 호환 및 편집 가능해야 합니다. 일치하지 않으면 내용이 [호환성 모드](#compatibility-mode)에 업로드됩니다. 기존 콘텐트가 호환되도록 하려면 [이 섹션](#editing-existing-contents-with-the-email-designer)을 참조하십시오.

**관련 항목:**

* [이메일 만들기](../../channels/using/creating-an-email.md)
* [랜딩 페이지 관리](../../channels/using/getting-started-with-landing-pages.md)

## 이메일 디자이너를 사용하여 기존 컨텐츠 편집{#editing-existing-contents-with-the-email-designer}

[이메일 디자이너](../../designing/using/designing-content-in-adobe-campaign.md)의 에디션 가능성을 완전히 활용하려면 업로드한 HTML에 WYSIWYG 편집기와 호환되도록 특정 태그가 포함되어야 합니다.

HTML의 전체 또는 일부에 이러한 태깅이 없는 경우 컨텐츠가 &#39; [호환성 모드](#compatibility-mode)&#39;로 로드됩니다.

이메일 디자이너 내에서 기존 외부 컨텐츠를 완전히 편집 가능하도록 하려면 기존 컨텐츠](../../designing/using/using-existing-content.md) 섹션을 사용하여 이메일 디자인 섹션을 참조하십시오.[

## 기존 전자 메일 내용 {#importing} 가져오기

### {#importing-content-from-a-file} 파일에서 콘텐트 가져오기

이메일 디자이너 홈 페이지에서 **[!UICONTROL Upload]** 단추를 클릭하여 컴퓨터에서 파일을 업로드한 다음 확인합니다.

zip 파일 구조에 제한이 없습니다. 그러나 HTML 파일을 참조하려면 상대 파일이어야 하며 zip 폴더의 트리 구조를 준수해야 합니다.

가져올 수 있는 형식은 다음과 같습니다.

* 스타일 시트가 포함된 HTML 파일
* HTML 파일, 스타일 시트(.CSS) 및 이미지가 포함된 .zip 폴더

>[!NOTE]
>
>이메일 컨텐츠의 경우 스타일 시트가 포함된 단일 HTML 파일을 가져오는 것이 좋습니다.

#### URL {#importing-content-from-a-url}에서 콘텐트 가져오기

URL에서 컨텐츠를 가져오기 전에 아래 요구 사항을 따라야 합니다.

* 이 URL을 통해 컨텐츠를 공개적으로 사용할 수 있어야 합니다.
* 보안상의 이유로 **[!UICONTROL https]**&#x200B;으로 시작하는 URL만 허용됩니다.
* 모든 리소스(이미지, CSS)가 절대 링크 및 HTTPS로 설정되어 있는지 확인합니다. 그렇지 않으면 이메일을 보낸 후 미러 페이지가 리소스 없이 표시됩니다. 다음은 절대 링크 정의의 예입니다.

   ```
   <a href="https://www.mywebsite.com/images/myimage.png">
   ```

>[!NOTE]
>
>URL에서 컨텐츠를 로드하는 것은 이메일 채널에만 사용할 수 있습니다.

URL에서 기존 컨텐츠를 검색하려면 아래 단계를 따르십시오.

1. 이메일 디자이너 홈 페이지에서 **[!UICONTROL Import from URL]** 단추를 선택합니다.

   ![](assets/email_designer_importfromurl.png)

1. 콘텐트를 검색할 URL을 정의합니다.
1. **[!UICONTROL Confirm]**&#x200B;을(를) 클릭합니다.

비디오에서 이 기능 살펴보기.

>[!VIDEO](https://video.tv.adobe.com/v/25926?quality=12)

추가 Campaign Standard 방법 비디오는 [여기](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/overview.html?lang=ko)에서 사용할 수 있습니다.

### 준비 시 {#retrieving-content-from-a-url-automatically-at-preparation-time} URL에서 자동으로 컨텐츠 검색

메시지 준비 중에 URL에서 컨텐츠를 가져오면 이메일이 준비될 때마다 최신 HTML 컨텐츠를 검색할 수 있습니다. 이렇게 하면 되풀이되는 이메일의 컨텐츠가 전송 시 항상 최신 상태로 유지됩니다. 이 기능을 사용하면 컨텐츠가 아직 준비되지 않은 경우에도 특정 날짜에 예약된 메시지를 만들 수도 있습니다.

준비 시 컨텐츠를 검색하려면 아래 단계를 따르십시오.

1. **[!UICONTROL Content imported during preparation]** 옵션을 선택합니다.

   ![](assets/email_designer_importfromurl2.png)

1. URL 컨텐츠는 편집기에 읽기 전용으로 표시됩니다.

   >[!CAUTION]
   >
   >이 단계에서는 컨텐츠 편집기의 HTML 표시를 고려해서는 안 됩니다. 준비 단계에서 검색됩니다.

1. 검색된 URL 내용을 미리 보려면 메시지를 만든 후 **[!UICONTROL Preview]** 단추를 클릭합니다.

콘텐트를 검색할 원격 URL을 개인화할 수 있습니다. 이렇게 하려면 아래 단계를 수행합니다:

1. 화면 상단에 있는 이메일 레이블을 클릭하여 이메일 디자이너 **[!UICONTROL Properties]** 탭에 액세스합니다.
1. **[!UICONTROL Remote URL]** 필드를 찾습니다.

   ![](assets/email_designer_importfromurl4.png)

1. 원하는 개인화 필드, 컨텐츠 블록 또는 동적 텍스트를 삽입합니다.

   예를 들어, **[!UICONTROL Current date - YYYYMMDD]** 내용 블록을 사용하면 날짜를 삽입할 수 있습니다.

   >[!NOTE]
   >
   >사용 가능한 개인화 필드는 **게재** 속성에만 연결됩니다(이메일 생성 날짜, 상태, 캠페인 레이블...).

### 호환성 모드 {#compatibility-mode}

컨텐츠를 업로드할 때 이메일 디자이너의 WYSIWYG 편집기와 완벽하게 호환되고 편집할 수 있도록 특정 태깅을 포함해야 합니다.

업로드된 HTML의 전체 또는 일부가 예상 태깅과 일치하지 않는 경우 컨텐츠가 &#39;호환성 모드&#39;로 로드되므로 UI를 통해 버전 가능성을 제한합니다.

호환성 모드에서 컨텐츠를 로드할 때 인터페이스를 통해 다음 수정 작업을 수행할 수 있습니다(사용할 수 없는 작업은 숨겨짐).

* 텍스트 변경 또는 이미지 변경
* 링크 및 개인화 필드 삽입
* 선택한 HTML 블록에서 일부 스타일 옵션 편집
* 조건부 컨텐츠 정의

![](assets/email_designer_compatibility.png)

이메일에 새 섹션 추가 또는 고급 스타일 지정 등의 기타 수정 사항은 HTML 모드를 통해 이메일의 소스 코드에서 직접 수행해야 합니다.

기존 이메일을 이메일 디자이너와 호환되는 이메일로 변환하는 방법에 대한 자세한 내용은 [이 섹션](../../designing/using/using-existing-content.md)을 참조하십시오.

**관련 항목**:

* [이메일 만들기](../../channels/using/creating-an-email.md)
* [이메일 디자이너를 위한 소개 비디오](../../designing/using/designing-content-in-adobe-campaign.md#video)
* [처음부터 이메일 컨텐츠 디자인](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch)

## HTML 내용 변환 중 {#converting-an-html-content}

여러 이메일에 재사용할 수 있도록 결합할 수 있는 모듈형 템플릿 및 조각의 프레임워크를 구축하려면 이메일 HTML을 이메일 디자이너 템플릿으로 변환하는 것을 고려해야 합니다.

이 사용 사례는 HTML 이메일을 이메일 디자이너 구성 요소로 신속하게 변환하는 방법을 제공합니다.

>[!CAUTION]
>
>이 섹션은 HTML 코드에 익숙한 고급 사용자를 위한 것입니다.

>[!NOTE]
>
>호환성 모드와 마찬가지로 HTML 구성 요소는 제한된 옵션으로 편집할 수 있습니다.즉석 에디션만 수행할 수 있습니다.

이메일 디자이너 외부에서 원본 HTML이 재사용 가능한 섹션으로 구분되어 있는지 확인합니다.

그렇지 않은 경우 HTML에서 다른 블록을 잘라냅니다. 예제:

```
<!-- 3 COLUMN w/CTA (SCALED) -->
<table width="100%" align="center" cellspacing="0" cellpadding="0" border="0" role="presentation" style="max-width:680px;">
<tbody>
<tr>
<td class="padh10" align="center" valign="top" style="padding:0 5px 20px 5px;">
<table width="100%" cellspacing="0" cellpadding="0" border="0" role="presentation">
<tbody>
<tr>
...
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>
<!-- //3 COLUMN w/CTA (SCALED) -->
```

모든 블록을 식별했으면 이메일 디자이너에서 기존 이메일의 각 섹션에 대해 다음 절차를 반복합니다.

1. 이메일 디자이너를 열어 빈 이메일 컨텐츠를 만듭니다.
1. 본문 수준 특성을 설정합니다.배경색, 폭 등 자세한 내용은 [전자 메일 스타일 편집](../../designing/using/styles.md)을 참조하십시오.
1. 구조 구성 요소를 추가합니다. 자세한 내용은 [전자 메일 구조 편집](../../designing/using/designing-from-scratch.md#defining-the-email-structure)을 참조하십시오.
1. HTML 구성 요소를 추가합니다. 자세한 내용은 [조각 및 구성 요소 추가](../../designing/using/designing-from-scratch.md#defining-the-email-structure)를 참조하십시오.
1. HTML을 해당 구성 요소에 복사하여 붙여넣습니다.
1. 모바일 보기로 전환합니다. 자세한 내용은 [이 섹션](../../designing/using/plain-text-html-modes.md#switching-to-mobile-view)을 참조하십시오.

   CSS가 없으므로 반응형 보기가 끊어집니다.

1. 이 문제를 해결하려면 소스 코드 모드로 전환한 다음 스타일 섹션을 새 스타일 섹션에 복사하여 붙여넣습니다. 예제:

   ```
   <style type="text/css">
   a {text-decoration:none;}
   body {min-width:100% !important; margin:0 auto !important; padding:0 !important;}
   img {line-height:100%; text-decoration:none; -ms-interpolation-mode:bicubic;}
   ...
   </style>
   ```

   >[!NOTE]
   >
   >다른 사용자 지정 스타일 태그에서 스타일 뒤에 스타일을 추가해야 합니다.
   >
   >이메일 디자이너가 생성한 CSS는 수정하지 마십시오.
   >
   >* `<style data-name="default" type="text/css">(##)</style>`
   >* `<style data-name="supportIOS10" type="text/css">(##)</style>`
   >* `<style data-name="mediaIOS8" type="text/css">(##)</style>`
   >* `<style data-name="media-default-max-width-500px" type="text/css">(##)</style>`
   >* `<style data-name="media-default--webkit-min-device-pixel-ratio-0" type="text/css">(##)</style>`


1. 모바일 보기로 돌아가 컨텐츠가 올바로 표시되는지 확인하고 변경 내용을 저장합니다.
