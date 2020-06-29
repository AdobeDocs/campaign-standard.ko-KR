---
title: 파일 추출
description: Extract 파일 작업을 사용하면 Adobe Campaign의 데이터를 외부 파일 형식으로 내보낼 수 있습니다.
page-status-flag: never-activated
uuid: 631f0fbd-9e8d-4f77-a338-fcb7f4fc1774
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: data-management-activities
discoiquuid: a06509f9-4731-4187-b43d-3bfa361284d3
context-tags: fileExport,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 15e5aebdd67e8f5ddee89506c0469a101d94d2e8
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 1%

---


# 파일 추출{#extract-file}

## 설명 {#description}

![](assets/export.png)

이 **[!UICONTROL Extract file]** 활동을 통해 Adobe Campaign의 데이터를 외부 파일 형식으로 내보낼 수 있습니다.

## 사용 상황 {#context-of-use}

데이터 압축을 해제할 방법은 활동을 구성할 때 정의됩니다.

>[!CAUTION]
>
>활동을 **[!UICONTROL Extract file]** 사용하려면 활동 **[!UICONTROL Query]** 뒤에 활동이 배치되어야 합니다.

**관련 항목:**

* [사용 사례: 외부 파일에서 프로필 내보내기](../../automating/using/exporting-profiles-in-file.md)

## 구성 {#configuration}

1. 활동을 워크플로우로 드래그하여 **[!UICONTROL Extract file]** 놓습니다.

   ![](assets/wkf_data_export1.png)

1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 활동을 엽니다.
1. 출력 파일의 레이블을 **입력합니다**. 파일의 레이블은 생성된 날짜 및 시간과 함께 자동으로 완료되어 고유합니다. 예: 2015년 8월 15일 08:15:32에 생성된 파일에 대한 recipients_20150815_081532.txt

   >[!NOTE]
   >
   >이 필드의 **[!UICONTROL formatDate]** 함수를 사용하여 파일 이름을 지정할 수 있습니다.

1. 원하는 경우 필드에서 선택하여 출력 파일 **[!UICONTROL Compression]** 을 압축할 수 **[!UICONTROL Add a pre-processing step]** 있습니다. 출력 파일은 GZIP 파일(.gz)로 압축됩니다.

   또한 이 **[!UICONTROL Add a pre-processing step]** 필드를 사용하면 파일을 추출하기 전에 파일을 암호화할 수 있습니다. 암호화된 파일을 사용하는 방법에 대한 자세한 내용은 [이 섹션을 참조하십시오.](../../automating/using/managing-encrypted-data.md)

1. 출력 열을 추가하려면 ![](assets/add_darkgrey-24px.png) 또는 **[!UICONTROL Add an element]** 단추를 클릭합니다.

   ![](assets/wkf_data_export2.png)

   새 창이 열립니다.

   ![](assets/wkf_data_export3.png)

1. 표현식을 입력합니다. 이를 위해 기존 표현식을 선택하거나 **표현식 편집기를 사용하여 새 표현식을 만들 수 있습니다**.
1. 표현식을 확인합니다.

   표현식이 출력 열에 추가됩니다.

1. 필요한 만큼 열을 만듭니다. 표현식과 레이블을 클릭하여 열을 편집할 수 있습니다.

   프로파일을 내보낼 때 외부 도구에서 사용하려면 고유한 식별자를 내보내야 합니다. 기본적으로 모든 프로필에는 데이터베이스에 추가하는 방식에 따라 고유한 식별자가 있는 것은 아닙니다. 자세한 내용은 프로필에 [대한 고유 ID 생성 섹션을](../../developing/using/configuring-the-resource-s-data-structure.md#generating-a-unique-id-for-profiles-and-custom-resources) 참조하십시오.

1. 내보낼 파일의 출력, 날짜 및 번호 형식을 구성하려면 **[!UICONTROL File structure]** 탭을 클릭합니다.

   열거형 값을 내보낼 **[!UICONTROL Export labels instead of internal values of enumerations]** 경우 옵션을 선택합니다. 이 옵션을 사용하면 ID 대신 이해하기 쉬운 짧은 레이블을 검색할 수 있습니다.

1. 인바운드 전환이 비어 있는 경우 **[!UICONTROL Properties]** 탭에서 SFTP 서버에 빈 파일을 만들고 업로드하지 **[!UICONTROL Do not generate a file if the inbound transition is empty]** 않도록 옵션을 선택합니다.
1. 활동 구성을 확인하고 워크플로우를 저장합니다.
