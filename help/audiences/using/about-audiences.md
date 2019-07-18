---
title: 대상 정보
seo-title: 대상 정보
description: 대상 정보
seo-description: 쿼리, 목록 또는 파일에서 대상을 구축하는 방법과 Adobe Experience Cloud에서 가져오는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: B 3996642-96 EC -489 E-B 146-C 8 C 2 CB 52 AA 32
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 대상
content-type: 참조
topic-tags: 관리 대상
discoiquuid: 750 ECD 8 D -67 A 5-4180-BFEC -2 A 8 E 3098 C 812
context-tags: 대상, 마법사; 고객, 개요,전달, 고객, 뒤로
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 6a877d878f01fa1e541dc20b8b0941602113d15b

---


# About audiences{#about-audiences}

대상자는 규칙 및 속성에 기반한 프로필 목록입니다.

Adobe Campaign를 사용하면 쿼리를 사용하거나 전용 워크플로우를 통해 자동으로 대상을 만들 수 있습니다. Adobe Experience Cloud의 공유 고객을 사용할 수도 있습니다. All of the audiences are regrouped into a list that can be accessed via the **[!UICONTROL Audiences]** card on the Adobe Campaign home page or from the **[!UICONTROL Audiences]** link.

![](assets/audience_1.png)

Adobe Campaign에서 다른 대상 유형을 조작할 수 있습니다. 대상 유형은 만들어진 방법과 일치합니다.

* **[!UICONTROL Query]**: 대상 목록에서 Adobe Campaign 데이터베이스의 데이터에 [대한 쿼리에서](../../automating/using/editing-queries.md#about-query-editor) 대상이 작성되었음을 나타냅니다. 쿼리에 의해 정의된 대상은 각 추가 사용시 다시 계산됩니다.
* **[!UICONTROL List]**: 대상이 고정 프로필 목록임을 나타냅니다. These lists are created in a [workflow](../../automating/using/discovering-workflows.md), where the data dimension is known when saving the audience. For example, after targeting activities (especially **[!UICONTROL Query]** ) or after the reconciliation of data imported from a file.
* **[!UICONTROL File]**: 대상이 [파일 가져오기](../../automating/using/load-file.md) 워크플로우에서 직접 작성되었으며 대상을 저장할 때 데이터 차원을 알 수 없음을 나타냅니다.
* **[!UICONTROL Experience Cloud]**: 대상을 Adobe Experience Cloud에서 가져왔음을 나타냅니다. 이 옵션은 대상 공유 기능이 구성된 경우에만 사용할 수 있습니다. For more information, see [Importing an audience from the Adobe Experience Cloud](../../integrating/using/sharing-audiences-with-audience-manager-or-people-core-service.md#importing-an-audience).

![](assets/audience_type_selection.png)

