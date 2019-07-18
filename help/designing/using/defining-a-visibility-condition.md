---
title: 가시성 조건 정의
seo-title: 가시성 조건 정의
description: 가시성 조건 정의
seo-description: 특정 조건을 준수하는 경우에만 웹 페이지 요소를 볼 수 있도록 합니다.
page-status-flag: 정품 인증 안 함
uuid: 224005 ba-ef 09-4790-b 2 f 0-30 ed 74 cfa 32 d
contentOwner: Sauviat
products: sg_ campaign/standard
audience: designing
content-type: 참조
topic-tags: defining-conditional-content
discoiquuid: c 12125 a 7-a 1 cf -4 bc 1-a 138-57 ff 74974024
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Defining a visibility condition{#defining-a-visibility-condition}

모든 요소에 대해 가시성 조건을 지정할 수 있습니다. 조건이 충족되는 경우에만 표시됩니다.

To add a visibility condition, select a block and enter the condition to be respected in the **[!UICONTROL Visibility condition]** field of its settings.

![](assets/delivery_content_5.png)

이 옵션은 다음 요소에만 사용할 수 있습니다. address, blockquote, center, dir, div, dl, fieldset, form, h 1, h 2, h 3, h 4, h 5, h 6, noscript, ol, p, pre, ul, tr, td.

The expression editor is presented in the [Advanced expression editing](../../automating/using/editing-queries.md#about-query-editor) section.

These conditions adopt the XTK expression syntax (e.g. **context.profile.email !=''** or **context.profile.status='0'**). 기본적으로 모든 필드가 표시됩니다.

>[!NOTE]
>
>동적 컨텐츠가 이미 있는 하위 요소 또는 이미 동적 컨텐츠를 구성하는 블록이 포함된 블록에 대해 조건을 정의할 수 없습니다. 드롭다운 목록과 같이 보이지 않는 동적 블록은 편집할 수 없습니다.

