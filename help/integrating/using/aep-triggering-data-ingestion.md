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
source-git-commit: 13d419c5fc51845ee14f8a3b288f4c467e0a60d9
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 6%

---

# API를 통한 데이터 수집 트리거 {#triggering-data-ingestion-apis}

>[!IMPORTANT]
>
>Adobe Experience Platform Data Connector는 현재 베타 버전으로, 예고 없이 자주 업데이트될 수 있습니다. 고객은 이러한 기능에 액세스하려면 Azure에서 호스팅(현재 북미 전용 베타 버전)해야 합니다. 액세스하려면 고객 지원 센터에 문의하십시오.

Adobe Campaign Standard을 사용하면 API를 통해 데이터 매핑을 즉시 수집하여 수집 요청의 상태를 검색할 수 있습니다.

이 페이지에서는 데이터 매핑의 수집 상태를 트리거하고 검색하는 방법을 설명합니다. Campaign Standard API에 대한 글로벌 정보는 [이 섹션](../../api/using/get-started-apis.md).

## 필수 구성 요소 {#prerequisites}

API를 사용하기 전에 데이터 매핑이 먼저 Campaign Standard 인터페이스 내에 구성 및 게시되어 있어야 합니다. 자세한 정보는 다음 섹션을 참조하십시오.

* [매핑 정의](../../integrating/using/aep-mapping-definition.md)
* [매핑 활성화](../../integrating/using/aep-mapping-activation.md)

데이터 매핑이 만들어지면 언제든지 API에서 트리거할 수 있도록 데이터 매핑의 실행을 중지해야 합니다. 이렇게 하려면 다음 단계를 수행합니다.

1. Campaign Standard에서 **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Platform]** > **[!UICONTROL Status of data export to platform]** 메뉴 아래의 제품에서 사용할 수 있습니다.

1. 데이터 매핑을 두 번 클릭하여 연 다음 **[!UICONTROL Stop]** 버튼을 클릭합니다.

   ![](assets/aep_datamapping_stop.png)

1. 변경 내용을 저장합니다

이제 데이터 매핑 실행이 중지됩니다. Campaign Standard API를 사용하여 수동으로 트리거할 수 있습니다.

## 데이터 매핑에 대한 즉각적인 수집 시작 {#starting-immediate-ingestion}

Adobe Experience Platform에 대한 XDM 매핑에 대한 즉각적인 섭취는 POST 작업을 사용하여 트리거됩니다.

`POST https://mc.adobe.io/<ORGANIZATION>/campaign/dataIngestion/xdmIngestion/<XDM Mapping ID>/ingest`

>[!NOTE]
>
>수집 POST API 호출을 실행하려면 사용자에게 **SQL 함수 실행** 역할 - Campaign Standard 관리자가 아래 JS 스크립트를 실행하여 제공할 수 있습니다.
>
>
```
>var sqlRoleObj = REST.head.roleBase.sql.get();
>REST.head.securityGroup.Administrators.roles.post(sqlRoleObj);
>```

POST 작업은 생성된 요청 상태에 대한 정보를 반환합니다.

* XDM 매핑에 대한 요청이 성공적으로 제출되었습니다.

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

* XDM 매핑이 게시되지 않았거나 중지되어 요청이 실패했습니다.

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

수집 요청의 상태는 매개 변수에 GET 작업 및 원하는 요청 ID를 사용하여 검색할 수 있습니다.

```
GET https://mc.adobe.io/<ORGANIZATION>/campaign/dataIngestion/xdmIngestion/<XDM Mapping ID>/ingest
{"requestId"="<value>"}
```

>[!NOTE]
>
>XDM 매핑 요청 상태 및 관련 작업에 대한 자세한 내용은 Campaign Standard 인터페이스에서 확인할 수 있습니다 **[!UICONTROL Status of data export to platform]** 메뉴(참조) [매핑 활성화](../../integrating/using/aep-mapping-activation.md)).

GET 작업은 아래 정보를 반환합니다.

* **batchId**: 이 필드는 일괄 준비 및 업로드 후에 오류가 발생한 경우에만 채워집니다.
* **info**: XDM 매핑 ID,
* **numRecords**: 수집된 레코드 수(성공 상태만 해당),
* **상태**: 수집 요청 상태(성공/실패/진행 중)

GET 작업에 대한 가능한 응답은 다음과 같습니다.

* 수집 요청 성공:

   ```
   {
   "batchId": "",
   "info": "Mapping Id: <value>. ",
   "numRecords": 15,
   "requestId": 3520,
   "status": "Success"
   }
   ```

* 수집된 레코드 0개로 수집 요청이 실패했습니다.

   ```
   {
   "batchId": "",
   "info": "Mapping Id: <value>. ACP-880056 Failed to fetch the record from the database.",
   "numRecords": 0,
   "requestId": 3520,
   "status": "Failed"
   }
   ```

* 일괄 처리 아래에 업로드된 일부 레코드를 사용하여 수집 요청이 실패했습니다.

   ```
   {
   "batchId": "<value>",
   "info": "Mapping Id: <value>. ACP-880096 Sync Job failed to upload. Please check the error in the Platform UI.",
   "numRecords": 0,
   "requestId": <value>,
   "status": "Failed"
   }
   ```

* 일부 레코드를 섭취한 후 수집 요청이 중단되었습니다(충돌 시나리오에서 발생할 수 있음).

   ```
   {
   "batchId": "",
   "info": "Mapping Id: <value>. Ingestion request aborted due to some issue with data ingestion service. Please submit a new request",
   "numRecords": 0,
   "requestId": <value>,
   "status": "Aborted"
   }
   ```

* 처리 중인 요청(요청이 일괄 처리로 업로드된 경우 또는 일괄 처리가 요청에 대해 준비되는 경우):

   ```
   {
   "batchId": "",
   "info": "Mapping Id: <value>.",
   "numRecords": 0,
   "requestId": <value>,
   "status": "In Progress"
   }
   ```
