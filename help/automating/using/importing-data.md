---
title: 데이터 가져오기
seo-title: 데이터 가져오기
description: 데이터 가져오기
seo-description: 워크플로우로 데이터를 가져오는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: d 909 d 26 a-cf 50-46 af-ae 09-f 0 fd 7258 ca 27
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: workflow-general-operation
discoiquuid: 75 b 83165-DCBD -4 BB 7-B 703-ED 769 F 489 B 16
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 6748e59aaeafce9dc6e77dc0664a9024a53c3e35

---


# Importing data{#importing-data}

## Collecting data {#collecting-data}

파일의 데이터를 수집하여 처리하고 Adobe Campaign 데이터베이스에서 가져올 수 있습니다.

* **[!UICONTROL Load file]** 활동을 통해 데이터를 Adobe Campaign에서 사용할 수 있도록 구조화된 형태로 가져올 수 있습니다. 데이터는 일시적으로 가져온 것이며 다른 활동은 Adobe Campaign 데이터베이스에 명확하게 통합하기 위해 필요합니다.
* **[!UICONTROL Transfer file]** 이 활동을 통해 파일을 받거나 보내거나 파일이 있는지 여부를 테스트하거나 Adobe Campaign에 파일을 표시할 수 있습니다.

   You can use this activity before a **[!UICONTROL Load file]** in case you need to retrieve the file from an external source.

## Import best practices {#import-best-practices}

주의해야 하며 아래 설명된 몇 가지 간단한 규칙을 따르면 데이터베이스 내의 데이터 일관성을 보장할 뿐만 아니라 데이터베이스 업데이트 또는 데이터 내보내기 중에 일반적인 오류를 방지할 수 있습니다.

### Using import templates {#using-import-templates}

Most import workflows should contain the following activities: **[!UICONTROL Load file]**, **[!UICONTROL Reconciliation]**, **[!UICONTROL Segmentation]**, **[!UICONTROL Deduplication]**, **[!UICONTROL Update data]**.

템플릿 가져오기를 사용하면 비슷한 가져오기를 준비하고 데이터베이스 내에서 데이터를 일관되게 유지할 수 있어 매우 편리합니다.

In many projects, imports are built without **[!UICONTROL Deduplication]** activity because the files used in the project do not have duplicates. 때로 다른 파일을 가져올 때 중복이 발생합니다. 중복 제거는 까다롭습니다. 따라서 중복 제거 단계는 모든 가져오기 워크플로우에 있어서 좋은 사전 조치입니다.

수신 데이터가 일관되고 정확하다는 가정 또는 IT 부서 또는 Adobe Campaign 슈퍼바이저가 IT 부서의 조치를 취할 것이라는 가정 하에 휴식을 취하지 마십시오. 프로젝트 중에 데이터 정리를 염두에 두십시오. 데이터를 가져올 때 중복 제거, 조정 및 일관성 유지

An example of a generic workflow template designed for importing data is available in the [Example: Import workflow template](../../automating/using/importing-data.md#example--import-workflow-template) section.

>[!NOTE]
>
>You can also use [import templates](../../automating/using/importing-data-with-import-templates.md). 관리자가 정의한 워크플로우 템플릿으로서, 활성화한 후에는 가져올 데이터가 들어 있는 파일을 지정하는 경우에만 가능합니다.

### Using flat file formats {#using-flat-file-formats}

가장 효율적인 포맷은 일반 파일입니다. 일반 파일은 데이터베이스 수준에서 일괄 모드로 가져올 수 있습니다.

예를 들면 다음과 같습니다.

* 구분 기호: 탭 또는 세미콜론
* 머리글이 있는 첫 번째 라인
* 문자열 구분 기호 없음
* 날짜 형식: YYYY/MM/DD HH: MM: SS

가져올 파일 예:

```
lastname;firstname;birthdate;email;crmID
Smith;Hayden;23/05/1989;hayden.smith@example.com;124365
Mars;Daniel;17/11/1987;dannymars@example.com;123545
Smith;Clara;08/02/1989;hayden.smith@example.com;124567
Durance;Allison;15/12/1978;allison.durance@example.com;120987
```

### Using compression {#using-compression}

zip 파일을 사용하여 가능한 경우 가져오고 내보냅니다. GZIP는 기본적으로 지원됩니다. **[!UICONTROL Load file]** 각각 및 **[!UICONTROL Extract file]** 워크플로우 활동에서 데이터를 추출할 때 파일 또는 사후 처리를 가져올 때 사전 처리를 추가할 수 있습니다.

### Importing in Delta mode {#importing-in-delta-mode}

일반 가져오기는 델타 모드에서 수행해야 합니다. 즉, 항상 전체 테이블 대신 수정된 데이터나 새 데이터가 Adobe Campaign로 전송됩니다.

전체 가져오기는 초기 로드에만 사용해야 합니다.

### Maintaining consistency {#maintaining-consistency}

Adobe Campaign 데이터베이스의 데이터 일관성을 유지하려면 아래 원칙을 따르십시오.

* 가져온 데이터가 Adobe Campaign의 참조 테이블과 일치하는 경우 워크플로우에서 해당 테이블과 조정되어야 합니다. 일치하지 않는 레코드는 거부되어야 합니다.
* Ensure that the imported data is always **"normalized"** (email, phone number, direct mail address) and that this normalization is reliable and will not change over the years. 이러한 경우가 아니라면, 일부 복제본은 데이터베이스에 나타날 가능성이 있으며, Adobe Campaign 에서는 "퍼지" 일치하기 위한 도구를 제공하지 않으므로, 이를 관리하고 제거하는 것은 매우 어렵습니다.
* 트랜잭션 데이터에는 중복 키가 있어야 하며 중복을 만들지 않도록 기존 데이터와 중재되어야 합니다.
* **관련 파일을 순서대로 가져올**&#x200B;수 있습니다. 가져오기가 서로 의존하는 여러 파일로 구성된 경우, 워크플로우는 파일을 올바른 순서로 가져왔는지 확인해야 합니다. 파일에 오류가 발생하면 다른 파일을 가져올 수 없습니다.
* **데이터를 가져올 때 중복 제거**, 조정 및 일관성 유지

## Example: Import workflow template {#example--import-workflow-template}

동일한 구조의 파일을 정기적으로 가져와야 하는 경우 가져오기 템플릿을 사용하는 것이 가장 좋습니다.

이 예에서는 Adobe Campaign 데이터베이스의 CRM에서 가져온 프로필을 가져오는 데 재사용할 수 있는 워크플로우를 미리 설정하는 방법을 보여줍니다.

1. Create a new workflow template from **[!UICONTROL Resources > Templates > Workflow templates]**.
1. 다음 활동을 추가합니다.

   * **[!UICONTROL Load file]**: 가져올 데이터가 들어 있는 파일의 예상 구조를 정의합니다.

      >[!NOTE]
      >
      >단일 파일에서 데이터를 가져올 수만 있습니다. If the workflow has multiple **[!UICONTROL Load file]** activities, the same file will be used each time.

   * **[!UICONTROL Reconciliation]**: 가져온 데이터를 데이터베이스 데이터와 함께 조정합니다.
   * **[!UICONTROL Segmentation]**: 필터를 만들어 중재할 수 있는지 여부에 따라 레코드를 다르게 처리합니다.
   * **[!UICONTROL Deduplication]**: 데이터베이스에 삽입 전에 들어오는 파일의 데이터를 중복 제거합니다.
   * **[!UICONTROL Update data]**: 가져온 프로필로 데이터베이스를 업데이트합니다.
   ![](assets/import_template_example0.png)

1. **[!UICONTROL Load file]** 활동 구성:

   * 샘플 파일을 업로드하여 예상 구조를 정의합니다. 샘플 파일에는 가져오기에 필요한 모든 열만 들어 있어야 합니다. 파일 형식을 확인하고 편집하여 각 열의 유형이 올바르게 설정되어 있는지 확인합니다. 텍스트, 날짜, 정수 등 예를 들면 다음과 같습니다.

      ```
      lastname;firstname;birthdate;email;crmID
      Smith;Hayden;23/05/1989;hayden.smith@mailtest.com;123456
      ```

   * **[!UICONTROL File to load]** 섹션에서 필드를 **[!UICONTROL Upload a new file from the local machine]** 선택하고 필드를 비워 둡니다. 이 템플릿에서 새 워크플로를 만들 때마다 정의된 구조에 해당하는 대로 여기에서 원하는 파일을 지정할 수 있습니다.

      원하는 옵션을 사용할 수 있지만 그에 따라 템플릿을 수정해야 합니다. For example, if you select **[!UICONTROL Use the file specified in the inbound transition]**, you can add a **[!UICONTROL Transfer file]** activity before to retrieve the file to import from a FTP/SFTP server.

      If you want users to be able to download a file containing errors that occurred during an import, check the **[!UICONTROL Keep the rejects in a file]** option and specify the **[!UICONTROL File name]**.

      ![](assets/import_template_example1.png)

1. **[!UICONTROL Reconciliation]** 활동을 구성합니다. 이 컨텍스트에서 이 활동의 목적은 들어오는 데이터를 식별하는 것입니다.

   * **[!UICONTROL Relations]** 탭에서 가져온 데이터와 수신자 타깃팅 차원 사이의 링크를 선택하고 **[!UICONTROL Create element]** 정의합니다 (차원 및 리소스 [](../../automating/using/query.md#targeting-dimensions-and-resources)타깃팅 참조). In this example, the **CRM ID** custom field is used to create the join condition. 고유한 레코드를 식별할 수 있도록 해주는 필드 또는 필드의 조합을 사용합니다.
   * **[!UICONTROL Identification]** 탭에서 **[!UICONTROL Identify the document from the working data]** 옵션을 선택 해제한 상태로 둡니다.
   ![](assets/import_template_example2.png)

1. Configure the **[!UICONTROL Segmentation]** activity to retrieve reconciled recipients in one transition and recipients that could not be reconciled but who have enough data in a second transition.

   그러면 중재된 받는 사람이 있는 전환을 사용하여 데이터베이스를 업데이트할 수 있습니다. 그런 다음 파일에 최소 정보를 사용할 수 있는 경우 알 수 없는 수신자와 전환을 사용하여 데이터베이스에 새 수신자 항목을 만들 수 있습니다.

   조정할 수 없고 데이터가 충분하지 않은 수신자는 아웃바운드 아웃바운드 전환 시 선택되어 별도의 파일로 내보내거나 무시하기만 하면 됩니다.

   * In the **[!UICONTROL General]** tab of the activity, set the **[!UICONTROL Resource type]** to **[!UICONTROL Temporary resource]** and select **[!UICONTROL Reconciliation]** as the targeted set.
   * **[!UICONTROL Advanced options]** 탭에서 **[!UICONTROL Generate complement]** 데이터베이스에 레코드를 삽입할 수 없는지 확인하려면 옵션을 선택합니다. 필요한 경우 추가 처리를 보완 데이터에 적용할 수 있습니다. 파일 내보내기, 목록 업데이트 등
   * **[!UICONTROL Segments]** 탭의 첫 번째 세그먼트에서 인바운드 모집단에 필터링 조건을 추가하여 프로필의 CRM ID가 0 이 아닌 레코드만 선택합니다. 이렇게 하면 데이터베이스의 프로파일과 조정되는 파일의 데이터가 해당 하위 세트에서 선택됩니다.

      ![](assets/import_template_example3.png)

   * 데이터베이스에 삽입할 데이터가 충분히 있는 분리되지 않은 레코드를 선택하는 두 번째 세그먼트를 추가합니다. 예를 들면 다음과 같습니다. 이메일 주소, 이름 및 성. 중재되지 않은 레코드는 프로필의 CRM ID 값이 0와 같습니다.

      ![](assets/import_template_example3_2.png)

   * All records that are not selected in the first two subsets are selected in the **[!UICONTROL Complement]**.

1. Configure the **[!UICONTROL Update data]** activity located after the first outbound transition of the **[!UICONTROL Segmentation]** activity configured previously.

   * Select **[!UICONTROL Update]** as **[!UICONTROL Operation type]** since the inbound transition only contains recipients already present in the database.
   * **[!UICONTROL Identification]** 탭에서 - 이 사례의 - 프로필 간 키를 선택하고 **[!UICONTROL Using reconciliation criteria]****[!UICONTROL Dimension to update]****[!UICONTROL Reconciliation]** 활동에서 만들어진 링크를 선택합니다. In this example, the **CRM ID** custom field is used.

      ![](assets/import_template_example6.png)

   * **[!UICONTROL Fields to update]** 탭에서 업데이트할 프로필 차원 필드를 파일에서 해당 열의 값으로 표시합니다. 파일 열의 이름이 수신자 차원 필드의 이름과 같거나 거의 일치하면 자동 선택 단추를 사용하여 다른 필드를 자동으로 일치시킬 수 있습니다.

      ![](assets/import_template_example6_2.png)

      >[!NOTE]
      >
      >이러한 프로필에 직접 메일을 전송할 계획이라면 우편 주소가 DM 공급자에게 반드시 있어야 하므로 우편 주소를 포함해야 합니다. Also make sure that the **[!UICONTROL Address specified]** box in your profiles' information is checked. To update this option from a workflow, simply add an element to the fields to update, and specify **1** as **[!UICONTROL Source]** and select the **postalAddress/@addrDefined** field as **[!UICONTROL Destination]**. For more on direct mail and the use of the **[!UICONTROL Address specified]** option, see [this document](../../channels/using/about-direct-mail.md#recommendations).

1. Configure the **[!UICONTROL Deduplication]** activity located after the transition containing unreconciled profiles:

   * **[!UICONTROL Properties]** 탭에서 워크플로우 **[!UICONTROL Resource type]****[!UICONTROL Reconciliation]** 활동에서 생성된 임시 리소스로를 설정합니다.

      ![](assets/import_template_example4.png)

   * 이 예에서, 이메일 필드는 고유한 프로필을 찾는 데 사용됩니다. 입력한 모든 필드와 고유한 조합의 일부를 사용할 수 있습니다.
   * **[!UICONTROL Deduplication method]** A를 선택합니다. 이 경우 애플리케이션은 중복의 경우에 보존할 레코드를 자동으로 결정합니다.
   ![](assets/import_template_example7.png)

1. Configure the **[!UICONTROL Update data]** activity located after the **[!UICONTROL Deduplication]** activity configured previously.

   * Select **[!UICONTROL Insert only]** as **[!UICONTROL Operation type]** since the inbound transition only contains profiles not present in the database.
   * **[!UICONTROL Identification]** 탭에서 - 이 사례의 - 프로필 간 키를 선택하고 **[!UICONTROL Using reconciliation criteria]****[!UICONTROL Dimension to update]****[!UICONTROL Reconciliation]** 활동에서 만들어진 링크를 선택합니다. In this example, the **CRM ID** custom field is used.

      ![](assets/import_template_example6.png)

   * **[!UICONTROL Fields to update]** 탭에서 업데이트할 프로필 차원 필드를 파일에서 해당 열의 값으로 표시합니다. 파일 열의 이름이 수신자 차원 필드의 이름과 같거나 거의 일치하면 자동 선택 단추를 사용하여 다른 필드를 자동으로 일치시킬 수 있습니다.

      ![](assets/import_template_example6_2.png)

      >[!NOTE]
      >
      >이러한 프로필에 직접 메일을 전송할 계획이라면 우편 주소가 DM 공급자에게 반드시 있어야 하므로 우편 주소를 포함해야 합니다. Also make sure that the **[!UICONTROL Address specified]** box in your profiles' information is checked. To update this option from a workflow, simply add an element to the fields to update, and specify **1** as **[!UICONTROL Source]** and select the **[postalAddress/@addrDefined]** field as **[!UICONTROL Destination]**. For more on direct mail and the use of the **[!UICONTROL Address specified]** option, see [this document](../../channels/using/about-direct-mail.md#recommendations).

1. **[!UICONTROL Segmentation]** 활동의 세 번째 전환 후 데이터베이스에 삽입되지 않은 데이터를 추적하려는 경우 **[!UICONTROL Extract file]** 활동 및 **[!UICONTROL Transfer file]** 활동을 추가합니다. 필요한 열을 내보내고 파일을 검색할 수 있는 FTP 또는 SFTP 서버에서 파일을 전송하려면 해당 활동을 구성합니다.
1. **[!UICONTROL End]** 활동을 추가하고 워크플로우 템플릿을 저장합니다.

이제 템플릿을 사용할 수 있으며 모든 새 워크플로에 사용할 수 있습니다. All is needed is then to specify the file containing the data to import in the **[!UICONTROL Load file]** activity.

![](assets/import_template_example9.png)

