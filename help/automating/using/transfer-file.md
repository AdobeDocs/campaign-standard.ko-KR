---
title: 파일 전송
description: 파일 전송 활동을 사용하면 파일을 수신하거나 보내고, 파일이 있는지 테스트하거나, Adobe Campaign에 파일을 나열할 수 있습니다.
page-status-flag: never-activated
uuid: a2f18118-b681-4310-aee0-9e82179d2032
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: data-management-activities
discoiquuid: 752f2aed-f897-485e-b329-f3cc1756ee8e
context-tags: fileTransfer,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: ff3b41589f47e7697a69bb68824aefd4d9036793

---


# 파일 전송{#transfer-file}

## 설명 {#description}

![](assets/file_transfer.png)

이 **[!UICONTROL Transfer file]**활동을 통해 파일을 수신하거나 보내고, 파일이 있는지 테스트하거나, Adobe Campaign에 파일을 나열할 수 있습니다.

## 사용 상황 {#context-of-use}

데이터를 추출하는 방법은 활동이 구성될 때 정의됩니다. 로드할 파일은 연락처 목록일 수 있습니다(예:

이 활동을 사용하여 **[!UICONTROL Load file]**활동과 함께 구조화된 데이터를 복구할 수 있습니다.

## 구성 {#configuration}

1. 워크플로우에 **[!UICONTROL Transfer file]**활동 삽입
1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 엽니다.
1. 필드의 드롭다운 목록을 사용하여 다음 활동 작업 중 하나를 선택합니다. **[!UICONTROL Action]**

   ![](assets/wkf_file_transfer_01.png)

   * **파일 다운로드**:파일을 다운로드할 수 있습니다.
   * **파일 업로드**:파일을 업로드할 수 있습니다. Adobe Campaign 파일에서 파일을 업로드하면 **[!UICONTROL Export audits]**메뉴에서 로그 항목이 생성됩니다. 내보내기 감사에 대한 자세한 내용은 감사 내보내기[섹션을](../../administration/using/auditing-export-logs.md)참조하십시오.
   * **파일이 있는지**&#x200B;테스트:파일이 있는지 확인할 수 있습니다.
   * **파일 목록**:adobe Campaign에 있는 파일을 나열할 수 있습니다.
   선택한 작업에 따라 하나 이상의 프로토콜을 사용할 수 있습니다.

   * **HTTP**:이 프로토콜을 사용하면 외부 계정 또는 URL에서 파일 다운로드를 시작할 수 있습니다.

      * 옵션을 **[!UICONTROL Use connection parameters defined in an external account]**클릭한 다음 원하는 계정을 선택하고 다운로드할 파일의 경로를 지정합니다.

         ![](assets/wkf_file_transfer_03.png)

      * 옵션을 **[!UICONTROL Quick configuration]**클릭한 다음 표시되는 필드에 URL을 입력합니다.

         ![](assets/wkf_file_transfer_04.png)
   * **S3**:이 프로토콜을 사용하면 Amazon Simple Storage Service(S3)를 통해 URL 또는 외부 계정에서 파일 다운로드를 시작할 수 있습니다.

      * 외부 계정을 선택하고 다운로드할 파일의 경로를 지정합니다.

         ![](assets/wkf_file_transfer_08.png)
   * **SFTP**:이 프로토콜을 사용하면 URL 또는 외부 계정에서 파일 다운로드를 시작할 수 있습니다.

      * 옵션을 **[!UICONTROL Use connection parameters defined in an external account]**클릭한 다음 원하는 계정을 선택하고 다운로드할 파일의 경로를 지정합니다.

         ![](assets/wkf_file_transfer_07.png)

         >[!CAUTION]
         >
         >와일드카드가 지원됩니다.

      * 옵션을 **[!UICONTROL Quick configuration]**클릭한 다음 표시되는 필드에 URL을 입력합니다.
      * 가져온 파일을 정렬하려면 **[!UICONTROL Sort alphanumerically]****[!UICONTROL Additional options]** 섹션에서 옵션을 선택합니다. 그러면 파일이 순차적 순서로 처리됩니다.

         ![](assets/wkf_file_transfer_sort.png)
   * **Adobe Campaign 서버에**&#x200B;있는 파일:이 프로토콜은 복구할 파일이 들어 있는 저장소에 해당합니다.

      메타 문자 또는 와일드카드(예: * 또는 ?) 를 사용하여 파일을 필터링할 수 있습니다.

      이 필드를 채우고 이 프로토콜을 사용할 활동을 확인합니다.

      >[!NOTE]
      >
      >경로는 Adobe Campaign 서버의 저장소 공간 디렉토리에 상대적이어야 합니다. 파일은 sftp&lt;yourinstancename>/ **디렉토리에 있습니다** . 또한 저장소 공간 위의 디렉토리는 검색할 수 없습니다. 예:

      >**user&lt;yourinstancename>/my_recipients.csv이** 정확합니다.
      **../hello/my_recipients.csv이** 잘못되었습니다.
      **/myserver/hello/myrecipients.csv이** 잘못되었습니다.
   프로토콜을 선택하고 관련 필드를 완료합니다.

   각 프로토콜에 사용할 수 있는 **[!UICONTROL Use a dynamic file path]**옵션을 사용하면 표준 표현식 및 이벤트 변수를 사용하여 전송할 파일의 이름을 개인화할 수 있습니다. 자세한 내용은 이벤트 변수를 사용하여[활동 사용자 지정](../../automating/using/calling-a-workflow-with-external-parameters.md#customizing-activities-with-events-variables)섹션을 참조하십시오.

1. 선택한 프로토콜에 따라 사용할 수 있는 **[!UICONTROL Additional options]**섹션에서 프로토콜에 매개 변수를 추가할 수 있습니다. 다음 작업을 수행할 수 있습니다.

   * **[!UICONTROL Delete the source files after transfer]**
   * **[!UICONTROL Disable passive mode]**
   * **[!UICONTROL List all files]**:이 옵션은**[!UICONTROL File listing]** 작업을 선택할 때 사용할 수 있습니다. 이 변수를 사용하면 서버에 있는 모든 파일을 **vars.filenames** 이벤트 변수에서 파일 이름이 **&#39;n&#39;** 문자로 구분되는 인덱스를 만들 수 있습니다.

1. 이 **[!UICONTROL If no files are found]**탭의**[!UICONTROL Advanced options]** 섹션에서 활동이 시작될 때 오류나 존재하지 않는 파일이 감지되면 특정 작업을 구성할 수 있습니다.

   재시도를 정의할 수도 있습니다. 다른 재시도가 워크플로우 실행 로그에 표시됩니다.

   ![](assets/wkf_file_transfer_09.png)

1. 활동 구성을 확인하고 워크플로우를 저장합니다.

## 내역 설정 {#historization-settings}

활동이 실행될 때마다 업로드되거나 다운로드된 파일이 전용 폴더에 저장됩니다. **[!UICONTROL Transfer file]**워크플로우의 각**[!UICONTROL Transfer file]** 활동에 대해 하나의 폴더가 생성됩니다. 따라서 서버의 물리적 공간을 보존하려면 이 폴더의 크기를 제한할 수 있어야 합니다.

이렇게 하려면 **[!UICONTROL Historization settings]**활동의**[!UICONTROL Advanced options]** **[!UICONTROL Transfer File]**창에서 정의할 수 있습니다.

**[!UICONTROL Historization settings]**활동의 폴더에 대한 최대 파일 수 또는 전체 크기를 정의할 수 있습니다. 기본적으로 100개 파일과 50MB가 인증됩니다.

활동이 실행될 때마다 폴더는 다음과 같이 선택됩니다.

* 활동이 실행되기 24시간 전에 생성된 파일만 고려됩니다.
* 고려된 파일 수가 **[!UICONTROL Maximum number of files]****[!UICONTROL Maximum number of files]** 매개 변수의 값보다 크면 허용된 파일에 도달할 때까지 가장 오래된 파일이 삭제됩니다.
* 고려된 파일의 전체 크기가 **[!UICONTROL Maximum size (in MB)]****[!UICONTROL Maximum size (in MB)]** 매개 변수의 값보다 크면 허용된 파일에 도달할 때까지 가장 오래된 파일이 삭제됩니다.

>[!NOTE]
활동이 다시 실행되지 않으면 해당 폴더는 검사되거나 삭제되지 않습니다. 따라서 대용량 파일을 전송할 때는 주의하십시오.

## 예 {#example}

다음 예는 파일 전송 **작업의 구성을** 보여 줍니다. 이 구성 **뒤에는 파일** 로드 **작업 다음에 데이터** 업데이트작업이표시됩니다. 이 워크플로우의 목표는 워크플로에서 복구된 데이터로 Adobe Campaign 데이터베이스 프로필을 추가하거나 업데이트하는 것입니다.

1. Transfer **파일** 작업을 워크플로우로 드래그하여 놓습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 엽니다.
1. 탭에서 SFTP를 **[!UICONTROL Protocol]**선택합니다****.
1. 외부 **계정에** 정의된 연결 매개 변수 사용 옵션을 선택합니다.
1. 외부 계정 이름을 입력합니다.
1. 원격 **서버에**&#x200B;파일 경로를 입력합니다.

   ![](assets/wkf_file_transfer_07.png)

1. 활동을 확인하고 워크플로우를 저장합니다.

