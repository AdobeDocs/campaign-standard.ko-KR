---
solution: Campaign Standard
product: campaign
title: '이메일 디자이너 FAQ '
description: 이메일 디자이너에 대한 FAQ
audience: designing
content-type: reference
topic-tags: working-with-campaign-and-analytics
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 7%

---


# 이메일 디자이너 FAQ

## 컨텐츠 블록과 컨텐츠 조각 간의 차이점은 무엇입니까?

콘텐츠 블록과 콘텐츠 조각은 여러 이메일에 공통으로 사용되는 재사용 가능한 콘텐츠의 일부입니다. 이 툴은 이메일 간의 일관성을 유지하고 이메일 제작을 최적화/표준화하는 데 사용됩니다. 컨텐츠 블록과 컨텐츠 조각 간의 차이는 사용자 정의 가능한 수준입니다.

* 컨텐츠 블록은 HTML 코드가 수동으로 삽입되는 순수 HTML입니다(사용자에게 친숙한 UI가 아니라 직접 소스 코드). HTML 지식이 있는 사용자에게는 지향적이지만 컨텐츠 조각에서는 개인화 수준을 사용할 수 없습니다.

* 컨텐츠 조각은 사용자에게 친숙한 UI를 사용하여 이메일 디자이너를 통해 만들어진 컨텐츠의 시각적 조각입니다. 그러나 컨텐츠를 개인화할 수는 없습니다. 개인화가 필요한 경우 콘텐츠 블록을 통해서만 수행할 수 있습니다.

## HTML 구조에서 요소에 패딩을 추가하려면 어떻게 해야 합니까?

HTML 브레드크럼을 사용하여 패딩을 추가할 수 있습니다.

1. 화면 왼쪽 하단에서 HTML 탐색 표시를 클릭합니다.

   ![](assets/do-not-localize/breadcrumb.png)

1. 패딩을 추가할 요소를 클릭합니다.
1. HTML 탐색 경로에서 상위 태그를 클릭합니다.
이제 이 요소에 패딩을 추가할 수 있습니다.

## 이메일 디자이너에서 HTML 컨텐츠를 가져올 수 있습니까?

자신의 HTML 컨텐츠를 이메일 디자이너에 업로드할 수 있습니다. 이메일 디자이너를 통해 만들지 않은 경우에는 원래 HTML을 유지하도록 설계된 호환성 모드로 로드되지만 UI를 통해 특정 에디션 기능을 제한합니다.

자세한 내용은 호환성 [모드를 참조하십시오.](../../designing/using/using-existing-content.md#compatibility-mode)

## 첫 번째 이메일 컨텐츠를 만들려면 어떻게 해야 합니까?

먼저 홈 페이지에서 이메일을 만듭니다.
그런 다음 이메일에 컨텐츠를 추가하려면 구조 구성 요소를 추가하고 컨텐츠 구성 요소를 삽입해야 합니다.

자세한 내용은 처음부터 [이메일 만들기를 참조하십시오.](../../designing/using/quick-start.md#from-scratch-email)

## 조각을 업데이트해야 하는 이유는 무엇입니까?

이메일 디자이너는 지속적으로 개선되고 있습니다. 처음부터 이메일 컨텐츠를 직접 작성하거나 곧바로 사용할 수 있는 템플릿에서 만든 경우, CSS 충돌 문제 등의 문제를 방지하기 위해 컨텐츠를 최신 버전으로 업데이트해야 할 수 있습니다.

자세한 내용은 조각 [업데이트를 참조하십시오.](../../designing/using/designing-content-in-adobe-campaign.md#email-designer-updates)

## 스타일을 테마로 저장할 수 있습니까?

향후 재사용을 위해 스타일을 테마로 저장할 수 없습니다. 그러나 CSS 스타일은 콘텐츠 템플릿 또는 이메일에 저장할 수 있습니다.

자세한 내용은 [스타일 참조](../../designing/using/styles.md)

## 어떤 글꼴을 사용할 수 있습니까?

스타일을 편집할 때 대부분의 이메일 클라이언트가 공식적으로 지원하는 웹 글꼴만 UI를 통해 기본적으로 사용할 수 있습니다. 사용자 정의 글꼴을 사용하려면 HTML 코드를 업데이트해야 합니다.
