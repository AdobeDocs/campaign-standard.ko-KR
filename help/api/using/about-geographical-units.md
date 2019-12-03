---
title: 지리적 단위 정보
description: 지리적 단위 및 API에 대한 자세한 내용을 살펴보십시오.
page-status-flag: never-activated
uuid: c7b9c171-0409-4707-9d45-3fa72aee8008
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
discoiquuid: 304e7779-42d2-430a-9704-8c599a4eb1da
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: aee0e0437cbfe578cb2f715a2433099c79dd1748

---


# 지리적 단위 정보 {#about-geographical-units}

>[!CAUTION]
>
>지리적 단위 기능은 Campaign Standard 18.7 릴리스에서 더 이상 사용되지 않습니다.
따라서 새 Campaign Standard 인스턴스와 지리적 단위를 만들지 않은 기존 인스턴스는 18.7 릴리스부터 이 기능을 구현할 수 없습니다.
자세한 내용은 더 이상 사용되지 않는 <a href="https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html">기능</a> 페이지를 참조하십시오.

geoUnit **Base** 종단점을 사용하면 지리적 단위와 상호 작용하여 속성을 업데이트하거나 프로필 단위를 업데이트할 수 있습니다.

프로필 **리소스를** 확장할 때 지리적 단위 필드가 프로필에 추가됩니다. 따라서 항상 profileAndServicesExt **끝점을 사용하여 지리적** 단위와 상호 작용해야 합니다. 프로필의 리소스 확장에 대한 자세한 내용은 Campaign [설명서를 참조하십시오](https://helpx.adobe.com/campaign/standard/administration/using/organizational-units.html#partitioning-profiles).
