---
title: 랜딩 페이지를 설정하는 기본 단계
seo-title: 랜딩 페이지를 설정하는 기본 단계
description: 랜딩 페이지를 설정하는 기본 단계
seo-description: 랜딩 페이지를 설정하는 기본 단계 학습
page-status-flag: 활성화 안 함
uuid: b316bf47-7d98-46fa-ab4f-67ff50de8095
contentOwner: 여우원숭이
products: SG_CAMPAIGN/STANDARD
audience: 채널
content-type: reference
topic-tags: 랜딩 페이지
discoiquuid: ca8d1698-6e8a-4f5a-b017-74a152e14286
context-tags: landingPage,wizard;landingPage,overview;landingPage,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 1f100f6b041c6dbb298113b4ecc7830951714131

---


# 랜딩 페이지를 설정하는 기본 단계 {#main-steps-create-a-landing-page}

## 랜딩 페이지 만들기 정보

랜딩 페이지를 설정할 때의 주요 단계는 다음과 같습니다.

![](assets/lp_steps.png)

이 페이지에서는 이러한 각 단계에 대한 정보와 전용 문서에 대한 참조를 확인할 수 있습니다.

## 랜딩 페이지 템플릿 구성 {#configure-the-landing-page-template}

랜딩 페이지를 설정하기 전에 첫 번째 단계는 필요에 맞는 랜딩 페이지 템플릿을 구성하는 것입니다. 템플릿이 준비되면 템플릿을 기반으로 하는 모든 랜딩 페이지가 원하는 매개 변수로 미리 구성됩니다.

1. 고급 메뉴에서 Adobe Campaign 로고를 통해 **[!UICONTROL Resources]** / **[!UICONTROL Templates]** / **[!UICONTROL Landing page templates]**&#x200B;를 선택한 다음 사용할 템플릿을 복제합니다.
1. 템플릿 속성에서 랜딩 페이지에 공통으로 포함해야 하는 모든 매개 변수를 지정합니다. 예:타깃팅 차원, 식별되거나 식별되지 않은 방문자에 대한 페이지 액세스 매개 변수, 방문자의 양식 유효성 검사에 특정한 작업, 컨텐츠에 사용할 브랜드/로고 등.
1. 수정 내용을 저장합니다.

랜딩 페이지 템플릿에 대한 자세한 내용은 [이 섹션을](../../channels/using/about-landing-pages.md)참조하십시오.

![](assets/lp-steps1.png)

## 랜딩 페이지 만들기 및 구성 {#create-and-configure-the-landing-page}

이전 단계에서 정의한 템플릿에서 프로그램 또는 캠페인에서 새 랜딩 페이지를 만듭니다.

1. 원하는 템플릿을 기반으로 랜딩 페이지를 만듭니다.
1. 랜딩 페이지의 일반 매개 변수(레이블, 설명 등)를 입력합니다.
1. 그러면 랜딩 페이지 대시보드에 액세스합니다. 필요한 경우 랜딩 페이지 속성을 편집합니다. 기본적으로 속성은 랜딩 페이지 템플릿에 구성된 속성입니다.
보안상의 이유 및 플랫폼 성능 때문에 랜딩 페이지 속성에서 만료 날짜를 설정하는 것이 좋습니다. 완료되면 선택한 날짜에 랜딩 페이지의 게시가 자동으로 취소됩니다. For more on validity parameters, refer to [this section](../../channels/using/sharing-a-landing-page.md#setting-up-validity-parameters).

   ![](assets/lp-steps3.png)

   >[!NOTE]
   >
   >수정 사항은 편집 중인 랜딩 페이지에만 적용됩니다. 이러한 수정 사항을 다른 랜딩 페이지에 적용하려면 전용 템플릿에서 수행한 다음 해당 템플릿에서 다른 랜딩 페이지를 만들 수 있습니다.

## 랜딩 페이지 디자인 {#design-the-landing-page}

이제 랜딩 페이지의 컨텐츠를 정의할 수 있습니다. 기본적으로 랜딩 페이지에는 스크롤 화살표를 통해 액세스할 수 있는 세 개의 페이지가 포함되어 있습니다.기본 컨텐츠 페이지, 확인 페이지 및 오류 페이지.

![](assets/lp-steps4.png)

각 페이지에서 기본적으로 여러 필드가 구성됩니다. 필요한 경우 속성 및 매핑을 편집할 수 있습니다.

또한 프로파일을 클릭하면 확인 버튼이 동작하는 방식을 구성하고 필요에 따라 컨텐츠를 개인화할 수 있습니다(이미지, 개인화 필드 등). 예를 들어, 등록해 주셔서 감사합니다. 랜딩 페이지의 확인 페이지에 프로필의 이름을 삽입할 수 있습니다.

랜딩 페이지 디자인에 대한 자세한 내용은 [이 섹션을](../../channels/using/designing-a-landing-page.md)참조하십시오.

## 랜딩 페이지 테스트 {#test-the-landing-page}

랜딩 페이지가 정의되면, 랜딩 페이지가 실행될 방법을 시뮬레이션하고, 이를 온라인에서 사용할 수 있을 때 동작할 수 있습니다.

![](assets/lp-steps5.png)

>[!CAUTION]
>
>랜딩 페이지 테스트는 테스트 프로필과 함께 수행할 수 없고 프로파일에서만 수행할 수 있습니다. 양식을 제출하면 선택한 프로필의 데이터가 실제로 업데이트됩니다. 실제 프로필을 수정하지 않으려면 가짜 고객 프로필을 사용하십시오.

랜딩 페이지의 작동 방식에 만족하면 이를 게시하여 온라인으로 사용할 수 있습니다.

랜딩 페이지를 테스트하는 방법에 대한 자세한 내용은 [이 섹션을](../../channels/using/sharing-a-landing-page.md#testing-the-landing-page-)참조하십시오.

## 랜딩 페이지 게시 {#publish-the-landing-page}

테스트가 완료되면 대시보드의 작업 표시줄에서 **[!UICONTROL Publish]** 단추를 사용하여 랜딩 페이지를 게시할 수 있습니다. 모니터링 블록은 게시의 진행 상황과 상태를 보여줍니다.

랜딩 페이지를 게시하면 온라인에서 액세스할 수 있습니다. 게시한 후에는 항상 업데이트할 수 있습니다.이렇게 하려면 각 수정 후에 다시 게시해야 합니다. 랜딩 페이지를 더 이상 사용할 수 없도록 언제든지 게시 취소할 수도 있습니다.

![](assets/lp-steps6.png)

게시되면 랜딩 페이지를 사용할 수 있습니다. 그런 다음 데이터베이스에 액세스하여 새 프로파일을 얻거나 기존 프로파일에 대한 추가 정보를 얻을 수 있도록 다른 메커니즘을 배치할 수 있습니다.

랜딩 페이지 게시에 대한 자세한 내용은 [이 섹션을](../../channels/using/sharing-a-landing-page.md#publishing-a-landing-page)참조하십시오.
