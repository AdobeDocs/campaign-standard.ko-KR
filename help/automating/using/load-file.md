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
source-git-commit: fc3c687328c5a460b442b8b2497965ccab3be50b

---


# 파일 로드{#load-file}

## description {#description}

![](assets/data_loading.png)

**[!UICONTROL Load file]** 활동을 통해 데이터를 Adobe Campaign에서 사용할 수 있도록 구조화된 형태로 가져올 수 있습니다. 데이터는 일시적으로 가져온 것이며 다른 활동은 Adobe Campaign 데이터베이스에 명확하게 통합하기 위해 필요합니다.

## 사용 상황 {#context-of-use}

데이터가 추출될 방법은 활동이 구성될 때 정의됩니다. 로드할 파일은 연락처 목록이 될 수 있습니다.

>[!CAUTION]
>
>예를 들어.txt. csv 등 "일반" 구조 파일만 고려됩니다.

다음을 수행할 수 있습니다.

* 파일 구조를 사용하여 **[!UICONTROL Transfer file]** 다른 파일의 데이터 (활동을 사용하여 복구됨) 또는,
* 파일의 구조 및 데이터를 사용하여 Adobe Campaign로 가져옵니다.

## 구성 {#configuration}

활동 구성은 두 단계로 이루어집니다. 먼저 샘플 파일을 업로드하여 예상 파일 구조를 정의해야 합니다. 이 작업이 끝나면 데이터를 가져올 파일의 원본을 지정할 수 있습니다.

>[!NOTE]
>
>샘플 파일의 데이터는 활동을 구성하는 데 사용되지만 가져오지는 않습니다. 데이터가 거의 들어 있는 샘플 파일을 사용하는 것이 좋습니다.

1. **[!UICONTROL Load file]** 워크플로우를 워크플로우로 드래그하여 놓습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업에서 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 엽니다.
1. 최종 파일을 가져올 때 예상되는 구조를 정의할 수 있는 샘플 파일을 업로드합니다.

   ![](assets/wkf_file_loading.png)

   데이터 파일이 업로드되면 활동에 두 개의 새 탭이 나타납니다. **[!UICONTROL File structure]** **[!UICONTROL Column definition]** And.

1. **[!UICONTROL File structure]** 탭으로 이동하여 샘플 파일에서 자동으로 감지된 구조를 봅니다.

   파일 구조가 잘못 탐지된 경우 가능한 오류를 수정할 수 있는 옵션이 몇 가지 있습니다.

   * 옵션을 선택하여 다른 파일의 구조를 사용하도록 **[!UICONTROL Detect structure from a new file]** 선택할 수 있습니다.
   * 기본 감지 매개 변수를 수정하여 파일에 적용할 수 있습니다. **[!UICONTROL File type]** 이 필드에서 가져오려는 파일이 고정 길이의 열로 이루어져 있는지 지정할 수 있습니다. 이 경우, 탭의 각 열에 대한 최대 문자 수를 지정해야 **[!UICONTROL Column definition]** 합니다.

      파일에서 데이터를 올바르게 복구하는 데 필요한 모든 감지 옵션이 다시 **[!UICONTROL File format]**&#x200B;그룹화됩니다. 이러한 새로운 설정을 고려하여 활동에 로드된 마지막 파일의 구조를 다시 감지할 수 있습니다. 이렇게 하려면 **[!UICONTROL Apply configuration]** 단추를 사용합니다. 예를 들어, 다른 열 구분 기호를 지정할 수 있습니다.

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

   자세한 내용은 [열 형식](../../automating/using/load-file.md#column-format) 섹션을 참조하십시오.

   ![](assets/wkf_file_loading4.png)

1. **[!UICONTROL Execution]** 탭에서 데이터를 로드하기 위해 파일을 처리할 것인지 지정합니다.

   * 워크플로우에서 인바운드 전환을 가져옵니다.
   * 는 이전 단계에서 업로드한 항목입니다.
   * 은 로컬 컴퓨터에서 업로드할 새 파일입니다. 이 **[!UICONTROL Upload a new file from local machine]** 옵션은 워크플로우에 첫 번째 파일을 업로드한 경우 나타납니다. 이렇게 하면 현재 파일이 사용자의 요구 사항에 맞지 않는 경우 처리할 다른 파일을 업로드할 수 있습니다.

      ![](assets/wkf_file_loading1.png)

1. 데이터를 로드할 파일이 GZIP 파일 (.gz로 압축되는 경우 필드에서 **[!UICONTROL Decompression]** 해당 옵션을 **[!UICONTROL Add a pre-processing step]** 선택합니다. 이렇게 하면 데이터를 로드하기 전에 파일의 압축을 해제할 수 있습니다. 이 옵션은 해당 파일이 활동의 인바운드 전환에서 오는 경우에만 사용할 수 있습니다.
1. **[!UICONTROL Keep the rejects in a file]** 이 옵션을 사용하면 가져오는 동안 발생한 오류가 포함된 파일을 다운로드하고 후처리 단계에 적용할 수 있습니다.

   >[!NOTE]
   >
   >**[!UICONTROL Add date and time to the file name]** 이 옵션을 사용하면 거부사항이 포함된 파일의 이름을 타임스탬프를 추가할 수 있습니다.

   ![](assets/wkf_file_loading_keeprejects.png)

1. 활동의 구성을 확인하고 워크플로우를 저장합니다.

## 열 형식 {#column-format}

샘플 파일을 로드할 때 각 데이터 유형에 대한 기본 매개 변수와 함께 열 형식이 자동으로 검색됩니다. 특히 오류 또는 빈 값이 있을 때 데이터에 적용할 특정 프로세스를 지정할 수 있도록 이러한 기본 매개 변수를 수정할 수 있습니다.

이렇게 하려면 형식을 정의할 열의 빠른 작업 **[!UICONTROL Edit properties]** 중에서 선택합니다. 열 형식 세부 사항 창이 열립니다.

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

## 예제 1: 데이터베이스 업데이트 {#example-1-update-the-database}

로드 파일 활동은 주로 기존 데이터에 데이터를 통합하기 위해 전송 파일 활동의 데이터를 구조화합니다.

다음 예는 파일 전송 활동을 통해 자동으로 다운로드한 로드 파일 활동의 결과와 그 뒤에 데이터 업데이트 기능을 보여 줍니다. 이 워크플로우는 Adobe Campaign 데이터베이스를 새 프로필로 보강하거나 가져온 파일에서 복구된 데이터를 사용하여 기존 프로필을 업데이트하는 것을 목표로 합니다.

![](assets/load_file_workflow_ex1.png)

1. **[!UICONTROL Transfer file]** 워크플로우를 워크플로우로 드래그하여 놓고 원하는 파일을 복구하도록 구성합니다.
1. **[!UICONTROL Load file]** 활동을 워크플로우로 드래그하여 놓고 **[!UICONTROL Transfer file]** 활동 뒤에 배치합니다.
1. 활동을 선택한 다음 나타나는 빠른 작업에서 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 엽니다.
1. 탭의 **[!UICONTROL File to load]** 섹션에서 **[!UICONTROL Execution]****[!UICONTROL Use the file specified in the inbound transition]** 옵션을 선택합니다.

   ![](assets/wkf_file_loading8.png)

1. 이전에 지정한 대로 활동을 구성합니다.
1. **[!UICONTROL Update data]** 활동을 워크플로우로 드래그하여 놓고 **[!UICONTROL Load file]** 활동 뒤에 배치한 다음 구성합니다. 데이터 [업데이트를 참조하십시오](../../automating/using/update-data.md).

워크플로우가 시작되면 업로드된 파일의 데이터가 추출되어 Adobe Campaign 데이터베이스를 보강하는 데 사용됩니다.

## 예제 2: 강화된 필드가 포함된 이메일 전송 {#example-2-email-with-enriched-fields}

<!--A new example showing how to send an email containing additional data retrieved from a load file activity has been added. [Read more](../../automating/using/load-file.md#example-2-email-with-enriched-fields)-->

또한 파일 로드 활동을 통해 동일한 워크플로우에서 외부 파일의 추가 데이터로 강화된 이메일을 보낼 수 있습니다.

아래 예제는 로드 파일 활동을 통해 외부 파일에서 검색된 추가 데이터를 사용하여 이메일을 전송하는 방법을 보여줍니다. 이 예에서 외부 파일에는 연결된 계정 번호와 함께 프로필 목록이 포함되어 있습니다. 이 데이터를 가져와서 계정 번호와 함께 각 프로필에 이메일을 보냅니다.

![](assets/load_file_workflow_ex2.png)

1. **[!UICONTROL Query]** 활동을 워크플로우로 드래그하여 놓고 열어서 기본 타겟을 정의합니다.

   <!--The Query activity is presented in the [Query](../../automating/using/query.md) section.-->

1. 활동에 일부 데이터를 할당하려면 **[!UICONTROL Load file]** 활동을 끌어다 놓으십시오. 이 예에서는 데이터베이스의 일부 프로필에 해당하는 계정 번호가 들어 있는 파일을 로드합니다.

   ![](assets/load_file_activity.png)

1. **[!UICONTROL Enrichment]** 활동을 워크플로우로 드래그하여 놓고 로드 파일과 쿼리 활동을 연결합니다.

1. 강화 활동의 **[!UICONTROL Advanced relations]** 탭에서를 선택하고 **[!UICONTROL 0 or 1 cardinality simple link]** 조정에 사용할 필드를 정의합니다. 여기서는 성을 사용하여 데이터를 데이터베이스 프로파일과 조정합니다.

   ![](assets/load_file_enrichment_relation.png)

1. **[!UICONTROL Additional data]** 탭에서 이메일에 사용할 요소를 선택합니다. 여기에서 계정 번호 (로드 파일 활동을 통해 검색한 파일에서 열) 를 선택합니다.

   ![](assets/load_file_enrichment_select_element.png)

   <!--![](assets/load_file_enrichment_additional_data.png)-->

   이에 대한 자세한 내용은 [강화](../../automating/using/enrichment.md) 섹션을 참조하십시오.

1. **[!UICONTROL Segmentation]** 활동을 워크플로우로 드래그하여 놓고 열면 기본 타겟이 세분화됩니다.

   ![](assets/load_file_segmentation.png)

   이에 대한 자세한 내용은 [세그멘테이션](../../automating/using/segmentation.md) 섹션을 참조하십시오.

1. **[!UICONTROL Email delivery]** 워크플로우를 워크플로우로 드래그하여 놓고 엽니다.

   <!--The Email delivery activity is presented in the [Email delivery](../../automating/using/email-delivery.md) section.-->

1. 개인화 필드를 추가하고 **[!UICONTROL Additional data (targetData)]** 노드에서 강화 활동 (계정 번호) 에 정의된 추가 데이터를 선택합니다. 이렇게 하면 이메일 컨텐츠에서 각 프로필의 계정 번호를 동적으로 검색할 수 있습니다.

   ![](assets/load_file_perso_field.png)

1. 이메일을 저장하고 워크플로우를 시작합니다.

이메일이 Target로 전송됩니다. 각 프로필은 해당 계정 번호와 함께 이메일을 받습니다.

![](assets/load_file_email.png)
