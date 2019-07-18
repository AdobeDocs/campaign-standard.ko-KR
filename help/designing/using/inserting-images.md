---
title: 이미지 삽입
seo-title: 이미지 삽입
description: 이미지 삽입
seo-description: 컨텐츠에 이미지를 추가하는 방법을 살펴봅니다.
page-status-flag: 정품 인증 안 함
uuid: AC 42 B 1 D 3-50 AD -4323-B 474-1 E 50 E 468901 F
contentOwner: Sauviat
products: sg_ campaign/standard
audience: designing
content-type: 참조
topic-tags: 이미지 사용
discoiquuid: EDE 832 AC -96 E 5-41 E 1-8390-6669 BA 30 D 4 D 8
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: a12df43de55dedf388a397fbf4670d99e3ea7f3d

---


# Inserting images{#inserting-images}

이메일 및 랜딩 페이지에 이미지를 삽입할 수 있습니다.

구성에 따라 다음 유형의 이미지를 사용할 수 있습니다.

* 로컬 이미지
* Images shared from Adobe Experience Cloud - refer to [Working with Campaign and Assets Core Service](../../integrating/using/working-with-campaign-and-assets-core-service.md) / Assets On Demand
* Dynamic images from Adobe Target - refer to [Working with Campaign and Target](../../integrating/using/about-campaign-target-integration.md)

활성화된 경우 Adobe Creative SDK를 사용하여 이미지를 수정할 수 있습니다. See [Modifying images with the Adobe Creative SDK](../../designing/using/modifying-images-with-the-adobe-creative-sdk.md).

>[!CAUTION]
>
>If you choose to add an image directly by editing the HTML version of the email, you must not call up **external files in a &lt;script&gt; tag** of the HTML page. 이러한 파일은 Adobe Campaign 서버로 가져올 수 없습니다.

## Inserting images in an email {#inserting-images-in-an-email}

1. 구조 구성 요소를 추가합니다. For more on this, see [Editing the email structure](../../designing/using/defining-the-email-structure.md#editing-the-email-structure).
1. Inside this structure component, add an **[!UICONTROL Image]** content component.

   ![](assets/des_insert_images_1.png)

1. **[!UICONTROL Browse]**&#x200B;을 클릭합니다. 이미지를 드래그하여 놓거나 컴퓨터에서 파일을 클릭하여 선택합니다.

   ![](assets/des_insert_images_2.png)

1. 방금 추가한 콘텐츠 구성 요소를 선택합니다.
1. 이미지 속성을 확인하고 필요한 경우 조정합니다.

   ![](assets/des_insert_images_3.png)

## Inserting images in a landing page {#inserting-images-in-a-landing-page}

1. 랜딩 페이지 컨텐츠에서 이미지가 포함된 블록을 선택합니다.
1. **[!UICONTROL Insert]** 단추를 선택합니다.

   ![](assets/des_insert_images_lp_1.png)

1. Choose **[!UICONTROL Local image]** from the contextual toolbar.

   ![](assets/des_insert_images_lp_2.png)

1. 파일을 선택합니다.

   ![](assets/des_insert_images_lp_3.png)

1. 필요에 따라 이미지 속성을 조정합니다.

   ![](assets/des_insert_images_lp_4.png)

