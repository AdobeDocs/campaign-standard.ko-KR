---
title: 사용자 정의 리소스 내보내기/가져오기
description: 이 자습서에서는 사용자 정의 리소스 패키지를 내보내고 가져오는 방법에 대해 설명합니다.
page-status-flag: never-activated
uuid: 631f0fbd-9e8d-4f77-a338-fcb7f4fc1774
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: data-management-activities
discoiquuid: a06509f9-4731-4187-b43d-3bfa361284d3
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: b10a4b3a81d676e279a9514530158286d58db813

---


# 사용자 정의 리소스 내보내기/가져오기 {#exporting-importing-custom-resources}

이 자습서에서는 개발 환경에서 프로덕션 환경으로 사용자 정의 리소스 패키지를 내보내고 가져오는 방법에 대해 설명합니다.

이 예는 Adobe Campaign에 연결된 기능 관리자를 대상으로 합니다.

사전 요구 사항은 다음과 같습니다.

* **사용 및 게시되는 하나 또는 여러 개의 사용자 지정 리소스** .

   또한 자동 기본 키는 패키지에서 내보내지지 않으므로 이러한 리소스에 대한 고유한 키를 정의해야 합니다. 따라서 리소스의 기본 키와 추가적인 고유 키를 사용하여 레코드의 고유성을 보장할 수 있습니다.
* **패키지를 만들고 내보내는 데 필요한 권한** .

추가 리소스:

* [패키지 관리](../../automating/using/managing-packages.md)
* [패키지 배포:운영 원칙](../../developing/using/data-model-concepts.md)
* [리소스 추가 또는 확장](../../developing/using/key-steps-to-add-a-resource.md)

## 구조 내보내기 {#exporting-the-structure}

이 섹션에서는 사용자 지정 리소스 데이터의 물리적 구조를 자세히 설명하는 첫 번째 패키지 내보내기를 수행합니다.

이 예에는 두 개의 사용자 지정 리소스가 있습니다.제품 **및** 주문 ****.

1. / **[!UICONTROL Administration]** / **[!UICONTROL Deployment]** / **[!UICONTROL Package exports]** 메뉴로 이동합니다.

   두 개의 사용자 지정 리소스 "제품"과 "주문"으로 필터링된 패키지를 내보낼 새 패키지를 **[!UICONTROL Custom resource (cusResource)]** 만듭니다.

1. 페이지에서 아이콘을 클릭하여 새 패키지를 **[!UICONTROL Package exports]** **[!UICONTROL Create]** 만듭니다.
1. 레이블을 완료한 다음 을 **[!UICONTROL Create element]**&#x200B;클릭합니다.

   ![](assets/cusresources_export1.png)

1. 를 검색하고 선택합니다 **[!UICONTROL Custom resource (cusResource)]**.

   ![](assets/cusresources_export2.png)

1. 필터링 조건에서 두 리소스, 제품 및 **[!UICONTROL Custom resource]** 주문을 **선택하여** 세부 **사항을**&#x200B;구성합니다.

   논리 연산자를 변경하는 것을 잊지 않도록 하십시오. 제품 리소스 및 주문 **리소스의** 구조가 패키지에 통합되도록 값을 OR로 설정해야 합니다.

   ![](assets/cusresources_export3.png)

1. 패키지 정의를 확인하고 저장합니다.

이제 을(를) 클릭할 수 **[!UICONTROL Start export]**&#x200B;있습니다.

![](assets/cusresources_export4.png)

생성된 패키지는 다운로드 폴더에서 사용할 수 있습니다. zip 파일의 이름은 임의로 생성됩니다. 이름을 변경할 수 있습니다.

## 데이터 내보내기 {#exporting-the-data}

두 번째 내보내기를 통해 제품 및 주문 **사용자** 지정 **리소스에서 데이터를 내보낼 수** 있습니다.

구조 내보내기와 동일한 유형의 내보내기를 기반으로 데이터가 포함된 두 번째 패키지를 만듭니다.

1. 페이지에서 아이콘을 클릭하여 새 패키지를 **[!UICONTROL Package exports]** **[!UICONTROL Create]** 만듭니다.
1. 레이블을 작성한 **[!UICONTROL Export data of my resources]** 다음 **[!UICONTROL Create element]****[!UICONTROL Export content]** 탭에서 을 클릭합니다.
1. 제품 리소스를 검색하고 **선택합니다** .

   ![](assets/cusresources_exportdata1.png)

1. @Label IS NULL을 사용하여 고급 **필터링 조건을** **구성합니다**.

   ![](assets/cusresources_exportdata2.png)

1. 카운트를 확인하십시오.

   ![](assets/cusresources_exportdata3.png)

1. 주문 사용자 지정 리소스에 대해 동일한 **작업을** 반복합니다.

   ![](assets/cusresources_exportdata4.png)

1. 패키지 정의를 확인하고 저장합니다.

이제 을(를) 클릭할 수 **[!UICONTROL Start export]**&#x200B;있습니다.

![](assets/cusresources_exportdata5.png)

생성된 패키지는 다운로드 폴더에서 사용할 수 있습니다. zip 파일의 이름은 임의로 생성됩니다. 이름을 변경할 수 있습니다.

## 구조 가져오기 {#importing-the-structure}

### 패키지 가져오기 {#importing-the-structure-package}

1. 새로 만든 패키지를 가져올 **대상 인스턴스에** 연결합니다.
1. 첫 번째 내보내기에서 파일을 가져올 새 패키지를 만들려면 **[!UICONTROL Administration]** / **[!UICONTROL Deployment]** / **[!UICONTROL Package imports]** 메뉴로 이동하십시오.
1. 이 용도로 제공된 영역에 **구조 파일을** 드래그하여 놓습니다. 허용되는 형식은 ZIP 또는 XML입니다.

   ![](assets/cusresources_import2.png)

1. 레이블 수정(예: 구조 **가져오기**)을 클릭한 다음 **[!UICONTROL Save]**&#x200B;을 클릭합니다.
1. Click **[!UICONTROL Start import]**.

   ![](assets/cusresources_import3.png)

### 게시 {#publish-structure}

1. / **[!UICONTROL Administration]** / **[!UICONTROL Development]** / **[!UICONTROL Publication]** 메뉴로 이동합니다.
1. 을 **[!UICONTROL Prepare publication]** 클릭한 **[!UICONTROL Publish]** 다음 새 사용자 지정 리소스의 데이터로 인스턴스를 업데이트합니다.
1. 설치된 패키지에 해당하는 메뉴 항목이 **[!UICONTROL Client data]** 메뉴에 삽입됩니다.

   ![](assets/cusresources_import1.png)

## 데이터 가져오기 {#importing-the-data}

이 섹션에서는 이전 단계의 인스턴스에 설치된 패키지에 연결된 데이터를 **** 가져옵니다.

이전 단계와 동일한 방식으로 두 부분으로 분할됩니다.패키지 가져오기 및 게시

### 패키지 가져오기 {#importing-the-data-package}

1. / **[!UICONTROL Administration]** / **[!UICONTROL Deployment]** / **[!UICONTROL Package imports]** 메뉴로 이동하여 데이터가 포함된 파일을 가져올 새 패키지를 만듭니다.
1. 이 용도로 제공된 영역에 데이터 파일을 드래그하여 놓습니다. 허용되는 형식은 ZIP 또는 XML입니다.
1. "데이터 가져오기"와 같이 레이블을 수정한 다음 을 클릭합니다 **[!UICONTROL Save]**.
1. Click **[!UICONTROL Start import]**.

   ![](assets/cusresources_importdata.png)

### 게시 {#publish-data}

1. / **[!UICONTROL Administration]** / **[!UICONTROL Development]** / **[!UICONTROL Publication]** 메뉴로 이동합니다.
1. 사용자 지정 리소스의 데이터로 인스턴스를 업데이트하려면 **[!UICONTROL Prepare publication]** 그런 다음 을 **[!UICONTROL Publish]** 클릭합니다.
