---
title: 자동 파일 다운로드를 기반으로 데이터 업데이트
description: '다음 예제는 전송 파일 활동을 통해 자동으로 다운로드된 로드 파일 활동, 업데이트 데이터 활동의 결과를 보여줍니다. '
page-status-flag: never-activated
uuid: 69af12cc-6f82-4977-9f53-aa7bc26f5d7e
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: data-management-activities
discoiquuid: 584ff893-9b1b-46c9-9628-714ab349ab88
context-tags: fileImport,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 7ffa48365875883a98904d6b344ac005afe26e18
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---


# 자동 파일 다운로드를 기반으로 데이터 업데이트 {#updating-data-automatic-file-download}

로드 파일 활동은 주로 기존 데이터에 통합하기 위해 전송 파일 활동의 데이터를 구성합니다.

다음 예제는 전송 파일 활동을 통해 자동으로 다운로드된 로드 파일 활동, 업데이트 데이터 활동의 결과를 보여줍니다. 이 워크플로우는 Adobe Campaign 데이터베이스를 새로운 프로파일로 보완하거나 가져온 파일에서 복구한 데이터를 사용하여 기존 프로파일을 업데이트하는 것을 목표로 합니다.

![](assets/load_file_workflow_ex1.png)

워크플로우를 빌드하려면 다음 단계를 따르십시오.

1. 전송 파일 [](../../automating/using/transfer-file.md) 활동을 워크플로우로 드래그하여 놓습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 활동을 엽니다.
1. 원하는 파일을 복구할 수 있도록 활동을 구성합니다. 탭에서 SFTP **[!UICONTROL Protocol]** 를 **선택합니다**.
1. 외부 계정 **에 정의된 연결 매개 변수 사용 옵션을** 선택합니다.
1. 외부 계정 이름을 입력합니다.
1. 원격 서버의 **파일 경로를 입력합니다**.

   ![](assets/wkf_file_transfer_07.png)

1. 활동을 확인합니다.
1. 파일 [로드](../../automating/using/load-file.md) 활동을 워크플로우로 드래그하여 놓고 **[!UICONTROL Transfer file]** 활동 뒤에 놓습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 활동을 엽니다.
1. 탭 **[!UICONTROL File to load]** 의 **[!UICONTROL Execution]** 섹션에서 **[!UICONTROL Use the file specified in the inbound transition]** 옵션을 선택합니다.

   ![](assets/wkf_file_loading8.png)

1. 활동을 앞에서 지정한 대로 구성합니다.
1. 데이터 [업데이트](../../automating/using/update-data.md) 활동을 워크플로우에 드래그 앤 드롭한 다음 활동 뒤에 **[!UICONTROL Load file]** 배치한 다음 구성합니다.

워크플로우가 시작되면 업로드된 파일의 데이터가 추출된 다음 Adobe Campaign 데이터베이스를 보완하는 데 사용됩니다.
