---
title: 자동 파일 다운로드를 기반으로 데이터 업데이트
description: 다음 예제는 파일 전송 활동을 통해 자동으로 다운로드한 파일 로드 활동 뒤에 데이터 업데이트 활동을 사용했을 때의 결과를 보여줍니다.
audience: automating
content-type: reference
topic-tags: data-management-activities
context-tags: fileImport,main
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: 2b21cf45-1c40-4e0e-ae2c-28c9f73e1964
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 70%

---

# 자동 파일 다운로드를 기반으로 데이터 업데이트 {#updating-data-automatic-file-download}

파일 로드 활동은 주로 파일 전송 활동에서 가져온 데이터를 구조화하여 기존 데이터에 통합할 수 있게 만드는 역할을 합니다.

다음 예제는 파일 전송 활동을 통해 자동으로 다운로드한 파일 로드 활동 뒤에 데이터 업데이트 활동을 사용했을 때의 결과를 보여 줍니다. 이 워크플로의 목적은 가져온 파일에서 복구한 데이터를 사용하여 새로운 프로필로 Adobe Campaign 데이터베이스를 보강하거나 기존 프로필을 업데이트하는 것입니다.

![](assets/load_file_workflow_ex1.png)

워크플로우를 빌드하려면 다음 단계를 수행합니다.

1. [파일 전송](../../automating/using/transfer-file.md) 활동을 워크플로로 끌어서 놓습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업에서 ![](assets/edit_darkgrey-24px.png) 버튼을 사용하여 활동을 엽니다.
1. 원하는 파일을 복구할 수 있도록 활동을 구성합니다. **[!UICONTROL Protocol]** 탭에서 **SFTP**&#x200B;를 선택합니다.
1. **외부 계정에 정의된 연결 매개 변수 사용** 옵션을 선택합니다.
1. 외부 계정 이름을 입력합니다.
1. **원격 서버의 파일 경로**&#x200B;를 입력합니다.

   ![](assets/wkf_file_transfer_07.png)

1. 활동을 확인합니다.
1. [파일 로드](../../automating/using/load-file.md) 활동을 워크플로우에 끌어다 놓고 **[!UICONTROL Transfer file]** 활동 뒤에 놓습니다.
1. 해당 활동을 선택하면 나타나는 빠른 작업 목록에서 ![](assets/edit_darkgrey-24px.png) 버튼을 눌러 창을 엽니다.
1. **[!UICONTROL Execution]** 탭의 **[!UICONTROL File to load]** 섹션에서 **[!UICONTROL Use the file specified in the inbound transition]** 옵션을 선택합니다.

   ![](assets/wkf_file_loading8.png)

1. 활동을 앞에서 지정한 대로 구성합니다.
1. [데이터 업데이트](../../automating/using/update-data.md) 활동을 워크플로우로 끌어서 놓고 **[!UICONTROL Load file]** 활동 뒤에 놓은 다음 구성합니다.

워크플로를 시작하면 업로드한 파일의 데이터를 추출하여 Adobe Campaign 데이터베이스를 보강하는 데 사용합니다.
