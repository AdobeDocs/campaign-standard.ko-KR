---
title: 데이터 저장 및 조정
seo-title: 데이터 저장 및 조정
description: 데이터 저장 및 조정
seo-description: Adobe Campaign 에서는 사용자가 랜딩 페이지에 입력한 데이터를 한 번 제출한 방법을 정의할 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 5 B 222 EA 2-6628-457 F-A 618-BFC 0 E 5 EB 93 DD
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 채널
content-type: 참조
topic-tags: 랜딩 페이지
discoiquuid: 899 c 7152-F 415-4 DF 9-B 4 B 4-5 FF 3470 A 4 E 32
context-tags: landingpage, main
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: d50d486ed77cb7989df47133bb49fde3227ae3a5

---


# Data storage and reconciliation{#data-storage-and-reconciliation}

데이터 조정 매개 변수를 사용하면 사용자가 랜딩 페이지에서 입력한 데이터를 한 번 제출한 방법을 정의할 수 있습니다.

이렇게 하려면:

1. Edit the landing page properties accessed via the ![](assets/edit_darkgrey-24px.png) icon in the landing page dashboard, and display the **[!UICONTROL Job]** parameters.

   ![](assets/lp_parameters_4.png)

1. Select the **[!UICONTROL Reconciliation key]**: these database fields (for example: email, first name, last name) are used to determine whether the visitor has a profile that is already known in the Adobe Campaign database. 이렇게 하면 정의된 업데이트 전략 매개 변수에 따라 프로필을 업데이트하거나 만들 수 있습니다.
1. Define the **[!UICONTROL Form parameter mapping]**: this section allows you to map the landing page field parameters and those used in the reconciliation key.
1. Select the **[!UICONTROL Update strategy]**: if the reconciliation key recovers an existing database profile, you can choose for this profile to be updated with the data entered in the form or instead prevent this update.

