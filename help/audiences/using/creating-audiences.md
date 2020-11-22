---
solution: Campaign Standard
product: campaign
title: 대상자 만들기
description: Adobe Campaign에서 대상자를 만드는 방법을 알아봅니다.
audience: audiences
content-type: reference
topic-tags: managing-audiences
context-tags: readAudience,main;audience,overview;delivery,audience,back
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '969'
ht-degree: 100%

---


# 대상자 만들기{#creating-audiences}

## 쿼리 대상자 만들기 {#creating-query-audiences}

이 섹션에서는 **쿼리** 대상자를 만드는 방법을 설명합니다. 파일을 가져오거나 [워크플로우](../../automating/using/get-started-workflows.md)에서 타겟팅하여 대상자를 만들 수도 있습니다.

대상자 목록에서 Adobe Campaign 프로필에 대한 쿼리를 수행하거나 Adobe Experience Cloud 대상자를 가져와 대상자를 만들 수 있습니다.

1. **[!UICONTROL Audiences]** 탭이나 카드를 통해 대상자 목록으로 이동합니다.

   ![](assets/audiences_query_1.png)

1. **[!UICONTROL Create]**&#x200B;을(를) 선택하여 새 대상자 만들기 화면에 액세스합니다.

   ![](assets/audiences_query.png)

1. 대상자의 이름을 지정합니다. 대상자 레이블은 대상자 목록과 쿼리 도구 팔레트에서 사용됩니다.
1. **[!UICONTROL Query]** 대상자 유형을 선택합니다. 쿼리로 정의한 대상자는 다시 사용할 때마다 다시 계산됩니다.

   ![](assets/audience_type_selection.png)

1. 그런 다음 고객을 필터링하는 데 사용할 **[!UICONTROL Targeting dimension]**&#x200B;을(를) 선택합니다. 각 대상자는 단일 타겟팅 차원으로 구성됩니다. 예를 들어 프로필, 테스트 프로필 및 구독자를 모두 적용하여 한 대상자를 만들 수는 없습니다. 타겟팅 차원에 대한 자세한 정보는 [이 페이지](../../automating/using/query.md#targeting-dimensions-and-resources)를 참조하십시오.
1. 대상자 모집단을 정의하는 쿼리를 만듭니다. [쿼리 편집](../../automating/using/editing-queries.md) 섹션을 참조하십시오.
1. **[!UICONTROL Create]** 버튼을 클릭하여 대상자를 저장합니다.

>[!NOTE]
>
>**[!UICONTROL Edit properties]** 아이콘을 통해 이 대상자에 대한 설명을 추가하고 액세스 권한을 정의할 수 있습니다.

## 목록 대상자 만들기 {#creating-list-audiences}

이 섹션에서는 워크플로우에서 타겟팅 후 **목록** 대상자를 만드는 방법을 설명합니다. 파일을 [워크플로우](../../automating/using/get-started-workflows.md)로 가져오거나 **[!UICONTROL Audiences]** 메뉴에서 쿼리를 통해 대상자를 만들 수도 있습니다.

**목록** 대상자를 만들려면 다음 단계를 수행합니다.

1. **마케팅 활동** 탭에서 **만들기**&#x200B;를 클릭하고 **워크플로우**&#x200B;를 선택합니다.

   ![](assets/audiences_list_1.png)

1. 끌어다 놓은 뒤 타겟팅 활동을 구성하면 **알려진** 차원이 있는 모집단을 선택할 수 있습니다. 사용 가능한 활동 목록 및 구성은 [타겟팅 활동](../../automating/using/about-targeting-activities.md) 섹션에 자세히 설명되어 있습니다.

   **[!UICONTROL Query]** 활동을 사용하거나, **[!UICONTROL Load file]** 활동을 사용하여 데이터를 가져온 뒤 **[!UICONTROL Reconciliation]** 활동을 사용하여 가져온 데이터의 차원을 확인할 수 있습니다. 여기서는 **[!UICONTROL Query]** 활동으로 스포츠 뉴스레터를 구독한 수신자를 타겟팅하려고 합니다.

   ![](assets/audiences_list_2.png)

1. 타겟팅 후 **[!UICONTROL Save audience]** 활동을 워크플로우로 끌어서 놓습니다. 예를 들어 **[!UICONTROL Create or update an audience]**&#x200B;을(를) 선택하면 대상자를 만든 뒤 새로운 데이터로 대상자를 자동으로 업데이트할 수 있습니다. 이 경우 워크플로우 맨 앞부분에 **[!UICONTROL Scheduler]** 활동을 추가합니다.

   이 활동 구성에 대한 자세한 내용은 [대상자 저장](../../automating/using/save-audience.md) 섹션을 참조하십시오.

   ![](assets/audiences_list_3.png)

1. 워크플로우를 저장하고 시작합니다.

   알려진 차원이 있는 타겟팅 다음에 **[!UICONTROL Save audience]**&#x200B;을(를) 배치했으므로, 이 활동을 통해 만든 대상자는 **목록** 대상자입니다.

   저장한 대상자의 콘텐츠는 대상자 목록을 통해 액세스할 수 있는 대상자 자세히 보기에서 사용할 수 있습니다. 이 보기에서 사용할 수 있는 열은 워크플로우 저장 활동의 인바운드 전환 열에 해당합니다. 가져온 파일의 열, 쿼리에서 추가한 데이터를 예로 들 수 있습니다.

   ![](assets/audiences_list_4.png)

## 파일 대상자 만들기 {#creating-file-audiences}

이 섹션에서는 파일을 워크플로우로 가져와서 **파일** 대상자를 만드는 방법에 대해 자세히 설명합니다. [워크플로우](../../automating/using/get-started-workflows.md)의 타겟팅 활동 또는 **[!UICONTROL Audiences]** 메뉴의 쿼리를 통해 대상자를 만들 수도 있습니다.

**파일** 대상자를 만들려면 다음 단계를 수행합니다.

1. **마케팅 활동** 탭에서 **만들기**&#x200B;를 클릭하고 **워크플로우**&#x200B;를 선택합니다.
1. 끌어다 놓은 뒤 **[!UICONTROL Load file]** 활동을 구성하면 활동 실행 시 **알 수 없는** 차원이 있는 모집단을 가져올 수 있습니다. 이 활동 구성에 대한 자세한 내용은 [파일 로드](../../automating/using/load-file.md) 섹션을 참조하십시오.

   ![](assets/audience_files_1.png)

1. **[!UICONTROL Save audience]** 활동을 **[!UICONTROL Load file]** 활동 뒤에 끌어다 놓습니다. 이 활동 구성에 대한 자세한 내용은 [대상자 저장](../../automating/using/save-audience.md) 섹션을 참조하십시오.
1. 워크플로우를 저장하고 시작합니다.

   ![](assets/audience_files_2.png)

   가져오기 다음에 **[!UICONTROL Save audience]**&#x200B;을(를) 배치했으므로, 데이터 차원은 알 수 없으며 이 활동을 통해 만든 대상자는 **파일** 대상자입니다.

   저장한 대상자의 콘텐츠는 대상자 목록을 통해 액세스할 수 있는 대상자 자세히 보기에서 사용할 수 있습니다. 이 보기에서 사용할 수 있는 열은 워크플로우 저장 활동의 인바운드 전환 열에 해당합니다. 가져온 파일의 열, 쿼리에서 추가한 데이터를 예로 들 수 있습니다.

   ![](assets/audience_files_3.png)

## Experience Cloud 대상자 만들기 {#creating-experience-cloud-audiences}

Adobe Campaign에서는 Adobe Experience Cloud를 통해 대상자를 공유하고 교환할 수 있습니다. **[!UICONTROL Import shared audience]** 기술 워크플로우로 **Experience Cloud** 유형 대상자를 People 핵심 서비스에서 Adobe Campaign으로 직접 가져옵니다.

Adobe Campaign의 프로필을 쿼리하는 **쿼리** 유형 대상자와 달리, **Experience Cloud** 대상자는 방문자 ID 목록으로 구성됩니다.

이렇게 통합하려면 먼저 구성해야 합니다. People 핵심 서비스로 대상자를 가져오거나 내보내는 방법 및 구성에 대한 자세한 내용은 다음 [섹션](../../integrating/using/sharing-audiences-with-audience-manager-or-people-core-service.md)을 참조하십시오.

![](assets/audience_peoplecore.png)

## 대상자 편집 {#editing-audiences}

대상자를 편집하는 방법은 대상자 유형에 따라 다릅니다.

* **쿼리** 대상자를 편집하려면 **[!UICONTROL Audiences]** 메뉴 또는 Adobe Campaign 홈페이지의 **[!UICONTROL Audiences]** 카드를 통해 대상자 목록으로 이동합니다.

   관련 대상자를 엽니다. 이전에 만든 대상자의 모든 요소를 편집할 수 있습니다.

   >[!CAUTION]
   >
   >쿼리의 **[!UICONTROL Filtering dimension]**&#x200B;을(를) 변경하면 이전에 정의된 규칙이 사라집니다.

* **목록** 또는 **파일** 대상자를 편집하려면 대상자를 만든 워크플로우를 편집하고 **[!UICONTROL Save audience]** 활동을 수정합니다. 워크플로우를 시작하여 대상자를 수정합니다.
* **Experience Cloud** 대상자를 편집하려면 [People 핵심 서비스로 대상자 가져오기/내보내기](../../integrating/using/sharing-audiences-with-audience-manager-or-people-core-service.md) 섹션을 참조하십시오.

## 대상자 삭제 {#deleting-audiences}

두 가지 방법으로 한 명 또는 여러 대상자를 삭제할 수 있습니다. 먼저 대상자에 대해 만료 날짜를 추가할 수 있습니다.

방법은 다음과 같습니다.

1. 대상자 중 한 명에게 액세스합니다.
1. ![](assets/edit_darkgrey-24px.png) 버튼을 클릭하여 대상자의 구성에 액세스합니다.

   ![](assets/audience_delete_2.png)

1. **[!UICONTROL Expires on]** 필드에서 대상자에 대해 만료 날짜를 추가합니다.

   ![](assets/audience_delete_3.png)

1. **[!UICONTROL Confirm]**&#x200B;을(를) 클릭한 뒤 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

이제 만료 날짜가 구성되었습니다. 해당 날짜가 되면 대상자가 자동으로 삭제됩니다.

아니면 간단히 한 명 또는 여러 대상자를 선택하고 **[!UICONTROL Delete element]** 버튼을 클릭하여 대상자를 삭제할 수도 있습니다.

![](assets/audience_delete_1.png)

