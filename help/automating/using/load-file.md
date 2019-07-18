---
title: 파일 로드
seo-title: 파일 로드
description: 파일 로드
seo-description: 로드 파일 활동을 사용하면 하나의 구조화된 형태로 데이터를 가져와서 Adobe Campaign에서 이 데이터를 사용할 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 69 AF 12 CC -6 F 82-4977-9 F 53-AA 7 BC 26 F 5 D 7 E
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 데이터 관리 활동
discoiquuid: 584 FF 893-9 B 1 B -46 C 9-9628-714 AB 349 AB 88
context-tags: Fileimport, Main
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 0454dac1a7976c1be2838c2a846d33e77e60c3b3

---


# Load file{#load-file}

## Description {#description}

![](assets/data_loading.png)

**[!UICONTROL Load file]** 활동을 통해 데이터를 Adobe Campaign에서 사용할 수 있도록 구조화된 형태로 가져올 수 있습니다. 데이터는 일시적으로 가져온 것이며 다른 활동은 Adobe Campaign 데이터베이스에 명확하게 통합하기 위해 필요합니다.

## Context of use {#context-of-use}

데이터가 추출될 방법은 활동이 구성될 때 정의됩니다. 로드할 파일은 연락처 목록이 될 수 있습니다.

>[!CAUTION]
>
>예를 들어.txt. csv 등 "일반" 구조 파일만 고려됩니다.

다음을 수행할 수 있습니다.

* Use the file structure to apply it to another file's data (recovered using the **[!UICONTROL Transfer file]** activity) or,
* 파일의 구조 및 데이터를 사용하여 Adobe Campaign로 가져옵니다.

## Configuration {#configuration}

활동 구성은 두 단계로 이루어집니다. 먼저 샘플 파일을 업로드하여 예상 파일 구조를 정의해야 합니다. 이 작업이 끝나면 데이터를 가져올 파일의 원본을 지정할 수 있습니다.

>[!NOTE]
>
>샘플 파일의 데이터는 활동을 구성하는 데 사용되지만 가져오지는 않습니다. 데이터가 거의 들어 있는 샘플 파일을 사용하는 것이 좋습니다.

1. **[!UICONTROL Load file]** 워크플로우를 워크플로우로 드래그하여 놓습니다.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. 최종 파일을 가져올 때 예상되는 구조를 정의할 수 있는 샘플 파일을 업로드합니다.

   ![](assets/wkf_file_loading.png)

   Once the data file is uploaded, two new tabs appear in the activity: **[!UICONTROL File structure]** and **[!UICONTROL Column definition]**.

1. **[!UICONTROL File structure]** 탭으로 이동하여 샘플 파일에서 자동으로 감지된 구조를 봅니다.

   파일 구조가 잘못 탐지된 경우 가능한 오류를 수정할 수 있는 옵션이 몇 가지 있습니다.

   * You can choose to use the structure of another file by selecting the **[!UICONTROL Detect structure from a new file]** option.
   * 기본 감지 매개 변수를 수정하여 파일에 적용할 수 있습니다. **[!UICONTROL File type]** 이 필드에서 가져오려는 파일이 고정 길이의 열로 이루어져 있는지 지정할 수 있습니다. In that case, you must also specify the maximum number of characters for each column in the **[!UICONTROL Column definition]** tab.

      All of the detection options necessary to correctly recover the data from the file are regrouped in **[!UICONTROL File format]**. 이러한 새로운 설정을 고려하여 활동에 로드된 마지막 파일의 구조를 다시 감지할 수 있습니다. To do this, use the **[!UICONTROL Apply configuration]** button. 예를 들어, 다른 열 구분 기호를 지정할 수 있습니다.

      >[!NOTE]
      >
      >이 작업은 활동에 로드된 마지막 파일을 고려합니다. 검색된 파일이 큰 경우 데이터 미리 보기에는 처음 30 개의 행만 표시됩니다.

      ![](assets/wkf_file_loading3.png)

      **[!UICONTROL File format]** 섹션에서 **[!UICONTROL Check columns from file against column definitions]** 이 옵션을 사용하면 업로드하려는 파일의 열이 열 정의에 해당하는지 확인할 수 있습니다.

      열의 번호 및/또는 이름이 열 정의와 일치하지 않으면 워크플로우를 실행할 때 오류 메시지가 표시됩니다. 이 옵션이 활성화되지 않으면 로그 파일에 경고가 표시됩니다.

      ![](assets/wkf_file_loading_check.png)

1. **[!UICONTROL Column definition]** 탭으로 이동하여 각 열의 데이터 형식을 확인하고 필요한 경우 매개 변수를 조정합니다.

   **[!UICONTROL Column definition]** 이 탭에서는 오류를 포함하지 않는 (예: null 관리 사용) 데이터를 가져와서 향후 작업을 위해 Adobe Campaign 데이터베이스에 이미 있는 유형과 일치시킬 수 있도록 각 열의 데이터 구조를 정확하게 지정할 수 있습니다.

   예를 들어, 열의 레이블을 변경할 수 있습니다 (문자열, 정수, 날짜 등). 오류 처리를 지정할 수도 있습니다.

   For more information, refer to the [Column format](../../automating/using/load-file.md#column-format) section.

   ![](assets/wkf_file_loading4.png)

1. **[!UICONTROL Execution]** 탭에서 데이터를 로드하기 위해 파일을 처리할 것인지 지정합니다.

   * 워크플로우에서 인바운드 전환을 가져옵니다.
   * 는 이전 단계에서 업로드한 항목입니다.
   * 은 로컬 컴퓨터에서 업로드할 새 파일입니다. The **[!UICONTROL Upload a new file from local machine]** option appears if uploading a first file was already defined in the workflow. 이렇게 하면 현재 파일이 사용자의 요구 사항에 맞지 않는 경우 처리할 다른 파일을 업로드할 수 있습니다.

      ![](assets/wkf_file_loading1.png)

1. If the file that you want to load the data from is compressed into a GZIP file (.gz), select the **[!UICONTROL Decompression]** option in the **[!UICONTROL Add a pre-processing step]** field. 이렇게 하면 데이터를 로드하기 전에 파일의 압축을 해제할 수 있습니다. 이 옵션은 해당 파일이 활동의 인바운드 전환에서 오는 경우에만 사용할 수 있습니다.
1. **[!UICONTROL Keep the rejects in a file]** 이 옵션을 사용하면 가져오는 동안 발생한 오류가 포함된 파일을 다운로드하고 후처리 단계에 적용할 수 있습니다.

   >[!NOTE]
   >
   >**[!UICONTROL Add date and time to the file name]** 이 옵션을 사용하면 거부사항이 포함된 파일의 이름을 타임스탬프를 추가할 수 있습니다.

   ![](assets/wkf_file_loading_keeprejects.png)

1. 활동의 구성을 확인하고 워크플로우를 저장합니다.

## Column format {#column-format}

샘플 파일을 로드할 때 각 데이터 유형에 대한 기본 매개 변수와 함께 열 형식이 자동으로 검색됩니다. 특히 오류 또는 빈 값이 있을 때 데이터에 적용할 특정 프로세스를 지정할 수 있도록 이러한 기본 매개 변수를 수정할 수 있습니다.

To do this, select **[!UICONTROL Edit properties]** from the quick actions of the column whose format you would like to define. 열 형식 세부 사항 창이 열립니다.

![](assets/wkf_file_loading4.png)

그런 다음 각 열에 대한 서식을 수정할 수 있습니다.

열 서식을 사용하여 각 열의 값 처리를 정의할 수 있습니다.

* **[!UICONTROL Ignore column]**: 데이터 로드 중에는 이 열을 처리하지 않습니다.
* **[!UICONTROL Data type]**: 각 열에 대해 예상되는 데이터 유형을 지정합니다.
* **[!UICONTROL Format and separators]**, **속성**: 열 컨텍스트에 의해 지정된 구분 기호뿐만 아니라 텍스트 속성, 시간, 날짜 및 숫자 값 형식을 지정합니다.

   * **[!UICONTROL Maximum number of characters]**: 문자열 유형 열에 사용할 최대 문자 수를 지정합니다.

      고정 길이의 열로 이루어진 파일을 로드할 때 이 필드를 채워야 합니다.

   * **[!UICONTROL Letter case management]**: 문자 대소문자 프로세스를 **텍스트** 데이터에 적용해야 할지 여부를 정의합니다.
   * **[!UICONTROL White space management]**: **텍스트** 데이터의 문자열에서 특정 공백을 무시해야 하는지 여부를 지정합니다.
   * **[!UICONTROL Time format]****[!UICONTROL Date format]**: **날짜**, **시간** , **날짜 및 시간** 데이터의 형식을 지정합니다.
   * **[!UICONTROL Format]**: **정수** 및 **부동 숫자** 데이터에 대한 숫자 값의 형식을 정의할 수 있습니다.
   * **[!UICONTROL Separator]**: **날짜**, **시간**, **날짜 및 시간**, **정수**&#x200B;및 **부동 숫자** 데이터에 대한 열 컨텍스트 (천 단위 구분 기호 또는 숫자 구분 기호, 날짜 및 시간에 대한 구분 기호) 에 의해 지정된 구분 기호를 정의합니다.

* **[!UICONTROL Remapping of values]**: 이 필드는 열 세부 사항 구성에서만 사용할 수 있습니다. 가져올 때 특정 값을 변형할 수 있습니다. 예를 들어 "3" 를 "3" 로 변형할 수 있습니다.
* **[!UICONTROL Error processing]**: 오류가 발생하는 경우 동작을 정의합니다.

   * **[!UICONTROL Ignore the value]**: 값은 무시됩니다. 워크플로우 실행 로그에 경고가 생성됩니다.
   * **[!UICONTROL Reject the line]**: 전체 줄은 처리되지 않습니다.
   * **[!UICONTROL Use a default value]**: 필드에 정의된 기본값으로 오류를 발생시키는 값을 **[!UICONTROL Default value]** 대체합니다.
   * **[!UICONTROL Use a default value in case the value is not remapped]**: 잘못된 값에 대해 매핑이 정의되지 않은 경우 **[!UICONTROL Default value]** 필드에 정의된 기본값으로 오류를 발생시키는 값을 대체합니다 (위 **[!UICONTROL Remapping of values]** 옵션 참조).
   * **[!UICONTROL Reject the line when there is no remapping value]**: 잘못된 값에 대해 매핑이 정의되어 있지 않으면 전체 줄이 처리되지 않습니다 (위 **[!UICONTROL Remapping of values]** 옵션 참조).
   >[!NOTE]
   >
   >**[!UICONTROL Error processing]** 가져온 파일의 값에 대한 오류를 표시합니다. 예를 들어 잘못된 데이터 유형 ("정수" 열에 대한 "4" 모든 문자), 허용되는 최대 숫자 수, 잘못된 구분 기호가 있는 날짜 등이 포함된 문자열입니다. 하지만 이 옵션은 빈 값 관리에 의해 생성된 오류를 걱정하지 않습니다.

* **[!UICONTROL Default value]**: 선택한 오류 처리에 따라 기본값을 지정합니다.
* **[!UICONTROL Empty value management]**: 데이터 로드 중에 빈 값을 관리하는 방법을 지정합니다.

   * **[!UICONTROL Generate an error for numerical fields]**: 숫자 필드에 대한 오류를 생성하며, 그렇지 않으면 null 값을 삽입합니다.
   * **[!UICONTROL Insert NULL in the corresponding field]**: 빈 값을 허용합니다. null 값이 삽입됩니다.
   * **[!UICONTROL Generate an error]**: 값이 비어 있으면 오류를 생성합니다.

## Example {#example}

로드 파일 활동은 주로 기존 데이터에 데이터를 통합하기 위해 전송 파일 활동의 데이터를 구조화합니다.

다음 예는 파일 전송 활동을 통해 자동으로 다운로드한 로드 파일 활동의 결과와 그 뒤에 데이터 업데이트 기능을 보여 줍니다. 이 워크플로우는 Adobe Campaign 데이터베이스를 새 프로필로 보강하거나 가져온 파일에서 복구된 데이터를 사용하여 기존 프로필을 업데이트하는 것을 목표로 합니다.

1. **[!UICONTROL Transfer file]** 워크플로우를 워크플로우로 드래그하여 놓고 원하는 파일을 복구하도록 구성합니다.
1. **[!UICONTROL Load file]** 활동을 워크플로우로 드래그하여 놓고 **[!UICONTROL Transfer file]** 활동 뒤에 배치합니다.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. In the **[!UICONTROL File to load]** section of the **[!UICONTROL Execution]** tab, check the **[!UICONTROL Use the file specified in the inbound transition]** option.

   ![](assets/wkf_file_loading8.png)

1. 이전에 지정한 대로 활동을 구성합니다.
1. **[!UICONTROL Update data]** 활동을 워크플로우로 드래그하여 놓고 **[!UICONTROL Load file]** 활동 뒤에 배치한 다음 구성합니다. Refer to [Update data](../../automating/using/update-data.md).

워크플로우가 시작되면 업로드된 파일의 데이터가 추출되어 Adobe Campaign 데이터베이스를 보강하는 데 사용됩니다.
