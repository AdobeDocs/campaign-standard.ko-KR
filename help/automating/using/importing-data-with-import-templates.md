---
title: 가져오기 템플릿으로 데이터 가져오기
description: 데이터를 수집하여 Campaign 데이터베이스를 제공하는 방법을 알아봅니다.
page-status-flag: 활성화 안 함
uuid: bfc03235-2032-448a-a9ed-21ff2a83fa09
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 자동화
content-type: reference
topic-tags: 가져오기 및 내보내기 데이터
discoiquuid: fb511bb8-6be7-43f6-86ab-94d5cfa3efc9
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 가져오기 템플릿으로 데이터 가져오기{#importing-data-with-import-templates}

데이터를 가져오면 데이터를 수집하여 Campaign의 데이터베이스를 제공할 수 있습니다.

또는 [워크플로우에서](../../automating/using/discovering-workflows.md)Adobe Campaign은 관리자가 정의한 특정 유형의 가져오기를 사용자가 관리할 수 있도록 해주는 간소화된 가져오기 기능을 제공합니다.

운영 원칙은 다음과 같습니다.관리자는 **가져오기 템플릿을 정의하고 관리합니다(가져오기 템플릿** 정의 참조 [](../../automating/using/defining-import-templates.md)). 이러한 가져오기 템플릿은 **[!UICONTROL Profiles & audiences]** &gt; **[!UICONTROL Imports]** 메뉴 아래에 보기가 간소화된 사용자가 사용할 수 있게 됩니다.

따라서 이러한 사용자는 가져올 가져오기 유형을 선택하고 가져올 데이터와 함께 파일을 업로드해야 합니다. 관리자가 정의한 워크플로우는 사용자가 투명하게 실행되며 사용자는 가져오기가 완료된 후 가져올 결과의 세부 정보에 액세스할 수 있습니다.

>[!NOTE]
>
>가져오기 데이터 기능은 **[!UICONTROL GENERIC IMPORT (import)]** 및 **[!UICONTROL WORKFLOW (workflow)]** 역할을 가진 사용자가 관리할 수 있습니다. 역할과 관련한 자세한 정보는 [이 섹션](../../administration/using/list-of-roles.md)을 참조하십시오.

가져오기는 실행된 템플릿, 실행 날짜 및 실행 상태에 따라 필터링할 수 있습니다.

1. 가져오기 개요에서 **[!UICONTROL Create]** 단추를 클릭합니다. 마법사가 열립니다.
1. 수행하려는 가져오기 유형을 선택합니다. 가져오기 유형은 사용 가능한 가져오기 템플릿에 해당합니다.
1. 필요한 경우 템플릿에 연결된 샘플 파일을 컴퓨터에 다운로드하여 가져올 파일에 필요한 데이터 유형을 확인합니다.
1. 마법사에서 가져올 데이터가 포함된 파일을 다운로드합니다.
1. 가져오기를 시작합니다. 마법사가 닫히고 사용된 템플릿과 함께 수행되는 가져오기 목록으로 돌아갑니다.
1. 페이지를 새로 고치고 방금 수행한 가져오기를 선택하여 실행 세부 사항을 봅니다.

   ![](assets/simplified_import1.png)

이제 가져오기 실행에 대한 세부 정보를 사용할 수 있습니다. 가져온 파일과 거부된 데이터(가져오지 않은 데이터)가 포함된 파일을 모두 컴퓨터에 다운로드할 수 있습니다.
