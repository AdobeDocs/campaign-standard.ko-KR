---
title: 파일 전송
seo-title: 파일 전송
description: 파일 전송
seo-description: 파일 전송 활동을 통해 파일을 받거나 보내거나 파일이 있는지 여부를 테스트하거나 Adobe Campaign에 파일을 표시할 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: A 2 F 18118-B 681-4310-AEE 0-9 E 82179 D 2032
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 데이터 관리 활동
discoiquuid: 752 F 2 AED-F 897-485 E-B 329-F 3 CC 1756 EE 8 E
context-tags: Filetransfer, Main
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 0fcedd464ae2074e7eda793bbf20cc53ce04f324

---


# Transfer file{#transfer-file}

## Description {#description}

![](assets/file_transfer.png)

**[!UICONTROL Transfer file]** 이 활동을 통해 파일을 받거나 보내거나 파일이 있는지 여부를 테스트하거나 Adobe Campaign에 파일을 표시할 수 있습니다.

## Context of use {#context-of-use}

데이터가 추출될 방법은 활동이 구성될 때 정의됩니다. 로드할 파일은 연락처 목록이 될 수 있습니다.

You can use this activity to recover data that will then be structured with the **[!UICONTROL Load file]** activity.

## Configuration {#configuration}

1. **[!UICONTROL Transfer file]** 워크플로우에 활동을 놓습니다.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. **[!UICONTROL Action]** 필드의 드롭다운 목록을 사용하여 다음 활동 작업 중 하나를 선택합니다.

   ![](assets/wkf_file_transfer_01.png)

   * **파일 다운로드**: 파일을 다운로드할 수 있습니다.
   * **파일 업로드**: 파일을 업로드할 수 있습니다. Uploading a file from Adobe Campaign file generates a log entry in the **[!UICONTROL Export audits]** menu. For more information on export audits, refer to the [Auditing exports](../../administration/using/auditing-export-logs.md) section.
   * **파일이 있는지 테스트합니다**. 파일이 있는지 여부를 확인할 수 있습니다.
   * **파일 목록**: Adobe Campaign에 있는 파일을 나열할 수 있습니다.
   선택한 작업에 따라 하나 또는 여러 개의 프로토콜을 사용할 수 있습니다.

   * **HTTP**: 이 프로토콜을 사용하면 외부 계정 또는 URL에서 파일을 다운로드할 수 있습니다.

      * **[!UICONTROL Use connection parameters defined in an external account]** 옵션을 클릭한 다음 원하는 계정을 선택하고 다운로드할 파일의 경로를 지정합니다.

         ![](assets/wkf_file_transfer_03.png)

      * **[!UICONTROL Quick configuration]** 옵션을 클릭한 다음 나타나는 필드에 URL를 입력합니다.

         ![](assets/wkf_file_transfer_04.png)
   * **S 3**: 이 프로토콜을 사용하면 Amazon Simple Storage Service (S 3) 를 통해 URL 또는 외부 계정에서 파일을 다운로드할 수 있습니다.

      * 외부 계정을 선택하고 다운로드할 파일의 경로를 지정합니다.

         ![](assets/wkf_file_transfer_08.png)
   * **Sftp**: 이 프로토콜을 사용하면 URL 또는 외부 계정에서 파일을 다운로드할 수 있습니다.

      * **[!UICONTROL Use connection parameters defined in an external account]** 옵션을 클릭한 다음 원하는 계정을 선택하고 다운로드할 파일의 경로를 지정합니다.

         ![](assets/wkf_file_transfer_07.png)

         >[!CAUTION]
         >
         >와일드카드가 지원됩니다.

      * **[!UICONTROL Quick configuration]** 옵션을 클릭한 다음 나타나는 필드에 URL를 입력합니다.
      * If you want to sort the imported files, select the **[!UICONTROL Sort alphanumerically]** option from the **[!UICONTROL Additional options]** section. 그러면 파일이 순차적 순서로 처리됩니다.

         ![](assets/wkf_file_transfer_sort.png)
   * **Adobe Campaign 서버에 있는 파일**: 이 프로토콜은 복구할 파일이 포함된 저장소에 해당합니다.

      메타 문자 또는 와일드카드 (예: * 또는?) 를 사용하여 파일을 필터링할 수 있습니다.

      이 필드를 채우고 이 프로토콜을 사용할 활동을 확인합니다.

      >[!NOTE]
      >
      >경로는 Adobe Campaign 서버의 저장소 공간 디렉토리에 상대적이어야 합니다. 파일은** sftp &lt; yourinstancename &gt;/** 디렉토리에 있습니다. 저장소 공간 위의 디렉토리도 찾을 수 없습니다. For example: **user&lt;yourinstancename&gt;/my_recipients.csv** is correct. **../hello/my_recipients.csv** 이 잘못되었습니다. **//myserver/hello/myrecipients.csv** 이 잘못되었습니다.
   프로토콜을 선택하고 연결된 필드를 완료합니다.

   The **[!UICONTROL Use a dynamic file path]** option, available for each protocol, lets you use a standard expression and events variables to personalize the name of the file to transfer. For more on this, refer to the [Customizing activities with events variables](../../automating/using/calling-a-workflow-with-external-parameters.md#customizing-activities-with-events-variables) section.

1. The **[!UICONTROL Additional options]** section, available depending on the protocol selected, allows you to add parameters to your protocol. 다음을 수행할 수 있습니다.

   * **[!UICONTROL Delete the source files after transfer]**
   * **[!UICONTROL Disable passive mode]**
   * **[!UICONTROL List all files]**: 이 옵션은 **[!UICONTROL File listing]** 작업을 선택할 때 사용할 수 있습니다. It allows you to index all the files present on the server in the **vars.filenames** event variable in which the file names are separated by the **'n'** characters.

1. The **[!UICONTROL If no files are found]** section of the **[!UICONTROL Advanced options]** tab allows you to configure specific actions if any errors or inexistent files are detected when the activity is started.

   재시도 횟수를 정의할 수도 있습니다. 다른 재시도가 워크플로우 실행 로그에 나타납니다.

   ![](assets/wkf_file_transfer_09.png)

1. 활동의 구성을 확인하고 워크플로우를 저장합니다.

## Historization settings {#historization-settings}

**[!UICONTROL Transfer file]** 활동이 실행될 때마다 업로드되거나 다운로드한 파일이 전용 폴더에 저장됩니다. One folder is created for each **[!UICONTROL Transfer file]** activity of a workflow. 따라서 서버의 물리적 공간을 유지하기 위해 이 폴더의 크기를 제한할 수 있어야 합니다.

To do that, you can define **[!UICONTROL Historization settings]** in the **[!UICONTROL Advanced options]** of the **[!UICONTROL Transfer File]** activity.

**[!UICONTROL Historization settings]** 허용되는 최대 파일 수 또는 활동 폴더에 대한 전체 크기의 정의를 허용합니다. 기본적으로 100 개 파일과 50 MB의 권한이 부여됩니다.

활동이 실행될 때마다 폴더는 다음과 같이 확인됩니다.

* 활동을 실행하기 전에 24 시간 이상 생성된 파일만 고려됩니다.
* If the number of files taken into account is greater than the value of the **[!UICONTROL Maximum number of files]** parameter, the oldest files are deleted until the **[!UICONTROL Maximum number of files]** allowed is reached.
* If the total size of files taken into account is greater than the value of the **[!UICONTROL Maximum size (in MB)]** parameter, the oldest files are deleted until the **[!UICONTROL Maximum size (in MB)]** allowed is reached.

>[!NOTE]
활동이 다시 실행되지 않으면 해당 폴더가 확인되거나 삭제되지 않습니다. 따라서 대용량 파일을 전송할 때는 주의하십시오.

## Example {#example}

The following example shows the configuration of a **File transfer** activity which will then be followed by a **Load file** activity then an **Update data** activity. 이 워크플로의 목표는 워크플로우에서 복구된 데이터로 Adobe Campaign 데이터베이스 프로필을 추가하거나 업데이트하는 것입니다.

1. **워크플로우로 파일** 전송 활동을 드래그하여 놓습니다.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. **[!UICONTROL Protocol]** 탭에서 **Sftp**&#x200B;를 선택합니다.
1. Select the **Use connection parameters defined in an external account** option.
1. 외부 계정 이름을 입력합니다.
1. Enter the **File path on the remote server**.

   ![](assets/wkf_file_transfer_07.png)

1. 활동을 확인하고 워크플로우를 저장합니다.

