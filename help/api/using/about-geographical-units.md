---
solution: Campaign Standard
product: campaign
title: 지리적 단위 정보
description: 지역 단위 및 API에 대한 자세한 내용을 살펴보십시오.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 3%

---


# 지리적 단위 정보 {#about-geographical-units}

>[!CAUTION]
>
>지리적 단위 기능은 Campaign Standard 18.7 릴리스에서 더 이상 사용되지 않습니다.
>
>따라서 지리학적 단위가 만들어지지 않은 기존 인스턴스는 물론 새 Campaign Standard 인스턴스는 18.7 릴리스부터 이 기능을 구현할 수 없습니다.
>
>자세한 내용은 더 이상 사용되지 않는 기능 <a href="https://helpx.adobe.com/kr/campaign/kb/acs-deprecated-and-removed-features.html">페이지를 참조하십시오</a> .

geoUnitBase **종단점을 사용하면 지리적 단위와 상호 작용하여 속성을 업데이트하거나 프로필 단위를 업데이트할 수** 있습니다.

프로필 리소스를 확장할 때 **지리적 단위** 필드가 프로필에 추가됩니다. 따라서 **profileAndServicesExt** 끝점을 항상 사용하여 지리적 단위와 상호 작용해야 합니다. 프로필의 리소스 확장명에 대한 자세한 내용은 [캠페인 설명서를 참조하십시오](https://helpx.adobe.com/campaign/standard/administration/using/organizational-units.html#partitioning-profiles).
