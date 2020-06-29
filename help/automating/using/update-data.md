---
title: 데이터 업데이트
description: 데이터 업데이트 작업을 사용하면 데이터베이스의 필드에 대한 대량 업데이트를 수행할 수 있습니다.
page-status-flag: never-activated
uuid: 1dc55db5-affd-4688-b673-adfb8c1338b5
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: data-management-activities
discoiquuid: 4db83c95-4b75-4a16-8dbf-bd8940431fa9
context-tags: writer,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 87e0611fae0560aca276caa3c4cf793e9c095d72
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 1%

---


# 데이터 업데이트{#update-data}

## 설명 {#description}

![](assets/data_update.png)

이 **[!UICONTROL Update data]** 활동을 통해 데이터베이스의 필드에 대한 대량 업데이트를 수행할 수 있습니다.

## 사용 상황 {#context-of-use}

파일을 가져온 후 **데이터** 업데이트 작업을 사용하여 복구된 데이터를 Adobe Campaign 데이터베이스에 삽입할 수 있습니다. 데이터 업데이트를 개인화할 수 있는 몇 가지 옵션을 제공합니다.

**관련 항목:**

* [사용 사례: 파일을 기반으로 데이터 업데이트](../../automating/using/update-database-file.md)
* [자동 파일 다운로드를 기반으로 데이터 업데이트](../../automating/using/update-data-automatic-download.md)

## 구성 {#configuration}

1. 활동을 워크플로우로 드래그하여 **[!UICONTROL Update data]** 놓습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 활동을 엽니다.
1. 수행할 작업 **[!UICONTROL Operation type]** 을 지정합니다.

   * **[!UICONTROL Insert or update]**: 데이터베이스에 레코드가 이미 있는 경우 데이터를 삽입하거나 업데이트합니다.
   * **[!UICONTROL Insert only]**: 데이터 삽입만. 이미 존재하는 레코드는 업데이트되지 않습니다. 조정 기준이 정의된 경우, 대사되지 않은 레코드만 추가됩니다.

      가져온 데이터에 오류가 발생하지 않도록 데이터베이스에 이미 존재하는 특정 레코드가 포함되어 있는 **[!UICONTROL Generate an outbound transition for rejects]** 경우 이 확인란을 선택합니다.

   * **[!UICONTROL Update]**: 데이터베이스에 이미 존재하는 레코드의 데이터를 업데이트합니다.
   * **[!UICONTROL Delete]**: 데이터 삭제
   >[!NOTE]
   >
   >이 필드를 **[!UICONTROL Batch size]** 사용하면 데이터를 업로드할 최대 배치 크기를 정의할 수 있습니다.

1. 탭에서 데이터베이스의 레코드를 식별하는 방법을 **[!UICONTROL Identification]** 지정합니다.

   * **[!UICONTROL Using the targeting dimension]**: 을 선택한 **[!UICONTROL Dimension to update]** 다음 을 지정합니다 **[!UICONTROL Keys for finding records]**. 자세한 내용은 [타깃팅 차원 및 리소스를 참조하십시오](../../automating/using/query.md#targeting-dimensions-and-resources).
   * 입력한 데이터가 기존 타깃팅 차원과 일치하는 경우 옵션을 **[!UICONTROL Using one or more links]** 선택합니다. 그런 다음 를 선택합니다 **[!UICONTROL Dimension to update]**.
   선택한 작업 유형에 업데이트가 필요한 경우 조정 키를 사용해야 합니다.

1. 탭에서 업데이트를 적용할 필드를 **[!UICONTROL Fields to update]** 지정하고 필요한 경우 이 업데이트가 수행되도록 조건을 추가합니다. 이렇게 하려면 열을 **[!UICONTROL Taken into account if]** 사용합니다. 조건이 목록 순서대로 적용됩니다. 오른쪽의 화살표를 사용하여 업데이트 순서를 변경합니다. 동일한 대상 필드를 여러 번 사용할 수 있습니다.

   단추를 사용하여 필드를 자동으로 연결할 수 ![](assets/wkf_magic_wand-24px.png) 있습니다. 자동 연결은 이름이 같은 필드를 검색합니다.

   유형 작업 동안 각 필드에 적용할 작업을 개별적으로 선택할 수 **[!UICONTROL Insert or update]** 있습니다. 이렇게 하려면 열에서 원하는 값을 **[!UICONTROL Operation]** 선택합니다.

   >[!NOTE]
   >
   >**업데이트** 관리 **[!UICONTROL lastModified]**, **[!UICONTROL modifiedBy]**&#x200B;및 필드 **[!UICONTROL created]** **[!UICONTROL createdBy]** 는 업데이트 데이터 활동이 실행될 때 필드 업데이트 테이블에서 해당 구성을 명시적으로 수행하지 않는 한 자동으로 업데이트됩니다. 이 업데이트는 적어도 하나의 차이가 감지된 레코드에서만 수행됩니다. 값이 동일하면 업데이트가 수행되지 않습니다.

1. 필요한 경우 활동의 전환 [을](../../automating/using/activity-properties.md) 관리하여 아웃바운드 모형에 대한 고급 옵션에 액세스합니다.

   선택한 데이터 **[!UICONTROL Insert only]** 가 데이터베이스에 이미 있는 레코드를 포함할 수 있는 경우, 발생 가능한 오류를 방지하려면 **[!UICONTROL Generate an outbound transition for the rejects]** 확인란을 선택하십시오.

1. 활동 구성을 확인하고 워크플로우를 저장합니다.
