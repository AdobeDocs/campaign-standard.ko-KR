---
title: 파일 추출
description: Extract 파일 작업을 사용하면 Adobe Campaign에서 외부 파일 형식으로 데이터를 내보낼 수 있습니다.
page-status-flag: 활성화 안 함
uuid: 631f0fbd-9e8d-4f77-a338-fcb7f4fc1774
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 자동화
content-type: reference
topic-tags: 데이터 관리 활동
discoiquuid: a06509f9-4731-4187-b43d-3bfa361284d3
context-tags: fileExport,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 파일 추출{#extract-file}

## 설명 {#description}

![](assets/export.png)

이 **[!UICONTROL Extract file]** 활동을 통해 외부 파일 형식으로 Adobe Campaign의 데이터를 내보낼 수 있습니다.

## 사용 상황 {#context-of-use}

데이터를 추출하는 방법은 활동을 구성할 때 정의됩니다.

>[!CAUTION]
>
>활동을 사용하려면 **[!UICONTROL Extract file]** 활동 다음에 **[!UICONTROL Query]** 활동을 배치해야 합니다.

## 구성 {#configuration}

1. 워크플로우를 워크플로우로 드래그하여 **[!UICONTROL Extract file]** 놓을 수 있습니다.

   ![](assets/wkf_data_export1.png)

1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 엽니다.
1. 출력 파일의 레이블을 **입력합니다**. 파일의 레이블은 생성된 날짜 및 시간과 함께 자동으로 완료되므로 파일의 내용이 고유합니다. 예:2015년 8월 15일 08:15:32에 생성된 파일에 대한 recipients_2015_081532.txt

   >[!NOTE]
   >
   >이 필드의 **[!UICONTROL formatDate]** 함수를 사용하여 파일 이름을 지정할 수 있습니다.

1. 원하는 경우 **[!UICONTROL Compression]** **[!UICONTROL Add a pre-processing step]** 필드에서 선택하여 출력 파일을 압축 해제할 수 있습니다. 출력 파일은 GZIP 파일(.gz)로 압축됩니다.
1. 출력 열을 추가하려면 ![](assets/add_darkgrey-24px.png) 또는 **[!UICONTROL Add an element]** 단추를 클릭합니다.

   ![](assets/wkf_data_export2.png)

   새 창이 열립니다.

   ![](assets/wkf_data_export3.png)

1. 표현식을 입력합니다. 이렇게 하려면 기존 표현식을 선택하거나 **표현식 편집기를**&#x200B;사용하여 새 표현식을 만들 수 있습니다.
1. 표현식을 확인합니다.

   표현식이 출력 열에 추가됩니다.

1. 필요한 만큼 열을 만듭니다. 표현식과 레이블을 클릭하여 열을 편집할 수 있습니다.

   프로파일을 내보낼 때 외부 도구에서 사용하려면 고유한 식별자를 내보내야 합니다. 기본적으로 모든 프로필에는 데이터베이스에 추가하는 방식에 따라 고유한 식별자가 있는 것은 아닙니다. 자세한 내용은 프로필에 [대한](../../developing/using/configuring-the-resource-s-data-structure.md#generating-a-unique-id-for-profiles-and-custom-resources) 고유 ID 생성 섹션을 참조하십시오.

1. 내보낼 파일의 출력, 날짜 및 번호 형식을 구성하려면 **[!UICONTROL File structure]** 탭을 클릭합니다.

   열거형 값을 내보낼 경우 이 **[!UICONTROL Export labels instead of internal values of enumerations]** 옵션을 선택합니다. 이 옵션을 사용하면 ID 대신 이해하기 쉬운 짧은 레이블을 검색할 수 있습니다.

1. 인바운드 전환이 비어 있는 경우 **[!UICONTROL Properties]** 탭에서 SFTP 서버에 빈 파일을 만들고 업로드하지 않도록 **[!UICONTROL Do not generate a file if the inbound transition is empty]** 옵션을 선택합니다.
1. 활동 구성을 확인하고 워크플로우를 저장합니다.

## 예 {#example}

다음 예에서는 활동 후 **[!UICONTROL Extract file]** **[!UICONTROL Query]** 활동을 구성하는 방법을 보여줍니다.

이 워크플로우의 목적은 Adobe Campaign 외부에서 데이터를 사용할 수 있도록 외부 파일 형식으로 프로필 목록을 내보내는 것입니다.

1. 활동을 워크플로우로 드래그하여 놓고 **[!UICONTROL Extract file]** **[!UICONTROL Query]** 활동 뒤에 배치합니다.

   이 예에서는 18세에서 30세 사이의 모든 프로파일에서 쿼리가 수행됩니다.

1. Extract 파일 작업을 열어 편집합니다.
1. 출력 파일의 이름을 지정합니다.
1. 출력 열을 추가합니다.

   이 예에서는 프로필의 이메일, 연령, 생년월일, 이름 및 성이 출력 열로 추가됩니다.

   ![](assets/wkf_data_export6.png)

1. 탭을 클릭하여 다음을 정의합니다. **[!UICONTROL File structure]**

   * CSV 출력 형식

      ![](assets/wkf_data_export7.png)

   * 날짜 형식

      ![](assets/wkf_data_export9.png)

1. 활동 확인
1. 활동 후에 **[!UICONTROL Transfer file]** **[!UICONTROL Extract file]** 활동을 드래그하여 놓아 외부 계정에서 추출 파일을 복구합니다.
1. 활동을 열고 **[!UICONTROL File upload]** 작업을 선택합니다.

   ![](assets/wkf_data_export11.png)

1. 외부 계정을 선택하고 서버의 폴더 경로를 입력합니다.

   ![](assets/wkf_data_export12.png)

1. 활동을 확인하고 워크플로우를 저장합니다.
1. 워크플로우를 시작합니다.

   워크플로우가 올바르게 실행되면 추출된 파일을 외부 계정에서 사용할 수 있습니다.

