---
title: 랜딩 페이지 정보
seo-title: 랜딩 페이지 정보
description: 랜딩 페이지 정보
seo-description: 캠페인 랜딩 페이지와 라이프사이클을 검색합니다.
page-status-flag: 활성화 안 함
uuid: b316bf47-7d98-46fa-ab4f-67ff50de8095
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 채널
content-type: reference
topic-tags: 랜딩 페이지
discoiquuid: ca8d1698-6e8a-4f5a-b017-74a152e14286
context-tags: landingPage,wizard;landingPage,overview;landingPage,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 0068746b0b90b85edfb2c93eb08a82e1adc2fca8

---


# 랜딩 페이지 정보{#about-landing-pages}

Campaign에는 고객 정보를 캡처하고, 서비스에 구독을 제공하고, 데이터를 표시하고, 데이터베이스를 확장하는 데 사용할 수 있는 웹 양식인 랜딩 페이지가 포함되어 있습니다. 랜딩 페이지는 기존 프로필을 가져오거나 업데이트하는 데에도 사용할 수 있습니다.

랜딩 페이지를 설정하는 데 필요한 단계에 대한 자세한 내용은 [이 섹션을 참조하십시오](../../channels/using/main-steps-to-set-up-a-landing-page.md)

**관련 항목:**

* [랜딩 페이지 만들기 자습서 비디오](https://helpx.adobe.com/campaign/kt/acs/using/acs-create-edit-landing-page-feature-video-use.html) 비디오
* [랜딩 페이지를 사용하여 서비스 구독](../../audiences/using/creating-a-service.md)

## 랜딩 페이지 라이프사이클 {#landing-pages-life-cycle}

랜딩 페이지의 전체 수명 주기는 다음과 같습니다.

1. 제작:랜딩 페이지의 컨텐츠를 디자인하고 설정합니다.
1. 테스트:테스트 프로필에서 랜딩 페이지 실행을 시뮬레이션합니다.
1. 게시:랜딩 페이지를 게시하여 라이브로 푸시합니다.
1. 만료 또는 게시 취소:수동으로 게시 취소 또는 랜딩 페이지가 만료될 때까지 기다렸다가 더 이상 사용할 수 없습니다.

![](assets/lp_livecycle.png)

작성 및 게시한 후에는 웹 사이트를 통해 랜딩 페이지에 액세스하거나 랜딩 페이지에 대한 직접 링크를 이메일에 [삽입하여 랜딩 페이지에 액세스할 수 있도록 만들](../../designing/using/links.md#inserting-a-link)수 있습니다.

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
