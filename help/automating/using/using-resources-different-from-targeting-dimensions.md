---
title: 타기팅 차원과 다른 리소스 사용
description: 타겟팅 차원과 다른 리소스를 사용하는 방법을 알아봅니다.
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: query,main
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: 5805bdfa-fb33-4a46-ba1e-7a10b067349b
source-git-commit: 9c14fc3de60d8e0304f8a7ebd46e7be34d2e0499
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 76%

---

# 타기팅 차원과 다른 리소스 사용 {#using-resources-different-from-targeting-dimensions}

이 사용 사례에서는 타깃팅 차원과 다른 리소스를 사용하여(예: 떨어진 표에 있는 특정 레코드를 찾는) 방법을 제공합니다.

타겟팅 차원 및 리소스에 대한 자세한 내용은 다음을 참조하십시오. [이 섹션](../../automating/using/query.md#targeting-dimensions-and-resources)

**예제 1: &quot;Welcome back !&quot;이라는 레이블이 있는 게재가 타겟팅한 프로필 확인**.

* 이 경우 프로필을 타겟팅하려고 합니다. 타겟팅 차원을 **[!UICONTROL Profiles (profile)]**(으)로 설정합니다 .
* 선택한 프로필을 게재의 레이블에 따라 필터링하려고 합니다. 따라서 리소스를 **[!UICONTROL Delivery logs]**(으)로 설정합니다 . 이 방법으로 게재 로그 표에서 직접 필터링하여 더 나은 성능을 제공합니다.

![](assets/targeting_dimension6.png)

![](assets/targeting_dimension7.png)

**예제 2: &quot;Welcome back !&quot;이라는 레이블이 있는 게재가 타겟팅하지 않은 프로필 확인**

앞의 예제에서는 타겟팅 차원과 다른 리소스를 사용했습니다. 이와 같은 작업은 떨어진 표(앞의 예제에서는 게재 로그)에 **존재하는** 레코드를 찾으려는 경우에만 가능합니다.

떨어진 표에 **존재하지 않는** 레코드(예: 특정 게재의 대상이 아닌 프로필)를 찾으려면 리소스와 타겟팅 차원이 동일해야 합니다. 해당 레코드가 떨어진 표(게재 로그)에 존재하지 않기 때문입니다.

* 이 경우 프로필을 타겟팅하려고 합니다. 타겟팅 차원을 **[!UICONTROL Profiles (profile)]**(으)로 설정합니다 .
* 선택한 프로필을 게재의 레이블에 따라 필터링하려고 합니다. 게재 로그 표에 없는 레코드를 찾고 있으므로, 게재 로그에서 직접 필터링할 수 없습니다. 따라서 리소스를 **[!UICONTROL Profile (profile)]**(으)로 설정하고 프로필 표에 쿼리를 작성합니다.

![](assets/targeting_dimension8.png)

![](assets/targeting_dimension9.png)
