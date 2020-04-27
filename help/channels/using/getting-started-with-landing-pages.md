---
title: 랜딩 페이지 설정 주요 단계
description: 랜딩 페이지를 설정하는 기본 단계 학습
page-status-flag: never-activated
uuid: b316bf47-7d98-46fa-ab4f-67ff50de8095
contentOwner: lemaitre
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: landing-pages
discoiquuid: ca8d1698-6e8a-4f5a-b017-74a152e14286
context-tags: landingPage,wizard;landingPage,overview;landingPage,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: efb1f14e0094e200d186423f98bfad65d25cfab2

---


# 랜딩 페이지 시작 {#getting-started-with-landing-pages}

## 랜딩 페이지 기본 정보 {#about-landing-pages}

Campaign에는 고객 정보를 캡처하고, 서비스에 구독을 제공하고, 데이터를 표시하고, 데이터베이스를 확장하는 데 사용할 수 있는 웹 양식인 랜딩 페이지가 포함되어 있습니다. 랜딩 페이지는 기존 프로필을 가져오거나 업데이트하는 데에도 사용할 수 있습니다.

랜딩 페이지를 사용하여 이중 옵트인 메커니즘을 설정할 수 있으므로, 플랫폼을 잘못되거나 잘못된 이메일 주소 또는 스팸보트에서 보호할 수 있습니다. 자세한 내용은 [전용 사용 사례를](../../channels/using/setting-up-a-double-opt-in-process.md)참조하십시오.

랜딩 페이지를 설정할 때의 주요 단계는 다음과 같습니다.

![](assets/lp_steps.png)

이 페이지에서는 이러한 각 단계에 대한 정보와 전용 문서에 대한 참조를 확인할 수 있습니다.

**관련 항목:**

* [랜딩 페이지 만들기 자습서 비디오](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/communication-channels/landing-pages/landing-page-create-and-edit.html) 비디오
* [서비스 만들기](../../audiences/using/creating-a-service.md)
* [이중 옵트인 프로세스 설정](setting-up-a-double-opt-in-process.md)

## 랜딩 페이지 제한 사항{#landing-page-limitations}

아래 섹션에는 랜딩 페이지 설정을 시작하기 전에 알아야 할 제한 사항이 나와 있습니다.

**데이터 작성 및 업데이트**

* 랜딩 페이지는 **[!UICONTROL Profile]** 및 **[!UICONTROL Subscription]** 리소스로만 제한됩니다. 기록을 저장 및 업데이트할 수 **[!UICONTROL Profile]** 있으며 구독/구독 취소 **[!UICONTROL Service]**가능
리소스 구성에 대한 자세한 내용은 [리소스의 데이터 구조](../../developing/using/configuring-the-resource-s-data-structure.md)구성을 참조하십시오.

>[!CAUTION]
>
>랜딩 페이지는 **[!UICONTROL Profile]** 및 이외의 다른 리소스에서 데이터를 표시하거나 업데이트할 수 없습니다 **[!UICONTROL Subscription]**.

**미리 로드**

* 랜딩 페이지는 자동으로 레코드 목록을 표시할 수 없으므로 이미 가입한 프로파일을 나열할 수 없습니다. 서비스에 대한 자세한 내용은 이 [페이지를](../../audiences/using/creating-a-service.md)참조하십시오.

* 양식이 미리 채워진 랜딩 페이지(데이터가 페이지에 미리 로드됨)는 Adobe Campaign 이메일에서만 액세스할 수 있습니다. 웹 사이트 페이지에서 이러한 양식에 액세스할 수 없습니다.

**조정**

* 조정 동작은 다음과 같습니다.일치가 발견되면 조정 프로세스가 중지됩니다. 즉, 재조정은 하나의 프로필 레코드에서만 수행할 수 있고 중복이 있는 경우 여러 레코드에서 수행할 수 없습니다.

예를 들어 다음 획득 랜딩 페이지를 프로필로 보내 프로필의 모바일 번호로 캠페인 데이터베이스를 업데이트할 수 있습니다.

![](assets/landing_page_limitation_1.png)

프로필 중 하나가 새 정보로 랜딩 페이지를 채우지만 이미 중복된 프로필이 있는 경우, 프로필은 작성 날짜에만 따라 우선 순위가 지정되므로 가장 빨리 만든 날짜를 가진 일치하는 프로필이 업데이트됩니다.

여기서 첫 번째 프로필은 가장 오래된 항목이므로 업데이트되었습니다.

![](assets/landing_page_limitation_2.png)

**랜딩 페이지 테스트**

* 랜딩 페이지는 프로필에서만 작동하고 테스트 프로필에서는 작동하지 않습니다. 즉, 랜딩 페이지는 이메일 증빙 자료로 테스트할 수 없습니다.

## 1단계 - 랜딩 페이지 템플릿 구성 {#configure-the-landing-page-template}

랜딩 페이지를 설정하기 전에 첫 번째 단계는 필요에 맞는 랜딩 페이지 템플릿을 구성하는 것입니다. 템플릿이 준비되면 템플릿을 기반으로 하는 모든 랜딩 페이지가 원하는 매개 변수로 미리 구성됩니다.

1. 고급 메뉴에서 Adobe Campaign 로고를 통해 **[!UICONTROL Resources]** / **[!UICONTROL Templates]** / **[!UICONTROL Landing page templates]**&#x200B;를 선택한 다음 사용할 템플릿을 복제합니다.
1. 템플릿 속성에서 랜딩 페이지에 공통으로 포함해야 하는 모든 매개 변수를 지정합니다. 예:타깃팅 차원, 식별되거나 식별되지 않은 방문자에 대한 페이지 액세스 매개 변수, 방문자의 양식 유효성 검사에 특정한 작업, 컨텐츠에 사용할 브랜드/로고 등. 랜딩 페이지의 속성에 대한 자세한 내용은 [이 섹션을 참조하십시오](../../channels/using/configuring-landing-page.md)
1. 수정 내용을 저장합니다.

랜딩 페이지 템플릿에 대한 자세한 내용은 [이 섹션을](../../channels/using/getting-started-with-landing-pages.md)참조하십시오.

![](assets/lp-steps1.png)

## 2단계 - 랜딩 페이지 만들기 및 구성 {#create-and-configure-the-landing-page}

이전 단계에서 정의한 템플릿에서 프로그램 또는 캠페인에서 새 랜딩 페이지를 만듭니다.

1. 원하는 템플릿을 기반으로 랜딩 페이지를 만듭니다.
1. 랜딩 페이지의 일반 매개 변수(레이블, 설명 등)를 입력합니다.
1. 그러면 랜딩 페이지 대시보드에 액세스합니다. 필요한 경우 랜딩 페이지 속성을 편집합니다( [랜딩 페이지](../../channels/using/configuring-landing-page.md)구성 참조). 기본적으로 속성은 랜딩 페이지 템플릿에 구성된 속성입니다.
보안상의 이유 및 플랫폼 성능 때문에 랜딩 페이지 속성에서 만료 날짜를 설정하는 것이 좋습니다. 완료되면 선택한 날짜에 랜딩 페이지의 게시가 자동으로 취소됩니다. For more on validity parameters, refer to [this section](../../channels/using/testing-publishing-landing-page.md#setting-up-validity-parameters).

   ![](assets/lp-steps3.png)

   >[!NOTE]
   >
   >수정 사항은 편집 중인 랜딩 페이지에만 적용됩니다. 이러한 수정 사항을 다른 랜딩 페이지에 적용하려면 전용 템플릿에서 수행한 다음 해당 템플릿에서 다른 랜딩 페이지를 만들 수 있습니다.

## 3단계 - 랜딩 페이지 디자인 {#design-the-landing-page}

이제 랜딩 페이지의 컨텐츠를 정의할 수 있습니다. 기본적으로 랜딩 페이지에는 스크롤 화살표를 통해 액세스할 수 있는 세 개의 페이지가 포함되어 있습니다.기본 컨텐츠 페이지, 확인 페이지 및 오류 페이지.

![](assets/lp-steps4.png)

각 페이지에서 기본적으로 여러 필드가 구성됩니다. 필요한 경우 속성 및 매핑을 편집할 수 있습니다.

또한 프로파일을 클릭하면 확인 버튼이 동작하는 방식을 구성하고 필요에 따라 컨텐츠를 개인화할 수 있습니다(이미지, 개인화 필드 등). 예를 들어, 등록해 주셔서 감사합니다. 랜딩 페이지의 확인 페이지에 프로필의 이름을 삽입할 수 있습니다.

랜딩 페이지 디자인에 대한 자세한 내용은 [이 섹션을](../../channels/using/designing-a-landing-page.md)참조하십시오.

## 4단계 - 랜딩 페이지 테스트 {#test-the-landing-page}

랜딩 페이지가 정의되면, 랜딩 페이지가 실행될 방법을 시뮬레이션하고, 이를 온라인에서 사용할 수 있을 때 동작할 수 있습니다.

![](assets/lp-steps5.png)

>[!CAUTION]
>
>랜딩 페이지 테스트는 테스트 프로필과 함께 수행할 수 없고 프로파일에서만 수행할 수 있습니다. 양식을 제출하면 선택한 프로필의 데이터가 실제로 업데이트됩니다. 실제 프로필을 수정하지 않으려면 가짜 고객 프로필을 사용하십시오.

랜딩 페이지의 작동 방식에 만족하면 이를 게시하여 온라인으로 사용할 수 있습니다.

랜딩 페이지를 테스트하는 방법에 대한 자세한 내용은 [이 섹션을](../../channels/using/testing-publishing-landing-page.md#testing-the-landing-page-)참조하십시오.

## 5단계 - 랜딩 페이지 게시 {#publish-the-landing-page}

테스트가 성공하면 대시보드의 작업 표시줄의 **[!UICONTROL Publish]** 단추를 사용하여 랜딩 페이지를 게시할 수 있습니다. 모니터링 블록은 게시의 진행 상황과 상태를 보여줍니다.

랜딩 페이지를 게시하면 온라인에서 액세스할 수 있습니다. 게시한 후에는 항상 업데이트할 수 있습니다.이렇게 하려면 각 수정 후에 다시 게시해야 합니다. 랜딩 페이지를 더 이상 사용할 수 없도록 언제든지 게시 취소할 수도 있습니다.

![](assets/lp-steps6.png)

게시되면 랜딩 페이지를 사용할 수 있습니다. 그런 다음 데이터베이스에 액세스하여 새 프로파일을 얻거나 기존 프로파일에 대한 추가 정보를 얻을 수 있도록 다른 메커니즘을 배치할 수 있습니다.

랜딩 페이지 게시에 대한 자세한 내용은 [이 섹션을](../../channels/using/testing-publishing-landing-page.md#publishing-a-landing-page)참조하십시오.
