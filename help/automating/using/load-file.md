---
title: 파일 로드
description: 파일 로드 활동을 사용하면 Adobe Campaign에서 이 데이터를 사용하기 위해 구조화된 하나의 양식으로 데이터를 가져올 수 있습니다.
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
source-git-commit: 867215b295a7539d8499fa0bb1865605695da020

---


# 파일 로드 {#load-file}

## 설명 {#description}

![](assets/data_loading.png)

이 **[!UICONTROL Load file]** 활동을 사용하면 Adobe Campaign에서 이 데이터를 사용하기 위해 구조화된 하나의 양식으로 데이터를 가져올 수 있습니다. 데이터를 일시적으로 가져오며 Adobe Campaign 데이터베이스에 통합하려면 다른 활동이 필요합니다.

## 사용 상황 {#context-of-use}

데이터를 추출하는 방법은 활동이 구성될 때 정의됩니다. 로드할 파일은 연락처 목록일 수 있습니다(예:

>[!CAUTION]
>
>예를 들어 .txt, .csv 등 "플랫" 구조 파일만 고려됩니다.

다음 작업을 수행할 수 있습니다.

* 파일 구조를 사용하여 다른 파일의 데이터에 적용( **[!UICONTROL Transfer file]** 활동을 사용하여 복구) 또는
* 파일의 구조와 데이터를 사용하여 Adobe Campaign으로 가져옵니다.

## 구성 {#configuration}

활동 구성에는 두 단계가 포함됩니다. 먼저 샘플 파일을 업로드하여 예상 파일 구조를 정의해야 합니다. 이렇게 하면 데이터를 가져올 파일의 원본을 지정할 수 있습니다.

>[!NOTE]
>
>샘플 파일의 데이터는 활동을 구성하는 데 사용되지만 가져오지 않습니다. 데이터가 거의 없는 샘플 파일을 사용하는 것이 좋습니다.

1. 워크플로우를 워크플로우로 드래그하여 **[!UICONTROL Load file]** 놓을 수 있습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 엽니다.
1. 최종 파일을 가져올 때 예상 구조를 정의할 수 있는 샘플 파일을 업로드합니다.

   ![](assets/wkf_file_loading.png)

   데이터 파일이 업로드되면 두 개의 새 탭이 활동에 표시됩니다. **[!UICONTROL File structure]** 및 **[!UICONTROL Column definition]** Adobe

1. 샘플 파일에서 자동으로 감지된 구조를 보려면 **[!UICONTROL File structure]** 탭으로 이동합니다.

   파일 구조가 잘못 검색된 경우 다음과 같은 몇 가지 옵션을 사용하여 가능한 오류를 수정할 수 있습니다.

   * 옵션을 선택하여 다른 파일의 구조를 사용하도록 선택할 수 **[!UICONTROL Detect structure from a new file]** 있습니다.
   * 기본 감지 매개 변수를 수정하여 파일에 적용할 수 있습니다. 이 **[!UICONTROL File type]** 필드를 사용하면 가져오려는 파일이 고정된 길이의 열로 구성되어 있는지 여부를 지정할 수 있습니다. 이 경우 **[!UICONTROL Column definition]** 탭에서 각 열에 대한 최대 문자 수를 지정해야 합니다.

      파일에서 데이터를 올바로 복구하는 데 필요한 모든 감지 옵션이 로 다시 그룹화됩니다 **[!UICONTROL File format]**. 이러한 설정을 수정한 다음 이 새로운 설정을 고려하여 활동에 로드된 마지막 파일의 구조를 다시 감지할 수 있습니다. 이렇게 하려면 **[!UICONTROL Apply configuration]** 단추를 사용하십시오. 예를 들어 다른 열 구분 기호를 지정할 수 있습니다.

      >[!NOTE]
      >
      >이 작업은 활동에 마지막으로 로드한 파일을 고려합니다. 감지된 파일이 크면 데이터 미리 보기에는 처음 30줄만 표시됩니다.

      ![](assets/wkf_file_loading3.png)

      섹션에서 이 **[!UICONTROL File format]** **[!UICONTROL Check columns from file against column definitions]** 옵션을 사용하여 업로드하는 파일의 열이 열 정의에 해당하는지 확인할 수 있습니다.

      열 수 및/또는 이름이 열 정의와 일치하지 않으면 워크플로우를 실행할 때 오류 메시지가 표시됩니다. 이 옵션이 활성화되지 않으면 경고가 로그 파일에 표시됩니다.

      ![](assets/wkf_file_loading_check.png)

1. 탭으로 이동하여 각 열에 대한 데이터 형식을 확인하고 필요한 경우 매개 변수를 조정합니다. **[!UICONTROL Column definition]**

   이 **[!UICONTROL Column definition]** 탭에서는 오류가 포함되지 않은 데이터(예: null 관리 사용)를 가져와서 이후 작업을 위해 Adobe Campaign 데이터베이스에 이미 있는 유형과 일치하도록 하기 위해 각 열의 데이터 구조를 정확하게 지정할 수 있습니다.

   예를 들어 열의 레이블을 변경하고 해당 유형(문자열, 정수, 날짜 등)을 선택할 수 있습니다. 오류 처리를 지정할 수도 있습니다.

   자세한 내용은 열 [형식](#column-format) 섹션을 참조하십시오.

   ![](assets/wkf_file_loading4.png)

1. 탭에서 데이터 로드를 위해 파일을 처리할지 여부를 **[!UICONTROL Execution]** 지정합니다.

   * 워크플로우의 인바운드 전환에서 가져옵니다.
   * 이전 단계에서 업로드한 것입니다.
   * 로컬 컴퓨터에서 업로드할 새 파일입니다. 첫 번째 파일을 업로드하는 것이 워크플로우에 이미 정의된 경우 이 **[!UICONTROL Upload a new file from local machine]** 옵션이 나타납니다. 따라서 현재 파일이 사용자의 요구 사항에 맞지 않을 경우 처리할 다른 파일을 업로드할 수 있습니다.

      ![](assets/wkf_file_loading1.png)

1. 데이터를 로드할 파일이 GZIP 파일(.gz)로 압축되면 **[!UICONTROL Decompression]** **[!UICONTROL Add a pre-processing step]** 필드에서 옵션을 선택합니다. 데이터를 로드하기 전에 파일의 압축을 해제할 수 있습니다. 이 옵션은 활동이 인바운드 전환에서 파일을 가져오는 경우에만 사용할 수 있습니다.
1. 이 **[!UICONTROL Keep the rejects in a file]** 옵션을 사용하면 가져오는 동안 발생한 오류가 포함된 파일을 다운로드하여 사후 처리 단계에 적용할 수 있습니다. 이 옵션이 활성화되면 아웃바운드 전환 이름이 "거부"로 바뀝니다.

   >[!NOTE]
   >
   >이 **[!UICONTROL Add date and time to the file name]** 옵션을 사용하면 배지를 포함하는 파일의 이름에 타임스탬프를 추가할 수 있습니다.

   ![](assets/wkf_file_loading_keeprejects.png)

1. 활동 구성을 확인하고 워크플로우를 저장합니다.

워크플로우를 실행한 후 활동에 오류가 발생하는 경우 로그를 참조하여 파일에서 잘못된 값에 대한 자세한 내용을 확인하십시오. For more on workflows logs, refer to [this section](../../automating/using/executing-a-workflow.md#monitoring)

## 열 형식 {#column-format}

샘플 파일을 로드할 때 각 데이터 유형의 기본 매개 변수와 함께 열 형식이 자동으로 검색됩니다. 특히 오류나 빈 값이 있는 경우 데이터에 적용할 특정 프로세스를 지정하기 위해 이러한 기본 매개 변수를 수정할 수 있습니다.

이렇게 하려면 형식을 정의할 열의 빠른 작업 **[!UICONTROL Edit properties]** 중에서 선택합니다. 열 형식 세부 정보 창이 열립니다.

![](assets/wkf_file_loading4.png)

그런 다음 각 열에 대한 서식을 수정할 수 있습니다.

열 서식을 사용하면 각 열의 값 처리를 정의할 수 있습니다.

* **[!UICONTROL Ignore column]**:은 데이터를 로드하는 동안 이 열을 처리하지 않습니다.
* **[!UICONTROL Data type]**:각 열에 필요한 데이터 유형을 지정합니다.
* **[!UICONTROL Format and separators]**, **속성**:텍스트 속성, 시간, 날짜 및 숫자 값 형식과 열 컨텍스트에 의해 지정된 구분 기호를 지정합니다.

   * **[!UICONTROL Maximum number of characters]**:문자열 유형 열의 최대 문자 수를 지정합니다.

      길이가 고정된 열로 구성된 파일을 로드할 때는 이 필드를 채워야 합니다.

   * **[!UICONTROL Letter case management]**:텍스트 데이터에 문자 대/소문자 프로세스를 적용해야 하는지 여부를 **정의합니다** .
   * **[!UICONTROL White space management]**:텍스트 데이터의 문자열에서 특정 공백을 무시할지 여부를 **지정합니다** .
   * **[!UICONTROL Time format]**, **[!UICONTROL Date format]**:날짜, 시간 **및**&#x200B;날짜 **및 시간** 데이터의 형식을 **지정합니다** .
   * **[!UICONTROL Format]**:정수 및 부동 번호 데이터에 대한 숫자 값 형식을 정의할 **수** **** 있습니다.
   * **[!UICONTROL Separator]**:separator를 열 컨텍스트(숫자 값의 천 또는 구분 기호, 날짜 및 시간의 **구분 문자)**, **시간**, **시간**, **날짜**&#x200B;및 시간 **, 정수,** 정수 및 부동 숫자 데이터로 정의합니다.

* **[!UICONTROL Remapping of values]**:이 필드는 열 세부 사항 구성에서만 사용할 수 있습니다. 특정 값을 가져올 때 변형할 수 있습니다. 예를 들어 "3"을 "3"으로 변환할 수 있습니다.
* **[!UICONTROL Error processing]**:오류가 발생하는 경우 동작을 정의합니다.

   * **[!UICONTROL Ignore the value]**:값이 무시됩니다. 워크플로우 실행 로그에 경고가 생성됩니다.
   * **[!UICONTROL Reject the line]**:전체 줄이 처리되지 않습니다.
   * **[!UICONTROL Use a default value]**:오류가 발생하는 값을 **[!UICONTROL Default value]** 필드에 정의된 기본값으로 바꿉니다.
   * **[!UICONTROL Use a default value in case the value is not remapped]**:잘못된 값에 대한 매핑이 정의되어 있지 않으면 오류가 발생하는 값을 **[!UICONTROL Default value]** 필드에 정의된 기본값으로 바꿉니다(위 **[!UICONTROL Remapping of values]** 옵션 참조).
   * **[!UICONTROL Reject the line when there is no remapping value]**:잘못된 값에 대해 매핑을 정의하지 않으면 전체 줄이 처리되지 않습니다(위 **[!UICONTROL Remapping of values]** 옵션 참조).
   >[!NOTE]
   >
   >**[!UICONTROL Error processing]** 가져온 파일의 값과 관련된 오류 발생. 예를 들어 잘못된 데이터 유형("정수" 열의 경우 모두 "4"), 허용된 최대 수보다 많은 문자를 포함하는 문자열, 잘못된 구분 기호가 있는 날짜 등이 있습니다. 그러나 이 옵션은 빈 값 관리로 생성된 오류에 대해서는 다루지 않습니다.

* **[!UICONTROL Default value]**:선택한 오류 처리에 따라 기본값을 지정합니다.
* **[!UICONTROL Empty value management]**:데이터를 로드하는 동안 빈 값을 관리하는 방법을 지정합니다.

   * **[!UICONTROL Generate an error for numerical fields]**:숫자 필드에 대해서만 오류를 생성하고, 그렇지 않으면 NULL 값을 삽입합니다.
   * **[!UICONTROL Insert NULL in the corresponding field]**:빈 값을 허용합니다. 따라서 NULL 값이 삽입됩니다.
   * **[!UICONTROL Generate an error]**:값이 비어 있으면 오류가 발생합니다.

## 예 1:데이터베이스 업데이트 {#example-1-update-the-database}

로드 파일 활동은 주로 기존 데이터에 통합하기 위해 전송 파일 작업의 데이터를 구성합니다.

다음 예제는 전송 파일 작업을 통해 자동으로 다운로드된 로드 파일 작업의 결과와 업데이트 데이터 활동을 보여줍니다. 이 워크플로우는 새 프로필로 Adobe Campaign 데이터베이스를 강화하거나 가져온 파일에서 복구된 데이터를 사용하여 기존 프로필을 업데이트하는 데 목적이 있습니다.

![](assets/load_file_workflow_ex1.png)

1. 작업을 워크플로우로 드래그하여 놓고 원하는 파일을 복구할 수 있도록 **[!UICONTROL Transfer file]** 구성합니다.
1. 활동을 워크플로우로 드래그하여 놓고 **[!UICONTROL Load file]** **[!UICONTROL Transfer file]** 활동 뒤에 배치합니다.
1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 엽니다.
1. 탭의 **[!UICONTROL File to load]** 섹션에서 **[!UICONTROL Execution]** **[!UICONTROL Use the file specified in the inbound transition]** 옵션을 선택합니다.

   ![](assets/wkf_file_loading8.png)

1. 앞에서 지정한 대로 활동을 구성합니다.
1. 활동을 워크플로우로 드래그하여 놓고 **[!UICONTROL Update data]** **[!UICONTROL Load file]** 활동 다음에 배치한 다음 구성합니다. 데이터 [업데이트를](../../automating/using/update-data.md)참조하십시오.

워크플로우가 시작되면 업로드된 파일의 데이터가 추출된 다음 Adobe Campaign 데이터베이스를 보완하는 데 사용됩니다.

## 예 2:풍부한 필드가 포함된 이메일 보내기 {#example-2-email-with-enriched-fields}

<!--A new example showing how to send an email containing additional data retrieved from a load file activity has been added. [Read more](example-2-email-with-enriched-fields)-->

또한 파일 로드 작업을 사용하면 동일한 워크플로우에서 외부 파일의 추가 데이터가 포함된 이메일을 보낼 수 있습니다.

아래 예제는 파일 로드 작업을 통해 외부 파일에서 검색된 추가 데이터를 사용하여 이메일을 보내는 방법을 보여줍니다. 이 예에서는 외부 파일에 연결된 계정 번호와 프로필 목록이 포함되어 있습니다. 이 데이터를 가져와 각 프로필에 계정 번호와 함께 이메일을 보내려는 경우

![](assets/load_file_workflow_ex2.png)

1. 워크플로우를 드래그하여 워크플로우에 **[!UICONTROL Query]** 놓고 열어서 기본 타겟을 정의합니다.

   <!--The Query activity is presented in the [Query](../../automating/using/query.md) section.-->

1. 활동을 드래그 앤 드롭하여 일부 데이터를 프로필에 할당합니다. **[!UICONTROL Load file]** 이 예에서는 데이터베이스의 일부 프로필에 해당하는 계정 번호가 포함된 파일을 로드합니다.

   ![](assets/load_file_activity.png)

1. 작업을 워크플로우로 드래그하여 놓고 로드 파일과 쿼리 활동을 해당 워크플로우에 연결합니다. **[!UICONTROL Enrichment]**

1. 농축활동 **[!UICONTROL Advanced relations]** 탭에서 조정을 위해 사용할 필드를 **[!UICONTROL 0 or 1 cardinality simple link]** 선택하고 정의합니다. 여기서 성은 데이터베이스 프로필과 데이터를 대사하기 위해 사용합니다.

   ![](assets/load_file_enrichment_relation.png)

1. 탭에서 이메일에 사용할 요소를 선택합니다. **[!UICONTROL Additional data]** 여기에서 계정 번호(로드 파일 작업을 통해 검색한 파일에서 열)를 선택합니다.

   ![](assets/load_file_enrichment_select_element.png)

   <!--![](assets/load_file_enrichment_additional_data.png)-->

   자세한 내용은 데이터 [수집 섹션을 참조하십시오](../../automating/using/enrichment.md) .

1. 워크플로우를 드래그하여 워크플로우에 **[!UICONTROL Segmentation]** 놓고 열어서 기본 타겟을 조정합니다.

   ![](assets/load_file_segmentation.png)

   자세한 내용은 세그멘테이션 [섹션을](../../automating/using/segmentation.md) 참조하십시오.

1. 워크플로우에 **[!UICONTROL Email delivery]** 활동을 드래그하여 놓고 엽니다.

   <!--The Email delivery activity is presented in the [Email delivery](../../automating/using/email-delivery.md) section.-->

1. 개인화 필드를 추가하고 **[!UICONTROL Additional data (targetData)]** 노드에서 농축활동에 정의된 추가 데이터(여기 계정 번호)를 선택합니다. 이렇게 하면 이메일 컨텐츠에서 각 프로필의 계정 번호를 동적으로 검색할 수 있습니다.

   ![](assets/load_file_perso_field.png)

1. 이메일을 저장하고 워크플로우를 시작합니다.

이메일이 타겟으로 전송됩니다. 각 프로필은 해당 계정 번호와 함께 이메일을 수신합니다.

![](assets/load_file_email.png)
