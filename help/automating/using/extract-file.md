---
title: 파일 추출
seo-title: 파일 추출
description: 파일 추출
seo-description: 파일 추출 활동을 사용하면 Adobe Campaign의 데이터를 외부 파일 형식으로 내보낼 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 631 F 0 FBD -9 E 8 D -4 F 77-A 338-FCB 7 F 4 FC 1774
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 데이터 관리 활동
discoiquuid: A 06509 F 9-4731-4187-B 43 D -3 BFA 361284 D 3
context-tags: Fileexport, Main
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: e384a0cef325bc01eb5ea050b0f3d926aea9a88f

---


# Extract file{#extract-file}

## Description {#description}

![](assets/export.png)

**[!UICONTROL Extract file]** 활동을 통해 Adobe Campaign의 데이터를 외부 파일 양식으로 내보낼 수 있습니다.

## Context of use {#context-of-use}

데이터를 추출할 방법은 활동을 구성할 때 정의됩니다.

>[!CAUTION]
>
>**[!UICONTROL Extract file]** 활동을 사용하려면 **[!UICONTROL Query]** 활동 뒤에 배치해야 합니다.

## Configuration {#configuration}

1. **[!UICONTROL Extract file]** 워크플로우를 워크플로우로 드래그하여 놓습니다.

   ![](assets/wkf_data_export1.png)

1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. Enter the label of the **Output file**. 파일의 레이블은 고유하도록 만들어진 날짜와 시간으로 자동으로 완료됩니다. 예를 들면 다음과 같습니다. recipients_20150815_081532.txt 파일은 2015 년 8 월 15 일 08:15:32에서 생성되었습니다.

   >[!NOTE]
   >
   >It is possible to use the **[!UICONTROL formatDate]** function in this field to specify the file name.

1. If you like, you can zip the output file by selecting **[!UICONTROL Compression]** in the **[!UICONTROL Add a pre-processing step]** field. 출력 파일은 GZIP 파일 (.gz) 로 압축됩니다.
1. ![](assets/add_darkgrey-24px.png) 또는 **[!UICONTROL Add an element]** 단추를 클릭하여 출력 열을 추가합니다.

   ![](assets/wkf_data_export2.png)

   새 창이 열립니다.

   ![](assets/wkf_data_export3.png)

1. 표현식을 입력합니다. To do this, you can select an existing expression or create a new one using the **expression editor**.
1. 표현식을 확인합니다.

   표현식이 출력 열에 추가됩니다.

1. 열을 원하는 만큼 만들 수 있습니다. 해당 표현식 및 레이블을 클릭하여 열을 편집할 수 있습니다.

   프로필을 내보내고 외부 도구에서 사용하려는 경우 고유 식별자를 내보내야 합니다. 기본적으로 일부 프로필에는 데이터베이스에 추가되는 방식에 따라 고유한 식별자가 있습니다. For more information, refer to the [Generating a unique ID for profiles](../../developing/using/configuring-the-resource-s-data-structure.md#generating-a-unique-id-for-profiles-and-custom-resources) section.

1. **[!UICONTROL File structure]** 탭을 클릭하여 내보낼 파일의 출력, 날짜 및 번호 형식을 구성합니다.

   Check the **[!UICONTROL Export labels instead of internal values of enumerations]** option in case you export enumeration values. 이 옵션을 사용하면 ID 대신 이해하기 쉬운 짧은 레이블을 검색할 수 있습니다.

1. In the **[!UICONTROL Properties]** tab, select the **[!UICONTROL Do not generate a file if the inbound transition is empty]** option to avoid creating and uploading empty files on SFTP servers if the inbound transition is empty.
1. 활동의 구성을 확인하고 워크플로우를 저장합니다.

## Example {#example}

The following example illustrates how to configure an **[!UICONTROL Extract file]** activity after a **[!UICONTROL Query]** activity.

이 워크플로우는 Adobe Campaign 외부에서 데이터를 사용할 수 있도록 외부 파일 형식으로 프로필 목록을 내보내는 것입니다.

1. **[!UICONTROL Extract file]** 활동을 워크플로우로 드래그하여 놓고 **[!UICONTROL Query]** 활동 뒤에 배치합니다.

   이 예에서 쿼리는 18 부터 30 까지의 모든 프로필에 대해 수행됩니다.

1. 파일 추출 활동을 열어 편집합니다.
1. 출력 파일의 이름을 지정합니다.
1. 출력 열을 추가합니다.

   이 예에서, 이메일, 연령, 생년월일, 프로필의 이름 및 성은 출력 열로 추가됩니다.

   ![](assets/wkf_data_export6.png)

1. **[!UICONTROL File structure]** 탭을 클릭하여 다음을 정의합니다.

   * CSV 출력 형식

      ![](assets/wkf_data_export7.png)

   * 날짜 형식

      ![](assets/wkf_data_export9.png)

1. 활동을 확인합니다.
1. Drag and drop a **[!UICONTROL Transfer file]** activity after the **[!UICONTROL Extract file]** activity to recover the extract file on an external account.
1. Open the activity and choose the **[!UICONTROL File upload]** action.

   ![](assets/wkf_data_export11.png)

1. 외부 계정을 선택하고 서버에 폴더 경로를 입력합니다.

   ![](assets/wkf_data_export12.png)

1. 활동을 확인하고 워크플로우를 저장합니다.
1. 워크플로우를 시작합니다.

   워크플로우가 올바르게 실행되면 추출된 파일은 외부 계정에서 사용할 수 있습니다.

