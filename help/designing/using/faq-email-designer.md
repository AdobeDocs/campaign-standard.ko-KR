---
title: 이메일 Designer FAQ
description: 이메일 Designer에 대한 FAQ.
audience: designing
content-type: reference
topic-tags: working-with-campaign-and-analytics
feature: Email Design
role: User
level: Intermediate
exl-id: f3208380-a4cf-4944-aa24-883995d1075d
source-git-commit: 13d419c5fc51845ee14f8a3b288f4c467e0a60d9
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 3%

---

# 이메일 Designer FAQ

## 콘텐츠 블록과 콘텐츠 조각의 차이점은 무엇입니까?

콘텐츠 블록 및 콘텐츠 조각 은 여러 이메일에서 공통되는 재사용 가능한 콘텐츠 조각입니다. 이메일 일관성을 보장하고 이메일 생성을 최적화/표준화하는 데 사용됩니다. 콘텐츠 블록과 콘텐츠 조각의 차이점은 가능한 사용자 지정 수준입니다.

* 콘텐츠 블록은 HTML 코드가 수동으로 삽입되는 순수 HTML(사용자에게 친숙한 UI가 아니라 직접 소스 코드)입니다. HTML 지식이 있는 사람을 대상으로 하지만, 콘텐츠 조각에서 사용할 수 없는 개인화 수준을 허용합니다.

* 콘텐츠 조각 은 사용자에게 친숙한 UI를 사용하여 이메일 Designer을 통해 만든 콘텐츠의 시각적 부분입니다. 단, 콘텐츠를 개인화할 수는 없습니다. 개인화가 필요한 경우 콘텐츠 블록을 통해서만 수행할 수 있습니다.

## HTML 구조에서 요소에 패딩을 추가하려면 어떻게 해야 합니까?

HTML 이동 경로를 사용하여 패딩을 추가할 수 있습니다.

1. 화면 왼쪽 하단에서 HTML 이동 경로를 클릭합니다.

   ![](assets/do-not-localize/breadcrumb.png)

1. 패딩을 추가할 요소를 클릭합니다.
1. HTML 탐색 표시에서 상위 태그를 클릭합니다.
이제 이 요소에 패딩을 추가할 수 있습니다.

## 이메일 Designer에서 HTML 콘텐츠를 가져올 수 있습니까?

이메일 Designer에 나만의 HTML 콘텐츠를 업로드할 수 있습니다. 이메일 Designer을 통해 작성되지 않은 경우, 원래 HTML을 유지하도록 디자인되었지만 UI를 통해 특정 에디션 기능을 제한하는 호환성 모드로 로드됩니다.

자세한 내용은 [호환성 모드](../../designing/using/using-existing-content.md#compatibility-mode)를 참조하세요.

## 첫 번째 이메일 콘텐츠를 만들려면 어떻게 해야 합니까?

우선 홈페이지에서 이메일을 만듭니다.
그런 다음 이메일에 콘텐츠를 추가하려면 구조 구성 요소를 추가하고 해당 구성 요소에 콘텐츠 구성 요소를 삽입해야 합니다.

자세한 내용은 [처음부터 전자 메일 만들기](../../designing/using/quick-start.md#from-scratch-email)를 참조하세요.

## 조각을 업데이트해야 하는 이유는 무엇입니까?

이메일 디자이너는 지속적으로 개선되고 있습니다. 처음부터 이메일 콘텐츠를 만든 경우, 기본 제공 템플릿에서 또는 조각을 만든 경우, CSS 충돌 문제와 같은 문제를 방지하기 위해 콘텐츠를 최신 버전으로 업데이트해야 할 수 있습니다.

자세한 내용은 [조각 업데이트](../../designing/using/designing-content-in-adobe-campaign.md#email-designer-updates)를 참조하세요.

## 테마에 스타일을 저장할 수 있습니까?

향후 재사용을 위해 스타일을 테마로 저장할 수 없습니다. 그러나 CSS 스타일은 콘텐츠 템플릿 또는 이메일에 저장할 수 있습니다.

자세한 내용은 [스타일](../../designing/using/styles.md)을 참조하세요.

## 사용 가능한 글꼴

스타일을 편집할 때 기본적으로 대부분의 이메일 클라이언트에서 공식적으로 지원하는 웹 글꼴만 UI를 통해 사용할 수 있습니다. 사용자 정의 글꼴을 사용하려면 HTML 코드를 업데이트해야 합니다.
