---
title: 패키지 관리
seo-title: 패키지 관리
description: 패키지 관리
seo-description: 관리자는 구조화된 XML 파일을 통해 여러 Adobe Campaign 인스턴스 간에 리소스를 교환하기 위한 패키지를 정의할 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: D 041 F 549-BFC 5-4 E 6 B -87 BF-A 63 C 7 C 224 BCA
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 가져오기 및 내보내기 데이터
discoiquuid: C 3015 CDC -8432-4 E 57-8 AC 0-43 AE 7827 E 3 B 0
context-tags: Packagedef, overview; Packageinstall, main
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 0454dac1a7976c1be2838c2a846d33e77e60c3b3

---


# Managing packages{#managing-packages}

관리자는 구조화된 XML 파일을 통해 여러 Adobe Campaign 인스턴스 간에 리소스를 교환하기 위한 패키지를 정의할 수 있습니다. 구성 매개 변수나 데이터일 수 있습니다.

이 기능은 한 서버에서 다른 서버로 데이터를 전송하거나 인스턴스의 구성을 복제하는 데 유용합니다.

Packages are available under the **[!UICONTROL Administration]** &gt; **[!UICONTROL Deployment]** &gt; **[!UICONTROL Package exports]** or **[!UICONTROL Package imports]** menus. 두 메뉴는 비슷하게 작동합니다.

각 목록의 요소는 수정 또는 설치 날짜에 따라 최근에 가장 최근부터 최근 순으로 표시됩니다.

![](assets/packages_1.png)

요소의 컨텐츠를 표시하고 수정하려면 해당 레이블을 클릭합니다. Refer to the [Exporting a package](../../automating/using/managing-packages.md#exporting-a-package) and [Importing a package](../../automating/using/managing-packages.md#importing-a-package) sections.

## Package exports {#package-exports}

### Standard packages {#standard-packages}

**[!UICONTROL Platform]** 또한 사전 정의된 리소스 목록을 포함하는 두 개의 기본 패키지가 **[!UICONTROL Administration]** 포함되어 있습니다. 읽기 전용 모드로 열 수 있으며 내보내기에는 적합합니다.

![](assets/packages_14.png)

>[!CAUTION]
>
>내보낸 리소스에 기본 ID가 있으면 패키지를 내보낼 수 없습니다. 따라서 내보내기 가능한 리소스의 ID는 Adobe Campaign Standard에서 표준으로 제공된 템플릿과 다른 이름을 사용하여 변경해야 합니다. 예를 들어 테스트 프로필을 내보내려면 값 "sdm" 또는 "sdm" 이 들어 있는 ID를 사용해서는 안 됩니다. 기본 ID가 포함된 패키지를 내보내려는 경우 다음과 같은 오류를 볼 수 있습니다. " 브랜드 (브랜드) 의 엔티티 유형은 패키지를 가져올 때 충돌을 일으킬 수 있는 기본 ID (' BRD 1 ') 를 사용합니다. 이 이름을 변경하고 작업을 반복합니다. "

The package export steps are described in the [Exporting a package](../../automating/using/managing-packages.md#exporting-a-package) section.

* **[!UICONTROL Platform]** 이 패키지는 기술 구성 중에 추가된 모든 리소스를 재그룹화합니다. 사용자 정의 리소스, 사용자 정의 리소스 세트, 트리거 및 **[!UICONTROL System]** 해당 유형의 응용 프로그램 옵션.
* The **[!UICONTROL Administration]** package regroups all the objects added during business configuration such as: campaign templates, content templates, delivery templates, landing page templates, program templates and workflow templates.

   It also includes the following objects: content blocks, target mappings, external accounts, organizational units, application options with the **[!UICONTROL User]** type, roles, typologies, typology rules and users.

>[!NOTE]
>
>이 두 패키지의 내용은 수정할 수 없습니다. 이와 반대로 이러한 패키지에는 항상 최신 데이터가 포함됩니다. You can [create your own packages](../../automating/using/managing-packages.md#creating-a-package) to export specific elements.

### Creating a package {#creating-a-package}

특정 데이터 세트를 내보내야 하는 경우 패키지를 만들어야 합니다.

패키지를 생성하려면 관리 권한이 필요합니다.

1. From **[!UICONTROL Administration]** &gt; **[!UICONTROL Deployment]** &gt; **[!UICONTROL Package exports]**, click the **[!UICONTROL Create]** button in the list of package contents.

   요소가 즉시 생성됩니다. 만들기를 취소하려면 목록으로 돌아가서 해당 상자를 선택하여 삭제합니다.

1. [콘텐트 패키지] 화면에서 이름과 ID를 지정합니다.
1. Click the **[!UICONTROL Edit properties]** button if you would like to add a description and restrict access to certain users.

   ![](assets/packages_18.png)

1. Use the **[!UICONTROL Create element]** button in the **[!UICONTROL Export content]** tab to select the resources you wish to export.

   ![](assets/packages_2.png)

1. 리소스는 알파벳 순으로 표시되며 이름별로 필터링할 수 있습니다. 기술 이름이 대괄호로 표시됩니다. 목록에서 요소를 선택하고 확인합니다.

   ![](assets/packages_3.png)

1. The resource name is displayed in the **[!UICONTROL Export content]** tab. To modify a resource, check the corresponding box and use the **[!UICONTROL Show detail of the element selected]** button.

   ![](assets/packages_4.png)

1. 쿼리 편집기를 사용하면 내보낼 요소를 필터링할 수 있습니다. For more on this, refer to the [Editing queries](../../automating/using/editing-queries.md#creating-queries) section.

   ![](assets/packages_5.png)

   >[!NOTE]
   >
   >리소스당 최대 5000 개의 객체를 내보낼 수 있습니다.

1. 내보낼 모든 리소스를 지정했으면 선택 항목을 저장합니다.

패키지가 생성되고 내보낼 준비가 되었습니다.

### Exporting a package {#exporting-a-package}

패키지를 내보내면 동일한 인스턴스의 다른 인스턴스에서 다시 가져올 수 있도록 하는 리소스의 특정 상태를 저장할 수 있습니다.

>[!CAUTION]
>
>내보낸 리소스에 즉시 사용 가능한 ID가 있으면 패키지를 내보낼 수 없습니다. 따라서 내보내기 가능한 리소스의 ID는 Adobe Campaign Standard에서 표준으로 제공된 템플릿과 다른 이름을 사용하여 변경해야 합니다. 예를 들어 테스트 프로필을 내보내려면 값 "sdm" 또는 "sdm" 이 들어 있는 ID를 사용해서는 안 됩니다.

1. From **[!UICONTROL Administration]** &gt; **[!UICONTROL Deployment]** &gt; **[!UICONTROL Package exports]**, select a package to access its detail.
1. 패키지에 필요한 데이터가 포함되어 있는지 확인합니다.
1. **[!UICONTROL Start export]** 단추를 클릭합니다.

내보낸 파일은 사용 중인 브라우저의 다운로드 폴더에 저장됩니다. 자동으로 "package_xxx.xml" 로 이름이 지정됩니다. 이 경우 "xxx" 가 패키지 ID에 해당합니다.

작업이 완료되면 몇 개의 섹션이 나타납니다.

* **[!UICONTROL Export status]**: 이 섹션은 작업이 올바르게 수행되었는지 여부를 보여줍니다.

   ![](assets/packages_6.png)

* You can consult the different steps of the export via the **[!UICONTROL Log]** tab. 여기에는 모든 이전 내보내기 상태가 포함됩니다.

   ![](assets/packages_7.png)

>[!NOTE]
>
>When selecting an element from the package content list that has already been exported, the **[!UICONTROL Log]** and **[!UICONTROL Last export]** tabs are still available.

## Package imports {#package-imports}

### System updates {#system-updates}

위의 패키지 가져오기 목록은 Adobe에서 수행한 업데이트에 연결된 자동 가져오기가 포함되어 있습니다.

![](assets/packages_15.png)

**[!UICONTROL Execution logs]** 탭에는 모든 가져오기 단계가 저장됩니다. 사이드 패널에 일반 정보가 표시됩니다.

![](assets/packages_11.png)

>[!NOTE]
>
>이러한 요소는 읽기 전용 모드에서 액세스할 수 있습니다.

### Importing a package {#importing-a-package}

관리자는 Adobe Campaign 인스턴스에서 이전에 실행한 내보내기에서 생성된 패키지를 수동으로 가져올 수 있습니다. For more on this, refer to the [Package exports](../../automating/using/managing-packages.md#package-exports) section.

수동 패키지 가져오기는 다음 두 단계로 이루어집니다. 먼저 파일을 업로드해야 해당 컨텐츠를 가져올 수 있습니다.

1. From **[!UICONTROL Administration]** &gt; **[!UICONTROL Deployment]** &gt; **[!UICONTROL Package imports]**, click the **[!UICONTROL Create]** button in the package import list.

   요소가 즉시 생성됩니다. 만들기를 취소하려면 목록으로 돌아가서 해당 상자를 선택하여 삭제합니다.

1. 새 가져오기에 사용할 이름과 ID를 지정합니다.
1. Select the file you wish to upload by dragging and dropping it, or by clicking the **[!UICONTROL Select from folder]** link.

   가져온 파일은 XML 또는 ZIP (XML 파일 포함) 형식이어야 합니다.

   ![](assets/packages_16.png)

   >[!NOTE]
   >
   >업로드된 문서를 교체하려면 파일 이름 오른쪽에 X 아이콘을 통해 파일을 삭제한 다음 작업을 반복합니다.

1. Once the file is uploaded, import its content into the database by using the **[!UICONTROL Start import]** button.

   ![](assets/packages_19.png)

작업이 완료되면 몇 개의 섹션이 나타납니다.

* **[!UICONTROL Import status]**: 이 섹션은 작업이 올바르게 수행되었는지 여부를 보여줍니다.
* You can consult the different steps of the import via the **[!UICONTROL Execution logs]** tab. 오류를 보는 것이 특히 중요합니다.

   ![](assets/packages_20.png)

패키지를 가져온 후에는 동일한 요소에서 다시 가져올 수 없습니다. 레이블과 ID만 수정할 수 있습니다.

동일한 패키지를 다시 가져오려면 패키지 가져오기 목록으로 돌아가서 요소를 생성한 다음 선택한 파일을 다시 업로드해야 합니다.
