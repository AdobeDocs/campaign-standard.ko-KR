---
title: 데이터를 가져오기 위한 워크플로우 템플릿 만들기
description: 워크플로우 템플릿을 만들어 데이터를 가져오는 방법을 알아봅니다.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
feature: Workflows
role: Data Architect
level: Experienced
exl-id: 5974a52c-8721-4575-b452-2982d6497235
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '1176'
ht-degree: 1%

---

# 데이터를 가져오기 위한 워크플로우 템플릿 만들기 {#import-workflow-template}

구조가 같은 파일을 정기적으로 가져오려면 가져오기 템플릿을 사용하는 것이 좋습니다.

이 예에서는 Adobe Campaign 데이터베이스의 CRM에서 가져온 프로필을 가져오는 데 다시 사용할 수 있는 워크플로우를 사전 설정하는 방법을 보여 줍니다.

1. 에서 새 워크플로우 템플릿 만들기 **[!UICONTROL Resources > Templates > Workflow templates]**.
1. 다음 활동을 추가합니다.

   * **[!UICONTROL Load file]**: 가져올 데이터가 포함된 파일의 예상 구조를 정의합니다.

     >[!NOTE]
     >
     >단일 파일에서만 데이터를 가져올 수 있습니다. 워크플로우에 여러 개가 있는 경우 **[!UICONTROL Load file]** 활동. 매번 동일한 파일이 사용됩니다.

   * **[!UICONTROL Reconciliation]**: 가져온 데이터를 데이터베이스 데이터와 조정합니다.
   * **[!UICONTROL Segmentation]**: 조정할 수 있는지 여부에 따라 레코드를 다르게 처리하는 필터를 만듭니다.
   * **[!UICONTROL Deduplication]**: 데이터베이스에 삽입하기 전에 들어오는 파일에서 데이터를 중복 제거합니다.
   * **[!UICONTROL Update data]**: 가져온 프로필로 데이터베이스를 업데이트합니다.

   ![](assets/import_template_example0.png)

1. 구성 **[!UICONTROL Load file]** 활동:

   * 샘플 파일을 업로드하여 예상 구조를 정의합니다. 샘플 파일에는 가져오기에 필요한 열을 제외한 몇 줄만 포함되어야 합니다. 파일 형식을 확인 및 편집하여 각 열의 유형(텍스트, 날짜, 정수 등)이 올바르게 설정되었는지 확인합니다. 예제:

     ```
     lastname;firstname;birthdate;email;crmID
     Smith;Hayden;23/05/1989;hayden.smith@mailtest.com;123456
     ```

   * 다음에서 **[!UICONTROL File to load]** 섹션, 선택 **[!UICONTROL Upload a new file from the local machine]** 필드를 비워 둡니다. 이 템플릿에서 새 워크플로우를 만들 때마다 정의된 구조에 해당하는 한 원하는 파일을 여기에서 지정할 수 있습니다.

     옵션을 사용할 수 있지만 그에 따라 템플릿을 수정해야 합니다. 예를 들어, **[!UICONTROL Use the file specified in the inbound transition]**, 다음을 추가할 수 있습니다. **[!UICONTROL Transfer file]** ftp/SFTP 서버에서 가져올 파일을 검색하기 전 작업입니다.

     사용자가 가져오는 동안 발생한 오류가 포함된 파일을 다운로드할 수 있도록 하려면 **[!UICONTROL Keep the rejects in a file]** 옵션 및 지정 **[!UICONTROL File name]**.

     ![](assets/import_template_example1.png)

1. 구성 **[!UICONTROL Reconciliation]** 활동. 이 컨텍스트에서 이 활동의 목적은 들어오는 데이터를 식별하는 것입니다.

   * 다음에서 **[!UICONTROL Relations]** 탭, 선택 **[!UICONTROL Create element]** 가져온 데이터와 수신자 타겟팅 차원 간의 링크를 정의합니다( 참조). [타겟팅 차원 및 리소스](../../automating/using/query.md#targeting-dimensions-and-resources)). 이 예에서는 **CRM ID** 사용자 지정 필드는 조인 조건을 만드는 데 사용됩니다. 고유한 레코드를 식별할 수 있는 한 필요한 필드 또는 필드 조합을 사용하십시오.
   * 다음에서 **[!UICONTROL Identification]** 탭에서 **[!UICONTROL Identify the document from the working data]** 옵션을 선택 취소했습니다.

   ![](assets/import_template_example2.png)

1. 구성 **[!UICONTROL Segmentation]** 활동은 한 전환에서 조정된 수신자와 조정할 수 없지만 두 번째 전환에서 충분한 데이터를 가진 수신자를 검색합니다.

   조정된 수신자와의 전환을 사용하여 데이터베이스를 업데이트할 수 있습니다. 파일에서 최소 정보 집합을 사용할 수 있는 경우 알 수 없는 수신자가 있는 전환을 사용하여 데이터베이스에서 새 수신자 항목을 만들 수 있습니다.

   조정할 수 없고 데이터가 충분하지 않은 수신자는 보충 아웃바운드 전환에서 선택되고 별도의 파일로 내보내거나 간단히 무시할 수 있습니다.

   * 다음에서 **[!UICONTROL General]** 활동의 탭에서 다음을 설정합니다. **[!UICONTROL Resource type]** 끝 **[!UICONTROL Temporary resource]** 및 선택 **[!UICONTROL Reconciliation]** 을(를) 타깃팅된 세트로 합니다.
   * 다음에서 **[!UICONTROL Advanced options]** 탭에서 다음을 확인합니다 **[!UICONTROL Generate complement]** 데이터베이스에 삽입할 수 없는 레코드가 있는지 확인할 수 있는 옵션입니다. 그런 다음 필요한 경우 파일 내보내기, 목록 업데이트 등의 추가 처리를 보조 데이터에 적용할 수 있습니다.
   * 의 첫 번째 세그먼트에서 **[!UICONTROL Segments]** 탭에서 인바운드 모집단에 필터링 조건을 추가하여 프로필의 CRM ID가 0과 같지 않은 레코드만 선택합니다. 이렇게 하면 데이터베이스의 프로필과 조정된 파일의 데이터가 해당 하위 집합에서 선택됩니다.

     ![](assets/import_template_example3.png)

   * 데이터베이스에 삽입할 데이터가 충분한 조정되지 않은 레코드를 선택하는 두 번째 세그먼트를 추가합니다. 이메일 주소, 이름 및 성 등을 예로 들 수 있습니다. 조정되지 않은 레코드의 프로필 CRM ID 값은 0입니다.

     ![](assets/import_template_example3_2.png)

   * 처음 두 하위 집합에서 선택되지 않은 모든 레코드는 **[!UICONTROL Complement]**.

1. 구성 **[!UICONTROL Update data]** 활동은 의 첫 번째 아웃바운드 전환 이후에 위치합니다. **[!UICONTROL Segmentation]** 활동이 이전에 구성되었습니다.

   * 선택 **[!UICONTROL Update]** 다음으로: **[!UICONTROL Operation type]** 인바운드 전환에는 데이터베이스에 이미 있는 수신자만 포함되므로
   * 다음에서 **[!UICONTROL Identification]** 탭, 선택 **[!UICONTROL Using reconciliation criteria]** 및 다음 사이에 키 정의 **[!UICONTROL Dimension to update]** - 이 경우의 프로필 - 및 및에서 만든 링크 **[!UICONTROL Reconciliation]** 활동. 이 예에서는 **CRM ID** 사용자 정의 필드가 사용됩니다.

     ![](assets/import_template_example6.png)

   * 다음에서 **[!UICONTROL Fields to update]** 탭에서 파일의 해당 열 값으로 업데이트할 프로필 차원의 필드를 나타냅니다. 파일 열의 이름이 수신자 차원 필드의 이름과 동일하거나 거의 동일한 경우 자동 선택 버튼을 사용하여 다른 필드를 자동으로 일치시킬 수 있습니다.

     ![](assets/import_template_example6_2.png)

     >[!NOTE]
     >
     >이러한 프로필로 DM을 보낼 계획이라면 우편 주소를 반드시 포함하십시오. DM 공급자에게는 이 정보가 필수이기 때문입니다. 또한 **[!UICONTROL Address specified]** 프로필 정보에 있는 확인란이 선택되어 있습니다. 워크플로우에서 이 옵션을 업데이트하려면 업데이트할 필드에 요소를 추가하고 을(를) 지정합니다 **1** 다음으로: **[!UICONTROL Source]** 및 선택 `postalAddress/@addrDefined` 다음으로 필드 **[!UICONTROL Destination]**. DM 및 사용에 대한 자세한 내용 **[!UICONTROL Address specified]** 옵션, 참조 [이 문서](../../channels/using/about-direct-mail.md#recommendations).

1. 구성 **[!UICONTROL Deduplication]** 조정되지 않은 프로필이 포함된 전환 뒤에 있는 활동:

   * 다음에서 **[!UICONTROL Properties]** 탭에서 다음을 설정합니다. **[!UICONTROL Resource type]** 에서 생성된 임시 리소스로 **[!UICONTROL Reconciliation]** 워크플로우의 활동.

     ![](assets/import_template_example4.png)

   * 이 예제에서는 이메일 필드를 사용하여 고유한 프로필을 찾습니다. 가 채워져 있고 고유한 조합의 일부인 모든 필드를 사용할 수 있습니다.
   * 선택 **[!UICONTROL Deduplication method]**. 이 경우 애플리케이션은 중복 시 보존되는 레코드를 자동으로 결정합니다.

   ![](assets/import_template_example7.png)

1. 구성 **[!UICONTROL Update data]** 활동 위치: **[!UICONTROL Deduplication]** 활동이 이전에 구성되었습니다.

   * 선택 **[!UICONTROL Insert only]** 다음으로: **[!UICONTROL Operation type]** 인바운드 전환에 데이터베이스에 없는 프로필만 포함되기 때문입니다.
   * 다음에서 **[!UICONTROL Identification]** 탭, 선택 **[!UICONTROL Using reconciliation criteria]** 및 다음 사이에 키 정의 **[!UICONTROL Dimension to update]** - 이 경우의 프로필 - 및 및에서 만든 링크 **[!UICONTROL Reconciliation]** 활동. 이 예에서는 **CRM ID** 사용자 정의 필드가 사용됩니다.

     ![](assets/import_template_example6.png)

   * 다음에서 **[!UICONTROL Fields to update]** 탭에서 파일의 해당 열 값으로 업데이트할 프로필 차원의 필드를 나타냅니다. 파일 열의 이름이 수신자 차원 필드의 이름과 동일하거나 거의 동일한 경우 자동 선택 버튼을 사용하여 다른 필드를 자동으로 일치시킬 수 있습니다.

     ![](assets/import_template_example6_2.png)

     >[!NOTE]
     >
     >이러한 프로필로 DM을 보낼 계획이라면 우편 주소를 반드시 포함하십시오. DM 공급자에게는 이 정보가 필수이기 때문입니다. 또한 **[!UICONTROL Address specified]** 프로필 정보에 있는 확인란이 선택되어 있습니다. 워크플로우에서 이 옵션을 업데이트하려면 업데이트할 필드에 요소를 추가하고 을(를) 지정합니다 **1** 다음으로: **[!UICONTROL Source]** 및 선택 **[postalAddress/@addrDefined]** 다음으로 필드 **[!UICONTROL Destination]**. DM 및 사용에 대한 자세한 내용 **[!UICONTROL Address specified]** 옵션, 참조 [이 문서](../../channels/using/about-direct-mail.md#recommendations).

1. 의 세 번째 전환 이후 **[!UICONTROL Segmentation]** 활동, 추가 **[!UICONTROL Extract file]** 활동 및 a **[!UICONTROL Transfer file]** 활동은 데이터베이스에 삽입되지 않은 데이터를 추적하려는 경우에 사용합니다. 필요한 열을 내보내고 파일을 검색할 수 있는 FTP 또는 SFTP 서버에 전송하도록 이러한 활동을 구성합니다.
1. 추가 **[!UICONTROL End]** 활동을 수행하고 워크플로 템플릿을 저장합니다.

이제 템플릿을 사용할 수 있으며, 모든 새 워크플로우에서 사용할 수 있습니다. 그런 다음 가져올 데이터가 포함된 파일을 지정하는 데 필요합니다. **[!UICONTROL Load file]** 활동.

![](assets/import_template_example9.png)
