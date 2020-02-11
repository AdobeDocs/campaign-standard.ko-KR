---
title: 랜딩 페이지 공유
description: Adobe Campaign에서 랜딩 페이지를 테스트하고 게시하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: fb7b087a-3292-496c-bc41-2e3012bacf59
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: landing-pages
discoiquuid: f7d4bb71-f957-4f86-97c7-8ac0a0030026
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 54612511de07edc3e6f3eea34ef095c26b35f4af

---


# 랜딩 페이지 테스트 및 게시{#testing-publishing--landing-page}

## 랜딩 페이지 게시 정보 {#about-landing-page-publication}

랜딩 페이지를 게시하기 전에 테스트를 수행해야 합니다.실행을 검증하고, 액세스를 구성하고, 랜딩 페이지의 수명 종료를 설정합니다. 이러한 단계는 전제 조건이며 신중하게 실행해야 합니다.

## 랜딩 페이지 테스트 {#testing-the-landing-page-}

랜딩 페이지가 플랫폼과 데이터에 영향을 주므로 실행을 신중하게 테스트해야 합니다. 이렇게 하려면:

1. 랜딩 페이지의 작업 표시줄에 있는 **[!UICONTROL Test]** 단추를 클릭합니다.
1. 테스트 화면에서 테스트 프로파일을 선택하고 랜딩 페이지가 구독을 관리하는 경우 테스트 서비스를 선택합니다.

   ![](assets/lp_test_2.png)

1. 필드에 데이터를 입력하고 옵션을 선택합니다.
1. 랜딩 페이지를 제출하고 데이터베이스에서 업데이트를 확인합니다.

   >[!IMPORTANT]
   >
   >양식이 제출되면 사용된 서비스 및 프로필이 업데이트됩니다.

1. 다양한 프로파일과 데이터를 사용하여 이 과정을 반복합니다.

   이 화면에서 랜딩 페이지 축소판을 생성할 수도 있습니다.

>[!NOTE]
>
>Campaign 사용자 인터페이스에 랜딩 페이지 미리 보기를 표시하려면 응용 프로그램 서버 URL이 안전해야 합니다. 이러한 경우, 브랜드를 [구성할 때 이 URL을 설정하려면 http://이 아닌 https://을 사용하십시오](../../administration/using/branding.md#configuring-and-using-brands).

## 유효성 매개 변수 설정 {#setting-up-validity-parameters}

게시하기 전에 보안상의 이유 및 플랫폼 성능 때문에 랜딩 페이지 속성에서 만료 날짜를 설정하는 것이 좋습니다. 선택한 날짜에 랜딩 페이지는 자동으로 게시 취소됩니다. 이렇게 하려면:

1. 랜딩 페이지 대시보드의 ![](assets/edit_darkgrey-24px.png) 단추를 통해 액세스한 랜딩 페이지 속성을 편집합니다.

   ![](assets/lp_edit_properties_button.png)

1. 다음 **[!UICONTROL Publication]** 섹션에서 만료 날짜 및 시간을 설정합니다.랜딩 페이지는 지정된 날짜에 자동으로 게시 취소되므로 더 이상 사용할 수 없습니다.

   이 날짜 및 시간을 고려할 시간대를 선택할 수 있습니다.

1. 비활성 랜딩 페이지에 액세스하려고 할 때 방문자를 리디렉션하도록 리디렉션 URL을 정의합니다.

   ![](assets/lp_settings_general.png)

>[!IMPORTANT]
>
>배포 날짜 및 시간을 정의할 수도 있습니다.그러면 랜딩 페이지가 지정된 날짜에 자동으로 게시됩니다.

## 랜딩 페이지 게시 {#publishing-a-landing-page}

랜딩 페이지를 게시하면 라이브로 이동하고 방문자가 액세스할 수 있습니다.

랜딩 페이지를 언제든지 **[!UICONTROL Publish]** 단추를 통해 게시 취소 또는 업데이트하거나 다시 게시할 수 있습니다. 그러나 재게시에 실패하고 랜딩 페이지의 게시를 아직 완료하지 않은 경우 첫 번째 버전은 온라인 상태로 유지됩니다.
