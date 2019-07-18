---
title: 데이터 업데이트
seo-title: 데이터 업데이트
description: 데이터 업데이트
seo-description: 데이터 업데이트 기능을 사용하면 데이터베이스의 필드에 대한 대량 업데이트를 수행할 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 1 dc 55 db 5-affd -4688-b 673-adfb 8 c 1338 b 5
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 데이터 관리 활동
discoiquuid: 4 DB 83 C 95-4 B 75-4 A 16-8 DBF-BD 8940431 FA 9
context-tags: writer, main
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 0454dac1a7976c1be2838c2a846d33e77e60c3b3

---


# Update data{#update-data}

## Description {#description}

![](assets/data_update.png)

**[!UICONTROL Update data]** 활동을 통해 데이터베이스의 필드에 대해 대량 업데이트를 수행할 수 있습니다.

## Context of use {#context-of-use}

The **Update data** activity can be used after importing a file in order to insert the data recovered into the Adobe Campaign database. 여러 옵션을 사용하여 데이터 업데이트를 개인화할 수 있습니다.

## Configuration {#configuration}

1. **[!UICONTROL Update data]** 워크플로우를 워크플로우로 드래그하여 놓습니다.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. Specify the **[!UICONTROL Operation type]** to be carried out:

   * **[!UICONTROL Insert or update]**: 데이터가 이미 데이터베이스에 있는 경우 데이터를 삽입하거나 업데이트합니다.
   * **[!UICONTROL Insert only]**: 데이터만 삽입. 이미 존재하는 레코드는 업데이트되지 않습니다. 조정 기준을 정의하면 중재되지 않은 레코드만 추가됩니다.

      Check the **[!UICONTROL Generate an outbound transition for rejects]** box if the data imported contains certain records that already exist in the database to avoid any possible errors.

   * **[!UICONTROL Update]**: 데이터베이스에 이미 존재하는 레코드만 업데이트합니다.
   * **[!UICONTROL Delete]**: 데이터 삭제.
   >[!NOTE]
   >
   >**[!UICONTROL Batch size]** 이 필드에서 업로드할 데이터의 최대 일괄 처리 크기를 정의할 수 있습니다.

1. **[!UICONTROL Identification]** 탭에서 데이터베이스에서 레코드를 식별하는 방법을 지정합니다.

   * **[!UICONTROL Using the targeting dimension]**: 을 선택하고 **[!UICONTROL Dimension to update]****[!UICONTROL Keys for finding records]**&#x200B;를 지정합니다. For more this, refer to [Targeting dimensions and resources](../../automating/using/query.md#targeting-dimensions-and-resources).
   * If the data entered matches an existing targeting dimension, select the **[!UICONTROL Using one or more links]** option. **[!UICONTROL Dimension to update]**&#x200B;그런 다음을 선택합니다.
   선택한 작업 유형에 업데이트가 필요한 경우 조정 키를 사용해야 합니다.

1. **[!UICONTROL Fields to update]** 탭에서 업데이트가 적용될 필드를 지정하고 필요한 경우 조건을 추가하여 이 업데이트가 수행되도록 합니다. To do this, use the **[!UICONTROL Taken into account if]** column. 조건이 목록 순서대로 적용됩니다. 오른쪽의 화살표를 사용하여 업데이트 순서를 변경합니다. 동일한 대상 필드를 여러 번 사용할 수 있습니다.

   You can automatically link fields using the ![](assets/wkf_magic_wand-24px.png) button. 자동 연결은 이름이 같은 필드를 감지합니다.

   **[!UICONTROL Insert or update]** 유형 작업 중에 각 필드에 적용할 작업을 개별적으로 선택할 수 있습니다. To do this, select the value you would like in the **[!UICONTROL Operation]** column.

   >[!NOTE]
   >
   >**업데이트를** **[!UICONTROL lastModified]**&#x200B;관리하는 작업은 **[!UICONTROL modifiedBy]****[!UICONTROL created]****[!UICONTROL createdBy]** 필드 업데이트 테이블에서 해당 구성이 명시적으로 수행되지 않는 한 업데이트 데이터 활동이 실행될 때 자동으로 업데이트됩니다. 업데이트는 하나 이상의 차이가 감지된 레코드에서만 수행됩니다. 값이 동일하면 업데이트가 수행되지 않습니다.

1. If needed, manage the activity's [Transitions](../../automating/using/executing-a-workflow.md#managing-an-activity-s-outbound-transitions) to access the advanced options for the outbound population.

   If you have selected **[!UICONTROL Insert only]** and the data imported may contain records that are already present in the database, check the **[!UICONTROL Generate an outbound transition for the rejects]** box to avoid any possible errors.

1. 활동의 구성을 확인하고 워크플로우를 저장합니다.

## Example {#example}

The following activity shows the configuration of an **[!UICONTROL Update data]** activity following a **[!UICONTROL Load file]** activity. 이 워크플로의 목표는 파일에서 복구된 데이터로 Adobe Campaign 데이터베이스에 프로필을 추가하거나 업데이트하는 것입니다. 사용된 조정 키는 이메일 주소입니다.

The file loaded is a **.txt** format file containing the following example data:

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

**[!UICONTROL Update data]** 활동은 다음과 같이 구성됩니다.

![](assets/deduplication_example2_writer1.png)

![](assets/deduplication_example2_writer2.png)

