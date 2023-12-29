---
title: API를 통한 데이터 수집 트리거
description: API를 통해 데이터 수집을 트리거하는 방법을 알아봅니다.
audience: administration
content-type: reference
topic-tags: configuring-channels
feature: Microsoft CRM Integration
role: Data Architect
level: Experienced
exl-id: d67a796a-0730-4502-802c-d0b3583dd1dc
hide: true
hidefromtoc: true
source-git-commit: 110f3ccb5865e70c78e18485b4ff4ba7a648af3f
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 6%

---

# API를 통한 데이터 수집 트리거 {#triggering-data-ingestion-apis}

>[!IMPORTANT]
>
>Adobe Experience Platform Data Connector는 현재 베타 버전이며 예고 없이 자주 업데이트될 수 있습니다. 이러한 기능에 액세스하려면 고객을 Azure(현재 북미 지역의 경우에만 베타 버전)에서 호스팅해야 합니다. 액세스하려면 Adobe 고객 지원 센터에 문의하십시오.

Adobe Campaign Standard을 사용하면 API를 통해 데이터 매핑의 즉각적인 수집을 트리거하고 수집 요청의 상태를 검색할 수 있습니다.

이 페이지에서는 데이터 매핑의 수집 상태를 트리거하고 검색하는 방법에 대해 설명합니다. Campaign Standard API에 대한 전역 정보는 다음을 참조하십시오. [이 섹션](../../api/using/get-started-apis.md).

## 필수 구성 요소 {#prerequisites}

API를 사용하기 전에 데이터 매핑이 먼저 구성되어 Campaign Standard 인터페이스 내에 게시되어야 합니다. 자세한 정보는 다음 섹션을 참조하십시오.

* [매핑 정의](../../integrating/using/aep-mapping-definition.md)
* [매핑 활성화](../../integrating/using/aep-mapping-activation.md)

데이터 매핑이 만들어지면 언제든지 API에서 트리거할 수 있도록 실행을 중지해야 합니다. 이렇게 하려면 다음 단계를 수행합니다.

1. Campaign Standard에서 **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Platform]** > **[!UICONTROL Status of data export to platform]** 메뉴 아래의 제품에서 사용할 수 있습니다.

1. 데이터 매핑을 두 번 클릭하여 연 다음 **[!UICONTROL Stop]** 단추를 클릭합니다.

   ![](assets/aep_datamapping_stop.png)

1. 변경 사항 저장

이제 데이터 매핑 실행이 중지되었습니다. Campaign Standard API를 사용하여 수동으로 트리거할 수 있습니다.

## 데이터 매핑의 즉각적인 수집 시작 {#starting-immediate-ingestion}

Adobe Experience Platform에 대한 XDM 매핑의 즉각적인 섭취는 POST 작업으로 트리거됩니다.

`POST https://mc.adobe.io/<ORGANIZATION>/campaign/dataIngestion/xdmIngestion/<XDM Mapping ID>/ingest`

>[!NOTE]
>
>수집 POST API 호출을 실행하려면 사용자에게 다음이 있어야 합니다 **SQL 함수 실행** Campaign Standard 관리자 가 JS 스크립트 아래에서 실행하여 제공할 수 있는 역할:
>
>```
>var sqlRoleObj = REST.head.roleBase.sql.get();
>REST.head.securityGroup.Administrators.roles.post(sqlRoleObj);
>```
>

POST 작업이 생성된 요청 상태에 대한 정보를 반환합니다.

* XDM 매핑에 대한 요청이 제출되었습니다.

```
{
"requestId": <value>,
"info": "Ingestion request submitted successfully for the Mapping ID: <value>",
"status":"Success"
}
```

* XDM 매핑에 대한 요청이 이미 진행 중입니다.

```
{
"requestId": <value>,
"info": "Ingestion request already in progress for the Mapping ID: <value>",
"status":"In Progress"
}
```

* XDM 매핑이 게시되지 않았거나 중지되었기 때문에 요청에 실패했습니다.

```
{
"info": "Unable to submit data ingestion request, XDM Mapping ID: <value> is not stopped",
"status": "Failed"
}
{
"info": "Unable to submit data ingestion request, XDM Mapping ID: <value> is not published",
"status": "Failed"
}
```

## 수집 요청 상태 검색 {#retrieving-status}

수집 요청의 상태는 GET 작업과 매개 변수의 원하는 요청 ID를 통해 검색할 수 있습니다.

```
GET https://mc.adobe.io/<ORGANIZATION>/campaign/dataIngestion/xdmIngestion/<XDM Mapping ID>/ingest
{"requestId"="<value>"}
```

>[!NOTE]
>
>XDM 매핑 요청 상태 및 관련 작업에 대한 자세한 내용은 Campaign Standard 인터페이스의 **[!UICONTROL Status of data export to platform]** 메뉴(참조) [매핑 활성화](../../integrating/using/aep-mapping-activation.md)).

GET 작업이 아래 정보를 반환합니다.

* **batchId**: 이 필드는 일괄 처리 준비 및 업로드 후 오류가 발생한 경우에만 채워집니다.
* **정보**: XDM 매핑 ID,
* **numRecords**: 수집된 레코드 수(성공 상태만 해당),
* **상태**: 요청 수집 상태(성공/실패/진행 중)

GET 작업에 대해 가능한 응답은 다음과 같습니다.

* 요청 수집 성공:

  ```
  {
  "batchId": "",
  "info": "Mapping Id: <value>. ",
  "numRecords": 15,
  "requestId": 3520,
  "status": "Success"
  }
  ```

* 0개의 레코드가 수집되어 수집 요청 실패:

  ```
  {
  "batchId": "",
  "info": "Mapping Id: <value>. ACP-880056 Failed to fetch the record from the database.",
  "numRecords": 0,
  "requestId": 3520,
  "status": "Failed"
  }
  ```

* 일부 레코드가 일괄 처리 아래에 업로드되어 수집 요청에 실패했습니다.

  ```
  {
  "batchId": "<value>",
  "info": "Mapping Id: <value>. ACP-880096 Sync Job failed to upload. Please check the error in the Platform UI.",
  "numRecords": 0,
  "requestId": <value>,
  "status": "Failed"
  }
  ```

* 일부 레코드를 수집한 후 수집 요청이 중단됨(충돌 시나리오에서 발생할 수 있음):

  ```
  {
  "batchId": "",
  "info": "Mapping Id: <value>. Ingestion request aborted due to some issue with data ingestion service. Please submit a new request",
  "numRecords": 0,
  "requestId": <value>,
  "status": "Aborted"
  }
  ```

* 수집 요청 진행 중(요청이 데이터를 일괄 업로드하거나 요청에 대한 일괄 처리를 준비하는 경우):

  ```
  {
  "batchId": "",
  "info": "Mapping Id: <value>.",
  "numRecords": 0,
  "requestId": <value>,
  "status": "In Progress"
  }
  ```
