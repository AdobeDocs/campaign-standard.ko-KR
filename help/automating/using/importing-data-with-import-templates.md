---
title: 가져오기 템플릿으로 데이터 가져오기
seo-title: 가져오기 템플릿으로 데이터 가져오기
description: 가져오기 템플릿으로 데이터 가져오기
seo-description: 캠페인 데이터베이스를 제공하기 위해 데이터를 수집하는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: BFC 03235-2032-448 A-A 9 ED -21 FF 2 A 83 FA 09
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 가져오기 및 내보내기 데이터
discoiquuid: fb 511 bb 8-6 be 7-43 f 6-86 ab -94 d 5 cfa 3 efc 9
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Importing data with import templates{#importing-data-with-import-templates}

데이터를 가져오면 데이터를 수집하여 캠페인의 데이터베이스를 피드할 수 있습니다.

Alternatively to [Workflows](../../automating/using/discovering-workflows.md), Adobe Campaign offers a simplified import function that allows the user to manage certain types of import that were defined by an administrator.

The operating principle is as follows: an **administrator** defines and manages import templates (see [Defining import templates](../../automating/using/defining-import-templates.md)). These import templates are then made available to users with simplified views under the **[!UICONTROL Profiles & audiences]** &gt; **[!UICONTROL Imports]** menu.

따라서 이러한 사용자는 가져오려는 가져오기 유형을 선택하고 가져올 데이터로 파일을 업로드해야 합니다. 관리자가 정의한 워크플로우는 사용자에 대해 투명하게 실행되며, 완료된 후 가져오기에 대한 세부 정보에 액세스할 수 있습니다.

>[!NOTE]
>
>Import data function can be managed by users with **[!UICONTROL GENERIC IMPORT (import)]** and **[!UICONTROL WORKFLOW (workflow)]** roles. 역할과 관련한 자세한 정보는 [이 섹션](../../administration/using/list-of-roles.md)을 참조하십시오.

가져오기가 실행된 템플릿, 실행 날짜 및 실행 상태에 따라 가져오기를 필터링할 수 있습니다.

1. From the imports overview, click the **[!UICONTROL Create]** button. 마법사가 열립니다.
1. 수행할 가져오기 유형을 선택합니다. 가져오기 유형은 사용 가능한 가져오기 템플릿에 해당합니다.
1. 필요한 경우 컴퓨터에 연결된 샘플 파일을 컴퓨터에 다운로드하여 가져올 파일에서 예상되는 데이터 유형을 확인합니다.
1. 마법사에서 가져올 데이터가 포함된 파일을 다운로드합니다.
1. 가져오기를 시작합니다. 마법사가 닫히고 사용된 템플릿으로 수행된 가져오기 목록으로 돌아갑니다.
1. 페이지를 새로 고치고 실행 세부 사항을 보기 위해 방금 수행한 가져오기를 선택합니다.

   ![](assets/simplified_import1.png)

이제 가져오기 실행에 대한 세부 정보를 사용할 수 있습니다. 가져온 파일과 거부된 데이터를 포함한 파일을 모두 컴퓨터에 다운로드할 수 있습니다.
