---
title: 이미지 속성 설정
seo-title: 이미지 속성 설정
description: 이미지 속성 설정
seo-description: 컨텐츠에 포함된 이미지의 속성을 관리하는 방법을 살펴봅니다.
page-status-flag: 정품 인증 안 함
uuid: 1 a 439105-D 9 AA -4 B 30-A 00 D-BCF 731 A 04 E 08
contentOwner: Sauviat
products: sg_ campaign/standard
audience: designing
content-type: 참조
topic-tags: 이미지 사용
discoiquuid: 80 C 9 C 1 A 5-6050-443 D -810 A -6 BB 755 D 39 DCA
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Setting up image properties{#setting-up-image-properties}

이미지가 포함된 블록을 선택하면 팔레트에서 다음 속성이 제공됩니다.

* **개인화를** 사용하면 이미지 소스를 사용자 지정할 수 있습니다. See [Personalizing an image source](../../designing/using/personalizing-an-image-source.md).
* **이미지 제목이미지의** 제목을 정의할 수 있습니다.
* **대체 텍스트** (이메일) 또는 **캡션** (랜딩 페이지) 이미지에 연결된 캡션을 정의할 수 있습니다 ( **대체** HTML 속성에 해당합니다).
* When editing an email, **Style** lets you specify the image size, background, and border.
* When editing a landing page, **Dimensions** lets you specify the image size in pixels.

The editor allows you to work with **all image types** whose formats are compatible with browsers. To be compatible with the editor, the **"Flash" type animations** have to be inserted in an HTML page as follows:

```
<object type="application/x-shockwave-flash" data="http://www.mydomain.com/flash/your_animation.swf" width="200" height="400">
 <param name="movie" value="http://www.mydomain.com/flash/your_animation.swf" />
 <param name="quality" value="high" />
 <param name="play" value="true"/>
 <param name="loop" value="true"/> 
</object>
```

