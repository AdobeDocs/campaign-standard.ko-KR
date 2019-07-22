---
title: 랜딩 페이지 제한 사항
seo-title: 랜딩 페이지 제한 사항
description: 랜딩 페이지 제한 사항
seo-description: 캠페인 랜딩 페이지와 라이프사이클 검색
page-status-flag: 정품 인증 안 함
uuid: B 316 BF 47-7 D 98-46 FA-AB 4 F -67 FF 50 DE 8095
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 채널
content-type: 참조
topic-tags: 랜딩 페이지
discoiquuid: CA 8 D 1698-6 E 8 A -4 F 5 A-B 017-74 A 152 E 14286
context-tags: landingpage, wizard; landingpage, 개요; landingpage, main
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 5dbb89eca363f252d0c69126878d4f79320e0f19

---


# Landing page limitations{#landing-page-limitations}

**데이터 작성 및 업데이트**

* Landing pages are limited to **[!UICONTROL Profile]** and **[!UICONTROL Subscription]** resources only. Record can be saved and updated from **[!UICONTROL Profile]** and a subscription/unsubscription to a **[!UICONTROL Service]**.
To learn more on resources configuration, see [Configuring the resource's data structure](../../developing/using/configuring-the-resource-s-data-structure.md).

>[!CAUTION]
>
>A landing page cannot display or update data from any other resource than **[!UICONTROL Profile]** and **[!UICONTROL Subscription]**.

**Preloading**

* 랜딩 페이지는 자동으로 레코드 목록을 표시할 수 없으며 이미 가입된 서비스는 목록 서비스를 표시할 수 없습니다. For more information on services, refer to this [page](../../audiences/using/creating-a-service.md).

* 사전 채워진 양식 (데이터가 페이지에 미리 로드됨) 이 있는 랜딩 페이지는 Adobe Campaign 이메일에서만 액세스할 수 있습니다. 웹 사이트 페이지에서 이러한 양식에 액세스할 수 없습니다.

**조정**

* 조정 동작은 다음과 같습니다. 일치 항목이 발견되면 조정 프로세스가 중지됩니다. 즉, 중복이 있을 때 한 프로필 레코드에 대해서만 조정이 수행되고 여러 레코드가 되지 않을 수 있습니다.

예를 들어 다음 획득 랜딩 페이지를 프로필로 전송하여 프로필의 모바일 번호로 캠페인 데이터베이스를 업데이트할 수 있습니다.

![](assets/landing_page_limitation_1.png)

프로필 중 하나에 새 정보가 있지만 이미 중복된 프로필이 있는 랜딩 페이지가 있는 경우 프로필 작성 날짜에 따라 프로필 우선 순위가 우선 순위가 지정되므로 가장 빠른 작성 날짜와 일치하는 프로필이 업데이트됩니다.

가장 오래된 프로필인 첫 번째 프로필만 업데이트되었습니다.

![](assets/landing_page_limitation_2.png)

**랜딩 페이지 테스트**

* 랜딩 페이지는 프로필에만 작동하고 테스트 프로필은 아닙니다. 랜딩 페이지는 이메일 확인서의 일부로 테스트할 수 없음을 의미합니다.
