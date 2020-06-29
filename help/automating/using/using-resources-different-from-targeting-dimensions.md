---
title: 타깃팅 차원과 다른 리소스 사용
description: 타깃팅 차원과 다른 리소스를 사용하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: b3c629fa-370e-481c-b347-fcf9f5a5e847
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: 8d46ce28-0101-4f13-865a-2208ed6d6139
context-tags: query,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: f3a668860659e40645ce3e4aab879cae5ad90083
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---


# 타깃팅 차원과 다른 리소스 사용 {#using-resources-different-from-targeting-dimensions}

이 사용 사례에서는 타깃팅 차원과 다른 리소스를 사용하는 방법(예: 먼 테이블에서 특정 레코드를 찾는 방법)을 보여 줍니다.

차원 및 리소스 타깃팅에 대한 자세한 내용은 [이 섹션을 참조하십시오.](../../automating/using/query.md#targeting-dimensions-and-resources)

**예 1: &quot;Welcome back !&quot;이라는 레이블이 있는 배달에서 타깃팅된 프로파일을 식별합니다**.

* 이 경우 프로파일을 타깃팅하려고 합니다. 타깃팅 차원을 다음으로 설정합니다 **[!UICONTROL Profiles (profile)]**.
* 배달 레이블에 따라 선택한 프로필을 필터링하려고 합니다. 따라서 리소스를 다음으로 설정할 것입니다 **[!UICONTROL Delivery logs]**. 이렇게 해서 배달 로그 테이블에서 바로 필터링하여 더 나은 성과를 제공합니다.

![](assets/targeting_dimension6.png)

![](assets/targeting_dimension7.png)

**예 2: &quot;Welcome back!&quot;이라는 레이블이 있는 배달에서 타깃팅되지 않은 프로파일을 식별합니다.**

이전 예에서 타깃팅 차원과 다른 리소스를 사용했습니다. 이 작업은 먼 테이블에 있는 레코드 **를 찾으려는** 경우에만 가능합니다(예: 배달 로그).

멀리 떨어진 테이블 **에 없는 레코드(예: 특정 게재의 대상이 아닌 프로파일)를 찾으려면 동일한 리소스 및 타깃팅 차원을 사용해야** 합니다. 해당 레코드가 먼 테이블(배달 로그)에 존재하지 않기 때문입니다.

* 이 경우 프로파일을 타깃팅하려고 합니다. 타깃팅 차원을 다음으로 설정합니다 **[!UICONTROL Profiles (profile)]**.
* 배달 레이블에 따라 선택한 프로필을 필터링하려고 합니다. 배달 로그 테이블에 없는 레코드를 찾고 있으므로 배달 로그에 직접 필터링할 수 없습니다. 따라서 프로필 테이블에서 리소스를 설정하고 쿼리를 **[!UICONTROL Profile (profile)]** 작성합니다.

![](assets/targeting_dimension8.png)

![](assets/targeting_dimension9.png)
