---
title: 랜딩 페이지 컨텐츠 디자인 정보
seo-title: 랜딩 페이지 컨텐츠 디자인 정보
description: 랜딩 페이지 컨텐츠 디자인 정보
seo-description: 랜딩 페이지 컨텐츠 편집기의 특성에 대해 알아봅니다.
page-status-flag: 활성화 안 함
uuid: 8b230690-8a63-44da-b4ed-8e9d8fd84262
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 디자인
content-type: reference
topic-tags: editing-landing-page-content
discoiquuid: 212720d2-5d57-4e7a-bb72-10512050e78c
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: ea825afe573959d95d0f7f3f6e79dd38ac5a678a

---

# 랜딩 페이지 컨텐츠 디자인 정보{#about-landing-page-content-design}

표준 컨텐츠 편집기를 사용하여 Adobe Campaign에서 랜딩 페이지의 컨텐츠를 만들고 수정합니다.

이 섹션에서는 랜딩 페이지 컨텐츠 편집기의 특성에 대해 설명합니다.

* [랜딩 페이지 컨텐츠 편집기 인터페이스](../../channels/using/landing-page-content-editor-interface.md)
* [랜딩 페이지 구조 및 스타일 관리](../../channels/using/managing-landing-page-structure-and-style.md)
* [랜딩 페이지 양식 데이터 속성 변경](../../channels/using/changing-a-landing-page-form-data-properties.md)

하나 이상의 마케팅 활동에 공통되는 작업에 대한 자세한 내용은 다음 섹션을 참조하십시오.

* 랜딩 페이지 컨텐츠를 개인화하는 방법에 대한 자세한 내용은 개인화 필드 [삽입](../../designing/using/personalization.md#inserting-a-personalization-field) 및 [콘텐츠 블록](../../designing/using/personalization.md#adding-a-content-block)추가를 참조하십시오.
* 랜딩 페이지에서 동적 컨텐츠를 정의하는 방법에 대한 자세한 내용은 [랜딩 페이지에서](../../channels/using/defining-dynamic-content-in-a-landing-page.md)동적 컨텐츠 정의를 참조하십시오.
* 랜딩 페이지에 링크 삽입에 대한 자세한 내용은 링크 [삽입을](../../designing/using/links.md#inserting-a-link)참조하십시오.
* 랜딩 페이지에서 이미지를 삽입하는 방법에 대한 자세한 내용은 이미지 [삽입을](../../designing/using/images.md)참조하십시오.

또한 컨텐츠 디자인에 [대한](../../designing/using/overview.md#content-design-best-practices)일반적인 모범 사례를 확인하십시오.

>[!NOTE]
>
>Adobe Campaign Standard 19.0 릴리스 전에 인스턴스가 설치된 경우 기존 이메일 컨텐츠 편집기에 액세스할 수 있습니다. 인터페이스, 사용 원칙 및 구성은 랜딩 페이지에 대해 아래에 설명된 것과 거의 동일합니다. 그러나 19.0 릴리스부터 더 이상 사용되지 않는 기존 이메일 컨텐츠 편집기에서 모든 기능을 사용할 수 없거나 유지 관리할 수 없습니다. 다양한 기능을 갖춘 드래그 앤 드롭 인터페이스를 통해 이메일 컨텐츠를 신속하게 편집하려면 이메일 [디자이너를 사용하십시오](../../designing/using/overview.md).

## 랜딩 페이지 디자인 모범 사례 {#landing-pages-best-practices-design}

* 랜딩 **페이지 컨텐츠를**&#x200B;편집할 때:

   * Adobe Campaign에서 HTML 페이지 템플릿을 가져오기 전에 다양한 브라우저에서 템플릿이 올바르게 열리고 표시되는지 확인하십시오.
   * HTML 페이지에 JavaScript 스크립트가 있는 경우 편집기 외부에서 오류 없이 실행해야 합니다. 일반적으로 메시지 컨텐츠에서 스크립트를 사용하여 이메일 클라이언트가 올바로 처리하는지 확인하십시오.
   * 템플릿을 작성할 때는 태그에 **'type'** 속성을 추가하는 것이 좋습니다. 이 정보는 편집자가 처리하며 웹 애플리케이션을 구성할 때 데이터베이스 필드를 양식 필드에 연결하는 데 도움이 됩니다.
   템플릿의 HTML 코드 예:

   ```
   <input id="email" type="email" name="email"/>
   ```

   'type' 속성의 공식 목록은 다음 주소로 사용할 수 있습니다. [http://www.w3schools.com/tags/att_input_type.asp](http://www.w3schools.com/tags/att_input_type.asp)