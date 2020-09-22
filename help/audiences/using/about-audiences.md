---
title: 대상자 기본 정보
description: 쿼리, 목록 또는 파일에서 대상자를 만드는 방법과 Adobe Experience Cloud에서 대상자를 가져오는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: b3996642-96ec-489e-b146-c8c2cb52aa32
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: managing-audiences
discoiquuid: 750ecd8d-67a5-4180-bfec-2a8e3098c812
context-tags: audience,wizard;audience,overview;delivery,audience,back
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c1147c4512b1485ae5d927a32970adcd41b540e7
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 91%

---


# 대상자 기본 정보{#about-audiences}

대상자는 규칙과 속성을 기반으로 하는 프로필 목록입니다.

Adobe Campaign에서는 수동으로 쿼리를 사용하거나 자동으로 전용 워크플로우를 사용하여 대상자를 만들 수 있습니다. Adobe Experience Cloud에서 공유한 대상자를 사용할 수도 있습니다. 모든 대상자는 목록으로 다시 그룹화되어 Adobe Campaign 홈페이지의 **[!UICONTROL Audiences]** 카드나 **[!UICONTROL Audiences]** 링크를 통해 사용할 수 있습니다.

![](assets/audience_1.png)

Adobe Campaign에서 다양한 대상자 유형을 조정할 수 있습니다. 대상자 유형은 대상자를 만든 방식에 따라 다릅니다.

* **[!UICONTROL Query]**:대상 목록을 통해 Adobe Campaign 데이터베이스의 데이터에 대한 [쿼리를](../../automating/using/editing-queries.md#about-query-editor) 사용하여 대상을 만들었음을 나타냅니다. 쿼리로 정의한 대상자는 이후 사용할 때마다 다시 계산됩니다.
* **[!UICONTROL List]**: 대상자가 고정 프로필 목록이라는 것을 나타냅니다. 이 목록은 대상자를 저장할 때 데이터 차원이 알려진 [워크플로우](../../automating/using/get-started-workflows.md)에서 만듭니다. 타겟팅 활동(특히 **[!UICONTROL Query]**) 이후나 파일에서 가져온 데이터의 조정 이후를 예로 들 수 있습니다.
* **[!UICONTROL File]**: 대상자를 [파일 가져오기](../../automating/using/load-file.md) 워크플로우에서 직접 만들었고 대상자를 저장할 때 데이터 차원을 알 수 없었다는 것을 나타냅니다.
* **[!UICONTROL Experience Cloud]**: 대상자를 Adobe Experience Cloud에서 가져왔다는 것을 나타냅니다. 이 옵션은 대상자 공유 기능을 구성해야만 사용할 수 있습니다. 자세한 내용은 [Adobe Experience Cloud에서 대상자 가져오기](../../integrating/using/sharing-audiences-with-audience-manager-or-people-core-service.md#importing-an-audience)를 참조하십시오.

![](assets/audience_type_selection.png)
