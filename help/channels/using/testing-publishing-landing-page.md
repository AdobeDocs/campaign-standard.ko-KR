---
solution: Campaign Standard
product: campaign
title: 랜딩 페이지 공유
description: Adobe Campaign에서 랜딩 페이지를 테스트하고 게시하는 방법을 알아봅니다.
audience: channels
content-type: reference
topic-tags: landing-pages
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 100%

---


# 랜딩 페이지 테스트 및 게시{#testing-publishing--landing-page}

## 랜딩 페이지 게시 기본 정보 {#about-landing-page-publication}

랜딩 페이지를 게시하기 전에 테스트를 수행해야 합니다. 실행의 유효성을 검사하고, 액세스를 구성하고, 랜딩 페이지의 만료 기한을 설정합니다. 이 단계는 필수 사항이며 신중하게 실행해야 합니다.

## 랜딩 페이지 테스트 {#testing-the-landing-page-}

랜딩 페이지는 플랫폼과 데이터에 영향을 주므로 실행을 신중하게 테스트해야 합니다. 방법은 다음과 같습니다.

1. 랜딩 페이지의 작업 표시줄에 있는 **[!UICONTROL Test]** 버튼을 클릭합니다.
1. 테스트 화면에서 테스트 프로필을 선택하고, 랜딩 페이지가 구독을 관리하는 경우 테스트 서비스를 선택합니다.

   ![](assets/lp_test_2.png)

1. 필드에 데이터를 입력하고 옵션을 선택합니다.
1. 랜딩 페이지를 제출하고 데이터베이스에서 업데이트를 확인합니다.

   >[!IMPORTANT]
   >
   >양식을 제출하면 서비스 및 사용한 프로필이 업데이트됩니다.

1. 다양한 프로필 및 데이터를 사용하여 이 과정을 반복합니다.

또한 이 화면에서 랜딩 페이지의 섬네일을 생성할 수 있습니다.

>[!NOTE]
>
>Campaign 사용자 인터페이스에서 랜딩 페이지 미리 보기를 표시하려면 애플리케이션 서버 URL의 보안이 유지되어야 합니다. 이 경우, [브랜드를 구성](../../administration/using/branding.md#configuring-and-using-brands)할 때 http://가 아닌 https://를 사용하여 이 URL을 설정합니다.

## 유효성 매개 변수 설정 {#setting-up-validity-parameters}

게시 전에는 보안 및 플랫폼 성능을 위하여 랜딩 페이지 속성에 만료 날짜를 설정하기를 강력히 추천합니다. 선택한 날짜에 해당 랜딩 페이지가 자동으로 게시 취소됩니다. 방법은 다음과 같습니다.

1. 랜딩 페이지 대시보드의 ![](assets/edit_darkgrey-24px.png) 버튼을 통해 액세스되는 랜딩 페이지 속성을 편집합니다.

   ![](assets/lp_edit_properties_button.png)

1. **[!UICONTROL Publication]** 섹션에서 만료 날짜 및 시간을 설정합니다. 지정한 날짜에 자동으로 랜딩 페이지의 게시가 취소되어 더 이상 사용할 수 없게 됩니다.

   이 날짜 및 시간에 대해 고려할 시간대를 선택할 수 있습니다.

1. 비활성 랜딩 페이지에 액세스하려고 할 때 방문자를 리디렉션할 리디렉션 URL을 정의합니다.

   ![](assets/lp_settings_general.png)

>[!IMPORTANT]
>
>배포 날짜와 시간을 정의할 수도 있습니다. 그러면 랜딩 페이지가 지정한 날짜에 자동으로 게시됩니다.

## 랜딩 페이지 게시 {#publishing-a-landing-page}

랜딩 페이지를 게시하면 랜딩 페이지는 실제로 사용 가능한 상태가 되어 방문자가 액세스할 수 있습니다.

**[!UICONTROL Publish]** 버튼을 통해 언제든지 랜딩 페이지 게시를 취소하거나 업데이트하여 다시 게시할 수 있습니다. 그러나 다시 게시하기에 실패하고 랜딩 페이지의 게시도 아직 취소하지 않은 경우, 첫 번째 버전이 온라인 상태로 유지됩니다.
