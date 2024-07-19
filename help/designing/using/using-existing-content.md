---
title: 기존 콘텐츠를 사용한 이메일 디자인
description: 이메일 Designer에서 기존 콘텐츠 이메일 콘텐츠를 사용하여 이메일을 디자인하는 방법을 살펴봅니다.
audience: designing
content-type: reference
topic-tags: editing-email-content
feature: Email Design
role: User
level: Intermediate
exl-id: 3bda4227-2a6e-4813-a288-93a4388a9787
source-git-commit: 6530ca1726a2aff18c5be9566d8008c317918e64
workflow-type: tm+mt
source-wordcount: '1277'
ht-degree: 3%

---

# 기존 콘텐츠를 사용하여 디자인 {#designing-using-existing-content}

## 기존 콘텐츠 선택{#selecting-an-existing-content}

Adobe Campaign에는 시작하는 데 도움이 되는 사전 정의된 콘텐츠 세트가 포함되어 있습니다. 이 중 하나를 사용하거나, 전송해야 하는 메시지의 콘텐츠가 Adobe Campaign 외부에서 준비되는 경우 컴퓨터 또는 URL에서 가져올 수 있습니다.

이메일 또는 랜딩 페이지를 만들 때 다른 소스에서 기존 콘텐츠를 로드하도록 선택할 수 있습니다.

>[!NOTE]
>
>아래 이미지는 [전자 메일 Designer](../../designing/using/designing-content-in-adobe-campaign.md)을 사용하여 기존 콘텐츠를 로드하는 방법을 보여 줍니다.

1. 이메일 또는 랜딩 페이지를 만든 후 해당 콘텐츠를 엽니다.
1. **[!UICONTROL Email Designer]** 홈 페이지에 액세스하려면 홈 아이콘을 클릭하십시오.

   ![](assets/des_loading_1.png)

1. 로드할 컨텐츠의 소스 선택:

   * [콘텐츠 템플릿](../../designing/using/using-reusable-content.md#content-templates): **[!UICONTROL Templates]** 탭을 클릭합니다.
   * [처음부터 콘텐츠](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch) 새로 시작하려면 **[!UICONTROL Create]** 단추를 클릭하세요.
   * [컴퓨터의 내용을 ZIP 또는 HTML 파일로](#importing-content-from-a-file): **[!UICONTROL Upload]** 단추를 클릭합니다.
   * [기존 URL의 콘텐츠](#importing-content-from-a-url)(전자 메일 전용): **[!UICONTROL Import from URL]** 단추를 클릭합니다.

   ![](assets/des_loading_2.png)

1. 콘텐츠를 로드합니다. 선택한 콘텐츠가 현재 콘텐츠를 대체합니다.

   가져온 콘텐츠는 편집하고 개인화할 수 있습니다.

   >[!NOTE]
   >
   >[전자 메일 Designer](../../designing/using/designing-content-in-adobe-campaign.md)에서 특정 태깅을 사용합니다. Campaign에 업로드된 표준 HTML 콘텐츠는 이메일 Designer에서 완벽하게 호환되고 편집할 수 있도록 예상 태깅과 일치해야 합니다. 일치하지 않으면 콘텐츠가 [호환성 모드](#compatibility-mode)에서 업로드됩니다. 기존 콘텐츠를 호환되도록 하려면 [이 섹션](#editing-existing-contents-with-the-email-designer)을 참조하세요.

**관련 항목:**

* [이메일 만들기](../../channels/using/creating-an-email.md)
* [랜딩 페이지 관리](../../channels/using/getting-started-with-landing-pages.md)

## 이메일 Designer으로 기존 콘텐츠 편집{#editing-existing-contents-with-the-email-designer}

[전자 메일 Designer](../../designing/using/designing-content-in-adobe-campaign.md)의 편집 가능성을 완전히 활용하려면 업로드된 HTML에 WYSIWYG 편집기와 호환되도록 하는 특정 태깅을 포함해야 합니다.

HTML 전체 또는 일부에 이 태깅이 없으면 콘텐츠가 &#39;[호환성 모드](#compatibility-mode)&#39;에서 로드됩니다.

이메일 Designer 내에서 기존 외부 콘텐츠를 완전히 편집할 수 있게 하려면 [기존 콘텐츠를 사용한 이메일 디자인](../../designing/using/using-existing-content.md) 섹션을 참조하십시오.

## 기존 이메일 콘텐츠 가져오기 {#importing}

### 파일에서 콘텐트 가져오기 {#importing-content-from-a-file}

Designer 전자 메일 홈 페이지에서 **[!UICONTROL Upload]** 단추를 클릭하여 컴퓨터에서 파일을 업로드한 다음 확인합니다.

zip 파일 구조에는 제한이 없습니다. 그러나 HTML 파일 참조는 상대적이어야 하며 zip 폴더의 트리 구조를 준수해야 합니다.

가져오기에 지원되는 형식은 다음과 같습니다.

* 통합 스타일시트가 있는 HTML 파일
* HTML 파일, 스타일 시트(.CSS) 및 이미지가 포함된 .zip 폴더

>[!NOTE]
>
>이메일 콘텐츠의 경우 통합 스타일시트가 있는 단일 HTML 파일을 가져오는 것이 좋습니다.

#### URL에서 콘텐츠 가져오기 {#importing-content-from-a-url}

URL에서 콘텐츠를 가져오기 전에 다음 요구 사항을 준수하는지 확인하십시오.

* 이 URL을 통해 콘텐츠를 공개적으로 사용할 수 있어야 합니다.
* 보안상의 이유로 **[!UICONTROL https]**(으)로 시작하는 URL만 허용됩니다.
* 모든 리소스(이미지, CSS)가 절대 링크 및 HTTPS로 설정되어 있는지 확인하십시오. 그렇지 않으면 이메일을 보낸 후 미러 페이지가 리소스 없이 표시됩니다. 다음은 절대 링크 정의의 예입니다.

  ```
  <a href="https://www.mywebsite.com/images/myimage.png">
  ```

>[!NOTE]
>
>URL에서 콘텐츠를 로드하는 것은 이메일 채널에만 사용할 수 있습니다.

URL에서 기존 콘텐츠를 검색하려면 아래 단계를 따르십시오.

1. Designer 전자 메일 홈 페이지에서 **[!UICONTROL Import from URL]** 단추를 선택합니다.

   ![](assets/email_designer_importfromurl.png)

1. 콘텐츠를 검색할 URL을 정의합니다.
1. **[!UICONTROL Confirm]**&#x200B;를 클릭합니다.

비디오에서 이 기능을 살펴보십시오.

>[!VIDEO](https://video.tv.adobe.com/v/25926?quality=12)

추가 Campaign Standard 방법 비디오를 [여기](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/overview.html?lang=ko)에서 사용할 수 있습니다.

### 준비 시 URL에서 자동으로 콘텐츠 검색 {#retrieving-content-from-a-url-automatically-at-preparation-time}

메시지를 준비하는 동안 URL에서 콘텐츠를 가져오면 이메일이 준비될 때마다 최신 HTML 콘텐츠를 검색할 수 있습니다. 이러한 방식으로 반복 이메일의 콘텐츠는 항상 전송 시 최신 상태로 유지됩니다. 이 기능을 사용하면 콘텐츠가 아직 준비되지 않은 경우에도 특정 날짜에 예약된 메시지를 만들 수 있습니다.

준비 시 콘텐츠를 검색하려면 아래 단계를 따르십시오.

1. **[!UICONTROL Content imported during preparation]** 옵션을 선택하십시오.

   ![](assets/email_designer_importfromurl2.png)

1. 편집기에 URL 콘텐츠가 읽기 전용으로 표시됩니다.

   >[!CAUTION]
   >
   >이 단계에서는 컨텐츠 편집기의 HTML 표시를 고려하지 않아야 합니다. 준비 단계에서 검색됩니다.

1. 검색된 URL 콘텐츠를 미리 보려면 메시지를 만든 후 열고 **[!UICONTROL Preview]** 단추를 클릭합니다.

콘텐츠를 검색할 원격 URL을 개인화할 수 있습니다. 이렇게 하려면 아래 단계를 수행합니다.

1. 화면 맨 위에 있는 전자 메일 레이블을 클릭하여 전자 메일 Designer **[!UICONTROL Properties]** 탭에 액세스합니다.
1. **[!UICONTROL Remote URL]** 필드를 찾습니다.

   ![](assets/email_designer_importfromurl4.png)

1. 원하는 개인화 필드, 콘텐츠 블록 또는 다이내믹 텍스트를 삽입합니다.

   예를 들어 **[!UICONTROL Current date - YYYYMMDD]** 콘텐츠 블록을 사용하면 그날의 날짜를 삽입할 수 있습니다.

   >[!NOTE]
   >
   >사용 가능한 개인화 필드는 **게재** 특성에만 연결됩니다(전자 메일 생성 날짜, 상태, 캠페인 레이블...).

콘텐츠 다운로드가 첫 번째 시도에서 실패하는 경우 두 번 다시 시도할 수 있습니다.

1. 두 번째 시도는 첫 번째 시도 후 50ms 후에 시작됩니다.
1. 세 번째 시도는 두 번째 시도 후 100 ms 후에 시작됩니다.

이러한 재시도는 다음과 같은 경우에 유용합니다.

* 원격 서버에서 단시간 서비스 오류 발생
* 클러스터에서 서버 오류가 발생합니다. 이 경우 작업 서버에 대한 부하 분산 덕분에 재시도가 성공할 가능성이 높아집니다

### 호환성 모드 {#compatibility-mode}

컨텐츠를 업로드할 때 컨텐츠를 완전히 준수하고 이메일 Designer의 WYSIWYG 편집기를 사용하여 편집할 수 있도록 특정 태깅이 포함되어야 합니다.

업로드된 HTML의 전부 또는 일부가 예상 태깅을 준수하지 않는 경우 콘텐츠가 &#39;호환성 모드&#39;로 로드되어 UI를 통한 편집 가능성이 제한됩니다.

콘텐츠가 호환성 모드로 로드되더라도 인터페이스를 통해 다음과 같은 수정 작업을 수행할 수 있습니다(사용할 수 없는 작업은 숨겨짐).

* 텍스트 변경 또는 이미지 변경
* 링크 및 개인화 필드 삽입
* 선택한 HTML 블록에서 일부 스타일 옵션 편집
* 조건부 콘텐츠 정의

![](assets/email_designer_compatibility.png)

이메일에 새 섹션 추가 또는 고급 스타일 지정과 같은 기타 수정 사항은 HTML 모드를 통해 이메일의 소스 코드에서 직접 수행해야 합니다.

기존 전자 메일을 Designer 호환 전자 메일로 변환하는 방법에 대한 자세한 내용은 [이 섹션](../../designing/using/using-existing-content.md)을 참조하세요.

**관련 항목**:

* [이메일 만들기](../../channels/using/creating-an-email.md)
* [이메일 Designer 소개 비디오](../../designing/using/designing-content-in-adobe-campaign.md#video)
* [이메일 콘텐츠를 처음부터 디자인하기](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch)

## HTML 컨텐츠 변환 {#converting-an-html-content}

여러 이메일에서 재사용하기 위해 결합할 수 있는 모듈식 템플릿 및 조각의 프레임워크를 구축하려면 이메일 HTML을 이메일 Designer 템플릿으로 변환하는 것을 고려해야 합니다.

이 사용 사례에서는 HTML 이메일을 이메일 Designer 구성 요소로 빠르게 변환할 수 있습니다.

>[!CAUTION]
>
>이 섹션은 HTML 코드에 익숙한 고급 사용자를 위한 것입니다.

>[!NOTE]
>
>호환성 모드와 마찬가지로 HTML 구성 요소는 제한된 옵션을 사용하여 편집할 수 있습니다. 즉석 편집만 수행할 수 있습니다.

이메일 Designer 외부에서 원래 HTML을 재사용 가능한 섹션으로 구분해야 합니다.

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

모든 블록을 식별한 후에는 이메일 Designer에서 기존 이메일의 각 섹션에 대해 다음 절차를 반복합니다.

1. 이메일 Designer을 열어 빈 이메일 콘텐츠를 만듭니다.
1. 바디 레벨 속성(배경색, 너비 등)을 설정합니다. 자세한 내용은 [전자 메일 스타일 편집](../../designing/using/styles.md)을 참조하십시오.
1. 구조 구성 요소를 추가합니다. 자세한 내용은 [전자 메일 구조 편집](../../designing/using/designing-from-scratch.md#defining-the-email-structure)을 참조하십시오.
1. HTML 구성 요소를 추가합니다. 자세한 내용은 [조각 및 구성 요소 추가](../../designing/using/designing-from-scratch.md#defining-the-email-structure)를 참조하십시오.
1. HTML을 해당 구성 요소에 복사하여 붙여넣습니다.
1. 모바일 보기로 전환합니다. 자세한 내용은 [이 섹션](../../designing/using/plain-text-html-modes.md#switching-to-mobile-view)을 참조하십시오.

   CSS가 누락되었기 때문에 응답형 보기가 손상되었습니다.

1. 이 문제를 해결하려면 소스 코드 모드로 전환하고 스타일 섹션을 새 스타일 섹션에 복사하여 붙여 넣습니다. 예제:

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
   >다른 사용자 지정 스타일 태그에서 이 항목 뒤에 스타일을 추가해야 합니다.
   >
   >이메일 Designer에서 생성한 CSS는 수정하지 마십시오.
   >
   >* `<style data-name="default" type="text/css">(##)</style>`
   >* `<style data-name="supportIOS10" type="text/css">(##)</style>`
   >* `<style data-name="mediaIOS8" type="text/css">(##)</style>`
   >* `<style data-name="media-default-max-width-500px" type="text/css">(##)</style>`
   >* `<style data-name="media-default--webkit-min-device-pixel-ratio-0" type="text/css">(##)</style>`

1. 모바일 보기로 돌아가서 콘텐츠가 올바르게 표시되는지 확인하고 변경 사항을 저장합니다.
