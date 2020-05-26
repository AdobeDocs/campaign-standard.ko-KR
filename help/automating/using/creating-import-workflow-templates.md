---
title: 데이터를 가져오기 위한 워크플로우 템플릿 만들기
description: 워크플로우 템플릿을 만들어 데이터를 가져오는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: d909d26a-cf50-46af-ae09-f0fd7258ca27
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: workflow-general-operation
discoiquuid: 75b83165-dcbd-4bb7-b703-ed769f489b16
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 44d6126023e9411477ccd7ffc07ecde806e7976d
workflow-type: tm+mt
source-wordcount: '1172'
ht-degree: 0%

---


# 데이터를 가져오기 위한 워크플로우 템플릿 만들기 {#import-workflow-template}

가져오기 템플릿을 사용하는 것은 구조가 동일한 파일을 정기적으로 가져와야 하는 경우에 가장 좋습니다.

이 예에서는 Adobe Campaign 데이터베이스의 CRM에서 가져온 프로필을 가져오는 데 재사용할 수 있는 워크플로우를 사전 설정하는 방법을 보여줍니다.

1. 에서 새 워크플로우 템플릿을 만듭니다 **[!UICONTROL Resources > Templates > Workflow templates]**.
1. 다음 활동을 추가합니다.

   * **[!UICONTROL Load file]**: 가져올 데이터가 포함된 파일의 예상 구조를 정의합니다.

      >[!NOTE]
      >
      >단일 파일에서 데이터만 가져올 수 있습니다. 워크플로에 여러 **[!UICONTROL Load file]** 활동이 있는 경우 매번 동일한 파일이 사용됩니다.

   * **[!UICONTROL Reconciliation]**: 가져온 데이터를 데이터베이스 데이터와 조정합니다.
   * **[!UICONTROL Segmentation]**: 조정 가능 여부에 따라 필터를 만들어 레코드를 다르게 처리합니다.
   * **[!UICONTROL Deduplication]**: 데이터베이스에 삽입되기 전에 들어오는 파일의 데이터를 중복 제거합니다.
   * **[!UICONTROL Update data]**: 가져온 프로필로 데이터베이스를 업데이트합니다.
   ![](assets/import_template_example0.png)

1. 활동을 **[!UICONTROL Load file]** 구성합니다.

   * 샘플 파일을 업로드하여 예상 구조를 정의합니다. 샘플 파일은 가져올 수 있는 몇 개의 줄만 포함해야 합니다. 파일 형식을 확인하고 편집하여 각 열의 유형이 올바르게 설정되어 있는지 확인합니다. 텍스트, 날짜, 정수 등 예:

      ```
      lastname;firstname;birthdate;email;crmID
      Smith;Hayden;23/05/1989;hayden.smith@mailtest.com;123456
      ```

   * 섹션에서 **[!UICONTROL File to load]** 필드를 **[!UICONTROL Upload a new file from the local machine]** 선택하고 비워 둡니다. 이 템플릿에서 새 워크플로우를 만들 때마다 정의된 구조에 해당하는 파일 중에서 원하는 파일을 여기에 지정할 수 있습니다.

      옵션을 사용할 수 있지만 그에 따라 템플릿을 수정해야 합니다. 예를 들어, 선택하는 경우 **[!UICONTROL Use the file specified in the inbound transition]** FTP/SFTP 서버에서 가져올 파일을 검색하기 전에 **[!UICONTROL Transfer file]** 활동을 추가할 수 있습니다.

      사용자가 가져오는 동안 발생한 오류가 포함된 파일을 다운로드할 수 있게 하려면 옵션을 선택하고 **[!UICONTROL Keep the rejects in a file]** 을 지정합니다 **[!UICONTROL File name]**.

      ![](assets/import_template_example1.png)

1. 활동을 **[!UICONTROL Reconciliation]** 구성합니다. 이 컨텍스트에서 이 활동의 목적은 들어오는 데이터를 식별하는 것입니다.

   * 탭에서 **[!UICONTROL Relations]** 가져온 데이터와 수신자 타깃팅 차원 간 링크 **[!UICONTROL Create element]** 를 선택하고 정의합니다(차원 및 리소스 [타깃팅 참조](../../automating/using/query.md#targeting-dimensions-and-resources)). 이 예에서 **CRM ID** 사용자 정의 필드는 조인 조건을 만드는 데 사용됩니다. 고유한 레코드를 식별할 수 있는 동안 필요한 필드 또는 필드 조합을 사용하십시오.
   * 탭에서 옵션 **[!UICONTROL Identification]** 을 선택 **[!UICONTROL Identify the document from the working data]** 취소하지 않습니다.
   ![](assets/import_template_example2.png)

1. 한 전환에서 조정된 받는 사람과 조정할 수 없지만 두 번째 변환에서 충분한 데이터를 가진 받는 사람을 검색할 **[!UICONTROL Segmentation]** 활동을 구성합니다.

   조정된 받는 사람과의 전환 기능을 사용하여 데이터베이스를 업데이트할 수 있습니다. 그러면 파일에서 최소 정보 세트를 사용할 수 있는 경우 알 수 없는 수신자와 함께 전환하여 데이터베이스에 새 받는 사람 항목을 만들 수 있습니다.

   조정할 수 없고 데이터가 충분하지 않은 수신자는 아웃바운드 보완에서 선택되며 별도의 파일로 내보내거나 무시하면 됩니다.

   * 활동 **[!UICONTROL General]** 탭에서 을 **[!UICONTROL Resource type]** 설정하고 **[!UICONTROL Temporary resource]** 타깃팅된 세트 **[!UICONTROL Reconciliation]** 로 선택합니다.
   * 탭에서 데이터베이스에 레코드를 삽입할 수 없는 **[!UICONTROL Advanced options]** **[!UICONTROL Generate complement]** 옵션을 확인합니다. 필요한 경우 보완 데이터에 추가 처리를 적용할 수 있습니다. 파일 내보내기, 목록 업데이트 등
   * 탭의 첫 번째 세그먼트에서 **[!UICONTROL Segments]** 프로필의 CRM ID가 0이 아닌 레코드만 선택하려면 인바운드 모집단에 필터링 조건을 추가합니다. 이렇게 하면 데이터베이스의 프로필과 조정된 파일의 데이터가 해당 하위 세트에서 선택됩니다.

      ![](assets/import_template_example3.png)

   * 데이터베이스에 삽입할 데이터를 충분히 가진 대사되지 않은 레코드를 선택하는 두 번째 세그먼트를 추가합니다. 예: 이메일 주소, 이름 및 성 조정되지 않은 레코드에는 프로필의 CRM ID 값이 0입니다.

      ![](assets/import_template_example3_2.png)

   * 처음 두 하위 세트에서 선택되지 않은 모든 레코드가 이 세트에 선택되어 **[!UICONTROL Complement]**&#x200B;있습니다.

1. 이전에 구성된 **[!UICONTROL Update data]** 활동의 첫 번째 아웃바운드 전환 뒤에 있는 **[!UICONTROL Segmentation]** 활동을 구성합니다.

   * 인바운드 전환 **[!UICONTROL Update]** 에 이미 데이터베이스에 있는 수신자만 포함되므로 **[!UICONTROL Operation type]** 을 선택합니다.
   * 탭에서 이 경우 **[!UICONTROL Identification]** - 프로필 **[!UICONTROL Using reconciliation criteria]** 과 활동에 생성된 링크 사이에 키를 선택하고 **[!UICONTROL Dimension to update]** **[!UICONTROL Reconciliation]** 정의합니다. 이 예에서는 **CRM ID** 사용자 정의 필드가 사용됩니다.

      ![](assets/import_template_example6.png)

   * 탭에서 파일의 해당 열 값으로 업데이트할 프로필 차원의 필드를 **[!UICONTROL Fields to update]** 지정합니다. 파일 열 이름이 받는 사람 차원 필드 이름과 동일하거나 거의 동일한 경우 자동 선택 단추를 사용하여 다른 필드를 자동으로 일치시킬 수 있습니다.

      ![](assets/import_template_example6_2.png)

      >[!NOTE]
      >
      >이러한 프로필로 직접 메일을 보낼 계획이라면 이 정보가 DM 업체에 필수이므로 우편 주소를 포함해야 합니다. 또한 프로필 정보에 있는 **[!UICONTROL Address specified]** 상자가 선택되어 있는지 확인합니다. 워크플로우에서 이 옵션을 업데이트하려면 업데이트할 필드에 요소를 추가한 다음 **으로** **[!UICONTROL Source]** 1 `postalAddress/@addrDefined` 을 지정하고 **[!UICONTROL Destination]**&#x200B;필드를로 선택하십시오. DM 및 옵션 사용에 대한 자세한 내용은 **[!UICONTROL Address specified]** 이 문서를 참조하십시오 [](../../channels/using/about-direct-mail.md#recommendations).

1. 조정되지 않은 프로필이 포함된 전환 뒤에 있는 **[!UICONTROL Deduplication]** 활동을 구성합니다.

   * 탭에서 워크플로우 **[!UICONTROL Properties]** 활동에서 생성된 임시 리소스 **[!UICONTROL Resource type]** 로 **[!UICONTROL Reconciliation]** 설정합니다.

      ![](assets/import_template_example4.png)

   * 이 예에서는 이메일 필드를 사용하여 고유한 프로필을 찾습니다. 반드시 채워야 하는 필드와 고유한 조합의 일부를 사용할 수 있습니다.
   * 원하는 **[!UICONTROL Deduplication method]**&#x200B;항목 선택 이 경우, 중복될 경우에 어느 레코드가 보관되는지가 자동으로 결정됩니다.
   ![](assets/import_template_example7.png)

1. 이전에 구성된 **[!UICONTROL Update data]** 활동 뒤에 **[!UICONTROL Deduplication]** 있는 활동을 구성합니다.

   * 인바운드 전환 **[!UICONTROL Insert only]** 에 데이터베이스에 없는 프로파일만 포함되므로 **[!UICONTROL Operation type]** 을 선택합니다.
   * 탭에서 이 경우 **[!UICONTROL Identification]** - 프로필 **[!UICONTROL Using reconciliation criteria]** 과 활동에 생성된 링크 사이에 키를 선택하고 **[!UICONTROL Dimension to update]** **[!UICONTROL Reconciliation]** 정의합니다. 이 예에서는 **CRM ID** 사용자 정의 필드가 사용됩니다.

      ![](assets/import_template_example6.png)

   * 탭에서 파일의 해당 열 값으로 업데이트할 프로필 차원의 필드를 **[!UICONTROL Fields to update]** 지정합니다. 파일 열 이름이 받는 사람 차원 필드 이름과 동일하거나 거의 동일한 경우 자동 선택 단추를 사용하여 다른 필드를 자동으로 일치시킬 수 있습니다.

      ![](assets/import_template_example6_2.png)

      >[!NOTE]
      >
      >이러한 프로필로 직접 메일을 보낼 계획이라면 이 정보가 DM 업체에 필수이므로 우편 주소를 포함해야 합니다. 또한 프로필 정보에 있는 **[!UICONTROL Address specified]** 상자가 선택되어 있는지 확인합니다. 워크플로우에서 이 옵션을 업데이트하려면 업데이트할 필드에 요소를 추가한 다음 **1** 개 **[!UICONTROL Source]** 를 지정하고 **[postalAddress/@addrDefined]** 필드를 로 **[!UICONTROL Destination]**&#x200B;선택하십시오. DM 및 옵션 사용에 대한 자세한 내용은 **[!UICONTROL Address specified]** 이 문서를 참조하십시오 [](../../channels/using/about-direct-mail.md#recommendations).

1. 활동에 대한 세 번째 전환 후 데이터베이스에 삽입되지 않은 데이터를 추적하려는 경우 **[!UICONTROL Segmentation]** 활동 및 **[!UICONTROL Extract file]** **[!UICONTROL Transfer file]** 활동을 추가합니다. 필요한 열을 내보내고 파일을 검색할 수 있는 FTP 또는 SFTP 서버에서 파일을 전송할 활동을 구성합니다.
1. 활동을 **[!UICONTROL End]** 추가하고 워크플로우 템플릿을 저장합니다.

이제 템플릿을 사용할 수 있으며 모든 새로운 워크플로우에서 사용할 수 있습니다. 그런 다음 활동에 가져올 데이터가 포함된 파일을 모두 **[!UICONTROL Load file]** 지정해야 합니다.

![](assets/import_template_example9.png)
