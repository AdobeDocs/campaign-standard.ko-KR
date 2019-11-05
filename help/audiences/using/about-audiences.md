---
title: 대상자 기본 정보
description: 쿼리, 목록 또는 파일에서 대상을 빌드하는 방법과 Adobe Experience Cloud에서 대상을 가져오는 방법을 알아봅니다.
page-status-flag: 활성화 안 함
uuid: b399642-96ec-489e-b146-c8c2cb52aa32
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: 고객 관리
discoiquuid: 750ecd8d-67a5-4180-bfec-2a8e3098c812
context-tags: 대상,마법사;대상,개요;전달,대상,뒤로
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 대상자 기본 정보{#about-audiences}

대상은 규칙과 속성을 기반으로 하는 프로파일 목록입니다.

Adobe Campaign을 사용하면 쿼리를 사용하거나 전용 워크플로우를 사용하여 고객을 수동으로 만들 수 있습니다. Adobe Experience Cloud에서 공유 대상을 사용할 수도 있습니다. 모든 대상은 Adobe Campaign 홈 페이지의 **[!UICONTROL Audiences]** 카드나 **[!UICONTROL Audiences]** 링크를 통해 액세스할 수 있는 목록으로 다시 그룹화됩니다.

![](assets/audience_1.png)

Adobe Campaign에서 다양한 대상 유형을 조작할 수 있습니다. 대상의 유형은 대상이 만들어진 방식에 따라 달라집니다.

* **[!UICONTROL Query]**:대상 목록의 Adobe Campaign 데이터베이스의 데이터에 대한 [쿼리에서](../../automating/using/editing-queries.md#about-query-editor) 대상이 생성되었음을 나타냅니다. 쿼리에 의해 정의된 대상은 추가로 사용할 때마다 다시 계산됩니다.
* **[!UICONTROL List]**:대상이 고정 프로파일 목록임을 나타냅니다. 이러한 목록은 [워크플로우에서](../../automating/using/discovering-workflows.md)만들어지며, 여기에서 대상을 저장할 때 데이터 차원이 알려져 있습니다. 예를 들어, 타깃팅 활동(특히 **[!UICONTROL Query]** ) 이후나 파일에서 가져온 데이터의 조정 이후입니다.
* **[!UICONTROL File]**:대상이 [파일 가져오기](../../automating/using/load-file.md) 워크플로우에서 직접 만들어졌고 대상을 저장할 때 데이터 차원을 알 수 없음을 나타냅니다.
* **[!UICONTROL Experience Cloud]**:대상을 Adobe Experience Cloud에서 가져왔다고 나타냅니다. 이 옵션은 대상 공유 기능이 구성된 경우에만 사용할 수 있습니다. 자세한 내용은 Adobe Experience [Cloud에서 대상 가져오기를 참조하십시오](../../integrating/using/sharing-audiences-with-audience-manager-or-people-core-service.md#importing-an-audience).

![](assets/audience_type_selection.png)

