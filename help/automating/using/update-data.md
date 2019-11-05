---
title: 데이터 업데이트
description: 데이터 업데이트 작업을 사용하면 데이터베이스의 필드에 대한 대량 업데이트를 수행할 수 있습니다.
page-status-flag: 활성화 안 함
uuid: 1dc55db5-affd-4688-b673-adfb8c1338b5
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 자동화
content-type: reference
topic-tags: 데이터 관리 활동
discoiquuid: 4db83c95-4b75-4a16-8dbf-bd8940431fa9
context-tags: 작성자,기본
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 데이터 업데이트{#update-data}

## 설명 {#description}

![](assets/data_update.png)

이 **[!UICONTROL Update data]** 활동을 통해 데이터베이스의 필드에 대한 대량 업데이트를 수행할 수 있습니다.

## 사용 상황 {#context-of-use}

파일 **가져오기 후 Adobe Campaign 데이터베이스에 복구된 데이터를 삽입하기 위해 데이터** 업데이트 활동을 사용할 수 있습니다. 몇 가지 옵션을 사용하여 데이터 업데이트를 개인화할 수 있습니다.

## 구성 {#configuration}

1. 워크플로우를 워크플로우로 드래그하여 **[!UICONTROL Update data]** 놓을 수 있습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 엽니다.
1. 수행할 **[!UICONTROL Operation type]** 작업을 지정합니다.

   * **[!UICONTROL Insert or update]**:데이터베이스에 레코드가 이미 있으면 데이터를 삽입하거나 업데이트합니다.
   * **[!UICONTROL Insert only]**:삽입에만 사용할 수 있습니다. 이미 존재하는 레코드는 업데이트되지 않습니다. 조정 기준이 정의된 경우, 대사되지 않은 레코드만 추가됩니다.

      가져온 데이터에 가능한 오류가 발생하지 않도록 데이터베이스에 이미 존재하는 특정 레코드가 포함되어 있는 **[!UICONTROL Generate an outbound transition for rejects]** 경우 이 확인란을 선택합니다.

   * **[!UICONTROL Update]**:데이터베이스에 이미 존재하는 레코드의 데이터를 업데이트합니다.
   * **[!UICONTROL Delete]**:데이터를 삭제합니다.
   >[!NOTE]
   >
   >이 **[!UICONTROL Batch size]** 필드를 사용하면 업로드할 데이터의 최대 배치 크기를 정의할 수 있습니다.

1. 탭에서 데이터베이스의 레코드를 식별하는 방법을 지정합니다. **[!UICONTROL Identification]**

   * **[!UICONTROL Using the targeting dimension]**:을 **[!UICONTROL Dimension to update]** 선택한 다음 **[!UICONTROL Keys for finding records]**&#x200B;을 지정합니다. 자세한 내용은 타깃팅 [차원 및 리소스를](../../automating/using/query.md#targeting-dimensions-and-resources)참조하십시오.
   * 입력한 데이터가 기존 타깃팅 차원과 일치하는 경우 **[!UICONTROL Using one or more links]** 옵션을 선택합니다. 그런 다음 를 **[!UICONTROL Dimension to update]**&#x200B;선택합니다.
   선택한 작업 유형에 업데이트가 필요한 경우 조정 키를 사용해야 합니다.

1. 탭에서 업데이트를 적용할 필드를 지정하고 필요한 경우 조건을 추가하여 이 업데이트가 수행되도록 합니다. **[!UICONTROL Fields to update]** 이렇게 하려면 **[!UICONTROL Taken into account if]** 열을 사용합니다. 조건이 목록 순서에서 차례로 적용됩니다. 오른쪽의 화살표를 사용하여 업데이트 순서를 변경합니다. 동일한 대상 필드를 여러 번 사용할 수 있습니다.

   단추를 사용하여 필드를 자동으로 연결할 수 ![](assets/wkf_magic_wand-24px.png) 있습니다. 자동 연결은 동일한 이름의 필드를 감지합니다.

   유형 작업 동안 각 필드에 적용할 작업을 개별적으로 선택할 수 있습니다. **[!UICONTROL Insert or update]** 이렇게 하려면 **[!UICONTROL Operation]** 열에서 원하는 값을 선택합니다.

   >[!NOTE]
   >
   >**업데이트** 관리 **[!UICONTROL lastModified]**, **[!UICONTROL modifiedBy]**&#x200B;데이터 업데이트 활동이 실행될 때 필드 업데이트 테이블에서 해당 구성이 명시적으로 수행되지 않는 한, **[!UICONTROL created]****[!UICONTROL createdBy]** , 및 필드는 자동으로 업데이트됩니다. 업데이트는 하나 이상의 차이가 감지된 레코드에서만 수행됩니다. 값이 동일하면 업데이트가 수행되지 않습니다.

1. 필요한 경우 활동의 전환을 관리하여 [아웃바운드](../../automating/using/executing-a-workflow.md#managing-an-activity-s-outbound-transitions) 모형에 대한 고급 옵션에 액세스합니다.

   이 옵션을 선택한 **[!UICONTROL Insert only]** 경우 가져온 데이터에 데이터베이스에 이미 있는 레코드가 포함될 수 있는 경우 **[!UICONTROL Generate an outbound transition for the rejects]** 이 확인란을 선택하여 오류가 발생하지 않도록 하십시오.

1. 활동 구성을 확인하고 워크플로우를 저장합니다.

## 예 {#example}

다음 활동은 **[!UICONTROL Update data]** 활동 이후 **[!UICONTROL Load file]** 활동의 구성을 보여줍니다. 이 워크플로우의 목적은 파일에서 복구된 데이터로 Adobe Campaign 데이터베이스에 프로필을 추가하거나 업데이트하는 것입니다. 사용된 조정 키는 이메일 주소입니다.

로드된 파일은 다음 예제 데이터를 포함하는 **.txt** 형식 파일입니다.

```
lastname;firstname;email;birthdate
jackman;megan;megan.jackman@testmail.com;07/08/1975
phillips;edward;phillips@testmail.com;09/03/1986
weaver;justin;justin_w@testmail.com;11/15/1990
martin;babeth;babeth_martin@testmail.net;11/25/1964
reese;richard;rreese@testmail.com;02/08/1987
cage;nathalie;cage.nathalie227@testmail.com;07/03/1989
xiuxiu;andrea;andrea.xiuxiu@testmail.com;09/12/1992
grimes;daryl;daryl_890@testmail.com;12/06/1979
tycoon;tyreese;tyreese_t@testmail.net;10/08/1971
```

활동은 다음과 같이 구성됩니다. **[!UICONTROL Update data]**

![](assets/deduplication_example2_writer1.png)

![](assets/deduplication_example2_writer2.png)

