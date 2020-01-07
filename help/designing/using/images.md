---
title: 이미지 작업
description: 이메일 디자이너를 사용하여 이메일의 이미지를 관리하는 방법을 살펴볼 수 있습니다.
page-status-flag: never-activated
uuid: 571ffc01-6e41-4501-9094-2f812b041a10
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: editing-email-content
discoiquuid: 39b86fda-7766-4e5f-ab48-bcc536ab66b3
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 7e300de836a74372e411b5b1d584851fac77aafe

---


# 이미지 작업 {#images}

## 이미지 삽입{#inserting-images}

이메일 및 랜딩 페이지에 이미지를 삽입할 수 있습니다.

구성에 따라 다음 유형의 이미지를 사용할 수 있습니다.

* 로컬 이미지
* Adobe Experience Cloud에서 공유된 이미지 - 캠페인 및 [자산 핵심 서비스](../../integrating/using/working-with-campaign-and-assets-core-service.md) /Assets On Demand 작업을 참조하십시오.
* Adobe Target의 동적 이미지 - 캠페인 [및 타겟 작업을 참조하십시오.](../../integrating/using/about-campaign-target-integration.md)

활성화된 경우 Adobe Creative SDK를 사용하여 이미지를 수정할 수 있습니다. Adobe [Creative SDK를 사용하여 이미지 수정을 참조하십시오](#modifying-images-with-the-adobe-creative-sdk).

>[!CAUTION]
>
>이메일의 HTML 버전을 편집하여 직접 이미지를 추가하도록 선택한 경우 HTML 페이지의 &lt;script> 태그에서 **외부 파일을** 호출해서는 안 됩니다. 이러한 파일은 Adobe Campaign 서버로 가져오지 않습니다.

### 이메일에 이미지 삽입 {#inserting-images-in-an-email}

1. 구조 구성 요소를 추가합니다. 자세한 내용은 이메일 [구조](../../designing/using/designing-from-scratch.md#defining-the-email-structure)편집을 참조하십시오.
1. 이 구조 구성 요소 내에서 **[!UICONTROL Image]**콘텐츠 구성 요소를 추가합니다.

   ![](assets/des_insert_images_1.png)

1. 클릭 **[!UICONTROL Browse]**. 이미지를 드래그하여 놓거나 클릭하여 컴퓨터에서 파일을 선택합니다.

   ![](assets/des_insert_images_2.png)

1. 방금 추가한 컨텐츠 구성 요소를 선택합니다.
1. 이미지 속성을 확인하고 필요한 경우 조정합니다.

   ![](assets/des_insert_images_3.png)

## 이미지 속성 설정{#setting-up-image-properties}

이미지가 포함된 블록을 선택하면 팔레트에서 다음 속성이 제공됩니다.

* **개인화를** 활성화하면 이미지 소스를 사용자 정의할 수 있습니다. 이미지 [소스](../../designing/using/personalization.md#personalizing-an-image-source)개인화를 참조하십시오.
* **이미지 제목을** 사용하면 이미지의 제목을 정의할 수 있습니다.
* **대체 텍스트** (이메일) 또는 **캡션** ( **랜딩 페이지)** 기능을 사용하면 이미지에 연결된 캡션을 정의할 수 있습니다(대체HTML 속성에 해당).
* 이메일을 편집할 때 **스타일을** 사용하면 이미지 크기, 배경 및 테두리를 지정할 수 있습니다.
* 랜딩 페이지를 편집할 때 **차원을** 사용하면 이미지 크기를 픽셀 단위로 지정할 수 있습니다.

편집기를 사용하면 브라우저와 호환되는 **모든 이미지 유형을** 사용하여 작업할 수 있습니다. 편집기와 호환되려면 **&quot;Flash&quot; 유형 애니메이션을** 다음과 같이 HTML 페이지에 삽입해야 합니다.

```
<object type="application/x-shockwave-flash" data="http://www.mydomain.com/flash/your_animation.swf" width="200" height="400">
 <param name="movie" value="http://www.mydomain.com/flash/your_animation.swf" />
 <param name="quality" value="high" />
 <param name="play" value="true"/>
 <param name="loop" value="true"/> 
</object>
```

## Adobe Creative SDK를 사용하여 이미지 수정{#modifying-images-with-the-adobe-creative-sdk}

이미지를 편집하고 Adobe Creative SDK에서 제공하는 전체 기능을 사용하여 이메일 또는 랜딩 페이지를 편집할 때 컨텐츠 편집기에서 바로 이미지를 향상시킬 수 있습니다.

이미지 편집기는 이미지를 편집하고 효과 및 프레임을 적용할 수 있는 강력하고 완벽한 기능을 갖춘 이미지 편집 UI 구성 요소를 제공하므로 원본 고품질의 스티커, 멋진 오버레이, 기울기 이동 및 색상 시작, 전문가 수준의 조정 등과 같은 재미있는 기능을 사용할 수 있습니다.

Adobe Creative SDK를 사용하여 이미지를 수정하려면:

1. 이미지를 선택합니다.
1. 도구 모음에서 Creative Cloud 아이콘을 클릭합니다.

   ![](assets/des_creative_sdk_icon.png)

1. 창 위쪽에 있는 아이콘을 통해 사용할 도구를 선택하여 이미지를 수정합니다.

   ![](assets/email_designer_ccsdktoolbar.png)

1. 수정이 **[!UICONTROL Save]**완료되면 을 클릭합니다. 업데이트된 이미지가 Adobe Campaign 서버에 저장되고 사용할 준비가 되었습니다.

>[!NOTE]
이미지 편집기에 제공된 도구를 사용자 지정할 수 없습니다.
