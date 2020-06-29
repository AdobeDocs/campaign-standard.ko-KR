---
title: 외부 파일에서 프로필 내보내기
description: 이 사용 사례에서는 외부 파일 형태로 프로파일 목록을 내보내 Adobe Campaign 외부에서 데이터를 사용할 수 있도록 하는 방법을 보여줍니다.
page-status-flag: never-activated
uuid: 631f0fbd-9e8d-4f77-a338-fcb7f4fc1774
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: data-management-activities
discoiquuid: a06509f9-4731-4187-b43d-3bfa361284d3
context-tags: fileExport,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c3911232a3cce00c2b9a2e619f090a7520382dde
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---


# 외부 파일에서 프로필 내보내기 {#exporting-profiles-external-file}

다음 예에서는 활동 후에 **[!UICONTROL Extract file]** 활동을 구성하는 방법을 **[!UICONTROL Query]** 보여 줍니다.

이 워크플로우의 목적은 외부 파일 형태로 프로파일 목록을 내보내 Adobe Campaign 외부에서 데이터를 사용할 수 있도록 하는 것입니다.

1. Extract 파일 [](../../automating/using/extract-file.md) 활동을 워크플로우로 드래그하여 놓고 [쿼리](../../automating/using/query.md) 활동 뒤에 놓습니다.

   이 예에서 쿼리는 18~30세의 모든 프로파일에서 수행됩니다.

1. 편집할 **[!UICONTROL Extract file]** 활동을 엽니다.
1. 출력 파일의 이름을 지정합니다.
1. 출력 열 추가

   이 예에서 프로필 이메일, 연령, 생년월일, 이름 및 성은 출력 열로 추가됩니다.

   ![](assets/wkf_data_export6.png)

1. 탭을 **[!UICONTROL File structure]** 클릭하여 다음을 정의합니다.

   * CSV 출력 형식

      ![](assets/wkf_data_export7.png)

   * 날짜 형식

      ![](assets/wkf_data_export9.png)

1. 활동을 확인합니다.
1. 활동 후에 [전송 파일](../../automating/using/transfer-file.md) 활동을 끌어다 놓아 **[!UICONTROL Extract file]** 외부 계정에서 추출 파일을 복구합니다.
1. 활동을 열고 작업을 **[!UICONTROL File upload]** 선택합니다.

   ![](assets/wkf_data_export11.png)

1. 외부 계정을 선택하고 서버의 폴더 경로를 입력합니다.

   ![](assets/wkf_data_export12.png)

1. 활동을 확인하고 워크플로우를 저장합니다.
1. 워크플로우를 시작합니다.

   워크플로우가 올바르게 실행되면 추출된 파일을 외부 계정에서 사용할 수 있습니다.
