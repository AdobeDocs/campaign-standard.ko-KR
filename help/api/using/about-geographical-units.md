---
solution: Campaign Standard
product: campaign
title: 지리적 단위 정보
description: 지역 단위 및 API에 대한 자세한 내용을 살펴보십시오.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
translation-type: tm+mt
source-git-commit: ad7322905c69f9575e11efc9d8f68cf909dc425f
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---


# 지리적 단위 {#about-geographical-units} 정보

>[!CAUTION]
>
>지리적 단위 기능은 Campaign Standard 18.7 릴리스에서 더 이상 사용되지 않습니다.
>
>따라서 지리학적 단위가 만들어지지 않은 기존 인스턴스는 물론 새 Campaign Standard 인스턴스는 18.7 릴리스부터 이 기능을 구현할 수 없습니다.
>
>자세한 내용은 <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/release-notes/deprecated-features.html">더 이상 사용되지 않는 기능</a> 페이지를 참조하십시오.

**geoUnitBase** 종단점을 사용하면 지리적 단위와 상호 작용하여 속성을 업데이트하거나 프로필 단위를 업데이트할 수 있습니다.

프로필 리소스를 확장할 때 **지리적 단위** 필드가 프로필에 추가됩니다. 따라서 지리적 단위와 상호 작용하려면 항상 **profileAndServicesExt** 끝점을 사용해야 합니다. 프로필의 리소스 확장명에 대한 자세한 내용은 [캠페인 설명서](https://helpx.adobe.com/campaign/standard/administration/using/organizational-units.html#partitioning-profiles)를 참조하십시오.
