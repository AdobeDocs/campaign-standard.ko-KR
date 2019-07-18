---
title: 랜딩 페이지에서 동적 컨텐츠 정의
seo-title: 랜딩 페이지에서 동적 컨텐츠 정의
description: 랜딩 페이지에서 동적 컨텐츠 정의
seo-description: 다음 단계에 따라 Adobe Campaign 표현식 편집기를 통해 정의된 조건에 따라 랜딩 페이지에서 동적으로 다른 컨텐츠를 표시합니다.
page-status-flag: 정품 인증 안 함
uuid: 64 a 8 ddd 2-8 bb 0-44 ef-bae 9-b 6 b 77 a 84 ca 8 b
contentOwner: Sauviat
products: sg_ campaign/standard
audience: designing
content-type: 참조
topic-tags: defining-conditional-content
discoiquuid: 00 E 5 ED 81-D 3 D 1-4211-8352-71805 A 7042 C 9
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Defining dynamic content in a landing page{#defining-dynamic-content-in-a-landing-page}

랜딩 페이지에서 동적 컨텐츠를 정의하려면 탐색 표시를 사용하거나 요소를 직접 클릭하여 블록을 선택합니다.

![](assets/dynamic_content_lp_1.png)

이미지와 같은 특정 블록은 직접 선택할 수 없습니다. 이 경우 탐색 표시를 사용하여 상위 블록을 선택합니다. 그런 다음 이미지를 포함하여 이 상위 요소에 포함된 모든 요소를 수정할 수 있습니다. 조건은 부모 블록 내의 모든 하위 요소에 적용됩니다.

The breadcrumb is presented in the [Managing blocks](../../designing/using/managing-landing-page-structure-and-style.md) section.

랜딩 페이지에서 동적 컨텐츠를 정의하는 다음 단계는 이메일에 대해 따라야 하는 단계와 유사합니다. See [this section](../../designing/using/defining-dynamic-content-in-an-email.md).

>[!NOTE]
>
>변형 요소가 빨간색으로 윤곽이 표시된 경우 표현식이 아직 정의되지 않았음을 의미합니다.

## Previewing dynamic content in a landing page {#previewing-dynamic-content-in-a-landing-page}

블록의 여러 동적 컨텐츠 간에 이동할 수 있습니다. 이렇게 하려면:

1. 블록을 선택합니다.

   화살표는 이미지의 오른쪽 및 왼쪽에 나타납니다.

1. 오른쪽 화살표를 클릭하여 사용 가능한 동적 컨텐츠를 검색합니다.

   ![](assets/dynamic_content_lp_2.png)

   마지막 또는 처음 사용 가능한 동적 컨텐츠에 도달했는지 여부에 따라 각 측면의 화살표가 흐리게 표시됩니다.

   ![](assets/dynamic_content_lp_3.png)

1. To delete all the conditions applied to a block, select that block and click the **[!UICONTROL Disable dynamic content]** icon.
1. 유지할 동적 컨텐츠를 선택합니다.

   ![](assets/dynamic_content_lp_5.png)

Palette:

* 입력한 표현식이 더 이상 빨간색으로 표시되지 않고 회색으로 표시됩니다.
* 현재 선택된 컨텐츠는 파란색으로 표시됩니다.

![](assets/dynamic_content_lp_4.png)

