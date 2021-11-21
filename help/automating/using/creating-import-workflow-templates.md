---
title: 데이터를 가져오기 위한 워크플로우 템플릿 만들기
description: 데이터를 가져오기 위해 워크플로우 템플릿을 만드는 방법을 알아봅니다.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
feature: Workflows
role: Data Architect
level: Experienced
exl-id: 5974a52c-8721-4575-b452-2982d6497235
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '1172'
ht-degree: 1%

---

# 데이터를 가져오기 위한 워크플로우 템플릿 만들기 {#import-workflow-template}

가져오기 템플릿을 사용하는 것은 구조가 동일한 파일을 정기적으로 가져와야 하는 경우에 가장 좋습니다.

This example shows how to pre-set a workflow that can be reused for importing profiles coming from a CRM in the Adobe Campaign database.

1. 에서 새 워크플로우 템플릿 만들기 **[!UICONTROL Resources > Templates > Workflow templates]**.
1. 다음 활동을 추가합니다.

   * **[!UICONTROL Load file]**: 가져올 데이터가 포함된 파일의 예상 구조를 정의합니다.

      >[!NOTE]
      >
      >하나의 파일만 가져올 수 있습니다. 워크플로우에 여러 개가 있는 경우 **[!UICONTROL Load file]** 활동마다 동일한 파일이 사용됩니다.

   * **[!UICONTROL Reconciliation]**: 가져온 데이터를 데이터베이스 데이터로 조정합니다.
   * **[!UICONTROL Segmentation]**: 필터를 만들어 레코드를 조정할 수 있는지 여부에 따라 다르게 처리합니다.
   * **[!UICONTROL Deduplication]**: 데이터베이스에 삽입되기 전에 들어오는 파일에서 데이터를 중복 제거합니다.
   * **[!UICONTROL Update data]**: Update the database with the imported profiles.

   ![](assets/import_template_example0.png)

1. 구성 **[!UICONTROL Load file]** 활동:

   * Define the expected structure by uploading a sample file. The sample file should contain only a few lines but all the columns necessary for the import. 파일 형식을 확인하고 편집하여 각 열의 유형이 올바르게 설정되었는지 확인합니다. 텍스트, 날짜, 정수 등 예제:

      ```
      lastname;firstname;birthdate;email;crmID
      Smith;Hayden;23/05/1989;hayden.smith@mailtest.com;123456
      ```

   * 에서 **[!UICONTROL File to load]** 섹션, **[!UICONTROL Upload a new file from the local machine]** 필드를 비워 둡니다. 이 템플릿에서 새 워크플로우를 만들 때마다 정의된 구조에 해당하는 한 여기에 원하는 파일을 지정할 수 있습니다.

      옵션을 사용할 수 있지만 그에 따라 템플릿을 수정해야 합니다. 예를 들어 **[!UICONTROL Use the file specified in the inbound transition]**&#x200B;를 추가할 수 있습니다. **[!UICONTROL Transfer file]** 활동 전에 FTP/SFTP 서버에서 가져올 파일을 검색합니다.

      If you want users to be able to download a file containing errors that occurred during an import, check the **[!UICONTROL Keep the rejects in a file]** option and specify the **[!UICONTROL File name]**.

      ![](assets/import_template_example1.png)

1. 구성 **[!UICONTROL Reconciliation]** 활동. 이 컨텍스트에서 이 활동의 목적은 들어오는 데이터를 식별하는 것입니다.

   * 에서 **[!UICONTROL Relations]** 탭, 선택 **[!UICONTROL Create element]** 가져온 데이터와 수신자 타겟팅 차원 간의 링크를 정의합니다(참조). [타겟팅 차원 및 리소스](../../automating/using/query.md#targeting-dimensions-and-resources)). 이 예에서 **CRM ID** 사용자 지정 필드는 조인 조건을 만드는 데 사용됩니다. 고유한 레코드를 식별할 수 있는 한 필요한 필드 또는 필드 조합을 사용하십시오.
   * In the **[!UICONTROL Identification]** tab, leave the **[!UICONTROL Identify the document from the working data]** option unchecked.

   ![](assets/import_template_example2.png)

1. Configure the **[!UICONTROL Segmentation]** activity to retrieve reconciled recipients in one transition and recipients that could not be reconciled but who have enough data in a second transition.

   조정된 수신자와 함께 전환하여 데이터베이스를 업데이트하는 데 사용할 수 있습니다. 그러면 알 수 없는 수신자가 있는 전환을 사용하여 파일에서 최소 정보 세트를 사용할 수 있는 경우 데이터베이스에서 새 수신자 항목을 만들 수 있습니다.

   조정할 수 없고 데이터가 충분하지 않은 수신자는 아웃바운드 전환을 보완하여 선택되며 별도의 파일로 내보내거나 무시하면 됩니다.

   * 에서 **[!UICONTROL General]** 활동의 탭에서 **[!UICONTROL Resource type]** to **[!UICONTROL Temporary resource]** 을(를) 선택합니다. **[!UICONTROL Reconciliation]** 를 타깃팅된 세트로 설정합니다.
   * 에서 **[!UICONTROL Advanced options]** 탭에서 다음을 확인합니다 **[!UICONTROL Generate complement]** 데이터베이스에 레코드를 삽입할 수 없는지 확인하는 옵션입니다. 필요한 경우 보완 데이터에 추가 처리를 적용할 수 있습니다. 파일 내보내기, 목록 업데이트 등
   * 의 첫 번째 세그먼트에서 **[!UICONTROL Segments]** 탭에서 인바운드 모집단에 필터링 조건을 추가하여 프로필의 CRM ID가 0과 같지 않은 레코드만 선택합니다. 이렇게 하면 데이터베이스의 프로필과 조정된 파일의 데이터가 해당 하위 집합에서 선택됩니다.

      ![](assets/import_template_example3.png)

   * 데이터베이스에 삽입할 충분한 데이터가 있는 조정되지 않은 레코드를 선택하는 두 번째 세그먼트를 추가합니다. For example: email address, first name and last name. 조정되지 않은 레코드에는 해당 프로필의 CRM ID 값이 0과 같은 값이 있습니다.

      ![](assets/import_template_example3_2.png)

   * All records that are not selected in the first two subsets are selected in the **[!UICONTROL Complement]**.

1. Configure the **[!UICONTROL Update data]** activity located after the first outbound transition of the **[!UICONTROL Segmentation]** activity configured previously.

   * 선택 **[!UICONTROL Update]** 로서의 **[!UICONTROL Operation type]** 인바운드 전환에는 데이터베이스에 이미 있는 수신자만 포함되므로
   * 에서 **[!UICONTROL Identification]** 탭, 선택 **[!UICONTROL Using reconciliation criteria]** 및 **[!UICONTROL Dimension to update]** - 이 경우 프로필 및 **[!UICONTROL Reconciliation]** 활동. 이 예에서 **CRM ID** 사용자 지정 필드가 사용됩니다.

      ![](assets/import_template_example6.png)

   * 에서 **[!UICONTROL Fields to update]** 탭에서 프로필 차원의 필드를 지정하여 파일의 해당 열 값으로 업데이트합니다. 파일 열의 이름이 수신자 차원 필드의 이름과 동일하거나 거의 동일한 경우 자동 선택 단추를 사용하여 다른 필드를 자동으로 일치시킬 수 있습니다.

      ![](assets/import_template_example6_2.png)

      >[!NOTE]
      >
      >If you plan on sending direct mails to these profiles, make sure to include a postal address as this information is essential to the direct mail provider. 또한 **[!UICONTROL Address specified]** 프로필 정보에 있는 상자가 선택됩니다. To update this option from a workflow, simply add an element to the fields to update, and specify **1** as **[!UICONTROL Source]** and select the `postalAddress/@addrDefined` field as **[!UICONTROL Destination]**. For more on direct mail and the use of the **[!UICONTROL Address specified]** option, see [this document](../../channels/using/about-direct-mail.md#recommendations).

1. 구성 **[!UICONTROL Deduplication]** 조정되지 않은 프로필이 포함된 전환 뒤에 있는 활동:

   * 에서 **[!UICONTROL Properties]** 탭에서 설정합니다. **[!UICONTROL Resource type]** 에서 생성된 임시 리소스로 **[!UICONTROL Reconciliation]** 워크플로우의 활동.

      ![](assets/import_template_example4.png)

   * 이 예제에서는 이메일 필드를 사용하여 고유한 프로필을 찾습니다. 입력되어 있는 모든 필드와 고유한 조합의 일부를 사용할 수 있습니다.
   * 선택 **[!UICONTROL Deduplication method]**. 이 경우 중복 시 보존되는 레코드를 애플리케이션에서 자동으로 결정합니다.

   ![](assets/import_template_example7.png)

1. 구성 **[!UICONTROL Update data]** 활동 뒤에 있음 **[!UICONTROL Deduplication]** 활동이 이전에 구성되었습니다.

   * 선택 **[!UICONTROL Insert only]** 로서의 **[!UICONTROL Operation type]** 인바운드 전환에는 데이터베이스에 없는 프로필만 포함되어 있습니다.
   * In the **[!UICONTROL Identification]** tab, select **[!UICONTROL Using reconciliation criteria]** and define a key between the **[!UICONTROL Dimension to update]** - Profiles in this case - and the link created in the **[!UICONTROL Reconciliation]** activity. In this example, the **CRM ID** custom field is used.

      ![](assets/import_template_example6.png)

   * 에서 **[!UICONTROL Fields to update]** 탭에서 프로필 차원의 필드를 지정하여 파일의 해당 열 값으로 업데이트합니다. If the names of the file columns are identical or almost identical to the names of the recipients dimension fields, you can use the magic wand button to automatically match the different fields.

      ![](assets/import_template_example6_2.png)

      >[!NOTE]
      >
      >If you plan on sending direct mails to these profiles, make sure to include a postal address as this information is essential to the direct mail provider. 또한 **[!UICONTROL Address specified]** 프로필 정보에 있는 상자가 선택됩니다. 워크플로우에서 이 옵션을 업데이트하려면 업데이트할 필드에 요소를 추가하고 **1** 로서의 **[!UICONTROL Source]** 을(를) 선택하고 을(를) 선택합니다. **[postalAddress/@addrDefined]** 필드 **[!UICONTROL Destination]**. DM 및 사용 방법에 대한 자세한 내용 **[!UICONTROL Address specified]** 옵션을 참조하십시오. [이 문서](../../channels/using/about-direct-mail.md#recommendations).

1. 의 세 번째 전환 후 **[!UICONTROL Segmentation]** 활동, 추가 **[!UICONTROL Extract file]** 활동 및 **[!UICONTROL Transfer file]** 데이터베이스에 삽입되지 않은 데이터를 추적하려면 활동. 필요한 열을 내보내고 파일을 검색할 수 있는 FTP 또는 SFTP 서버에서 파일을 전송하도록 활동을 구성합니다.
1. 추가 **[!UICONTROL End]** 활동을 수행하고 워크플로우 템플릿을 저장합니다.

The template can now be used and is available for every new workflow. 그런 다음 가져올 데이터가 포함된 파일을 지정해야 합니다 **[!UICONTROL Load file]** 활동.

![](assets/import_template_example9.png)
