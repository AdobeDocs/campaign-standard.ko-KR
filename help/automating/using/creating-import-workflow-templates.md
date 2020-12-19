---
solution: Campaign Standard
product: campaign
title: 데이터를 가져오기 위한 워크플로우 템플릿 만들기
description: 데이터를 가져오는 워크플로우 템플릿을 만드는 방법을 알아봅니다.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '1172'
ht-degree: 1%

---


# 데이터를 가져오기 위한 워크플로우 템플릿 만들기 {#import-workflow-template}

가져오기 템플릿을 사용하는 것은 구조가 동일한 파일을 정기적으로 가져와야 하는 경우에 가장 좋습니다.

이 예에서는 Adobe Campaign 데이터베이스의 CRM에서 가져온 프로파일을 가져오는 데 다시 사용할 수 있는 워크플로우를 사전 설정하는 방법을 보여줍니다.

1. **[!UICONTROL Resources > Templates > Workflow templates]**&#x200B;에서 새 워크플로 템플릿을 만듭니다.
1. 다음 활동을 추가합니다.

   * **[!UICONTROL Load file]**:가져올 데이터가 포함된 파일의 예상 구조를 정의합니다.

      >[!NOTE]
      >
      >단일 파일에서 데이터만 가져올 수 있습니다. 워크플로에 여러 개의 **[!UICONTROL Load file]** 활동이 있는 경우 매번 동일한 파일이 사용됩니다.

   * **[!UICONTROL Reconciliation]**:가져온 데이터를 데이터베이스 데이터와 조정합니다.
   * **[!UICONTROL Segmentation]**:조정 가능 여부에 따라 필터를 만들어 레코드를 다르게 처리합니다.
   * **[!UICONTROL Deduplication]**:데이터베이스에 삽입하기 전에 들어오는 파일에서 데이터를 중복 제거합니다.
   * **[!UICONTROL Update data]**:가져온 프로필로 데이터베이스를 업데이트합니다.

   ![](assets/import_template_example0.png)

1. **[!UICONTROL Load file]** 활동을 구성합니다.

   * 샘플 파일을 업로드하여 예상 구조를 정의합니다. 샘플 파일은 가져올 수 있는 열을 모두 제외하고 몇 줄만 포함해야 합니다. 파일 형식을 확인하고 편집하여 각 열의 유형이 올바르게 설정되어 있는지 확인합니다.텍스트, 날짜, 정수 등 예제:

      ```
      lastname;firstname;birthdate;email;crmID
      Smith;Hayden;23/05/1989;hayden.smith@mailtest.com;123456
      ```

   * **[!UICONTROL File to load]** 섹션에서 **[!UICONTROL Upload a new file from the local machine]**&#x200B;을 선택하고 필드를 비워 둡니다. 이 템플릿에서 새 워크플로우를 만들 때마다 정의된 구조에 해당하는 한 원하는 파일을 여기에서 지정할 수 있습니다.

      옵션을 사용할 수 있지만 이에 따라 템플릿을 수정해야 합니다. 예를 들어 **[!UICONTROL Use the file specified in the inbound transition]**&#x200B;을 선택하면 FTP/SFTP 서버에서 가져올 파일을 검색하기 전에 **[!UICONTROL Transfer file]** 활동을 추가할 수 있습니다.

      사용자가 가져오는 동안 발생한 오류가 포함된 파일을 다운로드할 수 있게 하려면 **[!UICONTROL Keep the rejects in a file]** 옵션을 선택하고 **[!UICONTROL File name]**&#x200B;을 지정합니다.

      ![](assets/import_template_example1.png)

1. **[!UICONTROL Reconciliation]** 활동을 구성합니다. 이 컨텍스트에서 이 활동의 목적은 들어오는 데이터를 식별하기 위한 것입니다.

   * **[!UICONTROL Relations]** 탭에서 **[!UICONTROL Create element]**&#x200B;을 선택하고 가져온 데이터와 수신자의 타깃팅 차원 사이의 링크를 정의합니다([타게팅 차원 및 리소스](../../automating/using/query.md#targeting-dimensions-and-resources) 참조). 이 예에서 **CRM ID** 사용자 정의 필드를 사용하여 조인 조건을 만듭니다. 고유한 레코드를 식별할 수 있는 동안 필요한 필드 또는 필드 조합을 사용합니다.
   * **[!UICONTROL Identification]** 탭에서 **[!UICONTROL Identify the document from the working data]** 옵션을 선택 해제한 상태로 두십시오.

   ![](assets/import_template_example2.png)

1. 한 전환에서 대사된 받는 사람과 조정할 수 없지만 두 번째 전환에서는 충분한 데이터가 있는 받는 사람을 검색하려면 **[!UICONTROL Segmentation]** 활동을 구성합니다.

   조정된 받는 사람과의 전환을 사용하여 데이터베이스를 업데이트할 수 있습니다. 파일에서 최소 정보 세트를 사용할 수 있는 경우 알 수 없는 수신자가 있는 전환을 사용하여 데이터베이스에 새 받는 사람 항목을 만들 수 있습니다.

   조정할 수 없고 데이터가 충분하지 않은 수신자는 보정을 통해 아웃바운드 전환으로 선택되며 별도의 파일로 내보내거나 무시하면 됩니다.

   * 활동의 **[!UICONTROL General]** 탭에서 **[!UICONTROL Resource type]**&#x200B;을 **[!UICONTROL Temporary resource]**&#x200B;로 설정하고 **[!UICONTROL Reconciliation]**&#x200B;을 타깃팅된 세트로 선택합니다.
   * **[!UICONTROL Advanced options]** 탭에서 **[!UICONTROL Generate complement]** 옵션을 선택하여 데이터베이스에 레코드를 삽입할 수 없는지 확인합니다. 필요한 경우 보완 데이터에 추가 처리를 적용할 수 있습니다.파일 내보내기, 목록 업데이트 등
   * **[!UICONTROL Segments]** 탭의 첫 번째 세그먼트에서 프로필의 CRM ID가 0이 아닌 레코드만 선택하려면 인바운드 모집단에 필터링 조건을 추가합니다. 이렇게 하면 데이터베이스의 프로필과 일치된 파일의 데이터가 해당 하위 집합에서 선택됩니다.

      ![](assets/import_template_example3.png)

   * 데이터베이스에 삽입할 데이터를 충분히 가진 대사되지 않은 레코드를 선택하는 두 번째 세그먼트를 추가합니다. 예:이메일 주소, 이름 및 성. 대사되지 않은 레코드는 프로필의 CRM ID 값이 0과 같습니다.

      ![](assets/import_template_example3_2.png)

   * 처음 두 하위 세트에서 선택되지 않은 모든 레코드는 **[!UICONTROL Complement]**&#x200B;에서 선택됩니다.

1. 이전에 구성한 **[!UICONTROL Segmentation]** 활동의 첫 번째 아웃바운드 전환 뒤에 있는 **[!UICONTROL Update data]** 활동을 구성합니다.

   * 인바운드 전환에는 데이터베이스에 이미 있는 받는 사람만 포함되므로 **[!UICONTROL Update]**&#x200B;을 **[!UICONTROL Operation type]**&#x200B;으로 선택합니다.
   * **[!UICONTROL Identification]** 탭에서 **[!UICONTROL Using reconciliation criteria]**&#x200B;을 선택하고 **[!UICONTROL Dimension to update]** - 이 경우 프로필과 **[!UICONTROL Reconciliation]** 활동에서 만든 링크 사이에 키를 정의합니다. 이 예에서 **CRM ID** 사용자 정의 필드가 사용됩니다.

      ![](assets/import_template_example6.png)

   * **[!UICONTROL Fields to update]** 탭에서 파일의 해당 열 값으로 업데이트할 프로필 차원의 필드를 지정합니다. 파일 열 이름이 받는 사람 차원 필드의 이름과 동일하거나 거의 동일한 경우 자동 선택 단추를 사용하여 다른 필드를 자동으로 일치시킬 수 있습니다.

      ![](assets/import_template_example6_2.png)

      >[!NOTE]
      >
      >이러한 프로필로 다이렉트 메일을 보낼 계획이라면 이 정보가 다이렉트 메일 공급자에게 필수이므로 반드시 우편 주소를 포함해야 합니다. 또한 프로필 정보에 있는 **[!UICONTROL Address specified]** 상자가 선택되어 있는지 확인합니다. 워크플로우에서 이 옵션을 업데이트하려면 업데이트할 필드에 요소를 추가하고 **1**&#x200B;을 **[!UICONTROL Source]**&#x200B;로 지정하고 `postalAddress/@addrDefined` 필드를 **[!UICONTROL Destination]**&#x200B;으로 선택하십시오. DM 및 **[!UICONTROL Address specified]** 옵션 사용에 대한 자세한 내용은 [이 문서](../../channels/using/about-direct-mail.md#recommendations)를 참조하십시오.

1. 대사되지 않은 프로파일이 포함된 전환 다음에 있는 **[!UICONTROL Deduplication]** 활동을 구성합니다.

   * **[!UICONTROL Properties]** 탭에서 **[!UICONTROL Resource type]**&#x200B;을 워크플로우의 **[!UICONTROL Reconciliation]** 활동에서 생성된 임시 리소스로 설정합니다.

      ![](assets/import_template_example4.png)

   * 이 예에서는 이메일 필드를 사용하여 고유한 프로필을 찾습니다. 반드시 채워야 하는 필드와 고유한 조합의 일부를 사용할 수 있습니다.
   * **[!UICONTROL Deduplication method]**&#x200B;을 선택합니다. 이 경우, 중복될 경우에 보존되는 레코드를 자동으로 결정합니다.

   ![](assets/import_template_example7.png)

1. 이전에 구성한 **[!UICONTROL Deduplication]** 활동 뒤에 있는 **[!UICONTROL Update data]** 활동을 구성합니다.

   * 인바운드 변환에는 데이터베이스에 없는 프로파일만 포함되므로 **[!UICONTROL Insert only]**&#x200B;을 **[!UICONTROL Operation type]**&#x200B;으로 선택합니다.
   * **[!UICONTROL Identification]** 탭에서 **[!UICONTROL Using reconciliation criteria]**&#x200B;을 선택하고 **[!UICONTROL Dimension to update]** - 이 경우 프로필과 **[!UICONTROL Reconciliation]** 활동에서 만든 링크 사이에 키를 정의합니다. 이 예에서 **CRM ID** 사용자 정의 필드가 사용됩니다.

      ![](assets/import_template_example6.png)

   * **[!UICONTROL Fields to update]** 탭에서 파일의 해당 열 값으로 업데이트할 프로필 차원의 필드를 지정합니다. 파일 열 이름이 받는 사람 차원 필드의 이름과 동일하거나 거의 동일한 경우 자동 선택 단추를 사용하여 다른 필드를 자동으로 일치시킬 수 있습니다.

      ![](assets/import_template_example6_2.png)

      >[!NOTE]
      >
      >이러한 프로필로 다이렉트 메일을 보낼 계획이라면 이 정보가 다이렉트 메일 공급자에게 필수이므로 반드시 우편 주소를 포함해야 합니다. 또한 프로필 정보에 있는 **[!UICONTROL Address specified]** 상자가 선택되어 있는지 확인합니다. 워크플로우에서 이 옵션을 업데이트하려면 업데이트할 필드에 요소를 추가하고 **1**&#x200B;을 **[!UICONTROL Source]**&#x200B;로 지정하고 **[postalAddress/@addrDefined]** 필드를 **[!UICONTROL Destination]**&#x200B;로 선택하십시오. DM 및 **[!UICONTROL Address specified]** 옵션 사용에 대한 자세한 내용은 [이 문서](../../channels/using/about-direct-mail.md#recommendations)를 참조하십시오.

1. 데이터베이스에 삽입되지 않은 데이터를 추적하려면 **[!UICONTROL Segmentation]** 활동의 세 번째 전환 후 **[!UICONTROL Extract file]** 활동 및 **[!UICONTROL Transfer file]** 활동을 추가합니다. 필요한 열을 내보내고 가져올 수 있는 FTP 또는 SFTP 서버에 파일을 전송하도록 해당 활동을 구성합니다.
1. **[!UICONTROL End]** 활동을 추가하고 워크플로우 템플릿을 저장합니다.

이제 템플릿을 사용할 수 있으며 모든 새 워크플로우에 사용할 수 있습니다. 그런 다음 **[!UICONTROL Load file]** 활동에서 가져올 데이터가 포함된 파일을 모두 지정해야 합니다.

![](assets/import_template_example9.png)
